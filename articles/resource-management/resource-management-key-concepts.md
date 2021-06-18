---
title: Nyckelkoncept för resurshantering
description: I det här ämnet finns information om resurshanteringsfunktioner i Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6362daab7e2e01c7b7b2c2b801fe7e258b21ef16
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000998"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="06e43-103">Nyckelkoncept för resurshantering</span><span class="sxs-lookup"><span data-stu-id="06e43-103">Resource management key concepts</span></span>

<span data-ttu-id="06e43-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="06e43-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="06e43-105">Resurser är den viktigaste tillgången i en tjänstebaserad organisation.</span><span class="sxs-lookup"><span data-stu-id="06e43-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="06e43-106">Förmågan att hitta rätt resurser vid rätt tidpunkt, boka resurser på projekt och hålla dem utnyttjade, hjälper organisationen att uppfylla intäktsmål och kundnöjdhetsmål.</span><span class="sxs-lookup"><span data-stu-id="06e43-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="06e43-107">Du kan använda funktionen för resurshantering för projekt i Dynamics 365 Project Operations för att göra följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="06e43-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="06e43-108">Skapa projektteam genom att boka tillgängliga och kvalificerade resurser.</span><span class="sxs-lookup"><span data-stu-id="06e43-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="06e43-109">Skapa generiska teammedlemsposter och definiera deras roller och resursorganisationsenhet.</span><span class="sxs-lookup"><span data-stu-id="06e43-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="06e43-110">Generera resurskrav för generiska teammedlemmar från deras uppdrag.</span><span class="sxs-lookup"><span data-stu-id="06e43-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="06e43-111">Matcha färdigheter genom att identifiera de färdigheter som definieras i resursbehovet mot tillgängliga resursfärdigheter.</span><span class="sxs-lookup"><span data-stu-id="06e43-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="06e43-112">Ersättningsresurser.</span><span class="sxs-lookup"><span data-stu-id="06e43-112">Substitute resources.</span></span>
- <span data-ttu-id="06e43-113">Justera projektschemauppdrag och resursbokningar.</span><span class="sxs-lookup"><span data-stu-id="06e43-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="06e43-114">Stämma av skillnader i bokningar och uppdrag.</span><span class="sxs-lookup"><span data-stu-id="06e43-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="06e43-115">Ändra resursbokningar som svar på statusen ej på kontoret.</span><span class="sxs-lookup"><span data-stu-id="06e43-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="06e43-116">Samarbeta mellan projektledare och resurschefer.</span><span class="sxs-lookup"><span data-stu-id="06e43-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="06e43-117">Se historien om resursutnyttjandet mot ett mål, inklusive en uppdelning av hur resursernas tid användes.</span><span class="sxs-lookup"><span data-stu-id="06e43-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="06e43-118">Håll en databas för kunskaper och färdigheter.</span><span class="sxs-lookup"><span data-stu-id="06e43-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="06e43-119">Du kan bemanna ditt projekt med ett team av generiska eller namngivna resurser i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="06e43-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="06e43-120">Du kan använda olika metoder för att lägga till och tilldela teammedlemmar och för att hantera deras bokningar och uppdrag.</span><span class="sxs-lookup"><span data-stu-id="06e43-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]