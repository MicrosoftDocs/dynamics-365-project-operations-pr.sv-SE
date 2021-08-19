---
title: Konfigurera kostnadsmallar
description: I det här ämnet finns information om hur du skapar och använder kostnadsmallar i Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b3a9f1e4f5ea0abe34dc860db87ef349daa46c487b03d271bfe207868c521f39
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993578"
---
# <a name="set-up-cost-templates"></a>Konfigurera kostnadsmallar

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_


I det här ämnet finns information om hur du skapar och använder kostnadsmallar i Project Operations. En kostnadsmall bestämmer:

- Projektkategorierna för prognos- och faktiska transaktioner som ska ingå i en procentandel av beräkningen av projektslutförandet. Procentandelsvärdet för slutförande används sedan för att beräkna hur mycket intäkter som redovisas.
- Huruvida slutförandeprocenten kan ändras om den beräknas automatiskt.
- Huruvida procentandelen för slutförande beräknas baserat på belopp eller enheter.

## <a name="cost-template-example"></a>Exempel på kostnadsmall

Du arbetar med ett projekt för webbplatsdesign för en kund där du tar ut en fast avgift på 10 000 dollar. Du prognostiserar att det kommer att ta 100 timmar (5 000 dollar) för att slutföra projektet. Du prognostiserar även två flygbiljetter och fyra nätter på ett hotell för resor till kundens anläggning (1 800 dollar). Detta resulterar i en total prognostiserad kostnad på USD 6 800.

När du kör processen för intäktsredovisning av fast pris för att skapa en uppskattning i slutet av månaden upptäcker du att du har arbetat 35 timmar med projektet. Detta inkluderar ännu inte flyg- eller hotellkostnader. Du lät också en assistent utföra fem timmars forskning för projektet till en kostnad av USD 100 som du inte hade planerat för.

När du beräknar procentandelsvärdet för slutförande för det här projektet har du följande val att göra:

- Vill du inkludera alla kostnader (timmar och utgifter) eller bara timmar?
- Vill du inkludera alla timmar eller endast planerade timmar?
- Vill du beräkna procentandelsvärdet för slutförande baserat på dollarkostnaden för de planerade timmarna (USD 5 000) eller bara på antalet timmar (100)?

Dina svar på dessa frågor avgör vilka alternativ som du anger för kostnadsmallen och de kategorier som du väljer på kostnadsmallraderna.

Följande tabell illustrerar resultaten av olika metoder för beräkning av värdet för procentandelsvärdet för slutförande för det här scenariot.

| Slutförande baserat på | Dollarkostnad eller enheter | Procent slutfört | Beräkning |
| --- | --- | --- | --- |
| Alla timmar, inga utgifter | Dollarkostnad | 37 % 35 x USD 50 + USD 100 = USD 1 850 USD 1 850/USD 5 000 |
| Alla timmar, inga utgifter | Enheter | 40 % | 40 timmar/100 timmar (inklusive fem oplanerade timmar) |
| Planerade timmar, inga utgifter | Dollarkostnad eller enheter | 35 % | 35/100 timmar eller 35 x USD 50/5 000 |
| Alla timmar och utgifter | Dollarkostnad | 27,2 % | USD 1 850/USD 6 800 |

Att bestämma vilken metod som ska implementeras för att skapa en kostnadsmall kan bero på flera olika överväganden:

- Om du tar med oplanerade timmar i kostnadsmallen riskerar du att nå 100 procent färdigställande innan projektet är färdigt. Detta beror på att faktiska timmar kommer att vara större än planerade timmar. Om du använder någon av de två första metoderna som anges i tabellen bör du ändra planen (prognostiserade enheter) när du får kännedom om avvikelser. I det här fallet skulle du lägga till eller subtrahera timmar baserat på dina kunskaper om vad som krävs för att avsluta projektet. Om projektet kräver ytterligare 65 timmar för att slutföras skulle du lägga till fem timmar i planen och totalt få 105. Om du vet att din assistent kommer att utföra ytterligare fem timmars forskning uppgår totalen till 110 timmar.
- Om du använder den tredje metoden som anges i tabellen skulle du bara uppdatera de planerade timmarna för din egen tid i syfte att hålla beräkningen av procentandelsvärdet korrekt. Din lönsamhet kommer att förändras när oplanerade timmar loggas, men du kommer att förbli på en känd bana för procentandelsvärdet för slutförande.
- Om du använder den fjärde metoden som anges i tabellen är risken att utgifter kommer att dyka upp vid oregelbundna tidpunkter och kanske inte återspeglas i ditt slutförandeförlopp. Om utgifterna inkluderas kan de därför få din slutförda procentandel att fluktuera mer än vad som är önskvärt. Till exempel: Eftersom du ännu inte flugit uppgick din slutförandeprocent till 27 procent istället för 35 procent eller 37 procent om du skulle basera beräkningen enbart på tid. Om du hade tagit en tvådagarsresa och prognostiserat dina flyg- och hotellkostnader exakt hade procentandelsvärdet för slutförande uppgått till 40,4 procent (USD 1 850 för arbetskraft och USD 900 för kostnader = USD 2 750 / USD 6 800 = 40,4 procent). Att ådra sig kostnaderna för en enda flygresa skulle därför ändra procentandelsvärdet för slutförande från 27 procent till 40 procent.

## <a name="create-cost-templates"></a>Skapa kostnadsmallar
Skapa kostnadsmallar genom att följa stegen nedan:

1. Om du vill komma åt kostnadsmallar i Dynamics 365 Finance-miljön går du till **Projektledning och redovisning** > **Konfiguration** > **Uppskattningar** > **Kostnadsmall**.
2. Välj **Ny** för att skapa en ny kostnadsmall. Ange ett namn och en beskrivning.
3. Tillhandahåll kostnadsrads-ID för respektive transaktionstyp.
4. Välj en standardmetod för slutförande:

  - **Automatisk**: Slutförandeprocenten beräknas automatiskt på ett projekt. Det resulterande värdet får inte ändras.
  - **Manuell**: Slutförandeprocenten beräknas automatiskt på ett projekt. Det resulterande värdet kan ändras.

  > [!NOTE]
  > För manuella beräkningar bibehålls slutförandeprocenten i **Manuell beräkning** på fliken **Allmänt** på sidan **Uppskattning**.

5. I **Slutförande baserat på** väljer du ett av följande värden:

  - **Belopp**: Beloppet i redovisningsvalutan beräknar slutförandeprocenten.
  - **Enhet**: Kvantiteten beräknar slutförandeprocenten.
  - **Rak linje**: Systemet beräknar slutförandeprocenten på proportionell basis genom att använda projektets start- och slutdatum för att bestämma projektets längd.

6. Välj **Kostnadsrader** för att granska kostnadsraderna i kostnadsmallen. Minst en kostnadsrad krävs för varje transaktionstyp. Du kan dock skapa flera kostnadsrader för samma transaktionstyper och ange önskade attribut för dessa rader.
7. Välj fliken **Kategorier** och välj de projektkategorier som ska ingå på kostnadsmallraden.
8. I fliken **Allmänt** väljer du om den här raden ska inkluderas i beräkningen av procentandelsvärdet för slutförande.
9. Välj den kostnad för slutförandemetod som ska användas vid beräkning av slutförandeprocenten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]