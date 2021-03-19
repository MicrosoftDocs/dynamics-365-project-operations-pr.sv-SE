---
title: Koncerninterna utgifter
description: Detta ämne innehåller information om hur du använder koncerninterna utgifter för att tilldela en medarbetares utgifter till den juridiska person som arbetet utförts för.
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
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271555"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="c470d-103">Koncerninterna utgifter</span><span class="sxs-lookup"><span data-stu-id="c470d-103">Intercompany expenses</span></span>

<span data-ttu-id="c470d-104">En arbetare som är anställd av en juridisk person i en organisation kan utföra arbete för en annan juridisk person i samma organisation.</span><span class="sxs-lookup"><span data-stu-id="c470d-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="c470d-105">Du kan använda koncerninterna utgifter för att tilldela en medarbetares utgifter till den juridiska person som arbetet utförts för.</span><span class="sxs-lookup"><span data-stu-id="c470d-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="c470d-106">Den juridiska personen där medarbetaren är anställd kallas utlånande juridisk person.</span><span class="sxs-lookup"><span data-stu-id="c470d-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="c470d-107">Den juridiska personen för vilken medarbetaren ådrar sig utgifter kallas lånande juridisk person.</span><span class="sxs-lookup"><span data-stu-id="c470d-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="c470d-108">Innan en anställd kan skapa och skicka in koncerninterna utgifter, måste du aktivera koncerninterna kostnadsrader.</span><span class="sxs-lookup"><span data-stu-id="c470d-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="c470d-109">På sidan **Parametrar för utgiftshantering** i den utlånande juridiska entiteten väljer du **Tillåt koncerninterna utgiftsrader**.</span><span class="sxs-lookup"><span data-stu-id="c470d-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="c470d-110">Momsbokföring för koncerninterna utgifter</span><span class="sxs-lookup"><span data-stu-id="c470d-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c470d-111">Innan du kan använda momsgrupper som är associerade med den utlånande (källrelaterade) juridiska entiteten i stället för den lånande juridiska personen (associerad med destination) i utgiftsrapporten måste du aktivera funktionen i momskonfigurationen för huvudboken.</span><span class="sxs-lookup"><span data-stu-id="c470d-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="c470d-112">När parametern **Juridisk entitet för momsbokföring** har angetts som **Källa** och **Tillämpa momsregler** har angetts som **Nej** används momskombinationen för den lånande juridiska entiteten.</span><span class="sxs-lookup"><span data-stu-id="c470d-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="c470d-113">När samma parameter anges till **Destination** används momskombinationen för lånande juridisk person.</span><span class="sxs-lookup"><span data-stu-id="c470d-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="c470d-114">För juridiska personer i USA, när parametern är inställd på **Källa**, måste också fältet **Momsfordran** konfigureras på sidan **Bokföringsgrupper i transaktionsregister**.</span><span class="sxs-lookup"><span data-stu-id="c470d-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="c470d-115">Redovisningsmotorn använder informationen från det här fältet för momsrelaterade redovisningsposter.</span><span class="sxs-lookup"><span data-stu-id="c470d-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="c470d-116">Beteendet är konsekvent för utgiftsrader som har bokförts med eller utan projekt.</span><span class="sxs-lookup"><span data-stu-id="c470d-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]