---
title: Hantera flera kunder på projektbaserade kontraktrader - lite
description: I det här ämnet finns information om hur du hanterar flera kunder i projektbaserade kontraktrader.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f28e7d1363647621f7bd23504aa6d4ea3fc95fc9
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181678"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a><span data-ttu-id="2c2cf-103">Hantera flera kunder på projektbaserade kontraktrader - lite</span><span class="sxs-lookup"><span data-stu-id="2c2cf-103">Manage multiple customers on project-based contract lines - lite</span></span>

<span data-ttu-id="2c2cf-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="2c2cf-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2c2cf-105">Projektbaserade kontraktrader kan innehålla en lista med kunder som är ansvarig för betalning.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-105">Project-based contract lines can include a list of customers that are responsible for payment.</span></span> <span data-ttu-id="2c2cf-106">Den här listan med kunder på den projektbaserade kontraktraden kan vara samma som listan med kunder i kontraktet, men det är inte obligatoriskt.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-106">This list of customers on the project-based contract line can be same as the list of customers on the contract but that isn't required.</span></span> <span data-ttu-id="2c2cf-107">När en projektoffert visas och ett projektkontrakt skapas, kopieras kundlistan på offertraden till motsvarande kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-107">When a project quote is won, and a project contract is created, the customer list on the quote line is copied to the corresponding contract line.</span></span> <span data-ttu-id="2c2cf-108">Kunderna i offerten kopieras till kontraktet.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-108">Customers on the quote are copied to the contract.</span></span>

<span data-ttu-id="2c2cf-109">När projektkontraktet faktureras prioriteras kundlistan i projektbaserade kontrakt med prioritet över kundlistan i kontraktet.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-109">When the project contract is invoiced, the customer list on project-based contract line takes priority over the customer list on the contract.</span></span> <span data-ttu-id="2c2cf-110">Kundlistan i projektkontraktet används endast som standard för nya kontraktrader.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-110">The customer list on the project contract is only used to default new contract lines.</span></span>

<span data-ttu-id="2c2cf-111">Alla kontraktkunder på fliken **Kunder** av projektkontraktets standard som kontraktskunder på nya kontraktsrader som skapats för projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-111">All contract customers on the **Customers** tab of the project contract default as contract line customers on any new contract lines created for the project contract.</span></span> <span data-ttu-id="2c2cf-112">Alla befintliga kontraktrader kommer inte att ärva de nya kontraktkundposterna som skapats efter dem.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-112">Any existing contract lines will not inherit the new contract customer records created after them.</span></span>

## <a name="create-update-or-delete-a-contract-line-customer-record"></a><span data-ttu-id="2c2cf-113">Skapa, uppdatera eller ta bort en kontraktrad kundpost</span><span class="sxs-lookup"><span data-stu-id="2c2cf-113">Create, update, or delete a contract line customer record</span></span>

<span data-ttu-id="2c2cf-114">Du kan skapa, uppdatera eller ta bort en kontraktradkund på fliken Kontraktradens kund och sidan Projektbaserade kontraktrader.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-114">You can create, update, or delete a contract line customer from the Contract Line Customers tab on the Project-based Contract Line page.</span></span> <span data-ttu-id="2c2cf-115">När en ny kund läggs till på den projektbaserade kontraktraden läggs de också till i det allmänna kontraktet som en kontraktkund med en standard delningsprocent på noll procent.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-115">When a new customer is added on the project-based contract line, they are also added on the overall contract as a contract customer with a default billing split percentage of zero percent.</span></span> <span data-ttu-id="2c2cf-116">Delningsprocenten för faktureringen i hela kontraktet kopieras till nya kontraktrader och projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-116">The billing split percentage on the overall contract is copied to new contract lines and to the eventual project contract.</span></span> <span data-ttu-id="2c2cf-117">När du fakturerar ett kontrakt är det emellertid faktureringsdelningsprocenten på den kontraktradnivå som används och inte för faktureringsdelningsprocenten procenten på den övergripande kontraktnivån.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-117">However, when invoicing from the contract, it's the billing split percentage at the contract line level that is used and not the billing split percentage at the overall contract level.</span></span>

