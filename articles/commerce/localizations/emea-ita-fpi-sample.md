---
title: Fiskalinio spausdintuvo integracijos pavyzdys (Italija)
description: Šiame straipsnyje pateikta Italijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-11-01
ms.openlocfilehash: 6ad97e87e4114a8f2250d0ba4880b7a466b3689e
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631402"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Fiskalinio spausdintuvo integracijos pavyzdys (Italija)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šiame straipsnyje pateikta Italijos finansinio integravimo pavyzdžio apžvalga Microsoft Dynamics 365 Commerce.

Italijos komercijos funkcijos apima ir elektroninį pardavimą (EKA) su iždo dokumentų spausdintuvu. [...](fiscal-integration-for-retail-channel.md)[Pavyzdys išplečia fiskalinio integravimo funkcijas, kad jis veikia su Epson FP-90II](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) serijos spausdintuvais iš Epson ir įgalina ryšį su fiskaliniu spausdintuvu žiniatinklio serverio režimu per EpsonFPMate žiniatinklio tarnybą, naudodama fiskalinę ePOS-print API. Pavyzdys palaiko tik Registratore Telematinio (RT) režimą. Pavyzdys pateikiamas šaltinio kodo forma ir yra "Commerce" programinės įrangos kūrimo rinkinio (SDK) dalis.

