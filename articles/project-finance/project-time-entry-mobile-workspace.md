---
title: Mobil arbetsyta för projektets tidspost
description: I den här ämne finns information om hur du använder mobil arbetsyta för projektets tidspost. På den här arbetsytan kan användare ange och spara tid för ett projekt med hjälp av deras mobila enheter.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756228"
---
# <a name="project-time-entry-mobile-workspace"></a>Mobil arbetsyta för projektets tidspost

[!include [banner](../includes/banner.md)]

I den här ämne finns information om hur du använder mobil arbetsyta för **projektets tidspost**. På den här arbetsytan kan användare ange och spara tid för ett projekt med hjälp av deras mobila enheter.

Den här mobila arbetsytan är avsedd att användas tillsammans med Dynamics 365 Unified Ops-mobilapp. 

## <a name="overview"></a>Översikt
Som en del av det dagliga arbetet är projektresurserna ofta på plats eller på resande fot. **Projektets tidsinmatning** mobil arbetsyta kan användarna ange sin fakturerbara eller ej fakturerbar tid för ett projekt på den mobila enheten som de väljer. Projektresurser kan därför registrera tidstransaktioner när som helst och var som helst. De kan också visa tidtransaktioner som redan har registrerats. 

Specifikt i **Projektets tidspost** kan mobil arbetsyta användarna utföra de här uppgifterna:

-   Ange antalet timmar som du har tillbringat för en viss uppgift för alla valda datum.
-   Sök efter projektnamn eller kund för att hitta projektet för att ange tid för.
-   Ange kategori och aktivitet för den tid du tillbringar.
-   Registrera tiden som fakturerbar eller ej fakturerbar för projektet.
-   Ange eventuella externa eller interna kommentarer.

## <a name="prerequisites"></a>Förutsättningar
Förutsättningarna varierar beroende på vilken version av Microsoft Dynamics 365 som har distribuerats för organisationen.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Krav om du använder Dynamics 365 Finance
Om Finance har distribuerats för organisationen måste systemadministratör publicera mobil arbetsytan **Projektets tidspost**. Instruktioner om hur du [publicerar en mobil arbetsyta](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

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

<td>Implementera KB 4018050.</td>
<td>Systemadministratör</td>
<td>KB 4018050 är en X++ uppdatering eller en snabb korrigering för mobil arbetsyta <strong>projekttidsinmatning</strong>. Innan du implementerar KB 4018050 måste systemadministratör följa stegen nedan.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Hämta snabb korrigeringen för metadata från Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installera snabbkorrigeringen för metadata</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Skapa ett distribuerbart paket</a> som innehåller modellerna <strong>ApplicationSuite</strong> och <strong>ProjectMobile</strong> och överför sedan det distributionsbara paketet till LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Använd det distributionsbara paketet</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publicera arbetsytan <strong>Projektets tidspost</strong>.</td>
<td>Systemadministratör</td>
<td>Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">publicerar en mobil arbetsyta</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Ladda ned och installera en mobilapp

Ladda ned och installera mobilappen Finance and Operations:

-   [För Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [För iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logga in på mobilappen
1.  Starta appen på din mobila enhet.
2.  Ange din Dynamics 365 URL
3.  Första gången du loggar in ombeds du ange ditt användarnamn och lösenord. Ange dina autentiseringsuppgifter.
4.  När du har loggat in visas de tillgängliga arbetsytorna för ditt företag. Observera att om systemadministratören publicerar en ny arbetsyta senare måste du uppdatera listan med mobila arbetsytor.

[![Dra nedåt för att uppdatera](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Ange tid genom att använda mobil arbetsyta för projektets tidsinmatning
1.  På din mobila enhet, välj arbetsytan **Projektets tidspost**.
2.  Välj **Tidspost**. Kalenderdatumen för den aktuella veckan visas.
3.  För ett valt datum, välj **Åtgärder** &gt; **Ny inmatning**.
4.  Ange hur många objekt som ska registreras.
5.  Välj projekt för tidsposten. En lista visar de projekt som har lästs in i din app för användning offline. Som standard laddas 50 objekt, men en utvecklare kan ändra antalet. Mer information finns i [mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Om projektet inte finns med i listan väljer du **Sök**. Sök efter namn eller växla till sökning efter projektnamn eller kund.
7.  Välj en kategori. En lista visar de kategorier som har lästs in i din app för användning offline. Som standard laddas 50 objekt, men en utvecklare kan ändra antalet. Mer information finns i [mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Om kategorin inte finns med i listan väljer du **Sök**. Sök efter kategori eller växla till att söka efter kategorinamn.
9.  Välj en aktivitet. En lista visar de aktiviteter som har lästs in i din app för användning offline. Som standard laddas 50 objekt, men en utvecklare kan ändra antalet. Mer information finns i [mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Om din aktivitet inte finns med i listan väljer du **Sök**. Sök efter aktivitetsnummer eller växla till sök efter syfte.

11. Välj radegenskapen.
12. Valfritt: Ange eventuella externa och interna kommentarer.
13. Välj **Utfört**.
