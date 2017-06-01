---
title: "Išplėstinės finansinių ataskaitų formatavimo parinktys"
description: "Kai finansinėse ataskaitose sukuriate ataskaitą, galima naudoti papildomas formatavimo funkcijas, įskaitant dimensijų filtrus, stulpelių ir ataskaitų vienetų apribojimų, nespausdinamas eilutes ir IF / THEN / ELSE sakinius skaičiavimuose."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter
ms.custom: 106571
ms.assetid: 895b5127-01d6-4495-b127-343387b743aa
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: cc22e564c68ab04c61f2a2fc9d0a70335dc05b06
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="advanced-formatting-options-in-financial-reporting"></a>Išplėstinės finansinių ataskaitų formatavimo parinktys

[!include[banner](../includes/banner.md)]


Kai finansinėse ataskaitose sukuriate ataskaitą, galima naudoti papildomas formatavimo funkcijas, įskaitant dimensijų filtrus, stulpelių ir ataskaitų vienetų apribojimų, nespausdinamas eilutes ir IF / THEN / ELSE sakinius skaičiavimuose. 

Šioje lentelėje paaiškinamos išplėstinės formatavimo funkcijos, galimos kuriant ataskaitas.

| Funkcija                   | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                                                                     |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dimensijos filtras           | Norėdami pasiekti konkrečius duomenų rinkinius, galite naudoti dimensijas, esančias eilutės ir stulpelio aprašuose. Daugelyje ataskaitų naudojamas tik tipo segmentas eilutės formatu. Tačiau eilutes galima modifikuoti, kad jose būtų dimensijų reikšmės. Stulpelio aprašo dimensijų filtrai naudojami konkrečioms dimensijų reikšmėms pasiekti. |
| Ataskaitinio vieneto apribojimas | Galite nustatyti ataskaitos eilutę, kad joje būtų rodoma tik informacija, susietą su konkrečiu ataskaitiniu vienetu.                                                                                                                                                                                                                      |
| Nespausdinamos (NP) eilutės     | Nespausdinamos eilutės naudingos daugelyje ataskaitų. Jei norint gauti reikšmę reikia keleto skaičiavimų, šie skaičiavimai gali būti paslėpti spausdintoje ataskaitoje. Nespausdinamos eilutės taip pat naudingos ataskaitos dizainų trikčių diagnostikai ir išplėstiniam langelių išdėstymui.                                                    |
| Stulpelio apribojimas         | Eilutės aprašo stulpelio apribojimas naudingas reikšmėms, kurios yra reikšmingos tik kai kurioms ataskaitos eilutėms, slėpti. Kai procentinės dalys skaičiuojamos eilutėje, stulpelio apribojimas neleidžia spausdinti visų stulpelių arba kitus stulpelių, jei šie skaičiau netaikomi.                              |
| Stulpelio lūžis               | Galite pridėti stulpelių lūžių eilutės apraše, kad šalia būtų rodoma ataskaitos informacija. Galite pridėti kelis stulpelio lūžius viename eilutės apraše, ir stulpelių antraštės bus kartojamos kiekvieno stulpelio viršuje po stulpelio lūžio. Ataskaitos komentarai rodomi tarp stulpelių lūžių.                              |
| IF / THEN / ELSE sakinys     | Galite modifikuoti eilutės aprašo arba stulpelio aprašo skaičiavimus.                                                                                                                                                                                                                                                         |

## <a name="advanced-cell-placement"></a>Išplėstinis langelių išdėstymas
Išplėstinis langelių išdėstymas arba *privertimas* yra konkrečių reikšmių išdėstymas konkrečiuose langeliuose. Pavyzdžiui, privertimas dažnai naudojamas teisingam balansui perkelti į pinigų srautų ataskaitą. Galite naudoti privertimą šiems tikslams.

-   Reikšmėms perkelti iš „Microsoft Excel“ į konkrečius langelius.
-   Tam tikroms reikšmėms įkoduoti į ataskaitą.
-   Ženklams modifikuoti kopijuojant reikšmę iš ankstesnio langelio ir dauginant šią reikšmę iš –1.

**Pastaba.** Daugeliu atvejų turite sukonfigūruoti savo ataskaitos aprašą, kad stulpelio skaičiavimai būtų atliekami prieš eilučių skaičiavimus. Norėdami užbaigti šią konfigūraciją, atlikite šiuos veiksmus.

1.  Ataskaitų konstruktoriuje atidarykite ataskaitos aprašą.
2.  Skirtuko **Parametrai** dalyje **Skaičiavimo prioritetas** pasirinkite **Pirmiau atlikti stulpelio, o tada eilutės skaičiavimą**.

