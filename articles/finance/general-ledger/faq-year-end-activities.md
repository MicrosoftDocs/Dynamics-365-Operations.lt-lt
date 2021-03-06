---
title: DUK apie metų pabaigos veiklas
description: Ši tema sukompiliuota siekiant suteikti pagalbą dėl uždarymo metų pabaigoje veiklų.
author: kweekley
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 379bb8a1f969a74618db0e57c84c2038db1b631c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822836"
---
# <a name="year-end-activities-faq"></a>DUK apie metų pabaigos veiklas 

[!include [banner](../includes/banner.md)]

Ši tema sukompiliuota siekiant suteikti pagalbą dėl uždarymo metų pabaigoje veiklų. Šios temos informacijoje didžiausias dėmesys teikiamas klausimams, susijusiems su didžiąja knyga ir mokėtinų sumų uždarymo metų pabaigoje veiklomis.

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Didžioji knyga: kaip sužinoti, kad atliekame uždarymą metų pabaigoje, o ne uždarymo metų pabaigoje anuliavimą?
Pastebėjome, kad kartais organizacijos bandė vykdyti uždarymą metų pabaigoje, tačiau vietoje to atlikdavo uždarymo metų pabaigoje anuliavimą. Jei uždarymas metų pabaigoje baigiamas labai greitai arba uždarymas metų pabaigoje nepateikia pradinių balansų, patikrinkite parametrą **Anuliuoti ankstesnį uždarymą** dalyje **Uždarymas metų pabaigoje** (**Didžioji knyga > Laikotarpio uždarymas > Uždarymas metų pabaigoje > Uždaryti finansinį laikotarpį**). 