<span data-ttu-id="2c2cf-118">Nedan visas fälten på kundposten för **kontrakt** raden för en projektbaserad kontraktrad som du bör tänka på när du arbetar med den:</span><span class="sxs-lookup"><span data-stu-id="2c2cf-118">Below are the fields on the **Contract** line customer record of a project-based contract line to keep in mind as you are working with it:</span></span>

| <span data-ttu-id="2c2cf-119">Fält</span><span class="sxs-lookup"><span data-stu-id="2c2cf-119">Field</span></span> | <span data-ttu-id="2c2cf-120">Plats</span><span class="sxs-lookup"><span data-stu-id="2c2cf-120">Location</span></span> | <span data-ttu-id="2c2cf-121">Beskrivning</span><span class="sxs-lookup"><span data-stu-id="2c2cf-121">Description</span></span> | <span data-ttu-id="2c2cf-122">Inverkan nedströms</span><span class="sxs-lookup"><span data-stu-id="2c2cf-122">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="2c2cf-123">**Konto**</span><span class="sxs-lookup"><span data-stu-id="2c2cf-123">**Account**</span></span> | <span data-ttu-id="2c2cf-124">Redigerbart rutnät på fliken **kontraktradkunder** och på **huvud**- och **snabbregistrering** sformulär för en kontraktradskund.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-124">Editable grid on the **Contract Customers** tab and the **Main** and **Quick Create** forms for a contract customer.</span></span> | <span data-ttu-id="2c2cf-125">Alla aktiva konton.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-125">All active accounts.</span></span> <span data-ttu-id="2c2cf-126">Det här fältet låses efter att posten skapas.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-126">This field is locked after the record is created.</span></span> <span data-ttu-id="2c2cf-127">Om du vill uppdatera fältet tar du bort posten och skapar en ny post.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-127">To update the field, delete the record, and create a new record.</span></span> <span data-ttu-id="2c2cf-128">Om du har registrerat verkliga värden kan du inte ta bort posten.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-128">If you have recorded any actuals, you can't delete the record.</span></span> <span data-ttu-id="2c2cf-129">Men du kan ange en faktureringsdelningsprocenten som noll för det kontot.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-129">However, you can mark the billing split percentage as zero for that account.</span></span> <span data-ttu-id="2c2cf-130">När posten har markerats som noll påverkas alla framtida och faktiska intäkter som hänförs till den här kunden.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-130">When the record is marked as zero, any future cost and revenue actuals that are attributed or split to this customer are impacted.</span></span> | <span data-ttu-id="2c2cf-131">När du plockar ett konto från huvudkontolistan för att lägga till och spara dem läggs kontraktradkunden också till som en kontraktkund.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-131">When you pick an account from the master list of accounts to add and save them, the contract line customer is also added as a contract customer.</span></span> <span data-ttu-id="2c2cf-132">Kontraktradkunder används när fakturor skapas.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-132">Contract line customers are used when invoices are generated.</span></span> |
| <span data-ttu-id="2c2cf-133">**Delningsprocent för fakturering**</span><span class="sxs-lookup"><span data-stu-id="2c2cf-133">**Billing Split Percent**</span></span> | <span data-ttu-id="2c2cf-134">Redigerbart rutnät på fliken **kontraktradkunder** och på **huvud**- och **snabbregistrering** sformulär för en kontraktradskund.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-134">Editable grid on the **Contract Customers** tab and the **Main** and **Quick Create** forms for a contract customer.</span></span> | <span data-ttu-id="2c2cf-135">Detta fält motsvarar procentandelen av varje fakturerad försäljningstransaktion som tilldelats den här kontraktradkunden.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-135">This field represents the percentage of each unbilled sales transaction that will be attributed to this contract line customer.</span></span> | <span data-ttu-id="2c2cf-136">Kontraktradkunder och faktureringsdelningsprocent används när faktiska värden skapas efter godkännande och när fakturan har genererats.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-136">Contract line customers and billing split percentages are used when actuals are created after approval and when the invoice is generated.</span></span> |
| <span data-ttu-id="2c2cf-137">**Undre gräns**</span><span class="sxs-lookup"><span data-stu-id="2c2cf-137">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="2c2cf-138">Redigerbart rutnät på fliken **kontraktradkunder** och på **huvud**- och **snabbregistrering** sformulär för en kontraktradskund.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-138">Editable grid on the **Contract Customers** tab and the **Main** and **Quick Create** forms for a contract customer.</span></span> | <span data-ttu-id="2c2cf-139">Anger om det finns en förhandlad gräns eller ett tak för det totala belopp som ska faktureras kunden för kontaktraden.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-139">Indicates if there is a negotiated limit or cap to the overall amount that will be invoiced to this customer for the contract line.</span></span> | <span data-ttu-id="2c2cf-140">Undre gränsen för kontraktradkunden används när faktiska värden skapas och fakturorna skapas.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-140">The not-to-exceed limit for the contract line customer is used when actuals are created and the invoices are generated.</span></span> |
| <span data-ttu-id="2c2cf-141">**Är Avrundning**</span><span class="sxs-lookup"><span data-stu-id="2c2cf-141">**Is Rounding**</span></span> | <span data-ttu-id="2c2cf-142">Redigerbart rutnät på fliken **kontraktkunder** och på **huvud**- och **snabbregistrerings** formulär för en kontraktradskund.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-142">Editable grid on **Contract Customers** tab and **Main** and **Quick Create** forms for a contract line customer.</span></span> | <span data-ttu-id="2c2cf-143">I det här fältet anges om kunden är en standardavrundning för kunden för den projektbaserade kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-143">This field indicates if this customer is a default rounding customer for this project-based contract line.</span></span> | <span data-ttu-id="2c2cf-144">När du genererar ett faktiskt värde enligt faktureringsdelningsprocenten kan det finnas vissa avrundningsdifferenser.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-144">When you generate an actual according to the billing split percentage, there may be some rounding differences.</span></span> <span data-ttu-id="2c2cf-145">Den här kunden avräknar avrundningsdifferenserna i det här fallet.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-145">This customer is attributed the rounding differences in this case.</span></span> |

