---
title: Sf fiksavimo sprendimo konfigūravimas
description: Šiame straipsnyje paaiškinama, kaip konfigūruoti SF fiksavimo sprendimą.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: e297dafc930368f14f2e68213ce4153ba792ef4d
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690999"
---
# <a name="configure-the-invoice-capture-solution"></a>Sf fiksavimo sprendimo konfigūravimas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Įdiegę SF fiksavimo sprendimą, turite sukonfigūruoti aplinką. Procesą sudaro šie pagrindiniai veiksmai.

1. **Būtina:** sinchronizuokite juridinius subjektus iš " Microsoft Dynamics 365 Finance". Šis veiksmas naudojamas organizacijos struktūrai nustatyti Microsoft Power Platform.
2. **Būtina:** sukonfigūruokite SF vaizdų importavimo kanalus. Sprendimas palaiko šiuos kanalus:

    - Office 365 Outlook (numatytoji)
    - Outlook.com
    - „OneDrive“
    - „SharePoint“

3. **Nebūtina: nurodykite** papildomas konfigūracijos grupes optiškai ženklų atpažinimo (OCR) tarnybai.
4. **Pasirinktinai:** apibrėžkite juridinio subjekto, tiekėjo sąskaitos, prekės ir įsigijimo tipo susiejimo taisykles.

Šis straipsnis daugiausia naudojamas dviem reikalingais proceso veiksmais. Norėdami gauti daugiau informacijos apie konfigūracijos grupes, žr. [SF fiksavimo sprendimo konfigūracijos grupes](invoice-capture-config-group.md). Norėdami gauti daugiau informacijos apie susiejimo taisykles, žr. [SF fiksavimo sprendimo susiejimo taisykles](invoice-capture-mapping-rules.md).

## <a name="manage-legal-entities"></a>Tvarkyti juridinius subjektus

Finansai apibrėžia juridinius subjektus kaip organizacijas, identifikuojamas registruojant su juridiniais subjektais. Verslo veikla atliekama ir įrašoma atskiruose juridiniuose subjektuose. Verslo Microsoft Power Platform vienetai, saugos vaidmenys ir vartotojai susiejami kartu tam, kad atitiktų vaidmenimis pagrįstą saugos modelį.

Verslo vienetai naudojami kartu su saugos vaidmenimis prieigos prie duomenų kontrolei atlikti. Vartotojai mato tik tą informaciją, kurios jiems reikia, kad galėtų atlikti savo užduotis. SF fiksavimo sprendimas suteikia konfigūracijos vietą, kur galite įkelti pagrindinę informaciją iš esamų finansų juridinių subjektų ir valdyti neautomatiniu būdu sukurtus subjektus. Juridiniai subjektai naudojami tiekėjo SF ir saugos kontrolėje.

Kai juridinis subjektas sukuriamas ir rodomas sąrašo rodinyje, automatiškai sukuriamas numatytasis verslo vienetas, pavadintas tokiu pačiu pavadinimu. Komandai suteikiamas **AP klerko saugos** vaidmuo. Kai importuojami juridiniai subjektai, importuojami pagrindiniai pagrindiniai duomenys iš finansų. Nefiksuotas prekes identifikuos juridinis subjektas ir įtrauks jas į SF fiksavimo sprendimą. Numatytoji konfigūracijos grupė priskiriama naujiems juridiniams subjektams.

### <a name="sync-legal-entities"></a>Sinchronizuoti juridinius subjektus

Negalima tiesiogiai kurti juridinių subjektų. Tačiau galite sinchronizuoti juridinius subjektus iš "Finance". Norėdami sinchronizuoti juridinius subjektus, atlikite šiuos veiksmus.

1. Eikite į **Nustatymo \> sistemos nustatymą Valdyti \> juridinius subjektus**.
2. Patvirtinimo **dialogo lange pasirinkite** Sinchronizuoti juridinius **subjektus**, tada pasirinkite Gerai.

Baigus sinchronizuoti, rodomas naujų juridinių subjektų skaičius. Nauji juridiniai subjektai rodomi sąrašo rodinyje. Numatytoji konfigūracijos grupė priskiriama naujiems juridiniams subjektams.

## <a name="configure-invoice-import-channels"></a>SF importavimo kanalų konfigūravimas

Tiekėjai SF siunčia iš skirtingų kanalų (el. pašto, failo darbo srities arba SF portalo) įvairiais formatais (popieriuje arba paveikslėlyje). SF fiksavimo sprendimas gali tvarkyti skirtingus kanalus ir formatus. Palaikomi šie tipai:

- Office 365 Outlook
- Outlook.com
- „SharePoint“
- „OneDrive“

