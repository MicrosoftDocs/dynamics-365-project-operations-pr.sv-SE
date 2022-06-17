---
title: Använd inköpskategorier för projektinköpsorder och väntande leverantörsfakturor
description: Denna artikel beskriver hur du konfigurerar inköpskategorier som kan användas för projektinköpsorder och väntande leverantörsfakturor.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7d774631a4712de9b29ddedfee2ea3fc4a2d436f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927442"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Använd inköpskategorier för projektinköpsorder och väntande leverantörsfakturor

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Inköpsproffs kan skapa och underhålla kataloger av de artiklar och tjänster som kan användas i inköpsorder för projekt och väntande leverantörsfakturor. [Inköpskataloger](/dynamics365/supply-chain/procurement/procurement-catalogs) som gör det enkelt att kategorisera inköp utan att behöva konfigurera och använda en produktkatalog som släppts. Varje inköpskategori kan mappas till en projektkategori för tid, utgifter eller artikeltransaktioner. När en väntande leverantörsfaktura som använder en inköpskategori publiceras skapar systemet faktiska projektvärden för tid, utgift eller material, projekttransaktioner och underleverantörsposter.

## <a name="minimum-version-requirements"></a>Lägsta versionskrav

Följande versioner krävs för att använda inköpskategorier med projektinköpsorder för icke-lagerbaserade/resursbaserade scenarier för Microsoft Dynamics 365 Project Operations:

- Project Operations Dataverse-lösning i version 4.41.0.45 eller senare
- Finance and Operations-miljö i version 10.0.26 eller senare

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Kör dubbelskrivningsmappningar för kategoristöd för inköp

Kontrollera att mappningen för **exportentitet \_projectvendorinvoicelines för rad i leverantörsfaktura för integreringsprojekt i Project Operations** använder version 1.0.0.4 eller senare.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Aktivera funktionsnyckeln för inköpskategorier

Följ stegen nedan om du vill använda inköpskategorier med projektinköpsorder.

1. Öppna arbetsytan **Funtionshantering** i Dynamics 365 Finance.
1. Leta upp funktionen **Använd inköpskategorier i Project Operations för resursbaserade/icke-lagerbaserade scenarier**, och välj sedan **Aktivera**.

> [!IMPORTANT]
> Du måste också aktivera aktivera funktionen **Aktivera väntande leverantörsfakturor i Project Operations för resurs-/icke-lagerbaserade scenarier**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Projektkategorier för mappning i kategorihierarkin för inköp

Följ stegen nedan om du vill mappa projektkategorier till inköpskategorier i hierarkin **Inköpskategori**.

1. Gå till **Anskaffning och källa \> Inköpskategorier**.
1. Välj **Redigera kategorihierarki**.
1. Markera den önskade kategorihierarkinoden och associera sedan, på fliken **Tilldela projektkategorier** noden med projektkategorin från kategorin **Tid**, **Utgift** eller **Artikelprojekt** (dvs. kategorin **Standardtid** eller **Standardutgift**).
1. Välj **Spara**.
1. Stäng sidan.

> [!NOTE]
> Det är valfritt att mappa en inköpskategori till en projektkategori. Om en inköpskategori inte har mappats kommer systemet att använda värdet i fältet **Artikel** i avsnittet **Standardkategori för projekt** på fliken **Project Operations i Dynamics 365 Customer engagement** på sidan **Projekthanterings- och redovisningsparametrar**.
