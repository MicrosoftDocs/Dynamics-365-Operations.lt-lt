---
title: Austrijos fiskalinės registracijos tarnybos integravimo pavyzdžio diegimo gairės (senstelėjęs)
description: Šioje temoje pateikiamos gairės, kaip įdiegti Fiskalinės integracijos pavyzdį Austrijai iš Microsoft Dynamics 365 Commerce "Retail" programinės įrangos kūrimo rinkinio (SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 7cb0e7b665add397b12e1a841b6a2e9565528d6d
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/19/2022
ms.locfileid: "8613941"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-austria-legacy"></a>Austrijos fiskalinės registracijos tarnybos integravimo pavyzdžio diegimo gairės (senstelėjęs)

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiamos gairės, kaip įdiegti fiskalinės registracijos paslaugos integravimo pavyzdį Austrijai iš Microsoft Dynamics 365 Commerce mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) kūrėjo virtualioje mašinoje Microsoft Dynamics (VM) "Lifecycle Services" (LCS). Daugiau informacijos apie šią fiskalinės integracijos imtį ieškokite [Fiscal Registration Service Integration Sample for Austria](emea-aut-fi-sample.md). 

Austrijos fiskalinės integracijos pavyzdys yra mažmeninės prekybos SDK dalis. Informacijos, kaip įdiegti ir naudoti SDK, ieškokite Mažmeninės prekybos programinės [įrangos kūrimo rinkinio (SDK) architektūroje](../dev-itpro/retail-sdk/retail-sdk-overview.md). Fiskalinės integracijos imtį sudaro "Commerce" vykdyklės (CRT), aparatūros stoties ir pardavimo vietos (EKA) plėtiniai. Norėdami paleisti šį pavyzdį, turite modifikuoti ir kurti CRT, Aparatūros stotis ir EKA projektus. Rekomenduojame naudoti nesumoduliuotą "Retail SDK", kad būtų atlikti šioje temoje aprašyti pakeitimai. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz.Azure DevOps, kurioje dar nėra pakeistų failų.

## <a name="development-environment"></a>Programavimo aplinka

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

### <a name="enable-commerce-runtime-extensions"></a>Įgalinti "Commerce" vykdyklės plėtinius

Plėtinio CRT komponentai įtraukiami į pavyzdžius CRT. Norėdami baigti šias procedūras, **dalyje RetailSdkSampleExtensionsCommerceRuntime** **atidarykite sprendimą CommerceRuntimeSamples.sln \\\\**.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample komponentas

1. Suraskite **Runtime.Extensions.DocumentProvider.EFRSample** projektą ir sukurkite jį.
2. **Aplanke Runtime.Extensions.DocumentProvider.EFRSamplebinDebug\\\\** **raskite rinkinio failą Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll.**
3. Nukopijuokite surinkimo failą į plėtinių CRT aplanką:

    - **"Commerce Scale Unit:" kopijuokite** failą **\\ į talpyklos\\ aplanką**, esantį informacinių interneto paslaugų (IIS) "Commerce Scale Unit" vietoje.
    - **" CRT Modern POS" vieta: kopijuokite** failą į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris skirtas CRT:

    - **"Commerce Scale Unit:**" failo vardas yra commerceruntime.ext.config **,** jis yra IIS "Commerce Scale Unit" vietos aplanke binext **\\.**
    - **" CRT Modern POS" vietinė:** **failo vardas yra CommerceRuntime.MPOSOffline.Ext.config**, jis priklauso vietinio kliento CRT brokerio vietai.

5. Užregistruokite CRT pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR komponentas

1. Raskite **Runtime.Extensions.DocumentProvider.DataModelEFR** projektą ir sukurkite jį.
2. **Aplanke Runtime.Extensions.DocumentProvider.DataModelEFRbinDebug\\\\** **raskite Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** surinkimo failą.
3. Nukopijuokite surinkimo failą į plėtinių CRT aplanką:

    - **"Commerce Scale Unit:"** kopijuokite failą į **\\ talpyklosext\\** aplanką, esantį IIS komercijos skalės vieneto svetainės vietoje.
    - **" CRT Modern POS" vieta: kopijuokite** failą į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris skirtas CRT:

    - **"Commerce Scale Unit:**" failo vardas yra commerceruntime.ext.config **,** jis yra IIS "Commerce Scale Unit" vietos aplanke binext **\\.**
    - **" CRT Modern POS" vietinė:** **failo vardas yra CommerceRuntime.MPOSOffline.Ext.config**, jis priklauso vietinio kliento CRT brokerio vietai.

5. Užregistruokite CRT pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Plėtinio konfigūracijos failas

1. Rasti plėtinio konfigūracijos failą, kuris skirtas CRT:

    - **"Commerce Scale Unit:**" failo vardas yra commerceruntime.ext.config **,** jis yra IIS "Commerce Scale Unit" vietos aplanke binext **\\.**
    - **" CRT Modern POS" vietinė:** **failo vardas yra CommerceRuntime.MPOSOffline.Ext.config**, jis priklauso vietinio kliento CRT brokerio vietai.

2. Užregistruokite CRT pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Įjungti "Fiscal Connector" plėtinius

"Hardware" arba EKA kasos [aparate galite](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) įjungti " [Fiscal Connector" plėtinius](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>Įjungti aparatūros stoties plėtinius

Aparatūros stoties plėtinio komponentai įtraukiami į aparatūros stoties pavyzdžius. Norėdami atlikti šias procedūras, dalyje RetailSdkSampleExtensionsHardwareStation atidarykite sprendimą HardwareStationSamples.sln **·** **.\\\\**

##### <a name="efrsample-component"></a>EFRSample komponentas

1. Raskite **HardwareStation.Extension.EFRSample** projektą ir sukurkite jį.
2. **Aplanke Extension.EFRSamplebinDebug\\\\** raskite šiuos surinkimo failus:

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

EKA plėtinio pavyzdys yra **sprendimų saugyklos aplanke srcFiscalIntegrationPosFiscalConnectorSample\\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).

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

