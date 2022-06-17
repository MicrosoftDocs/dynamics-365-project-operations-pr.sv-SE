---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 18, V3
description: Den här artikeln innehåller funktioner och korrigeringar som är tillgängliga i Project Service Automation uppdateringsutgåva 18, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: e8d423c550d9aa09c9cbb7d4f7c277c43bbe10ae
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918886"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation uppdateringsversion 18, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för Project Service Automation, V3, uppdateringsversion 18. Den här versionen har ett versionsnummer på V3.10.8.12 och är allmänt tillgänglig via en självuppdatering i april 2020.

## <a name="update-release-18"></a>Uppdatering version 18

### <a name="bug-fixes"></a>Felkorrigeringar

**Tid och utgift**

- Korrigerat: Flödena **Återkalla**, **Begär** och **Avbryt godkännande** skapar undantag med oklara felmeddelanden.
- Korrigerat: När **Avbryt godkännande** misslyckas för en utgift uppstår inte ett relevant undantagsfel.
- Korrigerat: rutnätet för tidsinmatning hanterar felaktigt lediga dagar i Australien efter växling av sommartid (DST) i oktober.
- Korrigerat: felaktig standardlogik förhindrar att utgifter skickas.
- Korrigerat: när godkännande av tidsinmatning misslyckas förblir godkännandet i ett **pågående** tillstånd.
- Korrigerat: SQL-fel i massgodkännanden (deadlock/tidsgräns).
- Korrigerat: viktiga prestandaproblem i användargränssnittet som orsakas av uppdatering av teammedlemmar under godkännande av tidsposter.

**Projektledning**

- Korrigerat: ett tidszonsmeddelande har flyttats från vyn **Avstämning** till vyn **Projekt**.
- Korrigerat: kalendermallen återställs inte korrekt till standardvärdet när ett nytt projektformulär öppnas.
- Korrigerat: för chromiumbaserade webbläsare kan användare inte enkelt välja de föregående aktiviteter som ska tas bort.
- Korrigerat: att skapa eller kopiera **Projekt från en tom mall** hämtar orelaterade uppgifter.
- Korrigerat: i specifika fall innebär en ny uppgift från aktivitetsrutnätet att det skapas dubbla poster.
- Korrigerat: i manuellt läge kan användare inte uppdatera uppgiftens startdatum innan det aktuella datumet har sparats.

**Resurshantering**

- Korrigerat: Vyn **avstämning** visa raden delsummor beräknar felaktigt bokningsavvikelse var för sig efter förlängning av bokningar.
- Korrigerat: Vyn **Avstämning** visar felaktigt resurstilldelningar när den bokningsbara resursen har en kalender som inte överensstämmer med projektkalendern.

**Sales**

- Korrigerat: När tidsposter godkänns igen (**Godkänn > Annullera >** Godkänn igen) skapas en dubblett av den verkliga transaktionen som inte kan debiteras.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
