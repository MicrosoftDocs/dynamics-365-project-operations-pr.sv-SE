---
title: Bokföra utgiftsrapporter
description: I det här ämnet beskrivs hur du bokför utgiftsrapporter.
author: suvaidya
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ec897373cd74f7d7f63cd9ca4c46f4245336eb7f
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907430"
---
# <a name="post-expense-reports"></a><span data-ttu-id="a3ab9-103">Bokföra utgiftsrapporter</span><span class="sxs-lookup"><span data-stu-id="a3ab9-103">Post expense reports</span></span>

<span data-ttu-id="a3ab9-104">När en utgiftsrapport har godkänts och överförts till den allmänna journalen kan den bokföras.</span><span class="sxs-lookup"><span data-stu-id="a3ab9-104">After an expense report has been approved and transferred to the general journal, it can be posted.</span></span> <span data-ttu-id="a3ab9-105">När du bokför en utgiftsrapport identifieras utgifter som är berättigade att få tillbaka moms.</span><span class="sxs-lookup"><span data-stu-id="a3ab9-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="a3ab9-106">Uppgiften att kontrollera och få tillbaka moms tilldelas den medarbetare som ansvarar för att kontrollera utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="a3ab9-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="a3ab9-107">Om utgifter i en utgiftsrapport debiteras ett företag som inte är samma företag där medarbetar arbetar, måste du kontrollera både företaget som dessa utgifter är skyldiga till och företaget de är skyldiga från.</span><span class="sxs-lookup"><span data-stu-id="a3ab9-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify both the company that those expenses are owed to and the company that they are owed from.</span></span> <span data-ttu-id="a3ab9-108">Den anställde som har skickat en utgiftsrapport fungerar till exempel för DAT-företaget men debiterar en utgift i DIR-företaget.</span><span class="sxs-lookup"><span data-stu-id="a3ab9-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="a3ab9-109">I det här fallet är DAT det företag som utgiften är skyldig till och DIR är det företag som utgiften är skyldig från.</span><span class="sxs-lookup"><span data-stu-id="a3ab9-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="a3ab9-110">När du har kontrollerat dessa journalrader kan du bokföra utgiftsraderna i huvudboken.</span><span class="sxs-lookup"><span data-stu-id="a3ab9-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="a3ab9-111">Om du vill bokföra en utgiftsrapport på sidan **Godkända utgiftsrapporter** väljer du utgiftsrapport och sedan, i åtgärdsfönstret, väljer du **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="a3ab9-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="a3ab9-112">Du kan också bokföra alla utgiftsrapporter i listan på samma gång.</span><span class="sxs-lookup"><span data-stu-id="a3ab9-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="a3ab9-113">Välj alla utgiftsrapporter och välj sedan **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="a3ab9-113">Select all the expense reports, and then select **Post**.</span></span>
