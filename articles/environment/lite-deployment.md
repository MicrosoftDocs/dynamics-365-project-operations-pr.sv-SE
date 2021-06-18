---
title: Distribuera Project Operations – Lite
description: I det här ämnet finns information om hur du installerar Project Operations enkel distribution – avtal till proforma-fakturering.
author: stsporen
ms.date: 10/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb1f1ad86e19d84d68a40b32b2fdb08dc4777a78
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995553"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="8f2f1-103">Distribuera Project Operations – Lite</span><span class="sxs-lookup"><span data-stu-id="8f2f1-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="8f2f1-104">_**Gäller:** Enkel distribution – avtal till proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="8f2f1-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8f2f1-105">Project Operations har stöd för flera distributionsmodeller.</span><span class="sxs-lookup"><span data-stu-id="8f2f1-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="8f2f1-106">Information om hur du fastställer den bästa distributionsmodellen finns i [Distributionstyper](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="8f2f1-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="8f2f1-107">Den här distributionen, Enkel distribution – avtal till proforma-fakturering, resulterar i en **Common Data Service-distribution av Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="8f2f1-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="8f2f1-108">Installera Project Operations i en ny CDS-miljö</span><span class="sxs-lookup"><span data-stu-id="8f2f1-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="8f2f1-109">Installera i en befintlig CDS-miljö</span><span class="sxs-lookup"><span data-stu-id="8f2f1-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="8f2f1-110">Installera Project Operations i en ny CDS-miljö</span><span class="sxs-lookup"><span data-stu-id="8f2f1-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="8f2f1-111">Som [Global eller Power Platform-administratör](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-licens skapar du en ny CDS-miljö i [PowerPlatforms administratörscenter](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="8f2f1-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="8f2f1-112">Kontrollera att **CDS-databasen** och **Dynamics 365-apparna** är aktiverade.</span><span class="sxs-lookup"><span data-stu-id="8f2f1-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="8f2f1-113">Mer information finns i [Skapa och hantera miljöer i Power Platforms administratörscenter](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="8f2f1-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="8f2f1-114">Välj **Microsoft Dynamics 365 Project Operations** i distributionslistan för Dynamics 365-appar.</span><span class="sxs-lookup"><span data-stu-id="8f2f1-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="8f2f1-115">Installera Project Operations i en befintlig CDS-miljö</span><span class="sxs-lookup"><span data-stu-id="8f2f1-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="8f2f1-116">Som [Global eller Power Platform-administratör](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-licens letar du upp miljön i [PowerPlatforms administratörscenter](https://admin.powerplatform.com) där du vill installera Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8f2f1-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="8f2f1-117">Installera **Microsoft Dynamics 365 Project Operations** i distributionslistan för Dynamics 365-appar.</span><span class="sxs-lookup"><span data-stu-id="8f2f1-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="8f2f1-118">Mer information finns i [Hantera Dynamics 365-appar](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="8f2f1-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]