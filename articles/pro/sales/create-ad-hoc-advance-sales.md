---
title: Skapa ett ad hoc-förskott i ett kontrakt
description: I det här ämnet finns information om hur du skapar ett förskott på ett kontrakt efter behov.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f0a6391a3bf6dd39d21504a6f286e4ff1954183
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273619"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a><span data-ttu-id="935e0-103">Skapa ett ad hoc-förskott i ett kontrakt</span><span class="sxs-lookup"><span data-stu-id="935e0-103">Creating an ad hoc advance on a contract</span></span>

<span data-ttu-id="935e0-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="935e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="935e0-105">Microsoft Dynamics 365 Project Operations har stöd för faktureringsscenarier som omfattar förskottsbetalningar och förskott.</span><span class="sxs-lookup"><span data-stu-id="935e0-105">Microsoft Dynamics 365 Project Operations supports invoicing scenarios that involve pre-payments and advances.</span></span> <span data-ttu-id="935e0-106">Processen för att använda **förskott** i **Project Operations** liknar kontrakt som **Kvarhållare**.</span><span class="sxs-lookup"><span data-stu-id="935e0-106">The process for using **Advances** in **Project Operations** is similar to **Retainer** contracts.</span></span> 

<span data-ttu-id="935e0-107">Följ stegen nedan om du vill fakturera kunden för ett förskott.</span><span class="sxs-lookup"><span data-stu-id="935e0-107">Complete the following steps to invoice the customer for an advance.</span></span>

1. <span data-ttu-id="935e0-108">Gå till sidan **Projektkontrakt** och välj fliken **Förskott och kvarhållare**.</span><span class="sxs-lookup"><span data-stu-id="935e0-108">Go to the **Project Contract** page, and then select the **Advances and Retainers** tab.</span></span>
2. <span data-ttu-id="935e0-109">Välj i undernätet som visar alla tidigare registrerade förskott och förskottsbetalningar **+ Ny projektkontraktkvarhållare**.</span><span class="sxs-lookup"><span data-stu-id="935e0-109">In the subgrid that lists all the previously recorded advances and prepayments, select **+ New Project contract retainer**.</span></span> 

    <span data-ttu-id="935e0-110">Formuläret **snabbregistrering** öppnas för att registrera en förskottsbetalning eller förskott.</span><span class="sxs-lookup"><span data-stu-id="935e0-110">The **Quick Create** form opens for recording a prepayment or advance.</span></span>
    
