---
title: Översikt över leverantörslagring
description: Den ämne innehåller en översikt över lagringsfunktioner för leverantörer.
author: sigitac
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5f89904af5fb00eac46de834a438f412b371e74e
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594633"
---
# <a name="vendor-retention-overview"></a>Översikt över leverantörslagring

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Organisationen kanske vill behålla en del av betalningarna till leverantörer som arbetar med projekt för organisationen. Innan du till exempel betalar leverantören kanske du vill vara säker på att de objekt och tjänster som de uppställda uppfyller dina förväntningar.

När du för förhandlar köp för projekt med leverantörer kan du ange vilka lagringsvillkor för leverantörer som omfattar den procentandel eller det belopp som ska behållas. När leverantören levererar objekt och tjänster, drar du av den angivna lagringsprocenten eller beloppet från din betalning till leverantören. När projektet är slutfört eller är i ett mellanstadium enligt vad som anges i leverantörskontraktet, frigör du det behållna beloppet och skapar en betalning till leverantören.

## <a name="vendor-retention-example"></a>Exempel på leverantörslagring

I följande exempel visas hur en procentandel av ett leverantörsfakturabelopp behålls baserat på den procentsats som har slutförts för ett projekt.

Contoso Robotics USA har anlitat leverantören Fabrikam för 100 utbildningstimmar för utrustningsförnyelseprojektet. Det totala kontraktvärdet summeras 30 000 USD med ett godkänt inköpspris på 300 USD i timmen.

Utbildningen levereras i tre faser enligt följande schema:

- Fas 1: 50 timmar eller 50 procent av projektet
- Fas 2: 30 timmar eller 80 procent av projektet totalt
- Fas 3: 20 timmar eller 100 procent av projektet

I följande tabell visas lagringsvillkoren.

| **Procent av levererade enheter** | **Kvarhållen procentsats** | **Procentandel att frisläppa** |
| --- | --- | --- |
| 50 % | 20 % | 0 % |
| 80 % | 10 % | 10 % |
| 100% | 0 % | 100% |

Transaktionerna resulterar i följande belopp:

- Fas 1:
  - Det belopp som ska betalas är 50 x 300 eller 15 000.
  - 20 procent av beloppet, eller 3 000, behålls och kommer att släppas senare.
  - Det belopp som betalas till leverantören är 12 000.
- Fas 2:
  - Det belopp som ska betalas är 30 x 300 eller 9 000.
  - 10 procent av beloppet, eller 900, behålls.
  - 10 procent av de 3 000 som behålls i fas 1 eller 300, släpps.
  - Det belopp som betalas till leverantören är 8 400. Det här beloppet är 9 000 mindre än de 900 behållningen plus de 300 som friser ur fas 1-lagringen.
- Fas 3:
  - Det belopp som ska betalas är 20 x 300 eller 6 000.
  - Inget belopp behålls.
  - Det belopp som frigörs är 3 600. Det här beloppet består av de 3 000 som fanns kvar i fas 1, mindre än 300 från fas 1 som gavs ut i fas 2, plus de 900 som fanns kvar i fas 2.
  - Det belopp som betalas till leverantören är 9 600. Beloppet består av ett kvarhållet belopp på 3 600 plus 6 000 för slutförande av fas 3.

Det totala belopp som betalas till leverantören efter att de tre faserna har slutförts är 30 000, vilket är det totala beloppet för ordern (15 000 + 9 000 + 6 000).
