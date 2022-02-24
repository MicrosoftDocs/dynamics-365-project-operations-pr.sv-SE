---
title: Registrera materialanvändning för projekt och projektuppgifter
description: Detta ämne ger information om hur du loggar materialanvändning för projekt och projektuppgifter.
author: rumant
manager: AnnBe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ab431ce4c18a4283cd887de9afcba0dd556d2567
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852900"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Registrera materialanvändning för projekt och projektuppgifter

_**Gäller till:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

När ett projektteam arbetar med uppgifter i ett projekt använder eller använder de material. Med hjälp av en materialanvändningslogg kan du registrera användningen så att den kan godkännas av projektledaren och faktureras kunden. 

Följ stegen nedan om du vill registrera användning av katalog- eller inskrivningsmaterial och skicka det till godkännaren: 

1. I navigeringsfönstret, välj **Materialanvändning** och välj sedan **Nytt**.
2. På sidan **Ny materialanvändning**, ange önskad materialanvändningsinformation och välj sedan **Spara**.

Följande tabell ger information om fälten på sidan **Materialförbrukningslogg**. 

| **Fält** | **Beskrivning** | **Inverkan nedströms** |
| --- | --- | --- |
| Beskrivning | En beskrivning av den specifika materialanvändningen. | Det här fältet har ingen inverkan nedströms. |
| Datum | Det datum då materialet förväntas användas. | Det här fältet har ingen inverkan nedströms. |
| Project | Ett listprojekt som är aktiva. | Om du väljer ett projekt för en materialanvändningslogg påverkas fältet **Uppgift** om endast de uppgifter som finns i projektet visas. |
| Uppgift | En lista med uppgifter för projektet, inklusive uppgifter för sammanfattning och nod. | Om du väljer en uppgift för en materialanvändningslogg påverkas den faktiska materialkostnaden och den faktiska materialförsäljningen för en uppgift. Om fältet är tomt spåras och summeras motsvarande materialanvändningskostnad och försäljning endast på projektnivån. |
| Välj produkt | Ange om denna materialanvändning är för en **Befintlig** (katalog) produkt eller en **Ej registrerad** produkt. | Fältet styr produkttypen. |
| Produkt | ID för produkten från produktkatalogen. När du väljer ett produkt-ID uppdateras fältet **Välj produkt** automatiskt till **Befintlig produkt**. ID används för att hämta kostnader och försäljningspriser från prislistan. | Det här fältet har ingen inverkan nedströms. |
| Beskrivning av oregistrerad produkt | Ett textfält som oregistrerad ska ange produktnamnet. Det här fältet är tillgängligt när du väljer **Oregistrerad** produkt i fältet **Välj produkt**.| Det här fältet har ingen inverkan nedströms. |
| Bokningsbar resurs| Resurs som använde det här materialet för projektet. Standardvärdet för det här fältet är den bokningsbara resursen för den inloggade användaren, men kan ändras till att registrera användning för andra medlemmars räkning i projektteamet. | Det här fältet har ingen inverkan nedströms. |
| Enhetsgrupp | Standardvärdet i det här fältet kommer från den enhetsgrupp som har angetts som standard för katalogprodukten. Du kan uppdatera fältet om du vill välja en annan enhetsgrupp. | Det här fältet har ingen inverkan nedströms. |
| Enhet | Standardvärdet i det här fältet är standardenheten för den valda produkten. Du kan uppdatera fältet om du vill välja en annan enhet. | Om du ändrar enheten får du ett annat standardpris och en annan standardkostnad för enheten. |
| Antal | Kvantitet av produkten som har använts i projektet eller projektuppgiften. | Det här fältet har ingen inverkan nedströms. |
| Enhetskostnad | Enhetskostnaden för den valda produkten och enhetskombinationen enligt den aktuella kostnadsprislistan. | Enhetskostnaden visas alltid i projektets kostnadsvaluta. Om det inte finns någon enhetskostnad för kombinationsprodukten och enheten i prislistan blir enhetskostnaden 0,00 som standard. |
| Total kostnad | Kostnadsbeloppet som beräknas som enhetskostnad för \* kvantitet.| Kostnadsbeloppet visas alltid i projektets kostnadsvaluta. |


## <a name="submit-material-usage-for-review-and-approval"></a>Skicka materialanvändning för granskning och godkännande 
När du har samlat in all materialanvändning och är redo att godkänna den måste du skicka användningsinformationen för granskning.

1. Gå till **Materialförbrukningslogg** och välj en eller flera poster. Du kan också markera alla materialanvändningsposter med hjälp av kryssrutan i sidhuvudet.
2. Välj **Skicka**. Systemet bearbetar de valda posterna och skapar sedan material begäran om användningsgodkännande.

## <a name="recall-a-material-usage-log"></a>Återkalla loggen för materialförbrukning

Vid behov kan du använda ett material som skickats in. Vilken tid som krävs för att godkänna en materialanvändningspost beror på godkännandestadiet.  Om godkännaren ännu inte har godkänt posten kan återkallelsen ske omedelbart. Om posten redan har godkänts ombeds godkännaren emellertid att godkänna återkallandet och återställa transaktionen.

1. Gå till **Materialanvändning** och välj den materialanvändning som ska användas i listan med materialanvändningsloggar.
2. Välj **återkalla**. Om materialanvändningsposten inte har godkänts ännu gäller den omedelbart för systemet. Om materialposten redan har godkänts skapas en begäran om godkännande så att du meddelar den som godkänner detta material. Godkännaren bekräftar då att återställandet kan utföras och att posten returneras.

## <a name="delete-a-material-usage-log"></a>Ta bort loggen för materialförbrukning

Du kan ta bort materialanvändningsloggar som inte har skickats. Om du vill ta bort en användningslogg för material som redan har skickats måste du först ta bort den.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
