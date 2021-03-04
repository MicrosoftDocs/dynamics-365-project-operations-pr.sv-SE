---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 21, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 21, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: b1194c1cf1997b68030fe88360c6ebb756c715fd
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147045"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation uppdateringsversion 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 21. Den här versionen har ett versionsnummer på V 3.10.32.50 och är allmänt tillgänglig via en självuppdatering i juni 2020.

## <a name="update-release-21"></a>Uppdatering version 21

### <a name="bug-fixes"></a>Felkorrigeringar

**Tid och utgift**

Följande problem har åtgärdats:

- När du är värd för **kontrollen rutnät för tidspost** i instrumentpaneler används inte rutnätets fulla bredd i instrumentpanelens behållare.
- För specifika tidszoner visas inte posterna för rutnätskontrollen **tidsinmatning**.
- Tidsposter efter 21:00 visas på fel dag.
- Användarna kan inte skicka utgifter om utgiftskategorin, om **utgiftsinleveransen** inte har något värde.

**Resurshantering**

Följande problem har åtgärdats:

- Inaktiva bokningar visas i vyn **avstämning**.
- En allmän resursuppfyllelse saknar verifiering för att se till att det finns en giltig bokningsstatus.

**Projektledning**

Följande problem har åtgärdats:

- Formulärets rutnät **Projekt** (vyn **Resurstilldelning**, **Uppgift**, **Avstämning**, **Utgiftsuppskattningar**) är fortfarande redigerbara även när ett projekt inte är aktivt.
- Dubbletter av kunder kan inte kopplas till kunder som är länkade till bekräftade projekt kontrakt.
- När en resurs som inte har en giltig kalender läggs till returnerar systemet inte ett användarvänligt felmeddelande.
- Knappen **Lägg till uppgift** i rutnätet aktiveras när projektet länkas till ett **Microsoft Project-tillägg**.
- Insatsen växer okontrollerat när en uppgift med en kategori tilldelas en resurs med en roll för vilken en självkostnad har definierats.

**Sales**

Följande förbättringar har gjorts:

- **Faktureringsfrekvens** och **faktureringsstart** har flyttats till fliken **fakturaschema**.

Följande problem har åtgärdats:

- **Totalt försäljningspris** är noll (0) för **kategori** även om **roll** har ett totalt försäljningspris som inte är noll.
- Kunder kan inte ändra värdet i fältet **fakturastatus** till **klar för fakturering** när en annan anpassad process uppdaterar ett extra fält.
- Med knappen **Uppdatera fakturarader** kan du skapa flera duplicerade rader om alternativet markeras flera gånger.
- Knappen **Uppdatera priser** fungerar inte i underrutnätet **Rollpriser** i formuläret **Snabbvy**.
- Logiken **Stängning av prislista för försäljning** hanterar tidszoner felaktigt, vilket resulterar i ett felaktigt urval av prislistor.
- Ett projekts **Total faktisk kostnad** kan avgränsas med ett decimal belopp efter att en enskild tid har godkänts.
- Logiken **Prismatchning** ger inte ett användarvänligt felmeddelande om **Hämta RolePrice** inte har värden i fälten **primär enhet** och **pris i primär enhet**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]