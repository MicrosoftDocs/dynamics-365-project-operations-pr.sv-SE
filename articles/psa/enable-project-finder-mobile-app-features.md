---
title: Aktivera funktionerna för Project Finder Mobile-appen
description: Aktivera funktionerna i appen Project Finder Mobile för Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: af267b5adc48b6edec57de196f91e338c058558c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132985"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="74b47-103">Aktivera funktionerna för Project Finder Mobile-appen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="74b47-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="74b47-104">Dina resurser kan använda appen Project Finder Mobile på sina telefoner med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i syfte att hitta nya projekt att arbeta med och uppdatera sina kompetenser.</span><span class="sxs-lookup"><span data-stu-id="74b47-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="74b47-105">Appen finns tillgänglig för [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-telefoner och [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="74b47-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="74b47-106">Du måste ange ett par olika alternativ i parameterinställningen för din organisationsenhet så att användarna kan visa projektresurskrav och uppdatera sina färdigheter.</span><span class="sxs-lookup"><span data-stu-id="74b47-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="74b47-107">Project Finder Mobile-appen fungerar bara med [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], inte med installationer för lokal version.</span><span class="sxs-lookup"><span data-stu-id="74b47-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="74b47-108">Gå till **Project Service > Parametrar**.</span><span class="sxs-lookup"><span data-stu-id="74b47-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="74b47-109">Klicka på den parameterinställning du vill använda för att tillåta Project Finder Mobile-appfunktionerna.</span><span class="sxs-lookup"><span data-stu-id="74b47-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="74b47-110">I området **Allmänt** anger du **Resurskrav visas för resurser** till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="74b47-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="74b47-111">Ange **Tillåt resurs att uppdatera färdighet** till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="74b47-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="74b47-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="74b47-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="74b47-113">Detta är en global inställning.</span><span class="sxs-lookup"><span data-stu-id="74b47-113">This is a global setting.</span></span> <span data-ttu-id="74b47-114">Projektledare kan ange om ett enskilt projekt kommer att visas i det projektets **projektteam**-sida.</span><span class="sxs-lookup"><span data-stu-id="74b47-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="74b47-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="74b47-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="74b47-116">E-postaviseringar</span><span class="sxs-lookup"><span data-stu-id="74b47-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="74b47-117">skickar e-post som berör begäran om resurser till följande mottagare vid följande tidpunkter:</span><span class="sxs-lookup"><span data-stu-id="74b47-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="74b47-118">Mottagare</span><span class="sxs-lookup"><span data-stu-id="74b47-118">Recipient</span></span>|<span data-ttu-id="74b47-119">Händelse</span><span class="sxs-lookup"><span data-stu-id="74b47-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="74b47-120">Projektledare</span><span class="sxs-lookup"><span data-stu-id="74b47-120">Project manager</span></span>|<span data-ttu-id="74b47-121">-   När en resurs registrerar sig för ett projekt med Project Finder Mobile-appen.</span><span class="sxs-lookup"><span data-stu-id="74b47-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="74b47-122">Resurs</span><span class="sxs-lookup"><span data-stu-id="74b47-122">Resource</span></span>|<span data-ttu-id="74b47-123">-   När det projektarbete som resursen har registrerats för redan har slutförts av en annan resurs.</span><span class="sxs-lookup"><span data-stu-id="74b47-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="74b47-124">-   När deras begäran om kompetensgodkännande har godkänts eller avvisats.</span><span class="sxs-lookup"><span data-stu-id="74b47-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="74b47-125">-   När deras begäran om projektregistrering har godkänts eller avvisats.</span><span class="sxs-lookup"><span data-stu-id="74b47-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="74b47-126">Sekretessmeddelande</span><span class="sxs-lookup"><span data-stu-id="74b47-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="74b47-127">Se även</span><span class="sxs-lookup"><span data-stu-id="74b47-127">See Also</span></span>  
 [<span data-ttu-id="74b47-128">Konfigurera resurser</span><span class="sxs-lookup"><span data-stu-id="74b47-128">Set up resources</span></span>](../psa/set-up-resources.md)
