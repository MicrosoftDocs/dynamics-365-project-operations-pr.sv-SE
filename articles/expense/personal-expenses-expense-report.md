---
title: Arbeta med privata utgifter i en utgiftsrapport
description: Detta ämne innehåller information om hur du arbetar med personliga utgifter som anställda har när de reser i affärssyfte.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025706"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="f9843-103">Arbeta med privata utgifter i en utgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="f9843-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="f9843-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="f9843-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f9843-105">Under resor kan en anställd debitera sina personliga utgifter på företagets kreditkort.</span><span class="sxs-lookup"><span data-stu-id="f9843-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="f9843-106">Om en process inte har definierats för hantering av personliga utgifter kan godkännandeprocessen för utgiftsrapporten komma att avbrytas när en anställd skickar in sin specificerade utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="f9843-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="f9843-107">Du kan använda två metoder för att arbeta med en anställds personliga utgifter:</span><span class="sxs-lookup"><span data-stu-id="f9843-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="f9843-108">**Betalas av den anställde**: Din organisation betalar inte privata utgifter som visas på fakturan för företagskreditkortet.</span><span class="sxs-lookup"><span data-stu-id="f9843-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="f9843-109">I stället betalar den anställde kreditkortsleverantören direkt för kostnaderna.</span><span class="sxs-lookup"><span data-stu-id="f9843-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="f9843-110">**Betald av företag**: Organisationen betalar den fullständiga fakturan för företagets kreditkort och debiterar sedan den anställdes konto för de personliga kostnaderna.</span><span class="sxs-lookup"><span data-stu-id="f9843-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="f9843-111">Du kan välja vilken metod som ska användas av organisationen på sidan **Parametrar för utgiftshantering**.</span><span class="sxs-lookup"><span data-stu-id="f9843-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="f9843-112">Aktivera funktionen dela utgift när fältet för personligt belopp har ett definierat värde</span><span class="sxs-lookup"><span data-stu-id="f9843-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="f9843-113">Funktionen **Aktivera funktionen dela utgift när fältet för personligt belopp har ett definierat värde** gäller endast utgiftsrapporter som har godkänts genom ett arbetsflöde på radnivå.</span><span class="sxs-lookup"><span data-stu-id="f9843-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="f9843-114">Rapporter godkänns genom att gå till **Bearbeta utgiftsrapporter** > **Utgiftsrapporter som har tilldelats mig** > **Öppna utgiftsrapport**.</span><span class="sxs-lookup"><span data-stu-id="f9843-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="f9843-115">Om du vill aktivera den här funktionen, går du till **Arbetsytor** > **Funktionshanterring**, väljer **Aktivera funktionen dela utgift när fältet personligt belopp har ett definierat värde** och väljer sedan **Aktivera nu**.</span><span class="sxs-lookup"><span data-stu-id="f9843-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="f9843-116">När funktionen har aktiverats skapar utgiftsrader som använder funktionen två rader när rapporten skickas.</span><span class="sxs-lookup"><span data-stu-id="f9843-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="f9843-117">Två rader skapas så att godkännaren kan godkänna varje rad separat.</span><span class="sxs-lookup"><span data-stu-id="f9843-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
