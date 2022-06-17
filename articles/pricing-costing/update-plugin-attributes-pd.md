---
title: Uppdatera attribut för plugin-program med nya prissättningsdimensioner
description: I den här artikeln finns information om hur du uppdaterar plugin-attribut för prissättningsdimensioner.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920036"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Uppdatera attribut för plugin-program med nya prissättningsdimensioner

I den här artikeln finns information om hur du uppdaterar plugin-attribut för prissättningsdimensioner.

> [!NOTE]
> Den här artikeln gäller endast offert- och kontraktfunktionerna i Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Förutsättningar
Innan du slutför stegen i den här artikeln måste du ha slutfört procedurerna i följande artiklar:

  - [Skapa anpassade fält och entiteter](create-custom-fields-entities-pricing-dimensions.md) 
  - [Lägga till anpassade fält i prisinställningar och transaktionella entiteter](add-custom-fields-price-setup-transactional-entities.md)
  - [Konfigurera anpassade fält som prissättningsdimensioner](set-up-custom-fields-pricing-dimensions.md). 
  
Om du inte har slutfört de här procedurerna slutför du dem och går sedan tillbaka till artikeln.

## <a name="register-a-plug-in"></a>Registrera ett plugin-program
När en offertradsdetalj skapas på sidan **Offertrad** för en projektoffertrad skapar systemet två uppskattningsrader. En rad är för kostnadssidan av uppskattningen och den andra raden är för försäljningsidan. Det här är samma för projektkontraktrader.

När du gör en ändring av kvantiteten eller ett fält på kostnadssidan görs samma ändring också på försäljningssidan. Detta är möjligt eftersom plugin-program för PreOperation på Quotelinedetail och kontraktline-detaljentiteter kopplar specifika attribut på kostnadssidan till transaktionens försäljningssida. Om ändringar som utförts på prissättningens dimensionsvärden på försäljningssidan också måste utföras på kostnadssidan, måste följande plugin-program registreras på nytt efter att du har gjort ändringar i en prissättningsdimension.

Dessa är de plugin-program som ska uppdateras och registreras om:

- PreOperationContractLineDetailUpdate - **Uppdatera msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **Uppdaterar msdyn_quotelinetransaction**

Slutför följande steg för att uppdatera och registrera om plugin-programen.

1. Öppna **PluginRegistrationTool** och anslut till din Project Operations Dataverse-miljö.
2. Välj **Sök** och skriv in de första bokstäverna i plugin-programmet som ska uppdateras.
3. När du har hittat plugin-programmet markerar du det och klickar sedan på **Välj på huvudformulär**.
4. Markera steget **Uppdatera msdyn_orderlinetransaction**, högerklicka och välj sedan **Uppdatera**.
5. I dialogfönstret **Uppdatera** väljer du ellipsen (**...**) bland filtreringsattributen.
6. Fönstret för filtreringsattribut öppnas och visar en lista över alla attribut i entiteten samt prissättningsdimensionerna. Markera kryssrutorna för attributen för prissättningsdimensionen.
7. Välj **OK** för att stänga sidan, och välj sedan **Uppdatera steg**.
8. Upprepa steg 2-7 för det andra plugin-programmet, **PreOperationQuoteLineDetail**. För detta plugin-program måste du uppdatera steget **Uppdatera msdyn_quotelinetransaction**.
9. Stäng **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]