## <a name="designing-the-report"></a>Ataskaitos kūrimas
Kurdami ataskaitą turite pirmiausia sukurti visas informacijos eilutes, kad užtikrintumėte, kad šios reikšmės bus įtrauktos, kaip yra numatyta. Tada pridėkite **NP** (nespausdinama) formato nepaisymus, kad informacija, kurioje yra galutinės reikšmės, nebūtų rodoma. **Svarbu.** Eilutės apraše naudojant **KPL** formato kodą, negalima detalizuoti operacijos informacijos. Priverčiant formulės naudoja šį formatą: &lt;paskirties stulpelis&gt;=&lt;kilmės stulpelis&gt;&lt;eilutės kodas&gt; Atskirkite visas papildomas padėtis eilutėje kableliu ir tarpu. Štai pavyzdys: D=C.190,E=C.100

## <a name="examples-of-advanced-formatting-options"></a>Išplėstinių formatavimo parinkčių pavyzdžiai
Toliau pateiktuose pavyzdžiuose parodyta, kaip suformatuoti eilutės aprašą ir stulpelio aprašą norint priverstinai sukurti pagrindinę pinigų srauto ataskaitą (1 pavyzdys) ir statistinę ataskaitą (2 pavyzdys).

### <a name="example-1-basic-forcing"></a>1 pavyzdys. Paprastasis privertimas

Toliau pateikiamoje lentelėje parodytas eilutės aprašo, naudojančio paprastąjį privertimą, pavyzdys.

| Eilutės kodas | Prekės/Paslaugos pavadinimas                      | Formato kodas | Susijusios formulės / eilutės / vienetai | Formato nepaisymas | Standartinis balansas | Spausdinimo valdiklis | Stulpelio apribojimas | Eilutės modifikatorius               | Saitas su finansinėmis dimensijomis |
|----------|----------------------------------|-------------|-----------------------------|-----------------|----------------|---------------|--------------------|----------------------------|------------------------------|
| 100      | Laikotarpio pradžios grynieji pinigai (NP) |             |                             |                 |                |               |                    | Sąskaitos modifikatorius = \[/BB\] | +2 segmentas = \[1100\]         |
| 130      | Laikotarpio pradžios grynieji pinigai      | KPL         | C=C.100,F=D.100             |                 |                |               |                    |                            |                              |
| 160      |                                  |             |                             |                 |                |               |                    |                            |                              |
| 190      |                                  |             |                             |                 |                |               |                    |                            |                              |

Toliau pateikiamoje lentelėje parodytas stulpelio aprašo, naudojančio paprastąjį privertimą eilutėje, pavyzdys.

|                              | A   | Mlrd.    | K        | D      | E      | Pn.    |
|------------------------------|-----|------|----------|--------|--------|------|
| 1 antraštė                     |     |      |          |        |        |      |
| 2 antraštė                     | A   | Mlrd.    | K        | D      | E      | Pn.    |
| 3 antraštė                     |     |      |          |        |        |      |
| Stulpelio tipas                  | EILUTĖ | APRAŠ. | FD       | FD     | FD     | SKAIČ. |
| Knygos kodas / atributo kategorija |     |      | FAKTINIS   | FAKTINIS | FAKTINIS |      |
| Finansiniai metai                  |     |      | PAGRINDINIS     | PAGRINDINIS   | PAGRINDINIS   |      |
| Laikotarpis                       |     |      | PAGRINDINIS     | PAGRINDINIS   | PAGRINDINIS   |      |
| Įtraukti laikotarpiai              |     |      | PERIODINIS | YTD/BB | YTD    |      |
| Formulė                      |     |      |          |        |        | E-D  |
| Stulpelio plotis                 | 5   | 30   | 14       | 14     | 14     | 14   |

### <a name="example-2-statistical-reports"></a>2 pavyzdys. Statistinės ataskaitos

Toliau pateikiamoje lentelėje parodytas eilutės aprašo, naudojančio statistinės ataskaitos privertimą, pavyzdys.

