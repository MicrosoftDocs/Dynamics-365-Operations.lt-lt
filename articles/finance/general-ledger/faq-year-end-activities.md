---
title: DUK apie metų pabaigos veiklas
description: Šioje temoje pateikiami klausimai, kurie gali kilti uždarant metus, ir atsakymai, kurie gali padėti atliekant uždarymo metų pabaigoje veiklas.
author: moaamer
ms.date: 12/21/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 19d23c2c5a8fabd6799c6240c25f3ede4064c001
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725606"
---
# <a name="year-end-activities-faq"></a>DUK apie metų pabaigos veiklas 

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiami klausimai, kurie gali kilti uždarant metus, ir atsakymai, kurie gali padėti atliekant uždarymo metų pabaigoje veiklas. Šios temos informacijoje didžiausias dėmesys teikiamas klausimams, susijusiems su didžiąja knyga ir mokėtinų sumų uždarymo metų pabaigoje veiklomis.

## <a name="general-ledger-year-end-enhancements"></a>Didžiosios knygos metų pabaigos patobulinimai 
10.0.20 versijoje pristatytas uždarymo metų pabaigoje patobulinimas, kuris įjungtas pagal numatytuosius nustatymus 10.0.25 ir naujesnėse versijose. Jei jūsų organizacija naudoja ankstesnę nei 10.0.25 versiją, rekomenduojame įjungti šią funkciją prieš pradedant uždarymo metų pabaigoje procesą. Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti funkcijos valdymo darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

 - Modulis: Didžioji knyga
 - Funkcijos pavadinimas: Didžiosios knygos metų pabaigos patobulinimai

Uždarymo metų pabaigoje šablonai buvo perkelti į naują sąrankos puslapį **Uždarymo metų pabaigoje šablono sąranka**. Esamas uždarymo metų pabaigoje puslapis bus pakeistas panašiu būdu, kuriuo buvo pakeistas didžiosios knygos užsienio valiutos kurso pasikeitimas; kiekvieną kartą paleidus arba atšaukus uždarymą metų pabaigoje bus rodomas sąrašas. Apskaitos vadovas gali inicijuoti uždarymą metų pabaigoje iš naujo puslapio. 

Norėdami atšaukti uždarymą metų pabaigoje, pasirinkite naujausius atitinkamo juridinio subjekto finansinius metus ir pasirinkite mygtuką **Atšaukti uždarymą metų pabaigoje**. Atšaukus bus panaikinti ankstesnio uždarymo metų pabaigoje įrašai, o uždarymas metų pabaigoje nebus automatiškai paleistas iš naujo. 

Iš naujo paleisdami finansinių metų ir juridinio subjekto procesą galite iš naujo paleisti uždarymą metų pabaigoje. Vykdant procesą ir toliau bus naudojamas didžiosios knygos parametro nustatymas, skirtas nustatyti, ar iš naujo paleidus uždarymą metų pabaigoje bus tik sukurtos naujos arba pakeistos operacijos, ar bus visiškai atšauktas ankstesnis uždarymas ir iš naujo paleistas visų operacijų procesas.  

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Didžioji knyga: kaip sužinoti, kad atliekame uždarymą metų pabaigoje, o ne uždarymo metų pabaigoje anuliavimą?
Pastebėjome, kad kartais organizacijos bandė vykdyti uždarymą metų pabaigoje, tačiau vietoje to atlikdavo uždarymo metų pabaigoje anuliavimą. Jei uždarymas metų pabaigoje baigiamas labai greitai arba uždarymas metų pabaigoje nepateikia pradinių balansų, patikrinkite parametrą **Anuliuoti ankstesnį uždarymą** dalyje **Uždarymas metų pabaigoje** (**Didžioji knyga > Laikotarpio uždarymas > Uždarymas metų pabaigoje > Uždaryti finansinį laikotarpį**). 

