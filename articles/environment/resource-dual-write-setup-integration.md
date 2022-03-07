---
title: Inställning och konfiguration av Project Operations för dataintegration
description: Avsnittet innehåller information om hur du ställer in och konfigurerar Project Operations-mappningar med dubbelriktad skrivning.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d263f7c5ef0d562edde6a603340a3b8746195df190fdb527bfa40297f68eed2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986558"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Inställning och konfiguration av Project Operations för dataintegration

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Detta avsnitt innehåller information om Project Operations-integration med dubbelriktad skrivning för inställnings- och konfigurationsentiteter.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektkontrakt, kontraktrader och projekt

Projektkontrakt, kontraktrader och projekt skapas i Dataverse och synkroniseras med Finance and Operations-appar för ytterligare redovisning. Posterna i entiteterna kan endast skapas och raderas i Dataverse. Däremot kan redovisningsattribut som standardvärden för momsgrupp och ekonomiska mått läggas till för dessa poster i Finance and Operations-apparna.

  ![Begrepp för projektkontraktintegration.](./media/1ProjectContract.jpg)

Leads, affärsmöjligheter och offerter från försäljningsaktiviteter spåras i Dataverse och synkroniseras inte med Finance and Operations-appar eftersom det inte finns någon redovisning nedströms som är associerad med aktiviteten.

Projektkontraktfunktionen i Dataverse skapar en projektkontraktpost i Finance and Operations-appar med tabellmappningen **Projektkontraktrubriker (salesorders)**. När du sparar ett projektkontrakt i Dataverse skapas också en kundentitetspost för projektkontraktet. Posten synkroniseras med Finance and Operations-apparna med hjälp av tabellmappningen **Projektfinansieringskälla (msdyn\_projectcontractssplitbillingrules)**. Mappningen synkroniserar även projektkontraktets kundtillägg, -uppdateringar och -raderingar. Dela upp faktureringsprocenten mellan projektkontraktskunder kan endast göras i Dataverse och synkroniseras inte med Finance and Operations-appar.

När ett projektkontrakt har skapats i Dataverse kan projektredovisaren uppdatera redovisningsattributen för projektkontraktet i Finance and Operations-appar genom att gå till **Projektledning och redovisning** >  **Projektkontrakt**  > **Ställ in** > **Visa standardredovisning**. Redovisaren kan granska projektkontraktattribut som används, som begärt leveransdatum och kontraktsumma, genom att välja projektkontrakt-ID i Finance and Operations-appar som öppnar relaterad projektkontraktpost i Dataverse.

Projektentiteten synkroniseras med Finance and Operations-appar med tabellmappningen **Projekt V2 (msdyn\_projects)**. Projektredovisaren kan:

  - Granska projekt i Finance and Operations-appar genom att gå till **Projektledning och redovisning** > **Alla projekt**. 
  - Uppdatera redovisningsattribut för projektet i Finance and Operations-appar genom att gå till **Projektledning och redovisning** > **Alla projekt** > **Ställ in** > **Visa standardredovisning**.  
  - Granska projektattribut som används, som beräknade start- och slutdatum, genom att välja projekt-ID i Finance and Operations-apparna som öppnar den relaterade projektposten i Dataverse.

Ett projekt associeras med ett projektkontrakt via entiteten **Projektkontraktrad**.

Projektkontraktrader i Dataverse skapar en projektkontraktfaktureringsregel i Finance and Operations-appar med tabellmappningen **Projektkontraktrader (salesorderdetails)**. Faktureringsmetoden definierar projektfaktureringsregeltypen i Finance and Operations-appar:

  - Projektkontraktrader med en faktureringsmetod för tid och material skapar en faktureringsregel för tid och materialtyp.
  - Kontraktrader med fastprisfaktureringsmetod skapar en milstolpesfaktureringsregel.

Projektkontraktrader kan granskas av projektredovisaren i Finance and Operations-appar genom att gå till **Projektledning och redovisning** > **Projektkontrakt** > **Ställ in** > **Visa standardredovisning** och granska informationen på fliken **Kontraktrader**. Redovisaren kan även ställa in förvalda ekonomiska mått för kontraktraderna med fastprisfaktureringsmetod på denna flik.

## <a name="billing-milestones"></a>Faktureringsmilstolpar

Projektkontraktrader med fastprisfaktureringsmetod faktureras via faktureringsmilstolpar. Faktureringsmilstolpar synkroniseras med projekt vid kontotransaktioner i Finance and Operations-appar med tabellmappningen **Kontraktradmilstolpar för Project Operations-integration (msdyn\_contractlinescheduleofvalues)**.

  ![Integration av faktureringsmilstolpar.](./media/2Milestones.jpg)

Redovisaren kan granska kontotransaktioner och justera redovisningsattribut för dessa transaktioner genom att gå till **Projektledning och redovisning** > **Projektkontrakt** > **Underhåll** > **Kontotransaktioner** eller **Projektledning och redovisning** > **Alla projekt** > **Underhåll** > **Kontotransaktioner**.

När du först skapar en faktureringsmilstolpe för en viss projektkontraktrad skapar systemet automatiskt en intäktsberäkning för fastprisprojekt för projektet som är associerat med kontraktraden. Du kan granska intäktsberäkningar för fastprisprojekt genom att gå till **Projektledning och redovisning** > **Intäktsberäkning för fastprisprojekt**.

### <a name="project-tasks"></a>Projektuppgifter

Projektuppgifter synkroniseras med Finance and Operations-appar via tabellmappningen **Projektuppgifter (msdyn\_projecttasks)** enbart som referens. Åtgärder för att skapa, uppdatera och radera stöds inte i Finance and Operations-appar.

  ![Integration med projektuppgifter.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektresurser

Entiteten **Projektresursroller** synkroniseras med Finance and Operations-appar med tabellmappningen **Projektresursroller för alla företag (bookableresourcecategories)** enbart som referens. Eftersom resursroller i Dataverse inte är företagsspecifika skapar systemet automatiskt motsvarande företagsspecifika resursrollposter i Finance and Operations-apparna för alla juridiska entiteter som ingår i integrationen för dubbelriktad skrivning.

![Integration av resursroller.](./media/5Resources.jpg)

Projektresurser i Project Operations underhålls i Dataverse och synkroniseras inte med Finance and Operations-appar.

### <a name="transaction-categories"></a>Transaktionskategorier

Transaktionskategorier underhålls i Dataverse och synkroniseras med Finance and Operations-appar med tabellmappningen **Projekttransaktionskategorier (msdyn\_transactioncategories)**. När posten för transaktionskategorin har synkroniserats skapas fyra poster för delad kategori automatiskt i systemet. Varje post motsvarar en transaktionstyp i Finance and Operations-appar och länkar dem till transaktionskategoriposten.

![Integration av transaktionskategorier.](./media/4TransactionCategories.jpg)

För att använda transaktionskategorier för beräkningar och faktiska värden krävs att projektredovisaren eller systemadministratören skapar motsvarande projektkategorier i alla juridiska entiteter. Mer information finns i [Konfigurera projektkategorier](../project-accounting/configure-project-categories.md).
