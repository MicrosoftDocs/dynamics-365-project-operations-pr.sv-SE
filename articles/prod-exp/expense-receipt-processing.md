---
title: Bearbetning av utgiftskvitto
description: I den här ämne finns information om optisk teckeninläsning (OCR) av kvitton. Den här funktionen är avsedd att förbättra användarupplevelsen när du skapar utgiftsrapporter i Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ed9c97ba9cc505106599c2896dc2112358d0c408
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993528"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="7a565-104">Bearbetning av utgiftskvitto</span><span class="sxs-lookup"><span data-stu-id="7a565-104">Expense receipt processing</span></span>

<span data-ttu-id="7a565-105">Utgiftsposten har förbättrats med introduktionen av optisk teckeninläsning (OCR) för inleveranser.</span><span class="sxs-lookup"><span data-stu-id="7a565-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="7a565-106">Den här funktionen är avsedd att förbättra användarupplevelsen när du skapar utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="7a565-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="7a565-107">Viktiga funktioner</span><span class="sxs-lookup"><span data-stu-id="7a565-107">Key features</span></span>

- <span data-ttu-id="7a565-108">Namn och datum för återförsäljaren och det totala beloppet extraheras från kvitton.</span><span class="sxs-lookup"><span data-stu-id="7a565-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="7a565-109">Den här funktionen försöker att matcha ej bifogade kvitton på ej bifogade utgiftstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="7a565-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="7a565-110">Användare kan skapa manuellt registrerade utgiftstransaktioner från kvitton.</span><span class="sxs-lookup"><span data-stu-id="7a565-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="7a565-111">Användningsexempel</span><span class="sxs-lookup"><span data-stu-id="7a565-111">Usage examples</span></span>

<span data-ttu-id="7a565-112">Om du vill automatiskt bifoga kvitton som inkluderar kreditkortstransaktioner när en utgiftsrapport skapas gör du följande:</span><span class="sxs-lookup"><span data-stu-id="7a565-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="7a565-113">Öppna arbetsytan för **utgiftshantering**.</span><span class="sxs-lookup"><span data-stu-id="7a565-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="7a565-114">På fliken **Kvitton** kontrollerar du att det finns ej bifogade kvitton.</span><span class="sxs-lookup"><span data-stu-id="7a565-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="7a565-115">Du kan även överföra kvitton på fliken **Kvitton**.</span><span class="sxs-lookup"><span data-stu-id="7a565-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="7a565-116">På fliken **Utgifter** kontrollerar du att det finns ej bifogade utgifter.</span><span class="sxs-lookup"><span data-stu-id="7a565-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="7a565-117">Vanligtvis importerar utgiftsadministratören dessa utgifter från kreditkortsutfärdaren.</span><span class="sxs-lookup"><span data-stu-id="7a565-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="7a565-118">Välj **ny utgiftsrapport**.</span><span class="sxs-lookup"><span data-stu-id="7a565-118">Select **New expense report**.</span></span> <span data-ttu-id="7a565-119">Observera att du även kan ta med utgifter och inleveranser när du skapar en utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="7a565-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="7a565-120">Om du lägger till både utgifter och inleveranser utlöses automatisk matchning av inleveranser mot utgifterna.</span><span class="sxs-lookup"><span data-stu-id="7a565-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="7a565-121">Följ stegen nedan om du vill skapa en utgift eller matcha en utgift från ett kvitto:</span><span class="sxs-lookup"><span data-stu-id="7a565-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="7a565-122">På en utgiftsrapport, på fliken **Kvitton** bifogar du ett kvitto genom att välja **Lägg till kvitton**.</span><span class="sxs-lookup"><span data-stu-id="7a565-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="7a565-123">Under kvittots uppladdade bild ser du alternativen **Skapa** och **Matcha**.</span><span class="sxs-lookup"><span data-stu-id="7a565-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="7a565-124">Välj **Skapa** om du vill skapa en manuellt registrerad utgiftstransaktion och fyll i värdena som ska extraheras från kvittot.</span><span class="sxs-lookup"><span data-stu-id="7a565-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="7a565-125">Om du väljer **Matcha** görs ett försök att matcha en befintlig utgift mot kvittot.</span><span class="sxs-lookup"><span data-stu-id="7a565-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="7a565-126">Installation</span><span class="sxs-lookup"><span data-stu-id="7a565-126">Installation</span></span>

