---
title: Organisationsenheter
description: Detta ämne beskriver konceptet med organisationsenheter och förklarar hur du skapar och underhåller organisationsenheter i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9a8c503dc6286f40c80ed9b7a8a04974ff7e50b4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581398"
---
# <a name="organizational-units-overview"></a>Översikt över organisationsenheter

I Microsoft Dynamics 365 Project Operations är en *organisationsenhet* en specifik grupp eller avdelning i ett professionellt tjänsteföretag som arbetar med fakturerbara resurser med kostnadstaxor.

Professionella tjänsteföretag som använder tekniska resurser inom olika verksamhetsområden eller affärslinjer kan kostnaden för att tillsätta en roll variera beroende på verksamhetssområde eller affärslinje där rollen tillsätts. I detta scenario bistår konceptet med organisationsenheter genom att möjliggöra gruppering av en uppsättning fakturerbara roller i en företagsavdelning med distinkt kostnadsstruktur för dessa roller.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Konceptet med organisationsenheter i Project Operations

I Project Operations har en organisationsenhet en specifik valuta och specifika självkostnadslistor.

Valutan för en organisationsenhet är den primära valuta som används för att spåra kostnader.

En eller flera självkostnadslistor kan kopplas till varje organisationsenhet. Project Operations lägger följande begränsningar på de prislistor som kan kopplas till en organisationsenhet:

- Prislistorna måste vara i organisationsenhetens valuta.
- Prislistorna måste vara av typen självkostnadslistor.

Entiteten Resurs innehåller även ett attribut för organisationsenheten. Varje resurs kan tilldelas en organisationsenhet.

### <a name="roles-of-organizational-units"></a>Roller för organisationsenheter

Organisationsenheten spelar två roller i Project Operations:

- **Kontrakteringsenhet** – den organisationsenhet som representerar den företagsgrupp eller avdelning som framför allt är ansvarig för att försäljningen och hanteringen av arbetet och tjänsterna i levereras till kunden. Kontrakteringsenheten identifieras av fältet **Kontrakteringsenhet** i huvudavsnittet på sidorna **affärsmöjlighet**, **offert**, **projektkontrakt**, **projekt**.
- **Resursenhet** – den organisationsenhet som en resurs tillhör eller tilldelas. Den här organisationsenheten kan ge resurser för vissa roller i verksamhetsredogörelsen (SOW) och projekt som ägs av den upphandlande enheten.

