---
title: Skapa ett ad hoc-förskott i ett kontrakt
description: I det här ämnet finns information om hur du skapar ett förskott på ett kontrakt efter behov.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f0a6391a3bf6dd39d21504a6f286e4ff1954183
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273619"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Skapa ett ad hoc-förskott i ett kontrakt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Microsoft Dynamics 365 Project Operations har stöd för faktureringsscenarier som omfattar förskottsbetalningar och förskott. Processen för att använda **förskott** i **Project Operations** liknar kontrakt som **Kvarhållare**. 

Följ stegen nedan om du vill fakturera kunden för ett förskott.

1. Gå till sidan **Projektkontrakt** och välj fliken **Förskott och kvarhållare**.
2. Välj i undernätet som visar alla tidigare registrerade förskott och förskottsbetalningar **+ Ny projektkontraktkvarhållare**. 

    Formuläret **snabbregistrering** öppnas för att registrera en förskottsbetalning eller förskott.
    
3. I tabellen nedan visas fälten för att registrera ett förskott och de överväganden du behöver tänka på när du skapar nya:

    | Fält | Beskrivning | Inverkan nedströms |
    | --- | --- | --- |
    | **Projektkontraktskund** | I det här fältet anges vilken kund i kontraktet som ska faktureras för förskott. | Om du har flera kunder i kontraktet och vill fakturera dem för en viss kvarhållande eller förskott skapar du ett förskott för varje kund för sig. |
    | **Beskrivning** | Beskrivning av syftet med och tidpunkten för förskottet för att identifiera förskottet. | Beskrivningen visas på fakturaraden för förskottet. |
    | **Belopp** | Beloppet för förskottsbetalningen eller förskott. | Beloppet visas på fakturaraden för förskottet. |
    | **Fakturadatum** | Datumet då förskottet faktureras till kunden. | Det här är datumet då den automatiska fakturan skapades för att skapa en fakturarad för förhandsproceduren. |
    | **Fakturastatus** | Det här är en alternativ inställning som anger om detta förskott läggs till i en utkastfaktura för den här kunden. Möjliga värden är:</br>- **Inte klar att fakturera**</br>- **Klar att fakturera** | När ett förskott eller en förskottsbetalningen markeras som **klar för fakturering**, läggs det till som en radtid i utkastfakturan. Endast ett helt fakturerat förskott kan användas för att stämma av mot projektkostnader för nästa fakturaperiod. |

4. Välj **Spara och stäng** i dialogrutan snabbregistrering för att registrera förskottet eller förskottsbetalningen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]