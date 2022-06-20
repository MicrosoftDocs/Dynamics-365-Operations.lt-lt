---
title: Italijos (senesnių) fiskalinio spausdintuvo integravimo pavyzdžio diegimo rekomendacijos
description: Šiame straipsnyje pateikiamos Italijos fiskalinio spausdintuvo integravimo pavyzdžio diegimo iš "Retail" programinės įrangos Microsoft Dynamics 365 Commerce kūrimo rinkinio (SDK) gairės.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: bb07ca91c9e5bf1a79f672f9ba29b7bcc21688c6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848903"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Italijos (senesnių) fiskalinio spausdintuvo integravimo pavyzdžio diegimo rekomendacijos

[!include[banner](../includes/banner.md)]

Šiame straipsnyje pateikiamos Microsoft Dynamics 365 Commerce gairės, kaip įdiegti Italijos fiskalinio spausdintuvo integravimo pavyzdį iš "Retail" programinės įrangos kūrimo rinkinio (SDK), kuris yra programuotojo virtualiojoje kompiuteryje (VM) Microsoft Dynamics ciklo tarnybose (LCS). Daugiau informacijos apie šį finansinio integravimo pavyzdį ieškokite Italijos iždo [dokumentų spausdintuvo integravimo pavyzdys](emea-ita-fpi-sample.md). 

