---
title: Italijos fiskalinio spausdintuvo integravimo pavyzdžio diegimo gairės (senstelėjęs)
description: Šioje temoje pateikiamos gairės, kaip įdiegti fiskalinio spausdintuvo integravimo pavyzdį Italijai iš Microsoft Dynamics 365 Commerce mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 617e97272fb4bd7cea0958958ae99648bb847b56
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/19/2022
ms.locfileid: "8614074"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Italijos fiskalinio spausdintuvo integravimo pavyzdžio diegimo gairės (senstelėjęs)

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiamos gairės, kaip įdiegti fiskalinio spausdintuvo integravimo pavyzdį Italijai iš Microsoft Dynamics 365 Commerce mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) kūrėjo virtualioje mašinoje Microsoft Dynamics (VM) "Lifecycle Services" (LCS). Daugiau informacijos apie šią fiskalinės integracijos imtį ieškokite [Italijos fiskalinio spausdintuvo integravimo pavyzdyje](emea-ita-fpi-sample.md). 

Italijos fiskalinės integracijos pavyzdys yra Mažmeninės prekybos SDK dalis. Informacijos, kaip įdiegti ir naudoti SDK, ieškokite Mažmeninės prekybos programinės [įrangos kūrimo rinkinio (SDK) architektūroje](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šį pavyzdį sudaro "Commerce Runtime (CRT) ir Hardware" stoties plėtiniai. Norėdami vykdyti šį pavyzdį, turite modifikuoti ir sukurti " CRT Hardware" stoties projektus. Rekomenduojame naudoti nesumoduliuotą "Retail SDK", kad būtų atlikti šioje temoje aprašyti pakeitimai. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz.Azure DevOps, kurioje dar nėra pakeistų failų.

## <a name="development-environment"></a>Programavimo aplinka

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

### <a name="commerce-runtime-extension-components"></a>"Commerce" vykdyklės plėtinio komponentai

Plėtinio CRT komponentai įtraukti į mažmeninės prekybos SDK. Norėdami baigti šias procedūras, **dalyje RetailSdkSampleExtensionsCommerceRuntime** **atidarykite sprendimą CommerceRuntimeSamples.sln \\\\**.

1. **Raskite projektą Runtime.Extensions.DocumentProvider.EpsonFP90IIIIIISample** ir sukurkite jį.
2. Aplanke **Extensions.DocumentProvider.EpsonFP90IIIIISamplebinDebug\\\\** raskite **aplanką Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIIISample.dll** rinkinio failą.
3. Nukopijuokite surinkimo failą į plėtinių CRT aplanką:

    - **"Commerce Scale Unit:" kopijuokite** failą **\\ į talpyklos\\ aplanką**, esantį informacinių interneto paslaugų (IIS) "Commerce Scale Unit" vietoje.
    - **" CRT Modern POS" vieta: kopijuokite** failą į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris skirtas CRT:

    - **"Commerce Scale Unit:**" failo vardas yra commerceruntime.ext.config **,** jis yra IIS "Commerce Scale Unit" vietos aplanke binext **\\.**
    - **" CRT Modern POS" vietinė:** **failo vardas yra CommerceRuntime.MPOSOffline.Ext.config**, jis priklauso vietinio kliento CRT brokerio vietai.

5. Užregistruokite CRT pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Iš naujo paleiskite "Commerce Scale Unit":

    - **Komercijos skalės vienetas:** iš naujo paleiskite "Commerce Scale Unit" svetainę iš IIS tvarkytuvo.
    - **Kliento brokeris:** Užbaikite **dllhost.exe** procesą užduočių tvarkytuve, tada iš naujo paleiskite "Modern POS".

### <a name="hardware-station-extension-components"></a>Aparatūros stoties plėtinio komponentai

Aparatūros stoties plėtinio komponentai įtraukiami į mažmeninės prekybos SDK. Norėdami atlikti šias procedūras, dalyje RetailSdkSampleExtensionsHardwareStation atidarykite sprendimą HardwareStationSamples.sln **·** **.\\\\**

1. **Raskite projektą HardwareStation.Extensions.EpsonFP90IIIIFiscalDeviceSample** ir sukurkite jį.
2. Aplanke **Extensions.EpsonFP90IIIFiscalDeviceSamplebinDebug\\\\** raskite **aplanką Contoso.Commerce.HardwareStation.EpsonFP90IIIIFiscalDeviceSample.dll** surinkimo failą.
3. Kopijuoti surinkimo failą į įdiegtą aparatūros stoties įrenginį:

    - **Nuotolinė aparatūros stotis:** nukopijuokite failą **į dėžės** aplanką, esantį IIS aparatūros stoties svetainės vietoje.
    - **Vietinė aparatūros stotis:** nukopijuokite failą į "Modern POS" kliento brokerio vietą.

4. Raskite aparatūros stoties plėtinių konfigūracijos failą. Failas pavadintas **HardwareStation.Extension.config**:

    - **Nuotolinė aparatūros stotis:** failas yra IIS aparatūros stoties vietos vietoje.
    - **Vietinė aparatūros stotis:** failas yra "Modern POS" kliento brokerio vietoje.

5. Įtraukite šį skyrių į **konfigūracijos failo sudėties** skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Iš naujo paleiskite aparatūros stoties tarnybą:

    - **Nuotolinė aparatūros stotis:** iš naujo paleiskite aparatūros stoties svetainę iš IIS tvarkytuvo.
    - **Vietinė aparatūros stotis:** užduočių tvarkytuve uždarykite **dllhost.exe** procesą ir iš naujo paleiskite "Modern POS".

## <a name="production-environment"></a>Gamybos aplinka

Norėdami sukurti diegiamus paketus, kuriuose yra "Commerce" komponentų, ir taikyti tuos paketus gamybos aplinkoje, atlikite šiuos veiksmus.

1. Atlikite veiksmus, aprašytus anksčiau šioje temoje esančiame [skyriuje Kūrimo aplinka](#development-environment).
2. Aplanke RetailSdkAssets **\\ pakuotės konfigūracijos failuose atlikite** šiuos pakeitimus:

    1. **Konfigūracijos failuose commerceruntime.ext.config** ir **CommerceRuntime.MPOSOffline.Ext.config** į kompozicijos **skyrių įtraukite** šią eilutę.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    1. Konfigūracijos faile **HardwareStation.Extension.config** įtraukite šią eilutę į skyriaus **sudėtį**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Atlikite šiuos pakeitimus **pritaikymo.settings** paketo tinkinimo konfigūravimo faile, esančiame aplanke **BuildTools**:

    1. Įtraukite šią eilutę, kad plėtinys CRT būtų įtrauktas į diegiamus paketus.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    1. Įtraukite šią eilutę, kad į diegtimus paketus įtraukumėte "Hardware" stoties plėtinį.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Aplanke PackagesSharedPackagingProjectComponents **faile Sdk.ModernPos.Shared.csproj** faile **atlikite \_ šiuos keitimus**, kad įtrauktumėte Italijos išteklių failus į diegiamus paketus:

    1. Įtraukite sekciją **ItemGroup**, kurioje yra mazgai, nukreipiantys į norimų vertimų išteklių failus. Įsitikinkite, kad nurodote teisingas vardų sritis ir vardų pavyzdžius. Toliau pateiktame pavyzdyje pridedami it **ir** it-CH **lokalių išteklių mazgai**.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Skyriuje Tikslinis **pavadinimas="CopyPackageFiles"** įtraukite po vieną eilutę kiekvienai lokalei, kaip parodyta toliau pateiktame pavyzdyje.

        ```xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it-CH" SkipUnchangedFiles="true" />
        ```

5. Aplanke PackagesSharedPackagingProjectComponents esančiame **faile** Sdk.RetailServerSetup.proj **atlikite šiuos keitimus\_, kad į diegiamus paketus įtrauktumėte Italijos išteklių** failus:

    1. Įtraukite sekciją **ItemGroup**, kurioje yra mazgai, nukreipiantys į norimų vertimų išteklių failus. Įsitikinkite, kad nurodote teisingas vardų sritis ir vardų pavyzdžius. Toliau pateiktame pavyzdyje pridedami it **ir** it-CH **lokalių išteklių mazgai**.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Skyriuje Tikslinis **pavadinimas="CopyPackageFiles"** įtraukite po vieną eilutę kiekvienai lokalei, kaip parodyta toliau pateiktame pavyzdyje.

        ``` xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it-CH" SkipUnchangedFiles="true" />
        ```

6. Paleiskite "MSBuild" komandinę eilutę, skirtą Visual Studio naudingumui, tada paleiskite **"msbuild** " aplanke "Retail SDK", kad sukurtumėte diegiamus paketus.
7. Taikykite paketus naudodami LCS arba rankiniu būdu. Daugiau informacijos ieškokite Create [deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Plėtinių dizainas

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra finansinių dokumentų teikėjas, tikslas yra generuoti spausdintuvui būdingus dokumentus ir tvarkyti atsakymus iš fiskalinio spausdintuvo.

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
