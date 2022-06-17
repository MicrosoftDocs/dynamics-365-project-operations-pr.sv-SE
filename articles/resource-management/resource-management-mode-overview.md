---
title: Resurshanteringslägen – Översikt
description: Den här artikeln innehåller information om resurshanteringsfunktioner i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dd50d12686a6ad17f6a95ccf0c2f1447cc470bf7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928454"
---
# <a name="resource-management-modes-overview"></a>Resurshanteringslägen – Översikt

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_


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

Utöver den centrala lägesprocessen som stöds, se följande artiklar för att hantera alla andra stödda bokningsflöden i hybridläget:

Boka en resurs direkt till ett projekt:
- [Boka namngivna bokningsbara resurser till ett projektgrupp och tilldela dem uppgifter](/dynamics365/project-service/assign-named-bookable-resource)

Boka en resurs från ett resurskrav:
- [Tilldela generiska bokningsbara resurser en uppgift och generera resursbehov](/dynamics365/project-service/assign-generic-bookable-resource)
- [Boka namngivna resurser från resurskrav](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]