---
title: Översikt över projektberäkning
description: I det här ämne finns information om beräkningar i Dynamics 365 i Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8e7ee4888a907b9d8c3ce06c1597f6b05be84477
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085429"
---
# <a name="estimate-projects-overview"></a>Översikt över projektberäkning

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

I en projektrelaterad offert kan du använda entiteten **offertradinformation** för att beräkna det arbete som krävs för att leverera ett projekt. Du kan sedan dela denna beräkning med kunden.

Projektbaserade offertrader kan ha noll till många uppgifter om offertrader. Offertraddetaljer används för att beräkna tid, utgifter eller avgifter. Microsoft Dynamics 365 Project Operations tillåter inte materialberäkningar på offertraddetaljer. Dessa kallas för transaktionsklasser. Beräknade momsbelopp kan också anges i en transaktionsklass.

Utöver transaktionsklasser har offertraddetaljer en transaktionstyp. Två transaktionstyper har stöd för information om offertrader: **kostnad** och **projektkontrakt**.

## <a name="estimate-by-using-a-contract"></a>Beräkning med hjälp av ett kontrakt

Om du använde en offert när du skapade ett projektbaserat kontrakt kopieras den beräkning som du har gjort för varje offertrad i offerten till projektkontraktet. Strukturen på projektkontraktets fungerar som strukturen för projektofferter med rader, raddetaljer och fakturascheman.

Beräkningar kan utföras direkt i ett projektkontrakt och i en projektoffert. För en projektoffert görs beräkningen med hjälp av kontraktrader och kontraktraddetaljer. Kontraktraddetaljer kan även skapas från en projektplan som skapades med hjälp av nerifrån och upp-uppskattningen.

Kontraktraddetaljer kan användas för att beräkna tid, utgifter eller avgifter. Beräknade momsbelopp kan också anges i en kontraktraddetalj.

Uppskattningar av material är inte tillåtna på kontraktraddetaljer.

De processer som stöds i ett projektkontrakt är skapande och bekräftelse av fakturor. När du skapar en faktura skapas ett utkast av en projektbaserade faktura som innehåller alla fakturerade faktiska försäljningsvärden till det aktuella datumet.

Bekräftelse gör kontraktet skrivskyddat och ändrar dess status från **utkast** till **bekräftat**. När du har utfört den här åtgärden kan du inte ångra den. Eftersom åtgärden är permanent är det en god idé att hålla kontraktet i status **utkast**.

De enda skillnaderna mellan kontraktutkast och bekräftade kontrakt är deras status och det faktum att utkastkontrakt kan redigeras, men att det inte går att ändra bekräftade kontrakt. Det går att skapa och spåra verkliga värden i både utkastkontrakt och bekräftade kontrakt.

Project Operations stöder inte ändringsorder i kontrakt eller projekt.

## <a name="estimating-projects"></a>Beräknar projekt

Du kan beräkna tid och utgifter i projekt. Project Operations tillåter inte uppskattning av material eller avgifter i projekt.

Tidsuppskattningar skapas när du skapar en uppgift och identifierar attributen för en allmän resurs som krävs för att utföra uppgiften. Tidsuppskattningar skapas från schemaläggning av uppgifter. Tidsuppskattningar skapas inte om du skapar allmänna teammedlemmar utanför schemats sammanhang.

Utgiftsberäkningar anges i rutnätet på sidan **beräkningar**.

## <a name="understanding-estimation"></a>Förstå beräkningar

Använd tabellen nedan som vägledning för att förstå affärslogiken i beräkningsfasen.

| Situation                                                                                                                                                                                                                                                                                                                                          | Entitetspost                                                                                                                                                                                                       | Transaktionstyp | Transaktionsklass | Ytterligare information                                                            |
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
5. I dialogrutan **Uppdatera befintliga steg** i fältet **filtrera attribut** väljer du ellips-knappen ( **...** ):
6. I dialogrutan **Välj attribut** markerar du kryssrutor för anpassade attribut.
7. Välj **OK** för att stänga dialogrutan och välj sedan **Uppdatera steg**.
8. Upprepa steg 1 till och med 7 för det andra plugin-programmet.
9. Stäng **PluginRegistrationTool**.
