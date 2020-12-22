---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 26, version 3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643285"
---
<a name="project-service-automation-update-release-26-v3"></a>Project Service Automation uppdateringsversion 26, V3
================================================

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I det här ämnet finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation, uppdateringsversion 26, version 3. Denna version har versionsnummer V3.10.44.59 och är allmänt tillgänglig via en självuppdatering i december 2020.

<a name="update-release-26"></a>Uppdatering version 26
-----------------

### <a name="bug-fixes"></a>Felkorrigeringar

**Tid och utgift**

Följande problem har åtgärdats:

-   Användare har möjlighet att ändra uppgiften på en tidspost som har godkänts/skickats.

-   "Object Reference Not Set"-fel när du sparar tidspost.

-   Tidspostimport från resurstilldelningar skapar tidsposter med de felaktiga DateTime-värdena.

-   När Project Service Automation och Field Service-appen båda är installerade visas knappen **Nytt** två gånger i kommandofältet för tidsposter i Field Service-appen.

-   Celluppdateringarna **Tillåt enhet** och **Enhetsgrupp** fungerar nu för rutnätet **Utgiftsuppskattningar**.

-   Formuläret **Uppdatera tidspost** innehåller **Tidslinje**.

-   Tidsgodkännande för icke-projekttidsposter blockerar systemet vid sökning efter en godkännar-roll för projektet.

**Resurshantering**

Följande problem har åtgärdats:

-   Lade till validering i plugin-programmet **PostProjectCreate** för att kontrollera om det finns ett primärt krav innan ett sådant skapas.

-   Snabbformuläret **Medlem i projektteam** avger ett nollreferensundantag om fält tas bort från formuläret.

-   Genererande av krav för 12 timmar över 1 år kommer att misslyckas.

-   Förbättrat nollreferensundantag för felmeddelande vid skapande av resurskrav.

**Projektledning**

Följande problem har åtgärdats:

-   Förbättrad validering för att adressera nollreferensundantag som genereras i plugin-programmet **PreProjectUpdate**.

-   Projekt som publiceras av det stationära Microsoft Project-tillägget tar bort ej tilldelade tilldelningar.

-   Lade till ny validering när en uppgifts projektreferens är ogiltig på grund av nollreferensundantag i plugin-programmet **PreValidateProjectTaskUpdate**.

-   Rutnätet gruppmedlem visar inte distinkta tilldelningar i gruppmedlemsposten.

-   Lade till nya verifierings- och felmeddelanden på grund av nollreferensundantag i plugin-programmet **PreProjectTaskDelete**.

**Sales**

Följande problem har åtgärdats:

-   Vid val av en projektbaserad rad inom en offert eller ett kontrakt ska knappen **Förslag** endast vara synlig när du väljer en produktbaserad rad som är kopplad till en befintlig produkt.

-   Spearera privilegiet **Skapa_produkt** från privilegiet **Skapa_projektkontrakt**.

-   Om du tar bort en fakturarad orsakas ett nollreferensfel i **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.
