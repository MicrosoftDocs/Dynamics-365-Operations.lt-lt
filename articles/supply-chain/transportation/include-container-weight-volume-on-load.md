---
title: Konteinerio svorio ir tūrio įtraukimas kraunant
description: Šiame straipsnyje aprašoma, kaip nustatyti ir taikyti funkcijas, kad būtų galima įtraukti konteinerio svorį ir tūrį kroviniams.
author: Weijiesa
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66dc84171f8b175476f37f736489d3d83cacfe57
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897406"
---
# <a name="include-container-weight-and-volume-on-load"></a>Konteinerio svorio ir tūrio įtraukimas kraunant

[!include [banner](../includes/banner.md)]

Naudojant krovinio konteinerių svorio ir tūrio įtraukimo funkciją, aiškiai perteikiamas bendrasis į krovinį perkeliamų konteinerių ir prekių svoris bei tūris.

Krovinyje yra viena siunta arba kelios siuntos, o jose yra atskirų prekių, priklausančių vienam pardavimo užsakymui arba keliems pardavimo užsakymams. Prekės saugomos konteineryje, o konteineriai pakraunami į krovinį. Ne konteineryje esančios prekės taip pat gali būti krovinio dalis. Pagal šias sąlygas sistema apskaičiuoja krovinio svorio ir tūrio reikšmes, atsižvelgdama į tiek konteinerių, tiek prekių svorį bei tūrį.

Jei apskaičiuotos reikšmės nėra tikslios, jas galite pakoreguoti įvesdami faktines krovinio svorio ir tūrio reikšmes. Svorio ir tūrio reikšmės naudojamos vykdant transportavimo valdymo procesus. Pavyzdžiui, šios reikšmės naudojamos tarifo ir maršruto darbo srityje, kurioje jos padeda apibrėžti krovinių tarifą ir maršrutą; reikšmės taip pat naudojamos su transportavimo mokėjimo priemonėmis ir registruojant vairuotojus.

## <a name="where-it-applies"></a>Kai taikoma

Krovinio konteinerių svorio ir tūrio įtraukimo funkcija taikoma vykdant transportavimo valdymo procesus, pvz., tarifo ir maršruto darbo srityje, su transportavimo mokėjimo priemonėmis ir registruojant vairuotojus.

## <a name="how-it-is-set-up"></a>Kaip tai nustatoma

Kiek konteinerių turėtų reikėti kroviniui, apskaičiuojama pagal konteinerio svorį bei tūrį ir pagal konteinerio naudojimo procentą.

-   Norėdami nustatyti konteinerio svorį ir tūrį, spustelėkite **Sandėlio valdymas** \> **Sąranka** \> **Konteineriai** \> **Konteinerių tipai**.

-   Norėdami nustatyti konteinerio naudojimo procentą, spustelėkite **Sandėlio valdymas** \> **Sąranka** \> **Konteineriai** \> **Konteinerių grupės** ir lauke **Konteinerio naudojimo procentas** įveskite reikšmę.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]