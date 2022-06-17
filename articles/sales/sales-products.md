---
title: Produkter
description: Den här artikeln innehåller information om produktkatalogen som du kan använda för att ge information till kunderna om produkterna och prissättningen av organisationens erbjudanden.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d45a705c48df84a8f5b3f60121fbcc25e225e6e5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933100"
---
# <a name="products"></a>Produkter

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Produkter utgör stommen i verksamheten. Produktkatalogen i Dynamics 365 Sales Professional är en samling med produkter och deras prisinformation. Gör det enklare för dina säljare att öka sin försäljning genom att skapa en produktkatalog snabbt.

## <a name="add-a-product"></a>Lägga till en produkt

1.  Kontrollera att du har rollen Försäljningsansvarig eller Systemadministratör så du kan lägga till produkter i Dynamics 365 Sales Professional.
2.  I webbplatsöversikten under **Konfiguration** väljer du **Produkter**.
3.  Välj **Lägg till produkt** och fyll i följande information:

    -  **Namn**
    -  **Produkt-ID**
    -  **Överordnad**: Välj en överordnad produktfamilj för produkt. Om du skapar en underordnad produkt i en produktfamilj fylls namnet på den överordnade produktfamiljen i här. Detta kan inte ändras när posten har sparats.
    -  **Giltigt från**/**Giltigt till**: Definierar den period som produktpaketet är giltigt för genom att välja ett **Giltigt från**- och **Giltigt till**-datum.
    -  **Enhetsgrupp**: Välj en enhetsgrupp. En enhetsgrupp är en samling av olika enheter som en produkt säljs i, och definierar hur enskilda objekt grupperas i större kvantiteter. Om du till exempel vill lägga till utsäde som en produkt, kan du har skapat en enhetsgrupp som heter "Frö" och definierat dess primära enhet som "paket".
    -  **Standardenhet**: Välj den vanligaste enheten som produkten säljs i. Enheterna är de kvantiteter eller de mått du säljer dina produkter i. Om du har lagt till utsäde som en produkt, kan du till exempel säljer dem i paket, lådor och lastpallar. Var och en av dessa blir en enhet för produkten. Om utsäde oftast säljs i paket väljer du det som enhet.
    -  **Standardprislista**: Om det är en ny produkt är fältet skrivskyddat. Innan du kan välja en standardprislista måste du fylla i alla obligatoriska fält och sedan spara posten. Även om standardprislista inte är obligatoriskt, är det en god idé att ange en standardprislista för varje enskild produkt när du har sparat produktposten. Om en kundpost sedan inte innehåller någon prislista kan Sales använda standardprislistan för att skapa offerter, order och fakturor.
    -  **Antal decimaler**: Ange ett heltal mellan 0 och 5. Om produkten inte kan delas upp i delade kvantiteter anger du 0. Precisionen för fältet **Kvantitet** i offert, order eller fakturapost verifieras mot värdet i det här fältet om produkten inte har någon associerad prislista.
    -  **Ämne**: Associera produkten med ett ämne. Använd ämnen om du vill kategorisera dina produkter och filtrera rapporter.

4.  Välj **Spara**.
5.  Fliken **Ytterligare information**. I avsnittet **Prislisteposter** går du till **Fler kommandon** och väljer **Lägg till ny prislistepost**.
7.  På fliken **Ytterligare information** i avsnittet **Produktrelation**, välj ikonen **Fler kommandon** och välj **Lägg till ny produktrelation.**
8.  I formuläret **Ny produktrelation**, anger du följande information och på kommandofältet väljer du **Spara och stäng**:

    -   **Relaterad produkt**: Välj en produkt som du vill lägga till som en produkt som är relaterade till den befintliga produktpost som du arbetar med.
    -   **Försäljningsrelationens typ**: Välj om du vill lägga till produkten som merförsäljnings-, korsförsäljnings-, tillbehörs- eller ersättningsprodukt.
    -   **Riktning**: Välj om förhållandet mellan produkterna ska vara enkelriktat eller dubbelriktat. När du väljer enkelriktad visas den produkt som du väljer i **Relaterad produkt** som rekommendation för den befintliga produkten, men inte tvärtom.

9.  I formuläret Produkt väljer du **Spara**.

## <a name="import-products"></a>Importera produkter

Du kan använda importmallar för att överföra produktdata till Dynamics 365 Sales.

## <a name="revise-a-product"></a>Revidera en produkt

Håll produktinformation uppdaterad genom att snabbt ändra egenskaperna för produkterna efter behov, och publicera om informationen så att säljarna kan se de senaste ändringarna i lagret.

1.  Kontrollera att du har en av följande säkerhetsroller eller motsvarande behörigheter: Systemadministratör, Systemanpassare, Försäljningsansvarig, Försäljningschef, Marknadschef eller VD, eller motsvarande behörighet.
2.  I webbplatsöversikten, markera **produkter**.
3.  Öppna en aktiv produkt som du vill ändra och välj **Revidera** i kommandofältet.
4.  I dialogrutan **Bekräfta ändring** väljer du **Bekräfta**. Detta ändrar produktstatusen till **Under revision**.
5.  När du är klar med ändringarna väljer du **Publicera** på kommandofältet.

    > [!TIP]
    > Om du vill återställa ändringarna och fortsätta med den senast aktiva versionen av produkten väljer du **Återställ**. Då ändras status för produkten tillbaka till **Aktiv**.

## <a name="clone-a-product"></a>Klona en produkt 

När du skapar en ny produkt kan du spara tid genom att klona ett befintligt. Detta skapar en kopia av den ursprungliga posten med allt utom namn och ID.

1.  Kontrollera att du har en av följande säkerhetsroller eller motsvarande behörigheter: Systemadministratör, Systemanpassare, Försäljningsansvarig, Försäljningschef, Marknadschef eller VD, eller motsvarande behörighet.
2.  I webbplatsöversikten, markera **produkter**.
3.  Välj en produktpost som du vill klona och klicka sedan på **Klona** i kommandofältet. En dialogruta för bekräftelse visas.
4.  Välj **Bekräfta**.

En ny produktpaketpost öppnas med samma information som den ursprungliga, förutom namn och ID.

## <a name="retire-a-product"></a>Dra in en produkt 

Om din organisation inte längre säljer en produkt kan du dra in den så att produkten inte längre är tillgänglig för dina säljare.

1.  Kontrollera att du har rollen Systemadministratör eller Sales Professional-ansvarig, eller motsvarande behörighet.
2.  I webbplatsöversikten, markera **produkter**.
3.  Öppna en aktiv produkt som du vill dra in och välj **Dra in** i kommandofältet.
4.  I dialogrutan **Bekräfta Dra in** väljer du **Bekräfta**.


## <a name="delete-a-product"></a>Ta bort produkt

Ta bort en produkt om du vill sluta sälja den.

> [!IMPORTANT]
> Du kan inte återställa en borttagen post.

1.  Kontrollera att du har rollen Systemadministratör eller Sales Professional-ansvarig, eller motsvarande behörighet.
2.  I webbplatsöversikten, markera **produkter**.
3.  Välj en produktpost som du vill ta bort och klicka sedan på **Ta bort** i kommandofältet.
4.  I dialogrutan **Bekräfta borttagning** väljer du **Fortsätt**.
 
 ## <a name="quantity-factors-for-products"></a>Kvantitetsfaktorer för produkter

Kvantitetsfaktorer för att stödja försäljning av prenumerationsbaserade produkter. För prenumerationsbaserade produkter uttrycks kvantitet på offert- eller projektkontraktraden som antalet användarmånader.

Vanligt vis lagras priset på prenumerationsprogram i katalogen som priset per användare i månaden. Du kan emellertid använda andra tidsbeskrivningar i stället. Under försäljningsprocessen är priset på offertraden vanligtvis per användare, per månadspris som förhandlas fram och rabatteras av IT-säljaren. Varje avtal har ett annat antal användare och ett annat antal prenumerationsmånader. Den kvantitet som används för att beräkna beloppet på offertraden är en produkt av antalet användare och antalet prenumerationsmånader.

För kvantitetskategorin förlitar sig sig på produktattribut. När du konfigurerar specifika egenskaper för en produkt kan du använda för att flagga en del uppsättning av dessa egenskaper, eller alla egenskaper, som kvantitetsfaktorer.

Systemet verifierar att endast numeriska egenskaper eller produktegenskaper som har en numerisk datatyp är flaggade som kvantitetsfaktorer. När en produkt som du har konfigurerat kvantitetsfaktorer för läggs till på en offertrad blir fältet **kvantitet** på offertraden skrivskyddat. När du har angett värden för produktegenskaper som är kvantitetsfaktorer beräknas kvantiteten på offertraden.

Om det till exempel finns följande egenskaper: 

- **Antal användare**: antalet användare 
- **Antal månader**: antalet prenumerationsmånader
- **Produkt-SKU** 

Egenskaperna **Antal användare** och **Antal för månader** kan flaggas som kvantitetsrapporter genom att egenskaperna för produktraden redigeras. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]