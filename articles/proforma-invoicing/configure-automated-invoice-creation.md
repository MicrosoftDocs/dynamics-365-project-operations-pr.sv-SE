---
title: Konfigurera automatiskt fakturaskapande
description: I det här ämnet finns information om hur du konfigurerar systemet för att automatiskt skapa fakturor.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0dddd963e79f8ecd91a96a6e684ab79e1b95bd6d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287935"
---
# <a name="configure-automatic-invoice-creation"></a><span data-ttu-id="d31f7-103">Konfigurera automatiskt fakturaskapande</span><span class="sxs-lookup"><span data-stu-id="d31f7-103">Configure automatic invoice creation</span></span>

<span data-ttu-id="d31f7-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="d31f7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="d31f7-105">Följ stegen nedan om du vill konfigurera automatisk fakturering i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d31f7-105">Complete the following steps to configure an automated invoice run in Dynamics 365 Project operations.</span></span>

1. <span data-ttu-id="d31f7-106">Gå till **Inställningar** > **Batchjobb**.</span><span class="sxs-lookup"><span data-stu-id="d31f7-106">Go to **Settings** > **Batch jobs**.</span></span>
2. <span data-ttu-id="d31f7-107">Skapa ett batch-jobb och ge det namnet **Project Operations skapa fakturor**.</span><span class="sxs-lookup"><span data-stu-id="d31f7-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="d31f7-108">Namnet på batch-jobbet måste innehålla orden "skapa fakturor".</span><span class="sxs-lookup"><span data-stu-id="d31f7-108">The name of the batch job must include the words "create invoices."</span></span>
3. <span data-ttu-id="d31f7-109">I fältet **Jobbtyp**, välj **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="d31f7-109">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="d31f7-110">Som standard är alternativen **Frekvens dagligen** och **Är aktiv** angivna som **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d31f7-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="d31f7-111">Välj **Kör arbetsflöde**.</span><span class="sxs-lookup"><span data-stu-id="d31f7-111">Select **Run Workflow**.</span></span> <span data-ttu-id="d31f7-112">I dialogrutan **Sök efter post** visas tre arbetsflöden:</span><span class="sxs-lookup"><span data-stu-id="d31f7-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="d31f7-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="d31f7-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="d31f7-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="d31f7-114">ProcessRunner</span></span>
    - <span data-ttu-id="d31f7-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="d31f7-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="d31f7-116">Välj **ProcessRunCaller** och välj **Lägg till**.</span><span class="sxs-lookup"><span data-stu-id="d31f7-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="d31f7-117">Klicka på **OK** i nästa dialogrutan.</span><span class="sxs-lookup"><span data-stu-id="d31f7-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="d31f7-118">Arbetsflödet **Vila** följs av **Process**.</span><span class="sxs-lookup"><span data-stu-id="d31f7-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

  > [!NOTE]
  > <span data-ttu-id="d31f7-119">Du kan också välja **ProcessRunner** i steg 5.</span><span class="sxs-lookup"><span data-stu-id="d31f7-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="d31f7-120">När du sedan väljer **OK**, följs arbetsflödet **Process** av arbetsflödet **Vila**.</span><span class="sxs-lookup"><span data-stu-id="d31f7-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="d31f7-121">Arbetsflödena **ProcessRunCaller** och **ProcessRunner** skapar fakturor.</span><span class="sxs-lookup"><span data-stu-id="d31f7-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="d31f7-122">**ProcessRunCaller** anropar **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="d31f7-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="d31f7-123">**ProcessRunner** är det arbetsflöde som verkligen skapade fakturorna.</span><span class="sxs-lookup"><span data-stu-id="d31f7-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="d31f7-124">Det går igenom alla kontraktrader som fakturorna måste skapas för och fakturor för dessa rader skapas.</span><span class="sxs-lookup"><span data-stu-id="d31f7-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="d31f7-125">För att fastställa vilka kontraktrader som fakturor ska skapas tittar jobbet på körningsdatum för faktura för kontraktraderna.</span><span class="sxs-lookup"><span data-stu-id="d31f7-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="d31f7-126">Om kontraktrader som tillhör ett kontrakt har samma datum för fakturakörning kombineras transaktionerna till en faktura med två fakturarader.</span><span class="sxs-lookup"><span data-stu-id="d31f7-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="d31f7-127">Om det inte finns några transaktioner för att skapa fakturor hoppar jobbet över skapandet av fakturan.</span><span class="sxs-lookup"><span data-stu-id="d31f7-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="d31f7-128">När **ProcessRunner** har körts klart anropas **ProcessRunCaller**, anger sluttiden och är stängd.</span><span class="sxs-lookup"><span data-stu-id="d31f7-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="d31f7-129">**ProcessRunCaller** startar sedan en timer som körs i 24 timmar från den angivna sluttiden.</span><span class="sxs-lookup"><span data-stu-id="d31f7-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="d31f7-130">**ProcessRunCaller** stängs i slutet av timern.</span><span class="sxs-lookup"><span data-stu-id="d31f7-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="d31f7-131">Batchprocessjobbet för att skapa fakturor är ett återkommande jobb.</span><span class="sxs-lookup"><span data-stu-id="d31f7-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="d31f7-132">Om batchprocessen körs flera gånger skapas flera instanser av jobbet och det uppstår fel.</span><span class="sxs-lookup"><span data-stu-id="d31f7-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="d31f7-133">Därför bör du endast starta batchprocessen en gång och du bör starta om den endast om den slutar att fungera.</span><span class="sxs-lookup"><span data-stu-id="d31f7-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="d31f7-134">Batchfakturering körs endast för projektkontraktrader som konfigurerats av fakturascheman.</span><span class="sxs-lookup"><span data-stu-id="d31f7-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="d31f7-135">En kontraktrad med en fast pris faktureringsmetod måste ha milstolpar konfigurerad.</span><span class="sxs-lookup"><span data-stu-id="d31f7-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="d31f7-136">En projekts kontraktrad med en tids- och material faktureringsmetod måste ha en datumbaserad fakturauppställning.</span><span class="sxs-lookup"><span data-stu-id="d31f7-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="d31f7-137">Detsamma gäller för en projektrelaterad kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="d31f7-137">The same applies to a project-based contract line.</span></span>     


[!INCLUDE[footer-include](../includes/footer-banner.md)]