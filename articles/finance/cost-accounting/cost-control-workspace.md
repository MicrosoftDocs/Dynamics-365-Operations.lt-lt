---
title: Savikainos kontrolės darbo sritis
description: Šioje temoje pateikiama informacija apie darbo sritį Savikainos kontrolė. Ši darbo sritis yra centrinis taškas, kuriame už dimensijos arba dimensijų savikainos objekto arba savikainos objektų rinkinį atsakingi vadybininkai gali pasiekti ataskaitas.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfiguration, CAMCostControlWorkspace, CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c54afd0d94a56f6306a11e03448cc66c168390c2
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2020
ms.locfileid: "4446216"
---
# <a name="cost-control-workspace"></a>Savikainos kontrolės darbo sritis 

[!include [banner](../includes/banner.md)]

Darbo sritis **Savikainos kontrolė** yra centrinis taškas, kuriame už dimensijos arba dimensijų (pavyzdžiui, išlaidų centrų ir produktų grupių) savikainos objekto arba savikainos objektų rinkinį atsakingi vadybininkai gali pasiekti ataskaitas. Darbo srityje pateiktas ataskaitas visiškai valdo išlaidų buhalteriai, kad ataskaitoms naudojamas maketas ir duomenys būtų vienodi visoje organizacijoje.

## <a name="cost-control-workspace-configuration"></a>Išlaidų kontrolės darbo srities konfigūracija

Išlaidų buhalteriai gali apibrėžti tiek ataskaitų konfigūracijų, kiek reikia norimai duomenų struktūrai arba maketui. Ataskaitų konfigūraciją sudaro šešios dalys ir kiekviena iš jų naudojama pasirenkant tikslinių duomenų struktūrą arba maketą.

Norėdami konfigūruoti savikainos kontrolės darbo sritį, spustelėkite **Kaštų apskaita**\>**Sąranka**\>**Savikainos kontrolės darbo srities konfigūracija**.

### <a name="general"></a>Bendra

„FastTab“ skirtuke **Bendra** galite sukurti unikalų ataskaitos maketą. Ataskaitos pavadinimas bus unikalus identifikatorius, kurį vartotojai galės atpažinti darbo srityje **Savikainos kontrolė**. Taip pat galite nurodyti, ar ataskaita turėtų būti naudojama bendrai, ar naudojama viduje tik išlaidų buhalteriams.

| Laukas       | aprašymas |
|-------------|-------------|
| Vardas        | Įveskite unikalų maketo pavadinimą. |
| aprašymas | Įveskite išsamų aprašymą. |
| Publikuota   | Jei šiame lauke nustatysite parinktį **Taip**, darbo srityje **Savikainos kontrolė** ataskaitą galės matyti naudotojas, kuriam priskirtas vienas iš šių vaidmenų:<ul><li>Savikainos apskaitos vadovas</li><li>Išlaidų buhalteris</li><li>Išlaidų buhalteris</li><li>Savikainos objekto valdiklis</li></ul>Jei šiame lauke nustatysite parinktį **Ne**, darbo srityje **Savikainos kontrolė** ataskaitą galės matyti tik tie naudotojai, kuriems priskirtas vienas iš šių vaidmenų:<ul><li>Savikainos apskaitos vadovas</li><li>Išlaidų buhalteris</li><li>Išlaidų buhalteris</li></ul> |

### <a name="data-filtering"></a>Duomenų filtravimas

„FastTab“ skirtuke **Duomenų filtravimas** nurodote ataskaitos duomenų pagrindą. Apdorojus šaltinio duomenis šios ataskaitos naudotojai ataskaitoje matys reikšmes.

