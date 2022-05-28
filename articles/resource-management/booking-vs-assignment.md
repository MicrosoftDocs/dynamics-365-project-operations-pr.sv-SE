---
title: Bokningar kontra tilldelningar
description: I det här ämnet finns information om skillnaderna mellan resursbokningar och resurstilldelningar.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b06555ec48e50f88c11872336539ca88c5cef34a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591289"
---
# <a name="bookings-vs-assignments"></a>Bokningar kontra tilldelningar

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Bokningar är en fast eller preliminär allokering av resurser till ett projekt. Fasta bokningar förbrukar en resurs kapacitet. Bokningar representerar organisationskoncept för grupper så att de kan förstå hur resurser ska engageras mellan olika projekt. Dynamics 365 Project Operations betraktar bokningar som ett koncept på projektnivå. 

Till skillnad från bokningar är tilldelningar åtagande av resurser till projektuppgifter i projektschemat. Resurserna kan vara namngivna eller generiska.  När ett resurskrav härleds från projektuppgiftstilldelningarna använder Project Operations insatsprofilerna från resurstilldelningen för att skapa informationsprofiler om resurskrav. En referens till resurstilldelningarna bibehålls emellertid inte. Uppdateringar av de bokningar som härleds från resurskravet uppdaterar inga resurstilldelningar.

Vanligtvis är summan av bokningarna för en resurs lika med summan av resursens tilldelningar för en eller flera uppgifter. Project Operations verkställer emellertid inte detta avtal. I vyn **avstämning** visas en projektledare där resursens bokningar och tilldelningar inte godkänner varandra.




[!INCLUDE[footer-include](../includes/footer-banner.md)]