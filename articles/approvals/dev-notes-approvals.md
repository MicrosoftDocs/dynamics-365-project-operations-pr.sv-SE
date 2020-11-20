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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483970"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="41bd0-103">Utvecklingsanteckningar för godkännanden</span><span class="sxs-lookup"><span data-stu-id="41bd0-103">Developer notes for Approvals</span></span>

<span data-ttu-id="41bd0-104">_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_</span><span class="sxs-lookup"><span data-stu-id="41bd0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="41bd0-105">Dynamics 365 Project Operations innehåller valideringslogik som säkerställer korrekt postövergång genom godkännandestegen.</span><span class="sxs-lookup"><span data-stu-id="41bd0-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="41bd0-106">Korrigera post övergångar garanterar följande:</span><span class="sxs-lookup"><span data-stu-id="41bd0-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="41bd0-107">Alla stödrader skapas i relaterade tabeller, t.ex. journaler och verkliga värden.</span><span class="sxs-lookup"><span data-stu-id="41bd0-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="41bd0-108">Godkännaren är markerad som **projektgodkännare** i projektet innan du går vidare.</span><span class="sxs-lookup"><span data-stu-id="41bd0-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
