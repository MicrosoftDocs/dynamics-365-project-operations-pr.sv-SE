---
title: Flera godkännare i en utgiftsrapport
description: I det här ämnet finns information om utgiftsrapporter som kräver godkännande av flera personer.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960629"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Flera godkännare i en utgiftsrapport

Beroende på organisationens godkännandeprinciper för utgifter kan fler än en person behöva godkänna en utgiftsrapport som skickas in av en medarbetare. När du konfigurerar arbetsflödesprocessen för godkännande av utgiftsrapporter kan du lägga till arbetsflödeselement som innehåller uppgifter eller steg för en eller flera godkännare av utgiftsrapporter. Du kan till exempel kräva att alla utgiftsrapporter ska godkännas först av chefen för den medarbetare som skickade in rapporten och sedan av koordinatorn för leverantörsreskontra.

Om du vill kräva flera godkännare för utgiftsrapporter kan du lägga till arbetsflödeselementen på något av följande sätt:

- Lägg till ett godkännandeelement som har ett steg. Steget kan till exempel kräva att en utgiftsrapport tilldelas en användargrupp och att den godkänns med 50 procent av användargruppens medlemmar.
- Lägg till ett godkännandeelement som har flera steg. Godkännandeelementet kan till exempel innehålla följande steg:

    1. Chefen för den medarbetare som skickade utgiftsrapporten godkänner den.
    2. Leverantörsreskontra ansvarig verifierar inleveranserna och objekt för utgiftsrapport.
    3. Budgetägaren godkänner utgiftsrapporten.

- Lägg till flera godkännandeelement, som vart och ett har ett steg. Du kan till exempel lägga till ett separat godkännandeelement för vart och ett av följande steg:

    1. Medarbetarens chef godkänner utgiftsrapporten.
    2. Budgetägaren godkänner utgiftsrapporten.
