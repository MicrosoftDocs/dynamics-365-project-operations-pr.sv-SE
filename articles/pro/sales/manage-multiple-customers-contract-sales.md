---
title: Hantera flera kunder i projektkontrakt - lite
description: I det här ämnet finns information om hur du hanterar flera kunder i projektkontrakt.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b248dabdbd5239b140da7c99d3f38609facfe75e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181339"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a><span data-ttu-id="907c6-103">Hantera flera kunder i projektkontrakt - lite</span><span class="sxs-lookup"><span data-stu-id="907c6-103">Manage multiple customers on project contracts - lite</span></span>

<span data-ttu-id="907c6-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="907c6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="907c6-105">Projektkontrakt i Dynamics 365 Project Operations har stöd för scenariot där ett avtal om flera kunder ingår i ett avtal.</span><span class="sxs-lookup"><span data-stu-id="907c6-105">Project contracts in Dynamics 365 Project Operations support the scenario where a contractual agreement involves multiple customers who are funding a deal.</span></span> <span data-ttu-id="907c6-106">På fliken **Sammanfattning** på sidan **Projektkontrakt** inkluderar fältet **Kund**.</span><span class="sxs-lookup"><span data-stu-id="907c6-106">The **Summary** tab on the **Project Contract** page includes the **Customer** field.</span></span> <span data-ttu-id="907c6-107">I det här fältet identifieras den primära kunden för affären.</span><span class="sxs-lookup"><span data-stu-id="907c6-107">This field identifies the primary customer of the deal.</span></span> <span data-ttu-id="907c6-108">Andra kunder för affären kan ställas in på fliken **kunder** på sidan **projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="907c6-108">Other customers for the deal can be set up on the **Customers** tab of the **Project Contract** page.</span></span>

<span data-ttu-id="907c6-109">Alla kontraktkunder som är förtecknade i projekkontrakt som standard som kontraktsrad kunder på alla nya projektbaserade kontraktrader som skapas för projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="907c6-109">All contract customers listed on the project contract default as contract line customers on any new project-based contract lines that are created for the project contract.</span></span> <span data-ttu-id="907c6-110">Befintliga projektbaserade kontraktrader ärver inte nya kontraktkunder som nya poster.</span><span class="sxs-lookup"><span data-stu-id="907c6-110">Existing project-based contract lines don't inherit new contract customers as new records are created.</span></span>

<span data-ttu-id="907c6-111">Produktbaserade kontraktrader kopplas automatiskt till den primära kunden.</span><span class="sxs-lookup"><span data-stu-id="907c6-111">Product-based contract lines are automatically associated to the primary customer.</span></span>

<span data-ttu-id="907c6-112">Kontraktskunder och kontraktradkunder kan läggas till, uppdateras eller tas bort när som helst innan kontraktet vanns.</span><span class="sxs-lookup"><span data-stu-id="907c6-112">Contract customers and contract line customers can be added, updated, or deleted at any time before the contract is won.</span></span>

## <a name="primary-customer"></a><span data-ttu-id="907c6-113">Primär kund</span><span class="sxs-lookup"><span data-stu-id="907c6-113">Primary customer</span></span>

<span data-ttu-id="907c6-114">Kunden som listas på fliken **Sammanfattning** i projektavtalet eftersom den potentiella kunden är den primära kunden för kontraktet.</span><span class="sxs-lookup"><span data-stu-id="907c6-114">The customer listed on the **Summary** tab of the project contract as the potential customer is the primary customer of the contract.</span></span> <span data-ttu-id="907c6-115">När du försöker ta bort den primära kunden från kundlistan i kontraktet visas ett felmeddelande om att det inte går att ta bort en primär kundpost i ett kontrakt.</span><span class="sxs-lookup"><span data-stu-id="907c6-115">When you try to delete the primary customer from the customer list on the contract, you will receive an error message that a primary customer record on a contract can't be deleted.</span></span>

