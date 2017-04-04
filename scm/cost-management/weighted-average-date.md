---
title: Svertinio vidurkio data
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 2016-01-07 19 - 58 - 01
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28991
ms.assetid: 945d5088-a99d-4e54-bc42-d2bd61c61e22
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d05059f1b1da12ec27bd83d43275c82ac6130590
ms.lasthandoff: 03/29/2017


---

# <a name="weighted-average-date"></a>Svertinio vidurkio data



Svertinio vidurkio diena yra atsargų modelis, kuris remiasi svertinio vidurkio principu. Svertinio vidurkio principo taikymui atsargų išdavimai vertinami naudojant vidutinę prekių, gautų į atsargas kiekvieną atskirą atsargų uždarymo laikotarpio dieną, vertę. Kai vykdote atsargų uždarymą, naudodami svertinio vidurkio dieną, visi dienos gavimai sudengiami prieš virtualų išdavimą. Šis virtualus išdavimas turi bendrą gautą kiekį ir vertę tą dieną. Virtualus išdavimas turi atitinkamą virtualų gavimą, pagal kurį bus sudengti išdavimai. Todėl visų išdavimų vidutinės išlaidos būna tokios pačios. Virtualus išdavimas ir virtualus gavimas gali būti suprantamas kaip virtualus perkėlimas, vadinamasis *svertinio vidurkio atsargų uždarymo perkėlimas*. Jei tą dieną arba iki tos dienos įvyko tik vienas gavimas, vidurkio vertinti nereikės. Visi išdavimai sutvarkomi nuo to gavimo, todėl nereikės kurti virtualaus perdavimo. Taip pat, jei vieninteliai išdavimai įvykdomi tą dieną, nėra gavimų, iš kurių būtų galima vertinti vidurkį, ir virtualusis perkėlimas taip pat nebus sukurtas. Kai naudojate svertinę vidutinę datą, galite pažymėti atsargų operacijas, kad tam tikros prekės gavimas būtų sudengiamas su tam tikru išdavimu. Šiuo atveju nereikia naudoti svertinio vidurkio dienos taisyklės. Naudojant svertinio vidurkio datos atsargų modelį, rekomenduojame kas mėnesį uždaryti atsargas. Svertinis vidutinis dienos įkainojimo metodą apskaičiuoti naudojama ši formulė: svertinis vidurkis = (\[Q1 × P1\] + \[2 k. x P2\] + \[Q*n* × P*n*\]) ÷ (Q1 + Q2 + Q*n*) metu atsargos, skaičiavimas atliekamas kiekvieną dieną per uždarymo laikotarpiu, kaip parodyta šioje iliustracijoje. ![Svertinio vidurkio dienos duomenų skaičiavimo modelis](./media/weightedaveragedatedailycalculationmodel.gif) Atsargų operacijos, paliekančios atsargas, įskaitant pardavimo užsakymus, atsargų žurnalus, pirkimo kredito pažymas ir gamybos užsakymus, atliekamos registravimo datą įvertinta savikaina. Ši apskaičiuota savikaina taip pat vadinama paleidžiamąja vidutine savikaina. Atsargas uždaryti dieną, sistema analizuoja ankstesnių laikotarpių, ankstesnių dienų ir einamosios dienos atsargų operacijas. Ši analizė naudojama siekiant nustatyti, kurį iš šių uždarymo principų reikia naudoti:

-   Tiesioginis sudengimas
-   Suvestinis sudengimas

Sudengimai yra atsargų uždarymo registravimas, per kurį išdavimai nustatomi pagal pataisytą svertinį vidurkį uždarymo datą. **Pastaba:** daugiau informacijos apie gyvenviečių, skaitykite straipsnį apie atsargų uždaryti. Pateiktame pavyzdyje parodytas svertinio vidurkio naudojimo su penkiomis konfigūracijomis poveikis:

