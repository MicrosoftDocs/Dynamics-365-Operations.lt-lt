---
title: Konsoliduotų finansinių ataskaitų generavimas
description: Šioje temoje aprašomi įvairūs atvejai, kuriais galite generuoti konsoliduotas finansines ataskaitas.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: a32fb8cce4353f57155fc7a723aa90e3c17178e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446044"
---
# <a name="generate-consolidated-financial-statements"></a>Konsoliduotų finansinių ataskaitų generavimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomi įvairūs atvejai, kuriais galite generuoti konsoliduotas finansines ataskaitas.

## <a name="single-level-and-multilevel-consolidations-across-legal-entities"></a>Vieno lygio ir kelių lygių konsolidavimas keliuose juridiniuose subjektuose
Paprasčiausias konsolidavimo naudojant finansines ataskaitas būdas yra naudoti ataskaitų medžius ir agreguoti duomenis visose įmonėse, kurių sąskaitų planai ir ataskaitiniai laikotarpiai sutampa. Toliau nurodyti aukšto lygio veiksmai, skirti konsoliduoti naudojant ataskaitų medį.

1. Sukurkite eilutės aprašą ir įsitikinkite, kad visos atitinkamos sąskaitos visose įmonėse yra įtrauktos į eilutes.
2. Sukurkite stulpelio aprašą, apimantį visus stulpelius, kurie reikalingi kuriamai ataskaitai.
3. Sukurkite ataskaitų medį, apimantį ataskaitų mazgus, skirtus kiekvienai įmonei, kurią naudojate konsoliduotose ataskaitose.

> [!TIP]
> Daugiau informacijos apie tai, kaip kurti ir tvarkyti eilučių aprašus, stulpelių aprašus ir ataskaitų medžius, žr. [Finansinių ataskaitų komponentai](../../dev-itpro/analytics/financial-report-components.md).

Tolesnėje iliustracijoje parodyta, kaip galima naudoti ataskaitų medžio aprašą finansinėse ataskaitose norint nustatyti kiekvieną įmonę, kurią konsoliduosite.

![Ataskaitų medžio apibrėžimas](./media/reporting-tree-definition.png "Ataskaitų medžio apibrėžimas")

Kaip parodyta toliau pateiktos iliustracijos konsoliduotoje ataskaitoje, kai naudojate ataskaitų medį kartu su ataskaitos aprašu, galite peržiūrėti kiekvieną įmonę atskirai. Konsoliduotos sumos rodomos suvestinės lygiu.

![Konsoliduotos sumos suvestinės lygis](./media/consolidate-amount-summary-level.png "Konsoliduotos sumos suvestinės lygis")

Taip pat galite kurti kelių lygių ataskaitų medį, kuris tiek lygių, kiek jums reikia. Toliau pateiktoje iliustracijoje rodomas kelių lygių ataskaitų medžio aprašas, kuriame sumavimas atliekamas pagal viso pasaulio regioną.

![Kelių lygmenų ataskaitų medžio apibrėžimas su kaupimais pagal regioną](./media/multilevel-reporting-tree-definition-roll-ups-worldwide-region.png "Kelių lygmenų ataskaitų medžio apibrėžimas su kaupimais pagal regioną")

Toliau pateiktoje iliustracijoje rodomas kelių lygių ataskaitų medžio aprašas, kuriame sumavimas atliekamas pagal viso funkciją.

![Kelių lygmenų ataskaitų medžio apibrėžimas su kaupimais pagal funkciją](./media/multilevel-reporting-tree-definition-roll-ups-by-function.png "Kelių lygmenų ataskaitų medžio apibrėžimas su kaupimais pagal funkciją")

### <a name="viewing-companies-side-by-side"></a>Vienos šalia kitos įmonių peržiūra
Daugelis klientų renkasi ataskaitas, kuriose įmonės pateikiamos viena šalia kitos, o stulpelyje rodoma konsoliduota bendra suma. Šis formatą lengva sukurti po to, kai sukuriate ataskaitų medį. Toliau nurodyti aukšto lygio veiksmai, skirti peržiūrėti įmones vieną šalia kitos konsoliduotose finansinėse ataskaitose.

