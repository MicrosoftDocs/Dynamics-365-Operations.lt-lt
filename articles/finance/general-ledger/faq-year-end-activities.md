---
title: DUK apie metų pabaigos veiklas
description: Šiame straipsnyje pateikiami klausimai, kurie gali kilti uždarant metus, ir atsakymai, kurie gali padėti atliekant uždarymo metų pabaigoje veiklas.
author: moaamer
ms.date: 12/01/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2e33c1dcbfa4da74f2e8acc6e29f04fda3abd185
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853047"
---
# <a name="year-end-activities-faq"></a>DUK apie metų pabaigos veiklas 

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiami klausimai, kurie gali kilti uždarant metus, ir atsakymai, kurie gali padėti atliekant uždarymo metų pabaigoje veiklas. Šio straipsnio informacijoje didžiausias dėmesys teikiamas klausimams, susijusiems su didžiąja knyga ir mokėtinų sumų uždarymo metų pabaigoje veiklomis.

## <a name="general-ledger-year-end-enhancements"></a>Didžiosios knygos metų pabaigos patobulinimai

„Microsoft Dynamics 365 Finance“ 10.0.20 versijoje pristatytas uždarymo metų pabaigoje patobulinimas. Šis patobulinimas nuo 10.0.25 versijos įjungtas kaip numatytasis, o nuo 10.0.29 versijos – kaip privalomas. Jei jūsų organizacija naudoja ankstesnę nei 10.0.25 versiją, rekomenduojame įjungti šią funkciją prieš jums pradedant uždarymo metų pabaigoje procesą. Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti **funkcijos valdymo** darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** Didžioji knyga
- **Funkcijos pavadinimas:** Didžiosios knygos metų pabaigos patobulinimai

Uždarymo metų pabaigoje šablonai buvo perkelti į naują sąrankos puslapį **Uždarymo metų pabaigoje šablono sąranka**. Esamas uždarymo metų pabaigoje puslapis taps panašus į puslapį **Didžiosios knygos užsienio valiutos kurso pasikeitimas**, kuriame kiekvieną kartą paleidus arba atšaukus uždarymą metų pabaigoje bus rodomas sąrašas. Puslapyje nebus rodoma istorinė informacija apie uždarymus metų pabaigoje, kurie buvo atlikti prieš įgalinant funkciją. Apskaitos vadovas gali inicijuoti uždarymą metų pabaigoje iš naujo puslapio.

Norėdami atšaukti uždarymą metų pabaigoje, pasirinkite naujausius atitinkamo juridinio subjekto finansinius metus ir pasirinkite **Atšaukti uždarymą metų pabaigoje**. Atšaukus bus panaikinti ankstesnio uždarymo metų pabaigoje įrašai, o uždarymas metų pabaigoje nebus automatiškai paleistas iš naujo. Jei užbaigę uždarymą metu pabaigoje įjungiate funkciją **Didžiosios knygos metų pabaigos patobulinimai** ir norite atšaukti istorinius metų pabaigos rezultatus, dar kartą paleiskite istorinį uždarymą metų pabaigoje įjungę didžiosios knygos parametrą **Naikinti esamus uždarymo metų pabaigoje įrašus iš naujo uždarant metus**.

Iš naujo paleisdami finansinių metų ir juridinio subjekto procesą galite iš naujo paleisti uždarymą metų pabaigoje. Vykdant procesą ir toliau bus naudojamas didžiosios knygos parametro nustatymas, skirtas nustatyti, ar iš naujo paleidus uždarymą metų pabaigoje bus tik sukurtos naujos arba pakeistos operacijos, ar procesas bus iš naujo paleistas visoms operacijoms ir ar bus visiškai atšauktas ankstesnis uždarymas.

