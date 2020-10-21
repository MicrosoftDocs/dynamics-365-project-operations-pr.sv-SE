---
title: Använda demoinställning och konfigurationsdata
description: I det här ämnet finns information om hur du tillämpar demoinställning konfigurationsdata i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949097"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Använd demoinställning och konfigurationsdata för Project Operations lite-distributionen – avtal till proforma-fakturering

_**Lite-distribution – avtal till proforma-fakturering_

1. Hämta [Huvuddatapaketet](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Navigera till mappen *ProjOpsDemoDataSetupAndMaster - Integrerad CMT* och kör den körbara filen *DataMigrationUtility*.
3. På sidan 1 i guiden Common Data Service konfigurationsmigrering (CMT) väljer du **Importera data** och sedan **Fortsätt**.

![Konfigurationsmigrering](./media/1ConfigurationMigration.png)

4. På sidan 2 i guiden CMT väljer du **Office 365** som **Distributionstyp**.
5. Markera kryssrutorna **Visa en lista över tillgängliga organisationer** och **Visa avancerat**.
6. Välj region för klientorganisationen, ange autentiseringsuppgifter och välj sedan **Logga in**.

![Konfigurationsinloggning](./media/2ConfigurationSignin.png)

7. På sidan 3 väljer du den organisation som du vill importera demodata till i listan över organisationer i klientorganisationen och väljer sedan **Logga in**.
8. På sidan 4 väljer du zip-filen *MasterAndSetupData* från den uppackade mappen *ProjOpsDemoDataSetupAndMaster - Integrerad CMT*.

![ZIP-fil](./media/3ZipFile.png)

![Välj en fil](./media/4SelectAFile.png)

9. När du har markerat zip-filen väljer du **Importera data**.

![Importera data](./media/5ImportData.png)

10. Importen körs i ungefär två–tio minuter beroende på nätverkets hastighet. När den är klar stänger du guiden för CMT. 
11. Kontrollera om organisationen har data i följande 20 entiteter:

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
- Information om faktureringsfrekvens
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
