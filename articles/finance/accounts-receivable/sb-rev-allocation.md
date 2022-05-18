---
title: Įplaukų paskirstymas
description: Šioje temoje paaiškinama, kaip naudoti įplaukų paskirstymą sąskaitų pateikimo metu.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 09d3e9295f1fb753156aa603b00372316173721e
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695252"
---
# <a name="revenue-allocation"></a>Įplaukų paskirstymas

Šioje temoje paaiškinama, kaip nustatyti sąskaitų pateikimo grafiko įplaukų paskirstymo parametrus. Kurdami sąskaitų pateikimo grafiką galite nustatyti arba redaguoti įplaukų paskirstymą. Kai atidarote aktyvaus **arba** nutrauktas sąskaitų pateikimo grafiko įplaukų paskirstymo puslapį, laukų informaciją galima tik skaityti.

## <a name="specify-the-revenue-allocation-for-a-billing-schedule"></a>Nurodyti įplaukų paskirstymą atsiskaitymo grafikui

Norėdami nurodyti įplaukų paskirstymą atsiskaitymo grafikui, atlikite šiuos veiksmus.

1. Visų / **aktyvių atsiskaitymo grafikų** sąrašo puslapyje pasirinkite atsiskaitymo grafiką arba atsiskaitymo grafiko eilutę.
2. **Puslapio viršuje skirtuke** Įplaukų paskirstymas pasirinkite Įplaukų **paskirstymas**.
3. Lauke Kelių **elementų išdėstymo tipas** pasirinkite kelių elementų išdėstymo tipą (MEA).
4. Lauke Kelių **elementų išdėstymo** numeris nurodykite MEA numerį. Tada lauke Atidėtų **sutarties įplaukų sąskaita** nurodykite atidėtos sutarties įplaukų sąskaitą.

    Jei lauke Kelių elementų **išdėstymo** tipas nustatomas kaip **Vienas**, **·** **kiekvienai** eilutei taikomos tos pačios kelių elementų išdėstymo ir Atidėtų sutarčių įplaukų sąskaitų vertės. Jei lauke Kelių elementų **išdėstymo tipas** nustatomas kaip **Kelios**, galite **nurodyti** **skirtingas kiekvienos eilutės kelių elementų išdėstymo numeris ir Atidėtos sutarties** įplaukų sąskaitos vertės.
    
    MEA numerį galima priskirti tik dviem arba daugiau prekių. Viena eilutė negali turėti savo MEA numerio.

5. Pasirinkite **Įrašyti**.

### <a name="fields"></a>Laukai

Puslapyje **Kelių elementų išdėstymas** yra šie laukai.

