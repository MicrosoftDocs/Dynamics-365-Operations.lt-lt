---
title: Fiskalinio spausdintuvo integracijos pavyzdys (Lenkija)
description: Šioje temoje pateikta Lenkijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-2-1
ms.openlocfilehash: 1b3d7d59494b215ae47f710e200e7e0c57e4ca29
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944870"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Fiskalinio spausdintuvo integracijos pavyzdys (Lenkija)

[!include[banner](../includes/banner.md)]

Šioje temoje pateikta Lenkijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.

Lenkijos Dynamics 365 Commerce funkcijos apima pavyzdinį pardavimo galimybių (EKA) integravimą su fiskaliniu spausdintuvu. Pavyzdys išplečia [fiskalinio integravimo funkcijas](fiscal-integration-for-retail-channel.md) ir palaiko POSNET HD 2.02 protokolą, skirtas iždo dokumentų spausdintuvams iš [Posnet Polska S.A.](https://www.posnet.com.pl) Pavyzdys leidžia prisijungti prie fiskalinio spausdintuvo, kuris prijungtas per COM prievadą, naudojant prigimtinę programinės įrangos tvarkyklę. Jis buvo įdiegtas ir patikrintas naudojant programinės įrangos emuliatorių, kuris posnet pateiktą Posnet Hd FV EJ fiskaliniu spausdintuvu. Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

"Microsoft" neišleidžia jokios aparatūros, programinės įrangos ar dokumentacijos iš Posnet. Norėdami gauti informacijos apie tai, kaip gauti fiskalinį spausdintuvą ir jį valdyti, susisiekite [su Posnet Polska S.A.](https://www.posnet.com.pl)

## <a name="scenarios"></a>Scenarijai

Šiuos scenarijus apima finansinio spausdintuvo integravimo pavyzdys Lenkijai:

- Pardavimo scenarijai:

    - Išspausdinkite fiskalinį grynųjų pinigų ir atliekamo pardavimo ir grąžinimo kvitą.
    - Perimti fiskalinio spausdintuvo atsakymą ir saugoti jį kanalo duomenų bazėje.
    - Mokesčiai:

        - Susieti su fiskalinio spausdintuvo mokesčių kodais (padaliniais).
        - Perkelkite susietus mokesčių duomenis į fiskalinį spausdintuvą.

    - Mokėjimai:

        - Susiekite su fiskalinio spausdintuvo mokėjimo metodais.
        - Spausdinti mokėjimus finansinio kvito metu.
        - Spausdinti keitimo informaciją.

    - Spausdinti eilutės nuolaidas.
    - Dovanų kortelės:

        - Iš pardavimo finansinio kvito pašalinti išduotą / iš naujo apmokestinamą dovanų kortelės eilutę.
        - Spausdinti mokėjimą, kuris naudoja dovanų kortelę kaip reguliarų mokėjimo būdą.

    - Spausdinti kliento užsakymo operacijų finansinius kvitus:

        - Nespausdinamas kliento užsakymo depozito finansinis kvitas.
        - Spausdinti kliento užsakymo atliekamų eilučių fiskalinį kvitą.
        - Spausdinti kliento užsakymo paėmimo operacijos fiskalinį kvitą.
        - Spausdinti grąžinimo užsakymo fiskalinį kvitą.

    - Spausdinti [kliento](emea-pol-customer-information.md) informaciją, nurodytą finansinio kvito pardavimo operacijai. Šios informacijos pavyzdys yra kliento PVM numeris.

- Dienos pabaigos išrašai (X finansiniai ir finansiniai Z ataskaitos).
- Klaidos tvarkymą, pvz., šias pasirinktis:

    - Jei galima atlikti kartojimo veiksmą, pvz., jei fiskalinis spausdintuvas neprijungtas, neparuoštas arba neatsako, spausdintuve nepakanka popieriaus arba yra popieriaus strigtis.
    - Atidėti finansinio registravimo datą.
    - Praleisti ataskaitinį registravimą arba pažymėti operaciją kaip užregistruotą ir įtraukti informacijos kodus, kad būtų fiksuojama trikties priežastis ir papildoma informacija.
    - Patikrinkite fiskalinio spausdintuvo pasiekiamumą prieš atidarę naują pardavimo operaciją arba kai pardavimo operacija baigiama.

### <a name="gift-cards"></a>Dovanų kortelės

Fiskalinio spausdintuvo integravimo pavyzdys vykdo šias taisykles, susijusias su dovanų kortelėmis:

- Pašalinti pardavimo eilutes, susijusias su dovanų kortelės *išdavimo ir įtraukti į* dovanų *kortelės operacijas iš finansinio* kvito.
- Nespausdinti finansinio kvito, jei jį sudaro tik dovanų kortelės eilutės.
- Atskaityti bendrą dovanų kortelių, kurios išduotos arba iš naujo apmokestinamos operacijoje, sumą iš finansinio kvito mokėjimo eilučių.
- Įrašykite apskaičiuotus mokėjimo eilučių koregavimus kanalo duomenų bazėje su nuoroda į atitinkamą fiskalinę operaciją.
- Mokėjimas dovanų kortele laikomas įprastu mokėjimu.

### <a name="customer-deposits-and-customer-order-deposits"></a>Kliento depozitai ir kliento užsakymo depozitai

Fiskalinio spausdintuvo integravimo pavyzdys vykdo šias taisykles, susijusias su kliento depozitais ir kliento užsakymo depozitais:

- Nespausdinti finansinio kvito, jei operacija yra kliento depozitas.
- Nespausdinti finansinio kvito, jei operacijoje yra tik kliento užsakymo depozitas arba kliento užsakymo depozito grąžinimas.
- Spausdinti kliento užsakymo paėmimo operacijos finansinio kvito anksčiau sumokėto depozito sumą.
- Atskaityti kliento užsakymo depozito sumą iš mokėjimo eilučių, kai sukurtas kliento užsakymas.
- Įrašykite apskaičiuotus mokėjimo eilučių koregavimus kanalo duomenų bazėje su nuoroda į kliento užsakymo ataskaitinę operaciją.

### <a name="limitations-of-the-sample"></a>Pavyzdžio apribojimai

- Fiskalinis spausdintuvas palaiko tik scenarijus, kuriuose PVM įtraukiamas į kainą. Todėl parduotuvių ir klientų parinktis Kaina su PVM turi būti **nustatyta** kaip **Taip**.
- Kasdienės ataskaitos (X finansinis ir finansinis Z) spausdinamos naudojant įdėtosios pamainos *ataskaitos* formatą.
- Brūkšninio kodo spausdinimas ant finansinių kvitų laikomas galimu pritaikymu, nes ši funkcija nepalaikoma įdėtųjų formatų ir gali būti įdiegta tik naudojant pritaikomą **superformatinę** ataskaitą.
- Fiskalinis spausdintuvas nepalaiko įvairių operacijų. EKA funkcijų šablonuose turi būti nustatyta Parinkties Uždrausti maišymą ir grąžinimą **viena** **kvito** pasirinktis Kaip Taip.

## <a name="set-up-fiscal-integration-for-poland"></a>Nustatyti finansų integravimą Lenkijai

Lenkijos fiskalinio spausdintuvo integravimo pavyzdys pagrįstas [finansinio integravimo funkcija ir yra](fiscal-integration-for-retail-channel.md) "Retail SDK" dalis. Pavyzdys yra sprendimų saugyklos **src \\ FiscalIntegration \\ Posnet** aplanke [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (pvz., išleidimo [/ 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet) pavyzdys). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskalinio dokumento teikėjas, kuris yra "Commerce" vykdymo laiko pratęsimas (CRT), ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Daugiau informacijos apie tai, kaip naudoti "Retail SDK", žr. "Retail SDK" architektūrą ir nepriklausomos pakavimo [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) [sukūrimo pardavimo galimybių](../dev-itpro/build-pipeline.md) sukūrimą.

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Ankstesnę mažmeninės prekybos SDK versiją turite naudoti kūrėjo virtualioje mašinoje (VM) Microsoft Dynamics "Lifecycle Services" (LCS). Daugiau informacijos ieškokite Lenkijos [(senesnės programos) fiskalinio spausdintuvo integravimo pavyzdžio diegimo](emea-pol-fpi-sample-sdk.md) rekomendacijose.
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

Atlikite finansinio integravimo nustatymo veiksmus, kaip aprašyta ["Commerce" kanalų finansinio integravimo](setting-up-fiscal-integration-for-retail-channel.md) nustatymas.

1. [Nustatyti fiskalinės registracijos procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taip pat pasižymėkite finansinio registravimo proceso parametrus, bvz., [šio fiskalinio spausdintuvo integravimo pavyzdį.](#set-up-the-registration-process)
1. [Nustatykite klaidų tvarkymo parametrus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Iš EKA nustatykite finansų X/Z](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos) ataskaitas.
1. [Įgalinti neautomatinį atidėtų fiskalinės registracijos vykdymą](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Sukonfigūruokite kanalo](#configure-channel-components) komponentus.

### <a name="set-up-the-registration-process"></a>Nustatyti registracijos procesą

Norėdami įgalinti registracijos procesą, atlikite šiuos veiksmus, kad nustatytumėte "Commerce" būstinę. Daugiau informacijos ieškokite [Set up fiscal integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųskite finansinio dokumento teikėjo ir finansinio jungties konfigūracijos failus:

    1. Atidaryti [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Pasirinkite teisingą išleidimo šakos versiją pagal savo SDK / programos versiją **[(pvz., leidimas / 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atidaryti **src \> FiscalIntegration \> Posnet.**
    1. Atsisiųskite finansinio dokumento teikėjo konfigūracijos failą **svetainėje CommerceRuntime \> DocumentProvider.PosnetSample \> Configuration \> DocumentProviderPosnetSample.xml** (pvz., failas, skirtas [release/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/CommerceRuntime/DocumentProvider.PosnetSample/Configuration/DocumentProviderPosnetSample.xml)
    1. Atsisiųskite "Fiscal Connector" konfigūracijos failą, kurį reikia atsisiųsti iš **\> HardwareStationVzviceSample \> Configuration \> ConnectorPosnetThermalFVEJ.xml** (pvz., [leidimo / 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/HardwareStation/ThermalDeviceSample/Configuration/ConnectorPosnetThermalFVEJ.xml) failas).

    > [!WARNING]
    > Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Šio finansinio integravimo pavyzdžio konfigūracijos failai yra šiuose LCS kūrėjo VM mažmeninės prekybos SDK aplankuose:
    >
    > - **Iždo dokumentų teikėjo konfigūracijos failas:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ Extension.DocumentProvider.PosnetSample \\ Configuration \\ DocumentProviderPosnetSample.xml
    > - **Iždo jungties konfigūracijos failas:** RetailSdk \\ SampleExtensions \\ HardwareStation \\ extension.Posnet.PjDeviceSample \\ Configuration \\ ConnectorPosnetThermalFVEJ.xml
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

- **Pridėtinės vertės mokesčio (PVM) tarifų konvertavimas – mokesčio procento verčių, kurios nustatytos PVM kodams, susiejimas su iždo dokumentų spausdintuvu** – konkrečiai PVM tarifams. Čia yra numatytasis susiejimas:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Pirmasis kiekvienos poros komponentas rodo PVM tarifo numerį, kuris sukonfigūruotas fiskalinio spausdintuvo. Antrasis komponentas rodo atitinkamą PVM tarifą. Daugiau informacijos apie fiskalinio spausdintuvo PVM tarifo konfigūraciją ieškokite POSNET tvarkyklės dokumentuose.

- **Mokėjimo priemonės tipo susiejimas – mokėjimo būdų, kurie sukonfigūruoti parduotuvei ir mokėjimo formoms, kurias** palaiko fiskalinis spausdintuvas, susiejimas. Čia yra numatytasis susiejimas:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Pirmasis kiekvienos poros komponentas atitinka parduotuvei nustatytą mokėjimo būdą. Antrasis komponentas nurodo atitinkamą mokėjimo formą, kurią palaiko fiskalinis spausdintuvas. Daugiau informacijos apie mokėjimo formas, kurias palaiko fiskalinis spausdintuvas, ieškokite POSNET tvarkyklės dokumentuose. Turite modifikuoti pavyzdžio susiejimą pagal mokėjimo metodus, kurie sukonfigūruoti jūsų programoje.

#### <a name="fiscal-connector-settings"></a>Iždo jungties parametrai

Šie parametrai įtraukiami į fiskalinės jungties konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdys:

- **Jungimosi eilutė – eilutė, aprašantys išsamią ryšio su įrenginiu** informaciją tvarkyklės palaikomu formatu. Daugiau informacijos ieškokite POSNET tvarkyklės dokumentuose.
- **Datos ir laiko sinchronizavimas – reikšmė, nurodanti, ar spausdintuvo data ir laikas turi būti** sinchronizuoti su prijungta aparatūros stotyje.
- **Įrenginio skirtasis laikas milisekunde, per kurį vairuotojas lauks atsakymo iš** įrenginio. Daugiau informacijos ieškokite POSNET tvarkyklės dokumentuose.

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Daugiau informacijos ieškokite Lenkijos [(senesnės programos) fiskalinio spausdintuvo integravimo pavyzdžio diegimo](emea-pol-fpi-sample-sdk.md) rekomendacijose.
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

#### <a name="set-up-the-development-environment"></a>Programavimo aplinkos kūrimas

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba [Dynamics 365 Commerce atsisiųskite](https://github.com/microsoft/Dynamics365Commerce.Solutions) sprendimų saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr.["Download Retail SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite finansinio spausdintuvo integravimo sprendimą **Dynamics365Commerce.Solutions \\ FiscalIntegration \\\\ Posnet Posnet.sln** ir sukurkite jį.
1. Įdiegti CRT plėtinius:

    1. Rasti plėtinio CRT diegimo programą:

        - **"Commerce Scale Unit":** **aplanke Posnet \\ ScaleUnit \\ ScaleUnit.Posnet.Installer \\ talpyklos \\ debug \\ net461** raskite **ScaleUnit.Posnet.Installer diegimo** kūrėjas.
        - **Vietinė CRT "Modern POS": aplanke** **Posnet \\\\ ModernPOS ModernPOS.Posnet.Installer talpyklos \\\\ debug \\ net461** raskite **ModernPOS.Posnet.Installer diegimo** kūrėjas.

    1. Paleiskite CRT plėtinio diegimo programą iš komandų eilutės:

        - **"Commerce Scale Unit":**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **"Modern CRT POS" vieta:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Įdiekite aparatūros stoties plėtinius:

    1. **\\\\ Posnet HardwareStation HardwareStation.PosnetThermalFFiscalPrinter.Installer talpyklos \\\\ debug \\ net461 aplanke** raskite **HardwareStation.PosnetThermalFVFiscalPrinter.Installer diegimo** priemonę.
    1. Paleiskite plėtinio diegimo programą iš komandų eilutės:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Norėdami sugeneruoti ir paleisti debesies skalės vienetą ir savitarnos diegiant finansinio integravimo pavyzdžio [paketus, atlikite nurodytus veiksmus.](fiscal-integration-sample-build-pipeline.md) **Posnet build-pipeline.yml šablono JAML failą galima rasti YAML_Files saugyklos** pardavimo galimybių **\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) aplanke.

## <a name="design-of-extensions"></a>Plėtinių dizainas

Lenkijos fiskalinio spausdintuvo integravimo pavyzdys pagrįstas [finansinio integravimo funkcija ir yra](fiscal-integration-for-retail-channel.md) "Retail SDK" dalis. Pavyzdys yra sprendimų saugyklos **src \\ FiscalIntegration \\ Posnet** aplanke [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (pvz., išleidimo [/ 9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet) pavyzdys). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskalinio dokumento teikėjas, kuris yra CRT plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Daugiau informacijos apie tai, kaip naudoti "Retail SDK", žr. "Retail SDK" architektūrą ir nepriklausomos pakavimo [SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) [sukūrimo pardavimo galimybių](../dev-itpro/build-pipeline.md) sukūrimą.

> [!WARNING]
> Dėl [naujo nepriklausomo pakavimo ir plėtinio modelio apribojimų](../dev-itpro/build-pipeline.md) šiuo metu jis negali būti naudojamas šiai fiskalinės integracijos imčiai. Turite naudoti ankstesnę "Retail SDK" versiją kūrėjo VM LCS. Daugiau informacijos ieškokite Lenkijos [(senesnės programos) fiskalinio spausdintuvo integravimo pavyzdžio diegimo](emea-pol-fpi-sample-sdk.md) rekomendacijose. Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti konkretaus spausdintuvo dokumentus ir tvarkyti atsakymus iš fiskalinio spausdintuvo. Šis plėtinys sugeneruoja poSNET 19-3678 specifikacijos apibrėžtą "JavaScript Object Notation" (JSON) formato spausdintuvui specialių komandų rinkinį.

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

DocumentProviderPosnetProtocol užklausos apdorojimo programa yra įvesties taškas, per kurį užklausa **generuoja** dokumentus iš fiskalinio spausdintuvo.

Apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą "Commerce" būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje pateikiama informacija apie tai, kokį dokumentą reikia generuoti. Grąžinamas spausdintuvui konkretus dokumentas, kuris turi būti užregistruotas fiskaliniu spausdintuvu.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas ir Z ataskaitos spausdinimas.

#### <a name="configuration"></a>Konfigūravimas

Finansinio dokumento teikėjo konfigūracijos failas yra **src \\ FiscalIntegration \\ Posnet \\ CommerceRuntime \\ DocumentProvider.PosnetSample \\ konfigūracijos \\ DocumentProviderPosnetSample.xml** sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo tikslas – įgalinti finansinio dokumento teikėjo parametrus konfigūruoti iš "Commerce" būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, paskirtis yra palaikyti ryšį su fiskaliniu spausdintuvu. Šis plėtinys išk prašo POSNET tvarkyklės funkcijų pateikti komandas, kurias CRT plėtinys sugeneruoja fiskaliniu spausdintuvu. Ji taip pat tvarko įrenginio klaidas.

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

**FiscalPrinterHandler užklausos** apdorojimo programa yra įvesties taškas, skirtas tvarkyti užklausą į fiskalinį per įrenginį.

Apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti "Commerce" būstinėje nurodytą fiskalinės jungties pavadinimą.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest – ši užklausa siunčia dokumentus spausdintuvams ir grąžina atsakymą** iš fiskalinio spausdintuvo.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama įrenginio sveikatos patikrai atlikti.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama spausdintuvui inicijuoti.

#### <a name="configuration"></a>Konfigūravimas

Fiskalinės jungties konfigūracijos failas yra **src \\ FiscalIntegration \\ Posnet \\\\ HardwareStationVzviceSample \\ Configuration \\ ConnectorPosnetThermalFVEJ.xml** sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo paskirtis – įgalinti fiskalinės jungties parametrus konfigūruoti iš "Commerce" būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
