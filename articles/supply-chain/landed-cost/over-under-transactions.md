---
title: Perviršio / trūkumo operacijos
description: Šioje temoje pateikiama informacija, kuri padės jums nustatyti perviršio / trūkumo operacijų strategijų informaciją, kad sistema galėtų nustatyti, kaip valdyti prekių perviršio apdorojimą ir trūkumo apdorojimą gavimo metu.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMOverUnderTrans, ITMOverUnderToleranceTable, ITMOverUnderReasonTable, ITMOverUnderToleranceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 63ba27d3fe10441f5e0ad54e684aa6799b521c7a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687846"
---
# <a name="overunder-transactions"></a>Perviršio/trūkumo operacijos

[!include [banner](../../includes/banner.md)]

Kai reiso užsakymai apdorojami, sistema tikisi, kad galutiniame paskirties sandėlyje gautas vartojimo prekių kiekis atitinka kiekį, nurodytą pirkimo užsakymo eilutėse, kurios susietos su reisu. Tačiau, kadangi tikslus pirkimo užsakymo eilutėse nurodytas kiekis ne visada gaunamas sandėlyje, modulis **Iškrovimo kaina** apibrėžia taisyklių, naudojamų valdant prekių perviršio ar trūkumo apdorojimą, rinkinį. Šios taisyklės itin svarbios, nes pradinio pirkimo užsakymo SF išrašyta ir jos nebegalima modifikuoti. Nustatydami perviršio / trūkumo operacijų strategijų informaciją, įgalinate sistemą, kad ji galėtų nustatyti, kaip valdyti prekių perviršio apdorojimą ir trūkumo apdorojimą gavimo metu. Atsargų perviršį ir trūkumą galite valdyti ir rankiniu būdu, naudodami puslapį **Perviršio / trūkumo operacijos**.

## <a name="overunder-tolerances"></a>Perviršio / trūkumo nuokrypiai

Nustatykite leistinus pristatymo perviršio ir trūkumo nuokrypius, norėdami nurodyti perviršio ir trūkumo kiekius arba tūrius, kuriuos galima apdoroti reiso metu nesukeliant klaidos. Jei reiso eilutėje nurodytas gavimo kiekis nepatenka į šių nuokrypių aprėptį, jį reikia modifikuoti ir išspręsti prieš uždarant reiso eilutę vėlesniam apdorojimui.

Norėdami konfigūruoti leistinus nuokrypius, eikite į **Iškrovimo kaina \> Perviršio / trūkumo nustatymas \> Leistini perviršio / trūkumo nuokrypiai**. Ten galite peržiūrėti, redaguoti, įtraukti ir pašalinti leidžiamo nuokrypio įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | Aprašymas |
|---|---|
| Sąskaitos kodas | <p>Apibrėžkite tiekėjų, kuriems taikomas leistinas nuokrypis, aprėptį, pasirinkdami vieną iš toliau pateiktų reikšmių.</p><ul><li>**Lentelė** – leistinas perviršio / trūkumo nuokrypis taikomas tik tiekėjui, pasirinktam eilutėje.</li><li>**Grupė** – leistinas perviršio / trūkumo nuokrypis taikomas visiems leistino tiekėjų nuokrypio grupės, pasirinktos eilutėje, tiekėjams.</li><li>**Visi** – leistinas perviršio / trūkumo nuokrypis taikomas visiems tiekėjams.</li></ul> |
| Sąskaitos ryšys | Pasirinkite tiekėją arba tiekėjų grupę, kuriai taikomas leistinas perviršio / trūkumo nuokrypis, atsižvelgdami į reikšmę, kurią pasirinkote lauke **Sąskaitos kodas**. |
| Prekės kodas | <p>Apibrėžkite prekių, kurioms taikomas leistinas nuokrypis, aprėptį, pasirinkdami vieną iš toliau pateiktų reikšmių.</p><ul><li>**Lentelė** – leistinas perviršio / trūkumo nuokrypis taikomas tik prekei, pasirinktai eilutėje.</li><li>**Grupė** – leistinas perviršio / trūkumo nuokrypis taikomas visoms leistino prekių nuokrypio grupės, pasirinktos eilutėje, prekėms.</li><li>**Visi** – leistinas perviršio / trūkumo nuokrypis taikomas visoms prekėms.</li></ul> |
| Prekės ryšys | Pasirinkite prekę arba prekių grupę, kuriai taikomas leistinas perviršio / trūkumo nuokrypis, atsižvelgdami į reikšmę, kurią pasirinkote lauke **Prekės kodas**. |
| Sumos leidžiamas nuokrypis | Įveskite visam pirkimo užsakymui taikomą leistiną sumos nuokrypį. |
| Procentinis leistinas nuokrypis | Įveskite atskirai pirkimo užsakymo eilutei taikomą leistiną procentinį nuokrypį. |