<span data-ttu-id="907c6-116">Den primära kunden kan inte uppdateras från listan kontraktkunder.</span><span class="sxs-lookup"><span data-stu-id="907c6-116">The primary customer can't be updated from the contract customers list.</span></span> <span data-ttu-id="907c6-117">Ändra i stället den potentiella kunden på fliken **Sammanfattning** i kontraktet.</span><span class="sxs-lookup"><span data-stu-id="907c6-117">Instead, change the potential customer on the **Summary** tab of the contract.</span></span> <span data-ttu-id="907c6-118">När det här fältet uppdateras på sidan **kontraktsammanfattning** läggs den till som en ny kontraktkund med den **primära** flagguppsättningen.</span><span class="sxs-lookup"><span data-stu-id="907c6-118">When this field is updated on the **Contract Summary** page, the new customer is added as a new contract customer with the **Primary** flag set.</span></span> <span data-ttu-id="907c6-119">Den föregående primära kunden blir fortfarande kund i kontraktet.</span><span class="sxs-lookup"><span data-stu-id="907c6-119">The previous primary customer will still be a customer on the contract.</span></span>

## <a name="create-update-or-delete-a-contract-customer-record"></a><span data-ttu-id="907c6-120">Skapa, uppdatera eller ta bort en kontrakt kundpost</span><span class="sxs-lookup"><span data-stu-id="907c6-120">Create, update, or delete a contract customer record</span></span>

<span data-ttu-id="907c6-121">En kontraktkund kan skapas, uppdateras eller tas bort från fliken **kunder** på sidan **projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="907c6-121">A contract customer can be created, updated, or deleted from the **Customers** tab on the **Project Contract** page.</span></span> <span data-ttu-id="907c6-122">Fälten i följande tabell visas i kontraktkundposten för ett projektkontrakt och du bör tänka på när du arbetar med kontraktet.</span><span class="sxs-lookup"><span data-stu-id="907c6-122">The fields in the following table are on the contract customer record of a project contract and should be kept in mind as you are working with the contract.</span></span>

