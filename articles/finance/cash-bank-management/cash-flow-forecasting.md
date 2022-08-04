---
title: Grynųjų pinigų srautų prognozavimas
description: Šiame straipsnyje pateikta pinigų srautų prognozės proceso apžvalga. Taip pat paaiškinama, kaip pinigų srautų prognozės integruojamos į kitus sistemos modulius.
author: angelad116
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: d76e47fc1456dfab7606f337f070a149b0c8e586
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151947"
---
# <a name="cash-flow-forecasting"></a>Grynųjų pinigų srautų prognozavimas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Naudodami pinigų srautų prognozavimo įrankius galite analizuoti būsimam pinigų srautui ir valiutai keliamus reikalavimus, kad galėtumėte įvertinti būsimą įmonės grynųjų pinigų poreikį. Norėdami gauti pinigų srautų prognozę, turite atlikti šias užduotis:

- Nurodyti ir išvardyti visas likvidumo sąskaitas. Likvidumo sąskaitos yra įmonės grynųjų pinigų arba grynųjų pinigų atitikmenų sąskaitos.
- Sukonfigūruoti įmonės likvidumo sąskaitas įtakojančių operacijų prognozių veikimo būdą.

Atlikę šias užduotis galėsite skaičiuoti ir analizuoti pinigų srautų ir būsimai valiutai keliamų reikalavimų prognozes.

## <a name="cash-flow-forecasting-integration"></a>Pinigų srauto prognozės integravimas

Pinigų srauto prognozę galima integruoti į didžiąją knygą, mokėtinas sumas, gautinas sumas, biudžetą ir atsargų valdymą. Prognozavimo procesas naudoja į sistemą įvestą operacijos informaciją ir skaičiavimo procesas prognozuoja numatomą kiekvienos operacijos grynųjų pinigų poveikį. Skaičiuojant pinigų srautą atsižvelgiama į šių tipų operacijas:

- **Pardavimo užsakymai** – Pardavimo užsakymai, kuriems dar neišrašyta SF ir kurie yra faktinio arba finansinio pardavimo priežastis.
- **Laisvos formos SF** – laisvos formos SF, kurios dar neužregistruotos ir kurios yra finansinio pardavimo rezultatas. 
- **Pirkimo užsakymai** – Pirkimo užsakymai, kuriems dar neišrašyta SF ir kurie yra faktinio arba finansinio pirkimo priežastis.
- **Gautinos sumos** – Atviros kliento operacijos (dar neapmokėtos SF).
- **Mokėtinos sumos** – Atviros tiekėjo operacijos (dar neapmokėtos SF).
- **DK operacijos** – Operacijos, kuriose nurodoma, kad ateityje bus atliekamas registravimas.
- **Biudžeto registro įrašai** – Pinigų srautų prognozėms pasirinkti biudžeto registro įrašai.
- **Poreikio prognozės** – Pinigų srautų prognozėms pasirinktos atsargų prognozės modelio eilutės.
- **Tiekimo prognozės** – Pinigų srautų prognozėms pasirinktos atsargų prognozės modelio eilutės.
- **Išorinis duomenų šaltinis** – išoriniai duomenys, kurie įvesti ar importuoti į pinigų srautų prognozes naudojant skaičiuoklės šablonus.
- **Projekto prognozės** – projektų valdymo ir apskaitos prognozės, naudojant prognozės modelį.
- **Pinigų srautų PVM institucijos mokėjimai** – numatytos PVM institucijos mokėjimų sumos ir laikas, dėl kurių atliekami finansiniai mokėjimai. Įgalinkite funkciją Pinigų srautų PVM institucijos mokėjimai.

## <a name="configuration"></a>Konfigūracija

Norėdami sukonfigūruoti pinigų srautų prognozės procesą, naudokite puslapį **Grynųjų pinigų srauto prognozės nustatymas**. Šiame puslapyje nurodote sekamas likvidumo sąskaitas ir numatytąsias kiekvienos srities prognozės elgsenas.

### <a name="general-ledger"></a>DK

