---
title: Austrijos (senesnių) finansinio registravimo tarnybos integravimo pavyzdžio diegimo rekomendacijos
description: Šioje temoje pateikiami Austrijos finansinio integravimo pavyzdžio diegimo iš "Retail" programinės įrangos Microsoft Dynamics 365 Commerce kūrimo rinkinio (SDK) gairės.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: c038773dc7c1c475f5852f0f0272b59516140593
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944668"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-austria-legacy"></a>Austrijos (senesnių) finansinio registravimo tarnybos integravimo pavyzdžio diegimo rekomendacijos

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiami austrijos finansinio registravimo tarnybos integravimo pavyzdžio iš "Retail" programinės įrangos kūrimo rinkinio (SDK), kuris yra programuotojo virtualiojoje mašinos (VM) ciklo tarnybose Microsoft Dynamics 365 Commerce Microsoft Dynamics (LCS), gairės. Daugiau informacijos apie šį finansinio integravimo pavyzdį ieškokite [Austrijos iždo registracijos tarnybos integravimo pavyzdys](emea-aut-fi-sample.md). 

Austrijos finansinio integravimo pavyzdys yra Mažmeninės prekybos SDK dalis. Informacijos, kaip įdiegti ir naudoti SDK, ieškokite Mažmeninės prekybos programinės [įrangos kūrimo rinkinio (SDK) architektūroje](../dev-itpro/retail-sdk/retail-sdk-overview.md). Finansinio integravimo pavyzdį sudaro "Commerce runtime ( ), Hardware station ir CRT point of sale (EKA) plėtiniai. Norėdami vykdyti šį pavyzdį, turite modifikuoti ir sukurti CRT projektus, "Hardware" stotį ir EKA. Rekomenduojame naudoti nesumoduliuotą "Retail SDK", kad būtų atlikti šioje temoje aprašyti pakeitimai. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz., Azure DevOps kurioje dar nėra pakeistų failų.

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
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
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

### <a name="enable-modern-pos-extension-components"></a>Įjungti modernaus EKA plėtinio komponentus

1. Atidarykite **ModernPOS.sln sprendimą dalyje RetailSdk POS ir įsitikinkite, kad jį galima** **\\** sukompiliuoti be klaidų. Be to, įsitikinkite, kad naudodami komandą Vykdyti galėsite Visual Studio paleisti "Modern **POS".**

    > [!NOTE]
    > "Modern POS" negalima pritaikyti. Turite įgalinti vartotojo abonemento valdymo programą (UAC) ir, jei reikia, pašalinti anksčiau įdiegtus "Modern POS" egzempliorius.

2. Įjunkite plėtinius, kad juos būtų galima įkelti, įtraukdami šias eilutes į **plėtinių.json** failą.

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
    > Norėdami gauti daugiau informacijos ir pavyzdžių, kurie parodo, kaip įtraukti šaltinio kodų aplankus ir įgalinti plėtinius įkelti, žr. instrukcijas eka readme.md failo **plėtinių** projekte.

3. Perkurti sprendimą.
4. Paleiskite modernų EKA derintuve ir patikrinkite funkcijas.

### <a name="enable-cloud-pos-extension-components"></a>Įjungti "Cloud POS" plėtinio komponentus

1. Atidarykite **CloudPOS.sln sprendimą dalyje RetailSdk POS ir įsitikinkite, kad jį galima** **\\** sukompiliuoti be klaidų.
2. Įjunkite plėtinius, kad juos būtų galima įkelti, įtraukdami šias eilutes į **plėtinių.json** failą.

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
    > Norėdami gauti daugiau informacijos ir pavyzdžių, kurie parodo, kaip įtraukti šaltinio kodų aplankus ir įgalinti plėtinius įkelti, žr. instrukcijas eka readme.md failo **plėtinių** projekte.

3. Perkurti sprendimą.
4. Paleiskite sprendimą naudodami komandą **Vykdyti** ir vykdykite "Retail SDK" vadove nurodytus veiksmus.

## <a name="production-environment"></a>Gamybos aplinka

Ankstesnė procedūra įgalina plėtinius, kurie yra finansinių registracijų tarnybos integravimo pavyzdžio komponentai. Be to, turite atlikti šiuos veiksmus, jei norite kurti diegtinas pakuotes, kuriose yra "Commerce" komponentai, ir taikyti šias pakuotes gamybos aplinkoje.

