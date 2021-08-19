---
title: Periodtyper
description: Detta ämne innehåller information om hur du konfigurerar periodtyper för intäktsuppskattning.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 487e3de7895ca0752e6c9033c7bb7007ba89301c01e6205b3bc8a7d750724bc9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998798"
---
# <a name="period-types"></a>Periodtyper

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

En periodtyp definierar hur ofta intäkter uppskattas på ett projekt. Detta ämne innehåller information om hur du konfigurerar periodtyper för intäktsuppskattning. 

## <a name="create-and-work-with-period-types"></a>Skapa och arbeta med periodtyper
Om du vill skapa och arbeta med periodtyper utför du följande steg:

1. I din Dynamics 365 Finance-miljö går du till **Projektledning och redovisning** > **Konfiguration** > **Uppskattningar** > **Periodtyper**.
2. Välj **Ny** för att skapa en ny periodtyp. Ange ett namn och en beskrivning.
3. Välj ett värde i fältet **Frekvens**:

    - Om du väljer **Vecka**, **Varannan vecka**, **Varannan månad**, **Månadsvis**, **Dagligen**, **Kvartalsvis** eller **Årligen** kommer kalendern att användas för att generera perioderna. 
    - Om du väljer **Redovisningsperiod** kommer redovisningsperioder från konfigurationen för huvudbok att användas för att generera perioder.
    - Om du väljer **Obegränsat** kan du ange anpassade perioder.
4. Välj periodtypposten och välj sedan **Generera perioder** för att skapa perioder för periodtypen. Baserat på periodfrekvensen som du har valt kanske du har möjlighet att ange ett startdatum eller antalet perioder som ska genereras.
5. Välj **Perioder** för att granska genererade perioder.



[!INCLUDE[footer-include](../includes/footer-banner.md)]