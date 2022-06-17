---
title: Leverantörsfakturering – Koncept och skapande
description: I denna artikel beskrivs konceptet med leverantörsfakturor, scenarier för användning samt hur du skapar leverantörsfakturor i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 38f0760697522b7a5e561cec7d38dfd5c3eaf9fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911480"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Leverantörsfakturering – Koncept och skapande

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Leverantörsfakturering i Microsoft Dynamics 365 Project Operations kan användas för att registrera kostnader från leveranser av tjänster och/eller material i ett projekt av leverantörer.

När tjänster och/eller material läggs ut på entreprenad till en leverantör, representerar en underleverantör det kontraktsenliga avtalet med den leverantören. När leverantören levererar tjänsterna, eller materialet tas emot och används i projektuppgifter, registreras kostnader för projektet. Leverantören skickar regelbundet fakturor som verifieras och matchas med kostnader som registreras i projektet. När verifieringsprocessen är klar bekräftas leverantörsfakturan och frigörs för betalning.

## <a name="scenarios-for-use"></a>Användbara scenarier

Leverantörsfakturor i Project Operations kan användas för två olika scenarier.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Kunderna använder de fullständiga underleverantörsupplevelserna

Med hjälp av leverantörsfakturan kan du verifiera och matcha tidsposter, materialanvändning och utgiftsposter som refererar underleverantörskomponenter med leverantörsfakturarader. Den här processen kan användas för att kontrollera att leverantörsfakturaraderna är korrekta. När verifieringsprocessen har slutförts och leverantörsfakturan har verifierats, vänder programmet de faktiska värden som registrerats av godkända tids-, utgifts- och materialanvändningsloggar, och skapar nya faktiska kostnader med hjälp av fakturaraderna för leverantör.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Kunderna använder inte alla underleverantörsupplevelser men vill ändå få en enhetlig bild av kostnaderna för projekt i Project Operations

Om du spårar underleverantörsprocessen i ett tredjepartssystem kan du registrera kostnader från det tredjepartssystemet till Project Operations genom att skapa leverantörsfakturor som inte refererar till underleverantörer. På så sätt kan dina projektansvariga få en enda, enhetlig bild av alla kostnader för ett visst projekt.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Skapa leverantörsfakturor i Project Operations

Leverantörsfakturor kan skapas på två sätt:

- Från sidan för leverantörsfakturalista eller informationssidan för en enda leverantörsfaktura
- Från listsidan för underleverantör eller informationssidan för en enskild underleverantör

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Skapa från sidan för leverantörsfakturalista eller informationssida

1. Gå till **Inköp** \> **Leverantörsfakturor**.
2. På listsidan för leverantörsfaktura eller på informationssidan för en enskild leverantörsfaktura väljer du **Ny** för att skapa en ny leverantörsfaktura.

Leverantörsfakturor som skapas på detta sätt kan också referera till en underleverantör.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Skapa från listsidan för underleverantörskontrakt eller informationssida

1. Gå till **Inköp** \> **Underleverantörer**.
2. Välj ett eller flera underkontrakt.
3. På listsidan för underleverantör eller på informationssidan för en enskild underleverantör väljer du **Skapa leverantörsfaktura** för att skapa en ny leverantörsfaktura.

En ny leverantörsfaktura med statusen **Utkast** skapas för varje underleverantörskontrakt du har valt.

Leverantörsfakturor som du skapar på det här sättet refererar alltid till underleverantören i leverantörsfakturahuvudet. Varje rad i underleverantörskontraktet som har en faktureringsmetod för tid och material leder till att en rad skapas på leverantörsfakturan. Varje rad i underleverantörskontraktet som har en faktureringsmetod med fast pris skapar en rad på leverantörsfakturan för varje milstolpe på underleverantörsraden som har statusen **Redo att fakturera**.

Följande fält och relaterade poster kopieras från underleverantörskontraktet till sidhuvudet på leverantörsfakturan:

- Leverantör.
- Relaterade prislistor kopieras till leverantörsfakturan som prislistor.
- Valuta.
- Kontrakteringsenhet.
- Betalningsvillkor.

För tids- och materialunderleverantörsrader kopieras följande fält och relaterade poster från underleverantörskontraktsraden till leverantörsfakturaraden:

- Referenser för underleverantör och underreferenser
- Transaktionsklass
- Roll
- Transaktionskategori
- Produktfält
- Project
- Aktivitet
- Bokningsbar resurs

För underleverantörsrader med fast pris kopieras följande fält från underleverantörskontraktsraden och milstolpen på denna rad till leverantörsfakturaraden:

- Referenser för underleverantör och underleverantörsrad.
- Transaktionsklass. Som standard blir värdet **Milstolpe**.
- Namnet och beloppet för milstolpen kopieras från den relaterade milstolpen på underleverantörsraden.
- Användaren kan välja ett projekt och en uppgift på leverantörsfakturaraden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