| <span data-ttu-id="907c6-123">Fält</span><span class="sxs-lookup"><span data-stu-id="907c6-123">Field</span></span> | <span data-ttu-id="907c6-124">Plats</span><span class="sxs-lookup"><span data-stu-id="907c6-124">Location</span></span> | <span data-ttu-id="907c6-125">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="907c6-125">Description</span></span> | <span data-ttu-id="907c6-126">Inverkan nedströms</span><span class="sxs-lookup"><span data-stu-id="907c6-126">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="907c6-127">**Konto**</span><span class="sxs-lookup"><span data-stu-id="907c6-127">**Account**</span></span> | <span data-ttu-id="907c6-128">Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund.</span><span class="sxs-lookup"><span data-stu-id="907c6-128">The grid can be edited on the **Contract Customers** tab and the **Main** and **Quick Create** forms for a contract customer.</span></span> | <span data-ttu-id="907c6-129">Lista alla aktiva konton.</span><span class="sxs-lookup"><span data-stu-id="907c6-129">Lists all the active accounts.</span></span> <span data-ttu-id="907c6-130">Det här fältet låses efter att posten skapas.</span><span class="sxs-lookup"><span data-stu-id="907c6-130">This field is locked after the record is created.</span></span> <span data-ttu-id="907c6-131">Om du vill uppdatera kontot tar du bort posten och skapar den på nytt.</span><span class="sxs-lookup"><span data-stu-id="907c6-131">To update the account, delete the record and re-create it.</span></span> <span data-ttu-id="907c6-132">Om du har registrerat verkliga värden, eller om kontraktets kundpost är en primär kund, kan du inte ta bort posten.</span><span class="sxs-lookup"><span data-stu-id="907c6-132">If you have recorded any actuals, or if the contract customer record is a primary customer, you can't delete the record.</span></span> | <span data-ttu-id="907c6-133">Kontraktskunder kopieras över som kontraktradkunder när en kontraktrad skapas.</span><span class="sxs-lookup"><span data-stu-id="907c6-133">Contract customers are copied over as contract line customers when a contract line is created.</span></span> |
| <span data-ttu-id="907c6-134">**Delningsprocent för fakturering**</span><span class="sxs-lookup"><span data-stu-id="907c6-134">**Billing Split Percent**</span></span> | <span data-ttu-id="907c6-135">Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund.</span><span class="sxs-lookup"><span data-stu-id="907c6-135">The grid can be edited on the **Contract Customers** tab and the **Main** and **Quick Create** forms for a contract customer.</span></span> | <span data-ttu-id="907c6-136">Motsvarar procentandelen av varje fakturerad försäljningstransaktion som tilldelats den här kontraktkunden.</span><span class="sxs-lookup"><span data-stu-id="907c6-136">Represents the percentage of each unbilled sales transaction that is attributed to this contract customer.</span></span> | <span data-ttu-id="907c6-137">Kopieras till nya kontraktrader och till projektets kontraktsradkunder på nya projekt kontraktrader.</span><span class="sxs-lookup"><span data-stu-id="907c6-137">Copied over to new contract lines and to project contract line customers on new project contract lines.</span></span> |
| <span data-ttu-id="907c6-138">**Namn på kontakten som ska faktureras**</span><span class="sxs-lookup"><span data-stu-id="907c6-138">**Bill to Contact Name**</span></span> | <span data-ttu-id="907c6-139">Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund.</span><span class="sxs-lookup"><span data-stu-id="907c6-139">The grid can be edited on the **Contract Customers** tab and the **Main** and **Quick Create** forms for a contract customer.</span></span> | <span data-ttu-id="907c6-140">Det här textfältet ska användas för att identifiera kundens kontaktperson för fakturering.</span><span class="sxs-lookup"><span data-stu-id="907c6-140">This text field should be used to identify the invoice contact person for this customer.</span></span> <span data-ttu-id="907c6-141">Det här fältet används som standard från den relaterade kontoposten.</span><span class="sxs-lookup"><span data-stu-id="907c6-141">This field defaults from the related account record.</span></span> | <span data-ttu-id="907c6-142">Kopieras till fältet **Fakturera till kontraktnamn** på fakturan som genereras för kunden.</span><span class="sxs-lookup"><span data-stu-id="907c6-142">Copied over to the **Bill to Contract Name** field on the invoice that is generated for this customer.</span></span> |
| <span data-ttu-id="907c6-143">**Fakturera till namn**</span><span class="sxs-lookup"><span data-stu-id="907c6-143">**Bill To Name**</span></span> | <span data-ttu-id="907c6-144">Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund</span><span class="sxs-lookup"><span data-stu-id="907c6-144">The grid can be edited on the **Contract Customers** tab and the **Main** and **Quick Create** forms for a contract customer</span></span> | <span data-ttu-id="907c6-145">Det här textfältet ska användas för att identifiera kundens kontaktperson för fakturering.</span><span class="sxs-lookup"><span data-stu-id="907c6-145">This text field should be used to identify the invoice contact person for this customer.</span></span> <span data-ttu-id="907c6-146">Det här fältet används som standard från den relaterade kontoposten.</span><span class="sxs-lookup"><span data-stu-id="907c6-146">This field defaults from the related account record.</span></span> | <span data-ttu-id="907c6-147">Kopieras till fältet **Fakturera till kontraktnamn** på fakturan som genereras för kunden.</span><span class="sxs-lookup"><span data-stu-id="907c6-147">Copied over to the **Bill to Contract Name** field on the invoice that is generated for this customer.</span></span> |
| <span data-ttu-id="907c6-148">**Betalningsvillkor**</span><span class="sxs-lookup"><span data-stu-id="907c6-148">**Payment Terms**</span></span> | <span data-ttu-id="907c6-149">Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund.</span><span class="sxs-lookup"><span data-stu-id="907c6-149">The grid can be edited on the **Contract Customers** tab and the **Main** and **Quick Create** forms for a contract customer.</span></span> | <span data-ttu-id="907c6-150">Standardvärdet från den relaterade kontoposten.</span><span class="sxs-lookup"><span data-stu-id="907c6-150">The values default from the related account record.</span></span> | <span data-ttu-id="907c6-151">Kopieras till fältet **Fakturera till kontraktnamn** på fakturan som genereras för kunden.</span><span class="sxs-lookup"><span data-stu-id="907c6-151">Copied over to the **Bill to Contract Name** field on the invoice that is generated for this customer.</span></span> |
| <span data-ttu-id="907c6-152">**Är Avrundning**</span><span class="sxs-lookup"><span data-stu-id="907c6-152">**Is Rounding**</span></span> | <span data-ttu-id="907c6-153">Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund.</span><span class="sxs-lookup"><span data-stu-id="907c6-153">The grid can be edited on the **Contract Customers** tab and the **Main** and **Quick Create** forms for a contract customer.</span></span> | <span data-ttu-id="907c6-154">Anger om kunden är en avrundningskund för den här affären.</span><span class="sxs-lookup"><span data-stu-id="907c6-154">Indicates if this customer is a default rounding customer for this deal.</span></span> <span data-ttu-id="907c6-155">Det kan bara finnas en avrundning av kunden i ett projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="907c6-155">There can only be one rounding customer on a project contract.</span></span> | <span data-ttu-id="907c6-156">När kostnads- och ofakturerade försäljningsdelningar i kvantitet leder till en avrundningsskillnad används den differensen på den faktiska som har mappats till kunden.</span><span class="sxs-lookup"><span data-stu-id="907c6-156">When cost and unbilled sales splits on quantity lead to a rounding difference, that difference is applied to the actual that maps to this customer.</span></span> |
| <span data-ttu-id="907c6-157">**Undre gräns**</span><span class="sxs-lookup"><span data-stu-id="907c6-157">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="907c6-158">Rutnätet kan redigeras på fliken **kontraktkunder** och formuläret **huvud** och **snabbregistrering** för en kontraktkund</span><span class="sxs-lookup"><span data-stu-id="907c6-158">The grid can be edited on the **Contract Customers** tab and the **Main** and **Quick Create** forms for a contract customer</span></span> | <span data-ttu-id="907c6-159">Anger om det finns en förhandlad gräns eller ett tak för det totala belopp som ska faktureras kunden för det här åtagandet.</span><span class="sxs-lookup"><span data-stu-id="907c6-159">Indicates if there is a negotiated limit or cap to the overall amount that will be invoiced to the customer for this engagement.</span></span> | <span data-ttu-id="907c6-160">Gränsen **Undre gräns** upprättas på kontraktsnivå kommer att utvärderas den **Faktiska värden för ofakturerad försäljning** som refererar till den här kontraktkunden.</span><span class="sxs-lookup"><span data-stu-id="907c6-160">The **Not-to-Exceed Limit** set up at the contract customer level will be evaluated on **Unbilled Sales Actuals** that reference this contract customer.</span></span> |