| Eilutės kodas | Prekės/Paslaugos pavadinimas               | Formato kodas | Susijusios formulės / eilutės / vienetai     | Formato nepaisymas      | Standartinis balansas | Spausdinimo valdiklis | Stulpelio apribojimas | Eilutės modifikatorius | Saitas su finansinėmis dimensijomis               |
|----------|---------------------------|-------------|---------------------------------|----------------------|----------------|---------------|--------------------|--------------|--------------------------------------------|
| 50       | Statistinė informacija   | LIK.         |                                 |                      |                |               |                    |              |                                            |
| 100      | Darbuotojų skaičiaus – JAV            | KPL         | 4                               | \#\#\#0.;($\#\#\#0.) |                |               |                    |              |                                            |
| 115      | Darbuotojų skaičiaus – tarptautinis | KPL         | 11                              | \#\#\#0.;($\#\#\#0.) |                |               |                    |              |                                            |
| 130      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 190      | JAV pardavimas                  |             |                                 |                      | K              |               |                    |              | +2segmentas = \[41\*\], 3segmentas = \[00\]    |
| 220      | Tarptautinis pardavimas       |             |                                 |                      | K              |               |                    |              | +2segmentas = \[41\*\], 3segmentas = \[01:99\] |
| 250      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 280      |                           |             |                                 |                      |                |               |                    |              |                                            |
| 310      | JAV pardavimas                  | KPL         | D=C.190,E=C.100,F=(C.100/C.190) |                      |                |               |                    |              |                                            |
| 340      | Tarptautinis pardavimas       | KPL         | D=C.220,E=C115,F=(C.220/C.115)  |                      |                |               |                    |              |                                            |

Toliau pateikiamoje lentelėje parodytas stulpelio aprašo, naudojančio statistinės ataskaitos privertimą, pavyzdys.

|                              | A   | Mlrd.    | K      | D            | E     | Pn.            |
|------------------------------|-----|------|--------|--------------|-------|--------------|
| 1 antraštė                     | A   | Mlrd.    | K      | D            | E     | Pn.            |
| 2 antraštė                     | -   | -    | Nuo metų pradžios    | Metų pardavimas | Darbuotojai | $ vienam asmeniui |
| 3 antraštė                     |     |      |        |              |       |              |
| Stulpelio tipas                  | EILUTĖ | APRAŠ. | FD     | SKAIČ.         | SKAIČ.  | SKAIČ.         |
| Knygos kodas / atributo kategorija |     |      | FAKTINIS |              |       |              |
| Finansiniai metai                  |     |      | PAGRINDINIS   |              |       |              |
| Laikotarpis                       |     |      | PAGRINDINIS   |              |       |              |
| Įtraukti laikotarpiai              |     |      | YTD    |              |       |              |
| Formulė                      |     |      |        |              |       | E-D          |
| Stulpelio plotis                 | 5   | 30   | 14     | 14           | 14    | 14           |

## <a name="restricting-a-row-to-a-specific-reporting-unit"></a>Eilutės apribojimas iki tam konkretaus ataskaitų vieneto
Kai ataskaitos eilutė yra apribota iki konkretaus ataskaitinio vieneto, toje eilutėje rodami tik nurodyto ataskaitinio vieneto susietieji duomenys, ir nepaisoma kitų ataskaitų medžio ataskaitinių vienetų duomenų. Pavyzdžiui, galite sukurti eilutę, kurioje pateikiama informacija apie konkretaus skyriaus bendrąsias veiklos išlaidas. Jūsų ataskaitoje gali būti pasikartojančių duomenų, jei ataskaitoje yra ataskaitų medžio ir eilutės aprašas, kuriame yra ne tik įprasta sąskaita. Pavyzdžiui, turite ataskaitų medį, kuriame pateikiami šeši jūsų organizacijos skyriai, ir taip pat turite eilutės aprašą, kuriame pateikiama tam tikra sąskaitos ir skyriaus eilutėje kombinacija. Generuojant ataskaitą, tam tikros sąskaitos ir skyriaus kombinacija spausdinama ant kiekvieno ataskaitų medžio lygio, nors tas skyrius gali neatitikti to, kas yra medyje. Taip atsitinka, nes eilutė nepaiso to, ką paprastai filtruoja ataskaitos aprašas. Vienas būdas išvengti besidubliuojančių duomenų yra apriboti eilutę iki konkretaus ataskaitinio vieneto. **Pastaba.** Jei eilutėje yra dimensijų ir apribosite tą eilutę iki antrinio ataskaitinio vieneto, bus įtraukta to ataskaitinio vieneto ir jo pirminių vienetų eilutės suma, bet dubliavimosi nebus.

### <a name="restrict-a-row-to-a-reporting-unit"></a>Eilutės apibojimas iki ataskaitinio vieneto

