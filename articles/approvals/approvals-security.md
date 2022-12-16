---
title: Säkerhet och godkännanden
description: Den här artikeln innehåller information om säkerhetsinställningarna för att arbeta med godkännanden i Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841946"
---
# <a name="security-and-approvals"></a>Säkerhet och godkännanden

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Microsoft Dynamics 365 Project Operations använder två säkerhetsroller för att godkänna poster för tid, utgifter och material:

- Projektgodkännare
- Projektgodkännare, administratör

## <a name="project-approver"></a>Projektgodkännare

Du måste ha säkerhetsroll **Projektgodkännare** för att godkänna projekttid, kostnader och materialposter. Du måste också ha åtkomst till relevanta relaterade entiteter, till exempel **Projekt**. Den åtkomsten kan tilldelas av någon som har rollen **Projektledare**. Dessutom måste du vara teammedlem i projektet och vara markerad som godkännare.

Om du vill godkänna icke-projektposter måste du vara den som skickar den som skickar den.

## <a name="project-approver-admin"></a>Projektgodkännare, administratör

> [!NOTE]
> Funktionen [Godkännandeuppsättningar](approval-sets.md) måste aktiveras innan du kan använda administrationsfunktionerna för Projekt godkännare.

Med säkerhetsroll **Projektgodkännare, administratör** användare att kringgå principer och tillåta godkännande av poster för alla projekt. Tilldelning av den här rollen kringgår valideringslogiken som kräver teammedlemskap och markeras som godkännare. Du måste ha åtkomst till relevanta relaterade tabeller, till exempel **Projekt**, via säkerhetsroller som är tilldelade dig.

SYSTEM användarkontext kringgår valideringar på samma sätt som säkerhetsrollen Projektgodkännare, administratör.
