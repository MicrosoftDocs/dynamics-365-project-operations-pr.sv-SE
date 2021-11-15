---
title: Skapa och uppdatera en projektmall
description: I det här ämnet finns information om uppdatering av projekt i Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d0847b5343cf3e353b91eae04c94509f14213ba5
ms.sourcegitcommit: 51224cb3bf7cdeae6614d39fc8d899c83dbad5f2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7678371"
---
# <a name="create-and-update-a-project"></a>Skapa och uppdatera en projektmall

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Följande är en sammanfattning av fälten som kan uppdateras för ett projekt efter att det har skapats. Detta omfattar även eventuella tillämpliga effekter som bygger på dessa uppdateringar.

## <a name="project-detail-fields"></a>Projektinformationsfält

- **Namn**: Projektets namn.
- **Beskrivning**: En översikt över projektet.
- **Kund**: Företaget som projektet ska levereras till.
- **Kalendermall**: Arbetstimmarna för projektet. När fältet ändras beräknas hela schemat om.
- **Valuta**: Valutan för projektet. Standardvärdet för det här fältet baseras på valutan som definierats i kontraktenheten. När kontrakteringsenheten uppdateras uppdateras även fältet.
- **Kontrakteringsenhet**: Den organisationsenhet som representerar den företagsgrupp eller avdelning som framför allt är ansvarig för att ta hem försäljningen och hantera leveransen av arbetet och tjänsterna till kunden.  När projektledarens organsationsenhet inte är definierad använder detta fält det värde som definierats i projektparametrarna som standarvärde.
- **Projektledare**: Den medlem i projektteamet som har behörighet att granska och godkänna tidsposter och utgifter.

## <a name="estimate-fields"></a>Uppskattningsfält

- **Uppskattat startdatum** : Datumet då projektet kommer att starta. När det här fältet uppdateras kommer alla uppgifter i projektet att förskjutas proportionerligt med det nya startdatumet.
- **Slutdatum**: Datumet då projektet planeras sluta.
- **Insats**: Projektets uppskattade insats. När uppgifter läggs till i projektet går det inte längre att redigera det här fältet.
- **Uppskattad arbetskostnad**: Projektets uppskattade arbetskostnad. När arbetskostnader läggs till i projektet går det inte längre att redigera det här fältet.
- **Uppskattade utgifter**: Projektets uppskattade utgifter. När utgifter läggs till i projektet går det inte längre att redigera det här fältet.

## <a name="project-actual-fields"></a>Fält för projektets faktiska värden
- **Faktisk start** : Datumet då projektet startades.
- **Faktiskt slut**: Uppdateras när ett projekt har slutförts.

## <a name="project-status-fields"></a>Projektstatusfält

- **Övergripande projektstatus**: Det övergripande projekthälsotillståndet från projektledaren.
- **Kommentarer**: om den aktuella hälsan för projektet som projektledaren har tillhandahållit.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