"Microsoft" neišleidžia jokios aparatūros, programinės įrangos ar dokumentacijos iš Epson. Norėdami gauti informacijos apie tai, kaip gauti fiskalinį spausdintuvą ir jį valdyti, susisiekite [su Epson S.p.A.](https://www.epson.it)

## <a name="scenarios"></a>Scenarijai

Šiuos scenarijus apima Italijos fiskalinio spausdintuvo integravimo pavyzdys:

- Pardavimo scenarijai:

    - Išspausdinkite fiskalinį grynųjų pinigų ir atliekamo pardavimo ir grąžinimo kvitą.
    - Perimti fiskalinio spausdintuvo atsakymą ir saugoti jį kanalo duomenų bazėje.
    - Mokesčiai:

        - Susieti su fiskalinio spausdintuvo mokesčių kodais (padaliniais).
        - Perkelkite susietus mokesčių duomenis į fiskalinį spausdintuvą.
        - Spausdinti finansinio kvito mokesčius.

    - Mokėjimai:

        - Susiekite su fiskalinio spausdintuvo mokėjimo metodais.
        - Spausdinti mokėjimus finansinio kvito metu.
        - Spausdinti keitimo informaciją.

    - Spausdinti eilutės nuolaidas.
    - Dovanų kortelės:

        - Iš pardavimo finansinio kvito pašalinti išduotą / iš naujo apmokestinamą dovanų kortelės eilutę.
        - Spausdinti mokėjimą, kuris naudoja dovanų kortelę kaip reguliarų mokėjimo būdą.

    - Spausdinti kliento užsakymo operacijų finansinius kvitus:

        - Nespausdinamas kliento užsakymo depozito finansinis kvitas.
        - Spausdinti finansinis kvitas, skirtas atlikti kliento užsakymo eilutes.
        - Spausdinti kliento užsakymo paėmimo operacijos fiskalinį kvitą.
        - Spausdinti grąžinimo užsakymo fiskalinį kvitą.

    - Išspausdinkite finansinio kvito kvito numerio brūkšninius kodus.
    - [Spausdinti kliento informaciją](emea-ita-customer-information.md), nurodytą finansinio kvito pardavimo operacijai. Šios informacijos pavyzdys yra kliento eilutės kodas. 

- Dienos pabaigos išrašai (X finansiniai ir finansiniai Z ataskaitos).
- Klaidos tvarkymą, pvz., šias pasirinktis:

    - Jei galima kartoti registraciją, pvz., jei fiskalinis spausdintuvas neprijungtas, neparuoštas arba neatsako, spausdintuvas neparuoštas, popierius arba yra popieriaus strigtis.
    - Atidėjimo finansinio registravimas.
    - Praleisti ataskaitinį registravimą arba pažymėti operaciją kaip užregistruotą ir įtraukti informacijos kodus, kad būtų fiksuojama trikties priežastis ir papildoma informacija.
    - Patikrinkite fiskalinio spausdintuvo pasiekiamumą prieš atidarę naują pardavimo operaciją arba kai pardavimo operacija baigiama.

### <a name="gift-cards"></a>Dovanų kortelės

Fiskalinio spausdintuvo integravimo pavyzdys vykdo šias taisykles, susijusias su dovanų kortelėmis:

- Pašalinti pardavimo eilutes, susijusias su dovanų kortelės *išdavimo ir įtraukti į* *dovanų kortelės operacijas* iš finansinio kvito.
- Nespausdinti finansinio kvito, jei jį sudaro tik dovanų kortelės eilutės.
- Atskaityti bendrą dovanų kortelių, kurios išduotos arba perskaičiuojamos iš operacijos, sumą iš finansinio kvito mokėjimo eilučių.
- Įrašykite apskaičiuotus mokėjimo eilučių koregavimus kanalo duomenų bazėje su nuoroda į atitinkamą fiskalinę operaciją.
- Mokėjimas dovanų kortele laikomas įprastu mokėjimu.

### <a name="customer-deposits-and-customer-order-deposits"></a>Kliento depozitai ir kliento užsakymo depozitai

Fiskalinio spausdintuvo integravimo pavyzdys vykdo šias taisykles, susijusias su kliento depozitais ir kliento užsakymo depozitais:

- Nespausdinti finansinio kvito, jei operacija yra kliento depozitas.
- Nespausdinti finansinio kvito, jei operacijoje yra tik kliento užsakymo depozitas arba kliento užsakymo depozito grąžinimas.
- Spausdinti kliento užsakymo paėmimo operacijos finansinio kvito anksčiau sumokėto depozito sumą.
- Atskaityti kliento užsakymo depozito sumą iš mokėjimo eilučių, kai sukurtas kliento užsakymas.
- Įrašykite apskaičiuotus mokėjimo eilučių koregavimus kanalo duomenų bazėje su nuoroda į kliento užsakymo ataskaitinę operaciją.

### <a name="limitations-of-the-sample"></a>Pavyzdžio apribojimai

- Fiskalinis spausdintuvas palaiko tik scenarijus, kuriuose PVM įtraukiamas į kainą. Todėl parduotuvių **ir klientų parinktis** Kaina su PVM turi **būti** nustatyta kaip Taip.
- Kasdienės ataskaitos (finansinis X ir finansinis Z) spausdinamos naudojant formatą, kuris yra įdėtas į fiskalinio spausdintuvo vedlį.
- Fiskalinis spausdintuvas nepalaiko įvairių operacijų. **EKA funkcijų šablonuose turi būti nustatyta** Parinkties Uždrausti maišymą ir **grąžinimą** viena kvito pasirinktis Kaip Taip.
- Pavyzdys palaiko integravimą tik su fiskaliniu spausdintuvu, kuris veikia registratore Telematinio (RT) režimu.

## <a name="set-up-fiscal-integration-for-italy"></a>Nustatyti Italijos finansų integravimą

Italijos fiskalinio spausdintuvo integravimo pavyzdys pagrįstas finansinio [integravimo funkcija](fiscal-integration-for-retail-channel.md) ir yra "Commerce SDK" dalis. Pavyzdys yra sprendimų saugyklos **src\\ FiscalIntegration\\ EpsonFP90IISample**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke. Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas, kuris yra "Commerce Runtime (CRT) plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie "Commerce SDK" naudojimą, [žr. "Download Commerce SDK" pavyzdžius ir nuorodų paketus iš GitHub NuGet](../dev-itpro/retail-sdk/sdk-github.md)[ir nustatykite nepriklausomos pakuotės SDK pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Italijos fiskalinio spausdintuvo integravimo pavyzdys yra "Commerce SDK", kuris naudojamas "Commerce" versijoje 10.0.29. Naudojant "Commerce" 10.0.28 arba senesnę versiją, reikia naudoti ankstesnę "Retail SDK" versiją programavimo virtualiojoje kompiuteryje (VM) Microsoft Dynamics ciklo tarnybose (LCS). Daugiau informacijos ieškokite Italijos [(senesnės programos) fiskalinio spausdintuvo integravimo pavyzdžio diegimo rekomendacijose](emea-ita-fpi-sample-sdk.md).

Atlikite finansinio integravimo nustatymo veiksmus, kaip aprašyta ["Commerce" kanalų finansinio integravimo nustatymas](setting-up-fiscal-integration-for-retail-channel.md).

1. [Nustatykite finansinio registravimo procesą](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Taip pat pasižymėkite finansinio registravimo proceso parametrus, bvz., šio [fiskalinio spausdintuvo integravimo pavyzdį](#set-up-the-registration-process).
1. [Nustatyti nuolaidų finansinius tekstus](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Nustatyti klaidų tvarkymo parametrus](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [EKA nustatykite finansų X/Z ataskaitas](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Įgalinkite atidėtų finansinių duomenų registravimą neautomatiniu būdu](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).
1. [Nustatykite kliento informacijos valdymo funkcijas EKA](emea-ita-customer-information.md#setup).
1. [Sukonfigūruokite kanalo komponentus](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nustatyti registravimo procesą

Norėdami įjungti registravimo procesą, atlikite šiuos veiksmus norėdami nustatyti "Commerce Headquarters". Daugiau informacijos rasite "Commerce [" kanalų finansinio integravimo nustatykite](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Atsisiųsti finansinio dokumento teikėjo ir fiskalinio jungties konfigūracijos failus:

    1. Atidaryti sprendimų [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) saugyklą.
    1. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją.
    1. Atidarykite **src \> FiscalIntegration \> EpsonFP90IIIAMple**.
    1. **Atsisiųskite finansinio dokumento teikėjo konfigūracijos failą commerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Konfigūracijos \> DocumentProviderEpsonFP90IIISample.xml**.
    1. Atsisiųskite finansinio **jungties konfigūracijos failą, kurį naudojant HardwareStation \> EpsonFP90IIIFiscalDeviceSample \> Configuration \> ConnectorEpsonFP90IISample.xml**.

    > [!NOTE]
    > Naudojant "Commerce" 10.0.28 arba senesnę versiją, LCS kūrėjui VM reikia naudoti ankstesnę "Retail SDK" versiją. Šio fiskalinio integravimo pavyzdžio konfigūracijos failai yra toliau esančiuuose "Retail" SDK, esantis LCS programuotojo VM, aplankuose:
    >
    > - **Iždo dokumentų teikėjo konfigūracijos failas:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ extension.DocumentProvider.EpsonFP90IIIISample\\ Configuration\\ DocumentProviderEpsonFP90IIIISample.xml
    > - **Iždo jungties konfigūracijos failas:** RetailSdk\\ SampleExtensions\\ HardwareStation\\ extension.EpsonFP90IIIFiscalDeviceSample\\ Configuration\\ ConnectorEpsonFP90IIISample.xml

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**. Skirtuke **Bendra** nustatykite pasirinktį **Įgalinti finansų integravimą** kaip **Taip**.
1. Eikite į **"Retail" ir "Commerce \> Channel" \> nustatymą "Fiscal integration \> Fiscal"** dokumentų teikėjai ir įkelkite anksčiau atsisiųstą fiskalinio dokumento teikėjo konfigūracijos failą.
1. Eikite į **"Retail" ir "Commerce Channel" \> nustatymą "Fiscal integration \> Fiscal \>" jungtis ir įkelkite anksčiau atsisiųstą "Fiscal** Connector" konfigūracijos failą.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" funkcinius profilius**. Sukurti naują jungties funkcinį profilį. Pasirinkite anksčiau įkeltą dokumento teikėją ir jungtį. Pagal reikia [atnaujinti duomenų susiejimo](#default-data-mapping) parametrus.
1. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Connector" techninius profilius**. Sukurkite naują jungties techninio profilio ir pasirinkite anksčiau įkeltą fiskalinę jungtį. Pagal reikiamą [parametrų versiją atnaujinkite](#fiscal-connector-settings) jungties parametrus.
6. Eikite į " **Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Fiscal" jungties grupes**. Sukurkite naują anksčiau sukurto jungties funkcinių profilių finansinių jungčių grupę.
7. Eikite į **"Retail" ir "Commerce \> Channel" nustatymo \> "Fiscal integration \> Fiscal" registracijos procesus**. Sukurkite naują finansinio registravimo procesą ir finansinio registravimo proceso veiksmą, tada pasirinkite anksčiau sukurtą finansinių jungčių grupę.
8. Eikite į **Mažmeninį prekyba ir komercija \> Kanalo sąranka \> EKA sąranka \> EKA profiliai \> Funkcionalumo profiliai**. Pasirinkite funkcijų šabloną, susietą su parduotuve, kurioje turi būti suaktyvintas registracijos procesas. Finansinio registravimo **proceso "** FastTab" pasirinkite anksčiau sukurtą finansinio registravimo procesą.
9. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**. Pasirinkite aparatūros šabloną, susietą su aparatūros stotiu, prie kurios bus prijungtas fiskalinis spausdintuvas. **"FastTab" Iždo išoriniuose** įrenginiuose pasirinkite senesnę jungtį sukūrusį techninio profilio jungtį.
10. Atidarykite paskirstymo grafiką (**"Retail and Commerce Retail ir Commerce \> IT \> Distribution"** grafiką) **ir pasirinkite užduotis 1070** **ir 1090**, kad duomenys būtų perkelti į kanalo duomenų bazę.

#### <a name="default-data-mapping"></a>Numatytųjų duomenų susiejimas

Toliau pateiktas numatytasis duomenų susiejimas yra įtrauktas į finansinio dokumento teikėjo konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdžio dalis:

- **Mokėjimo priemonės tipo** susiejimas – mokėjimo būdų, kurie sukonfigūruoti parduotuvei ir mokėjimo tipams, kuriuos palaiko fiskalinis spausdintuvas, susiejimas. Šiame pavyzdyje rodomas numatytasis susiejimas.

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    Čia pateikiamas šio susiejimo atributų paaiškinimas:

    - **StorePaymentMethod** yra mokėjimo būdas, nustatytas parduotuvei "Retail" ir " **Commerce \> Channel" mokėjimo \> būdų \> mokėjimo metoduose**.
    - **PrinterPaymentType** ir **PrinterPaymentIndex** yra atitinkamas mokėjimo tipas ir indeksas, nurodyti Epson fiskalinio spausdintuvo dokumentuose.
    - **DepositPaymentMethod** naudojamas spausdintuvo mokėjimo tipui ir kliento užsakymo paėmimo sumos, sudengtos su kliento užsakymo depozitu, daliai nurodyti ir indeksui.

    Šioje lentelėje parodyta, kaip mokėjimo būdų pavyzdžio susiejimas atitinka parduotuvės mokėjimo metodus, kurie sukonfigūruoti standartiniuose demonstraciniai duomenyse.

    | Mokėjimo būdas | Mokėjimo būdo pavadinimas |
    |----------------|---------------------|
    | 1              | Grynieji pinigai                |
    | 3              | Kortelė                |
    | 4              | Kliento kodas    |
    | 6              | Valiuta            |
    | 8              | Dovanų kortelė           |

    Turite modifikuoti pavyzdžio susiejimą pagal mokėjimo metodus, kurie sukonfigūruoti jūsų programoje.

- **Kvito numerio brūkšninio kodo** tipas – brūkšninio kodo tipas, naudojamas norint finansinio kvito kvito numerį rodyti. Numatytasis susiejimas yra **CODE128**.
- **Kvito antraštėje spausdinti finansinius duomenis** – jei šis parametras įjungtas, parduotuvės informacija bus spausdinama finansinio kvito kvite. Ši informacija apima parduotuvės pavadinimą, adresą, mokesčių identifikavimo numerį ir kasininko vardą bei pavardę.
- **Iždo dokumentų spausdintuvo padalinio** susiejimas – fiskalinio spausdintuvo padalinių susiejimas su pridėtinės vertės mokesčio (PVM) tarifais, PVM neapmokestinimo pobūdis ir produktų tipais. Šiame pavyzdyje rodomas numatytasis susiejimas.

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    Čia pateikiamas šio susiejimo atributų paaiškinimas:

    - **VATRate** yra palaikomas PVM tarifas, sukonfigūruotas kaip PVM kodas. Susiejimo reikšmėje yra du skaitmenys po dešimtainio kablelio, tačiau nėra dešimtainio skyriklio. Pavyzdžiui, **2200 reiškia** 22 procentus, **o 1000 reiškia** 10 procentų.
    - **VATExemptNature** taikoma tik tais atvejais, kai PVM tarifas yra 0 (nulis), įskaitant atvejus, kai nėra mokesčio. Šiuo metu **VATExemptNature** palaikomas tik dovanų kortelėms, **o susiejimo vertė turi atitikti XML konfigūracijos faile ypatybės VATExemptNatureForGiftCard** vertę.
    - **ProductType** yra produkto tipas. **Vertė 0 reiškia** prekes, o 1 vertė **reiškia** paslaugas.
    - **DepartmentNumber** yra padalinio, sukonfigūruoto spausdintuve ir atitinkančio ankstesnius tris atributus, numeris.

    Turite modifikuoti pavyzdžio susiejimą pagal PVM tarifus, sukonfigūruotus jūsų programoje, ir atitinkamus padalinius, kurie sukonfigūruoti jūsų fiskalinio spausdintuvo.

- **PVM neapmokestinimo pobūdis, skirtas** dovanų kortelei – PVM neapmokestinimo pobūdis, kuris turi būti taikomas išrašus arba pildus dovanų kortelę. Reikšmė turi atitikti tam tikrą iždo dokumentų spausdintuvo padalinio susiejimo įrašą. Numatytasis susiejimas yra **NS**.
- **Įgalinti laisvas prekes** – jei šis parametras įjungtas, prekių, kurios turi 100 procentų nuolaidą, *specialus oma discount* koregavimo tipas.
- **Grąžinimo kilmės informacijos kodas** – informacijos kodas, naudojamas grąžinimo operacijos kilmei fiksuoti, jei pateikiamas joks pradinis pardavimo kvitas. Šis **parametras** **naudojamas** kartu su pradinio pardavimo datos informacijos kodo ir grąžinimo kilmės susiejimo parametrais, norint sugeneruoti teisingą pranešimą fiskalinyje kvite apie grąžinimo operacijos kilmę, jei nėra pradinės pardavimo operacijos. 

    Šis informacijos kodas turėtų būti sukonfigūruotas siekiant leisti vartotojui pasirinkti arba įvesti vieną iš galimų grąžinimų jūsų parduotuvėse kilmės. Pavyzdžiui, jį galima konfigūruoti kaip antrinių kodų sąrašą (pvz. **, Grąžinti iš** svetainės arba **Grįžti iš kiosk**). Grąžinimo **kilmės susiejimo** parametras tada naudojamas informacijos kodo vertei išversti į iždo dokumentų spausdintuvo komandą.

    Informacijos kodas, pasirinktas grąžinimo kilmės **informacijos** kodui, turi būti sukonfigūruotas kaip privalomas informacijos kodas, kuris įtakouojamas vieną kartą per pardavimo operaciją. Jis turėtų būti priskirtas **kaip** grąžinimo produkto informacijos kodas EKA funkcijų šablone, kad jis būtų atmestas **paleidus** grąžinimo produkto operaciją.

    Nenurodyta jokia numatytoji šio susiejimo reikšmė. Turite pasirinkti informacijos kodą, sukonfigūruotą programoje.

- **Informacijos kodas pradinė pardavimo datai** – informacijos kodas, naudojamas fiksuoti pradinę grąžinimo operacijos pardavimo datą, jei nėra jokio pradinio pardavimo kvito. Šis **parametras** **naudojamas** kartu su grąžinimo kilmės informacijos kodu ir grąžinimo kilmės susiejimo parametrais norint sugeneruoti teisingą pranešimą fiskalinyje kvite apie grąžinimo operacijos kilmę, jei nėra pradinės pardavimo operacijos.

    Informacijos kodas turi būti sukonfigūruotas taip, kad įvesties **tipo** laukas būtų nustatytas kaip **Data**. Jis turėtų būti sukonfigūruotas kaip privalomas informacijos kodas, kuris vieną kartą per pardavimo operaciją įdegtas. Jis taip pat **turėtų** **būti** priskirtas kaip informacijos kodo, pasirinkto grąžinimo kilmės parametro informacijos kodui, susietas informacijos kodas, kad du informacijos kodai būtų atmesti vienas po kito.

    Nenurodyta jokia numatytoji šio susiejimo reikšmė. Turite pasirinkti informacijos kodą, sukonfigūruotą programoje.

- **Grąžinimo kilmės susiejimas** – grąžinimo kilmės susiejimas, naudojamas grąžinimo operacijos kilmei spausdinti, jei pateikiamas joks pradinis pardavimo kvitas. Šis **parametras** **naudojamas** kartu su grąžinimo kilmės informacijos kodu ir pradinių pardavimo datos parametrų informacijos kodu, siekiant sugeneruoti teisingą pranešimą fiskalinyje kvite apie grąžinimo operacijos kilmę, jei nėra pradinės pardavimo operacijos. Šiame pavyzdyje rodomas numatytasis susiejimas.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Čia pateikiamas šio susiejimo atributų paaiškinimas:

    - **ReturnOrigin** yra viena iš galimų grąžinimų jūsų parduotuvėse kilmės. Reikšmė turi atitikti grąžinimo kilmės parametro **informacijos kodo** reikšmę.
    - **PrinterReturnOrigin yra** viena iš grąžinimo rezultatų, kuriuos priima fiskalinis spausdintuvas (**EKA**, **OF** arba **ND**).
    - **PrinterReturnOriginWithoutFiscalData** yra grąžinimo šaltinis, kurį priima fiskalinis spausdintuvas ir kuris atitinka grąžinimo operaciją, kuri susieta su pradine pardavimo operacija, kuri neturi susietų finansinių duomenų, nes ji nebuvo užregistruota naudojant fiskalinį spausdintuvą. Šiuo atveju pradinė pardavimo data identifikuojama kaip pradinės pardavimo operacijos data.

Šie numatytieji duomenų susiejimai yra pasenę ir saugomi tik atgalinio suderinamumo tikslais:

- Pridėtinės vertės mokesčio (PVM) kodų susiejimas
- Įmokos mokėjimo tipas

#### <a name="fiscal-connector-settings"></a>Iždo jungties parametrai

Šie parametrai įtraukiami į fiskalinės jungties konfigūraciją, kuri pateikiama kaip finansinio integravimo pavyzdys:

- **Galinio punkto** adresas – spausdintuvo URL.
- **Datos ir laiko sinchronizavimas** – reikšmė, nurodanti, ar spausdintuvo data ir laikas turi būti sinchronizuoti su prijungta aparatūros stotyje.

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

> [!NOTE]
> - Italijos fiskalinio spausdintuvo integravimo pavyzdys yra "Commerce SDK", kuris naudojamas "Commerce" versijoje 10.0.29. Naudojant "Commerce" 10.0.28 arba ankstesnę versiją, LCS programuotojo VM turite naudoti ankstesnę "Retail SDK" versiją. Daugiau informacijos ieškokite Italijos [(senesnės programos) fiskalinio spausdintuvo integravimo pavyzdžio diegimo rekomendacijose](emea-ita-fpi-sample-sdk.md).
> - Jūsų aplinkoje įdiegti "Commerce" pavyzdžiai nėra automatiškai atnaujinami, kai taikote "Commerce" komponentų aptarnavimo arba kokybės naujinimus. Reikiamus pavyzdžius turite atnaujinti neautomatiniu būdu.

#### <a name="set-up-the-development-environment"></a>Programavimo aplinkos kūrimas

Norėdami nustatyti programavimo aplinką, kad būtų galima patikrinti ir išplėsti pavyzdį, atlikite šiuos veiksmus.

1. Užduokite arba atsisiųskite [Dynamics 365 Commerce sprendimų](https://github.com/microsoft/Dynamics365Commerce.Solutions) saugyklą. Pasirinkite tinkamą paleidimo šakos versiją pagal savo SDK / programos versiją. Norėdami gauti daugiau informacijos, žr. ["Download Commerce SDK" pavyzdžius ir nuorodų paketus iš GitHub ir NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Atidarykite **finansinio spausdintuvo integravimo sprendimą Dynamics365Commerce.Solutions\\ FiscalIntegration\\ EpsonFP90IIIISample\\ EpsonFP90IIISample.sln** ir sukurkite jį.
1. Įdiegti CRT plėtinius:

    1. Rasti plėtinio CRT diegimo programą:

        - **"Commerce Scale" vienetas:** aplanke EpsonFP90IIIIample **ScaleUnit.EpsonFP90II.Installer\\ talpyklos derinimas net461\\, \\ raskite ScaleUnit.EpsonFP90II.Installer\\\\** **diegimo priemonės.**
        - **Vietinė "Modern POS": CRT** aplanke EpsonFP90IIIIAMple **ModernPOS.EpsonFP90II.Installer talpyklos debug\\ net461 \\\\ raskite ModernPOS.EpsonFP90II.Installer\\\\** diegimo priemonės.**·**

    1. Paleiskite CRT plėtinio diegimo programą iš komandų eilutės:

        - **"Commerce Scale Unit":**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **" CRT Modern POS" vieta:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Įdiekite aparatūros stoties plėtinius:

    1. Aplanke EpsonFP90IIISample **HardwareStation.EpsonFP90II.Installer\\\\ talpyklos\\ debug\\ net461 \\** raskite HardwareStation.EpsonFP90II.Installer diegimo **priemonės.**
    1. Paleiskite plėtinio diegimo programą iš komandų eilutės:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Gamybos aplinka

Norėdami sugeneruoti [ir](fiscal-integration-sample-build-pipeline.md) paleisti debesies skalės vienetą ir savitarnos diegiant finansinio integravimo pavyzdžio paketus, atlikite nurodytus veiksmus. EpsonFP90II build-pipeline.yml **šablono JAML** **failą galima rasti sprendimų saugyklos YAML_Files\\**[Dynamics 365 Commerce pardavimo galimybių šablono aplanke.](https://github.com/microsoft/Dynamics365Commerce.Solutions)

## <a name="design-of-extensions"></a>Plėtinių dizainas

Italijos fiskalinio spausdintuvo integravimo pavyzdys pagrįstas finansinio [integravimo funkcija](fiscal-integration-for-retail-channel.md) ir yra "Commerce SDK" dalis. Pavyzdys yra sprendimų saugyklos **src\\ FiscalIntegration\\ EpsonFP90IISample**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) aplanke. Pavyzdį [sudaro](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskalinio dokumento teikėjas CRT, kuris yra plėtinys, ir fiskalinė jungtis, kuri yra "Commerce Hardware Station" plėtinys. Norėdami gauti daugiau informacijos apie "Commerce SDK" naudojimą, [žr. "Download Commerce SDK" pavyzdžius ir nuorodų paketus iš GitHub NuGet](../dev-itpro/retail-sdk/sdk-github.md)[ir nustatykite nepriklausomos pakuotės SDK pardavimo galimybių sukūrimą](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Italijos fiskalinio spausdintuvo integravimo pavyzdys yra "Commerce SDK", kuris naudojamas "Commerce" versijoje 10.0.29. Naudojant "Commerce" 10.0.28 arba ankstesnę versiją, LCS programuotojo VM turite naudoti ankstesnę "Retail SDK" versiją. Daugiau informacijos ieškokite Italijos [(senesnės programos) fiskalinio spausdintuvo integravimo pavyzdžio diegimo rekomendacijose](emea-ita-fpi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>"Commerce Runtime" plėtinio dizainas

Plėtinio, kuris yra fiskalinio dokumento teikėjas, paskirtis yra generuoti konkretaus spausdintuvo dokumentus ir tvarkyti atsakymus iš fiskalinio spausdintuvo.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

**DocumentProviderEpsonFP90III** užklausos apdorojimo programa yra užklausos sugeneruoti dokumentus iš fiskalinio spausdintuvo įvesties taškas.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su jungties dokumento teikėjo pavadinimu, kuris nurodytas "Commerce Headquarters".

Jungtis palaiko šias užklausas:

- **GetFiscalDocumentDocumentProviderRequest** – šioje užklausoje yra informacijos apie tai, koks dokumentas turėtų būti sugeneruotas. Grąžinamas spausdintuvui konkretus dokumentas, kuris turi būti užregistruotas fiskaliniu spausdintuvu.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – ši užklausa pateikia įvykių, prie kurių bus užsiprenumeruoti, sąrašą. Šiuo metu palaikomi šie įvykiai: pardavimas, X ataskaitos spausdinimas ir Z ataskaitos spausdinimas.

#### <a name="configuration"></a>Konfigūracija

Finansinio dokumento **teikėjo konfigūracijos failas yra src\\ FiscalIntegration\\ EpsonFP90IIISample\\ CommerceRuntime\\ DocumentProvider.EpsonFP90IIISample\\ konfigūracijos\\ DocumentProviderEpsonFP90IIISample.xml**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) sprendimų saugykloje. Failo paskirtis – įgalinti dokumento teikėjo parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais.

### <a name="hardware-station-extension-design"></a>Aparatūros stoties plėtinio dizainas

Plėtinio, kuris yra fiskalinė jungtis, paskirtis yra palaikyti ryšį su fiskaliniu spausdintuvu. Šis plėtinys naudoja HTTP protokolą dokumentams, kurie sugeneruoja CRT plėtinį, pateikti iždo dokumentų spausdintuvui. Jis taip pat tvarko iš fiskalinio spausdintuvo gautus atsakymus.

#### <a name="request-handler"></a>Užklausų apdorojimo programa

EpsonFP90IIISample **užklausos** apdorojimo programa yra išorinio finansinio įrenginio tvarkymo užklausos įvesties taškas.

Apdorojimo programa perimama iš **INamedRequestHandler** sąsajos. Metodas **HandlerName** yra atsakingas už apdorojimo programos pavadinimo grąžinimą. Apdorojimo programos pavadinimas turi sutapti su "Commerce Headquarters" nurodytu finansinio jungties pavadinimu.

Jungtis palaiko šias užklausas:

- **SubmitDocumentFiscalDeviceRequest** – ši užklausa siunčia dokumentus spausdintuvams ir grąžina atsakymą iš fiskalinio spausdintuvo.
- **IsReadyFiscalDeviceRequest** – ši užklausa naudojama įrenginio sveikatos patikrai atlikti.
- **InitializeFiscalDeviceRequest** – ši užklausa naudojama spausdintuvui inicijuoti.

#### <a name="configuration"></a>Konfigūracija

**Fiskalinės jungties konfigūracijos failas yra src\\ FiscalIntegration\\ EpsonFP90IIISample\\ HardwareStation\\ EpsonFP90IIIFiscalDeviceSample\\ Configuration\\ ConnectorEpsonFP90IIISample.xml**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) sprendimų saugykloje. Failo paskirtis – įgalinti jungties parametrus, kurie bus konfigūruoti iš "Commerce Headquarters". Failo formatas sulygiuotas su finansinio integravimo konfigūracijos reikalavimais.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