## <a name="general-ledger-the-general-ledger-year-end-enhancements-feature-is-enabled-why-cant-i-view-my-previous-year-closings-in-the-history-section-of-the-year-end-close-page"></a>Didžioji knyga: funkcija Didžiosios knygos metų pabaigos patobulinimai įjungta. Kodėl negalima peržiūrėti savo ankstesnių metų uždarymų uždarymo metų pabaigoje puslapio istorijos skyriuje?

Prieš įjungiant funkciją **Didžiosios knygos metų pabaigos patobulinimai**, sekama data ir laikas, kada paskutinis uždarymo metų pabaigoje procesas buvo paleistas. Nebuvo sekama kiekvieno karto, kai uždarymas metų pabaigoje buvo atliktas, istorija. Todėl nėra informacijos apie kiekvieną uždarymo metų pabaigoje vykdymą. Įjungus funkciją, tvarkoma kito uždarymo metų pabaigoje proceso informacija. Kvitus iš visų uždarymo metų pabaigoje procesų, net ir tų, kurie buvo vykdomi prieš funkcijos įjungimą, galima peržiūrėti puslapyje **Kvitų operacijos**. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-cant-be-run-because-one-or-more-ledger-transactions-posted-into-the-fiscal-year-that-you-are-closing-were-settled-to-a-ledger-transaction-in-a-different-fiscal-year-what-does-this-error-mean"></a>Didžioji knyga: uždarymo metų pabaigoje procesas nepavyksta dėl šios klaidos: „Metų pabaigos uždarymas negali būti vykdomas, nes viena ar daugiau didžiosios knygos operacijų, registruotų jūsų uždaromais finansiniais metais, buvo sudengtos pagal didžiosios knygos operaciją kitais finansiniais metais.“ Ką ši klaida reiškia?

Kadangi funkcija **Informacijos bendrinimas tarp didžiosios knygos atsiskaitymo ir metų pabaigos uždarymo** įjungta, į pradinį balansą neįtraukiamos tik sudengtos didžiosios knygos operacijos iš finansinių metų, kurie yra uždaromi. Dėl tokio veikimo būdo debetai ir kreditas nepatenka į balansą. Norėdami gauti daugiau informacijos, žr. [Informacijos bendrinimas tarp didžiosios knygos atsiskaitymo ir metų pabaigos uždarymo](awareness-between-ledger-settlement-year-end-close.md).

## <a name="general-ledger-reversal-of-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-for-112022-cant-be-reversed-because-beginning-balance-transaction-have-been-ledger-settled-in-fiscal-year-112023-what-does-this-error-mean"></a>Didžioji knyga: uždarymo metų pabaigoje proceso atšaukti nepavyko dėl šios klaidos: „2022-01-01 uždarymo metų pabaigoje atšaukti negalima, nes pradžios balanso operacija buvo sudengta didžiojoje knygoje 2023-01-01 finansiniais metais.“ Ką ši klaida reiškia?

Kadangi įjungta funkcija **Informacijos bendrinimas tarp didžiosios knygos atsiskaitymo ir metų pabaigos uždarymo**, metų pabaigos apdorojimo atšaukti negalima, jei atidarymo operacijos buvo sudengtos naujais finansiniais metais. Prieš atšaukdami 2022 m. sausio 1 d. uždarymą metų pabaigoje, atšaukite didžiosios knygos sudengimą naujais 2023 finansiniais metais. Arba iš naujo uždarykite 2022 m. sausio mėn. metus, tačiau tik naujiems koregavimo įrašams. Norėdami metus iš naujo uždaryti tik koregavimams, išjunkite didžiosios knygos parametrą **Panaikinti esamus metų pabaigos įrašus, kai metai uždaromi iš naujo**.

## <a name="general-ledger-why-isnt-the-ledger-settlement-automation-processing-decembers-ledger-settlement-transactions"></a>Didžioji knyga: kodėl didžiosios knygos sudengimo automatizavimas neapdoroja gruodžio mėn. didžiosios knygos sudengimo operacijų?

