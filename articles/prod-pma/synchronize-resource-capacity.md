---
title: Synkronisera resurskapacitet
description: I det här ämnet finns information om hur du synkroniserar en resurs kapacitet för kalendrar och projekt.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3911ffe9ecfd15a7852dea893084e0059b06c9b8
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682733"
---
# <a name="synchronize-resource-capacity"></a>Synkronisera resurskapacitet

[!include [banner](../includes/banner.md)]

Med hjälp av processerna för synkronisering av resurser kan du garantera att informationen för kalendern och baskalendern rinner ned i projektresursens schemaläggning. Om kalendern ändras gör processerna de nödvändiga uppdateringarna till schemaläggning av projektresurser. Processerna bidrar också till att förbättra prestanda eftersom kalenderns resursinformation synkroniseras i förväg. Uppdateringarna av resursplaneringsinformationen kan därför snabbare uppdateras. Vi rekommenderar att du schemalägger processerna som en batch i stället för en i taget. I annat fall kommer någon att glömma bort de ingående datumen när informationen senast synkroniserades. Om ingående datum inte används kan luckor uppstå vid synkronisering av datum.

![Synkronisering av kalender.](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Synkronisering av resurskapacitets sammanslagningar

Synkroniseringsprocessen synkroniserar all information i resurskalendern. Den här informationen inkluderar baskalenderinformation om eventuella ändringar i tabellen resurskalenderkapacitet för projektet. Om nya resurser läggs till i projektet hjälper synkroniseringen till att säkerställa att den uppdaterade kalenderinformationen är tillgänglig. Du kan utföra synkroniseringen när som helst.

Vi rekommenderar att du använder en batch. Alternativen är tillgängliga under synkroniseringen av kapacitetsreservationer.

1. Välj **Projektledning och redovisning** &gt; **Periodisk** &gt; **Synkronisering av kapacitet** &gt; **Synkronisering av resurskapacitets sammanslagningar**.
2. Ange alternativen visas i följande tabell.

    | Alternativ      | Beskrivning |
    |-------------|-------------|
    | Periodkod | Alternativt kan du välja en intervallkod för räkenskapsåret för att ange start- och slutdatum för synkroniseringsprocessen för resurskapacitets sammanslagningar. |
    | Startdatum  | Ange startdatum för synkroniseringsprocessen för resurskapacitets sammanslagning. |
    | Slutdatum    | Ange slutdatum för synkroniseringsprocessen för resurskapacitets sammanslagning. |

[![Synkroniseringsprocess.](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]