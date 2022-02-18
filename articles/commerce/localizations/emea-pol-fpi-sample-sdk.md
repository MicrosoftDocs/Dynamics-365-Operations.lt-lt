---
title: Fiskalinio spausdintuvo integravimo Lenkijoje pavyzdžio diegimo gairės (senas)
description: Šioje temoje pateikiamos gairės, kaip įdiegti mokesčių spausdintuvo integravimo pavyzdį Lenkijoje Microsoft Dynamics 365 Commerce Mažmeninės prekybos programinės įrangos kūrimo rinkinys (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 45cae498df8157b9561c54e9859daadcaedd7823
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076993"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Fiskalinio spausdintuvo integravimo Lenkijoje pavyzdžio diegimo gairės (senas)

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiamos gairės, kaip įdiegti mokesčių spausdintuvo integravimo pavyzdį Lenkijoje Microsoft Dynamics 365 Commerce Mažmeninės prekybos programinės įrangos kūrimo rinkinys (SDK) kūrėjo virtualioje mašinoje (VM).Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS). Daugiau informacijos apie šį fiskalinės integracijos pavyzdį žr [Fiskalinio spausdintuvo integravimo pavyzdys Lenkijai](emea-pol-fpi-sample.md). 

Lenkijos fiskalinės integracijos pavyzdys yra mažmeninės prekybos SDK dalis. Norėdami gauti informacijos apie tai, kaip įdiegti ir naudoti SDK, žr [Mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šį pavyzdį sudaro „Commerce“ vykdymo laiko plėtiniai (CRT) ir aparatinės įrangos stotis. Norėdami paleisti šį pavyzdį, turite modifikuoti ir sukurti CRT ir Aparatinės įrangos stočių projektai. Rekomenduojame naudoti nepakeistą mažmeninės prekybos SDK, kad atliktumėte šioje temoje aprašytus pakeitimus. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz Azure DevOps kur dar nepakeisti jokie failai.

## <a name="development-environment"></a>Talpinimo aplinka

Atlikite šiuos veiksmus, kad nustatytumėte kūrimo aplinką, kad galėtumėte išbandyti ir išplėsti pavyzdį.

### <a name="commerce-runtime-extension-components"></a>Prekybos vykdymo laiko plėtinio komponentai

The CRT plėtinio komponentai yra įtraukti į mažmeninės prekybos SDK. Norėdami užbaigti toliau nurodytas procedūras, atidarykite **CommerceRuntimeSamples.sln** sprendimas pagal **RetailSdk\\ Extensions pavyzdys\\ CommerceRuntime**.

1. Surask **Runtime.Extensions.DocumentProvider.PosnetSample** projektą ir jį pastatyti.
2. Viduje konors **Extensions.DocumentProvider.PosnetSample\\ šiukšliadėžė\\ Derinimas** aplanką, suraskite **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll** surinkimo failas.
3. Nukopijuokite surinkimo failą į CRT plėtinio aplankas:

    - **Prekybos masto vienetas:** Nukopijuokite failą į **\\ šiukšliadėžė\\ ext** aplanką, esantį interneto informacijos paslaugų (IIS) komercijos masto vieneto svetainėje.
    - **Vietinis CRT Šiuolaikinėje POS:** Nukopijuokite failą į **\\ ext** aplanką pagal vietinį CRT kliento brokerio vieta.

4. Raskite plėtinio konfigūracijos failą CRT:

    - **Prekybos masto vienetas:** Failas pavadintas **commerceruntime.ext.config**, ir jis yra **šiukšliadėžė\\ ext** aplanką, esantį IIS komercijos masto vieneto svetainės vietoje.
    - **Vietinis CRT Šiuolaikinėje POS:** Failas pavadintas **CommerceRuntime.MPOSOffline.Ext.config**, ir jis priklauso vietiniam CRT kliento brokerio vieta.

5. Užregistruokite CRT pakeisti plėtinio konfigūracijos failą.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Iš naujo paleiskite „Commerce“ paslaugą:

    - **Prekybos masto vienetas:** Iš naujo paleiskite „Commerce“ paslaugų svetainę iš „IIS Manager“.
    - **Klientų brokeris:** Baigti **dllhost.exe** procesą užduočių tvarkytuvėje, tada iš naujo paleiskite Modern POS.

### <a name="hardware-station-extension-components"></a>Aparatinės įrangos stoties išplėtimo komponentai

Aparatinės įrangos stoties plėtinio komponentai yra įtraukti į mažmeninės prekybos SDK. Norėdami užbaigti toliau nurodytas procedūras, atidarykite **HardwareStationSamples.sln** sprendimas pagal **RetailSdk\\ Extensions pavyzdys\\ HardwareStation**.

1. Surask **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** projektą ir jį pastatyti.
2. Viduje konors **Extension.Posnet.ThermalFVFiscalPrinterSample\\ šiukšliadėžė\\ Derinimas** aplanką, suraskite **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll** surinkimo failas.
3. Nukopijuokite surinkimo failą į įdiegtą aparatinės įrangos stoties įrenginį:

    - **Nuotolinė aparatūros stotis:** Nukopijuokite failą į **šiukšliadėžė** aplanką, esantį IIS aparatinės įrangos stoties vietoje. Nukopijuokite spausdintuvo tvarkyklės bibliotekas (**libposcmbth.dll**, **\_ serial.dll**, ir **cmbth\_ pl.lng**).

4. Raskite aparatūros stoties plėtinių konfigūracijos failą. Failas pavadintas **HardwareStation.Extension.config**:

    - **Nuotolinė aparatūros stotis:** Failas yra IIS aparatinės įrangos stoties vietoje.

5. Pridėkite šią eilutę prie **kompozicija** konfigūracijos failo skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Iš naujo paleiskite aparatūros stoties paslaugą:

    - **Nuotolinė aparatūros stotis:** Iš naujo paleiskite aparatūros stoties svetainę iš IIS tvarkyklės.

## <a name="production-environment"></a>Gamybos aplinka

Atlikdami ankstesnę procedūrą, įgalinote plėtinius, kurie yra fiskalinės registracijos paslaugos integravimo pavyzdžio komponentai. Be to, turite atlikti šiuos veiksmus, kad sukurtumėte diegiamus paketus, kuriuose yra „Commerce“ komponentų, ir pritaikytumėte tuos paketus gamybos aplinkoje.

1. Atlikite toliau nurodytus paketo konfigūracijos failų pakeitimus **RetailSdk\\ Turtas** aplankas:

    - Viduje konors **commerceruntime.ext.config** ir **CommerceRuntime.MPOSOffline.Ext.config** konfigūracijos failus, pridėkite šią eilutę prie **kompozicija** skyrius.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - Viduje konors **HardwareStation.Extension.config** konfigūracijos failą, pridėkite šią eilutę prie **kompozicija** skyrius.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Atlikite šiuos pakeitimus **Customization.settings** paketo tinkinimo konfigūracijos failą, esantį **BuildTools** aplankas:

    - Pridėkite šią eilutę, kad įtrauktumėte CRT plėtinį diegiamuose paketuose.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Pridėkite šią eilutę, kad įtrauktumėte aparatūros stoties plėtinį į diegiamus paketus.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Paleiskite MSBuild komandų eilutę, skirtą Visual Studio naudingumas, ir paleiskite **msbuild** mažmeninės prekybos SDK aplanke, kad sukurtumėte diegiamus paketus.
1. Taikykite pakuotes per LCS arba rankiniu būdu. Daugiau informacijos žr [Sukurkite dislokuojamus paketus](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Priestatų projektavimas

Fiskalinio spausdintuvo integravimo pavyzdys Lenkijai yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md). Norėdami gauti daugiau informacijos apie fiskalinės integracijos sprendimo dizainą, žr [fiskalinės integracijos pavyzdžio plano apžvalga](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Prekybos vykdymo laiko plėtinio dizainas

Plėtinio, kuris yra mokesčių dokumentų teikėjas, tikslas yra generuoti konkretiems spausdintuvams skirtus dokumentus ir tvarkyti atsakymus iš fiskalinio spausdintuvo.

The CRT pratęsimas yra **Runtime.Extensions.DocumentProvider.PosnetSample**. Šis plėtinys generuoja spausdintuvui būdingų komandų rinkinį JavaScript Object Notation (JSON) formatu, apibrėžtą POSNET specifikacijoje 19-3678.

Daugiau informacijos apie fiskalinės integracijos sprendimo dizainą žr [Fiskalinės registracijos procesas ir fiskalinės integracijos pavyzdžiai fiskaliniams įrenginiams ir paslaugoms](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **DocumentProviderPosnetProtocol** užklausų tvarkytojas yra užklausos generuoti dokumentus iš fiskalinio spausdintuvo įvesties taškas.

Prižiūrėtojas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Valdiklio pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – Šioje užklausoje pateikiama informacija apie tai, koks dokumentas turi būti sugeneruotas. Jis grąžina konkretaus spausdintuvo dokumentą, kuris turėtų būti užregistruotas mokesčių spausdintuve.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas ir Z ataskaitos spausdinimas.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra **Konfigūracija** plėtinio projekto aplanką. Failo tikslas – įgalinti dokumentų teikėjo nustatymus konfigūruoti „Commerce“ būstinėje. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie nustatymai:

- PVM tarifų susiejimas
- Mokėjimo priemonės tipo susiejimas
- Įmokos mokėjimo tipas

### <a name="hardware-station-extension-design"></a>Techninės įrangos stoties išplėtimo projektavimas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra susisiekti su mokesčių spausdintuvu.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**. Šis plėtinys iškviečia POSNET tvarkyklės funkcijas, kad pateiktų komandas, kurias CRT plėtinys sugeneruoja mokesčių spausdintuvą. Jis taip pat tvarko įrenginio klaidas.

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **FiscalPrinterHandler** užklausų tvarkytojas yra įvesties taškas, skirtas apdoroti užklausą į fiskalinį periferinį įrenginį.

Prižiūrėtojas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Droviklio pavadinimas turi atitikti fiskalinės jungties pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – Ši užklausa siunčia dokumentus į spausdintuvus ir grąžina atsakymą iš fiskalinio spausdintuvo.
- **IsReadyFiscalDeviceRequest** – Ši užklausa naudojama prietaiso sveikatos patikrinimui.
- **InitializeFiscalDeviceRequest** – Ši užklausa naudojama spausdintuvo inicijavimui.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra **Konfigūracija** plėtinio projekto aplanką. Failo tikslas – įgalinti jungties nustatymus, kuriuos būtų galima konfigūruoti „Commerce“ būstinėje. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie nustatymai:

- **Ryšio eilutė** – Eilutę, apibūdinančią išsamią ryšio su įrenginiu informaciją formatu, kurį palaiko tvarkyklė. Daugiau informacijos rasite POSNET tvarkyklės dokumentacijoje.
- **Datos ir laiko sinchronizavimas** – Reikšmė, nurodanti, ar spausdintuvo data ir laikas turi būti sinchronizuojami su prijungta aparatūros stotimi.
- **Įrenginio skirtasis laikas** – Laikas milisekundėmis, per kurį vairuotojas lauks atsakymo iš įrenginio. Daugiau informacijos rasite POSNET tvarkyklės dokumentacijoje.
