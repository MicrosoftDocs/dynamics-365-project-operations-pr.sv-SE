---
title: Konfigurera och använd betalning av leverantör vid betalning
description: I den här artikeln beskrivs hur du skapar villkor för betala vid betalning (PWP) så att du kan frisläppa leverantörsbetalningar för delbelopp baserat på kundbetalningar.
author: RadhikaRS
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 10e8e57695caece6c4b6ba4c2ddb52395dad1218
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920772"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Konfigurera och använd betalning av leverantör vid betalning

[!include [banner](../includes/banner.md)]

När du godkänner en leverantör att arbeta som en underleverantör kanske du vill kvarhålla betalning till leverantören tills kunden betalar för projektet. För att det här scenariot ska stödjas kan du ställa in villkoret att betala vid betalning (PWP) när du konfigurerar inköpsordern (PO) med leverantören.

När en kund t.ex. betalar ett belopp på en projektfaktura kan du släppa en del av eller hela leverantörsfakturabeloppet. Ange bara PWP-villkor som anger att leverantören kommer att betalas efter att du har fått en procentandel av den relaterade betalningen från kunden. Om du tar emot en delbetalning från en kund kan du manuellt släppa vissa av de relaterade leverantörsfakturorna för betalning.

I följande exempel beskrivs processen när PWP-villkor används.

## <a name="example"></a>Exempel

Din organisation accepterar att förse en kund med 100 datorer som har installerad programvara, till ett pris på 150,00 dollar (USD) per dator. Du anställer sedan en leverantör för att förse dig med de datorer som har en installerad programvara. Enligt avtalet måste kunden godkänna datorns kvalitet innan den betalar organisationen. Organisationens policy är att kvarhålla betalning till leverantörer tills kunden har betalat dig. Därför konfigurerar du projektet så att det har en PWP-procent på 100 procent.

Leverantören skickar dig de 100 datorer som har installerad programvara, tillsammans med en faktura på 10 000,00 USD. Eftersom PWP-villkor har konfigurerats för projektet betalar du inte leverantören vid mottagandet av datorerna. Du skickar i stället datorerna till kunden tillsammans med en faktura på 15 000,00. Kunden inspekterar datorerna och godkänner hela beloppet på projektfakturan.

När du har fått full betalning från kunden betalar du leverantören 10 000,00, hela beloppet på leverantörsfakturan.

## <a name="set-up-pwp-terms-for-a-project"></a>Ange PWP-villkor för ett projekt

När du ställer in PWP-villkor för ett projekt måste du ange i procent det minimibelopp som en kund ska betala för projektet innan du ska betala leverantören. Tröskelbeloppet beräknas automatiskt på kundfakturorna för projektet. Följ stegen nedan om du vill konfigurera tröskelprocentsatsen för PWP-villkor.

1. Gå till **Projektledning och redovisning** \> **Projekt** \> **Alla projekt**.
2. Sök efter och öppna det projekt som du vill konfigurera PWP-villkor för.
3. Under snabbfliken **Leverantörsavtal** väljer du **Lägg till rad**.
3. I fältet **Kontokod** väljer du något av följande alternativ:

    - **Tabell** – PWP-villkor gäller för en enskild leverantör.
    - **Grupp** – PWP-villkor gäller för alla leverantörer i en leverantörsgrupp.
    - **Alla** – PWP-villkor gäller för alla leverantörer.

4. Om du valde **Tabell** eller **Grupp** i föregående steg väljer du, i fältet **Leverantör/leverantörsgrupp**, den leverantör eller leverantörsgrupp som PWP-villkoren gäller för. Om du valde **Alla** i föregående steg går det inte att redigera fältet **Leverantör/leverantörsgrupp**.
5. Om villkoren för leverantörskvarhållande har konfigurerats för leverantören i projektet väljer du , i fältet **Villkor för leverantörskvarhållning**, ID för regeln för kvarhållningsvillkoren.
6. I fältet **Tröskelprocentsats för PWP** anger du tröskelprocentsatsen för projektet. Procentsatsen som du anger för projektet anger det minsta belopp som kunden måste betala innan du ska betala leverantören.

## <a name="create-a-po-that-has-pwp-terms"></a>Skapa en inköpsorder som innehåller PWP-villkor

När du bokför en faktura från en leverantör och leverantören omfattas av PWP-villkoren visas de här villkoren på inköpsorderraderna. Följ stegen nedan om du vill skapa en inköpsorder som innehåller PWP-villkor.

1. Gå till **Upphandling och anskaffning** \> **Inköpsorder** \> **Alla inköpsordrar**.
2. I åtgärdsrutan väljer du **Ny**. I dialogrutan **Skapa inköpsorder** anger du sedan den information som krävs och väljer **OK**.

    Alternativt kan du öppna en befintlig inköpsorder på listsidan **Alla inköpsordrar**.

4. På sidan **Inköpsorder**, under snabbfliken **Inköpsorderrader**, går du igenom informationen på inköpsorderraden för leverantören. Alternativet **Betala vid betalning** väljs automatiskt och värdet i fältet **Tröskelprocentsats för PWP** kopieras automatiskt från fältet **Tröskelprocentsats för PWP** på sidan **Projekt**.
6. Om du inte vill använda PWP-villkor för leverantören för en inköpsorderrad avmarkerar du alternativet **Betala vid betalning**. I det här fallet återställs fältet **Tröskelprocentsats för PWP** på inköpsorderraden till 0 (noll).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Uppdatera en kundbetalning och betala leverantören

När en leverantör har avslutat arbetet med ett projekt och skickar en faktura till dig måste du granska projektstatus och kundfakturor för att avgöra om PWP-villkoren har uppfyllts för projektet. Om PWP-villkoren för leverantören uppfylls kan du avgöra vilka rader på leverantörsfakturan som ska betalas, utifrån kundbetalningarna för projektet. Om du bestämmer dig för att betala leverantören även om PWP-villkoren inte uppfylls kan du åsidosätta PWP-villkoren på sidan **Leverantörsfaktura med betala vid betalning**.

1. Gå till **Projektledning och redovisning** \> **Frågor och rapporter** \> **Frågor om kvarhållning** \> **Leverantörsfaktura med betala vid betalning**.
2. På sidan **Leverantörsfaktura med betala vid betalning**, i sökfältet, anger du värden för att söka efter den leverantörsfaktura du vill granska, och väljer sedan **Sök**.
3. Under snabbfliken **Leverantörsfakturarader** väljer du de rader du vill ändra.
4. Om villkoren för **Betala vid betalning** uppfylls för fakturaraden väljer du **Släpp leverantörsbetalning**. Alternativet **Betala vid betalning** rensas och värdet i fältet **Klar för betalning** ändras till **Ja**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]