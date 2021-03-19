---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 21, version 3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 21, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 69b592db7456bf11c2e933256569d726056d1a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280645"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="f56ca-103">Project Service Automation uppdateringsversion 21, V3</span><span class="sxs-lookup"><span data-stu-id="f56ca-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f56ca-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f56ca-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f56ca-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="f56ca-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f56ca-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f56ca-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f56ca-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="f56ca-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f56ca-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f56ca-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f56ca-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 21.</span><span class="sxs-lookup"><span data-stu-id="f56ca-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="f56ca-110">Den här versionen har ett versionsnummer på V 3.10.32.50 och är allmänt tillgänglig via en självuppdatering i juni 2020.</span><span class="sxs-lookup"><span data-stu-id="f56ca-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="f56ca-111">Uppdatering version 21</span><span class="sxs-lookup"><span data-stu-id="f56ca-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f56ca-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="f56ca-112">Bug fixes</span></span>

<span data-ttu-id="f56ca-113">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="f56ca-113">**Time and Expense**</span></span>

<span data-ttu-id="f56ca-114">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="f56ca-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="f56ca-115">När du är värd för **kontrollen rutnät för tidspost** i instrumentpaneler används inte rutnätets fulla bredd i instrumentpanelens behållare.</span><span class="sxs-lookup"><span data-stu-id="f56ca-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="f56ca-116">För specifika tidszoner visas inte posterna för rutnätskontrollen **tidsinmatning**.</span><span class="sxs-lookup"><span data-stu-id="f56ca-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="f56ca-117">Tidsposter efter 21:00 visas på fel dag.</span><span class="sxs-lookup"><span data-stu-id="f56ca-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="f56ca-118">Användarna kan inte skicka utgifter om utgiftskategorin, om **utgiftsinleveransen** inte har något värde.</span><span class="sxs-lookup"><span data-stu-id="f56ca-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="f56ca-119">**Resurshantering**</span><span class="sxs-lookup"><span data-stu-id="f56ca-119">**Resource Management**</span></span>

<span data-ttu-id="f56ca-120">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="f56ca-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="f56ca-121">Inaktiva bokningar visas i vyn **avstämning**.</span><span class="sxs-lookup"><span data-stu-id="f56ca-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="f56ca-122">En allmän resursuppfyllelse saknar verifiering för att se till att det finns en giltig bokningsstatus.</span><span class="sxs-lookup"><span data-stu-id="f56ca-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="f56ca-123">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="f56ca-123">**Project Management**</span></span>

<span data-ttu-id="f56ca-124">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="f56ca-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="f56ca-125">Formulärets rutnät **Projekt** (vyn **Resurstilldelning**, **Uppgift**, **Avstämning**, **Utgiftsuppskattningar**) är fortfarande redigerbara även när ett projekt inte är aktivt.</span><span class="sxs-lookup"><span data-stu-id="f56ca-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="f56ca-126">Dubbletter av kunder kan inte kopplas till kunder som är länkade till bekräftade projekt kontrakt.</span><span class="sxs-lookup"><span data-stu-id="f56ca-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="f56ca-127">När en resurs som inte har en giltig kalender läggs till returnerar systemet inte ett användarvänligt felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="f56ca-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="f56ca-128">Knappen **Lägg till uppgift** i rutnätet aktiveras när projektet länkas till ett **Microsoft Project-tillägg**.</span><span class="sxs-lookup"><span data-stu-id="f56ca-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="f56ca-129">Insatsen växer okontrollerat när en uppgift med en kategori tilldelas en resurs med en roll för vilken en självkostnad har definierats.</span><span class="sxs-lookup"><span data-stu-id="f56ca-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="f56ca-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="f56ca-130">**Sales**</span></span>

<span data-ttu-id="f56ca-131">Följande förbättringar har gjorts:</span><span class="sxs-lookup"><span data-stu-id="f56ca-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="f56ca-132">**Faktureringsfrekvens** och **faktureringsstart** har flyttats till fliken **fakturaschema**.</span><span class="sxs-lookup"><span data-stu-id="f56ca-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="f56ca-133">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="f56ca-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="f56ca-134">**Totalt försäljningspris** är noll (0) för **kategori** även om **roll** har ett totalt försäljningspris som inte är noll.</span><span class="sxs-lookup"><span data-stu-id="f56ca-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="f56ca-135">Kunder kan inte ändra värdet i fältet **fakturastatus** till **klar för fakturering** när en annan anpassad process uppdaterar ett extra fält.</span><span class="sxs-lookup"><span data-stu-id="f56ca-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="f56ca-136">Med knappen **Uppdatera fakturarader** kan du skapa flera duplicerade rader om alternativet markeras flera gånger.</span><span class="sxs-lookup"><span data-stu-id="f56ca-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="f56ca-137">Knappen **Uppdatera priser** fungerar inte i underrutnätet **Rollpriser** i formuläret **Snabbvy**.</span><span class="sxs-lookup"><span data-stu-id="f56ca-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="f56ca-138">Logiken **Stängning av prislista för försäljning** hanterar tidszoner felaktigt, vilket resulterar i ett felaktigt urval av prislistor.</span><span class="sxs-lookup"><span data-stu-id="f56ca-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="f56ca-139">Ett projekts **Total faktisk kostnad** kan avgränsas med ett decimal belopp efter att en enskild tid har godkänts.</span><span class="sxs-lookup"><span data-stu-id="f56ca-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="f56ca-140">Logiken **Prismatchning** ger inte ett användarvänligt felmeddelande om **Hämta RolePrice** inte har värden i fälten **primär enhet** och **pris i primär enhet**.</span><span class="sxs-lookup"><span data-stu-id="f56ca-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]