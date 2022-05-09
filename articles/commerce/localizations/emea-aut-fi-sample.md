---
title: Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Austrijai
description: Šioje temoje apžvelgiama Austrijos fiskalinės integracijos imtis Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 826c1cb0fba7025b16dadbfa6157683392945103
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/19/2022
ms.locfileid: "8614156"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Fiskalinės registracijos paslaugos integravimo pavyzdys, skirtas Austrijai

[!include[banner](../includes/banner.md)]

Šioje temoje apžvelgiama Austrijos fiskalinės integracijos imtis Microsoft Dynamics 365 Commerce.

Siekiant patenkinti vietinius fiskalinius reikalavimus kasos aparatams Austrijoje, Dynamics 365 Retail Austrijos funkcija apima pavyzdinį prekybos vietos (EKA) integravimą su išorės fiskalinės registracijos paslauga. Pavyzdys išplečia fiskalinės [integracijos funkciją](fiscal-integration-for-retail-channel.md). Jis pagrįstas [EFSTA](https://www.efsta.eu/at/fiskalloesungen/oesterreich) EFR (Elektroninio fiskalinio [registro)](https://www.efsta.eu/at/) sprendimu ir leidžia bendrauti su EFR paslauga per HTTPS protokolą. EFR paslauga turėtų būti patalpinta mažmeninės prekybos aparatūros stotyje arba atskirame kompiuteryje, prie kurio galima prisijungti iš aparatūros stoties. Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

"Microsoft" neišleidžia jokios aparatūros, programinės įrangos ar dokumentacijos iš EFSTA. Norėdami gauti informacijos apie tai, kaip gauti EFR sprendimą ir jį valdyti, susisiekite su [EFSTA](https://www.efsta.eu/at/kontakt).

## <a name="scenarios"></a>Scenarijai

Austrijos fiskalinės registracijos paslaugos integravimo pavyzdys apima šiuos scenarijus:

- Grynųjų pinigų operacijų registravimas fiskalinės registracijos tarnyboje:

    - Siųsti išsamius operacijos duomenis fiskalinės registracijos tarnybai. Šie duomenys apima pardavimo eilutės informaciją ir informaciją apie nuolaidas, mokėjimus ir mokesčius.
    - Užfiksuokite fiskalinės registracijos tarnybos atsakymą. Šis atsakymas apima skaitmeninį parašą ir nuorodą į registruotą operaciją.
    - Užregistruokite mokesčius ir susiekite juos su fiskalinės registracijos tarnybos mokesčių kodais.
    - Kvite atsispausdinkite registruotos operacijos QR kodą.

- Dovanų kortelių operacijų ir klientų indėlių registravimas nepiniginėmis operacijomis fiskalinės registracijos tarnyboje:

    - Išduokite arba pridėkite pinigų prie dovanų kortelės.
    - Užregistruokite kliento sąskaitos indėlį.
    - Užregistruokite kliento užsakymo indėlį.

- Neparduotų operacijų ir įvykių registravimas nepiniginėmis operacijomis fiskalinės registracijos tarnyboje:

    - Atidaryti pamainą ir uždaryti pamainą
    - Pradžios suma, slankusis įrašas ir mokėjimo priemonės šalinimas
    - Kainos perrašymas
    - Mokesčio perrašymas
    - Išspausdinta kvito kopija
    - Atidaryti stalčių
    - Spausdinti X ataskaitą
    - Spausdinti Z ataskaitą

- Spausdinami dienos pabaigos išrašai (X/Z ataskaitos), kuriuose yra austrijai būdingi laukai:

    - Bendras klientams pristatytų produktų ar paslaugų skaičius
    - Pardavimų suskirstymas pagal mokesčio tarifą
    - Mokėjimų suskirstymas pagal kasos ir (arba) kasos operatorių
    - Kainų nuolaidos ir grąža, mažinanti kasdienius pardavimus
    - Nuliniai pardavimai (dovanos)

- Klaidų tvarkymas, pvz., šios parinktys:

    - Bandykite pakartotinę fiskalinę registraciją, jei galima bandyti dar kartą, pvz., jei fiskalinės registracijos paslauga nepasiekiama, neparuošta arba neatsako.
    - Atidėti fiskalinę registraciją.
    - Praleiskite fiskalinę registraciją arba pažymėkite operaciją kaip registruotą ir įtraukite informacijos kodus, kad užfiksuotumėte gedimo priežastį ir papildomą informaciją.
    - Patikrinkite, ar yra fiskalinės registracijos paslaugos, prieš atidarydami naują pardavimo operaciją arba užbaigdami pardavimo operaciją.

### <a name="gift-cards"></a>Dovanų kortelės

Fiskalinės registracijos paslaugos integravimo pavyzdys įgyvendina šias taisykles, susijusias su dovanų kortelėmis:

- Neįtraukti pardavimo eilučių, susijusių su išdavimo *dovanų kortele* ir *Įtraukti į dovanų kortelės* operacijas iš grynųjų pinigų operacijos. Užuot registravę šias eilutes kaip grynųjų pinigų operacijos dalį, užregistruokite jas kaip atskirą nepiniginę operaciją fiskalinės registracijos tarnyboje.
- Nespausdinkite mokesčių grupės suskirstymo ir QR kodo kvite, jei kvitą sudaro tik dovanų kortelės eilutės.
- Spausdinti bendrą dovanų kortelių sumą, kuri išduodama arba iš naujo nuskaičiuojama operacijoje atskirai nuo kvito grynųjų pinigų operacijos sumos.
- Įrašyti apskaičiuotus mokėjimo eilučių koregavimus kanalo duomenų bazėje su nuoroda į atitinkamą fiskalinę operaciją.
- Mokėjimas dovanų kortele laikomas įprastu mokėjimu.

### <a name="customer-deposits-and-customer-order-deposits"></a>Klientų indėliai ir klientų užsakymų indėliai

Fiskalinės registracijos paslaugos integravimo pavyzdys įgyvendina šias taisykles, susijusias su klientų indėliais ir klientų užsakymų indėliais:

- Užregistruokite nepiniginę operaciją, jei operacija yra kliento indėlis.
- Užregistruokite nepiniginę operaciją, jei operacijoje yra tik kliento užsakymo indėlis arba kliento užsakymo indėlio grąžinimas.
- Išskaičiuokite kliento užsakymo depozito sumą iš mokėjimo eilučių, kai sukuriamas hibridinis kliento užsakymas.
- Įrašyti apskaičiuotus mokėjimo eilučių koregavimus kanalo duomenų bazėje su nuoroda į hibridinio kliento užsakymo fiskalinę operaciją.

### <a name="limitations-of-the-sample"></a>Imties apribojimai

Fiskalinės registracijos tarnyba palaiko tik tuos atvejus, kai PVM yra įtrauktas į kainą. Todėl parinktis **Kaina su PVM** turi būti nustatyta kaip **Taip** tiek parduotuvėms, tiek pirkėjams.

## <a name="set-up-commerce-for-austria"></a>"Commerce for Austria" nustatymas

Šiame skyriuje aprašomi "Commerce" parametrai, būdingi Austrijai ir rekomenduojami. Daugiau informacijos apie sąranką ieškokite [Commerce pagrindiniame puslapyje](../index.md).

Norėdami naudoti austrijos funkciją, turite nurodyti šiuos parametrus:

- Pagrindiniame juridinio asmens adrese nustatykite **lauką Šalis /regionas** į **AUT** (Austrija).
- Kiekvienos Austrijoje esančios parduotuvės EKA funkcijų profilyje nustatykite **ISO kodo** lauką į **AT** (Austrija).

Taip pat turite nurodyti šiuos Austrijos parametrus. Atminkite, kad baigę sąranką turite vykdyti atitinkamas paskirstymo užduotis.

### <a name="set-up-vat-per-austrian-requirements"></a>Nustatyti PVM pagal Austrijos reikalavimus

Turite sukurti PVM kodus, PVM grupes ir prekės PVM grupes. Taip pat turite nustatyti produktų ir paslaugų PVM informaciją. Daugiau informacijos apie tai, kaip nustatyti ir naudoti PVM priemones, ieškokite [PVM peržiūra.](../../finance/general-ledger/indirect-taxes-overview.md)

Pardavimo kvituose galite išspausdinti sutrumpintą PVM kodo kodą (pvz., "A" arba "B"). Jei norite, kad ši funkcija būtų prieinama, puslapyje PVM kodai nustatykite **lauką Spausdinti kodą** **.**

### <a name="set-up-stores"></a>Parduotuvių nustatykite

**Puslapyje Visos parduotuvės** atnaujinkite parduotuvės informaciją. Tiksliau nustatykite šiuos parametrus:

- Lauke PVM **grupė nurodykite** PVM grupę, kurią reikia naudoti pardavimams numatytojam klientui.
- Nustatykite **parinktį Kainos su PVM** kaip **Taip**.
- Nustatykite **įmonės** pavadinimą lauke Pavadinimas. Šis pakeitimas padeda užtikrinti, kad įmonės pavadinimas būtų rodomas pardavimo kvite. Taip pat galite įtraukti įmonės pavadinimą į pardavimo kvito maketą kaip laisvos formos tekstą.
- Nustatyti mokesčio **identifikavimo numerio (TIN)** lauką kaip įmonės identifikavimo numerį. Šis pakeitimas padeda užtikrinti, kad įmonės identifikavimo numeris būtų rodomas pardavimo kvite. Taip pat galite prie pardavimo kvito maketo pridėti įmonės identifikavimo numerį kaip laisvos formos tekstą.

### <a name="set-up-functionality-profiles"></a>Funkcijų šablonų nustatymas

Nustatyti EKA funkcijų profilius:

- Kvitų **numeravimo** "FastTab" nustatykite kvitų **numeravimą**, sukurdami arba atnaujindami pardavimo, **pardavimo užsakymo** ir grąžinimo **kvitų** operacijų tipų įrašus.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruoti pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Galite konfigūruoti kalbos tekstą ir pasirinktinius laukus, kurie naudojami EKA kvitų formatuose. Numatytoji gavimo nustatymą sukūrusio vartotojo įmonė turėtų būti tas pats juridinis subjektas, kuriame sukurtas kalbos teksto nustatymas. Arba tas pats kalbos tekstas turėtų būti sukurtas ir vartotojo numatytoje įmonėje, ir parduotuvės juridiniame subjekte, kuriam sukurtas nustatymas.

Kalbos teksto **puslapyje** pridėkite šiuos kvitų maketų pasirinktinių laukų žymių įrašus. Atkreipkite dėmesį **, kad** lentelėje **pateiktos kalbos ID,** **teksto ID** ir teksto vertės yra tik pavyzdžiai. Galite keisti juos, kad jie atitiktų jūsų poreikius. Tačiau jūsų naudojamas **teksto ID** vertės turi būti unikalios ir turi būti lygios arba didesnės nei 900001.

Įtraukite šias EKA etiketes į **lentelės kalbos teksto** EKA **sekciją**:

| Kalbos ID | Teksto ID | Tekstas                      |
|-------------|---------|---------------------------|
| lt       | 900001  | QR kodas                   |
| lt       | 900002  | Tęstinis skaičius         |
| lt       | 900003  | Mažmeninės prekybos mokesčių spausdinimo kodas     |
| lt       | 900004  | Iš viso (pardavimas)             |
| lt       | 900005  | Bendras mokestis (pardavimai)         |
| lt       | 900006  | Iš viso įtraukti mokestį (pardavimai) |
| lt       | 900007  | Mokesčio suma (pardavimai)        |
| lt       | 900008  | Mokesčių pagrindas (pardavimas)         |

Pasirinktinių **laukų puslapyje** pridėkite šiuos įrašus prie kvitų maketų pasirinktinių laukų. Atminkite, kad **antraštės teksto ID** reikšmės turi atitikti **teksto ID** reikšmes **, kurias nurodėte puslapyje Kalbos teksto tekstas**:

| Vardas                 | Tipas    | Vaizdo aprašo teksto ID |
|----------------------|---------|-----------------|
| QRCODE               | Gavimas | 900001          |
| NEPERTRAUKIAMAS SKAIČIUS     | Gavimas | 900002          |
| RETAILPRINTCODE      | Gavimas | 900003          |
| SALESTOTAL           | Gavimas | 900004          |
| SALESTOTALTAX        | Gavimas | 900005          |
| SALESTOTALINCLUDETAX | Gavimas | 900006          |
| SALESTAXAMOUNT       | Gavimas | 900007          |
| SALESTAXBASIS        | Gavimas | 900008          |

> [!NOTE]
> Svarbu nurodyti teisingus pasirinktinių laukų pavadinimus, kurie išvardyti ankstesnėje lentelėje. Neteisingas pasirinktinio lauko pavadinimas gali sukelti kvitų duomenų.

### <a name="configure-receipt-formats"></a>Kvitų formatų konfigūravimas

Kiekvienam reikiamam gavimo formatui pakeiskite lauko Spausdinimo **elgsena** reikšmę į **Visada spausdinti**.

Kvitų formato dizaineryje į atitinkamus kvitų skyrius įtraukite šiuos pasirinktinius laukus. Nepamirškite, kad laukų pavadinimai atitinka ankstesniame skyriuje jūsų apibrėžtus kalbos tekstus.

- **Antraštė:** Įtraukite šiuos laukus:

    - **Parduotuvės pavadinimo** ir **mokesčių identifikavimo numerio** laukai, naudojami įmonės pavadinimui ir tapatybės numeriui kvituose spausdinti. Arba galite įtraukti įmonės pavadinimą ir tapatybės numerį į maketą kaip laisvos formos tekstą.
    - **Parduotuvės adresas**, **data**, **laikas 24 val**., **kvito numeris** ir registro **numerio** laukai.
    - **Nepertraukiamo numerio** laukus, kad būtų galima identifikuoti grynųjų pinigų operacijos numerį fiskalinės registracijos tarnyboje.

- **Eilutės:** įtraukite šiuos laukus:

    - **Prekės pavadinimas**.
    - **Kiekis**.
    - **Bendra kaina su mokesčiais**.
    - **Mažmeninės prekybos mokesčio spausdinimo kodas**, naudojamas spausdinti sutrumpintą kodą, atitinkantį prekei taikomą PVM kodą.

- **Poraštė:** įtraukite šiuos laukus:

    - Mokėjimo laukus, kad būtų išspausdintos kiekvieno mokėjimo būdo mokėjimo sumos. Pavyzdžiui, į vieną maketo **eilutę įtraukite** **laukus** Mokėjimo priemonės pavadinimas ir Mokėjimo priemonės suma.
    - **Pardavimų bendrųjų** laukų grupė:

        - **Iš viso (pardavimai)** laukas, naudojamas spausdinti bendrą kvito grynųjų pinigų pardavimo sumą. Į sumą neįskaičiuotas mokestis. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Laukas Iš viso įtraukti mokestį (pardavimus),** naudojamas spausdinti bendrą kvito grynųjų pinigų pardavimo sumą. Į sumą įskaičiuoti mokesčiai. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **bendras mokestis (pardavimai),** kuris naudojamas spausdinti kvito bendrą grynųjų pinigų pardavimo mokesčio sumą. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.

    - **Mokesčių skaidymo** laukų grupė. Visi šios laukų grupės laukai turi būti išspausdinti vienoje atskiroje eilutėje.

        - **Mokesčio ID** laukas, kuris yra standartinis laukas, leidžiantis spausdinti kiekvieno PVM kodo PVM suvestinę. Laukas turi būti pridėtas prie naujos eilutės.
        - **Mokesčio procento** laukas, kuris yra standartinis laukas, naudojamas PVM kodo galiojamam mokesčio tarifui spausdinti.
        - **Mokesčių pagrindo (pardavimo)** laukas, naudojamas spausdinant pvm kodo kvito bendrą grynųjų pinigų pardavimo sumą. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
        - **Mokesčio sumos (pardavimo)** laukas, naudojamas spausdinant PVM kodo grynųjų pardavimo kvitų mokesčių sumą.
        - **Mažmeninės prekybos mokesčių** spausdinimo kodo laukas, naudojamas sutrumpintam kodui, atitinkančiam PVM kodą, spausdinti.

    - **QR kodo laukas**, naudojamas nuorodai į registruotą grynųjų pinigų operaciją spausdinti QR kodo pavidalu.

        > [!NOTE]
        > QR **kodo vertė** nuskaitoma iš finansinio registro atsakymo. EFR savo atsakyme grąžina QR **kodą** tik tada, jei EFR konfigūracijos atributų lauko vertė yra aprašyta EFSTA dokumentuose. QR kodo formatas atributų **lauke**, EFR konfigūracijoje, turi būti nustatytas kaip **BMP**.

Daugiau informacijos apie tai, kaip dirbti su kvitų formatais, ieškokite [Gavimo kvitų formatų nustatymas ir kūrimas](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Nustatyti Austrijos fiskalinę integraciją

Austrijos fiskalinės registracijos tarnybos integravimo pavyzdys yra pagrįstas [fiskalinės integracijos funkcijomis](fiscal-integration-for-retail-channel.md) ir yra Mažmeninės prekybos SDK dalis. Pavyzdys yra sprendimų **saugyklos srcFiscalIntegrationEfr \\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke (pvz., [pavyzdys paleidime / 9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas, kuris yra "Commerce Runtime (CRT) plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti "Retail SDK", [žr. "Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)[" architektūrą ir nepriklausomo pakavimo SDK sukūrimo pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją programavimo virtualiojoje kompiuteryje (VM) ciklo Microsoft Dynamics tarnybose (LCS). Daugiau informacijos ieškokite [Austrijos fiskalinės integracijos imties diegimo gairėse (senstelėjęs)](emea-aut-fi-sample-sdk.md). Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

Atlikite finansinio integravimo nustatymo veiksmus, kaip aprašyta ["Commerce" kanalų finansinio integravimo nustatymas](setting-up-fiscal-integration-for-retail-channel.md):

1. [Nustatykite finansinio registravimo procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Be to, pateikite pastabą apie finansinio registravimo proceso parametrus, bvz [., šios finansinio registravimo tarnybos integravimo pavyzdį](#set-up-the-registration-process).
1. [Nustatyti klaidų tvarkymo parametrus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Įgalinkite neautomatinį atidėtos finansinio registravimo vykdymą](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Sukonfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nustatyti registravimo procesą

Norėdami įjungti registravimo procesą, atlikite šiuos veiksmus norėdami nustatyti "Commerce Headquarters". Daugiau informacijos rasite "Commerce [" kanalų finansinio integravimo nustatykite](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųsti finansinio dokumento teikėjo ir fiskalinio jungties konfigūracijos failus:

    1. Atidaryti sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK/programos versiją (pvz., **[paleidimas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atidaryti **src \> FiscalIntegration \> Efr**.
    1. Atidarykite Configurations DocumentProviders **ir atsisiųskite finansinių dokumentų teikėjo konfigūracijos failus: \> DocumentProviderFiscalEFRSampleAustria.xml** ir **DocumentProviderNonFiscalEFRSampleAustria.xml** (pvz., **failų vieta leidimui/9.33**).[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders)
    1. Atsisiųskite finansinio jungties konfigūracijos **failą \>\> konfigūracijos failu konfigūracijos jungčių ConnectorEFRSample.xml** (pvz., [paleidimo / 9.33 failas](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją LCS programuotojo VM. Šio fiskalinio integravimo pavyzdžio konfigūracijos failai yra toliau esančiuuose "Retail" SDK, esantis LCS programuotojo VM, aplankuose:
    >
    > - **Finansinių dokumentų teikėjo konfigūracijos failai:** RetailSdkSampleExtensionsCommerceRuntimeExtensions.DocumentProvider.EFRSampleConfiguration\\\\\\\\
    > - **Fiskalinės jungties konfigūracijos failas:** RetailSdkSampleExtensionsHardwareStationExtension.EFRSampleConfiguration\\\\\\\\
    > 
    > Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**. Skirtuke **Bendra** nustatykite pasirinktį **Įgalinti finansų integravimą** kaip **Taip**.
1. Eikite į **Mažmeninės prekybos ir komercijos \> kanalo nustatymą \> Fiskalinė integracija \> Fiskalinių dokumentų teikėjai** ir įkelkite anksčiau atsisiųstus finansinių dokumentų teikėjo konfigūracijos failus.
1. Eikite į **"Retail" ir "Commerce Channel" \> nustatymą "Fiscal integration \> Fiscal \>" jungtis ir įkelkite anksčiau atsisiųstą "Fiscal** Connector" konfigūracijos failą.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" funkcinius profilius**. Sukurkite du naujus jungties funkcinius profilius, po vieną kiekvienam finansinio dokumento teikėjui, kurį įkėlėte anksčiau, ir pasirinkite fiskalinę jungtį, kurią įkėlėte anksčiau. Pagal reikia [atnaujinti duomenų susiejimo](#default-data-mapping) parametrus.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" techninius profilius**. Sukurkite naują jungties techninio profilio ir pasirinkite anksčiau įkeltą fiskalinę jungtį. Pagal reikiamą [parametrų versiją atnaujinkite](#fiscal-connector-settings) jungties parametrus.
1. Eikite į " **Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Fiscal" jungties grupes**. Sukurkite dvi naujas finansinių jungčių grupes, po vieną kiekvienam jungties funkciniam profiliui, kurį sukūrėte anksčiau.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Fiscal" registracijos procesus**. Sukurkite naują fiskalinės registracijos procesą ir du fiskalinės registracijos proceso veiksmus bei pasirinkite anksčiau sukurtas finansinių jungčių grupes.
1. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų šabloną, susietą su parduotuve, kurioje turi būti suaktyvintas registracijos procesas. Finansinio registravimo **proceso "** FastTab" pasirinkite anksčiau sukurtą finansinio registravimo procesą. Norėdami įgalinti nefinansinių įvykių registravimą EKA, **FastTab Funkcijos** dalyje **EKA** nustatykite **parinktį Auditas** į **Taip**.
1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**. Pasirinkite aparatūros šabloną, susietą su aparatūros stotiu, prie kurios bus prijungtas fiskalinis spausdintuvas. **"FastTab" Iždo išoriniuose** įrenginiuose pasirinkite senesnę jungtį sukūrusį techninio profilio jungtį.
1. Atidarykite paskirstymo grafiką (**"Retail and Commerce Retail ir Commerce \> IT \> Distribution"** grafiką) **ir pasirinkite užduotis 1070** **ir 1090**, kad duomenys būtų perkelti į kanalo duomenų bazę.

#### <a name="default-data-mapping"></a>Numatytųjų duomenų susiejimas

Toliau pateiktas numatytasis duomenų susiejimas yra įtrauktas į finansinio dokumento teikėjo konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdžio dalis:

- **Pridėtinės vertės mokesčio (PVM) tarifų konvertavimas –** mokesčio procentų verčių, kurios nustatytos PVM kodams, susiejimas su atributo TaxG **(mokesčių grupė)** vertėmis užklausose, kurios siunčiamos į fiskalinę tarnybą. Čia yra numatytasis susiejimas:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Pirmasis kiekvienos poros komponentas rodo PVM mokesčių grupę, kurią palaiko EFR finansinio registravimo tarnyba. Antrasis komponentas rodo atitinkamą PVM tarifą. Daugiau informacijos apie PVM mokesčių grupes, kurias EFR remia Austrijai, ieškokite EFR [nuorodoje](https://public.efsta.net/efr/).

#### <a name="fiscal-connector-settings"></a>Iždo jungties parametrai

Šie parametrai įtraukiami į fiskalinės jungties konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdys:

- **Galinio punkto** adresas – finansinio registravimo tarnybos URL.
- **Įrenginio skirtasis** laikas – laikas milisekundėmis, per milisekundes fiskalinė jungtis lauks atsakymo iš fiskalinės registracijos tarnybos.
- **Rodyti finansinio registravimo pranešimus** – ši vėliavėlė valdo, ar finansinių registracijų tarnybos grąžinimai turėtų būti rodomi operatoriui.

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

> [!WARNING]
> Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją LCS programuotojo VM. Daugiau informacijos ieškokite [Austrijos fiskalinės integracijos imties diegimo gairėse (senstelėjęs)](emea-aut-fi-sample-sdk.md).
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

#### <a name="set-up-the-development-environment"></a>Programavimo aplinkos kūrimas

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba atsisiųskite [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr. ["Download Retail SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite EFR sprendimą **Dynamics365Commerce.SolutionsFiscalIntegrationEfrEFR.sln\\\\\\ ir sukurkite** jį.
1. Įdiekite CRT plėtinius:

    1. Rasti plėtinio CRT diegimo programą:

        - **"Commerce Scale Unit":** aplanke EfrScaleUnitScaleUnit.EFR.InstallerbinDebugnet461 **\\\\\\\\\\** raskite ScaleUnit.EFR.Installer diegimo **kūrėjas.**
        - **Vietinė CRT "Modern POS":** **aplanke EfrModardPOSModfrePOS.EFR.InstallerbinDebugnet461\\\\\\\\\\** **raskite ModernPOS.EFR.Installer diegimo** kūrėjas.

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

        1. **Aplanke EfrHardwareStationHardwareStation.EFR.InstallerbinDebugnet461\\\\\\\\\\** **raskite HardwareStation.EFR.Installer diegimo** priemonės.
        1. Paleiskite plėtinio diegimo programą iš komandų eilutės vykdydami šią komandą.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Įdiekite EKA plėtinius:

        1. Atidarykite EKA **iždo jungties pavyzdžio sprendimą Dynamics365Commerce.SolutionsFiscalIntegrationPosFiscalConnectorSampleContoso.PosFiscalConnectorSample.sln\\\\\\** ir sukurkite jį.
        1. **Aplanke PosFiscalConnectorSampleStoreCommerce.InstallerbinDebugnet461\\\\\\\\** **raskite Contoso.PosFiscalConnectorSample.StoreCommerce.Installer diegimo** priemonės.
        1. Paleiskite plėtinių diegimo programą iš komandų eilutės, kurioje veikia ši komanda.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Gamybos aplinka

Norėdami sugeneruoti [ir](fiscal-integration-sample-build-pipeline.md) paleisti debesies skalės vienetą ir savitarnos diegiant finansinio integravimo pavyzdžio paketus, atlikite nurodytus veiksmus. **EFR build-pipeline.yml šablono JAML** **failą galima rasti sprendimų saugyklos aplanke YAML_Files \\**[Dynamics 365 Commerce Pipeline.yml.](https://github.com/microsoft/Dynamics365Commerce.Solutions)

## <a name="design-of-extensions"></a>Plėtinių dizainas

Austrijos fiskalinės registracijos tarnybos integravimo pavyzdys yra pagrįstas [fiskalinės integracijos funkcijomis](fiscal-integration-for-retail-channel.md) ir yra Mažmeninės prekybos SDK dalis. Pavyzdys yra sprendimų **saugyklos srcFiscalIntegrationEfr \\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke (pvz., [pavyzdys paleidime / 9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas CRT, kuris yra plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti "Retail SDK", [žr. "Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)[" architektūrą ir nepriklausomo pakavimo SDK sukūrimo pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją LCS programuotojo VM. Daugiau informacijos ieškokite [Austrijos fiskalinės integracijos imties diegimo gairėse (senstelėjęs)](emea-aut-fi-sample-sdk.md). Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas 

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti paslaugai bvz., dokumentus ir tvarkyti atsakymus iš fiskalinių registracijų tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

Dokumentų teikėjams yra dvi užklausų apdorojimo programos:

- **DocumentProviderEFRFiscalAUT** – ši apdorojimo programa naudojama fiskalinės registracijos tarnybos fiskaliniams dokumentams generuoti.
- **DocumentProviderEFRNonFiscalAUT** – ši apdorojimo programa naudojama fiskalinės registracijos tarnybos nefinansiniams dokumentams generuoti.

Šie prižiūrėtojai yra paveldėti **iš INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su jungties dokumento teikėjo pavadinimu, kuris nurodytas "Commerce Headquarters".

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje yra informacijos apie tai, koks dokumentas turėtų būti sugeneruotas. Grąžinamas paslaugai konkretus dokumentas, kuris turi būti užregistruotas finansinio registravimo tarnybose.
- **GetNonFiscalDocumentDocumentProviderRequest** – šioje užklausoje yra informacijos apie tai, koks nefinansinis dokumentas turėtų būti generuojamas. Grąžinamas paslaugai konkretus dokumentas, kuris turi būti užregistruotas finansinio registravimo tarnybose.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa pateikia įvykių, prie kurių bus užsiprenumeruoti, sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimai, X ataskaitos spausdinimas, Z ataskaitos spausdinimas, kliento sąskaitų indėliai, kliento užsakymų indėliai, audito įvykiai ir nepardavimo operacijos.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – ši užklausa grąžina atsakymą iš finansinių registracijų tarnybos. Šis atsakymas yra eilutėmis išrašomas į formą, kad būtų galima įrašyti.

#### <a name="configuration"></a>Konfigūracija

Finansinių dokumentų teikėjo konfigūracijos failai yra sprendimų saugyklos aplanke **\\ srcFiscalIntegrationEfrConfigurationsDocumentProviders\\\\\\**[Dynamics 365 Commerce:](https://github.com/microsoft/Dynamics365Commerce.Solutions/)

- **DocumentProviderFiscalEFRSampleAustria** – finansinių dokumentų teikėjo konfigūracijos failas.
- **DocumentProviderNonFiscalEFRSampleAustria** – nefinansinių dokumentų teikėjo konfigūracijos failas.

Šių failų paskirtis – įgalinti finansinių dokumentų teikėjo parametrus konfigūruoti iš "Commerce" būstinės. Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Fiskalinės jungties plėtinio tikslas yra bendrauti su fiskalinės registracijos tarnyba. Aparatūros stoties plėtinys naudoja HTTP ir HTTPS protokolus, kad pateiktų dokumentus, kuriuos CRT plėtinys generuoja fiskalinės registracijos tarnybai. Jis taip pat tvarko atsakymus, gautus iš finansinio registravimo tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

**EFRHandler užklausos** apdorojimo programa yra iždo registracijos tarnybos užklausų tvarkymo įvesties taškas.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su "Commerce Headquarters" nurodytu finansinio jungties pavadinimu.

Fiskalinė jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus į finansinio registravimo tarnybą ir grąžina atsakymą iš jos.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama norint patikrinti finansinių registracijų tarnybos sveikumą.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama norint inicijuoti finansinių registracijų tarnybą.

#### <a name="configuration"></a>Konfigūracija

Iždo jungties **konfigūracijos failas yra srcFiscalIntegrationEfrConfigurationsConnectorsConnectorEFRSample.xml\\\\\\\\\\**[Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo paskirtis – įgalinti finansinių jungčių parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais.

### <a name="pos-fiscal-connector-extension-design"></a>EKA "Fiscal Connector" plėtinio dizainas

EKA finansinio jungties plėtinio paskirtis yra susisiekti su finansinio registravimo tarnyba iš EKA. Ryšio tikslais naudojamas HTTPS protokolas.

#### <a name="fiscal-connector-factory"></a>Finansinių jungčių gamykla

Iždo jungties gamyklos jungties pavadinimas susietas su "Fiscal Connector **" diegimas ir yra faile Pos.ExtensionConnectorsFiscalConnectorFactory.ts\\\\**. Jungties pavadinimas turi atitikti "Commerce Headquarters" nurodytą finansinio jungties pavadinimą.

#### <a name="efr-fiscal-connector"></a>EFR iždo jungtis

EFR fiskalinė jungtis yra **faile Pos.ExtensionConnectorsEfrEfrFiscalConnector.ts\\\\\\**. Jis įdiegia **IFiscalConnector sąsają**, palaikančią šias užklausas:

- **FiscalRegisterSubmitDocumentClientRequest** – ši užklausa siunčia dokumentus finansinio registravimo tarnybai ir grąžina atsakymą iš jos.
- **FiscalRegisterIsReadyClientRequest** – ši užklausa naudojama norint patikrinti iždo dokumentų registracijos tarnybos sveikumą.
- **FiscalRegisterInitializeClientRequest** – ši užklausa naudojama norint inicijuoti finansinio registravimo tarnybą.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra sprendimų saugyklos **aplanke srcFiscalIntegrationEfrConfigurationsConnectors\\\\\\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Failo paskirtis – įgalinti finansinio jungties parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais. Pridedami šie parametrai:

- **Galinio punkto** adresas – finansinio registravimo tarnybos URL.
- **Skirtasis** laikas milisekundiais, kurį jungtis lauks atsakymo iš fiskalinių registracijų tarnybos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
