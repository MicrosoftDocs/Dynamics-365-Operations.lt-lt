---
title: Čekijos Respublikai (iš senesnių) skirtas finansinio registravimo tarnybos integravimo pavyzdžio diegimo rekomendacijos
description: Šioje temoje pateikiamos Gairės, kaip iš "Retail" programinės įrangos kūrimo rinkinio (SDK) įdiegti Čekijos Microsoft Dynamics 365 Commerce Respublikai skirtą finansinio integravimo pavyzdį.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 18126f53dc314eca3e874e914346b860d7138109
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7945019"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-the-czech-republic-legacy"></a>Čekijos Respublikai (iš senesnių) skirtas finansinio registravimo tarnybos integravimo pavyzdžio diegimo rekomendacijos

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiamos Gairės, kaip čekijos Respublikai įdiegti finansinio registravimo tarnybos integravimo pavyzdį iš "Retail" programinės įrangos kūrimo rinkinio (SDK) programavimo virtualiojoje kompiuteryje (VM) ciklo tarnybose Microsoft Dynamics 365 Commerce Microsoft Dynamics (LCS). Daugiau informacijos apie šį finansinio integravimo pavyzdį ieškokite [Čekijos Respublika finansinio registravimo tarnybos integravimo pavyzdyje](emea-cze-fi-sample.md). 

