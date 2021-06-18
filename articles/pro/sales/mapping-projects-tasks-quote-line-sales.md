---
title: Mappa projekt och uppgifter till en projektbaserad offertrad
description: I det här ämnet finns information om hur du mappar projekt och uppgifter till en projektbaserad uppgiftsrad.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d1c98d6a903393a0afc0e94d7f9859d55b9dc1f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994608"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Mappa projekt och uppgifter till en projektbaserad offertrad

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

På projektbaserade offertrader kan du mappa specifika uppgifter för ett projekt som redan är associerat till en offertrad.

När du mappar uppgifter till en offertrad gäller följande artiklar som du har definierat på offertraden endast för dessa uppgifter:

- Faktureringsmetod
- Debiterbara alternativ
- Undre gränser
- Kunder

Du kanske till exempel har ett projekt där en fas är ett fast pris och alla andra faser är tid och material. I det här fallet kan du associera den första fasen och alla dess underordnade uppgifter till offertraden för den fasen med en faktureringsmetod med fast pris. Därefter kan du koppla alla andra faser till den tids- och det materialbaserade offertraden.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Associera uppgifter till projektbaserade offertrader

Du kan associera uppgifter med offertrader från följande platser:

- Sidan **Projekt** > fliken **Uppgiftsfakturering** (optimal)
- Sidan **Offertrad** > fliken **Debiterbara uppgifter** 

### <a name="from-the-project-page"></a>Från sidan Projekt

Sidan **Projekt** ger den optimala upplevelsen vid associering av uppgifter till offertrader. Du kan använda den här sidan om du vill välja flera uppgifter och associera alla, plus underordnade uppgifter, till den valda offertraden.

1. Under fliken **Allmänt** på en projektbaserad offertrad verifierar du att fältet **Projekt** har fyllts i.
2. I fältet **Inkluderade uppgifter** väljer du **Endast valda uppgifter**.
3. Spara den projektbaserade offertraden. När formuläret uppdateras visa fliken **Debiterbara uppgifter**.
4. Under fliken **Allmänt** väljer du länken för projektet från fältet **Projekt**.
5. På sidan **Projekt** väljer du fliken **Uppgiftsfakturering**.
6. I det andra rutnätet, som gäller för uppgiftsspecifika faktureringsinställningar, väljer du en eller flera uppgifter och väljer sedan **Associera offertrader**.
7. I dialogrutan som visas väljer du en offertrad som visar projektbaserade offertrader i offerten.
8. I fältet **Faktureringstyp** anger du om dessa uppgifter är debiterbara eller icke debiterbara.
9. Markera kryssrutan för att ange om associationen ska innehålla underordnade uppgifter för de valda uppgifterna. Om du markerar rutan associeras de underordnade uppgifterna för de valda uppgifterna till offertraden.
10. Stäng dialogrutan genom att välja **OK**.

### <a name="from-the-quote-line-page"></a>Från sidan Offertrad

Du kan associera projektuppgifter till offertrader från fliken **Debiterbara uppgifter** på sidan **Offertrad**.

>[!NOTE]
>Det bästa stället att associera projektuppgifter med offertrader finns under fliken **Uppgiftsfakturering** på sidan **Projekt**. Om du associerar uppgifter från fliken **Debiterbara uppgifter** på sidan **Offertrad**, måste du manuellt associera varje projekt.

1. Under fliken **Allmänt** på en projektbaserad offertrad verifierar du att ett projekt har valts i fältet **Projekt**.
2. I fältet **Inkluderade uppgifter** väljer du **Endast valda uppgifter**.
3. Spara den projektbaserade offertraden. När formuläret uppdateras visa fliken **Debiterbara uppgifter**.
4. Under fliken **Debiterbara uppgifter** väljer du **Lägg till en offertradsuppgift**.
5. På sidan **Offertradsuppgift**, i fältet **Uppgifter**, väljer du uppgiften och i fältet **Faktureringstyp** väljer du **Spara**. 
6. Stäng sidan. Den valda uppgiften är nu kopplad till offertraden.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Avassociera uppgifter från projektbaserade offertrader

### <a name="from-the-project-page"></a>Från sidan Projekt

Den här metoden ger den optimala upplevelsen vid avassociering av uppgifter från offertrader. Du kan välja flera uppgifter och avassociera alla, plus underordnade uppgifter, från den valda offertraden.

1. Under fliken **Allmänt** på en projektbaserad offertrad, i fältet **Projekt**, väljer du projektlänken.
2. På sidan **Projekt** väljer du fliken **Uppgiftsfakturering**.
3. I det andra rutnätet, som gäller för uppgiftsspecifika faktureringsinställningar, väljer du en eller flera uppgifter och väljer sedan **Avassociera offertrader**.
4. Välj en offertrad på den dialogruta som visas.
5. Markera kryssrutan för att ange om associationen också ska tas bort från underordnade uppgifter för de valda uppgifterna. Om du markerar rutan avassocieras även de underordnade uppgifterna för de valda uppgifterna från offertraden.
6. Välj **OK**. Ett varningsmeddelande visas om att du har tagit bort den här associationen. alla verkliga värden som tidigare registrerats för uppgiften kan återföras. 
7. Välj **OK** om du vill fortsätta och ta bort kopplingen mellan uppgiften och den projektbaserade offertraden.

### <a name="from-the-quote-line-page"></a>Från sidan Offertrad

Du kan även avassociera projektuppgifter från offertrader från fliken **Debiterbara uppgifter** på sidan **Offertrad**.

1. Under fliken **Debiterbara uppgifter** väljer du **Ta bort en offertradsuppgift**.
2. Välj **OK**. Ett varningsmeddelande visas om att du har tagit bort den här associationen. alla verkliga värden som tidigare registrerats för uppgiften kan återföras. 
3. Välj **OK** om du vill fortsätta och ta bort kopplingen mellan uppgiften och den projektbaserade offertraden.

>[!NOTE]
> Med den här proceduren tas inte uppgiften bort från projektet. Det är bara uppgiftskopplingen som tas bort från den projektbaserade offertraden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]