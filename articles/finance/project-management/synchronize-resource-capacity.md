---
title: Išteklių pajėgumų sinchronizavimas
description: Šioje temoje pateikiama informacija apie tai, kaip sinchronizuoti išteklių pajėgumą įvairiuose kalendoriuose ir projektuose.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760612"
---
# <a name="synchronize-resource-capacity"></a>Išteklių pajėgumų sinchronizavimas

[!include [banner](../includes/banner.md)]

Išteklių sinchronizavimo procesai padeda užtikrinti, kad kalendoriaus ir pagrindinio kalendoriaus informacija būtų perduodama bei naudojama ir planuojant projekto išteklius. Jei kalendorius pakinta, procesais pagal poreikį atnaujinamas projekto išteklių planavimas. Šie procesai taip pat padeda gerinti našumą, nes kalendoriaus išteklių informacija sinchronizuojama iš anksto. Todėl greičiau atnaujinama išteklių planavimo informacija. Rekomenduojame procesus planuoti kaip paketą, o ne po vieną. Kitu atveju atsiranda rizika, kad kažkas pamirš informacijos paskutinį sinchronizavimą apimančias datas. Jei apimančiosios datos nenaudojamos, sinchronizuojant datas gali atsirasti tarpų.

![Kalendoriaus sinchronizavimas](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Sinchronizuoti išteklių pajėgumų sumavimus

Sinchronizavimo procesas skirtas sinchronizuoti visai išteklių kalendoriaus informacijai. Ši informacija apima pagrindinio kalendoriaus informaciją apie visus projekto išteklių kalendoriaus pajėgumo lentelės keitimus. Jei į projektą įtraukiama naujų išteklių, sinchronizavimas padeda užtikrinti, kad būtų prieinama atnaujinta kalendoriaus informacija. Šį sinchronizavimą galima atlikti bet kuriuo metu.

Rekomenduojame naudoti paketą. Parinktys galimos sinchronizuojant pajėgumų rezervavimus.

1. Pasirinkite **Projektų valdymas ir apskaita** &gt; **Laikotarpio** &gt; **Pajėgumo sinchronizavimas** &gt; **Sinchronizuoti išteklių pajėgumų sumavimus**.
2. Nustatykite tolesnėje lentelėje nurodytas parinktis.

    | Parinktis      | aprašymas |
    |-------------|-------------|
    | Laikotarpio kodas | Pasirenkama: pasirinkite didžiosios knygos datų intervalo kodą, kad nustatytumėte išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios ir pabaigos datas. |
    | Pradžios data  | Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios datą. |
    | Pabaigos data    | Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pabaigos datą. |

[![Sinchronizavimo procesas](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)
