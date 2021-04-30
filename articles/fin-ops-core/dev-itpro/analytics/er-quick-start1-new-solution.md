---
title: Suprojektuokite naują ER sprendimą tinkintos ataskaitos spausdinimui
description: Šioje temoje paaiškinama, kaip suprojektuoti elektroninį ataskaitos sprendimą tinkintos ataskaitos spausdinimui.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a3e0e4a8389fdd6580f66004d86ef4b1980dd9f
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891798"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a>Suprojektuokite naują ER sprendimą tinkintos ataskaitos spausdinimui

[!include[banner](../includes/banner.md)]

Toliau atlikti žingsniai paaiškina, kaip vartotojas sistemos administratoriaus, elektroninės ataskaitos kūrėjo ar elektroninės ataskaitos funkcijų konsultanto vaidmenyje gali konfigūruoti ES darbo grafiko sprendimus, projektuoti reikiamas naujo ER konfigūracijas prieigai prie konkrečių verslo domeno duomenų ir kurti tinkintą ataskaitą „Microsoft Office“ formate. Šie žingsniai gali būti užbaigti **USMF** bendrovėje.

- [ER sistemos konfigūracija](#ConfigureFramework)

    - [ER parametrų konfigūravimas](#ConfigureParameters)
    - [Aktyvuokite ER konfigūracijos tiekėją](#ActivateProvider)

        - [Peržiūrėkite ER konfigūracijos teikėjų sąrašą](#ReviewProvidersList)
        - [Pridėkite naują ER konfigūracijos tiekėją](#AddProvider)
        - [Aktyvuokite ER konfigūracijos tiekėją](#ActivateAddedProvider)

- [Suprojektuokite specialų domeno duomenų modelį](#DesignModel)

    - [Importuokite naują duomenų modelio konfigūraciją](#ImportDataModel)
    - [Sukurti naują duomenų modelio konfigūraciją](#DesignDataModel)

        - [Pavadinkite duomenų modelį](#NameDataModel)
        - [Įtraukite duomenų modelio laukelius](#FieldsEntry)
        - [Užbaikite duomenų modelio projektavimą](#CompleteDataModel)

- [Suprojektuokite konfigūruoto duomenų modelio žemėlapį](#DesignMapping)

    - [Importuokite naują modelio žemėlapio konfigūravimą](#ImportModelMapping)
    - [Sukurkite naują modelio žemėlapio konfigūravimą](#CreateModelMapping)

        - [Projektuokite naują modelio žemėlapio komponentą](#DesignMappingComponent)
        - [Įtraukite duomenų šaltinius į prieigos programos lenteles](#AddMmDataSource1)
        - [Įtraukite duomenų šaltinius tam, kad prieitumėte prie programos numeracijų](#AddMmDataSource2)
        - [Įtraukite ER žymes tam, kad sukurtumėte ataskaitą konkrečia kalba](#AddMmLabels)
        - [Įtraukite duomenų šaltinį tam, kad paverstumėte numeracijos verčių lyginimo rezultatus į teksto vertes](#AddMmDataSource3)
        - [Susiekite duomenų šaltinius su duomenų modelio laukeliais](#AddMmBindings1)
        - [Užbaikite modelio žemėlapio projektavimą](#CompleteModelMapping)

- [Suprojektuokite tinkintos ataskaitos šabloną](#DesignReportTemplate)
- [Formato kūrimas](#DesignFormat)

    - [Importuokite suprojektuotą formato konfigūravimą](#FormatImport)
    - [Kurti naują formato konfigūraciją](#FormatCreate)

        - [Importuokite ataskaitos šabloną](#ImportReportTemplate)
        - [Konfigūruokite formatą](#ConfigureFormat)
        - [Nustatykite duomenų susiejimą ataskaitos pavadinimui](#DefineFormatBindings)
        - [Peržiūrėkite modelio duomenų šaltinį](#ReviewModelDataSource)
        - [Susiekite formato elementus su duomenų šaltinio laukeliais](#BindFormatElements)

    - [Vykdykite suprojektuotą formatą iš ER](#RunFormatFromER)

- [Suderinkite projektavimo formatą](#TuneFormat)

    - [Keiskite formatą tam, kad pakeistumėte sukurto dokumento pavadinimą](#ModifyToChangeName)
    - [Keiskite formatą tam, kad pakeistumėte klausimų seką](#ModifyToOrder)
    - [Vykdykite pakeistą formatą iš ER](#RunFormatFromER2)
    - [Užbaikite formato projektą](#CompleteFormat)

- [Vystykite programos artefaktus tam, kad iškviestumėte suprojektuotą ataskaitą](#DevelopCustomCode)

    - [Šaltinio kodo modifikavimas](#ModifySourceCode)

        - [Įtraukite duomenų sutarties klasę](#DataContractClass)
        - [Įtraukite UI kūrėjo klasę](#UIBuilderClass)
        - [Įtraukite duomenų tiekėjo klasę](#DataProviderClass)
        - [Įtraukite žymių failą](#LabelsFile)
        - [Įtraukite ataskaitos paslaugos klasę](#ServiceClass)
        - [Įtraukite ataskaitos valdiklio klasę](#ControllerClass)
        - [Įtraukite meniu elementą](#MenuItem)
        - [Įtraukite meniu elementą į meniu](#Menu)
        - [Sukurkite „Visual Studio“ projektą](#BuildVSProject)

    - [Vykdykite formatą iš programos](#RunFormatFromApp)

- [Suderinkite suprojektuotą ER sprendimą](#TuneSolution)

    - [Keiskite modelio žemėlapį](#ModifyModelMapping)

        - [Įtraukite duomenų šaltinį prieigai prie duomenų sutarties objekto](#AddDataSource1)
        - [Įtraukite duomenų šaltinį prieigai prie ER formato žemėlapio įrašų](#AddDataSource2)
        - [Įtraukti duomenų šaltinį prieigai prie formato žemėlapio ER formato įrašo vykdymo](#AddDataSource3)
        - [Įveskite vykdomo ER formato pavadinimą duomenų modelyje](#AddBinding)
        - [Užbaikite modelio žemėlapio dizainą](#CompleteModelMapping2)

    - [Keiskite formatą](#ModifyFormat)

        - [Įkelkite naują formato elementą](#AddFormatElement)
        - [Susiekite įkeltą formato elementą](#BindAddedFormatElement)
        - [Užbaikite formato projektavimą](#CompleteFormat2)

    - [Vykdykite formatą iš programos](#RunFormatFromApp2)
    - [Vykdykite formatą iš ER](#RunFormatFromER3)
    - [Konfigūruokite formato paskirtį ekrane rodomoje peržiūroje](#ConfigureDestination)
    - [Vykdykite formatą iš programos tam, kad peržiūrėtumėte jį kaip PDF dokumentą](#RunFormatFromApp3)

- [Papildomi ištekliai](#References)

Šiame pavyzdyje, sukursite naują ER sprendimą [Klausimynas](../../../human-resources/hr-learning-questionnaires.md) moduliui. Šis naujas ER sprendimas leidžia jums projektuoti ataskaitą naudojant „Microsoft Excel“ darbalapį kaip šabloną. Tuomet galite sukurti **Klausimyno** ataskaitą „Excel“ arba PDF formatu, taip pat sukurti esančią SQL serverio ataskaitos paslaugų ataskaitą SSRS. Taip pat galite keisti naują ataskaitą vėliau pagal užklausą. Kodavimas nebūtinas.

1. Tam, kad vykdytumėte esančią ataskaitą, eikite į **Klausimynas** \> **Projektavimas** \> **Klausimyno ataskaita**.

    ![Pasirinkite klausimyno ataskaitos meniu elementą klausimyno modulyje tam, kad vykdytumėte esančią SSRS ataskaitą](./media/er-quick-start1-application-menu-origin.png)

2. **Klausimyno ataskaitos** teksto laukelyje nurodykite atrankos kriterijus. Taikykite filtrą taip, kad ataskaita apimtų tik **SBCCrsExam** klausimyną.

    ![Atrankos kriterijų klausimyno ataskaitos teksto laukelyje nurodymas](./media/er-quick-start1-ssrs-report-dialog.png)

Toliau pateiktame paveikslėlyje rodoma bendra SSRS ataskaitos sukurta versija **SBCCrsExam** klausimynui.

![Sukurta SSRS ataskaita](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a>ER sistemos konfigūracija

Kaip elektroninės ataskaitos kūrėjo vaidmenyje esantis vartotojas, turite sukonfigūruoti mažiausią ER parametrų rinkinį prieš jums pradedant naudoti ER darbotvarkę jūsų naujo ER sprendimo projektavimui.

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a>ER parametrų konfigūravimas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Darbo srityje **Elektroninės ataskaitos** pasirinkite **Elektroninių ataskaitų parametrai**.
3. **Elektroninių ataskaitų parametrai** puslapyje **Bendra** skirtuke nustatykite **Įjungti dizaino režimą** parinktį į **Taip**.
4. **Priedai** skirtuke nustatykite tolesnius parametrus:

    - Nustatykite **Konfigūravimai** laukelį į **Failas** **USMF** bendrovei.
    - Nustatykite **Darbo archyvas**, **Laikinas**, **Pagrindinis** ir **Kiti** laukeliai į **Failas**.

Norėdami sužinoti daugiau apie ER parametrus, žr. [ER sistemos konfigūracija](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a>ER konfigūracijos tiekėjo aktyvavimas

Visi ER konfigūravimai yra pažymėti kaip turimi ER konfigūravimo tiekėjo. Dėl to, turite įjungti ER konfigūravimo tiekėją **Elektroninės ataskaitos** darbo srityje prieš tai, kai pradėsite įtraukti ar redaguoti visas ER konfigūracijas.

> [!NOTE]
> Tik ER konfigūracijos savininkas gali redaguoti. Todėl prieš redaguojant ER konfigūraciją atitinkamas ER konfigūracijos tiekėjas turi būti aktyvuotas **Elektroninė ataskaita** darbo srityje.

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a>ER konfigūracijos teikėjų sąrašo peržiūra

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Elektroninės ataskaitos** darbo srityje, **Susijusios nuorodos** skyriuje, pasirinkite **Konfigūravimo tiekėjai**.
3. **Konfigūravimo tiekėjai** puslapyje, visi konfigūravimo tiekėjo įrašai turi unikalų pavadinimą ir URL. Peržiūrėkite šio puslapio turinį. Jei įrašas, skirtas **Litware, Inc.** ( `https://www.litware.com`) jau yra, praleiskite sekančią procedūrą, [Pridėkite naują ER konfigūracijos teikėją](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a>Pridėkite naują ER konfigūracijos tiekėją

1. **Konfigūracijos tiekėjai** puslapyje pasirinkite **Nauja**.
2. Lauke **Pavadinimas** įveskite **Litware, Inc.**
3. **Internetinis adresas** lauke įveskite `https://www.litware.com`.
4. Pasirinkite **Įrašyti**.

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a>ER konfigūracijos tiekėjo aktyvavimas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Elektroninės ataskaitos** darbo srityje, pasirinkite **Litware, Inc.** konfigūravimo tiekėją.
3. Pasirinkite **Nustatyti kaip aktyvų**.

Daugiau informacijos apie ER konfigūracijos tiekėjus žr. [Konfigūracijos teikėjų kūrimas pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a>Suprojektuoti domeno konkretų duomenų modelį

Privalote sukurti naują ER konfigūraciją, kurioje yra verslo domeno **Klausimynas** komponentą [duomenų modelis](general-electronic-reporting.md#data-model-and-model-mapping-components). Šis duomenų modelis vėliau bus naudojamas kaip duomenų šaltinis, kai projektuosite ER formatą **Klausimyno** ataskaitos sukūrimui.

Atlikę žingsnius [Importuoti naują duomenų modelio konfigūravimą](#ImportDataModel) skyriuje, galite importuoti reikiamą duomenų modelį iš pateikto XML failo. Kitu atveju, galite atlikti žingsnius [Sukurti naują duomenų modelio konfigūravimą](#DesignDataModel) skyriuje tam, kad suprojektuotumėte šį duomenų modelį iš pradžių.

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a>Importuokite naują duomenų modelio konfigūraciją

1. Atsisiųskite [Klausimynų model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) failą ir įrašykite jį į savo vietinį kompiuterį.
2. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
3. **Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.
4. Veiksmų srityje pasirinkite **Pakeisti** \> **Įkelti iš XML failo**.
5. Pasirinkite **Naršyti** ir tuomet suraskite ir pasirinkite **Klausimynų model.version.1.xml** failą.
6. Pasirinkite **OK** tam, kad importuotumėte konfigūravimą.

Tam, kad tęstumėte, praleiskite kitą procedūrą, [Sukurti naują duomenų modelio konfigūravimą](#DesignDataModel).

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a>Sukurti naują duomenų modelio konfigūraciją

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. **Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.
3. Pasirinkite **Kurti konfigūraciją**.
4. Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **Klausimyno modelis**.
5. Pasirinkite **Sukurti konfigūravimą** tam, kad sukurtumėte konfigūravimą.

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a>Pavadinkite duomenų modelį

1. **Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno modelis**.
2. Pasirinkite **Dizaino įrankis**.
3. **Duomenų modelio kūrėjo** puslapyje, **Bendri** „FastTab“, **Pavadinimas** laukelyje įveskite <a name="DataModeName"></a>**Klausimynai**.

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a>Įtraukite naujus duomenų modelio laukelius

1. **Duomenų modelio kūrėjo** puslapyje, pasirinkite **Naujas**.
2. Iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:

    1. Pasirinkite **Modelio šaknis** kaip naujo modelio tipą.
    2. **Pavadinimas** laukelyje, įveskite <a name="RootDefinitionName"></a>**Šaknį**.
    3. Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują mazgą.

    Šis šaknies deskriptorius bus naudojamas duomenų pateikimui **Klausimyno** ataskaitoje. Vienas duomenų modelis gali turėti keletą deskriptorių. Visi deskriptoriai gali būti nurodyti vienam ER formatui tam, kad būtų atpažinti ataskaitos sukūrimui būtini duomenys.

3. Pasirinkite **Naujas** dar kartą ir tuomet iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:

    1. Pasirinkite **Įjungto mazgo vaikas** kaip naujo modelio tipą.
    2. **Pavadinimas** laukelyje, įveskite **Bendrovėspavadinimas**.
    3. Lauke **Elemento tipas** pasirinkite **Eilutė**.
    4. Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują laukelį.

    Šis laukelis yra būtinas esančios bendrovės pavadinimo perdavimui į ER ataskaitą, kuris naudoja šį duomenų modelį kaip duomenų šaltinį.

4. Pasirinkite **Naujas** dar kartą ir tuomet iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:

    1. Pasirinkite **Įjungto mazgo vaikas** kaip naujo modelio tipą.
    2. **Pavadinimas** laukelyje, įveskite **Klausimynas**.
    3. Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**.
    4. Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują laukelį.

    Šis laukelis bus naudojamas klausimyno sąrašo perdavimui į ER ataskaitą, kuri naudoja šį duomenų modelį kaip duomenų šaltinį.

5. Pasirinkite **Klausimynas** mazgą.
6. Tęskite redaguojamo duomenų modelio būtinų laukelių įtraukimą tokiu pačiu būdu, kol užbaigsite toliau pateiktų duomenų modelio struktūrą.

    | Lauko kelias                                                    | Duomenų tipas   | Laukelio projektavimas/grįžtamoji vertė |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | Šaknis                                                          |             | Ataskaitos taškas klausimyno duomenų užklausai. |
    | Šaknis\\Bendrovėspavadinimas                                             | Eilutė      | Esančios bendrovės pavadinimas. |
    | Šaknis\\Vykdymoturinys                                        | Įrašyti      | Vykdymo formato išsami informacija. |
    | Šaknis\\Vykdymoturinys\\Formatopavadinimas                            | Eilutė      | Vykdomo ER formato pavadinimas. |
    | Šaknis\\Klausimynas                                           | Įrašų sąrašas | Klausimynų sąrašas |
    | Šaknis\\Klausimynas\\Įjungtas                                   | Eilutė      | Esamo klausimyno statusas. |
    | Šaknis\\Klausimynas\\Kodas                                     | Eilutė      | Esamo klausimyno kodas. |
    | Šaknis\\Klausimynas\\Aprašas                              | Eilutė      | Esamo klausimyno aprašas. |
    | Šaknis\\Klausimynas\\Klausimynotipas                        | Eilutė      | Esamo klausimyno tipas. |
    | Šaknis\\Klausimynas\\Klausimynotvarka                            | Eilutė      | Esamo klausimyno eilės tvarka. |
    | Šaknis\\Klausimynas\\Rezultatogrupė                             | Įrašyti      | Esamo klausimyno eilės parametrų rezultatas. |
    | Šaknis\\Klausimynas\\Rezultatųgrupė\\Kodas                       | Eilutė      | Esamos rezultatų grupės identifikavimo kodas. |
    | Šaknis\\Klausimynas\\Rezultatųgrupė\\Aprašas                | Eilutė      | Esamo klausimyno rezultatų grupė. |
    | Šaknis\\Klausimynas\\Rezultatųgrupė\\Maks.taškųskaičius          | Tikrasis        | Maksimalus taškų skaičius, kurį galima gauti. |
    | Šaknis\\Klausimynas\\Klausimas                                 | Įrašų sąrašas | Esamo klausimyno klausimų sąrašas. |
    | Šaknis\\Klausimynas\\Klausimas\\Surinkimoeilėsnumeris       | Sveikasis skaičius     | Esamo atsakymo surinkimo eilės numeris. |
    | Šaknis\\Klausimynas\\Klausimas\\Id                             | Eilutė      | Esamos rezultatų grupės identifikavimo klausimas. |
    | Šaknis\\Klausimynas\\Klausimas\\Turibūtiužbaigtas                | Eilutė      | Vėliava rodanti, ar esamas klausimas turi būti atsakytas. |
    | Šaknis\\Klausimynas\\Klausimas\\Pirmasisklausimas                | Eilutė      | Vėliava rodanti, ar esamas klausimas yra pirmasis. |
    | Šaknis\\Klausimynas\\Klausimas\\Eilėsnumeris                 | Sveikasis skaičius     | Esamo klausimo eilės numeris. |
    | Šaknis\\Klausimynas\\Klausimas\\Tekstas                           | Eilutė      | Esamo klausimo tekstas. |
    | Šaknis\\Klausimynas\\Klausimas\\Atsakymas                         | Įrašų sąrašas | Esamo klausimo atsakymų sąrašas. |
    | Šaknis\\Klausimynas\\Klausimas\\Atsakymas\\Teisingasatsakymas          | Eilutė      | Vėliava rodanti, ar esamas atsakymas yra teisingas. |
    | Šaknis\\Klausimynas\\Klausimas\\Atsakymas\\Taškai                 | Tikrasis        | Taškai, kurie yra uždirbami, kai esamas atsakymas yra pasirenkamas. |
    | Šaknis\\Klausimynas\\Klausimas\\Atsakymas\\Eilėsnumeris         | Sveikasis skaičius     | Esamo atsakymo eilės numeris. |
    | Šaknis\\Klausimynas\\Klausimas\\Atsakymas\\Tekstas                   | Eilutė      | Esamo atsakymo tekstas. |

    Tolesnis paveikslėlis rodo užbaigtą redaguojamus duomenų modelį **Duomenų modelio kūrimo** puslapyje.

    ![Konfigūruotas duomenų modelis ER duomenų modelio kūrimo įrankyje](./media/er-quick-start1-model2.png)

7. Įrašykite pakeitimus.
8. Uždarykite **Duomenų modelio kūrimo** puslapį.

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a>Užbaikite duomenų modelio projektavimą

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno modelis**.
3. **Versijos** „FastTab“, pasirinkite konfigūravimo versiją, kuri turi statusą **Juodraštis**.
4. Pasirinkite **Keisti statusą** \> **Užbaigtas**.

Šios konfigūracijos versijos 1 statusas yra keičiamas iš **Juodraštis** į **Užbaigtas**. Versija 1 nebegali būti keičiama. Šioje versijoje yra konfigūruotų duomenų modelis ir gali būti naudojamas pagal kitas ER konfigūracijas. Šios konfigūracijos versija 2 yra sukurta ir turi **Juodraštis** statusą. Galite redaguoti šią versiją tam, kad keistumėte **Klausimyno** duomenų modelį.

![Redaguojamos ER konfigūracijos versijos konfigūravimo puslapyje](./media/er-quick-start1-model-configuration.png)

Dėl platesnės informacijos apie ER konfigūracijų versijas, žr. [Elektroninės ataskaitos (ER) peržiūra](general-electronic-reporting.md#component-versioning).

> [!NOTE]
> Konfigūruotas duomenų modelis yra **Klausimyno** verslo domeno bendra reprezentacija ir neturi jokio ryšio su artefaktais nurodytais „Microsoft Dynamics 365 Finance“.

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a>Suprojektuokite konfigūruoto duomenų modelio žemėlapį

Kaip vartotojas elektroninės ataskaitos kūrėjo vaidmenyje, turite sukurti naują ER konfigūravimą, kuris turi [modelio žemėlapį](general-electronic-reporting.md#data-model-and-model-mapping-components) komponentą **Klausimyno** duomenų modeliui. Kadangi šis komponentas įgyvendina konfigūruotų duomenų modelį finansams, jis yra skirtas būtent finansams. Privalote konfigūruoti modelio žemėlapio komponentą tam, kad nurodytumėte programos objektus, kurie turi būti naudojami konfigūruoto duomenų modelio užpildymui su programos duomenimis vykdymo metu. Šios užduoties atlikimui, turite žinoti duomenų struktūros implementavimo išsamius duomenis **Klausimyno** verslo domene finansuose.

Atlikę žingsnius [Naujo modelio žemėlapio konfigūravimo importavimo](#ImportModelMapping) toliau pateiktame skyriuje, galite importuoti būtiną modelį žemėlapio konfigūravimui iš pateikto XML failo. Kitu atveju, galite atlikti žingsnius [Naujo modelio žemėlapio konfigūravimo sukūrimas](#CreateModelMapping) skyriuje tam, kad suprojektuotumėte modelio žemėlapį iš pradžių.

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a>Importuokite naują modelio žemėlapio konfigūravimą

1. Atsisiųskite [Klausimynų mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) failą ir įrašykite jį į savo vietinį kompiuterį.
2. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
3. **Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.
4. Veiksmų srityje pasirinkite **Pakeisti** \> **Įkelti iš XML failo**.
5. Pasirinkite **Naršyti** ir tuomet suraskite ir pasirinkite **Klausimynų mapping.version.1.1.xml** failą.
6. Pasirinkite **OK** tam, kad importuotumėte konfigūravimą.

Tam, kad tęstumėte, praleiskite kitą procedūrą [Sukurti naują modelio žemėlapio konfigūravimą](#CreateModelMapping).

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a>Sukurkite naują modelio žemėlapio konfigūravimą

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno modelis**.
3. Pasirinkite **Kurti konfigūraciją**.
4. Išplečiamajame dialogo lange atlikite toliau nurodytus veiksmus.

    1. Laukelyje **Naujas** pasirinkite **Modelio žemėlapio kūrimas pagal duomenų modelio klausimynus**.
    2. **Pavadinimas** laukelyje, įveskite **Klausimyno žemėlapio kūrimas**.
    3. **Duomenų modelio sąvoka** laukelyje, pasirinkite **Šaknies** sąvoka.
    4. Pasirinkite **Sukurti konfigūravimą** tam, kad sukurtumėte konfigūravimą.

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a>Projektuokite naują modelio žemėlapio komponentą

1. **Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno žemėlapio kūrimas**.
2. Norėdami atidaryti susiejimų sąrašą, pasirinkite **Dizaino įrankis**.
3. Pasirinkite **Klausimyno žemėlapio kūrimas** žemėlapio kūrimą, kuris buvo automatiškai įtrauktas **Šaknies** sąvokai
4. Pasirinkite **Kūrimo įrankį** tam, kad pradėtumėte konfigūruoti pasirinktą žemėlapį.

Naujas žemėlapio kūrimas yra automatiškai įtrauktas **Šaknies** sąvokai. Šis žemėlapio kūrimas turi **Į modelį** paskirties vietą. Dėl to, šis žemėlapio kūrimas gali būti naudojamas duomenų modelio užpildymui būtinais duomenimis.

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a>Įtraukite duomenų šaltinius į prieigos programos lenteles

Privalote konfigūruoti duomenų šaltinius tam, kad prieitumėte prie programos lentelių, turinčių klausimyno išsamią informaciją.

1. **Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų šaltinio tipai** juostoje, pasirinkite **Dynamics 365 for Operations\\Lentelės įrašai**.
2. Įtraukite naują duomenų šaltinį, kuris bus naudojamas prieigai prie KMCollection lentelės, kurioje visi įrašai rodo vieną klausimyną:

    1. **Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.
    2. Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **Klausimynas**.
    3. **Lentelė** laukelyje, įveskite **KMCollection**.
    4. Nustatykite **Prašyti užklausos** parinktį į **Taip**. Galėsite tuomet nurodyti [filtravimo](../../fin-ops/get-started/advanced-filtering-query-options.md) parinktis šiai lentelei sistemos užklausos teksto laukelyje vykdymo metu.
    5. Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.

3. **Duomenų šaltinio tipai** juostoje pasirinkite **Dynamics 365 for Operations\\Lentelės įrašai**.
4. Įtraukite naują duomenų šaltinį, kuris bus naudojamas prieigai prie KMQuestion lentelės, kurioje visi įrašai rodo vieną klausimą klausimyne:

    1. **Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.
    2. Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **Klausimas**.
    3. **Lentelė** laukelyje, įveskite **KMQuestion**.
    4. Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.

5. **Duomenų šaltinio tipai** juostoje pasirinkite **Dynamics 365 for Operations\\Lentelės įrašai**.
6. Įtraukite naują duomenų šaltinio bandymą, kuris bus naudojamas prieigai prie KMAnswer lentelės, kurioje visi įrašai rodo vieną atsakymą į klausimą klausimyne:

    1. **Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.
    2. **Pavadinimas** laukelyje, įveskite **Atsakymas**.
    3. **Lentelė** laukelyje, įveskite **KMAnswer**.
    4. Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.

7. **Duomenų šaltinio tipai** juostoje, pasirinkite **Funkcijos\\Apskaičiuotas laukelis**.
8. Įtraukite naują apskaičiuotą laukelį, kuris bus naudojamas prieigai prie KMQuestionResultGroup lentelės įrašo iš kiekvienos susijusios KMCollection lentelės įrašo:

    1. **Duomenų šaltiniai** juostoje pasirinkite **Klausimynas**.
    2. Pasirinkite **Įtraukti**.
    3. Teksto laukelyje **Pavadinimas** laukelyje, įveskite **\$Rezultatogrupė**.
    4. Pasirinkite **Redaguoti formulę**.
    5. [ER formulės redaktoriuje](general-electronic-reporting-formula-designer.md), **Formulės** laukelyje įveskite **FIRSTORNULL(\@.'\<Sąsajos'.KMQuestionResultGroup)** tam, kad naudotumėte [kelią](er-formula-language.md#paths) vieno su daugeliu ryšyje tarp KMCollection ir KMQuestionResultGroup lentelių.
    6. Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.
    7. Pasirinkite **Gerai** tam, kad įtrauktumėte naują apskaičiuotą laukelį.

9. **Duomenų šaltinio tipai** juostoje, pasirinkite **Funkcijos\\Apskaičiuotas laukelis**.
10. Įtraukite naują apskaičiuotą laukelį, kuris bus naudojamas prieigai prie KMQuestionResultGroup klausimo įrašų iš kiekvienos susijusios KMCollectionQuestion lentelės įrašo:

    1. **Duomenų šaltiniai** juostoje pasirinkite **Klausimynas**.
    2. Išplėskite **\<Ryšiai** mazgą, kuris turi vieną su keliais ryšius KMCollection lentelę.
    3. Pasirinkite susijusią **KMCollectionQuestion** lentelę ir tuomet pasirinkite **Įtraukti**.
    4. Teksto laukelyje, **Pavadinimas** laukelyje įveskite **\$Klausimas**.
    5. Pasirinkite **Redaguoti formulę**.
    6. Formulės redaktoriuje **Formulės** laukelyje įveskite **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** tam, kad grąžintumėte atitinkamus klausimo įrašus iš KMQuestion lentelės.
    7. Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.
    8. Pasirinkite **Gerai** tam, kad įtrauktumėte naują apskaičiuotą laukelį.

11. **Duomenų šaltinio tipai** juostoje, pasirinkite **Funkcijos\\Apskaičiuotas laukelis**.
12. Įtraukite naują apskaičiuotą laukelį, kuris bus naudojamas prieigai prie KMAnswer atsakymo įrašų iš kiekvienos susijusios KMQuestion lentelės įrašo:

    1. **Duomenų šaltinio** juostoje pasirinkite **Klausimynas.\<Sąsajos.KMCollectionQuestion.\$Klausimas** ir tuomet pasirinkite **Įtraukti**.
    2. Teksto laukelyje, **Pavadinimas** laukelyje įveskite **\$Atsakymas**.
    3. Pasirinkite **Redaguoti formulę**.
    4. Formulės redaktoriaus laukelyje **Formulė** įveskite **FILTRAS (Atsakymas, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** tam, kad grįžtumėte prie atitinkamo atsakymo įrašų iš KMAnswer lentelės.
    5. Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.
    6. Pasirinkite **Gerai** tam, kad įtrauktumėte naują apskaičiuotą laukelį.

13. **Duomenų šaltinio tipai** juostoje pasirinkite **Dynamics 365 for Operations\\Lentelė**.
14. Įtraukite naują duomenų šaltinį, kuris bus naudojamas prieigos metodams CompanyInfo lentelėje. Atkreipkite dėmesį, kad **find()** metodas šioje lentelėje grįžta į įrašą rodantį esamos finansų instancijos bendrovę, kuriuo vadinamas šis žemėlapis.

    1. **Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.
    2. Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **CompanyInfo**.
    3. **Lentelė** laukelyje, įveskite **CompanyInfo**.
    4. Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a>Įtraukite duomenų šaltinius tam, kad prieitumėte prie programos numeracijų

Privalote konfigūruoti duomenų šaltinius prieigai prie programų numeracijų ir palyginti jų vertes su laukelių vertėmis **Numeracijos** tipo programos lentelėse. Privalote naudoti palyginimo rezultatą tam, kad užpildytumėte atitinkamus duomenų modelio laukelius.

1. **Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų šaltinio tipai** juostoje, pasirinkite **Dynamics 365 for Operations\\Numeracija**.
2. Įtraukite naują duomenų šaltinį, kuris bus naudojamas prieigos **EnumAppNoYes** numeracijai:

    1. **Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.
    2. Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **EnumAppNoYes**.
    3. **Numeracija** laukelyje, įveskite **NeTaip**.
    4. Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.

3. **Duomenų šaltinio tipai** juostoje pasirinkite **Dynamics 365 for Operations\\Numeracija**.
4. Įtraukite naują duomenų šaltinį, kuris bus naudojamas prieigos **KMCollectionQuestionMode** numeracijai:

    1. **Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.
    2. Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **EnumAppQuestionOrder**.
    3. **Numeracija** laukelyje, įveskite **KMCollectionQuestionMode**.
    4. Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a>Įtraukite ER žymes tam, kad sukurtumėte ataskaitą konkrečia kalba

Galite įtraukti ER žymes tam, kad konfigūruotumėte kai kuriuos savo duomenų šaltinius ir grąžintumėte vertes priklausančias nuo kalbos, nustatytos modelio žemėlapio iškvietimo turinyje.

1. **Modelio žemėlapio kūrimo įrankis** puslapyje **Duomenų šaltiniai** juostoje pasirinkite **Atsakymas** ir tuomet pasirinkite **Redaguoti**.
2. Įjunkite **Žymės** laukelį.
3. Pasirinkite **Versti**.
4. **Teksto vertimo** teksto laukelyje, pasirinkite šiuos žingsnius:

    1. **Žymos Id** laukelyje įveskite **Teigiamasatsakymas**.
    2. **Tekstas nustatytąja kalba** laukelyje įveskite **Taip**.
    3. Pasirinkite **Versti**.
    4. **Žymos Id** laukelyje įveskite **Neigiamasatsakymas**.
    5. **Tekstas nustatytąja kalba** laukelyje įveskite **Ne**.
    6. Pasirinkite **Versti**.

5. Uždarykite **Teksto vertimo** teksto laukelį.
6. Pasirinkite **Atšaukti**.

![ER žymių įtraukimas redaguojamam modelio žemėlapio kūrimui](./media/er-quick-start1-adding-labels.png)

Įvedėte ER žymes tik nustatytajai kalbai. Dėl informacijos apie tai, kaip ER žymės gali būti išverstos į kitas kalbas, žr. [Kelių kalbų ataskaitų projektavimas](er-design-multilingual-reports.md).

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a>Įtraukite duomenų šaltinį tam, kad paverstumėte numeracijos verčių lyginimo rezultatus į teksto vertes

Kadangi turite paversti palyginimo rezultatus tarp numeracijos verčių ir teksto verčių keletą kartų skirtingiems šaltiniams, būtų gerai konfigūruoti šią logiką kaip vieną duomenų šaltinį. Nepaisant to, tam, kad šis duomenų šaltinis galėtų būti dar kartą panaudojamas, tuomet turite sukonfigūruoti jį kaip parametrų duomenų šaltinį. Dėl išsamesnės informacijos, žr. [Palaikyti parametrų ER duomenų šaltinių skambučius apskaičiuotam laukelio tipui](er-calculated-field-type.md).

1. **Modelio žemėlapio kūrimo įrankio** puslapyje, **Duomenų šaltinio tipai** juostoje pasirinkite **Bendri\\Tuščia talpykla**.
2. Įtraukite naują talpyklos duomenų šaltinį:

    1. **Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.
    2. Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **Pagalbininkas**.
    3. Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinio talpyklą.

3. **Duomenų šaltinio tipai** juostoje, pasirinkite **Funkcijos\\Apskaičiuotas laukelis**.
4. Įtraukite naują duomenų šaltinį:

    1. **Duomenų šaltiniai** juostoje pasirinkite **Pagalbininkas**.
    2. Pasirinkite **Įtraukti**.
    3. Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **Klausimyno modelis**.
    4. Pasirinkite **Redaguoti formulę**.
    5. Formulės redaktoriuje pasirinkite **Parametrai**.
    6. Atlikite šiuos žingsnius tam, kad nurodytumėte parametrus konfigūruotai išraiškai:

        1. Pasirinkite **Naujas**.
        2. Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **Argumentas**.
        3. **Tipo** laukelyje pasirinkite **Boolean** duomenų tipą.
        4. Pasirinkite **Gerai**.

    7. **Formulės** laukelyje įveskite **IF (Argumentas = teisinga, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** tam, kad grąžintumėte tinkamos ER žymos tekstą priklausomai nuo vykdymo kalbos konteksto ir nurodyto parametro vertės.
    8. Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.
    9. Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.

![Konfigūruotas žemėlapio modelis ER duomenų žemėlapio modelio kūrimo įrankyje](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a>Susiekite duomenų šaltinius su duomenų modelio laukeliais

Privalote susieti konfigūruotus duomenų šaltinius į duomenų modelio laukelius tam, kad nurodytumėte, kaip duomenų modelis bus užpildytas programos duomenų vykdymo laike.

1. **Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų modelio** juostoje pasirinkite **BendrovėsPavadinimas**.
2. **Duomenų šaltiniai** juostoje išplėskite **Bendrovėsinformacija** ir tuomet atlikite šiuos žingsnius:

    1. Išplėskite **CompanyInfo.find()** mazgą, kuris atspindi **find()** metodą bendrovėsinformacijos lentelėje.
    2. Pasirinkite **CompanyInfo.find().Pavadinimą**.
    3. Pasirinkite **Susieti** tam, kad užpildytumėte bendrovės pavadinimą, kuris yra sukonfigūruotas modelio žemėlapio kūrimas, kuris iškviečiamas vykdymo laiko kontekste.

3. **Duomenų modelis** juostoje pasirinkite **Klausimynas**.
4. **Duomenų šaltiniai** juostoje pasirinkite **Klausimynas** ir tuomet pasirinkite **Susieti** tam, kad užpildytumėte klausimyno įrašus.
5. **Duomenų modelis** juostoje išplėskite **Klausimynas** ir tuomet atlikite šiuos žingsnius:

    1. **Duomenų modelis** juostoje pasirinkite **Įjungtas**.
    2. **Duomenų modelis** juostoje pasirinkite **Redaguoti**.
    3. **Formulės** laukelyje įveskite **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** tam, kad užpildytumėte nuo teksto ir kalbos priklausomą palyginimo rezultatą tarp numeracijos verčių.

6. Toliau tęskite duomenų šaltinių susiejimą su duomenų modelio laukeliais tokiu pačiu būdu, kol pasieksite tolesnį rezultatą.

    | Lauko kelias                                              | Duomenų tipas   | Veiksmas | Susiejimo išraiška |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | Bendrovėspavadinimas                                             | Eilutė      | Susieti   | CompanyInfo.'find()'.Pavadinimas |
    | Klausimynas                                           | Įrašų sąrašas | Susieti   | Klausimynas |
    | Klausimynas\\Įjungtas                                   | Eilutė      | Redagavimas   | Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes) |
    | Klausimyno\\Kodas                                     | Eilutė      | Susieti   | \@.kmCollectionId |
    | Klausimynas\\Aprašas                              | Eilutė      | Susieti   | \@.Aprašas |
    | Klausimynas\\Klausimynotipas                        | Eilutė      | Susieti   | \@.'&gt;Relations'.kmCollectionTypeId.Aprašas |
    | Klausimynas\\KlausimynoTvarka                            | Eilutė      | Redagavimas   | CASE (\@.questionMode,<br>EnumAppQuestionOrder.Conditional, "Conditional",<br>EnumAppQuestionOrder.Random, "Atsitiktinis (procentai klausimyne)",<br>EnumAppQuestionOrder.RandomGroup, "Atsitiktinis (procentai rezultato grupėse)",<br>EnumAppQuestionOrder.Sequence, "Nuoseklus",<br>"") |
    | Klausimynas\\Rezultatųgrupė                             | Įrašyti      |        | |
    | Klausimynas\\Rezultatųgrupė\\Kodas                       | Eilutė      | Susieti   | \@.'\$ResultGroup'.kmQuestionResultGroupId |
    | Klausimynas\\RezultatųGrupė\\Aprašas                | Eilutė      | Susieti   | \@.'\$ResultGroup'.aprašas |
    | Klausimynas\\RezultatųGrupė\\Maks.Taškųskaičius          | Tikrasis        | Susieti   | \@.'\$ResultGroup'.Maks.Taškai |
    | Klausimynas\\Klausimas                                 | Įrašų sąrašas | Susieti   | \@.'&lt;Ryšiai'.KMRinkimoKlausimas |
    | Klausimynas\\Klausimas\\RinkimoSekosNumeris       | Sveikasis skaičius     | Susieti   | \@.answerRinkimoSekosNumeris |
    | Klausimynas\\Klausimas\\Id                             | Eilutė      | Susieti   | \@.kmQuestionId |
    | Klausimynas\\Klausimas\\TuriBūtiUžbaigtas                | Eilutė      | Redagavimas   | Helper.NoYesEnumToString(\@.privalomas = EnumAppNoYes.Yes) |
    | Klausimynas\\Klausimas\\PirminisKlausimas                | Eilutė      | Susieti   | \@.parentQuestionId |
    | Klausimynas\\Klausimas\\EilėsNumeris                 | Sveikasis skaičius     | Susieti   | \@.EilėsNumeris |
    | Klausimynas\\Klausimas\\Tekstas                           | Eilutė      | Susieti   | \@.'\$Klausimo'.tekstas |
    | Klausimynas\\Klausimas\\Atsakymas                         | Įrašų sąrašas | Susieti   | \@.'\$Klausimas'.'\$Atsakymas' |
    | Klausimynas\\Klausimas\\Atsakymas\\TeisingasAtsakymas          | Eilutė      | Redagavimas   | Helper.NoYesEnumToString(\@.teisingasAtsakymas = EnumAppNoYes.Yes) |
    | Klausimynas\\Klausimas\\Atsakymas\\Taškai                 | Tikrasis        | Susieti   | \@.taškas |
    | Klausimynas\\Klausimas\\Atsakymas\\EilėsTvarka         | Sveikasis skaičius     | Susieti   | \@.eilėsNumeris |
    | Klausimynas\\Klausimas\\Atsakymas\\Tekstas                   | Eilutė      | Susieti   | \@.tekstas |

    Tolesnis paveikslėlis rodo galutinį konfigūruoto modelio žemėlapio statusą **Modelio žemėlapio kūrimo įrankio** puslapyje.

    ![Visiškai konfigūruotas žemėlapio modelis ER duomenų žemėlapio modelio kūrimo įrankyje](./media/er-quick-start1-mapping2.png)

7. Įrašykite pakeitimus.
8. Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a>Užbaikite modelio žemėlapio dizainą

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno žemėlapio kūrimas**.
3. **Versijos** „FastTab“, pasirinkite konfigūravimo versiją, kuri turi statusą **Juodraštis**.
4. Pasirinkite **Keisti statusą** \> **Užbaigtas**.

Šios konfigūracijos versijos 1.1 statusas yra keičiamas iš **Juodraštis** į **Užbaigtas**. Versija 1.1 nebegali būti keičiama. Šioje versijoje yra konfigūruotų žemėlapio modelis ir gali būti naudojamas pagal kitas ER konfigūracijas. Šios konfigūracijos versija 1.2 yra sukurta ir turi **Juodraštis** statusą. Galite redaguoti šią versiją tam, kad keistumėte **Klausimyno žemėlapio** konfigūravimą.

![Redaguojamos ER konfigūracijos versijos konfigūravimo puslapyje](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> Konfigūruotas modelio žemėlapis yra jūsų finansų konkretus abstrakčių duomenų modelio implementavimas, kuris rodo **Klausimyno** verslo domeną.

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a>Suprojektuokite tinkintos ataskaitos šabloną

ER darbotvarkė naudoja iš anksto nustatytus šablonus tam, kad sukurtų ataskaitas „Microsoft Office“ formatuose („Excel“ darbo knygose ar „Word“ dokumentuose). Kol būtina ataskaita yra kuriama, šablonas yra užpildomas su būtinais duomenimis pagal konfigūruotą darbo srautą. Dėl to, pirmiausia turite projektuoti šabloną jūsų tinkintai ataskaitai. Ši ataskaita turi būti sukurta kaip „Excel“ darbo knyga, struktūra rodo tinkintos ataskaitos maketą. Privalote užvadinti visus „Excel“ elementus, kuriuos planuojate užpildyti būtinais duomenimis.

1. Atsisiųskite [Klausimynų ataskaitos template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) failą ir įrašykite jį į savo vietinį kompiuterį.
2. Atverkite failą „Excel“ ir peržiūrėkite darbo knygos struktūrą.

Kaip rodo tolesnis paveikslėlis, atsiųstas šablonas buvo suprojektuotas konkrečių klausimynų spausdinimui, kurie rodo klausimyno klausimus kartu su atitinkamais atsakymais.

![„Excel“ šablonas konkrečių klausimų spausdinimui](./media/er-quick-start1-template-layout.png)

„Excel“ pavadinimai buvo įtraukti į šį šabloną tam, kad būtų užpildyta išsami klausimyno informacija. Galite naudoti vadovo pavadinimą „Excel“ pavadinimo peržiūrai.

![Pavadinimo vadovo naudojimas „Excel“ pavadinimų peržiūrai „Excel“ šablone](./media/er-quick-start1-template-names.png)

Ataskaitos žymės buvo įkeltos kaip fiksuotas tekstas anglų kalba. Galite pakeisti ataskaitos žymes naujais „Excel“ pavadinimais, kurie užpildo žymes nuo kalbos priklausomu tekstu naudojant ER formatą [žymes](#AddMmLabels), taip kaip padarėte nuo kalbos priklausomomis sąvokomis konfigūruotame modelio žemėlapyje. Šiuo atveju, ER žymės turi būti įtrauktos į redaguojamą ER formatą.

Kaip rodo tolesnis paveikslėlis, tinkinta ataskaitos antraštė buvo nurodyta siekiant įjungti „Excel“ puslapių numeravimui.

![Tinkinta ataskaitos antraštė pateiktame „Excel“ šablone](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a>Formato kūrimas

Kaip vartotojas elektroninės ataskaitos funkcijų konsultanto vaidmenyje, turite sukurti naują ER konfigūraciją, kurioje būtų [formato](general-electronic-reporting.md#FormatComponentOutbound) komponentas. Turite sukonfigūruoti formato komponentą tam, kad nurodytumėte, kaip ataskaitos šablonas bus užpildytas su būtinais duomenimis vykdymo laiku.

Atlikę žingsnius [Importuoti suprojektuoto formato konfigūravimą](#FormatImport) skyriuje, galite importuoti reikiamą formatą pateiktame XML faile. Kitu atveju, galite atlikti žingsnius [Sukurti naują formato konfigūravimą](#FormatCreate) skyriuje, kad suprojektuotumėte šį formatą iš pradžių.

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a>Importuokite suprojektuotą formato konfigūravimą

1. Atsisiųskite [Klausimynų format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) failą ir įrašykite jį į savo vietinį kompiuterį.
2. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
3. **Elektroninės ataskaitos** darbo srityje pasirinkite **Ataskaitos konfigūravimai**.
4. Veiksmų juostoje pasirinkite **Keisti** \> **Įkelti iš XML failo**.
5. Pasirinkite **Naršyti** ir tuomet suraskite ir pasirinkite **Klausimynų format.version.1.1.xml** failą.
6. Pasirinkite **OK** tam, kad importuotumėte konfigūravimą.

Tam, kad tęstumėte, praleiskite kitą procedūrą, [Sukurti naujo formato konfigūravimą](#FormatCreate).

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a>Kurti naują formato konfigūraciją
 
1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno modelis**.
3. Pasirinkite **Kurti konfigūraciją**.
4. Išplečiamajame dialogo lange atlikite toliau nurodytus veiksmus.

    1. **Naujas** laukelyje, pasirinkite **Formatas pagal duomenų modelio klausimynus**.
    2. **Pavadinimas** laukelyje, įveskite **Klausimyno ataskaita**.
    3. **Duomenų modelio versijos** laukelyje pasirinkite **1**.

        > [!NOTE]
        > - Jei pasirenkate konkrečia bazinio duomenų modelio versiją, atitinkamos duomenų modelio versijos struktūra bus rodoma jums kaip **Modelio** duomenų šaltinio struktūra sukurtame formate.
        > - Galite palikti šį laukelį tuščią. Tokiu atveju, **Juodraščio** duomenų modelio versijos struktūra bus rodoma jums kaip **Modelio** duomenų šaltinio struktūra sukurtu formatu. Tuomet galite keisti savo modelį ir nedelsiant matyti pakeitimus savo formate. Tokia prieiga gali pagerinti ER sprendimo projekto efektyvumą jums konfigūruojant savo duomenų modelį, modelio žemėlapio kūrimas ir formatą vienu metu.
        > - Jei pasirenkate konkrečią bazinio duomenų modelio versiją, galite perjungti į naudojimą **Juodraščio** versijos vėliau, kai pradėsite redaguoti formatą.

    4. **Duomenų modelio sąvoka** laukelyje, pasirinkite **Šaknies** sąvoka.

5. Pasirinkite **Sukurti konfigūravimą** tam, kad sukurtumėte konfigūravimą.

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a>Importuokite ataskaitos šabloną

1. **Konfigūravimai** puslapyje, konfigūravimo medyje, pasirinkite **Klausimyno ataskaita**.
2. Pasirinkite **Kūrimo įrankį** tam, kad konfigūruotumėte tinkintą formatą.
3. **Formato kūrimo įrankio** puslapyje, veiksmų juostoje pasirinkite  **Importuoti** \> **Importuoti iš „Excel“**.
4. Teksto laukelyje, pasirinkite šiuos žingsnius:

    1. Pasirinkite **Įtraukti šabloną**.
    2. Suraskite ir pasirinkite vietiniu lygmeniu įrašytus **Klausimynų ataskaitos template.xslx** failą ir tuomet pasirinkite **Atverti**.
    3. Pasirinkite **Gerai** tam, kad importuotumėte šabloną.

    ![Ataskaitos šablono importavimas](./media/er-quick-start1-template-import.png)

**„Excel“\\faile** formato elementas yra automatiškai įtrauktas į redaguojamą formatą kaip šaknies elementas. Taip pat, arba **„Excel“\\Intervalo** formato elementas arba **„Excel“\\Laukelis** formato elementas yra automatiškai įtraukiamas visiems „Excel“ atpažįstamiems importuoto šablono pavadinimams. **„Excel“\\Antraštės** formatas buvo patalpintas į lizdą **Eilutės** elemente yra automatiškai įtraukiamas taip, kad rodytų antraštės nustatymus importuotame šablone.

![Formato struktūra apima automatiškai įtrauktus elementus ER veikimo kūrimo įrankyje](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a>Konfigūruokite formatą

1. **Formato kūrimo įrankio** puslapyje, formato medyje pasirinkite **„Excel“** šaknies elementą.
2. **Formato** skirtuke dešinėje puslapio pusėje, **Pavadinimo** laukelyje įveskite <a name="AddFormatRootElement"></a>**Atskaitą**.
3. **Kalbos pirmenybės** laukelyje pasirinkite **Vartotojo pirmenybės** tam, kad vykdytumėte ataskaitą vartotojo pirmenybine kalba.
4. **Kultūros pirmenybės** laukelyje pasirinkite **Vartotojo pirmenybės** tam, kad vykdytumėte ataskaitą vartotojo pirmenybine kultūra.

    Dėl informacijos apie tai, kaip nurodyti kalbos ir kultūros kontekstus ER procesui, žr. [Kelių kalbų ataskaitų projektavimas](er-design-multilingual-reports.md).

    ![Kalbos ir kultūros nustatymų konfigūravimas pasirinktai ataskaitai ER veiksmų kūrimo įrankyje](./media/er-quick-start1-template-format-structure1.png)

5. Formato medyje išplėskite šaknies lizdą ir tuomet pasirinkite **RezultatųGrupė**.
6. **Formato** skirtuke, **Atkartojimo kryptis** laukelyje pasirinkite **Jokio atkartojimo**, nes nesitikite turėti daugiau nei vienos rezultatų grupės vienam klausimynui.

    ![Atkartojimo krypties nustatymas intervalo formato elementams ER veikimo kūrimo įrankyje](./media/er-quick-start1-template-format-structure2.png)

7. Pasirinkite **Įrašyti**.

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a>Nustatykite duomenų susiejimą ataskaitos pavadinimui

Privalote nurodyti duomenų susiejimą formato elementui, kuris yra naudojamas užpildyti sukurtos ataskaitos pavadinimą.

1. **Formato kūrimo įrankio** puslapyje, **Žemėlapio kūrimo** skirtuke dešinėje pasirinkite **Ataskaita\\Ataskaitos pavadinimas** elementą.
2. Pasirinkite **Redaguoti formulę**.
3. Formulės redaktoriuje pasirinkite **Versti**.
4. **Teksto vertimo** teksto laukelyje, pasirinkite šiuos žingsnius:

    1. **Žymos ID** laukelyje įveskite **Ataskaitopavadinimas**.
    2. **Tekstas nustatytąja kalba** laukelyje įveskite **Klausimyno ataskaita**.
    3. Pasirinkite **Versti**, tuomet pasirinkite **Įrašyti**.
    4. Pasirinkite **Versti** tam, kad užvertumėte **Teksto vertimo** teksto laukelį.

5. Uždarykite formulės redaktorių.

    ![Konfigūruokite susiejimą sukurtos ataskaitos pavadinimo užpildymui](./media/er-quick-start1-add-report-title-label.png)

Galite naudoti šią techniką tam, kad paverstumėte visas kitas esamo šablono žymes priklausomas nuo kalbos. Dėl informacijos apie tai, kaip vieno ER konfigūravimo žymės gali būti išverstos į visas palaikomas kalbas, žr. [Kelių kalbų ataskaitų projektavimas](er-design-multilingual-reports.md).

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a>Peržiūrėkite modelio duomenų šaltinį

1. **Formato kūrimo** puslapyje, **Žemėlapio** skirtuke pasirinkite <a name="ModelDSName"></a>**modelio** duomenų šaltinį, kuris rodo pagrindinį šio ER formato duomenų modelį.
2. Pasirinkite **Redaguoti**.
3. Peržiūrėkite informaciją esančią **Duomenų šaltinio ypatybės** teksto laukelyje. Šis duomenų šaltinis rodo **Klausimynų** duomenų modelio komponento versiją 1, kuri yra **Klausimynų modelio** ER konfigūravime.

![Modelio duomenų šaltinio ypatybės ER veikimo kūrimo įrankyje](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a>Susiekite formato elementus su duomenų šaltinio laukeliais

Tam, kad nurodytumėte, kaip šablonas yra užpildomas vykdymo laiku, privalote susieti visus formato elementus, susijusius su atitinkamu „Excel“ pavadinimu į vieną šio formato duomenų šaltinio laukelį.

1. **FFormato kūrimo įrankio** puslapyje, formato medyje, pasirinkite **Ataskaita\\BendrovėsPavadinimo** formato elementą.
2. **Žemėlapio kūrimas** skirtuke, pasirinkite **model.BendrovėPavadinimo** duomenų šaltinio laukelius **Eilutė** tipe.
3. Pasirinkite **Susieti** tam, kad įvestumėte bendrovės pavadinimą šablone.
4. Formato medyje pasirinkite **Ataskaita\\Klausimynas** elementą.
5. **Žemėlapio kūrimas** skirtuke, pasirinkite **model.Klausimynas** duomenų šaltinio laukelius **Įrašo sąrašas** tipe.
6. Pasirinkite **Susieti**.
7. Pasirinkite **Rodyti išsamią informaciją** tam, kad matytumėte daugiau išsamios informacijos formato elementams.

    **Klausimynas** intervalo formato elementas yra sukonfigūruotas vertikaliam atkartojimui. Kai jis susietas su duomenų šaltinius **Įrašo sąrašo** tipe, atitinkamas **Klausimyno** intervalas „Excel“ šablone yra kartojamas kiekvienam susieto duomenų šaltinio įrašui.
 
    ![Klausimyno intervalo formato elemento susiejimas su atitinkamais įrašo sąrašo duomenų šaltiniais ER veikimo kūrimo įrankyje](./media/er-quick-start1-bindings1.png)

    Kadangi **Klausimyno** intervalas „Excel“ šablone yra nurodytas tarp 5 per 14, šios eilutės yra atkartojamos visiems ataskaitos klausimynams.

    ![Eilutės „Excel“ šablone, kurios bus atkartotos sukurtoje ataskaitoje kiekvienam įrašui įrašo sąrašo duomenų šaltiniuose](./media/er-quick-start1-template-questionnaire-range.png)

8. Konfigūruoti panašius susiejimus likusiems formato elementams, kaip aprašyta tolesnėje lentelėje.

    > [!NOTE]
    > Šioje lentelėje, „Duomenų šaltinio kelio“ informacijos stulpelis daro prielaidą, kad [atitinkamas kelias](relative-path-data-bindings-er-models-format.md) ER funkcija yra įjungta.

    | Formato elemento kelias                                      | Duomenų šaltinio kelias |
    |----------------------------------------------------------|------------------|
    | „Excel“\\AtaskaitosPavadinimas                                       | **\@"GER\_LABEL:ReportTitle"** |
    | „Excel“\\BendrovėsPavadinimas                                       | **model.CompanyName** |
    | „Excel“\\Klausimynas                                     | **model.Questionnaire** |
    | „Excel“\\Klausimynas\\Įjungtas                             | **\@.Įjungtas**, kai **\@** yra **modelio.Klausimynas** |
    | „Excel“\\Klausimynas\\Kodas                               | **\@.Kodas** |
    | „Excel“\\Klausimynas\\Aprašas                        | **\@.Aprašas** |
    | „Excel“\\Klausimynas\\Klausimynotipas                  | **\@.KlausimynoTipas** |
    | „Excel“\\Klausimynas\\Klausimynotvarka                      | **\@.KlausimynoTvarka** |
    | „Excel“\\Klausimynas\\RezultatųGrupė\\Kodas\_               | **\@.RezultatųGrupės.Kodas** |
    | „Excel“\\Klausimynas\\RezultatųGrupė\\Aprašas\_        | **\@.RezultatųGrupės.Aprašas** |
    | „Excel“\\Klausimynas\\Rezultatųgrupė\\Maks.taškųskaičius    | **\@.RezultatųGrupė.Maks.taškųskaičius** |
    | „Excel“\\Klausimynas\\Klausimas                           | **\@.Klausimas** |
    | „Excel“\\Klausimynas\\Klausimas\\Surinkimoeilėsnumeris | **\@.CollectionSequenceNumber**, kai **\@** yra **modelio.Klausimynas.Klausimas** |
    | „Excel“\\Klausimynas\\Klausimas\\Id                       | **\@.Id** |
    | „Excel“\\Klausimynas\\Klausimas\\Turibūtiužbaigtas          | **\@.Turibūtiužbaigtas** |
    | „Excel“\\Klausimynas\\Klausimas\\Pirmasisklausimas          | **\@.PirmasisKlausimas** |
    | „Excel“\\Klausimynas\\Klausimas\\Eilėsnumeris           | **\@.EilėsNumeris** |
    | „Excel“\\Klausimynas\\Klausimas\\Tekstas                     | **\@.Tekstas** |
    | „Excel“\\Klausimynas\\Klausimas\\Atsakymas                   | **\@.Atsakymas** |
    | „Excel“\\Klausimynas\\Klausimas\\Atsakymas\\Teisingasatsakymas    | **\@.TeisingasAtsakymas**, kai **\@** yra **modelio.Klausimynas.Atsakymas** |
    | „Excel“\\Klausimynas\\Klausimas\\Atsakymas\\Taškai           | **\@.Taškai** |
    | „Excel“\\Klausimynas\\Klausimas\\Atsakymas\\Tekstas             | **\@.Tekstas** |

9. Jums pabaigus, pasirinkite **Įrašyti**.

Toliau pateiktas paveikslėlis rodo galutinį sukonfigūruotų susietus duomenis **Formato žemėlapio kūrimo įrankio** puslapyje.

![Konfigūruotas duomenų susiejimas ER veikimo kūrimo įrankyje](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> Visa konkrečių duomenų šaltinių ir susiejimų kolekcija rodo formato žemėlapio komponentą konfigūruotam formatui. Šio formato žemėlapio kūrimas yra iškviečiamas jums vykdant konfigūruotą formatą ataskaitos kūrimui.

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a>Vykdykite suprojektuotą formatą iš ER

Dabar galite vykdyti suprojektuotą formatą bandymo tikslais iš **Konfigūravimo** puslapio.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūravimo** puslapyje, konfigūravimo medyje, išplėskite **Klausimyno modelį** ir tuomet pasirinkite **Klausimyno ataskaitą**.
3. Pasirinkite **Kūrimo įrankį** formato versijai,, kuri turi statusą **Juodraštis**.
4. Puslapyje **Formato dizaino įrankis** pasirinkite **Vykdyti**.
5. **ER parametrai** teksto laukelyje, **Apimami įrašai** „FastTab“, konfigūruokite filtravimo parinktis taip, kad tik **SBCCrsExam** klausimynas būtų įtrauktas.
6. Pasirinkite **Gerai** filtravimo parinkties patvirtinimui.
7. Pasirinkite **Gerai** ataskaitos vykdymui.
8. Peržiūrėkite sukurtą ataskaitą.

Pagal [nutylėjimą](electronic-reporting-destinations.md#default-behavior), sukurta ataskaita yra pristatoma „Excel“ faile, kurį galite atsisiųsti. Tolesni paveikslėliai rodo du „Excel“ formatų sukurtos ataskaitos puslapius.

![„Excel“ formatų sukurtos ataskaitos pavyzdys, puslapis 1](./media/er-quick-start1-report1a.png)

![„Excel“ formatų sukurtos ataskaitos pavyzdys, puslapis 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a>Suderinkite projektavimo formatą

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a>Keiskite formatą tam, kad pakeistumėte sukurto dokumento pavadinimą

Pagal nutylėjimą, sukurtas dokumentas yra pavadintas naudojant esamo vartotojo slapyvardį. Keisdami formatą galite pakeisti šią elgseną taip, kad sukurtas dokumentas būtų pavadintas pagal jūsų tinkintą logiką. Pavyzdžiui, sugeneruoto dokumento pavadinimas gali būti paremtas esamos datos ir laiko sesija ir ataskaitos pavadinimu.

1. **Formato kūrimo įrankio** puslapyje, formato medyje pasirinkite **„Ataskaita“** šaknies elementą.
2. **Žemėlapis** skirtuke pasirinkite **Redaguoti failo pavadinimą**.
3. **Formulės** laukelyje įveskite **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.
4. Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.
5. Pasirinkite **Įrašyti**.

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a>Keiskite formatą tam, kad pakeistumėte klausimų seką

Klausimai yra teisingai išrikiuoti sukurtoje ataskaitoje. Galite keisti tvarką keisdami formatą.

1. **Formato kūrimo įrankio** puslapyje, formato medyje pasirinkite **„Ataskaita“** šaknies elementą.
2. **Žemėlapio** skirtuke, formato medyje, išplėskite **Ataskaita\\Klausimynas\\Klausimas**.

    ![Klausimo formato intervalo tipo elementas ER veikimo kūrimo įrankyje](./media/er-quick-start1-bindings3.png)

3. **Žemėlapis** skirtuke pasirinkite **modelio.Klausimynas**.
4. Pasirinkite **Įtraukti** \> **Funkcijos\\Apskaičiuotas laukelis** ir tuomet **Pavadinimo** laukelyje įveskite **IšrikiuotiKlausimai**.
5. Pasirinkite **Redaguoti formulę**.
6. Formulės redaktoriuje, **Formulės** laukelyje įveskite **RIKIUOTIPAGAL (modelis.Klausimynas.Klausimas, modelis.Klausimynas.Klausimas.EilėsTvarka)** tam, kad išrikiuotumėte klausimų sąrašą pagal esamą klausimyną eilės tvarkos skaičiais.
7. Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.
8. Pasirinkite **Gerai** tam, kad užbaigtumėte naujo apskaičiuoto laukelio įvedimą.
9. **Žemėlapis** skirtuke pasirinkite **modelio.Klausimynas.IšrikiuotiKlausimai**.
10. Formato medyje pasirinkite **„Excel“\\Klausimynas\\Klausimas**.
11. Pasirinkite **Susieti** ir tuomet patvirtinkite, kad esamas **modelis.Klausimynas.Klausimai** kelias yra pakeistas nauju **modeliu.Klausimynu.IšrikiuotiKlausimai** keliu visų lizduose esančių elementų susiejime.
12. Pasirinkite **Įrašyti**.

![Susiekite klausimų formato elementą su konfigūruotu išriškiuotųklausimų duomenų šaltiniu ER veikimo kūrimo įrankyje](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a>Vykdykite pakeistą formatą iš ER

Dabar galite vykdyti pakeistą formatą bandymo tikslais iš ER darbotvarkės.

1. Puslapyje **Formato dizaino įrankis** pasirinkite **Vykdyti**.
2. **ER parametrai** teksto laukelyje, **Apimami įrašai** „FastTab“, konfigūruokite filtravimo parinktis taip, kad tik **SBCCrsExam** klausimynas būtų įtrauktas.
3. Pasirinkite **Gerai** filtravimo parinkties patvirtinimui.
4. Pasirinkite **Gerai** ataskaitos vykdymui.
5. Peržiūrėkite sukurtą ataskaitą.

Tolesnis paveikslėlis rodo „Excel“ formatu sukurtą ataskaitą, kurioje klausimai yra teisingai išrikiuoti.

![Sukurta ataskaita „Excel“ formatu turi tinkamai išrikiuotus klausimus](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a>Užbaikite formato projektavimą

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūravimai** puslapyje, konfigūravimo medyje, išplėskite **Klausimyno modelį** ir tuomet pasirinkite **Klausimyno ataskaitą**.
3. **Versijos** „FastTab“, pasirinkite konfigūravimo versiją, kuri turi statusą **Juodraštis**.
4. Pasirinkite **Keisti statusą** \> **Užbaigtas**.

Šios konfigūracijos versijos 1.1 statusas yra keičiamas iš **Juodraštis** į **Užbaigtas**. Versija 1.1 nebegali būti keičiama. Šioje versijoje yra konfigūruotas formatas ir gali būti naudojamas jūsų tinkintos ataskaitos spausdinimui. Šios konfigūracijos versija 1.2 yra sukurta ir turi **Juodraštis** statusą. Galite redaguoti šią versiją tam, kad keistumėte jūsų ataskaitos **Klausimyno** formatą.

![Redaguojamos ER konfigūracijos versijos konfigūravimo puslapyje](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> Konfigūruotas formatas yra jūsų suprojektuota  **Klausimyno** ataskaita ir neturi jokių sąsajų su finansų artefaktais.

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a>Vystykite programos artefaktus tam, kad iškviestumėte suprojektuotą ataskaitą

Kaip vartotojas sistemos administratoriaus vaidmenyje, privalote vystyti naują logiką taip, kad konfigūruotas ER formatas galėtų būti iškviestas programos vartotojo sąsajos (UI) siekiant sukurti jūsų tinkintą ataskaitą. Šiuo metu, ER nesiūlo jokių galimybių konfigūruoti tokio tipo logikos. Dėl to, reikalingas nedidelis inžinerinis darbas. 

Naujos logikos sukūrimui, privalote talpinti topologiją, galinčią palaikyti nuolatinį kūrimą. Daugiau informacijos žr. [Visuotinis topologijų, palaikančių nuolatinio komponavimo versijų ir testavimo automatizavimo funkciją, diegimas](../perf-test/continuous-build-test-automation.md). Taip pat jums reikia prieigos prie šios topologijos kūrimo aplinkos. Dėl platesnės informacijos apie prieinamus ER API, žr. [ER darbotvarkės API](er-apis-app73.md).

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a>Šaltinio kodo modifikavimas

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a>Įtraukite duomenų sutarties klasę

Įtraukite naują **KlausimynoERataskaitossutarties** klasę į savo „Microsoft Visual Studio“ projektą ir parašykite kodą, kuris nurodo duomenų sutartį, naudotiną konfigūruoto ER formato vykdymui.

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a>Įtraukite UI kūrėjo klasę

Įtraukite naują **KlausimynoERAtaskaitosUIkūrėjo** klasę į savo „Microsoft Visual Studio“ projektą ir parašykite kodą, kuriuo bus sukuriamas vykdymo laiko teksto laukelis naudojamas būtino vykdyti ER formato ieškojimo žemėlapio ID. Pateiktas kodas ieško tik ER formatų, kurie gali turėti duomenų šaltinį **Duomenų modelio** tipo, kuris nurodo į **[Klausimynus](#DataModeName)** duomenų modelį naudojant **[Šaknies](#RootDefinitionName)** sąvoką.

> [!NOTE]
> Kitu atveju, galite naudoti ER integravimo taškus siekiant filtruoti ER formatus. Dėl išsamesnės informacijos, žr. [API formato žemėlapio paieškos rodymui](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a>Įtraukite duomenų tiekėjo klasę

Įtraukite naują **KlausimynoErAtaskaitosDP** klasę į savo „Microsoft Visual Studio“ projektą ir parašykite kodą, kuris pateikia duomenų tiekėją, naudotiną konfigūruoto ER formato vykdymui. Pateiktas kodas apima tik šio duomenų tiekėjo sutarties duomenis.

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a>Įtraukite žymių failą

Įtraukite naujas **QuestionnairesErReportLabels\_en-US** žymių failą savo „Visual Studio“ projektui ir nurodykite tolesnes žymes naujiems UI šaltiniams:

- **\@KlausimynoAtaskaita** žymė naujam meniu elementui, turinčiam tolesnį tekstą JAV anglų k. (en-US): **Klausimyno ataskaita (įjungta ER)**
- **\@QuestionnairesReportBatchJobDescription** žymė paketo darbo pavadinimui, jei pasirinktas ER formatas yra nustatytas paketo darbo vykdymui.

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a>Įtraukite ataskaitos paslaugos klasę

Įtraukite naują **KlausimynoERAtaskaitosPaslaugų** klasę į savo „Microsoft Visual Studio“ projektą ir parašykite kodą, kuris iškviečia ER formatą, atpažįsta jį formatuodamas žemėlapio ID ir pateikia duomenų sutartį kaip parametrą.

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

Kai turite naudoti ER formatą vykdantį programos duomenis, privalote konfigūruoti duomenų šaltinį **Duomenų modelio** tipe formato žemėlapyje. Šis duomenų šaltinis rodo į konkrečią konkrečių duomenų modelio dalį naudodamas vienos šaknies sąvoką. Kai ER formatas yra vykdomas, jis iškviečia duomenų šaltinį prieigai prie tinkamo ER modelio žemėlapio, kuris yra konfigūruotas pagal esamą modelį ir šaknies sąvoką.

Visa informacija, kurią jums gali reikėti parengti šaltinio kode yra laikyti kaip duomenų sutarties dalį, gali būti pakeista vykdant ER formatą ir naudojant šio tipo ER modelio žemėlapį. ER modelio žemėlapio kūrime, turite konfigūruoti **Objekto** tipo duomenų šaltinį, kuris rodo į **[KlausimynoErAtaskaitosSutarties](#DataContractClass)** klasę. Siekiant atpažinti modelio žemėlapį, turite nurodyti duomenų šaltinį, kuris iškviečia modelio žemėlapį. Pateiktame kode, šis duomenų šaltinis nurodytas **ERmodelioduomenųšaltiniopavadinimas** konstantoje turi **[modelio](#ModelDSName)** vertę. Siekiant atpažinti, kuris duomenų šaltinis yra naudojamas duomenų sutarties rodymui modelio žemėlapyje, turite nurodyti duomenų šaltinio pavadinimą. Pateiktame kode, šis pavadinimas yra nurodytas **ParametrųDuomenųŠaltinioPavadinimas** konstantoje, kuri turi <a name="DataContractDSName"></a>**VykdomoLaikoParametrų** vertę.

> [!NOTE]
> Naujoje aplinkoje, jums gali reikėti atnaujinti ER metaduomenis taip, kad šis klasės tipas būtų prieinamas ER modelio žemėlapio kūrimo įrankyje. Dėl platesnės informacijos, žr. [Konfigūruoti ER darbotvarkę](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a>Įtraukite ataskaitos valdiklio klasę

Įtraukite naują **QuestionnairesErReportController** klasę savo „Visual Studio“ projektui ir parašykite kodą, kuris vykdo ER formatą sinchroniniu būdu ar paketo būdu, kaip jums patogu, teksto laukelyje, kuris yra sukurtas pagal logiką pateiktą **QuestionnairesErReportUIBuilder** klasėje.

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a>Įtraukite meniu elementą

Įtraukite naują **QuestionnairesErReport** meniu elementą į savo „Visual Studio“ projektą. **Objekto** ypatybėse, šis meniu rodo į **QuestionnairesErReportController** klasę ir yra naudojamas nurodyti vartotojo teises pasirinkti ir vykdyti ER formatą. **Žymės** ypatybėse, šis meniu elementas rodo **\@QuestionnairesReport** žymę, kurią sukūrėte anksčiau, todėl teisingas tekstas yra rodomas UI programoje.

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a>Įtraukite meniu elementą į meniu

Įtraukite esantį **KM** meniu elementą į savo „Visual Studio“ projektą. Įtraukite naują **QuestionnairesErReport** elementą **Išorės** tipe šiame meniu. Šis elementas turi rodyti **QuestionnairesErReport** meniu elementą, kuris yra aprašytas ankstesniame skyriuje.

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a>Sukurkite „Visual Studio“ projektą

Sukurkite savo projektą tam, kad padarytumėte naują meniu elementą prieinamą vartotojams.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a>Vykdykite formatą iš programos

1. Eikite į **Klausimynas** \> **Projektavimas** \> **Klausimynų ataskaita (vykdoma ER)**.

    ![Pasirinkite klausimyno ataskaitą (vykdoma ER) meniu elementą klausimyno modulyje tam, kad vykdytumėte konfigūruotą ER formatą](./media/er-quick-start1-application-menu-modified.png)

2. Iškrentančiame teksto laukelyje, **Formato žemėlapis** laukelyje, pasirinkite **Klausimynų ataskaita**.
3. Pasirinkite **Gerai**.
4. **Elektroninės ataskaitos parametrai** teksto laukelyje, **Apimami įrašai** „FastTab“, konfigūruokite filtravimo parinktis taip, kad tik **SBCCrsExam** klausimynas būtų įtrauktas.
5. Pasirinkite **Gerai** filtravimo parinkties patvirtinimui.
6. Pasirinkite **Gerai** ataskaitos vykdymui.

    ![Atrankos kriterijų nurodymas elektroninės ataskaitos teksto laukelyje](./media/er-quick-start1-report-run-dialog-page.png)

7. Peržiūrėkite sukurtą ataskaitą.

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a>Suderinkite suprojektuotą ER sprendimą

Galite keisti konfigūruotą ER sprendimą taip, kad jis naudotų duomenis pateiktus klasėje, kuriuos sukūrėte prieigai prie ER formato vykdymo išsamios informacijos ir taip, kad jis įvestų šio ER formato pavadinimą sukurtoje ataskaitoje.

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a>Keiskite modelio žemėlapį

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a>Įtraukite duomenų šaltinį prieigai prie duomenų sutarties objekto

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūravimai** puslapyje, konfigūravimo medyje, išplėskite **Klausimyno modelį** ir tuomet pasirinkite **Klausimyno žemėlapis**.
3. Pasirinkit **Kūrimo įrankį** tam, kad atvertumėte **Modelis į duomenų šaltinio žemėlapio** puslapį.
4. Pasirinkite **Kūrimo įrankį** tam, kad atvertumėte žemėlapį modelio žemėlapio kūrimo įrankyje.
5. **Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų šaltinio tipai** juostoje, pasirinkite **Dynamics 365 for Operations\\Objektas**.
6. **Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.
7. Teksto laukelyje, **Pavadinimas** laukelyje įveskite **[RunTimeParameters](#DataContractDSName)**, kaip nurodytą šaltinio **QuestionnairesErReportService** klasės kodą.
8. **Klasės** laukelyje įveskite **[QuestionnairesErReportContract](#DataContractClass)**, kuris buvo užkoduotas anksčiau.
9. Pasirinkite **Gerai**.
10. Išplėskite **VykdymoLaikoParametrus**.

Įtrauktas duomenų šaltinis pateikia informaciją apie vykdomo ER formato žemėlapio įrašo ID.

![Įtrauktas duomenų šaltinis ER modelio žemėlapio kūrimo įrankyje](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a>Įtraukite duomenų šaltinį prieigai prie ER formato žemėlapio įrašų

Tęskite pasirinkto modelio žemėlapio redagavimą įtraukdami duomenų šaltinį prieigai prie ER formato žemėlapio įrašų.

1. **Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų šaltinio tipai** juostoje, pasirinkite **Dynamics 365 for Operations\\Lentelės įrašai**.
2. **Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.
3. Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **ER1**.
4. **Lentelė** laukelyje, įveskite **ERFormatMappingTable**.
5. Pasirinkite **Gerai**.

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a>Įtraukti duomenų šaltinį prieigai prie formato žemėlapio ER formato įrašo vykdymo

Tęskite pasirinkto modelio žemėlapio redagavimą įtraukdami duomenų šaltinį prieigai prie formato žemėlapio ER formato vykdymo įrašo.

1. **Modelio žemėlapio kūrimo įrankio** puslapyje, **Duomenų šaltinio tipai** juostoje pasirinkite **Funkcijos\\Apskaičiuotas laukelis**.
2. **Duomenų šaltiniai** juostoje pasirinkite **Įtraukti šaknį**.
3. Iškrentančiame teksto laukelyje, **Pavadinimas** laukelyje, įveskite **ER2**.
4. Pasirinkite **Redaguoti formulę**.
5. Formulės redaktoriuje **Formulės** laukelyje įveskite **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.
6. Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.
7. Pasirinkite **Gerai**.

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a>Įveskite vykdomo ER formato pavadinimą duomenų modelyje

Tęskite pasirinkto modelio žemėlapio redagavimą taip, kad ER formato vykdymo pavadinimas būtų įvestas į duomenų modelį.

1. **Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų modelis** juostoje išplėskite **ExecutionContext** ir tuomet pasirinkite **ExecutionContext\\FormatName**.
2. **Duomenų modelis** juostoje pasirinkite **Redaguoti** tam, kad konfigūruotumėte duomenų susiejimą pasirinkto duomenų modelio laukeliui.
3. Formulės redaktoriuje **Formulės** laukelyje įveskite **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.
4. Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.

Kadangi naudojote **FormatName** laukelį, konfigūruotas modelio žemėlapis dabar rodo ER formato pavadinimą, kuri iškviečia modelio žemėlapį vykdymo metu.

![Duomenų modelio laukelio susiejimas su įtrauktu duomenų šaltinio metodu ER modelio žemėlapio kūrimo įrankyje](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a>Užbaikite modelio žemėlapio dizainą

1. **Modelio žemėlapio kūrimo įrankis** puslapyje, pasirinkite **Įrašyti**.
2. Uždarykite puslapį.
3. Uždarykite modelio žemėlapio puslapį.
4. **Konfigūravimai** puslapyje, konfigūravimo medyje, įsitikinkite, kad **Klausimyno žemėlapio** konfigūravimas vis dar pasirinktas. Tuomet, **Versijos** „FastTab“, pasirinkite konfigūravimo versiją, kuri turi statusą **Juodraštis**.
5. Pasirinkite **Keisti statusą** \> **Užbaigtas**.

Šios konfigūracijos versijos 1.2 statusas yra keičiamas iš **Juodraštis** į **Užbaigtas**. Versija 1.2 nebegali būti keičiama. Šioje versijoje yra konfigūruotų žemėlapio modelis ir gali būti naudojamas pagal kitas ER konfigūracijas. Šios konfigūracijos versija 1.3 yra sukurta ir turi **Juodraštis** statusą. Galite redaguoti šią versiją tam, kad keistumėte **Klausimyno** žemėlapio modelį.

### <a name="modify-a-format"></a><a name="ModifyFormat"></a>Keisti formatą

Galite keisti konfigūruotą ER formatą taip, kad jo pavadinimas būtų rodomas ataskaitos poraštėje, kuri yra sukurta vykdant ER formatą.

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a>Įkelkite naują formato elementą

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūravimai** puslapyje, konfigūravimo medyje, išplėskite **Klausimyno modelį** ir tuomet pasirinkite **Klausimyno ataskaitą**.
3. Pasirinkite **Dizaino įrankis**.
4. **Formato kūrimo įrankio** puslapyje, formato medyje pasirinkite **„Ataskaita“** šaknies elementą.
5. Pasirinkite **Įtraukti** tam, kad įtrauktumėte lizdo formato elementą pasirinktam **Ataskaitos** šaknies elementui.
6. Pasirinkite **Excel\\Poraštė**.
7. **Pavadinimas** laukelyje, įveskite **Poraštė**.
8. Pasirinkite **Šaknis\Poraštė** ir tuomet pasirinkite **Įtraukti**.
9. Pasirinkite **Tekstas\\Eilutė**.

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a>Susiekite įkeltą formato elementą

1. **Formato kūrimo** puslapyje,**Žemėlapio** skirtuke, formato medyje, įjungtame **Poraštės\\Eilutės** elemente, pasirinkite **Redaguoti formulę**.
2. Formulės redaktoriaus laukelyje **Formulė** įveskite **CONCATENATE ("\&C\&10", FORMAT("Sukurta'\%1' ER sprendimas", model.ExecutionContext.FormatName))**.
3. Pasirinkite **Įrašyti** ir uždarykite formulės redaktorių.
4. Pasirinkite **Įrašyti**.

Konfigūruotas formatas dabar buvo pakeistas taip, kad jo pavadinimas bus įvestas sukurtos ataskaitos poraštėje naudojant **Poraštės\\Eilutės** elementą.

![Poraštės formato elemento įtraukimas į konfigūruotą formatą ER veiksmo kūrimo įrankyje](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a>Užbaikite formato projektavimą

1. Uždarykite puslapį **Formato dizaino įrankis**.
2. **Konfigūravimai** puslapyje, konfigūravimo medyje, įsitikinkite, kad **Klausimyno ataskaita** konfigūravimas vis dar pasirinktas. Tuomet, **Versijos** „FastTab“, pasirinkite konfigūravimo versiją, kuri turi statusą **Juodraštis**.
3. Pasirinkite **Keisti statusą** \> **Užbaigtas**.

Šios konfigūracijos versijos 1.2 statusas yra keičiamas iš **Juodraštis** į **Užbaigtas**. Versija 1.2 nebegali būti keičiama. Šioje versijoje yra konfigūruotų formatas ir gali būti naudojamas pagal kitas ER konfigūracijas. Šios konfigūracijos versija 1.3 yra sukurta ir turi **Juodraštis** statusą. Galite redaguoti šią versiją tam, kad keistumėte **Klausimyno** ataskaitą.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a>Vykdykite formatą iš programos

1. Eikite į **Klausimynas** \> **Projektavimas** \> **Klausimynų ataskaita (vykdoma ER)**.
2. Iškrentančiame teksto laukelyje, **Formato žemėlapis** laukelyje, pasirinkite **Klausimynų ataskaita**.
3. Pasirinkite **Gerai**.
4. **ER parametrai** teksto laukelyje, **Apimami įrašai** „FastTab“, konfigūruokite filtravimo parinktis taip, kad tik **SBCCrsExam** klausimynas būtų įtrauktas.
5. Pasirinkite **Gerai** filtravimo parinkties patvirtinimui.
6. Pasirinkite **Gerai** ataskaitos vykdymui.
7. Peržiūrėkite sukurtą ataskaitą „Excel“ formatu.

Atkreipkite dėmesį, kad sukurtos ataskaitos poraštė turi ER formato pavadinimą, kuris yra naudojamas jos sukūrimui.

![Sukurta ataskaita „Excel“ formatu](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a>Vykdykite formatą iš ER

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. **Konfigūravimai** puslapyje, konfigūravimo medyje, išplėskite **Klausimyno modelį** ir tuomet pasirinkite **Klausimyno ataskaitą**.
3. Veiksmų srityje pasirinkite **Vykdyti**.
4. **Elektroninės ataskaitos parametrai** teksto laukelyje, **Apimami įrašai** „FastTab“, konfigūruokite filtravimo parinktis taip, kad tik **SBCCrsExam** klausimynas būtų įtrauktas.
5. Pasirinkite **Gerai** filtravimo parinkties patvirtinimui.
6. Pasirinkite **Gerai** ataskaitos vykdymui.
7. Peržiūrėkite sukurtą ataskaitą „Excel“ formatu.

Atkreipkite dėmesį, kad sukurtos ataskaitos poraštė neturi ER formato pavadinimo, kuris buvo naudotas sukūrimui, nes duomenų sutarties objektas nebuvo perduotas vykdymo modelio žemėlapiui, kai jis buvo iškviestas ER formato vykdomo iš ER.

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a>Konfigūruokite formato paskirtį ekrane rodomoje peržiūroje

1. Eikite **Organizacijos administravimas** \> **Elektroninė ataskaita** \> **Elektroninės ataskaitos paskirtis**.
2. **Elektroninės ataskaitos paskirties** puslapyje įtraukite įrašo paskirtį konfigūruotą **Klausimyno ataskaitos** ER formatą.
3. **Failo paskirties** „FastTab“, nustatykite **Ekrano** [paskirtį](er-destination-type-screen.md) **Ataskaitos** formato komponentui, kuris buvo [įtrauktas](#AddFormatRootElement) kaip šaknies elementas konfigūruoto **Klausimyno ataskaitos** ER formato.
4. **PDF pakeitimo nustatymų** „FastTab“, konfigūruokite paskirties vietą pavertimui į ataskaitą [PDF formatu](electronic-reporting-destinations.md#OutputConversionToPDF), kuris naudoja **Kraštovaizdžio** puslapio orientaciją.

![Tinkinto ekrano paskirties vietos konfigūravimas ER formatui elektroninės ataskaitos paskirties puslapyje](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a>Vykdykite formatą iš programos tam, kad peržiūrėtumėte jį kaip PDF dokumentą

1. Eikite į **Klausimynas** \> **Projektavimas** \> **Klausimynų ataskaita (vykdoma ER)**.
2. Iškrentančiame teksto laukelyje, **Formato žemėlapis** laukelyje, pasirinkite **Klausimynų ataskaita**.
3. Pasirinkite **Gerai**.
4. **Elektroninės ataskaitos parametrai** teksto laukelyje, **Apimami įrašai** „FastTab“, konfigūruokite filtravimo parinktis taip, kad tik **SBCCrsExam** klausimynas būtų įtrauktas.
5. Pasirinkite **Gerai** filtravimo parinkties patvirtinimui.

    **Paskirties vietos** „FastTab“, atkreipkite dėmesį, kad **Išorės** laukelis yra nustatytas į **Ekranas**. Jei norite keisti konfigūruotą paskirties vietą, pasirinkite **Keisti**.

    ![ER ataskaitos vykdymo laiko teksto laukelis, kuriame galite keisti konfigūruotą paskirties vietą](./media/er-quick-start1-run-settings.png)

6. Pasirinkite **Gerai** ataskaitos vykdymui.
7. Peržiūrėkite sukurtą ataskaitą PDF formatu.

    ![Ekrane rodoma sukurtos ataskaitos PDF formatu peržiūra](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a>Papildomi ištekliai

- [Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų formulių kalba](er-formula-language.md)
- [Ataskaitų keliomis kalbomis kūrimas](er-design-multilingual-reports.md)
- [ER sistemos API](er-apis-app73.md)
- [CASE funkcija](er-functions-logical-case.md)
- [CONCATENATE funkcija](er-functions-text-concatenate.md)
- [DATETIMEFORMAT funkcija](er-functions-datetime-datetimeformat.md)
- [FILTER funkcija](er-functions-list-filter.md)
- [FIRSTORNULL funkcija](er-functions-list-firstornull.md)
- [FORMAT funkcija](er-functions-text-format.md)
- [IF funkcija](er-functions-logical-if.md)
- [ORDERBY funkcija](er-functions-list-orderby.md)
- [SESSIONNOW funkcija](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]