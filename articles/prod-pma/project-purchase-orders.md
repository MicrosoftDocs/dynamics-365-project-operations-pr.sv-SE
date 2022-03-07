---
title: Inköpsorder för ett projekt
description: I den här artikeln beskrivs olika metoder som du kan använda för att skapa inköpsorder för ett projekt. Vilken metod du ska använda beror på inköpsorderns syfte och när de inköpta artiklarna förbrukas och debiteras ett projekt.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c3ce2d0c0fb3cecf22157db5cb37eb744027d0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999378"
---
# <a name="purchase-orders-for-a-project"></a>Inköpsorder för ett projekt

[!include [banner](../includes/banner.md)]

I den här artikeln beskrivs olika metoder som du kan använda för att skapa inköpsorder för ett projekt. Vilken metod du ska använda beror på inköpsorderns syfte och när de inköpta artiklarna förbrukas och debiteras ett projekt.

### <a name="methods-for-creating-a-purchase-order"></a>Metoder för att skapa en inköpsorder

Du kan använda någon av följande metoder för att skapa en inköpsorder i projektledning och redovisning. Syftet med inköpsordern avgör när inköpsordern konsumeras och därför när artiklar debiteras för ett projekt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metod</th>
<th>Syfte</th>
<th>Förbrukning av artiklar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Skapa en inköpsorder direkt från ett projekt.</td>
<td>Använd den här metoden om du vill köpa artiklar från en extern leverantör för förbrukning i ett projekt. Du kan skapa inköpsorder på två sätt:
<ul>
<li>Från själva projektet. I det här fallet är projektet redan definierat för inköpsordern.</li>
<li>Genom att navigera till projektets inköpsorder. Du måste välja både leverantören och projektet för att skapa inköpsordern.</li>
</ul></td>
<td>Artiklar förbrukas när leverantörsfakturan uppdateras.</td>
</tr>
<tr class="even">
<td>Skapa en inköpsorder från en försäljningsorder.</td>
<td>Använd den här metoden om du vill köpa artiklar när du skapar en försäljningsorder från ett projekt.</td>
<td>Artiklar förbrukas när försäljningsordern faktureras kunden.</td>
</tr>
<tr class="odd">
<td>Skapa en inköpsorder från ett artikelkrav.</td>
<td>Använd den här metoden om du vill köpa artiklar när du skapar ett artikelkrav från ett projekt.</td>
<td>Artiklar förbrukas när följesedeln för artikelkrav uppdateras.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> När du uppdaterar leverantörsfakturan eller följesedeln uppmanas du att uppdatera följesedeln på artikelkravet.

Mer information finns i [Ta emot varor på inköpsordern från artikelkravet](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]