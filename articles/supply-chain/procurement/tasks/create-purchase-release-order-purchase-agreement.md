---
title: Pirkimo sutarties taikymas kuriant pirkimo užsakymą
description: Ši procedūra nurodo, kaip naudoti pirkimo sutartį, kai kuriate pirkimo užsakymą.
author: GalynaFedorova
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a21821d75be2d5340cd418c12be39431870d2779
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678749"
---
# <a name="apply-a-purchase-agreement-when-creating-a-purchase-order"></a>Pirkimo sutarties taikymas kuriant pirkimo užsakymą

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip naudoti pirkimo sutartį, kai kuriate pirkimo užsakymą. Pirkimo sutartis privalo būti taikoma, kai kuriate pirkimo užsakymą, nes yra bendrų sąlygų, kurios turi būti nukopijuotos į pirkimo užsakymo antraštę. Šią užduotį paprastai atlieka pirkimo agentas. Būtina šio vadovo sąlyga – privalote turėti galiojančią pirkimo sutartį su tiekėjo įsipareigojimu dėl produkto kiekio ir prekių. Saugojimo dimensijų grupė nustato, kurios saugojimo dimensijos bus naudojamos produktų operacijoms.

## <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas

1. Eikite į **Gamyba ir išteklių tiekimas \> Darbo sritys \> Pirkimo užsakymo parengimas**.
1. Veiksmų srityje pažymėkite **Naujas pirkimo užsakymas**.
1. Atidaromas **Kurti pirkimo užsakymą** dialogo langas. Pasirinkite **Tiekėjo sąskaitą**. Jei reikia, patikrinkite ir pakoreguokite kitus adreso laukus.
1. Išplėskite **Bendra** FastTab.
1. Lauke **Pirkimo sutartis** suraskite ir pasirinkite norimą naudoti galiojančią sutartį. Čia išvardytos visos esamos sutartys su tiekėjais.  
1. Pasirinkite **Taip**.
1. Pasirinkite **Gerai**.

## <a name="add-a-line"></a>Įtraukti eilutę

1. Lauke **Prekės numeris** įveskite vertę. Jei įsipareigojimas nurodo konkrečias atsargų arba vietos dimensijas, turite įvesti tas pačias reikšmes ir pirkimo užsakymo eilutėje, kad galėtumėte naudotis sutartimi.
1. Lauke **Vieta** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą. Svetainėje jau gali būti įvesta numatytoji reikšmė iš užsakymo arba iš tiekėjo. Tokiu atveju praleiskite šį veiksmą.  
1. Sąraše raskite ir pasirinkite norimą įrašą.
1. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
1. Lauke **Kiekis** įveskite skaičių. Patikrinkite, ar kaina nukopijuota iš įsipareigojimo.  

## <a name="look-up-the-commitment"></a>Ieškoti įsipareigojimo

1. Pasirinkite **Naujinti eilutę**.
1. Pažymėkite **Pridėta**. Čia galite gauti informaciją apie pirkimo sutartį. Pvz., galite matyti kainą ir ar kaina bei nuolaida yra fiksuotos – tai reiškia, kad pakeitus kainos ar nuolaidos reikšmę pirkimo užsakyme į kitą nei nurodyta įsipareigojime, sistema pašalins saitą, todėl pirkimo užsakymo eilutė neatitiks įsipareigojimo. Taip pat galite matyti, ar pasirinkta parinktis „Maksimaliai vykdoma“ – tai reiškia, kad negalima viršyti įsipareigojime nurodyto kiekio sudedant visus pirkimus, kurie atitinka įsipareigojimą.  
1. Uždarykite puslapį.

## <a name="look-up-the-purchase-agreement"></a>Ieškoti pirkimo sutarties

1. Pasirinkę **Veiksmų sritis**, pasirinkite **Bendra**.
1. Pasirinkite **Pirkimo sutartis**.
1. Uždarykite puslapį.
1. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]