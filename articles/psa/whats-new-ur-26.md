---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 26, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 26, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: cebfcd6425f11b74ce6331a093d8d3db3da356a0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577304"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation uppdateringsversion 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I det här ämnet finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation, uppdateringsversion 26, version 3. Denna version har versionsnummer V3.10.44.59 och är allmänt tillgänglig via en självuppdatering i december 2020.

## <a name="update-release-26"></a>Uppdatering version 26

### <a name="bug-fixes"></a>Felkorrigeringar

**Tid och utgift**

Följande problem har åtgärdats:

- Användare har möjlighet att ändra uppgiften på en tidspost som har godkänts/skickats.
- "Object Reference Not Set"-fel när du sparar tidspost.
- Tidspostimport från resurstilldelningar skapar tidsposter med de felaktiga DateTime-värdena.
- När Project Service Automation och Field Service-appen båda är installerade visas knappen **Nytt** två gånger i kommandofältet för tidsposter i Field Service-appen.
- Celluppdateringarna **Tillåt enhet** och **Enhetsgrupp** fungerar nu för rutnätet **Utgiftsuppskattningar**.
- Formuläret **Uppdatera tidspost** innehåller **Tidslinje**.
- Tidsgodkännande för icke-projekttidsposter blockerar systemet vid sökning efter en godkännar-roll för projektet.

**Resurshantering**

Följande problem har åtgärdats:

- Lade till validering i plugin-programmet **PostProjectCreate** för att kontrollera om det finns ett primärt krav innan ett sådant skapas.
- Snabbformuläret **Medlem i projektteam** avger ett nollreferensundantag om fält tas bort från formuläret.
- Genererande av krav för 12 timmar över 1 år kommer att misslyckas.
- Förbättrat nollreferensundantag för felmeddelande vid skapande av resurskrav.

**Projektledning**

Följande problem har åtgärdats:

- Förbättrad validering för att adressera nollreferensundantag som genereras i plugin-programmet **PreProjectUpdate**.
- Projekt som publiceras av det stationära Microsoft Project-tillägget tar bort ej tilldelade tilldelningar.
- Lade till ny validering när en uppgifts projektreferens är ogiltig på grund av nollreferensundantag i plugin-programmet **PreValidateProjectTaskUpdate**.
- Rutnätet gruppmedlem visar inte distinkta tilldelningar i gruppmedlemsposten.
- Lade till nya verifierings- och felmeddelanden på grund av nollreferensundantag i plugin-programmet **PreProjectTaskDelete**.

**Sales**

Följande problem har åtgärdats:

- Vid val av en projektbaserad rad inom en offert eller ett kontrakt ska knappen **Förslag** endast vara synlig när du väljer en produktbaserad rad som är kopplad till en befintlig produkt.
- Spearera privilegiet **Skapa_produkt** från privilegiet **Skapa_projektkontrakt**.
- Om du tar bort en fakturarad orsakas ett nollreferensfel i **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
