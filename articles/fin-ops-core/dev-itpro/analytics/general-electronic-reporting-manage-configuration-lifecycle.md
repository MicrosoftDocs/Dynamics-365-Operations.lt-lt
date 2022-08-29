---
title: Elektroninių ataskaitų (ER) konfigūracijų ciklo valdymas
description: Šiame straipsnyje aprašoma, kaip valdyti "Dynamics 365 Finance" elektroninių ataskaitų (ER) konfigūracijų ciklą.
author: kfend
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 0209679c9882d87edab68d043fba9e7b3400a2a2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337266"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Elektroninių ataskaitų (ER) konfigūracijų ciklo valdymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip valdyti "[Dynamics](general-electronic-reporting.md) 365 Finance" elektroninių ataskaitų (ER) [konfigūracijų](general-electronic-reporting.md#Configuration) ciklą.

## <a name="overview"></a>Apžvalga

Elektroninės ataskaitos (ER) yra mechanizmas, palaikantis įstatymiškai privalomus ir šaliai būdingus elektroninius dokumentus. Apskritai, ER suteikia galimybę atlikti tolesnes su vienu elektroniniu dokumentu susijusias užduotis. Išsamią informaciją žr. [Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md).

- Sukurti elektroninio dokumento šabloną.

    - Identifikuoti toliau nurodytus reikiamus duomenų šaltinius, kuriuos galima pateikti dokumente.

        - Pagrindiniai duomenys, pvz., duomenų lentelės, duomenų objektai ir klasės.
        - Konkretaus proceso ypatybės, pvz., vykdymo data ir laikas bei laiko juosta.
        - Vartotojo įvesties parametrai, kuriuos vykdymo metu nurodė galutinis vartotojas.

    - Apibrėžti reikiamus dokumento elementus ir jų topologiją siekiant nurodyti galutinį dokumento formatą.
    - Konfigūruoti norimą duomenų srautą iš pasirinktų duomenų šaltinių į nustatytus dokumento elementus (naudojant duomenų šaltinių susiejimus su dokumento formato komponentais) ir nurodyti proceso kontrolės logiką.

- Sukurkite šabloną, kurį būtų galima naudoti kituose egzemplioriuose.

    - Sukurtą dokumento šabloną transformuokite į ER konfigūraciją ir eksportuokite iš dabartinio programos egzemplioriaus kaip XML paketą, kurį būtų galima išsaugoti vietoje arba „Lifecycle Services” (LCS).
    - Transformuokite ER konfigūraciją programos dokumento šabloną.
    - Importuokite XML paketą, saugomą vietoje arba LCS, į dabartinį egzempliorių.

- Tinkinti elektroninio dokumento šabloną.

    - Šabloną iš LCS perduokite į dabartinį egzempliorių kaip ER konfigūraciją.
    - Kurti pasirinktinę ER konfigūracijos versiją ir išsaugoti nuorodą į pagrindinę versiją.

- Šabloną integruokite su konkrečiu verslo procesu, kad jį būtų galima naudoti programoje.

    - Konfigūruokite parametrus, kad programa pradėtų naudoti ER konfigūraciją, ją nurodant su procesu susijusiu parametru. Pvz., į ER konfigūraciją nurodyti konkrečiu mokėtinų sumų mokėjimo metodu, kad būtų generuojamas elektroninio mokėjimo pranešimas apie SF apdorojimą.

- Šabloną naudoti konkrečiame verslo procese.

    - ER konfigūraciją paleisti konkrečiame verslo procese. Pvz., siekiant generuoti SF apdorojimo elektroninio mokėjimo pranešimą, kai pasirenkamas mokėjimo metodas, nurodantis į ER konfigūraciją.

## <a name="concepts"></a>Koncepcijos
Su ER konfigūracijos ciklu susieti tolesni vaidmenys ir susijusios veiklos.

