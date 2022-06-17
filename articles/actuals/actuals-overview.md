---
title: Utfall
description: Den här artikeln innehåller information om hur du arbetar med faktiska värden i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924820"
---
# <a name="actuals"></a>Utfall

_**Gäller till:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Faktiska värden representerar den granskade och godkända ekonomiska förloppet och schemalägger förloppet för ett projekt. De skapas när tid, utgifter och materialanvändningsposter, journalposter och fakturor godkänns.

> [!IMPORTANT]
> Faktiska värden ska inte redigeras eller tas bort från systemet. I annat fall kan ekonomisk integritet och eventuell integrering med andra ekonomi- och redovisningssystem påverkas negativt. Microsoft Dynamics 365 Project Operations låter dig använda och ersätta faktiska värden för att redigera faktiska värden vid olika punkter i affärsprocessens livscykel för dina projekt.

## <a name="recording-actuals-based-on-project-events"></a>Registrera faktiska värden baserat på projekthändelser

Project Operations registrerar de ekonomiska transaktioner som sker under ett projektåtaganges livscykel som faktiska värden. Skapandet av faktiska värden vid olika händelser under livscykeln varierar beroende på om projektåtagandet använder faktureringsmodellen för tid och material eller faktureringsmodellen med fast pris, samt om det befinner sig i förförsäljningsstadiet eller är ett internt projekt.

I följande artikel förklaras påverkan på tabellen Faktiska värden vid olika händelser för olika variationer:

- [Faktiska effekter i tid- och materialåtagande](ActualsonTM.md)
- [Faktisk påverkan på ett åtagande med fast pris](ActualonFP.md)
- [Faktiska effekter under förförsäljningsstadiet för ett åtagande](ActualonPreSales.md)
- [Effekten av faktiska värden för ett internt projekt](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
