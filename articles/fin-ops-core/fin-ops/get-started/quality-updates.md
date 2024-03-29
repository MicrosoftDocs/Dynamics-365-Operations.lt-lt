---
title: Iniciatyvūs kokybės atnaujinimai
description: Šiame straipsnyje pateikiama informacija apie iniciatyvų kokybės naujinimų pristatymą.
author: rashmansur
ms.date: 11/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: ecfeb3e6c5760b526ade609ee38f83da083b34d2
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805320"
---
# <a name="proactive-quality-updates"></a>Iniciatyvūs kokybės atnaujinimai

[!include[banner](../includes/banner.md)]

Per keletą paskutinių metų Microsoft toliau truko tai, ką vadiname viena [versija](../../dev-itpro/lifecycle-services/oneversion-overview.md). Vienos versijos patalpos yra paprastos: kuo arčiau visų klientų gauti tą pačią programinės įrangos versiją, tuo aukštesnė kokybės, kurią galime pristatyti. Surandame ir ištaisome problemas vieną kartą, ir šiuos sprendimus naudojame daugiau klientų.

Šias patalpas patvirtina rezultatai: mažesnis incidentų skaičius mūsų produktuose. Kai klientai nėra toje pačioje versijoje, kreipkite dėmesį, kad jiems daro poveikį problemos, dėl kurių sprendimas jau galimas. Mes jau atlikome daug darbo su "Dynamics 365 Finance", "Dynamics 365" Dynamics 365 Project Operations Dynamics 365 Commerce tiekimo grandine ir dėkojame už naujausią techninio progresą, dabar galima pereiti prie kito veiksmo. Ši informacija pateikia daugiau informacijos, ką ketiname daryti, ką jau padarėme, norėdami nustatyti etapą ir kaip ir kada mes pristatome naujus pajėgumus be klaidos.

## <a name="what-you-need-to-know"></a>Ką reikia žinoti

