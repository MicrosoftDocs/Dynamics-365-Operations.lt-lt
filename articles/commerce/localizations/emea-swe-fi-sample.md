---
title: Švedijos kontrolės įtaiso integracijos pavyzdys
description: Šiame straipsnyje pateikta Švedijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: 3376e6a901b692371a44b5c74c1e6b4afd0cd573
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275072"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Švedijos kontrolės įtaiso integracijos pavyzdys

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta Švedijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Šis finansinio integravimo funkcijos pavyzdys pakeičia ankstesnį [EKA integravimo pavyzdį su Švedijos kontrolės vienetais](retail-sdk-control-unit-sample.md). Ankstesnis pavyzdys neatnaudoja finansų integravimo [sistemos ir](./fiscal-integration-for-retail-channel.md) vėlesniuose naujuose taps nebenaudojami. Norėdami gauti informacijos apie tai Dynamics 365 Commerce **, kaip perkelti iš ankstesnio pavyzdžio į pavyzdį, kuris atitinka 10.0.22** ir ankstesnę versiją, [žr. skyrių "Perkėlimas iš ankstesnio integravimo pavyzdžio"](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample).

Švedijos komercijos funkcionalumas apima elektroninio kasos kodo (EKA) integravimą su Švedijai skirtais finansiniais įrenginiais, kurie vadinami kontrolės *vienetais*. Šis pavyzdys išplečia finansinio [integravimo funkciją](fiscal-integration-for-retail-channel.md). Laikoma, kad valdymo vienetas yra faktiškai prijungtas prie aparatūros stoties, su kurią EKA galima susieti. Kaip pavyzdį šiame pavyzdyje naudojamas programos programavimo sąsaja (API), [kuri naudojama valdymo vieneto CleanCash Type A](https://www.retailinnovation.se/produkter), naudojant RetailNaudoja HTT AB. Naudojama CleanCash API 1.1.4 versija.

Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

"Microsoft" neišleidžia jokios aparatūros, programinės įrangos ar dokumentacijos iš "RetailKimo" HTT AB. Norėdami gauti informacijos apie tai, kaip gauti valdymo vienetą ir jį valdyti, susisiekite su ["RetailKimo HTT AB"](https://www.retailinnovation.se/).

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

Daugiau informacijos apie nustatymą, reikalingą Švedijai, ieškokite [Švedijos "Commerce" nustatymas](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden).

### <a name="configuring-swedenspecific-receipts"></a>Švedijos – konkrečių gavimų konfigūravimas

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruoti pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Galite konfigūruoti kalbos tekstą ir pasirinktinius laukus, kurie naudojami EKA kvitų formatuose. Numatytoji gavimo nustatymą sukūrusio vartotojo įmonė turėtų būti tas pats juridinis subjektas, kuriame sukurtas kalbos teksto nustatymas. Arba tas pats kalbos tekstas turėtų būti sukurtas ir vartotojo numatytoje įmonėje, ir parduotuvės juridiniame subjekte, kuriam sukurtas nustatymas.

Kalbos teksto **puslapyje** pridėkite šiuos kvitų maketų pasirinktinių laukų žymių įrašus. Atkreipkite dėmesį **, kad** lentelėje **pateiktos kalbos ID,** **teksto ID** ir teksto vertės yra tik pavyzdžiai. Juos galite pakeisti, kad jie atitiktų jūsų poreikius. Tačiau jūsų naudojamas **teksto ID** vertės turi būti unikalios ir jų vertės turi būti lygios arba didesnės 900001.

Įtraukite šias EKA žymes į **EKA** skyrių, kalbos **teksto** puslapį.

| Kalbos ID | Teksto ID | Tekstas                  |
|-------------|---------|-----------------------|
| lt       | 900001  | Registro kontrolinis kodas |
| lt       | 900002  | Užregistruoti įrenginį       |

Pasirinktinių **laukų puslapyje** pridėkite šiuos įrašus prie kvitų maketų pasirinktinių laukų. Atkreipkite **dėmesį, kad antraštės teksto ID** reikšmės turi **atitikti teksto ID** vertes, kurias nurodėte kalbos **teksto** puslapyje.

| Vardas                         | Tipas    | Vaizdo aprašo teksto ID |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Gavimas | 900001          |
| SE_FISCALREGISTERID          | Gavimas | 900002          |

> [!NOTE]
> Svarbu nurodyti teisingus pasirinktinius laukų pavadinimus, kaip pateikta pirmiau pateiktoje lentelėje. Neteisingas pasirinktinio lauko pavadinimas gali sukelti kvitų duomenų.

#### <a name="configure-receipt-formats"></a>Kvitų formatų konfigūravimas

Kiekvieno kvito formato atveju pakeiskite lauko Spausdinti veikimo būdą vertę **į** Visada **spausdinti**.

Kvitų formato dizaineryje į poraštės skyrių įtraukite šiuos pasirinktinius **laukus**. Atkreipkite dėmesį, kad laukų pavadinimai atitinka kalbos tekstus, kuriuos apibrėžiate ankstesniame šio straipsnio skyriuje.

- **Registro kontrolinis** kodas – šiame lauke spausdinamas kontrolinis kodas.
- **Užregistruoti įrenginį** – šiame lauke spausdinamas valdymo vieneto gamybos numeris.

Daugiau informacijos apie tai, kaip dirbti su kvitų formatais, žr. Kvitų [šablonus ir spausdinimą](../receipt-templates-printing.md).

### <a name="set-up-fiscal-integration-for-sweden"></a>Nustatyti Švedijos finansų integravimą

Švedijos kontrolės vieneto integravimo pavyzdys remiasi finansinio [integravimo funkcija ir](fiscal-integration-for-retail-channel.md) yra "Retail SDK" dalis. Pavyzdys yra sprendimų **saugyklos src\\ FiscalIntegration\\ CleanCash**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke (pvz., [išleidimo / 9.33 pavyzdys](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas, kuris yra "Commerce Runtime (CRT) plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti "Retail SDK", [žr. "Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)[" architektūrą ir nepriklausomo pakavimo SDK sukūrimo pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją programavimo virtualiojoje kompiuteryje (VM) ciklo Microsoft Dynamics tarnybose (LCS). Daugiau informacijos ieškokite Švedijos ([senesnės gamybos) valdymo vieneto integravimo pavyzdžio diegimo rekomendacijose](emea-swe-fi-sample-sdk.md).
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

Atlikite finansinio integravimo nustatymo veiksmus, kaip aprašyta ["Commerce" kanalų finansinio integravimo nustatymas](setting-up-fiscal-integration-for-retail-channel.md).

1. [Nustatykite finansinio registravimo procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taip pat pasižymėkite finansinio registravimo proceso parametrus, bvz., [šio valdymo vieneto integravimo pavyzdį](#set-up-the-registration-process).
1. [Nustatyti klaidų tvarkymo parametrus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Įgalinkite neautomatinį atidėtos finansinio registravimo vykdymą](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Sukonfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nustatyti registravimo procesą

Norėdami įjungti registravimo procesą, atlikite šiuos veiksmus norėdami nustatyti "Commerce Headquarters". Daugiau informacijos rasite "Commerce [" kanalų finansinio integravimo nustatykite](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųsti finansinio dokumento teikėjo ir fiskalinio jungties konfigūracijos failus:

    1. Atidaryti sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK/programos versiją (pvz., **[paleidimas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atidaryti **src \> FiscalIntegration \> CleanCash**.
    1. Atsisiųskite finansinio dokumento teikėjo konfigūracijos failą commerceRuntime **DocumentProvider.CleanCashSample Configuration DocumentProviderFiscalCleanCashSample.xml \> (pvz., \> leidimo / 9.33 failas \>).**[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)
    1. Atsisiųskite fiskalinės **jungties konfigūracijos failą, kurį yra HardwareStation \> Connector.CleanCashSample \> Configuration \> ConnectorCleanCashSample.xml (pvz** ., [leidimo / 9.33 failas](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)).

    > [!WARNING]
    > Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją LCS programuotojo VM. Šio fiskalinio integravimo pavyzdžio konfigūracijos failai yra toliau esančiuuose "Retail" SDK, esantis LCS programuotojo VM, aplankuose:
    >
    > - **Iždo dokumentų teikėjo konfigūracijos failas:** RetailSdk\\ SampleExtensions CommerceRuntime\\ extensions.DocumentProvider.CleanCashSample\\\\ konfigūracijos\\ DocumentProviderFiscalCleanCashSample.xml
    > - **Iždo jungties konfigūracijos failas:** RetailSdk\\ SampleExtensions\\ HardwareStation\\ extension.CleanCashSample\\ Configuration\\ ConnectorCleanCashSample.xml
    > 
    > Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**. Skirtuke **Bendra** nustatykite pasirinktį **Įgalinti finansų integravimą** kaip **Taip**.
1. Eikite į **"Retail" ir "Commerce \> Channel" \> nustatymą "Fiscal integration \> Fiscal"** dokumentų teikėjai ir įkelkite anksčiau atsisiųstą fiskalinio dokumento teikėjo konfigūracijos failą.
1. Eikite į **"Retail" ir "Commerce Channel" \> nustatymą "Fiscal integration \> Fiscal \>" jungtis ir įkelkite anksčiau atsisiųstą "Fiscal** Connector" konfigūracijos failą.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" funkcinius profilius**. Sukurti naują jungties funkcinį profilį. Pasirinkite anksčiau įkeltą dokumento teikėją ir jungtį. Pagal reikia [atnaujinti duomenų susiejimo](#default-data-mapping) parametrus.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" techninius profilius**. Sukurkite naują jungties techninio profilio ir pasirinkite anksčiau įkeltą fiskalinę jungtį. Pagal reikiamą [parametrų versiją atnaujinkite](#fiscal-connector-settings) jungties parametrus.
6. Eikite į " **Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Fiscal" jungties grupes**. Sukurkite naują anksčiau sukurto jungties funkcinių profilių finansinių jungčių grupę.
7. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Fiscal" registracijos procesus**. Sukurkite naują finansinio registravimo procesą ir finansinio registravimo proceso veiksmą, tada pasirinkite anksčiau sukurtą finansinių jungčių grupę.
8. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų šabloną, susietą su parduotuve, kurioje turi būti suaktyvintas registracijos procesas. Finansinio registravimo **proceso "** FastTab" pasirinkite anksčiau sukurtą finansinio registravimo procesą.
9. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**. Pasirinkite aparatūros šabloną, susietą su aparatūros stotiu, prie kurios bus prijungtas fiskalinis spausdintuvas. **"FastTab" Iždo išoriniuose** įrenginiuose pasirinkite senesnę jungtį sukūrusį techninio profilio jungtį.
10. Atidarykite paskirstymo grafiką (**"Retail and Commerce Retail ir Commerce \> IT \> Distribution"** grafiką) **ir pasirinkite užduotis 1070** **ir 1090**, kad duomenys būtų perkelti į kanalo duomenų bazę.

#### <a name="default-data-mapping"></a>Numatytųjų duomenų susiejimas

Toliau pateiktas numatytasis duomenų susiejimas yra įtrauktas į finansinio dokumento teikėjo konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdžio dalis:

- **Pridėtinės vertės mokesčio (PVM) kodo konvertavimas** – šis susiejimas nustato įrenginio pridėtinės vertės mokesčio (PVM) kodus iki atitinkamų PVM kodų. PVM kodo susiejimo formatas turėtų būti toks:

    ```
    1 : code1 ; 2 : code2
    ```

    Toliau pateikiamas šio formato paaiškinimas.

    - *1* ir *2* yra tam tikro įrenginio PVM kodai.
    - Kabliataškis (;) naudojamas kaip skyriklis.
    - *1* kodas *ir 2* kodas yra PVM kodai, sukonfigūruoti "Commerce Headquarters". Turite modifikuoti pavyzdžio susiejimą pagal jūsų programoje sukonfigūruotus mokesčių kodus.

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
> Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją LCS programuotojo VM. Daugiau informacijos ieškokite Švedijos ([senesnės gamybos) valdymo vieneto integravimo pavyzdžio diegimo rekomendacijose](emea-swe-fi-sample-sdk.md).
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

#### <a name="set-up-the-development-environment"></a>Programavimo aplinkos kūrimas

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba atsisiųskite [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr. ["Download Retail SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite kontrolinio vieneto integravimo sprendimą **Dynamics365Commerce.Solutions\\ FiscalIntegration\\ CleanCash\\ CleanCash.sln** ir sukurkite jį.
1. Įdiegti CRT plėtinius:

    1. Rasti plėtinio CRT diegimo programą:

        - **"Commerce Scale Unit":** **aplanke CleanCash\\ ScaleUnit\\ ScaleUnit.CleanCash.Installer\\ talpyklos\\ debug\\ net461** **raskite ScaleUnit.CleanCash.Installer diegimo** kūrėjas.
        - **Vietinė CRT "Modern POS":** **aplanke CleanCash\\ ModernPOS ModernPOS.CleanCash.Installer\\\\ talpyklos\\ debug\\ net461** **raskite ModernPOS.CleanCash.Installer diegimo** kūrėjas.

    2. Paleiskite CRT plėtinio diegimo programą iš komandų eilutės:

        - **"Commerce Scale Unit":**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **" CRT Modern POS" vieta:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Įdiekite aparatūros stoties plėtinius:

    1. **Aplanke CleanCash\\ HardwareStation\\ HardwareStation.CleanCash.Installer talpyklos\\\\ debug\\ net461** **raskite HardwareStation.CleanCash.Installer diegimo** priemonės.
    1. Paleiskite plėtinio diegimo programą iš komandų eilutės:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Norėdami sugeneruoti [ir](fiscal-integration-sample-build-pipeline.md) paleisti debesies skalės vienetą ir savitarnos diegiant finansinio integravimo pavyzdžio paketus, atlikite nurodytus veiksmus. CleanCash build-pipeline.yml **šablono JAML** **failą galima rasti sprendimų saugyklos YAML_Files\\** pardavimo [Dynamics 365 Commerce galimybių aplanke.](https://github.com/microsoft/Dynamics365Commerce.Solutions)

## <a name="design-of-the-extensions"></a>Plėtinių dizainas

Švedijos kontrolės vieneto integravimo pavyzdys remiasi finansinio [integravimo funkcija ir](fiscal-integration-for-retail-channel.md) yra "Retail SDK" dalis. Pavyzdys yra sprendimų **saugyklos src\\ FiscalIntegration\\ CleanCash**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke (pvz., [išleidimo / 9.33 pavyzdys](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas CRT, kuris yra plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti "Retail SDK", [žr. "Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)[" architektūrą ir nepriklausomo pakavimo SDK sukūrimo pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją LCS programuotojo VM. Daugiau informacijos ieškokite Švedijos ([senesnės gamybos) valdymo vieneto integravimo pavyzdžio diegimo rekomendacijose](emea-swe-fi-sample-sdk.md). Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

### <a name="crt-extension-design"></a>CRT plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti paslaugai bvz., dokumentus ir tvarkyti kontrolinio vieneto atsakymus.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

Yra viena **DocumentProviderCleanCash** užklausų apdorojimo programa, skirta dokumentų tiekėjui. Ši apdorojimo programa naudojama valdymo vieneto iždo dokumentams generuoti.

Ši apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su jungties dokumento teikėjo pavadinimu, kuris nurodytas "Commerce Headquarters".

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje yra informacijos apie tai, koks dokumentas turėtų būti sugeneruotas. Jis grąžina aptarnavimo dokumentą, kuris turi būti užregistruotas valdymo vienete.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa pateikia įvykių, prie kurių bus užsiprenumeruoti, sąrašą. Šiuo metu palaikomi pardavimo įvykiai ir audito įvykiai.

#### <a name="configuration"></a>Konfigūracija

Finansinio dokumento **teikėjo konfigūracijos failas yra src\\ FiscalIntegration\\ CleanCash\\ CommerceRuntime\\ DocumentProvider.CleanCashSample\\ konfigūracijos\\ DocumentProviderFiscalCleanCashSample.xml**[Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Šio failo paskirtis – įgalinti dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, paskirtis yra palaikyti ryšį su kontrolės vienetu. Ji naudoja HTTP protokolą dokumentams, kuriuos plėtinys CRT sugeneruoja valdymo vienetui, pateikti. Jis taip pat tvarko atsakymus, gautus iš kontrolinio vieneto.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

CleanCashHandler **užklausos** apdorojimo programa yra įvesties taškas valdymo užklausoms valdymo vienetui.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su "Commerce Headquarters" nurodytu finansinio jungties pavadinimu.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus valdymo vienetui ir grąžina atsakymą iš jo.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama kontrolinio vieneto sveikatos patikrinti.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama valdymo vienetui inicijuoti.

#### <a name="configuration"></a>Konfigūracija

**Iždo jungties konfigūracijos failas yra src\\ FiscalIntegration\\ CleanCash\\ HardwareStation\\ jungtyje.CleanCashSample\\ Configuration\\ ConnectorCleanCashSample.xml**[Dynamics 365 Commerce Sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo paskirtis – įgalinti finansinio jungties parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
