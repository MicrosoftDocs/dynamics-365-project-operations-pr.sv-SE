---
title: Hantera intäktsberäkningar
description: Detta ämne innehåller information om hur du arbetar med intäktsuppskattningar för projekt.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531567"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="29740-103">Hantera intäktsberäkningar</span><span class="sxs-lookup"><span data-stu-id="29740-103">Manage revenue estimates</span></span>

<span data-ttu-id="29740-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="29740-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="29740-105">Du kan skapa, beräkna, bokföra, återställa eller eliminera intäktsuppskattningar.</span><span class="sxs-lookup"><span data-stu-id="29740-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="29740-106">Du kan göra detta antingen manuellt eller genom att använda en periodisk process.</span><span class="sxs-lookup"><span data-stu-id="29740-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="29740-107">Detta ämne innehåller information om hur du arbetar med intäktsuppskattningar för projekt.</span><span class="sxs-lookup"><span data-stu-id="29740-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="29740-108">Hantera intäktsberäkningar manuellt</span><span class="sxs-lookup"><span data-stu-id="29740-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="29740-109">På sidan för intäktsberäkningar för fastprisprojektet eller **Uppskattningsförfrågan** (**Projektledning och redovisning** > **Rapporter och förfrågningar** > **Uppskattningsförfrågningar och -rapporter**), välj **Uppskattningar**.</span><span class="sxs-lookup"><span data-stu-id="29740-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="29740-110">Hantera intäktsuppskattningar med hjälp av en periodisk process</span><span class="sxs-lookup"><span data-stu-id="29740-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="29740-111">Gå till **Projektledning och redovisning** > **Periodisk** > **Uppskattningar** och välj motsvarande process.</span><span class="sxs-lookup"><span data-stu-id="29740-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="29740-112">Skapa en intäktsuppskattning</span><span class="sxs-lookup"><span data-stu-id="29740-112">Create a revenue estimate</span></span>

