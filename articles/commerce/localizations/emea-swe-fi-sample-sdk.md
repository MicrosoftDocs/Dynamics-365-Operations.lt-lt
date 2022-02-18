---
title: Švedijos valdymo bloko integravimo pavyzdžio diegimo gairės (palikimas)
description: Šioje temoje pateikiamos gairės, kaip įdiegti valdymo bloko integravimo pavyzdį Švedijoje iš mažmeninės prekybos SDK
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: b8d60f32d986dec6bb26d78ebdfe8cee3a6b688a
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077043"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Švedijos valdymo bloko integravimo pavyzdžio diegimo gairės (palikimas)

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiamos gairės, kaip įdiegti valdymo bloko integravimo pavyzdį Švedijoje iš mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) kūrėjo virtualioje mašinoje (VM).Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS). Daugiau informacijos apie šį fiskalinės integracijos pavyzdį žr [Valdymo bloko integravimo pavyzdys Švedijai](emea-swe-fi-sample.md). 

Švedijos fiskalinės integracijos pavyzdys yra mažmeninės prekybos SDK dalis. Norėdami gauti informacijos apie tai, kaip įdiegti ir naudoti SDK, žr [Mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šį pavyzdį sudaro „Commerce“ vykdymo laiko plėtiniai (CRT), Aparatinės įrangos stotis ir pardavimo vieta (POS). Norėdami paleisti šį pavyzdį, turite modifikuoti ir sukurti CRT, Aparatinės įrangos stotis ir POS projektai. Rekomenduojame naudoti nepakeistą mažmeninės prekybos SDK, kad atliktumėte šioje temoje aprašytus pakeitimus. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz Azure DevOps kur dar nepakeisti jokie failai.

## <a name="development-environment"></a>Talpinimo aplinka

Atlikite šiuos veiksmus, kad nustatytumėte kūrimo aplinką, kad galėtumėte išbandyti ir išplėsti pavyzdį.

### <a name="enable-crt-extensions"></a>Įgalinti CRT plėtiniai

The CRT pratęsimo komponentai yra įtraukti į CRT pavyzdžiai. Norėdami užbaigti toliau nurodytas procedūras, atidarykite **CommerceRuntimeSamples.sln** sprendimas pagal **RetailSdk\\ Extensions pavyzdys\\ CommerceRuntime**.

#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample komponentas

1. Surask **Runtime.Extensions.DocumentProvider.CleanCashSample** projektą ir jį pastatyti.
2. Viduje konors **Runtime.Extensions.DocumentProvider.CleanCashSample\\ šiukšliadėžė\\ Derinimas** aplanką, suraskite **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** surinkimo failas.
3. Nukopijuokite surinkimo failą į CRT plėtinių aplankas:

    - **Prekybos masto vienetas:** Nukopijuokite failą į **\\ šiukšliadėžė\\ ext** aplanką, esantį interneto informacijos paslaugų (IIS) komercijos masto vieneto svetainėje.
    - **Vietinis CRT Šiuolaikinėje POS:** Nukopijuokite failą į **\\ ext** aplanką pagal vietinį CRT kliento brokerio vieta.

4. Raskite plėtinio konfigūracijos failą CRT:

    - **Prekybos masto vienetas:** Failas pavadintas **commerceruntime.ext.config**, ir jis yra **šiukšliadėžė\\ ext** aplanką, esantį IIS komercijos masto vieneto svetainės vietoje.
    - **Vietinis CRT Šiuolaikinėje POS:** Failas pavadintas **CommerceRuntime.MPOSOffline.Ext.config**, ir jis priklauso vietiniam CRT kliento brokerio vieta.

5. Užregistruokite CRT pakeisti plėtinio konfigūracijos failą.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>Plėtinio konfigūracijos failas

1. Raskite plėtinio konfigūracijos failą CRT:

    - **Prekybos masto vienetas:** Failas pavadintas **commerceruntime.ext.config**, ir jis yra **šiukšliadėžė\\ ext** aplanką, esantį IIS komercijos masto vieneto svetainės vietoje.
    - **Vietinis CRT Šiuolaikinėje POS:** Failas pavadintas **CommerceRuntime.MPOSOffline.Ext.config**, ir jis priklauso vietiniam CRT kliento brokerio vieta.

2. Užregistruokite CRT pakeisti plėtinio konfigūracijos failą.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>Įgalinti aparatinės įrangos stoties plėtinius

Aparatūros stoties plėtinio komponentai yra įtraukti į aparatinės įrangos stoties pavyzdžius. Norėdami užbaigti toliau nurodytas procedūras, atidarykite **HardwareStationSamples.sln** sprendimas pagal **RetailSdk\\ Extensions pavyzdys\\ HardwareStation**.

#### <a name="cleancash-component"></a>CleanCash komponentas

1. Surask **HardwareStation.Extension.CleanCashSample** projektą ir jį pastatyti.
2. Viduje konors **Extension.CleanCashSample\\ šiukšliadėžė\\ Derinimas** aplanką, suraskite **Contoso.Commerce.HardwareStation.CleanCashSample.dll** ir **Interop.CleanCash\_ 1\_ 1.dll** surinkimo failai.
3. Nukopijuokite surinkimo failus į aplanką Hardware station extensions:

    - **Bendrinama aparatinės įrangos stotis:** Nukopijuokite failus į **šiukšliadėžė** aplanką, esantį IIS aparatinės įrangos stoties vietoje.
    - **Speciali aparatinės įrangos stotis šiuolaikinėje POS:** Nukopijuokite failus į Modern POS kliento tarpininko vietą.

4. Raskite aparatinės įrangos stoties plėtinių plėtinio konfigūracijos failą. Failas pavadintas **HardwareStation.Extension.config**.

    - **Bendrinama aparatinės įrangos stotis:** Failas yra IIS aparatinės įrangos stoties vietoje.
    - **Speciali aparatinės įrangos stotis šiuolaikinėje POS:** Failas yra modernaus POS kliento tarpininko vietoje.

5. Pridėkite šią eilutę prie **kompozicija** konfigūracijos failo skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Įgalinti Šiuolaikinius POS plėtinių komponentus

1. Atidaryk **ModernPOS.sln** sprendimas pagal **RetailSdk\\ POS**, ir įsitikinkite, kad jį galima sukompiliuoti be klaidų. Be to, įsitikinkite, kad galite paleisti Modern POS iš Visual Studio naudojant **Bėk** komandą.

    > [!NOTE]
    > Šiuolaikinės POS neturi būti pritaikytos. Turite įjungti vartotojo abonemento valdymą (UAC) ir, jei reikia, pašalinti anksčiau įdiegtus Modern POS egzempliorius.

2. Įgalinkite plėtinius, kuriuos reikia įkelti, įtraukdami šias eilutes **plėtiniai.json** failą.

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
    > Norėdami gauti daugiau informacijos ir pavyzdžių, kaip įtraukti šaltinio kodo aplankus ir įgalinti plėtinius, žr. instrukcijas readme.md faile **Poz.Plėtiniai** projektą.

3. Atkurkite sprendimą.
4. Debugeryje paleiskite Modern POS ir išbandykite funkcionalumą.

### <a name="enable-cloud-pos-extension-components"></a>Įgalinti „Cloud POS“ plėtinio komponentus

1. Atidaryk **CloudPOS.sln** sprendimas pagal **RetailSdk\\ POS**, ir įsitikinkite, kad jį galima sukompiliuoti be klaidų.
2. Įgalinkite plėtinius, kuriuos reikia įkelti, įtraukdami šias eilutes **plėtiniai.json** failą.

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
    > Norėdami gauti daugiau informacijos ir pavyzdžių, kaip įtraukti šaltinio kodo aplankus ir įgalinti plėtinius, žr. instrukcijas readme.md faile **Poz.Plėtiniai** projektą.

3. Atkurkite sprendimą.
4. Paleiskite sprendimą naudodami **Bėk** komandą ir atlikite mažmeninės prekybos SDK vadove nurodytus veiksmus.

## <a name="production-environment"></a>Gamybos aplinka

Ankstesnė procedūra įgalina plėtinius, kurie yra valdymo bloko integravimo pavyzdžio komponentai. Be to, turite atlikti šiuos veiksmus, kad sukurtumėte diegiamus paketus, kuriuose yra „Commerce“ komponentų, ir pritaikytumėte tuos paketus gamybos aplinkoje.

1. Atlikite toliau nurodytus paketo konfigūracijos failų pakeitimus **RetailSdk\\ Turtas** aplankas:

    - Viduje konors **commerceruntime.ext.config** ir **CommerceRuntime.MPOSOffline.Ext.config** konfigūracijos failus, pridėkite šias eilutes prie **kompozicija** skyrius.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - Viduje konors **HardwareStation.Extension.config** konfigūracijos failą, pridėkite šią eilutę prie **kompozicija** skyrius.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Atlikite šiuos pakeitimus **Customization.settings** paketo tinkinimo konfigūracijos failą, esantį **BuildTools** aplankas:

    - Pridėkite šią eilutę, kad įtrauktumėte CRT plėtinius diegiamuose paketuose.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Pridėkite šias eilutes, kad įtrauktumėte aparatūros stoties plėtinį į diegiamus paketus.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Įgalinkite POS plėtinį įtraukdami šias eilutes **plėtiniai.json** failą pagal **Mažmeninė SDK\\ POS\\ Plėtiniai** aplanką.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Paleiskite MSBuild komandų eilutę, skirtą Visual Studio naudingumas, ir paleiskite **msbuild** mažmeninės prekybos SDK aplanke, kad sukurtumėte diegiamus paketus.
5. Taikykite pakuotes per LCS arba rankiniu būdu. Daugiau informacijos žr [Sukurkite dislokuojamus paketus](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. Atlikite visas reikalingas sąrankos užduotis, kurios aprašytos [Integracijos su valdymo blokais nustatymas](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>Prailginimų dizainas

### <a name="crt-extension-design"></a>CRT pratęsimo dizainas

Plėtinio, kuris yra fiskalinių dokumentų teikėjas, tikslas yra generuoti su paslauga susijusius dokumentus ir tvarkyti valdymo bloko atsakymus.

The CRT pratęsimas yra **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Daugiau informacijos apie fiskalinės integracijos sprendimo dizainą žr [Fiskalinės registracijos procesas ir fiskalinės integracijos pavyzdžiai fiskaliniams įrenginiams ir paslaugoms](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Užklausų tvarkytojas

Yra vienas **DocumentProviderCleanCash** dokumentų teikėjo užklausų tvarkytojas. Šis tvarkytuvas naudojamas valdymo bloko fiskaliniams dokumentams generuoti.

Šis tvarkytuvas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Valdiklio pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – Šioje užklausoje pateikiama informacija apie tai, koks dokumentas turi būti sugeneruotas. Jis grąžina konkrečiai paslaugai skirtą dokumentą, kuris turi būti užregistruotas valdymo bloke.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi pardavimo ir audito renginiai.

#### <a name="configuration"></a>Konfigūracija

The **DocumentProviderFiscalCleanCashSample** konfigūracijos failas yra **Konfigūracija** plėtinio projekto aplanką. Šio failo tikslas – įgalinti dokumentų teikėjo nustatymus, kurie būtų konfigūruojami iš „Commerce“ būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie nustatymai:

- PVM kodų susiejimas

### <a name="hardware-station-extension-design"></a>Techninės įrangos stoties išplėtimo projektavimas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra susisiekti su valdymo bloku.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.CleanCashSample**. Jis naudoja HTTP protokolą, kad pateiktų dokumentus, kuriuos CRT plėtinys generuoja valdymo bloką. Ji taip pat tvarko atsakymus, gautus iš valdymo bloko.

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **CleanCashHandler** užklausų tvarkytojas yra įvesties taškas, skirtas tvarkyti užklausas į valdymo bloką.

Prižiūrėtojas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Droviklio pavadinimas turi atitikti fiskalinės jungties pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – Ši užklausa siunčia dokumentus į valdymo bloką ir grąžina iš jo atsakymą.
- **IsReadyFiscalDeviceRequest** – Ši užklausa naudojama valdymo bloko sveikatos patikrinimui.
- **InitializeFiscalDeviceRequest** – Ši užklausa naudojama valdymo blokui inicijuoti.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra **Konfigūracija** plėtinio projekto aplanką. Failo tikslas – įgalinti fiskalinės jungties nustatymus, kuriuos būtų galima konfigūruoti „Commerce“ būstinėje. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie nustatymai:

- **Ryšių eilutė** – Valdymo bloko prijungimo nustatymai.
- **Laikas baigėsi** – Laikas milisekundėmis, per kurį vairuotojas lauks atsakymo iš valdymo bloko.

## <a name="migrating-from-the-earlier-integration-sample"></a>Perkeliama iš ankstesnio integravimo pavyzdžio

Jei naudojate ankstesnį [pavyzdys POS integravimui su valdymo blokais Švedijai](retail-sdk-control-unit-sample.md), gali tekti pereiti iš jo į dabartinį integravimo pavyzdį. Jei norite pritaikyti pakeitimą ir laiku gauti Švedijos funkcijų naujinimus, gali tekti naujovinti, atlikti nedidelius kodo ir konfigūracijos koregavimus sukurtuose plėtiniuose ir iš naujo sukurti sprendimus. Jokių didelių jūsų sukurtos plėtinio logikos pakeitimų nereikia. Ankstesnis integravimo pavyzdys ir jūsų tinkinimai veiks ir toliau, jei nebus atlikta jokių pakeitimų. Todėl galite planuoti, pasiruošti ir pasirūpinti savo aplinka.

### <a name="migration-process"></a>Migracijos procesas

Perėjimas nuo ankstesnio integravimo pavyzdžio į dabartinį valdymo bloko integravimo pavyzdį turėtų būti pagrįstas laipsniško atnaujinimo koncepcija. Kitaip tariant, visi „Commerce“ būstinės ir „Commerce Scale Unit“ komponentai jau turėtų būti atnaujinti prieš pradedant atnaujinti POS ir aparatinės įrangos stoties komponentus.

Kad išvengtumėte situacijos, kai įvykis arba operacija pasirašoma du kartus (ty jį pasirašo ir ankstesnis plėtinys, ir dabartinis plėtinys), arba kai įvykio ar operacijos negalima pasirašyti dėl trūkstamos konfigūracijos, rekomenduojame išjungiate visus POS ir aparatūros stočių įrenginius, kurie naudoja ankstesnį pavyzdį, ir atnaujinate juos vienu metu. Šį vienalaikį atnaujinimą galima atlikti, pavyzdžiui, kiekvienoje parduotuvėje, atnaujinant parduotuvės funkcionalumo profilį ir Aparatinės įrangos stoties techninės įrangos profilį.

Perkėlimo procesą turėtų sudaryti šie žingsniai.

1. Atnaujinkite „Commerce“ būstinės komponentus.
1. Atnaujinkite „Commerce Scale Unit“ komponentus ir įgalinkite dabartinio pavyzdžio plėtinius.
1. Įsitikinkite, kad visos neprisijungus vykdomos operacijos yra sinchronizuojamos iš MPOS įrenginių, kuriuose įgalinta neprisijungus.
1. Išjunkite visus įrenginius, kuriuose naudojami ankstesnio pavyzdžio komponentai.
1. Atlikite visas reikalingas sąrankos užduotis, kurios aprašytos [Integracijos su valdymo blokais nustatymas](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. Atnaujinkite POS ir aparatinės įrangos stoties komponentus, išjunkite plėtinius, kurie yra ankstesnio pavyzdžio dalys, ir įgalinkite dabartinio pavyzdžio plėtinius.

    > [!NOTE]
    > Atsižvelgiant į aplinkos tipą, daugiau techninės informacijos apie perkėlimo procesą galite rasti bet kuriame iš [Migracija vystymosi aplinkoje](#migration-in-a-development-environment) skyrių arba [Migracija gamybos aplinkoje](#migration-in-a-production-environment) šios temos skyrių.

### <a name="migration-in-a-development-environment"></a>Migracija vystymosi aplinkoje

#### <a name="update-crt"></a>Atnaujinti CRT

1. Surask **Runtime.Extensions.DocumentProvider.CleanCashSample** projektą ir jį pastatyti.
2. Viduje konors **Runtime.Extensions.DocumentProvider.CleanCashSample\\ šiukšliadėžė\\ Derinimas** aplanką, suraskite **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** surinkimo failas.
3. Nukopijuokite surinkimo failą į CRT plėtinių aplankas:

    - **Prekybos masto vienetas:** Nukopijuokite failą į **\\ šiukšliadėžė\\ ext** aplanką, esantį IIS komercijos masto vieneto svetainės vietoje.
    - **Vietinis CRT Šiuolaikinėje POS:** Nukopijuokite failą į **\\ ext** aplanką pagal vietinį CRT kliento brokerio vieta.

4. Raskite plėtinio konfigūracijos failą CRT:

    - **Prekybos masto vienetas:** Failas pavadintas **CommerceRuntime.ext.config**, ir jis yra **šiukšliadėžė\\ ext** aplanką, esantį IIS komercijos masto vieneto svetainės vietoje.
    - **Vietinis CRT Šiuolaikinėje POS:** Failas pavadintas **CommerceRuntime.MPOSOffline.Ext.config**, ir jis yra **šiukšliadėžė\\ išorinis** aplanką pagal vietinį CRT kliento brokerio vieta.

    > [!WARNING]
    > Daryk **ne** redaguoti CommerceRuntime.config ir CommerceRuntime.MPOSOffline.config failus. Šie failai nėra skirti jokiems tinkinimams.

5. Suraskite ir pašalinkite ankstesnį CRT plėtinį iš plėtinio konfigūracijos failo.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Nebaikite šio veiksmo, kol neatnaujinsite visų POS įrenginių, kuriuose veikia su šiuo režimu CRT instancija.

6. Užregistruokite esamą pavyzdį CRT plėtinius plėtinio konfigūracijos faile, pridėdami šias eilutes.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Atnaujinkite aparatūros stotį

1. Surask **HardwareStation.Extension.CleanCashSample** projektą ir jį pastatyti.
2. Viduje konors **Extension.CleanCashSample\\ šiukšliadėžė\\ Derinimas** aplanką, suraskite **Contoso.Commerce.HardwareStation.CleanCashSample.dll** ir **Interop.CleanCash\_ 1\_ 1.dll** surinkimo failai.
3. Nukopijuokite surinkimo failus į aplanką Hardware station extensions:

    - **Bendrinama aparatinės įrangos stotis:** Nukopijuokite failus į **šiukšliadėžė** aplanką, esantį IIS aparatinės įrangos stoties vietoje.
    - **Speciali aparatinės įrangos stotis šiuolaikinėje POS:** Nukopijuokite failus į Modern POS kliento tarpininko vietą.

4. Surask **HardwareStation.Extension.config** plėtinio konfigūracijos failas:

    - **Nuotolinė aparatūros stotis:** Failas yra IIS aparatinės įrangos stoties vietoje.
    - **Vietinė aparatinės įrangos stotis šiuolaikinėje POS:** Failas yra modernaus POS kliento tarpininko vietoje.

    > [!WARNING]
    > Daryk **ne** redaguoti CommerceRuntime.config ir CommerceRuntime.MPOSOffline.config failus. Šie failai nėra skirti jokiems tinkinimams.

5. Raskite ir pašalinkite ankstesnį Aparatinės įrangos stoties plėtinį iš plėtinio konfigūracijos failo.

    # <a name="retail-73-and-earlier"></a>[Mažmeninė prekyba 7.3 ir senesnės versijos](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Mažmeninė prekyba 7.3.1 ir naujesnės versijos](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Mažmeninė prekyba 10.0 ir naujesnės versijos](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Pridėkite šią eilutę prie **kompozicija** plėtinio konfigūracijos failo skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Atnaujinkite Modern POS

1. Atidaryk **CloudPOS.sln** sprendimas pagal **RetailSdk\\ POS**.
2. Išjunkite ankstesnį POS plėtinį pašalindami šias eilutes iš **plėtiniai.json** failą.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Įgalinkite dabartinį POS plėtinio pavyzdį įtraukdami šias eilutes **plėtiniai.json** failą.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Atnaujinkite „Cloud POS“.

1. Atidaryk **ModernPOS.sln** sprendimas pagal **RetailSdk\\ POS**.
2. Išjunkite ankstesnį POS plėtinį pašalindami šias eilutes iš **plėtiniai.json** failą.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Įgalinkite dabartinį POS plėtinio pavyzdį įtraukdami šias eilutes **plėtiniai.json** failą.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Migracija gamybos aplinkoje

#### <a name="update-crt"></a>Atnaujinti CRT

1. Pašalinkite ankstesnįjį CRT pratęsimas iš **CommerceRuntime.ext.config** ir **CommerceRuntime.MPOSOffline.Ext.config** konfigūracijos failus pagal **RetailSdk\\ Turtas** aplanką.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Nebaikite šio veiksmo, kol neatnaujinsite visų POS įrenginių, kuriuose veikia su šiuo režimu CRT instancija.

2. Įgalinti dabartinį pavyzdį CRT plėtinius, atlikdami toliau nurodytus pakeitimus **CommerceRuntime.ext.config** ir **CommerceRuntime.MPOSOffline.Ext.config** konfigūracijos failus pagal **RetailSdk\\ Turtas** aplanką.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. Viduje konors **Customization.settings** paketo tinkinimo konfigūracijos failą, esantį **BuildTools** aplanką, pridėkite šią eilutę, kad įtrauktumėte dabartinį pavyzdį CRT plėtinys diegiamuose paketuose.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Atnaujinkite aparatūros stotį

1. Pašalinkite ankstesnį aparatinės įrangos stoties plėtinį pakeisdami **HardwareStation.Extension.config** konfigūracijos failą.

    # <a name="retail-73-and-earlier"></a>[Mažmeninė prekyba 7.3 ir senesnės versijos](#tab/retail-7-3)

    Pašalinkite kitą skyrių iš **HardwareStation.Shared.config** ir **HardwareStation.Dedicated.config** konfigūracijos failus.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Mažmeninė prekyba 7.3.1 ir naujesnės versijos](#tab/retail-7-3-1)

    Pašalinkite kitą skyrių iš **HardwareStation.Extension.config** konfigūracijos failą.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Mažmeninė prekyba 10.0 ir naujesnės versijos](#tab/retail-10-0)

    Pašalinkite kitą skyrių iš **HardwareStation.Extension.config** konfigūracijos failą.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. Įgalinkite dabartinį pavyzdinį aparatinės įrangos stoties plėtinį, pridėdami šią eilutę prie **kompozicija** skyriuje **HardwareStation.Extension.config** konfigūracijos failą.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. Atlikite šiuos pakeitimus **Customization.settings** paketo tinkinimo konfigūracijos failą, esantį **BuildTools** aplankas:

    - Pašalinkite šią eilutę, kad iš diegiamų paketų neįtrauktumėte ankstesnio aparatūros stoties plėtinio.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - Pridėkite šias eilutes, kad įtrauktumėte dabartinį aparatinės įrangos stoties plėtinio pavyzdį į diegiamus paketus.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>Atnaujinkite Modern POS

1. Atidaryk **CloudPOS.sln** sprendimas at **RetailSdk\\ POS**.
2. Išjunkite ankstesnį POS plėtinį:

    - Viduje konors **tsconfig.json** failą, pridėkite **FiscalRegisterSample** aplanką į neįtraukiamųjų sąrašą.
    - Pašalinkite šias eilutes iš **plėtiniai.json** failą pagal **Mažmeninė SDK\\ POS\\ Plėtiniai** aplanką.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Įgalinkite dabartinį POS plėtinio pavyzdį įtraukdami šias eilutes **plėtiniai.json** failą pagal **Mažmeninė SDK\\ POS\\ Plėtiniai** aplanką.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Atnaujinkite „Cloud POS“.

1. Atidaryk **ModernPOS.sln** sprendimas pagal **RetailSdk\\ POS**.
2. Išjunkite ankstesnį POS plėtinį:

    - Viduje konors **tsconfig.json** failą, pridėkite **FiscalRegisterSample** aplanką į neįtraukiamųjų sąrašą.
    - Pašalinkite šias eilutes iš **plėtiniai.json** failą pagal **Mažmeninė SDK\\ POS\\ Plėtiniai** aplanką.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Įgalinkite dabartinį POS plėtinio pavyzdį įtraukdami šias eilutes **plėtiniai.json** failą pagal **Mažmeninė SDK\\ POS\\ Plėtiniai** aplanką.

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

Bėk **msbuild** visam mažmeninės prekybos SDK, kad būtų sukurti diegiamieji paketai. Taikykite pakuotes per LCS arba rankiniu būdu. Daugiau informacijos žr [Mažmeninė SDK pakuotė](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
