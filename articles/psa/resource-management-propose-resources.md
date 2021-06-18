---
title: Föreslå projektresurser
description: I det här ämnet finns information om hur du föreslår projektresurser.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 02e47338e34a37e05455e2bc6e6a175210ed6bc7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997983"
---
# <a name="propose-project-resources"></a>Föreslå projektresurser

[!include [banner](../includes/psa-now-project-operations.md)]

Resursansvariga kan föreslå en resurs till projektledaren genom att använda en resursbegäran.

1. Från rutnätet för begäran eller själva begäran, välj **Hitta resurser**.
2. På sidan **schemaassistent** markerar du resursen och väljer rutan **Skapa resursbokning** i fältet **bokningsstatus** och väljer **boka**.

    ![Föreslagen resurs vald](media/Resource-Management-image62.png)

Följande statusuppdateringar inträffar:

- På sidan **schemaläggningsassistent** uppdateras statusindikatorerna för att indikera att bokningen är föreslagen, inte en fast bokade.

    ![Statusindikatorer för föreslagen bokning på sidan schemaläggningsassistenten](media/Resource-Management-image63.png)

- I resursbegäran ändras status till **måste granskas**.

    ![Resursbegärans status ändrad till måste granskas.](media/Resource-Management-image64.png)

- På fliken **team** i projektet ändras värdet för den allmänna teammedlemmens **Status för begäran** till **måste granskas**.

    ![Status för begäran för generisk teammedlem ändras till Måste granskas på fliken Team.](media/Resource-Management-image48.png)

Projektledaren kan antingen acceptera eller avvisa förslaget.

När resursansvariga behandlar resursbegäranden kan de använda någon av följande metoder:

- Föreslå flera resurser för att uppfylla behovet om ingen enskild resurs är tillgänglig för att uppfylla de timmar som krävs. Föreslagna timmar delas sedan mellan flera resurser som kan uppfylla de begärda timmarna. I det här scenariot kan timmarna inte överlappas.
- Föreslå färre resurser än vad som krävs. I det här scenariot är den föreslagna resurskapaciteten mindre än de timmar som begärdes av den begärande. När den som beställt accepterar de föreslagna resurserna skapas därför ett ouppfyllt resursbehov som fångar upp det återstående behovet.
- Boka flera resurser för att uppfylla behovet om ingen enskild resurs är tillgänglig för att slutföra arbetet.
- Boka färre resurser än vad som krävs. I det här scenariot är bokade timmar färre än de timmar som krävs. Systemet hjälper dig att föreslå resurser i stället för bokningar, så att den som gör en förfrågan kan verifiera och hålla ordning på återstående efterfrågan.

## <a name="billable-utilization"></a>Fakturerbar användning

Resurser kan ha fakturerbar användning. Den här målanvändningen definieras som ett attribut för en resurs standardroll eller anges i posten för den enskilda bokningsbara resursen. Användningsberäkningar baseras på de faktiska timmarna som resurserna har rapporterat med hjälp av godkända tidtransaktioner.

Följande formler används för att beräkna användningen:

- Fakturerbar användning = debiterbara faktiska timmar ÷ resurskapacitet för tillgång
- Användning av ej fakturerbar tid = faktisk tid med faktureringstyp-ID = inte debiterbar, komplementär eller ej disponibelt ÷ resurskapacitet
- Intern = faktisk tid utan försäljningskontrakt ÷ resurskapacitet
- Resurskapacitet = resursens arbetstider – frånvarande – lediga dagar

Du hittar vyn **Resursutnyttjande** i fönstret **Resurser**.

![Vy för resursutnyttjande](media/Resource-Management-image65.png)

Varje cell i rutnätet representerar resursens fakturerbara användningsprocent i en period, t.ex. dag, vecka eller månad. Följande formler används för att färglägga cellerna:

- **Grön:** fakturerbart resursutnyttjande \>= resursutnyttjande för målet
- **Gul:** mål för resursutnyttjande – 20 \<= fakturerbart resursutnyttjande \< mål för resursutnyttjande.
- **Röd:** fakturerbart resursutnyttjande \< mål för resursutnyttjande – 20

Eftersom vyn **Resursutnyttjande** baseras på schemaläggningstavlan kan du filtrera resultaten med hjälp av filtreringsfunktionerna i schemaläggningstavlan.

Rutnätet kräver att du anger ett utnyttjandemål för antingen rollen eller den enskilda resursen. För att göra detta går du till **Resurser** \> **Resursroller**.

Dessutom måste en standardroll tilldelas varje bokningsbar resurs. Gå till **Resurser** \> **Resurser**. På fliken **Project Service** kontrollera att en resursroll är definierad och att fältet **är standard** anges till **ja**. Du kan lägga till ytterligare roller där **är standard = nej**. Rollen där **är standard = ja** används för att utvärdera resursutnyttjande för resursen mot målet för rollen.

![Standardrolluppsättning](media/Resource-Management-image67.png)

På fliken **Project Service** kan du också ange ett enskilt målutnyttjande för resursen. Utnyttjandeberäkningen använder då målutnyttjande för att utvärdera resursens mål i stället för resursens standardroll.

Utnyttjande visas endast för en resurs om resursen har godkänt, debiterbar tid under den period som visas i rutnätet.

## <a name="resource-availability"></a>Resurstillgänglighet

Det är viktigt att resursansvariga kan visa tillgängligheten till resurser och uppdatera bokningar. I vissa fall finns ingen formell efterfrågan (resursbegäran), men en resursansvarig måste svara på en oplanerad efterfrågan som sker via kanaler som e-post, telefonsamtal eller snabbmeddelanden. Resursansvariga kan uppdatera resurser och bokningar med hjälp av schemaläggningstavlan.

Resursens arbetstider används som grund för att beräkna resursens tillgänglighet. Resursbokningarna förbrukar kapaciteterna för resurserna.

![Schemaläggningstavla](media/Resource-Management-image68.png)

I schemaläggningstavlan används färger och fyllning för att visa bokningar, tillgänglighet och förbokningar samt även status för bokningar. En inställning i schemaläggningstavlan gör att du kan visa en förklaring.

Om en högerriktad pil visas bredvid en enskild bokningsbar resurs på schemaläggningstavlan kan resursen expanderas så att den innehåller information om det arbete som resursen är bokad på.

![Bokningsbar resurs visas på schemaläggningstavlan](media/Resource-Management-image69.png)

Eftersom Dynamics 365 Project Service Automation använder Universal Resource Scheduling-motorn, om du även har Dynamics 365 Field Service installerat kan du visa information om resursbokningar för projekt, arbetsorder och andra entiteter som du har utvidgat schemaläggning till.

![Information om resursbokningar för projekt och arbetsorder](media/Resource-Management-image70.png)

Om du vill visa mer information om en enskild resurs högerklickar du på den så att resurskortet öppnas.

![Resurskort](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]