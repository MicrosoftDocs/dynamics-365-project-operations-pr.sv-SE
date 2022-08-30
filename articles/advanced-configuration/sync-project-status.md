---
title: Synkronisera projektstatus för att förhindra att projekt stängs
description: I den här artikeln finns information om hur du synkroniserar Projektstatus för att förhindra inaktiva eller stängda projekt.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348036"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Synkronisera projektstatus för att förhindra att projekt stängs

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

## <a name="scenario"></a>Scenario

Contoso använder Microsoft Dynamics 365 Project Operations för publicering av resurs-/icke-lagerbaserade scenarier. Som en del av normala affärsaktiviteter kan projekt slutföras eller vänta. Du kan inaktivera projektet så att inga utgifter eller fakturor genereras.

## <a name="solution"></a>Lösning

### <a name="prerequisites"></a>Förutsättningar

-   Microsoft Dynamics 365 Finance 10.0.29 eller senare måste installeras.
-   Mappning för dubbelriktad skrivning 1.0.0.3 för projekt V2 (msdyn\_projects) måste installeras eller konfigureras manuellt enligt beskrivningen nedan.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Skapa en uppdaterad version av integrering av mappning för dubbelriktad skrivning Project Operations Projekt V2

Uppdatera mappning för dubbelriktad skrivning för Project Operations projekt V2:

1. Gå till arbetsytan **Datahantering** och välj **Dubbelriktad skrivning**.
2. Välj panelen **Dubbelriktad skrivning**.
3. Från kolumnen **Tabellmappning** sök och välj **Projekt V2 (msdyn\_projects)** och välj sedan Stopp.
4. Öppna kartan genom att markera mappningsnamnet och välj sedan **[Ingen]**.
5. I dialogrutan Välj kolumn väljer du **statecode \[Projekttillstånd\]** och välj sedan OK. Du kan skriva **tillstånd** i filtervärdet för att begränsa listan.
6.  Välj **Lägg till eller redigera omvandling** i kolumnen **mappningstyp** om du vill redigera omvandlingen.
7.  Från **Transformeringstyp** väljer du **ValueMap**.
8.  Välj **Lägg till värdemappning** och lägg sedan till följande **nycklar** och **värden**:

   Key       | Värde 
   ----------|-------
   InProcess | 0     
   slutfört | 1     

![Skärmbild som visar mappning för dubbelskrivning](media/projectstage-dw-mapping.png)

9. Välj **Spara**.
10. Från överst på sidan **Dubbelriktad skrivning > Projekts V2 (msdyn_projects)**, välj **Spara som**.
11. Från **Lägg till tabell**, i fältet **Utgivare**, väljer du **CDS standardutgivare**.
12. Ange fältet **Version** till 1.0.0.3.
13. Skriv en **Beskrivning** och välj sedan **Spara**.
14. Från överst på sidan **Dubbelriktad skrivning > Projekts V2 (msdyn_projects)** välj **Kör** för att starta mappning och välj **Ja** om du uppmanas att bekräfta innan du kör. 

### <a name="close-a-newly-completed-project"></a>Stänga ett nyligen slutfört projekt

Dynamics 365 Finance använder fältet **projektfas** för att skilja mellan projekt som **pågår** eller som är **avslutade**. **Slutförda** projekt kan inte ådrar sig utgifter eller faktureras till kunder.

1. Öppna ett projekt för att inaktivera.
2. Välj **Inaktivera** i menyfliken.

> [!NOTE]
> Du kan antingen inaktivera eller stänga ett projekt eftersom båda fungerar på samma sätt i samband med Ekonomi.

3. Öppna sidan **Alla projektlistor** i Ekonomi.
4. Bekräfta att det inaktiverade projektet inte visas i listan.
5. I filtret **Visa projekt** ovanför listan ändrar du värdet från **Aktivt** till **Alla**.
6. Nu visas det inaktiverade projektet.

Om du försöker logga tid eller utgifter för det här projektet i Ekonomi bör du inte se projektet för val. Om du anger projektnumret manuellt på en utgifter visas ett meddelande som "Projektfasen är klar tillåter inte registrering i projektet". Fakturering och andra faktureringsfunktioner bör inaktiveras eftersom de är i samband med ett stängt projekt.