1.  Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada pasirinkite norimą keisti eilutės apibrėžimą.
2.  Dukart spustelėkite atitinkamą langelį **Susijusios formulės / eilutės / vienetai**.
3.  Dialogo lange **Ataskaitinio vieneto pasirinkimas**, lauke **Ataskaitų medis**, pasirinkite medį, priskirtą ataskaitos apraše.
4.  Pasirinkite ataskaitinį vienetą ir tada spustelėkite **Gerai**. Apribojimas rodomas eilutės aprašo langelyje.
5.  Dukart spustelėkite langelį apribotos eilutės stulpelyje **Saitas su finansinėmis dimensijomis** ir tada įveskite saitą su finansinių duomenų sistema.

## <a name="selecting-print-control-in-a-row-definition"></a>Spausdinimo valdiklio pasirinkimas eilutės apibrėžime
Galite nurodyti kiekvieno stulpelio spausdinimo kontrolinius kodus naudodami langelį **Spausdinimo valdiklis**.

### <a name="add-print-control-codes-to-a-report-row"></a>Spausdinimo kontrolinių kodų įtraukimas į ataskaitos eilutę

1.  Ataskaitų dizaino įrankyje atidarykite norimą modifikuoti eilutės apibrėžimą.
2.  Dukart spustelėkite langelį **Spausdinimo valdiklis**.
3.  Dialogo lange **Spausdinimo valdiklis** pasirinkite spausdinimo kontrolinį kodą arba paspauskite ir laikykite klavišą Ctrl norėdami pažymėti kelis kodus. Taip pat galite įvesti spausdinimo kontrolinius kodus tiesiai langelyje **Spausdinimo valdiklis**. Atskirkite kelis spausdinimo kontrolinius kodus kableliais.
4.  Pasirinkite sąlyginio spausdinimo pasirinktis.
5.  Spustelėkite **GERAI**.

### <a name="regular-print-control-codes"></a>Įprastiniai spausdinimo kontroliniai kodai

Toliau pateikiamoje lentelėje aprašomi paprastieji eilutės aprašo spausdinimo kontroliniai kodai.

| Spausdinimo kontrolinis kodas | Spausdinimo kontrolinio kodo šifravimas         | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Nespausdinama (NP) eilutė                                 | Neleiskite, kad eilutėje esančios sumos būtų spausdinamos ataskaitoje, ir neįtraukite sumų į skaičiavimus. Norėdami į skaičiavimą įtraukti nespausdinamą stulpelį, nurodykite stulpelį tiesiogiai skaičiavimo formulėje. Pavyzdžiui, 240 nespausdinama eilutė įtraukiama į šį skaičiavimą: **230 + 240 + 250**. Tačiau 240 nespausdinama eilutė neįtraukiama į šį skaičiavimą: **230:250**. |
| CS                 | Valiutos simbolis; valiutos formato naudojimas šioje eilutėje | Įtraukite valiutos simbolį į visas neprocentines sumas. Procentinės reikšmės niekada nebūna su valiutos simboliu.                                                                                                                                                                                                                                                                                                |
| XD                 | Eilutės slėpimas sąskaitos informacijos ataskaitoje            | Neleiskite rodyti sąskaitų sąskaitų informacijos aprašuose ir operacijų informacijos aprašuose. Šis spausdinimo valdiklis yra naudingas, kai eilutėje yra kelios sąskaitos, kurios neturėtų būti pateiktos sąskaitos informacijos ataskaitoje arba operacijų informacijos ataskaitoje.                                                                                                                                                           |
| X0                 | Eilutės slėpimas, jei visi nuliai                        | Neįtraukite eilutės į ataskaitą, jei visi tos eilutės langeliai yra tušti arba juose yra nuliai. Šis spausdinimo valdiklis yra prasmingą tik tada, kai ataskaitos apraše parinktis slėpti nulinį balansą nepasirinkta.                                                                                                                                                                                            |
| B0                 | Palikite nulinius stulpelius tuščius                         | Stulpelius eilutėje, kurioje yra sumos, lygios nuliui, palikite tuščius.                                                                                                                                                                                                                                                                                                                                                      |
| XR                 | Sumavimo sustabdymas                                  | Sustabdykite sumavimą. Jei ataskaita naudoja ataskaitų medį, sumos šioje eilutėje nėra sumuojamos, kad būtų gauti pirminiai mazgai.                                                                                                                                                                                                                                                                               |
| SR                 | Apvalinimo sustabdymas                                | Neleiskite, kad sumos šioje eilutėje būtų apvalinamos.                                                                                                                                                                                                                                                                                                                                                          |
| XT                 | Eilutės slėpimas operacijos informacijos ataskaitoje        | Neleiskite rodyti operacijų operacijų informacijos ataskaitose. Šis spausdinimo valdiklis yra naudingas, kai eilutėje yra kelios sąskaitos, kurios neturėtų būti pateiktos operacijų informacijos ataskaitoje.                                                                                                                                                                                                             |

