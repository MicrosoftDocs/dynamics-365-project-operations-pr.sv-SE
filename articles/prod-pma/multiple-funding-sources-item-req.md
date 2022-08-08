---
title: Artikelkrav för projektkontrakt med flera finansieringskällor
description: Denna artikel ger information om hur du konfigurerar och använder objektkrav med flera finansieringskällor.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028510"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Artikelkrav för projektkontrakt med flera finansieringskällor

_**Gäller för:** Project Operations för lagerbaserade/produktionsbaserade scenarier_

Vissa kontraktavtal om projektbaserade slutkontrakt kan kräva flera finansieringskällor. I denna artikel beskrivs hur du väljer och konfigurerar önskade finansieringskällor när flera källor krävs för ett projekt eller ett projektkontrakt.

## <a name="terminology"></a>Terminologi

- **Finansieringskälla** – Den entitet som finansierar projektkontraktsarbetet. Denna entitet kan vara en intern organisation eller ett externt fakturakonto (kund eller beviljande).
- **Projektkund** – Den entitet som projektarbetet levereras till.
- **Fakturakonto** – Den externa entitet som betalar för projektarbetet.

## <a name="example"></a>Exempel

Contoso har vunnit ett kontrakt för utrustningsförnyelse med två av sina kunder: Adatum US och Adatum Corporate. Kontraktet innehåller maskinvaru- och installationstjänster som kommer att levereras till Adatum USA (projektkunden). Maskinvaran finansieras av Adatum Corporate (fakturakonto 1) och installationsarbetet av Adatum US (fakturakonto 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Konfigurera standardregler för artikelkrav för fakturakonto

### <a name="prerequisites"></a>Förutsättningar

- Microsoft Dynamics 365 Finance **version 10.0.27** eller senare krävs för att kunna använda artikelkrav som har flera fakturakonton.
- Systemadministratören måste aktivera funktionen **Tillåt artikelbehov med flera finansieringskällor för Product Operations-scenarier med lager/produktionsbaserade sådana** i arbetsytan **Funktionshantering**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Konfigurera standardregler för fakturakonto

Konfigurera standardreglerna för fakturakontot genom att följa stegen nedan.

1. Gå till **Projektledning och redovisning** \> **Konfiguration** \> **Parametrar för projektledning och redovisning**.
1. På fliken **Allmänt** går du till avsnittet **Krav för försäljningsorder och artiklar** och anger alternativet **Tillåt för projekt med flera källor** som **Ja**.
1. I fältet **Standardkund** anger du var projektleveranskunden för artikelkravet kommer från som standard:

    - **Från finansieringskällan** – Standard-projektleveranskunden kommer från finansieringskällan. Om flera finansieringskällor är kopplade till projektkontraktet används den första finansieringskällan i listan.
    - **Från projekt** – Standardkunden för projektleverans kommer från den kund som har valts i fältet **Projektpostkonto**.

1. Valfritt: Ange eller ändra standardfakturakontot för projektposter:

    1. Gå till **Projekthantering och redovisning** \> **Projekt** \> **Alla projekt** och öppna projektpostinformationen.
    2. På fliken **Allmänt** ställer du in eller uppdaterar fältet **Standardkonto för faktura**. Kontot du anger används som standardfakturakonto för nya artikelkrav som skapas för projektet. Om fältet är tomt används som standard fakturakontot för det första projektkontraktet som finansieringskälla. Användare kan emellertid ändra kontot när de sparar posten.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Välj vilket fakturakonto som ska användas när du skapar ett artikelkrav

Följ dessa steg för att välja vilket fakturakonto som ska användas när du skapar ett artikelkrav.

1. Gå till **Projekthantering och redovisning** \> **Projekt** \> **Alla projekt** och välj projektposten.
1. På fliken **Plan** väljer du **Artikelkrav**.
1. Skapa en ny post för artikelkrav.

    - Som standard är fältet **Fakturakonto** i posten inställt på det fakturakonto som har angetts för projektet. Du kan ändra värdet för fältet **Fakturakonto** och sedan spara posten. När posten har sparats kan du inte längre uppdatera värdet **Fakturakonto**. Om du måste uppdatera värdet **fakturakonto** för artikelkravet tar du bort det befintliga artikelkravet och skapar sedan ett nytt som har det önskade värdet.
    - Som standard anges fältet **Kund** för artikelkravet utifrån det värde för **Standardkund** som anges på sidan **Projekthanterings- och redovisningsparametrar**.

    När posten för artikelkrav sparas associeras posten med huvudposten för **Försäljningsorder för artikelkrav**. Om det inte finns något öppet försäljningsorderhuvud som har det valda fakturakontot skapar systemet ett och associerar artikelbehovsraden med det.

> [!NOTE]
> Artikelkraven faktureras alltid helt till det fakturakonto som anges i posten. Systemet stöder för närvarande inte allokeringsregler som har artikelkrav och delar inte upp inlägget baserat på inställningarna för allokeringsregler.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Skapa ett artikelkrav från en objektprognospost

Följ dessa steg för att skapa ett artikelkrav från en artikelprognospost.

1. Gå till **Projekthantering och redovisning** \> **Projekt** \> **Alla projekt** och välj projektposten.
1. På fliken **Plan** väljer du **Artikelprognoser**.
1. Skapa en ny post för artikelprognos.
1. Valfritt: I fliken **Projekt** väljder du önskat fakturakonto i fältet **Finansieringskälla**.
1. Välj **Skapa artikelkrav** och bekräfta meddelandet som du tar emot.

    > [!NOTE]
    > Systemet kopierar värdet **Finansieringskälla** från artikelprognosposten till den nyligen skapade artikelkravsposten.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Standardfakturakonto när systemet automatiskt skapar ett artikelkrav från en inköpsorderrad

Om alternativet **Skapa artikelkrav** har angetts som **Ja** på sidan **Projekthanterings- och redovisningsparametrar** skapar systemet automatiskt ett artikelkrav när en ny orderrad för projektinköp sparas. Som standard anges värdet i fälten **Fakturakonto** och **Artikelkrav** som i fältet **Standardkonto för faktura** i projektposten. Systemet stöder för närvarande inte uppdatering eller ändring av fakturakontot för poster av den här typen.
