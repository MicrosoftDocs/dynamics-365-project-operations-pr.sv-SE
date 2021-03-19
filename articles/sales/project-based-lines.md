---
title: Projektbaserade affärsmöjlighetsrader
description: I det här ämnet finns information om hur du arbetar med projektbaserade affärsmöjlighetsrader.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91c53c917846a2b4e4fd64c14bb91782e9d05d66
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277675"
---
# <a name="project-based-opportunity-lines"></a>Projektbaserade affärsmöjlighetsrader

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_


Projektbaserade affärsmöjlighetsrader är endast tillgängliga i projektbaserade affärsmöjligheter. Projektbaserade affärsmöjlighetsposter har värdet i fältet **Typ** inställt på **Arbetsbaserad**.

Projektbaserade affärsmöjlighetsrader är de radartiklar som ska levereras till kunden med hjälp av ett projekt. Ett projekt kan emellertid inte vara knutet till en projektbaserad affärsmöjlighetsrad. Projekt kan vara bundna till radartiklar från steget **Offert**, eftersom affärsmöjligheten vanligtvis inträffar i ett tidigt stadium av en affär. Bestämningen av hur många projekt som ska användas för att leverera arbetet till kunden är ett beslut som fattas senare i försäljningsfasen. Använd affärsmöjlighetsfasen för att identifiera diskreta leveranskomponenter för kunden. De beslut som omger det verkliga antalet projekt som används för att leverera dessa komponenter kan hållas kvar tills mer information om själva arbetet är känd.

Nedan visas fälten i en projektbaserad affärsmöjlighetsrad:

| **Fält** | **Plats** | **Beskrivning** | **Inverkan nedströms** |
| --- | --- | --- | --- |
| Produkttyp | Fliken Allmänt (dold) | Det här är ett alternativuppsättningsfält. Om du har installerat Dynamics 365 Operations är ett av de tillgängliga alternativen **Projektbaserad tjänst**.  | Värdet i det här fältet anges till **Projektbaserad tjänst** när du skapar en projektbaserad affärsmöjlighetsrad från rutnätet med projektbaserade rader för affärsmöjligheten. <br> Om du ändrar eller åsidosätter det här värdet aktiveras inte projektfunktionerna på de projektbaserade radartiklarna. |
| Affärsmöjlighet | Fliken Allmänt | Fältet är skrivskyddat och refererar till den överordnade affärsmöjlighetsposten som den här radartikeln tillhör. | Det här fältet har ingen inverkan nedströms. |
| Namn | Fliken Allmänt | Det här är ett redigerbart textfält som kan användas för att ge en kort identitet för den här radartikeln | Det här värdet överförs till offertraden när du skapar en offert från den här affärsmöjligheten |
| Kundbudget | Fliken Allmänt | Det här redigerbara valutafältet kan användas för att spåra det belopp som kunden är villig att spendera för den här radartikeln. | Det här värdet överförs till motsvarande fält på offertraden när du skapar en offert från den här affärsmöjligheten |
| Faktureringsmetod | Fliken Allmänt | Det här redigerbara fältet har följande värden:</br>- Tid och material</br>- Fast pris | Det här värdet överförs till motsvarande fält på offertraden när du skapar en offert från den här affärsmöjligheten. När du har skapat offertraden är fältet låst och kan inte ändras. Tilldela det här fältvärdet så exakt som möjligt. Om du behöver ändra värdet i det här fältet på offertraden tar du bort och skapar offertraden på nytt. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]