| Laukas                                                             | aprašymas |
|-------------------------------------------------------------------|-------------|
| Savikainos apskaitos didžioji knyga                                            | **Kaštų apskaitos didžioji knyga** pagal kurią paruošta ataskaita. Vertė išvedama iš lauko **Savikainos kontrolės įtaisas**. |
| Savikainos kontrolės įtaisas                                                 | Nuo pasirinktos vertės priklauso tai, pagal kokią savikainos apskaitos didžiąją knygą ir savikainos objektus bus sudaryta ši ataskaita. |
| Statistinių dimensijų hierarchija. Savikainos elemento dimensijų hierarchija | Darbo srities **Savikainos kontrolė** konfigūracijos įraše gali būti pranešama apie nepinigines arba apie pinigines vertes, bet ne tame pačiame makete. Lauke **Savikainos elemento dimensijų hierarchija** pasirinkite reikšmę, kad būtų parengiama piniginių verčių ataskaita. Lauke **Statistinių dimensijų hierarchija** pasirinkite reikšmę, kad būtų parengiama nepiniginių verčių ataskaita. Nuo pasirinkto dimensijų hierarchijos įrašo priklauso ataskaitų ir telkimo lygių struktūra.<blockquote>[!NOTE]<br>Norėdami peržiūrėti nepinigines ir pinigines vertes vieną šalia kitos, galite eksportuoti duomenis į „Microsoft Power BI“ skirtos programos „Microsoft Excel“ turinio paketą.</blockquote> |
| Savikainos objekto dimensijų hierarchija                                   | Pasirinkite jūsų rengiamų ataskaitų tikslą atitinkančios savikainos objekto dimensijos hierarchiją. |
| Biudžeto pradinė versija                                           | Pasirinkite biudžeto versijos ID, kuri šios ataskaitos kontekste veikia kaip pradinis biudžetas. |
| Biudžeto peržiūrėta versija                                            | Pasirinkite biudžeto versijos ID, kuri šios ataskaitos kontekste veikia kaip patikslintas biudžetas. |

### <a name="assign-calculation-records"></a>Priskirti skaičiavimo įrašus

Atliekant pridėtinių išlaidų skaičiavimą atliekami keli šaltinio duomenų skaičiavimo veiksmai, pvz., išlaidų veikimo būdo klasifikavimas ir išlaidų paskirstymas. Jei aptinkama, kad trūksta šaltinio duomenų, arba būtina atnaujinti taisykles, galima atlikti kelis vieno ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimus. Kiekvienas pridėtinių išlaidų skaičiavimas įrašomas naudojant unikalų ID. Išlaidų buhalteris gali pasirinkti konkretų pridėtinių išlaidų skaičiavimo ID. Ataskaitos naudotojai, pvz., vadovai, pridėtinio skaičiavimo rezultatus matys darbo srityje **Savikainos kontrolė**.

| Laukas                  | aprašymas |
|------------------------|-------------|
| Ataskaitinis kalendorinis laikotarpis | Pasirinkite ataskaitinį kalendoriaus laikotarpį, kuriam priskirsite pridėtinių išlaidų skaičiavimo ID.<blockquote>[!NOTE]<br>Lauke išvardyti ataskaitiniai laikotarpiai gaunami iš finansinio kalendoriaus, kuris susietas su kaštų apskaitos didžiąja knyga.</blockquote> |
| Faktinė versija         | Pasirinkite atitinkamą pridėtinių išlaidų skaičiavimo ID. |
| Biudžeto versija         | Pasirinkite atitinkamą pridėtinių išlaidų skaičiavimo ID. |
| Peržiūrėta biudžeto versija | Pasirinkite atitinkamą pridėtinių išlaidų skaičiavimo ID. |

### <a name="fiscal-periods-per-column"></a>Ataskaitiniai laikotarpiai pagal stulpelį

„FastTab“ skirtuke **Ataskaitinių laikotarpių skaičius stulpelyje** išlaidų buhalteris nusprendžia, koks ataskaitinis laikotarpis turi būti rodomas ataskaitos makete.

Pažymėtų stulpelių vertės bus padaugintos iš „FastTab“ skirtuke **Ataskaitinių laikotarpių skaičius stulpelyje** pasirinktų verčių.

