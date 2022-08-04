---
title: Atsargų padėties valdymas
description: Šiame straipsnyje pateikiama informacija apie strateginį atsargų padėties žymėjimo procesą, apimantį atšiupimo taškų identifikavimą jūsų tiekimo grandinėje, kur galima sukurti turimų atsargų atsargas, siekiant padėti glaudinti gamybos laiką ir suglaudinti programos į jūsų tiekimo grandinę.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ReqGroup, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: bec36b5b51b937782afdb78d7009a58dcd0942f0
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186594"
---
# <a name="inventory-positioning"></a>Atsargų padėties valdymas

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Strateginių atsargų padėties nustatymas apima iššišiavimo taškus jūsų tiekimo grandinėje, kur galima sukurti turimų atsargų atsargas. Šis būdas dažniausiai naudojamas padėti glaudinti gamybos laiką ir amortizuoti jūsų tiekimo grandinę. Tai leidžia sumažinti "nepavykusį" poveikį, nes poreikio nuokrypis nėra pereina visą tiekimo grandinės būdą. (Gamybos *poveikis* nurodo, kaip maži poreikio svyravimai mažmeninės prekybos lygiu gali progresyviškai padidinti poreikio svyravimus didmeninio pardavimo, platintojo, gamintojo ir žaliavų tiekėjų lygiuose.)

Atsargų padėties planavimas yra pirmasis poreikio turimo medžiagų išteklių planavimo (DDMRP) žingsnis.

## <a name="inventory-positioning-for-manufacturing"></a>Gamybos atsargų padėties valdymas

Šiame skyriuje pateikiamas pavyzdys, kuriame parodyta, kaip priimti atsargų padėties nustatymo sprendimus, jei pagaminote įprastą įprastą produktą. Šis vekselis turi kelių lygių komplektavimo specifikaciją (KS), kaip parodyta toliau pateiktame pavyzdyje.

![Pavyzdys: kelių lygių komplektavimo specifikacija (KS), skirta produktui.](media/ddmrp-bom-example.png "Pavyzdys: kelių lygių komplektavimo specifikacija (KS), skirta daugkartinių produktų")

### <a name="choose-your-decoupling-points"></a>Pasirinkite savo iššiuosite taškus

Pasirinkdami, kur padėti savo iššiuos taškus, apsvarstykite visus šiuos kiekvienos KS prekės aspektus, kaip kriterijus:

- Išorinis nuokrypis
- Atsargų svertas ir lankstumo
- Kritinė operacijos apsauga
- Leistino kliento nuokrypio laikas
- Pardavimo užsakymo matomumo laikotarpis
- Rinkos potencialus gamybos laikas

Toliau pateiktame pavyzdyje galite nurodyti savo pirmąjį atsišiejimo tašką į *skyriaus* važtaraščius dėl šių priežasčių:

- Yra sunku šaltinio medžiagoms, kurios naudojamos, kad būtų sukurti važtaraščiai, o pasiekiamumas – pagal tai. Todėl laikomasi *išorinio nuokrypio* kriterijaus.
- Dienos važtaraščius galima perpjauti į daug skirtingų formų ir dydžių, kad būtų galima kurti ir kitų jūsų gaminamų produktų, ne tik to, kas buvo gaminama, įterpimo formą. Todėl yra laikomasi *atsargų sverto ir* lankstumo kriterijaus.

Tada galite padėti kitą iššišiavimo tašką medžiagos *rinkinyje*, kuris yra iš anksto iškirpta audinio dalis. Galite pasirinkti šį tašką, nes turite tik vieną medžiagos pjaustymo mašiną. Todėl laikomasi kritinio *operacijos* apsaugos kriterijaus.

Galiausiai paskutinį atsiejimo tašką galite padėti į baigtą prekę. Galite pasirinkti šį tašką, nes *pardavimams* skirtas labai žemas leistinas kliento nuokrypio laikas, *o jūsų pardavimo užsakymo matomumo* perspektyva yra gana trumpa. Todėl norite užtikrinti, kad turite turimų atsargų, kad jos atitiktų gaunamus užsakymus. Taip pat galite nustatyti didesnę kainą, išlaikydami gamybos laiką šį trumpą laiką, *į kurį rinkos potencialaus gamybos laiko* kriterijus nurodo.

