---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 15, version 3
description: I den här artikeln finns information om vad som är nytt och ändrat i Project Service Automation, uppdateringsversion 15, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: b87cae2cd8913457c2931d1661a57509d1398d29
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915666"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation uppdateringsversion 15, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi är glada att kunna presentera den senaste uppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet. Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet. Den här versionen är kompatibel med Dynamics 365 9.x. Om du vill uppdatera till den här utgåvan går du till administrationscenter för Dynamics 365 online och går till sidan lösningar för att installera uppdateringen. Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).

I denna artikel finns funktioner och korrigeringar som är nya eller har ändrats för PSA, V3, uppdateringsversion 15. Den här versionen har ett versionsnummer på V-3.10.5.28 och är allmänt tillgänglig via en självuppdatering i januari 2020.

## <a name="update-release-15"></a>Uppdatering version 15 

### <a name="enhancements"></a>Förbättringar

- Projektledning

### <a name="bug-fixes"></a>Felkorrigeringar

- Tid och utgift

  - Fast: Lägg till felhantering vid laddning i vyn avstämning.
  - Fast: projektresursnav: Byt namn **Belopp** för att minska tvetydighet.
  - Fast: justera vyn **Kopiera kolumner för tidspost** så att de inkluderar typen.
  - Fast: när du redigerar tid i rutnätsvy med decimaltal uppstår ett okänt fel för vissa tal.

- Projektledning

  - Fast: den nedrullningsbara menyn för **används i spårningsvy** expanderas nu baserat på alternativets bredd.
  - Fast: när du hanterar projekt i + 13 tidszon kan du visa felaktiga resultat i aktivitetsberäkningar.
  - Fast: **Sluttid för teammedlem** har inte korrigerats när 24-timmarsformat används.
  - Fast: återaktiverade **BPF** i huvudformuläret **msdyn_project**.
  - Fast: beräkningen av tilldelningar ignorerar inte längre en dag.
  - Fast: ett nytt meddelandebanderoll har lagts till i projektformuläret när tidszonen skiljer sig mellan användare och projekt.

- Sales

  - Fast: sökning efter utgiftskategori för utgiftsbedömning kan användas för att filtrera dubbletter.
  - Fast: kod i **PluginDomain.ExecuteInTryCatchBlock(..)** döljer inte längre undantagets ursprung.
  - Fast: får inte längre ett felmeddelande i **projektsökning** i formuläret **offertrad** när det finns fler än 1000 projekt.
  - Fast: **uppskattning** rutnät för arbetsuppskattningar och utgiftsuppskattningar visar nu rätt valutasymbol.
  - Fast: när en organisation uppdaterar PSA från uppdatering version 14 till uppdatering version 15 visas inte längre fliken **schema** som tom i formuläret **projekt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
