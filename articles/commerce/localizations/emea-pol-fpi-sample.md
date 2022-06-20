---
title: Fiskalinio spausdintuvo integracijos pavyzdys (Lenkija)
description: Šiame straipsnyje pateikta Lenkijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-2-1
ms.openlocfilehash: e71d7b342789e4cf2e7644a46bc847087063fc78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876954"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Fiskalinio spausdintuvo integracijos pavyzdys (Lenkija)

[!include[banner](../includes/banner.md)]

Šiame straipsnyje pateikta Lenkijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.

Lenkijos Dynamics 365 Commerce funkcijos apima pavyzdinį pardavimo galimybių (EKA) integravimą su fiskaliniu spausdintuvu. Pavyzdys išplečia fiskalinio [integravimo funkcijas](fiscal-integration-for-retail-channel.md) ir palaiko POSNET HD 2.02 [protokolą, skirtas iždo dokumentų spausdintuvams iš Posnet Polska S.A.](https://www.posnet.com.pl) Pavyzdys leidžia prisijungti prie fiskalinio spausdintuvo, kuris prijungtas per COM prievadą, naudojant prigimtinę programinės įrangos tvarkyklę. Jis buvo įdiegtas ir patikrintas naudojant programinės įrangos emuliatorių, kuris posnet pateiktą Posnet Hd FV EJ fiskaliniu spausdintuvu. Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

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

    - [Spausdinti kliento informaciją](emea-pol-customer-information.md), nurodytą finansinio kvito pardavimo operacijai. Šios informacijos pavyzdys yra kliento PVM numeris.

- Dienos pabaigos išrašai (X finansiniai ir finansiniai Z ataskaitos).
- Klaidos tvarkymą, pvz., šias pasirinktis:

    - Jei galima atlikti kartojimo veiksmą, pvz., jei fiskalinis spausdintuvas neprijungtas, neparuoštas arba neatsako, spausdintuve nepakanka popieriaus arba yra popieriaus strigtis.
    - Atidėti finansinio registravimo datą.
    - Praleisti ataskaitinį registravimą arba pažymėti operaciją kaip užregistruotą ir įtraukti informacijos kodus, kad būtų fiksuojama trikties priežastis ir papildoma informacija.
    - Patikrinkite fiskalinio spausdintuvo pasiekiamumą prieš atidarę naują pardavimo operaciją arba kai pardavimo operacija baigiama.

### <a name="gift-cards"></a>Dovanų kortelės

Fiskalinio spausdintuvo integravimo pavyzdys vykdo šias taisykles, susijusias su dovanų kortelėmis:

- Pašalinti pardavimo eilutes, susijusias su dovanų kortelės *išdavimo ir įtraukti į* *dovanų kortelės operacijas* iš finansinio kvito.
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

- Fiskalinis spausdintuvas palaiko tik scenarijus, kuriuose PVM įtraukiamas į kainą. Todėl parduotuvių **ir klientų parinktis** Kaina su PVM turi **būti** nustatyta kaip Taip.
- Kasdienės ataskaitos (X finansinis ir finansinis Z) spausdinamos naudojant įdėtosios pamainos *ataskaitos* formatą.
- Brūkšninio kodo spausdinimas ant finansinių kvitų laikomas galimu pritaikymu, **nes ši funkcija nepalaikoma įdėtųjų formatų ir gali būti įdiegta tik naudojant pritaikomą superformatinę** ataskaitą.
- Fiskalinis spausdintuvas nepalaiko įvairių operacijų. **EKA funkcijų šablonuose turi būti nustatyta** Parinkties Uždrausti maišymą ir **grąžinimą** viena kvito pasirinktis Kaip Taip.

## <a name="set-up-fiscal-integration-for-poland"></a>Nustatyti finansų integravimą Lenkijai

Lenkijos fiskalinio spausdintuvo integravimo pavyzdys pagrįstas finansinio [integravimo funkcija](fiscal-integration-for-retail-channel.md) ir yra "Retail SDK" dalis. Pavyzdys yra sprendimų **saugyklos src\\ FiscalIntegration\\ Posnet**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke (pvz., [išleidimo /9.33 pavyzdys](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas, kuris yra "Commerce Runtime (CRT) plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti "Retail SDK", [žr. "Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)[" architektūrą ir nepriklausomo pakavimo SDK sukūrimo pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją programavimo virtualiojoje kompiuteryje (VM) ciklo Microsoft Dynamics tarnybose (LCS). Daugiau informacijos ieškokite Lenkijos ([senesnės programos) fiskalinio spausdintuvo integravimo pavyzdžio diegimo rekomendacijose](emea-pol-fpi-sample-sdk.md).
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

Atlikite finansinio integravimo nustatymo veiksmus, kaip aprašyta ["Commerce" kanalų finansinio integravimo nustatymas](setting-up-fiscal-integration-for-retail-channel.md).

1. [Nustatykite finansinio registravimo procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taip pat pasižymėkite finansinio registravimo proceso parametrus, bvz., šio [fiskalinio spausdintuvo integravimo pavyzdį](#set-up-the-registration-process).
1. [Nustatyti klaidų tvarkymo parametrus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [EKA nustatykite finansų X/Z ataskaitas](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Įgalinkite neautomatinį atidėtos finansinio registravimo vykdymą](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Sukonfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nustatyti registravimo procesą

Norėdami įjungti registravimo procesą, atlikite šiuos veiksmus norėdami nustatyti "Commerce Headquarters". Daugiau informacijos rasite "Commerce [" kanalų finansinio integravimo nustatykite](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųsti finansinio dokumento teikėjo ir fiskalinio jungties konfigūracijos failus:

    1. Atidaryti sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK/programos versiją (pvz., **[paleidimas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atidaryti **src \> FiscalIntegration \> Posnet**.
    1. Atsisiųskite finansinio dokumento teikėjo konfigūracijos failą svetainėje CommerceRuntime **DocumentProvider.PosnetSample Configuration DocumentProviderPosnetSample.xml (pvz \>., failas, \> skirtas release/9.33 \>).**[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/CommerceRuntime/DocumentProvider.PosnetSample/Configuration/DocumentProviderPosnetSample.xml)
    1. Atsisiųskite "Fiscal Connector" konfigūracijos **failą, kurį reikia atsisiųsti iš HardwareStationVzviceSample \>\> Configuration \> ConnectorPosnetThermalFVEJ.xml (pvz** ., [leidimo / 9.33 failas](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/HardwareStation/ThermalDeviceSample/Configuration/ConnectorPosnetThermalFVEJ.xml)).

    > [!WARNING]
    > Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją LCS programuotojo VM. Šio fiskalinio integravimo pavyzdžio konfigūracijos failai yra toliau esančiuuose "Retail" SDK, esantis LCS programuotojo VM, aplankuose:
    >
    > - **Iždo dokumentų teikėjo konfigūracijos failas:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extension.DocumentProvider.PosnetSample\\ Configuration\\ DocumentProviderPosnetSample.xml
    > - **Iždo jungties konfigūracijos failas:** RetailSdk\\ SampleExtensions\\ HardwareStation\\ extension.Posnet.PjDeviceSample\\ Configuration\\ ConnectorPosnetThermalFVEJ.xml
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

- **Pridėtinės vertės mokesčio (PVM)** tarifų konvertavimas – mokesčio procento verčių, kurios nustatytos PVM kodams, susiejimas su iždo dokumentų spausdintuvu – konkrečiai PVM tarifams. Čia yra numatytasis susiejimas:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Pirmasis kiekvienos poros komponentas rodo PVM tarifo numerį, kuris sukonfigūruotas fiskalinio spausdintuvo. Antrasis komponentas rodo atitinkamą PVM tarifą. Daugiau informacijos apie fiskalinio spausdintuvo PVM tarifo konfigūraciją ieškokite POSNET tvarkyklės dokumentuose.

- **Mokėjimo priemonės tipo** susiejimas – mokėjimo būdų, kurie sukonfigūruoti parduotuvei ir mokėjimo formoms, kurias palaiko fiskalinis spausdintuvas, susiejimas. Čia yra numatytasis susiejimas:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Pirmasis kiekvienos poros komponentas atitinka parduotuvei nustatytą mokėjimo būdą. Antrasis komponentas nurodo atitinkamą mokėjimo formą, kurią palaiko fiskalinis spausdintuvas. Daugiau informacijos apie mokėjimo formas, kurias palaiko fiskalinis spausdintuvas, ieškokite POSNET tvarkyklės dokumentuose. Turite modifikuoti pavyzdžio susiejimą pagal mokėjimo metodus, kurie sukonfigūruoti jūsų programoje.

#### <a name="fiscal-connector-settings"></a>Iždo jungties parametrai

Šie parametrai įtraukiami į fiskalinės jungties konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdys:

- **Jungimosi** eilutė – eilutė, aprašantys išsamią ryšio su įrenginiu informaciją tvarkyklės palaikomu formatu. Daugiau informacijos ieškokite POSNET tvarkyklės dokumentuose.
- **Datos ir laiko sinchronizavimas** – reikšmė, nurodanti, ar spausdintuvo data ir laikas turi būti sinchronizuoti su prijungta aparatūros stotyje.
- **Įrenginio skirtasis** laikas milisekunde, per kurį vairuotojas lauks atsakymo iš įrenginio. Daugiau informacijos ieškokite POSNET tvarkyklės dokumentuose.

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

> [!WARNING]
> Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją LCS programuotojo VM. Daugiau informacijos ieškokite Lenkijos ([senesnės programos) fiskalinio spausdintuvo integravimo pavyzdžio diegimo rekomendacijose](emea-pol-fpi-sample-sdk.md).
>
> Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

#### <a name="set-up-the-development-environment"></a>Programavimo aplinkos kūrimas

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba atsisiųskite [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr. ["Download Retail SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite finansinio spausdintuvo integravimo sprendimą **Dynamics365Commerce.Solutions\\ FiscalIntegration\\ Posnet Posnet.sln\\** ir sukurkite jį.
1. Įdiegti CRT plėtinius:

    1. Rasti plėtinio CRT diegimo programą:

        - **"Commerce Scale Unit":** **aplanke Posnet\\ ScaleUnit\\ ScaleUnit.Posnet.Installer\\ talpyklos\\ debug\\ net461** **raskite ScaleUnit.Posnet.Installer diegimo** kūrėjas.
        - **Vietinė CRT "Modern POS":** **aplanke Posnet\\ ModernPOS ModernPOS.Posnet.Installer\\\\\\ talpyklos debug\\ net461** **raskite ModernPOS.Posnet.Installer diegimo** kūrėjas.

    1. Paleiskite CRT plėtinio diegimo programą iš komandų eilutės:

        - **"Commerce Scale Unit":**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **" CRT Modern POS" vieta:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Įdiekite aparatūros stoties plėtinius:

    1. Posnet **HardwareStation\\ HardwareStation.PosnetThermalFFiscalPrinter.Installer\\\\ talpyklos debug\\ net461 \\** aplanke raskite HardwareStation.PosnetThermalFVFiscalPrinter.Installer diegimo **priemonę.**
    1. Paleiskite plėtinio diegimo programą iš komandų eilutės:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Norėdami sugeneruoti [ir](fiscal-integration-sample-build-pipeline.md) paleisti debesies skalės vienetą ir savitarnos diegiant finansinio integravimo pavyzdžio paketus, atlikite nurodytus veiksmus. Posnet build-pipeline.yml **šablono JAML** **failą galima rasti YAML_Files \\** saugyklos pardavimo [Dynamics 365 Commerce galimybių aplanke.](https://github.com/microsoft/Dynamics365Commerce.Solutions)

## <a name="design-of-extensions"></a>Plėtinių dizainas

Lenkijos fiskalinio spausdintuvo integravimo pavyzdys pagrįstas finansinio [integravimo funkcija](fiscal-integration-for-retail-channel.md) ir yra "Retail SDK" dalis. Pavyzdys yra sprendimų **saugyklos src\\ FiscalIntegration\\ Posnet**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke (pvz., [išleidimo /9.33 pavyzdys](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)). Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas CRT, kuris yra plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti "Retail SDK", [žr. "Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md)[" architektūrą ir nepriklausomo pakavimo SDK sukūrimo pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl naujo nepriklausomo pakavimo [ir plėtinio modelio](../dev-itpro/build-pipeline.md) apribojimų, šiuo metu jo negalima naudoti šiame finansinio integravimo pavyzdyje. Turite naudoti ankstesnę "Retail SDK" versiją LCS programuotojo VM. Daugiau informacijos ieškokite Lenkijos ([senesnės programos) fiskalinio spausdintuvo integravimo pavyzdžio diegimo rekomendacijose](emea-pol-fpi-sample-sdk.md). Naujas nepriklausomas pakavimo ir plėtinio modelis, skirtas finansinio integravimo pavyzdžiui, planuojamas vėlesnėms versijoms.

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti konkretaus spausdintuvo dokumentus ir tvarkyti atsakymus iš fiskalinio spausdintuvo. Šis plėtinys sugeneruoja poSNET 19-3678 specifikacijos apibrėžtą "JavaScript Object Notation" (JSON) formato spausdintuvui specialių komandų rinkinį.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

**DocumentProviderPosnetProtocol užklausos** apdorojimo programa yra įvesties taškas, per kurį užklausa generuoja dokumentus iš fiskalinio spausdintuvo.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su jungties dokumento teikėjo pavadinimu, kuris nurodytas "Commerce Headquarters".

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje yra informacijos apie tai, koks dokumentas turėtų būti sugeneruotas. Grąžinamas spausdintuvui konkretus dokumentas, kuris turi būti užregistruotas fiskaliniu spausdintuvu.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa pateikia įvykių, prie kurių bus užsiprenumeruoti, sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas ir Z ataskaitos spausdinimas.

#### <a name="configuration"></a>Konfigūracija

Finansinio dokumento teikėjo konfigūracijos failas yra src **FiscalIntegration\\ Posnet\\ CommerceRuntime\\ DocumentProvider.PosnetSample konfigūracijos DocumentProviderPosnetSample.xml \\\\\\ sprendimų saugykloje.**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Failo paskirtis – įgalinti finansinio dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, paskirtis yra palaikyti ryšį su fiskaliniu spausdintuvu. Šis plėtinys išk prašo POSNET tvarkyklės funkcijų pateikti komandas, kurias plėtinys CRT sugeneruoja fiskaliniu spausdintuvu. Ji taip pat tvarko įrenginio klaidas.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

FiscalPrinterHandler **užklausos** apdorojimo programa yra įvesties taškas, skirtas tvarkyti užklausą į fiskalinį per įrenginį.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su "Commerce Headquarters" nurodytu finansinio jungties pavadinimu.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus spausdintuvams ir grąžina atsakymą iš fiskalinio spausdintuvo.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama įrenginio sveikatos patikrai atlikti.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama spausdintuvui inicijuoti.

#### <a name="configuration"></a>Konfigūracija

Fiskalinės jungties **konfigūracijos failas yra src\\ FiscalIntegration\\ Posnet\\ HardwareStationVzviceSample\\\\ Configuration\\ ConnectorPosnetThermalFVEJ.xml**[Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykloje. Failo paskirtis – įgalinti finansinių jungčių parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