Pagal šią analizę toliau pateikta iliustracija rodo, kaip atrodys kS. Geltonai atsargų simboliai išryškina iššiltavimo taškus.

![KS su išryškintu atsiejimo taškais pavyzdys.](media/ddmrp-bom-decoupling-example.png "KS su išryškintu atsiejimo taškais pavyzdys")

### <a name="calculate-your-decoupled-lead-time"></a>Apskaičiuoti iš anksto susietą gamybos laiką

Šiame skyriuje rodoma, kaip skaičiuoti savo naujus gamybos laikus po to, kai buvo pateikti atsiejimo taškai.

Toliau pateiktame pavyzdyje, pavyzdžiui, kuris buvo pradėtas ankstesniame skyriuje, gamybos laikas rodomas pilkose dėžėse, viršutinėje kairėje kiekvieno KS komponento pusėje. Langeliai, kurie turi raudoną struktūrą, nurodo prekes, kurios veikia kaupiamąjį gamybos laiką (ilgiausio gamybos laiko kiekviename KS lygyje suma). Šis gamybos laikas yra 21 diena, kai pradedate nuo pradžių.

![KS su gamybos laiku pavyzdys.](media/ddmrp-bom-lead-times-example.png "KS su gamybos laiku pavyzdys")

Tačiau jei taikysite anksčiau pasirinkote iššifravimo taškus, atsietos prekės visada bus atsargose. Todėl jų gamybos laikas bus 0 (nulis). Naujas gamybos laikas dabar yra tik penkios dienos: dvi dienos gijos pirkimui ir trys dienos, per kelias dienas pagaminti klientą. Šis gamybos laikas vadinamas išjungtu *gamybos laiku*.

![Atsietos gamybos laiko pavyzdys.](media/ddmrp-bom-decoupled-lead-time-example.png "Atsietos gamybos laiko pavyzdys")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>Strateginių atsargų padėties kūrimas mažmeninės prekybos modelyje

Kadangi mažmenininkai atsargose yra tik baigti produktai, KS nėra išdavimas. Tačiau mažmenininkai vis dar gali naudoti DDMRP nustatydami strateginių atsargų padėties ir buferio lygius, remdami paskirstymo tinklo saugojimo vietas.

Šiame pavyzdyje pateikiamas įmonės, kuri turi paskirstymo centrą Sietle, ir parduotuvių, parduotuvių, parduotuvių Oflande, Atlantoje ir Portlande, pavyzdys.

![Atsiejimo taškai, pagrįsti mažmeninės prekybos modelio vieta.](media/ddmrp-retail-decoupl-points-example.png "Atsiejimo taškai, pagrįsti mažmeninės prekybos modelio vieta")

Galite nuspręsti *, kad perkėlimo laikas, per kurį bus perkeliamas bendras produktas tarp paskirstymo centro ir parduotuvių, pažeidžia jūsų leistino kliento nuokrypio laiką*, nes jūsų klientai tikisi, kad po apsilankymo bendras produktas bus atsargose. Tokiu atveju, kiekvienoje iš trijų parduotuvių turėsite nustatyti bendrą prekę atsiejimo tašką. Kiekviena parduotuvė turės skirtingus buferio lygius, atsižvelgiant į gamybos laiką, poreikio modelius ir t. t.

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>Vykdyti atsargų padėties poziciją Dynamics 365 Supply Chain Management

Šiame skyriuje aprašoma, kaip įdiegti savo atsargų padėties nustatymo strategiją programoje "Microsoft"Dynamics 365 Supply Chain Management.

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>Nustatyti prekių padengimo grupes, kurios sukuria atsiejimo taškus

Prekės tampa iššifigūravimo **taškais**, kai jos priklauso padengimo grupei, kuri yra sukonfigūruota su atsiejimo taško padengimo *kodo verte*. Todėl pirmasis DDMRP nustatymo proceso žingsnis yra nuspręsti, kurias padengimo grupes turite įdiegti savo DDMRP strategijai, tada sukurti jas atlikdami šiuos veiksmus.

