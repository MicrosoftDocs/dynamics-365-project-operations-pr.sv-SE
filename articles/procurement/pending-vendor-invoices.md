---
title: Inköp av icke-lagerbaserade material med väntande leverantörsfaktura
description: I ämnet beskrivs hur du registrerar väntande leverantörsfakturor.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993837"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="9d3aa-103">Inköp av icke-lagerbaserade material med väntande leverantörsfaktura</span><span class="sxs-lookup"><span data-stu-id="9d3aa-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="9d3aa-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="9d3aa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9d3aa-105">När ett företag köper in icke-lagerbaserade material till ett projekt, kan kostnaderna registreras direkt på projektet.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="9d3aa-106">Exempelvis utför Contoso Robotics US ett projekt för utrustningsförnyelse och behöver programvarulicenser.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="9d3aa-107">Licenserna köps in från en tredjepartsleverantör.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="9d3aa-108">Med Dynamics 365 Finance registrerar den ansvariga för leverantörsreskontra ett väntande leverantörsfakturadokument och registrerar licenskostnaderna direkt på utrustningsförnyelseprojektet.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="9d3aa-109">Innan du använder funktionerna som beskrivs i ämnet måste du granska och tillämpa de konfigurationer som krävs.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="9d3aa-110">Mer information finns i [Aktivera icke-lagerbaserade material och väntande leverantörsfakturor](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="9d3aa-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="9d3aa-111">Registrera en projektrelaterad väntande leverantörsfaktura</span><span class="sxs-lookup"><span data-stu-id="9d3aa-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="9d3aa-112">Väntande leverantörsfakturor kan registreras på sidan **Väntande leverantörsfakturor** (**Leverantörsreskontra** > **Fakturor** > **Väntande leverantörsfakturor**).</span><span class="sxs-lookup"><span data-stu-id="9d3aa-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="9d3aa-113">Slutför följande steg för att registrera en projektrelaterad väntande leverantörsfaktura:</span><span class="sxs-lookup"><span data-stu-id="9d3aa-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="9d3aa-114">Gå till **Leverantörsreskontra** > **Fakturor** och välj **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="9d3aa-115">I fältet **Fakturakonto** väljer du leverantör och i fältet **Nummer** fyller du i identifiering för leverantörsfakturan.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="9d3aa-116">Lägg till en rad i leverantörsfakturan och i fältet **Artikelnummer** väljer du den icke-lagerbaserade artikeln som köpts in från leverantören.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="9d3aa-117">Det går inte att registrera leverantörsfakturarader som är baserade på en inköpskategori på projektet.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="9d3aa-118">Lägg till kvantiteten som köpts in.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-118">Add the quantity purchased.</span></span> <span data-ttu-id="9d3aa-119">Systemet fyller i enhetspriset baserat på priskonfiguration för den icke-lagerbaserade artikeln.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="9d3aa-120">Kontrollera totalbeloppet och annan obligatorisk information på raden.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="9d3aa-121">På fliken **Projekt**, i radinformationen, väljer du projekt-ID som denna artikel ska registreras på.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="9d3aa-122">Alternativt kan du välja aktivitetsnumret och uppdatera projektkategorin och radegenskapen.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="9d3aa-123">Efter väntande leverantörsfaktura.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-123">Post pending vendor invoice.</span></span> <span data-ttu-id="9d3aa-124">När fakturan har registrerats bokför systemet:</span><span class="sxs-lookup"><span data-stu-id="9d3aa-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="9d3aa-125">Leverantörens saldobelopp.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="9d3aa-126">Momsbeloppet.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-126">The sales tax amount.</span></span>
    - <span data-ttu-id="9d3aa-127">Kostnaden på projektet registreras på inköpsintegrationskontot.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="9d3aa-128">Den faktiska projekttransaktionen i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="9d3aa-129">Transaktionen bearbetas vidare med [Project Operations-integrationsjournal](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="9d3aa-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="9d3aa-130">Om du registrerar journalen flyttas beloppet från inköpsintegrationskontot till projektkostnadskontot.</span><span class="sxs-lookup"><span data-stu-id="9d3aa-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