1. Sukurkite stulpelio aprašą, kuris apima kiekvienos įmonės stulpelį **Finansinė dimensija**.
2. Naudokite lauką **Ataskaitinis vienetas** ir pasirinkite kiekvieno stulpelio medį ir ataskaitinį vienetą.
3. Pasirinktinai: įtraukite antraščių ir stulpelių.

Toliau nurodytoje iliustracijoje rodomas stulpelio aprašas viena šalia kitos pateikiamų įmonių formatu.

![Stulpelio apibrėžimas gretimu formatu](./media/column-definition-side-by-side-format.png "Stulpelio apibrėžimas gretimu formatu")

## <a name="consolidations-that-use-organization-structures-that-are-created-from-legal-entities"></a>Konsolidavimas naudojant organizacijų struktūras, kurios sukurtos iš juridinių subjektų
Organizacijų hierarchijos, kuriose yra dimensijų arba juridinių subjektų, dinamiškai kuria ataskaitų medžio aprašus finansinėse ataskaitose. Lengvas būdas supaprastinti konsolidacijas yra įtraukti organizacijos hierarchiją į ataskaitą finansinėse ataskaitose. Priklausomai nuo ataskaitos datos, finansinės ataskaitos pasirinks organizacijos hierarchiją įsigaliojimo dieną arba anksčiau, kaip parodyta tolesnėje iliustracijoje.

![Ataskaitų medžio apibrėžimo dinaminis kūrimas](./media/dynamically-create-reporting-tree-definitions.png "Ataskaitų medžio apibrėžimo dinaminis kūrimas")

## <a name="consolidations-that-involve-eliminations"></a>Konsolidavimas, apimantis pašalinimus
Pašalinimo operacijos yra įprasta konsolidavimo proceso dalis. Šiame pavyzdyje penkios sąskaitos pašalinamos konsolidavimo metu: 142600, 211400, 401420, 401180 ir 510820. Įmonės gali nustatyti savo vidinių įmonių sąskaitas skirtingai. Pavyzdžiui, kai kurios įmonės paskutinį skaitmenį nustato kaip 9, jei sąskaita yra naudojama vidinės įmonės operacijose. Nepriklausomai nuo naudojamo metodo, jei žinote vidinių įmonių sąskaitas, galite rodyti pašalinimus savo konsoliduotose finansinėse ataskaitose.

Toliau pateiktoje iliustracijoje rodomas konsoliduotos pelno ataskaitos stulpelio aprašas. Trys vidinių įmonių pelno ir nuostolių sąskaitos nurodytos ir priskirtos kiekvienai įmonei naudojant dimensijos filtrą. Stulpelis D apima pašalinimo sąskaitas, priklausančias tik USMF įmonei, o stulpelis E apima pašalinimus, priklausančius tik DEMF įmonei. Stulpelis D ir stulpelis E yra nustatyti taip, kad jie **nebūtų** spausdinami finansinėje ataskaitoje.

![Stulpelio apibrėžimo konsoliduota pajamų deklaracija](./media/column-definition-consolidated-income-statement.png "Stulpelio apibrėžimo konsoliduota pajamų deklaracija")

Kai sugeneruojama ataskaita, pašalinimo sumos apskaičiuojamos stulpeliuose F, G bei H susumuojamos stulpelyje I. Stulpelis J rodo konsoliduotas sumas. Šios konsolidavimo sumos neapima įmonių USMF, USRT ir DEMF pašalinimų.

> [!TIP]
> Sukurkite antrą ataskaitą, kurioje rodomi tik pašalinimo įrašai, ir naudokite ją ataskaitų grupėje, kuri apima jūsų konsoliduotą ataskaitą. Tokiu būdu turėsite visą būtiną informaciją, reikalingą norint kurti bet kuriuos būtinus žurnalo įrašus.

Toliau pateiktoje iliustracijoje rodoma konsoliduota ataskaita.

![Konsoliduotos ataskaitos pajamų deklaracija](./media/consolidated-report-income-statement.png "Konsoliduotos ataskaitos pajamų deklaracija")

Nesvarbu, ar naudojate sąskaitas, ar dimensijas, ar sąskaitas ir dimensijas, finansinės ataskaitos suteikia galimybę filtruoti pašalinimo įrašus naudojant dimensijos filtravimo galimybes.

