---
title: Sukurti pirkimo leidimo užsakymą iš pirkimo sutarties
description: Ši procedūra nurodo, kaip naudoti pirkimo sutartį, kai kuriate pirkimo užsakymą.
author: mkirknel
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da25486207319879a9acc8376f3f2c78f9b8d939
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149693"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a>Sukurti pirkimo leidimo užsakymą iš pirkimo sutarties

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip naudoti pirkimo sutartį, kai kuriate pirkimo užsakymą. Pirkimo sutartis turi būti taikoma, kai kuriate pirkimo užsakymą, nes yra bendrų sąlygų, kurios turi būti nukopijuotos į pirkimo užsakymo antraštę. Šią užduotį paprastai atlieka pirkimo agentas. Būtina šio vadovo sąlyga – privalote turėti galiojančią pirkimo sutartį su tiėkėjo įsipareigojimu dėl produkto kiekio ir prekių. Saugojimo dimensijų grupė nustato, kurios saugojimo dimensijos bus naudojamos produktų operacijoms. Šį vadovą galite vykdyti demonstracinių duomenų įmonėje USMF. Jei naudojate USMF, galite pirmiausia paleisti vadovą „Kurti pirkimo sutartį“, kad įvykdytumėte būtinas išankstines šio vadovo sąlygas.


## <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas
1. **Naršymo sritis** eikite į **Darbo sritys > Pirkimo užsakymo paruošimas**. 
2. Spustelėkite **Naujas pirkimo užsakymas**. 
3. Lauke **Tiekėjo sąskaita** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Išplėskite „fastTab“ **Bendra**.
7. Lauke **Pirkimo sutartis** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą. Čia išvardytos visos esamos sutartys su tiekėjais. Raskite galiojančią sutartį, kurią norite naudoti.  
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Spustelėkite **Taip**.
10. Spustelėkite **Gerai**.

## <a name="add-a-line"></a>Įtraukti eilutę
1. Lauke **Prekės numeris** įveskite vertę. Jei įsipareigojimas nurodo konkrečias atsargų arba vietos dimensijas, turite įvesti tas pačias reikšmes ir pirkimo užsakymo eilutėje, kad galėtumėte naudotis sutartimi.  
2. Lauke **Vieta** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą. Svetainėje jau gali būti įvesta numatytoji reikšmė iš užsakymo arba iš tiekėjo. Tokiu atveju praleiskite šį veiksmą.  
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Lauke **Kiekis** įveskite skaičių. Patikrinkite, ar kaina nukopijuota iš įsipareigojimo.  

## <a name="look-up-the-commitment"></a>Ieškoti įsipareigojimo
1. Spustelėkite **Naujinti eilutę**.
2. Spustelėkite **Pridėta**. Čia galite gauti informaciją apie pirkimo sutartį. Pvz., galite matyti kainą ir ar kaina bei nuolaida yra fiksuotos – tai reiškia, kad pakeitus kainos ar nuolaidos reikšmę pirkimo užsakyme į kitą nei nurodyta įsipareigojime, sistema pašalins saitą, todėl pirkimo užsakymo eilutė neatitiks įsipareigojimo. Taip pat galite matyti, ar pasirinkta parinktis „Maksimaliai vykdoma“ – tai reiškia, kad negalima viršyti įsipareigojime nurodyto kiekio sudedant visus pirkimus, kurie atitinka įsipareigojimą.  
3. Uždarykite puslapį.

## <a name="look-up-the-purchase-agreement"></a>Ieškoti pirkimo sutarties
1. **Veiksmų sritis** spustelėkite **Bendra**.
2. Spustelėkite **Pirkimo sutartis**. 
3. Uždarykite puslapį.
4. Uždarykite puslapį.

