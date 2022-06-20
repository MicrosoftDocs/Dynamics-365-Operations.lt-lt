---
title: GS1 brūkšniniai kodai
description: Šiame straipsnyje aprašoma, kaip nustatyti GS1 brūkšninius kodus ir QR kodus, kad žymės būtų nuskaitomos sandėlyje.
author: Mirzaab
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 67c54f344ff7091f4a25198fdafa745c6c84d5d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907151"
---
# <a name="gs1-bar-codes"></a>GS1 brūkšniniai kodai

[!include [banner](../includes/banner.md)]

Sandėlio darbuotojai dažnai turi atlikti keletą užduočių, kai, naudodami mobilųjį skaitytuvą, registruoja prekės, padėklo ar konteinerio judėjimą. Šios užduotys gali apimti ir brūkšninių kodų nuskaitymą, ir rankinį informacijos įvedimą mobiliajame įrenginyje. Brūkšniniams kodams naudojamas konkrečios įmonės formatas, kurį nustatote ir tvarkote naudodami „Microsoft Dynamics 365 Supply Chain Management“.

Siekiant užtikrinti visuotinį įmonių duomenų mainų standartą, buvo sukurtas siuntimo žymių GS1 brūkšninis kodas. Jie galimi ir linijinėmis (1D) simboliais (brūkšninių kodų formatais), pvz., GS1-128, ir 2D simboliais, pvz., GS1 DataMatrix ir GS1 QR kodais. GS1 brūkšniniai kodai ne tik užkoduoja *duomenis*, bet ir leidžia naudoti iš anksto apibrėžtą programos identifikatorių sąrašą, siekiant apibrėžti šių duomenų reikšmę. GS1 standartas apibrėžia duomenų formatą ir įvairius duomenis, kuriuos galima naudoti norint kažką užkoduoti. Skirtingai nei senesnių brūkšninių kodų standartai, GS1 brūkšniniuose koduose gali būti keletas duomenų elementų. Todėl, vieną kartą nuskaičius brūkšninį kodą, galima užfiksuoti kelių tipų produkto informaciją, pvz., paketą ir galiojimo datą.

GS1 palaiko tiekimo grandinės valdymą, pagal ką paprasčiau nuskaityti sandėlius, kur padėklai ir konteineriai žymimi naudojant brūkšninius kodus GS1 formatu. Sandėlio darbuotojai visą reikiamą informaciją gali gauti vieną kartą nuskaitę GS1 brūkšninį kodą. Kadangi nebereikia kelis kartus nuskaityti ir (arba) rankiniu būdu įvesti informacijos, GS1 brūkšniniai kodai padeda sumažinti užduotims atlikti reikiamą laiką. Taip pat jie padeda padidinti tikslumą.

Logistikos vadovai turi nustatyti reikiamą programos identifikatorių sąrašą ir kiekvieną iš jų susieti su atitinkamais mobiliojo įrenginio meniu elementais. Tada programos identifikatorius sandėliuose galima naudoti kaip visuotinį perkėlimo ir pakavimo parametrą. Todėl visos siuntimo etiketės bus vienodo formato.

Jei nenurodyta kitaip, šiame straipsnyje *naudojamas* terminas Brūkšninis kodas, kad būtų galima naudoti ir linijinius (1D) brūkšninius kodus, ir 2D brūkšninius kodus.

## <a name="the-gs1-bar-code-format"></a>GS1 brūkšninio kodo formatas

