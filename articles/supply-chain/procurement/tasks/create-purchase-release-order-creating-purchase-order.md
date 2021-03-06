---
title: Kurti pirkimo leidimą išduoti kuriant pirkimo užsakymą
description: Ši procedūra nurodo, kaip naudoti pirkimo sutartį, kai kuriate pirkimo užsakymą.
author: kamaybac
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2f02961f5f7da9bff389737b447e3b143dd72e3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812277"
---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a>Kurti pirkimo leidimą išduoti kuriant pirkimo užsakymą

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip naudoti pirkimo sutartį, kai kuriate pirkimo užsakymą. Pirkimo sutartis turi būti taikoma, kai kuriate pirkimo užsakymą, nes yra bendrų sąlygų, kurios turi būti nukopijuotos į pirkimo užsakymo antraštę. Šią užduotį paprastai atlieka pirkimo agentas. Būtina šio vadovo sąlyga – privalote turėti galiojančią pirkimo sutartį su tiekėjo įsipareigojimu dėl produkto kiekio ir prekių. Saugojimo dimensijų grupė nustato, kurios saugojimo dimensijos bus naudojamos produktų operacijoms. Šį vadovą galite vykdyti demonstracinių duomenų įmonėje USMF. Jei naudojate USMF, galite pirmiausia paleisti vadovą „Kurti pirkimo sutartį“, kad įvykdytumėte būtinas išankstines šio vadovo sąlygas.


## <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas
1. Atidarykite pirkimo užsakymo rengimo darbo sritį.
2. Spustelėkite „Naujas pirkimo užsakymas“.
3. Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Perjunkite dalies Bendra išplėtimą.
7. Lauke „Pirkimo sutartis“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Čia išvardytos visos esamos sutartys su tiekėjais. Raskite galiojančią sutartį, kurią norite naudoti.  
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Spustelėkite Taip.
10. Spustelėkite GERAI.

## <a name="add-a-line"></a>Įtraukti eilutę
1. Lauke Prekės numeris surinkite reikšmę.
    * Jei įsipareigojimas nurodo konkrečias atsargų arba vietos dimensijas, turite įvesti tas pačias reikšmes ir pirkimo užsakymo eilutėje, kad galėtumėte naudotis sutartimi.  
2. Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Svetainėje jau gali būti įvesta numatytoji reikšmė iš užsakymo arba iš tiekėjo. Tokiu atveju praleiskite šį veiksmą.  
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Lauke Kiekis įveskite skaičių.
    * Patikrinkite, ar kaina nukopijuota iš įsipareigojimo.  

## <a name="look-up-the-commitment"></a>Ieškoti įsipareigojimo
1. Spustelėkite eilutę „Atnaujinti“.
2. Spustelėkite „Pridėta“.
    * Čia galite gauti informaciją apie pirkimo sutartį. Pvz., galite matyti kainą ir ar kaina bei nuolaida yra fiksuotos – tai reiškia, kad pakeitus kainos ar nuolaidos reikšmę pirkimo užsakyme į kitą nei nurodyta įsipareigojime, sistema pašalins saitą, todėl pirkimo užsakymo eilutė neatitiks įsipareigojimo. Taip pat galite matyti, ar pasirinkta parinktis „Maksimaliai vykdoma“ – tai reiškia, kad negalima viršyti įsipareigojime nurodyto kiekio sudedant visus pirkimus, kurie atitinka įsipareigojimą.  
3. Uždarykite puslapį.

## <a name="look-up-the-purchase-agreement"></a>Ieškoti pirkimo sutarties
1. Veiksmų srityje spustelėkite Bendra.
2. Spustelėkite „Pirkimo sutartis“.
3. Uždarykite puslapį.
4. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]