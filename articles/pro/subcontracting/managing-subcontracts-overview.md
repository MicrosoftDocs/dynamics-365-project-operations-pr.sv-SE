---
title: Hantering av underavtal i Project Operations
description: Detta ämne ger en översikt över den fullständiga processen för underavtalshantering som är typisk för projektbaserade organisationer.
author: rumant
ms.date: 08/02/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d595e948b7be9a6822827f4841e737d3c0e1476b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593036"
---
# <a name="subcontract-management-in-project-operations"></a>Hantering av underavtal i Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Detta ämne ger en översikt över den fullständiga processen för underavtalshantering i projektbaserade organisationer. Underavtal för tjänster följer som regel det affärsprocessflöde som visas i följande diagram.

![Processflöde för underavtalering](../media/SubcontractingProcessFlow.png)

Följande lista ger en steg-för-steg-beskrivning av underavtalsprocessen.

1. Projektledaren skapar ett underavtal med en leverantör. Som standard används de prislistor som är kopplade till leverantörsposten för underavtalet. Leverantörskontot har relationstypen **Leverantör** eller **Leverantör**.
2. Projektledaren kan specificera alla inköp som radobjekt i underavtalet. Underavtalsrader kan vara för tid, utgifter eller produkter. Underavtalsradens transaktionsklass avgör vad raden avser.
3. Leverantörskontoansvarig och projektledaren kan iterera över underavtalet. Prissättningen kan justeras i inköpsprislistor som är kopplade till underavtalet.
4. Om underavtalsraden avser tid kommer leverantörskontoansvarig vid denna tidpunkt eller senare i processen att associera leverantörskontakter med respektive underavtalsrad. Den här associationen ger information till den projektledare som arbetar med underavtalet. När en leverantörskontakt associeras med en underavtalsrad skapar systemet automatiskt en bokningsbar resurs från kontakten (om en bokningsbar resurs inte redan finns).
5. Faktureringsmetoden för varje underavtalsrad kan vara **Fast pris** eller **Tid och material**. För underavtalsrader med fast pris skapas ett milstolpebaserat fakturaschema.
6.  När underavtalet har ställts in och förhandlingen är slutförd, bekräftas avtalet. Bekräftade underavtal kan inte redigeras, men om ändringar inträffar kan ett underavtal "öppnas på nytt för redigeringar", vilket återställer statusen från **Bekräftad** till **Utkast**, varpå förhandlingen kan öppnas på nytt. 
7.  När du skapar en generisk teammedlem i ett projekt kan teammedlemmen associeras till en underavtalsrad. Detta indikerar behovet av att bemanna den generiska teammedlemmen med underleverantörers kapacitet.
8.  Namngivna teammedlemmar kan antingen skapas direkt i ett projekt eller genom att boka dem med hjälp av resursschemaläggningsupplevelserna. Om en namngiven projektteammedlem är kontraktanställd går det att associera detta med en underavtalsrad. I så fall anges den tillgängliga kapaciteten på en underavtalsrad.
9.  Underleverantörers resurser kan logga tid, utgifter och materialanvändning för projekt och projektaktiviteter och sedan skicka in dessa för godkännande. Liknande gäller för anställda. När en kontraktsanställd registrerar tid kan han eller hon välja en viss underavtals- och underavtalsrad.
10. Vid godkännande kommer den tid som har godkänts av underavtal att registrera projektets faktiska kostnader baserat på inköpspriset för den kontraktsanställde eller den roll denne har utfört för projektet.
11. Leverantörsfakturor och objekt på leverantörsfakturarader kan registreras i systemet för det arbete som utförs av leverantörers resurser eller produkter som levereras av leverantören. Leverantörsfakturarader måste vara specifika för ett projekt och för en transaktionsklass bestående av tid, utgifter, produkt/material, milstolpe eller arvode. Alternativt kan leverantörsfakturarader referera till en underavtalsrad.
12. I systemet associeras automatiskt alla faktiska kostnader som matchar underavtalsraden och -projektet med leverantörsfakturan. Detta underlättar en trevägsmatchning och verifieringsprocess.
13. Projektledaren kan sedan granska projektets faktiska resultat automatiskt, ta bort eller lägga till andra faktiska projektkostnader och slutföra verifieringsprocessen.
14. Om verifieringsprocessen slutförs på alla rader markeras leverantörsfakturan som **Redo för betalning**. I det här skedet kan leverantörsfakturan och -raderna överföras till ett system för redovisning eller leverantörsreskontra i syfte att bearbeta betalningen till leverantören. Tidigare registrerade projektkostnader kommer att återställas och faktiska kostnader från leverantörens fakturarad registreras i projektet.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Kvantitetsbaserade och arbetsbaserade underavtalsrader

En underavtalsrad kan vara kvantitetsbaserad eller arbetsbaserad. 

När en underavtalsrad är **kvantitetsbaserad** kan den kvantitet som köps på underleverantörsraden för tid, utgifter eller material användas för vilket projekt som helst.

När en underavtalsrad är **avtalsbaserad** mappas underavtalsraden till ett arbete som representeras av en nod i projektplanen. Värdet på underleverantörsraden är summan av alla komponenter som krävs för att leverera det arbetet. Dessa modelleras som underleverantörsradinformation och kan vara en ansamling tid, utgifter eller material. För en arbetsbaserad underavtalsrad är underavtalseaden också dedikerad till ett enda projekt. Dessa typer av underleverantörer stöds för närvarande inte i Project Operations.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

