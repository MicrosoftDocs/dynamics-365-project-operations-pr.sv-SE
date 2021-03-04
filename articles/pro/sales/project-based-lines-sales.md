---
title: Projektbaserade affärsmöjlighetsrader - lite
description: I det här ämnet finns information om projektbaserade affärsmöjlighetsrader. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bba555003b76e3e87412679b274f74f68ac7203b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181043"
---
# <a name="project-based-opportunity-lines---lite"></a>Projektbaserade affärsmöjlighetsrader - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Projektbaserade affärsmöjlighetsrader är endast tillgängliga i projektbaserade affärsmöjligheter. Projektbaserade affärsmöjlighetsposter har värdet i fältet **Typ** inställt på **Arbetsbaserad**.

Projektbaserade affärsmöjlighetsrader är de radartiklar som ska levereras till kunden med hjälp av ett projekt. Ett projekt kan emellertid inte vara knutet till en projektbaserad affärsmöjlighetsrad. Projekt kan vara bundna till radartiklar från steget **Offert** och framåt, eftersom affärsmöjligheten vanligtvis är i ett tidigt stadium av en affärs livscykel. Bestämningen av hur många projekt som ska användas för att leverera arbetet till kunden är ett beslut som fattas senare i försäljningsfasen. Du kan använda affärsmöjlighetsfasen för att identifiera diskreta leveranskomponenter för kunden. De beslut som omger det verkliga antalet projekt som används för att leverera dessa komponenter kan hållas kvar tills mer information om själva arbetet är känd.

Nedan visas fälten i en projektbaserad affärsmöjlighetsrad:

| **Fält** | **Plats** | **Beskrivning** | **Inverkan nedströms** |
| --- | --- | --- | --- |
| Produkttyp | Fliken Allmänt (dold) | Du kan välja något av följande alternativ:</br>- Projektbaserad tjänst (endast tillgänglig när Dynamics 365 Project Operations är installerat)</br>- Produkt (endast tillgänglig när Project Operations och Dynamics 365 Sales är installerat) | Värdet i det här fältet anges till **Projektbaserad tjänst** när du skapar en projektbaserad affärsmöjlighetsrad från rutnätet med projektbaserade rader för affärsmöjligheten. <br> Om du ändrar eller åsidosätter det här värdet aktiveras inte projektfunktionerna på de projektbaserade radartiklarna. |
| Affärsmöjlighet | Fliken Allmänt | Fältet är skrivskyddat och refererar till den överordnade affärsmöjlighetsposten som den här radartikeln tillhör. | Det här fältet har ingen inverkan nedströms. |
| Namn | Fliken Allmänt | Det här är ett redigerbart textfält som kan användas för att ge en kort identitet för radartikeln. | Det här värdet överförs till offertraden när du skapar en offert från den här affärsmöjligheten. |
| Kundbudget | Fliken Allmänt | Det här redigerbara valutafältet kan användas för att spåra det belopp som kunden är villig att spendera för den här radartikeln. | Det här värdet överförs till motsvarande fält på offertraden när du skapar en offert från den här affärsmöjligheten. |
| Faktureringsmetod | Fliken Allmänt | Det här redigerbara fältet har följande värden:</br>- Tid och material</br>- Fast pris | Det här värdet överförs till motsvarande fält på offertraden när du skapar en offert från den här affärsmöjligheten. När du har skapat offertraden är fältet låst och kan inte ändras. Tilldela det här fältvärdet så exakt som möjligt. Om du behöver ändra värdet i det här fältet på offertraden tar du bort och skapar offertraden på nytt. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]