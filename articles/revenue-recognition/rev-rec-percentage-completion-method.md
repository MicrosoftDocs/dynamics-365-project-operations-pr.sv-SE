---
title: Intäktsberäkningar för fastprisprojekt
description: I det här ämnet finns information om intäkter i fastprisprojekt.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278935"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="aaca4-103">Intäktsberäkningar för fastprisprojekt</span><span class="sxs-lookup"><span data-stu-id="aaca4-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="aaca4-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="aaca4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="aaca4-105">När du skapar en projektkontraktrad med följande attribut i Dynamics 365 Project Operations för Microsoft Dataverse, skapar systemet automatiskt ett uppskattningsprojekt för fastprisintäkter.</span><span class="sxs-lookup"><span data-stu-id="aaca4-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="aaca4-106">Informationen i detta projekt baseras på följande:</span><span class="sxs-lookup"><span data-stu-id="aaca4-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="aaca4-107">En faktureringsmetod för fast pris.</span><span class="sxs-lookup"><span data-stu-id="aaca4-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="aaca4-108">Ett associerat projekt.</span><span class="sxs-lookup"><span data-stu-id="aaca4-108">An associated project.</span></span>
  - <span data-ttu-id="aaca4-109">Minst en milstolpe som definierats på fliken **Fakturaschema** på fliken **Projektkontaktrad**.</span><span class="sxs-lookup"><span data-stu-id="aaca4-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="aaca4-110">Granska intäktsberäkningar för fastprisprojekt</span><span class="sxs-lookup"><span data-stu-id="aaca4-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="aaca4-111">Slutför följande steg om du vill granska projekt för fasta prisintäkter:</span><span class="sxs-lookup"><span data-stu-id="aaca4-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="aaca4-112">I miljön Dynamics 365 Finance går du till **Projektledning och redovisning** > **Projekt** > **Intäktsberäkningar för fastprisprojekt**.</span><span class="sxs-lookup"><span data-stu-id="aaca4-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="aaca4-113">Välj det projekt som du vill visa och dubbelklicka på **Projekt-ID för uppskattning** för att öppna posten och granska informationen i projektet.</span><span class="sxs-lookup"><span data-stu-id="aaca4-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="aaca4-114">Expandera fliken **Projekt**. Du ser då ett projekt i rutnätet **Valda projekt**.</span><span class="sxs-lookup"><span data-stu-id="aaca4-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="aaca4-115">Systemet använder detta som standardprojekt eftersom det är projektet som är associerat med projektkontraktraden.</span><span class="sxs-lookup"><span data-stu-id="aaca4-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="aaca4-116">Om du vill ändra associationen väljer du ytterligare projekt och lägger till dem i rutnätet **Valda projekt**.</span><span class="sxs-lookup"><span data-stu-id="aaca4-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="aaca4-117">Om flera projekt väljs i det här rutnätet beräknas projektprocentberäkningen och intäktsuppskattningar tillsammans för samtliga valda projekt.</span><span class="sxs-lookup"><span data-stu-id="aaca4-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="aaca4-118">Projektkostnad, intäktsprofil, kostnadsmall och periodkod kan anges manuellt.</span><span class="sxs-lookup"><span data-stu-id="aaca4-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="aaca4-119">Om de inte anges manuellt kommer värdena att återgå till sina respektive standardvärden under den första uppskattningsberäkningen för projektet med hjälp av de regler som konfigurerats för projektkostnad och intäktsprofiler.</span><span class="sxs-lookup"><span data-stu-id="aaca4-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]