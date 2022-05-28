---
title: Skapa och bekräfta postjournaler
description: Detta ämne tillhandahåller information om hur du skapar och bekräftar postjournaler i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584250"
---
# <a name="create-and-confirm-entry-journals"></a>Skapa och bekräfta postjournaler

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Du använder postjournaler för att registrera faktiska värden direkt i Microsoft Dynamics 365 Project Operations. När du använder postjournaler behöver du inte ange användningsloggar för tid, utgifter och material i Project Operations.

Med en enda post kan du skapa flera journalrader. När bekräftelsen bekräftas registrerar en journalrad för en post det faktiska värdet för följande information:

- Kostnad eller intäkt, beroende på vilken transaktionstyp som valdes.
- Vald transaktionsklass. De tillgängliga klasserna är **Tid**, **Utgift**, **Material**, **Kvarhållare**, **Milstolpe** och **Moms**.
- Det projekt och/eller en uppgift som väljs på journalraden.

Skapa en postjournal i Project Operations genom att följa stegen nedan.

1. Gå till **Försäljning** \> **Transaktioner** \> **Journaler**.
2. På listsidan **Postjournaler** väljer du **Ny** i åtgärdsfönstret för att skapa en journal.
3. På sidan **Ny journal** anger du en beskrivning för journalen i fältet **Beskrivning**.
4. Kontrollera att fältet **Journaltyp** är inställd på **Post** och välj sedan **Spara**. När den nya posten har sparats visas fliken **Journalrader** på journalsidan.
5. På fliken **Journalrader** väljer du **Ny** i verktygsfältet ovanför rutnätet för att skapa en journalrad för post.
6. I dialogrutan **Snabbregistrering** för att skapa en postjournalrad ställer du inte fälten enligt beskrivet i följande tabell.

    | Fält | Description | Funktionellt påverkan |
    | --- | --- | --- |
    | Transaktionsklass | Journalraden kan tillskrivas någon av sex transaktionsklasser: **Tid**, **Utgifter**, **Material**, **Kvarhållare**, **Milstolpe** eller **Moms**. | Transaktionsklassen **Moms** har tagits bort i Project Operations. <br> Om du skapar en transaktionsklass för **Moms** bearbetas denna inte via faktura eller i kostnads- eller intäktsberäkningar. **Milstolpe** är en transaktionsklass endast för intäkter. <br>Transaktionsklassen **Kvarhållare** representerar ett förskott som tagits emot från en kund. Den ska alltid skapas som ett par bestående av fakturerad försäljning och icke-fakturerade försäljningsrader. |
    | Transaktionstyp | Transaktionstyperna **Kostnad**, **Försäljn. mellan org.** och **Kostnad per resursenhet** ska användas för att registrera kostnad.<br> Transaktionstyperna **Ofakturerad** och **Fakturerad försäljning** ska användas för att registrera intäkt. | Transaktionsklassen **Kvarhållare** fungerar endast med transaktionstyperna **Ofakturerad försäljning** och **Fakturerad försäljning**.<br> Transkationsklassen **Milstolpe** fungerar bara med transaktionstypen **Fakturerad försäljning**. <br>Transaktionstyperna **Försäljn. mellan org.** och **Enhetskostnad för resurs** kan endast tillämpas på transaktionsklassen **Tid**, och dessa är endast tillgängliga i postjournaler i distributionsscenariot Lite, inte när Project Operations distribueras i resurs-/icke-lagerbaserade scenarier. |
    | Välj produkt | När du väljer transaktionsklassen **Material** kan du i det här fältet ange om den materialtransaktion du skapar journalraden för är en befintlig produkt eller en produkt eji register. | Om du väljer **Produkt ej i register** kan du ange ett namn för produkten. |
    | Produkt | En referens till produkten från katalogen. | |
    | Description | En beskrivning av journalraden för att göra den lätt att identifiera. | För ofakturerade försäljningsjournalrader används värdet som beskrivning när fakturaradens information skapas. |
    | Extern beskrivning | Beskrivning av journalraden som kan användas för att dela med externa intressenter. | För ofakturerade försäljningsjournalrader används värdet som extern beskrivning när fakturaradens information skapas. Det kan också visas på fakturan som skickas till kunden. |
    | Faktureringstyp | Ett värde som anger om journalraden kommer att räknas som debiterbar, kostnadsfri eller icke-debiterbar projektkomponent. | I ett normalt flöde härleds faktureringstypen från de överenskomna villkor som har angetts i kontraktet. När du registrerar en journalrad kan du ange ett värde i det här fältet. |
    | Dokumentdatum | Använd ett datum då transaktionen ägde rum. | |
    | Startdatum | Använd det datum då transaktionen ägde rum. | Detta fält används som jämförelse med datumet då fakturan skapades för transaktioner av typen **Ofakturerad försäljning**. Den här jämförelsen hjälper dig att avgöra om transaktionen är daterad i framtiden eller i det förgångna. Endast transaktioner daterade i det förgångna läggs till i fakturan. |
    | Slutdatum | Använd det datum då transaktionen ägde rum. | |
    | Redovisningsdatum | Använd det datum då redovisningspåverkan registreras. | |
    | Kontraktradkund | Om kontraktraden endast har en (1) kund anges fältet som standard som kunden på kontraktraden när journalraden sparas. Om kontraktraden har flera kunder markerar du rätt kund på kontraktraden. | Om systemet inte kan fastställa kontraktradkunden på kontraktraden, och om det faktiska värdet för typen **Ofakturerad försäljning** som skapas från journalraden är tomt, kommer det faktiska värdet inte att faktureras. |
    | Project | Markera det projekt som det faktiska värdet ska registreras för. | Utifrån valt projekt, vald transaktionsklassen och vald uppgiften försöker systemet fastställa kontrakt, kontraktrad och kontraktradskund. |
    | Aktivitet | Markera den uppgift som det faktiska värdet ska registreras för. | Om du associerar uppgifter med kontraktrader under kontraktinstallationen använder systemet den valda uppgiften, tillsammans med en projekt- och transaktionsklass, för att fastställa kontrakt, kontraktrads och kontraktradskund. |
    | Transaktionskategori | Markera den transaktionskategori som det faktiska värdet ska registreras för. | För utgifter avgör den valda transaktionskategorin det standardpris som ska anges på journalraden när den sparas. |
    | Roll | Detta fält är relevant för tidsjournalrader. Välj rollen för den resurs som har ägnat tid åt projektet och/eller uppgiften. | Om du använder färdiga konfigurationer för att ange standardresurskostnader och faktureringstakter kommer, för tidsjournalrader, den valda rollen att användas tillsammans med resursenheten för att fastställa det standardpris som ska anges på journalraden när den sparas. Om du använder en anpassad konfiguration för att ange standardpriser bör du granska konfigurationen och fastställa om fältet **Roll** används för att ange standardprisvärden. |
    | Underleverantörskontrakt | Om kontraktraden representerar underleverantörskapacitet, eller kostnader eller material tillhörande underleverantör, väljer du relevant underleverantör. | När kostnadsjournalrader registreras avgör den valda underleverantören den prislista som används för att ange standardenhetskostnaden. |
    | Kontraktrad för underleverantör | Om kontraktraden representerar underleverantörskapacitet, eller kostnader eller material tillhörande underleverantör, väljer du relevant rad för underleverantör. | När kostnadsjournalrader registreras säkerställer den valda underleverantörsraden att tillgängliga kapacitetsberäkningar på kontraktraden för underleverantör beräknas korrekt. |
    | Beloppsmetod | Som standard är detta fält inställt på **Multiplicera kvantitet med pris**. När den här metoden används beräknas beloppet som *Kvantitet* × *Pris*. Den andra metoden som stöds är **Fast pris**. När den här metoden används anges priset som beloppet, och kvantiteten används inte i beräkningen. | |
    | Enhetsschema och Enhet | Tillsammans identifierar enhetsschemat och enheten gällande enhet för kvantiteten. | Kombinationen av enhet och transaktionskategori används för att ange standardpriser för utgifter. I standardkonfigurationen av Project Operations används kombinationen av enhet, roll och resourcing-enhet för att ange standardpriser för tid. Om du har en anpassad konfiguration för posten för standardpris används denna tillsammans med enheten. Kombinationen av produkt och enhet används för att ange standardpriser för material. |
    | Kvantitet | Ange kvantiteten. | |
    | Pris | Om priset lämnas tomt när journalraden skapas används relevanta värden för att ange standardpriser, beroende på transaktionsklassen. Om ett pris anges när journalraden skapas används det priset. | |
    | Skatt | Ange eventuellt momsbelopp. | Beroende på det momsbelopp som anges beräknas det utökade beloppet som *Belopp* + *Moms*. |

