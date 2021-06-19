---
title: Flera godkännare i en utgiftsrapport
description: I det här ämnet finns information om utgiftsrapporter som kräver godkännande av flera personer.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c745dda957fab5acc464b9d1c774fcdc783cde40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005273"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="f1381-103">Flera godkännare i en utgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="f1381-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="f1381-104">Beroende på organisationens godkännandeprinciper för utgifter kan fler än en person behöva godkänna en utgiftsrapport som skickas in av en medarbetare.</span><span class="sxs-lookup"><span data-stu-id="f1381-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="f1381-105">När du konfigurerar arbetsflödesprocessen för godkännande av utgiftsrapporter kan du lägga till arbetsflödeselement som innehåller uppgifter eller steg för en eller flera godkännare av utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="f1381-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="f1381-106">Du kan till exempel kräva att alla utgiftsrapporter ska godkännas först av chefen för den medarbetare som skickade in rapporten och sedan av koordinatorn för leverantörsreskontra.</span><span class="sxs-lookup"><span data-stu-id="f1381-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="f1381-107">Om du vill kräva flera godkännare för utgiftsrapporter kan du lägga till arbetsflödeselementen på något av följande sätt:</span><span class="sxs-lookup"><span data-stu-id="f1381-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="f1381-108">Lägg till ett godkännandeelement som har ett steg.</span><span class="sxs-lookup"><span data-stu-id="f1381-108">Add one approval element that has one step.</span></span> <span data-ttu-id="f1381-109">Steget kan till exempel kräva att en utgiftsrapport tilldelas en användargrupp och att den godkänns med 50 procent av användargruppens medlemmar.</span><span class="sxs-lookup"><span data-stu-id="f1381-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="f1381-110">Lägg till ett godkännandeelement som har flera steg.</span><span class="sxs-lookup"><span data-stu-id="f1381-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="f1381-111">Godkännandeelementet kan till exempel innehålla följande steg:</span><span class="sxs-lookup"><span data-stu-id="f1381-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="f1381-112">Chefen för den medarbetare som skickade utgiftsrapporten godkänner den.</span><span class="sxs-lookup"><span data-stu-id="f1381-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="f1381-113">Leverantörsreskontra ansvarig verifierar inleveranserna och objekt för utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="f1381-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="f1381-114">Budgetägaren godkänner utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="f1381-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="f1381-115">Lägg till flera godkännandeelement, som vart och ett har ett steg.</span><span class="sxs-lookup"><span data-stu-id="f1381-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="f1381-116">Du kan till exempel lägga till ett separat godkännandeelement för vart och ett av följande steg:</span><span class="sxs-lookup"><span data-stu-id="f1381-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="f1381-117">Medarbetarens chef godkänner utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="f1381-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="f1381-118">Budgetägaren godkänner utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="f1381-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]