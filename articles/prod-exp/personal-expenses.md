---
title: Privata utgifter i en utgiftsrapport
description: I det här ämnet beskrivs de två metoderna för att hantera en arbetares privata utgifter i Microsoft Dynamics 365 Finance.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf6bfc714751fa64914e684f67d37552b2df162e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271420"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="0ce8e-103">Privata utgifter i en utgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="0ce8e-103">Personal expenses on an expense report</span></span>

<span data-ttu-id="0ce8e-104">Under en affärsresa kan arbetstagarna ibland debitera företagets kreditkort för privata utgifter.</span><span class="sxs-lookup"><span data-stu-id="0ce8e-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="0ce8e-105">Om du inte definierar en process för hantering av privata utgifter kan godkännandeprocessen för utgiftsrapporter störas när arbetstagarna skickar in sina specificerade utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="0ce8e-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="0ce8e-106">Det finns två sätt att hantera en arbetares privata utgifter:</span><span class="sxs-lookup"><span data-stu-id="0ce8e-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="0ce8e-107">**Betalas av medarbetare** – din organisation betalar inte privata utgifter som visas på fakturan för företagskreditkortet.</span><span class="sxs-lookup"><span data-stu-id="0ce8e-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="0ce8e-108">I stället skapas en rapport som visar privata utgifter tillsammans med de företagsutgifter som debiterades företagskreditkortet.</span><span class="sxs-lookup"><span data-stu-id="0ce8e-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="0ce8e-109">**Betalas av företaget** – organisationen betalar hela fakturan för företagets kreditkort och debiterar sedan arbetarens konto för privata utgifter.</span><span class="sxs-lookup"><span data-stu-id="0ce8e-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="0ce8e-110">Du kan välja vilken metod som ska användas av organisationen på sidan **Parametrar för utgiftshantering**.</span><span class="sxs-lookup"><span data-stu-id="0ce8e-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]