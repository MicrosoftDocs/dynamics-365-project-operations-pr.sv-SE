---
title: Nyheter och ändringar i Project Service Automation, uppdateringsversion 20, V3
description: I detta ämne anges de funktioner och snabbkorrigeringar som finns tillgängliga i Project Service Automation, uppdateringsversion 20, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5562b1de1d655328cfbb22e46c7fed53525507b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006533"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="1d983-103">Project Service Automation uppdateringsversion 20, V3</span><span class="sxs-lookup"><span data-stu-id="1d983-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1d983-104">Vi är glada att kunna presentera den senaste uppdateringen för programmet Project Service Automation för Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1d983-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1d983-105">Den här versionen innehåller viktiga förbättringar av kvalitet, prestanda och användbarhet.</span><span class="sxs-lookup"><span data-stu-id="1d983-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1d983-106">Den här versionen är kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1d983-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1d983-107">Om du vill uppdatera till den här versionen går du till administrationscenter för Dynamics 365 online och går till sidan Lösningar för att installera uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="1d983-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1d983-108">Mer information finns i: [Installera, uppdatera eller ta bort en prioriterad lösning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1d983-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1d983-109">I det här ämne finns funktioner och korrigeringar som är nya eller ändrade för Project Service Automation V3, uppdatering version 20.</span><span class="sxs-lookup"><span data-stu-id="1d983-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="1d983-110">Den här versionen har ett versionsnummer på V 3.10.31.37 och är allmänt tillgänglig via en självuppdatering i juni 2020.</span><span class="sxs-lookup"><span data-stu-id="1d983-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="1d983-111">Uppdatering version 20</span><span class="sxs-lookup"><span data-stu-id="1d983-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1d983-112">Felkorrigeringar</span><span class="sxs-lookup"><span data-stu-id="1d983-112">Bug fixes</span></span>

<span data-ttu-id="1d983-113">**Projektledning**</span><span class="sxs-lookup"><span data-stu-id="1d983-113">**Project Management**</span></span>

<span data-ttu-id="1d983-114">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="1d983-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="1d983-115">Om du importerar projektmedlemmar med en allokeringsmetod som kräver timmar uppstår ett oklart felmeddelande när de angivna timmarna är noll.</span><span class="sxs-lookup"><span data-stu-id="1d983-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="1d983-116">Användare får ett felmeddelande när det maximala tillåtna antalet tecken har angetts i fältet **Beskrivning** för en projektaktivitet.</span><span class="sxs-lookup"><span data-stu-id="1d983-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="1d983-117">Sidan **Hämta tillägg för Microsoft Dynamics 365 Project Service Automation** omdirigeras till den engelska hämtningssidan när användarens språkinställningar är inställda på japanska.</span><span class="sxs-lookup"><span data-stu-id="1d983-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="1d983-118">När ett serverfel inträffar blir synkroniseringsetiketten på fliken **schema** i formuläret **projekt** ibland kvar.</span><span class="sxs-lookup"><span data-stu-id="1d983-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="1d983-119">Redundanta aktivitetsuppdateringar skickas till servern när en uppgift ändras.</span><span class="sxs-lookup"><span data-stu-id="1d983-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="1d983-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="1d983-120">**Sales**</span></span>

<span data-ttu-id="1d983-121">Följande problem har åtgärdats:</span><span class="sxs-lookup"><span data-stu-id="1d983-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="1d983-122">På formuläret **Kontrakt** dubbelklickar du på **Skapa faktura** för att skapa två fakturor för en post i en verklig post.</span><span class="sxs-lookup"><span data-stu-id="1d983-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="1d983-123">I Internet Explorer 11 kan användare inte skapa utgiftsposter.</span><span class="sxs-lookup"><span data-stu-id="1d983-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="1d983-124">Återföring av kostnad och återföring av faktiska fakturerade försäljningsvärden är inte kopplade.</span><span class="sxs-lookup"><span data-stu-id="1d983-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="1d983-125">Knappen **Uppdatera faktiska värden** på formuläret **Projekt** uppdaterar inte **Uppgifternas faktiska tider**.</span><span class="sxs-lookup"><span data-stu-id="1d983-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="1d983-126">Plugin-programmet **PreValidateProjectTeamMemberCreate** kan skapa dubbletter av allmänna bokningsbara resurser när attributet **msdyn_isgenericresourceprojectscoped** anges till **False**.</span><span class="sxs-lookup"><span data-stu-id="1d983-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="1d983-127">**Beräkna om** rensar debiterbara kostnader för produktbaserad offertradinformation och kontraktradinformation.</span><span class="sxs-lookup"><span data-stu-id="1d983-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="1d983-128">I vissa scenarier visar plugin-programmet **PostEstimateLineUpdate** ett undantagsfel med null-referens.</span><span class="sxs-lookup"><span data-stu-id="1d983-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="1d983-129">Varaktighet av tidsfas på **Diagram över lönsamhetsanalys** stämmer inte överens med kostnaderna i offertradsinformationen om fast pris.</span><span class="sxs-lookup"><span data-stu-id="1d983-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="1d983-130">Värdena för enhet och enhetsgrupp är inte korrekt standard för utgiftskategorier i formulären **kontraktradsinformation** och **offertradsinformation**.</span><span class="sxs-lookup"><span data-stu-id="1d983-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="1d983-131">**Självkostnad för organisationsenhet** anger tillåtna överlappningar i giltighetsdatum.</span><span class="sxs-lookup"><span data-stu-id="1d983-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="1d983-132">Användare har inte behörighet att ändra **OrgUnit** när ordertypen inte fungerar eftersom den leder till ett fel av typen null-referens.</span><span class="sxs-lookup"><span data-stu-id="1d983-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="1d983-133">När du försöker navigera från formuläret **Information om offertrad** tillbaka till **Offert** uppdateras formuläret och fliken **Sammanfattning**.</span><span class="sxs-lookup"><span data-stu-id="1d983-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]