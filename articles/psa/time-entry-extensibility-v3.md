---
title: Anpassa veckovis tidspost
description: I det här ämnet finns information om hur du implementerar anpassade affärsregler som stöder organisationens praxis.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c117e06e7a5c57c7f9b70d1380f450c0ea97cd12
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013058"
---
# <a name="customize-weekly-time-entry"></a>Anpassa tidsposter för en vecka 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I Microsoft Dynamics 365 Project Service Automation version 3.3 har Microsoft introducerat ett modernt rutnät som gör att projektresurserna snabbt kan ange tid för upp till en vecka i taget. Det nya rutnätet för veckovis tidspost kan visa summor för poster efter datum, rad eller vecka. Resurser kan göra kopior av tidsposter inom veckan och även samla in kopior från tidigare veckor. Med systemanpassare kan du anpassa vyn genom att lägga till fält, lägga till uppslag i andra entiteter och implementera anpassade affärsregler för att stödja organisationens praxis.

Tidspost och nyårs kalendern öppnas via webbplatsöversikten. Icke-utökningsbar anpassade tidspost som ingick i tidigare PSA-versioner har ersatts med rutnätet för en utökningsbar veckovis tidspost och även av en alternativ upplevelse i skrivskyddade rutnätet. På grund av ändringen kan användare ange tid i veckovisa belopp.

## <a name="page-layout"></a>Sidlayout
Det nya rutnätet för veckovis tidspost är en anpassad kontroll som har ett verktygsfält och två huvudområden **dimensioner** och **varaktighet**. I verktygsfältet finns en knapp som endast gäller den här anpassade kontrollen för rutnätet för tidspost. Knapparna i åtgärdsfönstret högst upp på sidan gäller för de tre typer av kontroller som stöds för tid, t.ex. veckovis tidspostkontroll, den skrivskyddade kontrollen och kalenderkontrollen.

### <a name="dimensions"></a>Mått
Avsnittet **dimensioner** visar alla dimensioner som det går att ange tid för, som kolumnrubriker. Följande medföljande dimensioner stöds:

- Projekt
- Projektuppgift
- Roll
- Typ
- Poststatus

Avsnittet **dimensioner** tillåter inte infogad redigering. Det här avsnittet är en vy som gör att anpassade fält kan läggas till i rutnätet för veckovisa tidsposter. Mer information om hur du lägger till anpassade fält finns i avsnittet "utökningsbarhet" längre ned i det här ämnet.

### <a name="duration"></a>Varaktighet
I området varaktighet visas veckodagarna som kolumnrubriker. I det här avsnittet kan du redigera på en rad. När en tidspostrad har skapats med lämpliga dimensioner kan användare snabbt ange, i rad, hur mycket tid som har lagts ned på de dimensionerna.

## <a name="create-a-new-time-entry"></a>Skapa en ny tidspost
Om du vill skapa en ny tidspost i rutnätet för tidspost välj **Ny**. Dialogrutan **Snabbregistrering för tidspost** visas. I den här dialogrutan kan användare välja datumet för tidsposten och sedan ange data för **Projekt**, **Projektuppgift**, **Roll** och **Varaktighet** dimensioner i s in minuter, timmar eller dagar genom att skriva **h**, **m**, or **d**, tillsammans med siffran. Användare kan även ange en beskrivning och kommentarer som kan delas ut externt för en tidspost. När användarna sparar sina ändringar visas de värden som angetts mot dimensionerna i området **dimensioner**. Varaktighetsinformationen som anges i fältet **varaktighet** visas det datum då tidsposten skapades.

Uppslagsfält säkerhetskopieras med systemvyer. När en användare har angett ett projekt anges fältet **projektuppgift** till vyn **kopiera** som standard. Om du vill skapa tidsposter för uppgifter som inte är tilldelade till användaren klickar du på **ändra vy** i dialogrutan uppslag och markerar vyn **Alla aktiva projektuppgifter**.

## <a name="edit-a-time-entry"></a>Redigera en tidspost
Information från vissa fält på sidan för tidspost, t.ex. **Beskrivning** och **Externa kommentarer**, visas inte i rutnätet för veckovis tidspost. En liten triangulär indikator visas istället i varaktighetsceller med dessa ytterligare detaljer. Markera cellen och välj sedan **redigera information** om du vill visa data i rutan **snabbredigering**. Om du vill redigera eller uppdatera informationen för en viss tidspost som inte är en del av rutnätet för veckovis tidspost måste användarna öppna fönstret **snabbredigering**.

## <a name="copy-a-time-entry-row"></a>Kopiera en tidspostrad
När tidsposten har skapats första gången kan användare välja **kopiera rad** för att kopiera hela raden till en ny rad. När en rad kopieras på det här sättet kopieras även dimensioner och varaktighet. Användare kan också välja **redigera rad** för att uppdatera dimensionsvärden och varaktigheter i området **varaktighet**.

## <a name="open-a-time-entry"></a>Öppna en tidspost
För att stödja optimal och snabb inmatning i de mest framträdande fälten visar rutnätet för veckovis tidspost en delmängd av valda dimensioner och tidslängder. Om du vill visa all information om en enskild tidspost väljer du **Redigera post** och **Öppna**.

