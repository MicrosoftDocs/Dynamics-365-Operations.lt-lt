---
title: Sukonfigūruoto produkto pardavimo užsakymo kūrimas
description: Šioje procedūroje parodoma, kaip konfigūracijos šabloną taikyti pardavimo užsakymo produktui.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81e573593fbbb0bf87e53c5cbd985b38a8db89ac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841604"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Sukonfigūruoto produkto pardavimo užsakymo kūrimas

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip konfigūracijos šabloną taikyti pardavimo užsakymo produktui. Šiame pavyzdyje naudojamas D0006 garsiakalbio modelis demonstracinių duomenų įmonėje USMF. Paprastai šią procedūrą naudoja pardavimo užsakymų procesorius.


## <a name="create-a-sales-order"></a>Kurti pardavimo užsakymą
1. Spustelėkite Pardavimo užsakymo apdorojimas ir užklausa.
2. Spustelėkite Naujas.
3. Spustelėkite Pardavimo užsakymas.
4. Lauke Kliento kodas pasirinkite US-001. 
5. Spustelėkite GERAI.
6. Lauke Prekės numeris pasirinkite D0006.
    * Šiai užduočiai atlikti turite pasirinkti konfigūruojamą produktą.  
7. Spustelėkite Produktas ir tiekimas.
8. Spustelėkite Konfigūruoti eilutę.
    * Atkreipkite dėmesį, kad kaina buvo pakeista pagal pasirinktą konfigūraciją, o laukas Įtraukti laidą dabar yra nustatytas į parinktį True.  
    * Įsiminkite pasirinktus laido parametrus ir numatytąją kainą.  
9. Spustelėkite Įkelti šabloną.
    * Šiame pavyzdyje parodoma, kaip galite pritaikyti šabloną, norėdami pasirinkti iš anksto nustatytą konfigūraciją. Jei naudojate šią procedūrą kaip užduočių vedlį ir norite matyti kitas atributų reikšmes, kurias galima naudoti, turite spustelėti mygtuką Atrakinti.  
10. Spustelėkite GERAI.
11. Spustelėkite GERAI.
12. Išplėskite skyrių Eilutės informacija.
13. Spustelėkite skirtuką Produktas.
    * Dabar prekės konfigūracija yra pateikta produkto dimensijose.  
14. Uždarykite puslapį.

## <a name="select-the-product-configuration"></a>Produkto konfigūracijos pasirinkimas



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]