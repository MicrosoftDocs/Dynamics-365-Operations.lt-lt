---
title: Italijoje skirto fiskalinio spausdintuvo integravimo pavyzdžio diegimo gairės (senas)
description: Šioje temoje pateikiamos gairės, kaip įdiegti fiskalinio spausdintuvo integravimo pavyzdį Italijoje iš Microsoft Dynamics 365 Commerce Mažmeninės prekybos programinės įrangos kūrimo rinkinys (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 93aca34239affb41998f4309d7c03f29f7b5f003
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076917"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Italijoje skirto fiskalinio spausdintuvo integravimo pavyzdžio diegimo gairės (senas)

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiamos gairės, kaip įdiegti fiskalinio spausdintuvo integravimo pavyzdį Italijoje iš Microsoft Dynamics 365 Commerce Mažmeninės prekybos programinės įrangos kūrimo rinkinys (SDK) kūrėjo virtualioje mašinoje (VM).Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS). Daugiau informacijos apie šį fiskalinės integracijos pavyzdį žr [Fiskalinio spausdintuvo integravimo pavyzdys Italijai](emea-ita-fpi-sample.md). 

Italijos fiskalinės integracijos pavyzdys yra mažmeninės prekybos SDK dalis. Norėdami gauti informacijos apie tai, kaip įdiegti ir naudoti SDK, žr [Mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šį pavyzdį sudaro „Commerce“ vykdymo laiko plėtiniai (CRT) ir aparatinės įrangos stotis. Norėdami paleisti šį pavyzdį, turite modifikuoti ir sukurti CRT ir Aparatinės įrangos stočių projektai. Rekomenduojame naudoti nepakeistą mažmeninės prekybos SDK, kad atliktumėte šioje temoje aprašytus pakeitimus. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz Azure DevOps kur dar nepakeisti jokie failai.

## <a name="development-environment"></a>Talpinimo aplinka

Atlikite šiuos veiksmus, kad nustatytumėte kūrimo aplinką, kad galėtumėte išbandyti ir išplėsti pavyzdį.

### <a name="commerce-runtime-extension-components"></a>Prekybos vykdymo laiko plėtinio komponentai

The CRT plėtinio komponentai yra įtraukti į mažmeninės prekybos SDK. Norėdami užbaigti toliau nurodytas procedūras, atidarykite **CommerceRuntimeSamples.sln** sprendimas pagal **RetailSdk\\ Extensions pavyzdys\\ CommerceRuntime**.

1. Surask **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample** projektą ir jį pastatyti.
2. Viduje konors **Extensions.DocumentProvider.EpsonFP90IIISample\\ šiukšliadėžė\\ Derinimas** aplanką, suraskite **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll** surinkimo failas.
3. Nukopijuokite surinkimo failą į CRT plėtinių aplankas:

    - **Prekybos masto vienetas:** Nukopijuokite failą į **\\ šiukšliadėžė\\ ext** aplanką, esantį interneto informacijos paslaugų (IIS) komercijos masto vieneto svetainėje.
    - **Vietinis CRT Šiuolaikinėje POS:** Nukopijuokite failą į **\\ ext** aplanką pagal vietinį CRT kliento brokerio vieta.

4. Raskite plėtinio konfigūracijos failą CRT:

    - **Prekybos masto vienetas:** Failas pavadintas **commerceruntime.ext.config**, ir jis yra **šiukšliadėžė\\ ext** aplanką, esantį IIS komercijos masto vieneto svetainės vietoje.
    - **Vietinis CRT Šiuolaikinėje POS:** Failas pavadintas **CommerceRuntime.MPOSOffline.Ext.config**, ir jis priklauso vietiniam CRT kliento brokerio vieta.

5. Užregistruokite CRT pakeisti plėtinio konfigūracijos failą.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Iš naujo paleiskite „Commerce Scale Unit“:

    - **Prekybos masto vienetas:** Iš naujo paleiskite „Commerce Scale Unit“ svetainę iš IIS tvarkyklės.
    - **Klientų brokeris:** Baigti **dllhost.exe** procesą užduočių tvarkytuvėje, tada iš naujo paleiskite Modern POS.

### <a name="hardware-station-extension-components"></a>Aparatinės įrangos stoties išplėtimo komponentai

Aparatinės įrangos stoties plėtinio komponentai yra įtraukti į mažmeninės prekybos SDK. Norėdami užbaigti toliau nurodytas procedūras, atidarykite **HardwareStationSamples.sln** sprendimas pagal **RetailSdk\\ Extensions pavyzdys\\ HardwareStation**.

1. Surask **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** projektą ir jį pastatyti.
2. Viduje konors **Plėtiniai.EpsonFP90IIIFiscalDeviceSample\\ šiukšliadėžė\\ Derinimas** aplanką, suraskite **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll** surinkimo failas.
3. Nukopijuokite surinkimo failą į įdiegtą aparatinės įrangos stoties įrenginį:

    - **Nuotolinė aparatūros stotis:** Nukopijuokite failą į **šiukšliadėžė** aplanką, esantį IIS aparatinės įrangos stoties vietoje.
    - **Vietinė aparatūros stotis:** Nukopijuokite failą į Modern POS kliento tarpininko vietą.

4. Raskite aparatūros stoties plėtinių konfigūracijos failą. Failas pavadintas **HardwareStation.Extension.config**:

    - **Nuotolinė aparatūros stotis:** Failas yra IIS aparatinės įrangos stoties vietoje.
    - **Vietinė aparatūros stotis:** Failas yra modernaus POS kliento tarpininko vietoje.

5. Pridėkite kitą skyrių prie **kompozicija** konfigūracijos failo skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Iš naujo paleiskite aparatūros stoties paslaugą:

    - **Nuotolinė aparatūros stotis:** Iš naujo paleiskite aparatūros stoties svetainę iš IIS tvarkyklės.
    - **Vietinė aparatūros stotis:** Baigti **dllhost.exe** procesą užduočių tvarkytuvėje, tada iš naujo paleiskite Modern POS.

## <a name="production-environment"></a>Gamybos aplinka

Norėdami sukurti diegiamus paketus, kuriuose yra „Commerce“ komponentų, ir pritaikyti tuos paketus gamybinėje aplinkoje, atlikite šiuos veiksmus.

1. Atlikite veiksmus, aprašytus [Plėtros aplinka](#development-environment) skyrių anksčiau šioje temoje.
2. Atlikite toliau nurodytus paketo konfigūracijos failų pakeitimus **RetailSdk\\ Turtas** aplankas:

    - Viduje konors **commerceruntime.ext.config** ir **CommerceRuntime.MPOSOffline.Ext.config** konfigūracijos failus, pridėkite šią eilutę prie **kompozicija** skyrius.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    - Viduje konors **HardwareStation.Extension.config** konfigūracijos failą, pridėkite šią eilutę prie **kompozicija** skyrius.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Atlikite šiuos pakeitimus **Customization.settings** paketo tinkinimo konfigūracijos failą, esantį **BuildTools** aplankas:

    - Pridėkite šią eilutę, kad įtrauktumėte CRT plėtinį diegiamuose paketuose.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    - Pridėkite šią eilutę, kad įtrauktumėte aparatūros stoties plėtinį į diegiamus paketus.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Paleiskite MSBuild komandų eilutę, skirtą Visual Studio naudingumą, tada paleiskite **msbuild** mažmeninės prekybos SDK aplanke, kad sukurtumėte diegiamus paketus.
5. Taikykite pakuotes per LCS arba rankiniu būdu. Daugiau informacijos žr [Sukurkite dislokuojamus paketus](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Priestatų projektavimas

### <a name="commerce-runtime-extension-design"></a>Prekybos vykdymo laiko plėtinio dizainas

Plėtinio, kuris yra mokesčių dokumentų teikėjas, tikslas yra generuoti konkretiems spausdintuvams skirtus dokumentus ir tvarkyti atsakymus iš fiskalinio spausdintuvo.

The CRT pratęsimas yra **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**.

Daugiau informacijos apie fiskalinės integracijos sprendimo dizainą žr [Fiskalinės registracijos procesas ir fiskalinės integracijos pavyzdžiai fiskaliniams įrenginiams ir paslaugoms](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **Document ProviderEpsonFP90III** užklausų tvarkytojas yra užklausos generuoti dokumentus iš fiskalinio spausdintuvo įvesties taškas.

Prižiūrėtojas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Valdiklio pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – Šioje užklausoje pateikiama informacija apie tai, koks dokumentas turi būti sugeneruotas. Jis grąžina konkretaus spausdintuvo dokumentą, kuris turėtų būti užregistruotas mokesčių spausdintuve.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas ir Z ataskaitos spausdinimas.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra **Konfigūracija** plėtinio projekto aplanką. Failo tikslas – įgalinti dokumentų teikėjo nustatymus konfigūruoti „Commerce“ būstinėje. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie nustatymai:

- PVM kodų susiejimas
- PVM tarifų susiejimas
- Mokėjimo priemonės tipo susiejimas
- Kvito numerio brūkšninio kodo tipas
- Įmokos mokėjimo tipas

### <a name="hardware-station-extension-design"></a>Techninės įrangos stoties išplėtimo projektavimas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra susisiekti su mokesčių spausdintuvu.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**. Šis plėtinys naudoja HTTP protokolą, kad pateiktų dokumentus, kuriuos CRT plėtinys sugeneruoja mokesčių spausdintuvą. Ji taip pat tvarko atsakymus, gautus iš mokesčių spausdintuvo.

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **EpsonFP90III pavyzdys** užklausų tvarkytuvas yra įvesties taškas, skirtas apdoroti užklausas į fiskalinį periferinį įrenginį.

Prižiūrėtojas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Droviklio pavadinimas turi atitikti fiskalinės jungties pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – Ši užklausa siunčia dokumentus į spausdintuvus ir grąžina atsakymą iš fiskalinio spausdintuvo.
- **IsReadyFiscalDeviceRequest** – Ši užklausa naudojama prietaiso sveikatos patikrinimui.
- **InitializeFiscalDeviceRequest** – Ši užklausa naudojama spausdintuvo inicijavimui.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra **Konfigūracija** plėtinio projekto aplanką. Failo tikslas – įgalinti jungties nustatymus, kuriuos būtų galima konfigūruoti „Commerce“ būstinėje. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie nustatymai:

- **Galinio taško adresas** – Spausdintuvo URL.
- **Datos ir laiko sinchronizavimas** – Reikšmė, nurodanti, ar spausdintuvo data ir laikas turi būti sinchronizuojami su prijungta aparatūros stotimi.