Italijos finansinio integravimo pavyzdys yra mažmeninės prekybos SDK dalis. Informacijos, kaip įdiegti ir naudoti SDK, ieškokite Mažmeninės prekybos programinės [įrangos kūrimo rinkinio (SDK) architektūroje](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šį pavyzdį sudaro "Commerce Runtime (CRT) ir Hardware" stoties plėtiniai. Norėdami vykdyti šį pavyzdį, turite modifikuoti ir sukurti " CRT Hardware" stoties projektus. Rekomenduojame naudoti nesumoduliuotą "Retail SDK", kad būtų atlikti šiame straipsnyje aprašyti pakeitimai. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz.Azure DevOps, kurioje dar nėra pakeistų failų.

## <a name="development-environment"></a>Programavimo aplinka

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

### <a name="commerce-runtime-extension-components"></a>"Commerce Runtime" plėtinio komponentai

Išplėstiniai CRT komponentai įtraukti į "Retail SDK". Norėdami atlikti šias procedūras, dalyje RetailSdk SampleExtensions CommerceRuntime **atidarykite sprendimą CommerceRuntimeSamples.sln** **\\.\\**

1. Suraskite **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample** projektą ir sukurkite jį.
2. Aplanke Extensions.DocumentProvider.EpsonFP90IISample talpyklos debug **\\ raskite Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll surinkimo\\ failą.** **·**
3. Nukopijuokite surinkimo failą į plėtinių CRT aplanką:

    - **"Commerce Scale Unit:" kopijuokite** failą **\\\\ į talpyklos iš** išorės aplanką, esantį informacinių interneto paslaugų (IIS) "Commerce Scale Unit" vietoje.
    - **" CRT Modern POS" vieta: kopijuokite** failą į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris skirtas CRT:

    - **"Commerce Scale Unit:** failas **yra pavadintas commerceruntime.ext.config**, **\\** jis yra talpyklos išorinio aplanko IIS "Commerce Scale Unit" vietoje.
    - **" CRT Modern POS" vietinė:** **failo vardas yra CommerceRuntime.MPOSOffline.Ext.config**, jis priklauso vietinio kliento CRT brokerio vietai.

5. Užregistruokite CRT pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Iš naujo paleisti "Commerce Scale Unit":

    - **"Commerce Scale Unit": iš** naujo paleiskite "Commerce Scale Unit" svetainę iš IIS tvarkytuvo.
    - **Kliento brokeris:** užbaigti **dllhost.exe procesą** užduočių tvarkytuve ir iš naujo paleisti "Modern POS".

### <a name="hardware-station-extension-components"></a>Aparatūros stoties plėtinio komponentai

Aparatūros stoties plėtinio komponentai įtraukti į "Retail SDK". Norėdami atlikti šias procedūras, dalyje RetailSdk SampleExtensions HardwareStation atidarykite sprendimą **HardwareStationSamples.sln** **\\.\\**

1. Raskite **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** projektą ir sukurkite jį.
2. **Aplanke Extensions.EpsonFP90IIIFiscalDeviceSample bin\\ Debug \\** **raskite Contoso.Commerce.HardwareStation.EpsonFP90IIFiscalDeviceSample.dll** surinkimo failą.
3. Nukopijuokite surinkimo failą į įdiegtą aparatūros stoties įrenginį:

    - **Nuotolinės aparatūros stotis:** kopijuokite failą į **talpyklos** aplanką, esantį IIS aparatūros stoties svetainės vietoje.
    - **Vietinės aparatūros stotis:** kopijuokite failą į "Modern POS" kliento brokerio vietą.

4. Raskite aparatūros stoties plėtinių konfigūracijos failą. Failo vardas yra **HardwareStation.Extension.config**:

    - **Nuotolinės aparatūros stotis:** failas yra IIS aparatūros stoties svetainės vietoje.
    - **Vietinė aparatūros stotis:** failas yra "Modern POS" kliento brokerio vietoje.

5. Įtraukite toliau nurodytą skyrių į **konfigūracijos** failo sudėties skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Iš naujo paleiskite aparatūros stoties tarnybą:

    - **Nuotolinės aparatūros stotis: iš** naujo paleiskite aparatūros stoties svetainę iš IIS tvarkytuvo.
    - **Vietinė aparatūros stotis:** užduočių tvarkytuve užbaigkite **dllhost.exe** procesą, tada iš naujo paleiskite "Modern POS".

## <a name="production-environment"></a>Gamybos aplinka

Norėdami kurti diegtinas paketus, kuriuose yra "Commerce" komponentai, ir taikyti šiuos paketus gamybos aplinkoje, atlikite šiuos veiksmus.

1. Atlikite veiksmus, kurie aprašyti anksčiau [šiame straipsnyje](#development-environment) skyriuje Programavimo aplinka.
2. Atlikite šiuos paketo konfigūracijos failų keitimus, nurodytus aplanke **"RetailSdk\\ Assets** ":

    1. Konfigūracijos failuose **commerceruntime.ext.config** **ir CommerceRuntime.MPOSOffline.Ext.config** įtraukite **šią eilutę į sudėties** skyrių.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    1. Konfigūracijos faile **HardwareStation.Extension.config** įtraukite šią eilutę į skyriaus **sudėtį**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Atlikite šiuos pakeitimus **customization.settings** paketo pritaikymo konfigūracijos faile, aplanke **BuildTools**:

    1. Įtraukite šią eilutę, kad įtraukumėte CRT plėtinį į diegiamus paketus.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    1. Įtraukite šią eilutę, kad į diegtimus paketus įtraukumėte "Hardware" stoties plėtinį.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. **Sdk.ModernPos.Shared.csproj** **aplanke Packages\_ SharedPackagingProjectComponents** atlikite šiuos pakeitimus, norėdami įtraukti Italijos išteklių failus į diegiamus paketus:

    1. Įtraukite **ItemGroup** skyrių, kuriame yra mazgai, nurodyti į išteklių failus norimams vertimams. Užtikrinkite, kad nurodysite tinkamas vardų sritis ir pavyzdžio pavadinimus. Toliau pateiktame pavyzdyje į jį įtraukti išteklių mazgai **ir** **CH** vietos.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Skyriuje Target **Name = "CopyPackageFiles"** pridėkite po vieną kiekvienos vietos eilutę, kaip parodyta toliau pateiktame pavyzdyje.

        ```xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it-CH" SkipUnchangedFiles="true" />
        ```

5. **Sdk.RetailServerSetup.proj** **faile, aplanke SharedPackagingProjectComponents\_ atlikite šiuos pakeitimus, kad į diegti norimus paketus** būtų įtraukti Italijos išteklių failai:

    1. Įtraukite **ItemGroup** skyrių, kuriame yra mazgai, nurodyti į išteklių failus norimams vertimams. Užtikrinkite, kad nurodysite tinkamas vardų sritis ir pavyzdžio pavadinimus. Toliau pateiktame pavyzdyje į jį įtraukti išteklių mazgai **ir** **CH** vietos.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Skyriuje Target **Name = "CopyPackageFiles"** pridėkite po vieną kiekvienos vietos eilutę, kaip parodyta toliau pateiktame pavyzdyje.

        ``` xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it-CH" SkipUnchangedFiles="true" />
        ```

6. Paleiskite MSBuild Visual Studio komandinę eilutę dėl paslaugų programos, **tada paleiskite msbuild** mažmeninės prekybos SDK aplanke, kad sukurtumėte diegiamus paketus.
7. Taikykite paketus naudodami LCS arba rankiniu būdu. Daugiau informacijos ieškokite Create [deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Plėtinių dizainas

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti konkretaus spausdintuvo dokumentus ir tvarkyti atsakymus iš fiskalinio spausdintuvo.

Plėtinys CRT yra **Runtime.Extensions.DocumentProvider.EpsonFP90IISample**.

Daugiau informacijos apie finansinio integravimo sprendimo dizainą ieškokite [finansinio įrenginių ir paslaugų finansinio integravimo procese ir finansinio integravimo pavyzdžius](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Užklausų apdorojimo programa

**DocumentProviderEpsonFP90III** užklausos apdorojimo programa yra užklausos sugeneruoti dokumentus iš fiskalinio spausdintuvo įvesties taškas.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su jungties dokumento teikėjo pavadinimu, kuris nurodytas "Commerce Headquarters".

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje yra informacijos apie tai, koks dokumentas turėtų būti sugeneruotas. Grąžinamas spausdintuvui konkretus dokumentas, kuris turi būti užregistruotas fiskaliniu spausdintuvu.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa pateikia įvykių, prie kurių bus užsiprenumeruoti, sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas ir Z ataskaitos spausdinimas.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra plėtinio **projekto** konfigūracijos aplanke. Failo paskirtis – įgalinti dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais. Pridedami šie parametrai:

- PVM kodų susiejimas
- PVM tarifų susiejimas
- Mokėjimo priemonės tipo susiejimas
- Kvito numerio brūkšninio kodo tipas
- Įmokos mokėjimo tipas

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, paskirtis yra palaikyti ryšį su fiskaliniu spausdintuvu.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**. Šis plėtinys naudoja HTTP protokolą dokumentams, kurie sugeneruoja CRT plėtinį, pateikti iždo dokumentų spausdintuvui. Jis taip pat tvarko iš fiskalinio spausdintuvo gautus atsakymus.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

EpsonFP90IIISample **užklausos** apdorojimo programa yra finansinio išorinio įrenginio tvarkymo užklausų įvesties taškas.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su "Commerce Headquarters" nurodytu finansinio jungties pavadinimu.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus spausdintuvams ir grąžina atsakymą iš fiskalinio spausdintuvo.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama įrenginio sveikatos patikrai atlikti.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama spausdintuvui inicijuoti.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra plėtinio **projekto** konfigūracijos aplanke. Failo paskirtis – įgalinti jungties parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais. Pridedami šie parametrai:

- **Galinio punkto** adresas – spausdintuvo URL.
- **Datos ir laiko sinchronizavimas** – reikšmė, nurodanti, ar spausdintuvo data ir laikas turi būti sinchronizuoti su prijungta aparatūros stotyje.
