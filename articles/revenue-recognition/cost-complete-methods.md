---
title: Kostnad för slutförandemetoder
description: Den här artikeln innehåller information om de metoder som används för att beräkna kostnaden för att slutföra ett projekt.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 39c10673afd04ad7d4a94a01211c2f9d335a02c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920312"
---
# <a name="cost-to-complete-methods"></a>Kostnad för slutförandemetoder

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Den här artikeln innehåller information om de metoder som används för att beräkna kostnaden för att slutföra ett projekt. Det finns flera metoder som du kan använda för att beräkna kostnaden för att slutföra ett projekt. 

När du skapar en uppskattning för ett projekt kan du på sidan **Skapa uppskattning**, i fältet **Kostnad för att slutföra metod**, välja någon av följande kostnader för att slutföra metoder.

| Kostnad för att slutföra metod    | Beskrivning                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Total kostnad – faktisk            | Ange uppskattningskostnader manuellt i fälten **Totalkostnad** eller **Total kvantitet** med hjälp av knappen **Kostnadsuppskattning** på **sidan Uppskattning**. Systemet subtraherar de faktiska kostnaderna från de summor du angett. Summan är kostnaden för att slutföra projektet. Den här metoden använder inte utgiftsuppskattningar och resurstilldelningar som angetts i Project Operations som skapats i Microsoft Dataverse. Den totala kostnaden eller den totala kvantiteten kan uppdateras manuellt efter behov.  |
| Total faktisk prognos        | Resurstilldelningar och utgiftsuppskattningar används för att fastställa det totala projektprognosbeloppet. Faktiska kostnader jämförs mot denna prognos för att beräkna kostnaden som ska slutföras.                                                                                                                                                                                                                                                                          |
| Som föregående uppskattning         | Här används samma uppskattningsmetoder som användes under föregående period. Den här metoden kräver en prognosmodell om den föregående perioden kräver en prognosmodell.                                                                                                                                                                                                                                                                                                                           |
| Ange att kostnaden ska slutföras till noll | Denna metod används vanligtvis innan uppskattningsprojektet elimineras, matchar totala uppskattningar med bokförda faktiska transaktioner och avmarkerar kolumnen **Kostnad för att slutföra**. Efter slutförande blir resultatet alltid 100 procent. För varje kostnadsrad som du skapar avmarkeras kryssrutan **Prognosticering** och den totala uppskattningen kopieras från den föregående kostnadsuppskattningen. Den faktiska förbrukningen för uppskattningsperioden dras från kostnaden för att slutföra projektet.              |
| Från kostnadsmall           | Kostnaden för att slutföra den konfigurerade metoden i kostnadsmallen som är kopplad till det valda uppskattningsprojektet.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]