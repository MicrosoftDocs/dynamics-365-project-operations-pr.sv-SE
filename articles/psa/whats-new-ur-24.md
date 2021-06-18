---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 24, V3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 24, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c95a9dcada4fbf6c462df29d450aaafab4e73aa5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000278"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="5ecb6-103">Project Service Automation uppdateringsversion 24, V3</span><span class="sxs-lookup"><span data-stu-id="5ecb6-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5ecb6-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5ecb6-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5ecb6-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5ecb6-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="5ecb6-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="5ecb6-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5ecb6-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 24.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="5ecb6-110">Den här versionen har versionsnummer V 3.10.42.43 och är allmänt tillgänglig via en självuppdatering i oktober 2020.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="5ecb6-111">Uppdatering version 24</span><span class="sxs-lookup"><span data-stu-id="5ecb6-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5ecb6-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="5ecb6-112">Bug fixes</span></span>

<span data-ttu-id="5ecb6-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="5ecb6-113">**Sales**</span></span>

<span data-ttu-id="5ecb6-114">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="5ecb6-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="5ecb6-115">Problem när standardprislistan för produkter anges.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="5ecb6-116">Resultatet av offertvinst är långsamt på grund av den inbäddade prislistan och kopian av rollprisregister.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="5ecb6-117">**Projektkontrakt/försäljningsnav** > **produktradartikel/orderradkvantitet** avrundas automatiskt till närmsta heltal.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="5ecb6-118">Höj till systemprivilegierna vid läsning av prislistor.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="5ecb6-119">Kopiera adressfält för kunder **address1_freighttermscode** och **address1_shippingmethodcode** till offert/order.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="5ecb6-120">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="5ecb6-120">**Time and Expense**</span></span>

<span data-ttu-id="5ecb6-121">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="5ecb6-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="5ecb6-122">**Tidsinmatningsrutnätet** stöder inte tidsfunktionen **endast datum**.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="5ecb6-123">**Tidsposten** uppdateras inte automatiskt.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="5ecb6-124">En manuell uppdatering krävs.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-124">A manual refresh is required.</span></span>
- <span data-ttu-id="5ecb6-125">Det går inte att importera tidsposterna från en tilldelning när det finns en rast (0 timme) i en resurs tilldelningar.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="5ecb6-126">När du skapar en tidspost anger du startvärdet som **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="5ecb6-127">Aktivera massredigering för tidsregistrering igen.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="5ecb6-128">**Resurshantering**</span><span class="sxs-lookup"><span data-stu-id="5ecb6-128">**Resource Management**</span></span>

<span data-ttu-id="5ecb6-129">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="5ecb6-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="5ecb6-130">Om du försöker uppdatera statusen för en bokning inom en dag utan ett krav kommer ett null-ref-undantag att resultera.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="5ecb6-131">Det gick inte att läsa in **avstämningsvyn**.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="5ecb6-132">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="5ecb6-132">**Project Management**</span></span>

<span data-ttu-id="5ecb6-133">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="5ecb6-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="5ecb6-134">I **Projektschema** när du ändrar från **Manuell** till **Auto** slutförs inte spara automatiskt.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="5ecb6-135">Utgiftskostnader ska inte beräknas mot varians i **projektspårningsrutnätet**.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="5ecb6-136">Inkonsekvent beteende för kolumnerna **taggen uppskattningar** under inläsning jämfört med ändring av typen **tidsfas**.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="5ecb6-137">Den faktiska kostnaden för ett projekt kan inte återspegla summorna från **faktiska värden**.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="5ecb6-138">**Det uppskattade avslutningsdatumet** på fliken **Sammanfattning** matchar inte **WBS-schemat**.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="5ecb6-139">**Uppdatera faktiska timmar** vid utdragning fungerar inte korrekt.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="5ecb6-140">En projektledare utanför roten **BU** kan inte skapa ett projekt.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="5ecb6-141">Ändringar i uppgift eller kategori i **utgiftsuppskattningar** kvarstår inte.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="5ecb6-142">**Kopia av kontrakt** kopierar fakturascheman och körningsstatus.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="5ecb6-143">Knappen **Uppdatera faktiska värden** för beräkning av sammanfattningsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="5ecb6-144">Microsoft Project-tillägg: korrigera null-referens-fel om en teammedlem har en tom resursenhet.</span><span class="sxs-lookup"><span data-stu-id="5ecb6-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]