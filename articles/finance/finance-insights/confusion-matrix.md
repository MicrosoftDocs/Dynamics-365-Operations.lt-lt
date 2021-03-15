---
title: Mašininio mokymo modelių rezultatai (peržiūros versija)
description: Šioje temoje aptariamos supainiojimo matricos, klasifikavimo problemos ir mašininio mokymo (ML) modelių tikslumas. Siekiama, kad geriau suprastumėte ML prognozavimo rezultatų tikslumą.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-14
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 5223bdfbc0f5828b5dccac30362783075ce8157f
ms.sourcegitcommit: f59df61799915f6a79aec7e3e8664c02df6597da
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/22/2021
ms.locfileid: "5044377"
---
# <a name="results-of-machine-learning-models-preview"></a>Mašininio mokymo modelių rezultatai (peržiūros versija)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje aptariamos supainiojimo matricos, klasifikavimo problemos ir mašininio mokymo (ML) modelių tikslumas. Siekiama, kad geriau suprastumėte ML prognozavimo rezultatų tikslumą. Tikslinė auditorija apima inžinierius, analitikus ir vadovus, kurie nori plėtoti savo žinias ir įgūdžius duomenų mokslo srityje.

## <a name="confusion-matrix"></a>Supainiojimo matrica
Kai prižiūrimos ML problemos išmokoma naudojant istorinių duomenų rinkinį, ji išbandoma naudojantis duomenimis, kurie nėra įtraukiami į mokymo procesą. Tokiu būdu galite palyginti išmokyto modelio prognozes su faktinėmis reikšmėmis. Supainiojimo matrica suteikia priemonių vertinti, kiek sėkminga yra klasifikacijos problema ir kur daroma klaidų (t. y., kur susipainiojama).

Pavyzdžiui, jūsų tikslas yra nuspėti, ar augintinis yra šuo, ar katė, remiantis tam tikrais fiziniais bei elgesio atributais. Jei naudojamas bandomasis duomenų rinkinys, kuriame yra 30 šunų ir 20 kačių, supainiojimo matrica gali būti panaši į šį paveikslėlį.

![Rūšių prognozavimo pavyzdys](media/species-prediction-matrix.png)

Žalių langelių skaičiai atitinka teisingas prognozes. Kaip matote, modelis teisingai prognozuoja didesnę faktinių kačių procentinę dalį. Bendrą modelio tikslumą yra lengva apskaičiuoti. Šiuo atveju: 42 ÷ 50 arba 0,84.

### <a name="multi-class-classifiers-in-a-confusion-matrix"></a>Kelių klasių klasifikatoriai supainiojimo matricoje

Dauguma diskusijų apie supainiojimo matricą yra sutelktos į dvejetainius klasifikatorius, kaip ankstesniame pavyzdyje. Šis atvejis yra specialus, nes galima atsižvelgti į kitą metriką, pvz., jautrumą ir atitiktį.

Toliau apsvarstysime finansinės situacijos klasifikavimo problemą, apimančią tris būsenas. Modelis prognozuoja, ar kliento SF bus sumokėta laiku, pavėluotai ar labai pavėluotai. Pavyzdžiui, iš 100 bandomųjų SF 50 yra apmokamos laiku, 35 apmokamos pavėluotai, o 15 – labai pavėluotai. Šiuo atveju modelis gali sukurti supainiojimo matricą, kuri panaši į šį paveikslėlį.

![1 modelis](media/payment-prediction-matrix.png)]

Supainiojimo matrica suteikia daug daugiau informacijos, nei paprasta tikslumo metrika. Tačiau ją vis tiek gana lengva suprasti. Supainiojimo matrica nurodo, ar turite subalansuotą duomenų rinkinį, kai pateikiamų klasių skaičiai yra panašūs. Naudojant kelių klasių scenarijų, ji nurodo, kaip toli nuo prognozės ji gali būti, kai pateikiamos klasės yra kelintiniai skaičiai, kaip ankstesniame pavyzdyje apie kliento mokėjimus.

## <a name="model-accuracy"></a>Modelio tikslumas 
Įvairi tikslumo metrika pranašesnė tuo, kad gali kiekybiškai įvertinti modelio kokybę. 

Kadangi tikslumas yra paprasta suprasti metrika, jis yra geras pradžios taškas aiškinant modelį kitiems žmonėms, ypač modelio vartotojams, kurie nėra duomenų mokslininkai. Norint suprasti modelio tikslumą, nėra būtina suprasti statistinius duomenis. Kai galima supainiojimo matrica, ji suteikia papildomų įžvalgų apie modelio našumą.

Tačiau, siekiant geresnio supratimo, reikia atkreipti dėmesį į keletą su tikslumu susijusių iššūkių. Metrikos naudingumas priklauso nuo problemos konteksto. Dažnai dėl modelio našumo kyla klausimas „Kiek geras modelis yra?“ Tačiau atsakymas į šį klausimą ne visada yra paprastas. Apsvarstykite tolesnę supainiojimo matricą (2 modelis).

