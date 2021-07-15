---
title: Uppgradera startsidan
description: I det här ämnet visas var du hittar viktig information om de nya och ändrade funktioner i Dynamics 365 Project Service Automation och hur du uppgraderar till den senaste versionen.
ms.prod: ''
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8fc820d8fa0e421cdc963f391133e7311de96982
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368543"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="174b9-103">Uppgradera startsidan</span><span class="sxs-lookup"><span data-stu-id="174b9-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="174b9-104">Uppgradera från PSA-version 2.x eller 1.x till version 3.x</span><span class="sxs-lookup"><span data-stu-id="174b9-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="174b9-105">Nya instanser</span><span class="sxs-lookup"><span data-stu-id="174b9-105">New instances</span></span>

<span data-ttu-id="174b9-106">Från och med 17 maj 2019 när Project Service Automation väljs under etableringen av en ny instans installeras version 3.x som standard.</span><span class="sxs-lookup"><span data-stu-id="174b9-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="174b9-107">Befintliga instanser</span><span class="sxs-lookup"><span data-stu-id="174b9-107">Existing instances</span></span>

<span data-ttu-id="174b9-108">Tidigare måste kunder med en instans av PSA version 2.x som vari behov av att uppgradera till version 3.x (som utgör den PSA-version som är Unified-klientbaserad) kontakta Microsoft Support och tillhandahålla information om sin instans, så att supporten kunde aktivera instans för uppgradering till version 3.x.</span><span class="sxs-lookup"><span data-stu-id="174b9-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="174b9-109">Från och med den 1 mars 2020 kan kunder som har en instans av PSA version 2.x och behöver uppgradera till version 3.x uppgradera sina instanser direkt från administrationsportalen utan att behöva kontakta Microsoft Support.</span><span class="sxs-lookup"><span data-stu-id="174b9-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="174b9-110">PSA version 3.x innehåller viktiga förändringar.</span><span class="sxs-lookup"><span data-stu-id="174b9-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="174b9-111">Den har byggts på ramverk för enhetligt gränssnitt för att ge en bättre användarupplevelse.</span><span class="sxs-lookup"><span data-stu-id="174b9-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="174b9-112">Den omkonstruerade appen levererar ett konsistent, enhetligt användargränssnitt (UI) och följer de designprinciper som är tillgängliga för optimal visning på alla skärmstorlekar och enheter.</span><span class="sxs-lookup"><span data-stu-id="174b9-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="174b9-113">Det har gjorts andra ändringar i hela programmet.</span><span class="sxs-lookup"><span data-stu-id="174b9-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="174b9-114">Vissa av de områden som har ändrats är bland annat prissättning, bokning och tilldelning av resurser, tid, utgifter och godkännanden.</span><span class="sxs-lookup"><span data-stu-id="174b9-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="174b9-115">Innan du börjar uppgraderingsprocessen rekommenderar vi att du utför följande uppgifter:</span><span class="sxs-lookup"><span data-stu-id="174b9-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="174b9-116">Kontrollera om både Dynamics 365 Field Service och Project Service Automation har installerats på den identifierade instansen.</span><span class="sxs-lookup"><span data-stu-id="174b9-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="174b9-117">Om båda lösningarna är installerade bör du planera för att uppgradera både innan du återupptar den vanliga användningen av instansen.</span><span class="sxs-lookup"><span data-stu-id="174b9-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="174b9-118">Läs noggrant igenom följande avsnitt.</span><span class="sxs-lookup"><span data-stu-id="174b9-118">Carefully review the following topics.</span></span> <span data-ttu-id="174b9-119">Medvetenheten och förståelsen av förändringar mellan versionerna hjälper dig att uppgradera processen.</span><span class="sxs-lookup"><span data-stu-id="174b9-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="174b9-120">I de här avsnitten finns information om de viktigaste ändringarna i PSA samt överväganden och rekommendationer för hur du planerar uppgraderingen till version 3.x.</span><span class="sxs-lookup"><span data-stu-id="174b9-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="174b9-121">Nyheter eller ändringar i Project Service Automation version 3</span><span class="sxs-lookup"><span data-stu-id="174b9-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="174b9-122">"Att tänka på när du uppgraderar - Project Service Automation version 2.x eller 1.x till version 3</span><span class="sxs-lookup"><span data-stu-id="174b9-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="174b9-123">Uppgradera testinstans i begränsat läge för att utvärdera ändringarna i implementeringen innan du uppgraderar produktionsinstansen.</span><span class="sxs-lookup"><span data-stu-id="174b9-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="174b9-124">När du har granskat ämnena som nämnts tidigare och är redo att uppgradera till PSA version 3.x eller den UCI-baserade versionen, skicka en begäran till Microsofts Support för att göra uppgraderingen tillgänglig från administrationscenter.</span><span class="sxs-lookup"><span data-stu-id="174b9-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="174b9-125">Ange information om instansen i din förfrågan.</span><span class="sxs-lookup"><span data-stu-id="174b9-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="174b9-126">Äldre versioner av PSA (PSA version 2.x) i en nyligen skapad instans</span><span class="sxs-lookup"><span data-stu-id="174b9-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="174b9-127">Från och med 17 maj 2019 kommer alla nya instanser att ha samma värde som standardklienten.</span><span class="sxs-lookup"><span data-stu-id="174b9-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="174b9-128">För att justeringen ska kunna ändras tillhandahålls PSA version 3.x och Field Service version 8.x som standard, eftersom dessa versioner har utformats för att fungera med UCI-klienten.</span><span class="sxs-lookup"><span data-stu-id="174b9-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="174b9-129">Från och med 1 mars 2020 kan Dynamics PSA-kunderna inte längre skapa en ny miljö med äldre versioner av PSA, till exempel PSA version 2.x eller lägre.</span><span class="sxs-lookup"><span data-stu-id="174b9-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="174b9-130">Alla nya miljöer kommer att behöva version 3.x av PSA.</span><span class="sxs-lookup"><span data-stu-id="174b9-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="174b9-131">För att få bästa möjliga resultat när du använder äldre versioner av Field Service och PSA-program går du till sidan **systeminställningar** och för fältet **Använd endast det nya enhetliga gränssnittet (rekommenderas)**, välj **Nej** eftersom de här versionerna inte har utformats för korrekt inläsning i UCI.</span><span class="sxs-lookup"><span data-stu-id="174b9-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="174b9-132">När du har inaktiverat UCI kan du öppna och köra de här versionerna av Field Service och PSA med hjälp av den gamla webbklienten.</span><span class="sxs-lookup"><span data-stu-id="174b9-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]