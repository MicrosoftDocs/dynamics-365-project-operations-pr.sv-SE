---
title: Flera godkännare i en utgiftsrapport
description: I det här ämnet finns information om utgiftsrapporter som kräver godkännande av flera personer.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960629"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="3ae12-103">Flera godkännare i en utgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="3ae12-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="3ae12-104">Beroende på organisationens godkännandeprinciper för utgifter kan fler än en person behöva godkänna en utgiftsrapport som skickas in av en medarbetare.</span><span class="sxs-lookup"><span data-stu-id="3ae12-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="3ae12-105">När du konfigurerar arbetsflödesprocessen för godkännande av utgiftsrapporter kan du lägga till arbetsflödeselement som innehåller uppgifter eller steg för en eller flera godkännare av utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="3ae12-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="3ae12-106">Du kan till exempel kräva att alla utgiftsrapporter ska godkännas först av chefen för den medarbetare som skickade in rapporten och sedan av koordinatorn för leverantörsreskontra.</span><span class="sxs-lookup"><span data-stu-id="3ae12-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="3ae12-107">Om du vill kräva flera godkännare för utgiftsrapporter kan du lägga till arbetsflödeselementen på något av följande sätt:</span><span class="sxs-lookup"><span data-stu-id="3ae12-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="3ae12-108">Lägg till ett godkännandeelement som har ett steg.</span><span class="sxs-lookup"><span data-stu-id="3ae12-108">Add one approval element that has one step.</span></span> <span data-ttu-id="3ae12-109">Steget kan till exempel kräva att en utgiftsrapport tilldelas en användargrupp och att den godkänns med 50 procent av användargruppens medlemmar.</span><span class="sxs-lookup"><span data-stu-id="3ae12-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="3ae12-110">Lägg till ett godkännandeelement som har flera steg.</span><span class="sxs-lookup"><span data-stu-id="3ae12-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="3ae12-111">Godkännandeelementet kan till exempel innehålla följande steg:</span><span class="sxs-lookup"><span data-stu-id="3ae12-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="3ae12-112">Chefen för den medarbetare som skickade utgiftsrapporten godkänner den.</span><span class="sxs-lookup"><span data-stu-id="3ae12-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="3ae12-113">Leverantörsreskontra ansvarig verifierar inleveranserna och objekt för utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="3ae12-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="3ae12-114">Budgetägaren godkänner utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="3ae12-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="3ae12-115">Lägg till flera godkännandeelement, som vart och ett har ett steg.</span><span class="sxs-lookup"><span data-stu-id="3ae12-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="3ae12-116">Du kan till exempel lägga till ett separat godkännandeelement för vart och ett av följande steg:</span><span class="sxs-lookup"><span data-stu-id="3ae12-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="3ae12-117">Medarbetarens chef godkänner utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="3ae12-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="3ae12-118">Budgetägaren godkänner utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="3ae12-118">The budget owner approves the expense report.</span></span>