![Upphandlande enheter och resursenheter.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Vanliga frågor och svar kring organisationsenhet

Här är svaren på några av de vanligaste frågorna om organisationsenhet.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Hur är entiteten Organisationsenhet i Project Operations relaterad till den organisationsenhet som redan finns i Dynamics 365?

Organisationsenheten i Dynamics 365 representerar namnet på en global Dynamics 365-instans. Det här namnet är vanligtvis namnet på det globala företaget.

Entiteten organisationsenhet representerar en grupp eller avdelning i det globala företaget. Den här gruppen eller avdelningen har en uppsättning roller och en självkostnadslista för dessa roller och de rollerna och prislistorna skiljer sig från rollerna och prislistan för andra grupper eller avdelningar i företaget.

När Project Operations är installerat skapas en standardinställd organisationsenhet utifrån organisationen. Alla befintliga resurser tilldelas till standardorganisationsenheten. Om några nya Active Directory-användare eller -resurser importeras till Dynamics 365 tilldelas importprocessen för använare dem till den standardinställda organisationsenheten i Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Hur skiljer sig entiteten Organisationsenhet från entiteten Affärsenhet?

I Dynamics 365 är entiteten affärsenhet en säkerhetskonstruktör. Associationen för en användare med en affärsenhet avgör vilka entiteter och enhetsposter som användaren har åtkomst till. Den avgör också vilka behörigheter (skapa, läsa, skriva, ta bort, lägg till, tillägg till, tilldela eller dela) som användaren har för dessa entitetsposter.

Entiteten organisationsenhet representerar en företagsgrupp eller avdelning som har olika kostnadstariffer för medarbetare som är tilldelade till den. En resursandel med en organisationsenhet avgör resursens kostnad för ett projektengagemang.

När du implementerar Dynamics 365 optimerar du säkerheten för hierarkin av affärsenheter och tilldelningen av användare till affärsenheter. Tilldela alla användare som ofta måste komma åt samma uppsättning poster till samma affärsenhet. Organisationsenheten påverkas inte av säkerhetsbehörighet eller åtkomst.

**Exempel som visar en möjlig skillnad i utformningen för organisationsenheter och affärsenheter**

Contoso, Ltd. har en blomstrande metod för Microsoft-teknik. Joel och Hillevi är båda C\#-utvecklare, men Hillevi är i USA och Joel är i Indien. De flesta projektåtaganden kräver resurser från både Contoso Indien och Contoso US, och Joel och Hillevi kräver samma nivå av säkerhetsåtkomst till projekt på detta övningsområde. Kostnaden för utvecklare från Contoso Indien skiljer sig emellertid avsevärt från dina utvecklares kostnader från Contoso US.

Här är ett optimalt sätt att utforma för det här scenariot med hjälp av Dynamics 365 och Project Operations.

1. Skapa metod för Microsoft-teknik som en affärsenhet och associera Joel och Hillevi med den. På så sätt säkerställer du att båda anställda har samma säkerhetsnivå som alla projekt på det övningsområdet. Båda kan kontrollera status och rapportera tid, utgifter, materialanvändnin och uppgiftsuppdateringar.
2. Skapa två organisationsenheter för att hjälpa till att säkerställa att kostnaden för projektet återspeglas korrekt.
3. Associera Hillevi med Contoso US och associera Joel med Contoso Indien.
4. Tilldela lämpliga självkostnadslistor till båda organisationsenheterna. På det här sättet kan du säkerställa att kostnaderna som registreras i projektet för Joel och Hillevi återspeglar skillnaden i kostnader mellan Contoso US och Contoso Indien korrekt.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Är organisationsenheter relaterade till försäljningsområden i Dynamics 365?

Det finns ingen association eller relation mellan försäljningsområden och organisationsenheter. Ett försäljningsområde är vanligt vis ett geografiskt område där försäljningen sker. En försäljningsprislista kan associeras med varje försäljningsområde.

En organisationsenhet är en intern grupp eller avdelning i företaget som spårar kostnader för en uppsättning roller som den säljer till andra avdelningar eller till externa kunder.

**Exempel som visar en möjlig skillnad i utformningen för organisationsenheter och försäljningsterritorier**

Contoso, Ltd. har två utvecklingscenter: Contoso US och Contoso Indien. Kostnaden för resurser varierar kraftigt mellan dessa två utvecklingscenter. Contoso säljer sina tjänster inom informationsteknik (IT) på många internationella marknader, t.ex. Latinamerika, Nordamerika, Asien, Stilla havet, Västeuropa och Mellanöstern. Faktureringskurserna för samma projektroller kan variera mycket över dessa marknader. Contoso US och Contoso Indien bör upprättas som organisationsenheter och varje organisationsenhet bör ha en egen självkostnadslista. Asien och Stilla havet, Latinamerika, Nordamerika, Västeuropa och Mellanöstern ska vara inställda på försäljningsområden och varje försäljningsområde bör ha en egen försäljningsprislista.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Varför finns det en begränsning för associationen mellan prislistorna och organisationsenheterna?

Försäljningspriserna är vanligtvis unika för de geografiska områden eller marknader där tjänster säljs. De interna avdelningarna i ett företag har vanligtvis inget eget försäljningspris för samma slags tjänster. Interna indelningar har emellertid en annan kostnad för sålda varor (COGS), beroende på hur de personer som de anställs och arbetsförhållandena i regionen är verksamma. Eftersom organisationsenheter är modellerade som interna divisioner i ett företag, kan de bara ha självkostnadslistor.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Varför går det inte att associera försäljningsprislistor med organisationsenheter?

I Project Operations kan försäljningsprislistor associeras med kunder och försäljningsområden. Transaktionella entiteter såsom affärsmöjlighet, offert, projektkontrakt och projekt använder försäljningsprislistor som är kopplade till kundkontot eller försäljningsområdet för att bestämma faktureringspriser och potentiell omsättning för projektåtagandet.

Självkostnadslistor är kopplade till organisationsenheter. Transaktionella entiteter såsom affärsmöjlighet, offert, projektkontrakt och projekt använder självkostnadslistor som är kopplade till den upphandlande enheten för att avgöra kostnaderna för ett projektengagemang.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Är organisationsenheter hierarkiska i Project Operations?

Nej. I den aktuella versionen av Project Operations är organisationsenheterna inte hierarkiska. Du kan därför inte utföra följande uppgifter:

- Konfigurera ett mönster för att ange standardkostnadspriser som färdas uppåt genom en hierarki.
- Rapportera intäkter eller kostnader som slås ihop på olika nivåer i organisationsenhetens hierarki.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Vi är ett stort multinationellt företag som har en komplex hierarki med kostnadsställen, avdelningar och faktureringskontor på flera nivåer. Hur kan vi bäst använda konceptet med organisationsenheter i den aktuella versionen av Project Operations?

När du har en komplex hierarki med kostnadsställen, avdelningar, faktureringskontor och så vidare ställer du in de lövnoder som distinkta organisationsenheter.

I följande exempel visas en typisk hierarki.

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

Om hierarkin liknar detta exempel måste du konfigurera den som en plan lista, som visas här:

- Contoso India - SAP-praxis – tekniska konsulter
- Contoso India - SAP-praxis – funktionella konsulter
- Contoso India - Microsoft-teknikpraxis för funktionella konsulter
- Contoso India - Microsoft-teknikpraxis för funktionella konsulter
- Contoso US - SAP-praxis – tekniska konsulter
- Contoso US - SAP-praxis – funktionella konsulter
- Contoso US - Microsoft-teknikpraxis - tekniska konsulter
- Contoso US - Microsoft-teknikpraxis - funktionella konsulter

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Vi är ett litet företag som bara arbetar med en avdelning. Hur kan vi bäst använda konceptet med organisationsenheter i den aktuella versionen av Project Operations?

Om företaget fungerar som en enhet som har en självkostnadsprislista behöver du inte skapa några organisationsenheter. Installationen av Project Operations skapar en standardorganisationsenhet som har samma namn som organisationen. Som standard är tilldelas alla användare denna organisationsenhet. När systemet kräver att en organisationsenhet väljs kommer denna organisationsenhet att väljas som standard.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>När ett projekt skapas från en offert eller en projektkontraktrad kommer den upphandlande standardenheten att komma från offert eller projektkontraktet. Vilken är den upphandlande standardenheten om ett projekt skapas före försäljningsentiteter som offert eller projektkontrakt?

När ett projekt skapas separat baseras den upphandlande standardenheten i projektet på den användare som skapar den. Den användaren är även standardprojektledare. Om projektet är mappat till en försäljningsenhet, t.ex. en offert eller ett projektkontrakt, baseras den upphandlande enheten av projektet på entiteten försäljning istället. I det här fallet kan projektuppskattningar räknas om, eftersom självkostnadsprislistan används för att beräkna kostnadsuppskattningsändringarna om den upphandlande enheten ändras. Försäljningsprislistan används för att beräkna de försäljningsuppskattningar som ska ändras så att dessa synkroniseras med projektprislistan för offerten.

Fälten **Kontrakteringsenhet** och **Valuta** för projektet är låsta för redigering, detta eftersom de måste synkroniseras med värdena i försäljningsentiteten (offert eller projektkontrakt) som projektet är mappat till.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Skapa och underhålla organisationsenheter i Project Operations

Följ dessa steg för att skapa en organisationsenhet i Project Operations.

1. Gå till **Inställningar \> Organisationsenheter**.
2. Välj **Nytt**.
3. I området **Allmänt** anger du ett namn för organisationsenheten i fältet **Namn**. Ange sedan de andra fälten efter behov.
4. Välj **Spara** för att skapa posten så att du kan fortsätta redigera den.
5. Under **Prislista för självkostnad**, väljer du plustecknet (**+**) för att lägga till en prislista. Här kan du endast lägga till prislistor som har kontexten **Kostnad**.
6. I fältet **namn** väljer du knappen **Sök** och väljer sedan en prislista som du vill göra tillgänglig för organisationsenheten. Fortsätt lägga till prislistor efter behov.
7. När du är klar med att lägga till prislistor väljer du **Spara** längst ned till höger på sidan.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