Funkcija **Automatizuoti didžiosios knygos sudengimus** paleis operacijų, kurių data yra nuo pirmos finansinių metų dienos iki esamos įvykių vykdymo datos, automatizavimą. Finansiniais metais, kurie baigiasi gruodžio 31 d., jums gali tekti koreguoti savo įvykio vykdymo datą, kad užtikrintumėte, jog jis vykdomas gruodžio mėn. Pavyzdžiui, automatizavimas nustatytas būti vykdomas pirmą kiekvieno mėnesio dieną. Šis automatizavimas bus vykdomas 2022 m. gruodžio 1 d. ir planuojama jį vykdyti 2023 m. sausio 1 d. Rekomenduojame pakeisti 2023 m. sausio 1 d. įvykį, kad jis būtų vykdomas 2022 m. gruodžio 31 d. Šis pakeitimas užtikrins, kad bus atsižvelgiama į operacijas, kurių data yra nuo gruodžio 2 d. iki 31 d., ir jos bus automatiškai sudengiamos.

## <a name="general-ledger-whats-the-difference-between-the-reverse-year-end-close-action-and-the-delete-existing-year-end-entries-when-reclosing-parameter-for-year-end-close"></a>Didžioji knyga: koks skirtumas tarp uždarymo metų pabaigoje veiksmo Atšaukti uždarymą metų pabaigoje ir parametro Naikinti esamus metų pabaigos įrašus uždarant iš naujo?

Gali kilti neaiškumų dėl skirtumų tarp veiksmo **Atšaukti uždarymą metų pabaigoje** ir parametro **Naikinti esamus metų pabaigos įrašus uždarant iš naujo** Didžiojoje knygoje (**Didžioji knyga \> Didžiosios knygos sąranka \> Didžiosios knygos parametrai**).

Pasirinkite veiksmą **Atšaukti uždarymą metų pabaigoje**, kai vykdote uždarymo metų pabaigoje procesą, kad būtų panaikinti visi uždarymo balanso ir pradinio balanso įrašai, tarsi uždarymas metų pabaigoje niekada nebuvo vykdomas. Šiuo atveju kvitai bus panaikinti. Uždarymas metų pabaigoje nebus vykdomas automatiškai. Norėdami vykdyti uždarymą metų pabaigoje, pasirinkite veiksmą **Vykdyti uždarymą metų pabaigoje** .

Parametras **Panaikinti esamus metų pabaigos įrašus, kai metai uždaromi iš naujo** didžiojoje knygoje naudojamas tik tada, kai vykdote (o ne atšaukiate) uždarymą metų pabaigoje. Jei parametras nustatytas į **Taip**, visi uždarymo balanso ir pradinio balanso įrašai bus panaikinti, o uždarymas metų pabaigoje bus vykdomas dar kartą. Ši parinktis naudojama tada, kai organizacija nori, kad visos operacijos, įskaitant koregavimus nuo paskutinio uždarymo metų pabaigoje, būtų registruojamos viename apskaitos įraše, skirtame uždarymo balanso ir pradinio balanso įrašams. Jei parametras nustatytas į **Ne**, visi uždarymo balanso ir pradinio balanso įrašai lieka. Jie nėra panaikinami. Vietoje to bus sukurtas naujas uždarymo balanso ir pradinio balanso įrašas, skirtas tik pokyčiui arba naujoms operacijoms, užregistruotoms nuo tų finansinių metų uždarymo metų pabaigoje.

> [!NOTE]
> Uždaromais metais sukuriamas uždarymo balanso įrašas. Tai įvyksta tik tokiu atveju, kai didžiosios knygos parametras **Uždarymo operacijų kūrimas perkėlimo metu** nustatytas į **Taip**. Pradinio balanso įrašas sukuriamas visada, nes jis yra kitų metų pradžios balansas.

## <a name="general-ledger-what-is-the-difference-between-close-all-and-close-single-options-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process"></a>Didžioji knyga: koks skirtumas tarp parinkčių „Uždaryti viską“ ir „Uždaryti vieną“ skyriuje Perkelti pelno ir nuostolių dimensiją uždarymo metų pabaigoje procese?

