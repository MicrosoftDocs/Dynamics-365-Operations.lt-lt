---
title: Kaupimų apžvalga
description: Šiame straipsnyje aprašyti kaupimai ir pateikta informacija apie tai, kaip juos nustatyti ir sukurti operacijas.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b97055f7eac12e3e82d028a0097ca926e5c355a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839646"
---
# <a name="accruals-overview"></a>Kaupimų apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašyti kaupimai ir pateikta informacija apie tai, kaip juos nustatyti ir sukurti operacijas.

Kaupimai naudojami taikant kaupimo apskaitos principą, kuriuo sekamos įplaukos, priskiriamos tam pačiam laikotarpiui, kada jos uždirbtos, o ne kada gautas apmokėjimas, ir sekamos išlaidos (sąnaudos), priskiriamos tuomet, kai jos įvyksta, o ne kada atliekamas apmokėjimas.

## <a name="accrual-schemes"></a>Kaupimo schemos
Kaupimo schemos naudojamos nustatant atidėtas įplaukas ir išlaidas – ta pati kaupimo schema gali būti naudojama ir įplaukoms, ir išlaidoms. DK kaupimai paskirsto žurnalo eilutės išlaidas ar įplaukas, kad išlaidos ir įplaukos būtų priskiriamos atitinkamuose laikotarpiuose. Puslapyje **Kaupimo schema** galite nurodyti debeto ir kredito sąskaitas, kurios bus naudojamos pritaikius kaupimo schemą.

-   **Debetas** – jūsų nurodyta sąskaita pakeis debeto pagrindinę sąskaitą žurnalo kvito eilutėje. Ši sąskaita bus taip pat naudojama atšaukiant atidėjimą pagal DK kaupimo operacijas.
-   **Kreditas** – jūsų nurodyta pagrindinė sąskaita pakeis kredito pagrindinę sąskaitą žurnalo kvito eilutėje. Ši sąskaita bus taip pat naudojama atšaukiant atidėjimą pagal DK kaupimo operacijas.

Nusprendę, kurias sąskaitas naudoti, galite nurodyti, kaip kuriamas kvito numeris, kai kuriamos kaupimo operacijos. Taip pat galite nurodyti, kaip dažnai vyksta operacijos, kiek kartų operacijos sukuriamos ir kada operacijos registurojamos. Sukūrę kaupimo schemą, galite ją naudoti kai kuriuose žurnaluose, pasitelkdami DK kaupimų funkciją.

## <a name="ledger-accruals"></a>DK kaupimai
Įvedę žurnalą, galite spustelėti **DK kaupimai** meniu **Funkcijos**. Tada, kai pasirenkate kaupimo schemą, matysite pagrindinę žurnalo sumą, kuri bus paskirstyta per laikotarpį pagal kaupimo schemą. Pavyzdžiui, jei sausį mokate darbuotojo draudimą už visus metus, ir ši suma yra 12 000, šias išlaidas turite priskirti kiekvieną mėnesį. Galite pasirinkti pradžios datą. Taip pat galite nurodyti, ar suma sukaupta pagal sąskaita arba korespondentinę sąskaitą. Atlikę savo pasirinkimus, spustelėkite **Operacijos**, kad peržiūrėtumėte visas operacijas, sukurtas pagal kaupimo schemą. Pavyzdžiui, jei 12 000 draudimo išlaidų paskirstysite per metus, kiekvieną mėnesį matysite 1 000. Užregistravę žurnalą, galite peržiūrėti operacijas naudodami užklausų puslapį **Kvito operacijos**. Jei kaupimo schemos pritaikyti negalima (pvz., kai yra pardavimo užsakymo SF arba pirkimo užsakymo SF), galite kredituoti iš anksto sumokėtą sumą ir debetuoti išlaidų sumą. Tada, taikydami kaupimo schemą, galite pasirinkti **Korespondentinė sąskaita**.


Daugiau informacijos žr. [Kurti kaupimo schemas](tasks/create-accrual-schemes.md) ir [Kurti DK kaupimo operacijas](tasks/create-ledger-accrual-transactions.md).
