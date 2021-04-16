---
title: Automatinis išlaidų nustatymas
description: Šioje temoje aprašoma, kaip nustatyti įvairių gaunamų reiso lygių savikainos taisykles. Pagal šias taisykles sistema apskaičiuoja savikainą ir automatiškai ją prideda. Todėl naudotojams nereikia rankiniu būdu pridėti savikainos.
author: sherry-zheng
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMCostAutoSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 2e9135019323db74a4dca9343d315cbbf9683e32
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841964"
---
# <a name="auto-costs-setup"></a>Automatinis išlaidų nustatymas

[!include [banner](../../includes/banner.md)]

Puslapį **Automatinė savikaina** galima nustatyti įvairių savikainos sričių savikainos taisykles (pvz., reisus, gabenimo konteinerius, foliantus, pirkimo užsakymus, prekes ar pervežimo užsakymo eilutes). Sistema, remdamasi taisyklėmis ir laukeliais, kuriuos naudotojai pasirenka kurdami vienos iš savikainos sričių įrašus, apskaičiuoja savikainą ir ją prideda automatiškai. Todėl naudotojams nereikia rankiniu būdu pridėti savikainos.

Norėdami dirbti su automatine savikaina pereikite į **Iškrauto produkto savikaina\> Įkainojimo nustatymas \> Automatinė savikaina**. Tada nustatykite savo automatinės savikainos taisykles, kaip aprašyta likusioje šios temos dalyje.

## <a name="work-with-cost-areas"></a>Darbas su savikainos sritims

Automatinė savikaina veikia kaip prekybos sutartys arba automatinė įvairi savikaina. Kiekvienas automatinis savikainos įrašas priklauso konkrečiam savikainos lygiui. Norėdami pasirinkti savikainos sritį, su kuria norite dirbti, naudokite laukelį **Savikainos sritis**, esantį puslapyje **Automatinė savikaina**. Sąrašo srityje rodoma tik automatinė savikaina, priklausančios šiuo metu pasirinktai savikainos sričiai. Bet kokia jūsų kuriama automatinė savikaina priklausys šiuo metu pasirinktai savikainos sričiai.

Savikainos sritys sistemai leidžia paskirstyti savikainą keliose pirkimo užsakymo eilutėse savikainos srityje. Pavyzdžiui, vieno gabenimo konteinerio išlaidų vertę paskirstys visiems produktams tame gabenimo konteineryje. Jei yra du arba daugiau gabenimo konteinerių, kiekvienam gabenimo konteineriui galima nurodyti tą patį savikainos tipą. Todėl konteinerio tipą galima naudoti norint rasti teisingą automatinę savikainą.

## <a name="buttons-on-the-action-pane"></a>Veiksmų srities mygtukai

Toliau pateiktoje lentelėje aprašomi mygtukai, esantys puslapio **Automatinė savikaina** veiksmų srityje.

| Mygtukas | aprašymas |
|---|---|
| Redagavimas | Redaguokite esamą automatinę savikainą. |
| Naujos | Sukurkite automatinę savikainą. |
| Panaikinti | Ištrinkite automatinę savikainą. |
| Kopijuoti iš | Sukurkite naują automatinės savikainos įrašą pagal esamą įrašą. Tada galėsite laisvai redaguoti naują įrašą. Šis mygtukas padeda greitai sukurti naujas automatine savikainas. |
| Rodyti dimensijas | Atidarykite dialogo langą, kuriame galima pasirinkti jūsų peržiūrimų savikainos operacijų rodomas atsargų dimensijas. Jei išvalysite varneles, savikainos operacijoms bus rodoma mažiau atsargų dimensijų. Todėl tai operacijai bus rodoma mažiau informacijos. Jei atsargų dimensija nurodyta automatinei savikainai, automatinė savikaina bus taikoma tik tada, kai nurodyta atsargų dimensija naudojama reiso prekei. |

## <a name="settings-on-the-header"></a>Parametrai antraštėje

