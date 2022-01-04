---
title: Italijos (senesnių) fiskalinio spausdintuvo integravimo pavyzdžio diegimo rekomendacijos
description: Šioje temoje pateikiami Italijos fiskalinio spausdintuvo integravimo pavyzdžio diegimo iš "Retail" programinės įrangos Microsoft Dynamics 365 Commerce kūrimo rinkinio (SDK) gairės.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: a7b5f4f042aa5457ff33e9762f0902c5c72f5921
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944845"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Italijos (senesnių) fiskalinio spausdintuvo integravimo pavyzdžio diegimo rekomendacijos

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiami gairės, kaip įdiegti Italijos fiskalinio spausdintuvo integravimo pavyzdį iš "Retail" programinės įrangos kūrimo rinkinio (SDK), programavimo virtualiosios mašinos (VM) ciklo tarnybose Microsoft Dynamics 365 Commerce Microsoft Dynamics (LCS). Daugiau informacijos apie šį finansinio integravimo pavyzdį ieškokite Italijos [iždo dokumentų spausdintuvo integravimo pavyzdys](emea-ita-fpi-sample.md). 

Italijos finansinio integravimo pavyzdys yra mažmeninės prekybos SDK dalis. Informacijos, kaip įdiegti ir naudoti SDK, ieškokite Mažmeninės prekybos programinės [įrangos kūrimo rinkinio (SDK) architektūroje](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šį pavyzdį sudaro "Commerce Runtime ( ) ir CRT Hardware" stoties plėtiniai. Norėdami vykdyti šį pavyzdį, turite modifikuoti ir sukurti CRT "Hardware" stoties projektus. Rekomenduojame naudoti nesumoduliuotą "Retail SDK", kad būtų atlikti šioje temoje aprašyti pakeitimai. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz., Azure DevOps kurioje dar nėra pakeistų failų.

## <a name="development-environment"></a>Talpinimo aplinka

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

### <a name="commerce-runtime-extension-components"></a>"Commerce Runtime" plėtinio komponentai

Išplėstiniai CRT komponentai įtraukti į "Retail SDK". Norėdami atlikti šias procedūras, dalyje **·** **RetailSdk \\ SampleExtensions \\ CommerceRuntime atidarykite sprendimą CommerceRuntimeSamples.sln.**

1. Suraskite **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample projektą** ir sukurkite jį.
2. Aplanke **Extensions.DocumentProvider.EpsonFP90IISample \\ talpyklos \\ debug** raskite **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll** surinkimo failą.
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **"Commerce Scale Unit:" kopijuokite failą į talpyklos iš išorės aplanką, esantį informacinių interneto paslaugų** **\\\\** (IIS) "Commerce Scale Unit" vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite failą į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **"Commerce Scale Unit:** failas **yra pavadintas commerceruntime.ext.config ir jis yra talpyklos išorinio aplanko** **\\** IIS "Commerce Scale Unit" vietoje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Iš naujo paleisti "Commerce Scale Unit":

    - **"Commerce Scale Unit":** iš naujo paleiskite "Commerce Scale Unit" svetainę iš IIS tvarkytuvo.
    - **Kliento brokeris:** užbaigti **dllhost.exe** procesą užduočių tvarkytuve ir iš naujo paleisti "Modern POS".

### <a name="hardware-station-extension-components"></a>Aparatūros stoties plėtinio komponentai

Aparatūros stoties plėtinio komponentai įtraukti į "Retail SDK". Norėdami atlikti šias procedūras, **dalyje** **RetailSdk \\ SampleExtensions HardwareStation atidarykite sprendimą HardwareStationSamples.sln. \\**

1. Raskite **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** projektą ir sukurkite jį.
2. Aplanke **Extensions.EpsonFP90IIIFiscalDeviceSample \\ bin \\ Debug** raskite **Contoso.Commerce.HardwareStation.EpsonFP90IIFiscalDeviceSample.dll** surinkimo failą.
3. Nukopijuokite surinkimo failą į įdiegtą aparatūros stoties įrenginį:

    - **Nuotolinės aparatūros** stotis: kopijuokite failą į **talpyklos** aplanką, esantį IIS aparatūros stoties svetainės vietoje.
    - **Vietinės aparatūros stotis:** kopijuokite failą į "Modern POS" kliento brokerio vietą.

4. Raskite aparatūros stoties plėtinių konfigūracijos failą. Failo vardas yra **HardwareStation.Extension.config:**

    - **Nuotolinės aparatūros** stotis: failas yra IIS aparatūros stoties svetainės vietoje.
    - **Vietinė aparatūros stotis:** failas yra "Modern POS" kliento brokerio vietoje.

5. Įtraukite toliau nurodytą skyrių **į** konfigūracijos failo sudėties skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Iš naujo paleiskite aparatūros stoties tarnybą:

    - **Nuotolinės aparatūros stotis:** iš naujo paleiskite aparatūros stoties svetainę iš IIS tvarkytuvo.
    - **Vietinė aparatūros stotis:** užduočių tvarkytuve **užbaigkite dllhost.exe** procesą, tada iš naujo paleiskite "Modern POS".

## <a name="production-environment"></a>Gamybos aplinka

Norėdami kurti diegtinas paketus, kuriuose yra "Commerce" komponentai, ir taikyti šiuos paketus gamybos aplinkoje, atlikite šiuos veiksmus.

1. Atlikite veiksmus, aprašytus programavimo [aplinkos](#development-environment) skyriuje, ankstesniame šios temos skyriuje.
2. Atlikite šiuos paketo konfigūracijos failų keitimus, nurodytus aplanke **"RetailSdk \\** Assets":

    - Konfigūracijos **failuose commerceruntime.ext.config ir** **CommerceRuntime.MPOSOffline.Ext.config įtraukite šią eilutę į** **sudėties** skyrių.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    - Konfigūracijos **faile HardwareStation.Extension.config** įtraukite šią eilutę į **skyriaus** sudėtį.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Atlikite šiuos pakeitimus **customization.settings** paketo pritaikymo konfigūracijos faile, aplanke **BuildTools:**

    - Įtraukite šią eilutę, kad CRT įtraukumėte plėtinį į diegiamus paketus.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    - Įtraukite šią eilutę, kad į diegtimus paketus įtraukumėte "Hardware" stoties plėtinį.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Paleiskite MSBuild komandinę eilutę dėl paslaugų programos, tada paleiskite msbuild mažmeninės prekybos SDK aplanke, kad sukurtumėte Visual Studio **diegiamus** paketus.
5. Taikykite paketus naudodami LCS arba rankiniu būdu. Daugiau informacijos ieškokite [Create deployable](../dev-itpro/retail-sdk/retail-sdk-packaging.md) packages.

## <a name="design-of-extensions"></a>Plėtinių dizainas

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti konkretaus spausdintuvo dokumentus ir tvarkyti atsakymus iš fiskalinio spausdintuvo.

Plėtinys CRT yra **Runtime.Extensions.DocumentProvider.EpsonFP90IISample.**

Daugiau informacijos apie finansinio integravimo sprendimo dizainą rasite finansinio įrenginių finansinio [registravimo procese ir finansinio integravimo pavyzdžius.](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

DocumentProviderEpsonFP90III užklausos apdorojimo programa yra užklausos sugeneruoti dokumentus **iš** fiskalinio spausdintuvo įvesties taškas.

Apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą "Commerce" būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje pateikiama informacija apie tai, kokį dokumentą reikia generuoti. Grąžinamas spausdintuvui konkretus dokumentas, kuris turi būti užregistruotas fiskaliniu spausdintuvu.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas ir Z ataskaitos spausdinimas.

#### <a name="configuration"></a>Konfigūravimas

Konfigūracijos failas yra **plėtinio** projekto konfigūracijos aplanke. Failo paskirtis – įgalinti dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie parametrai:

- PVM kodų susiejimas
- PVM tarifų susiejimas
- Mokėjimo priemonės tipo susiejimas
- Kvito numerio brūkšninio kodo tipas
- Įmokos mokėjimo tipas

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, paskirtis yra palaikyti ryšį su fiskaliniu spausdintuvu.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample.** Šis plėtinys naudoja HTTP protokolą dokumentams, kurie CRT sugeneruoja plėtinį, pateikti iždo dokumentų spausdintuvui. Jis taip pat tvarko iš fiskalinio spausdintuvo gautus atsakymus.

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

EpsonFP90IIISample užklausos apdorojimo programa yra finansinio išorinio įrenginio **tvarkymo** užklausų įvesties taškas.

Apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti "Commerce" būstinėje nurodytą fiskalinės jungties pavadinimą.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest – ši užklausa siunčia dokumentus spausdintuvams ir grąžina atsakymą** iš fiskalinio spausdintuvo.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama įrenginio sveikatos patikrai atlikti.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama spausdintuvui inicijuoti.

#### <a name="configuration"></a>Konfigūravimas

Konfigūracijos failas yra **plėtinio** projekto konfigūracijos aplanke. Failo paskirtis – įgalinti jungties parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie parametrai:

- **Galinio punkto** adresas – spausdintuvo URL.
- **Datos ir laiko sinchronizavimas – reikšmė, nurodanti, ar spausdintuvo data ir laikas turi būti** sinchronizuoti su prijungta aparatūros stotyje.
