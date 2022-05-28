---
title: Projektanslag
description: I det här ämnet beskrivs hur du skapar eller ändrar ett anslag.
author: RadhikaRS
ms.date: 04/22/2020
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
ms.openlocfilehash: 8bc8240c2193bd2c27d54c04b55e14725ab208ac
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684020"
---
# <a name="project-grants"></a>Projektanslag

[!include [banner](../includes/banner.md)]

Ett anslag är ett penningbidrag för ett visst syfte eller projekt. Det finns vanligtvis begränsningar för hur ett anslag kan spenderas. I Projektledning och redovisning kan du ange och spåra anslag samt definiera relationer till projekt och projektkontrakt. Till exempel kan du utföra följande uppgifter:

- Associera anslag med projekt och finansieringskällor via länkar till sidorna **Projekt** och **Projektkontraktsinformation**.
- Ange och spåra ändringar av ett anslag när det flyttas från en status till en annan.
- Ange och spåra kostnader, begärda belopp och tilldelade belopp.
- Skapa huvudanslag och associera delanslag med dem.

Du kan skapa ett anslag genom att ange alla detaljer i en ny post, eller så kan du kopiera informationen från ett befintligt anslag och sedan uppdatera dem.

## <a name="create-a-new-grant"></a>Skapa ett nytt anslag

1. Gå till **Projektledning och redovisning** \> **Anslag** \> **Anslag**.
2. Välj **Nytt** \> **Anslag**.
3. På sidan med anslagsinformation, under snabbfliken **Allmänt**, i fältet **Anslags-ID**, ange en alfanumerisk identifierare för anslaget.
4. I fältet **Anslagsnamn** anger du ett namn på anslaget.
5. I fälet **Beskrivning** lägger du till information om det nya anslaget.

    De flesta andra fält på sidan är valfria och du kan ange så lite eller så mycket information som du vill.

    I följande lista beskrivs den information som anges på varje snabbflik på sidan med information om anslaget:

    - **Allmänt** – Ange anslagets namn, status, beskrivning, syfte och belopp.
    - **Kontaktinformation** – Ange detaljer om personalmedlemmar, avdelningen som hanterar anslaget och anslagets kund eller organisationen som beviljar anslaget. Du kan också ange om organisationen är en direkt enhet som tar emot anslaget och sedan vidarebefordrar det till en annan mottagare. Välj **Lägg till** om du vill lägga till kontaktinformation, t.ex. telefonnummer och e-postadresser till organisationen som tillhandahåller anslaget.
    - **Datum och deadlines** – Ange datum som är relaterade till anslaget och anslagsansökan. Exempel: förfallodatum för ansökan, inlämningsdatum och datum då anslaget godkändes eller avvisas.
    - **Associerade projekt och projektkontrakt** – Du kan bara ange information på den här snabbfliken om fältet **Anslagets status** under snabbfliken **Allmänt** är inställd på **Aktivt** eller **Tilldelat**. Välj bland följande alternativ för att slutföra den relaterade uppgiften:

        - **Lägg till finansieringskälla** – Lägg till en ny finansieringskälla för anslaget. Du kan ange all information nu eller också kan du använda standardinformationen och sedan uppdatera den senare.
        - **Lägg till projektkontrakt** – Lägg till eller uppdatera information om projektkontrakt.
        - **Lägg till projekt** – Lägg till eller uppdatera projektinformation.

    - **Inställningar** – Ange information om matchningsmedel, om det behövs. Många organisationer som tilldelar anslag kräver att mottagaren lägger ned en specifik summa eller resurser för att matcha det belopp som tilldelas i anslaget. I fältet **Lokalt projekt eller spårnings-ID** kan du ange en identifierare som skiljer sig från projektets identifierare.

        > [!NOTE]
        > Om en del av anslaget tilldelas en annan organisation ställer du in alternativet **Undertilldelare** på **Ja**. För anslag som tilldelas i USA kan du ange om ett anslag ska tilldelas enligt ett statligt medgivande eller ett federalt medgivande.

    - **Information om utnyttjande** – Lägg till eller uppdatera information om hur ofta anslag kan utnyttjas, debiteras eller spenderas.

## <a name="create-a-new-grant-from-a-copy"></a>Skapa ett nytt anslag från en kopia

1. Gå till **Projektledning och redovisning** \> **Anslag** \> **Anslag**.
2. Välj **Nytt** \> **Kopiera från anslag**.
3. Ange en alfanumerisk identifierare och ett namn för det nya anslaget och klicka sedan på **OK**.
4. På sidan med anslagsinformation granskar du detaljerna för det kopierade anslaget och gör de ändringar som behövs. De flesta fälten på sidan är valfria.

## <a name="view-or-modify-grant-details"></a>Visa eller ändra anslagsinformation

1. Gå till **Projektledning och redovisning** \> **Anslag** \> **Anslag**.
2. Välj det anslag som ska ändras.
3. I åtgärdsfönstret under fliken **Anslag** i gruppen **Upprätthåll** väljer du **Redigera**.
4. Granska anslagsinformationen och gör de ändringar som behövs.


[!INCLUDE[footer-include](../includes/footer-banner.md)]