## <a name="submit-a-time-entry"></a>Skicka tidspost
Du kan skicka en enstaka post eller en grupp med tidsposter genom att markera ett block med celler eller en hel tidspostrad och sedan välja **skicka**. Skickade tidsposter visas som transaktioner som väntar på godkännande på godkännarens sida **godkännande**. När du har skickat tidsposter kan du inte redigera dem.

## <a name="recall-a-time-entry"></a>Återkalla tidspost
Du kan återkalla tidsposter som du har skickat in. Du kan återkalla en enskild tidspost, ett block med tidsposter eller en hel rad med tidsposter. Återkallade tidsposter är tillgängliga för resurser för redigering.

## <a name="time-entry-status"></a>Tidspostens status
Nya tidsposter tilldelas automatiskt statusen **utkast**. När en tidspost skickas uppdateras statusen till **skickad**. När en skickad tidspost godkänns uppdateras statusen till **godkänd**. Om en tidspost avvisas uppdateras statusen till **returnerad** och posten blir tillgänglig för korrigering och omsändning. Det går bara att ta bort tidsposter som har statusen **utkast**.

## <a name="view-rejection-comments"></a>Visa kommentarer till avvisning
När en tidspost avvisas av en godkännare kan godkännaren lägga till kommentarer som gör det lättare för resursen att förstå orsaken till avslaget. Om du vill visa avslagskommentarerna för en tidspost markerar du **öppna post**. Kommentarerna för avvisningen visas på tidslinjen. Pa tidslinjen kan resursen svara på de avslagskommentarerna innan han eller hon skickar posten på nytt.

## <a name="copy-week"></a>Kopiera vecka
När du har skapat några tidsposter kan användare välja **Kopiera vecka** för att skapa ytterligare många tidsposter samtidigt. Dialogrutan **Kopiera** visas. I avsnittet **från period** i fälten **Startdatum** och **Slutdatum** definierar du datumintervallet för att kopiera tidsposter från. I avsnittet **Till period** i fältet **Startdatum**, ange datumet att skapa tidsposter för. Markera sedan **Kopiera**. För det angivna datumet i "till"-perioden skapas en kopia av tidsposterna för den motsvarande veckodagen i "från"-perioden. Exempelvis kopieras tidsposten för måndagen från den senaste veckan till måndagen i veckan som anges som "till"-period.

## <a name="import"></a>Importera
Samma grundläggande process används för att importera från bokningar, tilldelningar och utbyten. Användare kan ange det datumintervall som bokningarna ska importeras från. De måste sedan uttryckligen välja de bokningar som ska kopieras till tidsposter utkast. I den tidigare versionen visades föreslagna tidsposter i rutnätet och kalendern och förlorade när sessionen uppdaterades.

## <a name="extensibility"></a>Utökningsbarhet
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Lägga till anpassade fält som har uppslag för andra entiteter
Du lägger till ett anpassat fält i rutnätet med en tidspost i veckan i tre steg.

1.  Lägg till det anpassade fältet i dialogrutan snabbregistrering.
2.  Konfigurera rutnätet så att det anpassade fältet visas.
3.  Lägg till det anpassade fältet antingen i flödet för redigera uppgift eller i cellen för redigera uppgiftsflöde enligt önskemål.

Du måste också kontrollera att de nya fälten har de valideringar som krävs i rad eller cell flödet för redigera uppgift. Som en del av det här steget måste du låsa fältet utifrån tidspoststatus.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Lägg till det anpassade fältet i dialogrutan snabbregistrering.
Du måste lägga till det anpassade fältet i dialogrutan Skapa tidspost för snabbregistrering. så att användarna kan ange ett värde när de lägger till tidsposter med hjälp av knappen **nytt**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurera rutnätet så att det anpassade fältet visas.
Du lägger till ett anpassat fält i rutnätet med en tidspost i veckan på två sätt. Det första alternativet är att anpassa **Mina veckovisa tidsposter** och lägga till ett anpassat fält i den. Du kan välja placering och storlek för det anpassade fältet i rutnätet genom att redigera egenskaperna i vyn.

Det andra alternativet är att skapa en ny vy för en egen tidspost och ange den som standardvy. Den här vyn ska innehålla fälten **Beskrivning** och **Externa kommentarer** förutom de kolumner som du vill ha i rutnätet. Du kan välja placering, storlek och standardorienteringsorder för rutnätet genom att redigera egenskaperna i vyn. Konfigurera sedan den anpassade kontrollen för vyn så att den är en kontroll för **rutnät för tidspost**. Lägg till den här kontrollen i vyn och välj den för webben, telefon och surfplatta. Konfigurera sedan parametrarna för rutnät för veckotids tidspost. Ange fältet **Startdatum** till **msdyn_date**, ange värdet för **varaktighet** till **msdyn_duration** och ange fältet **Status** till **msdyn_entrystatus**. För standardvyn är fältet **Skrivskyddad statuslista** inställt på **192350002,192350003,192350004**, fältet **Uppgiftsflöde för radredigering** är inställt på **msdyn_timeentryrowedit** och fältet **Uppgiftsflöde för cellredigering** inställt på **msdyn_timeentryedit**. Du kan anpassa de här fälten om du vill lägga till eller ta bort skrivskyddad status eller om du vill använda olika uppgiftsbaserade miljöer (TBX) för redigering av rader eller celler. De här fälten bör bindas till ett statiskt värde.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Lägg till det anpassade fältet i lämpligt flöde för uppgiftsredigering
TBX-sidorna som används för redigering finns under **processer**. Standardsidorna är **Project Service - Redigera tidspostrad** och **Project Service - Redigera tidspost**. Du kan antingen redigera de här standardsidorna eller skapa nya anpassade TBX-sidor.

