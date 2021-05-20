---
title: Distribuera Project Operations – Lite
description: I det här ämnet finns information om hur du installerar Project Operations enkel distribution – avtal till proforma-fakturering.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2470d573f4537cb22de4dbd98caff148cbe0bda3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950286"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="64037-103">Distribuera Project Operations – Lite</span><span class="sxs-lookup"><span data-stu-id="64037-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="64037-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="64037-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="64037-105">Project Operations har stöd för flera distributionsmodeller.</span><span class="sxs-lookup"><span data-stu-id="64037-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="64037-106">Information om hur du fastställer den bästa distributionsmodellen finns i [Distributionstyper](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="64037-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="64037-107">Den här distributionen, Enkel distribution – avtal till proforma-fakturering, resulterar i en **Common Data Service-distribution av Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="64037-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="64037-108">Installera Project Operations i en ny CDS-miljö</span><span class="sxs-lookup"><span data-stu-id="64037-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="64037-109">Installera i en befintlig CDS-miljö</span><span class="sxs-lookup"><span data-stu-id="64037-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="64037-110">Installera Project Operations i en ny CDS-miljö</span><span class="sxs-lookup"><span data-stu-id="64037-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="64037-111">Som [Global eller Power Platform-administratör](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-licens skapar du en ny CDS-miljö i [PowerPlatforms administratörscenter](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="64037-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="64037-112">Kontrollera att **CDS-databasen** och **Dynamics 365-apparna** är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="64037-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="64037-113">Mer information finns i [Skapa och hantera miljöer i Power Platforms administratörscenter](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="64037-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="64037-114">Välj **Microsoft Dynamics 365 Project Operations** i distributionslistan för Dynamics 365-appar.</span><span class="sxs-lookup"><span data-stu-id="64037-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="64037-115">Installera Project Operations i en befintlig CDS-miljö</span><span class="sxs-lookup"><span data-stu-id="64037-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="64037-116">Som [Global eller Power Platform-administratör](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-licens letar du upp miljön i [PowerPlatforms administratörscenter](https://admin.powerplatform.com) där du vill installera Project Operations.</span><span class="sxs-lookup"><span data-stu-id="64037-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="64037-117">Installera **Microsoft Dynamics 365 Project Operations** i distributionslistan för Dynamics 365-appar.</span><span class="sxs-lookup"><span data-stu-id="64037-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="64037-118">Mer information finns i [Hantera Dynamics 365-appar](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="64037-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]