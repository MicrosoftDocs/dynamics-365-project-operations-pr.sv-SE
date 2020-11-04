---
title: Uppdatera ett projekt
description: I det här ämnet finns information om uppdatering av projekt i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085395"
---
# <a name="update-a-project"></a>Uppdatera ett projekt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Nedan visas en sammanfattning av de fält som kan uppdateras i ett projekt efter att det har skapats och alla relevanta effekter av uppdateringarna.

## <a name="project-detail-fields"></a>Projektinformationsfält

- **Namn** : Projektets namn.
- **Beskrivning** : En översikt över projektet.
- **Kund** : Företaget som projektet ska levereras till.
- **Kalendermall** : Arbetstimmarna för projektet. När fältet ändras beräknas hela schemat om.
- **Valuta** : Valutan för projektet. Det här fältet hämtas baserat på valutan som definieras i kontrakteringsenheten. När kontrakteringsenheten uppdateras uppdateras även fältet.
- **Kontrakteringsenhet** : Den organisationsenhet som representerar den företagsgrupp eller avdelning som framför allt är ansvarig för att ta hem försäljningen och hantera leveransen av arbetet och tjänsterna till kunden. 
- **Projektledare** : Den medlem i projektteamet som har behörighet att granska och godkänna tidsposter och utgifter.

## <a name="estimate-fields"></a>Uppskattningsfält

- **Uppskattat startdatum** : Datumet då projektet kommer att starta. När det här fältet uppdateras kommer alla uppgifter i projektet att förskjutas proportionerligt med det nya startdatumet.
- **Slutdatum** : Datumet då projektet planeras sluta.
- **Insats** : Projektets uppskattade insats. När uppgifter läggs till i projektet går det inte längre att redigera det här fältet.
- **Uppskattad arbetskostnad** : Projektets uppskattade arbetskostnad. När arbetskostnader läggs till i projektet går det inte längre att redigera det här fältet.
- **Uppskattade utgifter** : Projektets uppskattade utgifter. När utgifter läggs till i projektet går det inte längre att redigera det här fältet.

## <a name="project-actual-fields"></a>Fält för projektets faktiska värden
- **Faktisk start** : Datumet då projektet startades.
- **Faktiskt slut** : Uppdateras när ett projekt har slutförts.

## <a name="project-status-fields"></a>Projektstatusfält

- **Övergripande projektstatus** : Det övergripande projekthälsotillståndet från projektledaren.
- **Kommentarer** : om den aktuella hälsan för projektet som projektledaren har tillhandahållit.

