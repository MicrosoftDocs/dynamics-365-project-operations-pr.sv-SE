---
title: Vanliga frågor om resurshantering
description: Det här ämnet innehåller svar på vanliga frågor om resurshantering.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 25e069beaffc9081a5516449d55b5c9304c23b0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008783"
---
# <a name="resource-management-faq"></a><span data-ttu-id="64599-103">Vanliga frågor om resurshantering</span><span class="sxs-lookup"><span data-stu-id="64599-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="64599-104">Vad är det för skillnad på en teammedlem och ett resurskrav?</span><span class="sxs-lookup"><span data-stu-id="64599-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="64599-105">En projektteammedlem kan tilldelas uppgifter, bokas eller överbokas och ställas in som godkännare.</span><span class="sxs-lookup"><span data-stu-id="64599-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="64599-106">Ett resurskrav kan existera utan en projektteammedlem som ett utkast till efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="64599-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="64599-107">Vad är det för skillnad på föreslagna och preliminärbokade timmar?</span><span class="sxs-lookup"><span data-stu-id="64599-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="64599-108">Föreslagna timmar och preliminärbokade timmar skiljer sig åt i synbarheten.</span><span class="sxs-lookup"><span data-stu-id="64599-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="64599-109">Föreslagna timmar visas endast för resursansvariga och projektledare som initierat behovet genom att använda en resursbegäran.</span><span class="sxs-lookup"><span data-stu-id="64599-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="64599-110">De preliminärbokade timmarna är synliga för alla som har till gång till schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="64599-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="64599-111">Hur kan jag visa de preliminärbokade timmarna för resurser i ett team?</span><span class="sxs-lookup"><span data-stu-id="64599-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="64599-112">Preliminärbokningar kan göras när du bokar ett resurskrav.</span><span class="sxs-lookup"><span data-stu-id="64599-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="64599-113">Resurser som är preliminärbokade i ett projektteam visas som teammedlemmar med preliminärbokade timmar.</span><span class="sxs-lookup"><span data-stu-id="64599-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="64599-114">De visas också på schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="64599-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="64599-115">Hur ändrar jag de begärda timmarna och start- och slutdatumen för en resurs (generiskt eller namngivet) som jag bokade?</span><span class="sxs-lookup"><span data-stu-id="64599-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="64599-116">När du har bokat resurser väljer du **Underhåll bokningar** för att göra nödvändiga ändringar.</span><span class="sxs-lookup"><span data-stu-id="64599-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="64599-117">Vilka resurstyper stöder Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="64599-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="64599-118">**Användare** och **kontakt** är de enda resurstyper som stöds i Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="64599-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="64599-119">Du kan skapa andra typer av resurser (t.ex. **utrustning** och **grupp**), men det finns inget fullständigt användningsfall som stöds för dem.</span><span class="sxs-lookup"><span data-stu-id="64599-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="64599-120">Vad är det för skillnad på en tilldelning och en bokning?</span><span class="sxs-lookup"><span data-stu-id="64599-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="64599-121">Tilldelningar är tilldelningen av resurser till projektuppgifter i projektschemat.</span><span class="sxs-lookup"><span data-stu-id="64599-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="64599-122">Resurserna kan antingen vara riktiga eller generiska resurser.</span><span class="sxs-lookup"><span data-stu-id="64599-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="64599-123">Bokningar är en fast eller preliminär allokering av resurser till ett projekt.</span><span class="sxs-lookup"><span data-stu-id="64599-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="64599-124">Fasta bokningar förbrukar en resurs kapacitet.</span><span class="sxs-lookup"><span data-stu-id="64599-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="64599-125">För verkliga resurser bör bokningarna och tilldelningarna godkännas eftersom de inte skiljer sig åt.</span><span class="sxs-lookup"><span data-stu-id="64599-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="64599-126">PSA tvingar emellertid inte detta avtal.</span><span class="sxs-lookup"><span data-stu-id="64599-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="64599-127">I vyn avstämning visas en projektledare där resursens bokningar och tilldelningar inte godkänner varandra.</span><span class="sxs-lookup"><span data-stu-id="64599-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]