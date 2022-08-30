---
title: Tillståndsövergångar på ett underkontrakt
description: Denna artikel förklarar tillståndsövergångarna på en underleverantör i Microsoft Dynamics 365 Project Operations allteftersom underleverantör skapas, körs och stängs.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 02553099a6728c19c219659dff431ff9a5cf10fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261297"
---
# <a name="state-transitions-on-a-subcontract"></a>Tillståndsövergångar på ett underkontrakt 

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Denna artikel förklarar tillståndsövergångarna på en underleverantör i Microsoft Dynamics 365 Project Operations. Varje tillstånd representeras antingen som utkast, bekräftat, stängt eller avbrutet. Följande bild representerar tillståndsövergångarna.

![Tillståndsmodell för underleverantör](../media/SubconStates.png)  

I följande tabell beskrivs vad varje tillstånd representerar i livscykeln för en underleverantör i Project Operations.

| State | Description | Tillåtna övergångar |
| --- | --- | --- |
| Utkast | Detta representerar det ursprungliga tillståndet för en underleverantör. Förhandlingarna med leverantören pågår. Raderna och prissättningen kan ändras. En underleverantör i det här tillståndet kan användas för att beräkna och bemanna projektkrav för resurser och material. Det kan också refereras till tid, utgifter och materialanvändning för ett projekt. En underleverantör i det här tillståndet kan redigeras och tas bort. | Bekräftat |
| Bekräftat | Detta är stadiet för en underleverantör efter att förhandlingarna med leverantören om prissättning och radobjekt har slutförts. Dock pågår faktiska leveranser av material och/eller arbete från underleverantörer. En underleverantör i det här tillståndet kan användas för att beräkna och bemanna projektkrav för resurser och material. Det kan också refereras till tid, utgifter och materialanvändning för ett projekt. En underleverantör i det här tillståndet kan inte redigeras eller tas bort. Men knappen **Avbryt** kan du avbryta ett bekräftat underleverantörskontrakt. Med knappen **Öppna på nytt** kan du öppna underleverantörskontraktet på nytt för att återställa det till statusen **Utkast**. Använd knappen **Stäng** för att stänga ett bekräftat underleverantörskontrakt. | Stängda <br> Avbruten <br> Utkast |
| Stängda | Detta är stadiet för en underleverantör när den faktiska leverans av material och/eller arbete som utförts av underleverantörer har slutförts. En underleverantör i det här tillståndet kan inte längre användas för att beräkna och bemanna projektkrav för resurser och material. Det kan inte heller längre refereras till tid, utgifter och materialanvändning för ett projekt. En underleverantör i det här tillståndet kan inte redigeras eller tas bort. | None |
| Avbruten | Detta är stadiet för en underleverantör när faktisk leverans av material och/eller arbete av underleverantörer inte längre behövs. En underleverantör i det här tillståndet kan inte användas för att beräkna och bemanna projektkrav för resurser och material och kan inte heller hänvisas till i tid, utgifter och materialanvändning för ett projekt. En underleverantör i det här tillståndet kan inte redigeras eller tas bort. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
