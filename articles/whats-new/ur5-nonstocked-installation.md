---
title: Uppdatera Project Operations i din Finance-miljö
description: I detta ämne finns information om hur du uppdaterar Project Operations i din Dynamics 365 Finance-miljö.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5292001"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Uppdatera Project Operations i din Finance-miljö

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_


I detta ämne finns information om hur du uppdaterar Dynamics 365 Project Operations i din Dynamics 365 Finance-miljö. Det krävs tre procedurer för att uppdatera Project Operations till Uppdatering 5 (UR5):

- [Importera paketet till förhandsgranskningsprojektet](#import)
- [Applicera uppdateringen](#apply)
- [Uppdatera din Dataverse-miljö](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importera paketet till ditt LCS-projekt

1. Logga in på [Lifecycle Services (LCS)](https://lcs.dynamics.com/) som projektägare eller miljöansvarig.
2. Välj ditt LCS-projekt i listan över projekt.
3. På sidan **Projekt**, i gruppen **Miljöer**, öppnar du den miljö som du vill uppdatera.
4. Kontrollera att miljön körs. Starta miljön om den inte redan körs.
5. I avsnittet **Ny version**, under **Tillgängliga uppdateringar**, väljer du **Visa uppdatering** för 10.0.15.

![Visa uppdateringsknappen](media/view-update.png)

6. På sidan **Binära uppdateringar** väljer du **Spara paket**.
7. På sidan **Granska och spara uppdateringar** väljer du **Spara paket**.
8. I fönstret **Spara paket i tillgångsbibliotek** som visas anger du paketets namn och väljer sedan **Spara paket**.
9. När LCS har slutat spara paketet aktiveras knappen **Klar**. Välj **Utfört**. LCS verifierar paketet. Verifieringen kan ta allt mellan några minuter och upp till en timme.


## <a name="apply-the-package-update"></a><a name="apply"></a>Verkställ paketuppdateringen

1. På sidan **Miljöinformation** i LCs väljer du **Underhåll** > **Verkställ uppdateringar**.
2. Välj det paket du sparade tidigare i listan och välj Sedan **Verkställ**.
3. Markera **Ja** om du vill bekräfta att du vill distribuera paketet.

![Dialogrutan Bekräfta paketdistribution](media/confirm-package-deployment.png)

4. Markera **Ja** om du vill bekräfta att du vill uppdatera programmet.

![Dialogrutan Bekräfta programuppdatering](media/confirm-application-update.png)

Distributionen och programuppdateringen startar. 

På sidan **Miljöinformation** uppdateras miljöstatusen till **Underhåll** i det övre högra hörnet. Uppdateringen kommer att slutföras på cirka två timmar. Programmets versionsinformation uppdateras till **Microsoft Dynamics 365 for Finance and Operations 10.0.15** och miljöstatusen uppdateras till **Distribuerad**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Uppdatera din Dataverse-miljö

1. Logga in på [Power Platform administratörscenter](https://admin.powerplatform.com/).
2. Leta upp och öppna den miljö du använde för att installera Project Operations i listan.
3. På sidan **Miljöer** väljer du **Resurs** > **Dynamics 365-appar**.
4. Leta upp **Microsoft Dynamics 365 Project Operations** i listan. I kolumnen **Status** väljer du **Uppdatering finns**.
5. Markera kryssrutan **Jag godkänner användarvillkoren** och välj sedan **Uppdatera**. Den senaste versionen av lösningen installeras.

När installationen är färdig har du version 4.5.0.134 installerad.

## <a name="configure-new-features"></a>Konfigurera nya funktioner

### <a name="enable-dual-write-mapping"></a>Aktivera mappning för dubbelskrivning

När du har slutfört uppdateringen för Finance- och Dataverse-miljöer kan du aktivera de nödvändiga mappningarna för dubbelskrivning. Slutför följande procedurer för att aktivera mappningar för dubbelskrivning:

- [Uppdatera säkerhetsinställningar i Customer Engagement-miljön](#security)
- [Uppdatera dataentiteter](#refresh)
- [Uppdatera och kör mappningarna för dubbel skrivning](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Uppdatera säkerhetsinställningar i Dataverse-miljön

Följande uppdateringar av säkerhetsprivilegier för entiteter krävs som en del av uppdateringen till UR5.

1. I din Dataverse-miljö går du till **Inställningar**. I gruppen **System** väljer du **Säkerhet**.

![Inställningar för Dataverse-miljö](media/Picture21.png)

2. Välj **säkerhetsroller**
3. I listan över roller väljer du **Användare av appar för dubbelriktad skrivning** och sedan fliken **Anpassade entiteter**. 
4. Kontrollera att rollen har behörigheterna **Läs** och **Lägg till i** för:

      - **Växelkurstyp för valuta**
      - **Kontolista** 
      - **Kalender för räkenskapsår** 
      - **Transaktionsregister**

5. När säkerhetsrollen uppdateras går du till **Inställningar** > **Säkerhet** > **Teams**. Kontrollera att rollen **Användare av appar för dubbelriktad skrivning** har tillämpats på teamet. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Uppdatera dataentiteter från uppdateringen

1. Öppna arbetsytan **Datahantering** i Finance-miljön, och öppna sedan sidan **Ramverksparametrar**.
2. I fliken **Entitetsinställningar** väljer du **Uppdatera entitetslista**.
3. Bekräfta entitetsuppdateringen genom att välja **Stäng**.

 > [!NOTE]
 > Processen tar cirka 20 minuter att genomföra. Du meddelas när uppdateringen har slutförts.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Uppdatera mappningar för dubbelskrivning

1. I arbetsytan **Datahantering** väljer du **Dubbel skrivning**.
2. Välj **Tillämpa lösningar**, markera båda lösningarna i listan och välj Sedan **Bekräfta**.
3. På sidan **Dubbelskrivning** markerar du följande tabellmappningar och väljer sedan **Stoppa**.

    - **Faktiska värden för Project Operations-integrering (msdyn_actuals)**
    - **Utgiftskategorier för integreringsprojekt för Project Operations (msdyn_expensecategories)**
    - **Exportentitet för faktiska projektutgifter för Project Operations-integrering (msdyn_expensecategories)**

4. På sidan **Tabellmappningsversion** tillämpar du en ny version av mappningen på respektive av de tre entiteterna.
5. På sidan **Dubbelriktad skrivning** väljer du Kör för att starta om mappningarna.
6. I mappningslistan väljer du mappningen **Huvudbok (msdyn_ledgers)** med alla obligatoriska delar och väljer sedan kryssrutan **Initial synkc**. 
7. I fältet **Master för initial synk** väljer du **Finance and Operations-appar** och sedan **Kör**.
 
 ![Synkronisering av huvudboksmappning](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]