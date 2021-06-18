---
title: Översikt över resursutnyttjande
description: I den här ämnet finns information om vyn resursanvändning i Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000818"
---
# <a name="resource-utilization-overview"></a>Översikt över resursutnyttjande

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Resurser kan ha fakturerbar användning. Den här målanvändningen definieras som ett attribut för en resurs standardroll eller anges i posten för den enskilda bokningsbara resursen. Användningsberäkningar baseras på de faktiska timmarna som resurserna har rapporterat med hjälp av godkända tidtransaktioner.

Följande formler används för att beräkna användningen:

  - Fakturerbar användning = debiterbara faktiska timmar ÷ resurskapacitet för tillgång
  - Användning av ej fakturerbar tid = faktisk tid med faktureringstyp-ID = inte debiterbar, komplementär eller ej disponibelt ÷ resurskapacitet
  - Intern = faktisk tid utan försäljningskontrakt ÷ resurskapacitet
  - Resurskapacitet = resursens arbetstider – frånvarande – lediga dagar

Du hittar vyn **Resursutnyttjande** i fönstret **Resurser**.

Varje cell i rutnätet representerar resursens fakturerbara användningsprocent i en period, t.ex. dag, vecka eller månad. Följande formler används för att färglägga cellerna:

  - **Grön**: fakturerbart resursutnyttjande >= resursutnyttjande för målet.
  - **Gul**: mål för resursutnyttjande – 20 <= fakturerbart resursutnyttjande < mål för resursutnyttjande
  - **Röd**: fakturerbart resursutnyttjande < mål för resursutnyttjande – 20

Eftersom vyn **Resursutnyttjande** baseras på schemaläggningstavlan kan du filtrera resultaten med hjälp av filtreringsfunktionerna i schemaläggningstavlan.

Rutnätet kräver att du anger ett utnyttjandemål för antingen rollen eller den enskilda resursen. För att göra detta går du till **Resurser** > **Resursroller**.

Dessutom måste en standardroll tilldelas varje bokningsbar resurs. Gå till **Resurser** > **Resurser**. På fliken **Project Service** kontrollera att en resursroll är definierad och att fältet **är standard** anges till **ja**. Du kan lägga till ytterligare roller där **är standard** = **Nej**. Rollen där **är standard** = **Ja** används för att utvärdera resursutnyttjande för resursen mot målet för rollen.

På fliken **Project Service** kan du också ange ett enskilt målutnyttjande för resursen. Utnyttjandeberäkningen använder då målutnyttjande för att utvärdera resursens mål i stället för resursens standardroll.

Utnyttjande visas endast för en resurs om resursen har godkänt, debiterbar tid under den period som visas i rutnätet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]