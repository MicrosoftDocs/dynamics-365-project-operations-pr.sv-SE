---
title: Skapa en manuell proforma-faktura
description: I det här ämnet finns information om hur du manuellt skapar en proforma-faktura i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4085769"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="e3b74-103">Skapa en manuell proforma-faktura</span><span class="sxs-lookup"><span data-stu-id="e3b74-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="e3b74-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="e3b74-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e3b74-105">I Dynamics 365 Project Operations kan du skapa proforma-fakturor manuellt efter behov.</span><span class="sxs-lookup"><span data-stu-id="e3b74-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="e3b74-106">Du kan manuellt skapa en proforma-faktura från listsidan **Projektkontrakt** eller från informationssidan **Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="e3b74-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="e3b74-107">Listsidan Projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="e3b74-107">Project Contracts list page</span></span>

<span data-ttu-id="e3b74-108">Från listsidan **Projektkontrakt** väljer du ett eller flera projektkontrakt och skapar fakturor för alla valda poster.</span><span class="sxs-lookup"><span data-stu-id="e3b74-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="e3b74-109">Systemet kontrollerar om de valda projektkontrakten har en backlogg **Redo att fakturera** före dagens datum.</span><span class="sxs-lookup"><span data-stu-id="e3b74-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="e3b74-110">Från dessa kontrakt skapas utkast av proforma-fakturor.</span><span class="sxs-lookup"><span data-stu-id="e3b74-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="e3b74-111">Om ett projektkontrakt har flera kunder kan en faktura skapas per kund och flera fakturor per projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="e3b74-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="e3b74-112">Alla projektfakturor som skapas finns på sidan **Faktura** i avsnittet **Fakturering** i områden **Försäljning**.</span><span class="sxs-lookup"><span data-stu-id="e3b74-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="e3b74-113">Informationssidan Projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="e3b74-113">Project Contract details page</span></span>

<span data-ttu-id="e3b74-114">En proforma-faktura kan även skapas från informationssidan **Projektkontrakt** , som skapar fakturan för det specifika projektkontraktet.</span><span class="sxs-lookup"><span data-stu-id="e3b74-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="e3b74-115">Systemet verifierar att projektkontraktet har en backlogg **Redo att fakturera** före dagens datum.</span><span class="sxs-lookup"><span data-stu-id="e3b74-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="e3b74-116">Från de här kontrakten skapas utkast av proforma-fakturor utifrån antalet kunder på varje kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="e3b74-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="e3b74-117">När du har skapat en proforma-faktura öppnas sidan **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="e3b74-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="e3b74-118">Om flera fakturor har skapats för projektkontraktet öppnas listsidan **Fakturor** där alla skapade fakturor visas.</span><span class="sxs-lookup"><span data-stu-id="e3b74-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
