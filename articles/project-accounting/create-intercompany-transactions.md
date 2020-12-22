---
title: Skapa koncerninterna transaktioner
description: Detta ämne innehåller information om hur du skapar koncerninterna transaktioner.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a9d34d69ff59f0cb470bb852d8a80ecaedf6544
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595565"
---
# <a name="create-intercompany-transactions"></a>Skapa koncerninterna transaktioner

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Koncerninterna transaktioner är tids- och utgiftstransaktioner från ett projektkontrakt som tillhör ett företag eller en organisationsenhet, medan resurserna i projektkontraktet ingår i ett annat företag eller en annan organisationsenhet.

När en koncernintern transaktion godkänns skapas följande faktiska transaktioner

| **Transaktionstyp** | **Tillämpad prislista** | **Transaktionsvaluta** |
| --- | --- | --- |
| Kostnad | Kostnadsprislista för entreprenadenhet | Valuta på prisraden |
| Icke-fakturerad försäljning. Dessa skapas endast för faktiska värden som är kopplade till en kontraktrad med faktureringstyp, tid och material. | Prislista för kontraktets projektförsäljning | Kontraktets valuta |
| Kostnad för resursenhet | Kostnadsprislista för resursenhet | Valuta på prisraden |
| Försäljning inom organisationsenhet | Kostnadsprislista för entreprenadenhet | Valuta på prisraden |

Kostnad, kostnad för resursenhet och transaktionspriser för organisationsenhetsintern försäljning och valuta drivs av **organisationsenheten**. Detta är viktigt att komma ihåg när man bestämmer hur du strukturerar företag och organisationsenheter i din implementering.

När du skapar affärsmöjlighets-, offert-, projektkontrakts- och projektposter verifierar systemet att entreprenadenhetens valuta matchar entreprenadföretagets redovisningsvaluta. När dessa inte är identiska kan dessa poster inte skapas. Den organisatoriska enhetsvalutan definieras i Dynamics 365 Project Operations genom att gå till **Dataverse** > **Inställningar** > **Organisationsenheter**. Ett företags redovisningsvaluta definieras i Dynamics 365 Finance genom att gå till **Huvudbok** > **Konfigurering av huvudbok** > **Redovisning**. Valutan synkroniseras med din Dataverse-miljö med hjälp av Ledgers Dual Write-mappningen.

Systemet skapar kostnad för resursenhet och organisationsenhetsintern faktisk försäljning i följande situationer:

  - När resursenheten skiljer sig från entreprenadenheten
  - När resursenhetens företag skiljer sig från entreprenadföretaget

Det är dock bara transaktioner som har ett annat resursföretag än entreprenadföretaget som kommer att överföras till Dynamics 365 Finance-miljön för ytterligare redovisning.

Redovisning av verkliga projektvärden registreras i integreringsjournalen för Project Operations i Finance. Systemet skapar följande journalrader.

| **Transaktionstyp** | **Juridisk person** | **Skapar projekttransaktion vid bokföring** | **Standardvärden för ekonomisk dimension från** | **Standardmomsgrupp för fakturering och momsgrupp för faktureringsartikel** |
| --- | --- | --- | --- | --- |
| Kostnad | Läggs inte till i integreringsjournalen | N\A | N\A | N\A |
| Ofakturerad försäljning | Integreringsjournal för låntagande juridiska enhet | Ja | Project | **Momsgrupp för fakturering**: Baserat på **kontraktskunden** <br/> **Momsgrupp för faktureringsartikel**: Från den aktuella projektkategorin för juridisk person på journalraden |
| Kostnad för resursenhet | Integreringsjournal för utlånande juridiska enhet | Inga | Koncernintern kund | **Momsgrupp för fakturering**: Baserat på **koncernintern kund** <br/> **Momsgrupp för faktureringsartikel**: Från den aktuella projektkategorin för juridisk person på journalraden |
| Koncernintern försäljning | Integreringsjournal för utlånande juridiska enhet | Inga | Koncernintern kund | **Momsgrupp för fakturering**: Baserat på **koncernintern kund** <br/> **Momsgrupp för faktureringsartikel**: Från den aktuella projektkategorin för juridisk person på journalraden |

### <a name="example-intercompany-transactions"></a>Exempel: koncerninterna transaktioner

Molly Clark, utvecklare anställd inom GBPM, registrerar 10 timmars arbete mot ett USPM Adventure Works-projekt som har godkänts av projektledaren. Utvecklarkostnad i GBPM är 88 GBP per timme. GBPM kommer att fakturera USPM 120 USD per utvecklartimme. USPM kommer att fakturera kunden Adventure Works 200 USD för arbete som utförs av GBPM-resursen. Mer information finns i [Konfigurera koncernintern fakturering](configure-intercompany-invoicing.md).

