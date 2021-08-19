---
title: Översikt över resurshanteringslägen
description: I det här ämnet finns information om funktionen för projekthantering i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 5c0f98a6f08129ebef9b6d3fed1cc85969aa347c815a643d3c8dd639b42c0e8c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008248"
---
# <a name="resource-management-modes-overview"></a>Resurshanteringslägen – Översikt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_


Dynamics 365 Project Operations har stöd för två lägen för att du ska kunna utföra det övergripande bokningsflödet. Hanteringsläget definieras som en projektparameter och kan ändras om företagets behov ändras.    

## <a name="central-mode"></a>Centralt läge
För organisationer som centraliserar tilldelningen för resurser till projekt, kan du med hjälp av centralläget se till att projektledarna kan definiera resurskrav på projektnivå. Uppfyllelse av resurskraven delegeras till en resursansvarig. Projektledarna kan acceptera eller avvisa resurser som föreslås av den resursansvariga.

![Centralt läge.](./media/resource-management-central.png)

Information om hur du hanterar resurser med centralt läge finns i:

- [Tilldela generiska bokningsbara resurser en uppgift och generera resursbehov](/dynamics365/project-service/assign-generic-bookable-resource)
- [Boka namngivna resurser från resurskrav](/dynamics365/project-service/book-named-resource)
- [Skicka en resursbegäran](/dynamics365/project-service/submit-resource-request)
- [Uppfyll en resursförfrågning](/dynamics365/project-service/resource-management-fulfill-requests)
- [Acceptera eller avvisa en föreslagen projektresurs från en resursförfrågan](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybridläge
För organisationer som behöver flexibilitet i tilldelningen av resurser innebär hybridläget att både projektledarna och resursansvariga kan boka resurser.

![Hybridläge.](./media/resource-management-hybrid.png)

Utöver den centrallägesprocess som stöds, se följande avsnitt för att hantera alla andra bokningsflöden som stöds i hybridläget:

Boka en resurs direkt till ett projekt:
- [Boka namngivna bokningsbara resurser till ett projektgrupp och tilldela dem uppgifter](/dynamics365/project-service/assign-named-bookable-resource)

Boka en resurs från ett resurskrav:
- [Tilldela generiska bokningsbara resurser en uppgift och generera resursbehov](/dynamics365/project-service/assign-generic-bookable-resource)
- [Boka namngivna resurser från resurskrav](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]