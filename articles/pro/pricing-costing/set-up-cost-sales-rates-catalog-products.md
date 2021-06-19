---
title: Konfigurera kostnads- och försäljningstaxa för katalogprodukter – Lite
description: I det här ämnet finns information om hur du konfigurerar kostnads- och försäljningstaxor för artiklar i en produktkatalog.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004364"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="2e3c4-103">Konfigurera kostnads- och försäljningstaxa för katalogprodukter – Lite</span><span class="sxs-lookup"><span data-stu-id="2e3c4-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="2e3c4-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="2e3c4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="2e3c4-105">Att ange priser för produktkatalogsobjekt i Dynamics 365 Project Operations sker på samma sätt som i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="2e3c4-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="2e3c4-106">I Project Operations kan produkter inte beräknas eller användas i projekt, varför produktkatalogpriser inte behöver anges i projektprislistor för offerter och kontrakt.</span><span class="sxs-lookup"><span data-stu-id="2e3c4-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="2e3c4-107">Använd fältet **Produktpris** för en offert, ett kontrakt eller ett konto om du vill konfigurera priser för produktkataloger.</span><span class="sxs-lookup"><span data-stu-id="2e3c4-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="2e3c4-108">Ange inga produktkatalogpriser i projektprislistorna.</span><span class="sxs-lookup"><span data-stu-id="2e3c4-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="2e3c4-109">Projektprislistor är exklusiva för Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2e3c4-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="2e3c4-110">Programspecifik affärslogik kopierar prislistorna från en offert till ett kontrakt.</span><span class="sxs-lookup"><span data-stu-id="2e3c4-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="2e3c4-111">Resultatet är en kontraktspecifik projektprislista.</span><span class="sxs-lookup"><span data-stu-id="2e3c4-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="2e3c4-112">Kopieringen kan fördröja offertvinsten om projektprislistan i offerten blir för stor.</span><span class="sxs-lookup"><span data-stu-id="2e3c4-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="2e3c4-113">Produktprislistor kopieras inte för att skapa anpassade prislistor i kontrakt.</span><span class="sxs-lookup"><span data-stu-id="2e3c4-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="2e3c4-114">Eftersom ingen kopiering förekommer påverkas inte offertprocessens prestanda.</span><span class="sxs-lookup"><span data-stu-id="2e3c4-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]