## <a name="minority-interest"></a>Segmento palūkanos
Įmonei gali priklausyti tik procentinė kitos įmonės dalis. Tokiu atveju generuojant konsoliduotą ataskaitą svarbu nurodyti tik procentinę dalį, kuri priklauso įmonei. Finansinėse ataskaitose galima rodyti segmento palūkanas keliais būdais, priklausomai nuo vartotojo pasirinkimo. Vienas būdas yra naudoti sumuojamą procentinę dalį ataskaitų medžio apraše. Kitas būdas – rodyti segmento nuosavybę kaip atskirą eilutę ataskaitoje.

### <a name="using-the-reporting-tree-definition"></a>Ataskaitų medžio aprašo naudojimas
Ataskaitų medžio apraše įveskite nuosavybės procentus stulpelyje **Sumavimo %** (stulpelis H), kaip pavaizduota tolesnėje iliustracijoje. Generuojant ataskaitą, šis procentas bus naudojamas konsoliduotai sumai apskaičiuoti. Šiame pavyzdyje „Contoso“ valdo tik 80 procentų įmonės „Contoso Germany“. Stulpelyje **Sumavimo %** galite įvesti **80** arba **.8** ir 80 procentų bus susumuota konsolidavimo lygiu.

> [!NOTE]
> Galite taikyti šį nuosavybės procentą bet kuriam ataskaitų vienetui (ne tik įmonės lygiu). 

![Ataskaitų medžio apibrėžimo procentų naudojimas](./media/Using-reporting-tree-definition-percentage.png "Ataskaitų medžio apibrėžimo procentų naudojimas")

Generuojant ataskaitą įmonės „Contoso Germany“ ataskaitoje bus rodoma 100 procentų pardavimo sumos ir 80 procentų sumos bus paskirstyta bei susumuota pardavimo konsolidavimo lygiu.

Jei jums priklauso mažiau nei 1 procentas įmonės, puslapio **Ataskaitos parametrai** skirtuke **Papildomos parinktys** galite pasirinkti žymės langelį **Leisti sumuoti mažiau nei 1 %**, kaip pavaizduota tolesnėje iliustracijoje. Šiuo atveju reikšmės, pateiktos ataskaitos medžio stulpelyje **Sumavimo %**, bus apdorojamos kaip mažesnės nei 1 procento dalys. Pavyzdžiui, jei įvedate **.8**, 0,8 procentinė dalis bus sumuojama konsolidavimo lygiu (o ne 80 procentų). Tą patį rezultatą galite pasiekti išvalydami žymės langelį **Leisti sumuoti mažiau nei 1 %** ir stulpelyje **Sumavimo %** įvesdami **.008**.

![Ataskaitos nustatymo parinktys](./media/reporting-setting-options.png "Ataskaitos nustatymo parinktys")

### <a name="showing-ownership-as-a-separate-row-on-the-consolidated-report"></a>Nuosavybės rodymas atskiroje konsoliduotos ataskaitos eilutėje
Kita segmento palūkanų rodymo galimybė yra rodyti 100 procentų filialo kiekvienoje ataskaitos eilutėje, tačiau atimti nevaldomas palūkanas iš grynųjų pajamų.

Kaip parodyta tolesnėje iliustracijoje, sakinį **IF THEN ELSE** ir stulpelio apribojimą eilutės apraše galima naudoti skaičiuojant segmento palūkanas finansinėse ataskaitose.

![Nuosavybės rodymas atskiroje konsoliduotos ataskaitos eilutėje](./media/Showing-ownership-separate-row-consolidated-report.png "Nuosavybės rodymas atskiroje konsoliduotos ataskaitos eilutėje")

## <a name="multiple-charts-of-accounts-across-legal-entities"></a>Keli sąskaitų planai keliuose juridiniuose subjektuose
Dažnai skirtingi juridiniai subjektai naudoja skirtingus sąskaitų planus, bet vis tiek nori generuoti konsoliduotas finansines ataskaitas. Tokiu atveju finansines ataskaitas galite naudoti duomenims konsoliduoti, kad galėtumėte generuoti konsoliduotas finansines ataskaitas. Toliau pateikti aukšto lygio veiksmai, skirti konsoliduoti, kai juridiniai subjektai naudoja skirtingus sąskaitų planus.

