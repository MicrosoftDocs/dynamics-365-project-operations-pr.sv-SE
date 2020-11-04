---
title: Koncerninterna utgifter
description: En arbetare som är anställd av en juridisk person i en organisation kan utföra arbete för en annan juridisk person i samma organisation. I det här fallet kan du använda funktionen för koncernintern utgift för att tilldela arbetarens utgifter till den juridiska personen för vilken arbetet har utförts.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085691"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="fa90e-104">Koncerninterna utgifter</span><span class="sxs-lookup"><span data-stu-id="fa90e-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa90e-105">En arbetare som är anställd av en juridisk person i en organisation kan utföra arbete för en annan juridisk person i samma organisation.</span><span class="sxs-lookup"><span data-stu-id="fa90e-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="fa90e-106">I det här fallet kan du använda funktionen för koncernintern utgift för att tilldela arbetarens utgifter till den juridiska personen för vilken arbetet har utförts.</span><span class="sxs-lookup"><span data-stu-id="fa90e-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="fa90e-107">Den juridiska personen där medarbetaren är anställd kallas utlånande juridisk person.</span><span class="sxs-lookup"><span data-stu-id="fa90e-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="fa90e-108">Den juridiska personen för vilken medarbetaren ådrar sig utgifter kallas lånande juridisk person.</span><span class="sxs-lookup"><span data-stu-id="fa90e-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="fa90e-109">Innan en medarbetare kan skapa och skicka in utgifter för arbete som utförs för en annan juridisk person går du till sidan **Parametrar för utgiftshantering** och väljer alternativet **Tillåt koncerninterna utgiftsrader**.</span><span class="sxs-lookup"><span data-stu-id="fa90e-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="fa90e-110">Momsbokföring för koncerninterna utgifter</span><span class="sxs-lookup"><span data-stu-id="fa90e-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa90e-111">Om du vill använda momsgrupper som är associerade med den utlånande juridiska personen (källa) i stället för den lånande juridiska personen (mål) i utgiftsrapporten, måste du konfigurera detta i redovisningens momskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="fa90e-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="fa90e-112">När redovisningsparametern **Juridisk person för bokföring av koncernintern moms** är inställd på **Källa** och **Tillämpa skatteregler för moms** är inställd på **Nej** används momskombinationen för den utlånande juridiska personen.</span><span class="sxs-lookup"><span data-stu-id="fa90e-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="fa90e-113">När samma parameter anges till **Destination** används momskombinationen för lånande juridisk person.</span><span class="sxs-lookup"><span data-stu-id="fa90e-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="fa90e-114">För juridiska personer i USA, när parametern är inställd på **Källa** , måste också fältet **Momsfordran** konfigureras på sidan **Bokföringsgrupper i transaktionsregister**.</span><span class="sxs-lookup"><span data-stu-id="fa90e-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="fa90e-115">Redovisningsmotorn använder informationen från det här fältet för momsrelaterade redovisningsposter.</span><span class="sxs-lookup"><span data-stu-id="fa90e-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="fa90e-116">Beteendet är konsekvent för utgiftsrader som har bokförts med eller utan projekt.</span><span class="sxs-lookup"><span data-stu-id="fa90e-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
