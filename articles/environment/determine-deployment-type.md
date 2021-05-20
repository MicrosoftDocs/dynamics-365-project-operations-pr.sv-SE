---
title: Fastställa din distributionstyp
description: I det här ämnet finns information som gör det lättare för dig att fastställa korrekt distributionstyp av Project Operations för ditt företag.
author: stsporen
manager: Annbe
ms.date: 03/15/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1aae04230104d27db2f62db8e674697fd83460ac
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948143"
---
# <a name="determine-your-deployment-type"></a>Fastställa din distributionstyp

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

> [!IMPORTANT]
> När du har köpt licensen, börja här för att bestämma den bästa distributionsmodellen för Dynamics 365 Project Operations med [Guidat installationsflöde](https://aka.ms/provisionprojectoperations).
> När du har slutfört flödet i den guidade installationen dirigeras du till rätt hanteringsportal för att slutföra installationen. Se distributionsinformationen för att slutföra installationen.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Befintliga kunder av Dynamics som använder Dynamics 365 Project Service Automation
Project Operations inkluderar de funktioner som levererades med Project Service Automation. En uppgraderingssökväg kommer att ges ut för dessa kunder i 2021 utgivningscykel 1.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Befintliga kunder av Dynamics 365 Finance som använder projekthantering och redovisning 

Befintliga kunder av finans Finance som använder funktionerna för projektledning och redovisning kan fortsätta att använda dem som de är. Se [Project Operations för lagerbaserade/produktionsorderbaserade scenarier](#pma).


## <a name="deployment-regions"></a>Distributionsregioner
För att avgöra vilka regioner som stöder distribution av Project Operations, se [Geografisk tillgänglighet för Dynamics 365 och Power Platform rapport](https://dynamics.microsoft.com/en-us/geographic-availability/). Välj **Visa rapport** och expandera **Dynamics 365 > Operations-appar > Dynamics 365 Project Operations** för att visa de regioner som stöds visas.

## <a name="deployment-types"></a>Distributionstyper
Project Operations har stöd för flera distributionsalternativ för att uppfylla dina krav. Oavsett om du är en ny eller befintlig Dynamics 365-kund kan Project Operations tillgodose dina behov.

Vår [distributionsenkät](https://aka.ms/provisionprojectoperations) hjälper dig att fastställa rätt distribution. Resultatet vägleder dig mot någon av följande distributionstyper:

- [Mindre distribution – avtal till proforma-fakturering](#lite)
- [Project Operations för resursscenarier/icke lagerbaserade scenarier](#integrated)
- [Project Operations för lagerbaserade/produktionsorderbaserade scenarier](#pma)

Project Operations har stöd för lagerbaserade/produktionsorderbaserade scenarier och icke lagerbaserade/resursbaserade scenarier i samma miljö via konfigurationer på en juridisk enhetsnivå. Kan till exempel, Contoso kan använda lager-/produktionsorderfunktionerna i deras tillverkningsanläggning i USA (juridisk entitet = Contoso tillverkning USA). Contoso kan använda den icke-lagerförda/resursbaserade kapaciteten i Contoso sin robotteknikarm serviceanläggning i Storbritannien (Juridisk entitet = Contoso Robotteknik Storbritannien).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Lite-distribution – avtal till proforma-fakturering

Den enkla distributionen omfattar följande funktioner:

- Försäljningsprocess för projekt som utökar Dynamics 365 Sales-appupplevelser
- Planera projekt med hjälp av Microsoft Project för webben
- Flerdimensionell prissättning
- Enhetlig resurshantering
- Tidsspårning
- Grundläggande utgift
- Proforma-fakturering för projektledarens granskning och redigeringar 

#### <a name="deployment-steps"></a>Instruktioner för distribution
Bestäm den bästa distributionsmodellen för Project Operations med hjälp av [distributionsenkäten](https://aka.ms/provisionprojectoperations).

Om du vill använda distributionen läser du [Registrera dig för förhandsversionsprenumeration](lite-preview-subscription-sign-up.md) och [Etablera en ny miljö](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations för resursscenarier/icke lagerbaserade scenarier
Project Operations för resursbaserade/icke lagerbaserade scenarier omfattar följande funktioner:
 
- Försäljningsprocess för projekt som utökar Dynamics 365 Sales-app
- Planera projekt med hjälp av Microsoft Project för webben
- Flerdimensionell prissättning
- Enhetlig resurshantering
- Tidsspårning
- Grundläggande utgift
- Fullständig utgift
- OCR på kvitto
- Proforma och kundorienterade fakturering 
- Intäktsredovisning för projekt

#### <a name="deployment-steps"></a>Instruktioner för distribution
Bestäm den bästa distributionsmodellen för Project Operations med hjälp av [distributionsenkäten](https://aka.ms/provisionprojectoperations).

Om du vill använda distributionen läser du [Registrera dig för förhandsversionsprenumeration](resource-sign-up-preview-subscription.md) och [Etablera en ny miljö](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations för lagerbaserade/produktionsorderbaserade scenarier

- Projektplanering med hjälp av WBS
- Resurshantering
- Tidsspårning
- Fullständig utgift
- OCR på kvitto
- Fullständig fakturering
- Intäktsredovisning
- Produktionsorder
- Stöd för lagermaterial med lager

#### <a name="deployment-steps"></a>Instruktioner för distribution
Bestäm den bästa distributionsmodellen för Project Operations med hjälp av [distributionsenkäten](https://aka.ms/provisionprojectoperations).

Om du vill använda distributionen läser du [Registrera dig för förhandsversionsprenumeration](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) och [Etablera en ny miljö](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]