---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 17, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 17, version 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 364a64e0ea501ac5b7faaf254c7af3648cfe1f9b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006713"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="dd393-103">Project Service Automation uppdateringsversion 17, V3</span><span class="sxs-lookup"><span data-stu-id="dd393-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="dd393-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="dd393-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="dd393-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="dd393-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="dd393-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="dd393-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="dd393-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="dd393-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="dd393-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="dd393-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="dd393-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för PSA V3, uppdatering version 17.</span><span class="sxs-lookup"><span data-stu-id="dd393-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="dd393-110">Den här versionen har versionsnummer V3.10.6.34 och är allmänt tillgänglig via en självuppdatering i mars 2020.</span><span class="sxs-lookup"><span data-stu-id="dd393-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="dd393-111">Uppdatering version 17</span><span class="sxs-lookup"><span data-stu-id="dd393-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="dd393-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="dd393-112">Bug fixes</span></span>

<span data-ttu-id="dd393-113">**Allmänt**</span><span class="sxs-lookup"><span data-stu-id="dd393-113">**General**</span></span>

- <span data-ttu-id="dd393-114">Åtgärdat: Uppdatering för Project Service Automation för att påtvinga licenser för team medlemmar (projektresursens nav omfattar tjänstplan-metadata för teammedlem, version 3.x)</span><span class="sxs-lookup"><span data-stu-id="dd393-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="dd393-115">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="dd393-115">**Time and Expense**</span></span>

- <span data-ttu-id="dd393-116">Åtgärdat: Det går inte att ändra en utgiftsuppskattning från ett pris som inte är noll till noll (0).</span><span class="sxs-lookup"><span data-stu-id="dd393-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="dd393-117">Ändringen ignoreras.</span><span class="sxs-lookup"><span data-stu-id="dd393-117">The change is ignored.</span></span>

<span data-ttu-id="dd393-118">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="dd393-118">**Project Management**</span></span>

- <span data-ttu-id="dd393-119">Åtgärdat: en kontroll för nollvärden har lagts till på en gruppmedlems befattningsnamn.</span><span class="sxs-lookup"><span data-stu-id="dd393-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="dd393-120">Åtgärdat: Fältet **msdyn_userresourceid** i entiteten **msdyn_resourceassignment** har blivit inaktuellt.</span><span class="sxs-lookup"><span data-stu-id="dd393-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="dd393-121">Åtgärdatt: Uppgraderingen från 2.x till 3.x hanterar nu tomma insatsprofiler i aktivitetstilldelningar.</span><span class="sxs-lookup"><span data-stu-id="dd393-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="dd393-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="dd393-122">**Sales**</span></span>

- <span data-ttu-id="dd393-123">Åtgärdat: **Invoice.PreValidateInvoiceUpdate** hanterar nu scenariot med att återtilldela postägare korrekt.</span><span class="sxs-lookup"><span data-stu-id="dd393-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="dd393-124">Åtgärdat: När transaktionsklassen är **Tid** är **UnitGroup** icke redigerbart för alla entiteter, inklusive **QuoteLineDetails**. **JournalLine**, **InvoiceLineDetail** och **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="dd393-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="dd393-125">**Enhet** är emellertid icke-redigerbart endast för **JournalLine** och **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="dd393-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]