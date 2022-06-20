---
title: Finansinio spausdintuvo integravimo pavyzdžio Lenkijai (senesni) diegimo rekomendacijos
description: Šiame straipsnyje pateikiamos gairės, kaip iš "Retail" programinės įrangos kūrimo rinkinio (SDK) įdiegti Lenkijos fiskalinio Microsoft Dynamics 365 Commerce spausdintuvo integravimo pavyzdį.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 3de7559838a8d8caf64993a468f06ba2d50fff46
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851162"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Finansinio spausdintuvo integravimo pavyzdžio Lenkijai (senesni) diegimo rekomendacijos

[!include[banner](../includes/banner.md)]

Šiame straipsnyje pateikiamos Microsoft Dynamics 365 Commerce gairės, kaip įdiegti finansinio spausdintuvo integravimo pavyzdį Lenkijai iš "Retail" programinės įrangos kūrimo rinkinio (SDK) programuotojo virtualiojoje kompiuteryje (VM) Microsoft Dynamics ciklo tarnybose (LCS). Daugiau informacijos apie šį finansinio integravimo pavyzdį ieškokite Lenkijai skirtas [iždo dokumentų spausdintuvo integravimo pavyzdys](emea-pol-fpi-sample.md). 

Lenkijos finansinio integravimo pavyzdys yra mažmeninės prekybos SDK dalis. Informacijos, kaip įdiegti ir naudoti SDK, ieškokite Mažmeninės prekybos programinės [įrangos kūrimo rinkinio (SDK) architektūroje](../dev-itpro/retail-sdk/retail-sdk-overview.md). Šį pavyzdį sudaro "Commerce Runtime (CRT) ir Hardware" stoties plėtiniai. Norėdami vykdyti šį pavyzdį, turite modifikuoti ir sukurti " CRT Hardware" stoties projektus. Rekomenduojame naudoti nesumoduliuotą "Retail SDK", kad būtų atlikti šiame straipsnyje aprašyti pakeitimai. Taip pat rekomenduojame naudoti šaltinio valdymo sistemą, pvz.Azure DevOps, kurioje dar nėra pakeistų failų.

## <a name="development-environment"></a>Programavimo aplinka

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

### <a name="commerce-runtime-extension-components"></a>"Commerce Runtime" plėtinio komponentai

Išplėstiniai CRT komponentai įtraukti į "Retail SDK". Norėdami atlikti šias procedūras, dalyje RetailSdk SampleExtensions CommerceRuntime **atidarykite sprendimą CommerceRuntimeSamples.sln** **\\.\\**

1. Raskite **Runtime.Extensions.DocumentProvider.PosnetSample** projektą ir sukurkite jį.
2. Aplanke Extensions.DocumentProvider.PosnetSample bin Debug **\\ raskite rinkinio failą Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll\\.** **·**
3. Nukopijuokite surinkimo failą į plėtinio CRT aplanką:

    - **"Commerce Scale Unit:" kopijuokite** failą **\\\\ į talpyklos iš** išorės aplanką, esantį informacinių interneto paslaugų (IIS) "Commerce Scale Unit" vietoje.
    - **" CRT Modern POS" vieta: kopijuokite** failą į **\\ iš išorės** aplanką, esantį vietinio kliento CRT brokerio vietoje.

4. Rasti plėtinio konfigūracijos failą, kuris skirtas CRT:

    - **"Commerce Scale Unit:** failas **yra pavadintas commerceruntime.ext.config**, **\\** jis yra talpyklos išorinio aplanko IIS "Commerce Scale Unit" vietoje.
    - **" CRT Modern POS" vietinė:** **failo vardas yra CommerceRuntime.MPOSOffline.Ext.config**, jis priklauso vietinio kliento CRT brokerio vietai.

5. Užregistruokite CRT pakeitimą plėtinio konfigūracijos faile.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Iš naujo paleisti "Commerce Service":

    - **"Commerce Scale Unit: iš** naujo paleisti "Commerce Service" svetainę iš IIS tvarkytuvo.
    - **Kliento brokeris:** užbaigti **dllhost.exe procesą** užduočių tvarkytuve ir iš naujo paleisti "Modern POS".

### <a name="hardware-station-extension-components"></a>Aparatūros stoties plėtinio komponentai

Aparatūros stoties plėtinio komponentai įtraukti į "Retail SDK". Norėdami atlikti šias procedūras, dalyje RetailSdk SampleExtensions HardwareStation atidarykite sprendimą **HardwareStationSamples.sln** **\\.\\**

1. Suraskite **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** projektą ir sukurkite jį.
2. Aplanke Extension.Posnet.PagalVFiscalPrinterSample talpyklos debug **\\ raskite surinkimo failą Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll\\.** **·**
3. Nukopijuokite surinkimo failą į įdiegtą aparatūros stoties įrenginį:

    - **Nuotolinės aparatūros stotis:** kopijuokite failą į **talpyklos** aplanką, esantį IIS aparatūros stoties svetainės vietoje. Kopijuokite spausdintuvo tvarkyklės bibliotekas (libposcmbth.dll **,** libcmbth **serial.dll\_ ir** cmbth **pl.lng\_**).

4. Raskite aparatūros stoties plėtinių konfigūracijos failą. Failo vardas yra **HardwareStation.Extension.config**:

    - **Nuotolinės aparatūros stotis:** failas yra IIS aparatūros stoties svetainės vietoje.

