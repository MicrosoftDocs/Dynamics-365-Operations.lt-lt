---
title: Švedijos kontrolės įtaiso integracijos pavyzdys
description: Šioje temoje pateikta Švedijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: 32c2cf31d82d17d3391536e7a9f1722e1462c336
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944771"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Švedijos kontrolės įtaiso integracijos pavyzdys

[!include [banner](../includes/banner.md)]

Šioje temoje pateikta Švedijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Šis finansinio integravimo funkcijos pavyzdys pakeičia ankstesnį [EKA integravimo pavyzdį su Švedijos kontrolės vienetais](retail-sdk-control-unit-sample.md). Ankstesnis pavyzdys neatnaudoja finansų integravimo [sistemos ir](./fiscal-integration-for-retail-channel.md) vėlesniuose naujuose taps nebenaudojami. Norėdami gauti informacijos apie tai, kaip perkelti iš ankstesnio pavyzdžio į pavyzdį, kuris atitinka Dynamics 365 Commerce **10.0.22 ir ankstesnę versiją, žr. skyrių "Perkėlimas iš**[ankstesnio integravimo pavyzdžio".](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample)

Švedijos komercijos funkcionalumas apima elektroninio kasos kodo (EKA) integravimą su Švedijai skirtais finansiniais įrenginiais, kurie vadinami kontrolės *vienetais*. Šis pavyzdys išplečia [finansinio integravimo](fiscal-integration-for-retail-channel.md) funkciją. Laikoma, kad valdymo vienetas yra faktiškai prijungtas prie aparatūros stoties, su kurią EKA galima susieti. Kaip pavyzdį šiame pavyzdyje naudojamas programos programavimo sąsaja (API), kuri naudojama valdymo vieneto [CleanCash Type A,](https://www.retailinnovation.se/produkter) naudojant RetailNaudoja HTT AB. Naudojama CleanCash API 1.1.4 versija.

Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

"Microsoft" neišleidžia jokios aparatūros, programinės įrangos ar dokumentacijos iš "RetailKimo" HTT AB. Norėdami gauti informacijos apie tai, kaip gauti valdymo vienetą ir jį valdyti, susisiekite su ["RetailVz." HTT](https://www.retailinnovation.se/) AB.

## <a name="scenarios"></a>Scenarijai

Švedijos kontrolės vieneto integravimo pavyzdys apima šiuos pajėgumus:

- Pardavimas, grąžinimas ir kvitų kopijos automatiškai užregistruojamos valdymo vienete, kuris prijungtas prie aparatūros stoties, kuri yra sujungta su EKA.
- Užregistruotos operacijos valdymo vieneto kontrolinis kodas ir gamybos numeris fiksuojami iš kontrolės vieneto ir įrašomi operacijoje. Šie duomenys dar vadinami finansiniu *atsakymu*. Fiskalinį atsakymą galima peržiūrėti parduotuvės **operacijų** puslapyje.
- Pasirinktiniai valdymo kodo laukai ir valdymo vieneto gamybos numeris gali būti įtraukti į kvito maketą. Tada galite kvite išspausdinti operacijos fiskalinį atsakymą.
- Finansinis operacijos atsakymas rodomas elektroninio žurnalo **(Švedijos) kanalo** ataskaitoje.
- Galimos kelios klaidų tvarkymo pasirinktys. Štai keletas pavyzdžių:

    - Jei galima kartoti, pakartokite finansinio registravimo veiksmą. Galite kartoti fiskalinę registraciją, jei, pvz., kontrolinis vienetas neprijungtas, neparuoštas arba neatsako.
    - Atidėti finansinio registravimo datą.
    - Praleisti ataskaitinį registravimą arba pažymėti operaciją kaip užregistruotą ir įtraukti informacijos kodus, kad būtų fiksuojama trikties priežastis ir papildoma informacija.
    - Prieš atidarę naują pardavimo operaciją ar uždarius pardavimo operaciją, patikrinkite valdymo vieneto pasiekiamumą.

### <a name="limitations-of-the-sample"></a>Pavyzdžio apribojimai

Švedijos kontrolės vieneto integravimo pavyzdys šiuo metu nepalaiko klientų užsakymų scenarijų.

## <a name="setting-up-the-integration-with-control-units"></a>Integravimo su valdymo vienetais nustatymas

Daugiau informacijos apie nustatymą, reikalingą Švedijai, ieškokite [Švedijos "Commerce"](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden) nustatymas.

### <a name="configuring-swedenspecific-receipts"></a>Švedijos – konkrečių gavimų konfigūravimas

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruoti pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Galite konfigūruoti kalbos tekstą ir pasirinktinius laukus, kurie naudojami EKA kvitų formatuose. Numatytoji gavimo nustatymą sukūrusio vartotojo įmonė turėtų būti tas pats juridinis subjektas, kuriame sukurtas kalbos teksto nustatymas. Arba tas pats kalbos tekstas turėtų būti sukurtas ir vartotojo numatytoje įmonėje, ir parduotuvės juridiniame subjekte, kuriam sukurtas nustatymas.

Kalbos **teksto puslapyje** pridėkite šiuos kvitų maketų pasirinktinių laukų žymių įrašus. Atsikreipkite **dėmesį, kad lentelėje pateiktos kalbos ID, teksto ID ir teksto vertės** **yra tik** **pavyzdžiai**. Juos galite pakeisti, kad jie atitiktų jūsų poreikius. Tačiau jūsų naudojamas teksto ID vertės turi būti unikalios ir jų vertės turi būti lygios arba **didesnės** 900001.

Įtraukite šias EKA žymes į **EKA** skyrių, kalbos **teksto** puslapį.

| Kalbos ID | Teksto ID | Tekstas                  |
|-------------|---------|-----------------------|
| en-JAV       | 900001  | Registro kontrolinis kodas |
| en-JAV       | 900002  | Užregistruoti įrenginį       |

Pasirinktinių **laukų** puslapyje pridėkite šiuos įrašus prie kvitų maketų pasirinktinių laukų. Atkreipkite **dėmesį, kad** antraštės teksto ID reikšmės turi atitikti teksto ID **vertes**, kurias nurodėte kalbos **teksto** puslapyje.

| Pavadinimas                         | Tipas    | Vaizdo aprašo teksto ID |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Gavimas | 900001          |
| SE_FISCALREGISTERID          | Gavimas | 900002          |

> [!NOTE]
> Svarbu nurodyti teisingus pasirinktinius laukų pavadinimus, kaip pateikta pirmiau pateiktoje lentelėje. Neteisingas pasirinktinio lauko pavadinimas gali sukelti kvitų duomenų.

#### <a name="configure-receipt-formats"></a>Kvitų formatų konfigūravimas

Kiekvienam kvito formatui, kuris būtinas, pakeiskite lauko Spausdinti veikimo būdą **vertę** į Visada **spausdinti**.

Kvitų formato dizaineryje į poraštės skyrių įtraukite šiuos **pasirinktinius** laukus. Įsidėmėkite, kad laukų pavadinimai atitinka ankstesniame šios temos skyriuje jūsų apibrėžtus kalbos tekstus.

- **Registro kontrolinis** kodas – šiame lauke spausdinamas kontrolinis kodas.
- **Užregistruoti** įrenginį – šiame lauke spausdinamas valdymo vieneto gamybos numeris.

Daugiau informacijos apie tai, kaip dirbti su kvitų formatais, žr. [Kvitų šablonus ir](../receipt-templates-printing.md) spausdinimą.

### <a name="set-up-fiscal-integration-for-sweden"></a>Nustatyti Švedijos finansų integravimą

Švedijos kontrolės vieneto integravimo pavyzdys remiasi finansinio [integravimo funkcija ir yra](fiscal-integration-for-retail-channel.md) "Retail SDK" dalis. Pavyzdys yra sprendimų saugyklos **src \\ FiscalIntegration \\ CleanCash aplanke**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (pvz., išleidimo [/ 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash) pavyzdys). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskalinio dokumento teikėjas, kuris yra "Commerce" vykdymo laiko pratęsimas (CRT), ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Daugiau informacijos apie tai, kaip naudoti "Retail SDK", žr. "Retail SDK" architektūrą ir nepriklausomos pakavimo [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) [sukūrimo pardavimo galimybių](../dev-itpro/build-pipeline.md) sukūrimą.

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Ankstesnę mažmeninės prekybos SDK versiją turite naudoti kūrėjo virtualioje mašinoje (VM) Microsoft Dynamics "Lifecycle Services" (LCS). Daugiau informacijos ieškokite Švedijos [(senesnės gamybos) valdymo vieneto integravimo pavyzdžio diegimo](emea-swe-fi-sample-sdk.md) rekomendacijose.
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

Atlikite finansinio integravimo nustatymo veiksmus, kaip aprašyta ["Commerce" kanalų finansinio integravimo](setting-up-fiscal-integration-for-retail-channel.md) nustatymas.

1. [Nustatyti fiskalinės registracijos procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taip pat pasižymėkite finansinio registravimo proceso parametrus, [bvz., šio valdymo vieneto integravimo pavyzdį.](#set-up-the-registration-process)
1. [Nustatykite klaidų tvarkymo parametrus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Įgalinti neautomatinį atidėtų fiskalinės registracijos vykdymą](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Sukonfigūruokite kanalo](#configure-channel-components) komponentus.

### <a name="set-up-the-registration-process"></a>Nustatyti registracijos procesą

Norėdami įgalinti registracijos procesą, atlikite šiuos veiksmus, kad nustatytumėte "Commerce" būstinę. Daugiau informacijos ieškokite [Set up fiscal integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųskite finansinio dokumento teikėjo ir finansinio jungties konfigūracijos failus:

    1. Atidaryti [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Pasirinkite teisingą išleidimo šakos versiją pagal savo SDK / programos versiją **[(pvz., leidimas / 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atidaryti **src \> FiscalIntegration \> CleanCash.**
    1. Atsisiųskite finansinio dokumento teikėjo konfigūracijos failą **commerceRuntime \> DocumentProvider.CleanCashSample \> Configuration \> DocumentProviderFiscalCleanCashSample.xml (pvz., failo paleidimui** / [9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)
    1. Atsisiųskite finansinio jungties konfigūracijos failą, kurį reikia atsisiųsti iš **HardwareStation \> Connector.CleanCashSample \> Configuration \> ConnectorCleanCashSample.xml** (pvz., leidimo / [9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml) failas).

    > [!WARNING]
    > Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Šio finansinio integravimo pavyzdžio konfigūracijos failai yra šiuose LCS kūrėjo VM mažmeninės prekybos SDK aplankuose:
    >
    > - **Iždo dokumentų teikėjo konfigūracijos failas:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ extensions.DocumentProvider.CleanCashSample \\ konfigūracijos \\ DocumentProviderFiscalCleanCashSample.xml
    > - **Iždo jungties konfigūracijos failas:** RetailSdk \\ SampleExtensions \\ HardwareStation \\ extension.CleanCashSample \\ Configuration \\ ConnectorCleanCashSample.xml
    > 
    > Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**. Skirtuke **Bendra** nustatykite **pasirinktį Įgalinti** fiskalinį integravimą kaip **Taip**.
1. Eikite į "Retail" ir "Commerce Channel" nustatymą "Fiscal integration Fiscal" dokumentų teikėjai ir įkelkite anksčiau **\>\>\>** atsisiųstą fiskalinio dokumento teikėjo konfigūracijos failą.
1. Eikite į "Retail" ir "Commerce Channel" nustatymą "Fiscal integration Fiscal" jungtis ir įkelkite anksčiau **\>\>\>** atsisiųstą "Fiscal Connector" konfigūracijos failą.
1. Eikite į **"Retail" ir \> "Commerce" kanalo nustatymo \> "Fiscal integration \> Connector" funkcinius** profilius. Sukurti naują jungties funkcinį profilį. Pasirinkite anksčiau įkeltą dokumento teikėją ir jungtį. Pagal reikia [atnaujinti duomenų](#default-data-mapping) susiejimo parametrus.
1. Eikite į **"Retail" ir \> "Commerce \> Channel" nustatymo "Fiscal \> integration Connector" techninius profilius.** Sukurkite naują jungties techninio profilio ir pasirinkite anksčiau įkeltą fiskalinę jungtį. Pagal reikiamą [parametrų versiją](#fiscal-connector-settings) atnaujinkite jungties parametrus.
6. Eikite į **"Retail" ir "Commerce \> Channel" \> nustatymo "Fiscal integration \> Fiscal" jungties** grupes. Sukurkite naują anksčiau sukurto jungties funkcinių profilių finansinių jungčių grupę.
7. Eikite į **"Retail" ir "Commerce \>\> Channel" nustatymo "Fiscal integration \> Fiscal" registracijos** procesus. Sukurkite naują finansinio registravimo procesą ir finansinio registravimo proceso veiksmą, tada pasirinkite anksčiau sukurtą finansinių jungčių grupę.
8. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų šabloną, susietą su parduotuve, kurioje turi būti suaktyvintas registracijos procesas. Finansinio registravimo **proceso** "FastTab" pasirinkite anksčiau sukurtą finansinio registravimo procesą.
9. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**. Pasirinkite aparatūros šabloną, susietą su aparatūros stotiu, prie kurios bus prijungtas fiskalinis spausdintuvas. **"FastTab" Iždo** išoriniuose įrenginiuose pasirinkite senesnę jungtį sukūrusį techninio profilio jungtį.
10. Atidarykite paskirstymo grafiką **("Retail and Commerce Retail" ir "Commerce IT Distribution" grafiką) ir pasirinkite \> užduotis \>** **1070 ir** **1090, kad** duomenys būtų perkelti į kanalo duomenų bazę.

#### <a name="default-data-mapping"></a>Numatytųjų duomenų susiejimas

Toliau pateiktas numatytasis duomenų susiejimas yra įtrauktas į finansinio dokumento teikėjo konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdžio dalis:

- **Pridėtinės vertės mokesčio (PVM) kodo konvertavimas – šis susiejimas nustato įrenginio pridėtinės vertės** mokesčio (PVM) kodus iki atitinkamų PVM kodų. PVM kodo susiejimo formatas turėtų būti toks:

    ```
    1 : code1 ; 2 : code2
    ```

    Toliau pateikiamas šio formato paaiškinimas.

    - *1* ir *2 yra tam tikro* įrenginio PVM kodai.
    - Kabliataškis (;) naudojamas kaip skyriklis.
    - *1* kodas *ir 2 kodas yra PVM* kodai, sukonfigūruoti "Commerce Headquarters". Turite modifikuoti pavyzdžio susiejimą pagal jūsų programoje sukonfigūruotus mokesčių kodus.

    Kontroliniai vienetai palaiko iki keturių skirtingų PVM kodų. Todėl PVM kodo susiejimas gali būti nustatytas tokiu būdu:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Keli PVM kodai gali būti susieti su tuo pačiu įrenginio PVM kodu.

#### <a name="fiscal-connector-settings"></a>Iždo jungties parametrai

Šie parametrai įtraukiami į fiskalinės jungties konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdys:

- **Ryšių eilutė** – valdymo vieneto ryšio nustatymai.
- **Skirtasis** laikas – laikas milisekunde, kurį vairuotojas lauks atsakymo iš valdymo vieneto.

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Daugiau informacijos ieškokite Švedijos [(senesnės gamybos) valdymo vieneto integravimo pavyzdžio diegimo](emea-swe-fi-sample-sdk.md) rekomendacijose.
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

#### <a name="set-up-the-development-environment"></a>Programavimo aplinkos kūrimas

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba [Dynamics 365 Commerce atsisiųskite](https://github.com/microsoft/Dynamics365Commerce.Solutions) sprendimų saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr.["Download Retail SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite kontrolinio vieneto integravimo sprendimą **Dynamics365Commerce.Solutions \\ FiscalIntegration \\\\ CleanCash CleanCash.sln** ir sukurkite jį.
1. Įdiegti CRT plėtinius:

    1. Rasti plėtinio CRT diegimo programą:

        - **"Commerce Scale Unit": aplanke** **CleanCash \\\\ ScaleUnit ScaleUnit.CleanCash.Installer \\ talpyklos \\ debug \\ net461** raskite **ScaleUnit.CleanCash.Installer diegimo** kūrėjas.
        - **Vietinė CRT "Modern POS": aplanke** **CleanCash \\\\ ModernPOS ModernPOS.CleanCash.Installer \\ talpyklos \\ debug \\ net461** raskite **ModernPOS.CleanCash.Installer diegimo** kūrėjas.

    2. Paleiskite CRT plėtinio diegimo programą iš komandų eilutės:

        - **"Commerce Scale Unit":**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **"Modern CRT POS" vieta:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Įdiekite aparatūros stoties plėtinius:

    1. Aplanke **CleanCash \\\\ HardwareStation HardwareStation.CleanCash.Installer \\ talpyklos \\ debug \\ net461** raskite **HardwareStation.CleanCash.Installer diegimo** priemonės.
    1. Paleiskite plėtinio diegimo programą iš komandų eilutės:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Norėdami sugeneruoti ir paleisti debesies skalės vienetą ir savitarnos diegiant finansinio integravimo pavyzdžio [paketus, atlikite nurodytus veiksmus.](fiscal-integration-sample-build-pipeline.md) **CleanCash build-pipeline.yml šablono JAML failą galima** rasti YAML_Files saugyklos pardavimo galimybių **\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) aplanke.

## <a name="design-of-the-extensions"></a>Plėtinių dizainas

Švedijos kontrolės vieneto integravimo pavyzdys remiasi finansinio [integravimo funkcija ir yra](fiscal-integration-for-retail-channel.md) "Retail SDK" dalis. Pavyzdys yra sprendimų saugyklos **src \\ FiscalIntegration \\ CleanCash aplanke**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (pvz., išleidimo [/ 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash) pavyzdys). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskalinio dokumento teikėjas, kuris yra CRT plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Daugiau informacijos apie tai, kaip naudoti "Retail SDK", žr. "Retail SDK" architektūrą ir nepriklausomos pakavimo [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) [sukūrimo pardavimo galimybių](../dev-itpro/build-pipeline.md) sukūrimą.

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Daugiau informacijos ieškokite Švedijos [(senesnės gamybos) valdymo vieneto integravimo pavyzdžio diegimo](emea-swe-fi-sample-sdk.md) rekomendacijose. Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

### <a name="crt-extension-design"></a>CRT plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti paslaugai bvz., dokumentus ir tvarkyti kontrolinio vieneto atsakymus.

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

Yra viena **DocumentProviderCleanCash** užklausų apdorojimo programa, skirta dokumentų tiekėjui. Ši apdorojimo programa naudojama valdymo vieneto iždo dokumentams generuoti.

Ši apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą "Commerce" būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje pateikiama informacija apie tai, kokį dokumentą reikia generuoti. Jis grąžina aptarnavimo dokumentą, kuris turi būti užregistruotas valdymo vienete.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi pardavimo įvykiai ir audito įvykiai.

#### <a name="configuration"></a>Konfigūravimas

Finansinio dokumento teikėjo konfigūracijos failas yra **src \\ FiscalIntegration \\ CleanCash \\ CommerceRuntime \\ DocumentProvider.CleanCashSample \\ konfigūracijos \\ DocumentProviderFiscalCleanCashSample.xml** sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Šio failo paskirtis – įgalinti dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, paskirtis yra palaikyti ryšį su kontrolės vienetu. Ji naudoja HTTP protokolą dokumentams, kuriuos CRT plėtinys sugeneruoja valdymo vienetui, pateikti. Jis taip pat tvarko atsakymus, gautus iš kontrolinio vieneto.

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

**CleanCashHandler** užklausos apdorojimo programa yra įvesties taškas valdymo užklausoms valdymo vienetui.

Apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti "Commerce" būstinėje nurodytą fiskalinės jungties pavadinimą.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest – ši užklausa siunčia dokumentus** valdymo vienetui ir grąžina atsakymą iš jo.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama kontrolinio vieneto sveikatos patikrinti.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama valdymo vienetui inicijuoti.

#### <a name="configuration"></a>Konfigūravimas

Iždo jungties konfigūracijos failas yra **src \\ FiscalIntegration \\ CleanCash \\ HardwareStation \\ jungtyje.CleanCashSample \\ Configuration \\ ConnectorCleanCashSample.xml** Sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo paskirtis – įgalinti finansinio jungties parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
