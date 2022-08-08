---
title: Projektfaktura-integration
description: Den här artikeln ger information om Project Operations integration för dubbelriktad skrivning för kundfakturering.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029046"
---
# <a name="project-invoice-integration"></a>Projektfaktura-integration

Den här artikeln ger information om Project Operations integration för dubbelriktad skrivning för kundfakturering.

I Project Operations hanterar projektansvarig eftersläpande projektfakturering och skapar en proformafaktura för kunden i Microsoft Dataverse. Baserat på proformafakturan skapar ansvarig för kundreskontra eller projektredovisaren en faktura för kund. Integrering med dubbelskrivning säkerställer att proforma-fakturainformationen synkroniseras med apparna för ekonomi och drift. När fakturan för kund har registrerats uppdaterar systemet relevanta projekts faktiska värden i Dataverse med redovisningsinformationen. Följande bild ger en översikt på hög nivå över integrationen.

   ![Projektfakturaintegration.](./media/DW5Invoicing.png)

När projektledaren har bekräftat proforma-fakturan i Dataverse synkroniseras proformafakturahuvudets information med apparna för ekonomi och drift med hjälp av tabellmappningen med dubbel skrivning, **Projektfakturaförslag V2 (fakturor)**. Detta är en envägsintegrering från Dataverse till apparna för ekonomi och drift. Det finns inte stöd för att skapa eller ta bort projektfakturaförslag direkt i apparna för ekonomi och drift.

Fakturabekräftelse i Dataverse utlöser även affärslogiken för att skapa faktureringsrelaterade poster i entiteten **Faktiska värden**. Posterna synkroniseras med ekonomi och drift med hjälp av tabellmappningen med dubbelskrivning, **Integrering av faktiska värden i Project Operations (msdyn\_actuals).** Mer information finns i [Projektberäkningar och faktiska värden](resource-dual-write-estimates-actuals.md). 

Projektfakturaförslagsrader skapas genom den regelbundna processen, **Importera från mellanlagring**. Processen baseras på den faktiska värden för fakturerad försäljning i tabellen **Faktiska värden i mellanlagring**. Mer information finns i [Hantera projektfakturaförslag](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