[![Uždarymo metų pabaigoje atlikimas ir uždarymo metų pabaigoje anuliavimas.](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Jei sritis **Anuliuoti ankstesnį uždarymą** nustatyta į **Taip**, ankstesnis uždarymas metų pabaigoje yra atšaukiamas. Vykdant anuliavimą bus panaikinti visi uždarymo balanso ir pradinio balanso įrašai, lyg uždarymas metų pabaigoje niekada nebūtų vykdytas. Kvitai panaikinami. Uždarymas metų pabaigoje nebus vykdomas automatiškai. Būtina iš naujo pradėti procesą šį kartą pakeičiant **Anuliuoti ankstesnį uždarymą** į **Ne**. 

> [!NOTE]
> Uždaromais metais pasirinktinai sukuriamas uždarymo balanso įrašas. Tai įvyksta tik tokiu atveju, kai didžiosios knygos parametras **Uždarymo operacijų kūrimas perkėlimo metu** nustatytas į **Taip**. Pradinio balanso įrašas sukuriamas visada, nes jis yra kitų metų pradžios balansas.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Didžioji knyga: kokie skirtumai tarp uždarymo metų pabaigoje anuliavimo ir DK parametro panaikinimo?
Gali kilti neaiškumų dėl skirtumų tarp parametro **Anuliuoti ankstesnį uždarymą**, kuris yra dialogo lange **Uždarymas metų pabaigoje**, ir parametro **Perkėlimo metu naikinti metų uždarymo operacijas** didžiojoje knygoje (**Didžioji knyga > Laikotarpio uždarymas > Uždarymas metų pabaigoje > Uždaryti finansinį laikotarpį**).  

[![Skirtumai tarp uždarymo metų pabaigoje anuliavimo ir DK parametro panaikinimo.](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Išplečiamajame dialogo meniu pasirinkite **Anuliuoti ankstesnį uždarymą**, kai vykdomas uždarymo metų pabaigoje procesas, kad būtų panaikinti visi uždarymo balanso ir pradinio balanso įrašai, tarsi uždarymas metų pabaigoje niekada nebuvo vykdomas. Kvitai bus panaikinti. Uždarymas metų pabaigoje nebus vykdomas automatiškai. Norėdami vykdyti uždarymą metų pabaigoje, turite inicijuoti šį procesą dar kartą, šį kartą pakeisdami **Anuliuoti ankstesnį uždarymą** į **Ne** (**Didžioji knyga > DK nustatymas > DK parametrai**). 

[![Didžiosios knygos parametro nustatymas.](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Parametras **Perkėlimo metu naikinti metų uždarymo operacijas** didžiojoje knygoje naudojamas tik vykdant (ne anuliuojant) uždarymą metų pabaigoje (parinktis **Anuliuoti ankstesnį uždarymą** nustatyta į **Ne**). Jei parametras nustatytas į **Taip**, visi uždarymo balanso ir pradinio balanso įrašai bus panaikinti, o uždarymas metų pabaigoje bus vykdomas dar kartą. Šis procesas naudojamas tada, kai organizacija nori, kad visos operacijos, įskaitant koregavimus nuo paskutinio uždarymo metų pabaigoje, būtų registruojamos viename apskaitos įraše, skirtame uždarymo balanso ir pradinio balanso įrašams. 

Jei ši pasirinktis nustatyta į **Ne**, visi uždarymo balanso ir pradinio balanso įrašai lieka. Jie nėra panaikinami. Vietoje to bus sukurtas naujas uždarymo balanso ir pradinio balanso įrašas, skirtas tik pokyčiui arba naujoms operacijoms, užregistruotoms nuo tų finansinių metų uždarymo metų pabaigoje.  

> [!NOTE]
> Uždaromais metais sukuriamas uždarymo balanso įrašas. Tai įvyksta tik tokiu atveju, kai didžiosios knygos parametras **Uždarymo operacijų kūrimas perkėlimo metu** nustatytas į **Taip**. Pradinio balanso įrašas sukuriamas visada, nes jis yra kitų metų pradžios balansas. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Didžioji knyga: ką galima pakeisti siekiant padidinti metų pabaigos apdorojimo našumą? 
Galite atlikti keletą pakeitimų siekdami pagerinti uždarymo metų pabaigoje našumą. Rekomenduojame peržiūrėti šiuos siūlomus pakeitimus ir įvertinti, ar pakeitimas tinka jūsų organizacijai.  

### <a name="dimension-sets"></a>Dimensijų rinkiniai
Vykdant uždarymą metų pabaigoje, kiekvienas dimensijų rinkinio balansas perkuriamas, o tai turi tiesioginės įtakos našumui. Kai kurios organizacijos bereikalingai kuria dimensijų rinkinius, nes jie kažkada buvo naudojami arba gali būti naudojami tam tikru metu.  Šie nebūtini dimensijų rinkiniai vis tiek perkuriami vykdant uždarymą metų pabaigoje, o tam reikia laiko. Skirkite pakankamai laiko įvertinti savo dimensijų rinkinius ir panaikinti visus nebūtinus dimensijų rinkinius.

Nebūtini dimensijų rinkiniai taip pat daro įtaką paketinei užduočiai **BudgetDimensionFocusInitializeBalance** (**Didžioji knyga > Sąskaitų planas > Dimensijos > Finansinių dimensijų rinkiniai**).

[![Finansinių dimensijų rinkiniai.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Uždarymo metų pabaigoje šablono konfigūravimas
Uždarymo metų pabaigoje šablonas leidžia organizacijoms pasirinkti finansinės dimensijos lygį, kurį reikia išlaikyti perkeliant pelno ir nuostolio balansus į nepaskirstytą pelną. Parametrai leidžia organizacijai tvarkyti išsamias finansines dimensijas (**Uždaryti viską**) perkeliant balansus į nepaskirstytą pelną arba pasirinkti sumuoti sumas į vieną dimensijos vertę (**Uždaryti vieną**). Tai galima apibrėžti nurodyti kiekvienai finansinei dimensijai. Daugiau informacijos apie šiuos parametrus žr. temoje [Uždarymas metų pabaigoje](year-end-close.md).

Rekomenduojame įvertinti savo organizacijos poreikius ir, jei galima, uždaryti kuo daugiau dimensijų naudojant uždarymo metų pabaigoje parinktį **Uždaryti vieną**, kad padidintumėte našumą. Uždarant vieną dimensijos vertę (kuri taip pat gali būti tuščia vertė), sistema, nustatydama nepaskirstyto pelno apskaitos įrašų balansus, apdoroja mažiau informacijos.

## <a name="degenerate-dimensions"></a>Faktų dimensijos

Faktų dimensijos beveik negalima arba iš viso negalima pakartotinai naudoti atskirai arba su kitomis dimensijomis. Faktų dimensijos yra dviejų tipų. Pirmasis tipas yra dimensija, kuri yra atskirai faktinė. Paprastai šis faktų dimensijos tipas bus rodomas tik vienoje operacijoje arba mažuose operacijų rinkiniuose. Antrasis tipas – tai dimensija, kuri tampa faktinė kartu su viena arba daugiau papildomų dimensijų, parodančių tą patį potencialą, remiantis galimais deriniais, kurie gali būti sukurti. Faktinė dimensija gali labai paveikti uždarymo metų pabaigoje efektyvumą. Norėdami sumažinti efektyvumo problemas iki minimumo, uždarymo metų pabaigoje sąrankoje apibrėžkite visas faktines dimensijas kaip **Uždaryti vieną**, kaip apibrėžta ankstesniame skyriuje.

## <a name="general-ledger-what-does-the-period-close-year-end-close-do"></a>Didžioji knyga: kokia laikotarpio uždarymo, uždarymo metų pabaigoje paskirtis?
 
[![Laikotarpio uždarymas, uždarymas metų pabaigoje.](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets"></a>Našumo patobulinimai, skirti finansinių dimensijų rinkiniams perkurti
Nauja į 10.0.16 versiją įtraukta funkcija padidina uždarymo metų pabaigoje ir konsolidavimo procesų našumą. Funkcijos pavadinimas – Našumo patobulinimai, skirti perkurti finansinių dimensijų rinkinius. Ši funkcija pakeičia dimensijų rinkinių perkūrimo būdą, kad jie būtų perkuriami tik atitinkamam laikotarpiui. Ankstesnėse versijose dimensijų rinkiniai buvo perkuriami visoms datoms. Pavyzdžiui, uždarant 2020 m., sistema perkurs tik per 2020 finansinius metus atliktų operacijų balansus. Jei atliekate konsolidavimą datų diapazonu nuo 2020 m. lapkričio 1 d. iki 2020 m. lapkričio 30 d., sistema perkurs tik to datų diapazono balansus.

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti funkcijos valdymo darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:
 
- Modulis: Didžioji knyga
- Funkcijos pavadinimas: Našumo patobulinimai, skirti perkurti finansinių dimensijų rinkinius

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2021"></a>Mokėtinos sumos: kokie pakeitimai atlikti siekiant palaikyti 2021-ųjų 1099 metų pabaigos ataskaitas?

2021 m. DIV, NEC ir MISC formos buvo šiek tiek pakeistos ir buvo įtraukti kai kurie papildomi langeliai.

#### <a name="div-new-box2e-2f"></a>DIV: naujas 2e, 2f langelis
 
- 2e langelis. 1a langelyje rodoma sumos dalis, kuri yra 897 skyriaus pelnas, priskiriamas JAV nekilnojamojo turto interesų (USRPI) perdavimui.  
- 2f langelis. 2a langelyje rodoma sumos dalis, kuri yra 897 skyriaus pelnas, priskiriamas USRPI perdavimui. Atkreipkite dėmesį, kad 2e ir 2f langeliai taikomi tik užsieniečiams ir užsienio subjektams, kurių pajamų savybės nesikeičia, kai yra perduodamos arba paskirstomos tiesioginiams arba netiesioginiams savininkams užsieniečiams arba gavėjams. Paprastai tai laikoma iš tikrųjų susiję su Jungtinių Valstijų prekyba ar verslu. Peržiūrėkite mokesčių grąžinimo instrukcijas. 
 
#### <a name="nec-new-box-2"></a>NEC: naujas 2 langelis 
 
Jei pažymėtas 2 langelis, pateikite vartojimo prekių, kurių suma 5 000 $ ar daugiau, kurie jums buvo parduoti perpardavimui, pirkimo ir pardavimo, depozito ir komiso ar kitu pagrindu. Apskritai praneškite apie bet kokias pajamas iš šių produktų pardavimo C grafike (1040 forma). 
 
Tuo pačiu metu keičiamas NEC formos dydis. Spausdinant puslapyje yra trys formos. 
 
#### <a name="misc-new-box-11"></a>MISC: naujas 11 langelis 
 
11 langelyje rodoma suma, sumokėta už žuvų pirkimą perpardavimui iš bet kokio asmens, vykdančio prekybą arba užsiimančio žvejyba. Norėdami gauti šių pajamų ataskaitą, žr. mokesčių grąžinimo instrukcijas. 
 
#### <a name="electronic-filing"></a>Elektroninis pateikimas 
Norėdami gauti informacijos apie elektroninį pateikimą, žr. [Elektroninio pateikimo reikalavimų nutarimas](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

Atnaujinti 2021 m. ataskaitos formato specifikacijas ir įrašo maketus 
- 2 skyr. Išdavusios įstaigos A įrašas. 
- Sumos kodai – padidintos 28–45 lauko padėtys, ilgis padidintas iki 18. 
 
#### <a name="sec-2-issuer-a-record-for-reporting-payments-on-form-1099-div"></a>2 skyr. Išdavusios įstaigos A įrašas, skirtas mokėjimams pateikti 1099-DIV formoje: 
- Sumos tipas – įtrauktas 897 skyrius Paprastieji dividendai ir pridėtas H sumos kodas. 
- Sumos tipas – įtrauktas 897 skyrius Kapitalo prieaugis ir pridėtas J sumos kodas. 
 
#### <a name="sec-3-payee-b-record"></a>3 skyr. Gavėjo B įrašas 
- Bendrosios informacijos įrašai – atnaujintas trečias ženklelis iš 16 į 18 mokėjimo sumos laukų. 
- H lauko pavadinimo mokėjimas – atnaujintos 247–258 lauko padėtys, lauko pavadinimas, ilgis ir bendrasis lauko aprašas. 
- J lauko pavadinimo mokėjimas – atnaujintos 259–270 lauko padėtys, lauko pavadinimas, ilgis ir bendrasis lauko aprašas. 
- Atnaujintas tuščias laukas į 271–286 lauko padėtis. 
- Atnaujintas užsienio šalies indikatorius į 287 lauko padėtį. 
- Atnaujintas gavėjo vardo eilutės laukas į 288–327 lauko padėtis. 
- Atnaujintas gavėjo pavardės eilutės laukas į 328–367 lauko padėtis. 
- Įrašo maketo padėtys, 1099-MISC forma – panaikinta 548 lauko padėtis ir lauko pavadinimas FATCA pateikimo reikalavimo indikatorius. 
- Įrašo maketo padėtys, 1099-NEC forma – atnaujintos 545–546 padėtys į Tuščia, atnaujintas 547 laukas į Tiesioginio pardavimo indikatorius, ilgis, aprašas ir pastabos ir atnaujintas 548–722 laukas į Tuščia. 
 
#### <a name="sec-4-end-of-issuer-c-record"></a>4 skyr. Išdavusios įstaigos C įrašo pabaiga 
- H lauko pavadinimo mokėjimas – atnaujintos 304–321 lauko padėtys, lauko pavadinimas, ilgis ir bendrasis lauko aprašas. 
- J lauko pavadinimo mokėjimas – atnaujintos 322–339 lauko padėtys, lauko pavadinimas, ilgis ir bendrasis lauko aprašas. 
- Lauko pavadinimo 340–499 – atnaujintas ilgis iki 160. 
 
#### <a name="sec-5-state-totals-k-record"></a>5 skyr. Valstybės sumų K įrašas 
- H lauko pavadinimo mokėjimas – atnaujintos 304–321 lauko padėtys, lauko pavadinimas, ilgis ir bendrasis lauko aprašas. 
- J lauko pavadinimo mokėjimas – atnaujintos 322–339 lauko padėtys, lauko pavadinimas, ilgis ir bendrasis lauko aprašas. 
- Lauko pavadinimo 340–499 – atnaujintas ilgis iki 160.  

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Mokėtinos sumos: 1099 – kaip pakeisti 1099 lauką ir tiekėjo, kuris per metus nesekė 1099 informacijos, vertes?
Naudokite funkciją Naujinti 1099 (**Mokėtinos sumos > Tiekėjai >Visi tiekėjai > Pasirinkti tiekėją > Tiekėjo skirtukas juostelėje > Atnaujinti 1099**), kad peržiūrėtumėte anksčiau apmokėtas SF operacijas, norėdami tinkamai priskirti 1099 duomenis pagal parametrus puslapio **Tiekėjas** skirtuke **1099 mokesčiai**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Ar galima paleisti visiems tiekėjams 1099 naujinimą vienu metu?
Ne. Naujinimo 1099 procedūra vienu metu atliekama vienam tiekėjui. Jei šis reikalavimas taikomas jūsų organizacijai, balsuokite už idėją, pavadintą [Tiekėjo 1099 duomenų naujinimo paketinis apdorojimas](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Mokėtinos sumos: 1099 – 1099 naujinimo priemonės funkcijos Perskaičiuoti esamas 1099 sumas ir Naujinti viską
Žymės langelis **Perskaičiuoti esamas 1099 sumas** iš naujo nustatys 1099 sumą pagal bendrą sumokėtų verčių sumą, kai naudojama kartu su žymės langeliu **Naujinti viską**. 

[![Mokesčio 1099 operacijos: prieš vykdant naujinimo procedūrą.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Žymės langelis **Perskaičiuoti esamas 1099 sumas** naudojamas tik tada, kai SF yra dalinių 1099 verčių arba jis buvo modifikuotas formoje 1099 mokesčiai. Tarkime, kad jūsų SF vertė yra 1000,00 $, tačiau vartotojas rankiniu būdu įveda 1099 sumą į 500,00 $ sąskaitą.

[![1099 mokesčių operacijos: pažymėjimas abiejų parinkčių Naujinti viską ir Perskaičiuoti esamas 1099 sumas.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Kai bus apmokama, 500,00 $ suma bus sumokėta 1099 suma. Jei atliekate perskaičiavimo procedūrą, sistema pakeis 1099 sumą į 1000,00 $; kuri yra bendroji sumokėta suma.

[![Mokesčių 1099 operacijos: paleidus 1099 procedūrą.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Mokėtinos sumos: 1099 – 1099 operacijų kūrimas rankiniu būdu
Organizacijai gali prireikti rankiniu būdu sukurti 1099 operacijas, kurios nėra susietos su SF. Galite įtraukti neautomatines 1099 operacijas eidami į **Mokėtinos sumos > Periodinės užduotys > Mokesčiai 1099 > Tiekėjo sudengimas 1099**. Pasirinkite mygtuką **Rankinės 1099 operacijos**. 

Rankiniu būdu sukurtos 1099 operacijos neatnaujinamos naudojant procesą **Naujinti viską** arba procesą **Perskaičiuoti esamas 1099 sumas** priemonėje **Naujinti 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Mokėtinos sumos: 1099 – ar „Dynamics 365 Finance“ palaiko 1096 formą? 

„Dynamics 365 Finance“ nespausdina 1096 metinės JAV informacijos grąžinimų suvestinės ir perdavimo formos.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Mokėtinos sumos: 1099 – ar yra naujų funkcijų, kurios palaiko viešajam sektoriui skirtas 1099 ataskaitas? 
Pridėta nauja viešojo sektoriaus funkcija **Naujinti 1099 informaciją pagal pagrindinę sąskaitą**, kurią galima įjungti darbo srityje **Funkcijų valdymas**. Ši funkcija leidžia susieti tiekėjo 1099 vertes pagal pagrindinę sąskaitą apskaitos paskirstyme, o ne pagal numatytąją tiekėjo įrašo sąskaitą.

Daugiau informacijos žr. [Tiekėjų nustatymas 1099 ataskaitoms](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