1. Pasirinkite **Bendrasis planavimas \> Sąranka \> Padengimas \> Padengimo grupės**.
1. Norėdami sukurti padengimo grupę **, veiksmų** srityje pasirinkite Naujas.
1. Įvesti informaciją, identifikuojanę padengimo grupę, ir pasirinkti naudotinį kalendorių.
1. Skirtuke **Bendra** nustatykite padengimo kodo **lauką** kaip Iššiavimo *tašką*. Dėl šio parametro visos šiai padengimo grupei priklausančios prekės bus laikomos DDMRP atsiejimo taškais. Taip pat įgalina visus šios grupės DDMRP parametrus, kaip aprašyta toliau šioje procedūroje.
1. Skirtuke **Kita**, **DDMRP parametrų skyriuje**, nustatykite šiuos laukus:

    - **Gamybos laiko koeficientas** – nurodykite koeficientą (kaip dešimtainę vertę nuo 0 iki 1), kad būtų galima valdyti gamybos laiko poveikį, kai skaičiuojamas šios padengimo grupės prekių mažiausias ir didžiausias atsargų lygis. Apskritai, kuo ilgesnis prekės gamybos laikas, turėtų būti mažesnis prekės gamybos laiko koeficientas. Kai gamybos laiko koeficientas yra mažesnis nei minimalus ir didžiausias atsargų lygis, dėl to užsakymai būna mažesni ir dažnesni. DDMRP metodologija rekomenduoja vertę nuo 0,20 iki 0,40 prekėms, kurių gamybos laikas ilgas, nuo 0,41 iki 0,60 ir prekėms, kurių gamybos laikas yra vidutinis, ir nuo 0,61 iki 1,00 prekių, kurių gamybos laikas trumpas. Daugiau informacijos rasite buferio [profilyje ir lygiuose](ddmrp-buffer-profile-and-levels.md).
    - **Nuokrypio koeficientas** – nurodykite koeficientą (kaip dešimtainę vertę nuo 0 iki 1), kad būtų galima valdyti poveikį, kurį kintantis poreikis turi turėti, kai skaičiuojamas mažiausias šios padengimo grupės prekių atsargų lygis. Apskritai, kuo daugiau kintamųjų yra prekės poreikis, kuo didesnis prekės nuokrypio koeficientas. Kuo didesnis nuokrypių koeficientas, lemia aukštesnį minimalų atsargų lygį. DDMRP metodologija rekomenduoja prekių, kurių nuokrypis yra mažas, vertę nuo 0,00 iki 0,40, o prekių, kurių nuokrypis yra didelis, – nuo 0,41 iki 0,60, arba nuo 0,61 iki 1,00. Daugiau informacijos rasite buferio [profilyje ir lygiuose](ddmrp-buffer-profile-and-levels.md).
    - **Min., maks. ir pakartotinio užsakymo taškų laikotarpis** – nurodykite, kaip dažnai apskaičiuoti buferio vertes (*Kasdien arba* *Kas savaitę*).

