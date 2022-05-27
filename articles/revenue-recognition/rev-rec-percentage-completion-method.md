---
title: Intäktsberäkningar för fastprisprojekt
description: I det här ämnet finns information om intäkter i fastprisprojekt.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 290608e5663f9c953212c156771bbf1ad6b1e901
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578730"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Intäktsberäkningar för fastprisprojekt 

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

När du skapar en projektkontraktrad med följande attribut i Dynamics 365 Project Operations för Microsoft Dataverse, skapar systemet automatiskt ett uppskattningsprojekt för fastprisintäkter. Informationen i detta projekt baseras på följande:

  - En faktureringsmetod för fast pris.
  - Ett associerat projekt.
  - Minst en milstolpe som definierats på fliken **Fakturaschema** på fliken **Projektkontaktrad**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Granska intäktsberäkningar för fastprisprojekt
Slutför följande steg om du vill granska projekt för fasta prisintäkter:

1. Gå till **Projekthantering och redovisning** > **Projekt** > **Intäktsberäkningar för fastprisprojekt** i Dynamics 365 Finance-miljön.
2. Välj det projekt som du vill visa och dubbelklicka på **Projekt-ID för uppskattning** för att öppna posten och granska informationen i projektet.
3. Expandera fliken **Projekt**. Du ser då ett projekt i rutnätet **Valda projekt**. Systemet använder detta som standardprojekt eftersom det är projektet som är associerat med projektkontraktraden. 
4. Om du vill ändra associationen väljer du ytterligare projekt och lägger till dem i rutnätet **Valda projekt**. Om flera projekt väljs i det här rutnätet beräknas projektprocentberäkningen och intäktsuppskattningar tillsammans för samtliga valda projekt.

  Projektkostnad, intäktsprofil, kostnadsmall och periodkod kan anges manuellt. Om de inte anges manuellt kommer värdena att återgå till sina respektive standardvärden under den första uppskattningsberäkningen för projektet med hjälp av de regler som konfigurerats för projektkostnad och intäktsprofiler.



[!INCLUDE[footer-include](../includes/footer-banner.md)]