Čekijos Respublikai skirtas finansinio integravimo pavyzdys yra mažmeninės prekybos SDK dalis. Informacijos, kaip įdiegti ir naudoti SDK, ieškokite Mažmeninės prekybos programinės [įrangos kūrimo rinkinio (SDK) architektūroje](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šį pavyzdį sudaro "Commerce Runtime ( ) ir CRT Hardware" stoties plėtiniai. Norėdami vykdyti šį pavyzdį, turite modifikuoti ir sukurti CRT "Hardware" stoties projektus. Rekomenduojame naudoti nesumoduliuotą "Retail SDK", kad būtų atlikti šioje temoje aprašyti pakeitimai. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz., Azure DevOps kurioje dar nėra pakeistų failų.

## <a name="development-environment"></a>Talpinimo aplinka

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

### <a name="enable-commerce-runtime-extensions"></a>Įgalinti "Commerce" vykdyklės plėtinius

Plėtinio CRT komponentai įtraukiami į CRT pavyzdžius. Norėdami atlikti šias procedūras, dalyje **·** **RetailSdk \\ SampleExtensions \\ CommerceRuntime atidarykite sprendimą CommerceRuntimeSamples.sln.**

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample komponentas

1. Suraskite **Runtime.Extensions.DocumentProvider.EFRSample** projektą ir sukurkite jį.
2. Aplanke **Runtime.Extensions.DocumentProvider.EFRSample \\ talpyklos \\ debug** raskite failą **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **"Commerce Scale Unit:" kopijuokite failą į talpyklos iš išorės aplanką, esantį informacinių interneto paslaugų** **\\\\** (IIS) "Commerce Scale Unit" vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite failą į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **"Commerce Scale Unit:** failas **yra pavadintas commerceruntime.ext.config ir jis yra talpyklos išorinio aplanko** **\\** IIS "Commerce Scale Unit" vietoje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR komponentas

1. Raskite **Runtime.Extensions.DocumentProvider.DataModelEFR** projektą ir sukurkite jį.
2. Aplanke **Runtime.Extensions.DocumentProvider.DataModelEFR \\ bin \\ Debug** raskite **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** surinkimo failą.
3. Nukopijuokite surinkimo failą į CRT plėtinių aplanką:

    - **"Commerce Scale** Unit:" kopijuokite failą į **\\ talpyklos \\ išorės** aplanką, esantį IIS "Commerce Scale Unit" svetainės vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite failą į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **"Commerce Scale Unit:** failas **yra pavadintas commerceruntime.ext.config ir jis yra talpyklos išorinio aplanko** **\\** IIS "Commerce Scale Unit" vietoje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Plėtinio konfigūracijos failas

1. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **"Commerce Scale Unit:** failas **yra pavadintas commerceruntime.ext.config ir jis yra talpyklos išorinio aplanko** **\\** IIS "Commerce Scale Unit" vietoje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

2. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
    ```

### <a name="enable-hardware-station-extensions"></a>Įjungti aparatūros stoties plėtinius

Aparatūros stoties plėtinio komponentai įtraukiami į aparatūros stoties pavyzdžius. Norėdami atlikti šias procedūras, **dalyje** **RetailSdk \\ SampleExtensions HardwareStation atidarykite sprendimą HardwareStationSamples.sln. \\**

#### <a name="efrsample-component"></a>EFRSample komponentas

1. Raskite **HardwareStation.Extension.EFRSample** projektą ir sukurkite jį.
2. Aplanke **Extension.EFRSample \\ talpyklos \\ derinimas** raskite šiuos surinkimo failus:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Nukopijuokite surinkimo failus į "Hardware" stoties plėtinių aplanką:

    - **Bendrai naudojama aparatūros** stotis: kopijuokite failus į **talpyklos** aplanką, esantį IIS aparatūros stoties svetainės vietoje.
    - **Skirtoji "Modern POS" aparatūros stotis:** kopijuokite failus į "Modern POS" kliento brokerio vietą.

4. Raskite aparatūros stoties plėtinių plėtinio konfigūracijos failą. Failo vardas yra **HardwareStation.Extension.config.**

    - **Bendrai naudojama aparatūros** stotis: failas yra IIS aparatūros stoties svetainės vietoje.
    - **Skirtoji "Modern POS" aparatūros** stotis: failas yra "Modern POS" kliento brokerio vietoje.

5. Įtraukite šią eilutę į **konfigūracijos** failo sudėties skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

### <a name="production-environment"></a>Gamybos aplinka

Ankstesnė procedūra įgalina plėtinius, kurie yra finansinių registracijų tarnybos integravimo pavyzdžio komponentai. Be to, turite atlikti šiuos veiksmus, jei norite kurti diegtinas pakuotes, kuriose yra "Commerce" komponentai, ir taikyti šias pakuotes gamybos aplinkoje.

1. Atlikite šiuos paketo konfigūracijos failų keitimus aplanke **RetailSdk \\** Assets.

    - Konfigūracijos **failuose commerceruntime.ext.config ir** **CommerceRuntime.MPOSOffline.Ext.config įtraukite šias eilutes į** **sudėties** skyrių.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
        ```

    - Konfigūracijos **faile HardwareStation.Extension.config** įtraukite šią eilutę į **skyriaus** sudėtį.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

2. Atlikite šiuos pakeitimus **customization.settings** paketo pritaikymo konfigūracijos faile, aplanke **BuildTools.**

    - Įtraukite šias eilutes, kad CRT įtraukdami plėtinius į diegiamus paketus.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Įtraukite šią eilutę, kad į diegtimus paketus įtraukumėte "Hardware" stoties plėtinį.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. Paleiskite MSBuild komandinę eilutę dėl paslaugų programos ir paleiskite Visual Studio msbuild "Retail" SDK aplanke, kad sukurtumėte **diegiamus** paketus.
4. Taikykite paketus naudodami LCS arba rankiniu būdu. Daugiau informacijos ieškokite [Create deployable](../dev-itpro/retail-sdk/retail-sdk-packaging.md) packages.
5. Užbaikite visas reikalingas nustatymo užduotis, [aprašytas Čekijos Komercijos](emea-cze-fi-sample.md#set-up-commerce-for-the-czech-republic) nustatyme.

## <a name="design-of-extensions"></a>Plėtinių dizainas

Čekijos finansinio registravimo tarnybos integravimo pavyzdys remiasi finansinio [integravimo](fiscal-integration-for-retail-channel.md) funkcija. Daugiau informacijos apie finansinio integravimo sprendimo dizainą ieškokite finansinio [integravimo pavyzdžio dizaino apžvalgoje.](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, tikslas yra generuoti konkrečios paslaugos dokumentus ir tvarkyti atsakymus iš fiskalinės registracijos tarnybos.

Plėtinys CRT yra **Runtime.Extensions.DocumentProvider.EFRSample.**

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

Yra viena **DocumentProviderEFRFiscalCZE** užklausų apdorojimo programa, skirta dokumentų tiekėjui. Jis naudojamas norint generuoti finansinio registravimo tarnybos finansinius dokumentus.

Ši apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą "Commerce" būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje pateikiama informacija apie tai, kokį dokumentą reikia generuoti. Jis grąžina su paslauga susijusius dokumentus, kurie turėtų būti užregistruoti fiskalinės registracijos tarnyboje.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, kliento sąskaitos depozitai ir klientų užsakymų depozitai.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – ši užklausa grąžina atsakymą iš fiskalinės registracijos tarnybos. Šis atsakymas serijizuotas, kad būtų galima suformuoti eilutę, kad ji būtų paruošta įrašyti.

#### <a name="configuration"></a>Konfigūravimas

**Konfigūracijos failas DocumentProviderFiscalEFRSampleCzech yra** **plėtinio** projekto konfigūracijos aplanke. Šio failo paskirtis – įgalinti dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie parametrai:

- PVM tarifų susiejimas
- Numatytoji PVM grupė
- Depozito PVM grupė

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra bendrauti su fiskalinės registracijos tarnyba.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.EFRSample**. Aparatūros stoties plėtinys naudoja HTTP protokolą dokumentams, kuriuos CRT plėtinys sugeneruoja, pateikti į fiskalinės registracijos tarnybą. Ji taip pat tvarko atsakymus, gautus iš fiskalinės registracijos tarnybos.

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

**EFRHandler** užklausų apdorojimo programa yra registracijos tarnybos užklausų tvarkymo pradinis taškas.

Apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti "Commerce" būstinėje nurodytą fiskalinės jungties pavadinimą.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus į fiskalinės registracijos tarnybą ir pateikia iš jos atsakymą.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama fiskalinės registracijos tarnybos sveikatos patikrinimui.
- **InicijuotiFiscalDeviceRequest** – ši užklausa naudojama fiskalinės registracijos tarnybai inicijuoti.

#### <a name="configuration"></a>Konfigūravimas

Konfigūracijos failas yra **plėtinio** projekto konfigūracijos aplanke. Failo paskirtis – įgalinti finansinio jungties parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie parametrai:

- **Galinio punkto** adresas – finansinio registravimo tarnybos URL.
- **Skirtasis laikas milisekundiais, kurį vairuotojas laukia atsakymo iš fiskalinių** registracijų tarnybos.
