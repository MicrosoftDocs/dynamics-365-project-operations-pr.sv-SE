---
title: Vanliga frågor om resurshantering
description: Det här ämnet innehåller svar på vanliga frågor om resurshantering.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 38d9509768323a5a1d78683a2e65ade241adc65f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120160"
---
# <a name="resource-management-faq"></a><span data-ttu-id="a370d-103">Vanliga frågor om resurshantering</span><span class="sxs-lookup"><span data-stu-id="a370d-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="a370d-104">Vad är det för skillnad på en teammedlem och ett resurskrav?</span><span class="sxs-lookup"><span data-stu-id="a370d-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="a370d-105">En projektteammedlem kan tilldelas uppgifter, bokas eller överbokas och ställas in som godkännare.</span><span class="sxs-lookup"><span data-stu-id="a370d-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="a370d-106">Ett resurskrav kan existera utan en projektteammedlem som ett utkast till efterfrågan.</span><span class="sxs-lookup"><span data-stu-id="a370d-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="a370d-107">Vad är det för skillnad på föreslagna och preliminärbokade timmar?</span><span class="sxs-lookup"><span data-stu-id="a370d-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="a370d-108">Föreslagna timmar och preliminärbokade timmar skiljer sig åt i synbarheten.</span><span class="sxs-lookup"><span data-stu-id="a370d-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="a370d-109">Föreslagna timmar visas endast för resursansvariga och projektledare som initierat behovet genom att använda en resursbegäran.</span><span class="sxs-lookup"><span data-stu-id="a370d-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="a370d-110">De preliminärbokade timmarna är synliga för alla som har till gång till schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="a370d-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="a370d-111">Hur kan jag visa de preliminärbokade timmarna för resurser i ett team?</span><span class="sxs-lookup"><span data-stu-id="a370d-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="a370d-112">Preliminärbokningar kan göras när du bokar ett resurskrav.</span><span class="sxs-lookup"><span data-stu-id="a370d-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="a370d-113">Resurser som är preliminärbokade i ett projektteam visas som teammedlemmar med preliminärbokade timmar.</span><span class="sxs-lookup"><span data-stu-id="a370d-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="a370d-114">De visas också på schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="a370d-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="a370d-115">Hur ändrar jag de begärda timmarna och start- och slutdatumen för en resurs (generiskt eller namngivet) som jag bokade?</span><span class="sxs-lookup"><span data-stu-id="a370d-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="a370d-116">När du har bokat resurser väljer du **Underhåll bokningar** för att göra nödvändiga ändringar.</span><span class="sxs-lookup"><span data-stu-id="a370d-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="a370d-117">Vilka resurstyper stöder Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="a370d-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="a370d-118">**Användare** och **kontakt** är de enda resurstyper som stöds i Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a370d-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="a370d-119">Du kan skapa andra typer av resurser (t.ex. **utrustning** och **grupp**), men det finns inget fullständigt användningsfall som stöds för dem.</span><span class="sxs-lookup"><span data-stu-id="a370d-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="a370d-120">Vad är det för skillnad på en tilldelning och en bokning?</span><span class="sxs-lookup"><span data-stu-id="a370d-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="a370d-121">Tilldelningar är tilldelningen av resurser till projektuppgifter i projektschemat.</span><span class="sxs-lookup"><span data-stu-id="a370d-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="a370d-122">Resurserna kan antingen vara riktiga eller generiska resurser.</span><span class="sxs-lookup"><span data-stu-id="a370d-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="a370d-123">Bokningar är en fast eller preliminär allokering av resurser till ett projekt.</span><span class="sxs-lookup"><span data-stu-id="a370d-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="a370d-124">Fasta bokningar förbrukar en resurs kapacitet.</span><span class="sxs-lookup"><span data-stu-id="a370d-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="a370d-125">För verkliga resurser bör bokningarna och tilldelningarna godkännas eftersom de inte skiljer sig åt.</span><span class="sxs-lookup"><span data-stu-id="a370d-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="a370d-126">PSA tvingar emellertid inte detta avtal.</span><span class="sxs-lookup"><span data-stu-id="a370d-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="a370d-127">I vyn avstämning visas en projektledare där resursens bokningar och tilldelningar inte godkänner varandra.</span><span class="sxs-lookup"><span data-stu-id="a370d-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