## <a name="overunder-reasons"></a>Perviršio / trūkumo priežastys

Kai kiekio perviršis / trūkumas susietas su gauta reiso eilute, gali tekti nustatyti kiekio perviršio / trūkumo priežastį. Tokiu atveju gavimo eilutėje galite pasirinkti pristatymo perviršio / trūkumo priežastį, kai prekės gautos.

Norėdami nustatyti pristatymo perviršio / trūkumo priežastis, eikite į **Iškrovimo kaina \> Perviršio / trūkumo nustatymas \> Perviršio / trūkumo priežastys**. Ten galite peržiūrėti, redaguoti, įtraukti ir pašalinti galimas pristatymo perviršio / trūkumo priežastis. Šioje lentelėje apibūdinami galimi kiekvienos priežasties laukai.

| Laukas | Aprašymas |
|---|---|
| Priežasties perviršis/trūkumas | Įveskite unikalų perviršio ar trūkumo operacijos priežasties pavadinimą. |
| Aprašymas | Įveskite perviršio / trūkumo priežasties aprašymą. |
| Judėjimas | Pasirinkite judėjimo žurnalą, susietą su perviršio / trūkumo priežastimi. Šiame lauke pateikiami visi galimi žurnalai, kurių žurnalo tipas yra *Judėjimas* puslapyje **Atsargų žurnalų pavadinimai** (**Atsargų valdymas > Sąranka \> Žurnalų pavadinimai \> Atsargos**). |

## <a name="item-overunder-tolerance-groups"></a>Prekės perviršio / trūkumo leistino nuokrypio grupės

Prekės, kurių leistini nuokrypiai panašūs, gali būti sugrupuotos kartu. Tokiu būdu galite tuo pačiu metu nustatyti visų tos grupės prekių leistiną perviršio / trūkumo nuokrypį.

Norėdami nustatyti prekių leistino perviršio / trūkumo nuokrypio grupes, eikite į **Iškrovimo kaina \> Perviršio / trūkumo nustatymas \> Prekių leistino perviršio / trūkumo nuokrypio grupės**. Ten galite peržiūrėti, redaguoti, įtraukti ir pašalinti leistino perviršio / trūkumo nuokrypio grupių įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | aprašymas |
|---|---|
| Perviršio / trūkumo nuokrypio grupė | Įveskite unikalų grupės pavadinimą. Pasirinkite pavadinimą, aprašantį nuokrypį, pvz., *1% Var*. |
| Aprašymas | Įveskite grupės aprašą. |

## <a name="vendor-overunder-tolerance-groups"></a>Tiekėjo perviršio / trūkumo nuokrypio grupės

Galite sugrupuoti tiekėjus, kurie reguliariai vykdo pristatymo perviršį arba trūkumą. Tada galite nustatyti kiekvienos grupės leistiną perviršio / trūkumo nuokrypį.

Norėdami nustatyti tiekėjų leistino perviršio / trūkumo nuokrypio grupes, eikite į **Iškrovimo kaina \> Perviršio / trūkumo nustatymas \> Tiekėjų leistino perviršio / trūkumo nuokrypio grupės**. Ten galite peržiūrėti, redaguoti, įtraukti ir pašalinti leistino perviršio / trūkumo nuokrypio grupių įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | Aprašymas |
|---|---|
| Perviršio / trūkumo grupės | Įveskite unikalų grupės pavadinimą. Pasirinkite pavadinimą, apibūdinantį grupei priklausančių tiekėjų tipą. |
| Aprašymas | Įveskite grupės aprašą. |

## <a name="view-and-process-overunder-transactions"></a>Perviršio / trūkumo operacijų peržiūra ir apdorojimas

Perviršio / trūkumo operacijos generuojamos, kai atidėtų prekių kiekis neatitinka inicijuoto kiekio. Gavimo žurnale nurodytas kiekis turėtų būti atnaujintas tik atidėtu kiekiu.

