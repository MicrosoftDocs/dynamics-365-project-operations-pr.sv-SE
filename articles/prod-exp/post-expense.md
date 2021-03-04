---
title: Bokför en utgiftsrapport
description: I det här ämnet förklaras hur du bokför en utgiftsrapport i redovisningen.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 982b7621c35547448b5d756f77f3873b9fbbcb9d
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960134"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="66030-103">Bokför en utgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="66030-103">Post an expense report</span></span>

<span data-ttu-id="66030-104">När en utgiftsrapport har godkänts och överförts till den allmänna journalen kan den bokföras i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="66030-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="66030-105">När du bokför en utgiftsrapport identifieras utgifter som är berättigade att få tillbaka moms.</span><span class="sxs-lookup"><span data-stu-id="66030-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="66030-106">Uppgiften att kontrollera och få tillbaka moms tilldelas den medarbetare som ansvarar för att kontrollera utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="66030-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="66030-107">Om utgifter i en utgiftsrapport debiteras ett företag som inte är samma företag där medarbetaren arbetar, måste du kontrollera företaget som dessa utgifter är skyldiga till och företaget som utgifterna är skyldiga från.</span><span class="sxs-lookup"><span data-stu-id="66030-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="66030-108">Den anställde som har skickat en utgiftsrapport fungerar till exempel för DAT-företaget men debiterar en utgift i DIR-företaget.</span><span class="sxs-lookup"><span data-stu-id="66030-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="66030-109">I det här fallet är DAT det företag som utgiften är skyldig till och DIR är det företag som utgiften är skyldig från.</span><span class="sxs-lookup"><span data-stu-id="66030-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="66030-110">När du har kontrollerat dessa journalrader kan du bokföra utgiftsraderna i huvudboken.</span><span class="sxs-lookup"><span data-stu-id="66030-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="66030-111">Om du vill bokföra en utgiftsrapport på sidan **Godkända utgiftsrapporter** väljer du utgiftsrapport och sedan, i åtgärdsfönstret, väljer du **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="66030-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="66030-112">Du kan också bokföra alla utgiftsrapporter i listan på samma gång.</span><span class="sxs-lookup"><span data-stu-id="66030-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="66030-113">Välj alla utgiftsrapporter och välj sedan **Bokför**.</span><span class="sxs-lookup"><span data-stu-id="66030-113">Select all the expense reports, and then select **Post**.</span></span>
