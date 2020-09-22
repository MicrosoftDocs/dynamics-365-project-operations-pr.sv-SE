---
title: Nyheter eller ändringar i Project Service Automation version 3.x våg 1 2020
description: I det här ämnet finns information om vad som är nytt och ändrat i Project Service Automation version 3 våg 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756211"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="afc42-103">Nyheter eller ändringar i Project Service Automation version 3 våg 1 2020</span><span class="sxs-lookup"><span data-stu-id="afc42-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="afc42-104">I ämnet framhävs viktiga uppgraderingsaspekter när de flyttar till den senaste versionen av Project Service Automation (PSA) version 3.x våg 1 2020.</span><span class="sxs-lookup"><span data-stu-id="afc42-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="afc42-105">Tidspost</span><span class="sxs-lookup"><span data-stu-id="afc42-105">Time entry</span></span>
<span data-ttu-id="afc42-106">Tidsingångsupplevelsen har utökats för att ge möjlighet att förlänga tidregistreringen i fler kundscenarier.</span><span class="sxs-lookup"><span data-stu-id="afc42-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="afc42-107">I det här ingår möjligheten att lägga till transaktionstyper, som nu specifikt styr funktioner som baseras på fältschemanamn **Inställningar för tidspost** som visas som **tidskälla**.</span><span class="sxs-lookup"><span data-stu-id="afc42-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="afc42-108">Att tänka på när du uppgraderar</span><span class="sxs-lookup"><span data-stu-id="afc42-108">Upgrade consideration</span></span>
<span data-ttu-id="afc42-109">För att du ska kunna använda den här funktionen har rollerna inom PSA-uppdateringen uppdaterats med nya privilegier.</span><span class="sxs-lookup"><span data-stu-id="afc42-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="afc42-110">De här privilegierna ger läsbehörighet till den nya entiteten **tidsinmatningsinställningar**.</span><span class="sxs-lookup"><span data-stu-id="afc42-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="afc42-111">Användare som kräver möjlighet att logga tid bör ges användarrollen **tidspostanvändare** utöver befintliga roller.</span><span class="sxs-lookup"><span data-stu-id="afc42-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="afc42-112">Den här rollen omfattar de nya funktionerna och ser till att tidsposten fortsätter att fungera.</span><span class="sxs-lookup"><span data-stu-id="afc42-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="afc42-113">För närvarande ändras utökad tidspost</span><span class="sxs-lookup"><span data-stu-id="afc42-113">Currently extended time entry changes</span></span>
<span data-ttu-id="afc42-114">Den här rolländringen är det enda grundläggande kravet som krävs för att fortsätta utnyttjandet av tidposten för att minimera påverkan för aktuella tidsposter.</span><span class="sxs-lookup"><span data-stu-id="afc42-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="afc42-115">Om du har skapat anpassade vyer eller olika tidstransaktionsupplevelser måste du ange korrekt fält för **tidspostinställning** i korrekt PSA-värde.</span><span class="sxs-lookup"><span data-stu-id="afc42-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
