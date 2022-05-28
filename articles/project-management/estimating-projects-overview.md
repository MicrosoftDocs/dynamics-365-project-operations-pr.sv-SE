---
title: Begrepp för ekonomisk kalkyl
description: Den ämne information om hur ekonomiska uppskattningar av projekt i Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 338d2924f0e2a4a7fb943686eaad421a892dce70
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597774"
---
# <a name="financial-estimation-concepts"></a>Begrepp för ekonomisk kalkyl

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

I Dynamics 365 Project Operations kan du göra en ekonomisk beräkning av dina projekt i två steg: 
1. Under förförsäljningsstadiet innan affären vunnits. 
2. Under körningsfasen efter att projektkontraktet har skapats. 

Du kan skapa en ekonomisk beräkning för projektbaserat arbete på någon av följande tre sidor:
- Sidan **Offertrad** med hjälp av information om offertraden.  
- Sidan **Projektkontraktrad** med hjälp av information om kontraktraden. 
- Sidan **Projekt** med fliksidorna **Uppgifter** eller **Utgiftsberäkningar**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Skapa en beräkning med hjälp av en projektoffert
I en projektrelaterad offert kan du använda entiteten **offertradinformation** för att beräkna det arbete som krävs för att leverera ett projekt. Du kan sedan dela denna beräkning med kunden.

Projektbaserade offertrader kan ha noll till många uppgifter om offertrader. Offertraddetaljer används för att beräkna tid, utgifter eller avgifter. Microsoft Dynamics 365 Project Operations tillåter inte materialberäkningar på offertraddetaljer. Dessa kallas för transaktionsklasser. Beräknade momsbelopp kan också anges i en transaktionsklass.

Utöver transaktionsklasser har offertraddetaljer en transaktionstyp. Två transaktionstyper har stöd för information om offertrader: **kostnad** och **projektkontrakt**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Skapa en beräkning med hjälp av ett projektkontrakt

Om du använde en offert när du skapade ett projektbaserat kontrakt kopieras den beräkning som du har gjort för varje offertrad i offerten till projektkontraktet. Strukturen på projektkontraktets fungerar som strukturen för projektofferter med rader, raddetaljer och fakturascheman.

Beräkningar kan utföras direkt i ett projektkontrakt och i en projektoffert. För en projektoffert görs beräkningen med hjälp av kontraktrader och kontraktraddetaljer. Kontraktraddetaljer kan även skapas från en projektplan som skapades med hjälp av nerifrån och upp-uppskattningen.

Kontraktraddetaljer kan användas för att beräkna tid, utgifter eller avgifter. Beräknade momsbelopp kan också anges i en kontraktraddetalj.

Uppskattningar av material är inte tillåtna på kontraktraddetaljer.

## <a name="use-a-project-to-create-an-estimate"></a>Skapa en beräkning med hjälp av ett projekt 

Du kan beräkna tid och utgifter i projekt. Project Operations stöder inte förseningar av material eller avgifter för projekt.

Tidsuppskattningar skapas när du skapar en uppgift och identifierar attributen för en allmän resurs som krävs för att utföra uppgiften. Tidsuppskattningar skapas från schemaläggning av uppgifter. Tidsuppskattningar skapas inte om du skapar allmänna teammedlemmar utanför schemats sammanhang.

Utgiftsberäkningar anges i rutnätet på sidan **Utgiftsberäkningar**.

Att skapa en uppskattning för ett projekt anses vara en bästa praxis eftersom du kan bygga detaljerade uppskattningar nedifrån och upp för arbete eller tid och kostnader för varje uppgift i projektplanen. Du kan sedan använda denna detaljerade uppskattning för att skapa uppskattningar för varje offertrad och bygga en mer trovärdig offert för kunden. När du importerar eller skapar en detaljerad uppskattning på offertraden med hjälp av projektplanen importerar Project Operations försäljningsvärdena och kostnadsvärdena för dessa uppskattningar. Efter importen kan du visa måtten för lönsamhet, marginaler och resultat i projektofferten.

