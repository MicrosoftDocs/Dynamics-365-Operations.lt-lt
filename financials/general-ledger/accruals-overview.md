---
title: "Kaupimų apžvalga"
description: "Šiame straipsnyje aprašyti kaupimai ir pateikta informacija apie tai, kaip juos nustatyti ir sukurti operacijas."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 328a4a7bef32ee8634e4a9f4854ebe78fcc99f6d
ms.lasthandoff: 03/31/2017


---

# <a name="accruals-overview"></a>Kaupimų apžvalga

Šiame straipsnyje aprašyti kaupimai ir pateikta informacija apie tai, kaip juos nustatyti ir sukurti operacijas.

Kaupimai naudojami taikant kaupimo apskaitos principą, kuriuo sekamos įplaukos, priskiriamos tam pačiam laikotarpiui, kada jos uždirbtos, o ne kada gautas apmokėjimas, ir sekamos išlaidos (sąnaudos), priskiriamos tuomet, kai jos įvyksta, o ne kada atliekamas apmokėjimas.

## <a name="accrual-schemes"></a>Kaupimo schemos
Kaupimo schemos naudojamos nustatant atidėtas įplaukas ir išlaidas – ta pati kaupimo schema gali būti naudojama ir įplaukoms, ir išlaidoms. DK kaupimai paskirsto žurnalo eilutės išlaidas ar įplaukas, kad išlaidos ir įplaukos būtų priskiriamos atitinkamuose laikotarpiuose. Puslapyje **Kaupimo schema** galite nurodyti debeto ir kredito sąskaitas, kurios bus naudojamos pritaikius kaupimo schemą.

-   **Debetas** – jūsų nurodyta sąskaita pakeis debeto pagrindinę sąskaitą žurnalo kvito eilutėje. Ši sąskaita bus taip pat naudojama atšaukiant atidėjimą pagal DK kaupimo operacijas.
-   **Kreditas** – jūsų nurodyta pagrindinė sąskaita pakeis kredito pagrindinę sąskaitą žurnalo kvito eilutėje. Ši sąskaita bus taip pat naudojama atšaukiant atidėjimą pagal DK kaupimo operacijas.

Nusprendę, kurias sąskaitas naudoti, galite nurodyti, kaip kuriamas kvito numeris, kai kuriamos kaupimo operacijos. Taip pat galite nurodyti, kaip dažnai vyksta operacijos, kiek kartų operacijos sukuriamos ir kada operacijos registurojamos. Sukūrę kaupimo schemą, galite ją naudoti kai kuriuose žurnaluose, pasitelkdami DK kaupimų funkciją.

## <a name="ledger-accruals"></a>DK kaupimai
Įvedę žurnalą, galite spustelėti **DK kaupimai** meniu **Funkcijos**. Tada, kai pasirenkate kaupimo schemą, matysite pagrindinę žurnalo sumą, kuri bus paskirstyta per laikotarpį pagal kaupimo schemą. Pavyzdžiui, jei mokate darbuotojo draudimo metus sausio mėnesį, ir suma yra 12 000, jus pripažinti, kad sąskaita kiekvieną mėnesį. Galite pasirinkti pradžios datą. Taip pat galite nurodyti, ar suma sukaupta pagal sąskaita arba korespondentinę sąskaitą. Atlikę savo pasirinkimais, spustelėkite **operacijos** Norėdami peržiūrėti visas operacijas, kurios buvo sukurtos remiantis kaupimo schemą. Pavyzdžiui, jei per metus paskirstytais 12.000 draudimo išlaidas, pamatysite 1000 kiekvieną mėnesį. Po to, kai užregistruosite žurnalą, galite peržiūrėti operacijos naudojant į **kvitų operacijos** puslapio užklausą. Jei kaupimo schemą negali būti taikomi (pvz., kai pardavimo užsakymo SF arba pirkimo užsakymo SF yra susijęs), galite iš anksto apmokėta suma kredituoja ir išlaidų suma. Tada, taikydami kaupimo schemą, galite pasirinkti **Korespondentinė sąskaita**.