### <a name="conditional-print-control-codes"></a>Sąlyginiai spausdinimo kontroliniai kodai

Toliau pateikiamoje lentelėje aprašomi sąlyginiai eilutės aprašo spausdinimo kontroliniai kodai.

| Spausdinimo kontrolinis kodas | Prekės/Paslaugos pavadinimas                                  |
|--------------------|----------------------------------------------|
| (nėra)             | Išvalyti sąlyginio spausdinimo pasirinkimą.       |
| DR                 | Spausdinti tik šios eilutės debeto balansus.  |
| CR                 | Spausdinti tik šios eilutės kredito balansus. |

## <a name="column-restriction-cell-in-a-row-definition"></a>Eilutės aprašo langelis Stulpelio apribojimas
Eilutės aprašo langelis **Stulpelio apribojimas** turi kelis tikslus. Atsižvelgiant į eilutės tipą, galite naudoti langelį **Stulpelio apribojimas** vienai iš šių funkcijų nurodyti.

-   Langelis gali apriboti eilutės sumų spausdinimą, kad būtų spausdinamos tik sumos konkrečiame stulpelyje. Ši funkcija yra naudinga kuriant lentelės balansą.
-   Langelis gali nurodyti sumų, kurias reikia rūšiuoti, stulpelį.

## <a name="using-a-calculation-formula-in-a-row-definition"></a>Skaičiavimo formulės naudojimas eilutės apraše
Skaičiavimo formulėje eilutės apraše gali būti operatoriai **+**, **-**, **\***, ir **/**, taip pat **IF / THEN / ELSE** sakiniai. Be to, skaičiavimas gali apimti atskirus langelius ir absoliučias sumas (faktinius skaičius, įtrauktus į formulę). Formulę gali sudaryti iki 1024 simbolių. Skaičiavimai negali būti taikomi eilutėms, kuriose yra tipo **Saitas su finansinėmis dimensijomis** (FD) langelių. Tačiau galite įtraukti iš eilės einančių eilučių skaičiavimus, neleisti tų eilučių spausdinti ir tada susumuoti skaičiavimo eilutes.

### <a name="operators-in-a-calculation-formula"></a>Operatoriai skaičiavimo formulėje

Skaičiavimo formulėje naudojami sudėtingesni operatoriai nei eilučių sumos formulėje. Tačiau galite naudoti operatorius **\*** ir **/** kartu su papildomais operatoriais norėdami padauginti (\*) ir padalyti (/) sumas. Norėdami skaičiavimo formulėje naudoti diapazoną arba sumą, turite naudoti ženklą eta (@) prieš bet kokį eilutės kodą, nebent eilutės apraše naudojate stulpelį. Pavyzdžiui, norėdami pridėti 100 eilutės sumą prie 330 eilutės sumos, galite naudoti eilutės sumos formulę **100 + 330** arba skaičiavimo formulę **@100+@330**. **Pastaba.** Turite naudoti ženklą eta (@) prieš kiekvieną eilutės kodą, kurį naudojate skaičiavimo formulėje. Kitu atveju skaičius suprantamas kaip absoliuti suma. Pvz., formulė **@100 + 330** prideda 330 USD prie 100 eilutės sumos. Kai nurodote stulpelį skaičiavimo formulėje, ženklas eta (@) nebūtinas.

### <a name="create-a-calculation-formula"></a>Skaičiavimo formulės kūrimas

1.  Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada atidarykite norimą keisti eilutės apibrėžimą.
2.  Dukart spustelėkite langelį **Formato kodas** ir tada pasirinkite **KPL**.
3.  Langelyje **Susijusios formulės / eilutės / vienetai** įveskite skaičiavimo formulę.

### <a name="example-of-a-calculation-formula-for-specific-rows"></a>Konkrečių eilučių skaičiavimo formulės pavyzdys

Šiame pavyzdyje skaičiavimo formulė **@100 + @330** reiškia, kad 100 eilutės suma pridedama prie 330 eilutės sumos. Eilučių sumos formulė **340 + 370** prideda 340 eilutės sumą prie 370 eilutės sumos. (370 eilutės suma yra suma iš skaičiavimo formulės.)

