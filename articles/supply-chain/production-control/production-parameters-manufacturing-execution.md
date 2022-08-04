---
title: Gamybos parametrai modulyje Gamybos vykdymas
description: Šiame straipsnyje pateikiama informacija apie gamybos parametrų nustatymą gamybos vykdymo dalyje.
author: johanhoffmann
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6d440a0d0d95fe93ed633fa588e1c3a193757d9d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070386"
---
# <a name="production-parameters-in-manufacturing-execution"></a>Gamybos parametrai modulyje Gamybos vykdymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie gamybos parametrų nustatymą gamybos vykdymo dalyje.

Modulis **Gamybos vykdymas** visų pirma skirtas gamybos įmonėms. Jį naudojant galima registruoti gamybos užduotims atlikti ar projektams vykdyti sugaištamą laiką ir sunaudojamas prekes. Prieš pradėdami naudoti modulį Gamybos vykdymas užduotims registruoti, turite nustatyti įvairius gamybos parametrus, apibrėžiančius, kaip ir kada gamybos proceso metu registruojamos registracijos. Nuo nustatytų gamybos parametrų priklauso, kaip valdomos atsargos, gamyba ir kaip skaičiuojami kaštai.

Prieš darbuotojams pradedant registruoti gamybos užduotis turite atidžiai apsvarstyti visus puslapio **Gamybos parametrai** parametrus. Spustelėkite **Gamybos kontrolė** &gt; **Sąranka** &gt; **Gamybos vykdymas** &gt; **Numatytoji gamybos užsakymų informacija**. Jei jūsų įmonė naudoja kelių teritorijų funkciją, galbūt norėsite nustatyti skirtingus gamybos parametrus kiekvienai teritorijai. Integravimo su moduliu **Gamyba** parametrai nustatomi tolesniuose puslapio **Gamybos parametrai** skirtukuose.

- **Bendra** – bendrieji gamybos užduočių parametrai modulyje Gamybos vykdymas.
- **Pradžia** – parametrai, naudojami prasidėjus gamybos operacijoms.
- **Operacijos** – parametrai, taikomi gamybos operacijoms ir atsiliepimams apie operacijas gamybos proceso metu.
- **Skelbti kaip baigtą** – parametrai, naudojami, kai atliekant paskutinę gamybos užsakymo operaciją prekės skelbiamos baigtomis.
- **Kiekio tikrinimas** – parametrai, kuriais tikrinami gamybos užsakymų pradžios ir grįžtamojo ryšio kiekiai.

## <a name="types-of-production-jobs"></a>Gamybos užduočių tipai
Skirtuke **Operacijos** pasirenkama, kuriuos gamybos užduočių tipus reikia registruoti puslapyje **Užduočių registracija**.

Paprastai darbuotojai atlieka nustatymų užduočių ir apdorojimo užduočių registraciją. Tačiau, jei taikoma užduočių planavimo funkcija, galite pasirinkti kitų tipų užduotis, kurias darbuotojai turi registruoti, kai apdorojami gamybos užsakymai. Pavyzdžiui, galite nustatyti, kad reikėtų registruoti transportavimo užduotis.

> [!IMPORTANT]
> Įsitikinkite, kad pasirinkote visus aktualius užduočių tipus. Kitu atveju užduočių gali nepavykti užregistruoti puslapyje **Užduoties registravimas**. Jūsų pasirinktys turi sutapti su pasirinktimis puslapio **Maršrutų grupės** (**Gamybos kontrolė** &gt; **Sąranka** &gt; **Maršrutai** &gt; **Maršrutų grupės**) skirtuko **Sąranka** stulpelyje **Užduočių valdymas**.

Jei maršrutų grupėje pasirinkta **Užduočių valdymas**, šis užduočių tipas skelbiamas baigtu gamybos užsakyme, kai užduotis paskelbiama baigta modulyje Gamybos vykdymas. Kai visi operacijos užduočių tipai, prie kurių pasirinkta **Užduočių valdymas**, paskelbti baigtais, modulyje Gamybos vykdymas operacija paskelbiama baigta.

> [!NOTE]
> Kai kuriuos užduočių tipus galima rankiniu būdu paskelbti naudojant gamybos žurnalus. Tokiu atveju prie užduočių tipo pasirinkite **Užduočių valdymas**, tačiau nesirinkite užduočių tipo registruoti modulio Gamybos vykdymas puslapio **Gamybos parametrai** skirtuke **Operacijos**.

