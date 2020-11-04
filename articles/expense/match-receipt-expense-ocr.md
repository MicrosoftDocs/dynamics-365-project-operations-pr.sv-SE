---
title: Matcha kvitto mot utgift med OCR
description: I den här ämne finns information om optisk teckeninläsning (OCR) av kvitton.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 62d6316c9602089518a94267d8ef2b7fb8d59cd0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085505"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="8dc9d-103">Matcha kvitto mot utgift med OCR</span><span class="sxs-lookup"><span data-stu-id="8dc9d-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="8dc9d-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="8dc9d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8dc9d-105">Utgiftsposten har förbättrats med introduktionen av optisk teckeninläsning (OCR) för inleveranser.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="8dc9d-106">Den här funktionen är avsedd att förbättra användarupplevelsen när du skapar utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="8dc9d-107">Viktiga funktioner</span><span class="sxs-lookup"><span data-stu-id="8dc9d-107">Key features</span></span>

- <span data-ttu-id="8dc9d-108">I systemet extraheras namn och datum för handlaren och det totala beloppet från kvitton.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="8dc9d-109">Systemet försöker att inte använda ej bifogade kvitton på icke-anslutna utgiftstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="8dc9d-110">Du kan skapa manuellt registrerade utgiftstransaktioner från kvitton.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="8dc9d-111">Bifoga kvitton till en utgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="8dc9d-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="8dc9d-112">Om du vill automatiskt bifoga kvitton som inkluderar kreditkortstransaktioner när en utgiftsrapport skapas utför du följande steg.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="8dc9d-113">Öppna arbetsytan för **utgiftshantering**.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="8dc9d-114">På fliken **Kvitton** kontrollerar du att det finns ej bifogade kvitton.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="8dc9d-115">Du kan även överföra kvitton på fliken **Kvitton**.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="8dc9d-116">På fliken **Utgifter** kontrollerar du att det finns ej bifogade utgifter.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="8dc9d-117">Vanligtvis importerar utgiftsadministratören dessa utgifter från kreditkortsutfärdaren.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="8dc9d-118">Välj **ny utgiftsrapport**.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-118">Select **New expense report**.</span></span> <span data-ttu-id="8dc9d-119">Observera att du även kan ta med utgifter och inleveranser när du skapar en utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="8dc9d-120">Om du lägger till både utgifter och inleveranser utlöses automatisk matchning av inleveranser mot utgifterna.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="8dc9d-121">Skapa eller matcha kvitton till en utgiftsrapport</span><span class="sxs-lookup"><span data-stu-id="8dc9d-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="8dc9d-122">Följ stegen nedan om du vill skapa en utgift eller matcha en kostnad från ett kvitto.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="8dc9d-123">På en utgiftsrapport, på fliken **Kvitton** bifogar du ett kvitto genom att välja **Lägg till kvitton**.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="8dc9d-124">Under kvittots uppladdade bild ser du alternativen **Skapa** och **Matcha**.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="8dc9d-125">Välj **Skapa** om du vill skapa en manuellt registrerad utgiftstransaktion och fyll i värdena som ska extraheras från kvittot.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="8dc9d-126">Om du väljer **Matcha** görs ett försök att matcha en befintlig utgift mot kvittot.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-126">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="8dc9d-127">Installation</span><span class="sxs-lookup"><span data-stu-id="8dc9d-127">Installation</span></span>

<span data-ttu-id="8dc9d-128">Om du vill använda de här avancerade utgiftsfunktionerna installerar du tillägget utgiftshanteringstjänst för Microsoft Dynamics 365 Finance och aktiverar funktionerna i din instans.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="8dc9d-129">Du kan komma åt tillägget från projektet i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8dc9d-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="8dc9d-130">Logga in på LCS och öppna den önskade miljön.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="8dc9d-131">Gå till **Alla detaljer**.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="8dc9d-132">Välj **Bibehåll** eller bläddra ned till snabbfliken **Miljötillägg**.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-132">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="8dc9d-133">Välj **Installera ett nytt tillägg**.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="8dc9d-134">Välj **utgiftshanteringstjänst**.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="8dc9d-135">Följ anvisningarna i installationsguiden och godkänn villkoren.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="8dc9d-136">Välj **Installera**.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-136">Select **Install**.</span></span>

<span data-ttu-id="8dc9d-137">Arbetsytan **Funktionshantering** aktiverar du följande funktioner:</span><span class="sxs-lookup"><span data-stu-id="8dc9d-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="8dc9d-138">Ny typ av utgiftsrapporter</span><span class="sxs-lookup"><span data-stu-id="8dc9d-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="8dc9d-139">Matcha automatiskt och skapa utgift från kvitto</span><span class="sxs-lookup"><span data-stu-id="8dc9d-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="8dc9d-140">När du aktiverar de här funktionerna utförs följande åtgärder:</span><span class="sxs-lookup"><span data-stu-id="8dc9d-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="8dc9d-141">Den befintliga arbetsytan **utgiftshantering** ersätts med den nya arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="8dc9d-142">Ett nytt menyobjekt för synlighet för utgiftsfält läggs till.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="8dc9d-143">Du kan fortfarande öppna sidan tidigare sidan **Utgiftsrapporter** genom att gå till **Utgiftshantering > Mina utgifter > Utgiftsrapporter**.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="8dc9d-144">Arbetsflöden och eventuella godkännanden går fortfarande till sidan befintliga utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="8dc9d-145">Kvitton bearbetas med hjälp av Microsoft Azure Cognitive Services och metadata extraheras och läggs till.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="8dc9d-146">Ett alternativ läggs till som gör att du kan skapa en utgiftsrapport som innehåller ej bifogade kvitton.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="8dc9d-147">Ett alternativ som läggs till i utgiftsrapporter innebär att du kan skapa en utgiftsrad från en inleverans eller att matcha en befintlig inleverans till en befintlig utgiftsrad.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="8dc9d-148">Vanliga frågor och svar</span><span class="sxs-lookup"><span data-stu-id="8dc9d-148">Frequently asked questions</span></span>

<span data-ttu-id="8dc9d-149">**Används mina data för modellerna i Microsoft?**</span><span class="sxs-lookup"><span data-stu-id="8dc9d-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="8dc9d-150">Nej, Microsoft har byggt en allmän maskininlärningsmodell för mottagande bearbetningstjänst.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="8dc9d-151">Den här modellen bygger inte på de kvitton som du har överfört.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="8dc9d-152">**Var är den här funktionen tillgänglig och bearbetad?**</span><span class="sxs-lookup"><span data-stu-id="8dc9d-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="8dc9d-153">USA stöds för närvarande.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="8dc9d-154">**Var hamnar mina kvitton?**</span><span class="sxs-lookup"><span data-stu-id="8dc9d-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="8dc9d-155">Finans ska kontakta Cognitive Services för att extrahera fältdata.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="8dc9d-156">Cognitive Services behåller en kopia av ditt kvitto i upp till 24 timmar under bearbetningen.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="8dc9d-157">När bearbetningen har slutförts tas kvittot bort av Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="8dc9d-158">Kvitton lagras fortfarande i Finance.</span><span class="sxs-lookup"><span data-stu-id="8dc9d-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="8dc9d-159">Mer information finns i [Aktivera kvittoförståelse med formigenkänningens nya förmåga](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="8dc9d-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
