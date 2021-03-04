---
title: Neigiamos dienos ir dinaminės neigiamos dienos
description: Šioje temoje pateikiama informacija apie neigiamas dienas ir dinamines neigiamas dienas, taip pat apie tai, kaip jomis naudotis, kad būtų lengviau atlikti verslo reikalus.
author: t-benebo
manager: tfehr
ms.date: 06/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e64a4bd9e65b62bb782785a363aa2eee5264e3a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433568"
---
# <a name="negative-days-and-dynamic-negative-days"></a>Neigiamos dienos ir dinaminės neigiamos dienos

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie neigiamas dienas ir dinamines neigiamas dienas, taip pat apie tai, kaip jomis naudotis, kad būtų lengviau atlikti verslo reikalus. *Neigiamų dienų laiko riba* reiškia, kiek dienų norite palaukti prieš užsisakydami naują papildymą, kai atsargų kiekis neigiamas.

Šioje temoje sužinosite toliau nurodytą informaciją.

- Kaip kuriami suplanuoti užsakymai
- Neigiamų dienų laiko ribos koreliavimas su prekės gamybos laiku
- Kaip apskaičiuojama dinaminių neigiamų dienų laiko riba ir kaip skaičiuojant įtraukiamas prekės gamybos laikas
- Kaip interpretuoti su neigiamomis dienomis susijusius [pasiūlymus dėl medžiagų poreikio planavimo (MRP) (bendrojo planavimo) vykdymo trukmės tobulinimo](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx)

Šioje temoje naudojami trys hipotetiniai scenarijai, padedantys suprasti šią informaciją. Scenarijai skiriasi toje vietoje, kurioje gaunamas poreikis: prieš, per prekės gamybos laikotarpį arba po jo.

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a>1 scenarijus: poreikis gaunamas prieš prekės gamybos laikotarpį

Gali būti, kad poreikį gausite sąlyginai anksti prekės gamybos laikotarpiu arba prieš pat gamybos laikotarpio pradžią. Toliau pateikiamas šio scenarijaus pavyzdys.

- DemoProduct prekei taikomas šešių dienų pirkimo vykdymo laikas.
- Nulinę dieną (sausio 1 d.) DemoProduct prekės atsargų lygis yra 0 (nulis).
- Nulinę dieną (sausio 1 d.) gausite pardavimo užsakymą, kuriame nurodytas 10 DemoProduct prekių kiekis.
- Septintą dieną (sausio 7 d.) esamame pirkimo užsakyme nurodytas 10 DemoProduct prekių kiekis.

Tolesnėje iliustracijoje vaizduojamas grafinis šio scenarijaus rodinys.