## <a name="bom-consumption-and-picking-list-journals"></a>KS suvartojimo ir išrinkimo dokumentų žurnalai
Svarbu nuosekliai nustatyti komplektavimo specifikacijų (KS) sunaudojimą, nes tai padeda užtikrinti, kad atsargos valdomos efektyviai. Pavyzdžiui, jei modulyje Gamybos vykdymas teisingai nenustatyti KS sunaudojimo parametrai, medžiagos iš atsargų gali būti atimamos du kartus arba apskritai neatimamos.

Puslapyje **Gamybos parametrai** automatinis KS sunaudojimas nustatomas tolesniais trimis etapais.

- Pradėjus gamybą. Šį etapą nustatykite skirtuke **Pradžia**.
- Gamybos proceso metu, baigus operaciją. Šį etapą nustatykite skirtuke **Operacijos**.
- Kai gamybos užsakymas paskelbiamas baigtu. Šį etapą nustatykite skirtuke **Skelbti kaip baigtą**.

Kiekviename etape lauke **Automatinis KS sunaudojimas** galite pasirinkti vieną iš tolesnių trijų prekių paėmimo gamybos užsakymui būdų.

- **Sunaudojimo principas** – ši parinktis naudojama kartu su KS parinktimi, apibrėžta modulyje **Gamyba**. Spustelėkite **Gamybos kontrolės gamybos** &gt; **užsakymai Visi** &gt; **gamybos užsakymai**. Puslapyje **Visi gamybos užsakymai** esančiame sąraše pasirinkite gamybos užsakymą ir veiksmų srityje spustelėkite **KS**. Puslapio **KS** skirtuko **Sąranka** lauke **Sunaudojimo principas** pasirinkite vieną iš tolesnių parinkčių.

  - **Pradžia**
  - **Pabaiga**
  - **Rankinis**
  - Tuščia (parinktis nepasirinkta)
  - **Yra vietoje**

    Jei modulio Gamybos vykdymas skirtuko **Pradžia** lauke **Automatinis KS sunaudojimas** pasirinkta **Sunaudojimo principas**, visos medžiagos, komplektavimo specifikacijoje nustatytos kaip **Pradžia**, iš atsargų atimamos pradėjus operaciją. Vietos **parinktis galima** produktams, kurie įgalinti sandėlio valdymo procesams (WMS). Jei pasirenkate šį sunaudojimo principą, medžiaga sunaudojama baigus sandėlio žaliavų paėmimo darbą. Medžiaga taip pat sunaudojama, kai šį sunaudojimo principą naudojanti KS eilutė pateikiama sandėliui ir medžiaga yra gamybos įvesties vietoje.

    > [!NOTE]
    > Jei modulio Gamybos vykdymas skirtuke **Pradžia** nustatytas laukas **Sunaudojimo principas**, tą patį principą turite pasirinkti skirtuke **Operacijos** arba skirtuke **Skelbti kaip baigtą**. Šis reikalavimas padeda užtikrinti, kad medžiagos iš atsargų atimamos tose KS, kurių gamybos užsakyme kaip sunaudojimo principas naudojamas **Pabaiga**. Jei skirtuke **Operacijos** arba skirtuke **Skelbti kaip baigtą** tas pats sunaudojimo principas nepasirenkamas, medžiagos iš atsargų gali būti atimamos du kartus.

- **Visada** – jei pasirenkate šią etapo parinktį, medžiagos iš atsargų visada atimamos tame etape. Pavyzdžiui, gamybos medžiagos atimamos pradėjus gamybos užsakymą. Kad šis parametras veiktų, skirtukuose **Operacijos** ir **Skelbti kaip baigtą** reikia pasirinkti **Niekada**. Šis reikalavimas padeda užtikrinti, kad prekės iš atsargų nebūtų atimtos du kartus.
- **Niekada** – jei pasirenkate šią etapo parinktį, tame etape KS nenaudojama. Pavyzdžiui, jei visuose trijuose skirtukuose (**Pradžia**, **Operacijos** ir **Skelbti kaip baigtą**) pasirenkate **Niekada**, medžiagas iš atsargų reikia atimti rankiniu būdu.

> [!IMPORTANT]
> Atidžiai apsvarstykite, kaip nustatyti gamybos parametrus, ir įsitikinkite, kad įvairiuose puslapio **Gamybos parametrai** skirtukuose pasirinkti parametrai neprieštarauja vienas kitam.

Tolesniuose pavyzdžiuose parodyti parametrai, palaikantys įvairius KS sunaudojimo principus. Parametrai nustatomi modulio Gamybos vykdymas puslapyje **Gamybos parametrai**.

### <a name="example-1-backflushing-on-operations"></a>1 pavyzdys: atvirkštinė operacijų tvarka

Tolesnius parametrus naudokite, jei išrinkimo dokumentų žurnalus ir KS prekių sunaudojimą reikia generuoti, kai operacijos prekės paskelbiamos baigtomis.

