---
title: Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Austrijai
description: Šiame straipsnyje pateikta Austrijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: f3429df2732d7d1ed6d2f0783a600c2b994c022b
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473883"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Austrijai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta Austrijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.

Siekiant patenkinti vietinius finansinius reikalavimus grynųjų pinigų registrams Austrijoje, Dynamics 365 Retail Austrijos funkcija apima pavyzdinį kasos aparato (EKA) integravimą su išorine finansinio registravimo tarnyba. Pavyzdys išplečia finansinio [integravimo funkciją](fiscal-integration-for-retail-channel.md). Jis remiasi [EFR (elektroninio finansinio registro)](https://www.efsta.eu/at/fiskalloesungen/oesterreich)[sprendimu iš EFSTA](https://www.efsta.eu/at/) ir įgalina ryšį su EFR tarnyba per HTTPS protokolą. EFR tarnyba turi būti laikoma "Retail Hardware" stotis arba atskirame kompiuteryje, kurį galima prijungti iš "Hardware" stoties. Pavyzdys pateikiamas šaltinio kodo forma ir yra "Commerce" programinės įrangos kūrimo rinkinio (SDK) dalis.

"Microsoft" neišleidžia jokios aparatūros, programinės įrangos ar dokumentacijos iš EFSTA. Norėdami gauti informacijos apie tai, kaip gauti EFR sprendimą ir jį valdyti, susisiekite su [EFSTA](https://www.efsta.eu/at/kontakt).

## <a name="scenarios"></a>Scenarijai

Šiuos scenarijus apima Austrijos finansinių registracijų tarnybos integravimo pavyzdys:

- Grynųjų pinigų operacijų registravimas finansinio registravimo tarnybose:

    - Siųsti išsamius operacijos duomenis į finansinio registravimo tarnybą. Šie duomenys apima pardavimo eilutės informaciją ir informaciją apie nuolaidas, mokėjimus ir mokesčius.
    - Perimti iždo registracijos tarnybos atsakymą. Šis atsakymas apima skaitmeninį parašą ir užregistruotos operacijos saitą.
    - Užregistruokite mokesčius ir susiekite juos su finansinio registravimo tarnybos mokesčių kodais.
    - Išspausdinkite kvite užregistruotos operacijos QR kodą.

- Dovanų kortelių operacijų ir kliento depozitų registravimas kaip ne grynųjų pinigų operacijos finansinio registravimo paslaugoje:

    - Išduoti arba įtraukti pinigus į dovanų kortelę.
    - Registruoti kliento sąskaitos depozitą.
    - Registruoti kliento užsakymo depozitą.

- Ne pardavimo operacijų ir įvykių registravimas kaip ne grynųjų pinigų operacijos finansinio registravimo paslaugoje:

    - Atidaryti pamainą ir uždaryti pamainą
    - Pradžios suma, ne pinigų išėmimas ir mokėjimo priemonės šalinimas
    - Kainos perrašymas
    - Mokesčio perrašymas
    - Išspausdinta kvito kopija
    - Atidaryti stalčių
    - Spausdinti X ataskaitą
    - Spausdinti Z ataskaitą

- Spausdinami dienos pabaigos išrašai (X/Z ataskaitos), kuriuose yra Austrijai specifiniai laukai:

    - Bendras produktų ar paslaugų, pristatytų klientams, skaičius
    - Pardavimo paskirstymas pagal mokesčių tarifą
    - Mokėjimų paskirstymas pagal kasininką / kasos aparato operatorių
    - Kainos nuolaidos ir grąžinimai, kurie sumažina kasdienį pardavimą
    - Nulinis pardavimas (give paslaugos)

- Klaidos tvarkymą, pvz., šias pasirinktis:

    - Pakartokite fiskalinę registraciją, jei galima kartoti, pvz., jei fiskalinių registracijų tarnyba negalima, neparuošta arba neatsako.
    - Atidėti finansinio registravimo datą.
    - Praleisti ataskaitinį registravimą arba pažymėti operaciją kaip užregistruotą ir įtraukti informacijos kodus, kad būtų fiksuojama trikties priežastis ir papildoma informacija.
    - Patikrinkite finansinio registravimo tarnybos pasiekiamumą prieš atidarę naują pardavimo operaciją arba kai pardavimo operacija baigiama.

### <a name="gift-cards"></a>Dovanų kortelės

Finansinio registravimo tarnybos integravimo pavyzdys vykdo šias taisykles, susijusias su dovanų kortelėmis:

- Pašalinti pardavimo eilutes, susijusias su dovanų kortelės *išdavimo ir įtraukti* į *dovanų kortelės operacijas* iš grynųjų pinigų operacijos. Užuot registruodami šias eilutes kaip grynųjų pinigų operacijos dalį, finansinio registravimo tarnybose užregistruokite jas kaip atskirą ne grynųjų pinigų operaciją.
- Nespausdinti mokesčių grupės paskirstymo ir QR kodo kvite, jei gavimą sudaro tik dovanų kortelės eilutės.
- Atskirai nuo kvito grynųjų pinigų operacijos sumos spausdinkite bendrą išduoti arba iš naujo išduoti dovanų kortelių sumą.
- Įrašykite apskaičiuotus mokėjimo eilučių koregavimus kanalo duomenų bazėje su nuoroda į atitinkamą fiskalinę operaciją.
- Mokėjimas dovanų kortele laikomas įprastu mokėjimu.

### <a name="customer-deposits-and-customer-order-deposits"></a>Kliento depozitai ir kliento užsakymo depozitai

Finansinio registravimo tarnybos integravimo pavyzdys vykdo šias taisykles, susijusias su kliento depozitais ir kliento užsakymo depozitais:

- Užregistruokite ne grynuosius pinigus, jei operacija yra kliento depozitas.
- Užregistruokite ne grynųjų pinigų operaciją, jei operacijoje yra tik kliento užsakymo depozitas arba kliento užsakymo depozito grąžinimas.
- Atskaityti kliento užsakymo depozito sumą iš mokėjimo eilučių, kai sukurtas kliento užsakymas.
- Įrašykite apskaičiuotus mokėjimo eilučių koregavimus kanalo duomenų bazėje su nuoroda į kliento užsakymo ataskaitinę operaciją.

### <a name="limitations-of-the-sample"></a>Pavyzdžio apribojimai

Finansinio registravimo tarnyba palaiko tik scenarijus, kuriuose PVM įtraukiamas į kainą. Todėl parduotuvių **ir klientų parinktis** Kaina su PVM turi **būti** nustatyta kaip Taip.

## <a name="set-up-commerce-for-austria"></a>Nustatyti Austrijos "Commerce"

Šiame skyriuje aprašomi Komercijos parametrai, kurie yra specifiniai Ir rekomenduojami Austrijai. Daugiau informacijos nustatymo informacijos ieškokite " [Commerce" pagrindinis puslapis](../index.md).

Norėdami naudoti Austrijai brastos funkcijos parametrus, turite nustatyti šiuos parametrus:

- Pirminiame juridinio subjekto adrese nustatykite šalies **/regiono lauką** **AUT** (Austrija).
- Kiekvienos Austrijos parduotuvės EKA **funkcijų šablone nustatykite ISO kodo lauką** **AT** (Austrija).

Taip pat turite nurodyti šiuos Austrijos parametrus. Atkreipkite dėmesį, kad užbaigę nustatymą turite vykdyti atitinkamas paskirstymo užduotis.

### <a name="enable-features-for-austria"></a>Įjungti Austrijos priemones

Funkcijų valdymo darbo srityje turite įgalinti **šias** funkcijas:

- (Austrija) Įjungti papildomus audito įvykius EKA
- (Austrija) Įjungti papildomą informaciją EKA dienos pabaigos ataskaitose

### <a name="set-up-vat-per-austrian-requirements"></a>Nustatyti AUSTRIJOS reikalavimų PVM

Turite sukurti PVM kodus, PVM grupes ir prekės PVM grupes. Taip pat turite nustatyti produktų ir paslaugų PVM informaciją. Daugiau informacijos apie tai, kaip nustatyti ir naudoti PVM priemones, ieškokite [PVM peržiūra.](../../finance/general-ledger/indirect-taxes-overview.md)

Pardavimo kvituose galite išspausdinti sutrumpintą PVM kodo kodą (pvz., "A" arba "B"). Kad ši funkcija būtų galima, nustatykite **PVM** kodų puslapio lauką **Spausdinti** kodą.

### <a name="set-up-stores"></a>Parduotuvių nustatykite

**Puslapyje Visos parduotuvės** atnaujinkite parduotuvės informaciją. Tiksliau nustatykite šiuos parametrus:

- Lauke PVM **grupė nurodykite** PVM grupę, kurią reikia naudoti pardavimams numatytojam klientui.
- Nustatykite **parinktį Kainos su PVM** kaip **Taip**.
- Nustatykite **įmonės** pavadinimą lauke Pavadinimas. Šis pakeitimas padeda užtikrinti, kad pardavimo kvite bus rodomas įmonės pavadinimas. Taip pat galite įtraukti įmonės pavadinimą į pardavimo kvito maketą kaip laisvos formos tekstą.
- Nustatyti mokesčio **identifikavimo numerio (TIN)** lauką kaip įmonės identifikavimo numerį. Šis pakeitimas padeda užtikrinti, kad pardavimo kvite bus rodomas įmonės identifikavimo numeris. Taip pat galite prie pardavimo kvito maketo pridėti įmonės identifikavimo numerį kaip laisvos formos tekstą.

### <a name="set-up-functionality-profiles"></a>Funkcijų šablonų nustatymas

Nustatykite EKA funkcijų šablonus:

- Kvitų **numeravimo** "FastTab" nustatykite kvitų **numeravimą**, sukurdami arba atnaujindami pardavimo, **pardavimo užsakymo** ir grąžinimo **kvitų** operacijų tipų įrašus.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruoti pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Galite konfigūruoti kalbos tekstą ir pasirinktinius laukus, kurie naudojami EKA kvitų formatuose. Numatytoji gavimo nustatymą sukūrusio vartotojo įmonė turėtų būti tas pats juridinis subjektas, kuriame sukurtas kalbos teksto nustatymas. Arba tas pats kalbos tekstas turėtų būti sukurtas ir vartotojo numatytoje įmonėje, ir parduotuvės juridiniame subjekte, kuriam sukurtas nustatymas.

Kalbos teksto **puslapyje** pridėkite šiuos kvitų maketų pasirinktinių laukų žymių įrašus. Atkreipkite dėmesį **, kad** lentelėje **pateiktos kalbos ID,** **teksto ID** ir teksto vertės yra tik pavyzdžiai. Juos galite pakeisti, kad jie atitiktų jūsų poreikius. Tačiau jūsų naudojamas **teksto ID** vertės turi būti unikalios ir turi būti lygios arba didesnės nei 900001.

Įtraukite šias EKA žymes į kalbos **teksto** EKA **skyrių** iš lentelės:

| Kalbos ID | Teksto ID | Tekstas                      |
|-------------|---------|---------------------------|
| lt       | 900001  | QR kodas                   |
| lt       | 900002  | Ištisinis numeris         |
| lt       | 900003  | Mažmeninės prekybos mokesčių spausdinimo kodas     |
| lt       | 900004  | Iš viso (pardavimas)             |
| lt       | 900005  | Bendra mokesčių suma (pardavimai)         |
| lt       | 900006  | Iš viso įtraukti mokesčius (pardavimai) |
| lt       | 900007  | Mokesčio suma (pardavimai)        |
| lt       | 900008  | Mokesčių pagrindas (pardavimas)         |

Pasirinktinių **laukų puslapyje** pridėkite šiuos įrašus prie kvitų maketų pasirinktinių laukų. Atkreipkite **dėmesį, kad antraštės teksto ID** reikšmės turi **atitikti teksto ID** vertes, kurias nurodėte kalbos **teksto** puslapyje:

| Vardas                 | Tipas    | Vaizdo aprašo teksto ID |
|----------------------|---------|-----------------|
| QRCODE               | Gavimas | 900001          |
| IŠTISINIS NUMERAVIMAS     | Gavimas | 900002          |
| "RETAILPRINTCODE"      | Gavimas | 900003          |
| PARDAVIMO SUMA           | Gavimas | 900004          |
| SALESTOTALTAX        | Gavimas | 900005          |
| SALESTOTALINCLUDETAX | Gavimas | 900006          |
| SALESTAMOUNT SUMA       | Gavimas | 900007          |
| PARDAVIMOTAXBASIS        | Gavimas | 900008          |

> [!NOTE]
> Svarbu nurodyti teisingus pasirinktinių laukų pavadinimus, kurie išvardyti ankstesnėje lentelėje. Neteisingas pasirinktinio lauko pavadinimas gali sukelti kvitų duomenų.

### <a name="configure-receipt-formats"></a>Kvitų formatų konfigūravimas

Kiekvieno reikiamo kvito formato atveju pakeiskite lauko Spausdinti veikimo būdą **vertę** į **Visada spausdinti**.

Kvitų formato dizaineryje į atitinkamus kvitų skyrius įtraukite šiuos pasirinktinius laukus. Nepamirškite, kad laukų pavadinimai atitinka ankstesniame skyriuje jūsų apibrėžtus kalbos tekstus.

- **Antraštė:** Įtraukite šiuos laukus:

    - **Parduotuvės pavadinimo** ir **mokesčio ID** laukai, naudojami įmonės pavadinimui ir tapatybės numeriui kvituose spausdinti. Taip pat galite įtraukti įmonės pavadinimą ir tapatybės numerį į maketą kaip laisvos formos tekstą.
    - **Parduotuvės adresas**, **data**, **laikas 24 val**., **kvito numeris** ir registro **numerio** laukai.
    - **Ištisinio** numerio laukai, kuriuose nurodomas grynųjų pinigų operacijos numeris finansinio registravimo tarnybose.

- **Eilutės:** įtraukite šiuos laukus:

    - **Prekės pavadinimas**.
    - **Kiekis**
    - **Bendra kaina su mokesčiu**.
    - **Mažmeninės prekybos mokesčių** spausdinimo kodas, naudojamas sutrumpintam kodui, kuris atitinka prekei taikymą PVM kodą, išspausdinti.

- **Poraštė:** įtraukite šiuos laukus:

    - Mokėjimo laukus, kad būtų išspausdintos kiekvieno mokėjimo būdo mokėjimo sumos. Pavyzdžiui, į vieną maketo **eilutę įtraukite** **laukus** Mokėjimo priemonės pavadinimas ir Mokėjimo priemonės suma.
    - **Bendrosios pardavimo sumos** laukų grupė:

        - **Laukas Bendroji suma** (pardavimas), naudojamas spausdinant visą kvito pardavimo grynaisiais sumą. Į sumą neįtraukti mokesčiai. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Laukas Bendra įskaitant mokestį** (pardavimas), naudojamas spausdinant bendrą kvito pardavimo grynaisiais sumą. Į sumą įtrauktas mokestis. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Laukas Bendra mokesčių (pardavimo)** suma, naudojamas spausdinant pardavimo grynaisiais pinigais mokesčių sumą. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.

    - **Mokesčių išs pertraukos** laukų grupė. Visi šios laukų grupės laukai turi būti išspausdinti vienoje atskiroje eilutėje.

        - **Mokesčio ID** laukas, kuris yra standartinis laukas, leidžiantis spausdinti kiekvieno PVM kodo PVM suvestinę. Laukas turi būti pridėtas prie naujos eilutės.
        - **Mokesčio procento** laukas, kuris yra standartinis laukas, naudojamas PVM kodo galiojamam mokesčio tarifui spausdinti.
        - **Mokesčių pagrindo (pardavimo)** laukas, naudojamas spausdinant pvm kodo kvito bendrą grynųjų pinigų pardavimo sumą. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Mokesčio sumos (pardavimo)** laukas, naudojamas spausdinant PVM kodo grynųjų pardavimo kvitų mokesčių sumą.
        - **Mažmeninės prekybos mokesčių** spausdinimo kodo laukas, naudojamas sutrumpintam kodui, atitinkančiam PVM kodą, spausdinti.

    - **QR kodo** laukas, naudojamas nuorodai į užregistruotas grynųjų pinigų operacijas spausdinti QR kodo formoje.

        > [!NOTE]
        > QR **kodo vertė** nuskaitoma iš finansinio registro atsakymo. EFR savo atsakyme grąžina QR **kodą** tik tada, jei EFR konfigūracijos atributų lauko vertė yra aprašyta EFSTA dokumentuose. QR kodo formatas atributų **lauke**, EFR konfigūracijoje, turi būti nustatytas kaip **BMP**.

Daugiau informacijos apie tai, kaip dirbti su kvitų formatais, ieškokite [Gavimo kvitų formatų nustatymas ir kūrimas](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Nustatyti Austrijos finansų integravimą

Austrijos finansinio registravimo tarnybos integravimo pavyzdys pagrįstas finansinio [integravimo funkcija](fiscal-integration-for-retail-channel.md) ir yra "Commerce SDK" dalis. Pavyzdys yra sprendimų saugyklos **src\\ FiscalIntegration\\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke. Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas, kuris yra "Commerce Runtime (CRT) plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie "Commerce SDK" naudojimą, [žr. "Download Commerce SDK" pavyzdžius ir nuorodų paketus iš GitHub NuGet](../dev-itpro/retail-sdk/sdk-github.md)[ir nustatykite nepriklausomos pakuotės SDK pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Austrijos finansinio registravimo tarnybos integravimo pavyzdį galima rasti "Commerce SDK", kuris naudojamas "Commerce" versijoje 10.0.29. Naudojant "Commerce" 10.0.28 arba senesnę versiją, reikia naudoti ankstesnę "Retail SDK" versiją programavimo virtualiojoje kompiuteryje (VM) Microsoft Dynamics ciklo tarnybose (LCS). Daugiau informacijos ieškokite Austrijos [(senesnės programos) finansinio integravimo pavyzdžio diegimo rekomendacijose](emea-aut-fi-sample-sdk.md).

Atlikite finansinio integravimo nustatymo veiksmus, kaip aprašyta ["Commerce" kanalų finansinio integravimo nustatymas](setting-up-fiscal-integration-for-retail-channel.md):

1. [Nustatykite finansinio registravimo procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Be to, pateikite pastabą apie finansinio registravimo proceso parametrus, bvz [., šios finansinio registravimo tarnybos integravimo pavyzdį](#set-up-the-registration-process).
1. [Nustatyti klaidų tvarkymo parametrus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Įgalinkite neautomatinį atidėtos finansinio registravimo vykdymą](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Sukonfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nustatyti registravimo procesą

Norėdami įjungti registravimo procesą, atlikite šiuos veiksmus norėdami nustatyti "Commerce Headquarters". Daugiau informacijos rasite "Commerce [" kanalų finansinio integravimo nustatykite](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųsti finansinio dokumento teikėjo ir fiskalinio jungties konfigūracijos failus:

    1. Atidaryti sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją.
    1. Atidaryti **src \> FiscalIntegration \> Efr**.
    1. Atidarykite **konfigūracijos \> DocumentProviders** ir atsisiųskite finansinio dokumento teikėjo konfigūracijos failus: 

        - DocumentProviderFiscalEFRSampleAustria.xml
        - DocumentProviderNonFiscalEFRSampleAustria.xml

    1. Atsisiųskite finansinio jungties konfigūracijos failą konfigūracijos **jungčių \>\> connectorEFRSample.xml.**

    > [!NOTE]
    > Naudojant "Commerce" 10.0.28 arba ankstesnę versiją, LCS programuotojo VM turite naudoti ankstesnę "Retail SDK" versiją. Šio fiskalinio integravimo pavyzdžio konfigūracijos failai yra toliau esančiuuose "Retail" SDK, esantis LCS programuotojo VM, aplankuose:
    >
    > - **Iždo dokumentų teikėjo konfigūracijos failai:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ extensions.DocumentProvider.EFRSample\\ konfigūracija
    > - **Iždo jungties konfigūracijos failas: RetailSdk** SampleExtensions\\ HardwareStation extension.EFRSample\\\\ konfigūracija\\

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**. Skirtuke **Bendra** nustatykite pasirinktį **Įgalinti finansų integravimą** kaip **Taip**.
1. Eikite į **"Retail" ir "Commerce \> Channel" \> nustatymą "Fiscal integration \> Fiscal"** dokumentų teikėjai ir įkelkite anksčiau atsisiųstus fiskalinių dokumentų teikėjo konfigūracijos failus.
1. Eikite į **"Retail" ir "Commerce Channel" \> nustatymą "Fiscal integration \> Fiscal \>" jungtis ir įkelkite anksčiau atsisiųstą "Fiscal** Connector" konfigūracijos failą.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" funkcinius profilius**. Sukurkite du naujus jungties funkcinius šablonus: po vieną kiekvienam anksčiau įkeltam finansinio dokumento tiekėjui ir pasirinkite anksčiau įkeltą fiskalinę jungtį. Pagal reikia [atnaujinti duomenų susiejimo](#default-data-mapping) parametrus.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" techninius profilius**. Sukurkite naują jungties techninio profilio ir pasirinkite anksčiau įkeltą fiskalinę jungtį. Pagal reikiamą [parametrų versiją atnaujinkite](#fiscal-connector-settings) jungties parametrus.
1. Eikite į " **Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Fiscal" jungties grupes**. Sukurkite dvi naujas finansinių jungčių grupes – po vieną kiekvienam anksčiau sukurtam jungties funkciniam profiliui.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Fiscal" registracijos procesus**. Sukurkite naują finansinio registravimo procesą ir du finansinio registravimo proceso veiksmus bei pasirinkite anksčiau sukurtas finansinių jungčių grupes.
1. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų šabloną, susietą su parduotuve, kurioje turi būti suaktyvintas registracijos procesas. Finansinio registravimo **proceso "** FastTab" pasirinkite anksčiau sukurtą finansinio registravimo procesą. Norėdami įjungti nefinansinių įvykių registravimą EKA, **EKA funkcijų "FastTab**" dalyje EKA **nustatykite** **parinktį Auditas kaip** Taip **.**
1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**. Pasirinkite aparatūros šabloną, susietą su aparatūros stotyje, prie kurios bus prijungta iždo registracijos tarnyba. **"FastTab" Iždo išoriniuose** įrenginiuose pasirinkite senesnę jungtį sukūrusį techninio profilio jungtį.
1. Atidarykite paskirstymo grafiką (**"Retail and Commerce Retail ir Commerce \> IT \> Distribution"** grafiką) **ir pasirinkite užduotis 1070** **ir 1090**, kad duomenys būtų perkelti į kanalo duomenų bazę.

#### <a name="default-data-mapping"></a>Numatytųjų duomenų susiejimas

Toliau pateiktas numatytasis duomenų susiejimas yra įtrauktas į finansinio dokumento teikėjo konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdžio dalis:

- **Pridėtinės vertės mokesčio (PVM) tarifų konvertavimas –** mokesčio procentų verčių, kurios nustatytos PVM kodams, susiejimas su atributo TaxG **(mokesčių grupė)** vertėmis užklausose, kurios siunčiamos į fiskalinę tarnybą. Čia yra numatytasis susiejimas:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Pirmasis kiekvienos poros komponentas rodo PVM mokesčių grupę, kurią palaiko EFR finansinio registravimo tarnyba. Antrasis komponentas rodo atitinkamą PVM tarifą. Daugiau informacijos apie PVM mokesčių grupes, kurias EFR palaiko Austrijai, ieškokite [EFR nuorodoje](https://public.efsta.net/efr/).

#### <a name="fiscal-connector-settings"></a>Iždo jungties parametrai

Šie parametrai įtraukiami į fiskalinės jungties konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdys:

- **Galinio punkto** adresas – finansinio registravimo tarnybos URL.
- **Įrenginio skirtasis** laikas milisekunde, per kurį fiskalinė jungtis lauks atsakymo iš fiskalinių registracijų tarnybos.
- **Rodyti finansinio registravimo pranešimus** – ši vėliavėlė valdo, ar finansinių registracijų tarnybos grąžinimai turėtų būti rodomi operatoriui.

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

> [!NOTE]
> - Austrijos finansinio registravimo tarnybos integravimo pavyzdį galima rasti "Commerce SDK", kuris naudojamas "Commerce" versijoje 10.0.29. Naudojant "Commerce" 10.0.28 arba ankstesnę versiją, LCS programuotojo VM turite naudoti ankstesnę "Retail SDK" versiją. Daugiau informacijos ieškokite Austrijos [(senesnės programos) finansinio integravimo pavyzdžio diegimo rekomendacijose](emea-aut-fi-sample-sdk.md).
> - Jūsų aplinkoje įdiegti "Commerce" pavyzdžiai nėra automatiškai atnaujinami, kai taikote "Commerce" komponentų aptarnavimo arba kokybės naujinimus. Reikiamus pavyzdžius turite atnaujinti neautomatiniu būdu.

#### <a name="set-up-the-development-environment"></a>Programavimo aplinkos kūrimas

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba atsisiųskite [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr. ["Download Commerce SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite EFR sprendimą Dynamics365Commerce.Solutions **FiscalIntegration\\ EFR.sln\\ ir sukurkite\\ jį.**
1. Įdiegti CRT plėtinius:

    1. Rasti plėtinio CRT diegimo programą:

        - **"Commerce Scale Unit":** **aplanke Efr\\ ScaleUnit\\ ScaleUnit.EFR.Installer\\\\ talpyklos debug\\ net461** **raskite ScaleUnit.EFR.Installer diegimo** priemonės.
        - **Vietinė CRT "Modern POS":** **aplanke Efr\\ ModernPOS ModernPOS.EFR.Installer\\\\\\ talpyklos debug\\ net461** **raskite ModernPOS.EFR.Installer diegimo** kūrėjas.

    1. Paleiskite CRT plėtinio diegimo programą iš komandų eilutės:

        - **"Commerce Scale Unit":**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **" CRT Modern POS" vieta:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Įdiekite "Fiscal Connector" plėtinius:

    "Hardware" arba EKA kasos [aparate galite](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) įdiegti " [Fiscal Connector" plėtinius](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

    1. Įdiekite aparatūros stoties plėtinius:

        1. **Aplanke Efr\\ HardwareStation\\ HardwareStation.EFR.Installer\\ talpyklos\\ debug\\ net461** **raskite HardwareStation.EFR.Installer diegimo** priemonės.
        1. Paleiskite plėtinio diegimo programą iš komandų eilutės vykdydami šią komandą.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Įdiekite EKA plėtinius:

        1. Atidarykite EKA **iždo jungties pavyzdžio sprendimą Dynamics365Commerce.Solutions\\ FiscalIntegration\\ PosFiscalConnectorSample\\ Contoso.PosFiscalConnectorSample.sln** ir sukurkite jį.
        1. **Aplanke PosFiscalConnectorSample\\ StoreCommerce.Installer\\ bin\\ Debug\\ net461** **raskite Contoso.PosFiscalConnectorSample.StoreCommerce.Installer diegimo** priemonės.
        1. Paleiskite plėtinio diegimo programą iš komandų eilutės, vykdomos šios komandos.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Gamybos aplinka

Norėdami sugeneruoti [ir](fiscal-integration-sample-build-pipeline.md) paleisti debesies skalės vienetą ir savitarnos diegiant finansinio integravimo pavyzdžio paketus, atlikite nurodytus veiksmus. **EFR build-pipeline.yml** šablono JAML **\\ failą galima rasti YAML_Files** saugyklos aplanke [Dynamics 365 Commerce Pardavimo](https://github.com/microsoft/Dynamics365Commerce.Solutions) galimybės.

## <a name="design-of-extensions"></a>Plėtinių dizainas

Austrijos finansinio registravimo tarnybos integravimo pavyzdys pagrįstas finansinio [integravimo funkcija](fiscal-integration-for-retail-channel.md) ir yra "Commerce SDK" dalis. Pavyzdys yra sprendimų saugyklos **src\\ FiscalIntegration\\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke. Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas CRT, kuris yra plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie "Commerce SDK" naudojimą, [žr. "Download Commerce SDK" pavyzdžius ir nuorodų paketus iš GitHub NuGet](../dev-itpro/retail-sdk/retail-sdk-overview.md)[ir nustatykite nepriklausomos pakuotės SDK pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Austrijos finansinio registravimo tarnybos integravimo pavyzdį galima rasti "Commerce SDK", kuris naudojamas "Commerce" versijoje 10.0.29. Naudojant "Commerce" 10.0.28 arba ankstesnę versiją, LCS programuotojo VM turite naudoti ankstesnę "Retail SDK" versiją. Daugiau informacijos ieškokite Austrijos [(senesnės programos) finansinio integravimo pavyzdžio diegimo rekomendacijose](emea-aut-fi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas 

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti paslaugai bvz., dokumentus ir tvarkyti atsakymus iš fiskalinių registracijų tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

Dokumentų teikėjai gali naudoti dvi užklausų apdorojimo programas:

- **DocumentProviderEFRFiscalAUT** – ši apdorojimo programa naudojama finansinių registracijų tarnybos iždo dokumentams generuoti.
- **DocumentProviderEFRNonFiscalAUT** – ši apdorojimo programa naudojama nefinansiniai dokumentams, skirti finansinio registravimo tarnybai, generuoti.

Šios apdorojimo programos perimamos iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su jungties dokumento teikėjo pavadinimu, kuris nurodytas "Commerce Headquarters".

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje yra informacijos apie tai, koks dokumentas turėtų būti sugeneruotas. Grąžinamas paslaugai konkretus dokumentas, kuris turi būti užregistruotas finansinio registravimo tarnybose.
- **GetNonFiscalDocumentDocumentProviderRequest** – šioje užklausoje yra informacijos apie tai, kas turėtų būti generuojamas nefinansinis dokumentas. Grąžinamas paslaugai konkretus dokumentas, kuris turi būti užregistruotas finansinio registravimo tarnybose.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa pateikia įvykių, prie kurių bus užsiprenumeruoti, sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas, Z ataskaitos spausdinimas, kliento sąskaitos depozitai, klientų užsakymų depozitai, audito įvykiai ir ne pardavimo operacijos.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – ši užklausa grąžina atsakymą iš finansinių registracijų tarnybos. Šis atsakymas yra eilutėmis išrašomas į formą, kad būtų galima įrašyti.

#### <a name="configuration"></a>Konfigūracija

Finansinio dokumento teikėjo konfigūracijos **failai yra sprendimų saugyklos src\\ FiscalIntegration\\ Efr\\ konfigūracijų\\ DocumentProviders**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke:

- **DocumentProviderFiscalEFRSampleAustria** – iždo dokumentų teikėjo konfigūracijos failas.
- **DocumentProviderNonFiscalEFRSampleAustria** – nefinansinių dokumentų teikėjo konfigūracijos failas.

Šių failų paskirtis – įgalinti finansinio dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Fiskalinio jungties plėtinio paskirtis yra palaikyti ryšį su finansinių dokumentų registravimo tarnyba. Aparatūros stoties plėtinys naudoja HTTP ir HTTPS protokolus dokumentams, kuriuos plėtinys CRT sugeneruoja iždo registracijos tarnybai, pateikti. Jis taip pat tvarko atsakymus, gautus iš finansinio registravimo tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

**EFRHandler užklausos** apdorojimo programa yra iždo registracijos tarnybos užklausų tvarkymo įvesties taškas.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su "Commerce Headquarters" nurodytu finansinio jungties pavadinimu.

"Fiscal Connector" palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus į finansinio registravimo tarnybą ir grąžina atsakymą iš jos.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama norint patikrinti finansinių registracijų tarnybos sveikumą.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama norint inicijuoti finansinių registracijų tarnybą.

#### <a name="configuration"></a>Konfigūracija

Finansinio jungties konfigūracijos **failas yra src\\ FiscalIntegration\\ Efr\\ konfigūracijų\\ jungčių\\ ConnectorEFRSample.xml**[Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo paskirtis – įgalinti finansinių jungčių parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais.

### <a name="pos-fiscal-connector-extension-design"></a>EKA "Fiscal Connector" plėtinio dizainas

EKA finansinio jungties plėtinio paskirtis yra susisiekti su finansinio registravimo tarnyba iš EKA. Ryšio tikslais naudojamas HTTPS protokolas.

#### <a name="fiscal-connector-factory"></a>Finansinių jungčių gamykla

Iždo jungties gamyklos jungties pavadinimas susietas su "Fiscal Connector **" diegimas ir yra faile Pos.Extension\\ Connectors\\ FiscalConnectorFactory.ts**. Jungties pavadinimas turi atitikti "Commerce Headquarters" nurodytą finansinio jungties pavadinimą.

#### <a name="efr-fiscal-connector"></a>EFR iždo jungtis

EFR fiskalinė jungtis yra **Pos.Extension\\ Connectors\\ Efr\\ EfrFiscalConnector.ts faile**. Jis įdiegia **IFiscalConnector sąsają**, palaikančią šias užklausas:

- **FiscalRegisterSubmitDocumentClientRequest** – ši užklausa siunčia dokumentus finansinio registravimo tarnybai ir grąžina atsakymą iš jos.
- **FiscalRegisterIsReadyClientRequest** – ši užklausa naudojama norint patikrinti iždo dokumentų registracijos tarnybos sveikumą.
- **FiscalRegisterInitializeClientRequest** – ši užklausa naudojama norint inicijuoti finansinio registravimo tarnybą.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra sprendimų saugyklos **src\\ FiscalIntegration\\ Efr\\ konfigūracijų \\**[Dynamics 365 Commerce jungčių](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke. Failo paskirtis – įgalinti finansinio jungties parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais. Pridedami šie parametrai:

- **Galinio punkto** adresas – finansinio registravimo tarnybos URL.
- **Skirtasis** laikas milisekundiais, kurį jungtis lauks atsakymo iš fiskalinių registracijų tarnybos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
