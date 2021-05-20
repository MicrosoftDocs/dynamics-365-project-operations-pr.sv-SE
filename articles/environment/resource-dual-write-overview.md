---
title: Project Operations-integration med dubbelriktad skrivning
description: Ämnet innehåller en översikt över Project Operations-integration med dubbelriktad skrivning.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955680"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="1121b-103">Översikt över Project Operations-integration med dubbelriktad skrivning</span><span class="sxs-lookup"><span data-stu-id="1121b-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="1121b-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="1121b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1121b-105">Project Operations använder [funktioner för dubbelriktad skrivning](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) för att synkronisera data mellan Microsoft Dataverse och Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="1121b-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="1121b-106">Följande illustrerar hur data synkroniseras som en del av integrationen mellan Dataverse och Ekonomi.</span><span class="sxs-lookup"><span data-stu-id="1121b-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Översikt över Project Operations dataflöden](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="1121b-108">Project Operations i Dataverse har ett modernt användargränssnitt (UI) och är enkelt att utöka med lite eller ingen kod med hjälp av funktionerna i Power Platform.</span><span class="sxs-lookup"><span data-stu-id="1121b-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="1121b-109">Projektansvariga, resursansvariga, projektteammedlemmar och andra personer på kontoret utför sina aktiviteter i Project Operations i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1121b-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="1121b-110">Project Operations i Ekonomi har stöd för projektredovisning och intäktsidentifiering.</span><span class="sxs-lookup"><span data-stu-id="1121b-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="1121b-111">Project Operations ansluter till det ekonomiska ramverket i Ekonomi för momsberäkning, växelkurser, rapportering av ekonomiska mått med mera.</span><span class="sxs-lookup"><span data-stu-id="1121b-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="1121b-112">Projektredovisaren är till största delen baserad i Ekonomi.</span><span class="sxs-lookup"><span data-stu-id="1121b-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="1121b-113">Project Operations-integration består av följande komponentintegration:</span><span class="sxs-lookup"><span data-stu-id="1121b-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="1121b-114">Inställning och konfiguration av Project Operations för dataintegration</span><span class="sxs-lookup"><span data-stu-id="1121b-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="1121b-115">Projektberäkningar och faktiska värden</span><span class="sxs-lookup"><span data-stu-id="1121b-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="1121b-116">Projektfaktura</span><span class="sxs-lookup"><span data-stu-id="1121b-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="1121b-117">Utgiftshantering</span><span class="sxs-lookup"><span data-stu-id="1121b-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="1121b-118">Leverantörsfaktura</span><span class="sxs-lookup"><span data-stu-id="1121b-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