1. Atlikite šiuos paketo konfigūracijos failų keitimus, nurodytus aplanke **"RetailSdk \\** Assets":

    - Konfigūracijos **failuose commerceruntime.ext.config ir** **CommerceRuntime.MPOSOffline.Ext.config įtraukite šias eilutes į** **sudėties** skyrių.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - Konfigūracijos **faile HardwareStation.Extension.config** įtraukite šią eilutę į **skyriaus** sudėtį.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Atlikite šiuos pakeitimus **customization.settings** paketo pritaikymo konfigūracijos faile, aplanke **BuildTools:**

    - Įtraukite šias eilutes, kad CRT įtraukdami plėtinius į diegiamus paketus.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Įtraukite šią eilutę, kad į diegtimus paketus įtraukumėte "Hardware" stoties plėtinį.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Paleiskite MSBuild komandinę eilutę dėl paslaugų programos ir paleiskite Visual Studio msbuild "Retail" SDK aplanke, kad sukurtumėte **diegiamus** paketus.
4. Taikykite paketus naudodami LCS arba rankiniu būdu. Daugiau informacijos ieškokite [Create deployable](../dev-itpro/retail-sdk/retail-sdk-packaging.md) packages.
5. Atlikite visas būtinas nustatymo užduotis, [aprašytas "Commerce for Austria"](emea-aut-fi-sample.md#set-up-commerce-for-austria) sąrankoje.

## <a name="design-of-extensions"></a>Plėtinių dizainas

Austrijos finansinio registravimo tarnybos integravimo pavyzdys paremtas [finansinio integravimo](fiscal-integration-for-retail-channel.md) funkcija. Daugiau informacijos apie finansinio integravimo sprendimo dizainą ieškokite finansinio [integravimo pavyzdžio dizaino apžvalgoje.](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, tikslas yra generuoti konkrečios paslaugos dokumentus ir tvarkyti atsakymus iš fiskalinės registracijos tarnybos.

Plėtinys CRT yra **Runtime.Extensions.DocumentProvider.EFRSample.**

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

Dokumentų teikėjai gali naudoti dvi užklausų apdorojimo programas:

- **DocumentProviderEFRFiscalAUT – ši apdorojimo programa naudojama finansinių** registracijų tarnybos iždo dokumentams generuoti.
- **DocumentProviderEFRNonFiscalAUT – ši apdorojimo programa naudojama** nefinansiniai dokumentams, skirti finansinio registravimo tarnybai, generuoti.

Šios apdorojimo programos perimamos iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą "Commerce" būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje pateikiama informacija apie tai, kokį dokumentą reikia generuoti. Jis grąžina su paslauga susijusius dokumentus, kurie turėtų būti užregistruoti fiskalinės registracijos tarnyboje.
- **GetNonFiscalDocumentDocumentProviderRequest – šioje užklausoje** yra informacijos apie tai, kas turėtų būti generuojamas nefinansinis dokumentas. Jis grąžina su paslauga susijusius dokumentus, kurie turėtų būti užregistruoti fiskalinės registracijos tarnyboje.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas, Z ataskaitos spausdinimas, kliento sąskaitos depozitai, klientų užsakymų depozitai, audito įvykiai ir ne pardavimo operacijos.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – ši užklausa grąžina atsakymą iš fiskalinės registracijos tarnybos. Šis atsakymas serijizuotas, kad būtų galima suformuoti eilutę, kad ji būtų paruošta įrašyti.

#### <a name="configuration"></a>Konfigūravimas

Konfigūracijos failai yra **plėtinio** projekto konfigūracijos aplanke:

- **DocumentProviderFiscalEFRSampleAustria** – skirta iždo dokumentams.
- **DocumentProviderNonFiscalEFRSampleAustria** – nefinansinių dokumentų.

Šių failų paskirtis yra įgalinti dokumento teikėjo parametrus, konfigūruojatus iš "Commerce Headquarters". Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedamas šis parametras:

- PVM tarifų susiejimas

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra bendrauti su fiskalinės registracijos tarnyba.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.EFRSample**. Ji naudoja HTTP protokolą dokumentams, kuriuos CRT sugeneruoja plėtinys, pateikti iždo registracijos tarnybai. Ji taip pat tvarko atsakymus, gautus iš fiskalinės registracijos tarnybos.

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