Kai kanalu sukuriamas tam tikros sąskaitos kanalas, automatiškai sukuriamas srautas, kuriame yra iš anksto nustatytas šablonas, skirtas gaunamiems el. laiškams arba failams, esantys gautame arba tarpe, stebėti. Bet kuris failas, turintis tinkamą SF, gali būti atpažintas ir išsiųstas į SF sritį, kad laukia, kol jį apdoros mokėtinų sumų (AP) klerkas. Priedas turėtų būti PDF arba vaizdo formatu. SF gali būti įkeliamos į SF fiksavimo sprendimą, atsižvelgiant į kanalo konfigūraciją.

### <a name="create-a-channel"></a>Kanalo kūrimas

Jei importavote papildomą sprendimų paketą ("Dynamics 365" SF fiksavimas – diegimo įrankiai), numatytasis "Outlook" Office 365 ryšys yra parengtas naudoti. Jei norite sukurti daugiau ryšių su skirtingais el. pašto abonementais arba kitais kanalų tipais, žr. [Sukurkite papildomų kanalų ryšių](invoice-capture-advanced-settings.md#create-additional-connections-for-channels).

Norėdami sukurti kanalą, atlikite šiuos veiksmus.

1. Eikite į **sąrankos \> sistemos nustatymo \> konfigūravimo kanalus**.
2. Pasirinkite **Nauja**.
3. Užpildykite toliau nurodytus laukus:

    - Kanalo pavadinimas
    - Aprašymas
    - Tipas
    - Ryšys

Į sprendimą galima importuoti tik el. laiškus arba failus, kurie atitinka nurodytus kriterijus.

| Tipas               | Konfigūracija  | Daugiau informacijos |
|--------------------|----------------|------------------|
| Office 365 Outlook | Aplankas         | El. pašto aplankas turi būti šakniniame kataloge. Pagal numatytuosius nustatymus naudojamas aplankas Gauta. Poaplankis nepalaikomas. |
|                    | Temos filtras | (Pasirinktinai) Antrinė dalis, kuri turėtų būti įtraukta į temą. |
|                    | Nuo           | (Pasirinktinai) Siuntėjo arba siuntėjo el. pašto adresas. Jei nurodote kelis adresus, naudokite kabliataškį (;) kaip skyriklis. |
| „SharePoint“         | Svetainės adresas   | Svetainės adreso URL. |
|                    | Aplankas         | Svetainės adrese yra aplankas. |

### <a name="activate-the-channel"></a>Suaktyvinti kanalą

Įrašius eigą, laukuose rodoma kanalo būsena ir laikas, kada jis buvo sukurtas. Iš pradžių laukas **Būsena** nustatomas į **Neaktyvus**. Būsenos **priežasties** laukas nurodo, kad kanalas buvo inicijuotas ir parengtas suaktyvinti.

Kanalui suaktyvinti pasirinkite **Aktyvinti**. Atnaujinami **laukai** **Būsenos ir** Būsenos priežastis.

Jei kanalas nebūtinas, galite jį išjungti. Jei norite išjungti kanalą, pasirinkite **Išjungti**. Atnaujinami **laukai** **Būsenos ir** Būsenos priežastis.

### <a name="manage-flows-in-flow-management"></a>Valdyti srauto valdymo srautus

Galite peržiūrėti kanalą konfigūravimo **kanalų puslapyje** arba srauto valdymo proceso metu.

Norėdami peržiūrėti daugiau informacijos, eikite į **administratoriaus sistemos numatytuosius \> sprendimų \> debesies srautus** ir pasirinkite tikslinį srautą. Informacija, kuri rodoma, apima susietus ryšius, savininkus ir paleisti jo istoriją.

Norėdami sinchronizuoti būseną pasirinkite Tikrinti **,** kad patvirtintumėte, jog kanalo būsena atitinka srauto būseną.

Kai kurie išimčių tvarkymo atvejai rodomi būsenos **priežasties** lauke:

- **Trūksta Dataverse ryšio** – dabartinis vartotojas nesukūrė bent vienos ryšio **Microsoft Dataverse** nuorodos.
- **Nerasta** – srautas, susietas su kanalu, panaikintas srauto valdymo proceso metu. Norint sukurti naują kanalą, kanalą reikia įrašyti iš naujo.
- **Išjungtas srauto** valdymo metu – srauto valdymas buvo išjungtas, o kanalo būsena skiriasi nuo srauto būsenos.
- **Aktyvinta srauto** valdymo metu – srautas buvo suaktyvintas srauto valdymo metu, o kanalo būsena skiriasi nuo srauto būsenos.
- **Įvyko netikėta klaida** – vartotojas turi patvirtinti, kad svetainė yra Ryšio svetainė ir kad aplankas yra Dokumentų biblioteka.