| Laukas | Aprašymas |
|---|---| 
| Kelių elementų išdėstymo tipas | <p>Pasirinkti operacijos MEA tipą:</p><ul><li>**Sudėtinis** – operacijos eilutės prekės yra MEA dalis arba yra daugiau nei vienas išdėstymas.</li><li>**Nėra** – operacija yra standartinė operacija, kuri neturi jokio įplaukų paskirstymo.</li><li>**Vienas** – visos operacijos prekės yra vienos MEA dalis.</li></ul> |
| Kelių elementų išdėstymo numeris | <p>Eilutės MEA numeris. Šis laukas galimas, kai kelių **elementų išdėstymo** tipo laukas nustatytas kaip **Kartotinis**.</p><p>Jei šis laukas tuščias, o jūs priskiriate MEA numerį, **·** **·** **atskira** pardavimo kainos kilmė ir atskirą pardavimo kainą laukai yra automatiškai atnaujinami, remiantis prekių atskirą pardavimo kainos puslapyje esančiomis vertėmis. Galimi tik MEA numeriai, priskirti kitoms pardavimo užsakymo eilutėms.</p> |
| Atidėtųjų sutarties įplaukų sąskaita | Nurodykite sąskaitą, kuri bus naudojama žurnalo įrašams kuriant MEA sutarties SF. Šis laukas galimas tik tada, kai naudojamas periodinis sutarties atsiskaitymas. |
| **Eilutės** | |
| Varianto numeris | Pardavimo užsakymo varianto numeris. |
| Prekės numeris | Pardavimo užsakymo prekės numeris. |
| Atsiskaitymo dažnumas | Įplaukų paskirstymo dažnumas: kas dieną **, kas mėnesį** **, ketvirtį** **,** kas pusmetį **arba kasmet** **.** |
| Kiekis | Vertė iš pardavimo užsakymo. |
| Sutarties vertė | Sutarties vertė. |
| Kelių elementų išdėstymo numeris | <p>Eilutės MEA numeris. Šis laukas galimas, kai kelių **elementų išdėstymo** tipo laukas nustatytas kaip **Kartotinis**.</p><p>Jei šis laukas tuščias, o jūs priskiriate MEA numerį, **·** **·** **atskira** pardavimo kainos kilmė ir atskirą pardavimo kainą laukai yra automatiškai atnaujinami, remiantis prekių atskirą pardavimo kainos puslapyje esančiomis vertėmis. Galimi tik MEA numeriai, priskirti kitoms pardavimo užsakymo eilutėms. Jei šios prekės vertės nėra nustatytos, naudojamos vertės iš puslapio **Kelių elementų įplaukų** paskirstymo parametrai.</p> | 
| Atskiros prekės pardavimo kainos kilmė | <p>Autonominės pardavimo kainos kilmė:</p><ul><li>**Suma** – atskira pardavimo kaina yra suma, kurią nurodote, kuri yra didesnė nei 0 (nulis). Jei reikia, suma konvertuojama tarp funkcinių ir keliomis valiutomis.</li><li>**Bazinė pardavimo** kaina – atskira pardavimo kaina atitinka prekės bazinę pardavimo kainą.</li><li>**SF kaina** – atskira pardavimo kaina atitinka prekės SF kainą.</li><li>**Prekės procentas** – atskira pardavimo kaina nurodoma kaip procentinė vertė ir skaičiuojama remiantis prekės kaina. Jei pasirinkta ši pasirinktis, nurodykite numatytąją procentinę dalį.</li><li>**Paskirstyti likutinę** sumą – *atskira* pardavimo kaina apskaičiuojama kaip bendroji pirminės prekės sutarties vertė – *bendroji atskira antrinių prekių pardavimo kaina*:</p><ul><li>*Bendroji pirminės prekės sutarties vertė yra* grynoji arba išrašytų sąskaitų suma.</li><li>*Bendroji atskira antrinių* prekių pardavimo kaina yra bendroji visų antrinių prekių išplėstinės ar sutarties atskira pardavimo kaina, išskyrus antrųjų prekių, kurios naudoja šią atskirą pardavimo kainos kilmę.</li></ul><p>Jei apskaičiuota suma yra neigiama, suma nustatoma 0 (nulis).</p><p>**Pastaba: šią** pasirinktį galima pasirinkti tik vienam antriniam elementui išskaidytoje įplaukų skaidymo metu.</p></li><li>**Nėra** – atskira pardavimo kaina kilmė – priklauso nuo antrinių prekių. Ši pasirinktis taikoma prekėms, kurios įplaukų skaidymo šablone apibrėžtos kaip pirminės prekės. Jei pažymėtas **žymės langelis** Įplaukų skaidymo, ši pasirinktis automatiškai pasirinkta ir parametro pakeisti negalima.</li><li>**Pirminės SF kainos procentas** – atskira pardavimo kaina yra pagrindinės prekės SF kainos procentas. Ši pasirinktis galima tik antriniams elementams įplaukų skaidymo šablone.</li><li>**Pirminės standartinės kainos** procentas – atskira pardavimo kaina yra standartinės pirminės prekės kainos procentas. Ši pasirinktis galima tik antriniams elementams įplaukų skaidymo šablone. **·** **·** **·** **Kai** antrinių prekių pasirinktis pakeičiama iš pirminės standartinės kainos procentinės dalies į Pirminės SF kainos procentas arba iš Pirminės SF kainos procentinės dalies į Pirminės standartinės kainos procentas, apskaičiuotos vertės taip pat atnaujinamos.</li></ul> |
| Atskira pardavimo kaina | <p>Atskira eilutės pardavimo kaina operacijos valiuta.</p><p>Lauke Suma įvesta **arba** apskaičiuota vertė.</p> |
| Atskira sutarties pardavimo kaina | Sutarties atskira pardavimo kaina. |
| Likusios sutarties įplaukos | Likusi sutarties įplaukų suma. Ši suma yra visų eilučių, kurioms nebuvo sukurtos sąskaitos faktūros, suma. |
| Visos sutarties įplaukos | Bendra sutarties įplaukų suma eilutėje. Ši suma yra visų eilučių suma, neatsižvelgiant į tai, ar joms buvo sukurtos SF. |
| Atidėtųjų sutarties įplaukų sąskaita | <p>Nurodykite sąskaitą, kuri bus naudojama žurnalo įrašams kuriant MEA sutarties SF.</p><p>Šis laukas galimas tik tada, kai naudojamas periodinis sutarties atsiskaitymas.</p> |
| Klaida | Visos klaidos, kurios įvyko paskirstant įplaukas. |

## <a name="use-revenue-allocation-on-a-sales-order"></a>Naudoti įplaukų paskirstymą pardavimo užsakyme

Norėdami pardavimo užsakyme naudoti įplaukų paskirstymo funkciją, atlikite šiuos veiksmus.

1. **Puslapyje Visi pardavimo užsakymai** sukurkite pardavimo užsakymą, kuriame yra prekės.
2. Skirtuke **SF** dalyje Įplaukų **paskirstymas pasirinkite** Įplaukų **paskirstymas**.
3. Lauke Kelių **elementų išdėstymo** tipas pasirinkite MEA tipą.
4. Lauke Kelių **elementų išdėstymo** numeris nurodykite MEA numerį.
5. Jei laukas **Kelių elementų išdėstymo** tipas nustatytas kaip **Kelios**, pasirinkite eilutes, kurias norite, tada pasirinkite Taikyti **pasirinktam**.
6. Pasirinkite **Įrašyti**.

Jei naudojate įplaukas ir išlaidų atidėjimus, atidėjimo grafikas sukuriamas automatiškai. Galite jį peržiūrėti visų **atidėjimų grafikų** puslapyje.
