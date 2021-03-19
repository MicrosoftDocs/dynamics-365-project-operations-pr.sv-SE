---
title: Lös självkostnader för beräkningar och utfall – Lite
description: I det här ämnet finns information om hur du löser självkostnader för uppskattningar och faktiska värden.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bbb79fdc5c68d67530b5aa34fe6105211eff1768
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274571"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a><span data-ttu-id="dfc9a-103">Lös självkostnader för beräkningar och utfall – Lite</span><span class="sxs-lookup"><span data-stu-id="dfc9a-103">Resolve cost prices on estimates and actuals - lite</span></span>

<span data-ttu-id="dfc9a-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="dfc9a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dfc9a-105">Om du vill lösa självkostnader och prislistan för självkostnad för uppskattningar och faktiska värden använder systemet informationen i fälten **Datum**, **Valuta** och **Kontrakterande enhet** i det relaterade projektet.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date**, **Currency**, and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="dfc9a-106">När prislistan för självkostnad har lösts löser programmet kostnadstaxan.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="dfc9a-107">Lösa kostnadstaxor på faktiska och uppskattade rader för tid</span><span class="sxs-lookup"><span data-stu-id="dfc9a-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="dfc9a-108">Uppskattningsrader för tid refererar till offert- och kontraktradsinformation för tids- och resurstilldelningar i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="dfc9a-109">När en kostnadsprislista har lösts matchas fälten **Roll** och **Resursenhet** på uppskattningsraden för Tid mot rollprisraderna i prislistan.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-109">After a cost price list is resolved, the **Role** and **Resourcing Unit** fields on the estimate line for Time are matched against the role price lines in the price list.</span></span> <span data-ttu-id="dfc9a-110">Denna matchning förutsätter att du använder standardprissättningsdimensionerna för arbetskostnad.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-110">This match assumes that you're using the standard pricing dimensions for labor cost.</span></span> <span data-ttu-id="dfc9a-111">Om du konfigurerade systemet för att matcha fält i stället för, eller utöver, **Roll** och **Resursenhet** används en annan kombination för att hämta en matchande rollprisrad.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-111">If you configured the system to match fields instead of, or in addition to **Role** and **Resourcing Unit**, then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="dfc9a-112">Om programmet hittar en rollprisrad som har en kostnadstaxa för kombinationen av **Roll** och **Resursenhet**, är detta standardkostnaden.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-112">If the application finds a role price line that has a cost rate for the **Role** and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="dfc9a-113">Om programmet inte kan matcha värdena **Roll** och **Resursenhet** hämtar det rollprisrader med en matchande roll, men null-värden för **Resursenheten**.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-113">If the application can't match the **Role** and **Resourcing Unit** values, then it retrieves role price lines with a matching role, but null values of the **Resourcing Unit**.</span></span> <span data-ttu-id="dfc9a-114">När den har en matchande rollprispost hämtas kostnadstaxan som standard från den posten.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-114">After it has a matching role price record, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="dfc9a-115">Om du konfigurerar en annan prioritering av **Roll** och **Resursenhet**, eller om du har andra dimensioner med högre prioritet, ändras det här beteendet i enlighet med detta.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-115">If you configure a different prioritization of **Role** and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="dfc9a-116">Systemet hämtar rollprisposter med värden som matchar alla dimensionsvärden för prissättning i prioritetsordning med rader som har null-värden för de dimensionerna sist.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="dfc9a-117">Lösa kostnadstaxor på faktiska och uppskattade rader för utgift</span><span class="sxs-lookup"><span data-stu-id="dfc9a-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="dfc9a-118">Uppskattningsrader för utgift refererar till offert- och kontraktradsinformation för rader för utgift och utgiftsuppskattning i ett projekt.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="dfc9a-119">När en självkostnadslista har lösts använder systemet en kombination av fälten **Kategori** och **Enhet** på utgiftsuppskattningsraden för att matcha mot raderna **Kategoripris** i den lösta prislistan.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the expense estimate line to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="dfc9a-120">Om systemet hittar en kategoriprisrad som har en kostnadstaxa för kombinationen av fälten **Kategori** och **Enhet** används kostnadstaxan som standard.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="dfc9a-121">Om systemet inte kan matcha värdena **Kategori** och **Enhet**, eller om det går att hitta en matchande kategoriprisrad, men prismodellen inte är **Pris per enhet**, kommer standardkostnaden att nollställas.</span><span class="sxs-lookup"><span data-stu-id="dfc9a-121">If the system can't match the **Category** and **Unit** values, or if it's able to find a matching category price line but the pricing method isn't **Price Per Unit**, the cost rate defaults to zero(0).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]