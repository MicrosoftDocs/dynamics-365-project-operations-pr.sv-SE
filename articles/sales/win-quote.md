---
title: Stäng en offert
description: I det här ämnet finns information om hur du stänger offerter i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 47804db0144c2b0f9dee2c60518e8aba6fb27473
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124705"
---
# <a name="close-a-quote"></a><span data-ttu-id="bbb7e-103">Stäng en offert</span><span class="sxs-lookup"><span data-stu-id="bbb7e-103">Close a quote</span></span>

<span data-ttu-id="bbb7e-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="bbb7e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bbb7e-105">En projektoffert kan stängas som Vunnen eller Förlorad.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="bbb7e-106">Eftersom åtgärderna Aktivera och Omarbeta inte stöds för offerter i Microsoft Dynamics 365 Project Operations, så kan du stänga ett utkast till en offert.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="bbb7e-107">Stänga en offert som Vunnen</span><span class="sxs-lookup"><span data-stu-id="bbb7e-107">Close a quote as Won</span></span>

<span data-ttu-id="bbb7e-108">Om du stänger en projektoffert som Vunnen anges statusen för offerten till **Stängd** och statusorsaken till **Vunnen**.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="bbb7e-109">Om du stänger offerter blir de skrivskyddade och ett utkast skapas i ett projektkontrakt med all offertinformationen.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="bbb7e-110">Eftersom en stängd offert inte kan öppnas på nytt innan du stänger en offert, bekräftas dina ändringar i en bekräftelsedialogruta.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="bbb7e-111">Projektkontraktet som skapas från en projektoffert görs också tillgängligt i projektlednings- och redovisningsmodulen i Project Operations.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="bbb7e-112">Om ett projektkontrakt inte är mappat till ett projekt på någon av raderna blir det här projektkontraktet tillgängligt som ett inaktivt projektkontrakt och aktiveras så fort ett projekt har mappats till minst en av kontraktraderna.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="bbb7e-113">Om offerten är kopplad till en affärsmöjlighet stängs alla andra projektofferter i affärsmöjligheten automatiskt som Förlorade.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="bbb7e-114">Ekonomiska följder av att stänga en offert som Vunnen</span><span class="sxs-lookup"><span data-stu-id="bbb7e-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="bbb7e-115">Om det finns verkliga värden för tid som har registrerats i ett projekt men det fortfarande är kopplat till ett utkast till en offert, registreras endast kostnaden för tiden eller kostnaden.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="bbb7e-116">När en offert stängs som Vunnen omstrukturerar programmet kostnaderna genom att återföra de äldre faktiska värdena för kostnad och återskapa nya faktiska värden för kostnad.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="bbb7e-117">Programmet behandlar dessa faktiska värden för kostnad baserat på den faktureringsmetod som är kopplad till projektkontraktsraden.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="bbb7e-118">Om de faktiska värdena för kostnad hänvisar till kontaktraden för tid och material, skapar systemet automatiskt motsvarande ofakturerade faktiska värden för försäljning när offerten stängs och projektkontraktet skapas.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="bbb7e-119">Om de faktiska värdena för kostnad hänvisar till en kontraktrad för fast pris, slutar programmet att behandla de faktiska värdena för kostnad baserat på reglerna för delad fakturering för projektkontraktets kunder.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="bbb7e-120">Alla ombearbetade verkliga värden finns i modulen Projektledning och redovisning för projektrevisorn att granska, uppdatera och bokföra i huvudboken.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="bbb7e-121">Stänga en offert som Förlorad</span><span class="sxs-lookup"><span data-stu-id="bbb7e-121">Close a quote as Lost</span></span>

<span data-ttu-id="bbb7e-122">Om du stänger en projektoffert som Förlorad anges status till **Stängd** och statusorsak som **Förlorad**.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="bbb7e-123">Om du stänger offerten blir den skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="bbb7e-124">Eftersom en stängd offert inte kan öppnas på nytt innan du stänger en offert, bekräftas dina ändringar i en bekräftelsedialogruta.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="bbb7e-125">Om projektofferten som stängs som Förlorad har ett projekt som refererar till någon av raderna visas även det projektet som Stängt och eventuella resursbokningar från den dagen framåt annulleras.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="bbb7e-126">När du stänger en offert som Vunnen eller Förlorad i Project Operations påverkas inte affärsmöjlighetens status, som förblir öppen tills den stängs manuellt.</span><span class="sxs-lookup"><span data-stu-id="bbb7e-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
