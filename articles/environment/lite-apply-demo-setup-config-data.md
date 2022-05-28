---
title: Använda demoinställning och konfigurationsdata – Lite
description: I det här ämnet finns information om hur du tillämpar demoinställning konfigurationsdata i Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ecb5da3bccf35f8ed7e2246f68dd4da2b145c6be
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587010"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Använda demoinställning och konfigurationsdata Project Operations - Lite 

_**Lite-distribution – avtal till proforma-fakturering_



## <a name="prerequisites"></a>Förutsättningar

Innan du påbörjar konfigurationen måste du ha installerat en Common Data Service (CDS)-miljö för Dynamics 365 Project Operations.


## <a name="instructions"></a>Anvisningar

1. Hämta [Huvuddatapaketet](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Navigera till mappen *ProjOpsSampleSetupData – CE endast CMT* och kör den körbara filen *DataMigrationUtility*.
3. På sidan 1 i guiden Common Data Service Configuration Migration (CMT) väljer du **Importera data** och sedan **Fortsätt**.

    ![Konfigurationsmigrering.](./media/1ConfigurationMigration.png)

4. På sidan 2 i guiden CMT väljer du **Microsoft 365** som **Distributionstyp**.
5. Markera kryssrutorna **Visa en lista över tillgängliga organisationer** och **Visa avancerat**.
6. Välj region för klientorganisationen, ange autentiseringsuppgifter och välj sedan **Logga in**.

   ![Konfigurationsinloggning.](./media/2ConfigurationSignin.png)

7. På sidan 3 väljer du den organisation som du vill importera demodata till i listan över organisationer i klientorganisationen och väljer sedan **Logga in**.
8. På sidan 4 väljer du zip-filen *SampleSetupAndConfigData* från den uppackade mappen *ProjOpsSampleSetupData - CE endast CMT*.

   ![ZIP-fil.](./media/3ZipFile.png)

   ![Välj en fil.](./media/4SelectAFile.png)

9. När du har markerat zip-filen väljer du **Importera data**.

   ![Importera data.](./media/5ImportData.png)

10. Importen körs i ungefär två–tio minuter beroende på nätverkets hastighet. När den är klar stänger du guiden för CMT. 
11. Kontrollera om organisationen har data i följande 18 entiteter:

    -   Valuta
    -   Konto
    -   Organisationsenhet
    -   Kontaktperson
    -   Enhet
    -   Enhetsgrupp
    -   Prislista
    -   Prislista för projektparameter 
    -   Fakturafrekvens
    -   Bokningsbar resurskategori
    -   Transaktionskategori
    -   Utgiftskategori
    -   Pris för roll
    -   Pris för transaktionskategori
    -   Egenskap
    -   Bokningsbar resurs
    -   Association för bokningsbar resurskategori
    -   Egenskap för bokningsbar resurs

    ![Slutför import.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