-   Svetinio vidurkio dienos tiesioginis sudengimas be pasirinkties **Įtraukti faktinę vertę**
-   Svetinio vidurkio dienos apibendrintas sudengimas be pasirinkties **Įtraukti faktinę vertę**
-   Svetinio vidurkio dienos tiesioginis sudengimas su pasirinktimi **Įtraukti faktinę vertę**
-   Svertinio vidurkio dienos suvestinis sudengimas su pasirinktimi **Įtraukti faktinę vertę**
-   Svertinio vidurkio diena su žymėjimu

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Svetinio vidurkio dienos tiesioginis sudengimas be pasirinkties Įtraukti faktinę vertę
Dabartinė versija naudoja tą patį tiesioginio atsiskaitymo principą, kuris buvo naudojamas svertinis vidurkis ankstesnėse versijose. Sistema sudengia tiesiogiai tarp gavimų ir išdavimų. Sistema naudoja šį tiesioginio atsiskaitymo principus konkrečiose situacijose:

-   Per laikotarpį užregistruotas vienas gavimas ir vienas arba keletas išdavimų.
-   Per laikotarpį buvo užregistruoti tik išdavimai, o atsargose yra prekių nuo ankstesnio uždarymo.

Toliau pateiktame scenarijuje užregistruotas finansiškai atnaujintas gavimas ir išdavimas. Atsargos, sistema įsikuria tiesiogiai nuo klausimo gavimo ir savikainai koreguoti būtina klausimo. Toliau pavaizduoti šie sandoriai:

-   1a. Atsargų faktinis gavimas atnaujintas 5 vienetais, kiekvieno vieneto kaina 10,00 USD.
-   1b. Atsargų finansinis gavimas atnaujintas 5 vienetais, kiekvieno vieneto kaina 10,00 USD.
-   2a. Atsargų faktinis išdavimas atnaujintas 2 vienetais, kiekvieno vieneto kaina 10,00 USD.
-   2b. Atsargų finansinis išdavimas atnaujintas 2 vienetais, kiekvieno vieneto kaina 10,00 USD.
-   3. Atsargų uždarymas atliekamas taikant tiesioginio sudengimo būdą, kad būtų sudengtas finansinis atsargų gavimas su finansiniu atsargų išdavimu.

![Svetinio vidurkio dienos tiesioginis sudengimas be pasirinkties Įtraukti faktinę vertę](./media/weightedaveragedatedirectsettlementwithoutincludephysicalvalue.gif) **Iliustracijos paaiškinimas:**

-   Atsargų operacijos parodomos vertikaliomis rodyklėmis.
-   Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
-   Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
-   Virš arba po kiekviena vertikalią rodyklę, atsargų operacijos vertė yra nurodyta kaip *kiekis*@*vieneto kaina*.
-   Jei atsargų operacijos vertė yra skliausteliuose, tai reiškia, kad atsargų operacija atsargose užregistruota fiziškai.
-   Jei atsargų operacijos vertė nėra skliausteliuose, tai reiškia, kad atsargų operacija atsargose užregistruota finansiškai.
-   Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
-   Each vertical arrow is labeled with a sequential identifier, such as *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje seką.
-   Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme *Atsargų uždarymas*.
-   Iki atsargų uždarymo atlikti sudengimai rodomi punktyrinėmis raudonomis rodyklėmis su brūkšneliais, einančiomis įstrižai nuo gavimo prie išdavimo.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Svetinio vidurkio dienos apibendrintas sudengimas be pasirinkties Įtraukti faktinę vertę
Svertinis vidurkis yra pagrįstas principu, kad visų įplaukų uždarymo laikotarpio, yra apibendrinti naują atsargų perdavimo sandorį. Šis sandoris vadinamas *svertinio vidurkio atsargų uždarymu*. Visi tos dienos gavimai bus sudengiami pagal naujai sukurtos atsargų perkėlimo operacijos išdavimą. Visi tos dienos išdavimai sudengiami pagal naujai sukurtos atsargų perkėlimo operacijos gavimą. Jeigu po atsargų uždarymo turimas atsargų kiekis yra teigiamas, tos turimos atsargos ir atsargų vertė susumuojamos naujoje atsargų perdavimo operacijoje (gavimas). Jeigu po atsargų uždarymo turimas atsargų kiekis yra neigiamas, turimos atsargos ir atsargų vertė yra iki galo nesudengtų atskirų išdavimų suma. Toliau pateikiamame scenarijuje nurodomi keli finansiškai atnaujinti gavimai ir išdavimai, užregistruoti šiuo laikotarpiu. Atliekant inventorizaciją, arti, sistema vertina kiekvieną dieną, siekiant nustatyti, kaip kiekvieną dieną turėtų būti vertinamas, uždaryti. Toliau pavaizduoti šie sandoriai: **1 diena:**

