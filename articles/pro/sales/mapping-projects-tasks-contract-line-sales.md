---
title: Mappa projekt och uppgifter till en projektbaserad kontraktrad - lite
description: I det här ämnet finns information om hur du lägger till och tar bort projekt och uppgifter på en kontraktrad.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4737f9870904bfc7adac11b8e2aa13bb8c610ca3
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858129"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Mappa projekt och uppgifter till en projektbaserad kontraktrad 

_**Gäller:** Lite-distribution - avtal för proforma-fakturering, Project Operations för resursscenarier/icke lagerbaserade scenarier_

På projektbaserade kontraktrader kan du mappa specifika uppgifter i ett projekt till kontraktraden.

När du mappar specifika uppgifter till en kontraktrad gäller faktureringsmetod, kostnadsfria alternativ, undre gränser och de kunder som definieras på kontraktraden gäller endast för dessa specifika uppgifter.

Om du har ett scenario där en fas i ett projekt, t.ex. prototypfasen, är fast pris och alla andra faser är tid och material, kan du associera prototypfasen och alla associerade underordnade uppgifter till kontraktraden för den fasen med en fast prisfaktureringsmetod.

Alla andra faser i projektets uppdelade arbetsstruktur (WBS) kan kopplas till den tid- och materialbaserade kontraktraden.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Associera uppgifter till projektbaserade kontraktrader

Uppgifter kan kopplas till kontraktrader från fliken **Debiterbara uppgifter** på sidan **kontraktrad** eller från fliken **Uppgiftsfakturering** på sidan **Projekt**.

### <a name="from-the-contract-line-page"></a>Från sidan Kontraktrad

Följ stegen nedan om du vill koppla projektuppgifter till kontraktraden från fliken **Debiterbara uppgifter** på sidan **Kontraktrad**.

1. På fliken **Allmänt** på en projektbaserad kontraktsrad, kontrollera att fältet **Projekt** är ifyllt.
2. I fältet **Inkluderade uppgifter** välj **Endast valda uppgifter**.
3. Spara dina ändringar. Formuläret uppdateras och fliken **Debiterbara uppgifter** visas.
4. Välj fliken **Debiterbara uppgifter** och välj **Lägg till en kontraktradens uppgift**.
5. På sidan **kontraktradens uppgift** i listrutan **uppgifter** väljer du uppgiften. 
6. Ange information i fältet **Faktureringstyp** och välj sedan **Spara och stäng**. Den valda uppgiften är kopplad till kontraktraden.

> [!NOTE]
> Detta är inte den optimala upplevelsen för att associera projektuppgifter med kontraktrader. Varje projekt måste associeras manuellt i det här arbetet. Det bästa sättet är att gå till fliken **Uppgiftsfakturering** på sidan **Projekt**.

### <a name="from-the-project-page"></a>Från sidan Projekt

Det här är den bästa metoden för att koppla uppgifter till kontraktrader. Du kan markera flera uppgifter och associera alla och deras underordnade uppgifter med den valda kontraktraden. Följ stegen nedan om du vill koppla uppgifter till kontraktraden från sidan **projekt**.

1. På fliken **Allmänt** på en projektbaserad kontraktsrad, kontrollera att fältet **Projekt** är ifyllt.
2. I fältet **Inkluderade uppgifter** välj **Endast valda uppgifter**.
3. Spara den projektbaserade kontraktraden. Formuläret uppdateras och fliken **Debiterbara uppgifter** visas. Detta är bara avsett som verifiering.
4. På fliken **Allmänt** på en projektbaserad kontraktsrad i fältet **Projekt** väljer du projektlänk.
5. På sidan **Projekt** väljer du fliken **Faktureringsinställningar för uppgift**.
6. Det finns två rutnät. Ett rutnät är för kontraktrader som gäller för hela projektet. Det andra rutnätet gäller för verksamhetsspecifika faktureringsinställningar. Välj en eller flera uppgifter i det andra rutnätet och välj sedan **associera kontraktrader**.
7. Välj en kontraktrad i listrutan på den dialogsida som öppnas.
8. Använd listrutan **Faktureringstyp** för att markera uppgifterna som debiterbara eller inte debiterbara.
9. Markera kryssrutan för att ange om associationen även ska omfatta underordnade uppgifter för de markerade aktiviteterna. Om du markerar rutan associeras även de underordnade uppgifterna för de markerade aktiviteterna till kontraktraden.
10. Stäng dialogrutan genom att välja **OK**.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Koppla bort uppgifter från projektbaserade kontraktrader

### <a name="from-the-contract-line-page"></a>Från sidan Kontraktrad

Följ stegen nedan om du vill koppla bort projektuppgifter från kontraktraden från fliken **Debiterbara uppgifter** på sidan **Kontraktrad**.

1. På fliken **debiteringsbara uppgifter** välj **ta bort en kontraktradsuppgift**.
2. Ett varningsmeddelande anger att om du tar bort den här associationen kan det resultera i återföring av eventuella verkliga värden som tidigare registrerats för uppgiften. Välj **OK** i dialogrutan om du vill ta bort kopplingen mellan uppgiften och den projektbaserade kontraktraden. 

> [!NOTE]
> Detta tar inte bort uppgiften från projektet. Istället tar det bort uppgiftskopplingen från den projektbaserade kontraktsraden.

### <a name="from-the-project-page"></a>Från sidan Projekt

Detta är den mer optimala upplevelsen för att koppla bort uppgifter från kontraktsrader. Du kan markera flera uppgifter och koppla bort alla och deras underordnade uppgifter från den valda kontraktraden. Följ stegen nedan om du vill koppla bort uppgifter från kontraktraden.

1. Från fliken **Allmänt** på en projektbaserad kontraktsrad i fältet **Projekt** klickar du på länken för projektet.
2. På sidan **Projekt** väljer du fliken **Faktureringsinställningar för uppgift**.
3. Det finns två rutnät på sidan. Ett rutnät är för kontraktrader som gäller för hela projektet och den andra gäller för kundspecifik faktureringsinställning. Välj en eller flera uppgifter i det andra rutnätet och välj sedan **Ta bort associering för kontraktrader**.
4. Välj en kontraktrad i listrutan på den dialogsida som öppnas.
5. Markera kryssrutan för att ange om associationen även ska tas bort från underordnade uppgifter för de markerade aktiviteterna. Om du markerar rutan kopplar även bort de underordnade uppgifterna från markerade aktiviteterna till kontraktraden.
6. Välj **OK**. Ett varningsmeddelande anger att om du tar bort den här associationen kan det resultera i återföring av eventuella verkliga värden som tidigare registrerats för uppgiften. Välj **OK** i dialogrutan för varning om du vill ta bort kopplingen mellan uppgiften och den projektbaserade kontraktraden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