- Proactive kokybės atnaujinimai taikomi kas mėnesį.
- "Microsoft" taiko aktyvius kokybės naujinimus bet kuriai sandų [dėžės](./public-preview-releases.md#targeted-release-schedule-dates-subject-to-change) aplinkai, kurioje vykdomas tarnybos naujinimas, kuris buvo naudojamas sukūrus aktyvius kokybės naujinimus.
- Klientų, kurie yra reguliuojami JAV maisto ir vaistų administracijos (FDA), išankstinės kokybės naujinimų išimtys bus leidžiamos.
- "Microsoft" nustato, kaip bus valdomi aktyvi kokybės atnaujinimai reguliuojams aplinkai ir vyriausybės debesies klientams.
- Pranešimai, susiję su aktyviais [Microsoft 365](https://admin.microsoft.com/AdminPortal/) kokybės atnaujinimais Microsoft Dynamics , registruojami pranešimų centre ir kliento ciklo tarnybų projekto dalyje.
- Klientams pranešama, kad atnaujinimas bus pritaikytas praėjus penkioms dienoms iki tada, kai bus taikomas aktyvus kokybės atnaujinimas.
- Klientai negali atšaukti arba atidėti aktyvių kokybės naujinimų.
- Aktyvūs kokybės naujinimai įdiegiami per regionui buotą suplanuoto [priežiūros langą](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).
- Kokybės atnaujinimai yra inžinieriai, kuriems žema problemų ar regresijų rizika, ir tai palaiko Microsoft duomenys.
- "Microsoft" rekomenduoja kryptingus konkrečių problemų arba konkrečių karštųjų pataisų, susijusių su aktyviu kokybės naujnimu, kryptingus bandymus.

## <a name="focus-on-quality-updates"></a>Aktyvinti kokybės naujinimus

Šiuo metu mes teikiame septynis [tarnybos naujinimus](public-preview-releases.md) per metus. Pavyzdžiui, 10.0.29 versija yra tarnybos atnaujinimas. Iki šiol buvo aštuoni atnaujinimai per metus. Tačiau mes numetėme vieną atnaujinimą, atsakydami į klientų grįžtamąjį ryšį, kuris išvengė noro išvengti pakeitimų iki kalendorinių metų pabaigos.

Mes nepasikeičiame aptarnavimo naujinimų kadastros. Vietoj to, mūsų kitas žingsnis į priekį vienos versijos žingsnyje daug dėmesio skiriama *kokybės naujams*. Kokybės naujinimai yra kaupiamieji karštųjų pataisų versijos. Jose nėra naujų funkcijų. Bet kuriuo metu mūsų visa klientų bendruomenė yra paskirstyta tarp trijų ar keturių naujausių aptarnavimo naujinimų. Tačiau bet kokiam pateiktam aptarnavimo atnaujinimų tuzinai skirtingų kokybės naujinimo versijų gali būti naudojami grupėje, atsižvelgiant į žmonių įdiegti datas. Sekame žingsnyje aktyviai išsiuntinsime kokybės atnaujinimus. Mes jau naudojame šį modelį mūsų Dataverse programoms ir gavome tikėtinus rezultatus, nes pagerėja jo kokybė ir sumažėja palaikymo incidentai.

Žinoma, defektų sumažinimas gali sumažinti arba visiškai panaikinti kokybės atnaujinimų poreikį. Mes naudojame kelias iniciatyvas skrydžio metu, kad sumažinsime defektus, kuriuos reikia atnaujinti. Net jei kokybės naujinime sumažinami mokami kroviniai, klientų sistemos vientisumas pagerina palaikymo galimybes, greičiau pagerins klientus ir sumažins klientų, susiduriančių su jau esamais sprendimais, dažnumą.

## <a name="making-proactive-distribution-possible"></a>Galimas aktyvus paskirstymas

Jau įdiegti keli išankstiniai avansai, kurie įgalina išankstinį kokybės naujinimų pristatymą:

- **Beveik nulinis downtime atnaujinimas**  – norėdami stumyti daugiau dažnesnių aplinkoje, būtina sumažinti poveikį aplinkos pasiekiamumui, kad būtų išlaikomos "Dynamics 365" paslaugų lygio sutartys (SLA). Iš pradžių buvo įdiegtas beveik nulinis prasto laiko atnaujinimas, siekiant padėti pagerinti mėnesinį operacinės sistemos pataisų tobulinimą, naudojant klasterio rinkmenų permetimą, kad atnaujintas vaizdas būtų aktyvinamas šiek tiek vėliau. Naujinimų taikymo mechanizmas yra patobulintas, kad jis dar mažiau nutrikdytų ir apimtų operacinės sistemos pataisų ir kokybės atnaujinimo diegimą.

    Interaktyviems vartotojams aktyvus seansas gali būti pertrauktas, o kartojimo programa pereis į dabar atnaujintą aplinką. Įdiegus prioritetinį [paketinį planavimą, paketinis](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md) planavimas ir apdorojimas atsistato ir tęsiami iškart po atnaujinimo. Prioritetinis paketinis planavimas bus skirtas klientams, prieš jiems pradedant dalyvauti proaktyvioje savo gamybos aplinkose kokybės naujinimų paskirstyme.

- **Tamsos**  valandos – tamsesnės valandos nustatomos kiekvienam "Azure" regionui ir beveik nulinis downtime atnaujinimas bus naujuose valandų laikotarpiu.

## <a name="the-proactive-update-process"></a>Iniciatyvaus atnaujinimo procesas

Aktyvių kokybės atnaujinimų diegimas bus po saugaus diegimo proceso (SDP). SDP specifikos gali keistis, tačiau kokybės atnaujinimai iš pradžių bus įdiegti į sandbox aplinkas. Sėkmingai įdiegtos sanddės padidėjimo procentinė dalis, bus pradėtas diegti gamybos aplinkose. Klausymo sistemos bus stebimi sistemos telemetikos ir seniausios versijos incidentai, o jei aptinkama kokia nors regresija, sustabdys konkrečios versijos iškliaumą. Jei reikia, klientai vis dar galės gauti kokybės naujinimus anksčiau už iniciatyvų diegimą.

Dabartiniai paleidimo valdymo duomenys rodo, kad į kokybės atnaujinimus įtraukta mažiau nei 3 procentai regresijų. Kuo daugiau dėmesio bus skiriama regresijos pašalinimui ir išplėstiniam SDP, galimas regresijų poveikis bus atitinkamai mažesnis nei kokybės pelnas, kurį pasieks daug greičiau gaunant klientams įdiegtas pataisas.

## <a name="process-changes"></a>Keitimų apdorojimas

Proceso pakeitimų rinkinys įgyvendintas prieš suaktyvinus aktyvią kokybės naujinimo įdiegtį:

- **Schema**  – įrankis užtikrina, kad kokybės naujinimo versijos apima tik schemos pakeitimus, kurie gali būti taikomi paslaugai internete. Šis būdas padės išlaikyti galimybę taikyti atnaujinimą beveik nulinio nulio laiku.
- **Padidintas pakeitimas –**  šiuo metu yra papildomas proceso žingsnis, skirtas patvirtinti įtraukimo į kokybės naujinimą pakeitimus. Papildomas veiksmas bus padidintas, kad būtų sumažintas galimas regresijų potencialas. Kokybės naujinimų pakeitimai negali būti atlikti, todėl padidintas keitimų skaičius padės užtikrinti, kad šį tikslą atitiksime.
- **Matomumas**  – pranešimai siunčiami per administratoriaus centrą, ciklo tarnybas ir kitus galimų kanalų, kad būtų galima atnaujinti būsimus aktyvius kokybės naujinimus. Be to, palaikymo komandos ir galimi klientai galės matyti, kur sėkmingai įdiegti kokybės atnaujinimai.

    > [!NOTE]
    > "Microsoft Communications" komanda ištirti, kaip vyksta el. pašto įrankių sistema, kuri neleidžia pristatyti el. paštu siunčiamų pranešimų. Tęskite pranešimų centro Microsoft 365 , kad jis būtų rodomas ir pateikiamas su pranešimais susijęs pranešimas.

- **Nepavyksta saugiai per skrydžio**  – skrydžio metu bus naudojamas kodui keisti bet kada, kai tai taikoma kokybės atnaujinimo klaidai taisyti arba naudoti esamą funkciją, susijusią su pataisa. Jei po aktyviai diegimo reikia atsarginio ar išjungimo keitimo, jį galima atlikti naudojant skrydžio sistemą, kad būtų išvengta tolimesnių trikčių.
- **Sandbox sinchronizavimo**  paskirtis – mažiau nei 20 procentų klientų šiuo metu turi keletą sanddėlių ir kad viena sandbox būtų įdiegta ten, kur versija atitinka gamybą, kad būtų padedama šalinti triktis. Jei klientas naudoja sandbox, kad galėtų patikrinti naujesnę versiją, o ne jų gamybą, tą sandinę bus gauti tos naujesnės versijos kokybės naujinimai.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Koks kokybės naujinimų iškeitimų kokybės atnaujinimas?

Numatyta, kad "Azure" viešų debesies klientų aktyvių kokybės naujinimų paskirstymas bus pradėtas 2022 m. spalio pabaigoje arba spalio mėn. Tuo metu bandomoji aplinka taip pat pradės gauti iniciatyvų naujinimo diegimą. Rugsėjo mėnesį bus išsiųstas pranešimas kiekvienam klientui, informuos apie numatomą jų aplinkos grafiką. Proactive atnaujinto paskirstymo proceso išimtys bus leidžiamos tik FDA reguliuojamųjų klientų. Mes vis dar veikiame, kaip bus valdomos reguliuojamos aplinkos ir vyriausybės debesies klientai bei vyriausybės debesies klientai.

Per kitą šešių mėnesių laikotarpį palaipsniui didinsime sandbox aplinkos, kurios gauna aktyvius naujinimus, procentą, kol visos nustatytos aplinkos bus įtrauktos ir vykdoma gamybos aplinkos atnaujinimo eiga. Visu laikotarpiu stebėsime, kaip užtikrinti, kad diegimo procesas būtų nuoseklias ir kad mes atsveiksime savo nenuosklandinių mokamųjų krūvių tikslą.

Kadangi klientai reguliariai gaus mažesnius mokėjimo krūvius, tikitės, kad dabartinis procesas taps paprastesnis. Mes koreguosime atnaujinimo diegimo dažnumą, nes pademonstruosime galimybę vykdyti procesą be jokios galimybės. Šis procesas jau efektyviai veikia mūsų platformai Dataverse ir programoms ir pateikia numatomus paslaugų kokybės patobulinimus. Norime atlikti tą patį žingsnį į priekį ir finansų, ir operacijų programoms.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Kada bus pradėti gamybos aplinkos kokybės naujinimai?
Šiuo metu kokybės atnaujinimai yra tik tiksliniai sand. langeliai. Mes atnaujinsime šią vietą gamybos aplinkos pradžios data, kai bus daugiau konkrečių duomenų ir metrikos iš aktyvių sandėlio atnaujinimų ir nustatyti gamybos pasirengimą.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Koks sandėlio aktyvių kokybės naujinimų grafikas?
Norėdami gauti informacijos apie tamsaus regiono valandas, žr. [Kokie yra suplanuoti priežiūros langai pagal regioną](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows)?

### <a name="proactive-quality-update-release-10028"></a>Aktyvus kokybės naujinimo paleidimas: 10.0.28
**Programos versija: 10.0.1265.89**  
**Atitinkamas naujausias žinių bazės straipsnis: 745340**

| Stotis | Regionai | Baigtas grafikas| Būsimų sand. dėžių grafikas
|---|---|---|---|
| 1 stotis | Kanados centrinis centras, Kanados rytų, Prancūzijos centrinis bankas, Indijos centras, Norvegijos rytų, Šveicarijos West | Nuo 2022 m. rugsėjo 15 d. iki rugsėjo 18 d., nuo rugsėjo 19 d. iki 2022 m. rugsėjo 22 d. ir spalio 7 d. – 2022 m. spalio 10 d. | 2022 m. spalio 25 d. iki spalio 28 d. |
| 2 stotis | Prancūzijos Pietų, Indijos Pietų, Norvegijos West, Šveicarijos Šiaurės, Pietų Afrikos Šiaurės, Australijos Rytų, UK Pietų, JAE Šiaurės, Japonijos Rytų, Australijos Pietų Rytų, Pietų Rytų Azijos | Nuo 2022 m. rugsėjo 25 d. iki rugsėjo 28 d. ir 2022 m. spalio 7 d. – spalio 10 d. | 2022 m. spalio 25 d. iki spalio 28 d. |
| 3 stotis | Rytų Azijos, UK West, Japan West, Brazilijos Pietų, West Europe, Rytų JAV, JAE centrinis centras | Nuo 2022 m. rugsėjo 26 d. iki rugsėjo 29 d. ir 2022 m. spalio 7 d. – spalio 10 d. | 2022 m. spalio 25 d. iki spalio 28 d. |
| 4 stotis | Šiaurės Europa, Centrinė JAV, West US | Nuo 2022 m. spalio 28 d. iki spalio 1 d. ir spalio 7 d. iki 2022 m. spalio 10 d. | 2022 m. spalio 25 d. iki spalio 28 d. |
| 5 stotis | Dod, Vyriausybės bendruomenės debesis, Kinija | Nesuplanuota | Nesuplanuota |

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a> Aktyvus kokybės atnaujinimo paleidimas: 10.0.29
**Programos versija: 10.0.1326.70**  
**Atitinkamas naujausias žinių bazės straipsnis: 750332**

| Stotis | Regionai | Baigtas grafikas | Būsimų sand. dėžių grafikas|
|---|---|---|---|
| 1 stotis | Kanados centrinis centras, Kanados rytų, Prancūzijos centrinis bankas, Indijos centras, Norvegijos rytų, Šveicarijos West | Spalio 14 d. iki 2022 m. spalio 17 d., lapkričio 2 d. iki 2022 m. lapkričio 5 d. ir lapkričio 13 d. | Gruodžio 5 d.–gruodžio 8 d.|
| 2 stotis | Prancūzijos Pietų, Indijos Pietų, Norvegijos West, Šveicarijos Šiaurės, Pietų Afrikos Šiaurės, Australijos Rytų, UK Pietų, JAE Šiaurės, Japonijos Rytų, Australijos Pietų Rytų, Pietų Rytų Azijos | 2022 m. spalio 15 d. iki spalio 18 d., lapkričio 2 d. iki 2022 m. lapkričio 5 d. ir lapkričio 13 d. | Gruodžio 5 d.–gruodžio 8 d.|
| 3 stotis | Rytų Azijos, UK West, Japan West, Brazilijos Pietų, West Europe, Rytų JAV, JAE centrinis centras | 2022 m. spalio 16 d. iki spalio 19 d., lapkričio 2 d. iki 2022 m. lapkričio 5 d. ir lapkričio 13 d. | Gruodžio 5 d.–gruodžio 8 d.|
| 4 stotis | Šiaurės Europa, Centrinė JAV, West US | 2022 m. spalio 17 d. iki spalio 20 d., lapkričio 2 d. iki 2022 m. lapkričio 5 d. ir lapkričio 15 d. | Gruodžio 5 d.–gruodžio 8 d.|
| 5 stotis | Dod, Vyriausybės bendruomenės debesis, Kinija | Nesuplanuota | Nesuplanuota |

### <a name="proactive-quality-update-release-10030"></a><a name="schedule"></a> Aktyvus kokybės atnaujinimo paleidimas: 10.0.30
**Programos versija: 10.0.1362.77 atitinkamas**
**naujausias žinių bazės straipsnis: 767597**

| Stotis | Regionai | Būsimų sand. dėžių grafikas |
|---|---|---|
| 1 stotis | Kanados centrinis centras, Kanados rytų, Prancūzijos centrinis bankas, Indijos centras, Norvegijos rytų, Šveicarijos West | 2022 m. gruodžio 1 d.–gruodžio 4 d. |
| 2 stotis | Prancūzijos Pietų, Indijos Pietų, Norvegijos West, Šveicarijos Šiaurės, Pietų Afrikos Šiaurės, Australijos Rytų, UK Pietų, JAE Šiaurės, Japonijos Rytų, Australijos Pietų Rytų, Pietų Rytų Azijos | 2022 m. gruodžio 2–gruodžio 5 d. |
| 3 stotis | Rytų Azijos, UK West, Japan West, Brazilijos Pietų, Šiaurės Europa, Rytų JAV, JAE centrinis centras | 2022 m. gruodžio 3–gruodžio 6 d. |
| 4 stotis | West Europe, Central US, West US | 2022 m. gruodžio 4 d.–gruodžio 7 d. |
| 5 stotis | Dod, Vyriausybės bendruomenės debesis, Kinija | Nesuplanuota |

> [!IMPORTANT] 
> "Microsoft" iš anksto per penkias dienas atnaujins ankstesnį planą ir siųs pranešimą apie aplinkos rinkinį, kurį numatyta gauti šiuos kokybės naujinimus. Ankstesnis grafikas taikomas tik aplinkai, kuri buvo paskelbta apie būsimą atnaujinimą. Norėdami gauti informacijos apie tamsaus regiono valandas, žr. [Kokie yra suplanuoti priežiūros langai pagal regioną](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows)?
>
> Kiekvienoje regiono grupėje ar *stotis*, kurioje šiuo metu planuojama atlikti kokybės naujinimą, grafike pateikiamas keturių dienų intervalas. Kokybės naujinimai bus pradėti tik naudojant sand. dėžės aplinkas. Tada, sėkmingai įdiegtos sandų dėžės padidėjimo procentinė dalis, diegimas į gamybos aplinką pradės nuo išankstinių pranešimų klientams.
> 
> Kokybės atnaujinimai visada bus diegiami slenkantis taip, kad įgalintų mus pasiekti aplinkos rinkinį pagal grafiką ir iki ketvirtos stoties dienos pabaigos užbaigti visus rinkinius. Tačiau tai nereiškia, kad aplinkos atnaujinimas truks keturias dienas. Tai tik reiškia, kad negalime iš anksto nustatyti, kuris aplinkos rinkinys bus atnaujinamas nurodytą dieną per keturių dienų diapazoną. Visi naujinimai bus atlikti tamsomis valandomis, kai bus naudojamas beveik nulinis downtime. Atnaujinimai pereis į tam tikrą regioną tam tikrą tam tikrą tamsos valandų langą.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Kaip klientų, kurie turi vieną finansų ir operacijų programėlių egzempliorių, bet kurie aktyvūs keliose laiko juostose, tamsos valandos tvarkomos? 
Nėra specialiųjų grafikų už tamsų valandų ribų, kur yra finansų ir operacijų programėlių egzempliorius, [nes mes planuojame įdiegti kokybės atnaujinimus minimaliai netrikdant n ŠIANDIENos veiksmų](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean).

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>Koks yra dabartinis išleisto kokybės atnaujinimo cadence?
Proactive quality updates (PQUs) šiuo metu yra siunčiami vieną kartą per mėnesį kiekvienai palaikomai tarnybos naujinimo versijai. Per mėnesį siunčiamas tik vienas pasirinktų sandų dėžės aplinkos naujinimas(-ų), nebent klientai pereina prie naujos tarnybos naujinimo versijos. Tokiu atveju jie gali gauti iš anksto suplanuotą PQU kaip esamo traukinyes dalį naujai paslaugai atnaujinti. Po to, kai 2023 m. baigiamas pasaulinis išbaigimas, šių atnaujinimų dažnumas didės. Kai tik bus pakeisti siuntimo cadence, jūs visada gausite bent vieno mėnesio įspėjimą.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Kaip "Microsoft" užtikrins šių naujinimų kokybę?
"Microsoft" pagal tai, kad paleidimo pardavimo galimybės būtų pakankamai efektyvios, kad būtų galima pristatyti smulkius mokančius komponentus, kad tikrinimo išlaidos būtų mažos. Kiekvienas kokybės atnaujinimo pataisas pereina per daug saugių ir saugių diegimų procesą, kuris padeda pagerinti kokybę ir patikimumą bei sumažina klientų įtaką. Diegimas bus vyksta etapais sandų dėžės aplinkose, po to – gamyboje. Diegiant į etapus leidžiama tinkamai stebėti, ar tolesnis diegimas yra saugus. Sustabdysime keitimų stabdymą, jei aptinkama problemų, aptiktų kiekvienoje įdiegtų klientų grupėje, ir užtikrinsime, kad kiekvienas iš sustabdytų veiksmų turi pakankamai laiko norint išmesti problemas. Būsimiems kokybės naujinimams mes suteiksime matomumą grafike atnaujindami viešus dokumentus ir el. laiškus, kad klientai galėtų planuoti ateities planus.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Ar klientai gali atidėti, perplanuoti ar pristabdyti kokybės atnaujinimą?
Ne. Pagrindinis kokybės atnaujinimo tikslas yra užtikrinti pagrindinius reikalavimus, pvz., saugą, privatumą, patikimumą, prieinamumą ir efektyvumą, nuolat tobulinti savo klientus. Atidedama arba prisilaikant atnaujinimą, saugą, prieinamumą ir patikimumą bus rizikuojama.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>Kaip žinoti, koks pakeitimų rinkinys nuėjo į kokybės atnaujinimo mokamąjį krūvį?
Norėdami nustatyti pakeitimų, kurie įtraukti į kokybės atnaujinimo mokaąją apkrovą, sąrašą, atlikite toliau aprašytus veiksmus. 

Naudokite 10.0.28 kokybės naujinimo traukinys ir susijusią programos 10.0.1265.89.

1. Ciklo tarnybose atidarykite sandėlio **aplinkos** informacijos puslapį. 
2. Skyriuje Galimi **naujinimai pasirinkite** Rodyti naujinimą **, kad būtų galima** naudoti naujausią kokybės naujinimo versiją. 
3. Eksportuoti versiją į CSV arba Microsoft Excel failą.
4. Eksportuotoje rinkmenoje filtruokite ir pasirinkite versiją **Kurti,** kuri yra mažesnė arba lygi versijos 10.0.1265.89. Dabar turėtumėte matyti pokyčių mokamatį.
 
> [!NOTE]
> Prieš atnaujinant aplinką reikia eksportuoti į CSV arba Excel failą. Kitu atveju galite naudoti aplinką, kurios konfigūracija panaši, bet neįdiegtas naujinimas, ir atlikite nurodytus veiksmus.

[![Aplinkos su kokybės naujnimu pavyzdys.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Koks procesas, jei po kokybės atnaujinimo randama kritinė problema?
Kritinis išdavimas ar regresija yra vienas ar daugiau įvykių, dėl kurių keli klientai įprastai patiria vieno ar kelių paslaugų naudojimo patirtį. Dėl šių problemų gali atsirasti nesuplanuotų prasto laiko, įskaitant netinkamumą, našumo pereiimą ir aptarnavimo valdymo perėjimą. Jei dėl tokių atgalinių keitimų kyla labai svarbus klientas, sustabdysime kokybės atnaujinimo atnaujinimą, kol sugalėsime palaikyti ryšį ir išspręsti problemą. Paprastai tolesnis kokybės atnaujinimas turės reikiamą pataisą, kad būtų galima ištęsti.

Jei paveikiama vieno kliento aplinka, susisiekite su Microsoft pagalbos tarnyba, kad atidarytumėte bilietą. Remiantis pagrindimu, mes sustabdysime kokybės atnaujinimo išbaigimą visoms kitoms to projekto aplinkai, kol išdavimas bus sumažintas.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lifecycle-services"></a>Ar klientai vis dar gali rankiniu būdu taikyti karštųjų pataisų naujinimus iš ciklo tarnybų?
Taip. Kad būtų užtikrintas tebevykdęs lygumas su karštųjų pataisų darbu, vis tiek galima taikyti karštųjų pataisų naujinimus klientų aplinkose ciklo tarnybose. Tačiau svarbu pažymėti, kad karštosios pataisos, kurios įdiegtos kaip kokybės naujinimo dalis, pereis per standartinį SDP prieš įdiegiant naujinimą. Dėl to dėl aukštesnio kokybės sumažėja regresijų rizika. Rekomenduojame pasirinkti kokybės naujinimą rankiniu būdu taikant karštąsias pataisas, kad būtų padidintas patikimumas.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Ar klientai gali aktyviai įdiegti kokybės naujinimą anksčiau už grafiką?
Taip. Galite įdiegti kokybės naujinimą proaktyviai. "Microsoft" praleis atnaujinimą, jei dabartinė aplinkos versija yra lygi arba didesnė už šį kokybės naujinimą.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Jei aplinkoje yra suplanuotų mėnesio paslaugų atnaujinimo per savaitę, ar vis tiek bus gauti kokybės atnaujinimai?
- Kokybės naujinimai nepritaikyti gamybos aplinkai, jei savaitei nuo tada, kai suplanuotas kokybės atnaujinimas, planuojamas planuojamas numatomas paslaugos atnaujinimas.
- Jei sandbox aplinkoje yra ta pati arba naujesnė versija nei laukiantis kokybės naujinimas, ji bus praleista.
- Jei gamybos aplinkos versija yra ta pati arba naujesnė nei laukiamas kokybės atnaujinimas, ji bus praleista.
- Jei dėl kokybės atnaujinimo arba neautomatinio gamybos atnaujinimo sanddėlyje yra ta pati arba naujesnė versija, gamyba vis tiek gaus suplanuotą mėnesinio tarnybos naujinimo versiją. Jei nenorite, kad suplanuotos gamybos aplinka būtų atnaujinta į tarnybos naujinimo versiją, galite pristabdyti tarnybos naujinimą iš ciklo tarnybų. 
- Rekomenduojame naudoti naujausią kokybės naujinimo versiją, kad būtų patikrinti būsimų tarnybos naujinimų pakeitimai, siekiant užtikrinti geresnį stabilumą ir rezultatus.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Jei aplinkoje yra suplanuotas būsimas veiksmas ir suplanuotas kokybės atnaujinimas tame pačiame priežiūros lange, ar vis tiek bus gauti kokybės atnaujinimas?
Jei yra turinio su iš anksto suplanuotu veiksmu, pavyzdžiui, taškų atkurkite laiką (PITR), kokybės atnaujinimas bus perplanuotas prie kito galimų priežiūros lango keturių dienų lange. Daugiau informacijos apie grafiką ieškokite Kas [yra aktyvių kokybės naujinimų grafikas?](#schedule) 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Ar galima aplinką grąžinti į ankstesnę būseną, jei pritaikius kokybės naujinimą kyla problemų?
Kai taikomas kokybės atnaujinimas, jokiais atvejais nėra keitimų atšaukimo. Yra tik pataisos persiuntimo pasirinktys, kurios gali sumažinti problemas.

## <a name="what-about-fda-regulation-and-gxp"></a>Kaip dėl FDA reglamento ir GxP?
Klientų, kuriems taikomas FDA tikrinimas ir taisyklės, planas dar tebėra taikomas. Greit tikimasi daugiau šios vietos naujinimų. Dabar visi tokie klientai atleidžiami nuo kokybės naujinimų. Norėdami užtikrinti, kad klientui taikomi FDA taisyklės, apsilankykite [Microsoft Azure GxP siūlymas](/azure/compliance/offerings/offering-gxp).

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Kokios tarnybos naujinimų versijos palaikomos šiems kokybės naujinams?
Visų palaikomų tarnybos naujinimų versijos klientai gali gauti kokybės naujinimus. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retail-sdk"></a>Diegiant finansų ir operacijų programas su "Retail" komponentais, be MPOS pakartotinio diegimo, paprastai reikia papildomo darbo. Kaip šie kokybės naujinimai turės įtakos mažmeninės prekybos SDK? 
Kadangi pačios karštųjų pataisų pobūdis nepasikeičia kokybės naujinimų mokamoji pataisa, mes nesitikite jokios papildomos įtakos, konkrečiai susijusios su "Retail" komponentais.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Ar yra koks nors poveikis debesies nuomojamoms aplinkai (CHE)? 
CHE aplinkos nepatenka į kokybės naujinimų aprėptį, nes jos nepatenka į "Microsoft" įvertinimą.

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Ar yra integravimo problemų Microsoft Dataverse? 
Nėra jokių žinomų integravimo problemų, susijusių su kokybės atnaujinimais Dataverse.

