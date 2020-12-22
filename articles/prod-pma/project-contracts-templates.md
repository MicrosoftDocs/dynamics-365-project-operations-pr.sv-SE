---
title: Synkronisera projektkontrakt och projekt direkt från Project Service Automation till Finance and Operations
description: I det här ämne beskrivs de mallar och underliggande uppgifter som används för att synkronisera projektkontrakt och projektet direkt från Microsoft Dynamics 365 Project Service Automation till Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0b3bc159fff25c4f6e5b1ed1b2eabbba675fb0f5
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642655"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Synkronisera projektkontrakt och projekt direkt från Project Service Automation till Finance and Operations

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I det här ämne beskrivs de mallar och underliggande uppgifter som används för att synkronisera projektkontrakt och projektet direkt från Dynamics 365 Project Service Automation till Dynamics 365 Finance.

> [!NOTE] 
> Om du använder Enterprise Edition 7.3.0 måste du installera KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflöde för Project Service Automation till Finance

> [!NOTE]
> Innan du kan använda integreringslösningen Project Service Automation till Finance bör du känna till data integreringsfunktionen i Dynamics 365.

Project Service Automation till Finance integreringslösning använder funktionen Dataintegrering feature för att synkronisera data över instanser av Project Service Automation och Finance. Integreringsmallen som är tillgänglig med funktionen Dataintegrering möjliggör flödet av data om projektkontrakt, projekt, projektkontraktsrader och milstolpar för projektkontrakt från Project Service Automation till Finance.

Följande illustration visar hur datasynkroniseras mellan Project Service Automation och Finance.

