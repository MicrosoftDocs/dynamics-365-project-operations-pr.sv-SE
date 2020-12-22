---
title: Uppdatera attribut för plugin-program med nya prissättningsdimensioner
description: I den här ämnet finns information om hur du uppdaterar plugin-attribut för prissättningsdimensioner.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643240"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="bc635-103">Uppdatera attribut för plugin-program med nya prissättningsdimensioner</span><span class="sxs-lookup"><span data-stu-id="bc635-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="bc635-104">I den här ämnet finns information om hur du uppdaterar plugin-attribut för prissättningsdimensioner.</span><span class="sxs-lookup"><span data-stu-id="bc635-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="bc635-105">Detta ämne är endast tillämpligt på offert- och kontraktsfunktionerna i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="bc635-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bc635-106">Förutsättningar</span><span class="sxs-lookup"><span data-stu-id="bc635-106">Prerequisites</span></span>
<span data-ttu-id="bc635-107">Innan du slutför stegen i detta ämne måste du ha slutfört procedurerna i följande avsnitt:</span><span class="sxs-lookup"><span data-stu-id="bc635-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="bc635-108">Skapa anpassade fält och entiteter</span><span class="sxs-lookup"><span data-stu-id="bc635-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="bc635-109">Lägga till anpassade fält i prisinställningar och transaktionella entiteter</span><span class="sxs-lookup"><span data-stu-id="bc635-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="bc635-110">[Konfigurera anpassade fält som prissättningsdimensioner](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="bc635-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="bc635-111">Om du inte har slutfört dessa procedurer går du tillbaka och slutför dem och går sedan tillbaka till detta ämne.</span><span class="sxs-lookup"><span data-stu-id="bc635-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="bc635-112">Registrera ett plugin-program</span><span class="sxs-lookup"><span data-stu-id="bc635-112">Register a plug-in</span></span>
<span data-ttu-id="bc635-113">När en offertradsdetalj skapas på sidan **Offertrad** för en projektoffertrad skapar systemet två uppskattningsrader.</span><span class="sxs-lookup"><span data-stu-id="bc635-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="bc635-114">En rad är för kostnadssidan av uppskattningen och den andra raden är för försäljningsidan.</span><span class="sxs-lookup"><span data-stu-id="bc635-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="bc635-115">Det här är samma för projektkontraktrader.</span><span class="sxs-lookup"><span data-stu-id="bc635-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="bc635-116">När du gör en ändring av kvantiteten eller ett fält på kostnadssidan görs samma ändring också på försäljningssidan.</span><span class="sxs-lookup"><span data-stu-id="bc635-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="bc635-117">Detta är möjligt eftersom plugin-program för PreOperation på Quotelinedetail och kontraktline-detaljentiteter kopplar specifika attribut på kostnadssidan till transaktionens försäljningssida.</span><span class="sxs-lookup"><span data-stu-id="bc635-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="bc635-118">Om ändringar som utförts på prissättningens dimensionsvärden på försäljningssidan också måste utföras på kostnadssidan, måste följande plugin-program registreras på nytt efter att du har gjort ändringar i en prissättningsdimension.</span><span class="sxs-lookup"><span data-stu-id="bc635-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="bc635-119">Dessa är de plugin-program som ska uppdateras och registreras om:</span><span class="sxs-lookup"><span data-stu-id="bc635-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="bc635-120">PreOperationContractLineDetailUpdate - **Uppdatera msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="bc635-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="bc635-121">PreOperationQuoteLineDetailUpdate - **Uppdaterar msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="bc635-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="bc635-122">Slutför följande steg för att uppdatera och registrera om plugin-programen.</span><span class="sxs-lookup"><span data-stu-id="bc635-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="bc635-123">Öppna **PluginRegistrationTool** och anslut till din Project Operations Dataverse-miljö.</span><span class="sxs-lookup"><span data-stu-id="bc635-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="bc635-124">Välj **Sök** och skriv in de första bokstäverna i plugin-programmet som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="bc635-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="bc635-125">När du har hittat plugin-programmet markerar du det och klickar sedan på **Välj på huvudformulär**.</span><span class="sxs-lookup"><span data-stu-id="bc635-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="bc635-126">Markera steget **Uppdatera msdyn_orderlinetransaction**, högerklicka och välj sedan **Uppdatera**.</span><span class="sxs-lookup"><span data-stu-id="bc635-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="bc635-127">I dialogfönstret **Uppdatera** väljer du ellipsen (**...**) bland filtreringsattributen.</span><span class="sxs-lookup"><span data-stu-id="bc635-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="bc635-128">Fönstret för filtreringsattribut öppnas och visar en lista över alla attribut i entiteten samt prissättningsdimensionerna.</span><span class="sxs-lookup"><span data-stu-id="bc635-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="bc635-129">Markera kryssrutorna för attributen för prissättningsdimensionen.</span><span class="sxs-lookup"><span data-stu-id="bc635-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="bc635-130">Välj **OK** för att stänga sidan, och välj sedan **Uppdatera steg**.</span><span class="sxs-lookup"><span data-stu-id="bc635-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="bc635-131">Upprepa steg 2-7 för det andra plugin-programmet, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="bc635-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="bc635-132">För detta plugin-program måste du uppdatera steget **Uppdatera msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="bc635-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="bc635-133">Stäng **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="bc635-133">Close **PluginRegistrationTool**.</span></span>