## <a name="confirm-an-entry-journal"></a>Bekräfta en postjournal

När du har angett alla journalrader i en postjournal kan du bekräfta journalen. Med den här processen registreras varje journalrad som faktiska värden för respektive projekt.

När en journal har bekräftats kan du inte längre redigera den eller raderna i den.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Faktiska värden som skapat av bekräftelse för postjournal

Det finns några viktiga skillnader mellan faktiska värden som skapas av bekräftelsen på postinmatning och faktiska värden som skapas under godkännande av användningsloggar för tid, utgifter och material, och fakturabekräftelse i Project Operations:

- Inmatningstransaktioner använder inte transaktionskopplingar för att länka kostnaden till den faktiska försäljningen som inte har fakturerats. De faktiska värden som skapas när användningsloggar för tid, utgifter och material godkänns använder alltid transaktionskopplingar för att länka faktiska kostnader och icke-fakturerad försäljning.
- Inmatningsjournaler använder inte transaktionsursprung för att länka den faktiska kostnaden och ofakturerad försäljning till någon ursprunglig post. De faktiska värden som skapas när användningsloggar för tid, utgifter och material godkänns använder alltid transaktionsursprung för att länka faktiska kostnader och icke-fakturerad försäljning till ursprunglig tidspost.
- När ofakturerad faktisk försäljning som skapas av bekräftelsen för postjournalen faktureras, länkas den fakturerade faktiska försäljningen som skapas i samband med fakturabekräftelse till den ofakturerade faktiska försäljningsen på samma sätt som den ofakturerade fkatiska försäljningen som skapas när användningsloggar för tid, utgift och material godkänns.
- Postjournalrader som skapas för tid som anges av resurser mellan organisationer medför inte att **Kostnad för resursenhet** eller **Försäljning mellan organisationer** skapas automatiskt. Dessa faktiska värden måste skapas manuellt. Detta beteende skiljer sig från beteendet hos tidsposter som registreras av resurser mellan organisationer. När tiden godkänns kommer programmet i detta fall automatiskt att skapa faktiska värden för typen **Kostnad** för projekt och faktiska värden för typerna **Enhetskostnad för resurs** och **Försäljning mellan organisationer** i medarbetarens ägande avdelning. Sedan används transaktionskopplingar för att länka dessa faktiska värden och transaktionens ursprung för att länka dem till ursprungstidsposten.
- När postjournaler bekräftas skapar de faktiska värden. Korrigeringsjournaler kan dock inte användas för att korrigera dessa faktiska värden. Detta beteende skiljer sig från beteendet för faktiska värden som skapas när användningsloggar för tid, utgifter och material godkänns. I så fall kan du med hjälp av Rättelsejournaler korrigera faktiska värden för att åtgärda eventuella fel, förutsatt att dessa faktiska värden ännu inte har fakturerats. Om de redan har fakturerats kan du fortfarande korrigera ett faktiskt värde om du bearbetar en fullständig kreditering av det faktiska värdet till kunden.

> [!NOTE]
> Postjournaler framtvingar inte strikta standardiseringsregler. Använd därför dessa postjournaler så lite som möjligt, och var försiktig så att du inte skapar skadade ekonomiska data i systemet. När så är möjligt bör du använda användningsloggar för tid, utgifter och materialanvändning, milstolpe- och behållarkonfigurationen för projektkontrakt och bekräftelseprocessen för projektfaktura i stället för postjournaler för att skapa faktiska värden.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