Kai reiso eilučių gavimas apdorojamas, tiekėjui galima nustatyti leistinus perviršio / trūkumo nuokrypius. Tada prekės bus peržiūrėtos ir patikrintos. Nuokrypį galima nustatyti procentais, suma vietos valiuta arba abiem būdais.

Jei gauta prekė patenka į leistino nuokrypio aprėptį, sistema sugeneruos judėjimo žurnalą. Šį žurnalą galima nurodyti reiso parametrų puslapyje. Be to, bus sukurta per perviršio / trūkumo operacija. Pavyzdžiui, užsakymo vertė yra 100 $, gavimo vertė – 99 $, o šios vertės atitinka leistino nuokrypio taisykles. Tokiu atveju bus sukurtas prekių kiekio trūkumo neigiamo judėjimo žurnalas.

Jei gauta prekė nepatenka į leistino nuokrypio aprėptį, sistema sugeneruos kiekio skirtumo perviršio / trūkumo operaciją.

Norėdami peržiūrėti ir apdoroti perviršio / trūkumo operacijas, eikite į **Iškrovimo kaina \> Užklausos \> Perviršio / trūkumo operacijos**. Ten perviršio / trūkumo operacija bus susieta su visomis reiso prekėmis, kurių yra per daug arba trūksta. Rekomenduojame naudoti puslapį **Perviršio / trūkumo operacijos**, kad išspręstumėte visas perviršio / trūkumo operacijas, susijusias su reisais. Taip pat rekomenduojame **nenaudoti** judėjimo ar skaičiavimo žurnalų norint rankiniu būdu išspręsti sandėlio pristatymo trūkumo operacijas. Vietoje jų naudokite puslapį **Perviršio / trūkumo operacijos**, norėdami valdyti sandėlio pristatymo kiekių trūkumą.

### <a name="upper-overview-tab"></a>Viršutinis skirtukas Apžvalga

Norėdami peržiūrėti perviršio / trūkumo operacijas, pasirinkite skirtuką **Apžvalga**, esantį viršutinėje puslapio **Perviršio / trūkumo operacijos** dalyje. Šioje lentelėje apibūdinami galimi tinklelio laukai.

| Laukas | Aprašymas |
|---|---|
| Perviršio/trūkumo operacijos numeris | Unikalus perviršio / trūkumo operacijos įrašo pavadinimas, kuris buvo automatiškai sukurtas apdorojant gavimo žurnalą. |
| Reisas | Reisas, prie kurio buvo pridėta pirkimo eilutė. |
| Gabenimo konteineris | Konteineris, prie kurio buvo pridėta pirkimo eilutė. |
| Atvykimo žurnalas | Gavimo žurnalas, pagal kurį buvo sugeneruota perviršio / trūkumo eilutė. |
| Nuoroda | Nuoroda į pirkimo užsakymą arba perkėlimo užsakymą, susijusį su perviršio / trūkumo operacija. |
| Numeris | Pirkimo užsakymas, nurodytas perviršio / trūkumo operacijoje. |
| Tiekėjo kodas | Tiekėjas, su kuriuos susijęs perviršis arba trūkumas. |
| Tranzito prekių numeris | Tranzito prekių numeris, jei taikoma. |
| Prekės Nr. | Prekės numeris, su kuriuos susijęs perviršis arba trūkumas. |
| Pradinis kiekis | Pradinis prie siuntos pridėtas ir pirkimo užsakymo eilutėje nurodytas kiekis. |
| Gautas kiekis | Faktinis gautas kiekis. |
| Skirtumas | Skirtumas tarp numatomos gavimo žurnalo sumos ir sumos, užregistruotos gavimo žurnale. Neigiama vertė nurodo pristatomų prekių perviršį. |
| Likęs kiekis | Kiekis, likęs gavimo žurnalo eilutėje. |
| Pristatymo perviršis/trūkumas | Vertė, nurodanti, ar yra gauto kiekio perviršis, ar trūkumas. |
| Būsena | Perviršio / trūkumo operacijos būsena. Atsižvelgiant į parametrus puslapyje **[Iškrovimo kainos parametrai](landed-cost-parameters.md)**, dėl pristatymo perviršio gali būti automatiškai sukurtas ir įregistruotas pristatymo perviršio kiekio judėjimo žurnalas. Tokiu atveju perviršio / trūkumo operacijos būsena bus *Baigta*. Jei reikia atlikti veiksmą, kad prekės būtų perkeltos iš trūkstamo pristatymo kiekio sandėlio, įrašo būsena bus *Apdorojama*. |
| Priežasties perviršis/trūkumas | Priežastis, susieta su perviršio / trūkumo operacija. |
| Kitos atsargų dimensijos | Jei reikia, tinklelyje galite rodyti papildomų dimensijų stulpelius. Šios dimensijos apima paketo numerį, atsargų būseną ir sandėlį. Veiksmų srityje pasirinkite **Atsargos \> Rodymo dimensijos**, norėdami atidaryti dialogo langą, kuriame galėsite pasirinkti, kurias dimensijas įtraukti. |

