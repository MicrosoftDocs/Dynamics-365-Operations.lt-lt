---
title: Papildymo metodai ir kiekio modifikavimas
description: Šiame straipsnyje pateikiama informacija apie papildymo metodus. Joje taip pat paaiškinama, kaip keli produkto užsakymo kiekiai paveikia rezultatą.
author: t-benebo
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1e0fe6c1f49bc0f6887f1b29118c1fee7a6222f
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739763"
---
# <a name="replenishment-methods-and-quantity-modification"></a>Papildymo metodai ir kiekio modifikavimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie papildymo metodus. Joje taip pat paaiškinama, kaip keli produkto užsakymo kiekiai paveikia rezultatą.

Papildymo metodai taip pat yra žinomi kaip padengimo ir partijos nustatymo metodai.

## <a name="coverage-codes"></a>Padengimo kodai

Bendrąjį planavimą galima konfigūruoti, kad būtų naudojami skirtingi papildymo metodai. Papildymo metodai yra principai, kuriuos sistema naudoja produkto reikalavimams skaičiuoti. Papildymo metodai apibrėžiami pagal padengimo kodus, kuriuos galite nustatyti padengimo grupėje arba produkte.

Gali būti naudojami šie padengimo kodai:

- **Laikotarpis** – papildymo metodas sujungia visą laikotarpio paklausą į vieną produkto užsakymą. Užsakymas bus suplanuotas pirmai laikotarpio dienai ir jo kiekis patenkins grynuosius poreikius nustatyto laikotarpio metu. Laikotarpis pradedamas nuo pirmo produkto poreikio ir apima nustatytą laiko trukmę. Kitas laikotarpis prasidės nuo kitų produkto reikalavimų. *Laikotarpio* padengimo kodas dažnai naudojamas nenuspėjamam atsargų paėmimui, sezoniniams arba aukštos savikainos produktams. Toliau pateikiamoje iliustracijoje vaizduojamas pavyzdys.

    ![Laikotarpio padengimo kodo naudojimo pavyzdys.](./media/coverage-code-period.png "Laikotarpio padengimo kodo panaudojimo pavyzdys")

- **Reikalavimas** – papildymo metode sistema sukuria suplanuotą pirkimo, perkėlimo ar gamybos užsakymą kiekvienam produkto reikalavimui. Šis metodas naudojamas brangesniems produktams, turintiems pasikartojantį poreikį. *Reikalavimo* padengimo kodas dažnai naudojamas konfigūruojamiems produktams arba gamybos pagal užsakymą scenarijams. Toliau pateikiamoje iliustracijoje vaizduojamas pavyzdys.

    ![Reikalavimų padengimo kodo panaudojimo pavyzdys.](./media/coverage-code-requirement.png "Reikalavimų padengimo kodo panaudojimo pavyzdys")

- **Min./maks.** – Papildymo metodas yra pagrįstas atsargų lygiu. Jis apibrėžia atsargų papildymą iki konkretaus lygio, kai numatomas turimų atsargų lygis yra mažesnis nei konkreti ribinė vertė. Papildymo kiekis bus skirtumas tarp maksimalaus lygio ir prognozuojamo turimų atsargų lygio. *Min. / Maks.* padengimo kodas dažnai naudojamas numatytajam atsargų paėmimui, aukšto lygio eigoms ar mažiau brangesniems produktams. Toliau pateikiamoje iliustracijoje vaizduojamas pavyzdys.

    ![Min. / Max. padengimo kodo panaudojimo pavyzdys.](./media/coverage-code-min-max.png "Min. / Max. padengimo kodo panaudojimo pavyzdys")

- **Rankinis** – Papildymo metodas, kai sistema nenurodo produkto pirkimo, perkėlimo ar gamybos užsakymų. Vietoj to, produkto planuotojas yra atsakingas už produkto papildymui reikalingų užsakymų sukūrimą. *Rankinis* padengimo kodas dažnai naudojamas produktams, kurių sistemos sugeneruoti suplanuoti užsakymai nenori.

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a>Užsakymo kiekio iš numatytųjų užsakymo parametrų poveikis

Išleisto produkto **Numatytojo užsakymo parametrų** puslapyje galite nurodyti kiekvieną iš toliau pateiktų kiekio parametrų **Pirkimo užsakymo**, **Atsargų** ir **Pardavimo užsakymo** „FastTab” skirtukuose. („FastTab” **Atsargos** naudojamas ir perkėlimo užsakymams, ir gamybos užsakymams.)