Parinktis **Uždaryti viską** išlaiko pradines finansinės dimensijos vertes iš užregistruotų operacijų ir panaudoja jas kuriant nepaskirstyto pelno sąskaitos pradinius balansus. Bus sukurti kiekvienai unikaliai finansinių dimensijų verčių kombinacijai skirti atskiri nepaskirstyto pelno pradiniai balansai. Jei pasirinkta parinktis **Uždaryti vieną**, visos užregistruotos operacijos, turinčios tą finansinę dimensiją, bus apibendrinamos kaip nepaskirstyto pelno pradiniai balansai, skirti dimensijos vertei, įvestai lauke, pasirodančiame po **Uždaryti vieną**. 

Pavyzdžiui, visos tų finansinių metų operacijos buvo užregistruotos naudojant sąskaitos struktūrą Pagrindinė sąskaita – Padalinys. Finansinei dimensijai Padalinys šablone pasirinkta **Uždaryti vieną**, o 100 įvedamas kaip dimensijos vertė. Jei bendros visų operacijų, kurios yra užregistruotos padaliniuose 200, 300 ir 400, pajamos siekia 100 000 JAV dolerių, bus sukurtas vienas pradinis balansas, skirtas Nepaskirstytam pelnui – 100. Jei pasirenkate **Uždaryti vieną**, bet paliekate finansinės dimensijos vertę tuščią, visos operacijos bus užregistruotos kaip nepaskirstytas pelnas, o tos dimensijos vertė bus tuščia.

## <a name="general-ledger-when-i-select-close-single-option-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process-will-my-detailed-transactional-information-be-lost"></a>Didžioji knyga: kai pasirenku parinktį „Uždaryti vieną“ uždarymo metų pabaigoje proceso skyriuje Perkelti pelno ir nuostolių dimensija, ar mano išsami operacijos informacija bus prarasta?

Parinktys **Uždaryti viską** ir **Uždaryti vieną** naudojamos norint nustatyti, kurios finansinės dimensijos operacijose, užregistruojamos į pelno ir nuostolio sąskaitas, bus perkeltos į susijusią pagrindinę nepaskirstytojo pelno sąskaitą. Istorinis ir išsamus registravimas į pelno ir nuostolio sąskaitas nėra paveikiamas ir liks išsamus. Ši pasirinktis turi įtakos išsamios informacijos, perkeliamos į nepaskirstytojo pelno sąskaitas kaip naujų metų pradžios likutis, lygiui. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-the-reporting-currency-for-the-year-does-not-balance-what-does-this-mean"></a>Didžioji knyga: nepavyksta atlikti uždarymo metu pabaigoje proceso, nes metų ataskaitų valiuta nesubalansuota. Ką tai reiškia?

Ši klaida gali kilti įjungus funkciją **Informacijos bendrinimas tarp didžiosios knygos atsiskaitymo ir metų pabaigos uždarymo** (informacijos funkcija). Įjungus funkciją, didžiosios knygos operacijos, kurios buvo sudengtos, nebebus įtrauktos į pradinį kitų finansinių metų balansą vykdant didžiosios knygos uždarymą metų pabaigoje. Neįtraukus didžiosios knygos operacijų, kurios yra sudengtos, klientams gali kilti sunkumų per uždarymą metų pabaigoje, jei didžioji knyga apibrėžta su ataskaitų valiuta.   
Didžiosios knygos sudengimas atliekamas tik apskaitos valiutai.  Kai didžiosios knygos operacijos yra sudengtos, tikrinimu užtikrinama tik tai, kad apskaitos valiutos debetai bus lygūs apskaitos valiutos kreditams. Šių didžiosios knygos operacijų ataskaitų valiutos sumos nėra patvirtintos ir negali būti debetų, lygių kreditams.  Be to, didžiosios knygos sudengimas automatiškai neskaičiuoja ir neregistruoja pelno / nuostolio ataskaitų valiuta.  Dėl šių apribojimų pelno / nuostolio operacija turi būti ataskaitų valiuta atliekant didžiosios knygos sudengimą.  Jei pelnas / nuostolis neįtrauktas į didžiosios knygos sudengimą, bus pateiktas pranešimas, kad uždarymas metų pabaigoje nepatenka į balansą.  Daugiau informacijos žr. [Informacijos bendrinimo tarp didžiosios knygos atsiskaitymo funkcija ir ataskaitų valiuta nepatenka į balansą](reporting-currency-yec.md).

