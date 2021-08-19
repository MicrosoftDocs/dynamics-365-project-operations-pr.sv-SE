---
title: Rapportera startsida
description: I det här ämnet finns information om rapportering i Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
- intro-internal
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
ms.openlocfilehash: 4e60fc8c3788f4a2997d894e79d0d510d63209dd1570d79f1c43c2814d8ab819
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998303"
---
# <a name="reporting-home-page"></a>Startsida för rapportering

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 Project Service Automation låter projektbaserade organisationer effektivt hantera verksamheten i företaget. I ett projekt måste teammedlemmarna hantera affärsmöjligheten, göra offerter och planera arbetet, dela projekten, hantera arbetet enligt planen, fakturera för arbetet och sedan utföra arbetet för att slutföra projektet. Förmågan att rapportera verksamheten är en viktig faktor för att fastställa organisationens hälsostatus och vidta de åtgärder som krävs. PSA använder Microsoft Dynamics 365 rapporteringsmetoder och tekniker för samtliga rapporter. Mer information om alternativen för rapportering finns i [rapporteringshandboken för Dynamics 365 Customer Engagement (on-premises) version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).

## <a name="report-wizard"></a>Rapportguiden

Rapportguiden låter icke-utvecklare skapa enkla rapporter. Eftersom appen bygger på en befintlig plattform är upplevelsen densamma som den erfarenhet som är dokumenterad i [skapa eller redigera en rapport med rapportguiden](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard). Du ska emellertid använda Project Service Automation-specifika entiteter.

## <a name="custom-sql-server-reporting-services-reports"></a>Anpassa SQL Server Reporting Services-rapporter

Om det krävs en specifik rapport i företaget som inte kan skapas med rapportguiden kan du skapa en anpassad rapport. Du måste ha Microsoft Visual Studio installerat tillsammans med lämpliga Microsoft SQL Server Data Tools och rapportredigeringstillägg. Mer information om verktyg och versioner finns i [Rapportskrivningsmiljö med hjälp SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools)av. Information om hur du skapar en anpassad rapport finns i [skapa en ny rapport med SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools)

## <a name="power-bi-insights-apps"></a>Power BI-insiktsappar

Tillsammans får Microsoft Power BI och Dynamics 365 ett kraftfullt sätt att arbeta med dina data i form av Insights-appar. Mer information om hur du kan få till gång till insiktsappar finns i [Sidan Power BI insiktsappar](https://powerbi.microsoft.com/power-bi-insights-apps/).


## <a name="additional-resources"></a>Ytterligare resurser
Mer information om rapportering i PSA finns i följande avsnitt:

- [Arbeta med datamodellen Project Service](reports-working-project-service-data-model.md)
- [Instrumentpaneler](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]