| Laukas                | aprašymas |
|----------------------|-------------|
| Dabartinis laikotarpis       | Rodomas dabartinio ataskaitinio laikotarpio likutis.<blockquote>[!NOTE]<br>Pagal numatytuosius nustatymus dabartinis laikotarpis nustatomas pagal seanso datą. Darbo srityje **Savikainos kontrolė** galima pasirinkti konkretų ataskaitinį laikotarpį. Tada pasirinkta vertė nurodo dabartinį laikotarpį.</blockquote> |
| Ankstesnis laikotarpis      | Rodomas ankstesnio ataskaitinio laikotarpio likutis. Naudojama ši formulė:<br>Dabartinis ataskaitinis laikotarpis – 1<blockquote>[!NOTE]<br>Pagal numatytuosius nustatymus ankstesnis laikotarpis išvedamas pagal seanso datą. Darbo srityje **Savikainos kontrolė** galima pasirinkti konkretų ataskaitinį laikotarpį kaip dabartinį laikotarpį. Tada bus atitinkamai perskaičiuojamas **Ankstesnis laikotarpis**.</blockquote> |
| Metai iki šios dienos         | Rodomi duomenys nuo šių metų pradžios. Naudojama ši formulė:<br>YearToDate (dabartinis ataskaitinis laikotarpis)<blockquote>[!NOTE]<br>Pagal numatytuosius nustatymus dabartinis laikotarpis nustatomas pagal seanso datą. Darbo srityje **Savikainos kontrolė** galima pasirinkti konkretų ataskaitinį laikotarpį. Pasirinkta vertė tada atitinka dabartinį laikotarpį, o vertė **Nuo šių metų pradžios** bus atitinkamai atnaujinta.</blockquote> |
| Vidurkis nuo metų pradžios | Rodomas duomenų nuo šių metų pradžios vidurkis. Naudojama ši formulė:<br>(YearToDate [Dabartinis ataskaitinis laikotarpis]) ÷ (Skaičius [Dabartinis ataskaitinis laikotarpis])<p><strong>Pavyzdys</strong></p><ul><li>**Statistinės dimensijos narys:** visą darbo dieną dirbantys darbuotojai</li><li>**Dabartinė data:** 2017-03-21</li><li>**Laikotarpis:** 1 ataskaitinis laikotarpis, 2 ataskaitinis laikotarpis, 3 ataskaitinis laikotarpis</li><li>**Reikšmė:** 10, 10, 12</li></ul>Šiuo atveju **Vidurkis nuo metų pradžios** = (10 + 10 + 12) ÷ 3 = 10,67<p>Galima apskaičiuoti savikainos elemento dimensijos nariams ir statistinės dimensijos nariams skirtą reikšmę **Vidurkis nuo metų pradžios**.</p><blockquote>[!NOTE]<br>Pagal numatytuosius nustatymus dabartinis laikotarpis nustatomas pagal seanso datą. Darbo srityje **Savikainos kontrolė** galima pasirinkti konkretų ataskaitinį laikotarpį. Pasirinkta vertė tada atitinka dabartinį laikotarpį, o vertės **Nuo šių metų pradžios** ir **Vidurkis nuo metų pradžios** bus atitinkamai atnaujintos.</blockquote> |

### <a name="columns-to-display-for-costs"></a>Rodytini išlaidų stulpeliai

„FastTab“ skirtuke **Rodytini išlaidų stulpeliai** išlaidų buhalteris nusprendžia, kurie stulpeliai turi būti rodomi ataskaitos makete. Yra trys kategorijos: fiksuota savikaina, kintama savikaina ir nesuklasifikuota savikaina.

