---
title: Ribotas pajėgumo planavimas ir planavimas
description: Ribotas pajėgumo planavimas ir planavimas padeda suprasti, kiek darbo galima atlikti tam tikrą laikotarpį, kai atsižvelgiama į skirtingų išteklių apribojimus.
author: t-benebo
ms.date: 09/19/2022
ms.topic: article
ms.search.form: ReqParameters, ReqPlanSched, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-19
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c5eebe9ef6258b43daa7c7007ee28b0278fe5b09
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573151"
---
# <a name="finite-capacity-planning-and-scheduling"></a>Ribotas pajėgumo planavimas ir planavimas

[!include [banner](../../includes/banner.md)]

Ribotas pajėgumas yra būdas, padedantis suprasti, kiek darbo galima pagaminti per tam tikrą laikotarpį, kai atsižvelgiama į skirtingų išteklių apribojimus. Riboto pajėgumo planavimo paskirtis yra užtikrinti, kad darbas tęstų darbą tolygiai ir efektyviai visoje gamykloje.

Ribotas pajėgumo planavimas ir planavimas sukuria realesnį gamybos procesų grafiką, nei sukuriamas neriboto įkėlimo būdas. Jei nėra pakankamai pajėgumų ištekliams, pristatymo data bus išstumta, o užduotis bus suplanuota, kai bus pakankamai pajėgumų.

## <a name="planning-optimization-support-for-finite-capacity-planning"></a>Riboto pajėgumo planavimo optimizavimo palaikymas

Ribotas pajėgumo planavimas ir planavimas veikia beveik taip pat, nepaisant to, ar naudojate planavimo optimizavimą, ar įtaisytą planavimo sistemą. Tačiau planavimo optimizavimas naudoja silpnios vietos **laiko ribos** parametrą. Naudojant planavimo optimizavimą, ribotosios gebos ištekliai visada planuojami naudojant tą pačią laiko ribą kaip ir ribotosios gebos ištekliai (kaip nurodyta riboto pajėgumo laiko ribose).

## <a name="set-up-finite-capacity-functionality"></a>Nustatyti riboto pajėgumo funkciją

Norėdami naudoti riboto pajėgumo funkciją, turite įgalinti pajėgumo planavimą visuotinai ir taip pat turite įgalinti riboto pajėgumo planavimą tiek pagrindiniame plane, kuriame norite jį naudoti, tiek visiems ištekliams, kuriuose jis taikomas. Planuojant planus ir išteklius, kuriuose įgalintas ribotas pajėgumas, planuojant suplanuotus gamybos užsakymus bus apsvarstyti jau rezervuotą pajėgumą. Suplanuoti gamybos užsakymai yra planuojami atgal nuo poreikio datos. Jei pajėgumas neatitinka optimalaus grafiko, sistema bandys reikalauti sudedamųjų prekių ankstesne data. Jei jūsų pajėgumas gali pasikeisti keisdami poreikius (pavyzdžiui, kai dirbate su pamainomis), turėtumėte nenaudoti riboto pajėgumo funkcijos, nes apskaičiuotas apdorojimo laikas bus neteisingas. Planuojant atsižvelgiama tik į jau rezervuotą išteklių pajėgumą, kai įgalintas ribotas pajėgumas. Įgalindami riboto pajėgumą ištekliams, įgalinsite riboto pajėgumo laiko ribą.

### <a name="activate-master-planning-parameters"></a>Suaktyvinti bendrojo planavimo parametrus

Norėdami naudoti riboto pajėgumo funkciją, turite įgalinti pajėgumo planavimą bendrojo planavimo **parametrų** puslapyje.

1. Eikite į **Bendrasis planavimas \> Sąranka \> Bendrojo planavimo parametrai**.
1. Skirtuko Suplanuoti **užsakymai** dalyje Pajėgumo **planavimas** nustatykite pasirinktį **Gamyba** kaip *Taip*.

### <a name="activate-a-master-plan"></a>Bendrojo plano aktyvinimas

Turite įgalinti kiekvieno bendrojo plano, kuriame norite jį naudoti, riboto pajėgumo planavimą ir planavimą.

1. Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.
1. Sąrašo srityje pasirinkite bendrąjį planą, kurį norite nustatyti norėdami naudoti riboto pajėgumo planavimą ir planavimą.
1. Skyriaus **Suplanuoti** gamybos užsakymai **bendro "** FastTab" dalyje Ribotas pajėgumas **nustatykite pasirinktį** Taip *·*.
1. Su kiekvienu papildomu pagrindiniu planu, kurį norite nustatyti, pakartokite 2 ir 3 veiksmus.

### <a name="activate-resources"></a>Aktyvinti išteklius

Turite įgalinti kiekvieno ištekliaus, kuriame norite juos naudoti, riboto pajėgumo planavimą ir planavimą.

1. Eikite į **Gamybos kontrolė \> Sąranka \> Ištekliai \> Ištekliai**.
1. Sąrašo srityje pasirinkite išteklius, kuriuos norite nustatyti norėdami naudoti riboto pajėgumo planavimą ir planavimą.
1. Operacijos "**FastTab**" mygtuko Pajėgumas **skyriuje** nustatykite parinktį **Ribotas pajėgumas** kaip *Taip*.
1. Su kiekvienu papildomais ištekliais, kuriuos norite nustatyti, pakartokite 2 ir 3 veiksmus.

## <a name="examples"></a>Pavyzdžiai

Šiame skyriuje pateikiami pavyzdžiai, kurie parodo, kaip dirbti naudojant neribotą ir riboto pajėgumo planavimą bei planavimą:

- 1 pavyzdys – neriboto pajėgumo planavimas
- 2 pavyzdys – ribotas pajėgumo planavimas, naudojant vienos dienos laiko ribą
- 3 pavyzdys – ribotas pajėgumo planavimas, naudojant dviejų dienų laiko ribą

### <a name="preconditions"></a>Išankstinės sąlygos

Visuose trijuose pavyzdžiuose tarkime šiame skyriuje aprašytos išankstinės sąlygos.

*1 produkto* maršrutas, kuriame yra šios operacijos.

| Operacijos Nr. | Operacijos pavadinimas | Ištekliai        | Apdorojimo laikas | Apdorojamas kiekis | Tolesnis |
|---------------|----------------|-----------------|----------|--------------|------|
| 10            | Suvirinimo        | Uždavimo eilutė    | 1        | 2            | 20   |
| 20            | Surinkimas     | Surinkimo linija | 1        | 4            |      |

Jūsų įmonės darbuotojai dirba viena pamaina aštuonioms valandoms (8:00–16:00).

Yra suplanuotas *24 produkto (1)* gamybos *užsakymas*. Jos pristatymo data yra šiandien *+ 3 dienos*.

Planuojant sistema įkelia išteklius tokiu būdu:

- **Taškinė eilutė:** šie ištekliai įkeliami nuo *šiandien 8.00* iki *šiandien + 1 12:00*.
- **Surinkimo eilutė: šie** ištekliai pakrauti *nuo šiandien + 1 į 12:00* iki *šiandien + 2 10:00*.

Toliau pateikta iliustracija rodo gautą Gantt diagramą (pasirinkite ją didesnį rodinį).

[![Gantt diagrama, kurioje rodomos išankstinės sąlygos.](media/finite-examples-conditions-small.png "Gantt diagrama, kurioje rodomos išankstinės sąlygos")](media/finite-examples-conditions.png)

### <a name="example-1--infinite-capacity-planning"></a>1 pavyzdys – neriboto pajėgumo planavimas

Šiame pavyzdyje rodomi planavimo rezultatai, kai naudojate neriboto pajėgumo planavimą, o ne riboto pajėgumo planavimą.

Bendrasis planas turi šiuos atitinkamus parametrus, kurie uždrausa plano riboto pajėgumo planavimą:

- **Ribotas pajėgumas:** *Ne.*

Taip **pat nustatyta abiejų** atitinkamų išteklių riboto pajėgumo *pasirinktis*, kad būtų išjungtas jų riboto pajėgumo planavimas:

- Uždavimo eilutė
- Surinkimo linija

Dabar įtraukiate naują pardavimo užsakymą, kuriame yra *8* produkto1 *prekės,* ir paleidžiate planą. Todėl sistema įkelia pagal šiandienos *eilutę 8.00* *val. iki šiandien 12.00* val. Kai operacijos eilutėje baigiamos, *sistema įkels surinkimo eilutę nuo šiandien 12.00* *iki šiandien 14.00 val*.

Toliau pateikta iliustracija rodo gautą Gantt diagramą (pasirinkite ją didesnį rodinį).