1. Sukurkite eilučių aprašą, kuriame pateikti keli saitai į finansines dimensijas. Kiekvienam sąskaitų planui turi būti priskirtas vienas saitas.
2. Naudokite ataskaitų vieneto apribojimą stulpelio apraše, kad kiekvienai įmonei priskirtumėte atitinkamą stulpelį.


Į kiekvieną eilutę eilutės apraše galima įtraukti kelis saitus į finansines dimensijas, skirtus kiekvienos unikalios įmonės sąskaitų planams. Tolesnėje iliustracijoje įmonė USMF naudoja sąskaitų rinkinį pirmame stulpelyje **Saitas į finansines dimensijas** (stulpelis J), o įmonė DEMF naudoja sąskaitas antrame stulpelyje **Saitas finansines dimensijas** (stulpelis K).

> [!TIP]
> Daugiau informacijos apie langelį **Saitas į finansines dimensijas** žr. temoje Langelio Finansinių dimensijų saitas nurodymas.

![Sąskaitų pirmo saito į finansinius matmenis nustatymas](./media/set-accounts-first-Link-to-Financial-Dimensions.png "Sąskaitų pirmo saito į finansinius matmenis nustatymas")

Galite naudoti ataskaitų medį norėdami nustatyti, kuris eilutės aprašo saitas į finansines dimensijas naudojamas kiekvienoje įmonėje. Pasirinkite eilutės aprašą stulpelyje E, tada pasirinkite atitinkamą eilutės saitą stulpelyje F, kaip parodyta tolesnėje iliustracijoje.

![Naudotas saito finansinių duomenų eilutės apibrėžimas](./media/link-financial-dimensions-row-definition-used.png "Naudotas saito finansinių duomenų eilutės apibrėžimas")

> [!TIP]
> Kai sukuriate saitus į finansines dimensijas, naudokite aprašymą, kad nustatytumėte įmones, kurioms taikomas kiekvienas saitas. Tokiu būdu galite lengviau pasirinkti teisingą įmonę, kai kuriate ataskaitų medį. Stulpelio aprašo lauke **Ataskaitų vienetas** galite apriboti kiekvieną stulpelį iki ataskaitų medžio vieneto, kad galėtumėte peržiūrėti vienus šalia kitų pateikiamus duomenis. Jei nenurodysite konkrečios stulpelio įmonės, bus rodomi visų įmonių konsoliduoti duomenys.

## <a name="different-fiscal-calendars-across-multiple-legal-entities"></a>Skirtingi finansiniai kalendoriai keliuose juridiniuose subjektuose
Gali būti, kad skirtingi juridiniai subjektai naudoja skirtingus finansinius kalendorius, bet vis tiek privalo generuoti konsoliduotas finansines ataskaitas. Kai juridiniuose subjektuose naudojami skirtingi ataskaitiniai laikotarpiai, konsoliduoti galima dviem būdais.

- Sukurkite stulpelio aprašą ir naudokite laikotarpio bei metus, kad susietumėte atitinkamus kiekvienos įmonės laikotarpius.
- Pasirinkite **Parametrai** \> **Kita** \> **Papildomos pasirinktys**, tada pasirinkite, ar norite konsoliduoti naudodami laikotarpio pabaigos datą, ar laikotarpio numerį.

Kai kuriate stulpelio aprašą, skirtą kelioms įmonėms, kuriose skaičiuojami ataskaitiniai laikotarpiai, svarbu nuspręsti, kuri įmonė bus nurodyta ataskaitos aprašo lauke **Įmonės pavadinimas**. Tos įmonės finansinis kalendorius bus naudojamas kaip pagrindinis ataskaitos aprašo finansinis kalendorius. Pavyzdžiui, toliau pateikiamoje lentelėje parodyta ataskaitinio laikotarpio sąranka, skirta įmonėms USMF ir INMF. Konsoliduotose ataskaitose naudokite finansinį kalendorių, kurį naudoja USMF. Stulpelyje Susiejimas rodomi kiekvienos įmonės atitinkami metai ir laikotarpis, jei ataskaita sugeneruota 2018 m. birželio 30 d.