Pirmiausia turite nurodyti likvidumo sąskaitas, kurias norite sekti naudodami pinigų srauto prognozes. Paprastai šios likvidumo sąskaitos yra pagrindinės sąskaitos, susietos su banko sąskaitomis, kurios gaus ir išmokės grynuosius pinigus. Puslapio **Pinigų srauto prognozės nustatymas** skirtuke **Didžioji knyga** pasirinkite pagrindines į prognozę įtrauktinas sąskaitas. Jei banko sąskaita susieta su pagrindine puslapyje **Banko sąskaita** nurodyta sąskaita, ji rodoma lauke **Banko sąskaita**.

Galite nustatyti priklausomas pinigų srautų prognozes pagrindinėse sąskaitose, kuriose yra operacijų, tiesiogiai susijusių su operacijomis, esančiomis kitoje pagrindinėje sąskaitoje. Kiekvieną kartą į dalį **Priklausomose sąskaitose** įtraukus eilutę priklausomoje pagrindinėje sąskaitoje sukuriama pinigų srautų prognozės suma. Ši suma yra jūsų pasirinktos pirminės pagrindinės sąskaitos pinigų srautų sumos procentas.

Pirmiausia nustatykite, kad lauke **Pagrindinė sąskaita** būtų rodoma pirminė pagrindinė sąskaita, kurioje tikimasi, kad bus vykdomos operacijos. Nustatykite, kad lauke **Priklausoma pagrindinė sąskaita** būtų rodoma sąskaita, kuriai turės įtakos pirminei pagrindinei sąskaitai atlikta pradinė operacija. Nustatykite tinkamas kitų eilutės laukų reikšmes. Norėdami parodyti pirminės pagrindinės sąskaitos poveikį priklausomai pagrindinei sąskaitai, galite pakeisti lauke **Procentas** nurodytą reikšmę. Pardavimo arba pirkimo prognozei pasirinkite tokią **Mokėjimo sąlygos** vertę, kuri būdinga daugumai klientų arba tiekėjų. Lauke **Registravimo tipas** nustatykite numatomą registravimo tipą, kuris yra susijęs su pinigų srautų prognoze.

### <a name="accounts-payable"></a>Mokėtinos sumos

Pirkimo prognozę galite apskaičiuoti naudodami puslapio **Pinigų srauto prognozės sąranka** skirtuke **Mokėtinos sumos** nurodytas nustatymo pasirinktis. Prieš konfigūruodami mokėtinų sumų pinigų srautų prognozavimą turite sukonfigūruoti mokėjimo sąlygas, tiekėjų grupes ir tiekėjų registravimo šablonus.

Dalyje **Numatytosios pirkimo prognozės nuostatos** galite pasirinkti numatytuosius pirkimo veiksmus, susijusius su pinigų srautų prognozėmis. Trijuose laukuose nurodomas grynųjų pinigų poveikio laikas: **Laikotarpis nuo pristatymo datos iki SF datos**, **Mokėjimo sąlygos**, ir **Laikotarpis nuo SF termino iki mokėjimo datos**. Prognozėje numatytosios lauko **Mokėjimo sąlygos** bus naudojamos tik tada, jeigu reikšmė nenurodyta operacijoje. Norėdami aprašyti kiekvienai proceso daliai būdingiausią dienų skaičių, naudokite mokėjimo sąlygą.

Lauke **Mokėjimų likvidumo sąskaitos** nurodoma dažniausiai mokėjimams naudojama likvidumo sąskaita. Lauką **Grynųjų pinigų srautų prognozei paskirstytina procentinė suma** naudokite norėdami nurodyti, ar atliekant prognozavimą turi būti naudojama tam tikra procentinė suma. Jeigu atliekant prognozavimą turi būti naudojamos visos operacijos sumos, palikite šį lauką tuščią.

Galite nepaisyti numatytosios specialioms tiekėjų grupėms skirto lauko **Laikotarpis nuo SF termino iki mokėjimo datos** nuostatos. Prognozė naudos numatytąją dalyje **Numatytosios pirkimo prognozės nuostatos** nurodytą reikšmę, nebent būtų nurodyta kita su operacijoje dalyvaujančiu tiekėju susijusios tiekėjų grupės reikšmė. Norėdami nepaisyti numatytosios reikšmės, pasirinkite tiekėjų grupę, o po to nustatykite naują lauko **Pirkimo laikas** reikšmę.

