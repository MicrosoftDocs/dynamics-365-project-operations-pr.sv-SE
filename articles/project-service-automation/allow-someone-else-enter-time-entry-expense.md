---
title: Låta någon annan ange din tidspost eller utgifter
description: Hur du tillåter någon annan att ange din tidsangivelse eller utgift i Project Service
author: revathiMuthiah
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 7/31/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 553cb9e3-8294-4469-b9f5-f0ef2d51f1f0
ms.author: revathim
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: dce23a1de2d56bcb6b20ec095b971cb23951c45c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756236"
---
# <a name="allow-someone-else-to-enter-your-time-entry-or-expense-project-service"></a><span data-ttu-id="be4be-103">Tillåt någon annan att ange din tidsangivelse eller utgift (Project Service)</span><span class="sxs-lookup"><span data-stu-id="be4be-103">Allow someone else to enter your time entry or expense (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="be4be-104">Skapa ett ombud för att låta någon annan skapa tids- eller utgiftsposter för din räkning i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] .</span><span class="sxs-lookup"><span data-stu-id="be4be-104">Set up a delegate to let someone else make time or expense entries on your behalf in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  
  
## <a name="create-a-delegate"></a><span data-ttu-id="be4be-105">Skapa ett ombud</span><span class="sxs-lookup"><span data-stu-id="be4be-105">Create a delegate</span></span>  
  
1.  <span data-ttu-id="be4be-106">I huvudmenyn klickar du på **Project Service** > **Delegeringar**.</span><span class="sxs-lookup"><span data-stu-id="be4be-106">From the main menu, click **Project Service** > **Delegations**.</span></span>  
  
2.  <span data-ttu-id="be4be-107">Klicka på **Nytt** i kommandofältet.</span><span class="sxs-lookup"><span data-stu-id="be4be-107">On the command bar, click **New**.</span></span>  
  
3. <span data-ttu-id="be4be-108">**Namn**: Ange ett namn för posten.</span><span class="sxs-lookup"><span data-stu-id="be4be-108">**Name**: Enter a name for the record.</span></span>  
  
4. <span data-ttu-id="be4be-109">**Typ**: Välj om ombudet kan ange poster för tid eller utgift för din räkning.</span><span class="sxs-lookup"><span data-stu-id="be4be-109">**Type**: Select whether the delegate can enter time or expense entries on your behalf.</span></span>  
  
5. <span data-ttu-id="be4be-110">**Ombud**: Välj namnet på den person som du vill utse till ombud.</span><span class="sxs-lookup"><span data-stu-id="be4be-110">**Delegate**: Select the name of the person you want to be the delegate.</span></span>  
  
6. <span data-ttu-id="be4be-111">**Start- och slutdatum**: Välj de datum då delegering börjar och slutar.</span><span class="sxs-lookup"><span data-stu-id="be4be-111">**Start and end dates**: Choose dates when delegation starts and ends.</span></span>  
  
7.  <span data-ttu-id="be4be-112">Klicka på **Spara och stäng** när du är klar.</span><span class="sxs-lookup"><span data-stu-id="be4be-112">When you're done, click **Save & Close**.</span></span>  
  
## <a name="turn-off-delegation"></a><span data-ttu-id="be4be-113">Stäng av delegering</span><span class="sxs-lookup"><span data-stu-id="be4be-113">Turn off delegation</span></span>  
  
1.  <span data-ttu-id="be4be-114">I huvudmenyn klickar du på **Project Service** > **Delegeringar**.</span><span class="sxs-lookup"><span data-stu-id="be4be-114">From the main menu, click **Project Service** > **Delegations**.</span></span>  
  
2.  <span data-ttu-id="be4be-115">Välj den delegeringspost som du vill stänga av.</span><span class="sxs-lookup"><span data-stu-id="be4be-115">Select the delegation record you want to turn off.</span></span>  
  
3.  <span data-ttu-id="be4be-116">Klicka på **Avaktivera** i kommandofältet.</span><span class="sxs-lookup"><span data-stu-id="be4be-116">On the command bar, click **Deactivate**.</span></span>  
  
4.  <span data-ttu-id="be4be-117">I dialogrutan **Bekräfta inaktivering** klcikar du på **Inaktivera**.</span><span class="sxs-lookup"><span data-stu-id="be4be-117">On the **Confirm Deactivation** dialog box, click **Deactivate**.</span></span>  
  
## <a name="enter-time-for-someone-else"></a><span data-ttu-id="be4be-118">Ange tid för någon annan</span><span class="sxs-lookup"><span data-stu-id="be4be-118">Enter time for someone else</span></span>  
  
1.  <span data-ttu-id="be4be-119">I huvudmenyn klickar du på **Project Service** > **Tidsposter**.</span><span class="sxs-lookup"><span data-stu-id="be4be-119">From the main menu, click **Project Service** > **Time Entries**.</span></span>  
  
