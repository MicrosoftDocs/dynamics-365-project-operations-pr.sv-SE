---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 18, V3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 18, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 1d7ea200531dd24d56a829f879e3a2532a9b38dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085494"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="7b940-103">Project Service Automation uppdateringsversion 18, V3</span><span class="sxs-lookup"><span data-stu-id="7b940-103">Project Service Automation Update Release 18, V3</span></span>

<span data-ttu-id="7b940-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7b940-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="7b940-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="7b940-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7b940-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="7b940-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7b940-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="7b940-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="7b940-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="7b940-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="7b940-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 18.</span><span class="sxs-lookup"><span data-stu-id="7b940-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="7b940-110">Den här versionen har ett versionsnummer på V3.10.8.12 och är allmänt tillgänglig via en självuppdatering i april 2020.</span><span class="sxs-lookup"><span data-stu-id="7b940-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="7b940-111">Uppdatering version 18</span><span class="sxs-lookup"><span data-stu-id="7b940-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="7b940-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="7b940-112">Bug fixes</span></span>

<span data-ttu-id="7b940-113">**Tid och utgift**</span><span class="sxs-lookup"><span data-stu-id="7b940-113">**Time and Expense**</span></span>

- <span data-ttu-id="7b940-114">Korrigerat: Flödena **Återkalla** , **Begär** och **Avbryt godkännande** skapar undantag med oklara felmeddelanden.</span><span class="sxs-lookup"><span data-stu-id="7b940-114">Fixed: **Recall** , **Request** , and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="7b940-115">Korrigerat: När **Avbryt godkännande** misslyckas för en utgift uppstår inte ett relevant undantagsfel.</span><span class="sxs-lookup"><span data-stu-id="7b940-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="7b940-116">Korrigerat: rutnätet för tidsinmatning hanterar felaktigt lediga dagar i Australien efter växling av sommartid (DST) i oktober.</span><span class="sxs-lookup"><span data-stu-id="7b940-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="7b940-117">Korrigerat: felaktig standardlogik förhindrar att utgifter skickas.</span><span class="sxs-lookup"><span data-stu-id="7b940-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="7b940-118">Korrigerat: när godkännande av tidsinmatning misslyckas förblir godkännandet i ett **pågående** tillstånd.</span><span class="sxs-lookup"><span data-stu-id="7b940-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="7b940-119">Korrigerat: SQL-fel i massgodkännanden (deadlock/tidsgräns).</span><span class="sxs-lookup"><span data-stu-id="7b940-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="7b940-120">Korrigerat: viktiga prestandaproblem i användargränssnittet som orsakas av uppdatering av teammedlemmar under godkännande av tidsposter.</span><span class="sxs-lookup"><span data-stu-id="7b940-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="7b940-121">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="7b940-121">**Project Management**</span></span>

- <span data-ttu-id="7b940-122">Korrigerat: ett tidszonsmeddelande har flyttats från vyn **Avstämning** till vyn **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="7b940-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="7b940-123">Korrigerat: kalendermallen återställs inte korrekt till standardvärdet när ett nytt projektformulär öppnas.</span><span class="sxs-lookup"><span data-stu-id="7b940-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="7b940-124">Korrigerat: för chromiumbaserade webbläsare kan användare inte enkelt välja de föregående aktiviteter som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7b940-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="7b940-125">Korrigerat: att skapa eller kopiera **Projekt från en tom mall** hämtar orelaterade uppgifter.</span><span class="sxs-lookup"><span data-stu-id="7b940-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="7b940-126">Korrigerat: i specifika fall innebär en ny uppgift från aktivitetsrutnätet att det skapas dubbla poster.</span><span class="sxs-lookup"><span data-stu-id="7b940-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="7b940-127">Korrigerat: i manuellt läge kan användare inte uppdatera uppgiftens startdatum innan det aktuella datumet har sparats.</span><span class="sxs-lookup"><span data-stu-id="7b940-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="7b940-128">**Resurshantering**</span><span class="sxs-lookup"><span data-stu-id="7b940-128">**Resource Management**</span></span>

- <span data-ttu-id="7b940-129">Korrigerat: Vyn **avstämning** visa raden delsummor beräknar felaktigt bokningsavvikelse var för sig efter förlängning av bokningar.</span><span class="sxs-lookup"><span data-stu-id="7b940-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="7b940-130">Korrigerat: Vyn **Avstämning** visar felaktigt resurstilldelningar när den bokningsbara resursen har en kalender som inte överensstämmer med projektkalendern.</span><span class="sxs-lookup"><span data-stu-id="7b940-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="7b940-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="7b940-131">**Sales**</span></span>

- <span data-ttu-id="7b940-132">Korrigerat: När tidsposter godkänns igen ( **Godkänn > Annullera >** Godkänn igen) skapas en dubblett av den verkliga transaktionen som inte kan debiteras.</span><span class="sxs-lookup"><span data-stu-id="7b940-132">Fixed: When time entries are re-approved ( **Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