Galite nepaisyti numatytosios specialiems tiekėjo registravimo šablonams naudojamo lauko **Likvidumo sąskaita** nuostatos. Prognozė naudos numatytąją dalyje **Numatytosios pirkimo prognozės nuostatos** nurodytą reikšmę, nebent būtų nurodyta kita su operacijoje dalyvaujančiu tiekėju susijusio registravimo šablono likvidumo sąskaita. Norėdami nepaisyti numatytosios reikšmės, pasirinkite registravimo šabloną, o po to nurodykite likvidumo sąskaitą, kuri turėtų būti paveikta.

### <a name="accounts-receivable"></a>Gautinos sumos

Pardavimo prognozę galite apskaičiuoti naudodami puslapio **Pinigų srauto prognozės sąranka** skirtuke **Gautinos sumos** nurodytas nustatymo pasirinktis. Prieš konfigūruodami gautinų sumų pinigų srautų prognozavimą turite sukonfigūruoti mokėjimo sąlygas, klientų grupes ir klientų registravimo šablonus.

Dalyje **Numatytosios pardavimo prognozės nuostatos** galite pasirinkti numatytuosius pardavimo veiksmus, susijusius su pinigų srautų prognozėmis. Trijuose laukuose nurodomas grynųjų pinigų poveikio laikas: **Laikotarpis nuo siuntimo datos iki SF datos**, **Mokėjimo sąlygos**, ir **Laikotarpis nuo SF termino iki mokėjimo datos**. Prognozėje numatytosios lauko **Mokėjimo sąlygos** bus naudojamos tik tada, jeigu reikšmė nenurodyta operacijoje. Norėdami aprašyti kiekvienai proceso daliai būdingiausią dienų skaičių, naudokite mokėjimo sąlygą. 

Lauke **Mokėjimų likvidumo sąskaitos** nurodoma dažniausiai mokėjimams naudojama likvidumo sąskaita. Lauką **Grynųjų pinigų srautų prognozei paskirstytina procentinė suma** naudokite norėdami nurodyti, ar atliekant prognozavimą turi būti naudojama tam tikra procentinė suma. Jeigu atliekant prognozavimą turi būti naudojamos visos operacijos sumos, palikite šį lauką tuščią.

Galite nepaisyti numatytosios specialioms klientų grupėms skirto lauko **Laikotarpis nuo SF termino iki mokėjimo datos** nuostatos. Prognozė naudos numatytąją dalyje **Numatytosios pardavimo prognozės nuostatos** nurodytą reikšmę, nebent būtų nurodyta kita su operacijoje dalyvaujančiu klientu susijusios klientų grupės reikšmė. Norėdami nepaisyti numatytosios reikšmės, pasirinkite klientų grupę, o po to nustatykite naują lauko **Pardavimo laikas** reikšmę.

Galite nepaisyti numatytosios specialiems kliento registravimo šablonams naudojamo lauko **Likvidumo sąskaita** nuostatos. Prognozė naudos numatytąją dalyje **Numatytosios pardavimo prognozės nuostatos** nurodytą reikšmę, nebent būtų nurodyta kita su operacijoje dalyvaujančiu klientu susijusio registravimo šablono likvidumo sąskaita. Norėdami nepaisyti numatytosios reikšmės, pasirinkite registravimo šabloną, o po to nustatykite likvidumo sąskaitą, kuri turėtų būti paveikta.

### <a name="budgeting"></a>Biudžeto sudarymas

Biudžetus, sukurtus naudojant biudžeto modelius, galite įtraukti į pinigų srautų prognozes. Puslapio **Pinigų srauto prognozės sąranka** skirtuke **Biudžetas** pasirinkite į prognozę įtrauktinus biudžeto modelius. Pagal numatytuosius nustatymus nauji biudžeto registro įrašai įtraukiami į prognozes įgalinus biudžeto modelio pinigų srauto prognozavimą.

Biudžeto registro įrašus galima įtraukti į pinigų srautų prognozę individualiai, naudojant personalizavimą. Kai pridedate stulpelį Įtraukti į pinigų srautų prognozes į įrašo puslapį **Biudžeto registro įrašas** sistema perrašys pinigų srautų prognozės nustatymo puslapio parametrus, kad į prognozę įtrauktų **Atskirą biudžeto registro įrašą**.


### <a name="inventory-management"></a>Atsargų valdymas

