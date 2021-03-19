---
title: Säkerhetsmodul
description: I det här ämnet finns information om säkerhetsmodellen i Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 3f65d13809fef342be8bec682c11d95c4d9e9b19
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276820"
---
# <a name="security-model"></a><span data-ttu-id="01b6c-103">Säkerhetsmodell</span><span class="sxs-lookup"><span data-stu-id="01b6c-103">Security Model</span></span>

<span data-ttu-id="01b6c-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="01b6c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="01b6c-105">Microsoft Dynamics 365 Project Operations innehåller en unik säkerhetsmodell som möjliggör en rollbaserad affärsmodell för verksamhetssäkerhet som samarbetar med Microsoft Office-grupper.</span><span class="sxs-lookup"><span data-stu-id="01b6c-105">Microsoft Dynamics 365 Project Operations contains a unique security model that allows for a role-based business security model that collaborates with Microsoft Office Groups.</span></span> 


## <a name="security-roles"></a><span data-ttu-id="01b6c-106">Säkerhetsroller</span><span class="sxs-lookup"><span data-stu-id="01b6c-106">Security roles</span></span>
<span data-ttu-id="01b6c-107">Klientdesfunktioner i Projet Operations innehåller följande roller:</span><span class="sxs-lookup"><span data-stu-id="01b6c-107">Project Operations front-end capabilities include the following roles:</span></span>

| <span data-ttu-id="01b6c-108">Roll</span><span class="sxs-lookup"><span data-stu-id="01b6c-108">Role</span></span>                          | <span data-ttu-id="01b6c-109">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="01b6c-109">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="01b6c-110">Omfång</span><span class="sxs-lookup"><span data-stu-id="01b6c-110">Scope</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="01b6c-111">Metodansvarig</span><span class="sxs-lookup"><span data-stu-id="01b6c-111">Practice manager</span></span>              | <span data-ttu-id="01b6c-112">Stöder rapportering mellan projekt.</span><span class="sxs-lookup"><span data-stu-id="01b6c-112">Supports cross-project reporting.</span></span>                                                                                                            | <span data-ttu-id="01b6c-113">Affärsenhet</span><span class="sxs-lookup"><span data-stu-id="01b6c-113">Business unit</span></span>              |
| <span data-ttu-id="01b6c-114">Projektgodkännare</span><span class="sxs-lookup"><span data-stu-id="01b6c-114">Project approver</span></span>              | <span data-ttu-id="01b6c-115">Godkänner tid och utgifter mot ett projekt.</span><span class="sxs-lookup"><span data-stu-id="01b6c-115">Approves time and expenses against a project.</span></span>                                                                                                                              | <span data-ttu-id="01b6c-116">Affärsenhet</span><span class="sxs-lookup"><span data-stu-id="01b6c-116">Business unit</span></span> |
| <span data-ttu-id="01b6c-117">Debiteringsadministratör för projekt</span><span class="sxs-lookup"><span data-stu-id="01b6c-117">Project billing administrator</span></span> | <span data-ttu-id="01b6c-118">Skapar fakturaförslaget.</span><span class="sxs-lookup"><span data-stu-id="01b6c-118">Creates the invoice proposal.</span></span>                                                                                                                                                 | <span data-ttu-id="01b6c-119">Affärsenhet</span><span class="sxs-lookup"><span data-stu-id="01b6c-119">Business unit</span></span> |
| <span data-ttu-id="01b6c-120">Projektledare</span><span class="sxs-lookup"><span data-stu-id="01b6c-120">Project manager</span></span>               | <span data-ttu-id="01b6c-121">Skapar projektplanen och begär resurser.</span><span class="sxs-lookup"><span data-stu-id="01b6c-121">Creates the project plan and requests resources.</span></span>                                                                                                                              | <span data-ttu-id="01b6c-122">Affärsenhet</span><span class="sxs-lookup"><span data-stu-id="01b6c-122">Business unit</span></span> |
| <span data-ttu-id="01b6c-123">Projektresurs</span><span class="sxs-lookup"><span data-stu-id="01b6c-123">Project resource</span></span>              | <span data-ttu-id="01b6c-124">Gruppmedlemmar som kan bokas och rapportera tid.</span><span class="sxs-lookup"><span data-stu-id="01b6c-124">Team members who can be booked and report time.</span></span>                                                                                                          | <span data-ttu-id="01b6c-125">Affärsenhet</span><span class="sxs-lookup"><span data-stu-id="01b6c-125">Business unit</span></span>|
| <span data-ttu-id="01b6c-126">Resurshanterare</span><span class="sxs-lookup"><span data-stu-id="01b6c-126">Resource manager</span></span>              | <span data-ttu-id="01b6c-127">Alla resurshanteringsfunktioner, t.ex. uppfyllande av resursbegäranden och bokningar, avgränsade med stöd för en hybridkonfiguration av projektledare + resurshanterare och en enskild och centraliserad resurshanteringsroll.</span><span class="sxs-lookup"><span data-stu-id="01b6c-127">All resource management functions, such as fulfill resource requests and bookings, separated to support a hybrid Project manager + Resource manager configuration and a single and centralized Resource manager role.</span></span> | <span data-ttu-id="01b6c-128">Affärsenhet</span><span class="sxs-lookup"><span data-stu-id="01b6c-128">Business unit</span></span> |


