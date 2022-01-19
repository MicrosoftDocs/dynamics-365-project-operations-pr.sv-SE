---
title: Tillståndsövergångar på en underleverantör i Project Operations
description: Detta ämne förklarar tillståndsövergångarna på en underleverantör i Microsoft Dynamics 365 Project Operations allteftersom underleverantör skapas, körs och stängs.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4ca658440c7a9b29a927098f24c092d72d9eb0c9
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902939"
---
# <a name="state-transitions-on-a-subcontract-in-project-operations"></a>Tillståndsövergångar på en underleverantör i Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Detta ämne förklarar tillståndsövergångarna på en underleverantör i Microsoft Dynamics 365 Project Operations. Varje tillstånd representeras antingen som utkast, bekräftat, stängt eller avbrutet. Följande bild representerar tillståndsövergångarna.

![Tillståndsmodell för underleverantör](../media/SubconStates.png)  

I följande tabell beskrivs vad varje tillstånd representerar i livscykeln för en underleverantör i Project Operations.

| State | Description | Tillåtna övergångar |
| --- | --- | --- |
| Utkast | Detta representerar det ursprungliga tillståndet för en underleverantör. Förhandlingarna med leverantören pågår. Raderna och prissättningen kan ändras. En underleverantör i det här tillståndet kan användas för att beräkna och bemanna projektkrav för resurser och material. Det kan också refereras till tid, utgifter och materialanvändning för ett projekt. En underleverantör i det här tillståndet kan redigeras och tas bort. | Bekräftat |
| Bekräftat | Detta är stadiet för en underleverantör efter att förhandlingarna med leverantören om prissättning och radobjekt har slutförts. Dock pågår faktiska leveranser av material och/eller arbete från underleverantörer. En underleverantör i det här tillståndet kan användas för att beräkna och bemanna projektkrav för resurser och material. Det kan också refereras till tid, utgifter och materialanvändning för ett projekt. En underleverantör i det här tillståndet kan inte redigeras eller tas bort. Men knappen **Avbryt** kan du avbryta ett bekräftat underleverantörskontrakt. Med knappen **Öppna på nytt** kan du öppna underleverantörskontraktet på nytt för att återställa det till statusen **Utkast**. Använd knappen **Stäng** för att stänga ett bekräftat underleverantörskontrakt. | Stängda <br> Avbruten <br> Utkast |
| Stängda | Detta är stadiet för en underleverantör när den faktiska leverans av material och/eller arbete som utförts av underleverantörer har slutförts. En underleverantör i det här tillståndet kan inte längre användas för att beräkna och bemanna projektkrav för resurser och material. Det kan inte heller längre refereras till tid, utgifter och materialanvändning för ett projekt. En underleverantör i det här tillståndet kan inte redigeras eller tas bort. | None |
| Avbruten | Detta är stadiet för en underleverantör när faktisk leverans av material och/eller arbete av underleverantörer inte längre behövs. En underleverantör i det här tillståndet kan inte användas för att beräkna och bemanna projektkrav för resurser och material och kan inte heller hänvisas till i tid, utgifter och materialanvändning för ett projekt. En underleverantör i det här tillståndet kan inte redigeras eller tas bort. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