[![Dataflöde för Project Service Automation-integrering med Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Mallar och uppgifter

Om du vill öppna tillgängligare mallar går du till administrationscenter för Microsoft Power Apps och markerar **Projekt** i det övre högra hörnet välj **Nytt projekt** för att välja offentliga mallar.

Följande mallar och underliggande uppgifter som används för att synkronisera projektkontrakt och projekt från Project Service Automation till Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integrera med Dynamics 365 Project Service Automation v2.x
- **Namn på mallen i dataintegrering:** projekt och kontrakt (PSA till Fin and Ops)
- **Namn på uppgifterna i projektet:**

    - Projektkontrakt PSA till Fin and Ops
    - Projekt PSA till Fin and Ops
    - Projektkontraktrader PSA till Fin and Ops
    - Milstolpar för projektkontraktrad PSA till Fin and Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrera med Dynamics 365 Project Service Automation v3.x
Det finns en schemaförändring i Project Service Automation som påverkar mallen milstolpe för projektkontraktsrad och användning av v2-versionen av mallen krävs för att integrera Project Service Automation v3.x med Dynamics 365.

- **Namn på mallen i dataintegrering:** projekt och kontrakt (PSA 3.x till Fin and Ops) - v2
- **Namn på uppgifterna i projektet:**

    - Projektkontrakt PSA till Fin and Ops
    - Projekt PSA till Fin and Ops
    - Projektkontraktrader PSA till Fin and Ops
    - Milstolpar för projektkontraktrad PSA till Fin and Ops

Innan synkronisering av projektkontrakt och projekt kan ske måste du synkronisera konton.

## <a name="entity-set"></a>Entitetsuppsättning

| Project Service Automation       | Finance                                                |
|----------------------------------|--------------------------------------------------------|
| Ordrar                           | Integrationsentitet för projektkontrakt                |
| Projekt                         | Integrationsentitet för projekt                         |
| Orderrader                      | Integrationsentitet för projektkontraktrad           |
| Milstolpar för projektkontraktrad | Integrationsentitet för milstolpar för projektkontraktrad |

## <a name="entity-flow"></a>Entitetsflöde

Projektkontrakt hanteras i Project Service Automation och synkroniseras med att Finance som projektkontrakt. Som en del av integrationsmallen kan du ange integrationskällan som Finance för projektkontraktet.

Tids- och materialprojekt och fastprisprojekt hanteras i Project Service Automation och synkroniseras med Finance som projekt. Som en del av mallintegrationen kan du ange integrationskällan som Finance för projekt.

Projektkontraktrad hanteras i Project Service Automation och synkroniseras med att Finance som faktureringsregler för projektkontrakt. Om faktureringsmetoden skiljer sig från standardprojekttypen uppdaterar synkroniseringen projekttypen för kontraktradsprojektet och projektgruppen.

Milstolpar för projektkontraktrad hanteras i Project Service Automation och synkroniseras med att Finance som milstolpar för faktureringsregel för projektkontrakt.

## <a name="project-service-automation-to-finance-integration-solution"></a>Project Service Automation till Finance-integreringslösning

Fältet **Projekt kontrakts ID** är tillgängligt på sidan **Projektkontrakt**. Det här fältet har gjorts till en naturlig och unik nyckel som stöder integreringen.

När ett nytt projekt kontrakt skapas, om ett värde **Projektkontrakt-ID** inte redan finns, genereras det automatiskt med hjälp av en nummerserie. Värdet består av **ORD** följt av en stegvis nummersekvens och sedan ett suffix på sex tecken. Här följer ett exempel: **ORD-01022-Z4M9Q0**.

Fältet **Projektnummer** är tillgängligt på sidan **Projekt**. Det här fältet har gjorts till en naturlig och unik nyckel som stöder integreringen.

När ett nytt projekt skapas, om ett värde **Projektnummer** inte redan finns, genereras det automatiskt med hjälp av en nummerserie. Värdet består av **PRJ** följt av en stegvis nummersekvens och sedan ett suffix på sex tecken. Här följer ett exempel: **PRJ-01049-CCNID0**.

När integreringslösningen för Project Service Automation till Finance integrationslösning tillämpas, ett uppgraderingsskript ställer in fältet **Projektkontrakt-ID** för befintliga projektkontrakt och fältet **Projektnummer** för befintliga projekt i Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Krav och mappningsinställningar

- Innan synkronisering av projektkontrakt och projekt kan ske måste du synkronisera konton.
- I din anslutningsuppsättning lägger du till en fältmappning för integrationsnyckel för **msdyn\_organizationalunits** till **msdyn\_name \[namn\]**. Du kanske först måste lägga till ett projekt i anslutningsuppsättningen. Mer information finns i [integrera data i Common Data Service för appar](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- I din anslutningsuppsättning lägger du till en fältmappning för integrationsnyckel för **msdyn\_projekts** till **msdynce\_projectnumber \[projektnummer\]**. Du kanske först måste lägga till ett projekt i anslutningsuppsättningen. Mer information finns i [integrera data i Common Data Service för appar](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** för projektkontrakt och projekt kan uppdateras till ett annat värde eller tas bort från mappningen. Standardmallens värde är **Project Service Automation**.
- Mappningen **PaymentTerms** måste uppdateras så att den visar giltiga betalningsvillkor i en Finance. Du kan också ta bort mappningen från projektuppgiften. Standardvärdes mappning har standardvärden för demonstrationsdata. I följande tabell visas värdena i Project Service Automation.

    | Värde | Beskrivning   |
    |-------|---------------|
    | 1     | 30 dagar netto        |
    | 2     | 2% 10, 30 dagar netto |
    | 3     | 45 dagar netto        |
    | 4     | 60 dagar netto        |

## <a name="power-query"></a>Power Query

Du måste använda Microsoft Power Query för Excel för att filtrera data om följande villkor är uppfyllda:

- Du har försäljningsorder i Dynamics 365 Sales.
- Du har flera organisationsenheter i Project Service Automation och de här organisationsenheterna mappas till flera juridiska entiteter i Finance.

Om du måste använda Power Query följer du dessa riktlinjer:

- Mallen projekt och kontrakt (PSA till Fin and Ops) har ett standardfilter som endast innehåller försäljningsorder av typen **Arbetsobjekt (msdyn\_ordertype = 192350001)**. Filtret hjälper till att garantera att projektkontrakt inte skapas för försäljningsorder i Finance. Om du skapar en egen mall måste du lägga till filtret.
- Du måste skapa ett Power Query filter som endast innehåller de kontraktsorganisationer som ska synkroniseras till den juridiska personen i anslutningsuppsättningen för integrering. Projektkontrakt som du har med kontraktets organisationsenhet för Contoso US ska synkroniseras till USSI juridiska personen, men projektkontrakt som du har med organisationsenheten organisationsstruktur för Contoso Global ska synkroniseras med USMF juridiska personen. Om du inte lägger till filtret i din uppgiftsmappning synkroniseras alla projektkontrakt med den juridiska personen som har definierats för anslutningsuppsättningen oavsett organisationsenhet.

## <a name="template-mapping-in-data-integration"></a>Mallgrupp i dataintegrering

> [!NOTE] 
> Fälten **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, och **AddressZipCode** ingår inte i standardmappningen för projektkontrakt. Du kan lägga till mappningarna om du kräver att dessa data ska synkroniseras för projektkontrakt.
>
> Fältet **Beskrivning**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** och **ProjectType** ingår inte i standardmappningen för projekt. Du kan lägga till mappningarna om du kräver att dessa data ska synkroniseras för projekt.

I följande illustration visas exempel på hur du mappar malluppgifter i dataintegrering. Mappningen visar fältinformationen som ska synkroniseras från Project Service Automation till Finance.

[![Mappning av projektkontraktmall](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Mappning av projektmall](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Mappning av mall för projektkontraktrader](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Mappning av mall för milstolpe för projektkontraktrader](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Mappning av milstolpe för projektkontrakt i projekt och kontrakt (PSA 3.x till Dynamics) - v2 mall:

[![Mappning av milstolpe för projektkontraktrader med mall av version två](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