3. <span data-ttu-id="935e0-111">I tabellen nedan visas fälten för att registrera ett förskott och de överväganden du behöver tänka på när du skapar nya:</span><span class="sxs-lookup"><span data-stu-id="935e0-111">The table below lists the fields for recording an advance and the considerations to keep in mind as you create new ones:</span></span>

    | <span data-ttu-id="935e0-112">Fält</span><span class="sxs-lookup"><span data-stu-id="935e0-112">Field</span></span> | <span data-ttu-id="935e0-113">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="935e0-113">Description</span></span> | <span data-ttu-id="935e0-114">Inverkan nedströms</span><span class="sxs-lookup"><span data-stu-id="935e0-114">Downstream impact</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="935e0-115">**Projektkontraktskund**</span><span class="sxs-lookup"><span data-stu-id="935e0-115">**Project Contract Customer**</span></span> | <span data-ttu-id="935e0-116">I det här fältet anges vilken kund i kontraktet som ska faktureras för förskott.</span><span class="sxs-lookup"><span data-stu-id="935e0-116">This field indicates which customer on the contract will be invoiced for this advance.</span></span> | <span data-ttu-id="935e0-117">Om du har flera kunder i kontraktet och vill fakturera dem för en viss kvarhållande eller förskott skapar du ett förskott för varje kund för sig.</span><span class="sxs-lookup"><span data-stu-id="935e0-117">If you have multiple customers on the contract and want to invoice each of them for a specific retainer or advance amount, create an advance for each customer individually.</span></span> |
    | <span data-ttu-id="935e0-118">**Beskrivning**</span><span class="sxs-lookup"><span data-stu-id="935e0-118">**Description**</span></span> | <span data-ttu-id="935e0-119">Beskrivning av syftet med och tidpunkten för förskottet för att identifiera förskottet.</span><span class="sxs-lookup"><span data-stu-id="935e0-119">The description of the purpose or timing of the advance to help identify this advance.</span></span> | <span data-ttu-id="935e0-120">Beskrivningen visas på fakturaraden för förskottet.</span><span class="sxs-lookup"><span data-stu-id="935e0-120">This description is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="935e0-121">**Belopp**</span><span class="sxs-lookup"><span data-stu-id="935e0-121">**Amount**</span></span> | <span data-ttu-id="935e0-122">Beloppet för förskottsbetalningen eller förskott.</span><span class="sxs-lookup"><span data-stu-id="935e0-122">The amount for the pre-payment or advance.</span></span> | <span data-ttu-id="935e0-123">Beloppet visas på fakturaraden för förskottet.</span><span class="sxs-lookup"><span data-stu-id="935e0-123">This amount is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="935e0-124">**Fakturadatum**</span><span class="sxs-lookup"><span data-stu-id="935e0-124">**Invoice Date**</span></span> | <span data-ttu-id="935e0-125">Datumet då förskottet faktureras till kunden.</span><span class="sxs-lookup"><span data-stu-id="935e0-125">The date on which this advance is invoiced to the customer.</span></span> | <span data-ttu-id="935e0-126">Det här är datumet då den automatiska fakturan skapades för att skapa en fakturarad för förhandsproceduren.</span><span class="sxs-lookup"><span data-stu-id="935e0-126">This is the date for the automated invoice creation process to create an invoice line for this advance.</span></span> |
    | <span data-ttu-id="935e0-127">**Fakturastatus**</span><span class="sxs-lookup"><span data-stu-id="935e0-127">**Invoice Status**</span></span> | <span data-ttu-id="935e0-128">Det här är en alternativ inställning som anger om detta förskott läggs till i en utkastfaktura för den här kunden.</span><span class="sxs-lookup"><span data-stu-id="935e0-128">This is an option setting that indicates whether this advance is added to a draft invoice for this customer.</span></span> <span data-ttu-id="935e0-129">Möjliga värden är:</span><span class="sxs-lookup"><span data-stu-id="935e0-129">The possible values are:</span></span></br><span data-ttu-id="935e0-130">- **Inte klar att fakturera**</span><span class="sxs-lookup"><span data-stu-id="935e0-130">- **Not ready to invoice**</span></span></br><span data-ttu-id="935e0-131">- **Klar att fakturera**</span><span class="sxs-lookup"><span data-stu-id="935e0-131">- **Ready to invoice**</span></span> | <span data-ttu-id="935e0-132">När ett förskott eller en förskottsbetalningen markeras som **klar för fakturering**, läggs det till som en radtid i utkastfakturan.</span><span class="sxs-lookup"><span data-stu-id="935e0-132">When an advance or pre-payment is marked as **Ready to invoice**, it is added as a line time on a draft invoice.</span></span> <span data-ttu-id="935e0-133">Endast ett helt fakturerat förskott kan användas för att stämma av mot projektkostnader för nästa fakturaperiod.</span><span class="sxs-lookup"><span data-stu-id="935e0-133">Only a fully invoiced advance can be used to reconcile against project costs for the next invoice period.</span></span> |

4. <span data-ttu-id="935e0-134">Välj **Spara och stäng** i dialogrutan snabbregistrering för att registrera förskottet eller förskottsbetalningen.</span><span class="sxs-lookup"><span data-stu-id="935e0-134">Select **Save and close** on the quick create dialog to record the advance or the pre-payment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]