---
title: Organisationsenheter
description: I det här ämnet finns information om organisationsenheter i Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 47855fdd-befa-4203-856d-4e917ecfc16d
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7282b83516e9234b5717b0b5d82d6650bc70f9d2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756310"
---
# <a name="organizational-units"></a>Organisationsenheter 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, en organisationsenhet är en specifik grupp eller avdelning i ett företag som arbetar med fakturerbar tid med kostnadstaxa.

För företag som har professionella tjänster som använder tekniska resurser i olika områden eller affärslinjer kan kostnaden för att fylla en roll i ett utbildningsområde eller en affärslinje från kostnaden för att fylla en roll i ett annat område eller affärslinje. Begreppen för organisationsenheter underlättar i det här scenariot genom att du kan gruppera en uppsättning fakturerbara roller i en division av ett företag som har en distinkt kostnadsstruktur för dessa roller.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Nyckelattribut och sammanslutningar av organisationsenheter

I PSA har en organisationsenhet i PSA en specifik valuta och specifika självkostnadslistor.

Valutan för en organisationsenhet är den primära valuta som används för att spåra kostnader.

En eller flera självkostnadslistor kan kopplas till varje organisationsenhet. PSA lägger följande begränsningar på de prislistor som kan kopplas till en organisationsenhet:

- Prislistor måste vara i organisationsenhetens valuta
- Prislistor måste vara av kostnadsprislistor

Det finns också ett attribut för organisationsenheten i entiteten resurs. Varje resurs kan tilldelas en organisationsenhet.

## <a name="roles-of-organizational-units"></a>Roller för organisationsenheter

Organisationsenheten spelar två roller i PSA:

- **Kontrakteringsenhet** – den organisationsenhet som representerar den företagsgrupp eller avdelning som framför allt är ansvarig för att försäljningen och hanteringen av arbetet och tjänsterna i levereras till kunden. Kontrakteringsenheten identifieras av fältet **Kontrakteringsenhet** i huvudavsnittet på sidorna **affärsmöjlighet**, **offert**, **projektkontrakt**, **projekt**.
- **Resursenhet** – den organisationsenhet som en resurs tillhör eller tilldelas. Den här organisationsenheten kan ge resurser för vissa roller i verksamhetsredogörelsen (SOW) och projekt som ägs av den upphandlande enheten.

