---
title: Elektroninių ataskaitų (ER) konfigūracijų ciklo valdymas
description: Šioje temoje aprašoma, kaip valdyti „Dynamics 365 Finance“ Elektroninių ataskaitų (ER) konfigūracijų ciklą.
author: NickSelin
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb7844a009bc35f7151827b8e675cb39f71459fd
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345743"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Elektroninių ataskaitų (ER) konfigūracijų ciklo valdymas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip valdyti „Dynamics 365 Finance“ Elektroninių ataskaitų (ER) konfigūracijų ciklą.

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
Dėl tolesnių su ER susijusių priežasčių rekomenduojame ER konfigūracijas kurti programavimo aplinkoje kaip atskirame „Finance and Operations“ egzemplioriuje.

- Vartotojai, kurių vaidmuo yra **Elektroninių ataskaitų kūrėjas** arba **Elektroninių ataskaitų funkcijų konsultantas**, gali konfigūracijas redaguoti ir vykdyti bandymams. Tokiu atveju gali būti iškviesti klasių ir lentelių, kurios gali būti potencialiai kenksmingos verslo duomenims ir egzemplioriaus naudojimo efektyvumui, metodai.
- Įvesties vietos neapriboja klasių ir lentelių kaip ER konfigūracijų ER duomenų šaltinių metodų iškvietimų ir jie yra užregistruoti įmonės turinyje. Todėl slaptus verslo duomenis gali pasiekti vartotojai, kurių vaidmuo yra **Elektroninių ataskaitų kūrėjas** arba **Elektroninių ataskaitų funkcijų konsultantas**.

Programavimo aplinkoje sukurtas ER konfigūracijas galima [įkelti](#data-persistence-consideration) į testavimo aplinką įvertinti konfigūracijai (tinkamam proceso integravimui, rezultatų tikslumui ir našumui) ir užtikrinti kokybei, pavyzdžiui, vaidmenų valdomų prieigos teisių tinkamumui ir pareigų atskyrimui. Šiuo tikslu galima naudoti funkcijas, leidžiančias mainytis ER konfigūracijomis. Patvirtintas ER konfigūracijas galima įkelti į LCS, kad jas būtų galima bendrinti su paslaugų prenumeratoriais arba [importuoti](#data-persistence-consideration) į gamybos aplinką vidiniam naudojimui.

![ER konfigūracijos ciklas.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a><a name="data-persistence-consideration" />Duomenų pastovumo svarstymas

Galite individualiai [importuoti](tasks/er-import-configuration-lifecycle-services.md) skirtingas ER [konfigūracijų](general-electronic-reporting.md#Configuration) [versijas](general-electronic-reporting.md#component-versioning) į savo „Finance” egzempliorių. Importavus naująją ER konfigūracijos versiją, sistema valdo šios konfigūracijos juodraščio versijos turinį:

   - Kai importuota versija yra žemesnė nei didžiausia šios konfigūracijos versija dabartiniame „Finance” egzemplioriuje, šios konfigūracijos juodraščio versijos turinys nekinta.
   - Kai importuota versija yra aukštesnė nei bet kuri kita šios konfigūracijos versija dabartiniame „Finance” egzemplioriuje, importuotos versijos turinys yra nukopijuojamas į šios konfigūracijos juodraščio versiją, kad būtų galima toliau redaguoti paskutinę baigtą versiją.

Jei šios konfigūracijos savininkas yra šiuo metu suaktyvintas konfigūracijos [teikėjas](general-electronic-reporting.md#Provider), šios konfigūracijos juodraščio versija matoma jums „FastTab” skirtuke **Versijos**, puslapyje **Konfigūracijos** (**Organizacijos administravimas** > **Elektroninės ataskaitos** > **Konfigūracijos**). Galite pasirinkti konfigūracijos juodraščio versiją ir [modifikuoti](er-quick-start2-customize-report.md#ConfigureDerivedFormat) jos turinį naudodami atitinkamą ER dizaino įrankį. Redagavus ER konfigūracijos juodraščio versiją, jos turinys nebeatitinka didžiausios šios konfigūracijos versijos dabartiniame „Finance” egzemplioriuje turinio. Norint išvengti jūsų pakeitimų praradimo, sistema rodo klaidą, kad nepavyko tęsti importavimo, nes šios konfigūracijos versija yra aukštesnė nei didžiausia šios konfigūracijos versija dabartiniame „Finance” egzemplioriuje. Kai tai įvyksta, pavyzdžiui, naudojant formato konfigūraciją **„X”**, rodomas klaidos pranešimas **„X” formato versija nėra baigta**.

Norėdami anuliuoti juodraščio versijoje įvestus pakeitimus, pasirinkite didžiausią baigtą arba bendrai naudojamą jūsų „Finance” ER konfigūracijos versiją „FastTab” skirtuke **Versijos** ir tada pasirinkite **Gauti šią versiją** parinktį. Pasirinktos versijos turinys yra nukopijuojamas į juodraščio versiją.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