![1 scenarijaus grafinis rodinys](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>A atvejis: neigiamų dienų skaičius mažesnis negu prekės gamybos laiko dienų skaičius

Jei nustatytas neigiamų dienų skaičius mažesnis negu prekės gamybos laiko dienų skaičius, MRP DemoProduct prekės kvitų ieško neigiamų dienų laiko riboje. Kadangi MRP kvitų neranda, sukuriamas naujas suplanuotas pirkimo užsakymas. Šis suplanuotas užsakymas nedelsiant atidedamas šešioms dienoms (gamybos laikas). Todėl jis bus pristatomas sausio 7 dieną. Vykdant esamą pirkimo užsakymą gaunamas veiksmo pranešimas **Atšaukti**, nes sukūrus naują suplanuotą pirkimo užsakymą, esamas užsakymas tapo perteklinis.

Tolesnėje iliustracijoje vaizduojama šio atvejo ekrano kopija.

![1 scenarijaus A atvejo ekrano kopija](./media/negative-days-2.png)

Tolesnėje iliustracijoje vaizduojamas grafinis rodinys, apimantis tai, kas nutinka šiuo atveju.

![1 scenarijaus A atvejo grafinis rodinys](./media/negative-days-3.png)

Jei atkreiptumėte dėmesį į MRP našumą ir plano nervingumą, šiuo atveju nepasiekiama gerų rezultatų. MRP turi sukurti naują suplanuotą užsakymą ir apskaičiuoti atidėjimus ir veiksmus. Šios užduotys užima daug laiko. Šiuo atveju į jūsų planą taip pat įtraukiamos dar dvi operacijos. Kita vertus, pardavimo užsakymas atidedamas tik šešioms dienoms, ne septynioms dienoms.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>B atvejis: neigiamų dienų skaičius didesnis negu prekės gamybos laiko dienų skaičius

Norėdami pagerinti MRP našumą, galite nustatyti tokį neigiamų dienų skaičių, kuris būtų didesnis negu prekės gamybos laiko dienų skaičius. Kadangi įgyvendindami šį scenarijų prekės gamybos laikotarpiu tiekimo gauti negalite, galite ieškoti kvitų tol, kol tai daryti bus prasminga. Nors MRP vykdymo laikas bus trumpesnis, turite stebėti, kad nebūtų kitų užsakymų atidėjimų.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>C atvejis: automatiškas prekės gamybos laiko koreliavimas su neigiamų dienų laiko riba

Norėdami automatiškai koreliuoti prekės gamybos laiką su neigiamų dienų laiko riba, naudokite dinamines neigiamas dienas. Norėdami naudoti dinamines neigiamas dienas, eikite į **Bendrasis planavimas \> Sąranka \> Bendrojo planavimo parametrai** ir skyriaus **Padengimas** skirtuke **Bendra** nustatykite **Naudoti dinamines neigiamas dienas** parinktį **Taip**. Tada MRP dinaminių neigiamų dienų laiko ribose ieško kvitų. Ši laiko riba apskaičiuojama pagal tokią formulę:

Dinaminių neigiamų dienų laiko riba = pirkimo vykdymo laikas + neigiamų dienų laiko riba + (dabartinė data – poreikio data)

(Jei numatytasis DemoProduct prekės užsakymo tipas yra **Gamyba** arba **Perkėlimas**, gamybos laikas yra **atsargų** gavimo laikas.)

Kai naudojamos dinaminės neigiamos dienos, laiko riba, kai MRP ieško kvitų, dabar yra 6 + 2 + 0 = 8 dienos. MRP randa esamą pirkimo užsakymą ir susieja jį su pardavimo užsakymu. Naujų suplanuotų užsakymų nesukuriama. Todėl MRP vykdymo laikas trumpesnis. Tolesnėje iliustracijoje vaizduojami DemoProduct prekės grynieji poreikiai.

![1 scenarijaus C atvejo grynieji poreikiai](./media/negative-days-4.png)

Tolesnėje iliustracijoje vaizduojamas grafinis rodinys, apimantis tai, kas nutinka šiuo atveju.

![1 scenarijaus C atvejo grafinis rodinys](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>D atvejis: naudoti tik dinamines neigiamas dienas

Nustačius neigiamų dienų reikšmę **0** (nulis) ir naudojantis tik dinaminių neigiamų dienų laiko riba, dinaminių neigiamų dienų laiko riba yra 6 + 0 + 0 = 6 dienos. Tokiu atveju rezultatas yra toks pat, kaip rezultatas šio scenarijaus A atveju. MRP turi sukurti naują suplanuotą užsakymą ir apskaičiuoti atidėjimus ir veiksmus. Šios užduotys užima daug laiko, taip pat gali būti erzinančios. Taip pat turite atlikti dar dvi operacijas. Kadangi negali būti laiku patenkintas poreikis, kad būtų galima pristatyti prekę, šiuo atveju tai sukuria nereikalingų jūsų plano komplikacijų.

Tolesnėje iliustracijoje vaizduojama šio atvejo ekrano kopija.

![1 scenarijaus D atvejo ekrano kopija](./media/negative-days-6.png)

Tolesnėje iliustracijoje vaizduojamas grafinis rodinys, apimantis tai, kas nutinka šiuo atveju.

![1 scenarijaus D atvejo grafinis rodinys](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>E atvejis: naudoti tiek neigiamas dienas, kurių daugiau negu prekės gamybos laiko dienų, tiek dinaminių neigiamų dienų laiko ribą

Jei nustatysite tokį neigiamų dienų skaičių, kuris bus didesnis negu prekės gamybos laiko dienų skaičius, taip pat naudosite dinaminių neigiamų dienų laiko ribą, dinaminių neigiamų dienų laiko riba bus 6 + 6 + 0 = 12 dienų. Taikant šį metodą gali būti sukuriama labai ilga laiko riba, per kurią MRP turi ieškoti rezultatų. Norėdami gauti informacijos apie tai, kaip E atvejis susijęs su situacija, kai nustatoma ilga neigiamų dienų laiko riba, žr. šios temos skyrių [Išvada](#conclusion).

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a>2 scenarijus: poreikis gaunamas prekės gamybos laikotarpiu

Gali būti, kad poreikį gausite kažkuriuo metu prekės gamybos laikotarpiu. Toliau pateikiamas šio scenarijaus pavyzdys.

- DemoProduct prekei taikomas šešių dienų pirkimo vykdymo laikas. 
- Nulinę dieną (sausio 1 d.) DemoProduct prekės atsargų lygis yra 0 (nulis).
- Ketvirtą dieną (sausio 5 d.), t. y. per prekės gamybos laiką, gaunate pardavimo užsakymą, kuriame nurodytas 10 DemoProduct prekių kiekis.
- Septintą dieną (sausio 8 d.) pirkimo užsakyme nurodytas 10 DemoProduct prekių kiekis.

Tolesnėje iliustracijoje vaizduojamas grafinis šio scenarijaus rodinys.

![1 scenarijaus grafinis rodinys](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>A atvejis: neigiamų dienų skaičius mažesnis negu prekės gamybos laiko dienų skaičius

Jei nustatytas neigiamų dienų skaičius mažesnis negu prekės gamybos laiko dienų skaičius, MRP DemoProduct prekės kvitų ieško neigiamų dienų laiko riboje. Kadangi MRP kvitų neranda, sukuriamas naujas suplanuotas pirkimo užsakymas, kuriame dabartinė data naudojama kaip užsakymo data. Šis suplanuotas užsakymas nedelsiant atidedamas šešioms dienoms (gamybos laikas). Todėl jis bus pristatomas sausio 7 dieną. Vykdant esamą pirkimo užsakymą gaunamas veiksmo pranešimas **Atšaukti**, nes sukūrus naują suplanuotą pirkimo užsakymą, esamas užsakymas tapo perteklinis.

Tolesnėje iliustracijoje vaizduojama šio atvejo ekrano kopija.

![2 scenarijaus A atvejo ekrano kopija](./media/negative-days-9.png)

Tolesnėje iliustracijoje vaizduojamas grafinis rodinys, apimantis tai, kas nutinka šiuo atveju.

![2 scenarijaus A atvejo grafinis rodinys](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>B atvejis: neigiamų dienų skaičius didesnis negu prekės gamybos laiko dienų skaičius

Ši atvejis panašus į 1 scenarijaus B atvejį. Jei nustatysite tokį neigiamų dienų skaičių, kuris bus didesnis negu prekės gamybos laiko dienų skaičius, naujo suplanuoto užsakymo negausite. Pardavimo užsakymas pridedamas prie esamo pirkimo užsakymo.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>C atvejis: automatiškas prekės gamybos laiko koreliavimas su neigiamų dienų laiko riba

Šis atvejis panašus į 1 scenarijaus C atvejį, nes dinaminės neigiamos dienos naudojamos lygiai taip pat kaip ir tuo atveju. Dinaminių neigiamų dienų laiko riba dabar yra 6 + 2 – 4 = 4 dienos. Taikant šį metodą, MRP randa esamą pirkimo užsakymą ir prie jo prideda pardavimo užsakymą. Kadangi nauji suplanuoti užsakymai nesukuriami, MRP vykdymo laikas trumpesnis.

Tolesnėje iliustracijoje vaizduojama šio atvejo ekrano kopija.

![2 scenarijaus C atvejo ekrano kopija](./media/negative-days-11.png)

Tolesnėje iliustracijoje vaizduojamas grafinis rodinys, apimantis tai, kas nutinka šiuo atveju.

![2 scenarijaus C atvejo grafinis rodinys](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>D atvejis: naudoti tik dinamines neigiamas dienas

Nustačius neigiamų dienų reikšmę **0** (nulis) ir naudojantis tik dinaminių neigiamų dienų laiko riba, dinaminių neigiamų dienų laiko riba dabar yra 6 + 0 – 4 = 2 dienos. Tokiu atveju rezultatas yra toks pat, kaip rezultatas šio scenarijaus A atveju. Norėdami pamatyti grafinį rodinį, kuriame vaizduojama, kas nutinka, žr. šio scenarijaus A atvejį.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>E atvejis: naudoti tiek neigiamas dienas, kurių daugiau negu prekės gamybos laiko dienų, tiek dinaminių neigiamų dienų laiko ribą

Jei nustatysite tokį neigiamų dienų skaičių, kuris bus didesnis negu prekės gamybos laiko dienų skaičius, taip pat naudosite dinaminių neigiamų dienų laiko ribą, dinaminių neigiamų dienų laiko riba bus 6 + 6 – 4 = 8 dienos. Taikant šį metodą gali būti sukuriama labai ilga laiko riba, per kurią MRP turi ieškoti rezultatų. Norėdami gauti informacijos apie tai, kaip E atvejis susijęs su situacija, kai nustatoma ilga neigiamų dienų laiko riba, žr. šios temos skyrių [Išvada](#conclusion).

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a>3 scenarijus: poreikis gaunamas pasibaigus prekės gamybos laikotarpiui

Gali būti, kad poreikį gausite pasibaigus prekės gamybos laikui. Toliau pateikiamas šio scenarijaus pavyzdys.

- DemoProduct prekei taikomas šešių dienų pirkimo vykdymo laikas.
- Nulinę dieną (sausio 1 d.) DemoProduct prekės atsargų reikšmė yra 0 (nulis).
- Septintą dieną (sausio 8 d.), t. y. ne prekės gamybos laiku, gaunate pardavimo užsakymą, kuriame nurodytas 10 DemoProduct prekių kiekis.
- 10 dieną (sausio 11 d.) pirkimo užsakyme nurodytas 10 DemoProduct prekių kiekis.

Tolesnėje iliustracijoje vaizduojamas grafinis šio scenarijaus rodinys.

![3 scenarijaus grafinis rodinys](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>A atvejis: neigiamų dienų skaičius mažesnis negu prekės gamybos laiko dienų skaičius

Jei nustatytas neigiamų dienų skaičius mažesnis negu prekės gamybos laiko dienų skaičius, MRP ieško dvi dienas iki pardavimo užsakymo poreikio datos. Kadangi MRP nieko neranda, sausio 2 d. sukuriamas suplanuotas pirkimo užsakymas. Šis suplanuotas pirkimo užsakymas bus išsiųstas pačiu laiku, kad būtų patenkintas pardavimo užsakymo poreikis. Vykdant esamą pirkimo užsakymą gaunamas veiksmo pranešimas **Atšaukti**, nes šio užsakymo nereikia.

Tolesnėje iliustracijoje vaizduojama šio atvejo ekrano kopija.

![3 scenarijaus A atvejo ekrano kopija](./media/negative-days-14.png)

Tolesnėje iliustracijoje vaizduojamas grafinis rodinys, apimantis tai, kas nutinka šiuo atveju.

![3 scenarijaus A atvejo grafinis rodinys](./media/negative-days-15.png)

> [!NOTE]
> Ankstesnėje ekrano kopijoje pirkimo užsakymo pareikalavimo data yra sausio 12 d. Kadangi ekrano kopija daryta 2015 m. sausio 11 d. sekmadienį, MRP perkėlė pareikalavimo datą į kitą darbo dieną – pirmadienį, sausio 12 d. Nepaisant to, pirkimo užsakymo pristatymo data yra sausio 11 d.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>B atvejis: neigiamų dienų skaičius didesnis negu prekės gamybos laiko dienų skaičius

Jei nustatysite tokį neigiamų dienų skaičių, kuris bus didesnis negu prekės gamybos laiko dienų skaičius, naujo suplanuoto užsakymo negausite. Pardavimo užsakymas susiejamas su esamu pirkimo užsakymu. Todėl pardavimo užsakymas atidedamas. Jei kuriate suplanuotą užsakymą, pardavimo užsakymą galite siųsti laiku.

Tolesnėje iliustracijoje vaizduojama šio atvejo ekrano kopija.

![3 scenarijaus B atvejo ekrano kopija](./media/negative-days-16.png)

Tolesnėje iliustracijoje vaizduojamas grafinis rodinys, apimantis tai, kas nutinka šiuo atveju.

![3 scenarijaus B atvejo grafinis rodinys](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>C atvejis: automatiškas prekės gamybos laiko koreliavimas su neigiamų dienų laiko riba

Šis atvejis panašus į 1 scenarijaus C atvejį, nes dinaminės neigiamos dienos naudojamos lygiai taip pat, kaip ir šio scenarijaus B atveju, o gal net ir geriau.

Dinaminių neigiamų dienų laiko riba yra 6 + 2 – 7 = 1 diena. Tačiau šiuo atveju sistema vis dar atsižvelgia į neigiamų dienų gamybos laiką (2), nes MRP įvertina maksimalią skirtumo tarp neigiamų dienų gamybos laiko ir dinaminių neigiamų dienų gamybos laiko reikšmę. Todėl tokiu atveju rezultatas yra toks pat, kaip rezultatas šio scenarijaus A atveju.

Tolesnėje iliustracijoje vaizduojamas grafinis rodinys, apimantis tai, kas nutinka šiuo atveju.

![3 scenarijaus C atvejo grafinis rodinys](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>D atvejis: naudoti tik dinamines neigiamas dienas

Nustačius neigiamų dienų reikšmę **0** (nulis) ir naudojantis tik dinaminių neigiamų dienų laiko riba, dinaminių neigiamų dienų laiko riba dabar yra 6 + 0 – 7 = -1 diena. Šiuo atveju sistema vis dar atsižvelgia į neigiamų dienų gamybos laiką (2). Todėl tokiu atveju rezultatas yra toks pat, kaip rezultatas šio scenarijaus A atveju, ir esama tokių pačių trūkumų. Norėdami pamatyti grafinį rodinį, kuriame vaizduojama, kas nutinka, žr. 2 scenarijaus A atvejį.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>E atvejis: naudoti tiek neigiamas dienas, kurių daugiau negu prekės gamybos laiko dienų, tiek dinaminių neigiamų dienų laiko ribą

Šis atvejis toks pat, kaip 1 ir 2 scenarijų E atvejis. Jam būdingi iš esmės tie patys privalumai ir trūkumai.

## <a name="conclusion"></a>Išvada

Kaip pastebima šioje temoje apžvelgus tris scenarijus, naudinga nustatyti tokį neigiamų dienų skaičių, kuris būtų didesnis negu padengimo grupės prekių gamybos laiko dienų skaičius. Taip pat naudinga naudoti tik dinamines neigiamas dienas ir nustatyti tokį neigiamų dienų skaičių, kuris atitiktų skaičių, kiek dienų norite palaukti prieš užsakydami naują papildymą, kai atsargų kiekis neigiamas (kitaip tariant, kiek dar dienų pageidaujate atidėti poreikį). Be to, tos pačios padengimo grupės prekių gamybos laikai turėtų būti panašūs.

Nustačius neigiamų dienų reikšmę **0** (nulis) ir nenaudojant dinaminių neigiamų dienų, MRP visada sukuria naują suplanuotą užsakymą, kad būtų patenkintas poreikis. Šiuo atveju svarbu dirbant atkreipti dėmesį į veiksmų pranešimus, kad įsitikintumėte, jog neprisikaups atsargų.

Galbūt norėsite nustatyti ilgą neigiamų dienų laiko ribą, o paskui dirbti su veiksmų pranešimais. Naudojantis šiuo metodu pasiekiama gerų planavimo rezultatų, bet jis lėtesnis. Taip pat gali būti sunkiau analizuoti, nes turite analizuoti ir taikyti veiksmų pranešimus. Toliau pateikiamas pavyzdys.

- DemoProduct prekei taikomas šešių dienų pirkimo vykdymo laikas.
- Nulinę dieną (sausio 1 d.) DemoProduct prekės atsargų reikšmė yra 0 (nulis).
- Nulinę dieną (sausio 1 d.) gausite pardavimo užsakymą, kuriame nurodytas 10 DemoProduct prekių kiekis.
- 10 dieną (sausio 10 d.) gausite pardavimo užsakymą, kuriame nurodytas 10 DemoProduct prekių kiekis.
- 12 dieną (sausio 12 d.) pirkimo užsakyme nurodytas 10 DemoProduct prekių kiekis.
- Nustatyta neigiamų dienų reikšmė **20** ir ši reikšmė daug didesnė už prekės gamybos laiko dienų reikšmę.

Tolesnėje iliustracijoje vaizduojamas grafinis rodinys, apimantis tai, kas nutinka.

![Grafinė pavyzdžio peržiūra](./media/negative-days-19.png)

MRP pasiekiama toliau nurodytų rezultatų.

![Rezultatai](./media/negative-days-20.png)

Ankstesnėje ekrano kopijoje pardavimo užsakymo pareikalavimo data yra sausio 9 d., o ne sausio 10 d. Kadangi ekrano kopija daryta 2015 m. sausio 10 d. šeštadienį, užsakymo pareikalavimo data turėtų būti ankstesnė darbo diena – penktadienis, sausio 9 d.

MRP sukuria suplanuotą pirkimo užsakymą, kad būtų patenkintas pirmame pardavimo užsakyme nurodytas poreikis, tačiau paskui taip pat rekomenduoja atšaukti suplanuotą užsakymą, nes galima paankstinti esamą pirkimo užsakymą ir padidinti jame nurodytą kiekį.

Rezultatai nėra klaidingi, tačiau MRP vykdymo laikas gali būti ilgesnis, nes MRP turi sukurti visus atidėjimus ir pasiūlymus. Be to, planuotuvui gali reikėti daugiau laiko MRP rezultatams suprasti. Šiuo atveju svarbiausia tai, kad planuotuvas suprastų ir naudotų veiksmų pranešimus.

Jei neigiamų dienų skaičių sumažinsite tiek, kad jis būtų artimesnis prekės gamybos laiko dienų skaičiui, ir naudositės dinaminėmis dienomis, MRP pasiekiama toliau nurodytų rezultatų.

![Rezultatai](./media/negative-days-21.png)

MRP sukuria suplanuotą užsakymą, kuris pridedamas prie pirmo pardavimo užsakymo. Paskui, kaip ir tikėtasi, antras pardavimo užsakymas susiejamas su esamu pirkimo užsakymu, atsižvelgiant į neigiamų dienų nuostatas. Šis suplanuotas rezultatas taip pat teisingas, o MRP vykdymo laikas gali būti trumpesnis. Šiuo atveju svarbu suprasti ir žinoti, kaip dirbti su veiksmų pranešimais.

Norėdami padėti užtikrinti, kad būtų įvedamos teisingos jūsų įmonės reikšmės, turite galvoti ir apie funkcines galimybes, ir apie MRP vykdymo laiką. Todėl norint nustatyti optimalias reikšmes gali tekti pasinaudoti bandymų ir klaidų metodu.

## <a name="see-also"></a>Taip pat žiūrėkite

Išsamaus aptarimo ieškokite pradiniame tinklaraščio įraše [Daugiau apie (dinamines) neigiamas dienas](https://blogs.msdn.microsoft.com/axmfg/2015/02/19/more-about-dynamic-negative-days/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]