---
title: Varför återställs priset till standardvärdet noll för tidskostnadstillgångar?
description: Felsökning kring varför ett pris återställs till standardvärdet 0 för tidsutgiftstillgångar.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 124719410f89dea506d43a1b64cb91c85d4f3968
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131407"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="53ffd-103">Varför återställs priset till standardvärdet noll för tidskostnadstillgångar?</span><span class="sxs-lookup"><span data-stu-id="53ffd-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="53ffd-104">Dessa Vanliga frågor och svar gäller tillgångar där transaktionsklassen anges som Tid och transaktionstypen som Kostnad.</span><span class="sxs-lookup"><span data-stu-id="53ffd-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="53ffd-105">Följande tre kontroller hjälper dig att felsöka anledningen till att priset anges som standardvärdet 0 för tidskostnadstillgångar.</span><span class="sxs-lookup"><span data-stu-id="53ffd-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="53ffd-106">Kontrol 1: Hitta självkostnadsprislistan för projektet</span><span class="sxs-lookup"><span data-stu-id="53ffd-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="53ffd-107">Hitta projekt via projektfältet för tillgången och gå sedan till projektsidan.</span><span class="sxs-lookup"><span data-stu-id="53ffd-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="53ffd-108">Klicka på kontraktenhetslänken i fältet.</span><span class="sxs-lookup"><span data-stu-id="53ffd-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="53ffd-109">Kontrollera om den upphandlande enheten har en prislista i rutnätet för självkostnadslistor den upphandlade enhetens sida.</span><span class="sxs-lookup"><span data-stu-id="53ffd-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="53ffd-110">Om det finns mer än en prislista har du hittat problemet.</span><span class="sxs-lookup"><span data-stu-id="53ffd-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="53ffd-111">Project Service har endast stöd för en prislista per organisationsenhet.</span><span class="sxs-lookup"><span data-stu-id="53ffd-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="53ffd-112">Ta bort alla prislistor från denna entitet tills endast en enda prislista finns kopplad i rutnätet för självkostnadslistor för organisationsenheten.</span><span class="sxs-lookup"><span data-stu-id="53ffd-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="53ffd-113">Om inga prislistor har kopplats till organisationsenheten, anteckna då valutan för organisationsenheten.</span><span class="sxs-lookup"><span data-stu-id="53ffd-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="53ffd-114">Gå till Project Service och därefter till Parametrar och öppna fliken Prislistor. Kontrollera om det finns några prislistor med kontext angiven som Kostnad samt valuta som matchar valutan i organisationsenheten.</span><span class="sxs-lookup"><span data-stu-id="53ffd-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="53ffd-115">Om det inte finns några prislistor som matchar dessa villkor har du hittat problemet.</span><span class="sxs-lookup"><span data-stu-id="53ffd-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="53ffd-116">Se till att du har minst en prislista vars sammanhang anges som Kostnad och vars valuta matchar valutan för organisationsenheten.</span><span class="sxs-lookup"><span data-stu-id="53ffd-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="53ffd-117">Om det finns mer än en prislista som matchar detta villkor, fortsätt då att läsa igenom detta dokument om du vill göra fler kontroller.</span><span class="sxs-lookup"><span data-stu-id="53ffd-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="53ffd-118">Kontroll 2: Är någon av de prislistor som anges ovan giltig för det aktuella datumet för tidskostnadstillgången?</span><span class="sxs-lookup"><span data-stu-id="53ffd-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="53ffd-119">För att Project Service ska beakta en prislista för standardprissättning bör den prislistan vara tillämpbar för datumet för tidskostnadstillgången.</span><span class="sxs-lookup"><span data-stu-id="53ffd-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="53ffd-120">Kontrollera följande för att se om ovanstående prislista/prislistor är tillämpbar(a):</span><span class="sxs-lookup"><span data-stu-id="53ffd-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="53ffd-121">Kontrollera att start- och slutdatum på fliken Allmänt för bifogade prislistor inte är tomma.</span><span class="sxs-lookup"><span data-stu-id="53ffd-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="53ffd-122">Om start- och slutdatum i ovanstående prislistor är tomma har du hittat problemet.</span><span class="sxs-lookup"><span data-stu-id="53ffd-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="53ffd-123">Anteckna fältet Startdatum för din tidskostnadstillgång och kontrollera om någon av de prislistor som identifierats gäller för detta datum.</span><span class="sxs-lookup"><span data-stu-id="53ffd-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="53ffd-124">Till exempel bör datumet för tidskostnadstillgången hamna inom ramarna för start- och slutdatum i prislistan.</span><span class="sxs-lookup"><span data-stu-id="53ffd-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="53ffd-125">Om det inte finns någon prislista som omfattar detta datum för tidskostnadstillgången har du hittat problemet.</span><span class="sxs-lookup"><span data-stu-id="53ffd-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="53ffd-126">Ändra prislistans start- och slutdatum så att prislistan omfattar datumet för tidskostnadstillgången.</span><span class="sxs-lookup"><span data-stu-id="53ffd-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="53ffd-127">Om det finns mer än en prislista som täcker datumet för tidskostnadstillgången har du hittat problemet.</span><span class="sxs-lookup"><span data-stu-id="53ffd-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="53ffd-128">Du kan åtgärda detta genom att redigera start- och slutdatum för prislistorna så att det finns bara en enda prislista som omfattar datumet för tidskostnadstillgången.</span><span class="sxs-lookup"><span data-stu-id="53ffd-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="53ffd-129">Om det finns bara en prislista som omfattar detta datum för tidskostnadstillgången, gå då vidare till nästa kontroll i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="53ffd-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="53ffd-130">När du har utfört nödvändiga korrigeringar, skapa då på nytt en tidspost, godkänn denna och kontrollera att tidskostnadstillgången anger ett giltigt pris.</span><span class="sxs-lookup"><span data-stu-id="53ffd-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="53ffd-131">Kontroll 3: Finns det ett pris i prislistan för prissättning på tidskostnadstillgången?</span><span class="sxs-lookup"><span data-stu-id="53ffd-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="53ffd-132">Om du har slutfört kontrollerna 1 och 2 bör du nu ha en enda prislista som gäller datumet för tidskostnadstillgången.</span><span class="sxs-lookup"><span data-stu-id="53ffd-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="53ffd-133">Öppna denna prislista och gå till fliken Rollpriser. Kontrollera att det finns en rad i rutnätet för prissättningen för tidskostnadstillgången.</span><span class="sxs-lookup"><span data-stu-id="53ffd-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="53ffd-134">Om det inte finns någon rad i rutnätet för rollpriser för prissättning för tidskostnadstillgången har du hittat problemet.</span><span class="sxs-lookup"><span data-stu-id="53ffd-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="53ffd-135">Skapa en rad i rutnätet Rollpriser för prissättning i tidskostnadstillgången.</span><span class="sxs-lookup"><span data-stu-id="53ffd-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="53ffd-136">När detta är gjort, skapa då på nytt en tidspost, godkänn denna och kontrollera att tidskostnadstillgången anger ett giltigt pris.</span><span class="sxs-lookup"><span data-stu-id="53ffd-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="53ffd-137">Om du fortfarande inte ser något giltigt pris på din tidskostnadstillgång efter att ha utfört de tre kontrollerna ovan, vänligen skapa då ett supportärende.</span><span class="sxs-lookup"><span data-stu-id="53ffd-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



