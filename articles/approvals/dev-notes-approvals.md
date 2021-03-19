---
title: Utvecklingsanteckningar för godkännanden
description: I det här ämnet finns ytterligare utvecklarinformation om att arbeta med godkännanden.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290291"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="ee1ed-103">Utvecklingsanteckningar för godkännanden</span><span class="sxs-lookup"><span data-stu-id="ee1ed-103">Developer notes for Approvals</span></span>

<span data-ttu-id="ee1ed-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="ee1ed-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ee1ed-105">Dynamics 365 Project Operations innehåller valideringslogik som säkerställer korrekt postövergång genom godkännandestegen.</span><span class="sxs-lookup"><span data-stu-id="ee1ed-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="ee1ed-106">Korrigera post övergångar garanterar följande:</span><span class="sxs-lookup"><span data-stu-id="ee1ed-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="ee1ed-107">Alla stödrader skapas i relaterade tabeller, t.ex. journaler och verkliga värden.</span><span class="sxs-lookup"><span data-stu-id="ee1ed-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="ee1ed-108">Godkännaren är markerad som **projektgodkännare** i projektet innan du går vidare.</span><span class="sxs-lookup"><span data-stu-id="ee1ed-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]