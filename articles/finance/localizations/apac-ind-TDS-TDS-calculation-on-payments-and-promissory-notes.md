---
title: Mokėjimų ir paprastųjų vekselių TDS skaičiavimas
description: Šioje temoje pateikiama nuorodos informacija apie skirtingas mokėjimo operacijas, pagal kurias skaičiuojamas šaltinis (TDS) išskaičiuotas mokestis.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d5c9822c2e4f71fb89776d1c1c76056bad85d484
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407666"
---
# <a name="tds-calculation-on-payments-and-promissory-notes"></a>Mokėjimų ir paprastųjų vekselių TDS skaičiavimas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama nuorodos informacija apie skirtingas mokėjimo operacijas, pagal kurias skaičiuojamas šaltinis (TDS) išskaičiuotas mokestis.

| Serijos Nr. | Operacijos tipas | Operacijos suma | Puslapio pavadinimas ir pasirinkimo maršrutas | Sąskaitos tipas ir kompensavimo sąskaitos tipas |
|---------------|------------------|--------------------|--------------------|--------------------------------------|
| 1             | Išankstinis mokėjimas / mokėjimas pagal SF (mokėtina TDS) | Debetas ar Kreditas | <ul><li>Didžioji knyga (**Didžioji knyga \> Žurnalų įrašai \> Bendrieji žurnalai**)</li><li>Sąskaitos žurnalas (**Mokėtinos sąskaitos \> Sąskaitos \> SF žurnalas**)</li><li>Mokėjimų žurnalas (**Mokėtinos sumos \> Mokėjimai \> Tiekėjo mokėjimo žurnalas**)</li></ul> | Tiekėjas (Dr.), Bankas (Cr.) |
| 2             | Išankstinis mokėjimas /mokėjimas pagal SF (Pirkimas iš kliento – mokėtina TDS) | Debetas ar Kreditas | <ul><li>Didžioji knyga (**Didžioji knyga \> Žurnalų įrašai \> Bendrieji žurnalai**)</li><li>Sąskaitos žurnalas (**Mokėtinos sąskaitos \> Sąskaitos \> SF žurnalas**)</li><li>Mokėjimų žurnalas (**Mokėtinos sumos \> Mokėjimai \> Tiekėjo mokėjimo žurnalas**)</li></ul> | Klientas (Dr.), Bankas (Cr.) |
| 3             | Paprastieji vekseliai | Debetas | Parengti paprastųjų vekselių žurnalą (**Mokėtinų sumų \> Mokėjimai \> Paprastieji vekseliai \> Paprastųjų vekselių traukimas**) | Tiekėjas (Dr.), DK (Cr.). |
| 4             | Įvairios pajamos (gautinos TDS) | Debetas ar Kreditas | Didžioji knyga (**Didžioji knyga \> Žurnalų įrašai \> Bendrieji žurnalai**) | Bankas (Dr.), DK (Cr.) |
| 5             | Kitos išlaidos (mokėtinos TDS) | Debetas ar Kreditas | Didžioji knyga (**Didžioji knyga \> Žurnalų įrašai \> Bendrieji žurnalai**) | Bankas (Dr.), DK (Cr.) |

Atlikite šiuos veiksmus, kad apskaičiuotumėte mokėjimų ir paprastųjų vekselių TDS.

1. Žurnalo puslapiuose sukurkite žurnalo eilutes. Rinkitės sąskaitos tipą ir kompensavimo sąskaitos tipą.
2. Pasirinkite **Funkcijų \> Sudengimas,** kad atidarytumėte puslapį **Atidaryti operacijų redagavimą**. Tada pasirinkite konkrečią SF, kurią reikia sudengti. Jei TDS jau buvo apskaičiuota SF lygiu, lauke **Sumos kilmė** rodoma bazinė suma, pagal kurią buvo apskaičiuota TDS. **TDS suma** – laukelis rodo TDS sumą, apskaičiuotą operacijai. Lauke **Suma** rodoma grynoji mokėjimo suma (t. m. mokėjimo suma išskaičiavus TDS).

    > [!NOTE]
    > Mokėjimui, atliktam pagal sąskaitą faktūrą, taikomos šios sąlygos:
    >
    > - Jei mokėjimo suma ir SF suma yra vienodos, TDS neskaičiuojama, jei ji jau buvo apskaičiuota SF lygiu.
    > - Jei sąskaitos faktūros suma išskaičiavus TDS sumą yra didesnė už mokėjimo sumą, TDS neskaičiuojama.
    > - Jei SF suma išskaičiavus TDS sumą yra mažesnė už mokėjimo sumą, TDS skaičiuojama nuo sumos, viršijančios SF sumą.

