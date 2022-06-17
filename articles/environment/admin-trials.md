---
title: Registrera dig för utvärderingsversioner av Project Operations
description: Den här artikeln innehåller information om hur du distribuerar en testversion av Dynamics 365 Project Operations.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 7db7ea6b3cffe6eb43ee0519bbaccfc9092c9311
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959534"
---
# <a name="sign-up-for-project-operations-trials"></a>Registrera dig för utvärderingsversioner av Project Operations 

_**Gäller till:** Project Operations för resurs-/icke-lagerbaserade scenarier, Lite-distribution - avtal till proforma-fakturering och Project Operations för lagerbaserade/produktionsbaserade scenarier_ 



Den här artikeln förklarar hur du prenumererar på förhandsgranskning partnererbjudandet och implementerar en Dynamics 365 Project Operations miljö.

Med den nya utvärderingsversionen av Project Operations kan du automatiskt distribuera samtliga de tre distributionsscenarier som stöds genom att fylla i en enkät som rekommenderar bästa distributionsmetod. Den här artikeln innehåller information om hur du:

- Löser in ditt utvärderingserbjudande.
- Påbörja etablering.
- Konfigurera dubbelriktad skrivning.
- Läs mer om Project Operations. 

I följande tabell beskrivs detaljerad information om det nya utvärderingserbjudandet.

| **Erbjudandeobjekt**               | **Detaljer**                                  |
|------------------------------|----------------------------------------------|
| Erbjudandetyp                   | Denna erbjudandetyp är admin-lead, varför en administratör för en klientorganisation krävs för inlösen. |
| Användning av erbjudande                    | En gång per klientorganisation                          |
| Erbjudandets varaktighet               | 30 kalenderdagar                             |
| Antal inlösen per klientorganisation       | 1                                            |
| Anknytning                    | 1 tillägg, 30 kalenderdagar               |
| Antal utvärderingsmiljöer | 3                                            |


## <a name="admin-trial-details"></a>Utvärderingsinformation för administratör
I följande tabell visas utvärderingsinformationen och hur denna tillämpas på respektive distributionstyp.

| **Artikel**                      | **Lite**                                     | **Ej lagerförda material** | **Lagerförda material** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Tillhandahållna installationsdata           | Ja                                          | Ja                       | Ja (USSI)            |
| Transaktionsdata            | Inga                                           | Inga                        | Inga                    |
| Etableringstid i minuter  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Förutsättningar
Följande förutsättningar krävs för att distribuera en utvärderingsversion av Dynamics 365 Project Operations.

- Registrera dig för [Dynamics 365 Project Operations – Utvärderingsversion](https://www.aka.ms/try-po).
- Den användare som distribuerar förhandsversionen måste ha behörighet som global administratör av Azure-klient.

> [!IMPORTANT]
> Endast en person inom en organisation – klientorganisationens administratör – behöver utföra den här uppgiften. Om du inte är prenumerant på den här versionen väntar du tills din organisation har registrerats och du har fått dina användarautentiseringsuppgifter.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations – Utvärderingsversion 

Innan du börjar loggar du in i en webbläsare med användarkontot i den klientorganisation där du vill förhandsgranska Project Operations.

1. Lös in den första erbjudandekoden, **Dynamics 365 Project Operations – Utvärderingsversion** genom att klistra in den i webbläsarens webbadressfält.

    ![Hämta erbjudande](./media/16RedeemFirstOfferNew.png)

2. Bekräfta order.

    ![Bekräfta order](./media/17ConfirmOrderNew.png)

  Du ser då att bekräftelseerbjudandet har lösts in.

   ![Bekräftelse](./media/18OrderConfirmationNew.png)

  Du omdirigeras till [administratörscentret för Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Enkät och etablering

1.  Gå till [administratörscentret för Power Platform](https://admin.powerplatform.com/projectoperationstrial) och fyll i enkäten.  
2.  Granska den rekommenderade distributionstypen och välj **Starta installationsprogrammet** för att starta etableringen.
3.  Granska villkoren och markera sedan **Start**.

   När etableringen har startat omdirigeras du till miljölistan i administrationscentret för Power Platform. Medan etablering pågår är statusen för din miljö **PreparingInstance**.
 
  När etableringen är klar är tillståndet för miljön **klar**. Etablering av miljön omfattar distribution av demodata.
 
4.  Välj respektive Microsoft Dataverse-URL och de URL:er för appar för ekonomi och drift som ska verifiera distributionen.

## <a name="configuring-dual-write"></a>Konfigurera dubbelriktad skrivning
- Information om hur du konfigurerar säkerhetsroller för dubbelriktad skrivning finns i [Uppdatera säkerhetsinställningar för Project Operations i Dataverse](resource-provision-new-environment.md#update-security-settings-on-project-operations-on-dataverse).
- För att få åtkomst till dubbelskrivningskonfiguration, navigera till Drift och ekonomi-instansen och navigera sedan till **Datahantering** > **Dubbelskrivning**.
- Information om hur du konfigurerar mappningar för dubbelriktad skrivning finns i [Köra Project Operations-mappningar för dubbelriktad skrivning](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Tilldela licenser

Du måste ha administratörsbehörighet till organisationens Microsoft 365-portal för att kunna utföra följande steg.

1. Gå till [administrationscentret för Microsoft 365](https://portal.office.com/) om du vill tilldela licenserna till användarna.

   ![Startsida för administratörscenter](./media/14AdminPortal.png)

2. På sidan **Aktiva användare** väljer du de användare som du vill tilldela en licens till.

   ![Tilldela licenser](./media/15AssignLicenses.png)

3. Bekräfta att livensen för **Dynamics 365 Project Operations-förhandsversion** har valts, och välj sedan **Spara ändringar**.

## <a name="additional-resources"></a>Ytterligare resurser

Följande resurser vägleder dig när du inleder din resa med Project Operations:

- [Videoserie – Översikt över Project Operations, djupdykningar ner i de olika funktionerna samt en översikt](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Fastställ din distributionstyp](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Vanliga frågor och svar

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Vad gör jag om jag behöver ALM eller ELM för min appmiljö för ekonomi och drift?

- För partners som behöver fullständiga funktioner för hantering av miljöns livscykel går du till [Licensbegäran för sandbox-miljö för partner](https://experience.dynamics.com/requestlicense) om du vill granska det nya partnererbjudandet. 
- För partners som vill ha mer information om interna användningsrättigheter, se [Interna användningsrättigheter: moln- och programvaruförmåner (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Kan jag förlänga min utvärderingsversionen efter 30 dagar?
Slutför följande steg om du vill förlänga utvärderingsversionen.

1. I **Administratörscentret för Microsoft 365** går du till **Fakturering** > **Dina produkter**.
2. Välj **Dynamics 365 Project Operations (CE) - Förhandsversion**.
3. Under **Utgångsdatum** väljer du **Förläng datum**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Kan jag uppgradera från lite-distributionen till den resurs-/icke-lagerbaserade scenariodistributionen?
För tillfället finns det inget stöd för att uppgradera en miljö från en lite-installation till en icke-lagrad distribution.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Kan jag få tillgång till Lifecycle Services (LCS) för mina Finance-miljöer?  
Nr. Distributionen för dessa utvärderingsversioner hanteras via administrationscentret för Power Platform. Åtkomsten till Finance-miljön är begränsad.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Kan jag installera min utvärderingsversion i en befintlig miljö?
Om det finns en befintlig miljö kan du installera lite-distributionen i en befintlig Dataverse-försäljningsmiljö från administrationscentret för Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
