---
title: Preliminärboka en resurs
description: I det här ämnet finns information om hur du kan schemalägga eller preliminärboka projektteammedlemmar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: 2675096085fc4c673d15741042ffc1b82ed3de8b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146460"
---
# <a name="soft-book-a-resource"></a>Preliminärboka en resurs

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan preliminärt schemalägga eller preliminärboka en resurs till ett projektteam i syfte att visa att du planerar att tilldela resursen till projektet. Preliminärbokningar förbrukar inte den tillgängliga kapaciteten för en resurs, och du kan tilldela preliminärbokade teammedlemmar till projektaktiviteter. Eftersom preliminär bokning inte förbrukar kapaciteten för en resurs kan du emellertid fortfarande ”fastboka” resursen för andra uppgifter under samma period. Generiska resurser kan inte preliminärbokas, och preliminärbokningar kan heller inte uppfylla en begäran för generiska resurser.

Preliminärbokade projektteammedlemmar visas på fliken **Team** på sidan **Projekct** sina preliminärbokade timmar angivna i kolumnen **preliminärbokade timmar** i vyn **Namngivna teammedlemmar**. Preliminärbokade teammedlemmar listas även på schemaläggningstavlan. Eftersom de är preliminärbokade visar inte schemaläggningstavlan någon kapacitetsförbrukning för dessa resurser. Preliminärbokad tid visas inte på fliken **Avstämning** eller i fältet **Utöka bokning** på fliken **Avstämning** på schemaläggningstavlan. 

Det finns två sätt att preliminärboka en teammedlem för ett projekt: direkt från schemaläggningstavlan eller genom att lägga till teammedlemmen på fliken **Team**. 

## <a name="soft-book-from-the-schedule-board"></a>Preliminärboka från schemaläggningstavlan
Följ stegen nedan om du vill preliminärboka en resurs från schemaläggningstavlan. 

1. Använd schemaläggningstavlan på panelen för **bokningskrav** på fliken **projekt**.
2. Hitta det projekt som du vill preliminärboka en resurs på. Om det finns ett stort antal projekt i listan väljer du kolumnrubriken **projekt** och använder sedan filtret för att söka efter ett eller flera projekt.
3. Välj projektet och dra och släpp det sedan på resursens tidsrutnät.
5. I panelen **Skapa resursbokning**, justera start- och slutdatum och ange **bokningsstatus** till **preliminär** och ange sedan timmarna. 
6. Klicka på **Boka**. Resursen visar nu fliken **Team** som en resurs för projektet. I vyn **Namngiven teammedlem** ser du preliminärbokade timmar i kolumnen **Preliminärbokade timmar**.

> [!NOTE]
> Du kan nu kan tilldela preliminärbokade till aktiviteter på fliken **Schema**. På fliken **Avstämning** visar resursen ett bokningsunderskott i förhållande till deras uppgift, detta eftersom fliken **Avstämning** endast beaktar fasta bokningar. Du kan använda funktionen **Utöka bokningar** för att fastboka resursen i syfte att undvika brist på fasta bokningar för resursens tilldelningar. Du måste manuellt avbryta en preliminär bokning för resursen genom att använda **Underhåll bokningar**.

## <a name="soft-book-on-the-team-tab"></a>Preliminärboka på fliken Team.

Du kan lägga till teammedlemmar direkt på fliken **Team** och ändra sedan deras bokningsstatus från **Fast** till **Preliminär** med **Underhåll bokningar**. När du lägger till en teammedlem på det här sättet resulterar detta alltid i en fast bokning såvida du inte markerar tilldelningsmetoden som **Ingen**.

Om du vill använda den här metoden måste du göra följande.

1. På sidan **Projekt** på fliken **Team**, klicka på **Ny**.
2. Markera den bokningsbara resursrollen samt Från- och Till-datum.
3. Välj en fördelningsmetod annan än **Ingen**.
4. Välj **Spara**. Resursen visas i rutnätet och arbetstiderna anges i kolumnen för som **fastbokade arbetstimmar**.
5. Behåll resursens bokningar genom att klicka på **Behåll bokningar**.
6. Expandera resursen om du vill visa bokningar när schemaläggningstavlan öppnas. Bokningen anges som **Fast**.
7. Högerklicka på bokningen och - under **Ändra Status** - markera **Preliminärboka** \> **Preliminär**. Bokningsstatusen är nu **Preliminär**.
8. När du har stängt schemaläggningstavlan ser du att timmarna för resursen har flyttats från kolumnen **Fastbokade timmar** till **Preliminärbokade timmar** i rutnätet för fliken **Team** när du visar vyn **Namngivna teammedlemmar**.

> [!NOTE]
> När du använder **Underhåll bokningar** för att ändra status från **Fast** till **Preliminär** om du fastbokar en resurs till teamet och sedan tilldelar resursen uppgifter kommer uppgiftstilldelningarna för den resursen att behållas. På fliken **Avstämning** kommer resursen emellertid att ha ett bokningsunderskott eftersom endast fasta bokningar beaktas vid avstämning mellan bokningar och tilldelningar. Du kan använda funktionen **Utöka bokningar** på fliken **Avstämning** för att fastboka resursen i syfte att undvika brist på fasta bokningar för resursens tilldelningar. Du måste manuellt avbryta en preliminär bokning för resursen genom att använda **Underhåll bokningar**.

När du är redo att ändra en preliminärbokad teammedlemsresurs till en fastbokad teammedlem kan du göra följande:

1. Expandera resursen på schemaläggningstavlan om du vill visa dess bokningar. Bokningen anges som **Preliminär**.
2. Högerklicka på bokningen och under **Ändra Status** - markera **Fastboka** \> **Fast**. Bokningsstatusen är nu **Fast**.
3. När du har stängt schemaläggningstavlan och återgått till projektet samt öppnat fliken **Team**, ser du att timmarna för resursen har flyttats från kolumnen **Preliminärbokade timmar** till kolumnen **Fastbokade timmar** i fliken **Team** när du visar vyn **Namngivna teammedlemmar**. Om resursen har tilldelats uppgifter visar de inte längre ett bokningsunderskott i fliken **Avstämning** eftersom deras bokningar nu är fasta.



[!INCLUDE[footer-include](../includes/footer-banner.md)]