### <a name="enable-modern-pos-extension-components"></a>Įgalinti šiuolaikinius EKA plėtinio komponentus

1. **Atidarykite "ModernPOS.sln** sprendimą dalyje **RetailSdkPOS\\** ir įsitikinkite, kad jį galima sukompiliuoti be klaidų. Be to, įsitikinkite, kad naudodami komandą Visual Studio Vykdyti galite paleisti "Modern POS **"**.

    > [!NOTE]
    > Šiuolaikinis EKA neturi būti pritaikytas. Turite įgalinti vartotojo abonemento valdymo tarnybą (UAC) ir, jei reikia, pašalinti anksčiau įdiegtus modernios EKA egzempliorius.

2. Įgalinkite plėtinių įkėlimą pridėdami šias eilutes faile **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Norėdami gauti daugiau informacijos ir pavyzdžių, rodančių, kaip įtraukti šaltinio kodo aplankus ir įgalinti plėtinių įkėlimą, readme.md **žr**.

3. Atkurkite sprendimą.
4. Derintuve paleiskite "Modern POS" ir išbandykite funkcionalumą.

### <a name="enable-cloud-pos-extension-components"></a>Įgalinti "Cloud POS" plėtinio komponentus

1. Atidarykite **"CloudPOS.sln** sprendimą dalyje **RetailSdkPOS\\** ir įsitikinkite, kad jį galima kompiliuoti be klaidų.
2. Įgalinkite plėtinių įkėlimą pridėdami šias eilutes faile **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Norėdami gauti daugiau informacijos ir pavyzdžių, rodančių, kaip įtraukti šaltinio kodo aplankus ir įgalinti plėtinių įkėlimą, readme.md **žr**.

3. Atkurkite sprendimą.
4. Paleiskite sprendimą naudodami komandą **Vykdyti** ir atlikdami "Retail SDK" vadove nurodytus veiksmus.

## <a name="production-environment"></a>Gamybos aplinka

Ankstesnė procedūra įgalina plėtinius, kurie yra finansinių registracijų tarnybos integravimo pavyzdžio komponentai. Be to, turite atlikti šiuos veiksmus, jei norite kurti diegtinas pakuotes, kuriose yra "Commerce" komponentai, ir taikyti šias pakuotes gamybos aplinkoje.

1. Aplanke RetailSdkAssets **\\ pakuotės konfigūracijos failuose atlikite** šiuos pakeitimus:

    - Konfigūracijos failuose **commerceruntime.ext.config** **ir CommerceRuntime.MPOSOffline.Ext.config** įtraukite **šias eilutes į sudėties** skyrių.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - Konfigūracijos faile **HardwareStation.Extension.config** įtraukite šią eilutę į skyriaus **sudėtį**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Atlikite šiuos pakeitimus **pritaikymo.settings** paketo tinkinimo konfigūravimo faile, esančiame aplanke **BuildTools**:

    - Įtraukite šias eilutes, kad įtraukdami CRT plėtinius į diegiamus paketus.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Įtraukite šią eilutę, kad į diegtimus paketus įtraukumėte "Hardware" stoties plėtinį.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Paleiskite MSBuild komandinę Visual Studio eilutę dėl paslaugų programos ir **paleiskite msbuild** "Retail" SDK aplanke, kad sukurtumėte diegiamus paketus.
4. Taikykite paketus naudodami LCS arba rankiniu būdu. Daugiau informacijos ieškokite Create [deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Užpildykite visas būtinas nustatymo užduotis, aprašytas " [Set up Commerce for Austria"](emea-aut-fi-sample.md#set-up-commerce-for-austria).

## <a name="design-of-extensions"></a>Plėtinių dizainas

Austrijos fiskalinės registracijos tarnybos integravimo pavyzdys pagrįstas fiskalinės [integracijos funkcija](fiscal-integration-for-retail-channel.md). Daugiau informacijos apie finansinio integravimo sprendimo dizainą ieškokite finansinio [integravimo pavyzdžio dizaino apžvalgoje](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti paslaugai bvz., dokumentus ir tvarkyti atsakymus iš fiskalinių registracijų tarnybos.

Plėtinys CRT yra **Runtime.Extensions.DocumentProvider.EFRSample**.

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

Konfigūracijos failai yra plėtinio **projekto aplanke Konfigūracija**:

- **DocumentProviderFiscalEFRSampleAustria** – fiskaliniams dokumentams.
- **DocumentProviderNonFiscalEFRSampleAustria** – nefinansiniams dokumentams.

Šių failų paskirtis – įgalinti dokumentų teikėjo parametrus konfigūruoti iš "Commerce" būstinės. Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais. Pridedamas šis parametras:

- PVM tarifų susiejimas

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Fiskalinės jungties plėtinio tikslas yra bendrauti su fiskalinės registracijos tarnyba. Aparatūros stoties plėtinys pavadintas **HardwareStation.Extension.EFRSample**. Ji naudoja HTTP arba HTTPS protokolą dokumentams, kuriuos plėtinys CRT sugeneruoja finansinio registravimo tarnybai, pateikti. Jis taip pat tvarko atsakymus, gautus iš finansinio registravimo tarnybos.

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
- **Skirtasis** laikas – laikas milisekundėmis, per milisekundes, per kurį vairuotojas lauks atsakymo iš fiskalinės registracijos tarnybos.

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