<span data-ttu-id="7a565-127">Den här funktionen fungerar tillsammans med funktionen **Ny typ av utgiftsrapporter** som hjälper dig att förenkla utgiftsupplevelsen.</span><span class="sxs-lookup"><span data-stu-id="7a565-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="7a565-128">Den här funktionen är endast tillgänglig för nivå 2+-miljöer, som är Sandbox och produktion.</span><span class="sxs-lookup"><span data-stu-id="7a565-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="7a565-129">Om du vill använda de här avancerade utgiftsfunktionerna installerar du tillägget utgiftshanteringstjänst för Microsoft Dynamics 365 Finance och aktiverar funktionerna i din instans.</span><span class="sxs-lookup"><span data-stu-id="7a565-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="7a565-130">Du kan komma åt tillägget från projektet i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="7a565-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="7a565-131">Logga in på LCS och öppna den önskade miljön.</span><span class="sxs-lookup"><span data-stu-id="7a565-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="7a565-132">Gå till **Alla detaljer**.</span><span class="sxs-lookup"><span data-stu-id="7a565-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="7a565-133">Välj **Bibehåll** eller bläddra ned till snabbfliken **Miljötillägg**.</span><span class="sxs-lookup"><span data-stu-id="7a565-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="7a565-134">Välj **Installera ett nytt tillägg**.</span><span class="sxs-lookup"><span data-stu-id="7a565-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="7a565-135">Välj **utgiftshanteringstjänst**.</span><span class="sxs-lookup"><span data-stu-id="7a565-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="7a565-136">Följ anvisningarna i installationsguiden och godkänn villkoren.</span><span class="sxs-lookup"><span data-stu-id="7a565-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="7a565-137">Välj **Installera**.</span><span class="sxs-lookup"><span data-stu-id="7a565-137">Select **Install**.</span></span>

<span data-ttu-id="7a565-138">Arbetsytan **Funktionshantering** aktiverar du följande funktioner:</span><span class="sxs-lookup"><span data-stu-id="7a565-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="7a565-139">Ny typ av utgiftsrapporter</span><span class="sxs-lookup"><span data-stu-id="7a565-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="7a565-140">Matcha automatiskt och skapa utgift från kvitto</span><span class="sxs-lookup"><span data-stu-id="7a565-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="7a565-141">När du aktiverar de här funktionerna utförs följande åtgärder:</span><span class="sxs-lookup"><span data-stu-id="7a565-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="7a565-142">Den befintliga arbetsytan **utgiftshantering** ersätts med den nya arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="7a565-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="7a565-143">Ett nytt menyobjekt för synlighet för utgiftsfält läggs till.</span><span class="sxs-lookup"><span data-stu-id="7a565-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="7a565-144">Du kan fortfarande öppna sidan tidigare sidan **Utgiftsrapporter** genom att gå till **Utgiftshantering > Mina utgifter > Utgiftsrapporter**.</span><span class="sxs-lookup"><span data-stu-id="7a565-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="7a565-145">Arbetsflöden och eventuella godkännanden går fortfarande till sidan befintliga utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="7a565-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="7a565-146">Kvitton bearbetas med hjälp av Microsoft Azure Cognitive Services och metadata extraheras och läggs till.</span><span class="sxs-lookup"><span data-stu-id="7a565-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="7a565-147">Ett alternativ läggs till som gör att du kan skapa en utgiftsrapport som innehåller ej bifogade kvitton.</span><span class="sxs-lookup"><span data-stu-id="7a565-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="7a565-148">Ett alternativ som läggs till i utgiftsrapporter innebär att du kan skapa en utgiftsrad från en inleverans eller att matcha en befintlig inleverans till en befintlig utgiftsrad.</span><span class="sxs-lookup"><span data-stu-id="7a565-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="7a565-149">Mer information om funktionen Ny typ av utgiftsrapporter finns i [Ny typ av utgiftsrapporter](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="7a565-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="7a565-150">Vanliga frågor och svar</span><span class="sxs-lookup"><span data-stu-id="7a565-150">Frequently asked questions</span></span>

<span data-ttu-id="7a565-151">**Används mina data för modellerna i Microsoft?**</span><span class="sxs-lookup"><span data-stu-id="7a565-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="7a565-152">Nej, Microsoft har byggt en allmän maskininlärningsmodell för mottagande bearbetningstjänst.</span><span class="sxs-lookup"><span data-stu-id="7a565-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="7a565-153">Den här modellen bygger inte på de kvitton som du har överfört.</span><span class="sxs-lookup"><span data-stu-id="7a565-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="7a565-154">**Var är den här funktionen tillgänglig och bearbetad?**</span><span class="sxs-lookup"><span data-stu-id="7a565-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="7a565-155">USA stöds för närvarande.</span><span class="sxs-lookup"><span data-stu-id="7a565-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="7a565-156">**Var hamnar mina kvitton?**</span><span class="sxs-lookup"><span data-stu-id="7a565-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="7a565-157">Finans ska kontakta Cognitive Services för att extrahera fältdata.</span><span class="sxs-lookup"><span data-stu-id="7a565-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="7a565-158">Cognitive Services behåller en kopia av ditt kvitto i upp till 24 timmar under bearbetningen.</span><span class="sxs-lookup"><span data-stu-id="7a565-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="7a565-159">När bearbetningen har slutförts tas kvittot bort av Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="7a565-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="7a565-160">Kvitton lagras fortfarande i Finance.</span><span class="sxs-lookup"><span data-stu-id="7a565-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="7a565-161">Mer information finns i [Aktivera kvittoförståelse med formigenkänningens nya förmåga](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="7a565-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]