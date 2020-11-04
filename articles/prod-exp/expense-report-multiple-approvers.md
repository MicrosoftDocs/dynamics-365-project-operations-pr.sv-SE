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
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085696"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Flera godkännare i en utgiftsrapport

[!include [banner](../includes/banner.md)]

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
