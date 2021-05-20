---
title: Inköp av icke-lagerbaserade material med väntande leverantörsfaktura
description: I ämnet beskrivs hur du registrerar väntande leverantörsfakturor.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880690"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="2a1d3-103">Inköp av icke-lagerbaserade material med väntande leverantörsfaktura</span><span class="sxs-lookup"><span data-stu-id="2a1d3-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="2a1d3-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="2a1d3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2a1d3-105">När ett företag köper in icke-lagerbaserade material till ett projekt, kan kostnaderna registreras direkt på projektet.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="2a1d3-106">Exempelvis utför Contoso Robotics US ett projekt för utrustningsförnyelse och behöver programvarulicenser.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="2a1d3-107">Licenserna köps in från en tredjepartsleverantör.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="2a1d3-108">Med Dynamics 365 Finance registrerar den ansvariga för leverantörsreskontra ett väntande leverantörsfakturadokument och registrerar licenskostnaderna direkt på utrustningsförnyelseprojektet.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="2a1d3-109">Innan du använder funktionerna som beskrivs i ämnet måste du granska och tillämpa de konfigurationer som krävs.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="2a1d3-110">Mer information finns i [Aktivera icke-lagerbaserade material och väntande leverantörsfakturor](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="2a1d3-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="2a1d3-111">Registrera en projektrelaterad väntande leverantörsfaktura</span><span class="sxs-lookup"><span data-stu-id="2a1d3-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="2a1d3-112">Väntande leverantörsfakturor kan registreras på sidan **Väntande leverantörsfakturor** (**Leverantörsreskontra** > **Fakturor** > **Väntande leverantörsfakturor**).</span><span class="sxs-lookup"><span data-stu-id="2a1d3-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="2a1d3-113">Slutför följande steg för att registrera en projektrelaterad väntande leverantörsfaktura:</span><span class="sxs-lookup"><span data-stu-id="2a1d3-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="2a1d3-114">Gå till **Leverantörsreskontra** > **Fakturor** och välj **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="2a1d3-115">I fältet **Fakturakonto** väljer du leverantör och i fältet **Nummer** fyller du i identifiering för leverantörsfakturan.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="2a1d3-116">Lägg till en rad i leverantörsfakturan och i fältet **Artikelnummer** väljer du den icke-lagerbaserade artikeln som köpts in från leverantören.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="2a1d3-117">Det går inte att registrera leverantörsfakturarader som är baserade på en inköpskategori på projektet.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="2a1d3-118">Lägg till kvantiteten som köpts in.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-118">Add the quantity purchased.</span></span> <span data-ttu-id="2a1d3-119">Systemet fyller i enhetspriset baserat på priskonfiguration för den icke-lagerbaserade artikeln.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="2a1d3-120">Kontrollera totalbeloppet och annan obligatorisk information på raden.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="2a1d3-121">På fliken **Projekt**, i radinformationen, väljer du projekt-ID som denna artikel ska registreras på.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="2a1d3-122">Alternativt kan du välja aktivitetsnumret och uppdatera projektkategorin och radegenskapen.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="2a1d3-123">Efter väntande leverantörsfaktura.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-123">Post pending vendor invoice.</span></span> <span data-ttu-id="2a1d3-124">När fakturan har registrerats bokför systemet:</span><span class="sxs-lookup"><span data-stu-id="2a1d3-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="2a1d3-125">Leverantörens saldobelopp.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="2a1d3-126">Momsbeloppet.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-126">The sales tax amount.</span></span>
    - <span data-ttu-id="2a1d3-127">Kostnaden på projektet registreras på inköpsintegrationskontot.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="2a1d3-128">Den faktiska projekttransaktionen i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="2a1d3-129">Transaktionen bearbetas vidare med [Project Operations-integrationsjournal](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="2a1d3-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="2a1d3-130">Om du registrerar journalen flyttas beloppet från inköpsintegrationskontot till projektkostnadskontot.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
