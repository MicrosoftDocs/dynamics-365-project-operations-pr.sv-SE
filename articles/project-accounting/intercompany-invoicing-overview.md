---
title: Koncernintern fakturering – Översikt
description: Detta ämne innehåller information och exempel om konfigurering av koncernintern fakturering av projekt.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287350"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="dc0a8-103">Koncernintern fakturering – Översikt</span><span class="sxs-lookup"><span data-stu-id="dc0a8-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="dc0a8-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="dc0a8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dc0a8-105">Organisationen kan ha flera avdelningar, dotterbolag och andra juridiska enheter som överför produkter och tjänster till varandra för projekt.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="dc0a8-106">Den juridiska person som tillhandahåller tjänsten eller produkten kallas den *långivande juridiska personen*.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="dc0a8-107">Den juridiska person som erhåller tjänsten eller produkten kallas den *låntagande juridiska personen*.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="dc0a8-108">Följande bild visar ett typiskt scenario där två juridiska personer, Contoso Robotics USA (den låntagande juridiska personen) och Contoso Robotics UK (den utlånande juridiska personen) delar resurser för att leverera ett projekt åt kunden, Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="dc0a8-109">För detta scenario är Contoso Robotics USA kontrakterat att leverera arbetet till Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Koncernintern fakturering](./media/IntercompanyScenario.png) 

<span data-ttu-id="dc0a8-111">Dynamics 365 Project Operations använder följande flöde för att bearbeta koncerninterna transaktioner:</span><span class="sxs-lookup"><span data-stu-id="dc0a8-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="dc0a8-112">Resurser från den utlånande juridiska personen registrerar koncerninterna tids- eller utgiftstransaktioner efter bokningstid och kostnad mot projekt i den låntagande juridiska personen.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="dc0a8-113">Tids- och utgiftskostnader bokförs i det långivande företaget genom att använda det låntagande företagets enhetskostnadslista.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="dc0a8-114">Koncerninterna, icke-fakturerade säljtransaktioner bokförs i det långivande företaget genom att använda det låntagande företagets enhetskostnadslista.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="dc0a8-115">Ej fakturerade intäkter bokförs i det låntagande företaget med hjälp av projektkontraktets försäljningsprislista.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="dc0a8-116">Kunden kan faktureras när ej fakturerade intäkter registreras.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="dc0a8-117">Kunden behöver inte vänta tills den koncerninterna fakturahanteringen är klar.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="dc0a8-118">Koncerninterna kundfakturor skapas på periodisk basis i det långivande företaget.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="dc0a8-119">Fakturorna skapas manuellt eller genom att använda en periodisk automatiserad process.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="dc0a8-120">En enskild faktura kan skapas för varje låntagande juridisk person, eller också kan separata fakturor kapas efter projekt.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="dc0a8-121">När den koncerninterna kundfakturan bokförs i den utlånande juridiska personen skapas motsvarande, väntande leverantörsfaktura i låntagande juridisk person.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="dc0a8-122">Kostnaderna i den väntande leverantörsfakturan kommer att registreras i projektredovisningen när fakturan bokförs.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="dc0a8-123">Följande diagram illustrerar koncernintern fakturering eftersom denna avser redovisningshändelser och förväntade bokföringar i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="dc0a8-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Koncerninternt flöde](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="dc0a8-125">Ytterligare resurser</span><span class="sxs-lookup"><span data-stu-id="dc0a8-125">Additional resources</span></span>

- [<span data-ttu-id="dc0a8-126">Konfigurera koncernintern fakturering</span><span class="sxs-lookup"><span data-stu-id="dc0a8-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="dc0a8-127">Registrera koncerninterna transaktioner</span><span class="sxs-lookup"><span data-stu-id="dc0a8-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="dc0a8-128">Skapa koncerninterna kund- och leverantörsfakturor</span><span class="sxs-lookup"><span data-stu-id="dc0a8-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]