---
title: Skapa ett nytt projekt
description: I det här ämnet finns information om hur du skapar ett nytt projekt.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270745"
---
# <a name="create-a-new-project"></a>Skapa ett nytt projekt

[!include [banner](../includes/banner.md)]

Följ stegen nedan om du vill skapa ett nytt projekt.

1. På sidan **Projekthantering** välj **Ny projekt** och ange följande värden:

    - **Projekttyp:** tid och material
    - **Projektnamn:** XYZ uppgraderingsfas 2
    - **Projektgrupp:** TM\_WIP
    - **Projektkontrakt-ID:** 00000002

2. Välj **Skapa projekt**.

## <a name="assign-a-resource-to-a-project"></a>Tilldela en resurs en projekt

1. På sidan **arbetare** i listan **arbetare** välj posten för den arbetare som du tidigare har ställt in kompetenser för och öppna arbetarposten.
2. I åtgärdsfönstret på fliken **Projekt** i gruppen **Inställning** välj **Tilldela projekt**.
3. På sidan **Tilldelning av resursvalideringsprojekt** på fliken **Projekt** i fältet **Lägg till projektet i utvalda projekt** i projektet **XYZ uppgradering fas 2**.
4. I fönstret **Återstående projekt**, välj ett projekt och välj sedan pilknappen för att lägga till det i rutan **Valda projekt**.

Du kan även tilldela kategorier för en resurs som du behöver. Kategoritypen är antingen **kostnad** eller **intäkt**. Kategoritypen bestäms av din organisation. Om du inte har tilldelats några kategorier för en resurs slår Finance upp kategorin som standard för timkostnader för kostnader och intäkter.

## <a name="set-up-project-resource-and-role-characteristics"></a>Ange egenskaper för projektresurser och roller

En projektledare kan använda projektets källfunktioner för att skapa de roller som krävs för projektet. Roller kan användas om bekräftade resurser fortfarande är okända när resurser reserveras. Roller kan tillfälligt reserveras som planerade resurser så att du kan fortsätta med projektplaneringsfaserna.

[![Exempel på en roll](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso anställdes för att slutföra ett tids- och materialprojekt som har en godkänd projektstadgar. Juniorprojektledaren håller fortfarande på att slutföra projektets omfattning. Resurshanteraren identifierar just nu specifika resurser som ska reserveras för att fungera i det nya projektet. På grund av projektets kritiska karaktär begärde projektsponsor chefsprojektledare som en av rollerna. Resurshanteraren måste skaffa den nya resursen och definiera rollen i systemet om oerfarna projektledare kräver resursinformationen under projektplanering.

I följande steg visas hur resurshanteraren kan konfigurera rollen som ansvarig för projektchefen och associera resursegenskaper med den. Senare kan rollen användas för att söka efter tillgängliga resurser som matchar de begärda resurskompetenserna.

1. På sidan **Konfigurera roller** välj **Ny** och ange följande värden:

    - **Roll-ID:** chefsprojektledare
    - **Beskrivning:** chefsprojektledare

2. Välj **Skapa**.
3. Välj rollen **Chefsprojektledare** och välj sedan **Konfigurera egenskaper**.
4. I fältet **Egenskapstyp** välj **Färdighet**.
5. I fältet **Tillgängliga egenskaper** anger du den färdighet du vill söka efter.
6. I fältet **Egenskapstyp** välj **Certifikat**.
7. I fältet **Tillgängliga egenskaper** anger du den certifikattyp du vill söka efter.

## <a name="assign-a-project-resource-to-a-project"></a>Tilldela en projektresurs en projekt

1. På sidan **Alla projekt** välj **XYZ uppgradera fas 2** projekt.
2. På sidan **Projektgrupp och schemaläggning** välj **Lägg till**.
3. I fält **Roll** välj **Teammedlem**.
4. Välj **Boka från kalendern**.
5. På sidan **Resurstillgänglighet** väljer du **Vyinställningar**.
6. På sida **Justera vyinställningarna** ange följande värden:

    - **Format för datumintervall:** dag
    - **Visa tillgänglighetsbeskrivningar:** Ja
    - **Visa resterande kapacitet:** Ja

7. Välj en resurs i listan över resurser.
8. Välj **Fast bokning** och **Full kapacitet**.

## <a name="assign-a-resource-to-a-default-role"></a>Tilldela en resurs till en standardroll

Om du vill att projekt eller resurshanterare ska kunna öka detaljnivån ytterligare information om vilka resurser som kan reserveras för ett projekt. Du kan associera en standardroll med en befintlig resurs eller en nyligen hämtad resurs. När till exempel Daniel har anställts har han erfarenheten och färdigheterna för rollen affärsanalytiker. Resurshanteraren har tilldelat rollen som Daniels standardroll. Därför lade resurshanteraren Daniel till i en pool av affärsanalytiker som är tillgängliga för att arbeta med projekt.

Vid resursreservationen kan projektledarna filtrera de rollresurser som är tillgängliga för arbete i projekt. De kan använda den här informationen som ett kriterium när de utför beslutsanalys med flera villkor när resurser är uppfyllda. De kan också lägga till andra resursegenskaper i filtret och söka efter resurser med specifika kunskaper, utbildning och erfarenheter för ett visst projekt.

**Scenario:** ett godkänt projekt har startats och rollen som chefsprojektledare reserverades som en planerad resurs under projektplaneringsfasen. Resurshanteraren har nu skaffat en resurs för att kunna utföra rollen som chefsprojektledare.

1. På sidan **Resurslista** välj **Daniel Goldschmidt**.
2. På sidan **Resursroll** välj **Ny** och ange följande värden:

    - **Giltig från:** Ange aktuellt datum.
    - **Förfallodatum:** ange **aldrig**.
    - **Roll:** Ange **chefsprojektledare**.

3. Klicka på **Spara** och stäng sedan sidan.
4. På fliken **kompetenser** lägger du till kompetensen **ProjectMgmt** och **PMP**-intyg.


[!INCLUDE[footer-include](../includes/footer-banner.md)]