[![Gantt diagrama, kurioje rodomas neriboto pajėgumo planavimo pavyzdys.](media/finite-examples-example1-small.png "Gantt diagrama, kurioje rodomas neriboto pajėgumo planavimo pavyzdys")](media/finite-examples-example1.png)

### <a name="example-2--finite-capacity-planning-with-a-time-fence-of-one-day"></a>2 pavyzdys – ribotas pajėgumo planavimas, naudojant vienos dienos laiko ribą

Šiame pavyzdyje rodomi planavimo rezultatai, kai naudojate riboto pajėgumo planavimą ir vienos dienos laiko ribą.

Bendrasis planas turi šiuos atitinkamus parametrus, kurie įgalina riboto pajėgumo planavimą ir nustato plano laiko ribą:

- **Ribotas pajėgumas:** *taip*
- **Ribotos pajėgumo laiko ribos:** *1*

Taip **pat nustatyta abiejų** atitinkamų išteklių riboto pajėgumo *pasirinktis Taip*, kad įgalintų jų riboto pajėgumo planavimą:

- Uždavimo eilutė
- Surinkimo linija

Dabar įtraukiate naują pardavimo užsakymą, kuriame yra *8* produkto1 *prekės,* ir paleidžiate planą. Todėl sistema įkelia *eilutę iš šiandien + 1 į 8:00* iki *šiandien + 1 12:00*. Kai operacijos eilutėje yra baigtos, *sistema įkels surinkimo eilutę nuo šiandien + 1 prie 12:00* *iki šiandien + 1 14:00*. Sistema atsižvelgia į tik vienos dienos pajėgumą.

Toliau pateikta iliustracija rodo gautą Gantt diagramą (pasirinkite ją didesnį rodinį).

[![Gantt diagrama, kurioje rodomas riboto pajėgumo planavimas naudojant vienos dienos laiko ribą.](media/finite-examples-example2-small.png "Gantt diagrama, kurioje rodomas riboto pajėgumo planavimas naudojant vienos dienos laiko ribą")](media/finite-examples-example2.png)

### <a name="example-3--finite-capacity-planning-with-a-time-fence-of-two-days"></a>3 pavyzdys – ribotas pajėgumo planavimas, naudojant dviejų dienų laiko ribą

Šiame pavyzdyje rodomi planavimo rezultatai, kai naudojate riboto pajėgumo planavimą ir dviejų dienų laiko ribą.

Bendrasis planas turi šiuos atitinkamus parametrus, kurie įgalina riboto pajėgumo planavimą ir nustato plano laiko ribą:

- **Ribotas pajėgumas:** *taip*
- **Ribotos pajėgumo laiko ribos:** *2*

Taip **pat nustatyta abiejų** atitinkamų išteklių riboto pajėgumo *pasirinktis Taip*, kad įgalintų jų riboto pajėgumo planavimą:

- Uždavimo eilutė
- Surinkimo linija

Dabar įtraukiate naują pardavimo užsakymą, kuriame yra *8* produkto1 *prekės,* ir paleidžiate planą. Todėl sistema įkelia *eilutę iš šiandien + 1 į 12:00* *iki šiandien + 1 16:00*. Kai operacijos eilutėje yra baigtos, *sistema įkels surinkimo eilutę nuo šiandien + 2 prie 8:00* iki *šiandien + 2 10:00*. Sistema atsižvelgia į tik dviejų dienų riboto pajėgumą.

Toliau pateikta iliustracija rodo gautą Gantt diagramą (pasirinkite ją didesnį rodinį).

[![Gantt diagrama, kurioje rodomas ribotas pajėgumo planavimas, naudojant dviejų dienų laiko ribą.](media/finite-examples-example3-small.png "Gantt diagrama, kurioje rodomas ribotas pajėgumo planavimas naudojant dviejų dienų laiko ribą")](media/finite-examples-example3.png)

> [!IMPORTANT]
> Visada turėtumėte nustatyti riboto pajėgumo laiko ribą, kurios reikia jūsų verslo poreikiams patenkinti. Pavyzdžiai, pateikti šiame straipsnyje, tik iliustruoja funkcijas. Iš tikrųjų, daugelio gamintojų, kurie naudoja riboto pajėgumo planavimą, vienos dienos laiko riba yra per žema.
