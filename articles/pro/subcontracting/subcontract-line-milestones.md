---
title: Milstolpar för underavtalsrad
description: Den här artikeln innehåller information om hur du skapar och upprätthåller ett milstolpebaserat fakturaschema för en underleverantör med en leverantör.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b146bf0becff5d0fa0da59f50c0d04aafaf5115f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927626"
---
# <a name="subcontract-line-milestones"></a>Milstolpar för underavtalsrad

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

I Dynamics 365 Project Operations kan en underavtalsrad med en faktureringsmetod med fast pris ange ett milstolpebaserat fakturaschema med leverantören.

Milstolpar för leverantörsfakturering kan skapas automatiskt med en fast frekvens, eller också kan du skapa dem manuellt.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Skapa automatiskt ett milstolpebaserat fakturaschema för en underavtalsrad

Slutför följande steg för att automatiskt skapa ett milstolpebaserat fakturaschema för en fast uppsättning jämndistribuerade milstolpar.

1. Gå till **Inställningar** > **Fakturafrekvenser** och ställ in fakturafrekvensen för underavtalsraderna.
2. Öppna sidan **Underavtal**, öppna det underavtal som du vill arbeta med, och öppna sedan den underavtalsrad med fast pris för vilken du vill skapa ett milstolpeschema.
3. På sidan **Milstolpar för underavtalsrad** väljer du **Skapa periodiska milstolpar**.
4. Ange eller markera ett datumintervall, antalet milstolpar samt fakturafrekvens i dialogrutan. Du kan välja startdatum , antal milstolpar, fakturafrekvens eller startdatum, eller ange slutdatum och fakturafrekvens. Du kan inte välja slutdatum och antal milstolpar.
Med hjälp av den här informationen genererar systemet milstolpar och poster som visas i rutnätet **Milstolpar**.

   - **Milstolpenamn** – Namnet på milstolpen anges som datumet för milstolpen baserat på fakturafrekvensen.
   - **Milstolpedatum** – Det datum som baseras på fakturafrekvensen.
   - **Milstolpebelopp** – Beräknas genom att delsummebeloppet på underavtalsraden beräknas utifrån antalet milstolpar.

Om underavtalsraden har ett värde i fältet **Beräknat momsvärde** läggs detta värde till jämnt fördelat i respektive milstolpe när periodiska milstolpar skapas.

Summan av belopp i milstolpar för underavtalsrader måste vara lika med värdet på underavtalsraden. Om de inte är identiska uppstår ett fel. Du kan åtgärda felet och kontrollera att milstolpen är lika med värdet för underavtalsraden genom att skapa, redigera eller ta bort milstolpe- och momsbelopp. När ändringarna har gjorts sparar och uppdaterar du sidan så att inga fler fel finns kvar.

## <a name="manually-create-subcontract-line-milestones"></a>Skapa milstolpar för underkontraktsrad manuellt

Milstolpar med fast pris på en underavtalsrad kan skapas manuellt när de inte delas regelbundet. Följ nedanstående steg om du vill skapa en milstolpe för underavtalsrad manuellt.

1. I navigeringsfönstret väljer du **Underavtal** och öppnar sedan det underavtal du vill arbeta med.
2. Öppna den underavtalsrad med fast pris som du vill skapa en milstolpe för.
3. På fliken **Milstolpar för underavtalsrad** i underrutnätet väljer du **+ Ny milstolpe för underavtalsrad**.
4. På sidan **Ny milstolpe för underavtalsrad** anger du erforderlig information baserat på följande tabell.

    | Fält | Beskrivning |Funktionellt påverkan|
    | --- | --- |----------------------|
    | Milstolpens namn | Namnet på milstolpen. |Detta visas som den första kolumnen i alla uppslag baserat på underkontraktradens milstolpe. Den leverantörsfakturarad som skapas utifrån den här milstolpen använder också namnet på underkontraktradens milstolpe som standardnamn för leverantörens fakturarad.|
    | Beskrivning | En beskrivning av milstolpen. |Den leverantörsfakturarad som skapas utifrån den här milstolpen använder också beskrivningen på underkontraktradens milstolpe som standardbeskrivning för leverantörens fakturarad.|
    | Milstolpens datum | Datumet när processen för automatisk fakturagenerering ska söka efter statusen för denna milstolpen i syfte att överväga den för fakturering.| Värdet används som standarddatum för leverantörsfakturaraden vid fakturering för den här underkontraktraden. |
    | Antal | Beloppet eller värdet för den milstolpe som ska faktureras kunden. |Värdet används som standardbelopp på leverantörsfakturaraden vid fakturering för den här underkontraktraden. |
    | Moms | Momsbeloppet som används på milstolpen.| Värdet används som standardmomsbelopp på leverantörsfakturaraden vid fakturering för den här underkontraktraden. |
    | Belopp efter skatt | Det här skrivskyddade fältet beräknas som Belopp + Moms.|Värdet används som standard på leverantörsfakturaraden vid fakturering för den här underkontraktraden. |
    | Fakturastatus | När milstolpen skapas anges denna status alltid som **Inte redo att faktureras**.|  När statusen är **Klar att fakturera** inkluderar skapandet av leverantörsfakturan denna milstolpe på leverantörsfakturan. |

5. Välj **Spara och stäng**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
