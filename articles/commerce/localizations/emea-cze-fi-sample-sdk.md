---
title: Čekijos Respublikos mokesčių registracijos paslaugos integravimo pavyzdžio diegimo gairės (palikimas)
description: Šioje temoje pateikiamos gairės, kaip taikyti Čekijos Respublikos fiskalinės integracijos pavyzdį Microsoft Dynamics 365 Commerce Mažmeninės prekybos programinės įrangos kūrimo rinkinys (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: adafde2123afdc793a6ef4edf8fa16b857c55bf8
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076941"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-the-czech-republic-legacy"></a>Čekijos Respublikos mokesčių registracijos paslaugos integravimo pavyzdžio diegimo gairės (palikimas)

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiamos gairės, kaip įdiegti mokesčių registravimo paslaugos integravimo pavyzdį Čekijoje Microsoft Dynamics 365 Commerce Mažmeninės prekybos programinės įrangos kūrimo rinkinys (SDK) kūrėjo virtualioje mašinoje (VM).Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS). Daugiau informacijos apie šį fiskalinės integracijos pavyzdį žr [Čekijos Respublikos mokesčių registravimo paslaugos integravimo pavyzdys](emea-cze-fi-sample.md). 

Čekijos Respublikos fiskalinės integracijos pavyzdys yra mažmeninės prekybos SDK dalis. Norėdami gauti informacijos apie tai, kaip įdiegti ir naudoti SDK, žr [Mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šį pavyzdį sudaro „Commerce“ vykdymo laiko plėtiniai (CRT) ir aparatinės įrangos stotis. Norėdami paleisti šį pavyzdį, turite modifikuoti ir sukurti CRT ir Aparatinės įrangos stočių projektai. Rekomenduojame naudoti nepakeistą mažmeninės prekybos SDK, kad atliktumėte šioje temoje aprašytus pakeitimus. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz Azure DevOps kur dar nepakeisti jokie failai.

## <a name="development-environment"></a>Talpinimo aplinka

Atlikite šiuos veiksmus, kad nustatytumėte kūrimo aplinką, kad galėtumėte išbandyti ir išplėsti pavyzdį.

### <a name="enable-commerce-runtime-extensions"></a>Įgalinti „Commerce“ vykdymo laiko plėtinius

The CRT pratęsimo komponentai yra įtraukti į CRT pavyzdžiai. Norėdami užbaigti toliau nurodytas procedūras, atidarykite **CommerceRuntimeSamples.sln** sprendimas pagal **RetailSdk\\ Extensions pavyzdys\\ CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample komponentas

1. Surask **Runtime.Extensions.DocumentProvider.EFRSample** projektą ir jį pastatyti.
2. Viduje konors **Runtime.Extensions.DocumentProvider.EFRSample\\ šiukšliadėžė\\ Derinimas** aplanką, suraskite **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** surinkimo failas.
3. Nukopijuokite surinkimo failą į CRT plėtinių aplankas:

    - **Prekybos masto vienetas:** Nukopijuokite failą į **\\ šiukšliadėžė\\ ext** aplanką, esantį interneto informacijos paslaugų (IIS) komercijos masto vieneto svetainėje.
    - **Vietinis CRT Šiuolaikinėje POS:** Nukopijuokite failą į **\\ ext** aplanką pagal vietinį CRT kliento brokerio vieta.

4. Raskite plėtinio konfigūracijos failą CRT:

    - **Prekybos masto vienetas:** Failas pavadintas **commerceruntime.ext.config**, ir jis yra **šiukšliadėžė\\ ext** aplanką, esantį IIS komercijos masto vieneto svetainės vietoje.
    - **Vietinis CRT Šiuolaikinėje POS:** Failas pavadintas **CommerceRuntime.MPOSOffline.Ext.config**, ir jis priklauso vietiniam CRT kliento brokerio vieta.

5. Užregistruokite CRT pakeisti plėtinio konfigūracijos failą.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR komponentas

1. Surask **Runtime.Extensions.DocumentProvider.DataModelEFR** projektą ir jį pastatyti.
2. Viduje konors **Runtime.Extensions.DocumentProvider.DataModelEFR\\ šiukšliadėžė\\ Derinimas** aplanką, suraskite **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** surinkimo failas.
3. Nukopijuokite surinkimo failą į CRT plėtinių aplankas:

    - **Prekybos masto vienetas:** Nukopijuokite failą į **\\ šiukšliadėžė\\ ext** aplanką, esantį IIS komercijos masto vieneto svetainės vietoje.
    - **Vietinis CRT Šiuolaikinėje POS:** Nukopijuokite failą į **\\ ext** aplanką pagal vietinį CRT kliento brokerio vieta.

4. Raskite plėtinio konfigūracijos failą CRT:

    - **Prekybos masto vienetas:** Failas pavadintas **commerceruntime.ext.config**, ir jis yra **šiukšliadėžė\\ ext** aplanką, esantį IIS komercijos masto vieneto svetainės vietoje.
    - **Vietinis CRT Šiuolaikinėje POS:** Failas pavadintas **CommerceRuntime.MPOSOffline.Ext.config**, ir jis priklauso vietiniam CRT kliento brokerio vieta.

5. Užregistruokite CRT pakeisti plėtinio konfigūracijos failą.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Plėtinio konfigūracijos failas

1. Raskite plėtinio konfigūracijos failą CRT:

    - **Prekybos masto vienetas:** Failas pavadintas **commerceruntime.ext.config**, ir jis yra **šiukšliadėžė\\ ext** aplanką, esantį IIS komercijos masto vieneto svetainės vietoje.
    - **Vietinis CRT Šiuolaikinėje POS:** Failas pavadintas **CommerceRuntime.MPOSOffline.Ext.config**, ir jis priklauso vietiniam CRT kliento brokerio vieta.

2. Užregistruokite CRT pakeisti plėtinio konfigūracijos failą.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
    ```

### <a name="enable-hardware-station-extensions"></a>Įgalinti aparatinės įrangos stoties plėtinius

Aparatūros stoties plėtinio komponentai yra įtraukti į aparatinės įrangos stoties pavyzdžius. Norėdami užbaigti toliau nurodytas procedūras, atidarykite **HardwareStationSamples.sln** sprendimas pagal **RetailSdk\\ Extensions pavyzdys\\ HardwareStation**.

#### <a name="efrsample-component"></a>EFRSample komponentas

1. Surask **HardwareStation.Extension.EFRSample** projektą ir jį pastatyti.
2. Viduje konors **Plėtinys.EFRSpavyzdys\\ šiukšliadėžė\\ Derinimas** aplanką, raskite šiuos surinkimo failus:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Nukopijuokite surinkimo failus į aplanką Hardware station extensions:

    - **Bendrinama aparatinės įrangos stotis:** Nukopijuokite failus į **šiukšliadėžė** aplanką, esantį IIS aparatinės įrangos stoties vietoje.
    - **Speciali aparatinės įrangos stotis šiuolaikinėje POS:** Nukopijuokite failus į Modern POS kliento tarpininko vietą.

4. Raskite aparatinės įrangos stoties plėtinių plėtinio konfigūracijos failą. Failas pavadintas **HardwareStation.Extension.config**.

    - **Bendrinama aparatinės įrangos stotis:** Failas yra IIS aparatinės įrangos stoties vietoje.
    - **Speciali aparatinės įrangos stotis šiuolaikinėje POS:** Failas yra modernaus POS kliento tarpininko vietoje.

5. Pridėkite šią eilutę prie **kompozicija** konfigūracijos failo skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

### <a name="production-environment"></a>Gamybos aplinka

Ankstesnė procedūra įgalina plėtinius, kurie yra fiskalinės registracijos paslaugos integravimo pavyzdžio komponentai. Be to, turite atlikti šiuos veiksmus, kad sukurtumėte diegiamus paketus, kuriuose yra „Commerce“ komponentų, ir pritaikytumėte tuos paketus gamybos aplinkoje.

1. Atlikite toliau nurodytus paketo konfigūracijos failų pakeitimus **RetailSdk\\ Turtas** aplanką.

    - Viduje konors **commerceruntime.ext.config** ir **CommerceRuntime.MPOSOffline.Ext.config** konfigūracijos failus, pridėkite šias eilutes prie **kompozicija** skyrius.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
        ```

    - Viduje konors **HardwareStation.Extension.config** konfigūracijos failą, pridėkite šią eilutę prie **kompozicija** skyrius.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

2. Atlikite šiuos pakeitimus **Customization.settings** paketo tinkinimo konfigūracijos failą, esantį **BuildTools** aplanką.

    - Pridėkite šias eilutes, kad įtrauktumėte CRT plėtinius diegiamuose paketuose.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Pridėkite šią eilutę, kad įtrauktumėte aparatūros stoties plėtinį į diegiamus paketus.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. Paleiskite MSBuild komandų eilutę, skirtą Visual Studio naudingumas, ir paleiskite **msbuild** mažmeninės prekybos SDK aplanke, kad sukurtumėte diegiamus paketus.
4. Taikykite pakuotes per LCS arba rankiniu būdu. Daugiau informacijos žr [Sukurkite dislokuojamus paketus](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Atlikite visas reikalingas sąrankos užduotis, kurios aprašytos [Nustatyti komerciją Čekijoje](emea-cze-fi-sample.md#set-up-commerce-for-the-czech-republic).

## <a name="design-of-extensions"></a>Priestatų projektavimas

Čekijos Respublikos mokesčių registravimo paslaugos integravimo pavyzdys yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md). Norėdami gauti daugiau informacijos apie fiskalinės integracijos sprendimo dizainą, žr [fiskalinės integracijos pavyzdžio plano apžvalga](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Prekybos vykdymo laiko plėtinio dizainas

Plėtinio, kuris yra fiskalinių dokumentų teikėjas, tikslas – generuoti konkrečiai paslaugai skirtus dokumentus ir tvarkyti fiskalinės registracijos tarnybos atsakymus.

The CRT pratęsimas yra **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Užklausų tvarkytojas

Yra vienas **DocumentProviderEFRFiscalCZE** užklausų tvarkytojas dokumentų teikėjui. Jis naudojamas fiskaliniams dokumentams fiskalinės registracijos paslaugai generuoti.

Šis tvarkytuvas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Valdiklio pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – Šioje užklausoje pateikiama informacija apie tai, koks dokumentas turi būti sugeneruotas. Jis grąžina konkrečiai paslaugai skirtą dokumentą, kuris turėtų būti užregistruotas fiskalinės registracijos tarnyboje.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimai, klientų sąskaitos įnašai ir klientų užsakymų įnašai.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Ši užklausa grąžina fiskalinės registracijos tarnybos atsakymą. Šis atsakymas yra serijinis, kad sudarytų eilutę, kad būtų galima išsaugoti.

#### <a name="configuration"></a>Konfigūracija

The **DocumentProviderFiscalEFRSampleCzech** konfigūracijos failas yra **Konfigūracija** plėtinio projekto aplanką. Šio failo tikslas – įgalinti dokumentų teikėjo nustatymus, kurie būtų konfigūruojami iš „Commerce“ būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie nustatymai:

- PVM tarifų susiejimas
- Numatytoji PVM grupė
- Indėlių PVM grupė

### <a name="hardware-station-extension-design"></a>Techninės įrangos stoties išplėtimo projektavimas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra susisiekti su mokesčių registravimo tarnyba.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.EFRSample**. Aparatinės įrangos stoties plėtinys naudoja HTTP protokolą, kad pateiktų dokumentus CRT plėtinys generuoja fiskalinės registracijos paslaugą. Ji taip pat tvarko atsakymus, gautus iš fiskalinės registracijos tarnybos.

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **EFRHandler** užklausų tvarkytojas yra įvesties taškas, kuriame tvarkomos užklausos į fiskalinės registracijos tarnybą.

Prižiūrėtojas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Droviklio pavadinimas turi atitikti fiskalinės jungties pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – Pagal šią užklausą dokumentai siunčiami fiskalinės registracijos tarnybai ir iš jos grąžinamas atsakymas.
- **IsReadyFiscalDeviceRequest** – Šis prašymas naudojamas fiskalinės registracijos tarnybos sveikatos patikrinimui.
- **InitializeFiscalDeviceRequest** – Ši užklausa naudojama fiskalinės registracijos paslaugai inicijuoti.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra **Konfigūracija** plėtinio projekto aplanką. Failo tikslas – įgalinti fiskalinės jungties nustatymus, kuriuos būtų galima konfigūruoti „Commerce“ būstinėje. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie nustatymai:

- **Galinio taško adresas** – Fiskalinės registracijos paslaugos URL.
- **Laikas baigėsi** – Laikas milisekundėmis, per kurį vairuotojas lauks atsakymo iš fiskalinės registracijos tarnybos.
