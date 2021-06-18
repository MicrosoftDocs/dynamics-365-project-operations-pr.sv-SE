---
title: Varför kan jag inte ta bort poster från entiteten Faktiska värden?
description: I det här ämnet finns information om varför det inte går att ta bort poster från entiteten verkliga värden.
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 434be93cedb4772616b1e6d5cbe15fc715eed19a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993123"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="a5952-103">Varför kan jag inte ta bort poster från entiteten Faktiska värden?</span><span class="sxs-lookup"><span data-stu-id="a5952-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a5952-104">Med Project Service Automation (PSA) kan du inte ta bort faktiska värden eftersom de fungerar som källa till sanningen för transaktioner som har ekonomiska effekter för underordnade system, t.ex. redovisningen.</span><span class="sxs-lookup"><span data-stu-id="a5952-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="a5952-105">Om verkliga värden kan tas bort kan det krävas att den ekonomiska rapporttransaktionens integritet ifrågasätts.</span><span class="sxs-lookup"><span data-stu-id="a5952-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="a5952-106">För att kunna upprätta en granskningskedja bör kunderna använda journaler för att skapa kompensationstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a5952-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]