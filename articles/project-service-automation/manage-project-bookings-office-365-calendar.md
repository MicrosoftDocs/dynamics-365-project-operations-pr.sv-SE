---
title: Hantera projekt och bokningar i din Office 365-kalender
description: Så här hanterar du projekt och bokningar i din Office 365-kalender
author: ruhercul
manager: kfend
ms.service: dynamics-365-projectservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 92428956-1058-4490-934f-907fbbdc8f25
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5c075e0b63db35c1e189a62a6b5b00f5bcb7ea97
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756132"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a><span data-ttu-id="1e5d7-103">Hantera projekt och bokningar i din kalender (Project Service)</span><span class="sxs-lookup"><span data-stu-id="1e5d7-103">Manage projects and bookings in your calendar (Project Service)</span></span>

> [!Note]
> <span data-ttu-id="1e5d7-104">INAKTUELLT: Den här funktionen har utfasats och är inte längre tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-104">DEPRECATED: This feature has been deprecated and is no longer available.</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

<span data-ttu-id="1e5d7-105">Visa personliga möten, projektarbetsbokningar och arbetsorder för Field Service-tilldelningar med hjälp av [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalendern.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-105">View personal appointments, project-work bookings, and field service work order assignments using the [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="1e5d7-106">Eftersom allt är samlat på ett ställe, blir det enkelt att hantera din dag.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-106">With everything in one place, it’s easy to manage your day.</span></span> <span data-ttu-id="1e5d7-107">Dina möten, avtalade tider, bokningar och uppgifter är tillgängliga i din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-107">Your meetings, appointments, bookings, and tasks are all available in your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="1e5d7-108">Om du använder [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kan du också ange dina personliga möten i tidinmatningsvyn för Project Service.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-108">If you’re using [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you can also enter your personal appointments in the Project Service time entry view.</span></span> <span data-ttu-id="1e5d7-109">Detta gör att projekt- och resursansvariga vet din tillgänglighet för projekt.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-109">This lets project and resource managers know your availability for projects.</span></span> <span data-ttu-id="1e5d7-110">Dessutom sparar du tid eftersom du inte behöver ange information om privata möten två gånger.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-110">It also saves you time, because you don’t have to enter info about your personal appointments twice.</span></span> <span data-ttu-id="1e5d7-111">Du kan helt enkelt importera dina personliga möten från din kalender till tidinmatningsvyn för Project Service.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-111">You can simply import your personal appointments from your calendar to Project Service time entry view.</span></span>  
  
 <span data-ttu-id="1e5d7-112">Din kalender synkroniserar projekt- och arbetsorderbokningar från dagens datum och upp till fyra veckor framåt.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-112">Your calendar will sync project and work order bookings from today to upcoming four weeks.</span></span> <span data-ttu-id="1e5d7-113">Denna inställning kan inte ändras.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-113">This setting can’t be changed.</span></span>  
  
 <span data-ttu-id="1e5d7-114">Synkroniserar stöds endast åt ena hållet, från PSA till din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-114">Syncing is only supported one way, from PSA to your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span> <span data-ttu-id="1e5d7-115">Du kan synkronisera i omvänd ordning.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-115">You can sync in the reverse order.</span></span> 
  
 <span data-ttu-id="1e5d7-116">För information om hur du använder din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender, se [Kalendern i Outlook på webben för företag](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span><span class="sxs-lookup"><span data-stu-id="1e5d7-116">To learn how to use your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, see [Calendar in Outlook on the web for business](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span></span>  
  
## <a name="setup"></a><span data-ttu-id="1e5d7-117">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="1e5d7-117">Setup</span></span>  
 <span data-ttu-id="1e5d7-118">Innan du kan visa och hantera dina bokningar i din [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender, måste du konfigurera ett par saker.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-118">Before you can see and manage your bookings on your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, you need to set a few things up.</span></span>  
  
- <span data-ttu-id="1e5d7-119">Du måste ha autentiseringsuppgifter för [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] global administratör eller Dynamics 365-systemadministratör.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-119">You will need to have [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Global Administrator or System Administrator credentials.</span></span>  
  
- <span data-ttu-id="1e5d7-120">Din administratör måste konfigurera e-postserverprofilen, och varje enskild användare måste konfigurera sin e-postlåda.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-120">Your Admin will need to configure the email server profile and each user will need to configure their mailbox.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="1e5d7-121">[Ställa in e-postbearbetning via serversynkronisering](../admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="1e5d7-121">[Set up email processing through server-side synchronization](../admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks.md)</span></span>  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a><span data-ttu-id="1e5d7-122">Aktivera synkronisering för din organisation (administratörsuppgift)</span><span class="sxs-lookup"><span data-stu-id="1e5d7-122">Turn on synchronization for your organization (admin task)</span></span>  
  
1.  <span data-ttu-id="1e5d7-123">I huvudmenyn klickar du på **Inställningar** > **Administration**.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-123">From the main menu, click **Settings** > **Administration**.</span></span>  
  
2.  <span data-ttu-id="1e5d7-124">Klicka på **Systeminställningar.**</span><span class="sxs-lookup"><span data-stu-id="1e5d7-124">Click **System Settings**.</span></span>  
  
3.  <span data-ttu-id="1e5d7-125">Klicka på fliken **Synkronisering**.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-125">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="1e5d7-126">Under **Välja om du vill aktivera synkronisering av resursbokning med**, markera **Synkronisera resursbokning med Outlook**.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-126">Under **Select whether to enable syncing of resource booking with**, check the **Synchronize resource booking with Outlook**.</span></span>  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a><span data-ttu-id="1e5d7-127">Aktivera synkronisering för din användarprofil (användaraktivitet)</span><span class="sxs-lookup"><span data-stu-id="1e5d7-127">Turn on synchronization for your user profile (user task)</span></span>  
  
1.  <span data-ttu-id="1e5d7-128">Klicka på knappen **Inställningar** längst upp till höger på skärmen.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-128">Click the **Settings** button in the upper-right corner of the screen.</span></span>  
  
2.  <span data-ttu-id="1e5d7-129">Klicka på **Alternativ**.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-129">Click **Options**.</span></span>  
  
3.  <span data-ttu-id="1e5d7-130">Klicka på fliken **Synkronisering**.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-130">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="1e5d7-131">Under **Resursbokningssynkronisering med Outlook** markerar du **Synkronisera resursbokning med Outlook**.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-131">Under **Resource booking sync with Outlook**, check the **Synchronization resource booking with Outlook**.</span></span>  
  
## <a name="import-your-personal-appointments-user-task"></a><span data-ttu-id="1e5d7-132">Importera dina personliga möten (användaraktivitet)</span><span class="sxs-lookup"><span data-stu-id="1e5d7-132">Import your personal appointments (user task)</span></span>  
 <span data-ttu-id="1e5d7-133">Du kan importera dina personliga möten från din kalender till inmatningsvyn för Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-133">You can import your personal appointments from your calendar to Project Service Automation time entry view.</span></span>  
  
1. <span data-ttu-id="1e5d7-134">Öppna kalendern i [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] och klicka på **Importera data**.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-134">Open [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar and click **Import Data**.</span></span>  
  
2. <span data-ttu-id="1e5d7-135">Välj **Möten från Exchange** på skärmen Filter, och klicka sedan på **Använd**.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-135">On the Filters screen, select **Appointments from Exchange** and then click **Apply**.</span></span>  
  
3. <span data-ttu-id="1e5d7-136">Systemet kommer att hämta avtalade tider i inmatningsvyn för tid i form av föreslagna poster från den aktuella veckan.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-136">The system will pull appointments into time entry view as suggested entries from the current week.</span></span> <span data-ttu-id="1e5d7-137">Klicka på **Föregående** eller **Nästa**.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-137">To add entries for another week, click **Previous** or **Next**.</span></span>  
  
4. <span data-ttu-id="1e5d7-138">Markera den avtalade tiden som du vill lägga till i inmatningsvyn för Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-138">Select the appointment that you want to add to Project Service Automation time entry view.</span></span>  
  
5. <span data-ttu-id="1e5d7-139">I popup-rutan **Tidspost** markerar du lämpliga alternativ för att konvertera den avtalade tiden till en inmatningsvy för Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-139">On the **Time Entry** popup box, select the appropriate options to convert the appointment to a Project Service Automation time entry view.</span></span>  
  
6. <span data-ttu-id="1e5d7-140">Klicka på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="1e5d7-140">Click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="1e5d7-141">Se även</span><span class="sxs-lookup"><span data-stu-id="1e5d7-141">See Also</span></span>  
 [<span data-ttu-id="1e5d7-142">Guide för tid, utgifter och samarbete</span><span class="sxs-lookup"><span data-stu-id="1e5d7-142">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