| Eilutės kodas | Prekės/Paslaugos pavadinimas                 | Formato kodas | Susijusios formulės / eilutės / vienetas | Spausdinimo valdiklis | Eilutės modifikatorius | Saitas su finansinėmis dimensijomis |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Laikotarpio pradžios grynieji pinigai |             |                            | NP            | BB           | +Sąskaita=\[1100:1110\]       |
| 370      | Metų pradžios grynieji pinigai   | KPL         | @100 + @330                  | NP            |              |                              |
| 400      | Laikotarpio pradžios grynieji pinigai | IŠ VISO         | 340 + 370                    |               |              |                              |

Jei eilutės aprašo eilutė turi **KPL** formato kodą ir langelyje **Susijusios formulės / eilutės / vienetai** įvedate matematinį skaičiavimą, taip pat turite įvesti susieto stulpelio raidę ir ataskaitos eilutę. Pavyzdžiui, įveskite **A.120** – tai reiškia A stulpelis, 120 eilutė. Arba galite naudoti ženklą eta (@) visiems stulpeliams nurodyti. Pavyzdžiui, įveskite **@120** – tai reiškia visus 120 eilutės stulpelius. Bet koks matematinis skaičiavimas, neturintis stulpelio raidės arba ženklo eta (@), laikomas realiuoju skaičiumi. **Pastaba**. Jei naudojate žymės eilutės kodą eilutei nurodyti, turite naudoti tašką (.) kaip skyriklį tarp stulpelio raidės ir žymės (pavyzdžiui, **A.BRUTO\_MARŽA/A.PARDAVIMAS)**. Jei naudojate ženklą (@), skyriklis nebūtinas (pavyzdžiui, **@GROSS\_MARGIN/@SALES**).

### <a name="example-of-a-calculation-formula-for-a-specific-column"></a>Konkretaus stulpelio skaičiavimo formulės pavyzdys

Šiame pavyzdyje skaičiavimo formulė **E=C.340** reiškia, kad langelio C stulpelyje ir 340 eilutėje skaičiavimas atliekamas tik stulpelyje E. **Pastaba.** Nurodant stulpelį skaičiavimo formulėje, ženklas eta (@) nebūtinas.

| Eilutės kodas | Prekės/Paslaugos pavadinimas                 | Formato kodas | Susijusios formulės / eilutės / vienetas | Spausdinimo valdiklis | Eilutės modifikatorius | Saitas su finansinėmis dimensijomis |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Laikotarpio pradžios grynieji pinigai |             |                            | NP            | BB           | +Sąskaita=\[1100:1110\]       |
| 370      | Metų pradžios grynieji pinigai   | KPL         | E=C.340                    | NP            |              |                              |
| 400      | Laikotarpio pradžios grynieji pinigai | IŠ VISO         | 340 + 370                    |               |              |                              |

### <a name="modifying-a-number-in-selected-columns"></a>Skaičiaus pasirinktuose stulpeliuose modifikavimas

Kai modifikuojate skaičių arba skaičiavimą viename konkrečios eilutės stulpelyje, tačiau nenorite paveikti kitų ataskaitos stulpelių, eilutės aprašo stulpelyje **Formato kodas** galite nurodyti **SKAIČ.** (skaičiavimas).

-   Norėdami atlikti visų ataskaitos (**FD**) stulpelių skaičiavimą, neįveskite stulpelio priskyrimo.
-   Norėdami taikyti formulę tik tam tikriems stulpeliams, įveskite stulpelio raidę, lygybės ženklą (**=**) ir tada – formulę.
-   Galite nurodyti kelis stulpelius. Naudojant ženklą eta (@) su konkrečia padėtimi stulpelyje, ženklas eta (@) yra susijęs su eilute.
-   Galite įvesti kelias stulpelio formules į vieną eilutę. Atskirkite formules kableliais.

### <a name="calculation-examples"></a>Skaičiavimo pavyzdžiai

| Skaičiavimas            | Sukurtas veiksmas                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| @130\*.75              | Kiekvieno stulpelio reikšmė 130 eilutėje dauginama iš 0,75. Tada rezultatas pateikiamas kiekvieno stulpelio dabartinėje eilutėje. |
| B=@130\*.75            | Tas pats skaičiavimas atliekamas tik stulpelyje B.                                                                      |
| A,B,C=(@100/@130)\*.75 | A=(A.100/A.130)\*.75 B=(B.100/B.130)\*.75 C=(C.100/C.130)\*.75                                                           |

### <a name="ifthenelse-statements-in-a-row-definition"></a>IF / THEN / ELSE sakiniai eilutės apraše