> ![Upphandlande enheter och resursenheter](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Vanliga frågor om organisationsenhet

Här är svaren på några av de vanligaste frågorna om organisationsenhet.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Hur är organisationsenheten i PSA relaterad till den organisationsenhet som redan finns i Dynamics 365?

Organisationsenheten i Microsoft Dynamics 365 representerar namnet på en global Dynamics 365-instans. Det här namnet är vanligtvis namnet på det globala företaget.

Entiteten organisationsenhet representerar en grupp eller avdelning i det globala företaget. Den här gruppen eller avdelningen har en uppsättning roller och en självkostnadslista för dessa roller och de rollerna och prislistorna skiljer sig från rollerna och prislistan för andra grupper eller avdelningar i företaget.

När PSA är installerat skapas en standardinställd organisationsenhet utifrån organisationen. Alla befintliga resurser tilldelas till standardorganisationsenheten. Om några nya Active Directory-användare eller resurser importeras till Dynamics 365 tilldelas de till den standardinställda organisationsenheten i PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Hur skiljer sig entiteten för organisationsenheten från entiteten affärsenhet?

I Dynamics 365 är entiteten affärsenhet en säkerhetskonstruktör. Associationen för en användare med en affärsenhet avgör vilka entiteter och enhetsposter som användaren har åtkomst till. Den avgör också vilka behörigheter (skapa, läsa, skriva, ta bort, lägg till, tillägg till, tilldela eller dela) som användaren har för dessa entitetsposter.

Entiteten organisationsenhet representerar en företagsgrupp eller avdelning som har olika kostnadstariffer för medarbetare som är tilldelade till den. En resursandel med en organisationsenhet avgör resursens kostnad för ett projektengagemang.

När du implementerar Dynamics 365 optimerar du säkerheten för hierarkin av affärsenheter och tilldelningen av användare till affärsenheter. Tilldela alla användare som ofta måste komma åt samma uppsättning poster till samma affärsenhet. Organisationsenheten påverkas inte av säkerhetsbehörighet eller åtkomst.

#### <a name="example-of-organizational-units-and-business-units"></a>Exempel på organisationsenheter och affärsenheter

Contoso, Ltd. har en blomstrande metod för Microsoft-teknik. Joel och Hillevi är båda C\#-utvecklare, men Hillevi är i USA och Joel är i Indien. De flesta projekt åtaganden kräver resurser från Contoso Indien och Contoso US, och Joel och Hillevi kräver samma nivå av säkerhets åtkomst till projekt i det här området. Kostnaden för utvecklare från Contoso Indien skiljer sig emellertid avsevärt från dina utvecklares kostnader från Contoso US.

Här är ett optimalt sätt att utforma för det här scenariot med hjälp av Dynamics 365 och PSA.

1. Skapa metod för Microsoft-teknik som en affärsenhet och associera Joel och Hillevi med den. På så sätt garanterar du att båda anställda har samma säkerhetsnivå som alla projekt i det området. Båda kan kontrollera status och rapportera tid, utgifter och uppgiftsuppdateringar. 
2. Skapa två organisationsenheter för att hjälpa till att garantera att kostnaden för projektet är korrekt återspeglad. 
3. Associera Hillevi med Contoso US och associera Joel med Contoso Indien.
4. Tilldela lämpliga självkostnadslistor till båda organisationsenheterna. På det här sättet kan du garantera att kostnaderna som registreras i projektet för Joel och Hillevi återspeglar skillnaden i kostnader mellan Contoso US och Contoso Indien.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Är organisationsenheter relaterade till försäljningsområden i Dynamics 365?

Det finns ingen association eller relation mellan försäljningsområden och organisationsenheter. Ett försäljningsområde är vanligt vis ett geografiskt område där försäljningen sker. En försäljningsprislista kan associeras med varje försäljningsområde.

En organisationsenhet är en intern grupp eller avdelning i företaget som spårar kostnader för en uppsättning roller som den säljer till andra avdelningar eller till externa kunder.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Exempel på organisationsenheter och försäljningsområden

Contoso, Ltd. har två utvecklingscenter: Contoso US och Contoso Indien. Kostnader för resurser varierar kraftigt mellan dessa två utvecklingscenter.

Contoso säljer sina IT-tjänster på många internationella marknader, t.ex. Latinamerika, Nordamerika, Asien, Stilla havet, Västeuropa och Mellanöstern. Faktureringskurserna för samma projektroller kan variera mycket över dessa marknader.

Contoso US och Contoso Indien bör upprättas som organisationsenheter och varje organisationsenhet bör ha en egen självkostnadslista. Asien och Stilla havet, Latinamerika, Nordamerika, Västeuropa och Mellanöstern ska vara inställda på försäljningsområden och varje försäljningsområde bör ha en egen försäljningsprislista.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Varför finns det en begränsning för associationen mellan prislistorna och organisationsenheterna? 

Försäljningspriserna är vanligtvis unika för de geografiska områden eller marknader där tjänster säljs. De interna avdelningarna i ett företag har vanligtvis inget eget försäljningspris för samma slags tjänster. Interna indelningar har emellertid en annan kostnad för sålda varor (COGS), beroende på hur de personer som de anställs och arbetsförhållandena i regionen är verksamma. Eftersom organisationsenheter är modellerade som interna divisioner i ett företag, kan de bara ha självkostnadslistor.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Varför går det inte att associera försäljningsprislistor till organisationsenheter?

I PSA kan försäljningsprislistor associeras med kunder och försäljningsområden. Transaktionella entiteter som affärsmöjlighet, offert, projektkontrakt och projekt använder försäljningsprislistor som är kopplade till kundkontot eller försäljningsområdet för att bestämma faktureringspriser och potentiell omsättning i projektåtagandet.

Självkostnadslistor är kopplade till organisationsenheter. Transaktionella entiteter som affärsmöjlighet, offert, projektkontrakt och projekt använder självkostnadslistor som är kopplade till den upphandlande enheten för att avgöra kostnaderna för ett projektengagemang.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Är organisationsenheter hierarkiska i PSA?

Nr I den aktuella versionen av PSA är organisationsenheterna inte hierarkiska. Det innebär att du inte kan:

- Konfigurera ett mönster för standardkostnadspriser som passerar en hierarki. 
- Rapportera intäkter eller kostnader som slagits samman på olika nivåer i organisationsenhetens hierarki.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Vi är ett stort multinationellt företag med en komplex hierarki med kostnadsställen, avdelningar och faktureringskontor på flera nivåer. Hur kan vi utnyttja det bästa sättet att använda organisationsenhetens koncept i den här versionen av Project Service-appen?

När du har en komplex hierarki med kostnadsställen, avdelningar, faktureringskontor osv, ställer du in de lövnoder som är distinkta organisationsenheter.
I följande exempel visas en typisk hierarki:

**Contoso India**

  - SAP-praxis 

    - Tekniska konsulter 
    - Funktionella konsulter 
    
  - Microsofts tekniska praxis 

    - Tekniska konsulter
    - Funktionella konsulter 
    
**Contoso US**

 - SAP-praxis 

    - Tekniska konsulter 
    - Funktionella konsulter 
    
 - Microsofts tekniska praxis 

    - Tekniska konsulter 
    - Funktionella konsulter 
 
Om hierarkin är snarlik måste du konfigurera den som en platt lista, som visas här:
- Contoso India - SAP-praxis – tekniska konsulter 
- Contoso India - SAP-praxis – funktionella konsulter       
- Contoso India - Microsoft-teknikpraxis för funktionella konsulter 
- Contoso India - Microsoft-teknikpraxis för funktionella konsulter 
- Contoso US - SAP-praxis – tekniska konsulter  
- Contoso US - SAP-praxis – funktionella konsulter  
- Contoso US - Microsoft-teknikpraxis - tekniska konsulter 
- Contoso US - Microsoft-teknikpraxis - funktionella konsulter

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Vi är ett litet företag som bara arbetar med en avdelning. Hur kan vi bäst använda organisationsenhetskonceptet i den aktuella versionen av PSA?

Om företaget fungerar som en enhet som har en självkostnadsprislista behöver du inte skapa några organisationsenheter. Under PSA-installationen skapar Dynamics 365 en standardorganisationsenhet som har samma namn som organisationen. Som standard är tilldelas alla användare denna organisationsenhet. När systemet kräver att en organisationsenhet väljs kommer denna organisationsenhet att väljas som standard.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>När ett projekt skapas från en offert eller en projektkontraktrad kommer den upphandlande standardenheten att komma från offert eller projektkontraktet. Om ett projekt skapas före försäljningsentiteter som offert eller projektkontrakt, vilken är den upphandlande standardenheten?

När ett projekt skapas separat baseras den upphandlande standardenheten i projektet på den användare som skapar den. Den användaren är även standardprojektledare. Om projektet är mappat till en försäljningsenhet, t.ex. en offert eller ett projektkontrakt, baseras den upphandlande enheten i projektet på entiteten försäljning i stället. I det här fallet kan projektuppskattningar räknas om, eftersom självkostnadsprislistan används för att beräkna kostnadsuppskattningsändringarna om den upphandlande enheten ändras. Försäljningsprislistan används för att beräkna de försäljningsuppskattningar som ska ändras så att de synkroniseras med projektprislistan i offerten.

Fälten **Kontrakteringsenhet** och **Valuta** i projektet är låsta för redigering eftersom de måste synkroniseras med värdena i försäljningsentiteten (offert eller projektkontrakt) som projektet är mappat till.
