---
title: Švedijos (senesnių) kontrolės vieneto integravimo pavyzdžio diegimo rekomendacijos
description: Šiame straipsnyje pateikiamos Švedijos kontrolės vieneto integravimo pavyzdžio diegimo iš "Retail SDK" rekomendacijos
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: fcc35a2203641b24fe4edd2ab34f2e4d5db9bb53
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324303"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Švedijos (senesnių) kontrolės vieneto integravimo pavyzdžio diegimo rekomendacijos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiamos Švedijos valdymo vieneto integravimo pavyzdžio diegimo iš "Retail" programinės įrangos kūrimo rinkinio (SDK) programuotojo virtualiojoje kompiuteryje (VM) Microsoft Dynamics ciklo tarnybose (LCS) rekomendacijos. Daugiau informacijos apie šį finansinio integravimo pavyzdį ieškokite Švedijos [kontrolės vieneto integravimo pavyzdys](emea-swe-fi-sample.md). 

Švedijos finansinio integravimo pavyzdys yra mažmeninės prekybos SDK dalis. Informacijos, kaip įdiegti ir naudoti SDK, ieškokite Mažmeninės prekybos programinės [įrangos kūrimo rinkinio (SDK) architektūroje](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šį pavyzdį sudaro "Commerce runtime (CRT), Hardware station ir point of sale (EKA) plėtiniai. Norėdami vykdyti šį pavyzdį, turite modifikuoti ir sukurti projektus CRT, "Hardware" stotį ir EKA. Rekomenduojame naudoti nesumoduliuotą "Retail SDK", kad būtų atlikti šiame straipsnyje aprašyti pakeitimai. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz.Azure DevOps, kurioje dar nėra pakeistų failų.

## <a name="development-environment"></a>Programavimo aplinka

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

### <a name="enable-crt-extensions"></a>Įjungti CRT plėtinius

Plėtinio CRT komponentai įtraukiami į pavyzdžius CRT. Norėdami atlikti šias procedūras, dalyje RetailSdk SampleExtensions CommerceRuntime **atidarykite sprendimą CommerceRuntimeSamples.sln** **\\.\\**

#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample komponentas

1. Suraskite **Runtime.Extensions.DocumentProvider.CleanCashSample** projektą ir sukurkite jį.
2. Aplanke Runtime.Extensions.DocumentProvider.CleanCashSample talpyklos debug **\\ raskite failą Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll\\.** **·**
3. Nukopijuokite surinkimo failą į plėtinių CRT aplanką:

    - **"Commerce Scale Unit:" kopijuokite** failą **\\\\ į talpyklos iš** išorės aplanką, esantį informacinių interneto paslaugų (IIS) "Commerce Scale Unit" vietoje.
    - **" CRT Modern POS" vieta: kopijuokite** failą į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris skirtas CRT:

    - **"Commerce Scale Unit:** failas **yra pavadintas commerceruntime.ext.config**, **\\** jis yra talpyklos išorinio aplanko IIS "Commerce Scale Unit" vietoje.
    - **" CRT Modern POS" vietinė:** **failo vardas yra CommerceRuntime.MPOSOffline.Ext.config**, jis priklauso vietinio kliento CRT brokerio vietai.

5. Užregistruokite CRT pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>Plėtinio konfigūracijos failas

1. Rasti plėtinio konfigūracijos failą, kuris skirtas CRT:

    - **"Commerce Scale Unit:** failas **yra pavadintas commerceruntime.ext.config**, **\\** jis yra talpyklos išorinio aplanko IIS "Commerce Scale Unit" vietoje.
    - **" CRT Modern POS" vietinė:** **failo vardas yra CommerceRuntime.MPOSOffline.Ext.config**, jis priklauso vietinio kliento CRT brokerio vietai.

2. Užregistruokite CRT pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>Įjungti aparatūros stoties plėtinius

Aparatūros stoties plėtinio komponentai įtraukiami į aparatūros stoties pavyzdžius. Norėdami atlikti šias procedūras, dalyje RetailSdk SampleExtensions HardwareStation atidarykite sprendimą **HardwareStationSamples.sln** **\\.\\**

#### <a name="cleancash-component"></a>CleanCash komponentas

1. Raskite **HardwareStation.Extension.CleanCashSample** projektą ir sukurkite jį.
2. **Aplanke Extension.CleanCashSample\\ talpyklos\\ debug** **raskite Contoso.Commerce.HardwareStation.CleanCashSample.dll** ir **Interop.CleanCash\_ 1\_ 1.dll** surinkimo failus.
3. Nukopijuokite surinkimo failus į "Hardware" stoties plėtinių aplanką:

    - **Bendrai naudojama aparatūros stotis:** kopijuokite failus į **talpyklos** aplanką, esantį IIS aparatūros stoties svetainės vietoje.
    - **Skirtoji "Modern POS" aparatūros stotis:** kopijuokite failus į "Modern POS" kliento brokerio vietą.

4. Raskite aparatūros stoties plėtinių plėtinio konfigūracijos failą. Failo vardas yra **HardwareStation.Extension.config**.

    - **Bendrai naudojama aparatūros stotis:** failas yra IIS aparatūros stoties svetainės vietoje.
    - **Skirta "Modern POS" aparatūros stotis:** failas yra "Modern POS" kliento brokerio vietoje.

5. Įtraukite šią eilutę į **konfigūracijos** failo sudėties skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Įjungti modernaus EKA plėtinio komponentus

1. Atidarykite **ModernPOS.sln** **sprendimą dalyje RetailSdk\\ POS** ir įsitikinkite, kad jį galima sukompiliuoti be klaidų. Be to, įsitikinkite, kad naudodami komandą Vykdyti galėsite paleisti Visual Studio "**Modern** POS".

    > [!NOTE]
    > "Modern POS" negalima pritaikyti. Turite įgalinti vartotojo abonemento valdymo programą (UAC) ir, jei reikia, pašalinti anksčiau įdiegtus "Modern POS" egzempliorius.

2. Įjunkite plėtinius, kuriuos reikia įkelti į failo extensions.json įtraukdami **šias** eilutes.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Norėdami gauti daugiau informacijos ir pavyzdžių, kurie parodo, kaip įtraukti šaltinio kodų aplankus ir įgalinti plėtinius įkelti, žr. readme.md **failo EKA plėtinių projekte instrukcijas**.

3. Perkurti sprendimą.
4. Paleiskite modernų EKA derintuve ir patikrinkite funkcijas.

### <a name="enable-cloud-pos-extension-components"></a>Įjungti "Cloud POS" plėtinio komponentus

1. Atidarykite **CloudPOS.sln** **sprendimą dalyje RetailSdk\\ POS** ir įsitikinkite, kad jį galima sukompiliuoti be klaidų.
2. Įjunkite plėtinius, kuriuos reikia įkelti į failo extensions.json įtraukdami **šias** eilutes.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Norėdami gauti daugiau informacijos ir pavyzdžių, kurie parodo, kaip įtraukti šaltinio kodų aplankus ir įgalinti plėtinius įkelti, žr. readme.md **failo EKA plėtinių projekte instrukcijas**.

3. Perkurti sprendimą.
4. Paleiskite sprendimą naudodami komandą **Vykdyti** ir vykdykite "Retail SDK" vadove nurodytus veiksmus.

## <a name="production-environment"></a>Gamybos aplinka

Ankstesnė procedūra įgalina plėtinius, kurie yra kontrolinio vieneto integravimo pavyzdžio komponentai. Be to, turite atlikti šiuos veiksmus, jei norite kurti diegtinas pakuotes, kuriose yra "Commerce" komponentai, ir taikyti šias pakuotes gamybos aplinkoje.

1. Atlikite šiuos paketo konfigūracijos failų keitimus, nurodytus aplanke **"RetailSdk\\ Assets** ":

    - Konfigūracijos failuose **commerceruntime.ext.config** **ir CommerceRuntime.MPOSOffline.Ext.config** įtraukite **šias eilutes į sudėties** skyrių.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - Konfigūracijos faile **HardwareStation.Extension.config** įtraukite šią eilutę į skyriaus **sudėtį**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Atlikite šiuos pakeitimus **customization.settings** paketo pritaikymo konfigūracijos faile, aplanke **BuildTools**:

    - Įtraukite šią eilutę, kad įtraukumėte CRT plėtinius į diegiamus paketus.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Įtraukite šias eilutes į diegtinius paketus įtraukdami "Hardware" stoties plėtinį.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Įjunkite EKA plėtinį įtraukdami **toliau nurodytas eilutes į failą extensions.json**, esantį aplanke **RetailSDK\\ POS\\ plėtiniai**.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Paleiskite MSBuild komandinę Visual Studio eilutę dėl paslaugų programos ir **paleiskite msbuild** "Retail" SDK aplanke, kad sukurtumėte diegiamus paketus.
5. Taikykite paketus naudodami LCS arba rankiniu būdu. Daugiau informacijos ieškokite Create [deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. Atlikite visas būtinas nustatymo užduotis, aprašytas [nustatant integravimą su kontrolės vienetais](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>Plėtinių dizainas

### <a name="crt-extension-design"></a>CRT plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti paslaugai bvz., dokumentus ir tvarkyti kontrolinio vieneto atsakymus.

Plėtinys CRT yra **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Daugiau informacijos apie finansinio integravimo sprendimo dizainą ieškokite [finansinio įrenginių ir paslaugų finansinio integravimo procese ir finansinio integravimo pavyzdžius](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Užklausų apdorojimo programa

Yra viena **DocumentProviderCleanCash** užklausų apdorojimo programa, skirta dokumentų tiekėjui. Ši apdorojimo programa naudojama valdymo vieneto iždo dokumentams generuoti.

Ši apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su jungties dokumento teikėjo pavadinimu, kuris nurodytas "Commerce Headquarters".

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje yra informacijos apie tai, koks dokumentas turėtų būti sugeneruotas. Jis grąžina aptarnavimo dokumentą, kuris turi būti užregistruotas valdymo vienete.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa pateikia įvykių, prie kurių bus užsiprenumeruoti, sąrašą. Šiuo metu palaikomi pardavimo įvykiai ir audito įvykiai.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos **failas DocumentProviderFiscalCleanCashSample** **yra** plėtinio projekto konfigūracijos aplanke. Šio failo paskirtis – įgalinti dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais. Pridedami šie parametrai:

- PVM kodų susiejimas

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, paskirtis yra palaikyti ryšį su kontrolės vienetu.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.CleanCashSample**. Ji naudoja HTTP protokolą dokumentams, kuriuos plėtinys CRT sugeneruoja valdymo vienetui, pateikti. Jis taip pat tvarko atsakymus, gautus iš kontrolinio vieneto.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

CleanCashHandler **užklausos** apdorojimo programa yra įvesties taškas valdymo užklausoms valdymo vienetui.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su "Commerce Headquarters" nurodytu finansinio jungties pavadinimu.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus valdymo vienetui ir grąžina atsakymą iš jo.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama kontrolinio vieneto sveikatos patikrinti.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama valdymo vienetui inicijuoti.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra plėtinio **projekto** konfigūracijos aplanke. Failo paskirtis – įgalinti finansinio jungties parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais. Pridedami šie parametrai:

- **Ryšių eilutė** – valdymo vieneto ryšio nustatymai.
- **Skirtasis** laikas – laikas milisekunde, kurį vairuotojas lauks atsakymo iš valdymo vieneto.

## <a name="migrating-from-the-earlier-integration-sample"></a>Perkėlimas iš ankstesnio integravimo pavyzdžio

Jei naudojate ankstesnį EKA [integravimo su Švedijos kontrolės vienetais](retail-sdk-control-unit-sample.md) pavyzdį, gali tekti perkelti iš jo į dabartinį integravimo pavyzdį. Norėdami pasinaudoti pakeitimais ir gauti laiku atnaujinamus Švedijos funkcijų atnaujinimus, gali tekti atnaujinti, atlikti neesminius kodus ir konfigūracijos koregavimus jūsų sukurtame plėtinyje ir perkurti savo sprendimus. Sukurtoje plėtinio logije nereikia atlikti jokių pagrindinių pakeitimų. Ankstesnis integravimo pavyzdys ir jūsų tinkinimai toliau veiks, jei jūsų pusėje nebus atliekami jokie pakeitimai. Todėl galite planuoti, ruošti ir atlikti sunaudojimą jūsų aplinkai.

### <a name="migration-process"></a>Perkėlimo procesas

Perkėlimas iš ankstesnio integravimo pavyzdžio į dabartinio valdymo vieneto integravimo pavyzdį turi būti paremtas naujinimo sąvoka. Kitaip tariant, visi "Commerce Headquarters" ir "Commerce Scale Unit" komponentai turi būti atnaujinti prieš pradedant naujinti EKA ir Aparatūros stoties komponentus.

Norėdami išvengti situacijų, kai įvykis arba operacija pasirašyta du kartus (t.vz., jį pasirašė ir ankstesnis plėtinys, ir dabartinis plėtinys), arba kai įvykis arba operacija negali būti pasirašyta dėl trūkstamos konfigūracijos, rekomenduojame išjungti visus EKA ir aparatūros stoties įrenginius, kurie naudoja ankstesnį pavyzdį ir tada atnaujinkite juos vienu metu. Šį tuo pačiu metu atnaujinami galima, pvz., pagal parduotuves, atnaujinant parduotuvės funkcijų šabloną ir aparatūros stoties aparatūros šabloną.

Perkėlimo procesą turėtų sudaryti toliau pateikiami veiksmai.

1. Atnaujinkite "Commerce Headquarters" komponentus.
1. Atnaujinkite "Commerce Scale Unit" komponentus ir įgalinkite dabartinio pavyzdžio plėtinius.
1. Įsitikinkite, kad visos autonominės operacijos sinchronizuojamos iš autonominių MPOS įrenginių.
1. Išjunkite visus įrenginius, kurie naudoja ankstesnio pavyzdžio komponentus.
1. Atlikite visas būtinas nustatymo užduotis, aprašytas [nustatant integravimą su kontrolės vienetais](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. Atnaujinkite EKA ir "Hardware" stoties komponentus, išjunkite plėtinius, kurie yra ankstesnio pavyzdžio dalys, ir įgalinkite dabartinio pavyzdžio plėtinius.

    > [!NOTE]
    > Atsižvelgiant į aplinkos tipą, [...](#migration-in-a-development-environment)[daugiau](#migration-in-a-production-environment) techninės informacijos apie perkėlimo procesą galite rasti šio straipsnio skyriuje "Perkėlimas" arba "Perkėlimas" gamybos aplinkos skyriuje.

### <a name="migration-in-a-development-environment"></a>Perkėlimas programavimo aplinkoje

#### <a name="update-crt"></a>Atnaujinti CRT

1. Suraskite **Runtime.Extensions.DocumentProvider.CleanCashSample** projektą ir sukurkite jį.
2. Aplanke Runtime.Extensions.DocumentProvider.CleanCashSample talpyklos debug **\\ raskite failą Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll\\.** **·**
3. Nukopijuokite surinkimo failą į plėtinių CRT aplanką:

    - **"Commerce Scale Unit:"** kopijuokite failą į **\\ talpyklos\\ išorės** aplanką, esantį IIS "Commerce Scale Unit" svetainės vietoje.
    - **" CRT Modern POS" vieta: kopijuokite** failą į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris skirtas CRT:

    - **"Commerce Scale Unit:** failo **pavadinimas CommerceRuntime.ext.config** ir **\\** jis yra talpyklos išorinio aplanko IIS "Commerce Scale Unit" vietoje.
    - **Vietinis CRT "Modern POS":** **failo vardas yra CommerceRuntime.MPOSOffline.Ext.config**, jis yra talpyklos išoriniame aplanke, **\\** CRT kuris yra vietinio kliento brokerio vietoje.

    > [!WARNING]
    > Ne **redaguoti** failų CommerceRuntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

5. Raskite ir pašalinkite ankstesnį CRT plėtinį iš plėtinio konfigūracijos failo.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Neatimsite šio veiksmo, kol neat naujinimo visi EKA įrenginiai, kurie veikia su šiuo egzemplioriumi CRT.

6. Užregistruokite dabartinius CRT plėtinių plėtinius plėtinio konfigūracijos faile įtraukdami šias eilutes.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Naujinti aparatūros stotį

1. Raskite **HardwareStation.Extension.CleanCashSample** projektą ir sukurkite jį.
2. **Aplanke Extension.CleanCashSample\\ talpyklos\\ debug** **raskite Contoso.Commerce.HardwareStation.CleanCashSample.dll** ir **Interop.CleanCash\_ 1\_ 1.dll** surinkimo failus.
3. Nukopijuokite surinkimo failus į "Hardware" stoties plėtinių aplanką:

    - **Bendrai naudojama aparatūros stotis:** kopijuokite failus į **talpyklos** aplanką, esantį IIS aparatūros stoties svetainės vietoje.
    - **Skirtoji "Modern POS" aparatūros stotis:** kopijuokite failus į "Modern POS" kliento brokerio vietą.

4. Suraskite **HardwareStation.Extension.config plėtinio** konfigūracijos failą:

    - **Nuotolinės aparatūros stotis:** failas yra IIS aparatūros stoties svetainės vietoje.
    - **"Modern POS" vietinė aparatūros stotis:** failas yra "Modern POS" kliento brokerio vietoje.

    > [!WARNING]
    > Ne **redaguoti** failų CommerceRuntime.config ir CommerceRuntime.MPOSOffline.config. Šie failai nėra skirti jokiam tinkinimo atvejui.

5. Raskite ir pašalinkite ankstesnį "Hardware" stoties plėtinį iš plėtinio konfigūracijos failo.

    # <a name="retail-73-and-earlier"></a>["Retail 7.3" ir ankstesnės versijos](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 ir vėlesnės versijos](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Mažmeninė prekyba 10,0 ir vėliau](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Įtraukite šią eilutę į plėtinio **konfigūracijos** failo sudėties skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Atnaujinti "Modern POS"

1. Atidarykite **CloudPOS.sln sprendimą** naudojant **RetailSdk\\ POS**.
2. Išjunkite ankstesnį EKA plėtinį pašalindami šias eilutes iš **failo extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Įjunkite dabartinį EKA plėtinį įtraukdami šias eilutes į **plėtinių.json** failą.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Atnaujinti debesį EKA

1. Atidarykite **ModernPOS.sln sprendimą** naudojant **RetailSdk\\ POS**.
2. Išjunkite ankstesnį EKA plėtinį pašalindami šias eilutes iš **failo extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Įjunkite dabartinį EKA plėtinį įtraukdami šias eilutes į **plėtinių.json** failą.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Perkėlimas gamybos aplinkoje

#### <a name="update-crt"></a>Atnaujinti CRT

1. Pašalinkite ankstesnį CRT plėtinį **iš Konfigūracijos failų CommerceRuntime.ext.config** **ir CommerceRuntime.MPOSOffline.Ext.config** **, esantį aplanke RetailSdk\\ Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Neatimsite šio veiksmo, kol neat naujinimo visi EKA įrenginiai, kurie veikia su šiuo egzemplioriumi CRT.

2. CRT **Įgalinkite dabartinius plėtinius, atstatę šiuos pakeitimus Konfigūracijos failuose CommerceRuntime.ext.config** **ir CommerceRuntime.MPOSOffline.Ext.config** **, aplanke RetailSdk\\ Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. Į tinkinimo.parametrų **paketo** pritaikymo konfigūracijos **failą, esantį aplanke BuildTools**, įtraukite šią eilutę, CRT kad įtraukumėte dabartinį pavyzdžio plėtinį į visuotinai diegiamus paketus.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Naujinti aparatūros stotį

1. Pašalinkite ankstesnį aparatūros stoties plėtinį modifikuodami konfigūracijos **failą HardwareStation.Extension.config**.

    # <a name="retail-73-and-earlier"></a>["Retail 7.3" ir ankstesnės versijos](#tab/retail-7-3)

    Pašalinkite šį skyrių iš **HardwareStation.Shared.config ir** **HardwareStation.Dedicated.config** konfigūracijos failų.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 ir vėlesnės versijos](#tab/retail-7-3-1)

    Pašalinkite šį skyrių iš **konfigūracijos failo HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Mažmeninė prekyba 10,0 ir vėliau](#tab/retail-10-0)

    Pašalinkite šį skyrių iš **konfigūracijos failo HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. Įjunkite dabartinį Aparatūros stoties plėtinio **pavyzdį** įtraukdami šią eilutę į sudėties **skyrių, nurodytą faile HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. Atlikite šiuos pakeitimus **customization.settings** paketo pritaikymo konfigūracijos faile, aplanke **BuildTools**:

    - Pašalinkite šią eilutę, kad pašalintumėte ankstesnį aparatūros stoties plėtinį iš diegiamų paketų.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - Įtraukite šias eilutes į diegiamus paketus įtraukdami dabartinį aparatūros stoties plėtinį.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>Atnaujinti "Modern POS"

1. Atidarykite **CloudPOS.sln sprendimą** RetailSdk **\\ POS**.
2. Išjunkite ankstesnį EKA plėtinį:

    - **Faile tsconfig.json** įtraukite aplanką **FiscalRegisterSample** į neįtrauktinųjų sąrašą.
    - Pašalinkite šias eilutes iš failo **extensions.json, esantį** aplanke **RetailSDK\\ POS\\ plėtiniai**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Įjunkite dabartinį EKA **plėtinį įtraukdami toliau nurodytas eilutes į failą extensions.json** **, esantį aplanke RetailSDK\\ POS\\ plėtiniai**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Atnaujinti debesį EKA

1. Atidarykite **ModernPOS.sln sprendimą** naudojant **RetailSdk\\ POS**.
2. Išjunkite ankstesnį EKA plėtinį:

    - **Faile tsconfig.json** įtraukite aplanką **FiscalRegisterSample** į neįtrauktinųjų sąrašą.
    - Pašalinkite šias eilutes iš failo **extensions.json, esantį** aplanke **RetailSDK\\ POS\\ plėtiniai**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Įjunkite dabartinį EKA **plėtinį įtraukdami toliau nurodytas eilutes į failą extensions.json** **, esantį aplanke RetailSDK\\ POS\\ plėtiniai**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="create-deployable-packages"></a>Diegiamų paketų kūrimas

Paleiskite **"Retail SDK" "msbuild** ", kad sukurtumėte diegiamus paketus. Taikykite paketus naudodami LCS arba rankiniu būdu. Norėdami gauti daugiau informacijos, žr. " [Retail SDK" pakuotę](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
