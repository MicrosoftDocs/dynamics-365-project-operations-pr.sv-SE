---
title: Hantera eftersläpad fakturering
description: I det här ämnet finns information om hur du visar och arbetar med faktureringseftersläpning i Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9837af0d3c0b2476edab35a53092cf95a44e5244
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600028"
---
# <a name="manage-billing-backlog"></a>Hantera eftersläpad fakturering

**Gäller:** Project Operations för resursbaserade/icke-lagerbaserade scenarier

Dynamics 365 Project Operations innehåller dedikerade vyer för att hantera förväntad fakturering. Om du vill hantera förväntad fakturering markerar du länkarna i området **försäljning** under **fakturering**. 

Följande vyer är tillgängliga:

- Kvarhållare och förskott
- Tillgängliga kvarhållare och förskott
- Milstolpar med fast pris
- Eftersläpad fakturering av tid och material

## <a name="retainers-and-advances"></a>Kvarhållare och förskott

Vyn **Kvarhållare och förskott** anger kvarhållare och framstegen i alla projektkontrakt. När en kvarhållare eller förskott har fakturerats blir förskottet tillgängligt för användning.

## <a name="available-retainers-and-advances"></a>Tillgängliga kvarhållare och förskott

Vyn **Tillgängliga kvarhållare och förskott** anger alla tillgängliga kvarhållare och framstegen i alla projektkontrakt. När en kvarhållare eller förskott har fakturerats blir förskottet tillgängligt för användning och läggs till i listan. När beloppen för spararen eller förskottet har använts helt tas det bort från listan.

## <a name="fixed-price-milestones"></a>Milstolpar med fast pris

Vyn **Milstolpar med fast pris** listar alla fasta pris milstolpar för alla projektavtal. Från denna vy kan enstaka eller flera milstolpar markeras som **Klar att fakturera** eller **Inte redo att fakturera**. Om du markerar en milstolpe som **klar att faktura** blir den tillgänglig så att den kan placeras i utkastfaktura.

När flera kundkontraktrader har en faktureringsmetod för fast pris skapas en milstolpe för varje kund på kontraktraden. En milstolpe kan skapas och delas upp i enskilda kundspecifika milstolpeposter. Delningen är intern och i enlighet med faktureringsdelningsprocenten som definierats för varje kund på kontraktraden. I vyn **Milstolpar för fast pris** visas de enskilda kundspecifika milstolpeposterna. Var och en av dessa milstolpeposter kan markeras som **Klar att fakturera** separat från den här vyn. När en eller flera av de relaterade milstolpsuppdelningarna är markerade som **Klar att fakturera**, rubrikens status uppdateras till **Pågår** från **Inte startad**. När alla delningar av milstolpen faktureras uppdateras huvudets milstolpe som rubrik till **Slutförd**.

En milstolpe i ett utkast till en faktura visas i den här vyn med faktureringsstatusen **Kundfaktura har skapats**. När utkastfakturan bekräftas uppdateras faktureringsstatusen för posten till **kundfakturan som har bokförts**. 

> [!NOTE] 
> Uppdatera inte statusvärdet med anpassad kod. Project Operations fungerar inte korrekt när dessa statusvärden uppdateras med anpassad kod.

## <a name="time-and-material-billing-backlog"></a>Eftersläpad fakturering av tid och material

Vyn **Eftersläpad fakturering av tid och material** visar alla ej fakturerade försäljningsvärden för alla projektkontrakt i systemet som inte har fakturerats. Du kan markera ett eller flera ofakturerade faktiska värden för försäljning som **Klart att fakturera** eller **Inte klart att fakturera** från den här vyn. Om du markerar ett ofakturerat faktiskt värde för försäljning som **Klart att fakturera** blir det tillgängligt så att det kan placeras i utkast till en faktura.

Ej fakturerade försäljningsvärden med statusen **Undre gräns** som **Misslyckad** kan inte markeras som **klar för fakturering**. Om verkliga värden måste markeras som **Klar att fakturera**, återställ status för andra faktiska förhållanden på kontraktet och gör en omvärdering av **Undre gräns** status.

Om kontraktrader för flera kunder har en faktureringsmetod för tid och material, när tid och utgifter godkänns, skapas en ofakturerad faktisk försäljning för varje kund på kontraktraden enligt den faktureringsdelningsprocent som angetts för varje kund. I vyn **Eftersläpad fakturering av tid och material**, kommer du att se dessa individuella kundspecifika, ej fakturerade försäljningsvärden. Vart och ett av dessa ofakturerade faktiska värden för försäljning kan markeras som **Klart att fakturera** separat från den här vyn.

En ofakturerade faktiska försäljningen som finns på en utkastfaktura visas i den här vyn med faktureringsstatusen **Kundfaktura skapad**. När utkastfakturan bekräftas uppdateras faktureringsstatusen för den här posten till **Kundfaktura har bokförts**. 

> [!NOTE] 
> Uppdatera inte statusvärdet med anpassad kod. Project Operations fungerar inte korrekt när dessa statusvärden uppdateras med anpassad kod.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
