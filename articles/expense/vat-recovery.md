---
title: Momsåterbetalning i utgiftshantering
description: I det här ämnet förklaras hur du erhåller återbetalning av momstransaktioner.
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 2c20e4a7fa9748e03bf1729fc2f7bdbfc2f292d1
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908650"
---
# <a name="vat-recovery-in-expense-management"></a>Momsåterbetalning i utgiftshantering

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

För att få berättigade momstransaktioner återbetalda måste ett företag identifiera, samla in, verifiera och skicka in korrekt information. Den här processen omfattar flera uppgifter och kan, beroende på företagets storlek, innehålla flera medarbetare eller roller.

För att få tillbaka moms i modulen **Utgiftshantering** måste följande krav uppfyllas:

- Momskoder måste skapas för länder/regioner som har tilldelats utgiftskategorier.
- En momsgrupp måste skapas för varje momskod.
- En momskod för artikelförsäljning måste skapas för varje momsgrupp.

När förutsättningarna har uppfyllts måste följande steg utföras för att begära återbetalningar av momstransaktioner.

1. I en utgiftsrapport anger du momsinformation för kreditkortstransaktioner för att identifiera berättigade momsåterbetalningar.
2. Kontrollera att all momsinformation är fullständig och skicka sedan utgiftsrapporten.
3. Bearbeta utgifter som är relevanta för internationell momsåterbetalning.
4. Skicka momsåterbetalningsdata till tredjepartsleverantören för att registrera internationella återbetalningar.
5. Bearbeta utgifter för inhemsk momsåterbetalning.

I följande avsnitt finns exempel som visar hur Contoso-anställda slutför varje steg.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Ange momsinformation för kreditkortstransaktioner för att identifiera berättigade momsåterbetalningar

Nancy, en säljare hos Contoso som är baserad i USA och som nyligen kom tillbaka från en säljresa till Storbritannien. Under resan ådrog sig Nancy några personliga utgifter på kreditkortet för måltider. Nancy måste nu skapa en utgiftsrapport för att kunna stämma av utgifterna.

När Nancy anger information i utgiftsrapporten väljer hon **Storbritannien** i fältet **Land/region** på sidan **Redigera utgiftsrapport**. Listan över momsgrupper filtreras sedan så att den endast visar de grupper som gäller för Storbritannien. Nancy väljer momsgruppen **Storbritannien 001** och väljer sedan momsgruppen för artikelförsäljning **Måltider**. Härnäst lägger Nancy till en ny transaktion för logi. Eftersom det endast finns en momsgrupp och en momsgrupp för artikelförsäljning för logi i Storbritannien fylls informationen i automatiskt på Nancys utgiftsrapport.

Enligt Contoso-policyn måste alla utgifter ha ett matchande kvitto. Därför får Nancy ett meddelande som anger att hon måste bifoga ett kvitto för varje transaktion som hon noterade i utgiftsrapporten när hon sparar utgiftsrapporten. Nancy kontrollerar att hon har bifogat en digital bild av varje transaktionskvitto till utgiftsrapporten och skickar rapporten för godkännande. Hon skickar sedan papperskvitton till backoffice-gruppen för behandling.. Det här teamet skickar momsåterbetalningsdata till den tredjepartsleverantör som registrerar internationella momsåterbetalningar för Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Kontrollera momsinformation och bokföra en utgiftsrapport

Innan April, koordinatorn av leverantörsreskontra för Contoso, kan bokföra en utgiftsrapport måste hon ange eventuell momsinformation som saknas i den. Hon öppnar sidan **Utgiftsrapportinformation** och ser Nancys godkända utgiftsrapport. April öppnar sedan utgiftsrapporten för att visa information om transaktionerna. Hon ser att Nancy inte angav någon momsgrupp för artikelförsäljning för en av transaktionerna. Eftersom den här informationen inte har angetts kan April inte bokföra utgiftsrapporten. Därför tittar hon på sidan **Momskonfiguration** i utgiftshanteringen och söker efter rätt momsgrupp för artikelförsäljning för landet/regionen och transaktionstypen. April kan nu bokföra utgiftsrapporten i huvudboken.

När utgiftsrapporten har bokförts av April skapas en arbetsuppgift med momsåterbetalning. Den här arbetsuppgiften tilldelas en medlem i backoffice-gruppen för behandling. April får ett meddelande som bekräftar att bokföringen har slutförts. I det här meddelandet visas även antalet momstransaktioner som identifierades för återbetalningen.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Bearbeta utgifter som är relevanta för internationell momsåterbetalning

Arnie, medlem i Contosos backoffice-grupp för behandling, ansvarar för att verifiera att all nödvändig information för momsåterbetalning ingår i utgiftsrapporter. Han öppnar sidan **Återbetalning av utgiftsmoms** och väljer utgiftsrapporten som Nancy skickat. Arnie verifierar sedan att alla begärda kvitton har bifogats och att rätt momsgrupp och momskoder har angetts.

När Arnie tar emot papperskvitton från Nancy verifierar han dem mot de digitala kvittona och ändrar sedan statusen på utgiftsrapporten till **Klar för återbetalning**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Skicka momsåterbetalningsdata till tredjepartsleverantören

När Arnie är redo att skicka utgiftsrapportdata till den tredje part som ska registrera momsåterbetalningen öppnar han sidan **Återbetalning av utgiftsmoms**. Han filtrerar sidan så att endast de utgiftsrapporter som är markerade som **Klar för återbetalning** visas. Arnie väljer sedan **Arkivera** &gt; **Exportera till Excel**. Momsinformationen från utgiftsrapporterna exporteras till ett Microsoft Excel-kalkylblad. Arnie skickar kalkylbladet till tredjepartsleverantören och inkluderar ett meddelande om att papperskvitton har skickats med bud.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Bearbeta utgifter för inhemsk momsåterbetalning

Arnie måste kontrollera att transaktionerna i utgiftsrapporten är berättigade till momsåterbetalning och att de digitala kvittona har bifogats till rapporterna. För att börja bearbeta utgifter som är berättigade till inhemsk återbetalning öppnar Arnie sidan **Återbetalning av utgiftsmoms** och väljer utgiftsrapporten som kräver verifiering. Han bekräftar att kvitton finns i företagets namn i stället för i medarbetarens. (För momsåterbetalning måste kvitton vara i företagets namn). Arnie verifierar sedan att alla begärda kvitton har bifogats och att rätt momsgrupp och momskoder har angetts.

När Arnie tar emot papperskvitton ändrar han status för utgiftsrapporten till **Klar för återbetalning**. Han kan sedan registrera återbetalningen hos rätt skattemyndighet. I det här fallet är rätt skattemyndighet i USA Internal Revenue Service (IRS).