| Įmonė   | Finansiniai metai                                  | Išdėstymas                     |
|-----------|----------------------------------------------|-----------------------------|
| USMF      | Finansiniai metai, liepos 1 d. – birželio 30 d.          | 12 laikotarpis, 2018 finansiniai metai | 
| INMF      | Kalendoriniai metai, sausio 1 d. – gruodžio 31 d. | 6 laikotarpis, 2018 finansiniai metai  |

Šioje iliustracijoje įmonė USMF nurodyta ataskaitos aprašo lauke **Įmonės pavadinimas**. Todėl įmonės USMF finansinis kalendorius bus naudojamas kaip pagrindinis finansinis kalendorius. Šiame pavyzdyje, kai ataskaita sugeneruojama 2018 m. birželio 30 d., įmonė USMF naudos PAGRINDINĮ laikotarpį, kuris ataskaitos apraše apibrėžiamas kaip 12 laikotarpis. Įmonė INMF naudos 6 PAGRINDINĮ laikotarpį, kuris yra 6 laikotarpis. Abiejuose stulpeliuose bus įtraukti 2018 m. birželio duomenys.

![Ataskaitos pagrindinis periodas](./media/report-base-period.png "Ataskaitos pagrindinis periodas")

Tolesnėje iliustracijoje rodomos ataskaitos aprašo parinktys, kurias naudodami galite pasirinkti, ar konsoliduojant naudojamas laikotarpio numeris, ar laikotarpio pabaigos data.

![Parinkčių ataskaitos apibrėžimo periodo numeris](./media/options-report-definition-period-number.png "Parinkčių ataskaitos apibrėžimo periodo numeris")

## <a name="business-unit-consolidations"></a>Verslo struktūros vienetų konsolidavimas
Šioje temoje pateikiama informacija apie ataskaitų medžio aprašų ir organizacijos hierarchijų naudojimą finansinėse ataskaitose konsolidavimo tikslais. Taip pat galite naudoti ataskaitų medį norėdami kurti verslo vienetų konsolidavimo ataskaitas, pvz., ataskaitas apie pardavimą arba operacijas visame pasaulyje. Šios ataskaitos yra bendras reikalavimas. Norėdami jas kurti, pasirinkite kiekvieno vieneto, kurį norite konsoliduoti, įmonę ir dimensiją. Pvz., tolesnėje iliustracijoje verslo struktūros vieneto sumavimas atliekamas nurodant kiekvieną įmonę stulpelyje **Įmonė** (stulpelyje A) ir nustatant įmonės padalinio dimensijų reikšmių grupę stulpelyje **Dimensijos** (stulpelyje D).

![Verslo vieneto konsolidavimo ataskaitos](./media/business-unit-consolidation-reports.png "Verslo vieneto konsolidavimo ataskaitos")

## <a name="consolidations-that-involve-multiple-reporting-currencies"></a>Konsolidavimas, apimantis kelias ataskaitų valiutas
Finansinės ataskaitos suteikia galimybę padidinti lankstumą, kai peržiūrite faktinius, biudžeto, biudžeto kontrolės ir biudžeto planavimo duomenis keliomis valiutomis. Sujungus pagrindinius sąrankos duomenis, jums nereikia atlikti jokių papildomų sąrankos veiksmų finansinėse ataskaitose, kad peržiūrėtumėte visas ataskaitas – bet kuria valiuta, bet kuriuo metu ir bet kurio vartotojo.

### <a name="prerequisites"></a>Būtinieji komponentai
Siekiant tinkamai apskaičiuoti konvertuotus balansus, finansinių ataskaitų kategorija **Nepaskirstyto pelno sąskaita** turi būti priskirta nepaskirstyto pelno sąskaitai sąraše **Pagrindinėje sąskaitoje**. Finansinės ataskaitos nepalaiko registravimo nepaskirstyto pelno sąskaitoje. Jei operacijos registruojamos nepaskirstyto pelno sąskaitoje, konvertuoti balansai nebus tinkamai apskaičiuoti. Rekomenduojame vartotojams nustatyti papildomą nepaskirstyto pelno sąskaitą norint registruoti koregavimus nepaskirstyto pelno sąskaitoje.