> [!NOTE] 
> Båda alternativen tar bort färdig filtrering på entiteterna **projekt** och **projektuppgift** så att alla uppslagsvyer för entiteter visas. Endast relevanta uppslagsvyer visas.

Du måste fastställa lämpligt uppgiftsflöde för det anpassade fältet. Om du har lagt till fältet i rutnätet bör du i så fall gå till redigera uppgiftsflödet för rader som används för fält som gäller för hela raden med tidsposter. Om det anpassade fältet har ett unikt värde varje dag, t.ex. ett anpassat fält för **Sluttid** ska det gå vidare i cellen för redigera uppgiftsflöde.

Om du vill lägga till det anpassade fältet i ett uppgiftsflöde drar du elementet **fält** till rätt plats på sidan och anger sedan egenskaperna. Ange egenskapen **Källa** till **Tidspost** och ange egenskapen för **datafältet** till det anpassade fältet. Egenskapen **Fält** anger visningsnamn på sidan TBX. Välj **Verkställ** för att spara ändringarna på fältet. Välj **Uppdatera** för att spara ändringarna på sidan.

Om du vill använda en ny anpassad TBX-sida i stället skapar du en ny process. Ange kategorin som **affärsprocessflöde**, ange posten till **tidspost** och ange affärsprocesstypen till **Kör process som uppgiftsflöde**. Under **egenskaper** ska egenskapen **sidnamn** anges som visningsnamn för sidan. Lägg till alla relevanta fält på sidan TBX. Spara och aktivera processen och uppdatera sedan egenskapen anpassad kontroll för det aktuella åtgärdsflödet till värdet för processens **namn**.

### <a name="add-new-option-set-values"></a>Lägg till nya värden för alternativuppsättning
Om du vill lägga till värden för alternativuppsättning i ett fält som inte finns i en ruta öppnar du redigeringssidan för fältet **Typ** och väljer sedan **redigera** bredvid alternativuppsättning. Lägg sedan till ett nytt alternativ som har en egen etikett och färg. Om du vill lägga till en ny tidspoststatus heter det färdiga fältet **Poststatus**, inte **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Ange en ny tidspoststatus som skrivskyddad
Om du vill ange en ny tidspoststatus som skrivskyddad lägger du till det nya värdet (inte etiketten) till egenskapen **Skrivskyddad statuslista**. Den redigerbara delen av rutnätet för tidsposter låses för rader med den nya statusen.
Lägg sedan till affärsregler för att låsa alla fält på TBX-sidorna **Redigera tidspostrad** och **Redigera tidspost**. Du kan komma åt affärsreglerna för de här sidorna genom att öppna affärsprocessflödesredigeraren för sidan och sedan välja **affärsregler**. Du kan lägga till den nya statusen i villkoret i befintliga affärsregler eller lägga till en ny affärsregel för den nya statusen.

### <a name="add-custom-validation-rules"></a>Lägga till anpassade verifieringsregler
Det finns två typer av verifieringsregler som du kan lägga till för rutnätet för veckovis tidspost: •   Affärsregler för klientsidan som fungerar i dialogruta för snabbregistrering och på TBX-sidor •   Plug-in-valideringar på serversidan som gäller för alla uppdateringar av tidsposter

#### <a name="business-rules"></a>Affärsregler
Använd affärsregler för att låsa och låsa upp fält, ange standardvärden i fält och definiera valideringar som endast kräver information från den aktuella tidsposten. Du kan komma åt affärsreglerna för en TBX-sida genom att öppna affärsprocessflödesredigeraren för sidan och sedan välja **affärsregler**. Du kan sedan redigera de befintliga affärsreglerna eller lägga till en ny affärsregel. För ännu mer anpassade valideringar kan du använda en affärsregel för att köra JavaScript.

#### <a name="plug-in-validations"></a>Valideringar av plugin-program
Du bör använda plugin-valideringar för alla valideringar som kräver mer kontext än vad som är tillgängligt i en enskild tidspost eller för alla verifieringar som du vill ska köras på infogade uppdateringar i rutnätet. Slutför valideringen genom att skapa ett eget plugin-program för entiteten **tidspost**.

> [!IMPORTANT] 
> För närvarande hindrar ett känt problem på TBX-sidorna användarna från att korrigera information och sedan välja Klart när en uppdatering misslyckas med en verifiering av plugin-program. Du kan lösa problemet genom att konfigurera affärsregelvalideringar för att förhindra situationen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]