## <a name="edit-billing-split-percentages"></a><span data-ttu-id="2c2cf-146">Redigera delningsprocent för fakturering</span><span class="sxs-lookup"><span data-stu-id="2c2cf-146">Edit billing split percentages</span></span>

<span data-ttu-id="2c2cf-147">Faktureringsdelningsprocenten kan redigeras i rutnätet.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-147">Billing split percentages can be edited in the grid.</span></span> <span data-ttu-id="2c2cf-148">När faktureringsdelningsprocenten inte är total till 100 procent får du ett felmeddelande.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-148">When the billing split percentages don't total 100 percent, an error will occur.</span></span> <span data-ttu-id="2c2cf-149">När du har redigerat faktureringsdelningsprocenten uppdaterar du sidan så att felmeddelandet stängs.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-149">After you edit the billing split percentages, refresh the page to remove the error.</span></span>

<span data-ttu-id="2c2cf-150">Du kan också välja **Fördela jämnt** i underrutnätet för kontraktsradkunden.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-150">You can also select **Evenly Distribute** on the contract line customer subgrid.</span></span> <span data-ttu-id="2c2cf-151">Den här åtgärden tilldelar jämn faktureringsdelning till alla kontraktradkunder.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-151">This action evenly allocates billing splits to all contract line customers.</span></span> <span data-ttu-id="2c2cf-152">Om det finns en avrundningsfaktor kommer den att läggas till i den avrundade kunden.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-152">If there is any rounding factor, it will be added to the rounding customer.</span></span> <span data-ttu-id="2c2cf-153">En kontraktradkund märks alltid som den **avrundande** kunden med **avrundning** inställd på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2c2cf-153">One contract line customer is always tagged as the **Rounding** customer with the **Rounding** flag set to **Yes**.</span></span>