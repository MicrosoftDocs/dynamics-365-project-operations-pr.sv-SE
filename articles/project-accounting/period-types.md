---
title: Periodtyper
description: Detta ämne innehåller information om hur du konfigurerar periodtyper för intäktsuppskattning.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287305"
---
# <a name="period-types"></a><span data-ttu-id="a5b6d-103">Periodtyper</span><span class="sxs-lookup"><span data-stu-id="a5b6d-103">Period types</span></span>

<span data-ttu-id="a5b6d-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="a5b6d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a5b6d-105">En periodtyp definierar hur ofta intäkter uppskattas på ett projekt.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="a5b6d-106">Detta ämne innehåller information om hur du konfigurerar periodtyper för intäktsuppskattning.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="a5b6d-107">Skapa och arbeta med periodtyper</span><span class="sxs-lookup"><span data-stu-id="a5b6d-107">Create and work with period types</span></span>
<span data-ttu-id="a5b6d-108">Om du vill skapa och arbeta med periodtyper utför du följande steg:</span><span class="sxs-lookup"><span data-stu-id="a5b6d-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="a5b6d-109">I din Dynamics 365 Finance-miljö går du till **Projektledning och redovisning** > **Konfiguration** > **Uppskattningar** > **Periodtyper**.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="a5b6d-110">Välj **Ny** för att skapa en ny periodtyp.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-110">Select **New** to create new period type.</span></span> <span data-ttu-id="a5b6d-111">Ange ett namn och en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-111">Enter a name and description.</span></span>
3. <span data-ttu-id="a5b6d-112">Välj ett värde i fältet **Frekvens**:</span><span class="sxs-lookup"><span data-stu-id="a5b6d-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="a5b6d-113">Om du väljer **Vecka**, **Varannan vecka**, **Varannan månad**, **Månadsvis**, **Dagligen**, **Kvartalsvis** eller **Årligen** kommer kalendern att användas för att generera perioderna.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="a5b6d-114">Om du väljer **Redovisningsperiod** kommer redovisningsperioder från konfigurationen för huvudbok att användas för att generera perioder.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="a5b6d-115">Om du väljer **Obegränsat** kan du ange anpassade perioder.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="a5b6d-116">Välj periodtypposten och välj sedan **Generera perioder** för att skapa perioder för periodtypen.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="a5b6d-117">Baserat på periodfrekvensen som du har valt kanske du har möjlighet att ange ett startdatum eller antalet perioder som ska genereras.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="a5b6d-118">Välj **Perioder** för att granska genererade perioder.</span><span class="sxs-lookup"><span data-stu-id="a5b6d-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]