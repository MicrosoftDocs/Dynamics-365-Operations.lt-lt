---
title: Bendrojo planavimo vykdymo stebėjimas
description: Šioje temoje paaiškinama, kaip gamybos planuotojas gali matyti, ar vyksta bendrasis planavimas.
author: josaw1
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1733562768b3fe869f326bbfb47b6135a91b5cb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829647"
---
# <a name="monitor-a-master-planning-run"></a>Bendrojo planavimo vykdymo stebėjimas

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>Gantt diagramos naudojimas siekiant vizualizuoti bendrojo planavimo eigą

Puslapyje **Peržiūrėti bendrojo planavimo eigą** galite peržiūrėti istorinius bendrojo planavimo vykdymus kaip Gantt diagramą. Ši funkcija gali padėti jums suprasti įvairių bendrojo planavimo etapų laiką. Dėl dabartinės aktyvios planavimo užduoties, puslapį **Peržiūrėti pagrindinio planavimo eigą** galima naudoti norint sekti eigą ir peržiūrėti apskaičiuotą likusį laiką.

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a>Pagrindinio plano eigos vizualizacijos funkcijos įjungimas ir naudojimas

Norėdami naudoti šią funkciją, atlikite toliau nurodytus veiksmus.

1. Darbo srityje **Funkcijos valdymas** skirtuke **Naujas** iš sąrašo pasirinkite **Pagrindinio planavimo eigos vizualizavimas**. Jei funkcija neatsiranda skirtuke **Naujas**, žiūrėkite skirtukus **Neįjungta** ir **Visi**.
1. Pasirinkite **Įjungti dabar**. Arba pasirinkite **Grafikas** ir pasirinkite laiką, kada norite, kad funkcija būtų įjungta.

Puslapyje **Bendrojo planavimo eiga** puslapyje gali būti rodomos istorinės planavimo užduotys ir aktyvios planavimo užduotys. 

Norint peržiūrėti istorines planavimo užduotis, galimos dvi parinktys. 

1. Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**, tada veiksmų skyde pasirinkite **Istorija**. Pasirinkę pageidaujamą užduotį, pasirinkite **Užklausos**, tada pasirinkite **Peržiūrėti eigą**
1. Eikite į **Bendrasis planavimas\> Darbo sritys \> Bendrasis planavimas**, bendrajame planavime spustelėkite **Istorija**. Pasirinkę pageidaujamą užduotį, pasirinkite **Užklausos**, tada pasirinkite **Peržiūrėti eigą**

Norint peržiūrėti aktyvias planavimo užduotis, galimos dvi parinktys. 
1. Eikite į **Bendrasis planavimas \> Darbo sritys \> Bendrasis planavimas**, veiksmų skyde pasirinkite **Nebaigta planavimo eiga**. Pasirinkę pageidaujamą užduotį, pasirinkite **Užklausos**, tada pasirinkite **Peržiūrėti eigą**.
1. Eikite į **Bendrasis planavimas\> Darbo sritys \> Bendrasis planavimas**, bendrajame planavime spustelėkite **Peržiūrėti eigą**. Pasirinkę pageidaujamą užduotį, pasirinkite **Užklausos**, tada pasirinkite **Peržiūrėti eigą**

Atkreipkite dėmesį, kad aktyvias užduotis galite peržiūrėti, tik kai vykdoma planavimo užduotis.

### <a name="analyze-a-master-planning-job"></a>Bendrojo planavimo užduoties analizavimas

Gantt diagramoje galite išplėsti kiekvieną iš šių planavimo eigų, norėdami peržiūrėti papildomą informaciją apie skirtą laiką:

- Inicijuojama
- Naikinami ir įterpiami duomenys
- Padengimo planavimas
- Delsos
- Veiksmų pranešimai
- Užbaigimas
- Automatinis patvirtinimas

Gantt diagrama yra naudingas įrankis, jei norite peržiūrėti veiksmų pranešimų naudojimo poveikį.

#### <a name="navigation-in-the-gantt-chart"></a>Gantt diagramos naršymas

