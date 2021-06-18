---
title: Projektfaktura-integration
description: Ämnet innehåller information om Project Operations-integration med dubbelriktad skrivning för kundfakturering.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996588"
---
# <a name="project-invoice-integration"></a>Projektfaktura-integration

Ämnet innehåller information om Project Operations-integration med dubbelriktad skrivning för kundfakturering.

I Project Operations hanterar projektansvarig eftersläpande projektfakturering och skapar en proformafaktura för kunden i Microsoft Dataverse. Baserat på proformafakturan skapar ansvarig för kundreskontra eller projektredovisaren en faktura för kund. Integrering med dubbelriktad skrivning säkerställer att proformafakturainformation synkroniseras med Finance and Operations-appar. När fakturan för kund har registrerats uppdaterar systemet relevanta projekts faktiska värden i Dataverse med redovisningsinformationen. Följande bild ger en översikt på hög nivå över integrationen.

   ![Projektfaktura-integration](./media/DW5Invoicing.png)

När projektansvarig bekräftar proformafakturan i Dataverse synkroniseras proformafakturarubrikens information med Finance and Operations-apparna med tabellmappning med dubbelriktad skrivning, **Projektfakturaförslag V2 (invoices)**. Det här är en enkelriktad integration från Dataverse till Finance and Operations-appar. Det finns inte stöd för att skapa eller radera projektfakturaförslag direkt i Finance and Operations-appar.

Fakturabekräftelse i Dataverse utlöser även affärslogiken för att skapa faktureringsrelaterade poster i entiteten **Faktiska värden**. Posterna synkroniseras med Finance and Operations-appar med tabellmappningen med dubbelriktad skrivning, **Project Operations-integration av faktiska värden (msdyn\_actuals)**. Mer information finns i [Projektberäkningar och faktiska värden](resource-dual-write-estimates-actuals.md). 

Projektfakturaförslagsrader skapas genom den regelbundna processen, **Importera från mellanlagring**. Processen baseras på den faktiska värden för fakturerad försäljning i tabellen **Faktiska värden i mellanlagring**. Mer information finns i [Hantera projektfakturaförslag](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
