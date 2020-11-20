---
title: Uppgradera startsidan
description: I det här ämnet visas var du hittar viktig information om de nya och ändrade funktioner i Dynamics 365 Project Service Automation och hur du uppgraderar till den senaste versionen.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fa25d069de8098c0e8788c9ebb8aa3426eec5db9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121780"
---
# <a name="upgrade-home-page"></a>Uppgradera startsidan

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Uppgradera från PSA-version 2.x eller 1.x till version 3.x

### <a name="new-instances"></a>Nya instanser

Från och med 17 maj 2019 när Project Service Automation väljs under etableringen av en ny instans installeras version 3.x som standard.

### <a name="existing-instances"></a>Befintliga instanser

Tidigare måste kunder med en instans av PSA version 2.x uppgradera till version 3.x, som är den UCI(Unified Client Interface)-baserade PSA-versionen, kontakta Microsoft-supporten och tillhandahålla information om sin instans så att supporten skulle kunna aktivera instansen för uppgradering till version 3.x. Från och med 1 mars 2020 kan kunder som har en instans av PSA version 2.x och behöver uppgradera till version 3.x uppgradera sina instanser direkt från administrationsportalen utan att först behöva kontakta Microsoft Support.  

> [!NOTE]
> PSA version 3.x innehåller viktiga förändringar. Den har byggts på ramverk för enhetligt gränssnitt för att ge en bättre användarupplevelse. Den omkonstruerade appen levererar ett konsistent, enhetligt användargränssnitt (UI) och följer de designprinciper som är tillgängliga för optimal visning på alla skärmstorlekar och enheter. Det har gjorts andra ändringar i hela programmet. Vissa av de områden som har ändrats är bland annat prissättning, bokning och tilldelning av resurser, tid, utgifter och godkännanden.

Innan du börjar uppgraderingsprocessen rekommenderar vi att du utför följande uppgifter:

- Kontrollera om både Dynamics 365 Field Service och Project Service Automation har installerats på den identifierade instansen. Om båda lösningarna är installerade bör du planera för att uppgradera både innan du återupptar den vanliga användningen av instansen.
- Läs noggrant igenom följande avsnitt. Medvetenheten och förståelsen av förändringar mellan versionerna hjälper dig att uppgradera processen. I de här avsnitten finns information om de viktigaste ändringarna i PSA samt överväganden och rekommendationer för hur du planerar uppgraderingen till version 3.x.

    - [Nyheter eller ändringar i Project Service Automation version 3](whats-new-changed-v3.md)
    - ["Att tänka på när du uppgraderar - Project Service Automation version 2.x eller 1.x till version 3](upgrade-v3.md)

- Uppgradera testinstans i begränsat läge för att utvärdera ändringarna i implementeringen innan du uppgraderar produktionsinstansen.

När du har granskat ämnena som nämnts tidigare och är redo att uppgradera till PSA version 3.x eller den UCI-baserade versionen, skicka en begäran till Microsofts Support för att göra uppgraderingen tillgänglig från administrationscenter. Ange information om instansen i din förfrågan.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Äldre versioner av PSA (PSA version 2.x) i en nyligen skapad instans

Från och med 17 maj 2019 kommer alla nya instanser att ha samma värde som standardklienten. För att justeringen ska kunna ändras tillhandahålls PSA version 3.x och Field Service version 8.x som standard, eftersom dessa versioner har utformats för att fungera med UCI-klienten.

Från och med den 1 mars 2020 kan kunder med Dynamics PSA inte längre skapa nya miljöer med äldre versioner av PSA, till exempel PSA version 2.x eller äldre. Alla nya miljöer kommer att behöva version 3.x av PSA.

> [!NOTE]
> För att få bästa möjliga resultat när du använder äldre versioner av Field Service och PSA-program går du till sidan **systeminställningar** och för fältet **Använd endast det nya enhetliga gränssnittet (rekommenderas)**, välj **Nej** eftersom de här versionerna inte har utformats för korrekt inläsning i UCI. När du har inaktiverat UCI kan du öppna och köra de här versionerna av Field Service och PSA med hjälp av den gamla webbklienten. 