Atsargų pasiūlos ir paklausos prognozes galima įtraukti į pinigų srautų prognozes. Puslapio **Pinigų srauto prognozės sąranka** skirtuke **Atsargų valdymas** pasirinkite į pinigų srauto prognozę įtrauktiną prognozės modelį. Įtraukimo į pinigų srautų prognozavimą gali būti nepaisoma atskirose pasiūlos ir paklausos prognozės eilutėse.

### <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Grynųjų pinigų srautų prognozavimo dimensijų nustatymas
Naujas skirtukas pinigų **srautų prognozės** nustatymo puslapyje leidžia kontroliuoti, kurios finansinės dimensijos bus naudojamos filtruojant pinigų **srautų prognozės darbo** srityje. Šis skirtukas bus rodomas tik įgalinus pinigų srautų prognozių priemonę.

Skirtuke **Dimensijos** pasirinkite iš dimensijų, kurias naudosite filtruodami, sąrašo ir naudokite rodyklių klavišus, kad perkeltumėte jas į dešinįjį stulpelį. Grynųjų pinigų srautų prognozavimo duomenims filtruoti galima pasirinkti tik dvi dimensijas. 

### <a name="setting-up-external-source"></a>Išorinio šaltinio nustatymas
Konfigūrus finansų įžvalgas, išorinius duomenis galima įvesti arba importuoti į pinigų srautų prognozes. Prieš pradedant įvesti ar importuoti išorinius duomenis, turi būti nustatyti išoriniai šaltiniai. Skirtuke **Išorinis šaltinis** nustatykite išorines pinigų srautų kategorijas. Kategorija gali būti siunčiama **arba** gaunama **·**. **Likvidumas** turėtų būti pasirinktas kaip registravimo tipas. Juridinio **subjekto parametrų** tinklelyje pasirinkite juridinius subjektus ir atitinkamas pagrindines sąskaitas, kuriems taikomos išorinės pinigų srautų kategorijos.

Daugiau informacijos rasite pinigų srautų [prognozių išoriniuose duomenyse](../../finance/finance-insights/external-data-in-cash-flow.md). 

### <a name="project-management-and-accounting"></a>Projektų valdymas ir apskaita

Versijoje 10.0.17 nauja funkcija įgalina integravimą su projektų valdymu ir apskaita bei pinigų srautų prognoze. Funkcijų valdymo darbo srityje įjunkite pinigų srautų projekto prognozės priemonę, kad į pinigų srautų prognozę įtraukite prognozuotas **išlaidas** ir **įplaukas**. Projektų valdymo ir apskaitos skirtuke, pinigų srautų prognozės nustatymo puslapyje, pasirinkite projekto tipus ir operacijų tipus, kuriuos reikia įtraukti **į pinigų** srautų **prognozę**. Tada pasirinkite projekto prognozės modelį. Mažinimo tipo submodelis tinka geriausiai. Likvidumo sąskaitos, įvestos gautinų sumų nustatyme, yra naudojamos kaip numatytosios likvidumo sąskaitos. Todėl nustatant pinigų srautų prognozę nereikia įvesti numatytųjų likvidumo sąskaitų. Biudžeto modelį taip pat galima naudoti, tačiau projektų valdymo ir apskaitos pinigų srautų prognozės nustatymo puslapyje **galima pasirinkti tik vieną** tipą. Prognozės modelis suteikia geriausią lankstumo, kai naudojamas projektų valdymas ir apskaita arba „Project Operations“.

