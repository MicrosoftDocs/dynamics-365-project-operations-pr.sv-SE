---
title: Avbryt tidigare godkända tids- och utgiftsposter
description: I det här ämnet finns information om hur du avbryter en godkänd projekttid och utgiftstransaktion.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bf3d146d2b07723b4d2e6e85eafd6f1b23b8b83f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014768"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Avbryt tidigare godkända tids- eller utgiftsposter

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I den senaste versionen av Dynamics 365 Project Service Automation kan godkännare annullera tids- eller utgiftsposter som de tidigare har godkänt.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Avbryt en tidigare godkänd tids- eller utgiftspost

Följ stegen nedan om du vill avbryta en tids- eller utgiftstransaktion som du tidigare godkänt.

1. Gå till **Projekt** \> **Mitt arbete** \> **Godkännanden**.
2. På listsidan **godkännanden** ändrar du vyn till **mina tidigare godkännanden**. En lista över de tids- och utgiftstransaktioner som du tidigare godkänt visas.
3. Markera en eller flera poster och välj sedan **Avbryt godkännande**. Ett varningsmeddelande visas.
4. Välj **OK** för att avbryta godkännandet.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Ta reda på hur du avbryter ett godkännande av tids- eller utgiftspost

När ett godkännande har annullerats finns det både driftseffekter och ekonomiska effekter.

### <a name="operational-impact"></a>Driftseffekter

På driftssidan återställs statusen för posten när ett godkännande avbryts **Utkast** och godkännandet visas inte längre i vyn **Mina senaste godkännanden**. I stället visas det annullerade godkännandet i antingen vyn **Tidsposter för godkännande** eller vyn **Utgiftsposter för godkännande** beroende på om det är en tidspost eller en utgiftspost. Dessutom ändras statusen för den relaterade tids- eller utgiftsposten till **skickad** så att den relaterade posten överensstämmer med godkännanden som har statusen **utkast**.

Som godkännare kan du redigera en del av fälten för ett godkännande som har statusen **utkast**. Dessa fält inkluderar **faktureringstyp** och **fakturerbara timmar för tidsposter**. När du har gjort ändringar kan du godkänna posten igen. Alternativt kan du avvisa transaktionen. Om du avvisar godkännandet av en tidspost ändras transaktionens status till **returnerad**. Om du avvisar godkännandet av en utgiftspost ändras transaktionens status till **Avvisad**. Funktionen returnerade och avvisade poster fungerar på samma sätt som en post som har statusen **utkast**. En projektgruppmedlem kan antingen göra nödvändiga ändringar i transaktionen och sedan skicka den på nytt för godkännande, eller ta bort posten helt.

### <a name="financial-impact"></a>Finansiella effekter

Ett projekt påverkas också ekonomiskt när ett godkännande annulleras. Först uppdateras motsvarande verkliga värden för kostnader och försäljning på följande sätt:

- Justeringsstatus är inställd på **justerad**.
- Faktureringsstatus är inställd på **Avbrutet**.

Sedan skapas återföringsposter i tabellen faktiska värden. Om du vill skapa återföringsposter kopieras systemet över fältvärdena från de ursprungliga värdena. De enda värden som inte kopieras över är antalet värden. De här värdena återförs i stället. Återförda faktiska värden skapas både för **kostnad** och för **fakturerade försäljningsvärden**. Fältet **justeringsstatus** på de återförda verkliga värdena ställs till att värdet **inte justerat** och faktureringsstatus är **annullerad**.

När ändringarna har gjorts bokförs det belopp som har registrerats som förbrukat i projektet och den totala förväntande omsättningen i projektet tar längre tid för de belopp som dessa faktiska värden representerar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]