**IF / THEN / ELSE** sakinius galima pridėti prie bet kokio tinkamo skaičiavimo ir naudoti su į **KPL** formatu. Skaičiavimo formulės su **IF / THEN / ELSE** sakiniais įvedamos stulpelio **Susijusios formulės / eilutės / vienetai** langelyje. Skaičiavimo formulės su **IF / THEN / ELSE** sakiniais naudoja tokį formatą: IF &lt;sakinys true / false&gt; THEN &lt;formulė&gt; ELSE &lt;formulė&gt; Sakinio dalis **ELSE &lt;formulė&gt;** yra pasirinktinė.

#### <a name="if-statements"></a>IF sakiniai

Sakinys po **IF** sakinio gali būti bet koks sakinys, kurį galima įvertinti kaip teisingą arba klaidingą. Sakinys po **IF** sakinio gali būti susijęs su paprastu įvertinimu, arba tai gali būti sudėtingas sakinys, galintis turėti kelias išraiškas. Štai keletas pavyzdžių:

-   **IF A.200&gt;0** (paprastas įvertinimas)
-   **IF A.200&gt;0 AND A.200&lt;10,000** (sudėtingas sakinys)
-   **IF A.200&gt;10000 OR ((A.340/B.1200)\*2 &lt;1200)** (sudėtingas sakinys, kuriame yra kelios išraiškos)

Terminas **Laikotarpiai** **IF** sakinyje nurodo ataskaitos laikotarpių skaičių. Šis terminas paprastai naudojamas vidurkiui nuo metų pradžios skaičiuoti. Pavyzdžiui, sudarant 7 laikotarpio nuo metų pradžios ataskaitą, sakinys **B.150/Laikotarpiai** reiškia, kad B stulpelio 150 eilutės reikšmė yra padalinama iš 7.

#### <a name="then-and-else-formulas"></a>THEN ir ELSE formulės

**THEN** ir **ELSE** formulės gali būti bet koks tinkamas skaičiavimas, pradedant labai paprastais reikšmės priskyrimais ir baigiant sudėtingomis formulėmis. Pavyzdžiui, sakinys **IF A.200&gt;0 THEN A=B.200** reiškia „Jei reikšmė A stulpelio 200 eilutės langelyje yra didesnė nei 0 (nulis), pateikite reikšmę iš B stulpelio 200 eilutės langelio dabartinės A stulpelio eilutės langelyje“. Pirmesnis **IF/THEN** sakinys pateikia reikšmę viename dabartinės eilutės stulpelyje. Tačiau įvertinimuose true / false arba formulėje taip pat galite naudoti ženklą eta (@), nurodantį visus stulpelius. Štai keletas kitų pavyzdžių, kurie aprašomi toliau pateikiamuose skyriuose.

-   **IF A.200 &gt;0 THEN B.200**: jei langelio A.200 reikšmė yra teigiama, kiekviename dabartinės eilutės stulpelyje pateikiama B.200 langelio reikšmė.
-   **IF A.200 &gt;0 THEN @200**: jei langelio A.200 reikšmė yra teigiama, atitinkamame dabartinės eilutės stulpelyje pateikiama kiekvieno 200 eilutės stulpelio reikšmė.
-   **IF @200 &gt;0 THEN @200**: jei dabartinio stulpelio 200 eilutėje reikšmė yra teigiama, 200 eilutės reikšmė pateikiama tame pačiame dabartinės eilutės stulpelyje.

### <a name="restricting-a-calculation-to-a-reporting-unit-in-a-row-definition"></a>Skaičiavimo taikymas tik eilutės aprašo ataskaitiniam vienetui