Parametrų derinys antraštės dalyje apibrėžia, kada ir kaip konkreti automatinė savikaina pridedama prie reiso. Automatinė savikaina bus taikoma reisui, gabenimo konteineriui arba foliantui tik tada, kai automatinės savikainos duomenys sutaps su tos savikainos srities antraštėje nurodytais duomenimis. Visų sutampančios automatinės savikainos suma apibrėžia įvertintą reiso iškrauto produkto savikainą. Ši savikaina paskirstoma visoms laivo ar reiso prekėms.

Šioje lentelėje apibūdinami visi laukeliai, kurie gali būti rodomi antraštės dalyje. Tačiau konkretūs galimi laukeliai skiriasi priklausomai nuo savikainos srities ir joje rodomos šiuo metu pažymėtos dimensijos.

| Laukas | aprašymas |
|---|---|
| **Sąskaitos kodas** | <p>Pasirinkite vieną iš šių reikšmių:</p><ul><li>**Lentelė** – savikainos taisyklė taikoma tik konkrečiam tiekėjui.</li><li>**Lentelė** – savikainos taisyklė taikoma tik konkrečiai tiekėjų grupei. Sistema ieškos [tiekėjo savikainos tipų grupės](costing-parameters-setup.md), susietos su tiekėjo įrašu.</li><li>**Visi** – savikainos taisyklė taikoma visiems tiekėjams. |
| **Gabenimo įmonė** | Pasirinkite tiekėją ar tiekėjų grupę, kuriai taikoma savikainos taisyklė. Šis laukelis naudojamas tik pasirinkus *Lentelė* arba *Grupė* laukelyje **Sąskaitos kodas**. |
| **Muitinės tarpininkas** | Pasirinkite tiekėją ar tiekėjų grupę, kuriai taikoma savikainos taisyklė. Šis laukelis naudojamas tik pasirinkus *Lentelė* arba *Grupė* laukelyje **Sąskaitos kodas**. |
| **Prekės kodas** | <p>Pasirinkite vieną iš šių reikšmių:</p><ul><li>**Lentelė** – savikainos taisyklė taikoma tik konkrečiai prekei.</li><li>**Lentelė** – savikainos taisyklė taikoma tik konkrečiai prekių grupei. Sistema ieškos [prekės savikainos tipų grupės](costing-parameters-setup.md), susietos su prekės įrašu.</li><li>**Visi** – savikainos taisyklė taikoma visoms prekėms.|
| **Prekės ryšys** | Pasirinkite prekę ar prekių grupę, kuriai taikoma savikainos taisyklė. Šis laukelis naudojamas tik pasirinkus *Lentelė* arba *Grupė* laukelyje **Prekės kodas**. |
| **Pristatymo būdas** | Pasirinkite pristatymo būdą (pvz., oru ar jūra), kuriam taikoma savikainos taisyklė. |
| **Konteinerio tipas** | Gabenimo konteinerio, kuriame bus siunčiamos prekės, tipas. Automatinė savikaina gali būti taikoma reisui tik jei konteinerio tipas automatinės savikainos nustatyme atitinka reiso konteinerio tipą. |
| **Išvykimo uostas** ir **Atvykimo uostas** | Reiso pradinis (išvykimo) uostas ir paskirties (atvykimo) uostas. (Kai kuriems gabenimo konteineriuose gali būti nurodyti skirtingi atvykimo uostai, nes reisas gali sustoti keliuose uostuose.) Automatinė savikaina gali būti taikoma reisui tik jei išvykimo ir atvykimo uostai automatinės savikainos sąrankoje atitinka reiso išvykimo ir atvykimo uostus. |
| **Aut. išlaidų numeris** | Unikalus automatinės savikainos taisyklės identifikatorius. Šio laukelio vertė automatiški generuojam pagal skaičių seką, kuri nustatoma puslapyje **Iškrauto produkto savikainos parametrai**. |
| **Atsargų dimensijos** | Kai kuriose savikainos srityse antraštėje galima įtraukti vieną ar kelias dimensijas (pvz., dydį, spalvą, sandėlį ir partijos numerį). Veiksmų srityje pasirinkite **Rodyti dimensijas**, kad pasirinktumėte dimensijas, kurias reikėtų įtraukti. |

