---
title: Mobil arbetsyta för utgiftshantering
description: I det här ämnet finns information om hur du använder mobil arbetsyta för utgiftshantering. Med den här arbetsytan kan användare fånga in och överföra ett kvitto så att de kan bifogas till en utgiftsrapport senare. Du kan också snabbt skapa en utgiftsrad genom att använda en kopplad inleverans och skapa och hantera deras utgiftsrapporter.
author: suvaidya
ms.date: 12/01/2017
ms.topic: article
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d5309b55ed146d21d7a42e0b40add9ee346d48aa
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682824"
---
# <a name="expense-management-mobile-workspace"></a>Mobil arbetsyta för utgiftshantering

I det här ämnet finns information om hur du använder mobil arbetsyta för **utgiftshantering**. Med den här arbetsytan kan användare fånga in och överföra ett kvitto så att de kan bifogas till en utgiftsrapport senare. Du kan också snabbt skapa en utgiftsrad genom att använda en kopplad inleverans och skapa och hantera deras utgiftsrapporter. Dessutom kan godkännare använda mobil arbetsyta för **utgiftshantering** för att visa utgiftsrapporter som har tilldelats dem och antingen godkänna eller avvisa dessa utgiftsrapporter.


Den här mobila arbetsytan är avsedd att användas tillsammans med Dynamics 365 Unified Ops-mobilapp.


## <a name="overview"></a>Översikt

Många organisationer kräver att en kopia av ett kvitto ska bifogas till en rese- eller affärsrelaterad utgiftsrapport som en medarbetare skickar in för återbetalning. Med arbetsytan **Utgiftshantering** kan användare snabbt skapa nya utgiftsrader på den mobila enheten med hjälp av ett bifogat foto av ett kvitto. Du kan också skapa ett foto av ett kvitto och sedan bifoga det i en utgiftsrapport senare. Medarbetare kan även skapa och hantera sina utgiftsrapporter och sedan skicka dem för godkännande och återbetalning med hjälp av deras mobila enheter.


Särskilt den mobila arbetsytan **utgiftshantering** kan användarna utföra de här uppgifterna:

- Ta en bild av ett kvitto och skicka det till Dynamics 365 Finance. Du kan sedan bifoga fotot i en utgiftsrapport senare.
- Överför en fil som ett insamlat kvitto. Du kan sedan bifoga filen i en utgiftsrapport senare.
- Skapa en ny utgiftsrad genom att använda en kopplad inleverans. Du kan sedan lägga till rad artikeln i en utgiftsrapport senare och skicka den för godkännande och återbetalning.

Du kan också använda dessa funktioner:

- Skapa en ny utgiftsrapport.
- Koppla kreditkortstransaktioner och andra tidigare skapade utgifter till en utgiftsrapport.
- Skapa nya utgifter för en utgiftsrapport.
- Koppla ett kvitto till valfri utgift för en utgiftsrapport, antingen genom att ta ett foto av kvittot eller genom att överföra en fil som ett insamlat kvitto.
- Beroende på företagets utgiftspolicy lägger du till listan över gäster i en utgift.
- Specifikation av utgifter, beroende på företagets utgiftsprincip.
- Skicka en utgiftsrapport för godkännande och återbetalning.
- Godkänn eller avvisa utgiftsrapporter som du är tilldelad godkännare för.

