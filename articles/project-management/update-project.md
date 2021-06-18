---
title: Uppdatera ett projekt
description: I det här ämnet finns information om uppdatering av projekt i Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c07542444b970430d8143a60aad6970305769b22
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993393"
---
# <a name="update-a-project"></a>Uppdatera ett projekt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Nedan visas en sammanfattning av de fält som kan uppdateras i ett projekt efter att det har skapats och alla relevanta effekter av uppdateringarna.

## <a name="project-detail-fields"></a>Projektinformationsfält

- **Namn**: Projektets namn.
- **Beskrivning**: En översikt över projektet.
- **Kund**: Företaget som projektet ska levereras till.
- **Kalendermall**: Arbetstimmarna för projektet. När fältet ändras beräknas hela schemat om.
- **Valuta**: Valutan för projektet. Det här fältet hämtas baserat på valutan som definieras i kontrakteringsenheten. När kontrakteringsenheten uppdateras uppdateras även fältet.
- **Kontrakteringsenhet**: Den organisationsenhet som representerar den företagsgrupp eller avdelning som framför allt är ansvarig för att ta hem försäljningen och hantera leveransen av arbetet och tjänsterna till kunden. 
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