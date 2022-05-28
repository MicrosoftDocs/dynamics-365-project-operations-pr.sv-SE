---
title: Inställning och konfiguration av Project Operations för dataintegration
description: Avsnittet innehåller information om hur du ställer in och konfigurerar Project Operations-mappningar med dubbelriktad skrivning.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586918"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Inställning och konfiguration av Project Operations för dataintegration

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Detta avsnitt innehåller information om Project Operations-integration med dubbelriktad skrivning för inställnings- och konfigurationsentiteter.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektkontrakt, kontraktrader och projekt

Projektkontrakt, kontraktrader och projekt skapas i Dataverse och synkroniseras med apparna för ekonomi och drift för ytterligare redovisning. Posterna i entiteterna kan endast skapas och raderas i Dataverse. Däremot kan redovisningsattribut som standardvärden för momsgrupp och ekonomiska mått läggas till för dessa poster i apparna för ekonomi och drift.

  ![Begrepp för projektkontraktintegration.](./media/1ProjectContract.jpg)

Leads, affärsmöjligheter och offerter från försäljningsaktiviteter spåras i Dataverse och synkroniseras inte med appar för ekonomi och drift eftersom det inte finns någon associerad redovisning nedströms med aktiviteten.

Projektkontraktsfunktionen i Dataverse skapar en projektkontraktpost i appar för ekonomi och drift med hjälp av tabellmappningen **Huvud för projektkontrakt (försäljningsorder)**. När du sparar ett projektkontrakt i Dataverse skapas också en kundentitetspost för projektkontraktet. Den här posten synkroniseras med appar för ekonomi och drift med hjälp av tabellmappningen **Finansieringskälla för projekt (msdyn\_projectcontractssplitbillingrules)**. Mappningen synkroniserar även projektkontraktets kundtillägg, -uppdateringar och -raderingar. Att dela upp faktureringsprocenten mellan projektkontraktskunder sker endast i Dataverse och synkroniseras inte med apparna för ekonomi och drift.

När ett projektkontrakt skapats i Dataverse kan projektrevisorn uppdatera redovisningsattributen för detta projektkontrakt i appar för ekonomi och drift genom att gå till **Projekthantering och redovisning** > **Projektkontrakt** > **Inställningar** > **Visa standardredovisning**. Revisorerna kan granska projektkontraktsattribut för verksamhet, till exempel begärt leveransdatum och kontraktbelopp genom att välja projektkontrakt-ID i appar för ekonomi och drift, som öppnar den relaterade projektkontraktposten i Dataverse.

Projektentiteten synkroniseras med appar för ekonomi och drift med hjälp av tabellmappningen **Projects V2 (msdyn\_projects**). Projektredovisaren kan:

  - Granska projekt i apparna för ekonomi och drift genom att gå till **Projekthantering och redovisning** > **Alla projekt**. 
  - Uppdatera redovisningsattribut för projektet i apparna för ekonomi och drift genom att gå till **Projekthantering och redovisning** > **Alla projekt** > **Inställningar** > **Visa standardredovisning**.  
  - Granska projektattribut för drift, till exempel beräknade start- och slutdatum, genom att välja projekt-ID:t i apparna för ekonomi och drift som öppnar den relaterade projektposten i Dataverse.

Ett projekt associeras med ett projektkontrakt via entiteten **Projektkontraktrad**.

Projektkontraktsrader i Dataverse skapar en faktureringsregel i projektkontrakt i appar för ekonomi och drift med hjälp av tabellmappningen **Projektkontraktrader (salesorderdetails)**. Faktureringsmetoden definierar faktureringsregeltypen för projektkontrakt i appar för ekonomi och drift:

  - Projektkontraktrader med en faktureringsmetod för tid och material skapar en faktureringsregel för tid och materialtyp.
  - Kontraktrader med fastprisfaktureringsmetod skapar en milstolpesfaktureringsregel.

Projektkontraktrader kan granskas av projektrevisorn i apparna för ekonomi och drift genom att gå till **Projekthantering och redovisning** > **Projektkontrakt** > **Inställningar** > **Visa standardredovisning** och granska informationen på fliken **Kontraktsrader**. Revisorn kan även ange ekonomiska standarddimensioner för kontraktsraderna för faktureringsmetoden för fast pris på denna flik.

## <a name="billing-milestones"></a>Faktureringsmilstolpar

Projektkontraktrader med fastprisfaktureringsmetod faktureras via faktureringsmilstolpar. Faktureringsmilstolpar synkroniseras till projekt för kontotransaktioner appar för ekonomi och drift genom att använda tabellmappningen **Kontraktsradmilstolpar för Project Operations-integrering (msdyn\_contractlinescheduleofvalues)**.

  ![Integration av faktureringsmilstolpar.](./media/2Milestones.jpg)

Redovisaren kan granska kontotransaktioner och justera redovisningsattribut för dessa transaktioner genom att gå till **Projektledning och redovisning** > **Projektkontrakt** > **Underhåll** > **Kontotransaktioner** eller **Projektledning och redovisning** > **Alla projekt** > **Underhåll** > **Kontotransaktioner**.

När du först skapar en faktureringsmilstolpe för en viss projektkontraktrad skapar systemet automatiskt en intäktsberäkning för fastprisprojekt för projektet som är associerat med kontraktraden. Du kan granska intäktsberäkningar för fastprisprojekt genom att gå till **Projektledning och redovisning** > **Intäktsberäkning för fastprisprojekt**.

### <a name="project-tasks"></a>Projektuppgifter

Projektuppgifter synkroniseras med appar för ekonomi och drift via tabellmappningen **Projektuppgifter (msdyn\_projecttasks)** endast i referenssyfte. Åtgärder för att skapa, uppdatera och ta bort åtgärder stöds inte via apparna för ekonomi och drift.

  ![Integration med projektuppgifter.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektresurser

Entiteten **Roller för projektresurs** synkroniseras med appar för ekonomi och drift med hjälp av tabellmappningen **Projektresursroller för alla företag (bookableresourcecategories)** endast i referenssyfte. Eftersom resursroller i Dataverse inte är företagsspecifika skapas automatiskt poster för företagsspecifika resursroller i appar för ekonomi och drift för alla juridiska entiteter som ingår i integreringsomfånget med dubbelskrivning.

![Integration av resursroller.](./media/5Resources.jpg)

Projektresurser i Project Operations upprätthålls i Dataverse och synkroniseras inte med apparna för ekonomi och drift.

### <a name="transaction-categories"></a>Transaktionskategorier

Transaktionskategorier upprätthålls i Dataverse och synkroniseras med appar för ekonomi och drift med hjälp av tabellmappningen **Projekttransaktionskategorier (msdyn\_transactioncategories**). När posten för transaktionskategorin har synkroniserats skapas fyra poster för delad kategori automatiskt i systemet. Varje post motsvarar en transaktionstyp i apaprna för ekonomi och drift och länkar dem till posten för transaktionskategori.

![Integration av transaktionskategorier.](./media/4TransactionCategories.jpg)

För att använda transaktionskategorier för beräkningar och faktiska värden krävs att projektredovisaren eller systemadministratören skapar motsvarande projektkategorier i alla juridiska entiteter. Mer information finns i [Konfigurera projektkategorier](../project-accounting/configure-project-categories.md).
