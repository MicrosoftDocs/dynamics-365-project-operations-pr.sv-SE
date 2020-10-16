---
title: Utgiftsberäkningar
description: I det här ämnet finns information om hur du definierar eller uppskattar projektbaserade utgifter.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908648"
---
# <a name="expense-estimates"></a>Utgiftsberäkningar
_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Tillsammans med att definiera resursbaserade uppskattningar kan projektledare med hjälp av Dynamics 365 Project Operations definiera projektbaserade utgifter för varje projekt. Varje utgiftspost kan kopplas till en specifik projektuppgift eller utgiftskategori. Utgiftskategorier definieras vanligtvis på organisationsnivå. Prissättning för varje utgiftskategori definieras vanligtvis i följande hierarki:

- Organisation
- Kund
- Offert/kontrakt

Följ stegen nedan om du vill visa, lägga till eller ta bort en projektutgift.

1. Gå till **Projekt** och välj det projekt du vill arbeta med.
2. Välj fliken **Projektuppskattningar** och visa listan med projektutgifter.
3. Välj **Ny utgift** om du vill lägga till en utgift. Du kan också välja vilka utgifter som ska tas bort och sedan välja **Ta bort utgift**.

Följande attribut anges för varje utgiftsradartikel:

- **Kategori**: de vanliga grupperingarna som används för att beskriva alla utgifter som uppstått i ett projekt.
- **Startdatum**: det datum då utgiften bedöms bli påförd.
- **Antal**: uppskattat antal utgiftsartiklar för en specifik kategori.
- **Självkostnad per enhet**: det enhetspris som används för att beräkna kostnaden för utgiften.
- **Försäljningspris per enhet**: det enhetspris som används för att beräkna försäljningspriset för utgiften.

