---
title: Fakturera arvode eller förskott - lite
description: I det här ämnet finns information om hur du fakturerar ett arvode eller förskott i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9013529b615026eab92177c9fd9fb84c50d66f4f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180574"
---
# <a name="invoice-a-retainer-or-an-advance---lite"></a>Fakturera arvode eller förskott - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Dynamics 365 Project Operations stöder arvode-baserade kontrakt och engångsförskott. I ett projektkontrakt kan du registrera ett schema över arvoden eller engångsförskott. Registrering på projektkontraktsnivå gör emellertid inte direkt ett arvode eller förskott tillgängligt för användning. Om du vill använda ett arvode eller förskott på en faktura som faktiskt debiterar kunden, måste arvodet eller förskottet faktureras först.

Slutför stegen nedan om du vill fakturera ett arvode eller förskott.

1. Välj **Försäljning** > **Fakturering** > **Arvoden och förskott**. 
2. På sidan **Förskott och arvoden** använder du filtret för att välja specifikt arvode eller förskott att fakturera och markera det som **Redo att fakturera**.
3. Skapa en faktura antingen manuellt från listan **Projektkontrakt** eller på sidan detaljerad lista. Arvodet eller förskottet visas i utkastfakturan i avsnittet **Förskott och arvoden** på sidan **Faktura**.
4. Bekräfta fakturan. På så vis blir arvodet eller förskottet tillgängligt för användning. Du kan verifiera fakturan på listsidan **Arvoden och förskott**. För ett fakturerat förskott eller arvode visas det tillgängliga beloppet i rutnätet.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Skapa ett arvode eller förskott från fakturarutnätet

Du kan skapa ett arvode eller förskott direkt på en faktura.

1. På ett utkast till en faktura går du till underrutnätet **Förskott och arvoden** och väljer **Nytt** för att skapa ett nytt arvode eller förskott. 
2. På sidan **Snabbskapa** lägger du till nödvändig information och väljer sedan **Spara**. Arvodet eller förskottet skapas i projektkontraktet som är relaterat till fakturan. Arvodet eller förskottet markeras automatiskt som **Redo att faktureras** och läggs sedan till i underrutnätet **Förskott och arvoden** på sidan **Faktura**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Stäm av ett fakturerat arvode eller förskott

När ett arvode eller förskott har fakturerats kan de användas eller stämmas av på en faktura med tid, utgifter, milstolpar eller andra projektbaserade avgifter. Kunden ser att fakturabeloppet har reducerats med arvodes- eller förskottsbeloppet som används på fakturan.

På alla fakturor som genereras för ett projektkontrakt som har fakturerade arvoden eller förskott tillämpar Project Operations automatiskt arvodet eller förskottet på fakturan.

Detta kan du se i rutnätet **Tillämpade arvoden och förskott** på sidan **Faktura**. I följande tabell finns information om fälten i rutnätet **Tillämpade arvoden och förskott** på sidan **Projektfaktura**.

| Fält | Plats | Beskrivning | Inverkan nedströms |
| --- | --- | --- | --- |
| Beskrivning | Rutnätet **Tillämpade förskott och arvoden** på sidan **Projektfaktura** |Det här skrivskyddade fältet innehåller en beskrivning av arvodet eller förskottet som används på fakturan. Det här värdet kan inte ändras på fakturan. Det här värdet kan uppdateras i underrutnätet på sidan **Projektkontrakt**. | Fältet kan visas för kunden på den utskrivna fakturan för att ange vilket arvode eller förskott som ska tillämpas på fakturan. |
| Levererades den | Rutnätet **Tillämpade förskott och arvoden** på sidan **Projektfaktura**  | Det här skrivskyddade fältet innehåller fakturadatumet för arvodet eller förskottet som används på fakturan. Det här värdet kan inte ändras på fakturan. Det här värdet kan uppdateras i underrutnätet på sidan **Projektkontrakt**. | Fältet kan visas för kunden på den utskrivna fakturan för att ange det datum då arvodet eller förskottet först fakturerades kunden. |
| Belopp | Rutnätet **Tillämpade förskott och arvoden** på sidan **Projektfaktura**  | Det här skrivskyddade fältet innehåller beloppet för arvodet eller förskottet som används på fakturan. Det här värdet kan inte ändras på fakturan. Det här värdet kan uppdateras i underrutnätet på sidan **Projektkontrakt**. | Fältet kan visas för kunden på den utskrivna fakturan för att ange det ursprungliga beloppet på arvodet eller förskottet som betalades av kunden. |
| Använt belopp | Rutnätet **Tillämpade förskott och arvoden** på sidan **Projektfaktura**  | Det här skrivskyddade fältet innehåller det beräknade värdet som sammanfattar hur mycket av arvodet eller förskottet som har använts. | Fältet kan visas för kunden på den utskrivna fakturan för att ange beloppet av arvodet eller förskottet som redan använts. |
| Utökat belopp | Rutnätet **Tillämpade förskott och arvoden** på sidan **Projektfaktura**  | Det här redigerbara fältet innehåller beloppet för arvodet eller förskottet som används på projektfakturan. Det här beloppet får inte vara mer än vad som är tillgängligt i förskottet. Systemet beräknar detta automatiskt som skillnaden mellan fälten **Belopp** och **Använt belopp** i rutnätet. Du kan minska det här beloppet om du vill använda mindre än vad som är tillgängligt, men du kan inte öka beloppet som ska användas till mer än vad som är tillgängligt. | Fältet kan visas för kunden på den utskrivna fakturan för att ange beloppet av arvodet eller förskottet som används på fakturan. |
| Saldo för arvodesbelopp. | Rutnätet **Tillämpade förskott och arvoden** på sidan **Projektfaktura**  | I det här skrivskyddade fältet visas värdet för hur mycket av arvodet eller förskottet som är kvar efter det att fakturan bekräftas. | Fältet kan visas för kunden på den utskrivna fakturan för att ange beloppet som är kvar av arvodet eller förskottet efter det att fakturan bekräftas och betalas. |
