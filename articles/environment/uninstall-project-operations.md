---
title: AvinstalleraDynamics 365 Project Operations
description: I detta ämne finns information om hur du avinstallerar Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783665"
---
# <a name="uninstall-dynamics-365-project-operations"></a>AvinstalleraDynamics 365 Project Operations 

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

För att avinstallera Dynamics 365 Project Operations måste du ha tilldelats rollen Administratör.

1. Gå till **Inställningar** > **Lösningar**.

    ![Sidan Inställningar.](./media/uninstall-proj-ops-solutions.png)
  
2. Ta bort lösningarna i exakt den ordning som de anges i följande tabell. 

    | Steg | Lösningsnamn                                    | Anteckning                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 2 | ProjectOperations_Anchor                           | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 5 | ProjectService                                     | Inga ytterligare kommentarer.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Inga ytterligare kommentarer.                                                                         |
    | 7 | ProjectServiceCore                                 | Inga ytterligare kommentarer.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 9 | FieldServiceCommon                                 | Krävs för dubbelskrivning med Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Krävs för dubbelskrivning med Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Krävs för Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Krävs för Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Krävs för Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Krävs för Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Krävs för Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Krävs för Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Krävs för Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 19 | Dynamics365Notes                                   | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 21 | DualWriteCore                                      | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 23 | Dynamics365AssetManagement                         | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 26 | HCMCommon                                          | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 28 | Part                                              | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 29 | Dynamics365Company                                 | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 30 | CurrencyExchangeRates                              | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |
    | 31 | AssetCommon                                        | Om ingen lösning hittas kan du hoppa över den här lösningen.                                                            |