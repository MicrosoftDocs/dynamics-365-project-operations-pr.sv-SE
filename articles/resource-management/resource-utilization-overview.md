---
title: Översikt över resursutnyttjande
description: I den här ämnet finns information om vyn resursanvändning i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401398"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="b705a-103">Översikt över resursutnyttjande</span><span class="sxs-lookup"><span data-stu-id="b705a-103">Resource utilization overview</span></span>

<span data-ttu-id="b705a-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="b705a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b705a-105">Resurser kan ha fakturerbar användning.</span><span class="sxs-lookup"><span data-stu-id="b705a-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="b705a-106">Den här målanvändningen definieras som ett attribut för en resurs standardroll eller anges i posten för den enskilda bokningsbara resursen.</span><span class="sxs-lookup"><span data-stu-id="b705a-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="b705a-107">Användningsberäkningar baseras på de faktiska timmarna som resurserna har rapporterat med hjälp av godkända tidtransaktioner.</span><span class="sxs-lookup"><span data-stu-id="b705a-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="b705a-108">Följande formler används för att beräkna användningen:</span><span class="sxs-lookup"><span data-stu-id="b705a-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="b705a-109">Fakturerbar användning = debiterbara faktiska timmar ÷ resurskapacitet för tillgång</span><span class="sxs-lookup"><span data-stu-id="b705a-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="b705a-110">Användning av ej fakturerbar tid = faktisk tid med faktureringstyp-ID = inte debiterbar, komplementär eller ej disponibelt ÷ resurskapacitet</span><span class="sxs-lookup"><span data-stu-id="b705a-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="b705a-111">Intern = faktisk tid utan försäljningskontrakt ÷ resurskapacitet</span><span class="sxs-lookup"><span data-stu-id="b705a-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="b705a-112">Resurskapacitet = resursens arbetstider – frånvarande – lediga dagar</span><span class="sxs-lookup"><span data-stu-id="b705a-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="b705a-113">Du hittar vyn **Resursutnyttjande** i fönstret **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="b705a-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="b705a-114">Varje cell i rutnätet representerar resursens fakturerbara användningsprocent i en period, t.ex. dag, vecka eller månad.</span><span class="sxs-lookup"><span data-stu-id="b705a-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="b705a-115">Följande formler används för att färglägga cellerna:</span><span class="sxs-lookup"><span data-stu-id="b705a-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="b705a-116">**Grön**: fakturerbart resursutnyttjande >= resursutnyttjande för målet.</span><span class="sxs-lookup"><span data-stu-id="b705a-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="b705a-117">**Gul**: mål för resursutnyttjande – 20 <= fakturerbart resursutnyttjande < mål för resursutnyttjande</span><span class="sxs-lookup"><span data-stu-id="b705a-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="b705a-118">**Röd**: fakturerbart resursutnyttjande < mål för resursutnyttjande – 20</span><span class="sxs-lookup"><span data-stu-id="b705a-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="b705a-119">Eftersom vyn **Resursutnyttjande** baseras på schemaläggningstavlan kan du filtrera resultaten med hjälp av filtreringsfunktionerna i schemaläggningstavlan.</span><span class="sxs-lookup"><span data-stu-id="b705a-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="b705a-120">Rutnätet kräver att du anger ett utnyttjandemål för antingen rollen eller den enskilda resursen.</span><span class="sxs-lookup"><span data-stu-id="b705a-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="b705a-121">För att göra detta går du till **Resurser** > **Resursroller**.</span><span class="sxs-lookup"><span data-stu-id="b705a-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="b705a-122">Dessutom måste en standardroll tilldelas varje bokningsbar resurs.</span><span class="sxs-lookup"><span data-stu-id="b705a-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="b705a-123">Gå till **Resurser** > **Resurser**.</span><span class="sxs-lookup"><span data-stu-id="b705a-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="b705a-124">På fliken **Project Service** kontrollera att en resursroll är definierad och att fältet **är standard** anges till **ja**.</span><span class="sxs-lookup"><span data-stu-id="b705a-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="b705a-125">Du kan lägga till ytterligare roller där **är standard** = **Nej**.</span><span class="sxs-lookup"><span data-stu-id="b705a-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="b705a-126">Rollen där **är standard** = **Ja** används för att utvärdera resursutnyttjande för resursen mot målet för rollen.</span><span class="sxs-lookup"><span data-stu-id="b705a-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="b705a-127">På fliken **Project Service** kan du också ange ett enskilt målutnyttjande för resursen.</span><span class="sxs-lookup"><span data-stu-id="b705a-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="b705a-128">Utnyttjandeberäkningen använder då målutnyttjande för att utvärdera resursens mål i stället för resursens standardroll.</span><span class="sxs-lookup"><span data-stu-id="b705a-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="b705a-129">Utnyttjande visas endast för en resurs om resursen har godkänt, debiterbar tid under den period som visas i rutnätet.</span><span class="sxs-lookup"><span data-stu-id="b705a-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>
