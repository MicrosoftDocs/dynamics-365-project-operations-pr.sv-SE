---
title: Leverantörsfakturaintegration
description: Ämnet ger information om leverantörsfakturaintegration i Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07839436c3777b0554e0721d250bff643e38c088
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955846"
---
# <a name="vendor-invoice-integration"></a>Leverantörsfakturaintegration

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Projektrelaterade inköp i Dynamics 365 Project Operations kan registreras genom att gå till **Leverantörsreskontra** > **Fakturor** > **Väntande leverantörsfakturor** och använda ett dokument för väntande leverantörsfaktura. Mer information finns i [Inköp av icke-lagerbaserade material med väntande leverantörsfaktura](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Innan du använder funktionerna som beskrivs i ämnet måste du granska och tillämpa de konfigurationer som krävs. Mer information finns i [Aktivera icke-lagerbaserade material och väntande leverantörsfakturor](../procurement/configure-materials-nonstocked.md).

I Project Operations registreras projektrelaterade leverantörsfakturor med specialbokföringsregler:

- Projektrelaterade kostnader (inklusive icke-återbetalningsbar moms) registreras inte direkt på projektkostnadskontot i huvudboken. Kostnaden registreras i stället på **Inköpsintegrationskontot**. Kontot ställs in i **Projekthantering och redovisning** > **Inställning** > **Projekthanterings- och redovisningsparametrar**, på fliken **Project Operations i Dynamics 365 Customer Engagement**.
- Dubbelriktad skrivning synkroniseras leverantörsfakturainformationen med Microsoft Dataverse med följande tabellmappningar:

     - **Project Operations-integration för entitet för export av projektleverantörsfaktura (msdyn_projectvendorinvoices)**: Den här tabellmappningen synkroniserar leverantörsfakturans rubrikinformation. Enbart leverantörsfakturor som har minst en rad som innehåller ett projekt-ID synkroniseras med Dataverse.
     - **Project Operations-integration för entitet för export av projektleverantörsfakturarad (msdyn_projectvendorinvoicelines)**: Den här tabellmappningen synkroniserar leverantörsfakturans radinformation. Endast rader som innehåller ett projekt-ID synkroniseras med Dataverse.

     > [!NOTE]
     > Leverantörsfakturainformationen i Dataverse kan inte redigeras.

Momsreskontra, leverantörsreskontra och andra ekonomiska poster registreras som tillämpligt i Dynamics 365 Finance när leverantörsfakturan registreras.

![Leverantörsfakturaintegration](media/DW7VendorInvoice.png)

När poster skrivs till en **Leverantörsfaktura**-entitet i Dataverse startas en automatisk godkännandeprocess för posterna. Vid behov kan du granska status för den automatiska godkännandeprocessen i Dataverse. Gå till **Avancerade inställningar** > **System** > **Systemjobb**. När godkännandet är klart skapar systemet poster för materialtransaktionsklassen i entiteten **Faktiska värden**.

Materialrelaterade faktiska värden bearbetas sedan med tabellmappningen med dubbelriktad skrivning **Project Operations-integration med faktiska värden (msdyn_actuals)**. Mer information finns i [Projektberäkningar och faktiska värden](resource-dual-write-estimates-actuals.md).

Den regelbundna processen **Importera från mellanlagring** skapar leverantörsfakturarelaterade Project Operations-integrationsjournalrader. Servicekontot använder som standard inköpsintegrationskontot. När integrationsjournalen registreras rensas kontosaldot för leverantörsfakturatransaktionen och radbeloppet flyttas till projektkostnadskontot. Det skapas även projektreskontratransaktioner för fakturering nedströms och intäktsidentifieringsändamål.