![Apmokėjimo prognozės pavyzdys su didesne imtimi](media/payment-prediction-matrix-2.png)

Greitai suskaičiavus matoma, kad šio modelio tikslumas yra (70 + 10 + 3) ÷ 100 arba 0,83. Iš pirmo žvilgsnio šis rezultatas atrodo geresnis nei ankstesnio kelių klasių modelio (1 modelis) rezultatas, kurio tikslumas buvo 0,73. Tačiau ar jis yra geresnis?

Norėdami pradėti spręsti šį klausimą, atsižvelkite į paprasto spėjimo tikslumą. Sprendžiant klasifikacijos problemą, paprastas spėjimas visada prognozuos dažniausią klasę. 1 modelio atveju spėjimas bus „laiku“, o jo tikslumas bus 0,50. 2 modelio spėjimas taip pat bus „laiku“, o jo tikslumas bus 0,80. Kadangi 1 modelis už paprastą spėjimą yra geresnis 0,73 – 0,50 = 0,23, o 2 modelis už paprastą spėjimą geresnis 0,83 – 0,80 = 0,03, 1 modelis yra geresnis, nors jo tikslumas ir yra mažesnis. Apskaičiavus matyti, kad, norint efektyviai įvertinti modelio kokybę, reikia atsižvelgti į platesnį kontekstą nei tikslumo reikšmė.

Verta pažymėti dar vieną aspektą. Įsivaizduokite situaciją, kai paciento liga nustatoma atliekant medicininį tyrimą. Ši problema yra dvejetainio klasifikavimo problema, kai teigiamas rezultatas rodo, kad pacientas serga liga. Šioje situacijoje turite pagalvoti apie tolesnių klaidų poveikį.

- Klaidingai teigiami rezultatai, kai tyrimu nustatoma, kad pacientas serga liga, bet iš tikrųjų jis neserga
- Klaidingai neigiami rezultatai, kai tyrimu nustatoma, kad pacientas neserga liga, bet iš tikrųjų jis serga

Akivaizdu, kad abu klaidų tipai yra nepageidautini, tačiau kuris iš jų yra blogesnis? Tai vėl priklauso nuo aplinkybių. Tuo atveju, kad liga yra pavojinga gyvybei ir ją reikia greitai gydyti, svarbiau yra sumažinti klaidinga neigiamų rezultatų skaičių (tada geriausia atlikti papildomų tyrimų). Kitose mažiau svarbiose situacijose modelių kūrėjai gali sumažinti klaidingai teigiamų rezultatų skaičių. Bet kokiu atveju galima daryti pagrįstą išvadą, kad, norint veiksmingai nustatyti modelio kokybę, reikia daugiau informacijos nei pateikia tikslumo metrika.

### <a name="recommendations"></a>Rekomendacijos

Tikslumas yra svarbi priemonė bendraujant su sričių ekspertais, kurie nėra susipažinę su statistika. Tačiau, norint, kad informacija būtų naudinga, svarbu kartu su tikslumo reikšme pateikti papildomo konteksto.

Mokėjimo prognozavimo situacijoje galite nustatyti ML modelio tikslą, apimantį skirtingo apmokėjimo elgesio veiksnius. Tikslas yra toks: modelis turi pagerinti paprastą spėjimą, bent 50 procentų sumažindamas neteisingų atsakymų skaičių. Kitaip tariant, norite, kad tikslinis tikslumas būtų maždaug per vidurį tarp paprasto spėjimo tikslumo ir 100 procentų tikslumo esanti reikšmė.

Tolesnėje lentelėje apibendrinamas šis principas, taikomas šioje temoje aprašomoms supainiojimo matricoms.

| Modelis   | Paprastas spėjimas | Uždavinys | Modelio tikslumas | Ar tikslas pasiektas?                                          |
|---------|-------------|--------|----------------|-----------------------------------------------------------|
| 1 modelis | 0.50        | 0.75   | 0.73           | Beveik. Šis modelis iš esmės pagerina spėjimą. |
| 2 modelis | 0.80        | 0.90   | 0.83           | Nr. Reikia tobulinti.                              |

## <a name="classification-f1-accuracy"></a>Klasifikacijos F1 tikslumas

Galiausiai šioje temoje panagrinėsime pažangesnę klasifikavimo ML našumo priemonę, vadinamą F1 tikslumu.

Kad būtų galima apibrėžti F1 tikslumą, reikia įvesti dvi papildomas metrikas: tikslumo ir atitikties. Tikslumas nurodo, kiek visų prognozių, kurios nurodytos kaip teigiamos, yra tinkamai priskirta. Ši metrika taip pat vadinama teigiama prognozavimo reikšme. Atitiktis yra bendrasis faktinių teigiamų atvejų skaičius, kuris buvo teisingas nuspėtas. Ši metrika taip pat vadinama jautrumu.

