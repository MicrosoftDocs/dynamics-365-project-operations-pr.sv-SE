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
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531569"
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

