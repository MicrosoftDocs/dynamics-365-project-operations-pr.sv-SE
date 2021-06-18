---
title: Utvecklingsanteckningar för godkännanden
description: I det här ämnet finns ytterligare utvecklarinformation om att arbeta med godkännanden.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996813"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="e40b6-103">Utvecklingsanteckningar för godkännanden</span><span class="sxs-lookup"><span data-stu-id="e40b6-103">Developer notes for Approvals</span></span>

<span data-ttu-id="e40b6-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="e40b6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e40b6-105">Dynamics 365 Project Operations innehåller valideringslogik som säkerställer korrekt postövergång genom godkännandestegen.</span><span class="sxs-lookup"><span data-stu-id="e40b6-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="e40b6-106">Korrigera post övergångar garanterar följande:</span><span class="sxs-lookup"><span data-stu-id="e40b6-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="e40b6-107">Alla stödrader skapas i relaterade tabeller, t.ex. journaler och verkliga värden.</span><span class="sxs-lookup"><span data-stu-id="e40b6-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="e40b6-108">Godkännaren är markerad som **projektgodkännare** i projektet innan du går vidare.</span><span class="sxs-lookup"><span data-stu-id="e40b6-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]