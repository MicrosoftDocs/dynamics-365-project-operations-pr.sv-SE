---
title: Hantera faktureringen som släpat efter
description: I det här ämnet finns information om hur du visar och arbetar med faktureringseftersläpning i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bec6afe04a705d4f55ac3a7de93a64b47021fbb4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122365"
---
# <a name="manage-the-billing-backlog"></a>Hantera faktureringen som släpat efter

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Dynamics 365 Project Operations har två dedikerade vyer som hjälper dig att arbeta med och hantera faktureringseftersläpning. De är **Milstolpar med fast pris** och **Eftersläpad fakturering av tid och material**. För att välja en vy går du till området **Försäljning** i Project Operations och väljer **Fakturering** i vänster navigeringsfönster. Länkar för faktureringseftersläpning lagras här.

## <a name="fixed-price-milestones"></a>Milstolpar med fast pris

Vyn listar alla milstolpar med fasta priser över alla projektkontraktrader i systemet. Du kan markera en eller flera milstolpar som **Klar att fakturera** eller **Inte klar att fakturera** från den här vyn. När du markerar en milstolpe som **Klar att fakturera** blir milstolpen tillgänglig för ett utkast till en faktura.

När kontraktrader med flera kunder har en faktureringsmetod med fast pris skapas en milstolpe för varje kund på kontraktraden. Användaren skapar en milstolpe och den milstolpen delas upp i kund = specifika milstolpeposter internt enligt den delning av faktureringsprocent som definierats för varje kund på kontraktraden. I vyn **Milstolpar med fast pris** visas enskilda kundspecifika milstolpeposter. Var och en av dessa milstolpeposter kan markeras som **Klar att fakturera** separat från den här vyn. När en eller flera av de relaterade milstolparna har markerats som **Klar att fakturera** går huvudet över till statusen **Pågår** från **Ej påbörjad**. När alla delningar av milstolpar har fakturerats, blir statusen för huvudmilstolpen **Klar**.

En milstolpe i ett utkast till en faktura visas i den här vyn med faktureringsstatusen **Kundfaktura har skapats**. När utkastfakturan bekräftas uppdateras faktureringsstatusen för den här posten till **Faktura har bokförts**. Du rekommenderas inte att uppdatera den här statusen genom att använda anpassad kod. Project Operations fungerar inte korrekt om dessa statusvärden uppdateras med anpassad kod.

## <a name="time-and-material-billing-backlog"></a>Eftersläpad fakturering av tid och material

I den här vyn visas alla ofakturerade faktiska värden för försäljning som inte har fakturerats för alla projektkontrakt i systemet. Du kan markera ett eller flera ofakturerade faktiska värden för försäljning som **Klart att fakturera** eller **Inte klart att fakturera** från den här vyn. Om du markerar ett ofakturerat faktiskt värde för försäljning som **Klart att fakturera** blir det tillgängligt så att det kan placeras i utkast till en faktura.

Ofakturerade faktiska värden för försäljning med **Får ej överskridas**-statusen **Misslyckades** kan inte markeras som **Klar att fakturera**. Om dessa faktiska värden behöver markeras som sådana, kan du återställa statusen för andra faktiska värden på den kontraktrad som har fastställts och sedan utvärdera statusen **Får ej överskridas**.

När det gäller kontraktrader med flera kunder som har en faktureringsmetod för tid och material, när tid och utgifter godkänns, skapas ett ofakturerat faktiskt värde för försäljning för varje kund på kontraktraden enligt den delningsprocent som definierats för varje kund på kontraktraden. I vyn **Eftersläpad fakturering av tid och material** ser du dessa enskilda kundspecifika ofakturerade faktiska värden för försäljning. Vart och ett av dessa ofakturerade faktiska värden för försäljning kan markeras som **Klart att fakturera** separat från den här vyn.

Ett ofakturerat faktiskt värde för försäljning i ett utkast till en faktura visas i den här vyn med **faktureringsstatusen** **Kundfaktura har skapats**. När utkastfakturan bekräftas uppdateras faktureringsstatusen för den här posten till **Kundfaktura har bokförts**. Du rekommenderas inte att uppdatera den här statusen när den är i detta tillstånd genom att använda anpassad kod. Project Operations fungerar inte korrekt när dessa statusvärden uppdateras med anpassad kod.
