---
title: Kostnad för slutförandemetoder
description: Detta ämne innehåller information om de metoder som används för att beräkna kostnaden för att slutföra ett projekt.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531568"
---
# <a name="cost-to-complete-methods"></a>Kostnad för slutförandemetoder

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Detta ämne innehåller information om de metoder som används för att beräkna kostnaden för att slutföra ett projekt. Det finns flera metoder som du kan använda för att beräkna kostnaden för att slutföra ett projekt. 

När du skapar en uppskattning för ett projekt kan du på sidan **Skapa uppskattning**, i fältet **Kostnad för att slutföra metod**, välja någon av följande kostnader för att slutföra metoder.

| Kostnad för att slutföra metod    | Beskrivning                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Total kostnad – faktisk            | Ange uppskattningskostnader manuellt i fälten **Totalkostnad** eller **Total kvantitet** med hjälp av knappen **Kostnadsuppskattning** på **sidan Uppskattning**. Systemet subtraherar de faktiska kostnaderna från de summor du angett. Summan är kostnaden för att slutföra projektet. Den här metoden använder inte utgiftsuppskattningar och resurstilldelningar som angetts i Project Operations som skapats i Microsoft Dataverse. Den totala kostnaden eller den totala kvantiteten kan uppdateras manuellt efter behov.  |
| Total faktisk prognos        | Resurstilldelningar och utgiftsuppskattningar används för att fastställa det totala projektprognosbeloppet. Faktiska kostnader jämförs mot denna prognos för att beräkna kostnaden som ska slutföras.                                                                                                                                                                                                                                                                          |
| Som föregående uppskattning         | Här används samma uppskattningsmetoder som användes under föregående period. Den här metoden kräver en prognosmodell om den föregående perioden kräver en prognosmodell.                                                                                                                                                                                                                                                                                                                           |
| Ange att kostnaden ska slutföras till noll | Denna metod används vanligtvis innan uppskattningsprojektet elimineras, matchar totala uppskattningar med bokförda faktiska transaktioner och avmarkerar kolumnen **Kostnad för att slutföra**. Efter slutförande blir resultatet alltid 100 procent. För varje kostnadsrad som du skapar avmarkeras kryssrutan **Prognosticering** och den totala uppskattningen kopieras från den föregående kostnadsuppskattningen. Den faktiska förbrukningen för uppskattningsperioden dras från kostnaden för att slutföra projektet.              |
| Från kostnadsmall           | Kostnaden för att slutföra den konfigurerade metoden i kostnadsmallen som är kopplad till det valda uppskattningsprojektet.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]