- **Kartotinis** – suplanuoti užsakymai bus šio kiekio kartotinis.

    Pavyzdžiui, jei nustatytas **Kartotinis** laukas nustatytas į *5*, užsakymo kiekis gali būti 5, 10, 15, 20 ir taip toliau.

- **Min. užsakymo kiekis** – suplanuoti užsakymai nebus mažesni už nurodytą vertę.

    Pavyzdžiui, jei **Min. užsakymo kiekio** laukas nustatytas į *10*, bus sukurtas suplanuotas užsakymas, kurio kiekis yra 10, net jeigu poreikiui patenkinti reikalingi tik keturi.

- **Max. užsakymo kiekis** – suplanuoti užsakymai neviršys nurodytos vertės. Jei poreikis yra didesnis nei **Max. užsakymo kiekio** vertė, jo padengimui bus sukurti keli suplanuoti užsakymai.

    Pavyzdžiui, jei **Maks. užsakymo kiekio** laukas nustatytas į *100*, o poreikis yra 450, bus sukurti keturi suplanuoti užsakymai, kurių kiekis yra 100, ir vienas suplanuotas užsakymas, kurio kiekis yra 50.

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a>Papildymo pavyzdžiai, kuriame naudojamas Min. / Maks. padengimo kodas

Jei nenurodote reikšmės lauke **Kartotinis** produktui puslapyje **Numatytieji užsakymo parametrai** ir naudojate *Min. /Maks.* Papildymo metodas, bendrasis planavimas papildo atsargas iki konkretaus lygio, kai numatytas turimų atsargų lygis bus mažesnis nei konkreti ribinė vertė.

Jei nustatote kartotinį kiekį produktui, *Min. / Maks.* papildymo metodas pakeičia jo elgseną ir atsižvelgia į **Kartotinio** reikšmę.

Kitaip tariant, bendrasis planavimas vis tiek papildo atsargas iki nustatyto didžiausio lygio, kai numatytas turimų atsargų lygis bus mažesnis nei nustatytas minimalus lygis. Tačiau papildymo kiekis turi būti **Kartotinio** reikšmės kartotinis.

Jei papildymo kiekis (skirtumas tarp didžiausio lygio ir numatymo turimo lygio) nėra nustatyto sudėtiaus kiekio kartotinis, bendrojo planavimo metu naudojama pirmoji galima vertė, kuri kartu su nuspėtuoju turimo kiekio lygiu bus mažesnė už maksimalų lygį. Jei suma mažesnė nei minimalus lygis, bendrojo planavimo metu naudojama pirmoji vertė, kuri kartu su numatyta turimo, bus didesnė už maksimalų lygį.

Toliau pateikti poskyriai pateikia keletą pavyzdžių, kurie parodo, kaip keli produkto užsakymo kiekiai veikia *Min. / Maks.* papildymo metodo rezultatą.

### <a name="example-1"></a>1 pavyzdys

Produktas turi šią konfigūraciją:

- **Padengimo kodas:** *Min. / Max.*
- **Mažiausia:** *15*
- **Didžiausia:** *22*
- **Keli:** *0*

Yra 10 produkto vienetų turimose atsargose ir nėra kito poreikio arba tiekimo.

Kai vykdomas bendrasis planavimas, sukuriamas 12 vienetų suplanuotas užsakymas, kad atsargos būtų papildytos iki didžiausio kiekio.

### <a name="example-2"></a>2 pavyzdys

Produktas turi šią konfigūraciją:

- **Padengimo kodas:** *Min. / Max.*
- **Mažiausia:** *15*
- **Didžiausia:** *22*
- **Keli:** *5*

Yra 10 produkto vienetų turimose atsargose ir nėra kito poreikio arba tiekimo.

Kai vykdomas bendrasis planavimas, sukuriamas 10 vienetų suplanuotas užsakymas (kadangi 15 papildymo vienetų pridėjus 10 turimų atsargų vienetų viršys didžiausią kiekį).

### <a name="example-3"></a>3 pavyzdys

Produktas turi šią konfigūraciją:

- **Padengimo kodas:** *Min. / Max.*
- **Mažiausia:** *21*
- **Didžiausia:** *24*
- **Keli:** *5*

Yra 10 produkto vienetų turimose atsargose ir nėra kito poreikio arba tiekimo.

Kai vykdomas bendrasis planavimas, sukuriamas 15 vienetų suplanuotas užsakymas (kadangi 10 papildymo vienetų pridėjus 10 turimų atsargų vienetų bus mažesnis nei mažiausias kiekis).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