GS1 bendrosios specifikacijos nurodo, kuriuos simbolius galima naudoti GS1 brūkšniniams kodams, ir kaip koduoti brūkšninio kodo duomenis. Šiame skyriuje pateikiama trumpas straipsnio įžanga. Norėdami gauti daugiau informacijos, žr [. GS1 bendrąsias specifikacijas](https://www.gs1.org/docs/barcodes/GS1_General_Specifications.pdf), kurias publikuos GS1. GS1 specifikacijų dokumentas yra reguliariai atnaujinamas, o jo pateikiama informacija yra naujausia su GS1 bendrųjų specifikacijų išleidimas 22.0.

GS1 brūkšniniuose koduose naudojami šie simboliai:

- **Linijiniai arba 1D brūkšniniai kodai** – GS1-128 ir GS1 DataBar
- **2D brūkšniniai kodai** – GS1 DataMatrix, GS1 QR kodas ir GS1 taškinis kodas

Atkreipkite dėmesį, kad GS1-128 specialiai nurodo GS1, kuris yra specialus įprasto kodo-128 linijinio brūkšninio kodo, GS1 DataMatrix ir GS1 QR kodo atvejis. Skirtumas tarp GS1 versijos ir ne GS1 versijos – tai, kad brūkšninio kodo duomenyse kaip pirmas simbolis yra specialusis simbolis (F²1). F JŲ1 simbolis nurodo, kad duomenys brūkšniniuose koduose turi būti suprantami pagal GS1 specifikaciją.

Patys brūkšninio kodo duomenys susideda iš kelių duomenų elementų, iš kurių kiekvienas identifikuojamas programos identifikatoriumi lauko pradžioje. Paprastai duomenys taip pat pateikiami su brūkšniniu kodu žmogiškuoju formatu, kur programos identifikatorius rodomas skliausteliuose. Pavyzdys: `(01) 09521101530001 (17) 210119 (10) AB-123`. Šiame brūkšninie kode yra trys elementai:

- **Programos identifikatorius 01** – GS1 prekės pasaulinis prekybos prekės numeris (GTIN).
- **Programos identifikatorius 17** – galiojimo pabaigos data.
- **Programos identifikatorius 10** – paketo numeris.

Kiekvieno elemento duomenys gali būti arba iš anksto nustatyti, arba kintami. Yra fiksuotas iš anksto nustatytų ilgių programos identifikatorių sąrašas. Visų kitų programų identifikatorių ilgis yra kintamas, o GS1 programos identifikatorių sąrašas nurodo maksimalų duomenų ilgį ir formatą. Pavyzdžiui, iš anksto nustatytas 01 programos identifikatoriaus ilgis yra 16 simbolių (vienas – pats programos identifikatorius, tada – 14 GTIN), o programos identifikatorius 17 turi iš anksto nustatytą aštuonių simbolių ilgį (du – pačiam programos identifikatoriui, o tada – šešiems – dienai). Tačiau programos identifikatorius 10 turi du numerius ir po to – iki 20 raidinių-skaitinių simbolių.

Kai elementai sudedami kartu, jei elementas seka kintamojo ilgio elementą, turi būti naudojamas skyriklio simbolis. Šis skyriklis gali būti specialusis FIKLIS1 simbolis arba grupės skyriklio simbolis (nespausdinamas simbolis, kuriame yra ASCII kodas 29 ir šešioliktainis kodas 1D). Skyriklis negali būti naudojamas po paskutinio elemento. Nors skyriklis taip pat neturi būti naudojamas po elementų, kurie turi iš anksto nustatytą ilgį, jo buvimo klaida nėra kritinė klaida.

Ankstesnio brūkšninio kodo, kuriame yra 01, 17 ir 10 identifikatorių, brūkšninio kodo duomenys, esantys kode-128, QR kode arba DataMatrix `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` simboliais, bus užkoduoti kaip (programos identifikatoriai rodomi paryškintuoju šriftu). Geriausia būtų pabaigti bet kurį elementą, kurio ilgis kintamas, kad būtų pašalintas papildomų grupės skyriklių simbolių poreikis. Tačiau brūkšninis kodas taip pat gali turėti skirtingą elementų tvarką, kai skyriklis yra privalomas. Čia yra pavyzdys:`<FNC1>`**`01`**`09521101530001`**`10`**`AB-123<GS>`**`17`**`210119`.

### <a name="dates-and-decimal-numbers"></a>Datos ir dešimtainiai skaičiai

Datos visada vaizduojamos *YYMMDD* formatu, kur metų amžių nustato GS1 specifikacijos. Gali būti nurodytos tik tos datos, kurios yra nuo 49 metų praeityje iki 50 metų ateityje (susijusios su šiais metais).

Kai kuriuose duomenų elementuose yra dešimtainių skaičių. Pavyzdžiui, prašymo identifikatoriai 3100, 3101, ... 3105 nurodo grynąjį svorį kilogramais. Šių programos identifikatorių ilgis iš anksto nustatytas 10, yra šeši galimi kiekio skaičiai. Dešimtainio skyriklio pozicija nurodoma pagal paskutinį programos identifikatoriaus numerį. Todėl ši programų identifikatorių šeima taip pat gali būti vaizduojama *310n*. Kadangi GS1 standartas nurodo, kad į kairę nuo dešimtainio skyriklio visada turi būti bent vienas skaičius, leidžiamas daugiausiai penkios dešimtainės trupmenos skaitmenys.

Pateikiami keli pavyzdžiai, kurie parodo, kaip numerių *123456* bus interpretuoti pagal skirtingus programos identifikatorius (rodomas paryškintuoju šriftu):

- **`3100`**`123456`&rarr; 123456 (integer)
- **`3101`**`123456`&rarr; 12345.6 (viena dešimtainė vieta)
- **`3102`**`123456`&rarr; 1234,56 (su dviem dešimtainėmis dalimis)
- **`3103`**`123456`&rarr; 123.456 (trys skaitmenys po dešimtainio kablelio)
- **`3104`**`123456`&rarr; 12,3456 (keturi skaičiai po kablelio)
- **`3105`**`123456`&rarr; 1.23456 (penki skaitmenys po dešimtainio kablelio)

## <a name="scanning-gs1-bar-codes-in-supply-chain-management"></a>GS1 brūkšninių kodų nuskaitymas tiekimo grandinės valdymo dalyje

Norėdami nuskaityti GS1 brūkšninius kodus, sandėlio darbuotojai naudoja skaitytuvą, įtaisytą mobiliajame įrenginyje arba prie jo prijungtą. Tada skaitytuvas persiunčia nuskaitytą brūkšninią kodą į sandėlio valdymo mobiliąją programą kaip klaviatūros įvykių seriją. Šis operacijos būdas taip pat vadinamas klaviatūros *klavišo nudažoma* *ar nudažoma*. Tada mobilioji programa siunčia gautą tekstą kaip tiekimo grandinės valdymą. Kai sistema gauna įvesties duomenis, pirmiausia ji nustato, ar duomenys prasideda vienu iš sukonfigūruotų prefiksų, kurie nurodo, kad duomenys iš tikrųjų yra GS1 brūkšninis kodas ([žr. skyrių Nustatyti visuotines GS1 pasirinktis](#set-gs1-options)). Jei nuskaityti duomenys prasideda vienu iš šių prefiksų, sistema naudoja GS1 analizatorių duomenims išanalizuoti ir išskleisti atskirus duomenų elementus pagal jų programos identifikatorius. Kai duomenys išanalizuoti, nuskaityti duomenys bus užpildyti arba dabartiniu įvesties lauku, arba keliais laukais.

### <a name="configuration-of-bar-code-scanner-hardware-and-software"></a>Brūkšninių kodų skaitytuvo aparatūros ir programinės įrangos konfigūracija

Kad tiekimo grandinės valdymas galėtų teisingai atpažinti ir iššifruoti GS1 brūkšninius kodus, aparatūros skaitytuvas arba palaikymo programinė įranga turi būti sukonfigūruota atlikti šiuos veiksmus:

- Pridėti prefiksą prie nuskaitytų brūkšninių kodų, kad sistema galėtų atpažinti GS1 brūkšninius kodus.
- Konvertuoti nespausdinamas ASCII grupės skyriklio simbolį (ASCII kodas 29 arba šešioliktainis kodas 1D) į spausdinamą simbolį, pvz., tilde (~).

Nors prie nuskaityto brūkšninio kodo galima pridėti bet kokį prefiksą, galima naudoti ir ISO/IEC 15424 simbolių identifikatorių, *taip pat vadinamą KLAVIŠĄ IDENTIFIER*. Prasideda šis trijų `]` simbolių identifikatorius, jame yra vienas simbolis, identifikuojantis naudojamą simbolį ir numeris, kuris naudojamas kaip tolesnis modifikatorius. Pavyzdžiui, THE `]C1` identifikatorius nurodo kodą 128 (`C` dėl simbolio), o modifikatorius `1` nurodo, kad pirmoje duomenų vietoje yra F TAMS1 simbolis. Kita vertus, tai `]C0` 128 brūkšninis kodas, kuriame kaip pirmas duomenų ženklą yra bet koks kitas simbolis.

Šie penki simbolių identifikatoriai atitinka GS1 brūkšninius kodus, kurie turi programos identifikatoriaus elementus:

- `]C1`– kodas 128 (`C`) su F²1 simboliu pirmoje vietoje (`1`), taip pat vadinamas GS1-128.
- `]e0`– GS1 DataBar.
- `]d2`– DataMatrix (`d`) su ECC 200 ir FARI1 pirmomis padėtimi (`2`), taip pat žinomas kaip GS1 DataMatrix.
- `]Q3`– QR kodas (`Q`) 2 modelio simbolis su FARI1 pirmomis padėtimi (`3`), taip pat vadinamas GS1 QR kodu.
- `]J1`– GS1 taškinis kodas.

Naudojant šiuos identifikatorius, siekiant pašalinti identifikatorius, kurie neatitinka GS1 identifikatorių, reikia sukonfigūruoti skaitytuvus ar nuskaityti programinę įrangą, kad būtų pašalinti visi identifikatoriai, kurie neatitinka GS1 identifikatorių. Pavyzdžiui, jei nuskaitysite "įprastą" 39 kodo brūkšninius kodus, bus pridėtas `]A0` prefiksas. Kadangi sistema nesupras šio prefikso kaip vieno iš GS1 prefiksų, jis bus interpretuoti kaip duomenys ir duoda netikėtų rezultatų.

> [!NOTE]
> Dėl patogumų, 2.0.17.0 ir vėliau sandėlio valdymo mobiliųjų įrenginių programos versija pašalins visus OF prefiksus, kurie nėra įtraukti į ankstesnį sąrašą. Taip galima naudoti atvejus, kai galima sukonfigūruoti skaitytuvą pridėti PREfiksĄ THE, bet ne pašalinti nepageidaujamų prefiksų.

### <a name="single-and-multiple-field-scanning"></a>Vieno ir kelių laukų nuskaitymas

Kai duomenys išanalizuoti iš brūkšninio kodo, jie bus pateikti mobiliojo įrenginio srauto valdikliuose. Yra du metodai, kurie bus apdoroti jų ruožtu:

- **Vieno lauko nuskaitymas** – šiuo metodu užpildomas tik tas laukas, į kurį buvo nuskaitytas brūkšninis kodas. Pavyzdžiui, jei nuskaitysite brūkšninius `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`**kodus**, kai žymeklis yra lauke Prekė, į tą lauką bus įvestas GTIN `09521101530001` iš brūkšninio kodo. Jei nuskaitysite tą patį brūkšninią kodą, kai žymeklis **yra lauke Paketo ID**, bus įvestas `AB-123` partijos numeris iš brūkšninio kodo. Šis režimas veikia visuose laukuose visuose srautuose ir reikalauja konfigūruoti tik bendrąjį GS1 nustatymą. Jei brūkšninis kodas turi keletą elementų, jį vis tiek reikia nuskaityti kelis kartus, nes į mobiliojo įrenginio srautą bus įvesta tik viena brūkšninio kodo dalis. Šį elgseną kontroliuoja GS1 bendrasis nustatymas, kaip aprašyta [skyriuje Nustatyti bendrąjį GS1 nustatymą](#generic-gs1-setup).
- **Kelių laukų nuskaitymas** – šis metodas užpildo kelis laukus, kai nuskaitomas vienas brūkšninis kodas, perstumdamas papildomus duomenis į mobiliojo įrenginio srauto būseną. Pavyzdžiui, strategija sukonfigūruota taip, kad į lauką būtų perstumtas programos identifikatorius 01 `ItemId` į valdiklio ir programos identifikatorių `InventBatchId` 10. Šiuo atveju, jei nuskaitysite brūkšninius `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` kodus, abiejų kintamųjų duomenys bus stumdami tuo pačiu metu. Todėl sistema neįsiųs jūsų apie srauto prekės ir (arba) paketo numerį. Šį elgseną kontroliuoja GS1 strategijos, susietos su meniu elementais, [kaip aprašyta GS1 strategijų, kurios turi būti taikomos mobiliųjų įrenginių meniu elementams,](#policies-for-menus) skyriuje Nustatyti GS1.

> [!WARNING]
> Numatytosios GS1 strategijos patikrintos taip, kad veiktų be netikėto veikimo būdo. Tačiau GS1 strategijų, susietų su meniu elementais, tinkinimas gali sukelti netikėtą elgseną, nes sraute gali nepavykti kai kurių duomenų, kurie bus pasiekiami tam tikru laiku.

## <a name="turn-on-the-gs1-feature"></a>GS1 funkcijos įjungimas

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Warehouse management*
- **Priemonės pavadinimas: nuskaityti** *GS1 brūkšninius kodus*

### <a name="turn-on-the-enhanced-parser-for-gs1-barcodes-feature"></a>Įjungti išplėstinį GS1 brūkšninių kodų funkcijos analizatorių

Jei naudojate GS1 brūkšninius kodus, *rekomenduojame įgalinti ir GS1 brūkšninių kodų funkcijos išplėstinį analizatorių*. Ši funkcija leidžia patobulintas GS1 brūkšninio kodo analizatoriaus diegimas. Jame pridėti šie patobulinimai:

- Jis atitinka GS1 bendrosios specifikacijos algoritmą, naudojamą simbolių duomenims išanalizuoti ir patikrinti, ar simbolio duomenys galioja pagal specifikaciją.
- Nesvarbu, kad jūs norite nustatyti maksimalų identifikatoriaus **reikšmės** ilgį ir naudosite ilgiausią prefikso gretinimą naudojant sukonfigūruotus programos identifikatorius.
- Naudodami raidę n *galite lengviau konfigūruoti dešimtainius programos identifikatorius, kad jis atitiktų* bet kokį skaičių. Pavyzdžiui, užuot atskirę atskirus programų identifikatorius (3101 *, 3102* *,* 3103 *ir taip toliau), galite konfigūruoti tik vieną programos identifikatorių (* *310n*).
- Tai pataiso problemą, kai netinkamai užkoduoti duomenys yra suprantami kaip lauko duomenys.
- Jis pateikiamas kaip atskira klasė, kurią galima pakartotinai naudoti kituose kontekstuose ir leidžia naudoti extensibility tašką nuskaityties duomenims valdyti prieš užpildant srauto laukus.

## <a name="set-up-global-gs1-options"></a><a name="set-gs1-options"></a>Visuotinių GS1 parinkčių nustatymas

Puslapyje **Sandėlio valdymo parametrai** pateikiami keli parametrai, kuriais nustatomos visuotinės GS1 parinktys.

Norėdami nustatyti visuotines GS1 parinktis, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
1. „FastTab“ skirtuke **Brūkšniniai kodai** nustatykite toliau nurodytus laukus.

    - **FVZ1 simbolis**, **Datamatrix** simbolis ir QR **kodo simbolis – nurodykite simbolius,** kurie turėtų būti suprantami kaip kiekvieno GS1 brūkšninio kodo tipo prefiksas.
    - **Grupės skyriklis** – nurodykite simbolį, kuris pakeičia ASCII grupės skyriklio simbolį.
    - **Maksimalus identifikatoriaus ilgis** – nurodykite maksimalų leidžiamą programos identifikatoriaus simbolių skaičių. Šis laukas nėra būtinas, jei jūsų sistemoje *įjungta išplėstinė GS1* analizatoriaus funkcija.

> [!NOTE]
> Prefiksai nurodo sistemai, kad brūkšninis kodas užkoduotas pagal GS1 standartą. Vienu metu įvairiais tikslais galima naudoti iki trijų prefiksų (**FNC1 simbolis**, **Duomenų matricos simbolis** ir **QR kodo simbolis**).

## <a name="gs1-application-identifiers"></a>GS1 prašymo identifikatoriai

GS1 formatai ne tik užkoduoja duomenis, bet ir leidžia naudoti iš anksto apibrėžtą programos identifikatorių sąrašą duomenų reikšmei nustatyti. Logistikos vadovai turi nustatyti reikiamą programos identifikatorių sąrašą ir kiekvieną iš jų susieti su atitinkamais mobiliojo įrenginio meniu elementais. Tada identifikatorius sandėliuose galima naudoti kaip visuotinį perkėlimo ir pakavimo parametrą. Todėl visos siuntimo etiketės bus vienodo formato.

Sistema naudoja duomenis, ypač iš anksto nustatytus programos identifikatorius, taisyklėms, kurios turi būti taikomos atitinkamai nuskaitytai informacijai, nustatyti.

Kiekvienas programos identifikatorius sistemai nurodo, kad vėlesni nuskaityto brūkšninio kodo simboliai turi būti laikomi užšifruotos informacijos bloku. Programos identifikatorių nustatymas apibrėžia, kaip sistema turi interpretuoti brūkšninį kodą ir jį įrašyti kaip reikšmę sistemoje.

Logistikos vadovai gali naudoti standartinius tarptautinius programos identifikatorius ir (arba) sukurti savus.

### <a name="load-the-standard-application-identifiers"></a>Standartinių programos identifikatorių įkėlimas

Norėdami greitai pradėti darbą, galite įkelti įprastų tarptautinių programos identifikatorių sąrašą. Jei reikia, sąrašą galite išplėsti arba redaguoti vėliau.

Norėdami įkelti standartinius programos identifikatorius, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> GS1 \> GS1 programos identifikatoriai**.
1. Veiksmų juostoje pasirinkite **Sukurti nustatytąją sąranką**.

> [!WARNING]
> Komanda **Kurti numatytąją sąranką** panaikina visus šiuo metu nustatytus programos identifikatorius ir pakeičia juos standartiniu sąrašu. Tačiau įkėlę numatytąją sąranką, jei reikia, galite sąrašą tinkinti.

### <a name="set-up-custom-application-identifiers"></a>Pasirinktinių programos identifikatorių nustatymas

Jei kai kurie arba visi programos identifikatoriai, kuriuos naudoja jūsų įmonė, skiriasi nuo standartinio rinkinio, galite kurti savo kodus nuo pradžių arba tinkinti standartinį rinkinį taip, kaip jums reikia.

Norėdami nustatyti ir tinkinti savo GS1 programos identifikatorius, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> GS1 \> GS1 programos identifikatoriai**.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami sukurti naują identifikatorių, veiksmų srityje pasirinkite **Naujas**.
    - Norėdami redaguoti esamą identifikatorių, pasirinkite identifikatorių, tada veiksmų srityje pasirinkite **Redaguoti**.

1. Nustatykite tolesnius naujo arba pasirinkto identifikatoriaus laukus.

    - **Programos identifikatorius** – įveskite programos identifikatoriaus identifikavimo kodą. Paprastai šis kodas yra dviejų skaitmenų sveikasis skaičius, tačiau jis gali būti ilgesnis. Paskutinis dešimtainių verčių skaitmuo nurodo skaitmenų po kablelio skaičių. Daugiau informacijos rasite toliau šiame sąraše pateiktame žymės langelio **Dešimtainė dalis** apraše. Jei įgalinta *GS1* brūkšninių kodų funkcijos patobulinto analizatoriaus funkcija, *galite sukurti vieną visų dešimtainės trupmenos variantų programos identifikatorių naudodami raidę n* kaip paskutinį programos identifikatoriaus simbolį. Pavyzdžiui, galite konfigūruoti tik vieną programos identifikatorių (*310n*), o ne atskirą kiekvieno dešimtainio skyriklio vietos numerio identifikatorių (*3101*, *3102*, *3103* ir taip toliau).
    - **Aprašas** – įveskite trumpą identifikatoriaus aprašą.
    - **Fiksuotas ilgis** – pažymėkite šį žymės langelį, jei naudojant šį programos identifikatorių nuskaitomų verčių simbolių skaičius yra fiksuotas. Jei verčių ilgis kintamas, šį žymės langelį išvalykite. Tokiu atveju, naudodami grupių skyriklio simbolį, kurį nurodėte puslapyje **Sandėlio valdymo parametrai**, turite nurodyti vertės pabaigą.
    - **Ilgis** – įveskite maksimalų simbolių, kurie gali būti rodomi vertėse, nuskaitomose naudojant šį programos identifikatorių, skaičių. Jei pažymėtas žymės langelis **Fiksuotas ilgis**, numatomas tiksliai toks simbolių skaičius.
    - **Tipas** – pasirinkite vertės, nuskaitomos naudojant šį programos identifikatorių, tipą (*Skaitinė*, *Raidinė-skaitinė* arba *Data*). Daugiau informacijos apie tai, kaip datos ir skaičiai pateikti brūkšninio kodo duomenyse, ieškokite [skyriuje Datos ir dešimtainiai](#dates-and-decimal-numbers) skaičiai.
    - **Dešimtainė dalis** – pažymėkite šį žymės langelį, jei vertėje yra numanomas dešimtainis skyriklis. Jei šis langelis pažymėtas, sistema paskutinį programos identifikatoriaus skaitmenį naudos tam, kad nustatytų skaitmenų po kablelio skaičių. Daugiau informacijos apie tai, kaip datos ir skaičiai pateikti brūkšninio kodo duomenyse, ieškokite [skyriuje Datos ir dešimtainiai](#dates-and-decimal-numbers) skaičiai.

> [!WARNING]
> **Nors** sistema leis nustatyti bet kurio programos identifikatoriaus žymės langelį Fiksuotas ilgis, jis turėtų būti naudojamas tik programų identifikatorių, kurių ilgis GS1 bendrosiose specifikacijose yra iš anksto nustatytas, subgrupei. Išplėstinis GS1 analizatorius jau apima visų iš anksto nustatytų ilgių programos identifikatorių sąrašą.

> [!NOTE]
> Grupės **skyriklio** vertė, nurodyta sandėlio **valdymo parametrų** puslapyje, yra pasirinktinė, jei vertės, po kurios eina programos identifikatorius, ilgis yra fiksuotas.

## <a name="establish-the-generic-gs1-setup"></a><a name="generic-gs1-setup"></a>Bendrosios GS1 sąrankos nustatymas

Bendroji GS1 sąranka nustato bendrų susiejimų rinkinį. Šie susiejimai kiekvieną atitinkamą mobiliųjų įrenginių programėlės įvesties lauką sutapdina su programos identifikatoriumi, kuris valdo, kaip nuskaitytų brūkšninių kodų vertės turi būti interpretuotos ir saugomos šiame lauke. Numatyta, kad šie parametrai taikomi visiems visų mobiliojo įrenginio meniu elementų nuskaitymams. Tačiau juos viename ar daugiau konkrečių laukų gali pakeisti GS1 strategija, priskirta konkrečiam meniu elementui.

Naudojant bendrąją GS1 sąranką, vienu metu galima nuskaityti tik vieną vertę. Todėl, jei iš vieno nuskaitymo norite įkelti keletą laukų verčių, turite nustatyti atitinkamų meniu elementų GS1 strategiją.

Daugiau informacijos apie GS1 strategijas rasite kitame skyriuje.

### <a name="load-the-standard-generic-gs1-setup"></a>Standartinės bendrosios GS1 sąrankos įkėlimas

Puslapyje **Bendroji GS1 sąranka** galima įkelti standartinį mobiliojo įrenginio laukų ir standartinių programos identifikatorių susiejimų, sukurtų pagal numatytąją sąranką, rinkinį.

Norėdami nustatyti bendrąją GS1 sąranką, eikite į **Sandėlio valdymas \> Sąranka \> GS1 \> Bendroji GS1 sąranka**. Tada pasirinkite **Kurti numatytąją sąranką**, kad kiekvienam laukui, kuris paprastai naudojamas mobiliojo įrenginio meniu elementuose, būtų automatiškai priskirtas tinkamas programos identifikatorius.

> [!WARNING]
> Jei jau yra bet kokia bendroji GS1 sąranka, komanda **Kurti numatytąją sąranką** visiškai ją panaikina ir įkelia standartinę sąranką.

### <a name="customize-the-standard-generic-gs1-setup"></a>Standartinės bendrosios GS1 sąrankos tinkinimas

Norėdami tinkinti bendrąją GS1 sąranką, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> GS1 \> Bendroji GS1 sąranka**.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami sukurti naują susiejimą, veiksmų srityje pasirinkite **Naujas**.
    - Norėdami redaguoti esamą susiejimą, pasirinkite susiejimą, tada veiksmų srityje pasirinkite **Redaguoti**.

1. Nustatykite tolesnius naujo arba pasirinkto susiejimo laukus.

    - **Laukas** – pasirinkite arba įveskite mobiliųjų įrenginių programėlės įvesties lauką, kuriam turi būti priskirta gaunama vertė. Ši vertė nėra rodomas pavadinimas, kurį mato darbuotojai. Tai yra rakto pavadinimas, priskirtas pagrindinio kodo laukui. Numatytoji sąranka pateikia laukų, kurie gali būti naudingi, rinkinį ir kiekvieno lauko bei sutampančių užprogramuotų funkcijų intuityvių raktų pavadinimų. Tačiau, norint nustatyti tinkamas pasirinktis savo įdiegčiai, gali reikėti pasitarti su programavimo partneriais.
    - **Programos identifikatorius** – pasirinkite taikytiną programos identifikatorių, kaip nurodyta puslapyje **GS1 programos identifikatoriai**. Identifikatorius nustato, kaip brūkšninis kodas bus interpretuojamas ir saugomas kaip įvardytojo lauko vertė. Kai pasirenkate programos identifikatorių, lauke **Aprašas** rodomas jo aprašas.

## <a name="set-up-gs1-policies-to-be-to-mobile-device-menu-items"></a><a name="policies-for-menus"></a> Nustatyti GS1 strategijas, kurios bus taikomos mobiliojo įrenginio meniu elementams

GS1 standarto paskirtis – leisti darbuotojams įkelti keletą verčių, vieną kartą nuskaičius vieną brūkšninį kodą. Siekdami šio tikslo logistikos vadovai turi nustatyti GS1 strategijas, kurios sistemai nurodo, kaip interpretuoti kelių verčių brūkšninius kodus. Vėliau galite priskirti strategijas mobiliojo įrenginio meniu elementams, kad galėtumėte valdyti, kaip brūkšninis kodas bus interpretuojamas, kai darbuotojai jį nuskaito naudodami konkretų meniu elementą.

Jei meniu elementui nepriskirta jokia GS1 strategija, sistema gali fiksuoti tik vieną vertę. Ši vertė taikoma mobiliųjų įrenginių programėlės įvesčiai, kuri pasirenkama darbuotojui atlikus nuskaitymą, kaip nurodyta bendrojoje GS1 sąrankoje. Jei GS1 strategija priskirta meniu elementui, sistema vis tiek naudoja bendrąją GS1 sąranką, kad pirmą brūkšninio kodo vertę susietų su pasirinktu lauku. Tačiau tada ji gali fiksuoti papildomas lauko vertes, kaip nurodyta taikomoje strategijoje.

### <a name="load-the-standard-specific-gs1-policies"></a>Standartinių konkrečių GS1 strategijų įkėlimas

Norėdami greitai pradėti darbą, galite įkelti GS1 strategijų rinkinį. Jei reikia, strategijas galite išplėsti arba redaguoti vėliau.

Norėdami įkelti standartinius programos identifikatorius, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> GS1 \> GS1 strategija**.
1. Veiksmų juostoje pasirinkite **Sukurti nustatytąją sąranką**.

> [!WARNING]
> Komanda **Kurti numatytąją sąranką** panaikina visas šiuo metu nustatytas strategijas ir pakeičia jas standartiniu strategijų rinkiniu. Tačiau įkėlę numatytąją sąranką, jei reikia, galite strategijas tinkinti.

### <a name="set-up-custom-specific-gs1-policies"></a>Pasirinktinių konkrečių GS1 strategijų nustatymas

> [!WARNING]
> Kai kurios GS1 strategijos gali neveikti su kiekvienu mobiliuoju srautu, kurį naudojate. Konfigūruokite pasirinktines GS1 strategijas, turite patikrinti mobiliojo įrenginio srautą naudodami skirtingas informacijos dalis, kurios nuskaitomos skirtinguose srauto taškuose. Tokiu būdu galite nustatyti, ar srauto darbo eiga, kaip tikitės.

Norėdami nustatyti ir tinkinti savo GS1 strategijas, atlikite tolesnius veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> GS1 \> GS1 strategija**.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami sukurti naują strategiją, veiksmų srityje pasirinkite **Nauja**.
    - Norėdami redaguoti esamą strategiją, pasirinkite ją sąrašo srityje.

1. Naujos arba pasirinktos strategijos antraštėje nustatykite tolesnius laukus.

    - **Strategijos pavadinimas** – įveskite strategijos pavadinimą.
    - **Aprašas** – įveskite trumpą strategijos aprašą.

1. Po antrašte esančiame „FastTab“ skirtuke susiekite laukų pavadinimus su programos identifikatoriais, kaip reikalauja dabartinė strategija. Naudokite mygtukus įrankių juostoje, kad pagal poreikį įtrauktumėte ar pašalintumėte eilutes. Kiekvienai eilutei nustatykite šiuos laukus:

    - **Laukas** – pasirinkite arba įveskite mobiliųjų įrenginių programėlės įvesties lauką, kuriam turi būti priskirta gaunama vertė. Ši vertė nėra rodomas pavadinimas, kurį mato darbuotojai. Tai yra rakto pavadinimas, priskirtas pagrindinio kodo laukui. Numatytoji sąranka pateikia laukų, kurie gali būti naudingi, rinkinį ir kiekvieno lauko bei sutampančių užprogramuotų funkcijų intuityvių raktų pavadinimų. Tačiau, norint nustatyti tinkamas pasirinktis savo įdiegčiai, gali reikėti pasitarti su programavimo partneriais.
    - **Programos identifikatorius** – pasirinkite taikytiną programos identifikatorių, kaip nurodyta puslapyje **GS1 programos identifikatoriai**. Identifikatorius nustato, kaip brūkšninis kodas bus interpretuojamas ir saugomas kaip įvardytojo lauko vertė. Kai pasirenkate programos identifikatorių, lauke **Aprašas** rodomas jo aprašas.
    - **Rikiavimas** – kiekvienas kelių verčių brūkšninis kodas apima programos identifikatorių, po kiekvieno iš kurių nurodyta vertė, seką. Taikoma GS1 strategija nustato, kuris programos identifikatorius susiejamas su kiekvienu duomenų bazės lauku. Tačiau, jei brūkšninis kodas tą patį programos identifikatorių naudoja daugiau nei vieną kartą, sistema naudoja tvarką, kuria programos identifikatoriai rodomi kode, kad susietų juos su laukais. Eilučių, kuriose programos identifikatorius sutampa su vienos ar kelių kitų eilučių identifikatoriumi, atveju naudokite šį lauką, kad nustatytumėte tvarką, kuria apdorojamos sutampančios eilutės. Eilutė, kurios rūšiavimo vertė mažiausia, bus apdorota pirmiausia.

> [!NOTE]
> Norėdami nustatyti laukų tvarką brūkšniniams kodams, kuriuose yra daugiau nei vienas identiškas programos identifikatorius, *privalote* naudoti lauką **Rūšiavimas**.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>GS1 strategijų priskyrimas mobiliojo įrenginio meniu elementams

Pagal numatytuosius parametrus visuose mobiliojo įrenginio meniu elementuose yra įvesties laukai, kuriuose darbuotojai gali nuskaityti vieną vertę pagal bendrąją GS1 sąranką. Jei norite, kad darbuotojai galėtų nuskaityti daugiau nei vieną mobiliojo įrenginio meniu elemento lauko vertę vienu nuskaitymu, turite priskirti GS1 strategiją, atlikdami šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Sukurkite arba atidarykite meniu elementą.
1. „FastTab“ skirtuke **Bendra** lauką **GS1 strategija** nustatykite kaip strategiją, taikomą meniu elementui.

## <a name="gs1-setup-example"></a>GS1 sąrankos pavyzdys

Šis pavyzdys taikomas sistemai, kurioje GS1 parinktys yra nustatytos taip, kaip nurodyta toliau.

- Puslapyje **Sandėlio valdymo parametrai** nustatomi tolesni visuotiniai parametrai.

    - **FNC1 simbolis:** *\]C1*
    - **Grupių skyriklis:** *\~*

- Puslapyje **GS1 programos identifikatoriai** šiam pavyzdžiui aktualūs tolesni programos identifikatoriai.

    | Programos identifikatorius | Aprašas | Fiksuotas ilgis | Ilgis | Tipas | Dešimtainis |
    |---|---|---|---|---|---|
    | 01 | GTIN | Pasirinkta | 14 | Skaitinis | Apmokėta |
    | 10 | Paketo numeris | Apmokėta | 20 | Raidinis ir skaitinis | Apmokėta |
    | 17 | Galiojimo data | Pasirinkta | 6 | Data | Apmokėta |
    | 30 | Gaunamas kiekis | Apmokėta | 8 | Skaitinis | Apmokėta |

- Puslapyje **Bendroji GS1 sąranka** šiam pavyzdžiui aktualūs tolesni bendrosios GS1 strategijos parametrai.

    | Laukas | Programos identifikatorius | Aprašas |
    |---|---|---|
    | ItemId | 01 | GTIN |

- Puslapyje **GS1 strategija** yra strategija, kurios laukas **Strategijos pavadinimas** nustatytas kaip *Pirkimo gavimas*. Šioje strategijoje yra toliau nurodytos eilutės.

    | Laukas | Programos identifikatorius | Aprašas | Rūšiavimas |
    |---|---|---|---|
    | „ExpDate” | 17 | Galiojimo data | 0 |
    | „InventBatchId” | 10 | Paketo numeris | 0 |
    | Kiekis | 30 | Gaunamas kiekis | 0 |

- Puslapyje **Mobiliojo įrenginio meniu elementai** yra meniu elementas, pavadintas *Pirkimo gavimas*. Jo laukas **GS1 strategija** nustatytas kaip *Pirkimo gavimas*.

Kai pirkimo užsakymo prekės pristatomos į sandėlį, darbuotojas atlieka šiuos veiksmus.

1. Mobiliajame įrenginyje pasirinkite meniu elementą **Pirkimo gavimas**.
1. Įveskite pirkimo užsakymo numerį.
1. Pasirinkite lauką **Prekė** ir nuskaitykite šį brūkšninius kodus: `]C10100000012345678~3030~10b1~17220215`.

Dėl parametrų, kurie nustatyti šiame pavyzdyje, sistema nuskaitytą brūkšninį kodą nuskaito taip, kaip nurodyta toliau.

| Lauko raktas | Programos ID | Reikšmė | Banknotas |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Kadangi darbuotojas nuskaitė į lauką **Prekė**, pirmoji brūkšninio kodo vertė susiejama su tuo lauku. Susiejimas paimamas iš bendrosios GS1 sąrankos. |
| Kiekis | 30 | 30 | Kadangi vienu nuskaitymu fiksuojamos kelios laukų vertės, šis susiejimas ir visi likę susiejimai paimami iš GS1 strategijos, priskirtos meniu elementui **Pirkimo gavimas**. Ši vertė yra gautas kiekis. |
| „InventBatchId” | 10 | b1 | Ši vertė yra paketo ID. |
| „ExpDate” | 17 | 220215 | Datos formatas yra mmMMDD. Todėl galiojimo data yra 2022 m. vasario 15 d. |

Tada užregistruojamas gavimas, o po vieno nuskaitymo įvedamos atitinkamos duomenų bazės vertės.
