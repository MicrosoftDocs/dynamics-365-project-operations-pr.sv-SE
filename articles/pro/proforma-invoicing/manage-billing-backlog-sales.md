---
title: Hantera faktureringen som släpat efter - lite
description: I det här ämnet finns information om de olika vyer som kan användas för att hantera förväntad fakturering.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e3ca167fa53a6923727eff3e7c34c8706dc7455
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176993"
---
# <a name="manage-the-billing-backlog---lite"></a>Hantera faktureringen som släpat efter - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Dynamics 365 Project Operations innehåller dedikerade vyer för att hantera förväntad fakturering. Om du vill hantera förväntad fakturering markerar du länkarna i området **försäljning** under **fakturering**. 

Följande vyer är tillgängliga:

- Kvarhållare och förskott
- Tillgängliga kvarhållare och förskott
- Milstolpar med fast pris
- Eftersläpad produktfakturering
- Eftersläpad fakturering av tid och material

## <a name="retainers-and-advances"></a>Kvarhållare och förskott

Vyn **Kvarhållare och förskott** visar alla de kvarhållare och förskott som finns för alla projektkontrakt i systemet. När en kvarhållare eller förskott har fakturerats blir förskottet tillgängligt för användning.

## <a name="available-retainers-and-advances"></a>Tillgängliga kvarhållare och förskott

Vyn **KTillgängliga kvarhållare och förskott** visar alla tillgängliga kvarhållare och förskott som finns för alla projektkontrakt i systemet. När en kvarhållare eller förskott har fakturerats blir förskottet tillgängligt för användning och läggs till i listan. När beloppet för kvarhållaren eller förskottet används helt tas det bort från listan.

## <a name="fixed-price-milestones"></a>Milstolpar med fast pris

Vyn **Milstolpar för fast pris** visar alla milstolpar med fast pris över alla projektkontraktrader i systemet. Du kan markera en eller flera milstolpar som **Klar att fakturera** eller **Inte klar att fakturera** från den här vyn. Om du markerar en milstolpe som **klar att faktura** blir den tillgänglig så att den kan placeras i utkastfaktura.

När flera kundkontraktrader har en faktureringsmetod för fast pris skapas en milstolpe för varje kund på kontraktraden. En milstolpe kan skapas och delas upp i enskilda kundspecifika milstolpeposter. Delningen är intern och i enlighet med faktureringsdelningsprocenten som definierats för varje kund på kontraktraden. I vyn **Milstolpar för fast pris** visas de enskilda kundspecifika milstolpeposterna. Var och en av dessa milstolpeposter kan markeras som **Klar att fakturera** separat från den här vyn. När en eller flera av de relaterade milstolparna har markerats som **klara att fakturera** uppdateras rubrikstatus till **pågår** från **inte startad**. När alla delningar av milstolparna har fakturerats uppdateras statusen för rubrikens milstolpe till **slutförd**.

En milstolpe i ett utkast till en faktura visas i den här vyn med faktureringsstatusen **Kundfaktura har skapats**. När utkastfakturan bekräftas uppdateras faktureringsstatusen för posten till **kundfakturan som har bokförts**. Uppdatera inte det här statusvärdet med hjälp av anpassad kod. Project Operations fungerar inte korrekt när dessa statusvärden uppdateras med anpassad kod.

## <a name="product-billing-backlog"></a>Eftersläpad produktfakturering

Vyn **Eftersläpad produktfakturering** visar alla produktbaserade kontraktrader för alla projektkontrakt i systemet. En eller flera produktbaserade kontraktrader kan markeras som **Klar att fakturera** eller **Inte klar att fakturera** från den här vyn. Om du markerar en produktbaserad kontraktrad som **klar att faktura** blir den tillgänglig så att den kan placeras i utkastfaktura.

En serverbaserad kontraktrad som finns på ett utkast till en faktura visas i den här vyn med faktureringsstatus för **kundfakturan har skapats**. När utkastfakturan bekräftas uppdateras faktureringsstatusen för den här posten till **Kundfaktura har bokförts**. Uppdatera inte det här statusvärdet med hjälp av anpassad kod. Project Operations fungerar inte korrekt när dessa statusvärden uppdateras med anpassad kod.

## <a name="time-and-material-billing-backlog"></a>Eftersläpad fakturering av tid och material

Vyn **Eftersläpad fakturering av tid och material** visar alla ej fakturerade försäljningsvärden för alla projektkontrakt i systemet som inte har fakturerats. Du kan markera ett eller flera ofakturerade faktiska värden för försäljning som **Klart att fakturera** eller **Inte klart att fakturera** från den här vyn. Om du markerar ett ofakturerat faktiskt värde för försäljning som **Klart att fakturera** blir det tillgängligt så att det kan placeras i utkast till en faktura.

Ej fakturerade försäljningsvärden med statusen **Undre gräns** som **Misslyckad** kan inte markeras som **klar för fakturering**. Om de faktiska värdena ska markeras som **klara för fakturering** återställer du statusen för andra verkliga värden på den kontraktrad som har bekräftats. och omvärderar status för **Undre gräns**.

Om kontraktrader för flera kunder har en faktureringsmetod för tid och material, när tid och utgifter godkänns, skapas en ofakturerad faktisk försäljning för varje kund på kontraktraden enligt den faktureringsdelningsprocent som angetts för varje kund. I vyn **Eftersläpad fakturering av tid och material**, kommer du att se dessa individuella kundspecifika, ej fakturerade försäljningsvärden. Vart och ett av dessa ofakturerade faktiska värden för försäljning kan markeras som **Klart att fakturera** separat från den här vyn.

Ett ej fakturerat försäljningsvärde som finns på ett utkast till en faktura visas i den här vyn med faktureringsstatus för **kundfakturan har skapats**. När utkastfakturan bekräftas uppdateras faktureringsstatusen för den här posten till **Kundfaktura har bokförts**. Uppdatera inte det här statusvärdet med hjälp av anpassad kod. Project Operations fungerar inte korrekt när dessa statusvärden uppdateras med anpassad kod.
