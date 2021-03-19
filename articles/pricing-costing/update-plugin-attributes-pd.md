---
title: Uppdatera attribut för plugin-program med nya prissättningsdimensioner
description: I den här ämnet finns information om hur du uppdaterar plugin-attribut för prissättningsdimensioner.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274705"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Uppdatera attribut för plugin-program med nya prissättningsdimensioner

I den här ämnet finns information om hur du uppdaterar plugin-attribut för prissättningsdimensioner.

> [!NOTE]
> Detta ämne är endast tillämpligt på offert- och kontraktsfunktionerna i Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Förutsättningar
Innan du slutför stegen i detta ämne måste du ha slutfört procedurerna i följande avsnitt:

  - [Skapa anpassade fält och entiteter](create-custom-fields-entities-pricing-dimensions.md) 
  - [Lägga till anpassade fält i prisinställningar och transaktionella entiteter](add-custom-fields-price-setup-transactional-entities.md)
  - [Konfigurera anpassade fält som prissättningsdimensioner](set-up-custom-fields-pricing-dimensions.md). 
  
Om du inte har slutfört dessa procedurer går du tillbaka och slutför dem och går sedan tillbaka till detta ämne.

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