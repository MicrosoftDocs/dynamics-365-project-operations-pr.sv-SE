---
title: Hantera intäktsberäkningar
description: Detta ämne innehåller information om hur du arbetar med intäktsuppskattningar för projekt.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e3cbaff18d8bd4d6f6a7577bba25b3e843b1757e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013869"
---
# <a name="manage-revenue-estimates"></a>Hantera intäktsberäkningar

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Du kan skapa, beräkna, bokföra, återställa eller eliminera intäktsuppskattningar. Du kan göra detta antingen manuellt eller genom att använda en periodisk process. Detta ämne innehåller information om hur du arbetar med intäktsuppskattningar för projekt.

### <a name="manage-revenue-estimates-manually"></a>Hantera intäktsberäkningar manuellt

På sidan för intäktsberäkningar för fastprisprojektet eller **Uppskattningsförfrågan** (**Projektledning och redovisning** > **Rapporter och förfrågningar** > **Uppskattningsförfrågningar och -rapporter**), välj **Uppskattningar**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Hantera intäktsuppskattningar med hjälp av en periodisk process

Gå till **Projektledning och redovisning** > **Periodisk** > **Uppskattningar** och välj motsvarande process.

## <a name="create-a-revenue-estimate"></a>Skapa en intäktsuppskattning

Slutför följ steg om du vill skapa en intäktsuppskattning. 

1. Gå till **Projektledning och redovisning** > **Periodisk** > **Uppskattningar**.
2. Välj **Nytt**. På sidan **Skapa uppskattning** och välj följande parametrar:

   - **Periodkod**: Denna kod bestämmer hur ofta uppskattningar bokförs.
   - **Uppskattningsdatum**: Det datum då uppskattningen bearbetas.
   - **Kontinuerlig**: Markera denna kryssruta om du vill skapa uppskattningar endast om uppskattningar bokfördes i föregående period, eller om uppskattningen är den första uppskattning som har skapats. Om detta val inte är markerat skapas uppskattningar även om uppskattningar inte bokfördes i föregående period.
   - **Kostnad för att slutföra metod**: Definiera hur du ska uppskatta det återstående projektarbetet. Mer information finns i [Kostnad för att slutföra metoder](cost-complete-methods.md).
   - **Slutförandemetod**: Välj en slutförandemetod bland följande alternativ:
     - **Automatisk**: Slutförandeprocenten beräknas automatiskt och baserat på de kostnadsrader som ingår i beräkningen. Kostnadsmallen definierar de kostnadsrader som ingår.
     - **Handbok**: Slutförandeprocenten är lika med slutförandeprocenten för den senaste uppskattningen. När uppskattningen har skapats kan du ändra den **manuella beräkningen** på sidan **Uppskattningar**.
     - **Från kostnadsmall**: En kombination av de automatiska och manuella metoderna. Detta alternativ ställs in automatiskt eller manuellt, beroende på standardvärdet i kostnadsmallen.
   - **Prognosmodell**: Välj en prognosmodell för uppskattningen.
   - **Skriv ut uppskattningslista**: Skapa och visa en uppskattningslista. Listan innehåller status för den aktuella funktionen. Du kan skriva ut eventuella varningar om uppskattningen på rapporten. Följande villkor gör att varningar visas i uppskattningslistan:
     - En slutförandeprocent på mer än 100 procent.
     - En slutförandeprocent på under noll procent.
     - Ett negativt belopp i kolumnen **Att slutföra**.
     - En uppskattning utan motsvarande kontraktsbelopp.
     - En uppskattning utan bifogad kostnadsberäkning.
   - **Visa Infologg**: Välj det här alternativet om du vill få ett meddelande som innehåller information om de uppskattningsprojekt som bearbetades när jobbet kördes.


## <a name="post-wip-or-accruals"></a>Bokför PIA eller periodiseringar

Efter det att uppskattningarna har utvärderats bibehålls, minskas eller ökas de. Du kan sedan bokföra PIA när du arbetar med bedömningsprincipen **Slutfört kontrakt** eller också bokföra periodiseringarna när du arbetar med bedömningsprincipen **Slutförd procentandel**.
  
Statusen för uppskattningsperioden ändras från **Skapad** till **Bokförd**.

## <a name="reverse-wip-or-accruals"></a>Omvänd PIA eller periodiseringar

Använd omvändningsalternativet för att kreditera redan bokförda PIA eller periodiseringar, och skapa sedan uppskattningar för perioden.

> [!NOTE]
> Om du vill omvända en period som ligger mellan andra perioder omvänder du erforderliga uppskattningsperioder och bokför dem sedan på nytt. Eftersom alla efterföljande perioder är beroende av uppskattningarna från föregående period ska du inte hoppa över några perioder.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Eliminera uppskattningsprojektet och avsluta projektet

Det sista steget i uppskattningsprocessen är att eliminera uppskattningsprojektet och avsluta fastprisprojektet när slutförandeprocenten når 100 procent.

Följande inträffar när du kör elimineringen:

- För ett fastprisprojekt med ett slutfört kontrakt rensar PIA-värdena från saldokontona och bokför på vinst- och förlustkontona.
- För ett fastprisprojekt med slutförd procentandel tas periodiseringarna bort från vinst- och förlustkontona.

Uppskattningen ändrar status till **Eliminerad**.

> [!NOTE]
> I särskilda fall kan procentsatsen sträcka sig längre än 100 procent. När detta händer minskar du slutförandeprocenten med hjälp av **Metoden Ange kostnad för att slutföra till noll** för att nå 100 procent.

## <a name="reverse-elimination"></a>Omvänd eliminering

1. Gå till **Projektledning och redovisning** > **Periodisk** > **Uppskattningar** > **Omvänd eliminering**. 
2. I fliken **Process** i åtgärdsfönstret väljer du gruppen **Underhåll** och sedan **Uppskattning**. 
3. Välj **Omvänd eliminering**.

Använd den här sidan om du vill omvända alla elimineringar med ett angivet uppskattningsdatum och med uppskattningsstatusen **Eliminerad**. Transaktionsstatusen ändras när du har valt lämpliga fält.

Detta ändrar också automatiskt projektstatusen till **Pågår** om projektstadiet är inställt på Slutfört. Uppskattningsstatusen för projektperioden ändras tillbaka till **Bokförd**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]