| Skirtukas                | Laukas                          | Parametras                             |
|--------------------|--------------------------------|-------------------------------------|
| Pradžios              | Atnaujinti pradžia tinkle           | **Būsena** arba **Būsena + kiekis** |
| Pradžios              | Automatinis KS suvartojimas      | **Niekada**                           |
| „Operations‟         | Automatinis KS suvartojimas      | **Visada**                          |
| Skelbti baigtu | Automatinis KS suvartojimas      | **Niekada**                           |
| Skelbti baigtu | Atnaujinti pabaigtą ataskaitą tinkle | **Būsena + kiekis**               |

### <a name="example-2-backflushing-on-production"></a>2 pavyzdys: atvirkštinė gamybos tvarka

Tolesnius parametrus naudokite, jei išrinkimo dokumentų žurnalus ir KS prekių sunaudojimą reikia generuoti, kai prekės paskelbiamos baigtomis gamybos užsakyme.

| Skirtukas                | Laukas                          | Parametras                             |
|--------------------|--------------------------------|-------------------------------------|
| Pradžios              | Atnaujinti pradžia tinkle           | **Būsena** arba **Būsena + kiekis** |
| Pradžios              | Automatinis KS suvartojimas      | **Niekada**                           |
| „Operations‟         | Automatinis KS suvartojimas      | **Niekada**                           |
| Skelbti baigtu | Automatinis KS suvartojimas      | **Visada**                          |
| Skelbti baigtu | Atnaujinti pabaigtą ataskaitą tinkle | **Būsena + kiekis**               |

### <a name="example-3-flushing-principle"></a>3 pavyzdys: sunaudojimo principas

Tolesnius parametrus naudokite, jei išrinkimo dokumentų žurnalus ir KS prekių sunaudojimą reikia generuoti atsižvelgiant į nustatytą KS prekių sunaudojimo principą.

| Skirtukas                | Laukas                          | Parametras                |
|--------------------|--------------------------------|------------------------|
| Pradžios              | Atnaujinti pradžia tinkle           | **Būsena + kiekis**  |
| Pradžios              | Automatinis KS suvartojimas      | **Sunaudojimo principas** |
| „Operations‟         | Automatinis KS suvartojimas      | **Sunaudojimo principas** |
| Skelbti baigtu | Automatinis KS suvartojimas      | **Niekada**              |
| Skelbti baigtu | Atnaujinti pabaigtą ataskaitą tinkle | **Būsena + kiekis**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>4 pavyzdys: medžiagų atėmimas paleidžiant gamybos užsakymą

Tolesnius parametrus naudokite, jei išrinkimo dokumentų žurnalus ir KS prekių sunaudojimą reikia generuoti, kai pradedama gamyba.

| Skirtukas                | Laukas                          | Parametras                             |
|--------------------|--------------------------------|-------------------------------------|
| Pradžios              | Atnaujinti pradžia tinkle           | **Būsena + kiekis**               |
| Pradžios              | Automatinis KS suvartojimas      | **Visada**                          |
| „Operations‟         | Automatinis KS suvartojimas      | **Niekada**                           |
| Skelbti baigtu | Automatinis KS suvartojimas      | **Niekada**                           |
| Skelbti baigtu | Atnaujinti pabaigtą ataskaitą tinkle | **Būsena** arba **Būsena + kiekis** |

Atsižvelgiant į anksčiau šiame skyriuje aprašytas pasirinktis, išrinkimo dokumentų žurnalai registruojami įvairiuose gamybos užsakymo proceso etapuose:

- Kai pradedama operacija
- Kai paskelbiamas operacijos kiekio grįžtamasis ryšys
- Kai gamybos užsakyme prekės paskelbiamos baigtomis

### <a name="example-5-manual-bom-consumption"></a>5 pavyzdys: rankinis KS sunaudojimas

Tolesnius parametrus galite naudoti, jei medžiagas iš atsargų visada reikia atimti rankiniu būdu. Šiuo atveju išrinkimo dokumentų žurnalai neregistruojami.


|        Skirtukas         |             Laukas              |         Parametras         |
|--------------------|--------------------------------|-------------------------|
|       Pradžios        |      Atnaujinti pradžia tinkle      | <strong>Būsena</strong> |
|       Pradžios        |   Automatinis KS suvartojimas    | <strong>Niekada</strong>  |
|     „Operations‟     |   Automatinis KS suvartojimas    | <strong>Niekada</strong>  |
| Skelbti baigtu |   Automatinis KS suvartojimas    | <strong>Niekada</strong>  |
| Skelbti baigtu | Atnaujinti pabaigtą ataskaitą tinkle | <strong>Būsena</strong> |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]