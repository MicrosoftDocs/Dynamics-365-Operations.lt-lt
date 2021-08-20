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
ms.openlocfilehash: f128518af01911a29ae297670883ef425f9117d65cc952cc1ffdb044c4ce085f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781907"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Sukonfigūruoto produkto pardavimo užsakymo kūrimas

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip konfigūracijos šabloną taikyti pardavimo užsakymo produktui. Šiame pavyzdyje naudojamas D0006 garsiakalbio modelis demonstracinių duomenų įmonėje USMF. Paprastai šią procedūrą naudoja pardavimo užsakymų procesorius.

## <a name="create-a-sales-order"></a>Kurti pardavimo užsakymą

1. Eikite **į pardavimo ir rinkodaros darbo sričių pardavimo užsakymo \> \> apdorojimą ir užklausą**.
1. Pasirinkite **Naujas**.
1. Pasirinkite **Pardavimo užsakymas**.
1. Lauke **Kliento kodas** pasirinkite *„US-001”*. 
1. Pasirinkite **Gerai**.
1. Lauke **Prekės numeris** pasirinkite *D0006*.
    * Šiai užduočiai atlikti turite pasirinkti konfigūruojamą produktą.  
1. Rinkitės **Produktas ir tiekimas**.
1. Pasirinkite **Eilutės konfigūravimas**.
    * Atkreipkite dėmesį, kad kaina buvo pakeista pagal pasirinktą konfigūraciją, o laukas Įtraukt **laidą** laukelis dabar nustatytas į parinktį *Teisnga*.  
    * Įsiminkite pasirinktus laido parametrus ir numatytąją kainą.  
1. Pasirinkite **Įkelti šabloną**.
    * Šiame pavyzdyje parodoma, kaip galite pritaikyti šabloną, norėdami pasirinkti iš anksto nustatytą konfigūraciją. Jei naudojate šią procedūrą kaip užduočių vedlį ir norite matyti kitas atributų reikšmes, kurias galima naudoti, turite spustelėti mygtuką **Atrakinti**.  
1. Pasirinkite **Gerai**.
1. Pasirinkite **Gerai**.
1. Išplėskite skyrių **Eilutės informacija** section.
1. Produkto **skirtuko** pasirinkimas.
    * Dabar prekės konfigūracija yra pateikta produkto dimensijose.  
1. Uždarykite puslapį.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]