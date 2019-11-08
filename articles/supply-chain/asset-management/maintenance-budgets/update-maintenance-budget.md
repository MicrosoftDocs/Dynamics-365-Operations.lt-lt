---
title: Priežiūros biudžeto atnaujinimas
description: Šioje temoje aiškinama, kaip atnaujinti priežiūros biudžetą modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f3b771319eeb602a371500fdc69c68f88afe341
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571742"
---
# <a name="update-maintenance-budgets"></a>Priežiūros biudžeto atnaujinimas

[!include [banner](../../includes/banner.md)]

 

Puslapyje **Priežiūros biudžeto eilutės** rodomos visos biudžeto eilutės, kurios buvo sukurtos puslapyje **Priežiūros biudžetas** pasirinktame biudžete. (Norėdami gauti daugiau informacijos žr. [Priežiūros biudžetų kūrimas](create-maintenance-budget.md).) Priežiūros biudžeto eilutes galite perskaičiuoti ir koreguoti tol, kol priežiūros biudžetas bus patvirtintas. Praėjus biudžeto laikotarpiui ir paskelbus išlaidas modulyje Turto valdymas biudžeto eilutes taip pat galite atnaujinti pagal faktines išlaidas.

## <a name="recalculate-a-maintenance-budget"></a>Priežiūros biudžeto perskaičiavimas

Priežiūros biudžetą galite perskaičiuoti puslapyje **Priežiūros biudžeto eilutės**. Perskaičiuojant priežiūros biudžetą esamos biudžeto eilutės ištrinamos ir atliekami nauji skaičiavimai.

1. Puslapyje **Priežiūros biudžeto eilutės** pasirinkite **Perskaičiuoti**.
2. Dialogo lange **Perskaičiuoti biudžetą** atlikite reikiamus pakeitimus naujam skaičiavimui, tada pasirinkite **Gerai**.

Atsižvelgiant į nustatytas reikšmes sukuriamos naujos biudžeto eilutės.

## <a name="adjust-budget-lines"></a>Biudžeto eilučių koregavimas

Vietoj viso priežiūros biudžeto perskaičiavimo galite koreguoti pasirinktas eilutes, susijusias su biudžeto išlaidomis.

1. Puslapyje **Priežiūros biudžeto eilutės** pasirinkite eilutes, dėl kurių norite atnaujinti biudžeto išlaidas.
2. Pasirinkite **Koreguoti**.
3. Norėdami į pasirinktas eilutes įtraukti sumą, pažymėkite žymės langelį **Įtraukti išlaidas**, o tada lauke **Įtraukti reikšmę** įveskite reikšmę.
4. Norėdami biudžeto išlaidas pasirinktose biudžeto eilutėse padauginti iš koeficiento, pažymėkite žymės langelį **Dauginti išlaidas**, o lauke **Dauginimo reikšmė** įveskite koeficientą.

    Pavyzdžiui, jei lauke **Dauginimo reikšmė** įvesite **1,2**, biudžeto išlaidos pasirinktose eilutėse padidės 20 procentų. Jei įvesite **0,7**, biudžeto išlaidos pasirinktose eilutėse sumažės 30 procentų.

5. Pasirinkite **Gerai**.

Pasirinktos biudžeto eilutės atnaujinamos pagal reikšmes, kurias nustatėte atlikdami 3 arba 4 veiksmą.

## <a name="update-actual-costs"></a>Faktinių išlaidų atnaujinimas

Praėjus biudžeto eilučių datoms ir paskelbus faktines išlaidas modulyje Turto valdymas galite atnaujinti priežiūros biudžeto faktines išlaidas.

1. Puslapyje **Priežiūros biudžeto eilutės** pasirinkite **Atnaujinti išlaidas**.
2. Dialogo lange **Apskaičiuoti faktines išlaidas** pažymėkite **Gerai**.

Biudžeto eilučių laukai **Faktinės išlaidos** atnaujinami, jei buvo paskelbtos faktinės išlaidos. Jei nuo tada, kai sukūrėte biudžetą, buvo sukurta naujų turto tipų, ir jei šie turto tipai buvo naudojami turtui, kuriam buvo sukurta darbo užsakymų ir paskelbtos susijusios išlaidos, gali būti sugeneruota naujų biudžeto eilučių. Naujose biudžeto eilutėse rodomos tik faktinės išlaidos, nes šiose eilutėse nebuvo apskaičiuotos biudžeto išlaidos.

> [!NOTE]
> Norėdami peržiūrėti faktinių išlaidų, padalytų į prevencines, korekcines ir investavimo išlaidas, apžvalgą, puslapyje **Turto išlaidų valdymas** galite atlikti skaičiavimą pagal tą patį laikotarpį. 

## <a name="manually-add-budget-lines"></a>Biudžeto eilučių įtraukimas rankiniu būdu

Puslapyje **Priežiūros biudžeto eilutės** galite rankiniu būdu įtraukti naują priežiūros eilutę pasirinkdami **Nauja**, o tada pasirinkdami atitinkamas parinktis eilutėje. Toliau pateikiame kelis situacijų, kuriose toks metodas gali būti naudingas, pavyzdžius.

- Žinote, kad planuojamas kai kurio turto atnaujinimas, tačiau modulyje Turto valdymas dar nėra sukurta susijusių užduočių. Tačiau norite, kad šių užduočių biudžeto išlaidos būtų įtrauktos į priežiūros biudžetą.
- Nuo tada, kai sudarėte priežiūros biudžetą, buvo sukurta naujo turto ar turto tipų, tačiau dar nėra nustatyta šio turto ar turto tipų priežiūros planų. Tačiau norite, kad šių turto tipų išlaidos būtų įtrauktos į priežiūros biudžetą.
