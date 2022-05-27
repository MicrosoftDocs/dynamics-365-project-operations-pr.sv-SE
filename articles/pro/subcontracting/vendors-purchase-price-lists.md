---
title: Hantering av leverantörs- och inköpsprislista i Project Operations
description: Det här ämnet innehåller information som hjälper dig skapa och underhålla leverantörsdata och inköpsprislistor för underleverantörskontrakt.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9c76d5ca45e03167f0ccfd2c1c7013f91fef0f86
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576752"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Hantering av leverantörs- och inköpsprislista i Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

## <a name="vendors-in-project-operations"></a>Leverantörer i Project Operations

I Microsoft Dynamics 365 Project Operations har leverantörskonton en relationstyp som **Leverantör** eller **Leverantör**. Du kan endast välja en kontopost som har en av dessa relationstyper som en leverantör på en underavtal.

Du kan associera en eller flera inköpsprislistor med en leverantörspost. Varje inköpsprislista som är associerad med en leverantörspost bör emellertid ha olika ikraftträdandedatum. Project Operations stöder inte överlappande giltighetsdatum i inköpsprislistor.

Som standard används följande fält och begrepp i en leverantörspost för alla underavtal som skapas för leverantören:

- Betalningsvillkor
- Faktureringsadress, kontaktperson
- Primär kontakt

    > [!NOTE]
    > Som standard används den primära kontakten för leverantören som ansvarig för leverantörskonto för underavtalet.

- Valuta
- Aktuella inköpsprislistor

## <a name="purchase-price-lists-in-project-operations"></a>Inköpsprislistor i Project Operations

En prislista där fältet **Kontext** har inställningen **Inköp** betraktas som en inköpsprislista. Inköpsprislistor kan definieras för att representera en katalog med inköpspriser för tid, utgifter och material. Inköpsprislistor liknar kostnads- och försäljningsprislistor i Project Operations. Följande koncept gäller för inköpsprislistor på samma sätt som för kostnads- och försäljningsprislistor:

- **Giltighetsdatum** – Inköpsprislistor har giltighetsdatum. Giltighetsdatum representeras av fälten startdatum och slutdatum i varje prislista. Tiden mellan startdatum och slutdatum är datumet för dess giltighetsperiod.
- **Valuta** – Valutan i prislistehuvudet används som den valuta som inköpspriser uttrycks i för arbete, utgiftskategorier och produkter i katalogen.
- **Standardtidsenhet** – Standardtidsenheten uttrycker arbetspriser för inköp. Tidsenhetsfältet i en prislista används endast för att tillhandahålla ett standardvärde. Det värdet kan ändras på prisrader för enskilda roller.

Inköpsprislistor kan kopplas till leverantörsposter som associationer som kallas projektprislistor. Dessa prislistor används för att ange standardpriser på underavtalsrader. När flera inköpsprislistor är kopplade till en leverantörspost används som standard den senaste prislistan för underavtal som skapas för leverantören. Endast prislistor där fältet **Kontext** är inställt på **Inköp** kan kopplas till leverantörsposter.

### <a name="subcontract-specific-purchase-price-lists"></a>Underavtalsspecifika inköpsprislistor

Inköpsprislistor kan också kopplas till underavtal som associationer som kallas projektprislistor. Dessa prislistor används för att ange standardpriser på underavtalsrader. Om flera inköpsprislistor är kopplade till ett underavtal måste var och en distinkta giltighetsdatum som standard. Project Operations stöder inte inköpsprislistor som har överlappande giltighetsdatum. Endast prislistor där fältet **Kontext** är inställt på **Inköp** kan kopplas till underavtal.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
