---
title: Project Service Automation-integreringsparametrar
description: I det här ämnet beskrivs hur du konfigurerar hur standarddata ska anges när du integrerar Microsoft Dynamics 365 for Project Service Automation med Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b58f34cb74be531a98518100158f39d74f136afc34444468d666cd4e9394af6f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005863"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation-integreringsparametrar

[!include[banner](../includes/banner.md)]

På sidan **Project Service Automation integreringsparametrar** kan du konfigurera hur standarddata ska anges när du integrerar Dynamics 365 Project Service Automation med Dynamics 365 Finance. För att projekt ska kunna synkroniseras från Project Service Automation till Finance måste du konfigurera följande fält.

Öppna sidan **Project Service Automation integreringsparametrar**, gå till **Projektledning och redovisning** \> **konfiguration** \> **Dynamics 365 for Project Service Automation integreringsparameter**. 

> [!NOTE]
> - OProjektuppgift, kategorier för utgiftstransaktioner, timuppskattningar, utgiftsuppskattningar och funktionslåsning är tillgängliga i version 8.0.
> - Verklig integreringsfunktion kan starta i version 8.0.1 eller senare.


| Tabb                    | Fält                | Beskrivning |
|------------------------|----------------------|-------------|
| Allmän                | Standardprojekttyp | Välj standardprojekttyp. När projekt synkroniseras från Project Service Automation används värdet om du inte angav ett standardvärde i integrationsmallen. Under synkroniseringen anges fältet **projekttyp** för nya projekt till detta värde. Värdet kan emellertid uppdateras när projekt kontraktsraderna synkroniseras från Project Service Automation. |
|                        | Tidskategori        | Markera standardtidskategorin. Värdet används när timuppskattningar synkroniseras från Project Service Automation. När timberäkningarna och faktiska timmar synkroniseras från Project Service Automation, anges fältet **Kategori** för den nya prognosen för projekttid i Finance anges till detta värde. |
|                        | Avgiftskategori         | Markera standardavgiftskategorin. Värdet används när faktiska avgifter synkroniseras från Project Service Automation. När faktiska avgifter timmar synkroniseras från Project Service Automation, anges fältet **Kategori** för den nya avgiftstransaktionen i Finance anges till detta värde. |
| Standard för projektgrupp | Projekttyp         | Klicka på **ny** om du vill lägga till en rad där du kan välja projekt typen för att ange standardprojektgruppen. Du kan bara välja en specifik projekttyp en gång i konfigurationen. |
|                        | Projektgrupp        | Välj standardprojektgrupp för den valda projekttypen. När nya projekt synkroniseras från Project Service Automation anges fältet **Projektgrupp** till standardvärdet för projekttypen om du inte angav ett standardvärde i integrationsmallen. |
| Faktureringstyp standard  | Faktureringstyp         | Klicka på **ny** om du vill lägga till en rad där du kan välja faktureringstypen för att ange standard radegenskapen. Du kan bara välja en specifik faktureringstyp en gång i konfigurationen. |
|                        | Radegenskap        | Välj standard radegenskap för den valda faktureringstypen. Om nya timuppskattningar, nya utgiftsuppskattningar eller nya verkliga värden synkroniseras från Project Service Automation anges fältet **radegenskap** till standardvärdet för faktureringstypen. |
| Funktioner som låser  | Gäller inte       | Välj vilka funktioner som ska inaktiveras i Finance för projekt och kontrakt som härrör från Project Service Automation. Du kan till exempel inaktivera möjligheten att redigera kontrakt och projekt, skapa uppdelnings strukturer och ange tid rapporter i Finance. Redovisningsfält som är relaterade till poster aktiveras även om de inte är tillgängliga i parameterinställningarna. Som standard är alla funktioner aktiverade. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]