-   1a. Atsargų faktinis gavimas atnaujintas 3 vienetais, kiekvieno vieneto kaina 15,00 USD.
-   1b. Atsargų finansinis gavimas atnaujintas 3 vienetais, kiekvieno vieneto kaina 15,00 USD.
-   2a. 1 vieneto, kurio slankiojo vidurkio kaina 15,00 USD, atsargų faktinis išdavimas.
-   2b. 1 vieneto, kurio slankiojo vidurkio kaina 15,00 USD, atsargų finansinis išdavimas.

Sistemos naudoja tiesioginio atsiskaitymo metodas 1 diena. **2 diena:**

-   3a. 1 vieneto, kurio slankiojo vidurkio kaina 15,00 USD, atsargų faktinis išdavimas.
-   3b. 1 vieneto, kurio slankiojo vidurkio kaina 15.00 USD, finansinis išdavimas iš atsargų

Sistemos naudoja tiesioginio atsiskaitymo metodas 2 diena. **3 diena:**

-   4a. 1 vieneto, kurio slankiojo vidurkio kaina 15,00 USD, atsargų faktinis išdavimas.
-   4b. 1 vieneto, kurio slankiojo vidurkio kaina 15.00 USD, finansinis išdavimas iš atsargų
-   5a. 1 vieneto, kurio kaina 17,00 USD, atsargų faktinis gavimas.
-   5b. 1 vieneto, kurio kaina 17,00 USD, atsargų finansinis gavimas.

Atsargų uždarymas atliktas. Reikės naudotis tiesioginiu sudengimu, nes per kelias dienas įvyksta keli gavimai.

-   7a. Svertinio vidurkio atsargų uždarymo operacijos finansinis išdavimas sukuriamas 2 vienetams, kurių kiekvieno kaina 32,00 USD, kad visų atsargų finansinių gavimų sudengimai būtų suvedami į datą, kuri dar nebuvo uždaryta.
-   7b. Svertinio vidurkio atsargų uždarymo operacijos finansinis gavimas sukuriamas kaip 7a balansas.

Sistema generuoja ir registruoja apibendrintą atsargų perdavimo operacijos. Be to, sistema nusėda visų įplaukų dieną ir turimų atsargų ankstesnių dienų prieš apibendrintą atsargų perdavimo išdavimo operaciją. Visi tos dienos išdavimai sudengiami pagal naujai sukurtos atsargų perkėlimo operacijos gavimą. Apskaičiuota svertinio vidurkio savikaina 16,00 USD. Išdavimas bus koreguojamas 1,00 USD prie svertinio vidurkio kainos prisitaikyti. Nauja slankiojo vidurkio savikaina yra 16,00 USD. Toliau pateikiamoje iliustracijoje rodoma ši operacijų seka su rezultatais, pasirinkus svertinio vidurkio atsargų modelį ir suvestinio sudengimo principą be **Įtraukti faktinę vertę** pasirinkties. ![Svetinio vidurkio dienos apibendrintas sudengimas be pasirinkties Įtraukti faktinę vertę](./media/weightedaveragedatesummarizedsettlementwithoutincludephysicalvalue.gif) **Iliustracijos paaiškinimas:**