Pagrindinės sąskaitos „FastTab“ **Finansinės ataskaitos** reikia nustatyti kiekvienos sąskaitos laukus **Finansinių ataskaitų valiutos kurso tipas** ir **Valiutos konvertavimo tipas**, kaip parodyta tolesniame pavyzdyje. Šią užduotį galite atlikti nustatydami vieną sąskaitą po kitos arba galite naudoti sąskaitų šablonus ir lengvai taikyti keitimus.

- Lauke **Finansinių ataskaitų valiutos kurso tipas** pasirinkite valiutos kurso tipą, kuris nurodo valiutas ir valiutų kursus, taikytinus sąskaitai. Tolesnė valiutų ir valiutų kursų lentelė bus taikoma faktiniams finansinių ataskaitų duomenims.
- Lauke **Valiutos konvertavimo tipas** pasirinkite sąskaitos valiutos kurso apskaičiavimo metodą. Šis valiutos kurso apskaičiavimo metodas naudojamas faktiniams ir biudžeto duomenims finansinėse ataskaitose skaičiuoti.

![Finansinės ataskaitos pagrindinės sąskaitos](./media/Financial-reporting-main-accounts.png "Finansinės ataskaitos pagrindinės sąskaitos")

Biudžeto, biudžeto kontrolės ir biudžeto planavimo duomenų valiutos kurso tipas nurodomas puslapyje **Didžioji knyga**. Ta lentelė bus naudojama valiutų kursams nustatyti ir bus naudojamas sąskaitai priskirtas valiutos konvertavimo tipas.

### <a name="currency-translation-methods"></a>Valiutos konvertavimo metodai
Valiutų kursus finansinėse ataskaitose galima apskaičiuoti keturiais būdais.

- **Svertinis vidurkis** – šis metodas dažniausiai naudojamas pelno ir nuostolių sąskaitose. Naudojant šį metodą taikoma ši formulė:

    (valiutos kursas x galiojimo dienų skaičius) ÷ dienų skaičius per laikotarpį

- **Vidurkis** – šis metodas yra alternatyvus metodas, naudojamas pelno ir nuostolių sąskaitose. Naudojant šį metodą taikoma ši formulė:

    valiutų kursų suma ÷ valiutos kursų skaičius

- **Dabartinis** – šis metodas dažniausiai naudojamas balanso sąskaitose. Naudojamas valiutos kursas, nustatytas ataskaitos sugeneravimo dieną ar anksčiau, arba naudojami finansinių ataskaitų stulpelio duomenys.
- **Operacijos data** – šis metodas naudojamas ilgalaikio turto sąskaitose. Naudojamas valiutos kursas, nustatytas tą dieną, kurią buvo įsigytas turtas. Jei tos dienos kursas nenurodytas, naudojamas vėliausias anksčiau nurodytas kursas.

### <a name="report-designer-options-for-currency-translation"></a>Ataskaitų dizaino įrankio valiutos konvertavimo parinktys
Finansinėse ataskaitose bet kurią ataskaitą galima pateikti naudojant bet kokį ataskaitų valiutų skaičių. Toliau nurodyti ataskaitos aprašo laukai palaiko šią parinktį.

- Puslapio **Ataskaitos aprašas** skiltis **Valiutos informacija**. Šioje skiltyje rodoma valiuta, kuria reikšmės pateikiamos generuojant ataskaitą.
- Naujas žymės langelis **Įtraukti visas ataskaitų valiutas**. Kai pažymėtas šis žymės langelis, sugeneravus ataskaitą, kurioje naudojama pagrindinė įmonės valiuta, kiekvienos ataskaitų valiutos ataskaita įtraukiama į ataskaitų eilę. Jei žymės langelis nepažymėtas, ataskaitų valiuta vis tiek galite pasirinkti žiniatinklio peržiūros programoje. Šiuo atveju ataskaitų valiuta bus apdorojama tik tada, kai ją pasirinksite.