- Norėdami išplėsti pasirinktą grupę ir rodyti išsamią informaciją, medžio rodinyje pasirinkite pliuso ženklą (**+**).
- Norėdami sutraukti pažymėtą grupę, medžio rodinyje pasirinkite minuso ženklą (**–**).
- Naršymui galite naudoti klaviatūrą. Klavišais **Rodyklės į viršų** ir **Rodyklė į apačią** galite judėti tarp eilučių. Naudokite klavišus **Rodyklė į dešinę** ir **Rodyklė į kairę**, kad išplėstumėte ir sutrauktumėte grupes.
- Norėdami atidaryti arba uždaryti visus Gantt diagramos lygius, pasirinkite **Išplėsti viską** arba **Sutraukti viską**.
- Norėdami peržiūrėti susijusį vykdymo laiką, užveskite žymeklį virš užduoties. (Užduotys yra žemiausias lygis Gantt diagramoje.)

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>Papildomo pagrindinio planavimo vykdymo peržiūrėjimas norint palyginti užduotis

Pasirinkus bendrojo planavimo užduotį lauke **Rodyti papildomą bendrąjį planavimą**, Gantt diagramoje galite peržiūrėti papildomo bendrojo planavimo vykdymą ir palyginti dvi užduotis.

#### <a name="bom-level-display"></a>KS lygio rodymas

Komplektavimo specifikacijų (KS) lygiai rodomi skirtingų padengimų planavimui, vėlavimams, veiksmams ir patvirtinimui.

- **Padengimo planavimas** – KS lygiai rodomi kaip numatyta. Jie apskaičiuojami iš viršaus į apačią.

    **Pavyzdys:** KS lygis 0, 1, 2

- **Vėlavimai** – KS lygiai rodomi kaip padengimo planavimo KS lygiai, padauginti iš –1. (Kitaip tariant, jie turi neigiamą ženklą.)

    **Pavyzdys:** KS lygis –2, –1, 0

- **Veiksmo pranešimas** – KS lygiai rodomi kaip numatyta. Jie apskaičiuojami iš viršaus į apačią.

    **Pavyzdys:** KS lygis 0, 1, 2

- **Automatinis patvirtinimas** – KS lygiai rodomi kaip 999 minus padengimo planavimo KS lygis.

    **Pavyzdys:** KS lygis 999, 998, 997

Šioje lentelėje apibendrinama elgsena.

| Rodomas KS lygis | Galutinė prekė | Subkomponentas | Žaliavos |
|---|---|---|---|
| Padengimo planavimas | 0 | 1 | 2 |
| Delsos | 0 | –1 | –2 |
| Veiksmo pranešimas | 0 | 1 | 2 |
| Automatinis patvirtinimas | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>Eigos vizualizavimas

Jei peržiūrite bendrojo planavimo užduotį, kuri šiuo metu vykdoma, eiga rodoma spalvotai Gantt diagramoje. Toliau nurodytos spalvos taikomos mėlynai temai. Kitose spalvų temose spalvos skirsis.

- **Tamsiai mėlyna** – baigtos planavimo užduotys.
- **Oranžinė** – šiuo metu vykdoma užduotis.
- **Žydra** – likusių užduočių įvertinimas.

Spalva rodoma tik žemiausiame Gantt diagramos lygyje. Norėdami peržiūrėti visas užduotis pagrindinio planavimo užduotyje, pasirinkite **Išplėsti viską** . Likusių užduočių įvertinimas paremtas istorinėmis bendrojo planavimo užduotimis.

## <a name="run-master-planning-and-track-processing-time"></a>Pagrindinio planavimo vykdymas ir vykdymo eigos stebėjimas

1. Numatytoje ataskaitų srityje pasirinkite **Pagrindinis planavimas**.
1. Lauke **Planas** įveskite arba pasirinkite reikšmę.
1. Pasirinkite **Vykdyti**.
1. Parinktį **Stebėti vykdymo laiką** nustatykite kaip **Taip**.
1. Lauke **Gijų skaičius** įveskite skaičių.
1. „FastTab„ **Įtrauktini įrašai** pasirinkite **Filtruoti**.
1. Tinklelyje pasirinkite eilutę, kurioje laukas **Laukas** yra nustatytas kaip **Elemento numeris.**
1. Lauke **Kriterijai** įveskite reikšmę.
1. Pasirinkite **Gerai**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]