---
title: Skapa en manuell proforma-faktura
description: I det här ämnet finns information om hur du manuellt skapar en proforma-faktura i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4085769"
---
# <a name="creating-a-manual-proforma-invoice"></a>Skapa en manuell proforma-faktura

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

I Dynamics 365 Project Operations kan du skapa proforma-fakturor manuellt efter behov. Du kan manuellt skapa en proforma-faktura från listsidan **Projektkontrakt** eller från informationssidan **Projektkontrakt**.

##  <a name="project-contracts-list-page"></a>Listsidan Projektkontrakt

Från listsidan **Projektkontrakt** väljer du ett eller flera projektkontrakt och skapar fakturor för alla valda poster.

Systemet kontrollerar om de valda projektkontrakten har en backlogg **Redo att fakturera** före dagens datum. Från dessa kontrakt skapas utkast av proforma-fakturor. Om ett projektkontrakt har flera kunder kan en faktura skapas per kund och flera fakturor per projektkontrakt.

Alla projektfakturor som skapas finns på sidan **Faktura** i avsnittet **Fakturering** i områden **Försäljning**.

## <a name="project-contract-details-page"></a>Informationssidan Projektkontrakt

En proforma-faktura kan även skapas från informationssidan **Projektkontrakt** , som skapar fakturan för det specifika projektkontraktet. Systemet verifierar att projektkontraktet har en backlogg **Redo att fakturera** före dagens datum. Från de här kontrakten skapas utkast av proforma-fakturor utifrån antalet kunder på varje kontraktrad.

När du har skapat en proforma-faktura öppnas sidan **Faktura**. Om flera fakturor har skapats för projektkontraktet öppnas listsidan **Fakturor** där alla skapade fakturor visas.