3. Puslapyje **Žurnalo kvitas** skirtuke **Peržiūra** lauke **TDS grupė** peržiūrėkite ar keiskite numatytąją TDS grupę, kuri nustatyta klientui ar tiekėjui. Žurnalo eilutėse apskaičiuota TDS suma pagrįsta TDS mokesčių kodų, išvardytų TDS grupės lauke formule.

    > [!NOTE]
    > TDS skaičiuojamas tik jei **Skaičiuoti išskaitomą mokestį** parinktis yra nustatyta į **Taip** teikėjui **Visi tiekėjai** puslapyje.

4. Skirtuke **Mokesčių informacija** ir **Įmonės informacija** skyrius, lauke **Pavadinimas** galite rinktis įmonės pavadinimą alternatyviems adresams, kurie nustatyti įmonei.

    Skyriuje **Išskaitymo mokestis** lauke **Vertinamo pobūdis** rodomas vertinamo kliento ar tiekėjo kategoriją. Lauke **Mokesčių sąskaitos numeris (TAN)** rodomas pasirinktos įmonės mokesčių sąskaitos numeris (TAN).

5. Rinkitės **Išskaitomo mokesčio mygtukas \> Išskaitomas mokestis** norėdami atverti **laikino išskaitomo mokesčio operacijų** puslapį. Viršutinėje šio puslapio dalyje yra šie laukai:

    - **Bendroji išskaitomo mokesčio suma** – bendroji TDS grupės operacijos TDS apskaičiuota suma.
    - **Vertė** – bendrasis procentas, kuris buvo naudojamas operacijos TDS apskaičiuoti. Bendrasis procentas remiasi formule, kuri nustatyta TDS mokesčių kodams, pridėtiems prie TDS grupės.
    - **Pakoreguota išskaitomo mokesčio suma visa** – bendroji koreguota TDS suma, skirta visiems TDS grupės mokesčių kodams.
    - **TDS** – pasirinktas žymės langelis rodo, kad prie operacijos pridėta TDS grupė.

    Laukeliai **Peržiūra**, **Bendra** ir **Koreguota** skirtukuose išskaitomo mokesčių operacijų puslapyje rodo apskaičiuotos TDS sumos informaciją ir pakoreguotos TDS sumos informaciją kiekvienam TDS mokesčių kodui, pridėtame prie TDS grupės.

6. Norėdami atidaryti **ribinės vertės** puslapį, rinkitės **Ribinė vertė** puslapį, kur galite peržiūrėti TDS mokesčio komponento, pridėto prie konkretaus TDS mokesčio kodo, vertės limitą, pasirinkite Ribinę vertę.
7. Pasirinkite **formulės konstruktorių,** norėdami atverti **Formulės konstruktoriaus** puslapį, kuriame galite peržiūrėti formulę nurodytą konkrečiam TDS mokesčio kodui.
8. Užverkite **Formulės konstruktorių** ir **Laikino išskaitomo mokesčio operacijų** puslapius, kad grįžtumėte į **Žurnalo kvito** puslapį.
9. Patikrinkite ir užregistruokite žurnalą. TDS suma, apskaičiuota pardavimo SF, užregistruojama gautinų sumų sąskaitoje, kuri nustatoma kiekvienam mokėtinam TDS mokesčio kodui TDS grupėje. TDS mokesčių kodų mokėtinos sumos arba gautinos sąskaitos nustatomos puslapyje **Išskaitomo mokesčio kodai**.
10. Rinkitės **Publikuotas išskaitomas mokestis** norėdami atverti **Išskaitomo mokesčio perlaidų** puslapį. Laukelis **Vertė** – bendrasis procentas, kuris buvo naudojamas operacijos TDS apskaičiuoti.

    Skirtuko **Peržiūra**, **Bendra** ir **Suma** rodo TDS sumas, apskaičiuotas operacijai pridėtai TDS grupei.

11. Peržiūrėti TDS skaičiavimo informaciją apie kiekvieną TDS mokesčių kodą, pridėtą prie TDS grupės.

## <a name="generate-payments"></a>Generuoti mokėjimus

Norėdami sukurti mokėjimus, imkitės šių veiksmų.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Eikite į **Mokėtinos sumos \> Mokėjimai \> Tiekėjo mokėjimų žurnalas**.
    - Eikite į **Gautinos sumos \> Mokėjimai \> Klientų mokėjimo žurnalas**.
    - Eikite į **Mokėtinos sumos \> Mokėjimai \> Paprastieji vekseliai \> Paprastųjų vekselių traukimas**.
    - Eikite į **Gautinos sumos \> Mokėjimai \> Įsakomasis vekselis \> Išduotų įsakomųjų vekselių žurnalas**.
    - Eikite į **Gautinos sumos \> Mokėjimai \> Įsakomasis vekselis \> Iš naujo išduotų įsakomųjų vekselių žurnalas**.

2. Pasirinkite **Eilutės**.
3. Pasirinkite **Funkcijos \> Generuoti mokėjimus**.
