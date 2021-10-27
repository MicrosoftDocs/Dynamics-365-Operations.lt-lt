---
title: Pakoreguokite ER formatą, kad sugeneruotumėte pasirinktinį elektroninį dokumentą
description: Šioje temoje paaiškinama, kaip pakoreguoti „Microsoft” pateiktą elektroninės ataskaitos angl. „Electronic reporting“ (ER) formatą, kad jis sugeneruotų pasirinktinį elektroninį dokumentą.
author: NickSelin
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47d8091e9199597857791f58f14587e2dea027e0
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605235"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a>Pakoreguokite ER formatą, kad sugeneruotumėte pasirinktinį elektroninį dokumentą

[!include[banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų funkcinio konsultanto vaidmens vartotojas gali atlikti šias užduotis:

- [Elektroninių ataskaitų (ER) sistemos](general-electronic-reporting.md) konfigūracijos parametrai.
- Importuokite „Microsoft” pateiktas ER konfigūracijas, naudojamas generuojant [tiekėjo apmokėjimo](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) failą.
- Sukurkite standartinės „Microsoft” pateiktos ER formato konfigūracijos pasirinktinę versiją.
- Modifikuokite pasirinktinę ER formato konfigūraciją, kad ji sugeneruotų mokėjimo failus, atitinkančius atitinkamo banko reikalavimus.
- Patvirtinkite atliktus standartinės ER formato konfigūracijos pakeitimus pasirinktinėje ER formato konfigūracijoje.

Visos šios procedūros gali būti atliktos **GBSI** įmonėje. Kodavimas nebūtinas.

- [ER sistemos konfigūracija](#ConfigureFramework)

    - [ER parametrų konfigūravimas](#ConfigureParameters)
    - [Aktyvuokite ER konfigūracijos tiekėją](#ActivateProvider)

        - [Peržiūrėkite ER konfigūracijos teikėjų sąrašą](#ReviewProvidersList)
        - [Pridėkite naują ER konfigūracijos tiekėją](#ActivateProvider)
        - [Aktyvuokite ER konfigūracijos tiekėją](#ActivateAddedProvider)

- [Importuokite standartinio ER formato konfigūracijas](#ImportERSolution1)

    - [Importuokite standartinio ER formato konfigūracijas](#ImportERFormat1)
    - [Peržiūrėkite importuotas ER konfigūracijas](#ReviewImportedERSolution)

- [Tiekėjo mokėjimą apdorojimui paruošimas](#PrepareVendorPayment)

    - [Pridėkite tiekėjo paskyros banko informaciją](#AddBankAccount)
    - [Įveskite tiekėjo mokėjimą](#EnterVendorPayment)

- [Apdorokite tiekėjo apmokėjimą naudojant standartinį ER formatą](#ProcessVendorPayment1)

    - [Nustatykite elektroninį mokėjimo būdą](#ConfigureMethodOfPayment1)
    - [Apdorokite tiekėjo mokėjimą](#ProcessPayment1)

- [Pritaikykite standartinį ER formatą](#CustomizeProvidedFormat)

    - [Sukurkite pritaikytą formatą](#DeriveProvidedFormat)
    - [Redaguokite pritaikytą formatą](#ConfigureDerivedFormat)
    - [Pažymėkite pritaikytą formatą kaip leistiną](#MarkFormatRunnable)

- [Apdorokite tiekėjo apmokėjimą naudodami pritaikytą ER formatą](#ProcessVendorPayment2)

    - [Nustatykite elektroninį mokėjimo būdą](#ConfigureMethodOfPayment2)
    - [Apdorokite tiekėjo mokėjimą](#ProcessPayment2)

- [Importuokite standartinio ER formato konfigūracijų naujas versijas](#ImportERSolution2)

    - [Importuokite standartinio ER formato konfigūracijų naujas versijas](#ImportERFormat2)
    - [Peržiūrėkite importuotas ER formato konfigūracijas](#ReviewImportedERFormat)

- [Patvirtinkite importuoto formato naujos versijos pakeitimus pasirinktiniame formate ](#AdoptNewBaseVersion)

    - [Užbaikite pasirinktinio formato esamą juodraštinę versiją](#CompleteDerivedFormat)
    - [Iš naujo pritaikykite pasirinktinį formatą pagal naują pagrindinę versiją](#RebaseDerivedFormat)
    - [Apdorokite tiekėjo apmokėjimą naudodami iš naujo pritaikytą ER formatą](#ProcessPayment3)

- [Papildomi ištekliai](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>ER sistemos konfigūracija

Kaip elektroninių ataskaitų funkcinio konsultanto vartotojas, turite sukonfigūruoti minimalų ER parametrų rinkinį, kad galėtumėte naudoti ER sistemą standartinio ER formato pasirinktinės versijos kūrimui.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>ER parametrų konfigūravimas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** pasirinkite **Elektroninių ataskaitų parametrai**.
3. **Elektroninių ataskaitų parametrai** puslapyje **Bendra** skirtuke nustatykite **Įjungti dizaino režimą** parinktį į **Taip**.
4. **Priedai** skirtuke nustatykite tolesnius parametrus:

    - **Konfigūracijos** lauke pasirinkite **Failas** tipą, skirtą **USMF** įmonei.
    - **Užduoties archyvas**, **Laikini**, **Bazinė linija** ir **Kiti** laukuose pasirinkite **Failas** tipą.

Norėdami sužinoti daugiau apie ER parametrus, žr. [ER sistemos konfigūracija](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>ER konfigūracijos tiekėjo aktyvavimas

Kiekviena pridėta ER konfigūracija pažymėta kaip priklausanti ER konfigūracijos teikėjui. ER konfigūracijos tiekėjas, kuris aktyvuojamas **Elektroninė ataskaita** darbo srityje naudojamas šiam tikslui. Todėl turite aktyvuoti ER konfigūracijos tiekėją **Elektroninė ataskaita** darbo srityje prieš pridėdami ar redaguodami ER konfigūracijas.

> [!NOTE]
> Tik ER konfigūracijos savininkas gali redaguoti. Todėl prieš redaguojant ER konfigūraciją atitinkamas ER konfigūracijos tiekėjas turi būti aktyvuotas **Elektroninė ataskaita** darbo srityje.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>ER konfigūracijos teikėjų sąrašo peržiūra

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Konfigūracijos tiekėjai**.
3. **Konfigūracijos teikėjo lentelė** puslapyje kiekvienas teikėjo įrašas turi unikalų pavadinimą ir URL. Peržiūrėkite šio puslapio turinį. Jei įrašas, skirtas **Litware, Inc.** ( `https://www.litware.com`) jau yra, praleiskite sekančią procedūrą, [Pridėkite naują ER konfigūracijos teikėją](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Pridėkite naują ER konfigūracijos tiekėją

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Konfigūracijos tiekėjai**.
3. **Konfigūracijos tiekėjai** puslapyje pasirinkite **Nauja**.
4. Lauke **Pavadinimas** įveskite **Litware, Inc.**
5. **Internetinis adresas** lauke įveskite `https://www.litware.com`.
6. Pasirinkite **Įrašyti**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>ER konfigūracijos tiekėjo aktyvavimas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos teikėjai** dalyje pasirinkite **„Litware, Inc.”** plytelę ir pasirinkite **Nustatyti kaip aktyvų**.

Daugiau informacijos apie ER konfigūracijos tiekėjus žr. [Konfigūracijos teikėjų kūrimas pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Standartinio ER formato konfigūracijų importavimas

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a>Standartinio ER konfigūracijų importavimas

Norėdami pridėti standartines ER konfigūracijas prie dabartinės „Microsoft Dynamics 365 Finance” programos, importuokite iš ER [saugyklos, ](general-electronic-reporting.md#Repository), sukonfigūruotos tam programos egzemplioriui.

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos teikėjai** dalyje pasirinkite **„Microsoft”** plytelę ir pasirinkite **Saugyklos**, kad peržiūrėtumėte „Microsoft” tiekėjo saugyklų sąrašą.
3. Puslapyje **Konfigūracijų saugyklos** pasirinkite **Visuotinis** tipo saugyklą, paskui pasirinkite **Atidaryti**. Jei esate raginami autorizuoti, kad prisijungtumėte prie „Regulatory Configuration Service”, vadovaukitės autorizavimo instrukcijomis.
4. **Konfigūracijos saugykla** puslapyje kairėje konfigūracijos medyje pasirinkite **BACS (JK)** formato konfigūraciją.
5. **Versijos** „FastTab” skirtuke pasirinkite pasirinktos ER formato konfigūracijos **1.1** versiją.
6. Pasirinkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš Bendrosios saugyklos į dabartinę „Finance“ programą.

![Konfigūracijos saugyklos puslapis.](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> Jei kyla problemų prisijungiant prie [Bendrosios saugyklos ](er-download-configurations-global-repo.md), vietoj to galite [atsisiųsti konfigūracijas](download-electronic-reporting-configuration-lcs.md) iš „Microsoft Dynamics Lifecycle Services (LCS)”.

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Importuotų ER konfigūracijų peržiūra

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.
3. **Konfigūracijos** puslapyje konfigūracijos medyje kairėje pusėje išplėskite **Mokėjimo būdas**.
4. Atkreipkite dėmesį, kad be pasirinkto **BACS (JK)** ER formato, buvo importuotos kitos būtinos ER konfigūracijos. Įsitikinkite, kad sekančios ER konfigūracijos yra prieinamos konfigūracijos medyje:

    - **Mokėjimo būdas** – šioje konfigūracijoje yra [duomenų modelio](general-electronic-reporting.md#data-model-and-model-mapping-components) ER komponentas, rodantis mokėjimo verslo domeno duomenų struktūrą.
    - **Apmokėjimo modelio susiejimas 1611** – šioje konfigūracijoje yra [modelio susiejimo ](general-electronic-reporting.md#data-model-and-model-mapping-components) ER komponentas, aprašantis, kaip duomenų modelis užpildomas programos duomenimis vykdymo metu.
    - **BACS (JK)** – šioje konfigūracijoje yra [formato](general-electronic-reporting.md#FormatComponentOutbound) ir formato susiejimo ER komponentai. Formato komponentas nurodo ataskaitos maketą. Formato susiejimo komponente yra modelio duomenų šaltinis ir nurodo, kaip ataskaitos maketas yra užpildomas naudojant šį duomenų šaltinį vykdymo metu.

![Konfigūracijų puslapis su nurodytomis ER konfigūracijomis prieinamas medyje.](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a>Paruoškite tiekėjo mokėjimą apdorojimui

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a>Pridėkite tiekėjo paskyros banko informaciją

Turite pridėti tiekėjo paskyros banko informaciją, kuri bus paminėta vėliau registruotame mokėjime.

1. Eikite į **Mokėtinos sumos** \> **Tiekėjai** \> **Visi tiekėjai**.
2. **Visi tiekėjai** puslapyje pasirinkite **GB_SI_000001** tiekėjo paskyrą, tada Veiksmų srityje **Tiekėjas** skirtuke **Nustatyti** grupę, pasirinkite **Banko sąskaitos**.
3. **Tiekėjo banko sąskaitos** puslapyje pasirinkite **Nauja** ir įveskite šią informaciją:

    1. **Banko sąskaita** lauke įveskite **GBP OPER**.
    2. **Banko grupė** lauke pasirinkite **BankoGBP**.
    3. **Banko sąskaitos numeris** lauke įveskite **202015**.
    4. **SWIFT kodas** lauke įveskite <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.
    5. **IBAN** lauke įveskite **GB33BUKB20201555555555**.
    6. **Banko kodas** lauke palikite numatytąją vertę, <a id="DefineRoutingNumber"></a>**123456**.

    ![Tiekėjų bankų paskyrų puslapis.](./media/er-quick-start2-bank-account.png)

4. Pasirinkite **Įrašyti**.
5. Uždarykite puslapį.
6. **Visi tiekėjai** puslapyje atidarykite **GB_SI_000001** tiekėjo paskyrą.
7. Jei reikia, tiekėjo informacijos puslapyje pasirinkite **Redaguoti**, kad puslapis būtų redaguojamas.
8. **Mokėjimas** „FastTab” skirtuke **Banko paskyra** lauke pasirinkite **GBP OPER**.

    ![Tiekėjo išsamios informacijos puslapis.](./media/er-quick-start2-bank-account-reference.png)

9. Pasirinkite **Įrašyti**.
10. Uždarykite puslapį.

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a>Įveskite tiekėjo mokėjimą

Turite sukurti naują tiekėjo mokėjimą naudodami [mokėjimo pasiūlymą](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md).

1. Eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Tiekėjo mokėjimų žurnalas**.
2. **Tiekėjo mokėjimo žurnalas** puslapyje pasirinkite **Nauja**.
3. Lauke **Pavadinimas** pasirinkite **Tiek.Mok.**
4. Pasirinkite **Eilutės**.
5. Pasirinkite **Mokėjimo pasiūlymas** \> **Sukurti mokėjimo pasiūlymą**.
6. Dialogo lange **Tiekėjo mokėjimo pasiūlymas** konfigūruokite sąlygas įrašams, skirtiems tik **GB_SI_000001** tiekėjo paskyrai, filtruoti ir tada pasirinkite **Gerai**.
7. Pasirinkite **00000007_SF** sąskaitos faktūros eilutę ir pasirinkite **Kurti mokėjimą**.

    ![Tiekėjo mokėjimo pasiūlymo dialogo langas.](./media/er-quick-start2-payment-proposal.png)

8. Patikrinkite, ar įvestas apmokėjimas sukonfigūruotas naudoti **Elektroninis** mokėjimo metodą.

    ![Puslapis Tiekėjo mokėjimai.](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a>Apdorokite tiekėjo mokėjimą naudodami standartinį ER formatą

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a>Nustatykite elektroninį mokėjimo būdą

Turite sukonfigūruoti elektroninio mokėjimo metodą, kad jis naudotų importuoto ER formato konfigūraciją.

1. Eikite į **Mokėtinos sumos** \> **Mokėjimo nustatymas** \> **Mokėjimo būdai**.
2. **Mokėjimo būdai – tiekėjai** puslapyje pasirinkite **Elektroninis** mokėjimo būdą kairiojoje srityje.
3. Pasirinkite **Redaguoti**.
4. **Failo formatai** „FastTab“ skirtuke nustatykite **Bendras elektroninis eksportavimo formatas** į **Taip**.
5. Lauke **Eksportuoti formato konfigūraciją** pasirinkite **BACS (JK)** formato konfigūraciją.

    ![Mokėjimo būdai – tiekėjų puslapis, skirtas nustatyti elektroninio mokėjimo būdu tiekėjo mokėjimams apdoroti, naudojant standartinį formatą.](./media/er-quick-start2-method-of-payment1.png)

6. Pasirinkite **Įrašyti**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a>Apdorokite mokėjimo būdą

1. Eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Tiekėjo mokėjimų žurnalas**.
2. Puslapyje **Tiekėjo mokėjimų žurnalas** pasirinkite anksčiau pridėtą mokėjimų žurnalą tada pasirinkite **Eilutės**.
3. **Tiekėjo mokėjimai** puslapyje pasirinkite **Generuoti mokėjimus**.
4. Dialogo lange **Generuoti mokėjimus** įveskite tolesnę informaciją:

    - Lauke **Mokėjimo būdas** pasirinkite **Elektroninis**.
    - Lauke **Banko sąskaita** įveskite **GBSI OPER**.

5. Pasirinkite **Gerai**.
6. **Elektroninės ataskaitos parametrai** dialogo lange nustatykite **Spausdinti kontrolės ataskaitą** pasirinktį į **Taip**, tada pasirinkite **Gerai**.

    ![Elektroninių ataskaitų parametrų dialogo puslapis.](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > Be mokėjimo failo, taip pat galite generuoti kontrolės ataskaitą.

7. Atsisiųskite suarchyvuotą failą, tada iš jo išskleiskite šiuos failus:

    - Kontrolės ataskaita „Excel” formatu
    - Mokėjimo failas TXT formatu

        Atkreipkite dėmesį, kad pagal pateikto ER formato [struktūrą](#PositionRoutingNumber), sugeneruotame faile mokėjimo eilutės failas prasideda banko kodu, kuris buvo [nurodytas](#DefineRoutingNumber) sukonfigūruotai banko paskyrai.

        ![Mokėjimo failas TXT formatu.](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Pritaikykite standartinį ER formatą

Pavyzdžiui, šiame skyriuje rodomas pavyzdys, kurį norite naudoti su „Microsoft” teikiamomis ER konfigūracijomis, kad būtų sugeneruoti tiekėjų mokėjimo failai BACS formatu, bet turite atitinkamai pritaikyti, kad atitiktų konkretaus banko reikalavimus. Jums taip pat reikia atnaujinti pasirinktinį formatą, kai naujos ER konfigūracijų versijos taps prieinamomis. Tačiau siekiate atnaujinti be didesnių išlaidų.

Šiuo atveju, būdami „Litware, Inc.” atstovu turite sukurti (išvesti) naują ER formato konfigūraciją naudodami „Microsoft” pateiktą konfigūraciją **BACS (JK)** kaip pagrindą.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Sukurkite pritaikytą formatą

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūracijos** puslapyje konfigūracijų medyje kairėje srityje išskleiskite **Mokėjimo modelis** ir tada pasirinkite **BACS (JK)**. „Litware, Inc.” naudos ER formato konfigūracijos 1.1 versiją kaip pasirinktinės versijos pagrindą.
3. Pasirinkite **Kurti konfigūraciją**, kad atidarytumėte išplečiamąjį dialogo langą. Galite naudoti dialogo langą, kad sukurtumėte naują pasirinktinio mokėjimo formato konfigūraciją.
4. **Nauja** lauko grupėje pasirinkite **Išvesti iš Pavadinimo: BACS (UK), „Microsoft”** parinktį.
5. **Pavadinimas** lauke įveskite **BACS (JK pritaikytas)**.

    ![Konfigūracijos išplečiamojo dialogo lango kūrimas.](./media/er-quick-start2-add-derived-format.png)

6. Pasirinkite **Kurti konfigūraciją**.

**BACS (pritaikyta JK)** sukuriama ER formato konfigūracijos versija 1.1.1. Ši versija turi [būseną](general-electronic-reporting.md#component-versioning) **Juodraštis** ir ji gali būti redaguojama. Jūsų pritaikyto ER formato dabartinis turinys atitinka „Microsoft” pateikto formato turinį.

![Konfigūracijos puslapis su BACS (pritaikyta JK) ER formato konfigūracijos versija 1.1.1.](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a>Redaguoti pritaikytą formatą

Turite sukonfigūruoti savo pritaikytą formatą, kad jis atitiktų banko konkrečius reikalavimus. Pavyzdžiui, bankas gali reikalauti, kad sugeneruotuose apmokėjimų failuose turi būti nurodytas Tarptautinių tarpbankinių finansinių atsiskaitymų organizacijos angl. „Society for Worldwide Interbank Financial Telecommunication“ (SWIFT) kodas, kuriam priskirtas agento vaidmuo apdorojant tiekėjo mokėjimą. SWIFT kodai yra tarptautiniai banko kodai, kurie nurodo tam tikrus bankus visame pasaulyje. Jie taip pat vadinami Banko identifikaciniais kodais (BIC). SWIFT kodas susideda iš 11 simbolių ir turi būti įvestas sugeneruoto apmokėjimo kiekvieno mokėjimo eilučių pradžioje.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūracijos** puslapyje konfigūracijų medyje kairėje srityje išskleiskite **Mokėjimo modelis** ir tada pasirinkite **BACS (pritaikyta JK)**.
3. **Versijos** „FastTab” skirtuke pasirinkite pasirinktos konfigūracijos **1.1.1** versiją.
4. Pasirinkite **Dizaino įrankis**.
5. **Formato kūrimo įrankis** puslapyje pasirinkite **Rodyti išsamią informaciją**, kad peržiūrėtumėte daugiau informacijos apie formatavimo elementus.
6. Išplėskite ir peržiūrėkite šiuos elementus:

    - **BACSAtaskaitųAplankas** **Aplankas** tipo elementas. Šis elementas naudojamas generuoti išvestį suskleistu formatu.
    - **Failas** **Failo** tipo elementas. Šis elementas naudojamas generuoti mokėjimo failą TXT formatu.
    - **Operacijos** **Seka** tipo elementas. Šis elementas naudojamas generuoti vieną mokėjimo eilutę mokėjimo faile.
    - **Operacija** **Seka** tipo elementas. Šis elementas naudojamas generuoti atskirus vienos mokėjimo eilutės laukus.

7. Pasirinkite **operacijos** elementą.

    ![Operacijos elementas, esantis ER operacijų kūrimo įrankyje.](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > Pateikta ataskaita sukonfigūruota taip, kad <a id="PositionRoutingNumber"></a>kiekviena mokėjimo eilutė prasideda banko kodu. **tiek.BankoKodas** formato elementas naudojamas šiam tikslui. 

8. Pasirinkite **Pridėti** ir pasirinkite **Tekstas \\Eilutė** pridedamo elemento formato tipą:

    1. **Pavadinimas** lauke įveskite **tiek.BankoSWIFT**.
    2. **Mažiausias ilgis** lauke įveskite **11**.
    3. **Didžiausias ilgis** lauke įveskite **11**.
    4. Pasirinkite **Gerai**.

    > [!NOTE]
    > **tiek.BankoSWIFT** elementas bus naudojamas įvesti tiekėjo banko SWIFT kodą sugeneruotuose failuose.

9. Formato struktūros medyje pasirinkite **tiek.BankoSWIFT**.
10. Pasirinkite **Perkelti aukštyn**, kad perkeltumėte pasirinkto formato elementą aukštyn vienu lygiu. Kartokite šį veiksmą, kol **tiek.BankoSWIFT** elementas taps <a id="PositionSWIFTCode"></a>pirmu elementu, esančiu pirminiame **operacija** elemente.

    ![TiekBankoSWIFT kaip pirmas elementas, esantis ER operacijų kūrimo įrankio operacijoje.](./media/er-quick-start2-derived-format1.png)

11. Kol **tiek.BankoSWIFT** vis dar yra pasirinkta formato struktūros medyje, pasirinkite **Susiejimas** skirtuke ir tada išplėskite **modelis** duomenų šaltinį.
12. Išplėskite **modelis.Mokėjimas** \> **modelis.Mokėjimas.KreditoriausAgentas** ir pasirinkite **modelis.Mokėjimas. KreditoriausAgentas.BICFI** duomenų šaltinio lauką. Šio duomenų šaltinio lauke rodomas tiekėjo banko SWIFT kodas, kuriam priskirtas agento vaidmuo apdorojant tiekėjo mokėjimą.
13. Pasirinkite **Susieti**. **tiek.BankoSWIFT** formato elementas dabar yra susietas su **modelis.Mokėjimas.KreditoriausAgentas.BICFI** duomenų šaltinio lauku, kad SWIFT kodai būtų įvesti sugeneruotuose mokėjimo failuose.

    ![tiekBankoSWIFT formato elementas, susietas su modelis.Mokėjimas.KreditoriausAgentas.BICFI duomenų šaltinio lauku ER operacijų kūrimo įrankyje.](./media/er-quick-start2-derived-format2.png)

14. Pasirinkite **Įrašyti**.
15. Uždarykite kūrimo įrankio puslapį.

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Pažymėkite pritaikytą formatą kaip leistiną

Dabar, kai sukurta pirmoji jūsų pritaikyto formato versija, kurios būsena **Juodraštis**, ją galite paleisti testavimui. Norėdami paleisti ataskaitą, turite apdoroti tiekėjo mokėjimą naudodami mokėjimo būdą, nurodantį jūsų pritaikytą ER formatą. Pagal numatytuosius nustatymus jums iškvietus ER formatą programoje tik būseną` **Baigta** ar **Bendrinta** turinčios versijos [bus svarstomos](general-electronic-reporting.md#component-versioning). Toks veikimas užtikrina, kad nebaigto dizaino ER formatai nebūtų naudojami. Tačiau, atliekant bandomuosius vykdymus, galite priversti programą naudoti ER formato **Juodraštis** būsenos versiją. Tokiu būdu galite koreguoti dabartinio formato versiją, jei reikia atlikti pakeitimus. Daugiau informacijos žr. [Taikomumas](electronic-reporting-destinations.md#applicability).

Norėdami naudoti ER formato juodraščio versiją, turite aiškiai pažymėti ER formatą.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. **Vartotojo parametrai** dialogo lange nustatykite **Leisti parametrus** parinktį į **Taip** ir pasirinkite **Gerai**.
4. Pasirinkite **Redaguoti**, kad pagal poreikį galėtumėte redaguoti esamą puslapį.
5. Kairiojoje srityje esančiame konfigūracijos medyje pasirinkite **BACS (pritaikyta JK)**.
6. Nustatykite **Leist juodraštį** parinktį į **Taip**.

    ![Paleiskite juodraštinę pasirinktį Konfigūracijų puslapyje.](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a>Apdorokite tiekėjo mokėjimą naudodami pritaikytą ER formatą

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a>Nustatykite elektroninį mokėjimo būdą

Turite sukonfigūruoti elektroninį mokėjimo būdą, kad jūsų pritaikyto ER formatas būtų naudojamas tiekėjo mokėjimams apdoroti.

1. Eikite į **Mokėtinos sumos** \> **Mokėjimo nustatymas** \> **Mokėjimo būdai**.
2. **Mokėjimo būdai – tiekėjai** puslapyje pasirinkite **Elektroninis** mokėjimo būdą kairiojoje srityje.
3. Pasirinkite **Redaguoti**.
4. **Failo formatas** „FastTab“ skirtuke nustatykite **Bendras elektroninis eksportavimo formatas** į **Taip**.
5. **Eksportuoti formato konfigūraciją** lauke pasirinkite **BACS (pritaikyta JK)** formato konfigūraciją.

    ![Mokėjimo būdai – tiekėjų puslapis, skirtas nustatyti elektroninio mokėjimo būdu tiekėjo mokėjimams apdoroti, naudojant pritaikytą formatą.](./media/er-quick-start2-method-of-payment2.png)

6. Pasirinkite **Įrašyti**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a>Apdorokite mokėjimo būdą

1. Eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Tiekėjo mokėjimų žurnalas**.
2. **Tiekėjo mokėjimo žurnalas** puslapyje pasirinkite jūsų anksčiau sukurtą mokėjimo žurnalą.
3. Pasirinkite **Eilutės**.
4. **Tiekėjo mokėjimai** puslapyje, virš tinklelio, pasirinkite **Mokėjimo būsena** \>**Nėra**.
5. Pasirinkite **Generuoti mokėjimą**.
6. Dialogo lange **Generuoti mokėjimus** įveskite tolesnę informaciją:

    - Lauke **Mokėjimo būdas** pasirinkite **Elektroninis**.
    - Lauke **Banko sąskaita** įveskite **GBSI OPER**.

7. Pasirinkite **Gerai**.
8. **Elektroninės ataskaitos parametrai** dialogo lange nustatykite **Spausdinti kontrolės ataskaitą** pasirinktį į **Taip**, tada pasirinkite **Gerai**.

    > [!NOTE]
    > Be mokėjimo failo, galite generuoti tik kontrolės ataskaitą.

9. Atsisiųskite suarchyvuotą failą, tada iš jo išskleiskite šiuos failus:

    - Kontrolės ataskaita „Excel” formatu
    - Mokėjimo failas TXT formatu

        Atkreipkite dėmesį, kad pagal jūsų pritaikyto ER formato struktūrą, sugeneruoto failo mokėjimo eilutė dabar [prasideda](#PositionSWIFTCode) SWIFT kodu,  [įvestu](#DefineSWIFTCode) tiekėjo, kurio apmokėjimas buvo apdorotas, banko sąskaitai.

        ![Mokėjimo failas TXT formatu, naudojamas tiekėjo mokėjimui apdoroti.](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a>Importuokite standartinio ER formato konfigūracijų naujas versijas

Pavyzdžiui, šiame skyriuje rodomas pavyzdys, kai gaunate pranešimą apie Žinių bazės straipsnį [KB 3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046). Šis pranešimas informuoja jus apie naują **BACS (JK)** „Microsoft” paskelbtą ER formato versiją. Be kontrolės ataskaitos ši nauja versija leidžia vartotojams generuoti mokėjimo pažymų ataskaitą ir lydinčios pažymos ataskaitą, kol tiekėjo mokėjimas apdorojamas. Jums ši funkcija pravers.

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a>Importuokite standartinio ER formato konfigūracijų naujas versijas

Norėdami pridėti standartinių ER konfigūracijų naujas versijas prie dabartinės „Finance” programos, importuokite jas iš jūsų sukonfigūruotos ER [saugyklos](general-electronic-reporting.md#Repository).

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos teikėjai** dalyje pasirinkite **„Microsoft”** plytelę ir pasirinkite **Saugyklos**, kad peržiūrėtumėte „Microsoft” tiekėjo saugyklų sąrašą.
3. Puslapyje **Konfigūracijų saugyklos** pasirinkite **Visuotinis** tipo saugyklą, paskui pasirinkite **Atidaryti**. Jei esate raginami autorizuoti, kad prisijungtumėte prie „Regulatory Configuration Service”, vadovaukitės autorizavimo instrukcijomis.
4. **Konfigūracijos saugykla** puslapyje kairėje konfigūracijos medyje pasirinkite **BACS (JK)** formato konfigūraciją.
5. **Versijos** „FastTab” skirtuke pasirinkite pasirinktos ER formato konfigūracijos **3.3** versiją.
6. Pasirinkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš Bendrosios saugyklos į dabartinę „Finance“ programą.

![Konfigūracijos saugyklos puslapis, Versijos "FastTab", Importavimo mygtukas.](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> Jei kyla problemų prisijungiant prie [Bendrosios saugyklos](er-download-configurations-global-repo.md), vietoj to galite [atsisiųsti konfigūracijas](download-electronic-reporting-configuration-lcs.md) iš LCS.

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a>Peržiūrėkite importuotas ER formato konfigūracijas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.
3. **Konfigūracijos** puslapyje konfigūracijų medyje kairėje srityje išskleiskite **Mokėjimo modelis** ir tada pasirinkite **BACS (JK)**.
4. Sparčiajame skirtuke **Versijos** paspauskite **3.3**.
5. Pasirinkite **Dizaino įrankis**.
6. **Formato kūrimo įrankis** puslapyje išplėskite **BACSAtaskaitosAplankas** formato elementą.
7.  Atkreipkite dėmesį, kad versijoje 3.3 yra **MokėjimoPažymosAtaskaita** formato elementas, kuris naudojamas mokėjimo pažymos ataskaitai generuoti, kai apdorojamas tiekėjo mokėjimas.

    ![MokėjimoPažymosAtaskaitos formato elementas ER operacijų kūrimo įrankyje.](./media/er-quick-start2-imported-solution2.png)

8. Uždarykite kūrimo įrankio puslapį.

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a>Patvirtinkite importuoto formato naujos versijos pakeitimus pritaikytame formate

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a>Užbaikite pritaikyto formato esamą juodraštinę versiją

Jei norite, kad dabartinė jūsų pritaikyto formato būsena būtų baigta, užbaikite juodraštinę versiją 1.1.1, pakeisdami jos būseną iš **Juodraštis** į **Baigta**.

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Lokalizavimo konfigūracijos** puslapyje **Konfigūracijos** dalyje pasirinkite plytelę **Konfigūracijų ataskaitos**.
3. **Konfigūracijos** puslapyje kairėje esančiame konfigūracijų medyje išskleiskite **Mokėjimo modelis**, išplėskite **BACS (JK)** ir tada pasirinkite **BACS (pritaikyta JK)**.
4. **Versijos** „FastTab” skirtuke pasirinkite **Pakeisti būseną**\>**Baigta** ir pasirinkite **Gerai**.

Versijos 1.1.1 būsena pakeista iš **Juodraštis** į **Baigta**, o versija tampa tik skaitoma. Nauja redaguotina versija, 1.1.2, buvo pridėta ir jos būsena yra **Juodraštis**. Šią versiją galite naudoti norėdami atlikti tolesnius keitimus savo pritaikytame ER formate.

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a>Iš naujo pritaikykite pritaikytą formatą pagal naują pagrindinę versiją

Norėdami naudoti naujas **BACS (JK)** formato 3.3 versijos funkcijas jūsų tinkinime, turite pakeisti pagrindinės konfigūracijos versiją, skirtą pritaikytam tinkinimui **BACS (pritaikyta JK)**. Šis procesas vadinamas [pritaikymu kitoje vietoje](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase). Vietoj **BACS (JK)** 1.1 versijos naudokite 3.3 versiją.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūracijos** puslapyje konfigūracijų medyje kairėje srityje išskleiskite **Mokėjimo modelis** ir tada pasirinkite **BACS (pritaikyta JK)**.
3. **Versijos** „FastTab” skirtuke pasirinkite versiją **1.1.2** ir pasirinkite **Pritaikyti kitoje vietoje**.
4. **Pritaikyti kitoje vietoje** dialogo lange **Tikslinė versija** lauke pasirinkite pagrindinės konfigūracijos **3.3** versiją pritaikyti ją kaip naują pagrindinę versiją ir naudoti ją konfigūracijai atnaujinti.

    ![Pritaikymo kitoje vietoje dialogo langas.](./media/er-quick-start2-rebase1.png)

5. Pasirinkite **Gerai**.
6. Atkreipkite dėmesį, kad juodraštinės versijos numeris pakeistas iš **1.1.2** į **3.3.2**, kad parodytų pagrindinės versijos pasikeitimą.

    Kai pritaikyta versija ir naujoji versija suliejamos, gali atsirasti konfliktų dėl formatų, kurie negali būti automatiškai sulieti, pasikeitimų.

    ![Pritaikykite konfigūraciją su konfliktais kitoje vietoje Konfigūracijų puslapyje.](./media/er-quick-start2-rebase2.png)

    Jei atsirado konfliktų, jie turi būti išspręsti neautomatiniu būdu formato kūrimo įrankyje.

7. Sparčiajame skirtuke **Versijos** paspauskite **3.3.2**.
8. Pasirinkite **Dizaino įrankis**.
9. **Formato kūrimo įrankis** puslapyje **Išsami informacija** „FastTab” pasirinkite pritaikyto kitoje vietoje konflikto įrašą ir pasirinkite **Taikyti pagrindinę vertę**.

    ![Pritaikykite konflikto įrašą kitoje vietoje ER operacijų kūrimo įrankyje.](./media/er-quick-start2-rebase3.png)

10. Pasirinkite **Įrašyti**.

    Pritaikyto kitoje vietoje konflikto įrašas nebeatsiras **Išsami informacija** „FastTab”.

    ![Konfliktas išspręstas ER operacijų kūrimo įrankyje.](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > Jūs išsprendėte konfliktą patvirtinę, kad šioje pagrindinio modelio versijoje Nr.3 turi būti naudojama šiame ER formate.

11. Išplėskite **BACSAtaskaitųAplankas** \> **failas** \>**operacijos** \> **operacija**.
12. **Susiejimas** skirtuke atkreipkite dėmesį, kad jūsų pritaikyto ER formato versijoje 3.3.2 yra tiek jūsų tinkinimas (**tiek.BankoSWIFT** formato elementas ir jo susiejimas) ir nauja „Microsoft” pateikta pagrindinio ER formato versijos 3.3 versijos funkcija ( **MokėjimoPažymosAtaskaita** formato elemento kartu su jo įdėtais elementais ir sukonfigūruotais susiejimais). Tik keliais pelės spustelėjimais patvirtinote naujos pagrindinės versijos pakeitimus suliedami juos su jūsų tinkinimu.

    ![Sulietas formatas ER operacijų kūrimo įrankyje.](./media/er-quick-start2-rebase5.png)

13. Uždarykite kūrimo įrankio puslapį.

> [!NOTE]
> Pritaikymo kitoje vietoje veiksmas nėra grįžtamas. Norėdami atšaukti šį pritaikymą kitoje vietoje, pasirinkite **1.1.1** **BACS (pritaikyta JK)** formato versiją **Versijos** „FastTab” skirtuke ir pasirinkite **Gauti šią versiją**. Tada 3.3.2 versija bus pernumeruota į 1.1.2, o juodraštinės versijos 1.1.2 turinys atitiks 1.1.1 versijos turinį.

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a>Apdorokite tiekėjo mokėjimą naudodami iš pritaikytą kitoje vietoje ER formatą

1. Eikite į **Mokėtinos sumos** \> **Mokėjimai** \> **Tiekėjo mokėjimų žurnalas**.
2. **Tiekėjo mokėjimo žurnalas** puslapyje pasirinkite jūsų anksčiau sukurtą mokėjimo žurnalą.
3. Pasirinkite **Eilutės**.
4. **Tiekėjo mokėjimai** puslapyje, virš tinklelio, pasirinkite **Mokėjimo būsena** \>**Nėra**.
5. Pasirinkite **Generuoti mokėjimą**.
6. Dialogo lange **Generuoti mokėjimus** įveskite tolesnę informaciją:

    - Lauke **Mokėjimo būdas** pasirinkite **Elektroninis**.
    - Lauke **Banko sąskaita** įveskite **GBSI OPER**.

7. Pasirinkite **Gerai**.
8. Dialogo lange **Elektroninių ataskaitų parametrai** įveskite šią informaciją:

    - Nustatykite parinktį **Spausdinti kontrolės ataskaitą** į **Taip**.
    - Nustatykite **Spausdinti mokėjimo pažymą** parinktį į **Taip**.

    ![Elektroninių ataskaitų parametrų dialogo langas.](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > Be mokėjimo failo galite generuoti tiek kontrolės ataskaita, tiek mokėjimo pažymos ataskaitą.

9. Pasirinkite **Gerai**.
10. Atsisiųskite suarchyvuotą failą, tada iš jo išskleiskite šiuos failus:

    - Kontrolės ataskaita „Excel” formatu
    - Mokėjimo pažymos ataskaita „Excel” formatu

        ![Mokėjimo pažymos ataskaita „Excel” formatu.](./media/er-quick-start2-payment-advice-report.png)

    - Mokėjimo failas TXT formatu

        Atkreipkite dėmesį į sugeneruoto failo, prasidedančio SWIFT kodu, kuris buvo įvestas tiekėjo, kurio apmokėjimas apdorojamas, banko sąskaitai, mokėjimo eilutę.

        ![Mokėjimo failas TXT formatu, naudojamas tiekėjo mokėjimui apdoroti, naudojant pakartotiną ER formatą.](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a>Papildomi ištekliai

- [Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)
- [ER konfigūracijų atsisiuntimas iš „Lifecycle Services“](download-electronic-reporting-configuration-lcs.md)
- [ER konfigūracijų atsisiuntimas iš „Configuration service” Bendrosios saugyklos](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