### <a name="upper-general-tab"></a>Viršutinis skirtukas Bendra

Norėdami peržiūrėti daugiau informacijos apie eilutę, šiuo metu pasirinktą viršutiniame skirtuke **Apžvalga**, viršutinėje puslapio **Perviršio / trūkumo operacijos** dalyje pasirinkite skirtuką **Bendra**. Šiame skirtuke pateikiama informacija apima visų galimų dimensijų vertes. Ši informacija gauta iš pradinio pirkimo užsakymo.

### <a name="lower-overview-tab"></a>Apatinis skirtukas Apžvalga

Norėdami peržiūrėti eilutės, pasirinktos viršutiniame skirtuke **Apžvalga**, dokumento tipą, apatinėje puslapio **Perviršio / trūkumo operacijos** dalyje pasirinkite skirtuką **Apžvalga**. Toliau pateikiamoje lentelėje aprašomi laukai, kuriuos galima naudoti.

| Laukas | aprašymas |
|---|---|
| Naujo dokumento tipas | Šis laukas nustatytas į *Judėjimo žurnalas* arba *Pirkimo užsakymas*, atsižvelgiant į veiksmą, rodomą pasirinktoje perviršio / trūkumo operacijos eilutėje. |
| Numeris | Nuoroda ir saitas į pirkimo užsakymą arba judėjimo žurnalą, susijusį su pasirinkta perviršio / trūkumo operacijos eilute. |
| Priežasties perviršis/trūkumas | Priežastis, susieta su pasirinkta perviršio / trūkumo operacijos eilute. |
| Kiekis | Kiekis, kurį pasirinkote pirkimo užsakyme arba judėjimo žurnale, susijusiame su pasirinkta perviršio / trūkumo operacijos eilute. |

### <a name="lower-general-tab"></a>Apatinis skirtukas Bendra

Norėdami peržiūrėti perviršio / trūkumo operacijos numerį, partijos ID ir dimensijos numerį, susietus su pasirinkta perviršio / trūkumo operacijos eilute, pasirinkite skirtuką **Bendra**, esantį apatinėje puslapio **Perviršio / trūkumo operacijos** dalyje. 

### <a name="process-overunder-transactions"></a>Perviršio / trūkumo operacijų apdorojimas

Puslapio **Perviršio / trūkumo operacijos** veiksmų sritis pateikia toliau pateiktas komandas, skirtas puslapyje pasirinktoms operacijoms apdoroti. Kiekviena komanda leidžia pasirinkti, kaip apdoroti kiekvieną operaciją.

- **Kurti \> Judėjimas** – kurkite ir užregistruokite pasirinktos operacijos judėjimo žurnalą. Automatiškai sukuriamas ir užregistruojamas trūkumo operacijų judėjimo žurnalas, kuriame nurodomas skirtumas tarp numatomo ir faktinio gauto kiekio. Pasirinkite šią perviršio operacijų komandą, jei norite, kad tiekėjas realizuotų savikainos skirtumą.
- **Kurti \> Pirkimo užsakymas** – kurkite pirkimo užsakymą, skirtą skirtumui tarp numatomo kiekio ir faktinio pasirinktos operacijos gauto kiekio nurodyti. Pasirinkite šią perviršio operacijų komandą, jei jūsų organizacija realizuos savikainos skirtumą.
- **Kurti \> Perkelti į paskirties vietą** – ši komanda taikoma tik perkėlimo užsakymams. Pasirinkite, jei norite perkelti perteklinį arba trūkstamą kiekį į paskirties sandėlį.
- **Kurti \> Perkelti į kilmės vietą** – ši komanda taikoma tik perkėlimo užsakymams. Pasirinkite, jei norite perkelti perteklinį arba trūkstamą kiekį į kilmės sandėlį.
