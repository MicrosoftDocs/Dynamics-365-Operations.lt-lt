---
title: Planavimo mechanizmo efektyvumo didinimas
description: Šioje temoje pateikiama informacija apie planavimo mechanizmą ir apie tai, kaip padidinti jo efektyvumą.
author: ChristianRytt
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1c1b940754021956998fe27ba16020d4b16aedf1
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433906"
---
# <a name="improve-scheduling-engine-performance"></a>Planavimo mechanizmo efektyvumo didinimas

[!include [banner](../includes/banner.md)]

Išteklių planavimo mechanizmas naudojamas planuojant suplanuotų ir paskelbtų gamybos užsakymų maršrutus. Iš pradžių mechanizmas buvo pristatytas kaip „Dynamics AX 2012“ dalis, o tada buvo kelis kartus tobulinamas.

[Užduočių planavimo problema](https://en.wikipedia.org/wiki/Job_shop_scheduling) yra itin sudėtinga kombinatorinė problema, kurios sprendimo laikas eksponentiškai auga didėjant kintamųjų skaičiui. Dažnai klientai sukonfigūruoja gamybos maršrutus ir susijusius duomenis taip, kad gautos planavimo problemos neįmanoma išspręsti per priimtiną laiką net ir naudojant pačią moderniausią įrangą. Ši tema padės jums perprasti planavimo modulį ir kaip konkretūs nustatymai gali turėti įtakos efektyvumui.

Kai siekiama pagerinti planavimo efektyvumą, bendrosios rekomendacijos gali padėti sumažinti problemos, kurią turi išspręsti mechanizmas, sudėtingumą. Kai kurie pagrindiniai veiksniai, kurie gali turėti įtakos efektyvumui:

- Maršrutai su daugeliu operacijų
- Maršrutai su lygiagrečiomis operacijomis
- Operacijos, kurių išteklių kiekis yra didesnis už vienetą
- Operacijos su daugeliu galimų išteklių
- Naudojami kietieji saitai
- Naudojamas ribotas pajėgumas
- Naudojami skirtingi kalendoriai
- Darbo laiko intervalų skaičius per dieną kalendoriuje
- Bendra maršruto trukmė
- Lygiagrečiai veikia keli planavimo mechanizmai

## <a name="overview-of-basic-scheduling-flow"></a>Pagrindinės planavimo eigos apžvalga

Norėdami suprasti, kokį poveikį sąranka gali turėti efektyvumui, svarbu suprasti apie proceso eigą tiek mechanizme, tiek susijusiame X++ kode.

Pagrindinį užsakymo planavimo procesą sudaro trys pagrindiniai veiksmai:

- **Duomenų įkėlimas** – čia X++ duomenų modeliai paverčiami į mechanizmo vidinį duomenų modelį, kuris dirba su užduotimis ir apribojimais.
- **Planavimas** – tai pagrindinis planavimo šaltinis, kuris apdoroja duotą modelį ir apribojimus bei generuoja rezultatą. Šio proceso metu mechanizmas pagal poreikį prašys X++ darbo laiko informacijos ir esamų pajėgumo rezervavimo.
- **Duomenų įrašymas** – sistemos rezultatą užduoties pajėgumo rezervavimo laiko intervalų forma apdoroja X++ kodas, kad įrašytų pajėgumų rezervavimus ir atnaujintų užduočių / darbo / užsakymo pradžios ir pabaigos laikus.

## <a name="load-data-into-the-engine"></a>Duomenų įkėlimas į mechanizmą

Planavimo mechanizmo duomenų modelis yra labiau abstraktus nei „Supply Chain Management“ duomenų bazė, nes jis buvo sukurtas kaip bendrinis mechanizmas, galintis dirbti su skirtingais duomenų šaltiniais. Maršruto, antrinių operacijų ir vykdymo laiko sąvokos turi būti „išverstos“ į bendrąją užduotį ir apribojimų modelį, su kuriuo dirba mechanizmas. Modelio kūrimo logika didele dalimi yra pagrįsta verslo logika ir skiriasi priklausomai nuo šaltinio duomenų. Atitinkama X++ klasė yra `WrkCtrScheduler`, kuri turi išvestines klases, skirtas planuojamiems gamybos užsakymams, paskelbtiems gamybos užsakymams ir projektų prognozėms.

Pavyzdžiui, panagrinėkime gana paprastai atrodantį maršrutą, pavaizduotą toliau esančioje lentelėje ir paveikslėlyje.

| Oper. Nr. | Pirmenybė | Nustatymo laikas | Apdorojimo laikas | Laukimo darbo grupėje laikas po | Išteklių kiekis | Paskesnis |
| --- | --- | --- | --- | --- | --- | --- |
| 10 | Pirminis | 1.00 | 2.00 | | 1 | 20 |
| 10 | Antrinis&nbsp;1 | | | | 1 | 20 |
| 20 | Pirminis | | 3.00 | 1.00 | 3 | 0 |

![Pavyzdinio maršruto diagrama](media/scheduling-engine-route.png "Pavyzdinio maršruto diagrama")

Siunčiant į variklį, jis suskirstomas į aštuonias užduotis, kaip parodyta toliau esančiame paveikslėlyje (pasirinkite paveikslėlį, kad jį padidintumėte).

[![Planavimo mechanizmo užduotys](media/scheduling-engine-jobs.png "Planavimo mechanizmo užduotys")](media/scheduling-engine-jobs-large.png)

Įprastinis dviejų užduočių saitas yra `FinishStart` t. y. vienos užduoties pabaigos laikas turi būti ankstesnis nei kitos užduoties pradžios laikas. Kadangi sąranka turi būti atliekama to paties ištekliaus, kuris vėliau vykdys procesą, tarp jų yra `OnSameResource` apribojimų. Tarp 10 pirminės ir antrinės operacijų yra `StartStart` ir `FinishFinish` saitai, o tai reiškia, kad abi užduotys turi ir prasidėti ir baigtis tuo pačiu metu, taip pat yra `NotOnSameResource` apribojimų, neleidžiančių naudoti to paties ištekliaus pirminei ir antrinei operacijai.

Atliekant 20 operaciją, kai nustatytas išteklių kiekis yra 3, proceso užduotis suskirstyta į tris atskiras užduotis, be to, visos užduotys turi būti vykdomos tuo pačiu metu.
Šiuo atveju maršruto grupė buvo nustatyta ne tam, kad rezervuotų pajėgumą eilei pasibaigus laikui, todėl po to esančiai eilei skirta tik viena užduotis.

Planavimo mechanizmas dirba tik su užduotimis ir nedirba su operacijomis. Tai reiškia, kad atliekant operacijų planavimą operacijos taip pat taip yra išskaidomos į užduotis, nors jos nėra saugomos duomenų bazėje.

Kiekvienai užduočiai taip pat nurodysime užduoties pajėgumo poreikį (reikiamą sekundžių skaičių). Atsižvelgiant į tai, kaip buvo nurodyti išteklių poreikiai, kiekvienai užduočiai taip pat gali būti siunčiamas visų galimų išteklių, kurie gali būti naudojami užduočiai vykdyti, ir pajėgumo reikalavimų konkretiems ištekliams sąrašas. Nepaisant to, kad kuriant modelį yra siunčiamas tinkamų išteklių sąrašas, mechanizmas vis tiek turi užtikrinti, kad išteklių priskyrimas yra tinkamas visai užduoties trukmei.

## <a name="scheduling-engine-internals"></a>Planavimo mechanizmo vidinė sandara

### <a name="scheduling-engine-interface"></a>Planavimo mechanizmo sąsaja

Norėdami suprasti vidinę mechanizmo sandarą, geriausia apžvelgti iš išorės prieinamas funkcijas. X++ pagrindinė sąsaja yra `WrkCtrSchedulerEngineInterface`. Ji turi metodus, aprašytus toliau esančiuose poskyriuose.

#### <a name="general-engine"></a>Bendrasis mechanizmas

| **Metodas** | **Paskirtis** |
| --- | --- |
| `run` | Suplanuoja visas įkeltas užduotis ir grąžina klaidos kodą. |
| `getJobSchedulingSequenceResult` | Gaunamas konkrečios užduoties nustatytos sekos planavimo rezultatas ir pirmoji klaidos užduotis. |
| `validateJobCapacityReservations` | Patvirtinami visų mechanizmo saugomų užduočių pajėgumų rezervavimai. |
| `setReservationsTimeStamp` | Į variklį siunčiama laiko žyma, nustatyta mechanizmo atmintinėje suplanuotų užduočių visiems naujiems pajėgumų rezervavimams. |
| `addPropertyToGroupAggregation` | Kai pajėgumai sujungiami, prie naudojamų ypatybių rinkinio pridedamas ypatybės prefiksas. |
| `addResource` | Prie planavimo mechanizmo išteklių telkinio pridedamas išteklius. |
| `addResourceGroup` | Prie planavimo mechanizmo išteklių grupių telkinio pridedama išteklių grupė. |
| `addResourceGroupMembership` | Prie išteklių grupės kaip narys pridedamas išteklius. |
| `addOptimizationGoal` | Pridedamas planavimo optimizavimo tikslas (trukmė arba prioritetas). |

#### <a name="individual-jobs"></a>Atskiros užduotys

| **Metodas** | **Paskirtis** |
| --- | --- |
| `addJobInfo` | Pridedamas užduoties informacijos įrašas, kuris praneša varikliui apie užduotį, kuri turi būti suplanuota. |
| `addConstraintJobEndsAt` | Pridedamas apribojimas, kad užduotis turi baigtis nurodytą dieną ir nurodytu laiku. |
| `addConstraintJobStartsAt` | Pridedamas apribojimas, kad užduotis turi prasidėti nurodytą dieną ir nurodytu laiku. |
| `addConstraintMaxJobDays` | Nurodomas apribojimas, kurį užduotis gali tęstis nurodytą maksimalų dienų skaičių. |
| `addConstraintResourceRequirement` | Pridedamas apribojimas, kad užduotis turi būti suplanuota naudojant tam tikrą išteklių. |
| `addJobBindPriority` | Pridedamas (užduoties, apribojimo lygio) poros užduoties susiejimo prioritetas. Didesnė prioriteto reikšmė reiškia, kad užduoties kintamieji bus susieti anksčiau. Užduotis toje pačioje sekoje bus apdorota prieš užduotis, kurių prioriteto reikšmė yra mažesnė. |
| `addJobCapacity` | Prideda užduoties pajėgumo informaciją (pvz., reikalingą užduoties vykdymo laiką), kuri nepriklauso nuo to, kuris išteklius naudojamas užduoties vykdymui. |
| `addJobResourceCapacity` | Prideda išteklių prie išteklių, kurie gali būti naudojami užduočiai atlikti, rinkinio ir nurodo pajėgumą, kurio reikia, kai vykdymui naudojamas šis išteklius. |
| `addJobGoal` | Prideda užduoties tikslo informaciją konkrečiam apribojimo lygiui (anksčiausias pabaigos laikas arba vėliausias pradžios laikas). |
| `addJobResourcePriority` | Prideda prioritetą, kuris naudojamas planuojant užduotį ištekliuje. |
| `addJobResourceRuntime` | Nurodo užduoties laiką, kuris priklauso nuo ištekliaus, kurs yra suplanuotas užduoties vykdymui. |
| `addJobRuntime` | Nurodo užduoties laiką, kuris nepriklauso nuo ištekliaus, kurs bus suplanuotas užduoties vykdymui. |
| `scheduleJobOnResourceGroup` | Žymi užduotį, skirtą išteklių grupės lygio planavimui. |
| `setJobResourcePreemptionAllowed` | Nustato, ar leidžiama atlikti užduoties, naudojančios išteklių, pertraukiamą (jei mechanizmui leidžiama planuoti užduotį naudojant nenuoseklius pajėgumo intervalus). |
| `setRequiredNumberOfResources` | Nustato išteklių, reikalingų užduočiai planuoti, skaičių (tik operacijų planavimui). |

#### <a name="constraints-between-jobs"></a>Užduočių apribojimai

| **Metodas** | **Paskirtis** |
| --- | --- |
| `addJobLink` | Pridedamas saitas (pvz., pabaiga \>pradžia) tarp dviejų užduočių. |
| `addConstraintEndsDelayed` | Nurodomas apribojimas, kad užduotis negali baigtis prieš kitas užduotis, atsižvelgiant į tam tikrą delsos laiką. |
| `addConstraintJobListWorkingTimeIntersect` | Pridedamas apribojimas, kad, esant dviem užduočių naudojamiems ištekliams, užduotims rezervuoti pajėgumo intervalai turi būti pateikti į susikertančius darbo laikus. |
| `addConstraintJobOverlap` | Pridedamas apribojimas, nurodantis, kaip užduotys išdėstomos, kai nurodytas prekės kiekis gali būti perkeltas tarp dviejų išteklių, o pirmasis išteklius dar nebaigė apdorojimo, kad apdorojimą galėtų pradėti antrasis išteklius. |
| `addConstraintNotOnSameResource` | Pridedamas apribojimas, kad dvi užduotys negali būti suplanuotos naudojant tą patį išteklių. |
| `addConstraintOnSameResource` | Pridedamas apribojimas, kad dvi užduotys privalo naudoti tą patį išteklių. |
| `addJobSameReservations` | Pridedamas apribojimas, kad galutiniai užduoties pajėgumų rezervavimai turi būti tiems patiems laiko intervalams kaip ir pirminės užduoties. |
| `setPrimaryParallelJob` | Pridedama informacija apie tai, kuri užduotis yra pirminė užduotis lygiagrečių užduočių rinkinyje. |

### <a name="solver"></a>Sprendimo priemonė

Pats mechanizmas iš esmės yra specializuota sprendimo su apribojimais priemonė su pridėta specialia euristika. Sprendimo priemonės pagrindą sudaro du pagrindiniai elementai: kintamieji ir apribojimai.

#### <a name="variable"></a>Kintamasis

Kintamasis atitinka galimų verčių sritį. Planavimo mechanizme yra dviejų tipų kintamieji:

- **Datos ir laiko kintamasis** – jo sritis yra visos galimos datos ir laikai, o pačią sritį galima apriboti perkeliant kintamojo apatinę ir viršutinę laiko ribas arčiau viena kitos.
- **Ištekliaus kintamasis** – jo sritis yra galimi ištekliai, o pačią sritį galima apriboti pašalinant išteklius iš sąrašo.

#### <a name="constraint"></a>Apribojimas

Apribojimas taikomas kintamiesiems apribodamas jų sritis, tačiau kartu priklauso nuo kintamųjų, todėl yra suaktyvinamas pasikeitus kintamiesiems. „Apribojimų taikymo“ procesas yra, kai apribojimas atlieka pagrindinę savo funkciją, o tada sėkmingai pateikia rezultatą pagrindinei loginei procedūrai.

Kintamasis laikomas susietu, kai jo negalima apriboti dar labiau. Datos ir laiko kintamojo atveju tai reiškia, kad viršutinė ir apatinė riba sutampa, o ištekliaus kintamojo atveju tai reiškia, kad yra tik vienas atitinkamas išteklius. Kai visi kintamieji yra susieti, sprendimas yra rastas.

### <a name="constraint-levels"></a>Apribojimo lygiai

Kai planavimas vykdomas kaip medžiagų poreikio planavimo (MRP) padengimo etapo dalis, atgalinis užsakymų planavimas bus vykdomas nuo poreikio datos. Tačiau, jei neįmanoma rasti grafiko, kuris prasideda šiandien arba vėliau ir baigiasi prieš poreikio datą, tada planavimo kryptis pasikeis ir planavimas bus vykdomas nuo šiandienos.

Ši pagrindinė verslo taisyklė tvarkoma apribojimus suskirstant į lygius. Jei naudojant aukščiausio lygio apribojimus sprendimo rasti nepavyksta, tada atitinkamo lygio apribojimai yra sumažinami ir bandoma taikyti žemesnio lygio apribojimus. Praktikoje tai reiškia, kad vykdant atgalinį planavimą modelis apims 1 lygį su vėliausio pradžios laiko užduoties tikslais esant maksimalaus pabaigos laiko apribojimui (poreikio data), ir 0 lygį su anksčiausio pabaigos laiko užduoties tikslais esant šiandienos minimalaus pradžios laiko apribojimui.

### <a name="algorithm"></a>Algoritmas

Pagrindiniai mechanizmo algoritmo veiksmai:

1. Suraskite sekas (užduočių grandines), kurias galima spręsti atskirai.
1. Pabandykite surasti pradinį aukščiausio apribojimo lygio sekos sprendimą.
    1. Surikiuokite sekoje esančias užduotis pagal užduoties tikslą ir prioritetus, kad būtų galima surasti pradinę užduotį.
    1. Nagrinėkite užduotis nurodyta tvarka:
        1. Suraskite visus apribojimus, kuriuos reikia pritaikyti, ir atlikite pritaikymo procedūrą.
        1. Jei visi užduoties kintamieji yra susieti, rastas užduoties sprendimas.
        1. Jeigu nepažeidžiant apribojimų nepavyko rasti vieno iš kintamųjų, tada atšaukite kintamojo susiejimą, išbandykite kitą sričiai priklausiančią vertę (ištekliaus kintamajam) ir iš naujo atlikite apribojimo pritaikymo procedūrą.
1. Jei sprendimo nepavyko rasti, visi dabartinio apribojimo lygio apribojimai pašalinami, apribojimo lygis sumažinamas (jei galimi žemesni lygiai) ir sprendimo paieška kartojama su nauju apribojimų rinkiniu.
1. Jei rastas patenkinamas sprendimas, pradedamas optimizavimo etapas, kurio metu bandoma rasti geresnį sprendimą, kol pasibaigs optimizavimui skirtas laikas arba bus išnagrinėti visi išteklių deriniai.

Sprendimo su apribojimais priemonė nėra susijusi su planavimo algoritmo detalėmis. Darbo efektyvumas priklauso nuo įvairių apribojimų apibrėžimo ir jų derinio.

### <a name="determining-working-times"></a>Darbo laiko nustatymas

Didelė mechanizmo (vidinių) apribojimų dalis kontroliuoja darbo laiką ir ištekliaus pajėgumą. Iš esmės tikslas yra išnagrinėti ištekliaus darbo laiko intervalus nuo nurodyto taško nurodyta kryptimi ir rasti pakankamai ilgą intervalą, į kurį galėtų tilpti reikalaujamas užduočių pajėgumas (laikas).

Norint tai padaryti, mechanizmui reikia žinoti ištekliaus darbo laikus. Skirtingai nuo pagrindinių modelio duomenų, darbo laikai yra *įkeliami atidėtai*, o tai reiškia, kad jie įkeliami į mechanizmą pagal poreikį. Priežastis taikyti tokį metodą yra ta, kad dažnai „Supply Chain Management“ darbo laikai yra iš labai ilgo laikotarpio kalendoriaus ir dažniausiai yra daug kalendorių, todėl įkeliamų duomenų apimtis gali būti gana didelė.

Mechanizmo reikalaujama kalendoriaus informacija įkeliama dalimis, naudojant X++ klasės metodą `WrkCtrSchedulingInteropDataProvider.getWorkingTimes`. Užklausa yra skirta tam tikram kalendoriaus ID ir konkrečiam laiko intervalui. Atsižvelgiant į „Supply Chain Management“ serverio atmintinės būseną, kiekvienos iš šių užklausų rezultatas gali būti keli duomenų bazės kvietimai, kurie gali užtrukti (lyginant su gryno skaičiavimo laiku). Be to, jei kalendoriuje yra labai sudėtingų darbo laiko apibrėžimų, apimančių daugelį darbo laiko intervalų per dieną, tai ilgina įkėlimo laiką.

Kai darbo laiko duomenys įkeliami į planavimo mechanizmą, jie saugomi konkretaus kalendoriaus vidinėje atmintinėje, o tai reiškia, kad jei kitos užduotys ar ištekliai naudoja tą patį kalendorių, kitos peržvalgos gali būti atliekamos greitai naudojantis atmintimi. Viena iš prasto efektyvumo priežasčių yra ta, kad kiekvienam ištekliui yra naudojamas atskiras kalendoriaus ID, nes tokiu atveju duomenys reikalaujami kiekvienam kalendoriui, nors kalendorių turinys gali sutapti.

### <a name="finite-capacity"></a>Ribotas pajėgumas

Esant ribotam pajėgumui, darbo laiko intervalai iš kalendoriaus yra padalijami ir sutrumpinami atsižvelgiant į esamus pajėgumų rezervavimus. Šie rezervavimai taip pat yra įkeliami naudojant tą pačią klasę `WrkCtrSchedulingInteropDataProvider`, kurią naudoja kalendoriai, tačiau šiuo atveju naudojamas metodas `getCapacityReservations`. Atliekant planavimą bendrojo planavimo metu, nagrinėjami konkretaus bendrojo plano rezervavimai ir, jei suaktyvinta puslapyje **Bendrojo planavimo parametrai**, taip pat įtraukiami rezervavimai iš patvirtintų gamybos užsakymų. Analogiškai, planuojant gamybos užsakymą, taip pat yra galimybė įtraukti rezervavimus iš esamų suplanuotų užsakymų, nors ši galybė nėra naudojama taip dažnai kaip priešingu atveju.

Naudojant ribotą pajėgumą, planavimas gali užtrukti ilgiau dėl kelių priežasčių:

- Pajėgumo informacijos gavimas iš duomenų bazės yra lėta operacija, o pajėgumo informacijos saugojimas serveryje paprastai nėra toks veiksmingas kaip darbo laikų atveju, nes informacija nėra bendra skirtingiems ištekliams kaip kalendorių atveju.
- Nagrinėjamų darbo laiko intervalų skaičius auga dėl padalijimų, be to, įprastai prieš randant sprendimą turi būti nagrinėjami ilgesni laiko intervalai.
- Baigus planavimą, reikia atlikti nesuderinamų rezervavimų patikrą (daugiau informacijos žr. skyriuje „Lygiagretus planavimo mechanizmų paleidimas“).

### <a name="examining-the-resource-combinations"></a>Išteklių derinių nagrinėjimas

Jei užduoties sekoje yra tik standartiniai `FinishStart` saitai (tai reiškia, kad ji yra paprasta grandinė be šakų), optimalų rezultatą (matomas iš vieno užsakymo, ne visų užsakymų) galima pasiekti ieškant geriausio pirmosios užduoties sprendimo, o tada pereinant prie geriausio kitos užduoties sprendimo paieškos. Geriausias užduoties sprendimas reiškia radimą ištekliaus, kuris gali užtikrinti užduoties pradžios ir pabaigos datą, artimiausią užduoties tikslui (vykdant tiesioginį planavimą, tai reiškia kuo ankstesnę užduoties pabaigos datą), kartu laikantis apribojimų.

Kai yra lygiagrečių užduočių, sprendimo paieška gali apimti skirtingų išteklių derinių nagrinėjimą. Galimų išteklių derinių skaičius priklauso nup susijusių lygiagrečių užduočių galimų išteklių skaičiaus. Ypač tada, kai atliekate atgalinį užsakymo planavimą nuo poreikio datos, gali užtrukti, kol loginė procedūra gaus rezultatą, kad nėra problemos sprendimo, kuris leistų vykdyti lygiagrečias užduotis prieš šiandienos datą, nes tam reikia patikrinti visus derinius, kadangi gali būti išteklių, kurių efektyvumas gali būti didesnis arba gali būti kitas kalendorius, kuris leistų gauti rezultatą. Tai reiškia, kad, jei nebuvo nustatyta skirtojo laiko riba, planavimas bus vykdomas ilgą laiką, kol kryptis bus pakeista į tiesioginę.

Ši kombinatorinė logika taip pat reiškia, kad pridėjus daugiau taikytinų išteklių mechanizmas gali veikti lėčiau. Jei efektyvumo problemų kyla vykdant lygiagrečias operacijas ir atliekant planavimą su neribotais pajėgumais, jas galima iš dalies išspręsti leidžiant maršruto sudarymo įrankiui priimti sprendimą, kuris išteklius turi būti naudojamas, o tada priskirti išteklių tiesiogiai operacijai (nes daugeliu atvejų mechanizmas galiausiai pasirinks tą patį išteklių, todėl galutinis rezultatas bus toks pats).

### <a name="hard-links"></a>Kietieji saitai

Nustačius dviejų užduočių saitą kaip kietąjį, užtikrinama, kad nebūtų laiko intervalo tarp vienos užduoties pabaigos ir kitos darbo pradžios. Tai gali būti labai naudinga, pavyzdžiui, kai metalas yra kaitinamas atliekant vieną užduotį, o tada yra apdorojamas atliekant kitą užduotį ir nėra pageidaujama, kad metalas atvėstų.

Naudojant standartinius minkštuosius saitus ir tiesioginį planavimą, jei maršrutas sudaro paprastą grandinę be šakų, rezultatą galima pasiekti ieškant pirmosios užduoties sprendimo, kuris atitiktų apribojimus, o tada keliaujant grandine ir perduodant pabaigos laiką iš ankstesnės užduoties į kitą užduotį. Jei dabartinei užduočiai nepavyksta rasti pajėgumo, jos pradžios laikas bus perkeliamas toliau, tačiau tai neturės įtakos ankstesnėms užduotims, todėl gali atsirasti tarpų tarp užduočių. Tačiau tam pačiam scenarijui naudojant kietuosius saitus (ypač bendrai su ribotu pajėgumu), tai, kad vienai užduočiai grandinėje nepavyksta rasti pajėgumo, reiškia, kad visos prieš tai suplanuotos užduotys turi būti perkeltos po vieną ir pakartotinis planavimas bus atliekamas kelis kartus. Ypač tais atvejais, kai kelių išteklių apkrova yra didelė, dėl kietųjų saitų gali įvykti grandininė reakcija, kurios metu užduotys darys poveikį viena kitai ir reikės atlikti keletą iteracijų, kol rezultatas stabilizuosis ir bus gautas patenkinamas grafikas.

## <a name="running-scheduling-engines-in-parallel"></a>Lygiagretus planavimo mechanizmų paleidimas

Kai planavimas yra atliekamas kaip bendrojo planavimo dalis, kuriai naudojami pagalbiniai įrankiai, kiekviena bendrojo planavimo pagalbinio įrankio gija taip pat gali perimti gamybos užsakymo planavimo užduotis. Tai reiškia, kad vienu metu galima paleisti kelis planavimo mechanizmus. Nors kelių gijų režimas apskritai labai padeda padidinti efektyvumą, yra tam tikrų funkcinių trūkumų planavimo požiūriu.

Vykdant MRP, visi duotos komplektavimo specifikacijos (KS) lygio gamybos užsakymai yra planuojami pagal poreikio datų seką, t. y. tie užsakymai, kurių poreikio data yra anksčiausia, turi būti suplanuoti pirmiausia ir tokiu būdu turėti didžiausią galimybę gauti atitinkamą ištekliaus pajėgumą. Tačiau tada, kai keli mechanizmai vykdo atranką iš nesuplanuotų užsakymų sąrašo, sekos nebegalima užtikrinti, nes vienas mechanizmas darbą gali baigti greičiau už kitą.

Be to, kai planavimas atliekamas naudojant ribotą pajėgumą ir kai keli mechanizmo egzemplioriai bando suplanuoti užsakymus, kurie potencialiai gali naudoti tuos pačius išteklius tą patį laikotarpį, gali prasidėti konkuravimas. Tokių konkuravimo sąlygų skaičius rodomas lauke **Planavimo konfliktai**, kuris yra bendrojo planavimo retrospektyvos puslapyje. Konfliktų sprendimo logika yra tokia:

- Suplanuokite užsakymą (be blokavimo) ir gaukite pajėgumo rezervavimus.
- Užblokuokite.
- Patikrinkite, ar suplanuotiems ištekliams laiko intervale yra naujesnių pajėgumo rezervavimų.
  - Jei ne, įrašykite pajėgumą ir atblokuokite.
  - Jei taip, atblokuokite ir perplanuokite užsakymą nuo pradžių.

Todėl, kai planavimas atliekamas kelis mechanizmo egzempliorius, rezultatas nėra visiškai apibrėžtas, nes jis priklausys nuo to, kaip veikia gijos.

## <a name="operation-scheduling-performance"></a>Operacijų planavimo efektyvumas

Nors operacijų planavimas yra žinomas kaip apytikslis pajėgumų planavimas, mechanizmo požiūriu, tai gali būti sunkiau išsprendžiama problema, jei naudojamas ribotas pajėgumas, nes šiuo atveju tinkamumui įvertinti reikia daugiau duomenų.

Išteklių grupės pajėgumas priklauso nuo to, kokių ir kiek išteklių yra išteklių grupės nariai. Pati išteklių grupė neturi pajėgumo &mdash; tik tada, kai grupei priklauso ištekliai, ji turės pajėgumą. Kadangi priklausymas išteklių grupei laikui bėgant gali kisti, turi būti vertinamas dienos pajėgumas.

Operacijų planavimo metu išteklių grupės kalendorius naudojamas nustatyti kiekvienos operacijos pradžios ir pabaigos laikus. Tai reiškia, kad išteklių grupės kalendoriuje yra riba, kiek laiko vieną dieną gali būti suplanuota vienai operacijai vienoje išteklių grupėje. Skirtingai nuo konkrečių išteklių kalendoriaus, išteklių grupei nepaisoma kalendoriaus efektyvumo duomenų, nes jie paprasčiausiai atitinka darbo pradžios valandas, o ne faktinį pajėgumą.

Pavyzdžiui, jei išteklių grupės darbo laikas tam tikrą dieną yra nuo 8:00 iki 16:00 valandos, vienos operacijos apkrova išteklių grupei negali būti didesnė nei 8 valandos, nepriklausomai nuo to, koks bendras išteklių grupės pajėgumas yra tą dieną. Tačiau apkrovą gali dar labiau apriboti pasiekiamas pajėgumas.

Skaičiuojant galimą tos pačios dienos išteklių grupės pajėgumą, vertinama visų išteklių, priklausančių išteklių grupei, užduoties planavimo apkrova duotą dieną. Kiekvienai dienai skaičiavimas atliekamas taip:

*Galimas išteklių grupės pajėgumas = Grupės išteklių pajėgumas pagal jų kalendorių &ndash; Grupės išteklių užduoties suplanuota apkrova &ndash; Grupės išteklių operacijų suplanuota apkrova &ndash; Išteklių grupės operacijų suplanuota apkrova*

Skirtuke **Išteklių reikalavimai** maršruto operacijai galima nurodyti išteklių reikalavimus. Tam galima naudoti konkretų išteklių (tokiu atveju operacija bus planuojama naudojant šį išteklių), išteklių grupę, ištekliaus tipą arba vieną ar kelias galimybes, įgūdžius, kursą ar sertifikatą. Nors naudojant visas šias pasirinktis maršruto kūrimas tampa lankstesnis, tai taip pat apsunkina planavimą mechanizmui, nes pajėgumas turi būti vertinamas pagal „ypatybę“ (abstraktus pavadinimas, mechanizme naudojamas galimybėms, įgūdžiams ir pan.).

Išteklių grupės galimybės pajėgumas yra visų išteklių grupės išteklių, apimančių atitinkamą galimybę, pajėgumo suma. Jei grupės išteklius turi galimybę, ji bus įskaičiuojama neatsižvelgiant į tai, kokio lygio pajėgumo reikia.

Atliekant operacijų planavimą, galimas išteklių grupės tam tikros galimybės pajėgumas bus sumažintas, kai ji įkeliama su operacija, kuriai reikia atitinkamos galimybės. Jei operacijai reikalinga daugiau nei viena galimybė, pajėgumas bus sumažintas visoms reikalingoms galimybėms.

Kiekvienai dienai reikalingas skaičiavimas atliekamas taip:

*Galimas galimybės pajėgumas = Galimybės pajėgumas &ndash; Išteklių ir konkrečios galimybės, įtrauktos į išteklių grupę, užduoties suplanuota apkrova &ndash; Išteklių ir konkrečios galimybės, įtrauktos į išteklių grupę, operacijų suplanuota apkrova &ndash; Išteklių grupės, kuriai reikia konkrečios galimybės, operacijų suplanuota apkrova*

Tai reiškia, kad, jei yra tam tikro ištekliaus apkrova, apkrova įtraukiama į išteklių grupės galimo pajėgumo pagal galimybę skaičiavimą, nes tam tikro ištekliaus apkrova sumažina įnašą į išteklių grupės pajėgumą pagal galimybę, neatsižvelgiant į tai, ar tam tikro ištekliaus apkrova yra susijusi su konkrečia galimybe. Jei apkrova yra išteklių grupės lygyje, ji yra įtraukiama į išteklių grupės galimo pajėgumo pagal galimybę skaičiavimą tik tada, kai apkrova kyla iš operacijos, kuriai reikia konkrečios galimybės.

Prieš tai aprašyta logika yra komplikuota, nes ji yra tokia pati kiekvienam „ypatybės“ tipui ir todėl vykdant operacijų planavimą su ribotais pajėgumais reikia įkelti didelį kiekį duomenų.

## <a name="viewing-scheduling-engine-input-and-output"></a>Planavimo mechanizmo įvesties ir išvesties peržiūra

Norėdami gauti tam tikrą informaciją apie planavimo proceso įvestį ir išvestį, įjunkite registravimą nueidami į **Organizacijos administravimas \> Sąranka \> Planavimas \> Planavimo sekimo centras**.

Šiame puslapyje, veiksmų srityje pirmiausia pasirinkite **Įjungti registravimą**. Tada paleiskite gamybos užsakymo planavimą. Baigus, sugrįžkite į puslapį **Planavimo sekimo centras** ir veiksmų srityje pasirinkite **Išjungti registravimą**. Atnaujinkite puslapį ir tinklelyje bus rodoma nauja eilutė. Pasirinkite naują eilutę ir veiksmų srityje pasirinkite **Atsisiųsti**. Tada gausite suglaudintą .zip aplanką su šiais failais:

- **Log.txt** – tai žurnalo failas, kuriame aprašomi veiksmai, kuriuos atlieka mechanizmas. Nors jis yra sudėtingas ir gali būti didelės apimties, tačiau, kai eksperimentuojate su maršruto sąranka, norėdami išspręsti efektyvumo problemas, pirmiausia pasižiūrėkite į laiko skirtumą tarp pirmosios ir paskutinės eilučių, nes tokiu būdu galėsite sužinoti tikslų laiką, kurį dirbo planuoklė.
- **XmlModel.xml** – jame yra modelis, sukurtas naudojant X++, kuriuo remiasi mechanizmas. Faile naudojamas `JobId` yra susijęs su `RecId` iš šaltinio lentelės, kurioje yra užduotys ( `ReqRouteJob` arba `ProdRouteJob`). Šiame faile patikrinkite, ar datos, nurodytos `ConstraintJobStartsAt` ir `ConstraintJobEndsAt`, yra tokios, kokių laukiama, ar `JobGoal` ypatybė yra tinkamai nustatyta ir ar užduotys yra tarpusavyje susietos `JobLink` apribojimais.
- **XmlSlots.xml** – jame yra visi darbo laikai ir pajėgumo rezervavimai, kurių reikalavo variklis. Mechanizmas reikalaus kalendoriaus darbo laikų ir rezervavimų tik laikotarpiams, kuriems mėgina planuoti užduotis (kartu su papildomu buferiu), todėl jei į failą yra įtraukti toli į ateitį nutolę laikai, tai gali reikšti sąrankos problemą. Kiekvienam ištekliui `ResourceProperty` mazguose bus matoma, su kokiomis ištekių grupėmis ir galimybėmis bei kuriais laikotarpiais jis yra susijęs.
- **Result.xml** – jame yra planavimo procedūros rezultatas.

Atkreipkite dėmesį, kad sekimo funkcija gali žymiai padidinti apkrovą, todėl ją naudokite tik nagrinėti konkrečių užsakymų planavimui kontroliuojamomis aplinkybėmis. Jei ji įjungta atliekant bendrąjį planavimą, ji greitai pasieks dydžio ribą ir sustos.

## <a name="troubleshooting-performance"></a>Efektyvumo trikčių šalinimas

Kaip galima suprasti iš visų prieš tai esančių skyrių, kalbant apie sąranką ir planavimo mechanizmo naudojimą, yra tam tikrų aplinkybių, kurios gali lemti efektyvumo problemas. Sprendžiant tokias problemas galima naudoti toliau pateiktą kontrolinį sąrašą. Svarbu įvertinti visus punktus, nes dažniausiai problemų kyla dėl įvairių veiksnių derinio.

### <a name="performing-scheduling-as-part-of-mrp-when-it-is-not-needed"></a>Planavimas vykdomas kaip MRP dalis, kai tai nėra būtina

Nepaisant to, kad maršrutai naudojami gamybos kontrolės tikslais, pvz., įkainojimui ir ataskaitoms, jie gali būti nebūtini vykdant MRP. Kai kuriais atvejais planavimui gali pakakti prekei nurodyto standartinio gamybos vykdymo laiko. Norėdami išjungti maršruto planavimą, nustatykite nulinę pajėgumo laiko ribą. Jei planavimą reikia vykdyti, pajėgumo laiko ribą reikia nustatyti atsargiai, nes gali būti nebūtina įvertinti maršrutų taikant visos MRP apimties laiko ribą.

Atkreipkite dėmesį, kad jei užsakymas nėra suplanuotas MRP, jį reikės suplanuoti suplanuoto užsakymo patvirtinimo metu. Tai reiškia, kad patvirtinimo procesas užtruks ilgiau, todėl, atsižvelgiant į tai, kiek siūlomų suplanuotų užsakymų yra patvirtinami, nauda dėl didesnio MRP efektyvumo gali būti prarasta patvirtinimo metu.

### <a name="route-with-unnecessary-operations"></a>Maršrutas su nereikalingomis operacijomis

Kuriant maršrutą, gali kilti noras bandyti modeliuoti realų pasaulį su visais gamybos proceso veiksmais. Nors tai gali būti naudinga kai kuriais atvejais, tai nėra gerai efektyvumo požiūriu, nes modelis, su kuriuo turi dirbti mechanizmas tampa didesnis (užduočių ir apribojimų požiūrių), be to, atliekant užduočių ir pajėgumų rezervavimų įterpimą bei atnaujinimą bus vykdoma daugiau SQL sakinių. Be to, tai turi poveikį galiausiai pateikiant atskaitas apie užduočių eigą, kurį galima sumažinti naudojant automatinį skelbimą. Jei duomenys nėra naudojami iš viso, sukuriama nereikalinga apkrova.

Rekomenduojame sukurti tik tokias operacijas, kurių būtinai reikia planavimui (paprastai tai yra ribojantys ištekliai) ir (arba) įkainojimui. Arba sugrupuokite daug mažesnių atskirų operacijų į vieną didesnę operaciją, kuri atitinka didesnę proceso dalį.

### <a name="many-applicable-resources-for-an-operation"></a>Operacija su daugeliu galimų išteklių

Galimų operacijos išteklių skaičius nustatomas pagal išteklių reikalavimus, nurodytus operacijos ryšyje. Reikalavimas gali būti taikomas konkrečiam (atskiram) ištekliui arba jis gali būti pagrįstas ištekliaus priklausomumu išteklių grupei arba galimybei.

Jei planavimas nėra atliekamas naudojant ribotą pajėgumą ir visi galimi ištekliai turi tą patį kalendorių ir pasižymi tuo pačiu efektyvumu, planavimo mechanizmas visada operacijai parinks tą patį išteklių, tačiau tik tada, kai prieš tai išbandys visus galimus išteklius, kad patikrintų, ar nėra geresnio. Tokiu atveju planavimo apkrovą galima žymiai sumažinti operacijai visada priskiriant tam tikrą išteklių maršruto kūrimo metu.

### <a name="route-with-parallel-operations"></a>Maršrutas su lygiagrečiomis operacijomis

Lygiagrečios operacijos (pirminės / antrinės) yra galingas įrankis, kurį galima naudoti modeliuoti scenarijams, kai, pavyzdžiui, įrenginys ir operatorius yra būtini tam tikrai užduočiai atlikti, tačiau jos taip pat yra daugelio efektyvumo problemų priežastis. Jei konkretaus atskiro ištekliaus reikalavimas kartu priskiriamas pirminei ir antrinei operacijai, dažniausiai tai nėra problema. Tačiau jei yra daug galimų išteklių kiekvienai iš operacijų, tai žymiai padidina skaičiavimo sudėtingumą planuojant.

Užduot naudojus lygiagrečias operacijas galima modeliuoti „virtualių“ išteklių poras (kurios atitiks komandą, kuri operacijoje visada yra kartu) arba vienos iš operacijų paprasčiausiai galima nemodeliuoti, jei ji nėra ribojanti.

### <a name="route-with-quantity-of-resources-higher-than-1"></a>Maršrutas, kurio išteklių kiekis yra didesnis už 1

Jeigu nustatytas operacijai reikalingų išteklių kiekis yra didesnis už vienetą, tada rezultatas bus toks pats kaip naudojant pirmines / antrines operacijas, nes mechanizmui siunčiamos kelios lygiagrečios užduotys. Tačiau šiuo atveju nėra galimybės naudoti konkrečius ištekliaus priskyrimus, nes kiekiui, kuris yra didesnis už vienetą, reikia, kad operacijai būtų taikomas daugiau nei vienas išteklius.

### <a name="excessive-use-of-finite-capacity"></a>Didelis riboto pajėgumo naudojimas

Norint naudoti ribotą pajėgumą, reikia, kad mechanizmas iš duomenų bazės įkeltų pajėgumo informaciją ir tai gali padidinti skaičiavimo apkrovą, nes bus sunkiau rasti sprendimą, ypač aplinkose, kur išteklių rezervavimas beveik siekia maksimalų pajėgumą. Dėl šios priežasties svarbu atidžiai įvertinti, ar ištekliui tikrai būtina naudoti ribotą pajėgumą ar jis gali būti išnaudojamas virš ribos. Kadangi riboto pajėgumo ištekliai gali skirtis pagal tai, kaip svarbu jų neišnaudoti virš ribos, rekomenduojame ribojimo parinktį ištekliui naudoti kartu su atskira plano „Ribojančių išteklių pajėgumo laiko riba“ verte. Naudojant ribojimo koncepciją galima užtikrinti mažesnę bendrojo riboto pajėgumo laiko ribą.

### <a name="setting-hard-links"></a>Kietųjų saitų nustatymas

Įprastas maršruto saito tipas yra *minkštasis*, o tai reiškia, kad tarp vienos operacijos pabaigos laiko ir kitos operacijos pradžios laiko leidžiamas laiko tarpas. Tokiu būdu gali susidaryti nepageidaujama situacija, kai vienai iš operacijų labai ilgą laiką neturint medžiagų arba pajėgumų, gamyba kurį laika gali vykti tuščiąja eiga, o tai gali reikšti atliekamo darbo apimties padidėjimą. Tai negali įvykti naudojant kietuosius saitus, nes pabaigos ir pradžios laikai turi visiškai sutapti. Tačiau nustačius kietuosius saitus planavimo problema tampa sudėtingesnė, nes dviem operacijų ištekliams reikia skaičiuoti darbo laiko ir pajėgumų sankirtas. Jei kartu atliekamos lygiagrečios operacijos, tai žymiai padidina skaičiavimo laiką. Jei dviejų operacijų ištekliai turi skirtingus kalendorius, kurie iš viso nepersidengia, problema yra neišsprendžiama.

Kietuosius saitus rekomenduojame naudoti tik tada, kai tai yra neišvengiama – kiekvienai maršruto operacijai įvertinkite, ar tai yra būtina.

Norint sumažinti atliekamų darbų apimtį ir nenaudoti kietųjų saitų, užsakymą galima planuoti du kartus, antrąjį kartą pakeičiant kryptį. Jei pirmas grafikas buvo apskaičiuotas atgal nuo pristatymo datos, antrasis turi būti apskaičiuotas į priekį nuo suplanuotos pradžios datos. Tokiu būdu užduočių apimtis bus sumažinta, kiek įmanoma, kad būtų kuo labiau sumažintas atliekamų darbų kiekis.

### <a name="separate-calendar-for-each-resource"></a>Atskiras kiekvieno ištekliaus kalendorius

Vienas iš pagrindinių planavimo mechanizmo duomenų šaltinių yra kalendoriaus informacija, kurios įkėlimui iš duomenų bazės gali reikėti daug išteklių. Kadangi kalendoriai yra generuojami remiantis šablonais, gali kilti noras generuoti kalendorių kiekvienam ištekliui ir tada koreguoti šio kalendoriaus informaciją, kai ištekliaus negalima naudoti arba kyla kitų problemų. Tačiau tai labai riboja mechanizmo galimybę kaupti kalendoriaus duomenis, nes kiekvienam ištekliui reikės naujų duomenų, o tai gali būti rimta efektyvumo problemų priežastis. Užuot tai darius, rekomenduojame, kiek įmanoma, ištekliams naudoti bendrus kalendorius, o tada kontroliuoti prastovų pakeitimus laikotarpiui priskiriant kitą kalendoriaus ID.

### <a name="high-number-of-working-time-slots-per-calendar-day"></a>Didelis darbo laiko intervalų skaičius per dieną kalendoriuje

Kadangi mechanizmas veikia po vieną pagal pajėgumą nagrinėdamas laiko intervalus, naudinga kuo labiau sumažinti kalendoriaus dienos laiko intervalų skaičių. Tai galima padaryti, pavyzdžiui, nusprendžiant, ar svarbu, kad gautame grafike būtų atsižvelgta į tai, kad darbuotojai kas valandą turi 5 minučių pertraukėlę.

### <a name="large-or-none-scheduling-timeouts"></a>Ilgas (arba jokio) planavimo skirtasis laikas

Planavimo mechanizmo efektyvumą galima optimizuoti naudojant parametrus, pateiktus puslapyje **Planavimo parametrai**. Parametrų **Planavimo skirtasis laikas įjungtas** ir **Planavimo optimizavimo skirtasis laikas įjungtas** reikšmė visada turi būti **Taip**. Jei reikšmė yra **Ne**, planavimas gali vykti be galo, jei sukurtas prastas maršrutas su daugeliu galimybių.

**Maksimalus planavimo laikas sekai** reikšmė nurodo, kiek sekundžių gali būti skirta bandymui rasti vienos sekos sprendimą (daugeliu atvejų seka atitinka vieną užsakymą). Čia pateikta reikšmė labai priklauso nuo maršruto sudėtingumo ir tokių parametrų kaip ribotas pajėgumas, tačiau maksimali 30 sekundžių reikšmė gali būti geras pradinis pasirinkimas.

**Optimizavimo bandymų skirtasis laikas** reikšmė nurodo, kiek sekundžių gali būti skirta rasti sprendimui, kuris yra geresnis už rastą prieš tai. Tai turės įtakos tik maršrutams, kurie naudoja lygiagrečias operacijas, nes joms būtina išbandyti skirtingus derinius.

> [!NOTE]
> Nustatytos skirtojo laiko reikšmės bus taikomos paskelbtų gamybos užsakymų ir suplanuotų užsakymų planavimui, kuris yra MRP dalis. Todėl nustačius labai dideles reikšmes gali žymiai pailgėti MRP vykdymo laikas, jei vykdomas planas su daugeliu suplanuotų gamybos užsakymų.
