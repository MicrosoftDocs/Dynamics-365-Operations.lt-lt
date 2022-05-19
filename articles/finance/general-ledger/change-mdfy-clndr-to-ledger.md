---
title: Didžiosios knygos kalendoriaus keitimas arba priskyrimas iš naujo
description: Šioje temoje aiškinama, kaip pakeisti kalendorių, kuris šiuo metu priskirtas didžiajai knygai, ir kaip didžiajai knygai priskirti naują kalendorių.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25777a5b807921acc13338116627e9356fe62a20
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711637"
---
# <a name="change-or-reassign-a-ledger-calendar"></a>Didžiosios knygos kalendoriaus keitimas arba priskyrimas iš naujo

[!include [banner](../includes/banner.md)]

Šioje temoje aiškinama, kaip pakeisti kalendorių, kuris šiuo metu priskirtas didžiajai knygai, ir kaip didžiajai knygai priskirti naują kalendorių.

## <a name="issue"></a>Problema

Kartais įmonės turi pakeisti esamą kalendorių, priskirtą didžiajai knygai, arba priskirti naują kalendorių.

## <a name="resolution"></a>Sprendimas

Yra du didžiosios knygos kalendoriaus keitimo arba priskyrimo iš naujo scenarijai. Pirmasis scenarijus apima esamo kalendoriaus, kuris jau priskirtas didžiajai knygai, keitimą. Antrasis scenarijus apima naujo kalendoriaus kūrimą ir priskyrimą didžiajai knygai. Abu keitimus galima atlikti bet kuriuo metu, net ir didžiojoje knygoje užregistravus operacijas.

### <a name="change-an-existing-fiscal-calendar"></a>Esamo finansinio kalendoriaus keitimas

Norėdami pakeisti esamą kalendorių, priskirtą jūsų didžiajai knygai, eikite į **Didžioji knyga \> Didžiosios knygos nustatymas \> Didžioji knyga** ir pasirinkite finansinio kalendoriaus saitą, kad atidarytumėte puslapį **Didžiosios knygos kalendoriai**.

Yra keitimų, kuriuos galima atlikti kalendoriuje, apribojimų. Pavyzdžiui, galite pakeisti metų *laikotarpių* pradžios ir pabaigos datas, tačiau negalite pakeisti *metų* pradžios i pabaigos datų kalendoriuje.

Norėdami pakeisti metų laikotarpius, pasirinkite atitinkamą kalendorių ir metus. Pirmiausia mygtuku **Naikinti laikotarpį** panaikinkite kai kuriuos arba visus esamus veiklos laikotarpius. Visus veiklos laikotarpius, išskyrus pirmąjį, galima panaikinti. Tada mygtuku **Padalyti laikotarpį** padalykite likusį laikotarpį arba laikotarpius į naujus laikotarpius įvesdami atitinkamą kito laikotarpio pradžios datą.

Pakeitę laikotarpius kalendoriuje, turite paleisti procesą **Perskaičiuoti didžiosios knygos laikotarpius** kiekviename juridiniame subjekte (įmonėje), kuriam priskirtas kalendorius. Nors jokiu įspėjamuoju pranešimu neprimenama atlikti šio veiksmo, perskaičiavimo procesas reikalingas norint atnaujinti laikotarpį, priskirtą kiekvienai didžiojoje knygoje užregistruotai operacijai. Norėdami paleisti perskaičiavimo procesą, kiekvienos įmonės puslapyje **Didžiosios knygos nustatymas** pasirinkite **Perskaičiuoti didžiosios knygos laikotarpius**.

Jei perskaičiavimo procesas nėra paleistas, bandomojo balanso arba finansinių ataskaitų operacijų balansai gali būti neteisingai įtraukti į laikotarpius. Tokiu atveju galite bet kada ištaisyti balansus paleisdami perskaičiavimo procesą.

### <a name="assign-a-new-fiscal-calendar"></a>Naujo finansinio kalendoriaus priskyrimas

Norėdami priskirti naują finansinį kalendorių, eikite į **Didžioji knyga \> Didžiosios knygos nustatymas \> Didžioji knyga** ir pasirinkite **Redaguoti**, kad įjungtumėte puslapio **Didžioji knyga** redagavimo režimą. Tada lauke **Finansinis kalendorius** pasirinkite naują finansinį kalendorių.

Pakeitę didžiosios knygos finansinį kalendorių, turite paleisti procesą **Perskaičiuoti didžiosios knygos laikotarpius**. Kai didžiajai knygai priskiriate naują finansinį kalendorių, pranešimu primenama atlikti šį veiksmą. Nors iš pranešimo galima sudaryti įspūdį, kad perskaičiavimo procesas yra pasirinktinis, tačiau taip nėra. Jis būtinas norint atnaujinti laikotarpį, priskirtą kiekvienai užregistruotai operacijai didžiojoje knygoje. Norėdami paleisti perskaičiavimo procesą, puslapyje **Didžiosios knygos nustatymas** pasirinkite **Perskaičiuoti didžiosios knygos laikotarpius**.

Jei perskaičiavimo procesas nėra paleistas, bandomojo balanso arba finansinių ataskaitų operacijų balansai gali būti neteisingai įtraukti į laikotarpius. Tokiu atveju galite bet kada ištaisyti balansus paleisdami perskaičiavimo procesą.
