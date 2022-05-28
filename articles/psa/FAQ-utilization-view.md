---
title: Visa debiterbar användning för resurser
description: I den här ämnet finns information om vyn resursanvändning.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 0f6240a3337eb78496570ddfabc85d431e61d640
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595658"
---
# <a name="view-chargeable-utilization-for-resources"></a>Visa debiterbar användning för resurser

[!include [banner](../includes/psa-now-project-operations.md)]
 
**Vyn för resursutnyttjande** på sidan **resursutnyttjande i Project Service** visar debiterbar användning för varje bokningsbar resurs. Eftersom vyn bygger på schemaläggningstavlan och innehåller därför många av de funktioner.

> ![Bild på vyn Utnyttjande.](media/FAQ-utilization-1.png)
 

Det debiterbara resursutnyttjandet beräknas så här:

   Debiterbar användning = (debiterbara timmar) / (resurskapacitet för tillgång)

Cellerna representerar det beräknade debiterbara resursutnyttjandet under den tidsperiod (dagar, veckor eller månader).

Färgerna i respektive cell visar debiterbart resursutnyttjande för en resurs jämfört med sina respektive debiterbara resursutnyttjandemål. 

Målet för resursutnyttjandet kan anges på antingen resursens standardroll eller på den enskilda resursen. Beräkningen undersöker den enskilda resursen för målet först, därefter resursens standardroll.

## <a name="set-target-on-a-resource"></a>Ange mål för en resurs

1. Gå till **Resurser** \> **Resurser**. 
2. Markera en resurs för att öppna posten. 
3. På fliken **Project Service** kan du ange hur målanvändningen av resursen ska vara.

> ![Bild på användning av fliken Project Service för att ange mål för utnyttjande.](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Ange målutnyttjande för en roll

1. Gå till **Resurser** \> **Resursroller**. 
2. Markera en roll och öppna posten. 
3. Ange målutnyttjandet för rollen.

> ![Bild på användning av resursroller för att ange målutnyttjande.](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Beräkna debiterbar användning för en resurs

Om du vill beräkna debiterbart utnyttjande för en resurs måste du slutföra några förutsättningar. 

### <a name="set-default-role-for-individual-resource"></a>Ange standardroll för enskild resurs

Utnyttjandemålet måste först anges för antingen den enskilda resursen eller för resursroller. Om du använder resursroller för mål måste respektive enskilda resurs ha en standardroll. 

1. För att ange denna går du till **Resurser** \> **Resurser**. 
2. Välj en resurs, öppna posten och välj sedan fliken **Project Service**. 
3. I rutnätet **Resursroll** finns en roll för resursen i resursens rutnät **Är standard** anges till **Ja**.
 
### <a name="change-billing-type-for-resource-role"></a>Ändra faktureringstyp för resursrollen.

Rollerna för resursen måste ha en faktureringsadress vars värde är av typen **debiterbar**. 

1. Gå till **Resurser** \> **Resursroller**. 
2. Öppna den post du vill uppdatera och ange sedan standarden för faktureringstyp som **Debiterbar**.

### <a name="set-working-hours-for-resource-role"></a>Ange arbetstider för resursroll
 
Resursen måste ha arbetstimmar för kapacitetsberäkningen. 

1. Gå till **Resurser** \> **Resurser**. 
2. Klicka på en resurs för att öppna posten och klicka sedan på **Visa arbetstimmar**. 
3. Du kan bulkuppdatera resurslistan genom att använda en **mall för arbetstimmar** från vyn **Resurslista**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Felsökning av debiterbara faktiska timmar

De debiterbara tillgångstimmarna hämtas från den entiteten **Faktiska värden**. Faktiska värden med faktureringstypen **debiterbar** inkluderas i beräkningen, och därför måste du ha projekt där tillgångarna är debiterbara.

Här följer några saker du kan kontrollera om du inte ser något debiterbart resursutnyttjande:

- Resursen har arbetstimmar definierade för kapacitet.
- Resursen har antingen ett enskilt definierat resursutnyttjandemål eller har tilldelas en standardroll. Rollen har ett definierat resursutnyttjandemål.
- Faktiska värden har faktureringstypen **debiterbar** för den tidsperiod som du förväntar dig en resursutnyttjandeberäkning för. Kontrollera följande om du ser faktiska värden med faktureringstyper andra än "debiterbar":

  - Den roll som används för tillgången har en standardfaktureringstyp annan än "debiterbar".
  - Rollen på projektkontraktraden bakom projektet har angetts som "icke-debiterbar".
  - Projektet har ingen associerad kontraktrad.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
