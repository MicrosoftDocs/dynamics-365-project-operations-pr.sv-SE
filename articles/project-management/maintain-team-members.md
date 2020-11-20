---
title: Underhålla teammedlemmar
description: I det här ämnet finns information om bokning av namngivna resurser till projektteam och tilldela dem till uppgifter.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: abab21ff98481166517be0c74a2c14c36d5e9d1d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131545"
---
# <a name="maintain-team-members"></a><span data-ttu-id="4255b-103">Underhålla teammedlemmar</span><span class="sxs-lookup"><span data-stu-id="4255b-103">Maintain team members</span></span>

<span data-ttu-id="4255b-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="4255b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4255b-105">Du kan lägga till en namngiven resurs i projektteamet genom att boka dem direkt på teamet.</span><span class="sxs-lookup"><span data-stu-id="4255b-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="4255b-106">I Dynamics 365 Project Operations, gå till **Projekt** och välj de öppna projekt du bokar för.</span><span class="sxs-lookup"><span data-stu-id="4255b-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="4255b-107">På sidan **Projekt** under fliken **Team**, välj **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4255b-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="4255b-108">I dialogrutan **Snabbregistrering av projektteammedlem** väljer du den bokningsbara resursen.</span><span class="sxs-lookup"><span data-stu-id="4255b-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="4255b-109">Fältet **Roll** fylls i med resursens standardroll om de har en tilldelad.</span><span class="sxs-lookup"><span data-stu-id="4255b-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="4255b-110">Du kan ändra rollen.</span><span class="sxs-lookup"><span data-stu-id="4255b-110">You can change the role.</span></span> 
4. <span data-ttu-id="4255b-111">Välj de från- och till-datum som resursen behövs och välj allokeringsmetod för resursens kapacitet.</span><span class="sxs-lookup"><span data-stu-id="4255b-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="4255b-112">I fältet **Projektgodkännare** väljer du **Ja** om du vill att teammedlemmen ska vara en projektgodkännare.</span><span class="sxs-lookup"><span data-stu-id="4255b-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="4255b-113">Teammedlemmen kan godkänna skickade tids- och utgiftsposter för det här projektet.</span><span class="sxs-lookup"><span data-stu-id="4255b-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="4255b-114">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="4255b-114">Select **Save**.</span></span>

<span data-ttu-id="4255b-115">Du kan nu tilldela den bokade resursen till aktiviteter i projektet.</span><span class="sxs-lookup"><span data-stu-id="4255b-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="4255b-116">På sidan **Projekt**, under fliken **Schema** tilldelar du uppgifter till den nya resursen.</span><span class="sxs-lookup"><span data-stu-id="4255b-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="4255b-117">Resursväljaren som startas från fältet **resurser** i uppgiftsrutnätet visar de team medlemmar som du kan välja.</span><span class="sxs-lookup"><span data-stu-id="4255b-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="4255b-118">I Project Operations är inte resursbokningar och uppgiftstilldelningar tätt kopplade.</span><span class="sxs-lookup"><span data-stu-id="4255b-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="4255b-119">När du använder resursväljaren i schemat kan du tilldela uppgifter till teammedlemmar så att de blir fler timmar än de som ingår i projektet.</span><span class="sxs-lookup"><span data-stu-id="4255b-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="4255b-120">Skillnaderna mellan bokföringar och tilldelningar av teammedlemmar visas på flikarna **Team** och **Resursavstämningar**.</span><span class="sxs-lookup"><span data-stu-id="4255b-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="4255b-121">Du kan även stämma av skillnaderna mellan bokningar och tilldelningar för resurser på en mer detaljerad nivå.</span><span class="sxs-lookup"><span data-stu-id="4255b-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="4255b-122">Använd resursväljaren under fliken **Schema** om du vill söka efter och välja bokningsbara resurser som inte redan ingår i projektteamet.</span><span class="sxs-lookup"><span data-stu-id="4255b-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="4255b-123">Dessa resurser visas i resursväljaren som **Andra resurser**.</span><span class="sxs-lookup"><span data-stu-id="4255b-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="4255b-124">När du gör ett val läggs resursen till i projektteamet och tilldelas uppgiften, men inga bokningar skapas.</span><span class="sxs-lookup"><span data-stu-id="4255b-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="4255b-125">Du kan använda den utökade bokningsfunktionen på fliken **avstämning** eller **Schemaläggningstavla** för att boka resursens kapacitet på projektet.</span><span class="sxs-lookup"><span data-stu-id="4255b-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="4255b-126">När en teammedlem är bokad i projektet kan du använda **Underhåll bokningar** eller **Schemaläggningstavlan** direkt för att hantera deras bokningar.</span><span class="sxs-lookup"><span data-stu-id="4255b-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