## <a name="general-ledger-what-can-be-changed-to-help-enhance-the-performance-of-year-end-processing"></a>Didžioji knyga: ką galima pakeisti siekiant padėti padidinti metų pabaigos apdorojimo našumą?

Galite atlikti keletą pakeitimų siekdami padėti pagerinti uždarymo metų pabaigoje našumą. Rekomenduojame peržiūrėti šiuos siūlomus pakeitimus ir nustatyti, ar jie tinka jūsų organizacijai.

### <a name="optimize-year-end-close-service"></a>Uždarymo metų pabaigoje optimizavimo paslauga

Paslauga **Uždarymo metų pabaigoje optimizavimas** suteikia „Microsoft Dynamics 365 Finance“ klientams galių paspartinti uždarymą metų pabaigoje perkeliant sudėtingą uždarymo metų pabaigoje procesą į mikrotarnybą. Laikas, sutaupytas efektyviai atliekant uždarymą metų pabaigoje, leidžia kiekvienai „Finance“ komandai laiku reaguoti į reikiamus koregavimus ir gauti sugeneruotas finansines ataskaitas. Apdorojant uždarymą metų pabaigoje mikrotarnyboje, atlaisvinami vertingi ištekliai. Apdorojimo pakilimas sumažina SQL serverio apkrovą ir klientams suteikia galimybę paspartinti uždarymo metų pabaigoje apdorojimą.

Paslauga **Uždarymo metų pabaigoje optimizavimas** pasiekiama 10.0.31 versijoje, kad daugiau klientų galėtų naudotis nauja paslauga 2022 metų pabaigos laikotarpiu. Be to, paslauga buvo atnaujinta senesnėse 10.0.30 ir 10.0.29 versijose. Daugiau informacijos ieškokite dalyje [Uždarymo metų pabaigoje optimizavimas](optimize-year-end-close.md).

### <a name="dimension-sets"></a>Dimensijų rinkiniai

Kai vykdote uždarymą metų pabaigoje, kiekvienas dimensijų rinkinio balansas sukuriamas iš naujo. Toks veikimas turi tiesioginės įtakos našumui. Kai kurios organizacijos bereikalingai kuria dimensijų rinkinius, nes jie kažkada buvo naudojami arba gali būti naudojami tam tikru metu. Kadangi šie nebūtini dimensijų rinkiniai vis tiek perkuriami vykdant uždarymą metų pabaigoje, prie proceso pridedamas laikas. Skirkite pakankamai laiko įvertinti savo dimensijų rinkinius ir panaikinti tuos, kurie nėra būtini.

Nebūtini dimensijų rinkiniai taip pat daro įtaką paketinei užduočiai **BudgetDimensionFocusInitializeBalance** (**Didžioji knyga \> Sąskaitų planas \> Dimensijos \> Finansinių dimensijų rinkiniai**).

