---
title: Projektfaktura-integration
description: Den här artikeln ger information om Project Operations integration för dubbelriktad skrivning för kundfakturering.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912124"
---
# <a name="project-invoice-integration"></a>Projektfaktura-integration

Den här artikeln ger information om Project Operations integration för dubbelriktad skrivning för kundfakturering.

I Project Operations hanterar projektansvarig eftersläpande projektfakturering och skapar en proformafaktura för kunden i Microsoft Dataverse. Baserat på proformafakturan skapar ansvarig för kundreskontra eller projektredovisaren en faktura för kund. Integrering med dubbelskrivning säkerställer att proforma-fakturainformationen synkroniseras med apparna för ekonomi och drift. När fakturan för kund har registrerats uppdaterar systemet relevanta projekts faktiska värden i Dataverse med redovisningsinformationen. Följande bild ger en översikt på hög nivå över integrationen.

   ![Projektfakturaintegration.](./media/DW5Invoicing.png)

När projektledaren har bekräftat proforma-fakturan i Dataverse synkroniseras proformafakturahuvudets information med apparna för ekonomi och drift med hjälp av tabellmappningen med dubbel skrivning, **Projektfakturaförslag V2 (fakturor)**. Detta är en envägsintegrering från Dataverse till apparna för ekonomi och drift. Det finns inte stöd för att skapa eller ta bort projektfakturaförslag direkt i apparna för ekonomi och drift.

Fakturabekräftelse i Dataverse utlöser även affärslogiken för att skapa faktureringsrelaterade poster i entiteten **Faktiska värden**. Posterna synkroniseras med Finance and Operations med hjälp av tabellmappningen med dubbelskrivning, **Integrerign av faktiska värden i Project Operations (msdyn\_actuals).** Mer information finns i [Projektberäkningar och faktiska värden](resource-dual-write-estimates-actuals.md). 

Projektfakturaförslagsrader skapas genom den regelbundna processen, **Importera från mellanlagring**. Processen baseras på den faktiska värden för fakturerad försäljning i tabellen **Faktiska värden i mellanlagring**. Mer information finns i [Hantera projektfakturaförslag](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
