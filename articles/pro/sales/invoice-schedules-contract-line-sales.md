---
title: Skapa faktureringsscheman för en projektbaserad kontraktrad - lite
description: I det här ämnet finns information om hur du skapar fakturascheman och milstolpar.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 548858f6d2257343a632657ca386da03f1f330a9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003253"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Skapa faktureringsscheman för en projektbaserad kontraktrad - lite

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Du kan bifoga ett faktureringsschema för en projektbaserad kontraktrad. Fakturering tillåts endast efter att kontraktet har vunnits skapa ett projektkontrakt. Med fakturascheman kan du skapa en projektbaserad kontraktrad som automatiskt skapas i utkast av fakturor. Om du planerar att alltid skapa fakturor manuellt kan du hoppa över att skapa fakturascheman på en projektbaserad kontraktrad eller en kontraktrad.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Skapa ett faktureringsschema för tid och material för en projektbaserad kontraktrad

När en projektbaserad kontraktrad har faktureringsmetoden Tid och material kan du generera ett datumbaserat faktureringsschema. Följ stegen nedan om du vill generera ett datumbaserat faktureringsschema automatiskt.

1. Gå till **Inställningar** > **Fakturafrekvenser** för att konfigurera fakturafrekvens.
2. Öppna projektkontraktet och på fliken **Sammanfattning** ställa in önskat leveransdatum.
3. Öppna den tids- och materialkontraktrad som du vill skapa ett datumbaserade fakturaschema för. 
4. På fliken **Faktureringsschema**, välj startdatum för fakturering och fakturafrekvens. 
5. I underrutnätet väljer du **Generera faktureringsschema**.

    Systemet genererar fakturaschemat med följande fältinformation:

    - **Körningsdatum för faktura** ställs in på datumet utifrån fakturafrekvensen.
    - **Transaktionens sista datum** har angetts till dagen före **fakturans kördatum**.
    - **Körstatus** är automatiskt inställd på **Ej körd**. När jobbet för automatiskt skapande av faktura körs för ett visst **fakturans kördatum** uppdateras detta fält till **Körning klar** eller **Körning misslyckades**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Skapa ett faktureringsschema med fast pris för en projektbaserad kontraktrad

När en projektrelaterad kontraktrad har en fast pris faktureringsmetod kan du skapa ett fakturaschema baserat på milstolpe. Utför följande steg för att automatiskt generera ett fakturaschema baserat på milstolpe för en fast uppsättning milstolpar som distribuerar lika för kalenderperioden.

1. Gå till **Inställningar** > **Fakturafrekvenser** för att konfigurera fakturafrekvens.
2. Öppna projektkontraktet och på fliken **Sammanfattning** ställa in önskat leveransdatum.
3. Öppna kontraktraden med fast pris som du behöver för att skapa ett milstolpeschema. 
4. På fliken **Faktureringsschema (faktureringsmilstolpar)**, välj startdatum för fakturering och fakturafrekvens. 
5. I underrutnätet väljer du **Generera periodiska milstolpar**.

    Systemet genererar fakturaschemat med följande information om milstolpe.

    - **Namnet på milstolpen** anges till det datum som dikteras utifrån fakturarekvensen.
    - **Datum för milstolpen** anges till det datum som dikteras utifrån fakturarekvensen.
    - **Belopp för milstolpe** beräknas genom att dela upp kontraktsbeloppet på projektbaserad kontraktrad utifrån antalet milstolpar som styrs av frekvensen, faktureringsstarten och begärda leveransdatum.
    - Om kontraktraden har ett värde i fältet **uppskattat momsbelopp** fördelas fältet även efter varje milstolpe lika när periodiska milstolpar genereras.

Fakturerings milstolpar ska vara lika med det kontrakterade värdet för den projektbaserade kontraktraden. Om de inte är identiska uppstår ett fel. Du kan åtgärda felet genom att kontrollera att faktureringsmilstolparna summerar det kontrakterade värdet på raden genom att antingen skapa, redigera eller ta bort milstolpar. Uppdatera sidan när ändringarna har gjorts.

### <a name="manually-create-milestones"></a>Skapa milstolpar manuellt

Milstolpar med fast pris kan skapas manuellt när de inte längre är delade. Följ stegen nedan om du vill skapa en milstolpe manuellt.

1. Öppna kontraktraden med fast pris som du behöver för att skapa ett milstolpe. 
2. På fliken **Faktureringsschema** i underrutnätet, välj **+ Skapa ny milstolpe för kontraktrad**.
3. I formuläret **Skapa milstolpe** ange den information som krävs utifrån följande tabell. 

| Fält | Plats | Beskrivning | Inverkan nedströms |
| --- | --- | --- | --- |
| Milstolpens namn | Snabbregistrering | Textfält för milstolpens namn. | Det här fältet ingår i milstolpen för projektkontraktraden och fakturan. |
| Projektuppgift | Snabbregistrering | Om milstolpen är kopplad till en projektuppgift kan du använda den här referensen för att lägga till anpassad logik och ange milstolpestatus utifrån uppgiftens status. | Den här referensen påverkas inte av någon efterföljande aktivitet. |
| Milstolpens datum | Snabbregistrering | Det datum då den automatiska faktura skapande processen ska söka efter statusen för den här milstolpen för att tänka på den för fakturering. | Detta ingår i milstolpen för projektkontraktraden och fakturan. |
| Fakturastatus | Snabbregistrering | När milstolpen skapas anges alltid statusen som **inte klar för fakturering** eller **inte startad**. | Detta ingår i milstolpen för projektkontraktraden och fakturan. |
| Radbelopp | Snabbregistrering | Beloppet eller värdet för den milstolpe som ska faktureras kunden. | Det här fältet ingår i milstolpen för projektkontraktraden och fakturan. |
| Moms | Snabbregistrering | Momsbeloppet som används på milstolpen. | Detta ingår i milstolpen för projektkontraktraden och fakturan. |

4. Välj **Spara och stäng**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]