Kai pinigų srautų projekto prognozės funkcija įjungta, galima peržiūrėti kiekvieno projekto pinigų srautų prognozę **visų projektų** puslapyje. Veiksmų srities skirtuko **Planas** grupėje **Prognozė** pasirinkite **Grynųjų pinigų srauto prognozė**. Grynųjų **pinigų apžvalgos** darbo srityje ([toliau](#reporting) šiame straipsnyje žr. ataskaitos skyrių), projekto prognozės operacijos tipas rodo įplaukas (projekto prognozės įplaukas) ir nutekėjimus (projekto prognozės išlaidos). Sumas galima įtraukti tik tuo atveju, jei grynųjų pinigų apžvalgos darbo sričių **projekto** etapo **laukas** nustatytas kaip **Apdorojamas**.

Projekto operacijos vis dar įtrauktos į pinigų srautų prognozę keliais būdais, neatsižvelgiant į tai, ar pinigų srautų projekto **prognozės** funkcija įjungta. Užregistruotos projekto SF įtraukiamos į prognozę kaip atvirų kliento operacijų dalis. Projekto paskatinti pardavimo ir pirkimo užsakymai įvedus juos į sistemą įtraukiami į prognozę kaip atviri užsakymai. Taip pat galite perkelti projekto prognozes į DK biudžeto modelį. Tada šis DK biudžeto modelis įtraukiamas į pinigų srautų prognozę kaip biudžeto registro įrašų dalis. Jei įjungėte pinigų srautų projekto prognozės priemonę, neįkelkite projekto prognozių į DK biudžeto modelį, nes dėl šio veiksmo projekto prognozės bus skaičiuojamos **du** kartus.

### <a name="sales-tax-authority-payments"></a>PVM institucijos mokėjimai 

Pinigų srautų PVM institucijos mokėjimų priemonė numato PVM mokėjimų pinigų srautų poveikį. Jis naudoja neapmokėtas PVM operacijas, mokesčių sudengimo laikotarpius ir mokesčių laikotarpio mokėjimo terminą pinigų srautų mokėjimų datai ir sumai nuspėti. 

### <a name="calculation"></a>Skaičiavimas

Norėdami peržiūrėti pinigų srautų prognozavimo analizę, turite paleisti pinigų srautų skaičiavimo procesą. Skaičiavimo procesas numatys būsimą įvestų operacijų pinigų poveikį.

Apskaičiuokite pinigų srauto prognozę naudodami puslapį **Pinigų srautų prognozių skaičiavimas**. Galite apskaičiuoti viso pinigų srauto prognozę arba didėjančio pinigų srauto prognozę. 

- Norėdami panaikinti visas pinigų srauto prognozės operacijas ir perskaičiuoti, nustatykite lauko **Pinigų srauto prognozės skaičiavimo metodas** parinktį **Iš viso**. Rekomenduojame naudoti šį metodą, jei ilgai neatnaujinote pinigų srautų prognozių. 
- Norėdami atnaujinti tik su naujomis operacijomis susijusią esamą pinigų srautų informaciją, nustatykite lauko **Pinigų srauto prognozės skaičiavimo metodas** parinktį **Naujas**. Puslapyje bus rodoma data, kai paskutinį kartą buvo paleistas jūsų pinigų srauto skaičiavimas.

Taip pat galite naudoti savo pinigų srauto prognozavimo paketinį apdorojimą. Siekiant užtikrinti, kad jūsų prognozavimo analitika yra tinkamai atnaujinta, nustatykite periodinio paketinį apdorojimą srauto prognozavimo apskaičiavimui.

Versijoje 10.0.13, buvo išleistas papildomas apskaičiavimo procesas naudojantis proceso automatizuotą tvarkaraštį, kuris numato pinigų srautų apskaičiavimo veiksmą. Tai padaroma naudojant **Pinigų srautų prognozavimo automatizavimo** funkciją **Funkcijos valdymo** darbo srityje. Kai jis įjungtas, pasirinkite **Pinigų srautų prognozavimo automatizavimo** nuorodą tam, kad būtų rodomas naujas automatizavimo puslapis, kuriame galite planuoti pinigų srautų apskaičiavimo procesą. Naujos pinigų srautų prognozavimo darbotvarkės sukūrimui, pasirinkite **Sukurti naują apdorojimo automatizavimą** ir tuomet pasirinkite **Pinigų srautų prognozavimo automatizavimą** **Darbotvarkės tipo** iškrentančiame meniu. Privalote nustatyti tvarkaraštį kiekvienai bendrovei, kuriai atnaujinate pinigų srautų prognozavimo duomenis.  Šis puslapis taip pat rodo, kuriuos pinigų srautų prognozavimo automatizavimo užduotys laukia ir paskutinę užbaigtą užduotį.  

> [!NOTE] 
> Jei esančios pakuotės užduotys jau yra suplanuotos pinigų srautų prognozėms, gausite klaidos pranešimą ir nebegalėsite įjungti šios funkcijos. Esamos pakuotės užduotys turės būti panaikintos prieš tai, kai galėsite įjungti šią funkciją. 

Norėdami gauti daugiau informacijos, [žr. Apdorojimo automatizavimas](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

### <a name="reporting"></a>Ataskaitos

Po to, kai apskaičiuojama pinigų srauto prognozė, turite atnaujinti susietą objekto informaciją apie analizės ataskaitas. Puslapyje **Objekto parduotuvė** pasirinkite priemonę **LedgerCovLiquidityMeasurement agregatas**, o po to spustelėkite **Atnaujinti**.

Yra dvi darbo sritys, kuriose yra pinigų srautų prognozės duomenų. Vienoje darbo srityje yra visų įmonių duomenys, o kitoje darbo srityje yra tik dabartinės įmonės duomenys.

Prieiga prie visų įmonių darbo srities yra valdoma atliekant veiksmą **Peržiūrėti visų įmonių pinigų srautų darbo sritį**. Pagal numatytuosius nustatymus galimi šie darbo srities **Pinigų apžvalga – visos įmonės** vaidmenys:

- Generalinis direktorius
- Finansų direktorius
- Finansų kontrolierius

Prieiga prie dabartinės įmonės darbo srities yra valdoma atliekant darbo srities veiksmą **Peržiūrėti dabartinės įmonės pinigų srautą**. Pagal numatytuosius nustatymus galimi šie darbo srities **Pinigų apžvalga – dabartinė įmonė** vaidmenys:

- Buhalteris
- Apskaitos vadovas
- Apskaitos prižiūrėtojas
- Mokėtinų sumų vadovas
- Gautinų sumų vadovas

Darbo srityje **Pinigų apžvalga – visos įmonės** rodoma pinigų srauto prognozavimo analizė sistemos valiuta. Analizei naudojama sistemos valiuta ir sistemos valiutos kurso tipas nurodomi puslapyje **Sistemos parametrai**. Šioje darbo srityje rodoma pinigų srauto prognozavimo ir visų įmonių banko sąskaitų likučių apžvalga. Grynųjų pinigų įplaukų ir išmokų diagramoje apžvelgiami būsimi pinigų perkėlimai ir likučiai sistemos valiuta, taip pat pateikiama išsami informacija apie numatytas operacijas. Taip pat galite matyti prognozuojamus valiutos likučius.

Darbo srityje **Pinigų apžvalga – dabartinė įmonė** rodoma pinigų srautų prognozavimo analizė įmonės nurodyta apskaitos valiuta. Analizei naudojama apskaitos valiuta nurodoma puslapyje **Didžioji knyga**. Šioje darbo srityje rodoma pinigų srauto prognozavimo ir dabartinės įmonės banko sąskaitų likučių apžvalga. Grynųjų pinigų įplaukų ir išmokų diagramoje apžvelgiami būsimi pinigų perkėlimai ir likučiai apskaitos valiuta, taip pat pateikiama išsami informacija apie numatytas operacijas. Taip pat galite matyti prognozuojamus valiutos likučius.

Dėl išsamesnės informacijos apie pinigų srautų prognozavimo analitiką, žr. [Pinigų apžvalgos „Power BI“ turinio temą](Cash-Overview-Power-BI-content.md).

Be to, toliau nurodytuose puslapiuose galite peržiūrėti tam tikrų sąskaitų, užsakymų ir prekių pinigų srautų prognozavimo duomenis.

- **Bandomasis balansas**: norėdami peržiūrėti būsimus pasirinktos pagrindinės sąskaitos pinigų srautus, pasirinkite **Pinigų srautų prognozės**.
- **Visi pardavimo užsakymai**: skirtuke **Sąskaita faktūra** norėdami peržiūrėti pasirinkto pardavimo užsakymo prognozuojamą pinigų poveikį, pasirinkite **Pinigų srautų prognozės**.
- **Visi pirkimo užsakymai**: skirtuke **Sąskaita faktūra** norėdami peržiūrėti pasirinkto pirkimo užsakymo prognozuojamą pinigų poveikį, pasirinkite **Pinigų srautų prognozės**.
- **Tiekimo prognozė**: norėdami peržiūrėti būsimus su pasirinktos prekės tiekimo prognoze susietus pinigų srautus, pasirinkite **Pinigų srautų prognozės**.
- **Poreikio prognozė**: norėdami peržiūrėti būsimus su pasirinktos prekės poreikio prognoze susietus pinigų srautus, pasirinkite **Pinigų srautų prognozės**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