<span data-ttu-id="01b6c-129">Microsoft Project for the Web innehåller följande roller:</span><span class="sxs-lookup"><span data-stu-id="01b6c-129">Microsoft Project for the Web includes the following roles:</span></span>

| <span data-ttu-id="01b6c-130">Roll</span><span class="sxs-lookup"><span data-stu-id="01b6c-130">Role</span></span>           | <span data-ttu-id="01b6c-131">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="01b6c-131">Description</span></span>                                                                                                        | <span data-ttu-id="01b6c-132">Omfång</span><span class="sxs-lookup"><span data-stu-id="01b6c-132">Scope</span></span>  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| <span data-ttu-id="01b6c-133">Projektanvändare</span><span class="sxs-lookup"><span data-stu-id="01b6c-133">Project user</span></span>   | <span data-ttu-id="01b6c-134">Samarbetande användare av Project som kan skapa sina egna projekt och visa projekt som delas med dem.</span><span class="sxs-lookup"><span data-stu-id="01b6c-134">Collaborative user of Project   who is able to create their own projects and view any projects shared with   them.</span></span> | <span data-ttu-id="01b6c-135">Användare</span><span class="sxs-lookup"><span data-stu-id="01b6c-135">User</span></span>   |
| <span data-ttu-id="01b6c-136">Projektsystem</span><span class="sxs-lookup"><span data-stu-id="01b6c-136">Project system</span></span> | <span data-ttu-id="01b6c-137">Roll som används för programsammanhang.</span><span class="sxs-lookup"><span data-stu-id="01b6c-137">Role used for application   context.</span></span> <span data-ttu-id="01b6c-138">Kunderna bör inte använda den här systemrollen.</span><span class="sxs-lookup"><span data-stu-id="01b6c-138">Customers should not use this system role.</span></span>                                    | <span data-ttu-id="01b6c-139">Global</span><span class="sxs-lookup"><span data-stu-id="01b6c-139">Global</span></span> |

## <a name="security-enforcement"></a><span data-ttu-id="01b6c-140">Säkerhet</span><span class="sxs-lookup"><span data-stu-id="01b6c-140">Security enforcement</span></span>
<span data-ttu-id="01b6c-141">Åtgärder som utförs på projektnivå utförs i den inloggade användarens kontext.</span><span class="sxs-lookup"><span data-stu-id="01b6c-141">Actions that are performed at the project level are performed in the context of the logged in user.</span></span> <span data-ttu-id="01b6c-142">Det innebär att om du ska kunna skapa, öppna eller ta bort ett projekt måste användaren ha åtkomst tillgänglig i CDS.</span><span class="sxs-lookup"><span data-stu-id="01b6c-142">This means that in order to create, open, or delete a project, the user is required to have access available in CDS.</span></span> <span data-ttu-id="01b6c-143">Åtkomst i CDS kan beviljas via alla tänkbara mekanismer som ingår i plattformen.</span><span class="sxs-lookup"><span data-stu-id="01b6c-143">Access in CDS may be granted through any of the possible mechanisms included in the platform.</span></span> <span data-ttu-id="01b6c-144">En användare med större omfång kan till exempel komma åt projektet eller om en uttrycklig åtgärd för projektdelning har utförts som ger användaren åtkomst.</span><span class="sxs-lookup"><span data-stu-id="01b6c-144">For example, a user with a larger scope may access the project or if an explicit project share action has been performed which grants the user access.</span></span>

<span data-ttu-id="01b6c-145">Det är viktigt att tänka på detta när du skapar projekt i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="01b6c-145">It's important to consider this when creating projects in Project Operations.</span></span>

## <a name="modern-group-collaboration-with-project-operations"></a><span data-ttu-id="01b6c-146">Modernt gruppsamarbete med Project Operations</span><span class="sxs-lookup"><span data-stu-id="01b6c-146">Modern group collaboration with Project Operations</span></span>
<span data-ttu-id="01b6c-147">Project for the Web och Project Operations har stöd för moderna grupper för samarbete.</span><span class="sxs-lookup"><span data-stu-id="01b6c-147">Project for the Web and Project Operations support modern groups for collaboration.</span></span> <span data-ttu-id="01b6c-148">Användare som har lagts till i projektet via en grupp kan redigera projektplanen.</span><span class="sxs-lookup"><span data-stu-id="01b6c-148">Users added to the project through a group are able to edit the project plan.</span></span>

<span data-ttu-id="01b6c-149">Project for the Web lägger automatiskt till användare i gruppen vid tilldelning.</span><span class="sxs-lookup"><span data-stu-id="01b6c-149">Project for the Web adds users to the group automatically upon assignment.</span></span>

