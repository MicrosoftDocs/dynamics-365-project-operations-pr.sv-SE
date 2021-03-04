---
title: Ställ in och använd konfigurationsdata i Common Data Service
description: I det här ämnet finns information om hur du konfigurerar och tillämpar konfigurationsdata i Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642250"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Ställ in och använd konfigurationsdata i Common Data Service 

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Förutsättningar

Innan du börjar konfigurera data i Common Data Service (CDS) måste följande krav uppfyllas:

1.  Konfigurera en CDS-miljö och en Dynamics 365 Finance-miljö för Project Operations.
2.  Information om juridisk person från Dynamics 365 Finance delas med CDS-miljön. Detta innebär att entiteten **företag** i CDS-skivor har följande företagsposter:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Installationsinställning och konfigurationsdata

1. Hämta, avblockera och packa upp paketet [Inställnings- och konfigurationsdata](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Navigera till den uppackade mappen och kör den körbara filen *DataMigrationUtility*.
3. På sidan 1 i guiden Common Data Service Configuration Migration (CMT) väljer du **Importera data** och sedan **Fortsätt**.

![Configuration Migration](./media/1ConfigurationMigration.png)

4. På sidan 2 i guiden CMT väljer du **Microsoft 365** som **Distributionstyp**.
5. Markera kryssrutorna **Visa en lista över tillgängliga organisationer** och **Visa avancerat**.
6. Välj region för klientorganisationen, ange autentiseringsuppgifter och välj **Logga in**.

![Konfigurationsinloggning](./media/2ConfigurationSignin.png)

7. På sidan 3 väljer du den organisation som du vill importera demodata till i listan över organisationer i klientorganisationen och väljer **Logga in**.
8. På sidan 4 väljer du zip-filen *SampleSetupAndConfigData* från den uppackade mappen.

![Välj zip-fil](./media/3ZipFile.png)

![Välj en fil](./media/4SelectAFile.png)

9. När du har markerat zip-filen väljer du **Importera data**.

![Importera data](./media/5ImportData.png)

10. Importen körs i ungefär två–tio minuter beroende på nätverkets hastighet. När importen är klar stänger du guiden för CMT. 
11. Kontrollera om organisationen har data i följande 19 entiteter:

  - Valuta
  - Organisationsenhet
  - Kontaktperson
  - Momsgrupp
  - Kundgrupp
  - Enhet
  - Enhetsgrupp
  - Prislista
  - Prislista för projektparameter
  - Fakturafrekvens
  - Bokningsbar resurskategori
  - Transaktionskategori
  - Utgiftskategori
  - Pris för roll
  - Pris för transaktionskategori
  - Egenskap
  - Bokningsbar resurs
  - Association för bokningsbar resurskategori
  - Egenskap för bokningsbar resurs

![Slutför import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Uppdatera Project Operations-konfigurationer

1. Navigera till CE-miljön. Du hittar den genom att öppna [Power Platform-administratörscenter](https://admin.powerplatform.microsoft.com/environments), välja miljön och sedan välja **Öppna miljö**. 

![Öppna miljön](./media/7OpenEnvironment.png)

2. Gå till **Projekt** > **Resurser** och välj sedan **Ny** för att skapa en bokningsbar resurs för användaren.

![Bokningsbara resurser](./media/8BookableResources.png)

3. Under fliken **Allmänt** väljer du administratörsanvändare. Kontrollera att tidszonen överensstämmer med den som du befinner dig i. 

![Ny bokningsbar resurs](./media/9NewBookableResource.png)

4. Under fliken **Schemaläggning**, i fältet **Företag**, väljer du företaget **USPM** och sedan **Spara**. 

![Fliken Schemaläggning](./media/10SchedulingTab.png)

5. Välj fliken **Arbetstider**.  

![Arbetstider](./media/11WorkHours.png)

6. Dubbelklicka på ett värde i kalendern och välj **Redigera** > **Alla händelser i serien**. 

![Arbetskalender](./media/12WorkCalendar.png)

7. Ändra arbetstider till en åttatimmars arbetsdag, markera helger som lediga dagar och kontrollera att tidszonen överensstämmer med din. 
8. Välj **Spara och stäng**.

![Uppdatera kalender](./media/13UpdateCalendar.png)

9. Gå till **Inställningar** > **Kalender-mallar** och välj **Ny**.
 
 ![Kalendermallar](./media/14CalendarTemplates.png)
 
 10. Ange ett namn, välj den mallresurs som du har skapat och välj sedan **Spara**. 
 
 ![Spara kalendermall](./media/15SaveCalendarTemplate.png)
 
 11. Gå till **Parametrar** och dubbelklicka på posten. 
 
 ![Projektparametrar](./media/16ProjectParameters.png)
 
12. Uppdatera följande fält:

 - **Standardföretag**: USPM
 - **Standardorganisationsenhet**: Contoso Robotics Global
 - **Faktureringsfrekvens**: sjunde och sista dagen
 - **Arbetstidsmall**: ändra till den mall du skapade.

13. Välj **Spara**. 

![Uppdaterade projektparametrar](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]