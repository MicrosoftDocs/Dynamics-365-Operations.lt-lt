---
title: Čekijos Respublikai (iš senesnių) skirtas finansinio registravimo tarnybos integravimo pavyzdžio diegimo rekomendacijos
description: Šiame straipsnyje pateikiamos Čekijos Respublika finansinio integravimo pavyzdžio diegimo iš "Retail" programinės įrangos Microsoft Dynamics 365 Commerce kūrimo rinkinio (SDK) rekomendacijos.
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 7406a6443f851fcfa9757deed57c108ba7b6e069
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473910"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-the-czech-republic-legacy"></a>Čekijos Respublikai (iš senesnių) skirtas finansinio registravimo tarnybos integravimo pavyzdžio diegimo rekomendacijos

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Šiame straipsnyje nurodytus nurodymus turite naudoti tik tada, jei naudojate Microsoft Dynamics 365 Commerce 10.0.28 arba ankstesnę versiją. Kaip ir "Commerce" 10.0.29 versiją Čekijos Respublika finansinio registravimo tarnybos integravimo pavyzdį galima rasti "Commerce" programinės įrangos kūrimo rinkinyje (SDK). Daugiau informacijos rasite Kanalo komponentų [konfigūravimas](./emea-cze-fi-sample.md#configure-channel-components).

Šiame straipsnyje pateikiamos Dynamics 365 Commerce Gairės, kaip įdiegti Čekijos Respublikai skirtą finansinio registravimo tarnybos integravimo pavyzdį iš "Retail SDK", kuris yra programuotojo virtualiojoje mašinos (VM) Microsoft Dynamics ciklo tarnybose (LCS). Daugiau informacijos apie šį finansinio integravimo pavyzdį ieškokite Čekijos [Respublika finansinio registravimo tarnybos integravimo pavyzdyje](emea-cze-fi-sample.md). 

Čekijos Respublikai skirtas finansinio integravimo pavyzdys yra mažmeninės prekybos SDK dalis. Informacijos, kaip įdiegti ir naudoti SDK, ieškokite Mažmeninės prekybos programinės [įrangos kūrimo rinkinio (SDK) architektūroje](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šį pavyzdį sudaro "Commerce Runtime (CRT) ir Hardware" stoties plėtiniai. Norėdami vykdyti šį pavyzdį, turite modifikuoti ir sukurti " CRT Hardware" stoties projektus. Rekomenduojame naudoti nesumoduliuotą "Retail SDK", kad būtų atlikti šiame straipsnyje aprašyti pakeitimai. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz.Azure DevOps, kurioje dar nėra pakeistų failų.

## <a name="development-environment"></a>Programavimo aplinka

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

### <a name="enable-commerce-runtime-extensions"></a>Įgalinti "Commerce" vykdyklės plėtinius

Plėtinio CRT komponentai įtraukiami į pavyzdžius CRT. Norėdami atlikti šias procedūras, dalyje RetailSdk SampleExtensions CommerceRuntime **atidarykite sprendimą CommerceRuntimeSamples.sln** **\\.\\**

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample komponentas

1. Suraskite **Runtime.Extensions.DocumentProvider.EFRSample** projektą ir sukurkite jį.
2. Aplanke Runtime.Extensions.DocumentProvider.EFRSample talpyklos debug **\\ raskite failą Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll\\.** **·**
3. Nukopijuokite surinkimo failą į plėtinių CRT aplanką:

    - **"Commerce Scale Unit:" kopijuokite** failą **\\\\ į talpyklos iš** išorės aplanką, esantį informacinių interneto paslaugų (IIS) "Commerce Scale Unit" vietoje.
    - **" CRT Modern POS" vieta: kopijuokite** failą į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris skirtas CRT:

    - **"Commerce Scale Unit:** failas **yra pavadintas commerceruntime.ext.config**, **\\** jis yra talpyklos išorinio aplanko IIS "Commerce Scale Unit" vietoje.
    - **" CRT Modern POS" vietinė:** **failo vardas yra CommerceRuntime.MPOSOffline.Ext.config**, jis priklauso vietinio kliento CRT brokerio vietai.

5. Užregistruokite CRT pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR komponentas

1. Raskite **Runtime.Extensions.DocumentProvider.DataModelEFR** projektą ir sukurkite jį.
2. Aplanke Runtime.Extensions.DocumentProvider.DataModelEFR bin Debug **\\ raskite Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll\\ surinkimo failą.** **·**
3. Nukopijuokite surinkimo failą į plėtinių CRT aplanką:

    - **"Commerce Scale Unit:"** kopijuokite failą į **\\ talpyklos\\ išorės** aplanką, esantį IIS "Commerce Scale Unit" svetainės vietoje.
    - **" CRT Modern POS" vieta: kopijuokite** failą į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris skirtas CRT:

    - **"Commerce Scale Unit:** failas **yra pavadintas commerceruntime.ext.config**, **\\** jis yra talpyklos išorinio aplanko IIS "Commerce Scale Unit" vietoje.
    - **" CRT Modern POS" vietinė:** **failo vardas yra CommerceRuntime.MPOSOffline.Ext.config**, jis priklauso vietinio kliento CRT brokerio vietai.

5. Užregistruokite CRT pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Plėtinio konfigūracijos failas

1. Rasti plėtinio konfigūracijos failą, kuris skirtas CRT:

    - **"Commerce Scale Unit:** failas **yra pavadintas commerceruntime.ext.config**, **\\** jis yra talpyklos išorinio aplanko IIS "Commerce Scale Unit" vietoje.
    - **" CRT Modern POS" vietinė:** **failo vardas yra CommerceRuntime.MPOSOffline.Ext.config**, jis priklauso vietinio kliento CRT brokerio vietai.

2. Užregistruokite CRT pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Įjungti "Fiscal Connector" plėtinius

"Hardware" arba EKA kasos [aparate galite](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) įjungti " [Fiscal Connector" plėtinius](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

### <a name="enable-hardware-station-extensions"></a>Įjungti aparatūros stoties plėtinius

Aparatūros stoties plėtinio komponentai įtraukiami į aparatūros stoties pavyzdžius. Norėdami atlikti šias procedūras, dalyje RetailSdk SampleExtensions HardwareStation atidarykite sprendimą **HardwareStationSamples.sln** **\\.\\**

#### <a name="efrsample-component"></a>EFRSample komponentas

1. Raskite **HardwareStation.Extension.EFRSample** projektą ir sukurkite jį.
2. **Aplanke Extension.EFRSample talpyklos\\\\ derinimas** raskite šiuos surinkimo failus:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Nukopijuokite surinkimo failus į "Hardware" stoties plėtinių aplanką:

    - **Bendrai naudojama aparatūros stotis:** kopijuokite failus į **talpyklos** aplanką, esantį IIS aparatūros stoties svetainės vietoje.
    - **Skirtoji "Modern POS" aparatūros stotis:** kopijuokite failus į "Modern POS" kliento brokerio vietą.

4. Raskite aparatūros stoties plėtinių plėtinio konfigūracijos failą. Failo vardas yra **HardwareStation.Extension.config**.

    - **Bendrai naudojama aparatūros stotis:** failas yra IIS aparatūros stoties svetainės vietoje.
    - **Skirtoji "Modern POS" aparatūros stotis:** failas yra "Modern POS" kliento brokerio vietoje.

5. Įtraukite šią eilutę į **konfigūracijos** failo sudėties skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>Įgalinti EKA plėtinius

EKA plėtinio pavyzdys yra **sprendimų saugyklos src\\ FiscalIntegration\\ PosFiscalConnectorSample**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke.

Norėdami naudoti EKA plėtinio pavyzdį senesnime SDK, atlikite šiuos veiksmus.

1. Nukopijuokite **aplanką EKA.Extension** į senesnio **SDK** aplanką EKA plėtiniai (pvz., `C:\RetailSDK\src\POS\Extensions`).
1. Pervardykite **EKA.Plėtinio** aplanko **PosFiscalConnector kopiją**.
1. Iš aplanko PosFiscalConnector **pašalinkite** šiuos aplankus ir failus:

    - talpykla
    - Duomenų tarnyba
    - devDependencies priklausomybė
    - Bibliotekos
    - Obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. Atidarykite **cloudPos.sln arba** **ModernPos.sln** sprendimą.
1. **Pos.Extensions projekte** įtraukite **posFiscalConnector** aplanką.
1. Atidarykite **plėtinio.json** failą ir įtraukite **PosFiscalConnector plėtinį**.
1. Sukurkite SDK.

### <a name="production-environment"></a>Gamybos aplinka

Ankstesnė procedūra įgalina plėtinius, kurie yra finansinių registracijų tarnybos integravimo pavyzdžio komponentai. Be to, turite atlikti šiuos veiksmus, jei norite kurti diegtinas pakuotes, kuriose yra "Commerce" komponentai, ir taikyti šias pakuotes gamybos aplinkoje.

1. Atlikite šiuos paketo konfigūracijos failų keitimus aplanke **RetailSdk\\ Assets**.

    - Konfigūracijos failuose **commerceruntime.ext.config** **ir CommerceRuntime.MPOSOffline.Ext.config** įtraukite **šias eilutes į sudėties** skyrių.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
        ```

    - Konfigūracijos faile **HardwareStation.Extension.config** įtraukite šią eilutę į skyriaus **sudėtį**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

2. Atlikite šiuos pakeitimus **customization.settings paketo** pritaikymo konfigūracijos faile, aplanke **BuildTools**.

    - Įtraukite šias eilutes, kad įtraukdami CRT plėtinius į diegiamus paketus.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Įtraukite šią eilutę, kad į diegtimus paketus įtraukumėte "Hardware" stoties plėtinį.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. Paleiskite MSBuild komandinę Visual Studio eilutę dėl paslaugų programos ir **paleiskite msbuild** "Retail" SDK aplanke, kad sukurtumėte diegiamus paketus.
4. Taikykite paketus naudodami LCS arba rankiniu būdu. Daugiau informacijos ieškokite Create [deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Užbaikite visas reikalingas nustatymo užduotis, aprašytas [Čekijos Komercijos nustatyme](emea-cze-fi-sample.md#set-up-commerce-for-the-czech-republic).

## <a name="design-of-extensions"></a>Plėtinių dizainas

Čekijos finansinio registravimo tarnybos integravimo pavyzdys yra paremtas finansinio [integravimo funkcionalumu](fiscal-integration-for-retail-channel.md). Daugiau informacijos apie finansinio integravimo sprendimo dizainą ieškokite finansinio [integravimo pavyzdžio dizaino apžvalgoje](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti paslaugai bvz., dokumentus ir tvarkyti atsakymus iš fiskalinių registracijų tarnybos.

Plėtinys CRT yra **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

Yra viena DocumentProviderEFRFiscalCZE **užklausų** apdorojimo programa, skirta dokumentų tiekėjui. Jis naudojamas norint generuoti finansinio registravimo tarnybos finansinius dokumentus.

Ši apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su jungties dokumento teikėjo pavadinimu, kuris nurodytas "Commerce Headquarters".

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje yra informacijos apie tai, koks dokumentas turėtų būti sugeneruotas. Grąžinamas paslaugai konkretus dokumentas, kuris turi būti užregistruotas finansinio registravimo tarnybose.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa pateikia įvykių, prie kurių bus užsiprenumeruoti, sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, kliento sąskaitos depozitai ir klientų užsakymų depozitai.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – ši užklausa grąžina atsakymą iš finansinių registracijų tarnybos. Šis atsakymas yra eilutėmis išrašomas į formą, kad būtų galima įrašyti.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos **failas DocumentProviderFiscalEFRSampleCzech** **yra** plėtinio projekto konfigūracijos aplanke. Šio failo paskirtis – įgalinti dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais. Pridedami šie parametrai:

- PVM tarifų susiejimas
- Numatytoji PVM grupė
- Depozito PVM grupė

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, paskirtis yra palaikyti ryšį su finansinių registracijų tarnyba.

Aparatūros stoties plėtinys pavadintas **HardwareStation.Extension.EFRSample**. Ji naudoja HTTP arba HTTPS protokolą dokumentams, kuriuos plėtinys CRT sugeneruoja finansinio registravimo tarnybai, pateikti. Jis taip pat tvarko atsakymus, gautus iš finansinio registravimo tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

**EFRHandler užklausos** apdorojimo programa yra iždo registracijos tarnybos užklausų tvarkymo įvesties taškas.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su "Commerce Headquarters" nurodytu finansinio jungties pavadinimu.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus į finansinio registravimo tarnybą ir grąžina atsakymą iš jos.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama norint patikrinti finansinių registracijų tarnybos sveikumą.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama norint inicijuoti finansinių registracijų tarnybą.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra plėtinio **projekto** konfigūracijos aplanke. Failo paskirtis – įgalinti finansinio jungties parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais. Pridedami šie parametrai:

- **Galinio punkto** adresas – finansinio registravimo tarnybos URL.
- **Skirtasis** laikas milisekundiais, kurį jungtis lauks atsakymo iš fiskalinių registracijų tarnybos.

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
