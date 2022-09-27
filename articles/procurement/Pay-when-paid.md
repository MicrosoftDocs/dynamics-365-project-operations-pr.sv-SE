---
title: Använd betalning av leverantör vid betalning
description: Här ämne hur du använder lönen när det betalas (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525347"
---
# <a name="pay-when-paid-vendor-payments"></a>Använd betalning av leverantör vid betalning

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Här ämne hur du använder lönen när det betalas (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Skapa en order med PWP-termer

När du bokför en faktura från en leverantör och leverantören omfattas av PWP-villkoren visas de här villkoren på inköpsorderraderna. Följ stegen nedan om du vill skapa en inköpsorder som innehåller PWP-villkor.

1. I Microsoft Dynamics 365 Finance, följ ett av dessa steg:

    - Gå till **Upphandling och anskaffning** \> **Inköpsorder** \> **Alla inköpsordrar**. I åtgärdsrutan väljer du **Ny**. I dialogrutan **Skapa inköpsorder**, välj leverantören för vilken PWP-villkor är inställda på projektet, ange annan nödvändig information och välj sedan **OK**.
    - Gå till **Projektledning och redovisning** \> **Projekt** \> **Alla projekt**. I åtgärdsfönstret, på fliken **Hantera**, väljer du **Artikeluppgift**. Välj inköpsorder. Välj den leverantör som PWP-termer är konfigurerade för i projektet och välj sedan **OK**.

2. På sidan **Inköpsorder** går du till fliken **Inköpsorderrader** markera **Lägg till rad** för att skapa en inköpsorderrad.
3. Välj artikelnummer eller kategori för verksamhetskategori och ange den övriga information som krävs. Granska informationen om inköpsorderraden för leverantören.

    Alternativet **Betala vid betalning** väljs automatiskt och värdet i fältet **Tröskelprocentsats för PWP** kopieras automatiskt från fältet **Tröskelprocentsats för PWP** på sidan **Projekt**.

4. Om du inte vill använda PWP-villkor för leverantören för en inköpsorderrad avmarkerar du alternativet **Betala vid betalning**. I det här fallet återställs fältet **Tröskelprocentsats för PWP** på inköpsorderraden till **0** (noll).
5. På sidan **Inköpsorder** i åtgärdsfönstret, på fliken **Inköp**, välj **Bekräfta** för att bekräfta inköpsorder.
6. I åtgärdsfönstret på fliken **Faktura**, välj **Faktura** för att generera fakturan för inköpsordern.

## <a name="create-a-project-invoice-proposal"></a>Skapa projektfakturaförslag

Projektfakturaförslag används för att skapa projektfakturor för kunden. I PWP-scenariot är leverantörsbetalningar beroende av kundbetalningar enligt PWP-inställningarna. Det finns emellertid alternativ som gör att du kan släppa betalningarna utan kundbetalningar som du behöver. Följ dessa steg för att skapa en projektfaktura för kunden.

1. I kundengagemangsappar, gå till **Projekt** \> **Projekt** och välj projektet.
2. På fliken **Faktiska värden**, välj den faktiska raden som genereras av den inköpsorder som har transaktionstypen **Ofakturerad**. Välj sedan **Klar för faktura**.
3. Gå till **Försäljning** \> **Försäljning** \> **Projektkontrakt** och markera projektkontraktet.
4. I åtgärdsfönstret, välj **Faktura** för att generera kundfakturan.
5. I Finance, gå till **Projektledning och redovisning** \> **Regelbundet** \> **Importera från mellanlagring** och välj **OK** för att generera integrationsjournalen för Project Operations.
6. Gå till **Projekthantering och redovisning** \> **Projektfakturor** \> **Projektfakturaförslag** och välj **Bokför** för att bokföra fakturaförslaget som genererades för projektet.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Uppdatera en kundbetalning och betala leverantören

När en leverantör har avslutat arbetet med ett projekt och skickar en faktura till dig måste du granska projektstatus och kundfakturor för att avgöra om PWP-villkoren har uppfyllts för projektet. Om PWP-villkoren för leverantören uppfylls kan du avgöra vilka rader på leverantörsfakturan som ska betalas, utifrån kundbetalningarna för projektet. Om du bestämmer dig för att betala leverantören även om PWP-villkoren inte uppfylls kan du åsidosätta PWP-villkoren på sidan **Leverantörsfaktura med betala vid betalning**.

1. I Finance, gå till **Projekthantering och redovisning** \> **Projekt** \> **Alla projekt** och välj ett projekt.
2. I åtgärdsfönstret, välj **Kontroll** och välj **Leverantörsfakturor** som visar alla leverantörsfakturor som har genererats för projektet.
3. På sidan **Leverantörsfaktura med betala vid betalning**, i sökfältet, anger du värden för att söka efter den leverantörsfaktura du vill granska, och väljer sedan **Sök**.
4. Välj alternativet **Betala när betald** om du endast vill visa PWP-fakturor.
5. Under snabbfliken **Leverantörsfakturarader** väljer du de rader du vill släppa för betalning.
6. Välj **Släpp leverantörsbetalning**. Alternativet **Betala vid betalning** rensas och värdet i fältet **Klar för betalning** ändras till **Ja**.
