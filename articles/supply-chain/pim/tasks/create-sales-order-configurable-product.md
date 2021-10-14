---
title: Sukonfigūruoto produkto pardavimo užsakymo kūrimas
description: Šioje procedūroje parodoma, kaip konfigūracijos šabloną taikyti pardavimo užsakymo produktui.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e42f121d1efa66f85a3dd811606962b907ed177d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570590"
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