1. I Project Operations går du till **Resurser** och väljer **Molly Clark** i listan. På fliken **Schemaläggning**, i fältet **Företag**, väljer du **GBPM**.
2. Gå till **Försäljning** > **Kunder** och välj **Ny** för att skapa en ny kundpost för Adventure Works.
    1. Ange företaget som **USPM**.
    2. Ange **Relationstyp** som **Kund**.
    3. Välj **Kundgrupp 10 – Inrikes**.
    4. Ange valutan som **USD**.
    5. Spara posten.
3. Gå till **Försäljning** > **Projektkontrakt** och skapa ett nytt projektkontrakt för Adventure Works.
    1. Ställ in det egna företaget som **USPM** och entreprenadenheten som **Contoso Robotics US**.
    2. Välj Adventure Works som kund.
    3. Välj en produktprislista och spara posten.
    4. Skapa en ny kontraktrad i fliken **Kontraktrader**. Ange valfritt namn och välj **Tid och material** som faktureringsmetod.
    5. Skapa ett nytt projekt och koppla det till den här kontraktraden.
4. Logga in som resursen **Natasha Hansson**. Gå till **Projekt** > **Tidsposter** och skapa en tidspost för projektet Adventure Works.
5. Logga in som projektledare. Gå till **Projekt** > **Godkännanden** och godkänn den tidstransaktionstransaktion som loggats av Natasha Hansson.
6. Navigera till Adventure Works-projektet och välj **Relaterat** > **Faktiska värden**. Följande verkliga transaktioner skapas.

| **Transaktionstyp** | **Pris** | **Transaktionsvaluta** | **Belopp** |
| --- | --- | --- | --- |
| Kostnad | 120 | USD | 1200 |
| Ofakturerad försäljning | 200 | USD | 2000 |
| Kostnad för resursenhet | 88 | GBP | 880 |
| Försäljning inom organisationsenhet | 120 | USD | 1200 |

7. Logga in som USPM-revisor. Öppna Finance-instansen av Project Operations och välj företaget **USPM**. 
8. Gå till **Projektledning och redovisning** > **Periodisk** > **Project Operations för Customer Engagement** > **Importera från mellanlagring** och välj att köra den periodiska processen. Den här periodiska processen kommer att fylla i integrationsjournalen för Project Operations.
9. Gå till **Projektledning och redovisning** > **Journaler** > **Integrationsjournal för Project Operations** och granska journalraderna. Systemet skapar följande rad.

    | **Transaktionstyp** | **Pris** | **Transaktionsvaluta** | **Belopp** |
    | --- | --- | --- | --- |
    | Ofakturerad försäljning | 200 | USD | 2000 |

    Om systemet har ställts in för att periodisera intäkter för det här projektet bokförs följande:

    - Debet: Projekt – PIA-försäljningsvärde 200 USD
    - Kredit: Projekt – Periodiserade intäkter 200 USD

    Denna icke-fakturerade försäljning är nu redo för fakturering. Fakturan för kunden Adventure Works kan bokföras ekonomiskt när så behövs.

10. Logga in som **GBPM**-revisor. Öppna Finance-instansen av Project Operations och öppna företaget **GBPM**. 
11. Gå till **Projektledning och redovisning** > **Periodisk** > **Project Operations för Customer Engagement** > **Importera från mellanlagring** och kör den periodiska processen för att fylla i integrationsjournalen för Project Operations.
12. Gå till **Projektledning och redovisning** > **Journaler** > **Integrationsjournal för Project Operations** och granska raderna. Systemet skapar följande rader.

    | **Transaktionstyp** | **Pris** | **Transaktionsvaluta** | **Belopp** |
    | --- | --- | --- | --- |
    | Kostnad för resursenhet | 88 | GBP | 880 |
    | Försäljning inom organisationsenhet | 120 | USD | 1200 |

    Bokföring av dessa poster resulterar i följande verifikationstransaktioner:

    - Debet: Projektkostnad 88 GBP
    - Kredit: Löneallokering 88 GBP

    Om systemet har ställts in för att periodisera koncerninterna intäkter för det här projektet bokförs följande:

    - Debet: Projekt – PIA-försäljningsvärde 120 USD
    - Kredit: Projekt – Periodiserade intäkter 120 USD

    Systemet är nu redo att skapa en koncernintern kundfaktura.
