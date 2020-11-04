---
title: Konfigurera inställningar för ytterligare parametrar
description: Konfigurera ytterligare parameterinställningar i Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 24a4fe83471da916fb91cfe20e739279c08d8e5e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085540"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="d0810-103">Konfigurera ytterligare parameterinställningar (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d0810-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d0810-104">När du har konfigurerat artiklarna i föregående avsnitt, måste du ange ytterligare projektparametrar som ska användas till dina projekt.</span><span class="sxs-lookup"><span data-stu-id="d0810-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="d0810-105">När du först installerade [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] så skapade du en parameterinställning för att först skapa alla poster som krävs för [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] att fungera.</span><span class="sxs-lookup"><span data-stu-id="d0810-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="d0810-106">Nu är det dags att gå tillbaka och konfigurera ytterligare fält för de här inställningarna.</span><span class="sxs-lookup"><span data-stu-id="d0810-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="d0810-107">Du måste ha konfigurerat följande inställningar:</span><span class="sxs-lookup"><span data-stu-id="d0810-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="d0810-108">Organisationsenhet</span><span class="sxs-lookup"><span data-stu-id="d0810-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="d0810-109">Faktureringsfrekvens</span><span class="sxs-lookup"><span data-stu-id="d0810-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="d0810-110">Arbetstidsmall</span><span class="sxs-lookup"><span data-stu-id="d0810-110">Work hours template</span></span>  
  
-   <span data-ttu-id="d0810-111">Prislista</span><span class="sxs-lookup"><span data-stu-id="d0810-111">Price list</span></span>  
 
<span data-ttu-id="d0810-112">I det här steget ska du också ange vilken typ av resursallokering som du vill använda:</span><span class="sxs-lookup"><span data-stu-id="d0810-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="d0810-113">**Central**.</span><span class="sxs-lookup"><span data-stu-id="d0810-113">**Central**.</span></span> <span data-ttu-id="d0810-114">Bara resursansvariga kan fördela resurser till projekt.</span><span class="sxs-lookup"><span data-stu-id="d0810-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="d0810-115">**Hybrid**.</span><span class="sxs-lookup"><span data-stu-id="d0810-115">**Hybrid**.</span></span> <span data-ttu-id="d0810-116">Resursansvariga, projektledare och kontoansvariga kan fördela resurser till projekt.</span><span class="sxs-lookup"><span data-stu-id="d0810-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="d0810-117">Om du vill konfigurera projektparametrar:</span><span class="sxs-lookup"><span data-stu-id="d0810-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="d0810-118">Gå till **Project Service > Parametrar**.</span><span class="sxs-lookup"><span data-stu-id="d0810-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="d0810-119">Klicka på den parameterinställning som du vill konfigurera (den som du skapade när du först installerade [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), eller klicka på **Ny** för att skapa en ny.</span><span class="sxs-lookup"><span data-stu-id="d0810-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="d0810-120">I området **Allmänt** anger du alla alternativ för dina projektparametrar.</span><span class="sxs-lookup"><span data-stu-id="d0810-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="d0810-121">I området **Prislista** , klicka på **+** om du vill lägga till en prislista, väljer en prislista i listrutan **Prislista för projektparameter** och klickar sedan på **Spara**.</span><span class="sxs-lookup"><span data-stu-id="d0810-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="d0810-122">Klicka på knappen **Spara** längst ned till höger på skärmen.</span><span class="sxs-lookup"><span data-stu-id="d0810-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="d0810-123">Projektparameterposten måste finnas kvar för att Project Service ska fungera korrekt.</span><span class="sxs-lookup"><span data-stu-id="d0810-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="d0810-124">Den här posten bör inte tas bort.</span><span class="sxs-lookup"><span data-stu-id="d0810-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="d0810-125">Se även</span><span class="sxs-lookup"><span data-stu-id="d0810-125">See Also</span></span>  
 [<span data-ttu-id="d0810-126">Konfigurera resurser</span><span class="sxs-lookup"><span data-stu-id="d0810-126">Set up resources</span></span>](../psa/set-up-resources.md)