<span data-ttu-id="29740-113">Slutför följ steg om du vill skapa en intäktsuppskattning.</span><span class="sxs-lookup"><span data-stu-id="29740-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="29740-114">Gå till **Projektledning och redovisning** > **Periodisk** > **Uppskattningar**.</span><span class="sxs-lookup"><span data-stu-id="29740-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="29740-115">Välj **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="29740-115">Select **New**.</span></span> <span data-ttu-id="29740-116">På sidan **Skapa uppskattning** och välj följande parametrar:</span><span class="sxs-lookup"><span data-stu-id="29740-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="29740-117">**Periodkod**: Denna kod bestämmer hur ofta uppskattningar bokförs.</span><span class="sxs-lookup"><span data-stu-id="29740-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="29740-118">**Uppskattningsdatum**: Det datum då uppskattningen bearbetas.</span><span class="sxs-lookup"><span data-stu-id="29740-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="29740-119">**Kontinuerlig**: Markera denna kryssruta om du vill skapa uppskattningar endast om uppskattningar bokfördes i föregående period, eller om uppskattningen är den första uppskattning som har skapats.</span><span class="sxs-lookup"><span data-stu-id="29740-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="29740-120">Om detta val inte är markerat skapas uppskattningar även om uppskattningar inte bokfördes i föregående period.</span><span class="sxs-lookup"><span data-stu-id="29740-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="29740-121">**Kostnad för att slutföra metod**: Definiera hur du ska uppskatta det återstående projektarbetet.</span><span class="sxs-lookup"><span data-stu-id="29740-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="29740-122">Mer information finns i [Kostnad för att slutföra metoder](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="29740-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="29740-123">**Slutförandemetod**: Välj en slutförandemetod bland följande alternativ:</span><span class="sxs-lookup"><span data-stu-id="29740-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="29740-124">**Automatisk**: Slutförandeprocenten beräknas automatiskt och baserat på de kostnadsrader som ingår i beräkningen.</span><span class="sxs-lookup"><span data-stu-id="29740-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="29740-125">Kostnadsmallen definierar de kostnadsrader som ingår.</span><span class="sxs-lookup"><span data-stu-id="29740-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="29740-126">**Handbok**: Slutförandeprocenten är lika med slutförandeprocenten för den senaste uppskattningen.</span><span class="sxs-lookup"><span data-stu-id="29740-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="29740-127">När uppskattningen har skapats kan du ändra den **manuella beräkningen** på sidan **Uppskattningar**.</span><span class="sxs-lookup"><span data-stu-id="29740-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="29740-128">**Från kostnadsmall**: En kombination av de automatiska och manuella metoderna.</span><span class="sxs-lookup"><span data-stu-id="29740-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="29740-129">Detta alternativ ställs in automatiskt eller manuellt, beroende på standardvärdet i kostnadsmallen.</span><span class="sxs-lookup"><span data-stu-id="29740-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="29740-130">**Prognosmodell**: Välj en prognosmodell för uppskattningen.</span><span class="sxs-lookup"><span data-stu-id="29740-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="29740-131">**Skriv ut uppskattningslista**: Skapa och visa en uppskattningslista.</span><span class="sxs-lookup"><span data-stu-id="29740-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="29740-132">Listan innehåller status för den aktuella funktionen.</span><span class="sxs-lookup"><span data-stu-id="29740-132">The list contains the status of the current function.</span></span> <span data-ttu-id="29740-133">Du kan skriva ut eventuella varningar om uppskattningen på rapporten.</span><span class="sxs-lookup"><span data-stu-id="29740-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="29740-134">Följande villkor gör att varningar visas i uppskattningslistan:</span><span class="sxs-lookup"><span data-stu-id="29740-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="29740-135">En slutförandeprocent på mer än 100 procent.</span><span class="sxs-lookup"><span data-stu-id="29740-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="29740-136">En slutförandeprocent på under noll procent.</span><span class="sxs-lookup"><span data-stu-id="29740-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="29740-137">Ett negativt belopp i kolumnen **Att slutföra**.</span><span class="sxs-lookup"><span data-stu-id="29740-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="29740-138">En uppskattning utan motsvarande kontraktsbelopp.</span><span class="sxs-lookup"><span data-stu-id="29740-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="29740-139">En uppskattning utan bifogad kostnadsberäkning.</span><span class="sxs-lookup"><span data-stu-id="29740-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="29740-140">**Visa Infologg**: Välj det här alternativet om du vill få ett meddelande som innehåller information om de uppskattningsprojekt som bearbetades när jobbet kördes.</span><span class="sxs-lookup"><span data-stu-id="29740-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="29740-141">Bokför PIA eller periodiseringar</span><span class="sxs-lookup"><span data-stu-id="29740-141">Post WIP or accruals</span></span>

<span data-ttu-id="29740-142">Efter det att uppskattningarna har utvärderats bibehålls, minskas eller ökas de.</span><span class="sxs-lookup"><span data-stu-id="29740-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="29740-143">Du kan sedan bokföra PIA när du arbetar med bedömningsprincipen **Slutfört kontrakt** eller också bokföra periodiseringarna när du arbetar med bedömningsprincipen **Slutförd procentandel**.</span><span class="sxs-lookup"><span data-stu-id="29740-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="29740-144">Statusen för uppskattningsperioden ändras från **Skapad** till **Bokförd**.</span><span class="sxs-lookup"><span data-stu-id="29740-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="29740-145">Omvänd PIA eller periodiseringar</span><span class="sxs-lookup"><span data-stu-id="29740-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="29740-146">Använd omvändningsalternativet för att kreditera redan bokförda PIA eller periodiseringar, och skapa sedan uppskattningar för perioden.</span><span class="sxs-lookup"><span data-stu-id="29740-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="29740-147">Om du vill omvända en period som ligger mellan andra perioder omvänder du erforderliga uppskattningsperioder och bokför dem sedan på nytt.</span><span class="sxs-lookup"><span data-stu-id="29740-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="29740-148">Eftersom alla efterföljande perioder är beroende av uppskattningarna från föregående period ska du inte hoppa över några perioder.</span><span class="sxs-lookup"><span data-stu-id="29740-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="29740-149">Eliminera uppskattningsprojektet och avsluta projektet</span><span class="sxs-lookup"><span data-stu-id="29740-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="29740-150">Det sista steget i uppskattningsprocessen är att eliminera uppskattningsprojektet och avsluta fastprisprojektet när slutförandeprocenten når 100 procent.</span><span class="sxs-lookup"><span data-stu-id="29740-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="29740-151">Följande inträffar när du kör elimineringen:</span><span class="sxs-lookup"><span data-stu-id="29740-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="29740-152">För ett fastprisprojekt med ett slutfört kontrakt rensar PIA-värdena från saldokontona och bokför på vinst- och förlustkontona.</span><span class="sxs-lookup"><span data-stu-id="29740-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="29740-153">För ett fastprisprojekt med slutförd procentandel tas periodiseringarna bort från vinst- och förlustkontona.</span><span class="sxs-lookup"><span data-stu-id="29740-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="29740-154">Uppskattningen ändrar status till **Eliminerad**.</span><span class="sxs-lookup"><span data-stu-id="29740-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="29740-155">I särskilda fall kan procentsatsen sträcka sig längre än 100 procent.</span><span class="sxs-lookup"><span data-stu-id="29740-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="29740-156">När detta händer minskar du slutförandeprocenten med hjälp av **Metoden Ange kostnad för att slutföra till noll** för att nå 100 procent.</span><span class="sxs-lookup"><span data-stu-id="29740-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="29740-157">Omvänd eliminering</span><span class="sxs-lookup"><span data-stu-id="29740-157">Reverse elimination</span></span>

1. <span data-ttu-id="29740-158">Gå till **Projektledning och redovisning** > **Periodisk** > **Uppskattningar** > **Omvänd eliminering**.</span><span class="sxs-lookup"><span data-stu-id="29740-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="29740-159">I fliken **Process** i åtgärdsfönstret väljer du gruppen **Underhåll** och sedan **Uppskattning**.</span><span class="sxs-lookup"><span data-stu-id="29740-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="29740-160">Välj **Omvänd eliminering**.</span><span class="sxs-lookup"><span data-stu-id="29740-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="29740-161">Använd den här sidan om du vill omvända alla elimineringar med ett angivet uppskattningsdatum och med uppskattningsstatusen **Eliminerad**.</span><span class="sxs-lookup"><span data-stu-id="29740-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="29740-162">Transaktionsstatusen ändras när du har valt lämpliga fält.</span><span class="sxs-lookup"><span data-stu-id="29740-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="29740-163">Detta ändrar också automatiskt projektstatusen till **Pågår** om projektstadiet är inställt på Slutfört.</span><span class="sxs-lookup"><span data-stu-id="29740-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="29740-164">Uppskattningsstatusen för projektperioden ändras tillbaka till **Bokförd**.</span><span class="sxs-lookup"><span data-stu-id="29740-164">The estimate status of the project period changes back to **Posted**.</span></span>