<span data-ttu-id="01b6c-150">Med grupper kan projektets behörigheter och stödjande samarbetsartefakter arbetas på kollektivt.</span><span class="sxs-lookup"><span data-stu-id="01b6c-150">Groups allow the permissions of the project and supporting collaboration artifacts to be worked on collaboratively.</span></span> <span data-ttu-id="01b6c-151">Följande diagram illustrerar de händelser och tillståndsändringar som inträffar under grupptilldelningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="01b6c-151">The following diagram depicts the events and state changes that happen during the group assignment process.</span></span>

<span data-ttu-id="01b6c-152">Project Operations innebär inte att en grupp skapas genom en implicit åtgärd och utförs endast med hjälp av en uttrycklig åtgärd av att trycka på grupper.</span><span class="sxs-lookup"><span data-stu-id="01b6c-152">Project Operations does not create a group through implicit action and only does so through the explicit action of pressing groups.</span></span>

<span data-ttu-id="01b6c-153">Sökning efter gruppmedlem i dialogrutan **Grupp hantering** är begränsad till dem som har angetts som en del av miljöns säkerhetsgrupp.</span><span class="sxs-lookup"><span data-stu-id="01b6c-153">Group member search in the **Group management** dialog, is limited to those who are set as part of the environment's security group.</span></span> <span data-ttu-id="01b6c-154">Läs mer: [Styra användarnas åtkomst till miljöer: säkerhetsgrupper och licenser](https://docs.microsoft.com/power-platform/admin/control-user-access).</span><span class="sxs-lookup"><span data-stu-id="01b6c-154">For more information, see [Control user access to environments: security groups and licenses](https://docs.microsoft.com/power-platform/admin/control-user-access).</span></span>

![Gruppläge](./media/groupsmode.png)

1. <span data-ttu-id="01b6c-156">Projektet skapas och ägs av användaren som skapar.</span><span class="sxs-lookup"><span data-stu-id="01b6c-156">The Project is created and owned by the creating User.</span></span>
2. <span data-ttu-id="01b6c-157">Projektägaren uppdateras till teamet.</span><span class="sxs-lookup"><span data-stu-id="01b6c-157">The Project owner is updated to the team.</span></span>
3. <span data-ttu-id="01b6c-158">Ägarteamet är mappat till den angivna eller skapade Office-gruppen.</span><span class="sxs-lookup"><span data-stu-id="01b6c-158">The Owner team is mapped to the specified or created Office Group.</span></span>
4. <span data-ttu-id="01b6c-159">Projektets ursprungliga ägare läggs till i Office-gruppen.</span><span class="sxs-lookup"><span data-stu-id="01b6c-159">The original owner of the Project is added to the Office Group.</span></span>

## <a name="deployment-recommendation"></a><span data-ttu-id="01b6c-160">Distributionsrekommendation</span><span class="sxs-lookup"><span data-stu-id="01b6c-160">Deployment recommendation</span></span>
<span data-ttu-id="01b6c-161">När modellen för gruppsamarbete utvecklas för Office-grupper kommer funktionerna att läggas till för att ge mer detaljerad kontroll över tid.</span><span class="sxs-lookup"><span data-stu-id="01b6c-161">As the Office group collaboration model evolves, functionality will be added to provide more detailed control over time.</span></span> <span data-ttu-id="01b6c-162">Kunder som distribuerar Project Operations i dag uppmuntras att fokusera på en traditionell Microsoft Dynamics 365-säkerhetsmodell.</span><span class="sxs-lookup"><span data-stu-id="01b6c-162">Customers that deploy Project Operations today are encouraged to focus on a traditional Microsoft Dynamics 365 security model.</span></span>

<span data-ttu-id="01b6c-163">Mer information finns i [Säkerhet i Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).</span><span class="sxs-lookup"><span data-stu-id="01b6c-163">For more information, see [Security in Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).</span></span>

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a><span data-ttu-id="01b6c-164">Project Operations och Microsoft Dynamics 365 Finance-säkerhet</span><span class="sxs-lookup"><span data-stu-id="01b6c-164">Project Operations and Microsoft Dynamics 365 Finance security</span></span>
<span data-ttu-id="01b6c-165">Project Operations omfattar följande roller:</span><span class="sxs-lookup"><span data-stu-id="01b6c-165">Project Operations includes the following roles:</span></span>

- <span data-ttu-id="01b6c-166">Projektledare</span><span class="sxs-lookup"><span data-stu-id="01b6c-166">Project manager</span></span>
- <span data-ttu-id="01b6c-167">Projektrevisor</span><span class="sxs-lookup"><span data-stu-id="01b6c-167">Project accountant</span></span>

<span data-ttu-id="01b6c-168">Mer information om säkerhet i Finance finns i [Rollbaserad säkerhet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span><span class="sxs-lookup"><span data-stu-id="01b6c-168">For more information about security in Finance, see [Role-based security](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]