---
title: Skapa en manuell proforma-faktura - lite
description: I det här ämnet finns information om hur du manuellt skapar en proforma-faktura i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274210"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="1a6f1-103">Skapa en manuell proforma-faktura - lite</span><span class="sxs-lookup"><span data-stu-id="1a6f1-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="1a6f1-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="1a6f1-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1a6f1-105">I Dynamics 365 Project Operations kan proforma-fakturor skapas manuellt efter behov.</span><span class="sxs-lookup"><span data-stu-id="1a6f1-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="1a6f1-106">Du kan manuellt skapa en proforma-faktura från listsidan **Projektkontrakt** eller från informationssidan **Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="1a6f1-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="1a6f1-107">Listsidan Projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="1a6f1-107">Project Contracts list page</span></span>

<span data-ttu-id="1a6f1-108">Från listsidan **Projektkontrakt** väljer du ett eller flera projektkontrakt och skapar fakturor för alla valda poster.</span><span class="sxs-lookup"><span data-stu-id="1a6f1-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="1a6f1-109">Systemet kontrollerar om de valda projektkontrakten har en **Redo att fakturera**-backlogg daterad före dagens datum.</span><span class="sxs-lookup"><span data-stu-id="1a6f1-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="1a6f1-110">Från dessa kontrakt skapas utkast av proforma-fakturor.</span><span class="sxs-lookup"><span data-stu-id="1a6f1-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="1a6f1-111">Om ett projektkontrakt har flera kunder kan en faktura skapas per kund och flera fakturor per projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="1a6f1-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="1a6f1-112">Alla projektfakturor som skapas finns på sidan **Faktura** i avsnittet **Fakturering** i områden **Försäljning**.</span><span class="sxs-lookup"><span data-stu-id="1a6f1-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="1a6f1-113">Informationssidan Projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="1a6f1-113">Project Contract details page</span></span>

<span data-ttu-id="1a6f1-114">En proforma-faktura kan också skapas från informationssidan **Projektkontrakt**.</span><span class="sxs-lookup"><span data-stu-id="1a6f1-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="1a6f1-115">Systemet bekräftar att projektkontraktet har en **Redo att fakturera**-backlogg daterad före dagens datum.</span><span class="sxs-lookup"><span data-stu-id="1a6f1-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="1a6f1-116">Från de här kontrakten skapas utkast av proforma-fakturor utifrån antalet kunder på varje kontraktrad.</span><span class="sxs-lookup"><span data-stu-id="1a6f1-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="1a6f1-117">När du har skapat en proforma-faktura öppnas sidan **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="1a6f1-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="1a6f1-118">Om flera fakturor skapas för projektkontraktet öppnas listsidan **Fakturor** för att visa alla skapade fakturor.</span><span class="sxs-lookup"><span data-stu-id="1a6f1-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]