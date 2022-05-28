---
title: Leverantörsfakturaintegration
description: Ämnet ger information om leverantörsfakturaintegration i Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8650eed2230b99b821c1635fdc88252bb65c5583
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591197"
---
# <a name="vendor-invoice-integration"></a>Leverantörsfakturaintegration

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

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

När leverantörsfakturan har bokförts registreras underböckerna för moms, leverantör och andra ekonomiska inlägg som tillämpliga i Dynamics 365 Finance.

![Leverantörsfakturaintegration.](media/DW7VendorInvoice.png)

När poster skrivs till en **Leverantörsfaktura**-entitet i Dataverse startas en automatisk godkännandeprocess för posterna. Vid behov kan du granska status för den automatiska godkännandeprocessen i Dataverse. Gå till **Avancerade inställningar** > **System** > **Systemjobb**. När godkännandet är klart skapar systemet poster för materialtransaktionsklassen i entiteten **Faktiska värden**.

Materialrelaterade faktiska värden bearbetas sedan med tabellmappningen med dubbelriktad skrivning **Project Operations-integration med faktiska värden (msdyn_actuals)**. Mer information finns i [Projektberäkningar och faktiska värden](resource-dual-write-estimates-actuals.md).

Den regelbundna processen **Importera från mellanlagring** skapar leverantörsfakturarelaterade Project Operations-integrationsjournalrader. Servicekontot använder som standard inköpsintegrationskontot. När integrationsjournalen registreras rensas kontosaldot för leverantörsfakturatransaktionen och radbeloppet flyttas till projektkostnadskontot. Det skapas även projektreskontratransaktioner för fakturering nedströms och intäktsidentifieringsändamål.
