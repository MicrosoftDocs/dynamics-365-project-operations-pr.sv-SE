---
title: Skapa prognosmodeller för projektbudgetar
description: I det här ämnet beskrivs hur du skapar en prognosmodell för resterande budgetar.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271060"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="ed960-103">Skapa prognosmodeller för projektbudgetar</span><span class="sxs-lookup"><span data-stu-id="ed960-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed960-104">I det här ämnet beskrivs hur du skapar en prognosmodell för resterande budgetar.</span><span class="sxs-lookup"><span data-stu-id="ed960-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="ed960-105">I ett projekt som är underställt budgetkontroll används två typer av budget: ursprunglig och resterande.</span><span class="sxs-lookup"><span data-stu-id="ed960-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="ed960-106">När du skapar en projektbudget måste du ange de prognosmodeller för ursprunglig och resterande budget som skapades på sidan **Prognosmodeller**.</span><span class="sxs-lookup"><span data-stu-id="ed960-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="ed960-107">Projektbudgetar som bygger på de angivna modellerna skapas när du fastställer projektbudgeten.</span><span class="sxs-lookup"><span data-stu-id="ed960-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="ed960-108">En prognosmodell som används för budgetkontroll kan inte ha en delmodell eller användas som en delmodell.</span><span class="sxs-lookup"><span data-stu-id="ed960-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="ed960-109">Välj **Projekthantering och redovisning** > **Konfiguration** > **Prognoser**  > **Prognosmodeller**.</span><span class="sxs-lookup"><span data-stu-id="ed960-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="ed960-110">Välj **Ny** om du vill skapa en ny prognosmodell och ange sedan ID-nummer och namn för den nya modellen.</span><span class="sxs-lookup"><span data-stu-id="ed960-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="ed960-111">Ange alternativet **Stoppad** till **Ja** om du vill förhindra att prognosraderna för prognosmodellen ändras.</span><span class="sxs-lookup"><span data-stu-id="ed960-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="ed960-112">Om prognosraderna som modellen är kopplad till ska generera kassaflödesprognoser i redovisningen anger du **Inkludera i kassaflödesprognoser** till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ed960-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="ed960-113">Om du vill använda projektdatumet som fakturadatum anger du **Prognosfakturadatum** till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ed960-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="ed960-114">I fältet **Budgettyp** väljer du en av följande modelltyper:</span><span class="sxs-lookup"><span data-stu-id="ed960-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="ed960-115">**Ursprunglig budget**: Använd de ursprungliga budgetbeloppen som har fastställts när den inledande budgeten skapas och godkänns.</span><span class="sxs-lookup"><span data-stu-id="ed960-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="ed960-116">**Resterande budget**: Använd resterande budgetbelopp under projektets livslängd.</span><span class="sxs-lookup"><span data-stu-id="ed960-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="ed960-117">Saldon i denna prognosmodell minskas genom faktiska transaktioner och ökas eller minskas genom budgetrevideringar.</span><span class="sxs-lookup"><span data-stu-id="ed960-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="ed960-118">**Överför**: Använd de överförda budgetbeloppen för projektet.</span><span class="sxs-lookup"><span data-stu-id="ed960-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="ed960-119">Överföring är en frivillig process som kan köras för att överföra oanvända budgetbelopp från ett räkenskapsår till ett annat.</span><span class="sxs-lookup"><span data-stu-id="ed960-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="ed960-120">Ange följande alternativ efter behov:</span><span class="sxs-lookup"><span data-stu-id="ed960-120">Set the following options as required:</span></span>

   - <span data-ttu-id="ed960-121">Aktivera **Prognosfakturadatum** om du vill använda projektdatumet som fakturadatum.</span><span class="sxs-lookup"><span data-stu-id="ed960-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="ed960-122">Aktivera **Prognos med PIA** för prognos baserad på pågående arbete (PIA) och välj sedan typ av PIA.</span><span class="sxs-lookup"><span data-stu-id="ed960-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="ed960-123">Du kan behålla den förvalda **budgettypen** som **Ingen** eller ange en ny typ.</span><span class="sxs-lookup"><span data-stu-id="ed960-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="ed960-124">Budgettypen kan inte ändras när du har ändrat en post.</span><span class="sxs-lookup"><span data-stu-id="ed960-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="ed960-125">Om du ändrar den förvalda budgettypen blir inga andra alternativ tillgängliga för uppdatering och du kan inte återanvända prognosmodellen.</span><span class="sxs-lookup"><span data-stu-id="ed960-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]