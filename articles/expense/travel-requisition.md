---
title: Reserekvisitioner
description: I det här ämnet finns information om reserekvisitioner.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: fa612696944082e179ab2484e2fdd76d1696b889
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276010"
---
# <a name="travel-requisitions"></a>Reserekvisitioner

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

En reserekvisition visar de utgifter som uppstår i samband med resan. En reserekvisition skickas för granskning och kan användas för att godkänna utgifter.

Du kan behöva skicka in en reserekvisition innan du ådrar dig kostnader som debiteras organisationen. Detta krav gäller oavsett om du debiterar utgifter till ett företags kreditkort, spenderar pengar som du erhåller från ett förskott eller ådrar dig utgifter som inte kommer att betalas tillbaka av företaget.

Reserekvisitioner och principer kan användas för att hantera organisationens utgifter. Om din organisation till exempel arbetar med ett fastprisprojekt som kräver resa, måste reseutgifterna för projektets teammedlemmar passa i projektbudgeten. Genom att kräva att resekostnaderna godkänns innan de uppkommer kan organisationen se till att projektet förblir inom budgeten.

## <a name="configuration"></a>Konfiguration 

Reserekvisitioner kan konfigureras som "obligatoriska" genom att aktivera parametern "Förauktorisering av resa är obligatorisk" i utgiftshanteringsparametrar. 

## <a name="create-and-submit-a-travel-requisition"></a>Skapa och skicka en reserekvisition

1. Gå till **Mina utgifter: reserekvisition** och välj **Ny reserekvisition**.
2. Ange ett syfte och en destination för rekvisitionen.
3. I fältet **Resebeskrivning** anger du eventuell ytterligare information. 
4. För var och en av de förväntade kostnaderna, t.ex. flyg, måltider och hyrbil, skapar du en utgiftsradartikel. Ange uppskattat datum, uppskattat belopp och valuta för varje utgift. 
5. När du har lagt till de förväntade utgifterna väljer du **Spara**.
6. När du är klar att skicka reserekvisitionen väljer du **Arbetsflöde** > **Skicka**.

Du kan visa godkända reserekvisitioner under **Mina utgifter: reserekvisition**. 

## <a name="view-available-travel-requisitions"></a>Visa tillgängliga reserekvisitioner

Du kan visa alla dina godkända reserekvisitioner under **Mina utgifter: reserekvisitioner**.

## <a name="approve-travel-requisitions"></a>Godkänn reserekvisitioner

Välj den reserekvisition som du vill godkänna och välj sedan **Arbetsflöde** > **Godkänn**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Skicka in en utgiftsrapport med hjälp av en godkänd reserekvisition

1. Skapa en ny utgiftsrapport och i rubriken för utgiftsrapporten, och från listan över godkända reserekvisitioner, väljer du **Mappa till reserekvisition**.
2. Fältet **Reserekvisitionsbelopp** uppdateras automatiskt i utgiftsrapportrubriken.
3. Lägg till alla utgifter som uppstår för resan. Om fältet **Förauktoriserad** är aktiverat uppdateras avstämt belopp och godkänt belopp för den angivna utgiftskategorin.

> [!NOTE]
> När du mappar en utgiftsrapport till en godkänd reserekvisition får transaktionsbeloppet inte vara större än det godkända beloppet. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]