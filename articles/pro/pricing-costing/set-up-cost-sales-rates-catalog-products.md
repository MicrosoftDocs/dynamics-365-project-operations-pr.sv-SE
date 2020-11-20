---
title: Konfigurera kostnads- och försäljningstaxa för katalogprodukter – Lite
description: I det här ämnet finns information om hur du konfigurerar kostnads- och försäljningstaxor för artiklar i en produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176723"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="62c19-103">Konfigurera kostnads- och försäljningstaxa för katalogprodukter – Lite</span><span class="sxs-lookup"><span data-stu-id="62c19-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="62c19-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="62c19-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="62c19-105">Att konfigurera prissättning för produktkatalogsartiklar i Dynamics 365 Project Operations är samma som i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="62c19-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="62c19-106">Eftersom produkter inte kan uppskattas eller användas i Project Operations behöver du inte ange produktkatalogspriser på projektprislistor för offerter och kontrakt.</span><span class="sxs-lookup"><span data-stu-id="62c19-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="62c19-107">Produktkatalogspriser bör konfigureras i fältet **Produktpris** i en offert, ett kontrakt eller konto.</span><span class="sxs-lookup"><span data-stu-id="62c19-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="62c19-108">Konfigurera inte produktkatalogspriser i projektprislistorna för dessa entiteter.</span><span class="sxs-lookup"><span data-stu-id="62c19-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="62c19-109">Projektprislistor är exklusiva för Project Operations.</span><span class="sxs-lookup"><span data-stu-id="62c19-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="62c19-110">Det finns programspecifik affärslogik som kopierar prislistorna från en offert till ett kontrakt.</span><span class="sxs-lookup"><span data-stu-id="62c19-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="62c19-111">Resultatet är en kontraktspecifik projektprislista.</span><span class="sxs-lookup"><span data-stu-id="62c19-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="62c19-112">Kopieringen kan fördröja offertvinsten om projektprislistan i offerten blir för stor.</span><span class="sxs-lookup"><span data-stu-id="62c19-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="62c19-113">Produktprislistor kopieras inte för att skapa anpassade prislistor i kontrakt.</span><span class="sxs-lookup"><span data-stu-id="62c19-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="62c19-114">Detta innebär att produktprislistor inte påverkar effektiviteten i offertvinstprocessen.</span><span class="sxs-lookup"><span data-stu-id="62c19-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
