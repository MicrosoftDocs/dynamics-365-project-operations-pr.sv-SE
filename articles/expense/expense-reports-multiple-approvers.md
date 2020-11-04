---
title: Utgiftsrapporter och flera godkännare
description: I det här ämnet finns information om utgiftsrapporter som kräver godkännande av fler än en person.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085543"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="eb1db-103">Utgiftsrapporter och flera godkännare</span><span class="sxs-lookup"><span data-stu-id="eb1db-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="eb1db-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="eb1db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eb1db-105">Beroende på organisationens godkännandeprinciper för utgifter kan fler än en person behöva godkänna en skickad utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="eb1db-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="eb1db-106">När du konfigurerar arbetsflödesprocessen för godkännande av utgiftsrapporter kan du lägga till arbetsflödeselement som innehåller uppgifter eller steg för en eller flera godkännare av utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="eb1db-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="eb1db-107">Du kan till exempel kräva att alla utgiftsrapporter ska godkännas av två olika personer, chefen för den medarbetare som skickade rapporten och koordinatorn för leverantörsreskontra.</span><span class="sxs-lookup"><span data-stu-id="eb1db-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="eb1db-108">Om du vill kräva flera godkännare för utgiftsrapporter kan du lägga till arbetsflödeselementen på något av följande sätt:</span><span class="sxs-lookup"><span data-stu-id="eb1db-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="eb1db-109">Lägg till ett godkännandeelement som har ett steg.</span><span class="sxs-lookup"><span data-stu-id="eb1db-109">Add one approval element that has one step.</span></span> <span data-ttu-id="eb1db-110">Steget kan till exempel kräva att en utgiftsrapport tilldelas en användargrupp och att den godkänns med 50 procent av användargruppens medlemmar.</span><span class="sxs-lookup"><span data-stu-id="eb1db-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="eb1db-111">Lägg till ett godkännandeelement som har flera steg.</span><span class="sxs-lookup"><span data-stu-id="eb1db-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="eb1db-112">Godkännandeelementet kan till exempel innehålla följande steg:</span><span class="sxs-lookup"><span data-stu-id="eb1db-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="eb1db-113">Chefen för den medarbetare som skickade utgiftsrapporten godkänner den.</span><span class="sxs-lookup"><span data-stu-id="eb1db-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="eb1db-114">Leverantörsreskontra ansvarig verifierar inleveranserna och objekt för utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="eb1db-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="eb1db-115">Budgetägaren godkänner utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="eb1db-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="eb1db-116">Lägg till flera godkännandeelement, som vart och ett har ett steg.</span><span class="sxs-lookup"><span data-stu-id="eb1db-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="eb1db-117">Du kan till exempel lägga till ett separat godkännandeelement för vart och ett av följande steg:</span><span class="sxs-lookup"><span data-stu-id="eb1db-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="eb1db-118">Medarbetarens chef godkänner utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="eb1db-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="eb1db-119">Budgetägaren godkänner utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="eb1db-119">The budget owner approves the expense report.</span></span>