| Laukas                 | aprašymas |
|-----------------------|-------------|
| Fiksuotos išlaidos            | Šio tipo stulpelyje rodoma fiksuota savikaina pagal pasirinktą pridėtinių išlaidų skaičiavimo ID.<blockquote>[!NOTE]<br>Šio tipo stulpelyje likutis bus rodomas tik tada, kai pasirenkamas ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimo ID.</blockquote> |
| Kintamos išlaidos         | Šio tipo stulpelyje rodoma kintama savikaina pagal pasirinktą pridėtinių išlaidų skaičiavimo ID.<blockquote>[!NOTE]<br>Šio tipo stulpelyje likutis bus rodomas tik tada, kai pasirenkamas ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimo ID.</blockquote> |
| Fiksuota + kintamoji savikaina | Šio tipo stulpelyje rodoma fiksuota savikaina ir kintama savikaina pagal pasirinktą pridėtinių išlaidų skaičiavimo ID.<blockquote>[!NOTE]<br>Šio tipo stulpelyje likutis bus rodomas tik tada, kai pasirenkamas ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimo ID.</blockquote> |
| Bendroji savikaina            | Šio tipo stulpelyje rodoma bendroji savikaina (nesuklasifikuota savikaina, fiksuota savikaina ir kintama savikaina).<blockquote>[!NOTE]<br>Šio tipo stulpelyje visada rodomas likutis.</blockquote> |
| Nesuklasifikuota savikaina     | Šio tipo stulpelyje rodoma nesuklasifikuota savikaina.<blockquote>[!NOTE]<br>Šį stulpelį galima naudoti norint patikrinti, ar visos išlaidos buvo teisingai suklasifikuotos pagal pridėtinių išlaidų skaičiavimą, ar išlaidų veikimo būdo taisykles būtina koreguoti.</blockquote> |

### <a name="columns-to-display-for-budgeted-costs"></a>Rodytini biudžeto išlaidų stulpeliai

„FastTab“ skirtuke **Rodytini biudžeto išlaidų stulpeliai** išlaidų buhalteris nusprendžia, kurie turi būti rodomi pasirinktų biudžeto versijų stulpeliai. Galima atskirai pasirinkti pradinio ir patikslinto biudžeto parinktis.

> [!NOTE]
> Kadangi toliau nurodytų laukų veikimo būdas atitinka pradinio biudžeto ir patikslinto biudžeto veikimo būdą, jie bus paaiškinti tik vieną kartą.

| Laukas                     | aprašymas |
|---------------------------|-------------|
| Biudžetas                    | Biudžeto likučiai bus rodomi pagal pasirinktus stulpelius.<blockquote>[!NOTE]<br>Likučiai priklausys nuo „FastTab“ skirtuke **Duomenų filtravimas** pasirinktų biudžeto versijų.</blockquote> |
| Biudžeto nuokrypis           | Apskaičiuoti ir rodyti skirtumą tarp biudžeto ir faktinės vertės. Naudojama ši formulė:<br>Biudžeto likutis – faktinis likutis |
| Biudžeto nuokrypis %      | Apskaičiuoti ir rodyti skirtumą tarp biudžeto ir faktinės vertės procentais. Naudojama ši formulė:<br>(Biudžeto likutis – faktinis likutis) ÷ biudžeto likutis |
| Nuokrypio laikotarpio ribinė vertė | Nustatyti dabartinio laikotarpio nuokrypio pinigine suma ribinę vertę. Jeigu ribinė vertė viršyta, darbo srityje **Savikainos kontrolė** linija bus paryškinta raudona spalva.<blockquote>[!NOTE]<br>Šis laukas taikomas tik tiems savikainos elementams, kurie atitinka išlaidas.</blockquote> |
| Nuokrypio metų ribinė vertė   | Nustatyti metų laikotarpio nuokrypio pinigine suma ribinę vertę. Jeigu ribinė vertė viršyta, darbo srityje **Savikainos kontrolė** linija bus paryškinta raudona spalva. |
| Nuokrypio ribinė vertė %      | Nustatyti nuokrypio ribinę vertę procentais. Jeigu ribinė vertė viršyta, darbo srityje **Savikainos kontrolė** linija bus paryškinta raudona spalva.<blockquote>[!NOTE]<br>Ta pati procentinė ribinė vertė taikoma dabartiniam laikotarpiui ir metams.</blockquote> |

## <a name="cost-control-workspace"></a>Savikainos kontrolės darbo sritis

