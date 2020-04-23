---
title: Bendrojo planavimo nustatymas
description: Šioje temoje aprašomos įvairios svarbios strategijos ir parametrai, naudojami norint nustatyti bendrąjį planavimą.
author: t-benebo
manager: tfehr
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 7b6b4cb1c3035e8341928562c447b03affd40167
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213566"
---
# <a name="set-up-master-planning"></a>Bendrojo planavimo nustatymas


[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos įvairios svarbios strategijos ir parametrai, naudojami norint nustatyti bendrąjį planavimą. Joje apžvelgiami planų tipai, naudojami bendrojo planavimo metu, ir paaiškinama, kurią plano strategiją naudoti, atsižvelgiant į jūsų verslo poreikius. Joje taip pat apibūdinami pagrindiniai parametrai, kurie įtakoja planą, ir paaiškinama, kaip šie parametrai įtakoja suplanuotus užsakymus, kurie yra siūlomi.

## <a name="types-of-master-plans"></a>Pagrindinių planų tipai

Bendrojo planavimo metu galima pasirinkti du planų tipus: statinį ir dinaminį. Kiekvienas tipas sukurtas naudoti skirtingu tikslu. Siekiant didžiausio našumo, rekomenduojame naudoti planą, tinkamą jūsų scenarijui.

### <a name="static-plan"></a>Statinis planas

Statinis planas lieka nepakitęs, nepriklausomai nuo tiekimo ir poreikio pokyčių, kol bus vykdomas kitas bendrasis planavimas.

Statinis planas naudojamas patvirtinti ir įtvirtinti siūlomus užsakymus. Tai veikiantis planas, kurį įvairus įmonės personalas, pavyzdžiui, pirkėjų arba gamybos planuotojas, gali naudoti savo sprendimams pagrįsti ir kasdienėms užduotims atlikti.

Statinis planas taip pat palaiko regeneravimą. Visiškai naujas optimizuotas planas apskaičiuojamas kiekvieną kartą, kai vykdomas bendrasis planavimas, ir panaikinami jau patvirtinti esami užsakymai.

### <a name="dynamic-plan"></a>Dinaminis planas

Dinaminis planas paprastai pradedamas kaip statinio plano kopija, bet jis gali būti atnaujinamas kaskart, kai pasikeičia pagrindiniai duomenys. Pavyzdžiui, jei duomenys pasikeičia, sukuriamas naujas pardavimo užsakymas.

Dinaminis planas naudojamas vykdant ad hoc planavimą. Tai įmonei suteikia galimybę stebėti kintančią užsakymo struktūrą ir prekių prieinamumą, netrikdant statinio plano, kurį kiti naudoja savo darbo procesams. Jis ypač dažnai naudojamas tvarkant galimas pateikti atsargas (CTP). Dinaminis planas yra numatytasis planas, kai grynieji poreikiai atidaromi iš užsakymo puslapių (pvz., pardavimo užsakymo, pirkimo užsakymo ar gamybos užsakymo puslapių).

Dinaminis planas naudoja grynąjį pokytį. Todėl jis padeda užtikrinti spartesnį vykdymo laiką.

## <a name="strategies-for-using-master-plans"></a>Bendrojo plano naudojimo strategijos

Bendrojo planavimo metu galite naudoti vieną arba du planus. Strategija, kurią naudosite, priklauso nuo jūsų verslo poreikių.

### <a name="one-plan-strategy"></a>Vieno plano strategija

Norėdami naudoti vieno plano strategiją, naudokite tą patį bendrąjį planą, skirtą statiniam planui ir dinaminiam planui. Ši strategija naudojama „iš gamybos į atsargas“ scenarijuose, kuriuose paprastai nereikia modeliuoti plano, kuris vykdo užsakymo.

Vieno plano strategija paprastai naudojama mažmeninės prekybos ir paskirstymo pramonėse arba kai pardavimo pristatymo datos yra patvirtinamos pagal aptarnavimo lygio sutartis (SLA) ar gamybos laiką. Plano pristatymo datos valdiklis gali būti naudojamas be CTP.

Jei turite atlikti modeliavimą, iš naujo galima paleisti planą, skirtą prekėms, kurias reikia modeliuoti. Suplanuoti užsakymai, kuriuos kuria užsakymų modeliavimas, paprastai yra patvirtinti.

### <a name="two-plan-strategy"></a>Dviejų planų strategija

Dviejų planų strategijoje naudojamas statinis planas ir kitas dinaminis planas. Dviejų planų strategija paprastai naudojama „konfigūravimo į užsakymą“ ir „gamybos į užsakymą“ scenarijuose, kai reikia atlikti pardavimo užsakymų modeliavimą ir apskaičiuoti tikslias pardavimo užsakymų pristatymo datas, tačiau skaičiavimai neturi įtakoti kasdienių operacijų. Šie modeliavimai visuomet atliekami naudojant dinaminį planą. Pavyzdžiui, dviejų planų strategija naudinga automobilių ir originalios įrangos gamintojų (OEM) pramonėse.

Dviejų planų strategijos pristatymo datos valdiklio CTP gali būti naudojamas. Naudojant CTP, jis automatiškai įjungia dinaminio plano vykdymą.

### <a name="setting-up-the-plans"></a>Planų nustatymas

Planus galite kurti puslapyje **Bendrieji planai** (**Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**).

Galite nurodyti, kurie planai bus naudojami statiniame plane ir dinaminiame plane nustatydami laukus **Dabartinis statinis bendrasis planas** ir **Dabartinis dinaminis bendrasis planas** puslapyje **Bendrojo planavimo parametrai** (**Bendrasis planavimas \> Sąranka \>Bendrojo planavimo parametrai**). Norėdami naudoti vieno plano strategiją, laukuose **Dabartinis statinis bendrasis planas** ir **Dabartinis dinaminis bendrasis planas** pasirinkite tą patį planą.

## <a name="types-of-planning-methods"></a>Planavimo metodų tipai

Gali būti naudojami trys skaičiavimo metodai bendrajam planavimui vykdyti: regeneravimas ir grynasis pokytis. Kiekvienas metodas pateikia kitą planą, kai jis vykdomas.

Planavimo metodas nurodomas dialogo lange **Bendrojo planavimo vykdymas**. Norėdami atidaryti šį dialogo langą, pasirinkite **Bendrasis planavimas \> Bendrasis planavimas \> Vykdyti \> Bendrasis planavimas** arba pasirinkite **Vykdyti** darbo srityje **Bendrasis planavimas**.

### <a name="regeneration"></a>Regeneravimas

Regeneravimo planavimo metodas panaikina esamus suplanuotus užsakymus, nebent jie patvirtinti. Jis generuoja naujus suplanuotus užsakymus pagal visus poreikius. Regeneravimas yra vienintelis planavimo metodas, skirtas statiniams planams.

- Atsižvelgiama į tiekimo pakeitimus. Šie pakeitimai apima prognozės pakeitimus.
- Šis metodas atsižvelgia į **laikotarpio** padengimo kodą.
- Šis metodas palaiko produkto pakeitimo funkciją (PI).

### <a name="net-change"></a>Grynasis pokytis

Grynojo pokyčio planavimo metodas sugeneruoja suplanuotus užsakymus, kad būtų patenkinti poreikiai, sukurti arba pakeisti po paskutinio bendrojo planavimo vykdymo. Kai vykdomas šis metodas, į tiekimo pakeitimus neatsižvelgiama. Sistema neatsižvelgia į naujas atsargas, o anksčiau sukurti suplanuoti užsakymai nėra panaikinami, jei jų nebereikia. Grynojo pokyčio planavimo metodas vykdomas sparčiau nei regeneravimo metodas. Jis taikomas tik dinaminiams planams.

- Atnaujinami visų poreikių veiksmų ir ateities datos.
- Šis metodas neatsižvelgia į **laikotarpio** padengimo kodą.
- Šis metodas neįvykdo prognozės, net jei ji pasirinkta plane.
- Šis metodas nepalaiko produkto pakeitimo funkcijos (PI).

### <a name="net-change-minimized"></a>Sumažintas grynasis pokytis

Sumažinto grynojo pokyčio planavimo metodas sugeneruoja suplanuotus užsakymus, kad būtų tik patenkinti poreikiai, sukurti arba pakeisti po paskutinio bendrojo planavimo vykdymo. Priešingai nei grynojo pakeitimo metodas, naudojant šį metodą veiksmų datos ir būsimos datos atnaujinamos tik naujuose arba pakeistuose poreikiuose. Šis planavimo metodas galimas tik dinaminiuose planuose.

## <a name="types-of-scheduling-methods"></a>Planavimo metodų tipai

Kiekvieno plano puslapio **Bendrieji planai** „FastTab“ **Bendra** (**Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**) turite pasirinkti gamybos užsakymuose naudojamą planavimo metodą. Gamybą galite planuoti operacijos lygiu ir darbo lygiu.

### <a name="operations-scheduling"></a>Operacijų planavimas

Galite naudoti operacijų planavimą, norėdami bendrai įvertinti gamybos procesą per tam tikrą laikotarpį. Operacijų planavimo metu maršruto gamybos operacijos neišskaidomos į užduotis. Norėdami gauti daugiau informacijos apie operacijų planavimą, žr. [Operacijų planavimas](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling).

### <a name="job-scheduling"></a>Užduočių planavimas

Užduočių planavimas yra išsamesnis planavimo metodas, kuriame kiekviena operacija skirstoma į atskiras užduotis. Užduočių planavimas įtraukia informaciją apie pajėgumą. Užduočių planavimas paprastai naudojamas norint planuoti atskiras darbo laiko užduotis, kurios bus atliekamos iškart arba greitai. Norėdami gauti daugiau informacijos apie užduočių planavimą, žr. [Užduočių planavimas](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="time-fences-in-days"></a>Laiko ribos dienomis

Kiekviename plane galite pasirinkti, kaip tolimoje ateityje įvairūs poreikiai ir kiti veiksniai turi būti skaičiuojami bendrojo planavimo metu. Laikotarpis vadinamas *laiko riba*. Siekiant didžiausio bendrojo planavimo našumo, rekomenduojame pakoreguoti įvairias laiko ribas, kad būtų patenkinti jūsų verslo poreikiai. Kiekviename plane galite rasti laiko ribas puslapio **Bendrieji planai** „FastTab“ **Laiko ribos dienomis** (**Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**).

> [!NOTE]
> Laiko ribos nurodo, kaip tolimoje ateityje įvairūs poreikiai ir kiti veiksniai turi būti skaičiuojami bendrojo planavimo metu. Šiame puslapyje atrinktos laiko ribos perrašys padengimo grupėje nurodytas laiko ribas. Tai reiškia, kad nustačius laiko ribos parinktį Taip ir apibrėžus dienas bus nepaisoma padengimo grupėje nustatytos laiko ribos. Kai nustatytas parametras Ne, laiko riba apibrėžiama padengimo grupėje. Galiausiai, jei nenorite arba neprivalote naudoti parinkties (pavyzdžiui, nenorite naudoti veiksmo pranešimų), nustatykite jos parametrą **Taip**, tada nustatykite laiko ribą į **0** (nulis) dienų.

### <a name="coverage"></a>Padengimas

Padengimo laiko riba nurodo planavimo laikotarpį arba tai, kiek toli į ateitį poreikį reikia įtraukti. Kitaip tariant, ji nurodo planavimo horizontą.

Nustatę parinkties **Padengimas** parametrą **Taip** galite perrašyti bendrojo planavimo metu nustatomą prekės padengimo laiko ribą. Šiuo įveskite dienų, kurias bendrojo planavimo skaičiavimas turėtų padengti poreikius, skaičių. Padengimo laiko ribos skaičiuojamos į priekį nuo šios dienos datos. Anksčiau nei dabartinė data iškilę poreikiai visada bus apdorojami.

> [!NOTE]
> Siekiant didžiausio bendrojo planavimo našumo, rekomenduojame pakoreguoti padengimo laiko ribą pagal savo planavimo horizontą.

### <a name="freeze"></a>Blokuoti

Blokavimo laiko riba nurodo laikotarpį, kurio metu esami suplanuoti užsakymai nėra keičiami, kai vykdomas naujas bendrasis planas. Suplanuoti užsakymai yra blokuojami ir nesiūlomi jokie nauji suplanuoti užsakymai.

Nustatę parinkties **Blokavimas** parametrą **Taip** galite perrašyti bendrojo planavimo metu nustatomą prekės blokavimo laiko ribą. Šiuo atveju įveskite dienų, per kurias įšaldoma planuojama veikla, skaičių. Atminkite, kad šiuo laikotarpiu nauji suplanuoti užsakymai negeneruojami, o esami suplanuoti užsakymai nekeičiami.

### <a name="firming"></a>Patvirtinimas

Tvirtinimo laiko riba nurodo laiko horizontą, per kurį suplanuoti užsakymai automatiškai konvertuojami į gamybos ir pirkimo užsakymus. Šis procesas taip pat žinomas kaip *automatinis suplanuotų užsakymų tvirtinimas*.

Nustatę parinkties **Tvirtinimas** parametrą **Taip** galite perrašyti bendrojo planavimo metu nustatomą prekės tvirtinimo laiko ribą. Šiuo įveskite dienų, per kurias automatiškai patvirtinami suplanuoti pirkimo užsakymai ir suplanuoti gamybos užsakymai, skaičių. Tvirtinimo laiko ribos skaičiuojamos į priekį nuo pagrindinio planavimo datos. Automatinis suplanuoto pirkimo užsakymo tvirtinimas vykdomas tik jei prekė yra susieta su tiekėju.

### <a name="forecast-plan"></a>Prognozės planas

Prognozės plano laiko riba nurodo, kaip toli į ateitį atliekant bendrąjį planavimą sukuriami suplanuoti prekių, kurių poreikis prognozuojamas, užsakymai.

Nustatę parinkties **Prognozės planas** parametrą **Taip** galite perrašyti bendrojo planavimo metu nustatomą prekės prognozės plano laiko ribą. Šiuo atveju įveskite dienų, per kurias prognozės plane esanti pardavimo prognozė turi būti įtraukta į bendrąjį planavimą, skaičių.

### <a name="capacity"></a>Pajėgumas

Pajėgumo laiko riba nurodo, kaip toli į ateitį sistema atsižvelgia į maksimalų jūsų išteklių pajėgumą suplanuodama užsakymus. Kitaip tariant, planas suplanuoja gamybos užsakymus naudodamas prekių gamybos maršrutą, jis atsižvelgia į gamybos maršruto išteklius bei didžiausią kiekvieno ištekliaus pajėgumą.

Nustatę parinkties **Pajėgumas** parametrą **Taip** galite perrašyti bendrojo planavimo metu nustatomą prekės pajėgumo laiko ribą. Šiuo atveju įveskite dienų, per kurias planuojamas suplanuotų gamybos užsakymų pajėgumas, skaičių. Bendrasis planavimas naudoja aktyvų prekės gamybos maršrutą ir planuoja ankstesne nei poreikio data. Jei suplanuoto gamybos užsakymo poreikio data nepatenka į pajėgumo laiko ribas, gamybos laikas nustatomas, atsižvelgiant į prekės pristatymo laiką. Pajėgumo laiko ribos skaičiuojamos į priekį nuo šios dienos datos.

### <a name="action-message"></a>Veiksmo pranešimas

Veiksmo pranešimuose siūlomi pakeitimai, kurie gali būti atlikti esamame tiekimo užsakyme, siekiant padėti optimizuoti tiekimo planą. Pavyzdžiui, jie gali rekomenduoti jums paankstinti ar atidėti užsakymus arba padidinti ar sumažinti užsakymo kiekius.

Nustatę parinkties **Veiksmo pranešimas** parametrą **Taip** galite perrašyti bendrojo planavimo metu nustatomą prekės veiksmo pranešimo laiko ribą. Šiuo atveju įveskite dienų, kurias bendrasis planavimas sugeneruoja poreikiams skirtus veiksmų pranešimus, skaičių. Veiksmo pranešimo laiko ribos skaičiuojamos į priekį nuo šios dienos datos.

Norėdami gauti daugiau informacijos apie veiksmų pranešimus, žr. [Veiksmų pranešimai](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/action-messages).

> [!NOTE]
> Dėl veiksmų pranešimų skaičiavimo bendrasis planavimas gali užtrukti ilgiau. Jei veiksmų pranešimai nėra reguliariai analizuojami ir taikomi (kasdien, kas savaitę ir t. t.), bendrojo planavimo vykdymo metu išjunkite skaičiavimą. Norėdami išjungti skaičiavimą, puslapyje **Bendrieji planai** nustatykite parinkties **Veiksmų pranešimas** vykdomo bendrojo plano laiko ribą į **0** (nulis). Taip pat įsitikinkite, kad parametras **Veiksmo pranešimas** yra išjungtas visose padengimo grupėse.

### <a name="calculated-delays"></a>Apskaičiuoti atidėjimai

Galite nurodyti, kaip tolį į ateitį galimi būti nustatomi ir įtraukiami ataskaitas suplanuotų užsakymų vėlavimo atvejai. Tokiu būdu galite planuoti galimas (atidėtas) pristatymo datas.

Jei negalima įvykdyti planuojamo užsakymo iki pageidaujamos datos, jis planuojamas anksčiausią operacijos vykdymo datą, atsižvelgiant į gamybos laiką, medžiagas ir pajėgumo pasiekiamumą.

### <a name="approved-requisitions-time-fence"></a>Patvirtintų paraiškų laiko riba

Galite nustatyti bendrąjį planavimą, kad būtų sukurti suplanuoto paraiškų poreikio užsakymai. Nustatykite parinkties **Įtraukti paraiškas** parametrą **Taip** puslapio **Bendrieji planai** „FastTab“ **Bendra**. Tada, kai patvirtintos paraiškos paskirtis yra papildymas, jam įvykdyti bendrasis planavimas automatiškai sukuria atitinkamą suplanuotą užsakymą. Papildymo būdą nustato tiekimo strategijos, kurios buvo nustatytos jūsų organizacijos prekėms. Kai papildymo paraiškos buvo sukurtos ir patvirtintos, nereikia jokių papildomų vartotojo veiksmų.

Nustatydami parinkties **Patvirtintų paraiškų laiko ribos** parametrą **Taip** „FastTab“ **Laiko ribos dienomis**, galite perrašyti patvirtintų paraiškų prekės laiko ribą, nustatytą atliekant bendrąjį planavimą. Šiuo atveju įveskite praeities dienų, per kurias į bendrąjį planavimą įtrauktas patvirtintų paraiškų, kurių paskirtis – Papildymas, poreikis, skaičių. Pvz., galite nurodyti, ar tik neįvykdytų, pasibaigusio termino patvirtintų paraiškų, kurios buvo sukurtos per pastarąsias 10 dienų, turėtų būti laikomasi ir ar jos turėtų būti planuojamos.

### <a name="sequencing"></a>Seka

Sekos leidžia suplanuotus užsakymus išdėstyti remiantis sekos atributais, kurie susieti su baigtu produktu. Dažnai jos naudojamos ruošiant pakavimo gamybos užsakymus. Pavyzdžiui, jos gali būti naudojamos norint pakuoti dėžes konkrečia seka, atsižvelgiant į spalvą ir dydį.

Nustatydami parinkties **Seka** parametrą **Taip**, galite nurodyti, kaip toli į ateitį operacijos arba užduotys bus atliekamos tam tikra seka. Atminkite, kad kuo ilgesnė laiko riba, tuo ilgiau bus vykdomas bendrasis planavimas.

### <a name="calculated-delays"></a>Apskaičiuoti atidėjimai

Delsos parinktys padeda užtikrinti, kad nustatytos įvykdomas užsakymų numatomos datos. Puslapio **Bendrieji planai** „FastTab“ **Apskaičiuoti atidėjimai** galima naudoti toliau nurodytas parinktis.

- **Užtikrinti, kad suplanuoti užsakymai nėra kuriami prieš bendrojo planavimo vykdymo datą** – nustatykite šios parinkties parametrą **Taip**, kad būtų galima užtikrinti, jog užsakymai nebūtų planuojami praeities datomis.
- **Įtraukti apskaičiuotą atidėjimą į poreikio datą** (pasirinkus **Suplanuoti pirkimo užsakymai**) – nustatykite šios parinkties parametrą **Taip**, kad į poreikius įtrauktumėte apskaičiuotą atidėjimą.
- **Įtraukti apskaičiuotą atidėjimą į poreikio datą** (pasirinkus **Suplanuoti gamybos užsakymai**) – nustatykite šios parinkties parametrą **Taip**, kad į poreikius įtrauktumėte apskaičiuotą atidėjimą.
- **Įtraukti apskaičiuotą atidėjimą į poreikio datą** (pasirinkus **Suplanuoti perkėlimo užsakymai**) – nustatykite šios parinkties parametrą **Taip**, kad į poreikius įtrauktumėte apskaičiuotą atidėjimą.
- **Įtraukti apskaičiuotą atidėjimą į poreikio datą** (pasirinkus **Suplanuoti „kanban“ užsakymai**) – nustatykite šios parinkties parametrą **Taip**, kad į poreikius įtrauktumėte apskaičiuotą atidėjimą.

Kai nustatote parinkties **Įtraukti apskaičiuotą atidėjimą į poreikio datą** parametrą **Taip**, kad į poreikius įtrauktumėte atidėjimų, sistema atsižvelgia į išteklių pajėgumą ir sukuria įvykdomus suplanuotus užsakymus. Suplanuoto užsakymo datų perskaičiavimas pailgina bendrojo planavimo vykdymo laiką. Todėl, jei nereikia naudoti atidėjimų, nustatykite parinktį **Ne**.

## <a name="positive-and-negative-days"></a>Teigiamos ir neigiamos dienos

Teigiamos ir neigiamos dienos veikia tai, kaip bendrasis planavimas siūlo suplanuotus užsakymus ir veiksmus. Teigiamos ir neigiamos dienos yra nustatomos prekės padengimo grupėje. Apibrėžti įvairias padengimo grupes ir nustatyti jų parametrus galite puslapyje **Padengimo grupės** (**Bendrasis planavimas \> Sąranka \> Padengimas \> Padengimo grupės**).

### <a name="positive-days"></a>Teigiamos dienos

Teigiamos dienos nurodo, kaip toli į ateitį bendrojo planavimo metu atsižvelgiamą į dabartines atsargas ar gavimus, kad būtų patenkintas ateities poreikis. Pvz., jei teigiamos dienos nustatytos kaip **100**, dabartinės atsargos gali būti naudojamos norint patenkinti poreikį per artimiausias 100 dienų. Jei numatytas užsakymas po 150 dienų nuo esamos datos, bendrasis planavimas sukurs suplanuotą užsakymą, kad patenkintų tą poreikį, net jei turimos prekės atsargos gali įvykdyti užsakymą. Jei prekės perkeliamos ir gaminamos greitai, galbūt nenorėsite naudoti turimų atsargų, kad įvykdytumėte užsakymą, kuris suplanuotas tolimesnėje ateityje. Šiuo greitu atveju dabartinės turimos atsargos greitai bus baigtos, o ateityje būtų galima pateikti daugiau užsakymų, kad laiku būtų patenkinti būsimi poreikiai, o tai bus įmanoma, nes prekės gamybos laikas yra trumpas.

Teigiamos dienos taip pat paveikia veiksmo pranešimus. Pavyzdžiui, sistema gali rekomenduoti padidinti planuojamą pirkimo užsakymą, kad į jį būtų įtrauktas poreikis, kuris patenka į teigiamų dienų skaičių ateityje. Jei teigiamos dienos nustatytos kaip **100** ir jei prekės poreikis nustatytas po 30 dienų nuo esamos datos, sistema sukurs numatytą užsakymą, kad patenkintų tą poreikį. Jei tos pačios prekės poreikis nustatytas po 90 dienų nuo esamos datos, sistema rekomenduos padidinti užsakymo kiekį per 30 dienų nuo esamos datos, kad užsakymas taip pat padengtų poreikį po 90 dienų. Tačiau, jei prekės poreikis nustatytas po 150 dienų nuo esamos datos, sistema nerekomenduos padidinti jau suplanuoto užsakymo kiekio. Vietoj to bus sukurtas naujas suplanuoti užsakymas.

Paprastai teigiamos dienos yra nustatomos į skaičių, kuris yra tarp ilgiausio prekių gamybos laiko ir padengimo laiko ribos. Rekomenduojame priskirti prekes, kurios yra reguliariai įsigyjamos arba gamintos, padengimo grupei, kurioje teigiamos dienos lygios prekės gamybos laikui.

### <a name="negative-days"></a>Neigiamos dienos

Neigiamos dienos nurodo, kaip vėlai prekių gavimas bus leidžiamas. Jos nurodo, kiek dienų norite palaukti prieš užsisakydami naują papildymą, kai atsargų kiekis neigiamas arba nepakankamas. Neigiamos dienos atsako į klausimą: ar kurti naują prekės pirkimo užsakymą, ar naudoti esamą pirkimą, net jei žinome, kad prekė bus gauta vėliau?

Pavyzdžiui, prekės pardavimo užsakymas suplanuotas po 15 dienų nuo esamos datos. Taip pat suplanuotas tos pačios prekės pirkimo užsakymas. Šis pirkimo užsakymas bus gaunamas per 20 dienų nuo esamos datos. Ar norite, kad sistema sukurtų to pardavimo užsakymo pirkimo užsakymą, ar norite naudoti esamą užsakymą, net jei laiku negalite įvykdyti pardavimo užsakymo? Jei neigiamos dienos nustatytos į mažesnę reikšmę nei **5**, siekiant nurodyti, kad prekė gali būti atidėta daugiausiai penkiomis dienomis, sistema sukuria naują suplanuotą pirkimo užsakymą, kad būtų patenkintas pardavimo užsakymas. Jei neigiamos dienos nustatytos į didesnę reikšmę nei **5**, sistema naudoja esamą prekės užsakymą.

Neigiamos dienos taip pat paveikia bendrojo planavimo našumą. Jei neigiamos dienos nustatytos į didelį skaičių, bus sugeneruota daug veiksmų pranešimų.

Rekomenduojame nustatyti neigiamų dienų skaičių, kuris yra mažesnis nei prekės gamybos laikas.

### <a name="dynamic-negative-days"></a>Dinaminės neigiamos dienos

Dinaminės neigiamos dienos atsižvelgia į prekės gamybos laiką ir neigiamas dienas, kurias nurodėte. Sistema sukurs naują suplanuotą pirkimo užsakymą, pagrįstą neigiamų dienų laiko riba, kuri apskaičiuojama naudojant šią formulę:

gamybos laikas + neigiamos dienos + esama data – poreikio data

Sistema naudoja tik šiose laiko ribose suplanuotus tiekimo užsakymus, o kitu atveju ji sukuria naują planuojamą užsakymą. Dinaminių neigiamų dienų privalumas yra tai, kad bus įtrauktas atskiro produkto gamybos laikas, siekiant pakartotinai naudoti esamus užsakymus ir nekurti naujų užsakymų, kurie bus įvykdyti vėliau tą pačią dieną, užfiksuotas atidėjimas dėl gamybos laiko. 

Norėdami gauti daugiau informacijos žr. [Neigiamos dienos ir dinaminės neigiamos dienos](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/more-about-dynamic-negative-days).
