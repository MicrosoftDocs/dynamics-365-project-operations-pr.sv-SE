---
title: Varför kan jag inte ta bort poster från entiteten Faktiska värden?
description: I det här ämnet finns information om varför det inte går att ta bort poster från entiteten verkliga värden.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127180"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="642dd-103">Varför kan jag inte ta bort poster från entiteten Faktiska värden?</span><span class="sxs-lookup"><span data-stu-id="642dd-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="642dd-104">Med Project Service Automation (PSA) kan du inte ta bort faktiska värden eftersom de fungerar som källa till sanningen för transaktioner som har ekonomiska effekter för underordnade system, t.ex. redovisningen.</span><span class="sxs-lookup"><span data-stu-id="642dd-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="642dd-105">Om verkliga värden kan tas bort kan det krävas att den ekonomiska rapporttransaktionens integritet ifrågasätts.</span><span class="sxs-lookup"><span data-stu-id="642dd-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="642dd-106">För att kunna upprätta en granskningskedja bör kunderna använda journaler för att skapa kompensationstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="642dd-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