| Vaidmuo                                       | Veikla                                                      | aprašymas |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Elektroninės ataskaitos funkcijų konsultantas | Kurti ir valdyti ER komponentus (modelius ir formatus).           | Verslininkas, kuriantis konkrečių ER domenų duomenų modelius, kuria reikiamus elektroninių dokumentų šablonus ir atitinkamai juos susieja. |
| Elektroninės ataskaitos kūrėjas             | Kurti ir valdyti duomenų modelių susiejimus.                          | Specialistas, kuris parenka reikiamus „Finance‟ duomenų šaltinius ir juos susieja su konkrečių ER domenų duomenų modeliais. |
| Apskaitos prižiūrėtojas                      | Konfigūruoti su procesu susijusius parametrus, nurodančius į ER artefaktus. | Pavyzdžiui, **Apskaitos prižiūrėtojo** vaidmuo, leidžiantis ER konfigūracijos parametrus naudoti su konkrečiu mokėtinų sumų mokėjimo metodu, kad būtų galima generuoti elektroninio mokėjimo pranešimą apie SF apdorojimą. |
| Mokėtinų sumų mokėjimo klerkas            | ER artefaktus naudoti konkrečiame verslo procese.                | Pvz., **Mokėtinų sumų mokėjimo klerko** vaidmuo, leidžiantis pagal sukonfigūruotą konkretaus mokėjimo metodo ER formatą generuoti elektroninio mokėjimo pranešimus apie SF apdorojimą. |

## <a name="er-configuration-development-lifecycle"></a>ER konfigūracijos plėtros ciklas
Dėl šių su ER susijusių priežasčių rekomenduojame programavimo aplinkoje sukurti ER konfigūracijas kaip atskirą finansų ir operacijų egzempliorių:

- Vartotojai, kurių vaidmuo yra **Elektroninių ataskaitų kūrėjas** arba **Elektroninių ataskaitų funkcijų konsultantas**, gali konfigūracijas redaguoti ir vykdyti bandymams. Tokiu atveju gali būti iškviesti klasių ir lentelių, kurios gali būti potencialiai kenksmingos verslo duomenims ir egzemplioriaus naudojimo efektyvumui, metodai.
- Įvesties vietos neapriboja klasių ir lentelių kaip ER konfigūracijų ER duomenų šaltinių metodų iškvietimų ir jie yra užregistruoti įmonės turinyje. Todėl slaptus verslo duomenis gali pasiekti vartotojai, kurių vaidmuo yra **Elektroninių ataskaitų kūrėjas** arba **Elektroninių ataskaitų funkcijų konsultantas**.