5. Įtraukite šią eilutę į **konfigūracijos** failo sudėties skyrių.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Iš naujo paleiskite aparatūros stoties tarnybą:

    - **Nuotolinės aparatūros stotis: iš** naujo paleiskite aparatūros stoties svetainę iš IIS tvarkytuvo.

## <a name="production-environment"></a>Gamybos aplinka

Ankstesnės procedūros metu įgalinote plėtinius, kurie yra finansinio registravimo tarnybos integravimo pavyzdžio komponentai. Be to, turite atlikti šiuos veiksmus, jei norite kurti diegtinas pakuotes, kuriose yra "Commerce" komponentai, ir taikyti šias pakuotes gamybos aplinkoje.

1. Atlikite šiuos paketo konfigūracijos failų keitimus, nurodytus aplanke **"RetailSdk\\ Assets** ":

    - Konfigūracijos failuose **commerceruntime.ext.config** **ir CommerceRuntime.MPOSOffline.Ext.config** įtraukite **šią eilutę į sudėties** skyrių.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - Konfigūracijos faile **HardwareStation.Extension.config** įtraukite šią eilutę į skyriaus **sudėtį**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Atlikite šiuos pakeitimus **customization.settings** paketo pritaikymo konfigūracijos faile, aplanke **BuildTools**:

    - Įtraukite šią eilutę, kad įtraukumėte CRT plėtinį į diegiamus paketus.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Įtraukite šią eilutę, kad į diegtimus paketus įtraukumėte "Hardware" stoties plėtinį.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Paleiskite MSBuild komandinę Visual Studio eilutę dėl paslaugų programos ir **paleiskite msbuild** "Retail" SDK aplanke, kad sukurtumėte diegiamus paketus.
1. Taikykite paketus naudodami LCS arba rankiniu būdu. Daugiau informacijos ieškokite Create [deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Plėtinių dizainas

Lenkijos fiskalinio spausdintuvo integravimo pavyzdys pagrįstas finansinio [integravimo funkcijomis](fiscal-integration-for-retail-channel.md). Daugiau informacijos apie finansinio integravimo sprendimo dizainą ieškokite finansinio [integravimo pavyzdžio dizaino apžvalgoje](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti konkretaus spausdintuvo dokumentus ir tvarkyti atsakymus iš fiskalinio spausdintuvo.

Plėtinys CRT yra **Runtime.Extensions.DocumentProvider.PosnetSample**. Šis plėtinys sugeneruoja poSNET 19-3678 specifikacijos apibrėžtą "JavaScript Object Notation" (JSON) formato spausdintuvui specialių komandų rinkinį.

Daugiau informacijos apie finansinio integravimo sprendimo dizainą ieškokite [finansinio įrenginių ir paslaugų finansinio integravimo procese ir finansinio integravimo pavyzdžius](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Užklausų apdorojimo programa

**DocumentProviderPosnetProtocol užklausos** apdorojimo programa yra įvesties taškas, per kurį užklausa generuoja dokumentus iš fiskalinio spausdintuvo.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su jungties dokumento teikėjo pavadinimu, kuris nurodytas "Commerce Headquarters".

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje yra informacijos apie tai, koks dokumentas turėtų būti sugeneruotas. Grąžinamas spausdintuvui konkretus dokumentas, kuris turi būti užregistruotas fiskaliniu spausdintuvu.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa pateikia įvykių, prie kurių bus užsiprenumeruoti, sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas ir Z ataskaitos spausdinimas.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra plėtinio **projekto** konfigūracijos aplanke. Failo paskirtis – įgalinti dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais. Pridedami šie parametrai:

- PVM tarifų susiejimas
- Mokėjimo priemonės tipo susiejimas
- Įmokos mokėjimo tipas

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, paskirtis yra palaikyti ryšį su fiskaliniu spausdintuvu.

Aparatūros stoties plėtinys yra **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**. Šis plėtinys išk prašo POSNET tvarkyklės funkcijų pateikti komandas, kurias plėtinys CRT sugeneruoja fiskaliniu spausdintuvu. Ji taip pat tvarko įrenginio klaidas.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

FiscalPrinterHandler **užklausos** apdorojimo programa yra įvesties taškas, skirtas tvarkyti užklausą į fiskalinį per įrenginį.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su "Commerce Headquarters" nurodytu finansinio jungties pavadinimu.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus spausdintuvams ir grąžina atsakymą iš fiskalinio spausdintuvo.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama įrenginio sveikatos patikrai atlikti.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama spausdintuvui inicijuoti.

#### <a name="configuration"></a>Konfigūracija

Konfigūracijos failas yra plėtinio **projekto** konfigūracijos aplanke. Failo paskirtis – įgalinti jungties parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais. Pridedami šie parametrai:

- **Jungimosi** eilutė – eilutė, aprašantys išsamią ryšio su įrenginiu informaciją tvarkyklės palaikomu formatu. Daugiau informacijos ieškokite POSNET tvarkyklės dokumentuose.
- **Datos ir laiko sinchronizavimas** – reikšmė, nurodanti, ar spausdintuvo data ir laikas turi būti sinchronizuoti su prijungta aparatūros stotyje.
- **Įrenginio skirtasis** laikas milisekunde, per kurį vairuotojas lauks atsakymo iš įrenginio. Daugiau informacijos ieškokite POSNET tvarkyklės dokumentuose.