## <a name="settings-on-the-lines-fasttab"></a>„FastTab” eilutės parametrai

„FastTab“ skirtuke **Eilutės** pridėkite po eilutę kiekvienai valiutai, kurią galima naudoti reiso pirkimo užsakymo eilutėje. 

Prekių ir pirkimo užsakymų sistema kiekvienos pirkimo užsakymo eilutės valiutą patikrins su „FastTab“ skirtuke **Eilutės** nurodytomis valiutomis. Bus taikoma tik išlaidų vertė, nustatyta sutampančiai eilutei ar prekei. Jei eilutei ar prekei nėra nustatyta valiutos eilutė, automatinė savikaina tai eilutei ar prekei nebus taikoma.

Kitų tipų savikainos sritims visos eilutės, nurodytos „FastTab“ skirtuke **Eilutės**, bus taikomos kiekvienam reisui, gabenimo konteineriui, foliantui ar pervežimo užsakymo eilutei, kuri atitinka antraštėje nurodytas vertes.

Šioje lentelėje apibūdinami visi laukeliai, kurie gali būti rodomi kiekvienoje eilutėje. Tačiau konkretūs galimi laukeliai skiriasi priklausomai nuo šiuo metu pasirinktos savikainos srities.

| Laukas | aprašymas |
|---|---|
| **Valiuta** | Pasirinkite valiutą, kuriai taikoma eilutė. Ši valiuta yra susijusi su pirkimo užsakymu. Kai sistema mėgina rasti automatinę savikainą, kuri turėtų būti taikoma reisui ir jos reiso eilutėms, ji pasirinks eilutę, kurioje nurodyta ta pati valiuta kaip ir pirkimo užsakyme. Šis laukelis naudojamas tik tada, kai laukelis **Savikainos sritis** nustatoma kaip *Pirkimo užsakymas* arba *Prekė*. |
| **Išlaidų tipo kodas** | Savikainos tipas. |
| **Paskirstymo metodas** | <p>Metodas, naudojamas savikainai eilutėse paskirstyti. Galimos toliau nurodytos parinktys.</p><ul><li><p>**Procentas** – laukelio **Išlaidų vertė** yra bendrai prekių vertei taikoma dalis procentais.</p><p>Pavyzdžiui, jei laukelis **Išlaidų vertė** nustatomas kaip *10*, o bendra prekių vertė yra 800 USD, išlaidų vertė bus 80 USD (= 800 USD × 10 procentų).</p></li><li>**Kiekis** – savikaina bus priskirta remiantis prekių kiekiu.</li><li>**Suma** – savikaina bus priskirta remiantis prekių verte.</li><li>**Tūris** – savikaina bus priskirta remiantis prekių tūriu. Tūris nurodomas pagrindinėje prekėje.</li><li>**Svoris** – savikaina bus priskirta remiantis prekių svoriu. Svoris nurodomas pagrindinėje prekėje.</li><li>**Tūrinis** – savikaina bus priskirta remiantis prekių tūriniais matavimais.</li><li><p>**Matavimai** – ši pasirinktis leidžia matavimus nurodyti modulyje **Iškrauto produkto savikaina**. Juos dažnai naudoja organizacijos, kurios nežino atskirų prekių tūrio ar svorio, bet reikalauja tikslesnio paskirstymo, nei leidžia parinktys **Suma** ir **Kiekis**. Krovinių ekspeditorius arba agentas organizacijai nurodys svorį arba kubinį matavimo vienetą kiekvienai prekei atskirai arba bendrai visam pirkimo užsakymui.</p><p>Pavyzdžiui, pervežimo jūrų transportu kaina yra 900 USD. A prekės svoris yra 800 kilogramų (kg), o tūris – 2 kubiniai metrai (m³). B prekės svoris yra 100 kg, o tūris – 1 m³. Štai rezultatai, kai savikaina nurodoma pagal svorį:</p><ul><li>A prekė = 800 USD</li><li>B prekė = 100 USD</li></ul><p>Štai rezultatai, kai savikaina nurodoma pagal tūrį:</p><ul><li>A prekė = 600 USD</li><li>B prekė = 300 USD</li></ul><p>**Pastaba.** Kai laukelis **Paskirstymo mechanizmas** nustatytas kaip *Matavimas*, sistema naudoja matavimus, kurie yra įvesti savikainos sričiai (gabenimo konteineris) ir eilutėms. Šie matavimai nebūtinai turi būti pridedami prie numatomos bendrosios sumos. Tačiau jei reikia, kad jie būtų pridėti prie numatomos bendrosios sumos, galima atlikti greitą patikrinimą, naudojant statistiką bendram matavimui peržiūrėti. Matavimo raginimo nustatymas ir automatinis matavimo atnaujinimas siuntos arba konteinerio lygmeniu nustatomas reiso antraštėje.</p></li></ul> |
| **Nuo datos** | Jei nurodomas datų diapazonas, nurodykite įkainojimo datų diapazono pradžią. Tai yra pirmoji data, nuo kurios bus taikoma automatinė savikaina. |
| **Data Iki** | Jei nurodomas datų diapazonas, nurodykite įkainojimo datų diapazono pabaigą. Tai yra paskutinė data, nuo kurios bus taikoma automatinė savikaina. |
| **Kategorija** | <p>Pasirinkite būdą, kuris bus naudojamas savikainai apskaičiuoti. Galimos toliau nurodytos parinktys.</p><ul><li>**Fiksuota** – savikaina bus priskirta remiantis paskirtuoju būdu.</li><li>**Vienetai** – savikaina bus paskirstyta pagal vienetą. Todėl skirtasis būdas nebus naudojamas.</li><li>**Procentas** – bus pridėta prekių vertės dalis procentais. Todėl skirtasis būdas nebus naudojamas.</li><li>**Tarifas** – pasirinkite šią pasirinktį, jei kiekis yra paskirstomas. Eilutės laukelį **Skirtasis būdas** reikia nustatyti kaip *Matavimas*.</li><ul> |
| **Išdėstyta pagal kiekį** | <p>Pažymėkite šį langelį, kad mygtuką **Kiekio paskirstymai** būtų galima naudoti „FastTab“ skirtuke **Eilutės**. Kiekio paskirstymai leidžia paskirstyti savikainą, o skirtingos savikainos gali keistis priklausomai nuo reiso pirkimo užsakymo eilutės kiekio. Ši funkcija dažnai naudojama, kai pristatymo būdas yra oru. Eilutės laukelį **Kategorija** reikia nustatyti kaip *Tarifas*.</p><p>Kiekis priklauso parinkčiai, kuri yra pasirinkta laukelyje **Skirtasis būdas**. Išlaidų vertė nustatoma iki laukelyje **Išlaidų vertė** įvesto kiekio.<p>Pavyzdžiui, jei produkcijos kiekis yra 45–100 kg, kiekvienam matavimui taikomas 6,00 USD mokestis (pvz., kg/m³). Jei produkcijos kiekis viršija 100 kg, kiekvienam matavimui taikomas 5,50 USD mokestis (pvz., kg/m³).</p> |
| **Išlaidų vertė** | Įveskite išlaidų vertę. |
| **Išlaidų valiutos kodas** | Pasirinkite savikainos valiutą. |
| **Prekės PVM grupė** | Pasirinkite savikainos mokesčio kodą. |
| **Mažiausios išlaidos** | <p>Šis laukelis taikomas tik pažymėjus žymės langelį **Suskirstyta pagal kiekį**. Jei matavimas šios vertės nepasiekia, pasirenkama mažiausia vertė, nepriklausomai nuo puslapyje **Paskirstytas kiekis** nurodytos savikainos.<p>Pavyzdžiui, jei produkcijos kiekis yra 0–45 kg, kiekvienam matavimui taikomas 6 USD mokestis (pvz., kg/m³). Jei produkcijos kiekis yra 46–100 kg, kiekvienam matavimui taikomas 5,50 USD mokestis (pvz., kg/m³). Jei išsiunčiami 2 kg, paskirsčius kiekį sukuriama 12 USD išlaidų vertė. Tačiau jei laukelis **Mažiausia savikaina** nustatomas kaip *100 USD*, galutinė kaina bus 100 USD.</p> |
| **Sujungti** | Pažymėkite šį žymės langelį, kad naudotojai šią savikainą galėtų perkelti iš gabenimo konteinerio lygio į reiso lygį. Tokiu atveju savikainą galima automatiškai apskaičiuoti gabenimo konteinerio lygiu. Tačiau ją taip pat galima suderinti ir paskirstyti visoms prekėms visuose reiso konteineriuose, o ne visoms prekėms atskiruose gabenimo konteineriuose. |
| **Susietas išlaidų tipas** | <p>Šią eilutę susiekite su kita eilute tame pačiame automatinės savikainos įraše, nustatydami eilutės, su kuria norite susieti, vertę **Savikainos tipo kodas**. Ši funkcija naudojama tik tada, kai laukelis **Kategorija** dabartinei eilutei yra nustatytas kaip *Procentas*. Kai dabartinė eilutė susiejama su kita eilute, dabartinės eilutės savikaina grindžiama kitos eilutės savikaina.</p><p>Pavyzdžiui, krovinio savikaina yra 1 000 USD ir norite, kad kuro priemoka būtų 10 procentų krovinio savikainos. Tokiu atveju eilutės vertė **Kategorija** turi turėti vertę *Procentai*, vertė **Išlaidų vertė** būtų *10 %*, o vertė **Susietos savikainos tipas** būtų nustatyta vertei *Krovinys*.</p> |
| **Vertės koregavimas** ir **Koregavimo suma** | <p>Naudokite šiuos laukelius įvairių procentinių dalių vertei ir sumai koreguoti. Juos galima naudoti tik tada, kai laukelis **Savikainos sritis** nustatytas kaip *Prekė*.</p><p>Skirtingiems prekių komponentams galima nustatyti skirtingą įkainojimą. Vienas prekės komponentas gali turėti kitokią savikainos dalį procentais, nei kiti tos prekės komponentai. Kartais toks požiūris reikalingas, kad konkreti prekių dalis būtų įvertinta skirtingais tarifais.</p><p>Pavyzdžiui, muitas už laikrodį apskaičiuojamas pagal du tarifus: vienam laikrodžio komponentui taikomas 10 procentų muito mokesčio tarifas, o antrajam – 2 procentų muito mokesčio tarifas. Šiuo atveju įkainojimas bus padalintas dviem komponentams.</p><p>Prekės savikaina skaičiuojama, bet išlaidų vertė koreguojama pagal komponentų, kurie yra priskirti skirtingoms savikainos kategorijoms, vertę. Likusių komponentų savikainą galima apskaičiuoti naudojant sumą, pagal kurią buvo reguliuojamas ankstesnis skaičiavimas.</p><p>Pavyzdžiui, laikrodžio A komponento savikaina yra 9,50 USD ir taikomas 10 procentų muito mokestis, o B komponento savikaina yra 0,50 USD bei taikomas 2 procentų muito mokestis. Todėl bendra savikaina yra 10,00 USD. Pirmasis įrašas skirtas 10 procentų eilutei. Jis naudoja šias vertes:</p><ul><li>**Kategorija:** *Procentas*</li><li>**Išlaidų vertė:** *10*</li><li>**Pakoreguota vertė:** *Koreguoti pagal*</li><li>**Pakoreguota vertė:** *–0,50*</li></ul><p>Šioje sąrankoje nurodoma, kad prekės savikainą (10 USD) reikia sumažinti 0,50 USD (B komponento kaina) prieš apskaičiuojant 10 procentų muito mokestį. Todėl 10 procentų bus taikoma 9,50 USD sumai.</p><p>Antrasis įrašas skirtas 2 procentų eilutei (0,50 USD, pagal kurį buvo pakoreguotas ankstesnis įrašas). Jis naudoja šias vertes:</p><ul><li>**Kategorija:** *Procentas*</li><li>**Išlaidų vertė:** *2*</li><li>**Pakoreguota vertė:** *Naudoti*</li><li>**Koregavimas** *0,50*</li></ul><p>Šioje sąrankoje apskaičiuojamas likęs muito mokestis, kuris mokamas už B komponentą.</p> |
