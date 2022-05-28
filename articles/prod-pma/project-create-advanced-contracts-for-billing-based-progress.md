---
title: Skapa avancerade kontrakt för fakturering baserad på förlopp
description: I det här ämnet beskrivs hur du skapar projektkontrakt så att du kan skapa fakturor för kunder, baserat på en procent färdigt arbete.
author: RadhikaRS
ms.date: 03/26/2020
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
ms.openlocfilehash: bdafc2ed2398054d8b0bf42bdd96dfe0eccee93b
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683185"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Skapa avancerade kontrakt för fakturering baserad på förlopp
[!include [banner](../includes/banner.md)]

I det här ämnet beskrivs hur du skapar projektkontrakt så att du kan skapa fakturor för kunder, baserat på en procent färdigt arbete. Fakturabelopp beräknas automatiskt för de budgetkategorier för arbete som du konfigurerar för ett projekt. Fakturans tidsinställning ställs in när du förhandlar om projektkontraktet med kunden.

Använd procedurerna i det här ämnet om du vill skapa ett kontrakt, ett associerat projekt och faktureringsregler som beräknar fakturabelopp för de budgetkategorier som du konfigurerar för projektet.

När du har skapat kontraktet och projektet kan du ange information om projektet. Du kan till exempel definiera aktiviteter och tilldela arbetare till projektet.

## <a name="example"></a>Exempel

Din organisation är ett företag för programutveckling. Du samtycker till att utveckla ett paket för löneredovisning för en kund för en total avgift på 20 000 dollar (USD). Din organisation går med på att fakturera kunden allt eftersom du slutför specifika delar av projektet. Du kan ange följande projektkategorier för arbetet, så att du kan använda dem i faktureringsprocessen:

- Konsultverksamhet
- Design
- Installation

Du ställer även in faktureringsregler som automatiskt beräknar fakturabeloppen för den procentandel av projektarbetet som slutförts i varje kategori.

Budgetansvarig skapar en budget för projektkategorierna. Mängden färdigt arbete beräknas automatiskt som en procentandel av det faktiska arbetet i jämförelse med de budgeterade beloppen.

## <a name="prerequisites"></a>Förutsättningar

Innan du skapar ett projekt som använder faktureringsregler måste du ange nummerserier för faktureringsregler och en avgiftsjournal som används för att bokföra förloppsfaktureringar.

1. Gå till **Projektledning och redovisning** \> **Konfiguration** \> **Parametrar för projektledning och redovisning**.
2. På sidan **Parametrar för projektledning och redovisning**, under fliken **Nummerserier**, konfigurerar du nummerserier som du vill använda när faktureringsregler skapas.
3. Gå till **Projektledning och redovisning** \> **Journaler** \> **Avgift**.
4. På sidan **Avgiftsjournal** väljer du **Ny** och anger journalnamnet.

## <a name="create-a-contract-for-progress-billings"></a>Skapa ett kontrakt för förloppsfakturering

Använd den här proceduren om du vill skapa ett projektkontrakt för ett fastprisprojekt. Du skapar en projektfaktura när det arbete som har slutförts i projektet uppnår en angiven procentsats.

1. Gå till **Projektledning och redovisning** \> **Projekt** \> **Projektkontrakt**.
2. På sidan **Projektkontrakt** väljer du **Ny**.
3. I dialogrutan **Nytt projektkontrakt** ställer du in följande fält:

    - **Namn**
    - **Finansieringstyp**
    - **Finansieringskälla**
    - **Försäljningsvaluta** – Som standard används valutan för kundfakturor som är associerade med projektkontraktet. Du kan emellertid ändra försäljningsvalutan på en specifik kundfaktura.

4. Välj **OK**. Informationen kopieras till huvudet på sidan **Projektkontrakt**.
5. På sidan **Projektkontrakt** fyller du i resten av den information som krävs för projektet.

## <a name="create-a-project-for-progress-billings"></a>Skapa ett projekt för förloppsfakturering

Följ stegen nedan om du vill skapa ett projekt och eventuella delprojekt som är associerade med ett projektkontrakt.

1. Gå till **Projektledning och redovisning** \> **Projekt** \> **Alla projekt**.
2. På sidan **Alla projekt** väljer du **Nytt**.
3. I dialogrutan **Nytt projekt**, i fältet **Projekttyp**, väljer du **Tid och material**.
4. Välj en projektgrupp. En projektgrupp definierar bokföringsinformationen för de projekt som är tilldelade till gruppen.
5. Välj **Skapa projekt**.
6. När projektet har skapats ställer du in projektstadiet på **Pågår**.

## <a name="create-a-budget-for-a-project"></a>Skapa en budget för ett projekt

Budgetkategorier används för att automatiskt beräkna fakturabeloppen för den procentandel av arbetet som slutförts för varje kategori. Följ stegen nedan om du vill skapa budgetkategorier för de beräknade kostnaderna.

1. Gå till **Projektledning och redovisning** \> **Projekt** \> **Alla projekt**.
2. På sidan **Alla projekt** markerar du och öppnar önskat projekt.
3. På sidan **Projekt**, i åtgärdsrutan, under fliken **Plan**, i gruppen **Budget**, välj **Projektbudget**.
4. På sidan **Projektbudget** anger du en uppskattad kostnad för varje kategori i projektet.

## <a name="create-billing-rules-for-progress-billings"></a>Skapa faktureringsregler för förloppsfakturering

1. Gå till **Projektledning och redovisning** \> **Projekt** \> **Projektkontrakt**.
2. På sidan **Projektkontrakt** markerar du och öppnar ett projektkontrakt.
3. På projektkontraktsidan, under snabbfliken **Faktureringsregler**, väljer du **Lägg till**.
4. På sidan **Faktureringsregel**, i fältet **Radtyp**, väljer du **Förlopp**.
5. Under snabbfliken **Information om rad för faktureringsregel**, i fältet **Kontraktvärde**, anger du det totala värdet för kontraktet.
6. I fältet **Kategori** väljer du den kategori som avgiftstransaktionen ska bokföras i.
7. I fältet **Projekt** väljer du det projekt som använder den här faktureringsregeln.
8. Valfritt: tilldela faktureringsregeln till ytterligare projekt. Under snabbfliken **Projekt**, i avsnittet **Tillgängliga projekt**, väljer du ett projekt och sedan högerpilen för att lägga till projektet i avsnittet **Valda projekt**.
9. Valfritt: beräkna procentsatsen som kunden håller inne från betalningar på en faktura. Under snabbfliken **Villkor för innehållen betalning** väljer du finansieringskälla och sedan, i fältet **Innehållen procentsats**, anger du innehållen procentsats.
10. Upprepa stegen för att skapa ytterligare faktureringsregler för projektkontraktet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]