Programavimo aplinkoje sukurtas ER konfigūracijas galima [įkelti](#data-persistence-consideration) į testavimo aplinką įvertinti konfigūracijai (tinkamam proceso integravimui, rezultatų tikslumui ir našumui) ir užtikrinti kokybei, pavyzdžiui, vaidmenų valdomų prieigos teisių tinkamumui ir pareigų atskyrimui. Šiuo tikslu galima naudoti funkcijas, leidžiančias mainytis ER konfigūracijomis. Patvirtintas ER konfigūracijas galima įkelti į LCS, kad jas būtų galima bendrinti su paslaugų prenumeratoriais arba [importuoti](#data-persistence-consideration) į gamybos aplinką vidiniam naudojimui.

![ER konfigūracijos ciklas.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Duomenų pastovumo svarstymas

Į savo finansų [egzempliorių](tasks/er-import-configuration-lifecycle-services.md) galite atskirai importuoti skirtingas [ER](general-electronic-reporting.md#Configuration) konfigūracijos versijas. Importavus naująją ER konfigūracijos versiją, sistema valdo šios konfigūracijos juodraščio versijos turinį:

- Kai importuota versija yra žemesnė nei didžiausia šios konfigūracijos versija dabartiniame „Finance” egzemplioriuje, šios konfigūracijos juodraščio versijos turinys nekinta.
- Kai importuota versija yra aukštesnė nei bet kuri kita šios konfigūracijos versija dabartiniame „Finance” egzemplioriuje, importuotos versijos turinys yra nukopijuojamas į šios konfigūracijos juodraščio versiją, kad būtų galima toliau redaguoti paskutinę baigtą versiją.

Jei šios konfigūracijos savininkas yra šiuo metu suaktyvintas konfigūracijos [teikėjas](general-electronic-reporting.md#Provider), šios konfigūracijos juodraščio versija matoma jums „FastTab” skirtuke **Versijos**, puslapyje **Konfigūracijos** (**Organizacijos administravimas** > **Elektroninės ataskaitos** > **Konfigūracijos**). Galite pasirinkti konfigūracijos juodraščio versiją ir [modifikuoti](er-quick-start2-customize-report.md#ConfigureDerivedFormat) jos turinį naudodami atitinkamą ER dizaino įrankį. Redagavus ER konfigūracijos juodraščio versiją, jos turinys nebeatitinka didžiausios šios konfigūracijos versijos dabartiniame „Finance” egzemplioriuje turinio. Norint išvengti jūsų pakeitimų praradimo, sistema rodo klaidą, kad nepavyko tęsti importavimo, nes šios konfigūracijos versija yra aukštesnė nei didžiausia šios konfigūracijos versija dabartiniame „Finance” egzemplioriuje. Kai tai įvyksta, pavyzdžiui, naudojant formato konfigūraciją **„X”**, rodomas klaidos pranešimas **„X” formato versija nėra baigta**.

Norėdami anuliuoti juodraščio versijoje įvestus pakeitimus, pasirinkite didžiausią baigtą arba bendrai naudojamą jūsų „Finance” ER konfigūracijos versiją „FastTab” skirtuke **Versijos** ir tada pasirinkite **Gauti šią versiją** parinktį. Pasirinktos versijos turinys yra nukopijuojamas į juodraščio versiją.

## <a name="applicability-consideration"></a>Taikomumo svarstymas

Kurdami naują ER konfigūracijos versiją, galite nustatyti jos priklausomybę nuo [kitų](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) programinės įrangos komponentų. Šis veiksmas yra laikomas išankstine sąlyga, norint kontroliuoti šios konfigūracijos versijos atsisiuntimą iš ER saugyklos ar išorės XML failą ir toliau naudoti šią versiją. Bandant importuoti naują ER konfigūracijos versiją, sistema naudoja sukonfigūruotas būtinuosius komponentus, kad galėtų kontroliuoti, ar galima importuoti versiją.

Kai kuriais atvejais gali reikėti, kad sistema nepaisytų sukonfigūruotų būtinųjų komponentų importuojant naujas ER konfigūracijų versijas. Jei norite, kad importuojant sistema nepaisytų būtinųjų komponentų, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. Nustatykite parinktį **Praleisti produkto naujinimus ir tikrinti versijos būtinuosius komponentus** importavimo metu kaip **Taip**.

    > [!NOTE]
    > Šis parametras yra susijęs su konkrečiu vartotoju ir įmone.

## <a name="dependencies-on-other-components"></a>Priklausomybės nuo kitų komponentų

ER konfigūracijas galima konfigūruoti kaip priklausomas [nuo](er-download-configurations-global-repo.md#import-filtered-configurations) kitų konfigūracijų. Pavyzdžiui, [galite importuoti ER duomenų modelio konfigūraciją iš visuotinės saugyklos į savo "Microsoft" reguliavimo konfigūracijos tarnybas (RCS)](er-download-configurations-global-repo.md) arba "Dynamics 365" finansų egzempliorių, o tada sukurti naują [ER](er-overview-components.md#data-model-component)[formato](../../../finance/localizations/rcs-overview.md) [...](er-overview-components.md#format-component)[konfigūraciją, išvestą iš importuoto ER duomenų modelio konfigūracijos.](er-quick-start2-customize-report.md#DeriveProvidedFormat) Išvestinė ER formato konfigūracija bus priklausoma nuo pagrindinės ER duomenų modelio konfigūracijos.

![Išvestinė ER formato konfigūracija konfigūracijos puslapyje.](./media/ger-configuration-lifecycle-img1.png)

Baigę kurti formatą, galite pakeisti pradinės ER **formato konfigūracijos versijos būseną iš Juodraštis į** **Baigta**. Tada galėsite bendrai naudoti ER formato konfigūracijos užbaigtą versiją [publikuodami](../../../finance/localizations/rcs-global-repo-upload.md) ją visuotiniame saugykloje. Po to galite prieiti prie visuotinės saugyklos iš bet kurios RCS ar finansų debesies egzemplioriaus. Tada galite importuoti bet kurią ER konfigūracijos versiją, taikomą programai, iš visuotinės saugyklos į tą programą.

![Publikuota ER formato konfigūracija konfigūracijos saugyklos puslapyje.](./media/ger-configuration-lifecycle-img2.png)

Atsižvelgiant į konfigūracijos priklausomybę, kai ER formato konfigūraciją pasirenkate visuotinyje saugykloje, kad ją importuotų į naujai įdiegtą RCS arba finansų egzempliorių, pagrindinė ER duomenų modelio konfigūracija automatiškai randama visuotinėje saugykloje ir importuojama kartu su pasirinkta ER formato konfigūracija kaip pagrindinė konfigūracija.

Taip pat galite eksportuoti savo ER formato konfigūracijos versiją iš dabartinės RCS ar finansų egzemplioriaus ir saugoti ją vietoje kaip XML failą.

![Konfigūracijos puslapyje eksportuojama ER formato konfigūracijos versija kaip XML.](./media/ger-configuration-lifecycle-img3.png)

**Finansų** versijose prieš 10.0.29 versiją, bandant importuoti ER formato konfigūracijos versiją iš to XML failo arba iš bet kurios kitos, ne visuotinės saugyklos, saugyklos į naujai įdiegtą RCS arba finansų egzempliorių, kuriame dar nėra ER konfigūracijų, bus pateikta ši išimtis, siekiant informuoti, kad nepavyksta gauti pagrindinės konfigūracijos:

> Liko neišspręstų nuorodų<br>
Negalima nustatyti objekto '\<imported configuration name\>' nuorodos į objektą 'Base' (\<globally unique identifier of the missed base configuration\>,\<version of the missed base configuration\>)

![Importuojama ER formato konfigūracijos versija konfigūracijos saugyklos puslapyje.](./media/ger-configuration-lifecycle-img4.gif)

**Versijoje 10.0.29** ir vėliau bandant importuoti tą pačią konfigūraciją nepavyko rasti pagrindinės konfigūracijos dabartiniame programos egzemplioriuje arba šaltinio saugykloje, kurią naudojate (jei taikoma), ER sistema automatiškai bandys rasti trūkstamos pagrindinės konfigūracijos pavadinimą visuotinės saugyklos talpykloje. Tada bus pateikiamas trūkstamos pagrindinės konfigūracijos pavadinimas ir visuotinai unikalus identifikatorius (GUID) leidžiamos išimties tekste.

> Liko neišspręstų nuorodų<br>
Negalima nustatyti objekto '\<imported configuration name\>' nuorodos į objektą 'Base' (\<name of the missed base configuration\>\<globally unique identifier of the missed base configuration\>;\<version of the missed base configuration\>)

![Konfigūracijos saugyklos puslapio išimtis, kai nepavyko rasti pagrindinės konfigūracijos.](./media/ger-configuration-lifecycle-img5.png)

Norėdami surasti pagrindinę konfigūraciją ir rankiniu būdu ją importuoti, galite naudoti pateiktą pavadinimą.

> [!NOTE]
> Ši [nauja](er-download-configurations-global-repo.md#open-configurations-repository)[pasirinktis](er-extended-format-lookup.md) veikia tik tada, kai bent vienas vartotojas jau užsiregistravo visuotinyje saugykloje naudodamas konfigūracijos saugyklos puslapį arba vieną iš dabartinio finansų egzemplioriaus visuotinio saugyklos peržvalgos laukų ir kai visuotinės saugyklos turinys yra talpykloje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)

[ER konfigūracijų priklausomybės nuo kitų komponentų apibrėžimas](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

