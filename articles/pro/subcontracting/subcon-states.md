---
title: Tillståndsövergångar på ett underkontrakt
description: Denna artikel förklarar tillståndsövergångarna på en underleverantör i Microsoft Dynamics 365 Project Operations allteftersom underleverantör skapas, körs och stängs.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b41e3d44a17c51778dd850c7d4a48351a5d44554
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919760"
---
# <a name="state-transitions-on-a-subcontract"></a>Tillståndsövergångar på ett underkontrakt 

[!include [banner](../../includes/dataverse-preview.md)]

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