[![Teisingi rezultatai, palyginti su klaidingais rezultatais](./media/tn-fn.png)](./media/tn-fn.png)

Pirmesnėje iliustracijoje pateiktoje supainiojimo matricoje ši metrika apskaičiuojamos taip:

- Tikslumas = TP ÷ (TP + FP)
- Atitiktis = TP ÷ (TP + FN)

F1 priemonė sujungia tikslumą ir atitiktį. Rezultatas yra dviejų reikšmių harmoninis vidurkis. Jis apskaičiuojamas taip:

- F1 = 2 × (tikslumas × atitiktis) ÷ (tikslumas + atitiktis)

Pažvelkime į konkretų pavyzdį. Anksčiau šioje temoje buvo pateiktas modelio pavyzdys, kuris prognozavo, ar gyvūnas buvo šuo, ar katė. Iliustracija pakartojama čia.

[![Rūšių spėjimo pavyzdys (pakartotinas)](./media/species-prediction-matrix.png)](./media/species-prediction-matrix.png)

Toliau pateikiami rezultatai, jei kaip teigiamas atsakymas naudojamas „Šuo“.

- Tikslumas = 24 ÷ (24 + 2) = 0,9231
- Atitiktis = 24 ÷ (24 + 6) = 0,8
- F1 = 2 × (0,9231 × 0,8) ÷ (0,9231 + 0,8) = 0,8572

Kaip matote, F1 reikšmė yra tarp tikslumo ir atitikties reikšmių.

Nors F1 tikslumą nėra taip lengva suprasti, jis pagrindinį tikslumo skaičių patikslina. Jis taip pat gali padėti naudojant nesubalansuotus duomenų rinkinius, kaip bus aptarta toliau.

Šios temos skyriuje [Modelio tikslumas](#model-accuracy) buvo palygintos tolesnės dvi supainiojimo matricos. Nepaisant to, kad pirmo modelio tikslumas buvo mažesnis, jis buvo laikomas naudingesniu, nes jis pasirodė esantis tobulesnis už numatytąjį spėjimą dėl vienkartinio mokėjimo.

![Apmokėjimo prognozavimas, palyginti su faktiniais duomenimis (pavyzdys)](media/payment-prediction-matrix.png)

![Mokėjimo spėjimo pavyzdys su didesniu pavyzdžiu (pakartotinas)](media/payment-prediction-matrix-2.png)

Pažiūrėkime, kaip šie du modeliai atrodo, kai naudojamas F1 balas. Į F1 balą įskaičiuojamas kiekvienos būsenos tikslumas ir atitiktis, o F1 makroskaičiavimais tada nustatomas vidutinis visų būsenų F1 balas, kad būtų galima nustatyti bendrąjį F1 balą. Yra ir kitų F1 variantų, tačiau naudingiau panagrinėti makroversiją, atsižvelgiant į vienodą visų trijų būsenų nagrinėjimą.

Norint supaprastinti skaičiavimus, buvo sukurti imčių masyvai, kad būtų sugretintos faktinės ir prognozuojamos reikšmės. Šie masyvai reikšmėms apskaičiuoti naudojo „Python“ „sklearn“ metrikos biblioteką. Toliau parodytas rezultatas.

| Modelis   | Paprastas spėjimas | Tikslumas | F1 makro |
|---------|-------------|----------|----------|
| 1 modelis | 0.5         | 0.73     | 0.67     |
| 2 modelis | 0.80        | 0.83     | 0.66     |

Kad galėtumėte daugiau sužinoti apie tai, kaip šis skaičiavimas veikia, toliau pateikiama 1 modelio sklearn.metrics klasifikacijos ataskaita. Tris būsenas „Laiku“, „Vėluoja“ ir „Labai vėluoja“ atitinka eilutės, atitinkamai pažymėtos 1, 2 ir 3. Makrovidurkis yra tik stulpelio „F1-score“ vidurkis.

|           | tikslumas | atitiktis   | f1-score |
|-----------|-----------|----------|----------|
| **1**     | 0.83      | 0.80     | 0.82     |
| **2**     | 0.68      | 0.71     | 0.69     |
| **3**     | 0.50      | 0.50     | 0.50     |

Kaip rodo šie rezultatai, šių dviejų modelių F1 makrotikslumo balai yra beveik vienodi. Šiuo ir daugeliu kitų atvejų F1 tikslumas yra geresnis modelio pajėgumo rodiklis. Tikslumo atžvilgiu, interpretuojant rezultatus reikia suprasti, ką svarbiausia nagrinėti modelyje.

#### <a name="privacy-notice"></a>Privatumo pranešimas
Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]