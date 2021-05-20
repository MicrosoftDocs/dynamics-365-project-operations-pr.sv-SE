---
title: Rapportera startsida
description: I det här ämnet finns information om rapportering i Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 32b504a862f98dac4b1d9b54289476026d988c13
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951501"
---
# <a name="reporting-home-page"></a><span data-ttu-id="86c5e-103">Startsida för rapportering</span><span class="sxs-lookup"><span data-stu-id="86c5e-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="86c5e-104">Microsoft Dynamics 365 Project Service Automation låter projektbaserade organisationer effektivt hantera verksamheten i företaget.</span><span class="sxs-lookup"><span data-stu-id="86c5e-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="86c5e-105">I ett projekt måste teammedlemmarna hantera affärsmöjligheten, göra offerter och planera arbetet, dela projekten, hantera arbetet enligt planen, fakturera för arbetet och sedan utföra arbetet för att slutföra projektet.</span><span class="sxs-lookup"><span data-stu-id="86c5e-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="86c5e-106">Förmågan att rapportera verksamheten är en viktig faktor för att fastställa organisationens hälsostatus och vidta de åtgärder som krävs.</span><span class="sxs-lookup"><span data-stu-id="86c5e-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="86c5e-107">PSA använder Microsoft Dynamics 365 rapporteringsmetoder och tekniker för samtliga rapporter.</span><span class="sxs-lookup"><span data-stu-id="86c5e-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="86c5e-108">Mer information om alternativen för rapportering finns i [rapporteringshandboken för Dynamics 365 Customer Engagement (on-premises) version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="86c5e-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="86c5e-109">Rapportguiden</span><span class="sxs-lookup"><span data-stu-id="86c5e-109">Report Wizard</span></span>

<span data-ttu-id="86c5e-110">Rapportguiden låter icke-utvecklare skapa enkla rapporter.</span><span class="sxs-lookup"><span data-stu-id="86c5e-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="86c5e-111">Eftersom appen bygger på en befintlig plattform är upplevelsen densamma som den erfarenhet som är dokumenterad i [skapa eller redigera en rapport med rapportguiden](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="86c5e-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="86c5e-112">Du ska emellertid använda Project Service Automation-specifika entiteter.</span><span class="sxs-lookup"><span data-stu-id="86c5e-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="86c5e-113">Anpassa SQL Server Reporting Services-rapporter</span><span class="sxs-lookup"><span data-stu-id="86c5e-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="86c5e-114">Om det krävs en specifik rapport i företaget som inte kan skapas med rapportguiden kan du skapa en anpassad rapport.</span><span class="sxs-lookup"><span data-stu-id="86c5e-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="86c5e-115">Du måste ha Microsoft Visual Studio installerat tillsammans med lämpliga Microsoft SQL Server Data Tools och rapportredigeringstillägg.</span><span class="sxs-lookup"><span data-stu-id="86c5e-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="86c5e-116">Mer information om verktyg och versioner finns i [Rapportskrivningsmiljö med hjälp SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools)av.</span><span class="sxs-lookup"><span data-stu-id="86c5e-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="86c5e-117">Information om hur du skapar en anpassad rapport finns i [skapa en ny rapport med SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools)</span><span class="sxs-lookup"><span data-stu-id="86c5e-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="86c5e-118">Power BI-insiktsappar</span><span class="sxs-lookup"><span data-stu-id="86c5e-118">Power BI insights apps</span></span>

<span data-ttu-id="86c5e-119">Tillsammans får Microsoft Power BI och Dynamics 365 ett kraftfullt sätt att arbeta med dina data i form av Insights-appar.</span><span class="sxs-lookup"><span data-stu-id="86c5e-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="86c5e-120">Mer information om hur du kan få till gång till insiktsappar finns i [Sidan Power BI insiktsappar](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="86c5e-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="86c5e-121">Ytterligare resurser</span><span class="sxs-lookup"><span data-stu-id="86c5e-121">Additional resources</span></span>
<span data-ttu-id="86c5e-122">Mer information om rapportering i PSA finns i följande avsnitt:</span><span class="sxs-lookup"><span data-stu-id="86c5e-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="86c5e-123">Arbeta med datamodellen Project Service</span><span class="sxs-lookup"><span data-stu-id="86c5e-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="86c5e-124">Instrumentpaneler</span><span class="sxs-lookup"><span data-stu-id="86c5e-124">Dashboards</span></span>](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]