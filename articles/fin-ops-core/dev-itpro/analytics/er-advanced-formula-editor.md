---
title: Elektroninių ataskaitų išplėstinė formulių rengyklė
description: Šiame straipsnyje aprašoma, kaip išplėstinės formulės rengyklę galima naudoti norint konfigūruoti išraiškas elektroninės ataskaitos (ER) modelių išdėstymo ir formato komponentams.
author: NickSelin
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f54ab248e38d87b0a9fb7a73143f56fa704a3f67
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869105"
---
# <a name="electronic-reporting-advanced-formula-editor"></a>Elektroninių ataskaitų išplėstinė formulių rengyklė

[!include [banner](../includes/banner.md)]

Be [elektroninių ataskaitų](general-electronic-reporting.md)[formulių rengyklės](general-electronic-reporting-formula-designer.md), galite naudoti išplėstinę elektroninių ataskaitų formulių rengyklę, kad pagerėtų elektroninių ataskaitų (ER) išraiškų konfigūravimo patirtis. Išplėstinė rengyklė veikia naršyklėje [„Monaco Editor“ pagrindu](https://microsoft.github.io/monaco-editor). Dažniausiai naudojamos išplėstinės rengyklės priemonės aprašytos šiame straipsnyje:

- [Automatinis kodo formatavimas](#Autoformatting)
- [„IntelliSense“](#IntelliSense)
- [Kodo užbaigimas](#CodeCompletion)
- [Kodo naršymas](#CodeNavigation)
- [Kodo susisteminimas](#CodeStructuring)
- [Surasti ir pakeisti](#FindAndReplace)
- [Duomenų įklijavimas](#DataPasting)
- [Sintaksės žymėjimas spalvomis](#SyntaxColorization)

## <a name=""></a><a name="ActivateAdvEditor">Išplėstinės formulių rengyklės aktyvinimas</a>

Norėdami pradėti naudoti išplėstinį formulės doroklį savo Microsoft Dynamics 365 finansų egzemplioriuje, atlikite šiuos veiksmus.

1.  Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2.  Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3.  Dialogo lange **Vartotojo parametrai**, skyriuje **Vykdymo sekimas** nustatykite parinkties **Įgalinti išplėstinę formulių rengyklę** parametrą **Taip**.

[![Paryškinti Vartotojo parametrų dialogo langas, Patobulintos formulių rengyklės parametro įgalinimas.](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> Atminkite, kad šis parametras yra susijęs su konkrečiu vartotoju ir įmone.

Pradėdami nuo Microsoft Dynamics 365 finansų versijos 10.0.19, pagal numatytuosius nustatymus galite kontroliuoti, koks ER formulės doroklis yra siūlomas. Atlikite šiuos veiksmus, norėdami įgalinti patobulintą formulių rengyklę visiems dabartinio „Finance” egzemplioriaus vartotojams ir įmonėms.

1.  Atidarykite parinkties **Funkcijos valdymas** darbo sritį.
2.  Raskite ir pasirinkite funkciją **Nustatyti ER patobulintą formulių rengyklę kaip numatytąją visiems vartotojams** sąraše, o tada pasirinkite **Įgalinti dabar**.
3.  Eikite į **Organizacijos administravimas** > **Elektroninės ataskaitos** > **Konfigūracijos**.
4.  Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
5.  Dialogo lange **Vartotojo parametrai** suraskite parametrą **Išjungti patobulintą formulių rengyklę** ir patikrinkite, ar jis nustatytas į **Ne**.

[![Paryškinti Vartotojo parametrų dialogo langas, Patobulintos formulių rengyklės parametro išjungimas.](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)

> [!NOTE]
> Parametrų **Įgalinti patobulintą formulių rengyklę** ir **Išjungti patobulintą formulių rengyklę** reikšmės yra atskiros kiekvienam vartotojui ir siūlomos **Vartotojo parametrų** dialogo lange, priklausomai nuo funkcijos **Nustatyti ER patobulintą formulių rengyklė kaip numatytąją visiems vartotojams** būsenos.

## <a name=""></a><a name="Autoformatting">Automatinis kodo formatavimas</a>

Rašant sudėtingą išraišką, kurią sudaro keletas kodo eilučių, naujai įvestos eilutės įtrauka bus automatiškai pagrįsta ankstesnės eilutės įtrauka. Galite pasirinkti eilutes ir pakeisti jų įtrauką, paspausdami **Tabuliavimo klavišas** arba **„Shift“ + tabuliavimo klavišas**.

[![ER formulių rengyklės gif, rodantis eilučių pasirinkimą ir įtraukos keitimą.](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

Automatinis formatavimas leidžia išsaugoti visos išraiškos tinkamą formatavimą, kad būtų lengviau atlikti priežiūrą ir būtų paprasčiau suprasti sukonfigūruotą logiką.

## <a name=""></a><a name="IntelliSense">„IntelliSense“</a>

Rengyklėje yra žodžių užbaigimo funkcija, padedanti parašyti išraišką greičiau ir išvengti rašybos klaidų. Pradėjus įtraukti naują tekstą, rengyklėje automatiškai siūlomas sąrašas funkcijų, kurios palaikomos naudojant ER funkcijas ir kuriose yra įvestų simbolių. Taip pat galite paleisti „IntelliSense“ bet kurioje sukonfigūruotos išraiškos vietoje, paspausdami **„Ctrl“+ tarpo klavišas**.

[![ER formulių rengyklės gif, kuriame rodomas „IntelliSense” suaktyvinimas.](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">Kodo užbaigimas</a>

Rengyklėje kodas automatiškai užbaigiamas toliau pateikiamais būdais.

- Uždarymo skliaustas įterpiamas, įvedus pirmą skliaustą, o žymeklis lieka skliaustų viduje.
- Įrašomas antrasis kabučių simbolis, įvedus pirmąjį, o žymeklis lieka kabučių viduje.
- Įrašomas antrasis dvigubų kabučių simbolis, įvedus pirmąjį, o žymeklis lieka kabučių viduje.

[![ER formulių rengyklės gif, rodantis rengyklę automatiškai pateikiančią kodą.](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

Kai žymeklį nukreipiate į įvestą skliaustą, antras šios poros skliaustas automatiškai paryškinamas, kad būtų rodoma skliaustuose esanti konstrukcija.

## <a name=""></a><a name="CodeNavigation">Kodo naršymas</a>

Išraiškoje norimus simbolius arba eilutes rasite, įvedę komandą **Eiti į**, naudodami komandų paletę arba kontekstinį meniu.

Pavyzdžiui, norėdami pereiti į **8** eilutę, atlikite tolesnius veiksmus.

- Paspauskite **„Ctrl“ + „G“**, įveskite vertę **„8“** ir paspauskite **„Enter“**.

  Arba

- Paspauskite **„F1“**, įveskite **„G“**, pasirinkite **Pereiti prie eilutės**, įveskite vertę **„8“** ir paspauskite **„Enter“**.

[![ER formulių rengyklės gif, kuriame rodoma, kaip rasti išraiškos dalis naudojant komandų paletę.](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

## <a name=""></a><a name="CodeStructuring">Kodo susisteminimas</a>

Kai kurių funkcijų, pvz., [„IF“](er-functions-logical-if.md) ar [„CASE“](er-functions-logical-case.md), kodas yra automatiškai susisteminamas. Galite išplėsti ir sutraukti keletą arba visas šio kodo sulankstomas sritis, kad būtų sumažinta redaguojama išraiškos dalis ir būtų sutelktas dėmesys tik į tą kodo fragmentą, kuriam turite skirti dėmesio. Tam galima naudoti sulenkimo / atlenkimo perjungimo komandas.

Pavyzdžiui, norėdami sulenkti visas sritis, atlikite tolesnius veiksmus.

- Paspauskite **„Ctrl“ + „K“**

  Arba

- Paspauskite **„F1“**, paspauskite **„FO“**, pasirinkite **Sulenkti viską**, paskui paspauskite **„Enter“**

Norėdami atlenkti visas sritis, atlikite tolesnius veiksmus.

- Paspauskite **„Ctrl“ + „J“**

  Arba
  
- Paspauskite **„F1“**, įveskite **„UN“**, pasirinkite **Atlenkti viską**, paskui paspauskite **„Enter“**

[![ER formulių rengyklės gif, kuriame rodomas kodo išsiskleidimas.](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

## <a name=""></a><a name="FindAndReplace">Surasti ir pakeisti</a>

Norėdami rasti tam tikro teksto pasikartojimų, pažymėkite tekstą išraiškoje ir atlikite tolesnius veiksmus.

- Paspauskite **„Ctrl“ + „F“**, paskui paspauskite **„F3“**, kad rastumėte kitą pažymėto teksto pasikartojimą, arba paspauskite **„Shift“ + „F3“**, kad rastumėte ankstesnį pasikartojimą.

  Arba
  
- Paspauskite **„F1“**, įveskite **„F“**, tada pasirinkite reikiamą parinktį, kad rastumėte pažymėtą tekstą.

Norėdami pakeisti tam tikro teksto pasikartojimus kitu tekstu, pažymėkite tekstą išraiškoje ir atlikite tolesnius veiksmus.

- Paspauskite **„Ctrl“ + „H“** Įveskite įterptiną tekstą ir pasirinkite pakeitimo parinktį, norėdami pakeisti pažymėtą tekstą arba visus šio teksto pasikartojimus pasirinktoje išraiškoje.

  Arba
  
- Paspauskite **„F1“**, įveskite **„R“**, tada pasirinkite reikiamą parinktį, kad pakeistumėte pažymėtą tekstą kitu. Įveskite įterptiną tekstą ir pasirinkite pakeitimo parinktį, norėdami pakeisti pažymėtą tekstą arba visus šio teksto pasikartojimus pasirinktoje išraiškoje.

Norėdami pakeisti visus tam tikro teksto pasikartojimus, pažymėkite tekstą išraiškoje ir atlikite tolesnius veiksmus.

- Paspauskite **„Ctrl“ + „F2“**, tada įveskite įterptiną tekstą.

  Arba
  
- Paspauskite **„F1“**, įveskite **„C“**, tada pasirinkite reikiamą parinktį, kad pakeistumėte pažymėtą tekstą. Įveskite įterptiną tekstą.

[![ER formulių rengyklės gif, kuriame rodoma rasti ir pakeisti funkcija.](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">Duomenų šaltiniai ir funkcijų įklijavimas</a>

Galite pasirinkti **Įtraukti duomenų šaltinį**, kad į dabartinę išraišką būtų įklijuotas duomenų šaltinis, kuris šiuo metu yra pasirinktas kairiajame skyde **Duomenų šaltinis**. Taip pat galite pasirinkti **Įtraukti funkciją**, kad į dabartinę išraišką būtų įklijuota funkcija, kuri šiuo metu yra pasirinkta dešiniajame skyde **Funkcijos**. Jei naudojate ER formulių rengyklę, pasirinkta funkcija arba pasirinktas duomenų šaltinis visuomet įklijuojami sukonfigūruotos išraiškos gale. Kai naudojate išplėstinę ER formulių rengyklę, pasirinktą funkciją arba pasirinktą duomenų šaltinį galima įklijuoti į bet kurią sukonfigūruotos išraiškos vietą. Turėsite žymekliu nurodyti, kur norite įklijuoti duomenis.

[![ER formulių rengyklės gif, kuriame rodomas duomenų šaltinio pridėjimas ir funkcijos įklijavimas.](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">Sintaksės žymėjimas spalvomis</a>

Šiuo metu skirtingomis spalvomis paryškinamos toliau pateikiamos išraiškų dalys.

- Tekstas dvigubuose skliaustuose, kuris gali reikšti teksto konstantos žymės ID.

[![ER formulių rengyklė.](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="limitations"></a>Apribojimai

Šiuo metu rengyklė palaikoma toliau nurodytose interneto naršyklėse.

- „Chrome“
- „Edge”
- „Firefox“
- „Opera”
- „Safari”

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)
- [„Monaco Editor“](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
