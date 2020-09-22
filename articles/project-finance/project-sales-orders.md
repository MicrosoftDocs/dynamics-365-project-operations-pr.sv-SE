---
title: Projektförsäljningsorder för tids- och materialprojekt
description: I det här ämnet beskrivs hur du skapar projektbaserade försäljningsorder för tids- och materialprojekt.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756170"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="5658b-103">Projektförsäljningsorder för tids- och materialprojekt</span><span class="sxs-lookup"><span data-stu-id="5658b-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="5658b-104">I den här ämnet beskrivs hur du skapar en försäljningsorder för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="5658b-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="5658b-105">Det går endast att skapa försäljningsorder för projekt av typen **tid och material**.</span><span class="sxs-lookup"><span data-stu-id="5658b-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="5658b-106">Om ett tids- och materialprojekt har flera finansieringskällor i projektkontraktet måste du aktivera parametern **Tillåt försäljningsorder för projekt med flera finansieringskällor** på sidan **Projektledning och redovisningsparametrar**.</span><span class="sxs-lookup"><span data-stu-id="5658b-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="5658b-107">Stöd för projektförsäljningsorder med flera finansieringskällor kan startas med hjälp av programversionen 10.0.2 och senare.</span><span class="sxs-lookup"><span data-stu-id="5658b-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="5658b-108">Parametern för att aktivera stöd för projektförsäljningsorder med flera finansieringskällor tas bort i april 2020 utgivningsvåg, efter vilken funktionen alltid är aktiverad.</span><span class="sxs-lookup"><span data-stu-id="5658b-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="5658b-109">Du kan skapa projektbaserade försäljningsorder på två sätt:</span><span class="sxs-lookup"><span data-stu-id="5658b-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="5658b-110">Gå till själva projektet.</span><span class="sxs-lookup"><span data-stu-id="5658b-110">Go to the project itself.</span></span> <span data-ttu-id="5658b-111">I åtgärdsrutan väljer du **hantera > artikeluppgifter > försäljningsorder**.</span><span class="sxs-lookup"><span data-stu-id="5658b-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="5658b-112">Projektinformationen används som standard för försäljningsordern från projektet.</span><span class="sxs-lookup"><span data-stu-id="5658b-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="5658b-113">Om projektkontraktet har fler än en finansieringskälla måste du välja finansieringskällan för att ange kunden för försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="5658b-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="5658b-114">Om det bara finns en finansieringskälla för projektet kommer kunden att ställas in automatiskt.</span><span class="sxs-lookup"><span data-stu-id="5658b-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="5658b-115">Gå till listsidan **Alla försäljningsorder** och skapa en ny försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="5658b-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="5658b-116">Du måste välja projektet för försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="5658b-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="5658b-117">När du har valt projektet kommer kunden att ställas in från finansieringskällan, eller så måste du välja finansieringskälla om projektkontraktet har flera finansieringskällor.</span><span class="sxs-lookup"><span data-stu-id="5658b-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

