---
title: Finansinio spausdintuvo integravimo pavyzdžio Lenkijai (senesni) diegimo rekomendacijos
description: Šioje temoje pateikiamos gairės, kaip iš "Retail" programinės įrangos kūrimo rinkinio (SDK) įdiegti Lenkijos Microsoft Dynamics 365 Commerce fiskalinio spausdintuvo integravimo pavyzdį.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: bff3a6ad74d50e7b706d4df92b17a4a3af36521b
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944820"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Finansinio spausdintuvo integravimo pavyzdžio Lenkijai (senesni) diegimo rekomendacijos

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiami gairės, kaip įdiegti Lenkijos fiskalinio spausdintuvo integravimo pavyzdį iš "Retail" programinės įrangos kūrimo rinkinio (SDK), programavimo virtualiosios mašinos (VM) ciklo tarnybose Microsoft Dynamics 365 Commerce Microsoft Dynamics (LCS). Daugiau informacijos apie šį finansinio integravimo pavyzdį ieškokite [Lenkijai skirtas iždo dokumentų spausdintuvo integravimo pavyzdys](emea-pol-fpi-sample.md). 

Lenkijos finansinio integravimo pavyzdys yra mažmeninės prekybos SDK dalis. Informacijos, kaip įdiegti ir naudoti SDK, ieškokite Mažmeninės prekybos programinės [įrangos kūrimo rinkinio (SDK) architektūroje](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šį pavyzdį sudaro "Commerce Runtime ( ) ir CRT Hardware" stoties plėtiniai. Norėdami vykdyti šį pavyzdį, turite modifikuoti ir sukurti CRT "Hardware" stoties projektus. Rekomenduojame naudoti nesumoduliuotą "Retail SDK", kad būtų atlikti šioje temoje aprašyti pakeitimai. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz., Azure DevOps kurioje dar nėra pakeistų failų.

## <a name="development-environment"></a>Talpinimo aplinka

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

### <a name="commerce-runtime-extension-components"></a>"Commerce Runtime" plėtinio komponentai

Išplėstiniai CRT komponentai įtraukti į "Retail SDK". Norėdami atlikti šias procedūras, dalyje **·** **RetailSdk \\ SampleExtensions \\ CommerceRuntime atidarykite sprendimą CommerceRuntimeSamples.sln.**

1. Raskite **Runtime.Extensions.DocumentProvider.PosnetSample** projektą ir sukurkite jį.
2. Aplanke **Extensions.DocumentProvider.PosnetSample bin Debug raskite \\\\ rinkinio failą** **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll.**
3. Nukopijuokite surinkimo failą į CRT plėtinio aplanką:

    - **"Commerce Scale Unit:" kopijuokite failą į talpyklos iš išorės aplanką, esantį informacinių interneto paslaugų** **\\\\** (IIS) "Commerce Scale Unit" vietoje.
    - **"Modern CRT POS" vieta:** kopijuokite failą į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris CRT skirtas:

    - **"Commerce Scale Unit:** failas **yra pavadintas commerceruntime.ext.config ir jis yra talpyklos išorinio aplanko** **\\** IIS "Commerce Scale Unit" vietoje.
    - **"Modern POS" vietinė: failo vardas yra CRT** **CommerceRuntime.MPOSOffline.Ext.config, jis priklauso vietinio** kliento CRT brokerio vietai.

5. CRT Užregistruokite pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Iš naujo paleisti "Commerce Service":

    - **"Commerce Scale Unit: iš** naujo paleisti "Commerce Service" svetainę iš IIS tvarkytuvo.
    - **Kliento brokeris:** užbaigti **dllhost.exe** procesą užduočių tvarkytuve ir iš naujo paleisti "Modern POS".

### <a name="hardware-station-extension-components"></a>Aparatūros stoties plėtinio komponentai

Aparatūros stoties plėtinio komponentai įtraukti į "Retail SDK". Norėdami atlikti šias procedūras, **dalyje** **RetailSdk \\ SampleExtensions HardwareStation atidarykite sprendimą HardwareStationSamples.sln. \\**

1. Suraskite **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** projektą ir sukurkite jį.
2. Aplanke **Extension.Posnet.PagalVFiscalPrinterSample \\ talpyklos \\ debug raskite surinkimo failą** **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll.**
3. Nukopijuokite surinkimo failą į įdiegtą aparatūros stoties įrenginį:

    - **Nuotolinės aparatūros** stotis: kopijuokite failą į **talpyklos** aplanką, esantį IIS aparatūros stoties svetainės vietoje. Kopijuokite spausdintuvo tvarkyklės **bibliotekas (libposcmbth.dll,** **libcmbth \_ serial.dll** ir **cmbth \_ pl.lng).**

4. Raskite aparatūros stoties plėtinių konfigūracijos failą. Failo vardas yra **HardwareStation.Extension.config:**

    - **Nuotolinės aparatūros** stotis: failas yra IIS aparatūros stoties svetainės vietoje.

5. Įtraukite šią eilutę į **konfigūracijos** failo sudėties skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Iš naujo paleiskite aparatūros stoties tarnybą:

    - **Nuotolinės aparatūros stotis:** iš naujo paleiskite aparatūros stoties svetainę iš IIS tvarkytuvo.

## <a name="production-environment"></a>Gamybos aplinka

Ankstesnės procedūros metu įgalinote plėtinius, kurie yra finansinio registravimo tarnybos integravimo pavyzdžio komponentai. Be to, turite atlikti šiuos veiksmus, jei norite kurti diegtinas pakuotes, kuriose yra "Commerce" komponentai, ir taikyti šias pakuotes gamybos aplinkoje.

1. Atlikite šiuos paketo konfigūracijos failų keitimus, nurodytus aplanke **"RetailSdk \\** Assets":

    - Konfigūracijos **failuose commerceruntime.ext.config ir** **CommerceRuntime.MPOSOffline.Ext.config įtraukite šią eilutę į** **sudėties** skyrių.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - Konfigūracijos **faile HardwareStation.Extension.config** įtraukite šią eilutę į **skyriaus** sudėtį.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Atlikite šiuos pakeitimus **customization.settings** paketo pritaikymo konfigūracijos faile, aplanke **BuildTools:**

    - Įtraukite šią eilutę, kad CRT įtraukumėte plėtinį į diegiamus paketus.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Įtraukite šią eilutę, kad į diegtimus paketus įtraukumėte "Hardware" stoties plėtinį.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Paleiskite MSBuild komandinę eilutę dėl paslaugų programos ir paleiskite Visual Studio msbuild "Retail" SDK aplanke, kad sukurtumėte **diegiamus** paketus.
1. Taikykite paketus naudodami LCS arba rankiniu būdu. Daugiau informacijos ieškokite [Create deployable](../dev-itpro/retail-sdk/retail-sdk-packaging.md) packages.

## <a name="design-of-extensions"></a>Plėtinių dizainas

Lenkijos fiskalinio spausdintuvo integravimo pavyzdys pagrįstas [finansinio integravimo](fiscal-integration-for-retail-channel.md) funkcijomis. Daugiau informacijos apie finansinio integravimo sprendimo dizainą ieškokite finansinio [integravimo pavyzdžio dizaino apžvalgoje.](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti konkretaus spausdintuvo dokumentus ir tvarkyti atsakymus iš fiskalinio spausdintuvo.

Plėtinys CRT yra **Runtime.Extensions.DocumentProvider.PosnetSample.** Šis plėtinys sugeneruoja poSNET 19-3678 specifikacijos apibrėžtą "JavaScript Object Notation" (JSON) formato spausdintuvui specialių komandų rinkinį.

Daugiau informacijos apie finansinio integravimo sprendimo dizainą rasite finansinio įrenginių finansinio [registravimo procese ir finansinio integravimo pavyzdžius.](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

DocumentProviderPosnetProtocol užklausos apdorojimo programa yra įvesties taškas, per kurį užklausa **generuoja** dokumentus iš fiskalinio spausdintuvo.

Apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą "Commerce" būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje pateikiama informacija apie tai, kokį dokumentą reikia generuoti. Grąžinamas spausdintuvui konkretus dokumentas, kuris turi būti užregistruotas fiskaliniu spausdintuvu.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas ir Z ataskaitos spausdinimas.

#### <a name="configuration"></a>Konfigūravimas

Konfigūracijos failas yra plėtinio **projekto** konfigūracijos aplanke. Failo paskirtis – įgalinti dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie parametrai:

- PVM tarifų susiejimas
- Mokėjimo priemonės tipo susiejimas
- Įmokos mokėjimo tipas

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, paskirtis yra palaikyti ryšį su fiskaliniu spausdintuvu.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample.** Šis plėtinys išk prašo POSNET tvarkyklės funkcijų pateikti komandas, kurias CRT plėtinys sugeneruoja fiskaliniu spausdintuvu. Ji taip pat tvarko įrenginio klaidas.

#### <a name="request-handler"></a>Užklausų apdorojimo teotorius

**FiscalPrinterHandler užklausos** apdorojimo programa yra įvesties taškas, skirtas tvarkyti užklausą į fiskalinį per įrenginį.

Apdorojimo programa yra paveldėta iš **INamedRequestHandler** sąsajos. **HandlerName** metodas yra atsakingas už apdorojimo įmonės pavadinimo grąžinimą. Apdorojimo įmonės pavadinimas turi atitikti "Commerce" būstinėje nurodytą fiskalinės jungties pavadinimą.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest – ši užklausa siunčia dokumentus spausdintuvams ir grąžina atsakymą** iš fiskalinio spausdintuvo.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama įrenginio sveikatos patikrai atlikti.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama spausdintuvui inicijuoti.

#### <a name="configuration"></a>Konfigūravimas

Konfigūracijos failas yra **plėtinio** projekto konfigūracijos aplanke. Failo paskirtis – įgalinti jungties parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais. Pridedami šie parametrai:

- **Jungimosi eilutė – eilutė, aprašantys išsamią ryšio su įrenginiu** informaciją tvarkyklės palaikomu formatu. Daugiau informacijos ieškokite POSNET tvarkyklės dokumentuose.
- **Datos ir laiko sinchronizavimas – reikšmė, nurodanti, ar spausdintuvo data ir laikas turi būti** sinchronizuoti su prijungta aparatūros stotyje.
- **Įrenginio skirtasis laikas milisekunde, per kurį vairuotojas lauks atsakymo iš** įrenginio. Daugiau informacijos ieškokite POSNET tvarkyklės dokumentuose.