1. Skirtuko Kita **skyriuje** Vidutinis kasdienis **naudojimas** nustatykite šiuos laukus:

    - **Vidutinis kasdienis naudojimas,** pagrįstas – pasirinkti, kuriais laikotarpiais turi būti pagrįstas vidutinio kasdienio naudojimo (ADU) skaičiavimas. Pasirinkite vieną iš šių reikšmių:

        - *Praeitis* – peržiūrėkite tik praeities naudojimą, kiek dienų nurodytas lauke **Praeities laikotarpis (** dienos). ADU apskaičiuojamas kaip bendras prekės poreikis skaičiavimo laikotarpiu (atsargų vienetais), padalintas iš skaičiavimo laikotarpio dienų skaičiaus.
        - *Pirmyn* – pažiūrėkite tik būsimą dienų skaičiaus, nurodyto lauke Pirmyn (**dienos), naudojimą (įskaitant prognozes**). ADU apskaičiuojamas kaip bendras prekės poreikis skaičiavimo laikotarpiu (atsargų vienetais), padalintas iš skaičiavimo laikotarpio dienų skaičiaus. 
        - *Mišrus* – pažiūrėkite ir praeities, ir būsimą naudojimą. Praėjusi laikotarpio **(dienų) lauko**, laikotarpio **pirmyn (dienų) lauko ir** derinimo pasirinkčių visos yra taikomos. 

            *Mišrusis ADU* = (buvusio\[*svoriu* × *ankstesnis ADU*\] + \[*toliau* × *ADU*\]) ÷ (toliau *·* + *svorius svorius)*

    - **Ankstesnis laikotarpis (dienos)** – įveskite praeities dienų (iki šios dienos ir aprėpties) skaičių, į kurį sistema turi atsižvelgti skaičiuojant šios padengimo grupės prekių ADU. Šis parametras taikomas tik tada, kai **nustatytas vidutinis kasdienis** naudojimas, remiantis lauku *, yra nustatytas į Praeitis* arba *Mišrus*.
    - **Ateities laikotarpis (dienomis)** – įveskite būsimų dienų skaičių (nuo šiandien iki nurodytos dienos), į kurį sistema turi atsižvelgti skaičiuodama šios padengimo grupės prekių ADU. Šis parametras taikomas tik tada, kai **vidutinis kasdienis naudojimas**, remiantis lauku, nustatytas į *Pirmyn* arba *Mišrus*.
    - **Santykinis praėjusio laikotarpio svoris**, naudojamas kartu naudojant vidutinį dienos naudojimą – įveskite svorį (kaip procentą), kuris bus taikomas praėjusiu laikotarpiu, kai skaičiuojamas kartu apskaičiuotas ADU. Šis parametras taikomas tik tada, kai **vidutinis kasdienis naudojimas,** remiantis lauku, nustatytas kaip *Mišrus*.
    - **Santykinis į priekį** laikotarpio svoris, naudojamas maišyto vidutinio kasdienio naudojimo metu – įveskite svorį (kaip procentą), kuris turi būti taikomas į priekį laikotarpiui, kai skaičiuojamas maišusis ADU. Šis parametras taikomas tik tada, kai **vidutinis kasdienis naudojimas,** remiantis lauku, nustatytas kaip *Mišrus*.

1. Visuose kituose skirtukuose ir laukuose įveskite išsamius parametrus, naudojamus prekių, kurios susietos su šia padengimo grupe, reikalavimams apskaičiuoti.

### <a name="set-an-item-as-a-decoupling-point"></a>Nustatyti prekę kaip iššiavimo tašką

Norėdami nustatyti prekę kaip iššišiavimo tašką, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Suraskite ir pasirinkite išleistą prekę, kurią norite nustatyti DDMRP.
1. Veiksmų srities skirtuke Planas **pasirinkite** Prekės **padengimas**.
1. Prekių padengimo **puslapyje** gali būti pateikti keli prekių padengimo įrašai, kiekvienas iš jų taikomas skirtingoms saugojimo ir produkto dimensijų kombinacijoms. Galite pasirinkti esamą prekės padengimo įrašą, kuris taikomas dimensijoms, kur norite sukurti iššipimo tašką. Taip pat galite veiksmų srityje pasirinkti **Naujas**, kad sukurtumėte naują prekės padengimo įrašą.
1. Nustatykite prekių padengimo įrašą kaip įprasta. Reikia nurodyti vietą ir sandėlį, kur bus taikomas iššišiavimo taškas.
1. Kol dar pasirenkamas atitinkamas įrašas, pasirinkite skirtuką **Bendra**.
1. Pažymėkite žymės **langelį Naudoti konkrečius** parametrus.
1. Padengimo **grupės lauką** nustatykite padengimo grupei, kuri nustatyta kurti atsišiejimo taškus (kaip aprašyta ankstesniame skyriuje).
1. Prekė konfigūruota kaip iššiavimo taškas. Paprastai, naudodami DDMRP, taip pat konfigūruosite čia parametrus, kurie turės įtakos buferio dydžiui ir užsakymo kiekiui. Vis dėlto konfigūraciją galima baigti kurti vėliau. Daugiau informacijos apie nustatymus ieškokite atsiejimo [taško prekės buferių nustatymas](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

> [!NOTE]
> Norėdami planuoti prekes, kurios nėra atsiejamos taškais, atlikite tuos pačius veiksmus, kuriuos turite atlikti naudodami standartinių medžiagų poreikių planavimą (MRP).
