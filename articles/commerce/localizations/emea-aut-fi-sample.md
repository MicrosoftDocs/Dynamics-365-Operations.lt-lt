---
title: Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Austrijai
description: Šioje temoje pateikta Austrijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: f03eab49f0abfc8a279ea43f69fa2ac0100bd34a
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7945044"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Austrijai

[!include[banner](../includes/banner.md)]

Šioje temoje pateikta Austrijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.

Siekiant patenkinti vietinius finansinius reikalavimus grynųjų pinigų registrams Austrijoje, Austrijos funkcija apima pavyzdinį kasos aparato Dynamics 365 Retail (EKA) integravimą su išorine finansinio registravimo tarnyba. Pavyzdys išplečia finansinio [integravimo funkciją](fiscal-integration-for-retail-channel.md). Jis remiasi [EFR (elektroninio finansinio registro)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) sprendimu iš [EFSTA](https://www.efsta.eu/at/) ir įgalina ryšį su EFR tarnyba per HTTPS protokolą. EFR tarnyba turi būti laikoma "Retail Hardware" stotis arba atskirame kompiuteryje, kurį galima prijungti iš "Hardware" stoties. Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

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

- Pašalinti pardavimo eilutes, susijusias su dovanų kortelės *išdavimo ir įtraukti į* dovanų *kortelės* operacijas iš grynųjų pinigų operacijos. Užuot registruodami šias eilutes kaip grynųjų pinigų operacijos dalį, finansinio registravimo tarnybose užregistruokite jas kaip atskirą ne grynųjų pinigų operaciją.
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

Finansinio registravimo tarnyba palaiko tik scenarijus, kuriuose PVM įtraukiamas į kainą. Todėl parduotuvių ir klientų parinktis Kaina su PVM turi būti **nustatyta** kaip **Taip**.

## <a name="set-up-commerce-for-austria"></a>Nustatyti Austrijos "Commerce"

Šiame skyriuje aprašomi Komercijos parametrai, kurie yra specifiniai Ir rekomenduojami Austrijai. Norėdami gauti daugiau informacijos, žr.["Commerce" pagrindinį](../index.md) puslapį.

Norėdami naudoti Austrijai brastos funkcijos parametrus, turite nustatyti šiuos parametrus:

- Pirminiame juridinio subjekto adrese nustatykite **šalies/regiono** lauką **AUT** (Austrija).
- Kiekvienos Austrijos parduotuvės EKA funkcijų šablone nustatykite **ISO kodo** lauką **AT** (Austrija).

Taip pat turite nurodyti šiuos Austrijos parametrus. Atkreipkite dėmesį, kad užbaigę nustatymą turite vykdyti atitinkamas paskirstymo užduotis.

### <a name="set-up-vat-per-austrian-requirements"></a>Nustatyti AUSTRIJOS reikalavimų PVM

Turite sukurti PVM kodus, PVM grupes ir prekės PVM grupes. Taip pat turite nustatyti produktų ir paslaugų PVM informaciją. Daugiau informacijos apie tai, kaip nustatyti ir naudoti PVM priemones, ieškokite [PVM](../../finance/general-ledger/indirect-taxes-overview.md) peržiūra.

Pardavimo kvituose galite išspausdinti sutrumpintą PVM kodo kodą (pvz., "A" arba "B"). Kad ši funkcija būtų galima, nustatykite **PVM** kodų **puslapio lauką Spausdinti** kodą.

### <a name="set-up-stores"></a>Parduotuvių nustatykite

Puslapyje **Visos** parduotuvės atnaujinkite parduotuvės informaciją. Tiksliau nustatykite šiuos parametrus:

- Lauke **PVM grupė** nurodykite PVM grupę, kurią reikia naudoti pardavimams numatytojam klientui.
- Nustatykite **parinktį Kainos su PVM kaip** **Taip**.
- Nustatykite **įmonės** pavadinimą lauke Pavadinimas. Šis pakeitimas padeda užtikrinti, kad pardavimo kvite bus rodomas įmonės pavadinimas. Taip pat galite įtraukti įmonės pavadinimą į pardavimo kvito maketą kaip laisvos formos tekstą.
- Nustatyti mokesčio **identifikavimo numerio (TIN)** lauką kaip įmonės identifikavimo numerį. Šis pakeitimas padeda užtikrinti, kad pardavimo kvite bus rodomas įmonės identifikavimo numeris. Taip pat galite prie pardavimo kvito maketo pridėti įmonės identifikavimo numerį kaip laisvos formos tekstą.

### <a name="set-up-functionality-profiles"></a>Funkcijų šablonų kūrimas

Nustatykite EKA funkcijų šablonus:

- Kvitų **numeravimo "FastTab" nustatykite kvitų numeravimą, sukurdami arba atnaujindami pardavimo, pardavimo užsakymo ir** **grąžinimo** **·** **kvitų** operacijų tipų įrašus.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruoti pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Galite konfigūruoti kalbos tekstą ir pasirinktinius laukus, kurie naudojami EKA kvitų formatuose. Numatytoji gavimo nustatymą sukūrusio vartotojo įmonė turėtų būti tas pats juridinis subjektas, kuriame sukurtas kalbos teksto nustatymas. Arba tas pats kalbos tekstas turėtų būti sukurtas ir vartotojo numatytoje įmonėje, ir parduotuvės juridiniame subjekte, kuriam sukurtas nustatymas.

Kalbos **teksto puslapyje** pridėkite šiuos kvitų maketų pasirinktinių laukų žymių įrašus. Atsikreipkite **dėmesį, kad lentelėje pateiktos kalbos ID, teksto ID ir teksto vertės** **yra tik** **pavyzdžiai**. Galite keisti juos, kad jie atitiktų jūsų poreikius. Tačiau jūsų naudojamas teksto ID vertės turi būti unikalios ir jos turi būti lygios arba **didesnės** 900001.

Įtraukite šias EKA žymes į **kalbos** teksto EKA skyrių iš **lentelės**:

| Kalbos ID | Teksto ID | Tekstas                      |
|-------------|---------|---------------------------|
| en-JAV       | 900001  | QR kodas                   |
| en-JAV       | 900002  | Ištisinis numeris         |
| en-JAV       | 900003  | Mažmeninės prekybos mokesčių spausdinimo kodas     |
| en-JAV       | 900004  | Iš viso (pardavimas)             |
| en-JAV       | 900005  | Bendra mokesčių suma (pardavimai)         |
| en-JAV       | 900006  | Iš viso įtraukti mokesčius (pardavimai) |
| en-JAV       | 900007  | Mokesčio suma (pardavimai)        |
| en-JAV       | 900008  | Mokesčių pagrindas (pardavimas)         |

Pasirinktinių **laukų** puslapyje pridėkite šiuos įrašus prie kvitų maketų pasirinktinių laukų. Atkreipkite **dėmesį, kad** antraštės teksto ID reikšmės turi atitikti teksto ID **vertes**, kurias nurodėte kalbos **teksto** puslapyje:

| Pavadinimas                 | Tipas    | Vaizdo aprašo teksto ID |
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

Pakeiskite kiekvieno reikiamo kvito formato lauko Spausdinti veikimo būdą **reikšmę** į **Visada** spausdinti.

Kvitų formato dizaineryje į atitinkamus kvitų skyrius įtraukite šiuos pasirinktinius laukus. Nepamirškite, kad laukų pavadinimai atitinka ankstesniame skyriuje jūsų apibrėžtus kalbos tekstus.

- **Antraštė:** Įtraukite šiuos laukus:

    - **Parduotuvės pavadinimo** **ir mokesčio ID** laukai, naudojami įmonės pavadinimui ir tapatybės numeriui kvituose spausdinti. Taip pat galite įtraukti įmonės pavadinimą ir tapatybės numerį į maketą kaip laisvos formos tekstą.
    - **Parduotuvės** adresas, **data**, **laikas 24** val., **kvito** numeris ir registro **numerio** laukai.
    - **Ištisinio** numerio laukai, kuriuose nurodomas grynųjų pinigų operacijos numeris finansinio registravimo tarnybose.

- **Eilutės:** įtraukite šiuos laukus:

    - **Prekės** pavadinimas.
    - **Kiekis**
    - **Bendra kaina su** mokesčiu.
    - **Mažmeninės prekybos mokesčių spausdinimo kodas, naudojamas sutrumpintam kodui, kuris atitinka prekei** taikymą PVM kodą, išspausdinti.

- **Poraštė:** įtraukite šiuos laukus:

    - Mokėjimo laukus, kad būtų išspausdintos kiekvieno mokėjimo būdo mokėjimo sumos. Pavyzdžiui, į vieną maketo eilutę įtraukite **laukus Mokėjimo priemonės pavadinimas** ir Mokėjimo priemonės **suma**.
    - **Bendrosios pardavimo** sumos laukų grupė:

        - **Laukas Bendroji suma** (pardavimas), naudojamas spausdinant visą kvito pardavimo grynaisiais sumą. Į sumą neįtraukti mokesčiai. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Laukas Bendra įskaitant mokestį** (pardavimas), naudojamas spausdinant bendrą kvito pardavimo grynaisiais sumą. Į sumą įtrauktas mokestis. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Laukas Bendra mokesčių** (pardavimo) suma, naudojamas spausdinant pardavimo grynaisiais pinigais mokesčių sumą. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.

    - **Mokesčių išs pertraukos** laukų grupė. Visi šios laukų grupės laukai turi būti išspausdinti vienoje atskiroje eilutėje.

        - **Mokesčio ID** laukas, kuris yra standartinis laukas, leidžiantis spausdinti kiekvieno PVM kodo PVM suvestinę. Laukas turi būti pridėtas prie naujos eilutės.
        - **Mokesčio** procento laukas, kuris yra standartinis laukas, naudojamas PVM kodo galiojamam mokesčio tarifui spausdinti.
        - **Mokesčių pagrindo (pardavimo) laukas, naudojamas spausdinant pvm kodo kvito bendrą** grynųjų pinigų pardavimo sumą. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Mokesčio sumos (pardavimo) laukas, naudojamas spausdinant PVM kodo grynųjų pardavimo** kvitų mokesčių sumą.
        - **Mažmeninės prekybos mokesčių** spausdinimo kodo laukas, naudojamas sutrumpintam kodui, atitinkančiam PVM kodą, spausdinti.

    - **QR kodo** laukas, naudojamas nuorodai į užregistruotas grynųjų pinigų operacijas spausdinti QR kodo formoje.

        > [!NOTE]
        > **QR kodo vertė** nuskaitoma iš finansinio registro atsakymo. EFR savo atsakyme grąžina QR kodą tik tada, jei EFR konfigūracijos atributų lauko vertė yra aprašyta **EFSTA** dokumentuose. QR kodo formatas **atributų** lauke, EFR konfigūracijoje, turi būti nustatytas kaip **BMP**.

Daugiau informacijos apie tai, kaip dirbti su gavimo formatais, ieškokite [Set up and design receipt formatus](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Nustatyti Austrijos finansų integravimą

Austrijos finansinio registravimo tarnybos integravimo pavyzdys remiasi finansinio [integravimo funkcija ir yra Mažmeninės prekybos SDK](fiscal-integration-for-retail-channel.md) dalis. Pavyzdys yra **sprendimų saugyklos src \\ FiscalIntegration \\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke (pvz., [išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskalinio dokumento teikėjas, kuris yra "Commerce" vykdymo laiko pratęsimas (CRT), ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Daugiau informacijos apie tai, kaip naudoti "Retail SDK", žr. "Retail SDK" architektūrą ir nepriklausomos pakavimo [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) [sukūrimo pardavimo galimybių](../dev-itpro/build-pipeline.md) sukūrimą.

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Ankstesnę mažmeninės prekybos SDK versiją turite naudoti kūrėjo virtualioje mašinoje (VM) Microsoft Dynamics "Lifecycle Services" (LCS). Daugiau informacijos ieškokite Austrijos [(senesnės programos) finansinio integravimo pavyzdžio diegimo](emea-aut-fi-sample-sdk.md) rekomendacijose. Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

Atlikite fiskalinės integracijos nustatymo veiksmus, aprašytus [Komercijos kanalų finansinio integravimo nustatymas](setting-up-fiscal-integration-for-retail-channel.md):

1. [Nustatyti fiskalinės registracijos procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Be to, atkreipkite dėmesį į fiskalinės registracijos proceso parametrus, [būdingus šiam fiskalinės registracijos tarnybos integravimo ėminiui](#set-up-the-registration-process).
1. [Nustatykite klaidų tvarkymo parametrus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Įgalinti neautomatinį atidėtų fiskalinės registracijos vykdymą](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Sukonfigūruokite kanalo](#configure-channel-components) komponentus.

### <a name="set-up-the-registration-process"></a>Nustatyti registracijos procesą

Norėdami įgalinti registracijos procesą, atlikite šiuos veiksmus, kad nustatytumėte "Commerce" būstinę. Daugiau informacijos ieškokite [Set up fiscal integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųskite finansinio dokumento teikėjo ir finansinio jungties konfigūracijos failus:

    1. Atidaryti [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Pasirinkite teisingą išleidimo šakos versiją pagal savo SDK / programos versiją **[(pvz., leidimas / 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atidaryti **src \> FiscalIntegration \> Efr**.
    1. Atidarykite konfigūracijas DocumentProviders ir atsisiųskite finansinio dokumento teikėjo konfigūracijos **\>** failus: **DocumentProviderFiscalEampleAustria.xml ir** **DocumentProviderNonFiscalEFRSampleAustria.xml** (pvz., paleidimo [/ 9.33 failų](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders) vieta).
    1. Atsisiųskite fiskalinės jungties konfigūracijos failą **\> "Configurations \> Connectors ConnectorEFRSample.xml** (pvz., [išleidimo failą/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Šio finansinio integravimo pavyzdžio konfigūracijos failai yra šiuose LCS kūrėjo VM mažmeninės prekybos SDK aplankuose:
    >
    > - **Iždo dokumentų teikėjo konfigūracijos failai:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ extensions.DocumentProvider.EFRSample \\ konfigūracija
    > - **Iždo jungties konfigūracijos failas:** RetailSdk \\ SampleExtensions \\ HardwareStation \\ extension.EFRSample \\ konfigūracija
    > 
    > Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**. Skirtuke **Bendra** nustatykite **pasirinktį Įgalinti** fiskalinį integravimą kaip **Taip**.
1. Eikite į "Retail" ir "Commerce Channel" nustatymą "Fiscal integration Fiscal" dokumentų teikėjai ir įkelkite anksčiau **\>\>\>** atsisiųstus fiskalinio dokumento teikėjo konfigūracijos failus.
1. Eikite į "Retail" ir "Commerce Channel" nustatymą "Fiscal integration Fiscal" jungtis ir įkelkite anksčiau **\>\>\>** atsisiųstą "Fiscal Connector" konfigūracijos failą.
1. Eikite į **"Retail" ir \> "Commerce" kanalo nustatymo \> "Fiscal integration \> Connector" funkcinius** profilius. Sukurkite du naujus jungties funkcinius šablonus: po vieną kiekvienam anksčiau įkeltam finansinio dokumento tiekėjui ir pasirinkite anksčiau įkeltą fiskalinę jungtį. Pagal reikia [atnaujinti duomenų](#default-data-mapping) susiejimo parametrus.
1. Eikite į **"Retail" ir \> "Commerce \> Channel" nustatymo "Fiscal \> integration Connector" techninius profilius.** Sukurkite naują jungties techninio profilio ir pasirinkite anksčiau įkeltą fiskalinę jungtį. Pagal reikiamą [parametrų versiją](#fiscal-connector-settings) atnaujinkite jungties parametrus.
1. Eikite į **"Retail" ir "Commerce \> Channel" \> nustatymo "Fiscal integration \> Fiscal" jungties** grupes. Sukurkite dvi naujas finansinių jungčių grupes – po vieną kiekvienam anksčiau sukurtam jungties funkciniam profiliui.
1. Eikite į **"Retail" ir "Commerce \>\> Channel" nustatymo "Fiscal integration \> Fiscal" registracijos** procesus. Sukurkite naują finansinio registravimo procesą ir du finansinio registravimo proceso veiksmus bei pasirinkite anksčiau sukurtas finansinių jungčių grupes.
1. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų šabloną, susietą su parduotuve, kurioje turi būti suaktyvintas registracijos procesas. Finansinio registravimo **proceso** "FastTab" pasirinkite anksčiau sukurtą finansinio registravimo procesą. Norėdami įjungti nefinansinių įvykių registravimą EKA, **·** "FastTab" Funkcijos dalyje **EKA** nustatykite parinktį **Auditas** kaip **Taip**.
1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**. Pasirinkite aparatūros šabloną, susietą su aparatūros stotiu, prie kurios bus prijungtas fiskalinis spausdintuvas. **"FastTab" Iždo** išoriniuose įrenginiuose pasirinkite senesnę jungtį sukūrusį techninio profilio jungtį.
1. Atidarykite paskirstymo grafiką **("Retail and Commerce Retail" ir "Commerce IT Distribution" grafiką) ir pasirinkite \> užduotis \>** **1070 ir** **1090, kad** duomenys būtų perkelti į kanalo duomenų bazę.

#### <a name="default-data-mapping"></a>Numatytųjų duomenų susiejimas

Toliau pateiktas numatytasis duomenų susiejimas yra įtrauktas į finansinio dokumento teikėjo konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdžio dalis:

- **Pridėtinės vertės mokesčio (PVM) tarifų konvertavimas – mokesčio procentų verčių, kurios nustatytos PVM kodams, susiejimas su** **atributo TaxG (mokesčių grupė) vertėmis užklausose, kurios siunčiamos į fiskalinę** tarnybą. Čia yra numatytasis susiejimas:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Pirmasis kiekvienos poros komponentas rodo PVM mokesčių grupę, kurią palaiko EFR finansinio registravimo tarnyba. Antrasis komponentas rodo atitinkamą PVM tarifą. Daugiau informacijos apie PVM mokesčių grupes, kurias EFR palaiko Austrijai, ieškokite [EFR](https://public.efsta.net/efr/) nuorodoje.

#### <a name="fiscal-connector-settings"></a>Iždo jungties parametrai

Šie parametrai įtraukiami į fiskalinės jungties konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdys:

- **Galinio punkto** adresas – finansinio registravimo tarnybos URL.
- **Įrenginio skirtasis laikas milisekunde, per kurį fiskalinė jungtis lauks atsakymo iš** fiskalinių registracijų tarnybos.
- **Rodyti finansinio registravimo pranešimus** – ši vėliavėlė valdo, ar finansinių registracijų tarnybos grąžinimai turėtų būti rodomi operatoriui.

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Daugiau informacijos ieškokite Austrijos [(senesnės programos) finansinio integravimo pavyzdžio diegimo](emea-aut-fi-sample-sdk.md) rekomendacijose.
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

#### <a name="set-up-the-development-environment"></a>Programavimo aplinkos kūrimas

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba [Dynamics 365 Commerce atsisiųskite](https://github.com/microsoft/Dynamics365Commerce.Solutions) sprendimų saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr.["Download Retail SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite EFR sprendimą **Dynamics365Commerce.Solutions \\ FiscalIntegration \\\\ EFR.sln** ir sukurkite jį.
1. Įdiegti CRT plėtinius:

    1. Rasti plėtinio CRT diegimo programą:

        - **"Commerce Scale Unit":** **aplanke Efr \\\\ ScaleUnit ScaleUnit.EFR.Installer talpyklos \\\\ debug \\ net461** raskite **ScaleUnit.EFR.Installer diegimo** priemonės.
        - **Vietinė CRT "Modern POS": aplanke** **Efr \\ ModernPOS \\ ModernPOS.EFR.Installer talpyklos \\\\ debug \\ net461** raskite **ModernPOS.EFR.Installer diegimo** kūrėjas.

    1. Paleiskite CRT plėtinio diegimo programą iš komandų eilutės:

        - **"Commerce Scale Unit":**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **"Modern CRT POS" vieta:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Įdiekite aparatūros stoties plėtinius:

    1. Aplanke **Efr \\ HardwareStation \\ HardwareStation.EFR.Installer \\ talpyklos \\ debug \\ net461** raskite **HardwareStation.EFR.Installer diegimo** priemonės.
    1. Paleiskite plėtinio diegimo programą iš komandų eilutės.

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Norėdami sugeneruoti ir paleisti debesies skalės vienetą ir savitarnos diegiant finansinio integravimo pavyzdžio [paketus, atlikite nurodytus veiksmus.](fiscal-integration-sample-build-pipeline.md) **EFR build-pipeline.yml šablono JAML failą galima** rasti sprendimų saugyklos YAML_Files pardavimo galimybių **\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) aplanke.

## <a name="design-of-extensions"></a>Plėtinių dizainas

Austrijos finansinio registravimo tarnybos integravimo pavyzdys remiasi finansinio [integravimo funkcija ir yra Mažmeninės prekybos SDK](fiscal-integration-for-retail-channel.md) dalis. Pavyzdys yra **sprendimų saugyklos src \\ FiscalIntegration \\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke (pvz., [išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskalinio dokumento teikėjas, kuris yra plėtinys, ir fiskalinė jungtis, kuri yra CRT "Commerce Hardware Station" plėtinys. Daugiau informacijos apie tai, kaip naudoti "Retail SDK", žr. "Retail SDK" architektūrą ir nepriklausomos pakavimo [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) [sukūrimo pardavimo galimybių](../dev-itpro/build-pipeline.md) sukūrimą.

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Daugiau informacijos ieškokite Austrijos [(senesnės programos) finansinio integravimo pavyzdžio diegimo](emea-aut-fi-sample-sdk.md) rekomendacijose. Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, tikslas yra generuoti konkrečios paslaugos dokumentus ir tvarkyti atsakymus iš fiskalinės registracijos tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

Dokumentų teikėjai gali naudoti dvi užklausų apdorojimo programas:

- **DocumentProviderEFRFiscalAUT – ši apdorojimo programa naudojama finansinių** registracijų tarnybos iždo dokumentams generuoti.
- **DocumentProviderEFRNonFiscalAUT – ši apdorojimo programa naudojama** nefinansiniai dokumentams, skirti finansinio registravimo tarnybai, generuoti.

Šios apdorojimo programos perimamos iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą "Commerce" būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje pateikiama informacija apie tai, kokį dokumentą reikia generuoti. Jis grąžina su paslauga susijusius dokumentus, kurie turėtų būti užregistruoti fiskalinės registracijos tarnyboje.
- **GetNonFiscalDocumentDocumentProviderRequest – šioje užklausoje** yra informacijos apie tai, kas turėtų būti generuojamas nefinansinis dokumentas. Jis grąžina su paslauga susijusius dokumentus, kurie turėtų būti užregistruoti fiskalinės registracijos tarnyboje.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas, Z ataskaitos spausdinimas, kliento sąskaitos depozitai, klientų užsakymų depozitai, audito įvykiai ir ne pardavimo operacijos.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – ši užklausa grąžina atsakymą iš fiskalinės registracijos tarnybos. Šis atsakymas serijizuotas, kad būtų galima suformuoti eilutę, kad ji būtų paruošta įrašyti.

#### <a name="configuration"></a>Konfigūravimas

Finansinio dokumento teikėjo konfigūracijos failai yra sprendimų saugyklos **src \\ FiscalIntegration \\ Efr \\\\ konfigūracijų DocumentProviders**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke:

- **DocumentProviderFiscalEFRSampleAustria – iždo dokumentų** teikėjo konfigūracijos failas.
- **DocumentProviderNonFiscalEFRSampleAustria – nefinansinių dokumentų** teikėjo konfigūracijos failas.

Šių failų paskirtis – įgalinti finansinio dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra bendrauti su fiskalinės registracijos tarnyba. Aparatūros stoties plėtinys naudoja HTTP protokolą dokumentams, kuriuos CRT plėtinys sugeneruoja, pateikti į fiskalinės registracijos tarnybą. Ji taip pat tvarko atsakymus, gautus iš fiskalinės registracijos tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

**EFRHandler** užklausų apdorojimo programa yra registracijos tarnybos užklausų tvarkymo pradinis taškas.

Apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti "Commerce" būstinėje nurodytą fiskalinės jungties pavadinimą.

"Fiscal Connector" palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus į fiskalinės registracijos tarnybą ir pateikia iš jos atsakymą.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama fiskalinės registracijos tarnybos sveikatos patikrinimui.
- **InicijuotiFiscalDeviceRequest** – ši užklausa naudojama fiskalinės registracijos tarnybai inicijuoti.

#### <a name="configuration"></a>Konfigūravimas

Fiskalinės jungties konfigūracijos failas yra **src \\ FiscalIntegration \\ Efr \\\\ Configurations \\ Connectors ConnectorEFRSample.xml** sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo paskirtis – įgalinti fiskalinės jungties parametrus konfigūruoti iš "Commerce" būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