-   Atsargų operacijos parodomos vertikaliomis rodyklėmis.
-   Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
-   Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
-   Virš arba po kiekviena vertikalią rodyklę, atsargų operacijos vertė yra nurodyta kaip *kiekis*@*vieneto kaina*.
-   Jei atsargų operacijos vertė yra skliausteliuose, tai reiškia, kad atsargų operacija atsargose užregistruota fiziškai.
-   Jei atsargų operacijos vertė nėra skliausteliuose, tai reiškia, kad atsargų operacija atsargose užregistruota finansiškai.
-   Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
-   Each vertical arrow is labeled with a sequential identifier, such as *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje seką.
-   Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme *Atsargų uždarymas*.
-   Iki atsargų uždarymo atlikti sudengimai rodomi punktyrinėmis raudonomis rodyklėmis su brūkšneliais, einančiomis įstrižai nuo gavimo prie išdavimo.
-   Raudonos ištisinės įstrižai einančios rodyklės rodo gavimo operacijas, sudengiamas su sistemos sukurta išdavimo operacija.
-   Žaliomis ištisinėmis įstrižai einančiomis rodyklėmis rodoma korespondentinės sistemos sugeneruota gavimo operacija, kuri sudengiama su pradine užregistruota išdavimo operacija.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Svetinio vidurkio dienos tiesioginis sudengimas su pasirinktimi Įtraukti faktinę vertę
Dabartinę versiją naudoja tą patį tiesioginio atsiskaitymo principą svertinė vidutinė data naudojama ankstesnėse versijose. Sistema sudengia tiesiogiai tarp gavimų ir išdavimų. Sistema naudoja šį tiesioginio atsiskaitymo principus konkrečiose situacijose:

-   Per laikotarpį užregistruotas vienas gavimas ir vienas arba keletas išdavimų.
-   Per laikotarpį buvo užregistruoti tik išdavimai, o atsargose yra prekių nuo ankstesnio uždarymo.

Jei pasirinksite į **įtraukti faktinę vertę** žymės langelį klausimu į **atsargų modelio grupė** puslapyje, sistema naudoja fiziškai atnaujintų gavimų skaičiuodama įvertinta savikaina, arba veikia vidurkį. Išdavimai registruojami remiantis įvertinta laikotarpio savikaina. Uždarant atsargas finansiškai atnaujinti gavimai bus naudojami tik skaičiuojant svertinį vidurkį.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Svertinio vidurkio dienos suvestinis sudengimas su pasirinktimi Įtraukti faktinę vertę
Jei pasirinksite į **įtraukti faktinę vertę** žymės langelį klausimu į **atsargų modelio grupė** puslapyje, sistema naudoja fiziškai atnaujintų gavimų skaičiuodama įvertinta savikaina, arba veikia vidurkį. Išdavimai registruojami remiantis įvertinta laikotarpio savikaina. Uždarant atsargas finansiškai atnaujinti gavimai bus naudojami tik skaičiuojant svertinį vidurkį. Svertinio vidurkio sudengimo principas paremtas tuo, kad visi uždarymo laikotarpio gavimai yra sumuojami naujoje atsargų perkėlimo operacijoje, kuri vadinama *svertinio vidurkio atsargų uždarymu*. Visi tos dienos gavimai bus sudengiami pagal naujai sukurtos atsargų perkėlimo operacijos išdavimą. Visi tos dienos išdavimai sudengiami pagal naujai sukurtos atsargų perkėlimo operacijos gavimą. Jeigu po atsargų uždarymo turimas atsargų kiekis yra teigiamas, tos turimos atsargos ir atsargų vertė susumuojamos naujoje atsargų perdavimo operacijoje (gavimas). Jeigu po atsargų uždarymo turimas atsargų kiekis yra neigiamas, turimos atsargos ir atsargų vertė yra iki galo nesudengtų atskirų išdavimų suma.

