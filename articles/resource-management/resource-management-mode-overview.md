---
title: Översikt över resurshanteringslägen
description: I det här ämnet finns information om resurshanteringsfunktioner i Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930113"
---
# <a name="resource-management-modes-overview"></a>Översikt över resurshanteringslägen

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_


Dynamics 365 Project Operations stöder två lägen för att du ska kunna utföra hela bokningsflödet. Hanteringsläget definieras som en projektparameter och kan ändras om företagets behov ändras.    

## <a name="central-mode"></a>Centralt läge
För organisationer som centraliserar tilldelningen för resurser till projekt, kan du med hjälp av centralläget se till att projektledarna kan definiera resurskrav på projektnivå. Uppfyllelse av resurskraven delegeras till en resursansvarig. Projektledarna kan acceptera eller avvisa resurser som föreslås av den resursansvariga.

![Centralt läge](./media/resource-management-central.png)

Information om hur du hanterar resurser med centralt läge finns i:

- [Tilldela generiska bokningsbara resurser en uppgift och generera resursbehov](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Boka namngivna resurser från resurskrav](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Skicka en resursbegäran](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Uppfyll en resursförfrågning](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Acceptera eller avvisa en föreslagen projektresurs från en resursförfrågan](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybridläge
För organisationer som behöver flexibilitet i tilldelningen av resurser innebär hybridläget att både projektledarna och resursansvariga kan boka resurser.

![Hybridläge](./media/resource-management-hybrid.png)

Utöver den centrallägesprocess som stöds, se följande avsnitt för att hantera alla andra bokningsflöden som stöds i hybridläget:

Boka en resurs direkt till ett projekt:
- [Boka namngivna bokningsbara resurser till ett projektgrupp och tilldela dem uppgifter](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Boka en resurs från ett resurskrav:
- [Tilldela generiska bokningsbara resurser en uppgift och generera resursbehov](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Boka namngivna resurser från resurskrav](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