## <a name="prerequisites"></a>Förutsättningar
Förutsättningarna varierar beroende på vilken version av som har distribuerats för organisationen.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Krav om du använder Dynamics 365 Finance 
Om Finance har distribuerats för organisationen måste systemadministratör publicera mobilarbetsytan **utgiftshantering**. Instruktioner finns i [Publicerar mobila arbetsytor](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Förutsättningar om du använder version 1611 med plattformsuppdatering 3 eller senare
Om version 1611 med plattformsuppdatering 3 eller senare har distribuerats för organisationen måste systemadministratör uppfylla följande krav. 

<table>
<thead>
<tr class="header">
<th>Förutsättningar</th>
<th>Roll</th>
<th>Beskrivning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementera KB 4019015.</td>
<td>Systemadministratör</td>
<td>KB 4019015 är en X++ uppdatering eller en snabb korrigering för mobil arbetsyta <strong>utgiftshantering</strong>. Innan du implementerar KB 4019015 måste systemadministratör följa stegen nedan.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Hämta snabb korrigeringen för metadata från Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Installera snabbkorrigeringen för metadata</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Skapa ett distribuerbart paket</a> som innehåller modellerna <strong>ApplicationSuite</strong> och <strong>ExpenseMobile</strong> och överför sedan det distributionsbara paketet till LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Använd det distributionsbara paketet</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publicera mobila ytan för <strong>utgiftshantering</strong>.</td>
<td>Systemadministratör</td>
<td>Se <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">publicerar en mobil arbetsyta</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Ladda ned och installera mobilappen Dynamics 365 for Operations
Hämta och installera mobilappen Dynamics 365 Unified Ops:

- [För Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
- [För iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logga in på mobilappen
1. Starta appen på din mobila enhet.
2. Ange din Dynamics 365 URL
4. Första gången du loggar in ombeds du ange ditt användarnamn och lösenord. Ange dina autentiseringsuppgifter.
5. När du har loggat in visas de tillgängliga arbetsytorna för ditt företag. Observera att om systemadministratören publicerar en ny arbetsyta senare måste du uppdatera listan med mobila arbetsytor.


[![Dra nedåt för att uppdatera.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Skapa ett kvitto med hjälp av mobila ytan för utgiftshantering

1. På din mobila enhet, öppna arbetsytan **Utgiftshantering**.
2. Välj **insamlingskvitto**.
3. Välj **Ta foto** eller **Välj bild**.
4. Följ ett av de här stegen:

    - Om du valde **Ta foto** följer du stegen nedan:

        1. Du är på kameran på den mobila enheten så att du kan ta ett foto av kvittot. När du är klar med fotot väljer du **OK** för att godkänna fotot.
        2. Valfritt: Ange ett namn på fotot och skriv eventuella anteckningar.

    - Om du valde **Välj bild** följer du stegen nedan:

        1. Välj en bild i listan.
        2. Valfritt: Ange ett namn på bilden och skriv eventuella anteckningar.

5. Välj **Utfört**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Ange snabbt utgifter med hjälp av mobila ytan för utgiftshantering
1. På din mobila enhet, öppna arbetsytan **Utgiftshantering**.
2. Välj **Post för snabbutgift**.
3. Välj kategorin för utgiften. Du ser en lista över utgiftskategorier som har lästs in i din app för användning offline. Som standard laddas 50 objekt, men en utvecklare kan ändra antalet. För information bör utvecklare läsa [mobil plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Om kategorin inte finns med i listan väljer du **Sök** för att göra en sökning online. Sök efter utgiftskategori eller växla till att söka efter utgiftstyp.
4. Ange transaktionsdatum för utgiften.
5. Valfritt: Ange en återförsäljare för utgiften.
6. Ange belopp för utgiften.
7. Välj valuta för utgiften. Du ser en lista valutakoder som har lästs in i din app för användning offline. Som standard laddas 400 valutor, men en utvecklare kan ändra antalet. För information bör utvecklare läsa [mobil plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Om valutan inte finns med i listan väljer du **Sök** för att göra en sökning online. Sök efter valuta eller växla till att söka efter namn.
8. Välj **Ta foto** eller **Välj bild**.
9. Följ ett av de här stegen:

    - Om du valde **Ta foto** tas du till kameran på din mobila enhet så att du kan ta ett foto av kvittot. När du är klar med fotot väljer du **OK** för att godkänna fotot.
    - Om du valde **Välj bild** markerar du en bild i listan.

10. Välj **Utfört**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Godkänn en utgiftsrapport med hjälp av mobila arbetsytan utgiftshantering (om du använder uppdateringen från juli 2017)
1. På din mobila enhet, öppna arbetsytan **Utgiftshantering**.
2. **Utgiftsgodkännanden** visar antalet utgiftsrapporter som har tilldelats dig för godkännande. Antalet uppdateras ungefär var trettionde minut. Välj **utgiftsgodkännanden**.

    Listan över utgiftsrapporter som har tilldelats dig för godkännande visas.
    
3. Välj en utgiftsrapport om du vill visa utgiftsdetaljer för den.
4. Välj en utgift om du vill visa detaljer för den. I informationen som visas för en utgift ingår all information om kvitto, gäst och specificering.
5. Sidan **Utgiftsrapport** väljer du om du vill godkänna eller avvisa utgiftsrapporten.
6. Ange kommentarer för godkännande åtgärden.
7. Välj **Utfört**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Skapa en ny utgiftsrapport och skicka in det för godkännande med hjälp av mobila arbetsytan utgiftshantering (om du använder uppdateringen från juli 2017)
1. På din mobila enhet, öppna arbetsytan **Utgiftshantering**.
2. Välj **Utgiftspost**.
3. Välj **ny rapport** eller välj en befintlig utgiftsrapport i listan.
4. För nya utgiftsrapporter anger du syftet med och eventuell ytterligare information som är tillgänglig. Informationen varierar beroende på vilket utgiftshantering som har konfigurerats för företaget.
5. Välj **Utfört**.
6. Om du vill lägga till befintliga utgifter, t.ex. kreditkortstransaktioner, i utgiftsrapporten väljer du **Bifoga**.
7. Markera en eller flera användare i listan.
8. Välj **Utfört**.
9. Om du vill lägga till en ny utgift i utgiftsrapporten väljer du **ny utgift**.
10. Välj kategorin för utgiften. Du ser en lista över utgiftskategorier som har lästs in i din app för användning offline. Som standard laddas 50 objekt, men en utvecklare kan ändra antalet. För information bör utvecklare läsa [mobil plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Om kategorin inte finns med i listan väljer du **Sök** för att göra en sökning online. Sök efter utgiftskategori eller växla till att söka efter utgiftstyp.
11. Valfritt: Ange en återförsäljare för utgiften.
12. Ange transaktionsdatum för utgiften.
13. Ange belopp för utgiften.
14. Välj valuta för utgiften. Du ser en lista valutakoder som har lästs in i din app för användning offline. Som standard laddas 400 valutor, men en utvecklare kan ändra antalet. För information bör utvecklare läsa [mobil plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Om valutan inte finns med i listan väljer du **Sök** för att göra en sökning online. Sök efter valuta eller växla till att söka efter namn.
15. Välj **Utfört**.
16. Om du vill lägga till fler detaljer i utgiften väljer du **Lägg till fler detaljer**. Vilka fält som är tillgängliga beror på konfigurationen av utgiftshantering för ditt företag.
17. Om företagspolicyn kräver ett kvitto för utgiften markerar du **inleveranser** och följer sedan stegen nedan:

    1. Välj **insamlingskvitto** eller **bifoga kvitto**.
    2. Följ ett av de här stegen:

        - Om du valde **insamlingskvitto** följer du stegen nedan:

            1. Välj **Ta foto** eller **Välj bild**.
            2. Följ ett av de här stegen:

                - Om du valde **Ta foto** följer du stegen nedan:

                    1. Du är på kameran på den mobila enheten så att du kan ta ett foto av kvittot. När du är klar med fotot väljer du **OK** för att godkänna fotot.
                    2. Valfritt: Ange ett namn på fotot och skriv eventuella anteckningar.

                - Om du valde **Välj bild** följer du stegen nedan:

                    1. Välj en bild i listan.
                    2. Valfritt: Ange ett namn på bilden och skriv eventuella anteckningar.

            3.  Välj **Utfört**.

        - Om du valde **bifoga kvitto** följer du stegen nedan:

            1.  Välj en eller flera bilder i listan.
            2.  Välj **Utfört**.

    3. Välj **Tillbaka** för att återgå till utgiftsinformationen.

18. Om företagspolicyn kräver gäster för utgiften markerar du **Gäster** och följer sedan stegen nedan:

    1. Välj **Gäst**, **Tidigare gäster** eller **Medarbetare**.
    2. Följ ett av de här stegen:

        - Om du valde **Gäst** följer du stegen nedan:

            1. Ange namnet på gäst.
            2. Valfritt: Ange gästens organisation och/eller land.
            3. Valfritt: Ange gästens titel.
            4. Välj **Utfört**.

        - Om du valde **Tidigare gäster** följer du stegen nedan:

            1. Välj en eller flera tidigare gäster i listan. Du ser en lista över tidigare gäster som du har lagt till i tidigare utgiftsrapporter som läses in i din app för offlineanvändning. Som standard laddas 50 objekt, men en utvecklare kan ändra antalet. För information bör utvecklare läsa [mobil plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Om din tidigare gäster inte finns med i listan väljer du **Sök** för att göra en sökning online. Sök efter namn eller byt till sökning efter organisation, land eller titel.
            2. Välj **Utfört**.

        - Om du valde **medarbetare** följer du stegen nedan:

            1. Välj en eller flera medarbetare i listan. Du ser en lista över medarbetare som har lästs in i din app för användning offline. Som standard laddas 50 objekt, men en utvecklare kan ändra antalet. För information bör utvecklare läsa [mobil plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Om medarbetare inte finns med i listan väljer du **Sök** för att göra en sökning online. Sök efter namn eller byt till sökning efter land eller titel.
            2. Välj **Utfört**.

    3. Välj **Tillbaka** för att återgå till utgiftsinformationen.

19. Om företagspolicyn kräver att utgiften specificeras markerar du **specificera** och följer sedan stegen nedan:

    1. Välj det första datum som ska specificeras.
    2. Välj **Lägg till specificera**.
    3. Välj underkategorin för kostnadsspecificering. Du ser en lista över underkategorier för utgifter som har lästs in i din app för användning offline. Som standard laddas 50 objekt, men en utvecklare kan ändra antalet. För information bör utvecklare läsa [mobil plattform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Om underkategorin inte finns med i listan väljer du **Sök** för att göra en sökning online. Sök efter utgiftens underkategorinamn.
    4. Ange transaktionsbeloppet för specificering.
    5. Redigera transaktionsdatumet om det behövs.
    6. Välj **Utfört**.
    7. Upprepa föregående steg tills du är klar med att lägga till alla specificeringar för det valda datumet.
    8. För ytterligare dagar kan du välja **Kopiera till nästa dag** för att kopiera specificering till nästa dag. Alternativt kan du välja datum för att specificera och sedan lägga till specificeringar som du gjort för det första datumet.
    9. När du har utfört utgiften väljer du knappen **tillbaka** för att återgå till utgiftsinformationen.

20. Välj knappen **Tillbaka** för att återgå till sidan **Utgiftsrapport**.
21. Upprepa stegen ovan tills du är klar med att lägga till alla utgifter.
22. Välj **Skicka**.
23. Ange kommentarer för godkännare.
24. Välj **Utfört**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]