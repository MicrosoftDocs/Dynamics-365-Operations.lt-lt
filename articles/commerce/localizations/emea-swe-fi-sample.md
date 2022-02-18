---
title: Švedijos kontrolės įtaiso integracijos pavyzdys
description: Šioje temoje pateikiama Švedijos fiskalinės integracijos imties apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: ace1bd5b1a06317b6753a34779ecfa96e519a63e
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077018"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Švedijos kontrolės įtaiso integracijos pavyzdys

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama Švedijos fiskalinės integracijos imties apžvalga Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Ši pavyzdinė fiskalinio integravimo funkcija pakeičia ankstesnę [pavyzdys POS integravimui su valdymo blokais Švedijai](retail-sdk-control-unit-sample.md). Ankstesnis pavyzdys nepasinaudoja [fiskalinės integracijos sistema](./fiscal-integration-for-retail-channel.md) ir vėlesniuose atnaujinimuose bus pasenę. Norėdami gauti informacijos apie tai, kaip pereiti iš ankstesnio pavyzdžio į pavyzdį, kuris atitinka Dynamics 365 Commerce versija **10.0.22 ir anksčiau**, matyti [Perkeliama iš ankstesnio integravimo pavyzdžio](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample).

„Commerce“ funkcija Švedijoje apima pavyzdinį pardavimo vietos (POS) integravimą su Švedijai būdingais mokesčių įrenginiais, žinomais kaip *valdymo blokai*. Šis pavyzdys išplečia [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md). Daroma prielaida, kad valdymo blokas yra fiziškai prijungtas prie aparatinės įrangos stoties, su kuria POS yra susietas. Pavyzdžiui, šiame pavyzdyje naudojama programų programavimo sąsaja (API).[CleanCash A tipas](https://www.retailinnovation.se/produkter) valdymo blokas Retail Innovation HTT AB. Naudojama CleanCash API 1.1.4 versija.

Pavyzdys pateikiamas šaltinio kodo forma ir yra mažmeninės prekybos programinės įrangos kūrimo rinkinio (SDK) dalis.

„Microsoft“ neišleidžia jokios aparatinės įrangos, programinės įrangos ar dokumentų iš „Retail Innovation HTT AB“. Norėdami gauti informacijos apie tai, kaip gauti valdymo bloką ir jį valdyti, susisiekite su [Retail Innovation HTT AB](https://www.retailinnovation.se/).

## <a name="scenarios"></a>Scenarijai

Švedijos valdymo bloko integravimo pavyzdys apima šias galimybes:

- Pardavimo, grąžinimo ir kvitų kopijos automatiškai registruojamos valdymo bloke, kuris yra prijungtas prie aparatinės įrangos stoties, susietos su POS.
- Registruotos operacijos valdymo bloko valdymo kodas ir gamybos numeris paimami iš valdymo bloko ir išsaugomi operacijoje. Šie duomenys taip pat vadinami a *fiskalinis atsakas*. Fiskalinį atsakymą galite peržiūrėti **Sandoriai parduotuvėje** puslapį.
- Prie kvito maketo galima pridėti pasirinktinius valdymo kodo ir valdymo bloko gamybos numerio laukus. Tokiu būdu kvite galite atspausdinti operacijos fiskalinį atsakymą.
- Operacijos fiskalinis atsakas rodomas **Elektroninis žurnalas (Švedija)** kanalo ataskaita.
- Galimos kelios klaidų valdymo parinktys. Štai keletas pavyzdžių:

    - Pabandykite dar kartą registruoti fiskalinę informaciją, jei įmanoma. Galite iš naujo bandyti fiskalinę registraciją, jei, pavyzdžiui, valdymo blokas neprijungtas, nėra pasirengęs arba nereaguoja.
    - Atidėti fiskalinę registraciją.
    - Praleiskite fiskalinę registraciją arba pažymėkite operaciją kaip registruotą ir įtraukite informacinius kodus, kad užfiksuotumėte gedimo priežastį ir papildomą informaciją.
    - Prieš atidarant naują pardavimo operaciją arba užbaigiant pardavimo operaciją, patikrinkite valdymo bloko prieinamumą.

### <a name="limitations-of-the-sample"></a>Mėginio apribojimai

Švedijos valdymo bloko integravimo pavyzdys šiuo metu nepalaiko klientų užsakymų scenarijų.

## <a name="setting-up-the-integration-with-control-units"></a>Integracijos su valdymo blokais nustatymas

Daugiau informacijos apie Švedijai reikalingą sąranką žr [Švedijos komercijos nustatymas](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden).

### <a name="configuring-swedenspecific-receipts"></a>Švedijai būdingų kvitų konfigūravimas

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruokite pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Galite konfigūruoti kalbos tekstą ir pasirinktinius laukus, kurie naudojami POS kvitų formatuose. Numatytoji kvito sąranką kuriančio vartotojo įmonė turėtų būti tas pats juridinis asmuo, kuriame sukurta kalbos teksto sąranka. Arba tos pačios kalbos tekstai turėtų būti sukurti ir vartotojo numatytoje įmonėje, ir parduotuvės, kuriai sukurta sąranka, juridiniame subjekte.

Ant **Kalbos tekstas** puslapyje pridėkite šiuos kvito maketų pasirinktinių laukų etikečių įrašus. Atkreipkite dėmesį, kad **Kalbos ID**, **ID**, ir **Tekstas** lentelėje pateiktos vertės yra tik pavyzdžiai. Galite juos pakeisti, kad atitiktų jūsų poreikius. Tačiau, **Teksto ID** naudojamos reikšmės turi būti unikalios ir lygios arba didesnės už 900001.

Pridėkite šias POS etiketes **POS** skyrių **Kalbos tekstas** puslapį.

| Kalbos ID | Teksto ID | Tekstas                  |
|-------------|---------|-----------------------|
| en-US       | 900001  | Užregistruokite valdymo kodą |
| en-US       | 900002  | Užregistruokite įrenginį       |

Ant **Pasirinktiniai laukai** puslapyje pridėkite toliau nurodytus kvito maketų pasirinktinių laukų įrašus. Prisimink tai **Antraštės teksto ID** reikšmės turi atitikti **Teksto ID** vertes, kurias nurodėte **Kalbos tekstas** puslapį.

| Pavadinimas                         | Tipas    | Vaizdo aprašo teksto ID |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Gavimas | 900001          |
| SE_FISCALREGISTERID          | Gavimas | 900002          |

> [!NOTE]
> Svarbu nurodyti teisingus tinkintų laukų pavadinimus, kaip nurodyta aukščiau esančioje lentelėje. Dėl neteisingo tinkinto lauko pavadinimo kvituose trūks duomenų.

#### <a name="configure-receipt-formats"></a>Konfigūruoti kvitų formatus

Kiekvienam reikalaujamam kvito formatui pakeiskite reikšmę **Spausdinimo elgsena** laukas į **Visada spausdinkite**.

Kvito formato dizainerėje pridėkite šiuos pasirinktinius laukus prie **Poraštė** skyrius. Atminkite, kad laukų pavadinimai atitinka kalbos tekstus, kuriuos apibrėžėte ankstesniame šios temos skyriuje.

- **Užregistruokite valdymo kodą** – Šiame lauke išspausdinamas valdymo kodas.
- **Užregistruokite įrenginį** – Šiame lauke spausdinamas valdymo bloko gamybos numeris.

Norėdami gauti daugiau informacijos apie tai, kaip dirbti su kvito formatais, žr [Kvitų šablonai ir spausdinimas](../receipt-templates-printing.md).

### <a name="set-up-fiscal-integration-for-sweden"></a>Nustatyti Švedijos fiskalinę integraciją

Švedijos valdymo bloko integravimo pavyzdys yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ Fiskalinė integracija\\ CleanCash** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla (pvz.[išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Pavyzdys [susideda](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) mokesčių dokumentų teikėjo, kuris yra komercijos vykdymo laiko pratęsimas (CRT) ir fiskalinę jungtį, kuri yra „Commerce Hardware Station“ plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti mažmeninės prekybos SDK, žr [Mažmeninės prekybos SDK architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) ir [Nustatykite nepriklausomo pakavimo SDK kūrimo procesą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo virtualioje mašinoje (VM).Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS). Daugiau informacijos žr [Švedijos valdymo bloko integravimo pavyzdžio diegimo gairės (palikimas)](emea-swe-fi-sample-sdk.md).
>
> Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

Atlikite fiskalinės integracijos sąrankos veiksmus, kaip aprašyta [Nustatykite fiskalinį prekybos kanalų integravimą](setting-up-fiscal-integration-for-retail-channel.md).

1. [Nustatykite fiskalinės registracijos procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taip pat atkreipkite dėmesį į fiskalinės registracijos proceso nustatymus [būdingas šiam valdymo bloko integravimo pavyzdžiui](#set-up-the-registration-process).
1. [Nustatykite klaidų tvarkymo nustatymus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Įgalinti atidėtos fiskalinės registracijos vykdymą rankiniu būdu](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nustatykite registracijos procesą

Norėdami įjungti registracijos procesą, atlikite šiuos veiksmus, kad nustatytumėte „Commerce“ būstinę. Daugiau informacijos žr [Nustatykite fiskalinį prekybos kanalų integravimą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųskite mokesčių dokumentų teikėjo ir fiskalinės jungties konfigūracijos failus:

    1. Atidaryk [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla.
    1. Pasirinkite tinkamą leidimo šakos versiją pagal savo SDK / programos versiją (pvz.,**[išleidimas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Atviras **src \> Fiskalinė integracija \> CleanCash**.
    1. Atsisiųskite fiskalinio dokumento teikėjo konfigūracijos failą adresu **CommerceRuntime \> DocumentProvider.CleanCashSample \> Konfigūracija \> DocumentProviderFiscalCleanCashSample.xml** (pavyzdžiui, [išleidimo failas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)).
    1. Atsisiųskite fiskalinės jungties konfigūracijos failą adresu **HardwareStation \> Jungtis.CleanCashSample \> Konfigūracija \> ConnectorCleanCashSample.xml** (pavyzdžiui, [išleidimo failas/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)).

    > [!WARNING]
    > Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Šio fiskalinio integravimo pavyzdžio konfigūracijos failai yra šiuose mažmeninės prekybos SDK aplankuose kūrėjo VM LCS:
    >
    > - **Fiskalinio dokumento teikėjo konfigūracijos failas:** RetailSdk\\ Extensions pavyzdys\\ CommerceRuntime\\ Extensions.DocumentProvider.CleanCashSample\\ Konfigūracija\\ DocumentProviderFiscalCleanCashSample.xml
    > - **Fiskalinės jungties konfigūracijos failas:** RetailSdk\\ Extensions pavyzdys\\ HardwareStation\\ Extension.CleanCashSample\\ Konfigūracija\\ ConnectorCleanCashSample.xml
    > 
    > Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**. Ant **Generolas** skirtuką, nustatykite **Įgalinti fiskalinę integraciją** galimybė į **Taip**.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinių dokumentų teikėjai** ir įkelkite fiskalinio dokumento teikėjo konfigūracijos failą, kurį atsisiuntėte anksčiau.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinės jungtys** ir įkelkite fiskalinės jungties konfigūracijos failą, kurį atsisiuntėte anksčiau.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Jungčių funkciniai profiliai**. Sukurkite naują jungties funkcinį profilį. Pasirinkite dokumento teikėją ir jungtį, kurią įkėlėte anksčiau. Atnaujinkite [duomenų atvaizdavimo nustatymus](#default-data-mapping) kaip reikalaujama.
1. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Jungčių techniniai profiliai**. Sukurkite naują jungties techninį profilį ir pasirinkite fiskalinę jungtį, kurią įkėlėte anksčiau. Atnaujinkite [jungties nustatymai](#fiscal-connector-settings) kaip reikalaujama.
6. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinių jungčių grupės**. Sukurkite naują fiskalinių jungčių grupę jungties funkciniam profiliui, kurį sukūrėte anksčiau.
7. Eiti į **Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinės registracijos procesai**. Sukurkite naują fiskalinės registracijos procesą ir fiskalinės registracijos proceso veiksmą ir pasirinkite anksčiau sukurtą fiskalinių jungčių grupę.
8. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų profilį, susietą su parduotuve, kurioje turėtų būti suaktyvintas registracijos procesas. Ant **Fiskalinės registracijos procesas** FastTab, pasirinkite fiskalinės registracijos procesą, kurį sukūrėte anksčiau.
9. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**. Pasirinkite aparatūros profilį, susietą su aparatūros stotimi, prie kurios bus prijungtas fiskalinis spausdintuvas. Ant **Fiskaliniai periferiniai įrenginiai** FastTab, pasirinkite jungties techninį profilį, kurį sukūrėte anksčiau.
10. Atidarykite platinimo tvarkaraštį (**Mažmeninė prekyba ir prekyba \> Mažmeninė prekyba ir IT \> Platinimo grafikas**) ir pasirinkite darbus **1070** ir **1090** perkelti duomenis į kanalo duomenų bazę.

#### <a name="default-data-mapping"></a>Numatytasis duomenų atvaizdavimas

Šis numatytasis duomenų atvaizdavimas įtrauktas į fiskalinio dokumento teikėjo konfigūraciją, kuri pateikiama kaip fiskalinės integracijos pavyzdžio dalis:

- **Pridėtinės vertės mokesčio (PVM) kodų atvaizdavimas** – Šis susiejimas nustato konkrečiam įrenginiui taikomus pridėtinės vertės mokesčio (PVM) kodus į atitinkamus pardavimo mokesčio kodus. PVM kodo atvaizdavimas turi būti tokio formato:

    ```
    1 : code1 ; 2 : code2
    ```

    Toliau pateikiamas šio formato paaiškinimas.

    - *1* ir *2* yra konkretaus įrenginio PVM kodai.
    - Kabliataškis (;) naudojamas kaip skyriklis.
    - *kodas1* ir *kodas2* yra pardavimo mokesčių kodai, sukonfigūruoti „Commerce“ būstinėje. Turite modifikuoti pavyzdinį susiejimą pagal mokesčių kodus, kurie sukonfigūruoti jūsų programoje.

    Valdymo blokai palaiko iki keturių skirtingų PVM kodų. Todėl PVM kodo susiejimas gali būti nustatytas taip:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Keli pardavimo mokesčių kodai gali būti susieti su tuo pačiu konkretaus įrenginio PVM kodu.

#### <a name="fiscal-connector-settings"></a>Fiskalinės jungties nustatymai

Šie nustatymai įtraukti į fiskalinės jungties konfigūraciją, kuri pateikiama kaip fiskalinės integracijos pavyzdžio dalis:

- **Ryšių eilutė** – Valdymo bloko prijungimo nustatymai.
- **Laikas baigėsi** – Laikas milisekundėmis, per kurį vairuotojas lauks atsakymo iš valdymo bloko.

### <a name="configure-channel-components"></a>Konfigūruokite kanalo komponentus

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Daugiau informacijos žr [Švedijos valdymo bloko integravimo pavyzdžio diegimo gairės (palikimas)](emea-swe-fi-sample-sdk.md).
>
> Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

#### <a name="set-up-the-development-environment"></a>Nustatykite kūrimo aplinką

Norėdami nustatyti kūrimo aplinką pavyzdžiui išbandyti ir išplėsti, atlikite šiuos veiksmus.

1. Klonuokite arba atsisiųskite [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugykla. Pasirinkite tinkamą leidimo šakos versiją pagal savo SDK / programos versiją. Daugiau informacijos žr [Atsisiųskite mažmeninės prekybos SDK pavyzdžius ir nuorodų paketus iš „GitHub“ ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite valdymo bloko integravimo sprendimą adresu **Dynamics365Commerce.Solutions\\ Fiskalinė integracija\\ CleanCash\\ CleanCash.sln**, ir pastatyti jį.
1. Diegti CRT plėtiniai:

    1. Surask CRT plėtinio diegimo programa:

        - **Prekybos masto vienetas:** Viduje konors **CleanCash\\ ScaleUnit\\ ScaleUnit.CleanCash.Installer\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **ScaleUnit.CleanCash.Installer** montuotojas.
        - **Vietinis CRT Šiuolaikinėje POS:** Viduje konors **CleanCash\\ Šiuolaikinis POS\\ ModernPOS.CleanCash.Installer\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **ModernPOS.CleanCash.Installer** montuotojas.

    2. Pradėkite CRT plėtinio diegimo programa iš komandinės eilutės:

        - **Prekybos masto vienetas:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Vietinis CRT Šiuolaikinėje POS:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Įdiekite aparatinės įrangos stoties plėtinius:

    1. Viduje konors **CleanCash\\ HardwareStation\\ HardwareStation.CleanCash.Installer\\ šiukšliadėžė\\ Derinimas\\ net461** aplanką, suraskite **HardwareStation.CleanCash.Installer** montuotojas.
    1. Paleiskite plėtinio diegimo programą iš komandinės eilutės:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Atlikite nurodytus veiksmus [Nustatykite fiskalinės integracijos pavyzdžio kūrimo dujotiekį](fiscal-integration-sample-build-pipeline.md) sugeneruoti ir išleisti Cloud Scale Unit ir savitarnos dislokuojamus paketus fiskalinės integracijos pavyzdžiui. The **CleanCash build-pipeline.yml** šablono YAML failą galima rasti **Dujotiekis\\ YAML_Failai** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugykla.

## <a name="design-of-the-extensions"></a>Prailginimų dizainas

Švedijos valdymo bloko integravimo pavyzdys yra pagrįstas [fiskalinės integracijos funkcionalumas](fiscal-integration-for-retail-channel.md) ir yra mažmeninės prekybos SDK dalis. Pavyzdys yra **src\\ Fiskalinė integracija\\ CleanCash** aplankas [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla (pvz.[išleidimo pavyzdys/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Pavyzdys [susideda](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) mokesčių dokumentų teikėjo, kuris yra pratęsimas CRT ir fiskalinė jungtis, kuri yra „Commerce Hardware Station“ plėtinys. Norėdami gauti daugiau informacijos apie tai, kaip naudoti mažmeninės prekybos SDK, žr [Mažmeninės prekybos SDK architektūra](../dev-itpro/retail-sdk/retail-sdk-overview.md) ir [Nustatykite nepriklausomo pakavimo SDK kūrimo procesą](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Dėl apribojimų [naujas nepriklausomas pakuotės ir prailginimo modelis](../dev-itpro/build-pipeline.md), šiuo metu jo negalima naudoti šiam fiskalinės integracijos pavyzdžiui. Turite naudoti ankstesnę mažmeninės prekybos SDK versiją kūrėjo VM sistemoje LCS. Daugiau informacijos žr [Švedijos valdymo bloko integravimo pavyzdžio diegimo gairės (palikimas)](emea-swe-fi-sample-sdk.md). Naujos nepriklausomos pakuotės ir fiskalinės integracijos pavyzdžių išplėtimo modelio palaikymas planuojamas vėlesnėse versijose.

### <a name="crt-extension-design"></a>CRT pratęsimo dizainas

Plėtinio, kuris yra fiskalinių dokumentų teikėjas, tikslas yra generuoti su paslauga susijusius dokumentus ir tvarkyti valdymo bloko atsakymus.

#### <a name="request-handler"></a>Užklausų tvarkytojas

Yra vienas **DocumentProviderCleanCash** dokumentų teikėjo užklausų tvarkytojas. Šis tvarkytuvas naudojamas valdymo bloko fiskaliniams dokumentams generuoti.

Šis tvarkytuvas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Valdiklio pavadinimas turi atitikti jungties dokumento teikėjo pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – Šioje užklausoje pateikiama informacija apie tai, koks dokumentas turi būti sugeneruotas. Jis grąžina konkrečiai paslaugai skirtą dokumentą, kuris turi būti užregistruotas valdymo bloke.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Ši užklausa grąžina prenumeruojamų įvykių sąrašą. Šiuo metu palaikomi pardavimo ir audito renginiai.

#### <a name="configuration"></a>Konfigūracija

Fiskalinio dokumento teikėjo konfigūracijos failas yra adresu **src\\ Fiskalinė integracija\\ CleanCash\\ CommerceRuntime\\ DocumentProvider.CleanCashSample\\ Konfigūracija\\ DocumentProviderFiscalCleanCashSample.xml** viduje konors [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla. Šio failo tikslas – įgalinti dokumentų teikėjo nustatymus, kurie būtų konfigūruojami iš „Commerce“ būstinės. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Techninės įrangos stoties išplėtimo projektavimas

Plėtinio, kuris yra fiskalinė jungtis, tikslas yra susisiekti su valdymo bloku. Jis naudoja HTTP protokolą, kad pateiktų dokumentus, kuriuos CRT plėtinys generuoja valdymo bloką. Ji taip pat tvarko atsakymus, gautus iš valdymo bloko.

#### <a name="request-handler"></a>Užklausų tvarkytojas

The **CleanCashHandler** užklausų tvarkytojas yra įvesties taškas, skirtas tvarkyti užklausas į valdymo bloką.

Prižiūrėtojas yra paveldėtas iš **INamedRequestHandler** sąsaja. The **Valdytojo vardas** metodas yra atsakingas už tvarkytojo vardo grąžinimą. Droviklio pavadinimas turi atitikti fiskalinės jungties pavadinimą, nurodytą „Commerce“ būstinėje.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – Ši užklausa siunčia dokumentus į valdymo bloką ir grąžina iš jo atsakymą.
- **IsReadyFiscalDeviceRequest** – Ši užklausa naudojama valdymo bloko sveikatos patikrinimui.
- **InitializeFiscalDeviceRequest** – Ši užklausa naudojama valdymo blokui inicijuoti.

#### <a name="configuration"></a>Konfigūracija

Fiskalinės jungties konfigūracijos failas yra adresu **src\\ Fiskalinė integracija\\ CleanCash\\ HardwareStation\\ Jungtis.CleanCashSample\\ Konfigūracija\\ ConnectorCleanCashSample.xml** viduje konors [Dynamics 365 Commerce Sprendimai](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugykla. Failo tikslas – įgalinti fiskalinės jungties nustatymus, kuriuos būtų galima konfigūruoti „Commerce“ būstinėje. Failo formatas suderintas su fiskalinės integracijos konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
