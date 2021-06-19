---
title: Projektförsäljningsorder för tids- och materialprojekt
description: I det här ämnet beskrivs hur du skapar projektbaserade försäljningsorder för tids- och materialprojekt.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009683"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="11992-103">Projektförsäljningsorder för tids- och materialprojekt</span><span class="sxs-lookup"><span data-stu-id="11992-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="11992-104">I den här ämnet beskrivs hur du skapar en försäljningsorder för ett projekt.</span><span class="sxs-lookup"><span data-stu-id="11992-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="11992-105">Det går endast att skapa försäljningsorder för projekt av typen **tid och material**.</span><span class="sxs-lookup"><span data-stu-id="11992-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="11992-106">Om ett tids- och materialprojekt har flera finansieringskällor i projektkontraktet måste du aktivera parametern **Tillåt försäljningsorder för projekt med flera finansieringskällor** på sidan **Projektledning och redovisningsparametrar**.</span><span class="sxs-lookup"><span data-stu-id="11992-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="11992-107">Stöd för projektförsäljningsorder med flera finansieringskällor kan startas med hjälp av programversionen 10.0.2 och senare.</span><span class="sxs-lookup"><span data-stu-id="11992-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="11992-108">Parametern för att aktivera stöd för projektförsäljningsorder med flera finansieringskällor tas bort i april 2020 utgivningsvåg, efter vilken funktionen alltid är aktiverad.</span><span class="sxs-lookup"><span data-stu-id="11992-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="11992-109">Du kan skapa projektbaserade försäljningsorder på två sätt:</span><span class="sxs-lookup"><span data-stu-id="11992-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="11992-110">Gå till själva projektet.</span><span class="sxs-lookup"><span data-stu-id="11992-110">Go to the project itself.</span></span> <span data-ttu-id="11992-111">I åtgärdsrutan väljer du **hantera > artikeluppgifter > försäljningsorder**.</span><span class="sxs-lookup"><span data-stu-id="11992-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="11992-112">Projektinformationen används som standard för försäljningsordern från projektet.</span><span class="sxs-lookup"><span data-stu-id="11992-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="11992-113">Om projektkontraktet har fler än en finansieringskälla måste du välja finansieringskällan för att ange kunden för försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="11992-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="11992-114">Om det bara finns en finansieringskälla för projektet kommer kunden att ställas in automatiskt.</span><span class="sxs-lookup"><span data-stu-id="11992-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="11992-115">Gå till listsidan **Alla försäljningsorder** och skapa en ny försäljningsorder.</span><span class="sxs-lookup"><span data-stu-id="11992-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="11992-116">Du måste välja projektet för försäljningsordern.</span><span class="sxs-lookup"><span data-stu-id="11992-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="11992-117">När du har valt projektet kommer kunden att ställas in från finansieringskällan, eller så måste du välja finansieringskälla om projektkontraktet har flera finansieringskällor.</span><span class="sxs-lookup"><span data-stu-id="11992-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]