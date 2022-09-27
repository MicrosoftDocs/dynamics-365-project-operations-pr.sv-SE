---
title: Verifiering av leverantörsfakturor med godkända faktiska värden
description: I denna artikel beskrivs hur Microsoft Dynamics 365 Project Operations låter projektansvariga verifiera leverantörsfakturor med de faktiska värden som godkänts när leverantörer utförde arbete och registrerade tid, samt de utgifter och material som använts av projektteammedlemmarna.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522915"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verifiering av leverantörsfakturor med godkända faktiska värden

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Genom Microsoft Dynamics 365 Project Operations kan projektansvariga verifiera leverantörsfakturarader på följande sätt:

- Använd fältet **Verifieringsstatus** på leverantörsfakturaraderna.
- Om leverantörens fakturarader refererar till en underleverantörsrad länkar du de faktiska kostnaderna från underleverantörsaktiviteten till dessa leverantörsfakturarader. Länken skapas genom att matcha faktiska kostnader med leverantörsfakturaraderna.

    > [!NOTE]
    > Även om verifieringsstatus kan spåras för leverantörsfakturarader som inte refererar till en underleverantör, går det inte att länka faktiska kostnader till dessa leverantörsfakturarader.

## <a name="verification-status"></a>Verifieringsstatus

Fältet **Verifieringsstatus** på en leverantörsfakturarad anger verifieringens status. Följande tillstånd stöds:

1. Inte startat
2. Pågår
3. Slutförd

Leverantörsfakturarader med verifieringsstatusen **Inte startad** kan redigeras.

Leverantörsfakturarader med verifieringsstatusen **Pågår** kan inte längre redigeras. För en leverantörsfakturarad som refererar till en underleverantör anges verifieringsstatusen automatiskt som **Pågår** så fort den första faktiska kostnaden matchas med leverantörsfakturaraden.

Leverantörsfakturarader med verifieringsstatusen **Slutförd** kan inte längre redigeras. Om samtliga rader i en leverantörsfaktura har denna verifieringsstatus kan leverantörsfakturan bekräftas.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Matcha faktiska kostnader med leverantörsfakturarader

Matchning av faktiska kostnader underlättar med verifieringsprocessen på en leverantörsfakturarad. Följ stegen nedan om du vill matcha faktiska kostnader med en leverantörsfakturarad.

1. Öppna leverantörsfakturaraden och välj fliken **Faktiska kostnader utan matchning**. I ett rutnät visas en lista över faktiska kostnader som refererar till samma underleverantörsrad som leverantörsfakturaraden.
2. Markera en eller flera av de faktiska kostnaderna och välj sedan **Matcha** i verktygsfältet ovanför rutnätet. Systemet verifierar att de valda faktiska kostnaderna kan matchas. När valideringen har godkänts länkas de faktiska kostnaderna till leverantörsfakturaraden.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Valideringsvillkor som används för att länka faktiska kostnader till leverantörsfakturarader

Under matchningsprocessen kan en länk mellan en faktisk kostnad och en leverantörsfakturarad endast upprättas om båda följande villkor uppfylls:

- Fältet **Justeringsstatus** för respektive vald faktisk kostnad måste vara tomt. Med andra ord får de faktiska kostnaderna inte ha ersatts med andra faktiska kostnader under journalprocesser för återkallande, annullering av godkännande eller korrigering.
- Värdena i följande fält matchas mellan leverantörsfakturaraden och den valda faktiska kostnaden. Om något fält inte anges på leverantörsfakturaraden övervägs det inte för matchning.

    - Projektkontrakt
    - Projektkontraktrad
    - Transaktionsklass
    - Project
    - Aktivitet
    - Resurskategori
    - Transaktionskategori
    - Produkt
    - Kontraktrad för underleverantör
    - Bokningsbar resurs

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Ta bort matchningen mellan faktiska kostnader från en leverantörsfakturarad

Om faktiska kostnader inte matchas kan det också underlätta verifieringsprocessen på en leverantörsfaktura genom att tidigare etablerade länkar kan tas bort. Matchinngen för faktiska kostnader kan endast tas bort från leverantörsfakturarader som har verifikationsstatusen **Pågår**. Följ stegen nedan om du vill ta bort en matchning mellan faktiska kostnader och en leverantörsfakturarad.

1. Öppna leverantörsfakturaraden och välj fliken **Matchade faktiska kostnader**. I ett rutnät visas en lista över faktiska kostnader som refererar till samma leverantörsfakturarad.
2. Markera en eller flera av de faktiska kostnaderna och välj sedan **Ta bort matchning** i verktygsfältet ovanför rutnätet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
