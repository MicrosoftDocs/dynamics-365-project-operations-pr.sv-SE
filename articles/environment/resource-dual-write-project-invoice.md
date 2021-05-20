---
title: Projektfaktura-integration
description: Ämnet innehåller information om Project Operations-integration med dubbelriktad skrivning för kundfakturering.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955843"
---
# <a name="project-invoice-integration"></a>Projektfaktura-integration

Ämnet innehåller information om Project Operations-integration med dubbelriktad skrivning för kundfakturering.

I Project Operations hanterar projektansvarig eftersläpande projektfakturering och skapar en proformafaktura för kunden i Microsoft Dataverse. Baserat på proformafakturan skapar ansvarig för kundreskontra eller projektredovisaren en faktura för kund. Integrering med dubbelriktad skrivning säkerställer att proformafakturainformation synkroniseras med Finance and Operations-appar. När fakturan för kund har registrerats uppdaterar systemet relevanta projekts faktiska värden i Dataverse med redovisningsinformationen. Följande bild ger en översikt på hög nivå över integrationen.

   ![Projektfaktura-integration](./media/DW5Invoicing.png)

När projektansvarig bekräftar proformafakturan i Dataverse synkroniseras proformafakturarubrikens information med Finance and Operations-apparna med tabellmappning med dubbelriktad skrivning, **Projektfakturaförslag V2 (invoices)**. Det här är en enkelriktad integration från Dataverse till Finance and Operations-appar. Det finns inte stöd för att skapa eller radera projektfakturaförslag direkt i Finance and Operations-appar.

Fakturabekräftelse i Dataverse utlöser även affärslogiken för att skapa faktureringsrelaterade poster i entiteten **Faktiska värden**. Posterna synkroniseras med Finance and Operations-appar med tabellmappningen med dubbelriktad skrivning, **Project Operations-integration av faktiska värden (msdyn\_actuals)**. Mer information finns i [Projektberäkningar och faktiska värden](resource-dual-write-estimates-actuals.md). 

Projektfakturaförslagsrader skapas genom den regelbundna processen, **Importera från mellanlagring**. Processen baseras på den faktiska värden för fakturerad försäljning i tabellen **Faktiska värden i mellanlagring**. Mer information finns i [Hantera projektfakturaförslag](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