## <a name="understanding-estimates"></a>Förstå beräkningar

Använd tabellen nedan som vägledning för att förstå affärslogiken i beräkningsfasen.

| Scenario                                                                                                                                                                                                                                                                                                                                          | Entitetspost                                                                                                                                                                                                       | Transaktionstyp | Transaktionsklass | Ytterligare information                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| När du behöver beräkna försäljningsvärde för tid i en offert                                                                                                                                                                                                                                                                                    | En post för offertraddetalj (QLD) skapas                                                                                                                                                                               | Projektkontrakt | Time        | I fältet transaktionsursprung på försäljningssidan QLD-raden står referenser till kostnadssidan QLD |
|                                                                                                                                                                                                                                                                                     | En andra QLD-post skapas av systemet för att lagra motsvarande kostnadsvärden. Alla icke-monetära fält kopieras från försäljnings-QLD till den kostnads-QLD som systemet har.                                                                                                                                                                               | Kostnad | Time        | I fältet transaktionsursprung på försäljningssidan för information om offertrader refererar (QLD)-raden till kostnadssidan QLD |
| När du behöver beräkna försäljningsvärde för tid i ett kontrakt                                                                                                                                                                                                                                                                                 | Posten för information om projektkontraktrad (CLD) skapas                                                                                                                                                                    | Projektkontrakt | Time        | I fältet transaktionsursprung på försäljningssidan CLD-raden står referenser till kostnads-CLD      |
|                                                                                                                                                                                                                                                                                  | En andra CLD-post skapas av systemet för att lagra motsvarande kostnadsvärden. Alla icke-monetära fält kopieras från försäljnings-CLD till den kostnads-CLD som systemet har.                                                                                                                                                                    | Kostnad | Time        | I fältet transaktionsursprung på försäljningssidan CLD-raden står referenser till kostnads-CLD      |
| När en användare beskriver en resurs i en projektuppgift                                                                                                                                                                                                                                                                                            | Poster för beräkningsrader som visar försäljningsvärdet för uppgiften skapas när en uppgift skapas med alla obligatoriska prissättningsdimensioner. Roll och organisationsenheter är dimensionerna för prissättning | Projektkontrakt | Tid        |                                                                                   |
|     | Posten för beräkningsraden som visar kostnadsvärdet för uppgiften skapas när en uppgift skapas med alla obligatoriska prissättningsdimensioner. Alla icke-monetära fält kopieras från försäljningsberäkningsraden till kostnadsberäkningsraden som systemet har. Roll och organisationsenhet är prissättningsdimensionerna för både kostnads- och faktureringskostnader.                                                                                                                                                                                                                | Kostnad             | Tid           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Anpassa entiteterna för information om offertrader och kontraktrader

Om du har lagt till ett anpassat fält på offertradinformationen och vill att fältets värde ska anges som ett standardvärde på den relaterade kostnadsraden som den skapar använder du registreringsverktyg för plugin-program **PreOperationContractLineDetailUpdate** och **PreOperationQuoteLineDetailUpdate**. Dessa plugin-program måste registreras igen efter det att informationen om offertrad eller kontraktrad har ändrats. Följ dessa steg för att slutföra processen.

1. Öppna PluginRegistrationTool och anslut till din online-instans.
2. Välj **Sök** och sök efter det plugin-program som du vill uppdatera.
3. Markera plugin-programmet och välj sedan **Välj** på huvudsidan.
4. Markera steget för det plugin-program som ska uppdateras, högerklicka och välj sedan **uppdatera**.
5. I dialogrutan **Uppdatera befintliga steg** i fältet **filtrera attribut** väljer du ellips-knappen (**...**):
6. I dialogrutan **Välj attribut** markerar du kryssrutor för anpassade attribut.
7. Välj **OK** för att stänga dialogrutan och välj sedan **Uppdatera steg**.
8. Upprepa steg 1 till och med 7 för det andra plugin-programmet.
9. Stäng **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
