---
title: Hantera projektkontrakt
description: I det här ämnet finns information om att visa projektbaserade kontrakt.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e2f182f66bd1f4fe57d19e4bf82525ac8b84c29
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003113"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="f7766-103">Hantera projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="f7766-103">Manage project contracts</span></span>

<span data-ttu-id="f7766-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="f7766-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f7766-105">Projektkontrakt i Dynamics 365 Project Operations fångar in och hanterar avtalsenlig information om åtaganden och faktureringsuppgifter för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="f7766-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="f7766-106">Strukturen på ett projektkontrakt i Project Operation är skräddarsydd för projektbaserade funktioner med följande komponenter:</span><span class="sxs-lookup"><span data-stu-id="f7766-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="f7766-107">Kontraktrader som identifierar de diskreta komponenterna i arbete som visas som högnivå komponenter på en projektfaktura.</span><span class="sxs-lookup"><span data-stu-id="f7766-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="f7766-108">Kontraktradsinformation som identifierar och uppskattar arbetet för varje hög nivå komponent eller kontraktsrad.</span><span class="sxs-lookup"><span data-stu-id="f7766-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="f7766-109">Uppskattningen inkluderar schema och finansiella aspekter för arbetet knutet till kontraktraden.</span><span class="sxs-lookup"><span data-stu-id="f7766-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="f7766-110">Avtalade modeller och debiterbara komponenter skapas för varje kontraktrad som innehåller faktureringsöverenskommelsen för varje kontraktrad och hela kontraktet.</span><span class="sxs-lookup"><span data-stu-id="f7766-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="f7766-111">Visa alla projektbaserade kontrakt</span><span class="sxs-lookup"><span data-stu-id="f7766-111">View all project-based contracts</span></span>

<span data-ttu-id="f7766-112">En lista över alla projektkontrakt visas på listsidan **kontrakt**.</span><span class="sxs-lookup"><span data-stu-id="f7766-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="f7766-113">Gå till **Försäljning** > **Kontakter**.</span><span class="sxs-lookup"><span data-stu-id="f7766-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="f7766-114">En lista över alla projektkontrakt i systemet visas.</span><span class="sxs-lookup"><span data-stu-id="f7766-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="f7766-115">Välj **Visa växlare** (listpilen bredvid vyns namn) om du vill välja andra filtrerade vyer.</span><span class="sxs-lookup"><span data-stu-id="f7766-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="f7766-116">Du kan skapa egna vyer med villkor för anpassade filter.</span><span class="sxs-lookup"><span data-stu-id="f7766-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="f7766-117">Du kan skapa eller ta bort kontrakt från den här listsidan eller informationssidorna.</span><span class="sxs-lookup"><span data-stu-id="f7766-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]