---
title: Nyheter eller ändringar i Project Service Automation version 3.x våg 1 2020
description: I det här ämnet finns information om vad som är nytt och ändrat i Project Service Automation version 3 våg 1 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f77c881c62428e423e0dab66eb34b033628a2a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996858"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="9344b-103">Nyheter eller ändringar i Project Service Automation version 3 våg 1 2020</span><span class="sxs-lookup"><span data-stu-id="9344b-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9344b-104">I ämnet framhävs viktiga uppgraderingsaspekter när de flyttar till den senaste versionen av Project Service Automation (PSA) version 3.x våg 1 2020.</span><span class="sxs-lookup"><span data-stu-id="9344b-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="9344b-105">Tidspost</span><span class="sxs-lookup"><span data-stu-id="9344b-105">Time entry</span></span>
<span data-ttu-id="9344b-106">Tidsingångsupplevelsen har utökats för att ge möjlighet att förlänga tidregistreringen i fler kundscenarier.</span><span class="sxs-lookup"><span data-stu-id="9344b-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="9344b-107">I det här ingår möjligheten att lägga till transaktionstyper, som nu specifikt styr funktioner som baseras på fältschemanamn **Inställningar för tidspost** som visas som **tidskälla**.</span><span class="sxs-lookup"><span data-stu-id="9344b-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="9344b-108">En ny lösning som kallas tid, kostnad, status och godkännanden (TESA) har lagts till för att stödja den här funktionen.</span><span class="sxs-lookup"><span data-stu-id="9344b-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="9344b-109">Att tänka på när du uppgraderar</span><span class="sxs-lookup"><span data-stu-id="9344b-109">Upgrade consideration</span></span>
<span data-ttu-id="9344b-110">För att du ska kunna använda den här funktionen har rollerna inom PSA-uppdateringen uppdaterats med nya privilegier.</span><span class="sxs-lookup"><span data-stu-id="9344b-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="9344b-111">De här privilegierna ger läsbehörighet till den nya entiteten **tidsinmatningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="9344b-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="9344b-112">Användare som kräver möjlighet att logga tid bör ges användarrollen **tidspostanvändare** utöver befintliga roller.</span><span class="sxs-lookup"><span data-stu-id="9344b-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="9344b-113">Den här rollen omfattar de nya funktionerna och ser till att tidsposten fortsätter att fungera.</span><span class="sxs-lookup"><span data-stu-id="9344b-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="9344b-114">Om du har några anpassade programmoduler som innehåller alla formulär för entiteten tidspost måste du ta bort **Snabbregistreringsformulär för TESA tidspost** från modulen.</span><span class="sxs-lookup"><span data-stu-id="9344b-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="9344b-115">För närvarande ändras utökad tidspost</span><span class="sxs-lookup"><span data-stu-id="9344b-115">Currently extended time entry changes</span></span>
<span data-ttu-id="9344b-116">Den här rolländringen är det enda grundläggande kravet som krävs för att fortsätta utnyttjandet av tidposten för att minimera påverkan för aktuella tidsposter.</span><span class="sxs-lookup"><span data-stu-id="9344b-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="9344b-117">Om du har skapat anpassade vyer eller olika tidstransaktionsupplevelser måste du ange korrekt fält för **tidspostinställning** i korrekt PSA-värde.</span><span class="sxs-lookup"><span data-stu-id="9344b-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]