## <a name="edit-billing-split-percentages"></a><span data-ttu-id="907c6-161">Redigera delningsprocent för fakturering</span><span class="sxs-lookup"><span data-stu-id="907c6-161">Edit billing split percentages</span></span>

<span data-ttu-id="907c6-162">Du kan redigera delningsprocent satser med hjälp av redigeringsfunktionen i rutnätet.</span><span class="sxs-lookup"><span data-stu-id="907c6-162">Billing split percentages can be edited using the in-line grid edit experience.</span></span> <span data-ttu-id="907c6-163">När faktureringsdelningsprocenten inte är total till 100 procent får du ett felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="907c6-163">When the billing split percentages do not total to 100 percent, you will receive an error.</span></span> <span data-ttu-id="907c6-164">När du har redigerat faktureringsdelningsprocenten uppdaterar du sidan så att felmeddelandet stängs.</span><span class="sxs-lookup"><span data-stu-id="907c6-164">After you edit the billing split percentages, refresh the page to dismiss the error.</span></span>

<span data-ttu-id="907c6-165">Du kan också välja **jämnt fördelat** i underrutnätet **kontraktkund** för att fördela faktureringsdelning jämnt för alla kontraktskunder.</span><span class="sxs-lookup"><span data-stu-id="907c6-165">You can also select **Evenly Distribute** on the **Contract Customers** subgrid to allocate billing splits evenly to all contract customers.</span></span> <span data-ttu-id="907c6-166">Om det finns en avrundningsfaktor kommer den att läggas till i den avrundade kunden.</span><span class="sxs-lookup"><span data-stu-id="907c6-166">If there is a rounding factor, it will be added to the rounding customer.</span></span> <span data-ttu-id="907c6-167">En av kontraktskunderna är alltid märkt som **avrundning**, vilket innebär att kontraktets kundpost har avrundningsflaggan satt till **Ja**.</span><span class="sxs-lookup"><span data-stu-id="907c6-167">One of the contract customers is always tagged as the **rounding** customer, which means that the contract customer record has the rounding flag set to **Yes**.</span></span> <span data-ttu-id="907c6-168">Detta är vanligtvis den primära kunden för kontraktet, men det kan också ändras.</span><span class="sxs-lookup"><span data-stu-id="907c6-168">Typically, this is the primary customer of the contract, but it can be changed as well.</span></span>