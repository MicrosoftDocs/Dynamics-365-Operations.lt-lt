---
title: Elektroninių ataskaitų išplėstinė formulių rengyklė
description: Šioje temoje aprašoma, kaip išplėstinę formulių rengyklę galima naudoti konfigūruojant išraiškas elektroninių ataskaitų (ER) modelių susiejime ir formato komponentuose.
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
ms.openlocfilehash: f7f80928e1d3f5d4892f72d4bd2fd09b70a26c1f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270712"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="dade1-103">Elektroninių ataskaitų išplėstinė formulių rengyklė</span><span class="sxs-lookup"><span data-stu-id="dade1-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dade1-104">Be [elektroninių ataskaitų](general-electronic-reporting.md)[formulių rengyklės](general-electronic-reporting-formula-designer.md), galite naudoti išplėstinę elektroninių ataskaitų formulių rengyklę, kad pagerėtų elektroninių ataskaitų (ER) išraiškų konfigūravimo patirtis.</span><span class="sxs-lookup"><span data-stu-id="dade1-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="dade1-105">Išplėstinė rengyklė veikia naršyklėje [„Monaco Editor“ pagrindu](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="dade1-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="dade1-106">Dažniausiai naudojamos išplėstinės rengyklės funkcijos aprašomos šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="dade1-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="dade1-107">Automatinis kodo formatavimas</span><span class="sxs-lookup"><span data-stu-id="dade1-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="dade1-108">„IntelliSense“</span><span class="sxs-lookup"><span data-stu-id="dade1-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="dade1-109">Kodo užbaigimas</span><span class="sxs-lookup"><span data-stu-id="dade1-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="dade1-110">Kodo naršymas</span><span class="sxs-lookup"><span data-stu-id="dade1-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="dade1-111">Kodo susisteminimas</span><span class="sxs-lookup"><span data-stu-id="dade1-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="dade1-112">Surasti ir pakeisti</span><span class="sxs-lookup"><span data-stu-id="dade1-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="dade1-113">Duomenų įklijavimas</span><span class="sxs-lookup"><span data-stu-id="dade1-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="dade1-114">Sintaksės žymėjimas spalvomis</span><span class="sxs-lookup"><span data-stu-id="dade1-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="dade1-115"><a name="ActivateAdvEditor">Išplėstinės formulių rengyklės aktyvinimas</a></span><span class="sxs-lookup"><span data-stu-id="dade1-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="dade1-116">Atlikite tolesnius veiksmus, kad pradėtumėte naudoti išplėstinę formulių rengyklę „Microsoft Dynamics 365 Finance“ egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="dade1-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="dade1-117">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="dade1-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="dade1-118">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dade1-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="dade1-119">Dialogo lange **Vartotojo parametrai**, skyriuje **Vykdymo sekimas** nustatykite parinkties **Įgalinti išplėstinę formulių rengyklę** parametrą **Taip**.</span><span class="sxs-lookup"><span data-stu-id="dade1-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="dade1-120">[![Paryškinti Vartotojo parametrų dialogo langas, Patobulintos formulių rengyklės parametro įgalinimas](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="dade1-120">[![User parameters dialog box, Enable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="dade1-121">Atminkite, kad šis parametras yra susijęs su konkrečiu vartotoju ir įmone.</span><span class="sxs-lookup"><span data-stu-id="dade1-121">Be aware that this parameter is user specific and company specific.</span></span>

<span data-ttu-id="dade1-122">Pradedant nuo 10.0.19 „Microsoft Dynamics 365 Finance” versijos, galite kontroliuoti, kokia ER formulių rengyklė siūloma pagal numatytuosius nustatymus.</span><span class="sxs-lookup"><span data-stu-id="dade1-122">Starting in Microsoft Dynamics 365 Finance version 10.0.19, you can control what ER formula editor is offered by default.</span></span> <span data-ttu-id="dade1-123">Atlikite šiuos veiksmus, norėdami įgalinti patobulintą formulių rengyklę visiems dabartinio „Finance” egzemplioriaus vartotojams ir įmonėms.</span><span class="sxs-lookup"><span data-stu-id="dade1-123">Complete the following steps to enable the advanced formula editor for all users and companies of the current Finance instance.</span></span>

1.  <span data-ttu-id="dade1-124">Atidarykite parinkties **Funkcijos valdymas** darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="dade1-124">Open the **Feature management** workspace.</span></span>
2.  <span data-ttu-id="dade1-125">Raskite ir pasirinkite funkciją **Nustatyti ER patobulintą formulių rengyklę kaip numatytąją visiems vartotojams** sąraše, o tada pasirinkite **Įgalinti dabar**.</span><span class="sxs-lookup"><span data-stu-id="dade1-125">Find and select the feature **Set the ER advanced formula editor as the default one for all users** in the list, and then select **Enable now**.</span></span>
3.  <span data-ttu-id="dade1-126">Eikite į **Organizacijos administravimas** > **Elektroninės ataskaitos** > **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="dade1-126">Go to **Organization administration** > **Electronic reporting** > **Configurations**.</span></span>
4.  <span data-ttu-id="dade1-127">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dade1-127">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
5.  <span data-ttu-id="dade1-128">Dialogo lange **Vartotojo parametrai** suraskite parametrą **Išjungti patobulintą formulių rengyklę** ir patikrinkite, ar jis nustatytas į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="dade1-128">In the **User parameters** dialog box, find the **Disable advanced formula editor** parameter and verify that it is set to **No**.</span></span>

<span data-ttu-id="dade1-129">[![Paryškinti Vartotojo parametrų dialogo langas, Patobulintos formulių rengyklės parametro išjungimas](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span><span class="sxs-lookup"><span data-stu-id="dade1-129">[![User parameters dialog box, Disable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span></span>

> [!NOTE]
> <span data-ttu-id="dade1-130">Parametrų **Įgalinti patobulintą formulių rengyklę** ir **Išjungti patobulintą formulių rengyklę** reikšmės yra atskiros kiekvienam vartotojui ir siūlomos **Vartotojo parametrų** dialogo lange, priklausomai nuo funkcijos **Nustatyti ER patobulintą formulių rengyklė kaip numatytąją visiems vartotojams** būsenos.</span><span class="sxs-lookup"><span data-stu-id="dade1-130">The values of the parameters **Enable advanced formula editor** and **Disable advanced formula editor** are kept separate for each user and offered on the **User parameters** dialog box depending on the status of the **Set the ER advanced formula editor as the default one for all users** feature.</span></span>

## <a name=""></a><span data-ttu-id="dade1-131"><a name="Autoformatting">Automatinis kodo formatavimas</a></span><span class="sxs-lookup"><span data-stu-id="dade1-131"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="dade1-132">Rašant sudėtingą išraišką, kurią sudaro keletas kodo eilučių, naujai įvestos eilutės įtrauka bus automatiškai pagrįsta ankstesnės eilutės įtrauka.</span><span class="sxs-lookup"><span data-stu-id="dade1-132">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="dade1-133">Galite pasirinkti eilutes ir pakeisti jų įtrauką, paspausdami **Tabuliavimo klavišas** arba **„Shift“ + tabuliavimo klavišas**.</span><span class="sxs-lookup"><span data-stu-id="dade1-133">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="dade1-134">[![ER formulių rengyklės gif, rodantis eilučių pasirinkimą ir įtraukos keitimą](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="dade1-134">[![ER formula editor gif showing selecting lines and changing the indentation](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="dade1-135">Automatinis formatavimas leidžia išsaugoti visos išraiškos tinkamą formatavimą, kad būtų lengviau atlikti priežiūrą ir būtų paprasčiau suprasti sukonfigūruotą logiką.</span><span class="sxs-lookup"><span data-stu-id="dade1-135">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="dade1-136"><a name="IntelliSense">„IntelliSense“</a></span><span class="sxs-lookup"><span data-stu-id="dade1-136"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="dade1-137">Rengyklėje yra žodžių užbaigimo funkcija, padedanti parašyti išraišką greičiau ir išvengti rašybos klaidų.</span><span class="sxs-lookup"><span data-stu-id="dade1-137">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="dade1-138">Pradėjus įtraukti naują tekstą, rengyklėje automatiškai siūlomas sąrašas funkcijų, kurios palaikomos naudojant ER funkcijas ir kuriose yra įvestų simbolių.</span><span class="sxs-lookup"><span data-stu-id="dade1-138">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="dade1-139">Taip pat galite paleisti „IntelliSense“ bet kurioje sukonfigūruotos išraiškos vietoje, paspausdami **„Ctrl“+ tarpo klavišas**.</span><span class="sxs-lookup"><span data-stu-id="dade1-139">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="dade1-140">[![ER formulių rengyklės gif, kuriame rodomas „IntelliSense” suaktyvinimas](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="dade1-140">[![ER formula editor gif showing triggering IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="dade1-141"><a name="CodeCompletion">Kodo užbaigimas</a></span><span class="sxs-lookup"><span data-stu-id="dade1-141"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="dade1-142">Rengyklėje kodas automatiškai užbaigiamas toliau pateikiamais būdais.</span><span class="sxs-lookup"><span data-stu-id="dade1-142">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="dade1-143">Uždarymo skliaustas įterpiamas, įvedus pirmą skliaustą, o žymeklis lieka skliaustų viduje.</span><span class="sxs-lookup"><span data-stu-id="dade1-143">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="dade1-144">Įrašomas antrasis kabučių simbolis, įvedus pirmąjį, o žymeklis lieka kabučių viduje.</span><span class="sxs-lookup"><span data-stu-id="dade1-144">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="dade1-145">Įrašomas antrasis dvigubų kabučių simbolis, įvedus pirmąjį, o žymeklis lieka kabučių viduje.</span><span class="sxs-lookup"><span data-stu-id="dade1-145">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="dade1-146">[![ER formulių rengyklės gif, rodantis rengyklę automatiškai pateikiančią kodą](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="dade1-146">[![ER formula editor gif showing the editor automatically providing code completion](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="dade1-147">Kai žymeklį nukreipiate į įvestą skliaustą, antras šios poros skliaustas automatiškai paryškinamas, kad būtų rodoma skliaustuose esanti konstrukcija.</span><span class="sxs-lookup"><span data-stu-id="dade1-147">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="dade1-148"><a name="CodeNavigation">Kodo naršymas</a></span><span class="sxs-lookup"><span data-stu-id="dade1-148"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="dade1-149">Išraiškoje norimus simbolius arba eilutes rasite, įvedę komandą **Eiti į**, naudodami komandų paletę arba kontekstinį meniu.</span><span class="sxs-lookup"><span data-stu-id="dade1-149">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="dade1-150">Pavyzdžiui, norėdami pereiti į **8** eilutę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dade1-150">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="dade1-151">Paspauskite **„Ctrl“ + „G“**, įveskite vertę **„8“** ir paspauskite **„Enter“**.</span><span class="sxs-lookup"><span data-stu-id="dade1-151">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="dade1-152">Arba</span><span class="sxs-lookup"><span data-stu-id="dade1-152">-or-</span></span>

- <span data-ttu-id="dade1-153">Paspauskite **„F1“**, įveskite **„G“**, pasirinkite **Pereiti prie eilutės**, įveskite vertę **„8“** ir paspauskite **„Enter“**.</span><span class="sxs-lookup"><span data-stu-id="dade1-153">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="dade1-154">[![ER formulių rengyklės gif, kuriame rodoma, kaip rasti išraiškos dalis naudojant komandų paletę](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="dade1-154">[![ER formula editor gif showing how to locate parts of an expression using the command palette](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="dade1-155"><a name="CodeStructuring">Kodo susisteminimas</a></span><span class="sxs-lookup"><span data-stu-id="dade1-155"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="dade1-156">Kai kurių funkcijų, pvz., [„IF“](er-functions-logical-if.md) ar [„CASE“](er-functions-logical-case.md), kodas yra automatiškai susisteminamas.</span><span class="sxs-lookup"><span data-stu-id="dade1-156">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="dade1-157">Galite išplėsti ir sutraukti keletą arba visas šio kodo sulankstomas sritis, kad būtų sumažinta redaguojama išraiškos dalis ir būtų sutelktas dėmesys tik į tą kodo fragmentą, kuriam turite skirti dėmesio.</span><span class="sxs-lookup"><span data-stu-id="dade1-157">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="dade1-158">Tam galima naudoti sulenkimo / atlenkimo perjungimo komandas.</span><span class="sxs-lookup"><span data-stu-id="dade1-158">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="dade1-159">Pavyzdžiui, norėdami sulenkti visas sritis, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dade1-159">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="dade1-160">Paspauskite **„Ctrl“ + „K“**</span><span class="sxs-lookup"><span data-stu-id="dade1-160">Press **Ctrl+K**</span></span>

  <span data-ttu-id="dade1-161">Arba</span><span class="sxs-lookup"><span data-stu-id="dade1-161">-or-</span></span>

- <span data-ttu-id="dade1-162">Paspauskite **„F1“**, paspauskite **„FO“**, pasirinkite **Sulenkti viską**, paskui paspauskite **„Enter“**</span><span class="sxs-lookup"><span data-stu-id="dade1-162">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="dade1-163">Norėdami atlenkti visas sritis, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dade1-163">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="dade1-164">Paspauskite **„Ctrl“ + „J“**</span><span class="sxs-lookup"><span data-stu-id="dade1-164">Press **Ctrl+J**</span></span>

  <span data-ttu-id="dade1-165">Arba</span><span class="sxs-lookup"><span data-stu-id="dade1-165">-or-</span></span>
  
- <span data-ttu-id="dade1-166">Paspauskite **„F1“**, įveskite **„UN“**, pasirinkite **Atlenkti viską**, paskui paspauskite **„Enter“**</span><span class="sxs-lookup"><span data-stu-id="dade1-166">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="dade1-167">[![ER formulių rengyklės gif, kuriame rodomas kodo išsiskleidimas](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="dade1-167">[![ER formula editor gif showing code being unfolded](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="dade1-168"><a name="FindAndReplace">Surasti ir pakeisti</a></span><span class="sxs-lookup"><span data-stu-id="dade1-168"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="dade1-169">Norėdami rasti tam tikro teksto pasikartojimų, pažymėkite tekstą išraiškoje ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dade1-169">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="dade1-170">Paspauskite **„Ctrl“ + „F“**, paskui paspauskite **„F3“**, kad rastumėte kitą pažymėto teksto pasikartojimą, arba paspauskite **„Shift“ + „F3“**, kad rastumėte ankstesnį pasikartojimą.</span><span class="sxs-lookup"><span data-stu-id="dade1-170">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="dade1-171">Arba</span><span class="sxs-lookup"><span data-stu-id="dade1-171">-or-</span></span>
  
- <span data-ttu-id="dade1-172">Paspauskite **„F1“**, įveskite **„F“**, tada pasirinkite reikiamą parinktį, kad rastumėte pažymėtą tekstą.</span><span class="sxs-lookup"><span data-stu-id="dade1-172">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="dade1-173">Norėdami pakeisti tam tikro teksto pasikartojimus kitu tekstu, pažymėkite tekstą išraiškoje ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dade1-173">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="dade1-174">Paspauskite **„Ctrl“ + „H“**</span><span class="sxs-lookup"><span data-stu-id="dade1-174">Press **Ctrl+H**.</span></span> <span data-ttu-id="dade1-175">Įveskite įterptiną tekstą ir pasirinkite pakeitimo parinktį, norėdami pakeisti pažymėtą tekstą arba visus šio teksto pasikartojimus pasirinktoje išraiškoje.</span><span class="sxs-lookup"><span data-stu-id="dade1-175">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="dade1-176">Arba</span><span class="sxs-lookup"><span data-stu-id="dade1-176">-or-</span></span>
  
- <span data-ttu-id="dade1-177">Paspauskite **„F1“**, įveskite **„R“**, tada pasirinkite reikiamą parinktį, kad pakeistumėte pažymėtą tekstą kitu.</span><span class="sxs-lookup"><span data-stu-id="dade1-177">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="dade1-178">Įveskite įterptiną tekstą ir pasirinkite pakeitimo parinktį, norėdami pakeisti pažymėtą tekstą arba visus šio teksto pasikartojimus pasirinktoje išraiškoje.</span><span class="sxs-lookup"><span data-stu-id="dade1-178">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="dade1-179">Norėdami pakeisti visus tam tikro teksto pasikartojimus, pažymėkite tekstą išraiškoje ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dade1-179">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="dade1-180">Paspauskite **„Ctrl“ + „F2“**, tada įveskite įterptiną tekstą.</span><span class="sxs-lookup"><span data-stu-id="dade1-180">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="dade1-181">Arba</span><span class="sxs-lookup"><span data-stu-id="dade1-181">-or-</span></span>
  
- <span data-ttu-id="dade1-182">Paspauskite **„F1“**, įveskite **„C“**, tada pasirinkite reikiamą parinktį, kad pakeistumėte pažymėtą tekstą.</span><span class="sxs-lookup"><span data-stu-id="dade1-182">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="dade1-183">Įveskite įterptiną tekstą.</span><span class="sxs-lookup"><span data-stu-id="dade1-183">Enter the alternative text.</span></span>

<span data-ttu-id="dade1-184">[![ER formulių rengyklės gif, kuriame rodoma rasti ir pakeisti funkcija](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="dade1-184">[![ER formula editor gif showing find and replace](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="dade1-185"><a name="DataPasting">Duomenų šaltiniai ir funkcijų įklijavimas</a></span><span class="sxs-lookup"><span data-stu-id="dade1-185"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="dade1-186">Galite pasirinkti **Įtraukti duomenų šaltinį**, kad į dabartinę išraišką būtų įklijuotas duomenų šaltinis, kuris šiuo metu yra pasirinktas kairiajame skyde **Duomenų šaltinis**.</span><span class="sxs-lookup"><span data-stu-id="dade1-186">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="dade1-187">Taip pat galite pasirinkti **Įtraukti funkciją**, kad į dabartinę išraišką būtų įklijuota funkcija, kuri šiuo metu yra pasirinkta dešiniajame skyde **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="dade1-187">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="dade1-188">Jei naudojate ER formulių rengyklę, pasirinkta funkcija arba pasirinktas duomenų šaltinis visuomet įklijuojami sukonfigūruotos išraiškos gale.</span><span class="sxs-lookup"><span data-stu-id="dade1-188">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="dade1-189">Kai naudojate išplėstinę ER formulių rengyklę, pasirinktą funkciją arba pasirinktą duomenų šaltinį galima įklijuoti į bet kurią sukonfigūruotos išraiškos vietą.</span><span class="sxs-lookup"><span data-stu-id="dade1-189">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="dade1-190">Turėsite žymekliu nurodyti, kur norite įklijuoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="dade1-190">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="dade1-191">[![ER formulių rengyklės gif, kuriame rodomas duomenų šaltinio pridėjimas ir funkcijos įklijavimas](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="dade1-191">[![ER formula editor gif showing adding a data source and pasting a function](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="dade1-192"><a name="SyntaxColorization">Sintaksės žymėjimas spalvomis</a></span><span class="sxs-lookup"><span data-stu-id="dade1-192"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="dade1-193">Šiuo metu skirtingomis spalvomis paryškinamos toliau pateikiamos išraiškų dalys.</span><span class="sxs-lookup"><span data-stu-id="dade1-193">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="dade1-194">Tekstas dvigubuose skliaustuose, kuris gali reikšti teksto konstantos žymės ID.</span><span class="sxs-lookup"><span data-stu-id="dade1-194">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="dade1-195">[![ER formulių rengyklė](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="dade1-195">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="dade1-196">Apribojimai</span><span class="sxs-lookup"><span data-stu-id="dade1-196">Limitations</span></span>

<span data-ttu-id="dade1-197">Šiuo metu rengyklė palaikoma toliau nurodytose interneto naršyklėse.</span><span class="sxs-lookup"><span data-stu-id="dade1-197">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="dade1-198">„Chrome“</span><span class="sxs-lookup"><span data-stu-id="dade1-198">Chrome</span></span>
- <span data-ttu-id="dade1-199">„Edge”</span><span class="sxs-lookup"><span data-stu-id="dade1-199">Edge</span></span>
- <span data-ttu-id="dade1-200">„Firefox“</span><span class="sxs-lookup"><span data-stu-id="dade1-200">Firefox</span></span>
- <span data-ttu-id="dade1-201">„Opera”</span><span class="sxs-lookup"><span data-stu-id="dade1-201">Opera</span></span>
- <span data-ttu-id="dade1-202">„Safari”</span><span class="sxs-lookup"><span data-stu-id="dade1-202">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dade1-203">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="dade1-203">Additional resources</span></span>

- [<span data-ttu-id="dade1-204">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="dade1-204">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="dade1-205">Elektroninių ataskaitų formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="dade1-205">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="dade1-206">„Monaco Editor“</span><span class="sxs-lookup"><span data-stu-id="dade1-206">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