Norėdami taikyti skaičiavimą vienam ataskaitų medžio ataskaitiniam vienetui, kad gauta suma nebūtų sumuojama aukštesnio lygio vieneto sumai gauti, galite eilutės aprašo langelyje **Susijusios formulės / eilutės / vienetai** naudoti kodą **@Unit**. Kodas **@Unit** nurodomas ataskaitų medžio B stulpelyje – **Vieneto pavadinimas**. Naudojant kodą **@Unit** reikšmės nesumuojamos, tačiau skaičiavimas įvertinamas visuose ataskaitų medžio lygiuose. **Pastaba.** Norint naudoti šią funkciją, ataskaitų medis turi būti susietas su eilutės aprašu. Skaičiavimo eilutė gali nurodyti skaičiavimo eilutę arba finansinių duomenų eilutę. Skaičiavimas įrašomas eilutės aprašo langelyje **Susijusios formulės / eilutės / vienetai** ir finansinių duomenų tipo apribojime. Skaičiuojant būtina naudoti sąlyginį skaičiavimą, pradedamą konstrukcija **IF @Unit**. Štai pavyzdys: IF @Unit(PARDAVIMAS) THEN @100 ELSE 0 Šiame skaičiavime naudojama suma iš kiekvieno ataskaitos stulpelio 100 eilutės, bet tik PARDAVIMO vieneto. Jei keli vienetai yra pavadinti PARDAVIMAS, suma rodoma kiekviename iš šių vienetų. Be to, 100 eilutė gali būti finansinių duomenų eilutė ir gali būti apibrėžta kaip nespausdinama. Tokiu atveju sumos neleidžiama rodyti visuose medžio vienetuose. Taip pat galite nustatyti, kad suma būtų rodoma viename ataskaitos stulpelyje, pavyzdžiui, H stulpelyje, naudodami stulpelio apribojimą, kad reikšmė būtų spausdinama tik tame ataskaitos stulpelyje. Galite įtraukti į **IF** sakinį **OR** kombinacijų. Toliau pateikiamas pavyzdys: jei @Unit(PARDAVIMAS) arba @Unit(PARDAVIMASVAKARŲ) tada 5 ELSE @100 galite nurodyti vienetą skaičiavimo tipo apribojimo vienu iš tolesnių būdų.

-   Įveskite vieneto pavadinimą, kad būtų įtraukti atitinkantys vienetai. Pavyzdžiui, **IF @Unit(PARDAVIMAS)** leidžia atlikti kiekvieno vieneto, pavadinto PARDAVIMAS, skaičiavimus, net jei ataskaitų medyje yra keli PARDAVIMO vienetai.
-   Įveskite įmonės ir vieneto pavadinimą, kad skaičiavimas būtų taikomas tik konkretiems konkrečios įmonės vienetams. Pavyzdžiui, įveskite **IF @Unit(ACME:PARDAVIMAS)**, kad skaičiavimas būtų taikomas įmonės ACME PARDAVIMO vienetams.
-   Įveskite visą hierarchijos kodą iš ataskaitų medžio, kad skaičiavimas būtų taikomas konkrečiam vienetui. Pavyzdžiui, įveskite **IF @Unit(SUMMARY^ACME^WEST COAST^SALES)**. **Pastaba.** Norėdami rasti visą hierarchijos kodą, dešiniuoju pelės klavišu spustelėkite ataskaitų medžio aprašą ir tada pasirinkite **Kopijuoti ataskaitinio vieneto identifikatorių (H kodas)**.

#### <a name="restrict-a-calculation-to-a-reporting-unit"></a>Skaičiavimo taikymas tik ataskaitiniam vienetui

1.  Ataskaitos dizaino įrankyje spustelėkite **Eilučių apibrėžimai**, tada atidarykite norimą keisti eilutės apibrėžimą.
2.  Dukart spustelėkite langelį **Formato kodas** ir tada pasirinkite **KPL**.
3.  Spustelėkite langelį **Susijusios formulės / eilutės / vienetai** ir tada įveskite sąlyginį skaičiavimą, pradedamą konstrukcija **IF @Unit**.

### <a name="ifthenelse-statements-in-a-column-definition"></a>IF / THEN / ELSE sakiniai stulpelio apraše

**IF / THEN / ELSE** sakinys leidžia, kad bet koks skaičiavimas priklausytų nuo bet kurio kito stulpelio rezultatų. **IF** sakinyje galite nurodyti kitus stulpelius, bet negalite nurodyti ataskaitos langelio. Skaičiavimas turi būti taikomas visam stulpeliui. Pavyzdžiui, sakinys **IF B&gt;100 THEN B ELSE C\*1.25** reiškia „Jei B stulpelio suma yra didesnė nei 100, pateikti B stulpelio reikšmę stulpelyje **CALC**. Jei B stulpelio suma yra ne didesnė nei 100, dauginti stulpelio C reikšmę iš 1,25 ir pateikti šį rezultatą stulpelyje **SKAIČ.**“. Po **IF** sakinio visada turi būti loginis sakinys, kurį galima įvertinti kaip teisingą arba klaidingą. Formulėse, kurias naudojate tiek **THEN**, tiek **ELSE** sakiniams, gali būti nuorodų į bet kokį skaičių stulpelių, ir šios formulės gali būti kiek norima sudėtingos. **Pastaba.** Negalima pateikti skaičiavimo rezultatų kitame stulpelyje. Rezultatai turi būti stulpelyje, kuriame yra formulė.




