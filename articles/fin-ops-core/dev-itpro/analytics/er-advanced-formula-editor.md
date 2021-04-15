---
title: Elektroninių ataskaitų išplėstinė formulių rengyklė
description: Šioje temoje aprašoma, kaip išplėstinę formulių rengyklę galima naudoti konfigūruojant išraiškas elektroninių ataskaitų (ER) modelių susiejime ir formato komponentuose.
author: NickSelin
ms.date: 04/10/2020
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
ms.openlocfilehash: d18aeedb2f21176ffe964b926168d4bf088a093b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751213"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="c0f36-103">Elektroninių ataskaitų išplėstinė formulių rengyklė</span><span class="sxs-lookup"><span data-stu-id="c0f36-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0f36-104">Be [elektroninių ataskaitų](general-electronic-reporting.md)[formulių rengyklės](general-electronic-reporting-formula-designer.md), galite naudoti išplėstinę elektroninių ataskaitų formulių rengyklę, kad pagerėtų elektroninių ataskaitų (ER) išraiškų konfigūravimo patirtis.</span><span class="sxs-lookup"><span data-stu-id="c0f36-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="c0f36-105">Išplėstinė rengyklė veikia naršyklėje [„Monaco Editor“ pagrindu](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="c0f36-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="c0f36-106">Dažniausiai naudojamos išplėstinės rengyklės funkcijos aprašomos šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="c0f36-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="c0f36-107">Automatinis kodo formatavimas</span><span class="sxs-lookup"><span data-stu-id="c0f36-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="c0f36-108">„IntelliSense“</span><span class="sxs-lookup"><span data-stu-id="c0f36-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="c0f36-109">Kodo užbaigimas</span><span class="sxs-lookup"><span data-stu-id="c0f36-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="c0f36-110">Kodo naršymas</span><span class="sxs-lookup"><span data-stu-id="c0f36-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="c0f36-111">Kodo susisteminimas</span><span class="sxs-lookup"><span data-stu-id="c0f36-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="c0f36-112">Surasti ir pakeisti</span><span class="sxs-lookup"><span data-stu-id="c0f36-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="c0f36-113">Duomenų įklijavimas</span><span class="sxs-lookup"><span data-stu-id="c0f36-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="c0f36-114">Sintaksės žymėjimas spalvomis</span><span class="sxs-lookup"><span data-stu-id="c0f36-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="c0f36-115"><a name="ActivateAdvEditor">Išplėstinės formulių rengyklės aktyvinimas</a></span><span class="sxs-lookup"><span data-stu-id="c0f36-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="c0f36-116">Atlikite tolesnius veiksmus, kad pradėtumėte naudoti išplėstinę formulių rengyklę „Microsoft Dynamics 365 Finance“ egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="c0f36-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="c0f36-117">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="c0f36-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="c0f36-118">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c0f36-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="c0f36-119">Dialogo lange **Vartotojo parametrai**, skyriuje **Vykdymo sekimas** nustatykite parinkties **Įgalinti išplėstinę formulių rengyklę** parametrą **Taip**.</span><span class="sxs-lookup"><span data-stu-id="c0f36-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="c0f36-120">[![ER konfigūracijų puslapis](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="c0f36-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="c0f36-121">Atminkite, kad šis parametras yra susijęs su konkrečiu vartotoju ir įmone.</span><span class="sxs-lookup"><span data-stu-id="c0f36-121">Be aware that this parameter is user specific and company specific.</span></span>

## <a name=""></a><span data-ttu-id="c0f36-122"><a name="Autoformatting">Automatinis kodo formatavimas</a></span><span class="sxs-lookup"><span data-stu-id="c0f36-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="c0f36-123">Rašant sudėtingą išraišką, kurią sudaro keletas kodo eilučių, naujai įvestos eilutės įtrauka bus automatiškai pagrįsta ankstesnės eilutės įtrauka.</span><span class="sxs-lookup"><span data-stu-id="c0f36-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="c0f36-124">Galite pasirinkti eilutes ir pakeisti jų įtrauką, paspausdami **Tabuliavimo klavišas** arba **„Shift“ + tabuliavimo klavišas**.</span><span class="sxs-lookup"><span data-stu-id="c0f36-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="c0f36-125">[![ER formulių rengyklė](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="c0f36-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="c0f36-126">Automatinis formatavimas leidžia išsaugoti visos išraiškos tinkamą formatavimą, kad būtų lengviau atlikti priežiūrą ir būtų paprasčiau suprasti sukonfigūruotą logiką.</span><span class="sxs-lookup"><span data-stu-id="c0f36-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="c0f36-127"><a name="IntelliSense">„IntelliSense“</a></span><span class="sxs-lookup"><span data-stu-id="c0f36-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="c0f36-128">Rengyklėje yra žodžių užbaigimo funkcija, padedanti parašyti išraišką greičiau ir išvengti rašybos klaidų.</span><span class="sxs-lookup"><span data-stu-id="c0f36-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="c0f36-129">Pradėjus įtraukti naują tekstą, rengyklėje automatiškai siūlomas sąrašas funkcijų, kurios palaikomos naudojant ER funkcijas ir kuriose yra įvestų simbolių.</span><span class="sxs-lookup"><span data-stu-id="c0f36-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="c0f36-130">Taip pat galite paleisti „IntelliSense“ bet kurioje sukonfigūruotos išraiškos vietoje, paspausdami **„Ctrl“+ tarpo klavišas**.</span><span class="sxs-lookup"><span data-stu-id="c0f36-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="c0f36-131">[![ER formulių rengyklė](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="c0f36-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="c0f36-132"><a name="CodeCompletion">Kodo užbaigimas</a></span><span class="sxs-lookup"><span data-stu-id="c0f36-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="c0f36-133">Rengyklėje kodas automatiškai užbaigiamas toliau pateikiamais būdais.</span><span class="sxs-lookup"><span data-stu-id="c0f36-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="c0f36-134">Uždarymo skliaustas įterpiamas, įvedus pirmą skliaustą, o žymeklis lieka skliaustų viduje.</span><span class="sxs-lookup"><span data-stu-id="c0f36-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="c0f36-135">Įrašomas antrasis kabučių simbolis, įvedus pirmąjį, o žymeklis lieka kabučių viduje.</span><span class="sxs-lookup"><span data-stu-id="c0f36-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="c0f36-136">Įrašomas antrasis dvigubų kabučių simbolis, įvedus pirmąjį, o žymeklis lieka kabučių viduje.</span><span class="sxs-lookup"><span data-stu-id="c0f36-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="c0f36-137">[![ER formulių rengyklė](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="c0f36-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="c0f36-138">Kai žymeklį nukreipiate į įvestą skliaustą, antras šios poros skliaustas automatiškai paryškinamas, kad būtų rodoma skliaustuose esanti konstrukcija.</span><span class="sxs-lookup"><span data-stu-id="c0f36-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="c0f36-139"><a name="CodeNavigation">Kodo naršymas</a></span><span class="sxs-lookup"><span data-stu-id="c0f36-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="c0f36-140">Išraiškoje norimus simbolius arba eilutes rasite, įvedę komandą **Eiti į**, naudodami komandų paletę arba kontekstinį meniu.</span><span class="sxs-lookup"><span data-stu-id="c0f36-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="c0f36-141">Pavyzdžiui, norėdami pereiti į **8** eilutę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c0f36-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="c0f36-142">Paspauskite **„Ctrl“ + „G“**, įveskite vertę **„8“** ir paspauskite **„Enter“**.</span><span class="sxs-lookup"><span data-stu-id="c0f36-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="c0f36-143">Arba</span><span class="sxs-lookup"><span data-stu-id="c0f36-143">-or-</span></span>

- <span data-ttu-id="c0f36-144">Paspauskite **„F1“**, įveskite **„G“**, pasirinkite **Pereiti prie eilutės**, įveskite vertę **„8“** ir paspauskite **„Enter“**.</span><span class="sxs-lookup"><span data-stu-id="c0f36-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="c0f36-145">[![ER formulių rengyklė](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="c0f36-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="c0f36-146"><a name="CodeStructuring">Kodo susisteminimas</a></span><span class="sxs-lookup"><span data-stu-id="c0f36-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="c0f36-147">Kai kurių funkcijų, pvz., [„IF“](er-functions-logical-if.md) ar [„CASE“](er-functions-logical-case.md), kodas yra automatiškai susisteminamas.</span><span class="sxs-lookup"><span data-stu-id="c0f36-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="c0f36-148">Galite išplėsti ir sutraukti keletą arba visas šio kodo sulankstomas sritis, kad būtų sumažinta redaguojama išraiškos dalis ir būtų sutelktas dėmesys tik į tą kodo fragmentą, kuriam turite skirti dėmesio.</span><span class="sxs-lookup"><span data-stu-id="c0f36-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="c0f36-149">Tam galima naudoti sulenkimo / atlenkimo perjungimo komandas.</span><span class="sxs-lookup"><span data-stu-id="c0f36-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="c0f36-150">Pavyzdžiui, norėdami sulenkti visas sritis, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c0f36-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="c0f36-151">Paspauskite **„Ctrl“ + „K“**</span><span class="sxs-lookup"><span data-stu-id="c0f36-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="c0f36-152">Arba</span><span class="sxs-lookup"><span data-stu-id="c0f36-152">-or-</span></span>

- <span data-ttu-id="c0f36-153">Paspauskite **„F1“**, paspauskite **„FO“**, pasirinkite **Sulenkti viską**, paskui paspauskite **„Enter“**</span><span class="sxs-lookup"><span data-stu-id="c0f36-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="c0f36-154">Norėdami atlenkti visas sritis, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c0f36-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="c0f36-155">Paspauskite **„Ctrl“ + „J“**</span><span class="sxs-lookup"><span data-stu-id="c0f36-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="c0f36-156">Arba</span><span class="sxs-lookup"><span data-stu-id="c0f36-156">-or-</span></span>
  
- <span data-ttu-id="c0f36-157">Paspauskite **„F1“**, įveskite **„UN“**, pasirinkite **Atlenkti viską**, paskui paspauskite **„Enter“**</span><span class="sxs-lookup"><span data-stu-id="c0f36-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="c0f36-158">[![ER formulių rengyklė](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="c0f36-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="c0f36-159"><a name="FindAndReplace">Surasti ir pakeisti</a></span><span class="sxs-lookup"><span data-stu-id="c0f36-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="c0f36-160">Norėdami rasti tam tikro teksto pasikartojimų, pažymėkite tekstą išraiškoje ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c0f36-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="c0f36-161">Paspauskite **„Ctrl“ + „F“**, paskui paspauskite **„F3“**, kad rastumėte kitą pažymėto teksto pasikartojimą, arba paspauskite **„Shift“ + „F3“**, kad rastumėte ankstesnį pasikartojimą.</span><span class="sxs-lookup"><span data-stu-id="c0f36-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="c0f36-162">Arba</span><span class="sxs-lookup"><span data-stu-id="c0f36-162">-or-</span></span>
  
- <span data-ttu-id="c0f36-163">Paspauskite **„F1“**, įveskite **„F“**, tada pasirinkite reikiamą parinktį, kad rastumėte pažymėtą tekstą.</span><span class="sxs-lookup"><span data-stu-id="c0f36-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="c0f36-164">Norėdami pakeisti tam tikro teksto pasikartojimus kitu tekstu, pažymėkite tekstą išraiškoje ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c0f36-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="c0f36-165">Paspauskite **„Ctrl“ + „H“**</span><span class="sxs-lookup"><span data-stu-id="c0f36-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="c0f36-166">Įveskite įterptiną tekstą ir pasirinkite pakeitimo parinktį, norėdami pakeisti pažymėtą tekstą arba visus šio teksto pasikartojimus pasirinktoje išraiškoje.</span><span class="sxs-lookup"><span data-stu-id="c0f36-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="c0f36-167">Arba</span><span class="sxs-lookup"><span data-stu-id="c0f36-167">-or-</span></span>
  
- <span data-ttu-id="c0f36-168">Paspauskite **„F1“**, įveskite **„R“**, tada pasirinkite reikiamą parinktį, kad pakeistumėte pažymėtą tekstą kitu.</span><span class="sxs-lookup"><span data-stu-id="c0f36-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="c0f36-169">Įveskite įterptiną tekstą ir pasirinkite pakeitimo parinktį, norėdami pakeisti pažymėtą tekstą arba visus šio teksto pasikartojimus pasirinktoje išraiškoje.</span><span class="sxs-lookup"><span data-stu-id="c0f36-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="c0f36-170">Norėdami pakeisti visus tam tikro teksto pasikartojimus, pažymėkite tekstą išraiškoje ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c0f36-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="c0f36-171">Paspauskite **„Ctrl“ + „F2“**, tada įveskite įterptiną tekstą.</span><span class="sxs-lookup"><span data-stu-id="c0f36-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="c0f36-172">Arba</span><span class="sxs-lookup"><span data-stu-id="c0f36-172">-or-</span></span>
  
- <span data-ttu-id="c0f36-173">Paspauskite **„F1“**, įveskite **„C“**, tada pasirinkite reikiamą parinktį, kad pakeistumėte pažymėtą tekstą.</span><span class="sxs-lookup"><span data-stu-id="c0f36-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="c0f36-174">Įveskite įterptiną tekstą.</span><span class="sxs-lookup"><span data-stu-id="c0f36-174">Enter the alternative text.</span></span>

<span data-ttu-id="c0f36-175">[![ER formulių rengyklė](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="c0f36-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="c0f36-176"><a name="DataPasting">Duomenų šaltiniai ir funkcijų įklijavimas</a></span><span class="sxs-lookup"><span data-stu-id="c0f36-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="c0f36-177">Galite pasirinkti **Įtraukti duomenų šaltinį**, kad į dabartinę išraišką būtų įklijuotas duomenų šaltinis, kuris šiuo metu yra pasirinktas kairiajame skyde **Duomenų šaltinis**.</span><span class="sxs-lookup"><span data-stu-id="c0f36-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="c0f36-178">Taip pat galite pasirinkti **Įtraukti funkciją**, kad į dabartinę išraišką būtų įklijuota funkcija, kuri šiuo metu yra pasirinkta dešiniajame skyde **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="c0f36-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="c0f36-179">Jei naudojate ER formulių rengyklę, pasirinkta funkcija arba pasirinktas duomenų šaltinis visuomet įklijuojami sukonfigūruotos išraiškos gale.</span><span class="sxs-lookup"><span data-stu-id="c0f36-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="c0f36-180">Kai naudojate išplėstinę ER formulių rengyklę, pasirinktą funkciją arba pasirinktą duomenų šaltinį galima įklijuoti į bet kurią sukonfigūruotos išraiškos vietą.</span><span class="sxs-lookup"><span data-stu-id="c0f36-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="c0f36-181">Turėsite žymekliu nurodyti, kur norite įklijuoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="c0f36-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="c0f36-182">[![ER formulių rengyklė](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="c0f36-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="c0f36-183"><a name="SyntaxColorization">Sintaksės žymėjimas spalvomis</a></span><span class="sxs-lookup"><span data-stu-id="c0f36-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="c0f36-184">Šiuo metu skirtingomis spalvomis paryškinamos toliau pateikiamos išraiškų dalys.</span><span class="sxs-lookup"><span data-stu-id="c0f36-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="c0f36-185">Tekstas dvigubuose skliaustuose, kuris gali reikšti teksto konstantos žymės ID.</span><span class="sxs-lookup"><span data-stu-id="c0f36-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="c0f36-186">[![ER formulių rengyklė](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="c0f36-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="c0f36-187">Apribojimai</span><span class="sxs-lookup"><span data-stu-id="c0f36-187">Limitations</span></span>

<span data-ttu-id="c0f36-188">Šiuo metu rengyklė palaikoma toliau nurodytose interneto naršyklėse.</span><span class="sxs-lookup"><span data-stu-id="c0f36-188">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="c0f36-189">„Chrome“</span><span class="sxs-lookup"><span data-stu-id="c0f36-189">Chrome</span></span>
- <span data-ttu-id="c0f36-190">„Edge”</span><span class="sxs-lookup"><span data-stu-id="c0f36-190">Edge</span></span>
- <span data-ttu-id="c0f36-191">„Firefox“</span><span class="sxs-lookup"><span data-stu-id="c0f36-191">Firefox</span></span>
- <span data-ttu-id="c0f36-192">„Opera”</span><span class="sxs-lookup"><span data-stu-id="c0f36-192">Opera</span></span>
- <span data-ttu-id="c0f36-193">„Safari”</span><span class="sxs-lookup"><span data-stu-id="c0f36-193">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0f36-194">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c0f36-194">Additional resources</span></span>

- [<span data-ttu-id="c0f36-195">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="c0f36-195">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="c0f36-196">Elektroninių ataskaitų formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="c0f36-196">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="c0f36-197">„Monaco Editor“</span><span class="sxs-lookup"><span data-stu-id="c0f36-197">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]