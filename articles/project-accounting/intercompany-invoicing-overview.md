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
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595563"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="04ecd-103">Koncernintern fakturering – Översikt</span><span class="sxs-lookup"><span data-stu-id="04ecd-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="04ecd-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="04ecd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="04ecd-105">Organisationen kan ha flera avdelningar, dotterbolag och andra juridiska enheter som överför produkter och tjänster till varandra för projekt.</span><span class="sxs-lookup"><span data-stu-id="04ecd-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="04ecd-106">Den juridiska person som tillhandahåller tjänsten eller produkten kallas den *långivande juridiska personen*.</span><span class="sxs-lookup"><span data-stu-id="04ecd-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="04ecd-107">Den juridiska person som erhåller tjänsten eller produkten kallas den *låntagande juridiska personen*.</span><span class="sxs-lookup"><span data-stu-id="04ecd-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="04ecd-108">Följande bild visar ett typiskt scenario där två juridiska personer, Contoso Robotics USA (den låntagande juridiska personen) och Contoso Robotics UK (den utlånande juridiska personen) delar resurser för att leverera ett projekt åt kunden, Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="04ecd-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="04ecd-109">För detta scenario är Contoso Robotics USA kontrakterat att leverera arbetet till Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="04ecd-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Koncernintern fakturering](./media/IntercompanyScenario.png) 

<span data-ttu-id="04ecd-111">Dynamics 365 Project Operations använder följande flöde för att bearbeta koncerninterna transaktioner:</span><span class="sxs-lookup"><span data-stu-id="04ecd-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="04ecd-112">Resurser från den utlånande juridiska personen registrerar koncerninterna tids- eller utgiftstransaktioner efter bokningstid och kostnad mot projekt i den låntagande juridiska personen.</span><span class="sxs-lookup"><span data-stu-id="04ecd-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="04ecd-113">Tids- och utgiftskostnader bokförs i det långivande företaget genom att använda det låntagande företagets enhetskostnadslista.</span><span class="sxs-lookup"><span data-stu-id="04ecd-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="04ecd-114">Koncerninterna, icke-fakturerade säljtransaktioner bokförs i det långivande företaget genom att använda det låntagande företagets enhetskostnadslista.</span><span class="sxs-lookup"><span data-stu-id="04ecd-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="04ecd-115">Ej fakturerade intäkter bokförs i det låntagande företaget med hjälp av projektkontraktets försäljningsprislista.</span><span class="sxs-lookup"><span data-stu-id="04ecd-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="04ecd-116">Kunden kan faktureras när ej fakturerade intäkter registreras.</span><span class="sxs-lookup"><span data-stu-id="04ecd-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="04ecd-117">Kunden behöver inte vänta tills den koncerninterna fakturahanteringen är klar.</span><span class="sxs-lookup"><span data-stu-id="04ecd-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="04ecd-118">Koncerninterna kundfakturor skapas på periodisk basis i det långivande företaget.</span><span class="sxs-lookup"><span data-stu-id="04ecd-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="04ecd-119">Fakturorna skapas manuellt eller genom att använda en periodisk automatiserad process.</span><span class="sxs-lookup"><span data-stu-id="04ecd-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="04ecd-120">En enskild faktura kan skapas för varje låntagande juridisk person, eller också kan separata fakturor kapas efter projekt.</span><span class="sxs-lookup"><span data-stu-id="04ecd-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="04ecd-121">När den koncerninterna kundfakturan bokförs i den utlånande juridiska personen skapas motsvarande, väntande leverantörsfaktura i låntagande juridisk person.</span><span class="sxs-lookup"><span data-stu-id="04ecd-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="04ecd-122">Kostnaderna i den väntande leverantörsfakturan kommer att registreras i projektredovisningen när fakturan bokförs.</span><span class="sxs-lookup"><span data-stu-id="04ecd-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="04ecd-123">Följande diagram illustrerar koncernintern fakturering eftersom denna avser redovisningshändelser och förväntade bokföringar i redovisningen.</span><span class="sxs-lookup"><span data-stu-id="04ecd-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Koncerninternt flöde](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="04ecd-125">Ytterligare resurser</span><span class="sxs-lookup"><span data-stu-id="04ecd-125">Additional resources</span></span>

- [<span data-ttu-id="04ecd-126">Konfigurera koncernintern fakturering</span><span class="sxs-lookup"><span data-stu-id="04ecd-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="04ecd-127">Registrera koncerninterna transaktioner</span><span class="sxs-lookup"><span data-stu-id="04ecd-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="04ecd-128">Skapa koncerninterna kund- och leverantörsfakturor</span><span class="sxs-lookup"><span data-stu-id="04ecd-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)
