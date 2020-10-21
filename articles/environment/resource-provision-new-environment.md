---
title: Etablera en ny miljö
description: I det här ämnet finns information om hur du etablerar en ny Project Operations-miljö.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949384"
---
# <a name="provision-a-new-environment"></a>Etablera en ny miljö

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

I den här ämne finns information om hur du etablerar en ny Dynamics 365 Project Operations-miljö för resursbaserade/icke lagerbaserade scenarier.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Aktivera automatisk etablering av Project Operations i ett LCS-projekt

Följ stegen nedan om du vill aktivera det automatiska etableringsflödet för Project Operations för ditt LCS-projekt.

1. Gå till [LCS](https://lcs.dynamics.com/v2) och välj ikonen **Hantering av förhandsgranskningsfunktion**.
2. I listan **Förhandsgranskningsfunktion** väljer du **Project Operations** och sedan **Förhandsgranskningsfunktion aktiverad** för att aktivera Project Operations.

> [!NOTE]
> Det här steget utförs endast en gång per LCS-projekt.

## <a name="provision-a-project-operations-environment"></a>Etablera en Project Operations-miljö

1. Öppna en ny Dynamics 365 Finance [demomiljö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) eller [sandbox-miljö/produktionsmiljö](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) distribution. 
2. Gå igenom guiden **Miljöetablering**. 

> [!IMPORTANT]
> Kontrollera att den valda programversionen är 10.0.13 eller senare.

3. Om du vill etablera Project Operations väljer du, under **Avancerade inställningar**, **Common Data Service**. 
4. Aktivera **Common Data Service-inställningen** genom att välja **Ja** och sedan ange information i de obligatoriska fälten:

  - Namn
  - Region
  - Språk
  - Valuta
 
5. I fältet **Common Data Service-mall** väljer du **Project Operations** 

6. Välj miljötypen för din distribution. Med en prenumerationsbaserad utvärderingsversion kan du distribuera en CDS-miljö i 30 dagar. 

![Distributionsinställningar](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Välj **Godkänn** för att bekräfta tjänstvillkoren och välj sedan **Klar** för att återgå till distributionsinställningarna.

![Distributionsmedgivande](./media/2DeploymentConsent.png)

7. Fyll i de återstående obligatoriska fälten i guiden och bekräfta distributionen. Hur lång tid det tar att etablera miljön varierar beroende på miljötypen. Etableringen kan ta upp till sex timmar.

  När distributionen har slutförts visas miljön som **Distribuerad**.

8. Du bekräftar att miljön har distribuerats genom att välja **Logga in** och sedan logga in på miljön.

![ miljöinformation](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Tillämpa Project Operations Finance-demodata (valfritt steg)

Tillämpa Project Operations Finance-demodata till 10.0.13-tjänstutgåvan av molnbaserad miljö enligt beskrivningen i [den här artikeln](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Tillämpa uppdateringar av Finance-miljön

Project Operations kräver en Finance-miljö med programversion **10.0.13 (10.0.569.20009)** eller senare.

Du kan behöva tillämpa kvalitetsuppdateringar av Finance-miljön för att få den här versionen.

1. I LCS, på sidan **Miljöinformation**, i avsnittet **Tillgängliga uppdateringar**, väljer du **Visa uppdatering**.

![Visa uppdateringar](./media/5ViewUpdates.png)

2. På sidan **Binära uppdateringar** väljer du **Spara paket.**

![Spara paket](./media/6SavePackage.png)

3. Klicka på **Välj alla** och välj sedan **Spara paket**.

![Granska och spara uppdateringar](./media/7ReviewAndSaveUpdates.png)

4. Ange ett namn och en beskrivning för paketet och välj sedan **Spara**. Beroende på vilken internetanslutning du har kan processen ta lite tid.

![Ladda upp paket till resursbiblioteket](./media/8UploadPackageToAssetsLibrary.png)

5. När paketet har sparats väljer du **Klart** och sparar det här paketet i resursbiblioteket i LCS-projektet.

Det kan ta ~ 15 minuter att spara och verifiera paketet.

6. Om du vill tillämpa uppdateringen navigerar du till sidan **Miljöinformation** i LCS och väljer **Upprätthåll** > **Tillämpa uppdateringar**.

![Upprätthåll miljöer](./media/9MaintainEnvironment.png)

7. Välj det paket du skapade i listan med uppdateringar och välj **Tillämpa**.

![Tillämpa uppdateringar](./media/10ApplyUpdates.png)

Miljöunderhållet tar lite tid. När det är klart kommer miljön att återgå till ett distribuerat tillstånd.

![Miljö distribuerad](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Upprätta en anslutning med dubbelskrivning 

1. I ditt LCS-projekt går du till sidan **Miljöinformation**.
2. Under **Information om Common Data Service-miljö** väljer du **Länk till CDS for Apps**.
3. När länken är klar väljer du **Länk till CDS for Apps** igen. Du omdirigeras då till dubbelskrivning i Finance.

![Länk till CDS](./media/12LinktoCDS.png)

4. Välj **Tillämpa lösning** för att komma åt de entiteter som ska mappas i integrationen.

![Tillämpa lösningar](./media/13ApplySolutions.png)

5. Välj båda lösningarna, **Dynamics 365 Finance and Operations Dual Write Entity Map** och **Dynamics 365 Project Operations Dual Write Entity Maps**, och välj sedan **Tillämpa**.

![Bekräfta lösningar](./media/14ConfirmSolutions.png)

När lösningarna har tillämpats tillämpas entiteterna med dubbelskrivning i miljön.

![Tillämpa lösningar](./media/15ApplyingSolutions.png)

När entiteterna har tillämpats visas alla tillgängliga mappningar i miljön.

![Kartor dubbelskrivning](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Uppdatera dataentiteterna efter uppdateringen

1. I Finance går du till arbetsytan **Datahantering**.

![Datahantering arbetsyta](./media/16DataManagement.png)

2. Välj ikonen **Ramverksparametrar**.

![Ramverksparametrar](./media/17FrameworkParameters.png)

3. På sidan **Entitetsinställningar** väljer du **Uppdatera entitetslista**.

![Uppdatera entitetslista](./media/18RefreshEntityList.png)

Uppdateringen ska ta cirka 20 minuter. Du kommer att få en avisering när den är klar.

![Uppdateringsbekräftelse](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Kör kartor för dubbelskrivning i Project Operations

1. I ditt LCS-projekt går du till sidan **Miljöinformation**.
2. Under **Information om Common Data Service-miljö** väljer du **Länk till CDS for Apps.** När du har valt länken dirigeras du om till listan över entiteter i mappningarna.
3. Starta kartorna enligt beskrivningen i följande tabell. Kontrollera att du följer sekvensen enligt anvisningarna nedan.

| **Entitetsmappning** | **Uppdatera entitet** | **Initial synkronisering** | **Huvud för initial synkronisering** | **Kör förutsättningar** | **Förutsättningar initial synkronisering** |
| --- | --- | --- | --- | --- | --- |
| **Projektresursroller för alla företag (bookableresourcecategories)** | Inga | Ja | Common Data Service | Inga | N\A |
| **Juridiska personer (cdm\_companies)** | Inga | Ja | Finance and Operations-appar | Inga | N\A |
| **Verkliga värden för Project Operations-integrering (msdyn\_actuals)** | Inga | Inga | N\A | Ja | Inga |
| **Projektkontraktrader (salesorderdetails)** | Inga | Inga | N\A | Inga | Inga |
| **Integrationsentitet för projekttransaktionsrelationer (msdyn\_transactionconnections)** | Inga | Inga | N\A | Inga | N\A |
| **Milstolpar för kontraktrad för Project Operations-integration (msdyn\_contractlinesscheduleofvalues)** | Inga | Inga | N\A | Inga | N\A |
| **Entitet för Project Operations-integration för utgiftsuppskattningar (msdyn\_estimateslines)** | Inga | Inga | N\A | Inga | N\A |
| **Entitet för Project Operations-integration för tidsuppskattningar (msdyn\_resourceassignments)** | Inga | Inga | N\A | Inga | N\A |
| **Entitet för export av projektutgifter i Project Operations-integration (msdyn\_expenses)** | Ja | Inga | N\A | Inga | N\A |
| **Entitet för Project Operations-integration för tidsuppskattningar (msdyn\_resourceassignments)** | Ja | Inga | N\A | Inga | N\A |

4. Om du vill uppdatera entiteten väljer du kartnamnet och väljer sedan **Uppdatera entiteter**. 
5. Fortsätt köra kartan efter att uppdateringen har slutförts.

![Uppdatera karta](./media/20RefreshMapping.png)

Innan du aktiverar nästa karta ska du kontrollera att kartan i tabellen är i tillståndet **Körs**. Det kan ta en stund att köra kartor med ett större antal förutsättningar.

Om du vill köra en karta med förutsättningar ska du aktivera **Visa relaterade entitetskartor**. Om tabellen anger att **Förutsättning initial synkronisering** är **Nej**, verifierar du att flaggan **Initial synkronisering** är **Av** i alla förutsättningskartor innan du kör den.

![Kör karta](./media/21RunMap.png)

6. Kontrollera att alla projektrelaterade kartor är i körläge.

![Alla kartor körs](./media/22AllMapsRunning.png)

Project Operations-miljön har nu etablerats och konfigurerats.
