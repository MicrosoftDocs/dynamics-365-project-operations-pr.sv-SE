---
title: Projektbaserade affärsmöjlighetsrader
description: Den här artikeln innehåller information om att arbeta med projektbaserade affärsmöjlighetsrader.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f4b8d80a7e3ec06c4089d7c5c32fdb41ac86fb76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918288"
---
# <a name="project-based-opportunity-lines"></a>Projektbaserade affärsmöjlighetsrader

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_


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