[![Uždarymo metų pabaigoje atlikimas ir uždarymo metų pabaigoje anuliavimas](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Jei sritis **Anuliuoti ankstesnį uždarymą** nustatyta į **Taip**, ankstesnis uždarymas metų pabaigoje yra atšaukiamas. Vykdant anuliavimą bus panaikinti visi uždarymo balanso ir pradinio balanso įrašai, lyg uždarymas metų pabaigoje niekada nebūtų vykdytas. Kvitai panaikinami. Uždarymas metų pabaigoje nebus vykdomas automatiškai. Būtina iš naujo pradėti procesą šį kartą pakeičiant **Anuliuoti ankstesnį uždarymą** į **Ne**. 

> [!NOTE]
> Uždaromais metais pasirinktinai sukuriamas uždarymo balanso įrašas. Tai įvyksta tik tokiu atveju, kai didžiosios knygos parametras **Uždarymo operacijų kūrimas perkėlimo metu** nustatytas į **Taip**. Pradinio balanso įrašas sukuriamas visada, nes jis yra kitų metų pradžios balansas.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Didžioji knyga: kokie skirtumai tarp uždarymo metų pabaigoje anuliavimo ir DK parametro panaikinimo?
Gali kilti neaiškumų dėl skirtumų tarp parametro **Anuliuoti ankstesnį uždarymą**, kuris yra dialogo lange **Uždarymas metų pabaigoje**, ir parametro **Perkėlimo metu naikinti metų uždarymo operacijas** didžiojoje knygoje (**Didžioji knyga > Laikotarpio uždarymas > Uždarymas metų pabaigoje > Uždaryti finansinį laikotarpį**).  

[![Skirtumai tarp uždarymo metų pabaigoje anuliavimo ir DK parametro panaikinimo?](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Išplečiamajame dialogo meniu pasirinkite **Anuliuoti ankstesnį uždarymą**, kai vykdomas uždarymo metų pabaigoje procesas, kad būtų panaikinti visi uždarymo balanso ir pradinio balanso įrašai, tarsi uždarymas metų pabaigoje niekada nebuvo vykdomas. Kvitai bus panaikinti. Uždarymas metų pabaigoje nebus vykdomas automatiškai. Norėdami vykdyti uždarymą metų pabaigoje, turite inicijuoti šį procesą dar kartą, šį kartą pakeisdami **Anuliuoti ankstesnį uždarymą** į **Ne** (**Didžioji knyga > DK nustatymas > DK parametrai**). 

[![DK parametro nustatymas](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Parametras **Perkėlimo metu naikinti metų uždarymo operacijas** didžiojoje knygoje naudojamas tik vykdant (ne anuliuojant) uždarymą metų pabaigoje (parinktis **Anuliuoti ankstesnį uždarymą** nustatyta į **Ne**). Jei parametras nustatytas į **Taip**, visi uždarymo balanso ir pradinio balanso įrašai bus panaikinti, o uždarymas metų pabaigoje bus vykdomas dar kartą. Šis procesas naudojamas tada, kai organizacija nori, kad visos operacijos, įskaitant koregavimus nuo paskutinio uždarymo metų pabaigoje, būtų registruojamos viename apskaitos įraše, skirtame uždarymo balanso ir pradinio balanso įrašams. 

Jei ši pasirinktis nustatyta į **Ne**, visi uždarymo balanso ir pradinio balanso įrašai lieka. Jie nėra panaikinami. Vietoje to bus sukurtas naujas uždarymo balanso ir pradinio balanso įrašas, skirtas tik pokyčiui arba naujoms operacijoms, užregistruotoms nuo tų finansinių metų uždarymo metų pabaigoje.  

> [!NOTE]
> Uždaromais metais sukuriamas uždarymo balanso įrašas. Tai įvyksta tik tokiu atveju, kai didžiosios knygos parametras **Uždarymo operacijų kūrimas perkėlimo metu** nustatytas į **Taip**. Pradinio balanso įrašas sukuriamas visada, nes jis yra kitų metų pradžios balansas. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Didžioji knyga: ką galima pakeisti siekiant padidinti metų pabaigos apdorojimo našumą? 
Galite atlikti keletą pakeitimų siekdami pagerinti uždarymo metų pabaigoje našumą. Rekomenduojame peržiūrėti šiuos siūlomus pakeitimus ir įvertinti, ar pakeitimas tinka jūsų organizacijai.  

### <a name="dimension-sets"></a>Dimensijų rinkiniai
Vykdant uždarymą metų pabaigoje, kiekvienas dimensijų rinkinio balansas perkuriamas, o tai turi tiesioginės įtakos našumui. Kai kurios organizacijos bereikalingai kuria dimensijų rinkinius, nes jie kažkada buvo naudojami arba gali būti naudojami tam tikru metu.  Šie nebūtini dimensijų rinkiniai vis tiek perkuriami vykdant uždarymą metų pabaigoje, o tam reikia laiko. Skirkite pakankamai laiko įvertinti savo dimensijų rinkinius ir panaikinti visus nebūtinus dimensijų rinkinius.

Nebūtini dimensijų rinkiniai taip pat daro įtaką paketinei užduočiai **BudgetDimensionFocusInitializeBalance** (**Didžioji knyga > Sąskaitų planas > Dimensijos > Finansinių dimensijų rinkiniai**).

[![Finansinių dimensijų rinkiniai](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Uždarymo metų pabaigoje šablono konfigūravimas
Uždarymo metų pabaigoje šablonas leidžia organizacijoms pasirinkti finansinės dimensijos lygį, kurį reikia išlaikyti perkeliant pelno ir nuostolio balansus į nepaskirstytą pelną. Parametrai leidžia organizacijai tvarkyti išsamias finansines dimensijas (**Uždaryti viską**) perkeliant balansus į nepaskirstytą pelną arba pasirinkti sumuoti sumas į vieną dimensijos vertę (**Uždaryti vieną**). Tai galima apibrėžti nurodyti kiekvienai finansinei dimensijai. Daugiau informacijos apie šiuos parametrus žr. temoje [Uždarymas metų pabaigoje](year-end-close.md).

Rekomenduojame įvertinti savo organizacijos poreikius ir, jei galima, uždaryti kuo daugiau dimensijų naudojant uždarymo metų pabaigoje parinktį **Uždaryti vieną**, kad padidintumėte našumą. Uždarant vieną dimensijos vertę (kuri taip pat gali būti tuščia vertė), sistema, nustatydama nepaskirstyto pelno apskaitos įrašų balansus, apdoroja mažiau informacijos.

### <a name="10013-update-or-later"></a>10.0.13 naujinimas arba vėlesnis
Jei atnaujinote į 10.0.13 versiją ar vėlesnę nuo paskutiniojo organizacijos uždarymo metų pabaigoje, metų pabaigos uždarymo procesas gali trukti ilgiau dėl [HashV2 funkcijos diegimo](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2). Terminas *hash* nurodo lauką, kuris apskaičiuojamas iš kitų eilutės laukų. API, skirta apskaičiuoti „hash“ GUID vertę, atnaujinta siekiant padidinti saugą. Norint paspartinti uždarymo metų pabaigoje procesą, rekomenduojame prieš vykdant uždarymą metų pabaigoje perkurti dimensijų rinkinių balansus. Jei jau atlikote dimensijų rinkinio balansų perkūrimą po 10.0.13 naujinimo, perkūrimo proceso dar kartą vykdyti nebūtina.
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a>Didžioji knyga – kokis laikotarpio uždarymo, uždarymo metų pabaigoje paskirtis?
 
[![Laikotarpio uždarymas, uždarymas metų pabaigoje](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a>Našumo patobulinimai, skirti perkurti finansinių dimensijų rinkinius (nauja funkcija)
Nauja į 10.0.16 įtraukta funkcija padidina uždarymo metų pabaigoje ir konsolidavimo procesų našumą. Funkcijos pavadinimas – Našumo patobulinimai, skirti perkurti finansinių dimensijų rinkinius. Ši funkcija pakeičia dimensijų rinkinių perkūrimo būdą, kad jie būtų perkuriami tik atitinkamam laikotarpiui. Ankstesnėse versijose dimensijų rinkiniai buvo perkuriami visoms datoms. Pavyzdžiui, uždarant 2020 m., sistema perkurs tik per 2020 finansinius metus atliktų operacijų balansus. Jei atliekate konsolidavimą datų diapazonu nuo 2020 m. lapkričio 1 d. iki 2020 m. lapkričio 30 d., sistema perkurs tik to datų diapazono balansus.

Ši funkcija laikoma svarbiu pakeitimu, todėl jums reikės įgalinti ją naudojant darbo sritį **Funkcijų valdymas**.
 
[![Uždarymas metų pabaigoje](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a>Mokėtinos sumos: kokie pakeitimai atlikti siekiant palaikyti 2020-ųjų 1099 metų pabaigos ataskaitas?

2020-aisiais 1099 metų pabaigos pakeitimams pritaikytos dvi naujos reguliavimo priemonės. Pirmoji priemonė, **1099-NEC ir 1099-MISC formų, skirtų 2020-iesiems, pakeitimų taikymas**, metų viduryje buvo išleista kaip privalomoji priemonė. Jos paskirtis – užtikrinti, kad 2020-ųjų 1099 operacijų duomenis būtų galima sekti naujoje 1099-NEC formoje. Ši funkcija įtraukė 1099 laukus, kurie yra būtini siekiant palaikyti naują 1099-NEC ir atnaujinti 1099-MISC laukus. Šis naujinimas taip pat atnaujino tiekėjo įrašo duomenis 1099 langelio informacijai. 

Antroji reguliavimo priemonė – **1099 išrašai, atnaujinti pagal 2020-ųjų mokesčių įstatymus**, apima toliau nurodytus keitimus.

- 1099-OID – IRS konvertavo formą į tęstinio naudojimo.
   - Spausdinant būtina įvesti 3 ir 4-ą ataskaitinių metų skaitmenį. Naudokite lauko **Ataskaitiniai metai** 3 ir 4-ą skaitmenis iš **Mokesčių 1099 spausdinimo parinktys**. 

- 1099-NEC – nauja 2020-ųjų forma. Įrašo ne darbuotojų kompensaciją. 

-   1099-MISC – dėl formos 1099-NEC sukūrimo IRS peržiūrėjo 1099-MISC formą ir pakeitė langelių numerius, kad būtų galima pateikti tam tikrų pajamų ataskaitas.
Pajamų ataskaitos pakeitimai ir formos langelių numeriai išvardyti toliau.
   - 7 langelyje mokėtojas atliko tiesioginių pardavimų už 5 000 $ ar daugiau (žymės langelis).
   - 9 langelyje nurodomos derliaus draudimo pajamos.
   - 10 langelyje nurodomos bendrosios pajamos patikėtiniui.
   - 12 langelyje nurodomi 409A skyriaus atidėjimai.
   - 14 langelyje nurodomos nekvalifikuotos atidėtos kompensacijos pajamos.
   - 15, 16 ir 17 langeliuose atitinkamai nurodomi išskaitytini valstybiniai mokesčiai, valstybinio identifikavimo numeris ir valstybėje gautų pajamų suma.

- Nėra pakeitimų 2020 m. 1099–DIV ar 1099-INT.

- Elektroninis pateikimas – formatas pasikeitė, kad būtų galima naudoti naują NEC formą ir pirmiau apibūdintus MISC langelio pakeitimus. Konkrečios informacijos apie elektroninio pateikimo reikalavimus, žr. [IRS 1220 nutarimą](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Mokėtinos sumos: 1099 – kaip pakeisti 1099 lauką ir tiekėjo, kuris per metus nesekė 1099 informacijos, vertes?
Naudokite funkciją Naujinti 1099 (**Mokėtinos sumos > Tiekėjai >Visi tiekėjai > Pasirinkti tiekėją > Tiekėjo skirtukas juostelėje > Atnaujinti 1099**), kad peržiūrėtumėte anksčiau apmokėtas SF operacijas, norėdami tinkamai priskirti 1099 duomenis pagal parametrus puslapio **Tiekėjas** skirtuke **1099 mokesčiai**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Ar galima paleisti visiems tiekėjams 1099 naujinimą vienu metu?
Ne. Naujinimo 1099 procedūra vienu metu atliekama vienam tiekėjui. Jei šis reikalavimas taikomas jūsų organizacijai, balsuokite už idėją, pavadintą [Tiekėjo 1099 duomenų naujinimo paketinis apdorojimas](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a>Mokėtinos sumos: 1099 – 1099 naujinimo priemonės funkcijos „Perskaičiuoti esamas 1099 sumas“ ir „Naujinti viską“.
Žymės langelis **Perskaičiuoti esamas 1099 sumas** iš naujo nustatys 1099 sumą pagal bendrą sumokėtų verčių sumą, kai naudojama kartu su žymės langeliu **Naujinti viską**. 

[![Mokesčio 1099 operacijos: prieš vykdant naujinimo procedūrą](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Žymės langelis **Perskaičiuoti esamas 1099 sumas** naudojamas tik tada, kai SF yra dalinių 1099 verčių arba jis buvo modifikuotas formoje 1099 mokesčiai. Tarkime, kad jūsų SF vertė yra 1000,00 $, tačiau vartotojas rankiniu būdu įveda 1099 sumą į 500,00 $ sąskaitą.

[![1099 mokesčių operacijos: pažymėjimas abiejų parinkčių Naujinti viską ir Perskaičiuoti esamas 1099 sumas](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Kai bus apmokama, 500,00 $ suma bus sumokėta 1099 suma. Jei atliekate perskaičiavimo procedūrą, sistema pakeis 1099 sumą į 1000,00 $; kuri yra bendroji sumokėta suma.

[![Mokesčių 1099 operacijos: paleidus 1099 procedūrą](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Mokėtinos sumos: 1099 – 1099 operacijų kūrimas rankiniu būdu
Organizacijai gali prireikti rankiniu būdu sukurti 1099 operacijas, kurios nėra susietos su SF. Galite įtraukti neautomatines 1099 operacijas eidami į **Mokėtinos sumos > Periodinės užduotys > Mokesčiai 1099 > Tiekėjo sudengimas 1099**. Pasirinkite mygtuką **Rankinės 1099 operacijos**. 

Rankiniu būdu sukurtos 1099 operacijos neatnaujinamos naudojant procesą **Naujinti viską** arba procesą **Perskaičiuoti esamas 1099 sumas** priemonėje **Naujinti 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Mokėtinos sumos: 1099 – ar „Dynamics 365 Finance“ palaiko 1096 formą? 

„Dynamics 365 Finance“ nespausdina 1096 metinės suvestinės ir JAV informacijos grąžinimo formos perdavimo.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Mokėtinos sumos: 1099 – ar yra naujų funkcijų, kurios palaiko viešajam sektoriui skirtas 1099 ataskaitas? 
Pridėta nauja viešojo sektoriaus funkcija **Naujinti 1099 informaciją pagal pagrindinę sąskaitą**, kurią galima įjungti darbo srityje **Funkcijų valdymas**. Ši funkcija leidžia susieti tiekėjo 1099 vertes pagal pagrindinę sąskaitą apskaitos paskirstyme, o ne pagal numatytąją tiekėjo įrašo sąskaitą.

Daugiau informacijos žr. [Tiekėjų nustatymas 1099 ataskaitoms](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
