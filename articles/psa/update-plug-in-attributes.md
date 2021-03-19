---
title: Uppdatera plugin-attribut för att inkludera nya prissättningsdimensioner
description: I den här ämnet finns information om hur du uppdaterar plugin-attribut för prissättningsdimensioner.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 958646c9e06a15e265bc0caa8b0f3eb9f79fc347
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281815"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="ce3e6-103">Uppdatera plugin-attribut för att inkludera nya prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="ce3e6-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="ce3e6-104">Om du inte använder funktionerna för offert och kontrakt i Project Service Automation (PSA) kan du hoppa över det här ämnet.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="ce3e6-105">I den här ämnet förutsätts att du har slutfört procedurerna i avsnittet [Skapa anpassade fält och entiteter](create-custom-fields-entities.md), [Lägg till anpassade fält till prisinställningar och transaktionsenheter](field-references.md) och [Ställ in anpassade fält som prissättningsdimensioner](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="ce3e6-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="ce3e6-106">Om du inte har slutfört de här procedurerna går du tillbaka och slutför dem och går sedan tillbaka till ämne.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="ce3e6-107">När en offertraddetalj skapas på sidan **Offertrad** för en projektoffert rad skapas två uppskattningsrader i bakgrunden, en rad för kostnadssidan för uppskattningen och en för försäljningssidan.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="ce3e6-108">Det här är samma för projektkontraktrader.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="ce3e6-109">När du gör en ändring av kvantiteten eller ett fält på kostnadssidan, sprids den ändringen till försäljningssidan.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="ce3e6-110">Detta kan bero på att följande plugin-program måste registreras om efter en ändring i prissättningsdimensionerna.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="ce3e6-111">PreOperationContractLineDetailUpdate - uppdateringar **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="ce3e6-112">PreOperationQuoteLineDetailUpdate - uppdateringar **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="ce3e6-113">Nedan förklaras hur du registrerar plugin-programmen.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="ce3e6-114">Öppna **PluginRegistrationTool** och anslut till din online-instans.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="ce3e6-115">Klicka på **Sök** och sök efter det plugin-program som du vill uppdatera.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Skärmbild av sökträdet](media/PRT-1.png)

3. <span data-ttu-id="ce3e6-117">När du har hittat plugin-programmet markerar du det och klickar på **Välj på huvudformulär**.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="ce3e6-118">Markera steget för det plugin-program som ska uppdateras, högerklicka och välj sedan **uppdatera**.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Skärmbild av det plugin-program som ska uppdateras](media/PRT-2.png)
 
5. <span data-ttu-id="ce3e6-120">I uppdateringsfönstret, klicka på ellipsen (**...**) i filtreringsattributen.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Skärmbild av Uppdatera befintlig stegkonfigurationsinformation](media/PRT-3.png)
 
6. <span data-ttu-id="ce3e6-122">Markera kryssrutorna för prissättningsattribut.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-122">Select the pricing attribute check boxes.</span></span>

 ![Skärmbild som visar markeringen i kryssrutan för prissättningsattribut](media/PRT-4.png)

7. <span data-ttu-id="ce3e6-124">Klicka på **OK** för att stänga sidan och välj sedan **Updatera steg**.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Skärmbild som visar knappen "Uppdatera steg"](media/PRT-5.png)
 
8. <span data-ttu-id="ce3e6-126">Upprepa den här processen för det andra plugin-programmet **PreOperationQuoteLineDetail - uppdatera msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="ce3e6-127">Stäng registrering av plugin-program.</span><span class="sxs-lookup"><span data-stu-id="ce3e6-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]