Ataskaitos aprašo parinktys suteikia galimybę lengvai konvertuoti ataskaitą į visas ataskaitų valiutas. Todėl galėsite panaikinti pasikartojančius ataskaitų aprašus, kurie skiriasi tik naudojama valiuta. Jei reikia ataskaitos, kurioje kelios valiutos pateikiamos viena šalia kitos, galite naudoti puslapio **Stulpelio aprašas** lauką **Valiutos rodymas**, kad į alternatyvią ataskaitų valiutą konvertuotumėte tik tą ataskaitos stulpelį.

### <a name="currency-translation-adjustment"></a>Valiutos konvertavimo koregavimas
Valiutos konvertavimo koregavimas (VKK) yra skirtumas tarp kursų, naudojamų skaičiuojant balanso sąskaitas, ir kurso, naudojamo pajamų išrašo sąskaitose. Dėl šio skirtumo balansas nepateks į balansą. Naudodami finansines ataskaitas galite apskaičiuoti VKK dviem būdais.

- Naudokite eilutės aprašo puslapį **Apvalinimo koregavimai**, kaip pavaizduota tolesnėje iliustracijoje.

    ![Valiutų konvertavimo apvalinimo koregavimas](./media/Currency-translation-adjustment-rounding-adjustments.png "Valiutų konvertavimo apvalinimo koregavimas")

    Kai nurodote eilutę, kurioje turėtų būti rodomas apvalinimo koregavimas (VKK), viso turto eilutę, visų įsipareigojimų bei kapitalo eilutę ir jums tinkančią ribinę reikšmę, finansinės ataskaitos apskaičiuos skirtumą ir nurodys jį pageidaujamoje eilutėje. Eilutė pavadinimu **Apvalinimo koregavimas** bus sukurta ir rodoma detalizavimo skiltyje, kaip pavaizduota tolesnėje iliustracijoje.

    ![Apvalinimo koregavimo detalizavimas](./media/rounding-adjustment-drill-down.png "Apvalinimo koregavimo detalizavimas")

- Pateikite visas sąskaitas diapazone iš turto į išlaidas. Kaip parodyta tolesnėje iliustracijoje, skirtumas bus tokia pati suma kaip apvalinimo koregavimas (VKK). Todėl galite ją naudoti kaip patikrintą bendrą sumą, norėdami įsitikinti, kad apvalinimo koregavimo puslapyje nepateikiami jokie trūkstami sąskaitos balansai.

    ![Apvalinimo koregavimo formos patikrinimas](./media/rounding-adjustment-form-check.png "Apvalinimo koregavimo formos patikrinimas")

### <a name="balance-calculation-approach"></a>Balanso skaičiavimo metodas
Finansinės ataskaitos naudoja toliau nurodytus balansų skaičiavimo metodus, kad sumos būtų tinkamai konvertuotos, kai naudojamos valiutos.

- **Svertinis vidurkis ir vidurkis** – kiekvienas laikotarpis apskaičiuojamas pagal jo svertinį vidurkį ir susumuojamas stulpeliuose, pvz., ketvirčio ir metų iki dabartinės datos stulpeliuose.
- **Retrospektyviniai duomenys** – bet kurioje sąskaitoje, kurioje naudojamas praeities konvertavimo metodas, visada naudojama operacijos data. Jei įsigijimo data yra susijusi su operacija, ta data naudojama valiutos kursui nustatyti. Tada kiekvienas laikotarpis susumuojamas ir duomenys išsaugomi siekiant sumažinti skaičiavimo trukmę.
- **Dabartinis** – apskaičiuotų ir bendrų sumų stulpeliai, pvz., ketvirčio ir metų iki dabartinės datos stulpeliai, apskaičiuojami naudojant momentinį kursą, kuris nustatomas stulpelyje arba ataskaitoje. Pvz., stulpelyje **1 ketvirtis** bus naudojamas kovo 31 d. kursas, jei naudojami kalendoriniai metai.

## <a name="additional-resources"></a>Papildomi ištekliai

Daugiau informacijos apie konsolidavimą ir valiutų konvertavimą žr. pagrindinėje šios temos temoje [Finansinio konsolidavimo ir valiutų konvertavimo apžvalga](./financial-consolidations-currency-translation.md).

Daugiau informacijos apie tai, kaip įvesti konsolidavimo informaciją internete, žr. [Internetinis finansinis konsolidavimas](./consolidate-online.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]