## <a name="weighted-average-date-when-marking-is-used"></a>Svertinio vidurkio diena su žymėjimu
Ženklas yra procesas, kuris leidžia jums susieti išdavimo operaciją, gavimo operacija. Žymėjimą galima atlikti prieš arba po operacijos registravimo. Žymėjimą galima naudoti norint sužinoti tikslią atsargų kainą registruojant operaciją arba atliekant atsargų uždarymą. Pavyzdžiui, jūsų Klientų aptarnavimo tarnyba priėmė skubų užsakymą iš svarbaus kliento. Kadangi tai skubus užsakymas, norėdami patenkinti kliento pageidavimus, už šią prekę turėsite mokėti daugiau. Įsitikinkite, kad šios atsargų prekės kaina atitinka maržą, arba šio pardavimo užsakymo SF parduotų prekių kainą (COGS). Kai pirkimo užsakymas užregistruojamas, gaunama atsargų už 120,00 USD. Jeigu šis pardavimo užsakymo dokumentas pažymėtas prie pirkimo užsakymo prieš užregistruojant važtaraštį. Tada COGS bus 120,00 USD – prekei nebus taikoma dabartinio slankiojo vidurkio kaina. Jeigu pardavimo užsakymo važtaraštis arba SF užregistruojami prieš žymėjimą, COGS bus užregistruota taikant slankiojo vidurkio savikainą. Prieš atsargų uždarymą šias dvi operacijas dar galima žymėti kartu. Kai gavimo operacija yra pažymėta išdavimo operacijai, vertinimo metodo, kuris yra apibrėžtas prekės modelių grupei, bus nepaisoma. Vietoj to, sistema sprendžia šiuos sandorius tarpusavyje. Galite pažymėti išdavimo operaciją su gavimu prieš užregistruodami operaciją. Tai galima atlikti iš pardavimo užsakymo eilutės puslapyje **Išsami pardavimo užsakymo informacija**. Galite peržiūrėti atidarytas gavimo operacijas **Žymėjimo** puslapyje. Galite pažymėti išdavimo operaciją prie gavimo užregistravę operaciją. Galite pažymėti išdavimo operaciją atvirai gavimo atsargose esančiai prekei iš registruoto atsargų koregavimo žurnalo. Toliau pavaizduoti šie sandoriai:

-   1a. 1 vieneto, kurio savikaina 10,00 USD, atsargų faktinis gavimas.
-   1b. 1 vieneto, kurio savikaina 10,00 USD, atsargų finansinis gavimas.
-   2a. 1 vieneto, kurio savikaina 20,00 USD, atsargų faktinis gavimas.
-   2b. 1 vieneto, kurio savikaina 20,00 USD, atsargų finansinis gavimas.
-   3a. 1 vieneto, kurio savikaina 25,00 USD, atsargų faktinis gavimas.
-   4a. 1 vieneto, kurio savikaina 30,00 USD, atsargų faktinis gavimas.
-   4b. 1 vieneto, kurio savikaina 30,00 USD, atsargų finansinis gavimas.
-   5a. 1 vieneto, kurio savikaina 21,25 USD, atsargų faktinis išdavimas (finansinių ir faktinių atnaujintų operacijų slankusis vidurkis).
-   5b. Prieš užregistruojant operaciją, 1 vieneto atsargų finansinis išdavimas yra pažymimas kaip 2b atsargų gavime. Ši operacija užregistruojama 20,00 USD savikaina.
-   6a. 1 vieneto, kurio savikaina 21,25 USD, atsargų faktinis išdavimas.
-   7. Atsargų uždarymas atliktas. Dėl to, kad finansiškai atnaujinta operacija yra pažymėta kaip jau esamas gavimas, šios operacijos sudengiamos ir joks koregavimas neatliekamas.

Nauja slankiojo vidurkio savikaina rodo finansiškai ir fiziškai atnaujintų operacijų vidurkį – 27,50 USD. Toliau iliustruojama operacijų serija, kai pasirenkamas svertinio vidurkio atsargų modelis su žymėjimu. ![Svertinio vidurkio diena su žymėjimu](./media/weightedaveragedatewithmarking.gif) **Iliustracijos paaiškinimas:**

-   Atsargų operacijos parodomos vertikaliomis rodyklėmis.
-   Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
-   Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
-   Virš arba po kiekviena vertikalią rodyklę, atsargų operacijos vertė yra nurodyta kaip *kiekis*@*vieneto kaina*.
-   Jei atsargų operacijos vertė yra skliausteliuose, tai reiškia, kad atsargų operacija atsargose užregistruota fiziškai.
-   Jei atsargų operacijos vertė nėra skliausteliuose, tai reiškia, kad atsargų operacija atsargose užregistruota finansiškai.
-   Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
-   Each vertical arrow is labeled with a sequential identifier, such as *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje seką.
-   Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme *Atsargų uždarymas*.
-   Iki atsargų uždarymo atlikti sudengimai rodomi punktyrinėmis raudonomis rodyklėmis su brūkšneliais, einančiomis įstrižai nuo gavimo prie išdavimo.