[![Finansinių dimensijų rinkiniai.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Uždarymo metų pabaigoje šablono konfigūravimas

Uždarymo metų pabaigoje šablonas leidžia organizacijoms pasirinkti finansinės dimensijos lygį, kurį reikia išlaikyti perkeliant pelno ir nuostolio balansus į nepaskirstytą pelną. Parametrai leidžia organizacijai tvarkyti išsamias finansines dimensijas (**Uždaryti viską**) perkeliant balansus į nepaskirstytą pelną arba pasirinkti sumuoti sumas į vieną dimensijos vertę (**Uždaryti vieną**). Tai galima apibrėžti nurodyti kiekvienai finansinei dimensijai. Daugiau informacijos apie šiuos parametrus žr. straipsnyje [Uždarymas metų pabaigoje](year-end-close.md).

Rekomenduojame įvertinti savo organizacijos poreikius ir, jei galima, uždaryti kuo daugiau dimensijų naudojant uždarymo metų pabaigoje parinktį **Uždaryti vieną**, kad padidintumėte našumą. Uždarant vieną dimensijos vertę (kuri taip pat gali būti tuščia vertė), sistema, nustatydama nepaskirstyto pelno apskaitos įrašų balansus, apdoroja mažiau informacijos.

### <a name="degenerate-dimensions"></a>Faktų dimensijos

Faktų dimensijos beveik negalima arba iš viso negalima pakartotinai naudoti atskirai arba su kitomis dimensijomis. Faktų dimensijos yra dviejų tipų. Pirmasis tipas yra dimensija, kuri yra atskirai faktinė. Paprastai šis faktų dimensijos tipas bus rodomas tik vienoje operacijoje arba mažuose operacijų rinkiniuose. Antrasis tipas – tai dimensija, kuri tampa faktinė kartu su viena arba daugiau papildomų dimensijų, parodančių tą patį potencialą, remiantis galimais deriniais, kurie gali būti sukurti. Faktinė dimensija gali labai paveikti uždarymo metų pabaigoje efektyvumą. Norėdami sumažinti efektyvumo problemas iki minimumo, uždarymo metų pabaigoje sąrankoje apibrėžkite visas faktines dimensijas kaip **Uždaryti vieną**, kaip apibrėžta ankstesniame skyriuje.

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>Mokėtinos sumos: kokie pakeitimai atlikti siekiant palaikyti 2022 m. 1099 metų pabaigos ataskaitas?

#### <a name="update-to-all-1099-forms"></a>Atnaujinti į visas 1099 formas

Buvo atlikti šie 2022 m. mokestinamų metų visų 1099 formų pakeitimai:

- 2021 m. buvo fiksuoti 1099 formose. Pradedant nuo 2022 m., metai užpildomi pagal ataskaitą.

#### <a name="1099-misc"></a>1099-MISC

Buvo atlikti šie 2022 m. mokestinamų metų 1099-MISC formos naujinimai:

- 13 langelis: Dabar nurodo užsienio sąskaitoms taikomų mokestinių prievolių vykdymo akto (FATCA) pildymo reikalavimą.
- 14 langelis: dabar naudojamas norint pateikti ataskaitą apie per didelius auksinių parašiutų mokėjimus.
- 15 langelis: dabar naudojamas norint pateikti ataskaitą apie mokėjimo pagal nenustatytas atidėtas kompensacijas (NQDC) planus.
- 16 langelis: dabar naudojamas norint teikti ataskaitą apie valstybės išskaičiuotus mokesčius.
- 17 langelis: dabar naudojamas teikti ataskaitą apie mokėtojo valstybės numerį.
- 18 langelis: dabar naudojamas norint teikti ataskaitą apie valstybės pajamas.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Mokėtinos sumos: 1099 – kaip pakeisti 1099 lauką ir tiekėjo, kuris per metus nesekė 1099 informacijos, vertes?

Naudokite funkciją **Atnaujinti 1099**, kad peržiūrėtumėte ankstesnes sumokėtų sąskaitų faktūrų operacijas ir iš naujo priskirtumėte 1099 duomenis tinkamu būdu pagal skirtuko **1099 mokestis** puslapyje **Tiekėjas** parametrus. Norėdami naudoti funkciją **Atnaujinti 1099**, eikite į **Mokėtinos sumos \> Tiekėjai \> Visi tiekėjai**, pasirinkite tiekėją, tada veiksmų srityje skirtuke **Tiekėjas** pasirinkite **Atnaujinti 1099**.

## <a name="can-i-run-the-update-1099-functionality-for-all-my-vendors-at-once"></a>Ar galima paleisti visiems tiekėjams funkciją Atnaujinti 1099 vienu metu?

Galite naudoti puslapį **Atnaujinti kelių tiekėjų 1099 informaciją** 1099 laukui atnaujinti tiekėjo įraše ir operacijoms atnaujinti įtraukdami informaciją iš 1099 lauko. Norėdami atidaryti šį puslapį, eikite į **Mokėtinos sumos \> Periodinė užduotis \> 1099 mokestis**. Norėdami pasiekti puslapį, jums turi būti priskirta **Atnaujinti kelių tiekėjų 1099 lauką ir operacijas** saugos teisė.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Mokėtinos sumos: 1099 – 1099 naujinimo priemonės funkcijos Perskaičiuoti esamas 1099 sumas ir Naujinti viską

Žymės langelis **Perskaičiuoti esamas 1099 sumas** iš naujo nustatys 1099 sumą pagal bendrą sumokėtų verčių sumą, kai naudojama kartu su žymės langeliu **Naujinti viską**.

[![Mokesčio 1099 operacijos: prieš vykdant naujinimo procedūrą.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Žymės langelis **Perskaičiuoti esamas 1099 sumas** naudojamas tik tada, kai sąskaitoje faktūroje yra dalinių 1099 verčių arba sąskaita faktūra buvo modifikuota formoje 1099 mokestis. Tarkime, kad jūsų sąskaitos faktūros vertė yra 1000,00 $, tačiau vartotojas rankiniu būdu įveda 500,00 $ 1099 sumą į sąskaitą faktūrą.

[![1099 mokesčio operacijos: pažymėjimas abiejų parinkčių Naujinti viską ir Perskaičiuoti esamas 1099 sumas.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Kai bus sąskaita faktūra bus apmokėta, 500,00 $ suma bus sumokėta 1099 suma. Jei atliekate perskaičiavimo procedūrą, 1099 suma bus pakeista į 1000,00 $; kuri yra bendroji sumokėta suma.

[![1099 mokesčio operacijos: paleidus 1099 procedūrą.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Mokėtinos sumos: 1099 – 1099 operacijų kūrimas rankiniu būdu

Organizacijai gali prireikti rankiniu būdu sukurti 1099 operacijas, kurios nėra susietos su SF. Galite įtraukti neautomatines 1099 operacijas eidami į **Mokėtinos sumos \> Periodinės užduotys \> Mokesčiai 1099 \> Tiekėjo sudengimas 1099**. Pasirinkite mygtuką **Rankinės 1099 operacijos**.

Rankiniu būdu sukurtos 1099 operacijos neatnaujinamos naudojant procesą **Naujinti viską** arba procesą **Perskaičiuoti esamas 1099 sumas** priemonėje **Naujinti 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Mokėtinos sumos: 1099 – ar „Dynamics 365 Finance“ palaiko 1096 formą?

„Dynamics 365 Finance“ nespausdina 1096 metinės JAV informacijos grąžinimų suvestinės ir perdavimo formos.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Mokėtinos sumos: 1099 – ar yra naujų funkcijų, kurios palaiko viešajam sektoriui skirtas 1099 ataskaitas?

Pridėta nauja viešojo sektoriaus funkcija **Naujinti 1099 informaciją pagal pagrindinę sąskaitą**, kurią galima įjungti darbo srityje **Funkcijų valdymas**. Ši funkcija leidžia susieti tiekėjo 1099 vertes pagal pagrindinę sąskaitą apskaitos paskirstyme, o ne pagal numatytąją tiekėjo įrašo sąskaitą.

Daugiau informacijos žr. [Tiekėjų nustatymas 1099 ataskaitoms](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