2.  <span data-ttu-id="be4be-120">I kommandofältet väljer du listrutemenyn **RESURSNAMN** och markerar namnet på den person som du anger tid för.</span><span class="sxs-lookup"><span data-stu-id="be4be-120">On the command bar, select the **RESOURCE NAME** drop-down menu, and select the name of the person who you’re entering time for.</span></span>  
  
3.  <span data-ttu-id="be4be-121">Klicka på **OK**.</span><span class="sxs-lookup"><span data-stu-id="be4be-121">Click **OK**.</span></span>  
  
4.  <span data-ttu-id="be4be-122">Kalendern visas.</span><span class="sxs-lookup"><span data-stu-id="be4be-122">This brings up the calendar.</span></span> <span data-ttu-id="be4be-123">Om du vill se kalendern för föregående eller nästa vecka klickar du på **Föregående** eller **Nästa**.</span><span class="sxs-lookup"><span data-stu-id="be4be-123">To see the calendar for the previous or next week, click **Previous** or **Next**.</span></span> <span data-ttu-id="be4be-124">Klicka på **Idag** för att komma tillbaka till den aktuella veckan.</span><span class="sxs-lookup"><span data-stu-id="be4be-124">Click **Today** to get back to the current week.</span></span>  
  
5.  <span data-ttu-id="be4be-125">Om du vill ange din tid klickar du antingen på **Ny**, eller också dubbelklickar du i kalendern under den dag som du vill registrera tid för.</span><span class="sxs-lookup"><span data-stu-id="be4be-125">To enter your time, either click **New** or double-click in the calendar under the day you want to enter time for.</span></span>  
  
6.  <span data-ttu-id="be4be-126">Fyll i fälten i formuläret **Tidspost** och klicka på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="be4be-126">Fill in the fields in the **Time Entry** form and click **Save**.</span></span>  
  
7.  <span data-ttu-id="be4be-127">Fortsätt att ange tid för veckan.</span><span class="sxs-lookup"><span data-stu-id="be4be-127">Continue entering time for the week.</span></span> <span data-ttu-id="be4be-128">När du är klar och allt ser korrekt ut klickar du på **Skicka**.</span><span class="sxs-lookup"><span data-stu-id="be4be-128">When you’re done and everything looks correct, click **Submit**.</span></span>  
  
## <a name="enter-expenses-for-someone-else"></a><span data-ttu-id="be4be-129">Ange utgifter för någon annan</span><span class="sxs-lookup"><span data-stu-id="be4be-129">Enter expenses for someone else</span></span>  
  
1.  <span data-ttu-id="be4be-130">I huvudmenyn klickar du på **Project Service** > **Utgifter**.</span><span class="sxs-lookup"><span data-stu-id="be4be-130">From the main menu, click **Project Service** > **Expenses**.</span></span>  
  
2.  <span data-ttu-id="be4be-131">I kommandofältet väljer du listrutemenyn **RESURSNAMN** och markerar namnet på den person som du anger utgifter för.</span><span class="sxs-lookup"><span data-stu-id="be4be-131">On the command bar, select the **RESOURCE NAME** drop-down menu, and select the name of the person who you’re entering expenses for.</span></span>  
  
3.  <span data-ttu-id="be4be-132">Klicka på **OK**.</span><span class="sxs-lookup"><span data-stu-id="be4be-132">Click **OK**.</span></span>  
  
4.  <span data-ttu-id="be4be-133">Om du vill se kalendern för föregående eller nästa vecka klickar du på **Föregående** eller **Nästa**.</span><span class="sxs-lookup"><span data-stu-id="be4be-133">To see the calendar for the previous or next week, click **Previous** or **Next**.</span></span> <span data-ttu-id="be4be-134">Klicka på **Idag** för att komma tillbaka till den aktuella veckan.</span><span class="sxs-lookup"><span data-stu-id="be4be-134">Click **Today** to get back to the current week.</span></span>  
  
5.  <span data-ttu-id="be4be-135">Om du vill ange en utgift klickar du antingen på **Ny**</span><span class="sxs-lookup"><span data-stu-id="be4be-135">To enter an expense, either click **New**</span></span>  
  
6.  <span data-ttu-id="be4be-136">Fyll i fälten i formuläret **Ny utgift**.</span><span class="sxs-lookup"><span data-stu-id="be4be-136">Fill in the fields in the **New Expense** form.</span></span> <span data-ttu-id="be4be-137">Du kan också lägga till kvitton.</span><span class="sxs-lookup"><span data-stu-id="be4be-137">You can also add receipts.</span></span>  
  
7.  <span data-ttu-id="be4be-138">När du är klar klickar du på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="be4be-138">When you’re done, click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="be4be-139">Se även</span><span class="sxs-lookup"><span data-stu-id="be4be-139">See Also</span></span>  
 [<span data-ttu-id="be4be-140">Guide för tid, utgifter och samarbete</span><span class="sxs-lookup"><span data-stu-id="be4be-140">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
