---
title: Pridėti TDS mokesčių kodus prie TDS mokesčių grupių ir nustatyti TDS apskaičiavimo formulę
description: Šioje temoje paaiškinama, kaip nustatyti iš šaltinio (TDS) mokesčių grupes atskaičius mokesčius ir TDS mokesčių kodus pridėti prie TDS mokesčių grupių. Norėdami skaičiuoti TDS mokesčių grupės TDS, turite nurodyti prie jos pridėtų TDS mokesčių kodų formulę.
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
ms.openlocfilehash: ce4c2dcfb6ac6f95af3bc354412c36956ae63242
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407490"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a>Pridėti TDS mokesčių kodus prie TDS mokesčių grupių ir nustatyti TDS apskaičiavimo formulę

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti iš šaltinio (TDS) mokesčių grupes atskaičius mokesčius ir TDS mokesčių kodus pridėti prie TDS mokesčių grupių. Norėdami skaičiuoti TDS mokesčių grupės TDS, turite nurodyti prie jos pridėtų TDS mokesčių kodų formulę.

Norėdami nustatyti TDS mokesčių grupę, pridėti TDS mokesčių kodus ir nustatyti TDS skaičiavimo formulę, atlikite šiuos veiksmus.

1. Pasirinkite **Mokestis \> Netiesioginiai mokesčiai \> Išskaitomas mokestis \> Išskaitomo mokesčio grupės**.

    [![Išskaitomo mokesčio grupių puslapis.](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)

2. Norėdami sukurti **TDS** išskaitomo mokesčio grupę, veiksmų srityje pasirinkite Naujas ir įveskite reikiamą informaciją.
3. Lauke **Mokesčio tipas** pasirinkite **TDS**.
4. Norėdami sukurti eilutę, „FastTab” **Nustatymai** pasirinkite **Įtraukti**.
5. Lauke **Išskaitomo mokesčio kodas** pasirinkite TDS mokesčio kodą TDS mokesčių grupei. Laukelyje **Išskaitomo mokesčio pavadinimas** lauke rodomas TDS mokesčio kodo pavadinimas, o lauke **Vertė** rodoma vertė.
6. Norėdami nepaisyti ribinės ribos ir išimties ribinės vertės, nustatytos TDS mokesčio komponentui, kuris pridėtas prie TDS mokesčio kodo TDS operacijose, pažymėkite žymės langelį **Peržiūros** slenkstis.
7. Norėdami apsaugoti mokesčių grupę nuo skaičiavimo perlaidose, pasirinkite **Netaikoma** žymimą laukelį.
8. Veiksmų srityje pasirinkite **Konstruktorius** kad atidarytumėte formulės konstruktorių, kad būtų galima nustatyti TDS mokesčių grupės TDS skaičiavimo formulę. Puslapyje **Konstruktorius** puslapyje, skirtuke Mokesčiai rodomi TDS mokesčių kodai, **pasirinkti** TDS mokesčių grupei.

    [![Konstruktoriaus puslapis.](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)

9. Norėdami **sukurti** eilutę, skirtuke Skaičiavimas pasirinkite **Alt+N**. ID **laukas** rodo automatiškai sugeneruotą TDS skaičiavimo prioriteto ID.
10. Lauke **Mokesčio kodas** pasirinkite TDS mokesčio kodą norėdami nustatyti formulę. Visus TDS mokesčių kodus, pasirinktus TDS mokesčių grupei, galima pasirinkti šiame lauke.
11. **Apmokestinamo pagrindo** lauke pasirinkite TDS skaičiavimo pagrindą:

    - **Bendra suma** – skaičiuoti TDS pagal bendrą operacijos sumą (t. y. SF sumą) naudojant mokesčio kodui nustatytą skaičiavimo išraišką.
    - **Neįskaitant bendros sumos**– skaičiuoti TDS remiantis skaičiavimo išraiška, nustatyta mokesčio kodui.

    > [!NOTE]
    > Laukelis **Apmokestinamas pagrindas** negali būti nustatytas į **Excl bendra suma** TDS mokesčio kodui, kurio ID prioritetas yra **1**.

12. TDS skaičiavimas remiasi formule, kuri nurodyta kiekvieno prie TDS mokesčių grupės **pridėto mokesčio** kodo skaičiavimo išraiškos lauke. Rinkitės pliuso ženklą (+), minuso ženklą (–), daugybos ženklą (\*), ar dalybos ženklo (/) mygtuką norėdami įvesti skaičiuoklės išraišką pasirinktam TDS mokesčio kodui **Skaičiavimo išraiškos** lauke.

    > [!NOTE]
    > Negalima nustatyti TDS mokesčio kodo, kurio prioriteto ID **1** skaičiavimo išraiškos.

13. Norėdami nustatyti TDS mokesčio kodo skaičiavimo išraišką lauke Skaičiavimo išraiška, pridėkite TDS **mokesčių kodus,** kurie galimi skirtuke **Mokesčiai**. Norėdami įtraukti TDS mokesčių kodus į **skaičiavimo išraiškos** lauką, galite naudoti bet kurį iš šių metodų:

    - Nuvilkite reikiamą mokesčio kodą iš skirtuko **Mokesčiai** į lauką **Skaičiavimo išraiška**.
    - Dukart pažymėkite (arba du kartus spustelėkite) reikiamą mokesčio kodą skirtuke **Mokesčiai**.
    - Paspauskite ir laikykite (ar dešiniu klavišu) spauskite reikiamą mokesčio kodą **Mokesčiai** skirtuke ir tada rinkitės **Įtraukti mokesčio kodą**.

    > [!NOTE]
    > Įterpti skaičiavimo išraišką prieš kiekvieną TDS mokesčio kodą. TDS mokesčių kodai, įtraukti į skaičiavimo išraišką, rodomi skliausteliuose (\[... \]).

14. Norėdami išvalyti skaičiavimo išraišką, nurodytą mokesčio kodui lauke **Skaičiavimo išraiška**, pasirinkite mygtuką **C**.
15. Norėdami panaikinti įrašą skirtuke **Skaičiavimas**, pasirinkite **Naikinti**.
16. Uždarykite puslapį.
