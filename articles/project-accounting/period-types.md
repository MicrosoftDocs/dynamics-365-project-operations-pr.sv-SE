---
title: Periodtyper
description: Detta ämne innehåller information om hur du konfigurerar periodtyper för intäktsuppskattning.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287305"
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