Darbo sritis **Savikainos kontrolė** sukurta kaip interneto ataskaita. Todėl visiems vadovams, kurie yra atsakingi už savikainos objektą, gali būti suteikta prieiga, kaip aprašyta dalyje [Savikainos objekto valdiklių prieigos teisių apibrėžimas](access-rights-cost-object-controller.md).

Ataskaitų, kurios galimos naudotojams, pvz., vadybininkams, sąrašas yra kontroliuojamas puslapyje **Savikainos kontrolės darbo srities konfigūracijos** nustatant parinktį **Paskelbta**.

![Ataskaita, kurią naudotojai gali matyti darbo srityje Savikainos kontrolė](./media/report-cost-control.png)

Vadybininkas gali pasirinkti norimą peržiūrėti ataskaitinį kalendoriaus laikotarpį. Seanso data naudojama norint nustatyti numatytąjį dabartinį laikotarpį.

Ataskaitinio kalendoriaus laikotarpio reikšmės nustatomos pagal ataskaitos pavadinimą ir pasirinktą puslapyje **Savikainos kontrolės darbo srities konfigūracijos** su ataskaitos pavadinimu susietos savikainos apskaitos didžiosios knygos ataskaitinį kalendorių.

Savikainos objektų dimensijų hierarchijoje naudotojai gali pasirinkti telkimo lygį, kuriuo turi būti rodomi likučiai. Įgalindami prieigos lygio saugą kontroliuojate leidimus, todėl naudotojai gali pasirinkti tik tuos hierarchijos lygius, prie kurių jiems buvo suteikta prieiga. Todėl jie gali matyti tik sujungtus likučius, prie kurių jiems buvo suteikta prieiga.

### <a name="add-or-remove-columns"></a>Įtraukti arba pašalinti stulpelius

Naudotojai gali pritaikyti ataskaitos stulpelius pagal savo poreikius.

### <a name="view-details"></a>Peržiūrėti informaciją

Naudotojai gali detalizuoti už darbo srityje rodomų likučių esančią informaciją. Jeigu naudotojai pasirenka savikainos elemento dimensijų hierarchijos mazgą, o po to spusteli **Peržiūrėti informaciją**, dialogo lange **Savikainos elemento informacija** rodoma išsami informacija apie mazgą.

Tinklelyje rodomas kiekvienas su išlaidų elemento dimensijų hierarchijos mazgu susietas savikainos elementas ir jo vertės. Tinklelyje rodomi stulpeliai atitinka darbo srities parametrus.

Dviejose diagramose rodoma faktinių duomenų palyginimo su biudžeto duomenimis suvestinė ir biudžeto nuokrypis pagal laikotarpį.

![Diagramos, kuriose rodoma faktinių duomenų palyginimo su biudžeto duomenimis suvestinė ir biudžeto nuokrypis pagal laikotarpį](./media/cost-element-details-operations.png)

Spustelėdami **Savikainos įrašai** naudotojai gali pagal poreikius detalizuoti įrašo informaciją.

![Savikainos įrašai](./media/cost-entries.png)

Pvz., nuoma yra išlaidų centrams paskirstytos išlaidos. Naudotojas, kuris nori suprasti, kokia turi būti jo išlaidų centro nuomos kaina, detalizuodamas informaciją gali pamatyti, kaip apskaičiuota nuoma.

Jeigu naudotojai puslapyje **Savikainos įrašai** spusteli **Paskirstymo bazė**, rodomas dialogo langas. Tada naudotojai gali taisyklei priskirti paskirstymo pagrindą ir peržiūrėti atitinkamus užregistruotus laikotarpio statistinius duomenis.

Toliau pateiktame pavyzdyje paskirstymo pagrindo tipas yra **Formulės paskirstymo pagrindas** ir rodoma formulė. Išvardijami formulę nurodantys koeficientai. Be to, tinklelyje rodomas atliktas kiekvieno išlaidų objekto skaičiavimas.

![Kiekvieno savikainos objekto skaičiavimai](./media/cost-entries-allocation-base.png)

Papildomi ištekliai 

[Savikainos objekto valdiklių prieigos teisių apibrėžimas](access-rights-cost-object-controller.md)


