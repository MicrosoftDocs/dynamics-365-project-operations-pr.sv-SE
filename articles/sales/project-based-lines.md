---
title: Projektbaserade affärsmöjlighetsrader
description: I det här ämnet finns information om hur du arbetar med projektbaserade affärsmöjlighetsrader.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7b255d607ac8180c249a9b9831db6f8d0cd3937b
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898418"
---
# <a name="project-based-opportunity-lines"></a>Projektbaserade affärsmöjlighetsrader

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_


Projektbaserade affärsmöjlighetsrader är endast tillgängliga i projektbaserade affärsmöjligheter. Projektbaserade affärsmöjlighetsposter har värdet i fältet **Typ** inställt på **Arbetsbaserad**.

Projektbaserade affärsmöjlighetsrader är de radartiklar som ska levereras till kunden med hjälp av ett projekt. Ett projekt kan emellertid inte vara knutet till en projektbaserad affärsmöjlighetsrad. Projekt kan vara bundna till radartiklar från steget **Offert**, eftersom affärsmöjligheten vanligtvis inträffar i ett tidigt stadium av en affär. Bestämningen av hur många projekt som ska användas för att leverera arbetet till kunden är ett beslut som fattas senare i försäljningsfasen. Använd affärsmöjlighetsfasen för att identifiera diskreta leveranskomponenter för kunden. De beslut som omger det verkliga antalet projekt som används för att leverera dessa komponenter kan hållas kvar tills mer information om själva arbetet är känd.

Nedan visas fälten i en projektbaserad affärsmöjlighetsrad:

| **Fält** | **Plats** | **Relevans, syfte och vägledning** | **Inverkan nedströms** |
| --- | --- | --- | --- |
| Produkttyp | Fliken Allmänt (dold) | Det här är ett alternativuppsättningsfält. Om du har installerat Dynamics 365 Operations är ett av de tillgängliga alternativen **Projektbaserad tjänst**.  | Värdet i det här fältet anges till **Projektbaserad tjänst** när du skapar en projektbaserad affärsmöjlighetsrad från rutnätet med projektbaserade rader för affärsmöjligheten. <br> Om du ändrar eller åsidosätter det här värdet aktiveras inte projektfunktionerna på de projektbaserade radartiklarna. |
| Affärsmöjlighet | Fliken Allmänt | Fältet är skrivskyddat och refererar till den överordnade affärsmöjlighetsposten som den här radartikeln tillhör. | Det här fältet har ingen inverkan nedströms. |
| Namn | Fliken Allmänt | Det här är ett redigerbart textfält som kan användas för att ge en kort identitet för den här radartikeln | Det här värdet överförs till offertraden när du skapar en offert från den här affärsmöjligheten |
| Kundbudget | Fliken Allmänt | Det här redigerbara valutafältet kan användas för att spåra det belopp som kunden är villig att spendera för den här radartikeln. | Det här värdet överförs till motsvarande fält på offertraden när du skapar en offert från den här affärsmöjligheten |
| Faktureringsmetod | Fliken Allmänt | Det här redigerbara fältet har följande värden:</br>- Tid och material</br>- Fast pris | Det här värdet överförs till motsvarande fält på offertraden när du skapar en offert från den här affärsmöjligheten. När du har skapat offertraden är fältet låst och kan inte ändras. Tilldela det här fältvärdet så exakt som möjligt. Om du behöver ändra värdet i det här fältet på offertraden tar du bort och skapar offertraden på nytt. |
