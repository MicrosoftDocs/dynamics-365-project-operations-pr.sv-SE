---
title: Nyckelkoncept för resurshantering
description: I det här ämnet finns information om resurshanteringsfunktioner i Microsoft Dynamics Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 124d9bad5cc0c16955417a8213db047a2d8bae1d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085387"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="cb65c-103">Nyckelkoncept för resurshantering</span><span class="sxs-lookup"><span data-stu-id="cb65c-103">Resource management key concepts</span></span>

<span data-ttu-id="cb65c-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="cb65c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cb65c-105">Resurser är den viktigaste tillgången i en tjänstebaserad organisation.</span><span class="sxs-lookup"><span data-stu-id="cb65c-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="cb65c-106">Förmågan att hitta rätt resurser vid rätt tidpunkt, boka resurser på projekt och hålla dem utnyttjade, hjälper organisationen att uppfylla intäktsmål och kundnöjdhetsmål.</span><span class="sxs-lookup"><span data-stu-id="cb65c-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="cb65c-107">Du kan använda funktionen för resurshantering för projekt i Dynamics 365 Project Operations för att göra följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="cb65c-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="cb65c-108">Skapa projektteam genom att boka tillgängliga och kvalificerade resurser.</span><span class="sxs-lookup"><span data-stu-id="cb65c-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="cb65c-109">Skapa generiska teammedlemsposter och definiera deras roller och resursorganisationsenhet.</span><span class="sxs-lookup"><span data-stu-id="cb65c-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="cb65c-110">Generera resurskrav för generiska teammedlemmar från deras uppdrag.</span><span class="sxs-lookup"><span data-stu-id="cb65c-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="cb65c-111">Matcha färdigheter genom att identifiera de färdigheter som definieras i resursbehovet mot tillgängliga resursfärdigheter.</span><span class="sxs-lookup"><span data-stu-id="cb65c-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="cb65c-112">Ersättningsresurser.</span><span class="sxs-lookup"><span data-stu-id="cb65c-112">Substitute resources.</span></span>
- <span data-ttu-id="cb65c-113">Justera projektschemauppdrag och resursbokningar.</span><span class="sxs-lookup"><span data-stu-id="cb65c-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="cb65c-114">Stämma av skillnader i bokningar och uppdrag.</span><span class="sxs-lookup"><span data-stu-id="cb65c-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="cb65c-115">Ändra resursbokningar som svar på statusen ej på kontoret.</span><span class="sxs-lookup"><span data-stu-id="cb65c-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="cb65c-116">Samarbeta mellan projektledare och resurschefer.</span><span class="sxs-lookup"><span data-stu-id="cb65c-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="cb65c-117">Se historien om resursutnyttjandet mot ett mål, inklusive en uppdelning av hur resursernas tid användes.</span><span class="sxs-lookup"><span data-stu-id="cb65c-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="cb65c-118">Håll en databas för kunskaper och färdigheter.</span><span class="sxs-lookup"><span data-stu-id="cb65c-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="cb65c-119">Du kan bemanna ditt projekt med ett team av generiska eller namngivna resurser i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="cb65c-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="cb65c-120">Du kan använda olika metoder för att lägga till och tilldela teammedlemmar och för att hantera deras bokningar och uppdrag.</span><span class="sxs-lookup"><span data-stu-id="cb65c-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 
