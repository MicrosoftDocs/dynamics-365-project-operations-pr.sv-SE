---
title: Hantera leads (Pro)
description: I det här ämnet finns information om hantering av projektbaserade leads (pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 005e36811643b0b1e98a686792cf39125ae97949
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896348"
---
# <a name="manage-leads-pro"></a>Hantera leads (Pro)

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Projektbaserade leads kan hanteras och kvalificeras i Project Operations. I processen för hantering av leads ingår att skapa arbetsbaserade leads och kvalificera sådana leads. 

## <a name="list-of-project-sales-leads"></a>Lista över projektbaserade försäljningsleads

I avsnittet **Försäljning**, i vänster navigeringsfönster, öppnar du sidan **Leads** för att visa en lista över alla leadposter i systemet. Listan med leads som visas är arbetsbaserade och andra typer av leads som kan skapas om du även har Dynamics 365 Sales eller Dynamics 365 Field Service-program.

Du kan skapa en filtrerad vy om du endast vill visa projektbaserade leads genom att skapa ett filter för värdet **Typ**. Du kan till exempel välja att endast visa arbetsbaserade leads.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Skapa en ny lead för en projektbaserad affär

När en projektbaserad lead kvalificeras skapas en affärsmöjlighet och ett konto. En projektbaserad affärsmöjlighet är startpunkten för försäljningsaktiviteter i fasen Affärsmöjlighet. Projektbaserade affärsmöjligheter har unika funktioner som krävs för att kunna sälja projektarbete. Dessa funktioner omfattar:

- Faktureringsmetoderna Tid och material och Fast pris
- Flera datumeffektiva prislistor för personal, utgifter och material som uppstår i projekt.

Om du vill att en kvalificerad lead automatiskt ska skapa en affärsmöjlighet sätter du attributet **Typ** på **Arbetsbaserat** när du skapar en lead. Om du väljer en annan typ skapar en lead inte en projektbaserad affärsmöjlighet när den kvalificeras. Om projektbaserade affärsmöjligheter inte skapas blir de projektspecifika funktionerna inte tillgängliga i de efterföljande försäljningsprocesserna.

Följande tabell innehåller viktig fältinformation för en lead och effekterna nedströms för dessa fält.

| **Fält** | **Plats** | **Relevans, syfte och vägledning** | **Inverkan nedströms** |
| --- | --- | --- | --- |
| Område | Fliken Allmänt | Det här textfältet och bör innehålla en kort beskrivning av affären. | Leadämnet blir standardvärdet för affärsmöjlighetens ämne och namnet på offert- och projektkontraktet. |
| Type | Fliken Allmänt | Den här alternativuppsättningen har följande alternativ:</br>- Arbetsbaserad (endast tillgängligt när Project Operations är installerat)</br>- Artikelbaserad (endast tillgänglig när Project Operations och Sales är installerat)</br>- Serviceunderhåll-baserad (tillgängligt när Field Service är installerat) | När värdet i det här fältet är inställt på **Arbetsbaserat** i leaden är leaden kvalificerad för att skapa en projektbaserad affärsmöjlighet. Det krävs en projektbaserad affärsmöjlighet för att aktivera alla projektspecifika tillägg och funktioner i den efterföljande försäljningsprocessen för affären. |
| Förnamn | Fliken Allmänt | Förnamn på den potentiella kundens kontaktperson | När en lead kvalificeras skapas ett konto, en kontakt och en affärsmöjlighet. Kontaktens förnamn anges här. |
| Efternamn | Fliken Allmänt | Efternamn på den potentiella kundens kontaktperson | När en lead kvalificeras skapas ett konto, en kontakt och en affärsmöjlighet. Kontaktens efternamn anges här. |
| Företag | Fliken Allmänt | Namnet på den potentiella kundens företag | När en lead kvalificeras skapas ett konto, en kontakt och en affärsmöjlighet. Namnet på det skapade kontot anges här. |
| Valuta | Detaljflik | Den potentiella kundens valuta | När en lead kvalificeras skapas ett konto, en kontakt och en affärsmöjlighet. Valutan på det skapade kontot anges här. |

## <a name="qualify-a-new-project-based-lead"></a>Kvalificera en ny projektbaserad lead

Leads som har värdet **Typ** inställt på **Arbetsbaserat** kallas projektbaserade leads. När en projektbaserad lead kvalificeras skapas följande:

- Ett konto som använder fältet **Företag** från leaden.
- En kontaktpost som är kopplad till kontot utifrån värdena i fälten **Förnamn** och **Efternamn** i leaden.
- En projektbaserad affärsmöjlighet som har fältet **Typ** inställt på &quot;**Arbetsbaserad**.

Mer detaljerad information om kvalificering av leads finns i [Kvalificera eller konvertera leads](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Affärsprocessflöde för projektbaserade affärer

Följande affärsprocessflöden stöds för projektbaserade affärer i Project Operations:

- Affärsprocessen Lead till affärsmöjlighet
- Affärsmöjlighet, försäljningsprocess

Affärsprocessen Lead till affärsmöjlighet stöder följande steg:

| Namn på stadium | Mappad entitet | Funktioner |
| --- | --- | --- |
| Kvalificera | Lead | Kvalificera lead för att skapa ett konto, en kontakt och en affärsmöjlighet. |
| Ta fram | Affärsmöjlighet | Utveckla affärsmöjligheten och lägg till mer information om det arbete som ingår, viktiga intressenter och konkurrens. |
| Föreslå | Affärsmöjlighet | Utarbeta förslaget och få godkännande från det interna granskningsteamet. |
| Stängning | Affärsmöjlighet | Vinn affärsmöjligheten för att stänga affären. |
