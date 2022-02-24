---
title: Hantera projektkontrakt
description: I det här ämnet finns information om att visa projektbaserade kontrakt.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441fbc378a423334f45bc65658811ef238515393
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177353"
---
# <a name="manage-project-contracts"></a>Hantera projektkontrakt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Projektkontrakt i Dynamics 365 Project Operations fångar in och hanterar avtalsenlig information om åtaganden och faktureringsuppgifter för ett projekt. Strukturen på ett projektkontrakt i Project Operation är skräddarsydd för projektbaserade funktioner med följande komponenter:

- Kontraktrader som identifierar de diskreta komponenterna i arbete som visas som högnivå komponenter på en projektfaktura.
- Kontraktradsinformation som identifierar och uppskattar arbetet för varje hög nivå komponent eller kontraktsrad. Uppskattningen inkluderar schema och finansiella aspekter för arbetet knutet till kontraktraden.
- Avtalade modeller och debiterbara komponenter skapas för varje kontraktrad som innehåller faktureringsöverenskommelsen för varje kontraktrad och hela kontraktet.

## <a name="view-all-project-based-contracts"></a>Visa alla projektbaserade kontrakt

En lista över alla projektkontrakt visas på listsidan **kontrakt**. 

1. Gå till **Försäljning** > **Kontakter**. En lista över alla projektkontrakt i systemet visas. 
2. Välj **Visa växlare** (listpilen bredvid vyns namn) om du vill välja andra filtrerade vyer. Du kan skapa egna vyer med villkor för anpassade filter.

Du kan skapa eller ta bort kontrakt från den här listsidan eller informationssidorna.
