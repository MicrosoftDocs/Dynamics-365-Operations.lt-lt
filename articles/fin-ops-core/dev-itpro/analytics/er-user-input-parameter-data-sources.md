---
title: Naudoti VARTOTOJO ĮVESTIES PARAMETRO duomenų šaltinius ataskaitos parametrams nurodyti
description: Šiame straipsnyje paaiškinama, kaip naudoti VARTOTOJO ĮVESTIES PARAMETRŲ duomenų šaltinius ataskaitų, kurias generuojate, parametrams nurodyti.
author: NickSelin
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.openlocfilehash: 62b7a8173416a1d36a2985823d186a7a0e6a7e60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872978"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>Naudoti VARTOTOJO ĮVESTIES PARAMETRO duomenų šaltinius ataskaitos parametrams nurodyti

[!include[banner](../includes/banner.md)]

[Kurdami](general-electronic-reporting.md) elektroninių ataskaitų (ER) [modelio](er-overview-components.md#model-mapping-component) susiejimą ir ER [formato](er-overview-components.md#format-component) komponentus, *galite naudoti VARTOTOJO ĮVESTIES PARAMETRO* tipo duomenų šaltinius, kad gautumėte reikiamas vertes, kurias galima nurodyti duomenų įrašo laukuose dialogo lange apdorojimo laiku, prieš pradėdami ER formato vykdymą. Šiame straipsnyje aprašomi šiuo *metu palaikomi* VARTOTOJO ĮVESTIES PARAMETRŲ duomenų šaltiniai.

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a> Privalomos ypatybės

Turite nurodyti šias kiekvieno vartotojo ĮVESTIES PARAMETRo tipo duomenų *šaltinių ypatybes*:

- **Lauke Pavadinimas** įveskite vidinį duomenų šaltinio pavadinimą. Šį pavadinimą galite naudoti kitose išraiškose [ir sukonfigūruoto](er-formula-language.md) modelio išdėstymo ar formato komponento susiejimuose.

## <a name="optional-properties"></a><a name="optional-properties"></a> Nebūtinos ypatybės

Galite pasirinktinai nurodyti šias VARTOTOJO ĮVESTIES PARAMETRo tipo duomenų šaltinių *ypatybes*:

- Lauke Žyma **nurodykite** žymę, kuri apdorojimo metu naudojama susijusiam duomenų įvedimo laukui dialogo lange. Galite pridėti kitą žymės tekstą prie skirtingų kalbos kodų, suaktyvindami lauką **Žyma** ir pasirinkdami **Versti**.
- Žinyno **lauke nurodykite žinyno tekstą,** **·** **kuris** rodomas dizaino metu formato kūrimo puslapio arba modelio susiejimo dizaino įrankio puslapio apačioje, kai pasirinktas redaguojamas VARTOTOJO *ĮVESTIES PARAMETRo tipo duomenų šaltinis.* Šis tekstas gali pateikti papildomos informacijos apie duomenų šaltinį, kad vartotojai galėtų padėti jiems sukonfigūruoti redaguojamą formatą arba modelio susiejimo komponentą. Pasirinkę Versti, galite pridėti kitą žinyno tekstą prie skirtingų kalbos **kodų**.

    > [!NOTE]
    > Mygtukas **Versti**[...](er-design-multilingual-reports.md#format-component), kurį galite naudoti, norėdami pridėti kalbai skirtas žymes ir tekstą, tampa galimas tik įtraukus duomenų šaltinį, įrašę pakeitimus ir dar kartą atidarykite duomenų šaltinį, kad jį būtų galima redaguoti.

- Lauke Tik **skaityti sukonfigūruokite** išraišką, kuri grąžina Bulio *[logikos](er-formula-supported-data-types-primitive.md#boolean)* vertę.

    - Jei sukonfigūruota išraiška **grąžina** vertę Teisinga apdorojimo laiku, susijęs duomenų įrašo laukas rodo blankią dialogo lange ir jūs negalite keisti jos vertės.
    - Jei sukonfigūruota **išraiška grąžina vertę False** apdorojimo laiku arba jei nėra sukonfigūruotos jokios išraiškos, dialogo lange galima naudoti susijusį duomenų įvedimo lauką, todėl galite keisti jo vertę.

- Lauke Numatytoji **vertė** sukonfigūruokite išraišką, kuri pateikia nurodomo parametro tipo vertę. Šią vertę galima naudoti norint apdorojimo laiku užpildyti numatytąją susijusių duomenų įvedimo lauko vertę.

    Kai vykdote ER formatą, vertė, kurią įvedate susijusiuose duomenų įvedimo laukuose, vykdymo metu, išsaugoma atmintyje kaip anksčiau naudota vertė. Anksčiau naudotos vertės įrašomos kiekvienam laukui atskirai, paleidus ER formatą, dabartinį vartotoją ir dabartinę organizaciją (įmonę).

    - Nustatykite **numatytosios** **·** **vertės** pasirinktį Visada nustatyti kaip Taip, jei vertė, kurią pateikė numatytosios vertės išraiška, visada turi būti naudojama kaip numatytoji vertė, nepaisant anksčiau naudotų verčių.
    - Nustatykite **numatytosios** **·** **vertės** pasirinktį Visada nustatyti kaip Ne, jei vertė, kurią pateikė numatytosios vertės išraiškos vertė, turi būti naudojama kaip numatytoji vertė tik tada, kai trūksta anksčiau naudomos vertės.

    > [!NOTE]
    > Jei nustatote numatytosios **vertės pasirinktį Visada nustatyti** kaip **Taip**, išraiška turi būti konfigūruota numatytosios **vertės** lauke.

- Jei nustatote parinktį **Leisti pasirinkti kelis nustatymus** **taip**, galite pasirinkti kelias sukonfigūruoto parametro vertes vykdyklėje. Jei ją nustatote kaip **Ne**, galite pasirinkti tik vieną vertę.

    > [!NOTE]
    > Ši pasirinktis netaikoma visiems VARTOTOJO ĮVESTIES *PARAMETRŲ tipams*. Dizaino metu pateikiama išimtis, kuri informuoja vartotoją, kad sukonfigūruotas vartotojo įvesties parametras nepalaiko kelių pasirinkimų ir kad galima pasirinkti arba įvesti tik vieną vertę.
    >
    > Jei nustatote **pasirinktį** **Leisti** pasirinkti kelis pasirinkimus kaip Taip, **o** lauke Numatytoji vertė nurodėte išraišką, tą išraišką galima naudoti tik viena numatyta vertei nustatyti.

- Pasirinkti redagavimo **matomumo** pasirinktį, norint nurodyti, ar sukonfigūruotas parametras turi būti rodomas dialogo lange vykdyklėje.

    > [!NOTE]
    > Vartotojo ĮVESTIES PARAMETRo tipo duomenų šaltinių *numatytasis matomumas* priklauso nuo ER komponento, kuris juos laiko.
    >
    > - Jei duomenų šaltinis konfigūruojamas formato komponentu, pagal numatytuosius nustatymus jis matomas.
    > - Jei duomenų šaltinis konfigūruojamas modelio susiejimo komponente, jis matomas tik jei duomenų šaltinio vertė veikia rezultatą, kai vykdomas ER komponentas. Pavyzdžiui, įtraukėte duomenų šaltinį, bet nenaudojo jo išraiškose ir dabartinio modelio susiejimo komponento susiejimuose. Tokiu atveju, pagal numatytąjį nustatymą, apdorojimo metu dialogo lange nebus rodomas atitinkamas duomenų įvedimo laukas. 

    Formulės dizainerio **puslapio** formulės lauke sukonfigūruokite **išraišką**, kuri grąžina Bulio *logikos* vertę.

    - Jei sukonfigūruota išraiška **grąžina** vertę Teisinga apdorojimo laiku arba jei nėra sukonfigūruotos jokios išraiškos, susijusių duomenų įrašo laukas apdorojimo metu matomas dialogo lange.
    - Jei sukonfigūruota išraiška pateikia vertę **Klaidinga**, susijęs duomenų įrašo laukas apdorojimo metu yra paslėptas dialogo lange. Kai jis iškvievie naudojamas kitų išraiškų apdorojimo metu, grąžinama numatytoji vertė, anksčiau naudota vertė arba numatytoji dabartinio duomenų tipo vertė, atsižvelgiant į kitus parametrus.

## <a name="type-specific-properties"></a>Tipui konkrečios ypatybės

### <a name="application-dependent-user-input-parameter"></a>Nuo programos priklausomo vartotojo įvesties parametras

Norėdami gauti **reikiamą** \> **·** Microsoft Dynamics duomenų tipo, nurodyto dabartinio finansų programos 365 egzemplioriaus, vertę arba vertes, naudokite bendrojo vartotojo įvesties parametro tipo duomenų šaltinį. Kai į ER komponentą įtraukiate šio tipo duomenų šaltinį, nurodykite šias ypatybes:

- Lauke Operacijų **duomenų tipo pavadinimas (EDT, enum)** pasirinkite programos išplėstinį [duomenų tipą (EDT)](../extensibility/extensible-edts.md) arba programos išvardijimas.

> [!NOTE]
> Patariame peržiūrėti išraiškas, kurios sukonfigūruotos laukuose Tik skaityti ir Numatytoji reikšmė, kai pakeisite operacijos duomenų tipo pavadinimą (EDT, išvardiėjimas) **kaip redaguojamą šio VARTOTOJO ĮVESTIES** **·** **PARAMETRo** tipo duomenų *šaltinį.*

Šioje iliustracijoje rodomos duomenų šaltinio `$TaxRegNum`, kuris buvo sukonfigūruotas **Instat XML (DE) ER formato** konfigūracijoje, ypatybės. Šis duomenų šaltinis sukonfigūruotas naudoti *aprašo* EDT **·**, kad būtų galima pasiūlyti mokesčio registracijos numerio duomenų įvedimo lauką dialogo lange apdorojimo laiku.

![VARTOTOJO ĮVESTIES PARAMETRo duomenų šaltinio ypatybės tipo formato dizaino įrankio puslapio dialogo langas.](./media/er-user-input-parameter-data-sources-01.png)

Šioje iliustracijoje rodomas dialogo langas, rodomas **vykdyklėje, kai Instat XML (DE)** ER formato konfigūracija [vykdoma](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) Intrastat deklaracijai generuoti. Atkreipkite dėmesį, kad **sukonfigūruotas mokesčio registracijos numerio** laukas galimas duomenims įvesti.

![Intrastat puslapio ER formato Intrastat ataskaitos dialogo langas.](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a>Duomenų modelių išvardijimo vartotojo įvesties parametras

Norėdami gauti reikiamą **vieno** \> **·**[duomenų modelio išvardijimo vertę ar vertes naudokite duomenų modelio išvardijimo vartotojo įvesties parametro tipo duomenų šaltinį.](er-formula-supported-data-types-primitive.md#enumeration) Kai į ER komponentą įtraukiate šio tipo duomenų šaltinį, nurodykite šias ypatybes:

- **Lauke Modelis** nurodykite nuorodą į pagrindinį duomenų modelį.
- **Modelio išvardijimo** lauke nurodykite nuorodą į nuorodos duomenų modelio išvardiavimą.
- Versijos lauke **pasirinkite** ER duomenų modelio komponento, kuriame yra nurodomas modelių išvardijimas, tikslinimo numerį.

    > [!TIP]
    > Dizaino metu lauką Versija galite palikti tuščią, kad būtų galima pasiekti nurodomų duomenų modelio komponentų, **kurie** yra atitinkamos ER duomenų modelio konfigūracijos juodraščio versijoje, išvardijimo sąrašą. Tokiu būdu galite vienu metu redaguoti savo modelio susiejimo arba formato komponento juodraščio versiją ir pagrindinio duomenų modelio komponento juodraščio versiją.
    >
    > Tačiau įsidėmėkite **, kad** versijos laukas gali būti paliktas tuščias tik modelio susiejimo arba formato komponento juodraščio versijoje. Kai **ER** **modelio** susiejimo arba formato konfigūracijos būseną keičiate iš Juodraštis į Baigta, šį lauką automatiškai užpildo didžiausias modelio tikslinimo numeris, kuris galimas dabartiniame finansų egzemplioriuje. Jei savo pagrindinio duomenų modelio juodraščio versijoje pristatote naują išvardijimo arba naują išvardijimo vertę ir ją nurodote redaguojamame modelio susiejime arba formato komponente, baikite, kad prieš pabaigus savo ER modelio susiejimo arba formato konfigūracijos juodraščio versiją atverkite tą pagrindinio duomenų modelio konfigūracijos juodraščio versiją. Kitu atveju, jums pakeičiant **modelio** susiejimo arba formato konfigūracijos būseną iš Juodraštis į Baigta, bus pateikta išimtis "Nepavyko rasti **maršruto"**. Pranešimas informuos, kad nėra pagrindinės duomenų modelio nuorodos išvardijimo ar išvardijimo reikšmės.

Toliau esantis pavyzdys rodo duomenų šaltinio `$ReportDirection`, kuris buvo sukonfigūruotas **Instat XML (DE) Contoso** ER formato konfigūracijoje, ypatybes. Instat **XML (DE) "Contoso**" konfigūracija išvesta [iš](general-electronic-reporting.md#Configuration) **Instat XML (DE)** konfigūracijos. Šis duomenų šaltinis sukonfigūruotas naudoti *ReportDirection* modelio išvardijimo naudojimą, kad apdorojimo laiku būtų galima pasiūlyti atitinkamą peržvalgos lauką dialogo lange.

![VARTOTOJO ĮVESTIES PARAMETRo duomenų šaltinio ypatybės tipo formato dizaino įrankio puslapio dialogo langas.](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a>Formatų išvardijimo vartotojo įvesties parametras

Norėdami gauti **reikiamą** \> **vieno** formato išvardijimo vertę ar vertes naudokite formato išvardijimo vartotojo įvesties parametro tipo duomenų šaltinį. Kai į ER komponentą įtraukiate šio tipo duomenų šaltinį, nurodykite šias ypatybes:

- **Lauke Formato išvardijimas** nurodykite redaguojamo formato išvardijimas.

> [!NOTE]
> Šio tipo duomenų šaltinius galima konfigūruoti tik redaguojamo formato komponento aprėptimi.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[„USER INPUT PARAMETER“ tipo duomenų šaltinio verčių inicijavimas iš šaltinio kodo](er-initiate-uip-data-source-value-from-source-code.md)
