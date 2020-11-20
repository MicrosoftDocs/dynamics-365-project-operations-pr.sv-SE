---
title: Stänga en offert - lite
description: I det här ämnet finns information om hur du stänger en offert i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175733"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="4b96a-103">Stänga en offert - lite</span><span class="sxs-lookup"><span data-stu-id="4b96a-103">Close a quote - lite</span></span>

<span data-ttu-id="4b96a-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="4b96a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4b96a-105">En projektoffert kan stängas som Vunnen eller Förlorad.</span><span class="sxs-lookup"><span data-stu-id="4b96a-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="4b96a-106">Åtgärderna för att aktivera och omarbeta offerter stöds inte i Microsoft Dynamics 365 Project Operations, så ett utkast till en offert kan stängas.</span><span class="sxs-lookup"><span data-stu-id="4b96a-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="4b96a-107">Stänga en offert som Vunnen</span><span class="sxs-lookup"><span data-stu-id="4b96a-107">Close a quote as Won</span></span>

<span data-ttu-id="4b96a-108">Om du stänger en projektoffert som vunnen stängs offerten med status satt till Stängd och statusorsaken inställd på Vunnen.</span><span class="sxs-lookup"><span data-stu-id="4b96a-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="4b96a-109">Om du stänger offerten blir projektofferten skrivskyddad och ett utkast skapas i ett projektkontrakt som innehåller offertinformationen.</span><span class="sxs-lookup"><span data-stu-id="4b96a-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="4b96a-110">Eftersom det inte går att öppna en stängd offert igen visas en bekräftelsedialogruta innan ändringarna görs eftersom en stängd offert inte kan öppnas på nytt och ändringarna inte kan ångras.</span><span class="sxs-lookup"><span data-stu-id="4b96a-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="4b96a-111">Om offerten är kopplad till en affärsmöjlighet stängs alla andra projektofferter i affärsmöjligheten automatiskt som Förlorade.</span><span class="sxs-lookup"><span data-stu-id="4b96a-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="4b96a-112">Ekonomiska följder av att stänga en offert som Vunnen</span><span class="sxs-lookup"><span data-stu-id="4b96a-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="4b96a-113">Om det finns verkliga värden för tid som har registrerats i ett projekt men det fortfarande är kopplat till ett utkast till en offert, registreras endast kostnaden för tiden eller kostnaden.</span><span class="sxs-lookup"><span data-stu-id="4b96a-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="4b96a-114">När en offert stängs som Vunnen omstrukturerar programmet kostnaderna genom att återföra de äldre faktiska värdena för kostnad och återskapa nya faktiska värden för kostnad.</span><span class="sxs-lookup"><span data-stu-id="4b96a-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="4b96a-115">Programmet behandlar dessa faktiska värden för kostnad baserat på den faktureringsmetod som är kopplad till projektkontraktsraden.</span><span class="sxs-lookup"><span data-stu-id="4b96a-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="4b96a-116">Om de faktiska värdena för kostnad hänvisar till kontaktraden för tid och material, skapar systemet automatiskt motsvarande ofakturerade faktiska värden för försäljning när offerten stängs och projektkontraktet skapas.</span><span class="sxs-lookup"><span data-stu-id="4b96a-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="4b96a-117">Om de faktiska värdena för kostnad hänvisar till en kontraktrad för fast pris, slutar programmet att behandla de faktiska värdena för kostnad baserat på reglerna för delad fakturering för projektkontraktets kunder.</span><span class="sxs-lookup"><span data-stu-id="4b96a-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="4b96a-118">Stänga en offert som förlorad:</span><span class="sxs-lookup"><span data-stu-id="4b96a-118">Closing a quote as lost:</span></span>

<span data-ttu-id="4b96a-119">Om du stänger en projektoffert som Förlorad anges status till Stängd för statusorsak som Förlorad.</span><span class="sxs-lookup"><span data-stu-id="4b96a-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="4b96a-120">Om du stänger offerten blir projektofferten skrivskyddad.</span><span class="sxs-lookup"><span data-stu-id="4b96a-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="4b96a-121">Eftersom en stängd offert inte kan öppnas på nytt innan du stänger en offert, bekräftas dina ändringar i en bekräftelsedialogruta.</span><span class="sxs-lookup"><span data-stu-id="4b96a-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="4b96a-122">Om projektofferten som stängs som Förlorad har ett projekt som refererar till någon av raderna visas även det projektet som Stängt och eventuella resursbokningar från den dagen framåt annulleras.</span><span class="sxs-lookup"><span data-stu-id="4b96a-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="4b96a-123">När du stänger en offert som Vunnen eller Förlorad i Project Operations påverkas inte affärsmöjlighetens status, som förblir öppen tills den stängs manuellt.</span><span class="sxs-lookup"><span data-stu-id="4b96a-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
