---
title: Skaičiuoti SF TDS naudojant žurnalus
description: Šioje temoje pateikiami žurnalų iš šaltinio (TDS) išskaityamų mokesčių skaičiavimo veiksmai.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: bc1a8570e60e2b17f27c3e63c5ff847b3cb7a2dd
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358463"
---
# <a name="calculate-tds-on-invoices-using-journals"></a>Skaičiuoti SF TDS naudojant žurnalus

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiami žurnalų iš šaltinio (TDS) išskaityamų mokesčių skaičiavimo veiksmai.

Pradėkite veiksmą atidarydami **Bendrųjų žurnalų** puslapį (**Didžioji knyga > Žurnalo įrašai > Bendrieji žurnalai**).

[![Pagrindiniai žurnalai.](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)

1. Kurti žurnalo eilutes, naudojant lentelėje pateiktas žurnalo formas. Pasirinkite sąskaitos tipą bei korespondentinės sąskaitos tipą ir įveskite operacijos sumą. 

   > [!NOTE]
   > SF **patvirtinimo žurnalo puslapyje** pasirinkite **Rasti kvitus** ir pasirinkite sąskaitas faktūras, kurioms norite apskaičiuoti TDS. Peržiūrėti SF registro puslapyje **sukurtas SF** arba **Rasti kvitų** puslapį.  

2. Skirtuke **Bendri** puslapyje **Žurnalo kvitas** peržiūrėkite ir keiskite numatytąją TDS grupę, nustatytą tiekėjui ar klientui **TDS grupės** laukelyje. Žurnalo eilutėse apskaičiuota TDS suma pagrįsta TDS mokesčių kodų, išvardytų **TDS grupės** lauke formule. 

   > [!NOTE]
   > Laukelis **Išskaitimo mokesčio grupė**  ir **TCS grupės** laukelis tampa neprieinamas jums pasirinkus TDS grupę **TDS grupės** laukelyje. Laukelis **Išskaitomo mokesčio grupė** galimas tik **bendrojo žurnalo** puslapyje. TDS skaičiuojamas tik jei **Skaičiuoti išskaitomą mokestį** žymimas laukelis yra pažymėtas tiekėjui ar klientui **Visi tiekėjai** ar **Visi klientai** puslapiuose.   

3. Pasirinkite **mokesčių informacijo** skirtuką. Jei reikia, pasirinkite alternatyvius įmonės, nustatytos įmonės adresus šiame lauke. Įmonės pavadinimą galite peržiūrėti lauke **Pavadinimas**, kuris yra **įmonės informacijos** laukų grupėje. 

4. Peržiūrėkite tiekėjo arba kliento vertinimo kategorijos pobūdį lauke Gavėjo tikslas, kuris priklauso **išskaitomo mokesčio** laukų **grupei**. Laukelyje **Mokesčio sąskaitos numeris** (**TAN**) peržiūrėkite pasirinktos įmonės pavadinimo TAN, kuris rodomas.  

5. Rinkitės **Išskaitomo mokesčio meniu** esantį **Išskaitomo mokesčio** meniu, kad atidarytumėte **laikino išskaitomo mokesčio operacijų** puslapį. Šie laukai rodomi viršutinėje laikino išskaitomo **mokesčio operacijų puslapio** srityje.

   - **Bendroji išskaitomo mokesčio suma** – bendroji TDS grupės operacijos TDS suma.

   - **Vertė** – bendrasis procentas, naudojamas operacijos TDS apskaičiuoti. Bendrasis procentas remiasi formule, kuri nustatyta TDS mokesčių kodams, pridėtiems prie TDS grupės.

   - **Pakoreguota išskaitomo mokesčio suma visa** – bendroji koreguota TDS suma, skirta visiems TDS grupės mokesčių kodams.

   - **TDS** – jei pasirinkta, prie operacijos pridedama TDS grupė.

  Laukeliai **Peržiūra**, **Bendra**, ir **Koregavimas** laikinų išskaitomo **mokesčių operacijų puslapyje** rodo apskaičiuotą TDS sumą ir pakoreguotos TDS sumos informaciją kiekvienam TDS mokesčių kodui, pridėtame prie TDS grupės.

6. Pasirinkite **Ribinės vertės** lauką, kad atidarytumėte **slenkstį**. Peržiūrėkite šiame puslapyje nurodytą TDS mokesčio komponento, pridėto prie konkretaus TDS mokesčio kodo, ribinės vertės ir išimties ribą.

   Norėdami **atidaryti formulės** konstruktoriaus **formą, pasirinkite** Formulės konstruktorius. Peržiūrėkite šiame puslapyje nurodytą konkretaus TDS mokesčio kodo formulę. Užverkite **Formulės konstruktorių** ir **Laikino išskaitomo mokesčio operacijų** puslapius, kad grįžtumėte į **Žurnalo kvito** puslapį.

8. Įveskite kitą reikiamą informaciją. Patikrinkite ir užregistruokite žurnalą. TDS suma, apskaičiuota pirkimo SF, užregistruojama mokėtinoje sąskaitoje. TDS suma, apskaičiuota pardavimo SF, užregistruojama gautinų sumų sąskaitoje, kuri nustatoma kiekvienam TDS mokesčio kodui TDS grupėje. TDS mokesčių kodų mokėtinos sumos arba gautinos sąskaitos nustatomos puslapyje **Išskaitomo mokesčio kodai**.

9. Rinkitės **Publikuotas išskaitomas mokestis** norėdami atverti **Išskaitomo** **mokesčio** **perlaidų** puslapį. Laukelyje **Vertė** – bendrasis procentas, naudojamas rodomos operacijos TDS apskaičiuoti.

   Laukeliai **Peržiūra**, **Bendra** ir **Suma** skirtukuose išskaitomo mokesčių operacijų puslapyje rodo apskaičiuotą TDS sumą ir pakoreguotos TDS sumos informaciją kiekvienam TDS mokesčių kodui, pridėtame prie TDS grupės.
