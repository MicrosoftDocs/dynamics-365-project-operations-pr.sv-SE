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
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531569"
---
# <a name="period-types"></a><span data-ttu-id="bb392-103">Periodtyper</span><span class="sxs-lookup"><span data-stu-id="bb392-103">Period types</span></span>

<span data-ttu-id="bb392-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="bb392-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bb392-105">En periodtyp definierar hur ofta intäkter uppskattas på ett projekt.</span><span class="sxs-lookup"><span data-stu-id="bb392-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="bb392-106">Detta ämne innehåller information om hur du konfigurerar periodtyper för intäktsuppskattning.</span><span class="sxs-lookup"><span data-stu-id="bb392-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="bb392-107">Skapa och arbeta med periodtyper</span><span class="sxs-lookup"><span data-stu-id="bb392-107">Create and work with period types</span></span>
<span data-ttu-id="bb392-108">Om du vill skapa och arbeta med periodtyper utför du följande steg:</span><span class="sxs-lookup"><span data-stu-id="bb392-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="bb392-109">I din Dynamics 365 Finance-miljö går du till **Projektledning och redovisning** > **Konfiguration** > **Uppskattningar** > **Periodtyper**.</span><span class="sxs-lookup"><span data-stu-id="bb392-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="bb392-110">Välj **Ny** för att skapa en ny periodtyp.</span><span class="sxs-lookup"><span data-stu-id="bb392-110">Select **New** to create new period type.</span></span> <span data-ttu-id="bb392-111">Ange ett namn och en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="bb392-111">Enter a name and description.</span></span>
3. <span data-ttu-id="bb392-112">Välj ett värde i fältet **Frekvens**:</span><span class="sxs-lookup"><span data-stu-id="bb392-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="bb392-113">Om du väljer **Vecka**, **Varannan vecka**, **Varannan månad**, **Månadsvis**, **Dagligen**, **Kvartalsvis** eller **Årligen** kommer kalendern att användas för att generera perioderna.</span><span class="sxs-lookup"><span data-stu-id="bb392-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="bb392-114">Om du väljer **Redovisningsperiod** kommer redovisningsperioder från konfigurationen för huvudbok att användas för att generera perioder.</span><span class="sxs-lookup"><span data-stu-id="bb392-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="bb392-115">Om du väljer **Obegränsat** kan du ange anpassade perioder.</span><span class="sxs-lookup"><span data-stu-id="bb392-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="bb392-116">Välj periodtypposten och välj sedan **Generera perioder** för att skapa perioder för periodtypen.</span><span class="sxs-lookup"><span data-stu-id="bb392-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="bb392-117">Baserat på periodfrekvensen som du har valt kanske du har möjlighet att ange ett startdatum eller antalet perioder som ska genereras.</span><span class="sxs-lookup"><span data-stu-id="bb392-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="bb392-118">Välj **Perioder** för att granska genererade perioder.</span><span class="sxs-lookup"><span data-stu-id="bb392-118">Select **Periods** to review generated periods.</span></span>

