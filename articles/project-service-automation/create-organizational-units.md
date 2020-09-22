---
title: Skapa organisationsenheter
description: Skapa organisationsenheter i Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f27cfd9d-1265-40e6-b19e-5d02c3d91ca6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2712c8a22d97148b5481be3cb5cced1746ea08e8
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756153"
---
# <a name="create-organizational-units-project-service"></a><span data-ttu-id="8c476-103">Skapa organisationsenheter (Project Service)</span><span class="sxs-lookup"><span data-stu-id="8c476-103">Create organizational units (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="8c476-104">Ditt företag ordnar förmodligen sin konsultverksamheten efter geografi, funktionen eller andra områden.</span><span class="sxs-lookup"><span data-stu-id="8c476-104">Your company probably organizes its consulting business by geography, function, or other areas.</span></span> <span data-ttu-id="8c476-105">Du kan skapa organisationsenheter som speglar din konsultverksamhet.</span><span class="sxs-lookup"><span data-stu-id="8c476-105">You can create organizational units that reflect your consulting business.</span></span> <span data-ttu-id="8c476-106">En [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-organisationsenhet är en grupp eller en avdelning inom ett professionellt tjänsteföretag som använder sig av fakturerbara resurser med utgiftstaxor som särskiljer sig från andra sådana grupper eller avdelningar i företaget.</span><span class="sxs-lookup"><span data-stu-id="8c476-106">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is a group or division in a professional services company that employs billable resources with cost rates that are distinct from other such groups or divisions in the company.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8c476-107">En [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-organisationsenhet skiljer sig från en affärsenhet i [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="8c476-107">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is separate from a business unit in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="8c476-108">Affärsenheterna är mer av en säkerhetstruktur som påverkar åtkomstnivåer för [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)]-information och är vanligtvis organiserade runt företagsdivisioner som moderbolag och dotterbolag eller divisioner.</span><span class="sxs-lookup"><span data-stu-id="8c476-108">Business units are more of a security structure that affects levels of access to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] information, and are usually organized around company divisions, like parent company and subsidiaries or divisions.</span></span> <span data-ttu-id="8c476-109">Organisationsenheter representerar hur konsultföretaget kategoriserar sina olika verksamheter, antingen efter geografisk plats (som EMEA eller LATAM), efter funktion (t ex produktutveckling eller IT-outsourcing) eller andra parametrar.</span><span class="sxs-lookup"><span data-stu-id="8c476-109">Organizational units represent how your consulting company categorizes its different businesses, whether by geographic location (like EMEA or LATAM), by function (like Product Development or IT Outsourcing), or by other parameters.</span></span>  
  
1.  <span data-ttu-id="8c476-110">Gå till **Project Service > Organisationsenheter**.</span><span class="sxs-lookup"><span data-stu-id="8c476-110">Go to **Project Service > Organizational Units**.</span></span>  
  
2.  <span data-ttu-id="8c476-111">Klicka på **Nytt**.</span><span class="sxs-lookup"><span data-stu-id="8c476-111">Click **New**.</span></span>  
  
3.  <span data-ttu-id="8c476-112">I området **Allmänt** anger du ett namn för organisationsenheten i fältet **Namn**, och fyller sedan i övriga fält som behövs.</span><span class="sxs-lookup"><span data-stu-id="8c476-112">In the **General** area, enter a name for the organization unit in **Name**, and fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="8c476-113">Klicka på **Spara** för att skapa posten så att du kan fortsätta redigera den.</span><span class="sxs-lookup"><span data-stu-id="8c476-113">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="8c476-114">Under **Prislista för självkostnad**, klickar du på **+** för att lägga till en prislista.</span><span class="sxs-lookup"><span data-stu-id="8c476-114">Under **Cost Price Lists**, click **+** to add a price list.</span></span> <span data-ttu-id="8c476-115">Du kan endast lägga till prislistor med kontexten **Kostnad** här.</span><span class="sxs-lookup"><span data-stu-id="8c476-115">You can only add price lists with the **Cost** context here.</span></span>  
  
6.  <span data-ttu-id="8c476-116">I fältet **namn** klickar du på knappen **Sök** och väljer en prislista som du vill göra tillgänglig för den här organisationsenheten.</span><span class="sxs-lookup"><span data-stu-id="8c476-116">In the **Name** field, click the **Search** button and select a price list you want to make available to this organizational unit.</span></span> <span data-ttu-id="8c476-117">Fortsätt lägga till prislistor som behövs.</span><span class="sxs-lookup"><span data-stu-id="8c476-117">Continue adding price lists as needed.</span></span>  
  
7.  <span data-ttu-id="8c476-118">Klicka på **Spara** i skärmens nedre högra hörn när du är klar.</span><span class="sxs-lookup"><span data-stu-id="8c476-118">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="8c476-119">Se även</span><span class="sxs-lookup"><span data-stu-id="8c476-119">See Also</span></span>  
 [<span data-ttu-id="8c476-120">Konfigurera Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8c476-120">Configure Project Service Automation</span></span>](../project-service/configure.md)
