---
title: Konfigūracijos, skirtos dokumentams „Excel“ formatu generuoti, kūrimas
description: Šioje temoje pateikiama informacija, kaip kurti Elektroninės ataskaitos (ER) formatą, kad būtų galima pildyti „Excel“ šabloną, o tada generuoti siunčiamus „Excel“ formato dokumentus.
author: NickSelin
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e889b08f10c5d0c95fed7c9e422340706bdd154a
ms.sourcegitcommit: 67ce81c57194afb26a04ae4c0b7509e0efa32afc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/14/2020
ms.locfileid: "3375818"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="85e53-103">Konfigūracijos, skirtos dokumentams „Excel“ formatu generuoti, kūrimas</span><span class="sxs-lookup"><span data-stu-id="85e53-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="85e53-104">Galite sukurti [Elektroninės ataskaitos (ER)](general-electronic-reporting.md) formato konfigūraciją, kurios ER [formato komponentą](general-electronic-reporting.md#FormatComponentOutbound) galite sukonfigūruoti taip, kad siunčiamas dokumentas būtų sugeneruotas „Microsoft Excel“ darbaknygės formatu.</span><span class="sxs-lookup"><span data-stu-id="85e53-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="85e53-105">Šiam tikslui reikia naudoti konkrečius ER formato komponentus.</span><span class="sxs-lookup"><span data-stu-id="85e53-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="85e53-106">Norėdami daugiau sužinoti apie šią funkciją, atlikite veiksmus, aprašytus temoje [Konfigūracijos, skirtos ataskaitoms OPENXML formatu generuoti, kūrimas](tasks/er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="85e53-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="85e53-107">Naujo ER formato įtraukimas</span><span class="sxs-lookup"><span data-stu-id="85e53-107">Add a new ER format</span></span>

<span data-ttu-id="85e53-108">Kai įtraukiate naują ER formato konfigūraciją, kad siunčiami dokumentai būtų generuojami „Excel“ darbaknygės formatu, turite pasirinkti formato atributo **Formato tipas** reikšmę **Excel** arba atributą **Formato tipas** palikti tuščią.</span><span class="sxs-lookup"><span data-stu-id="85e53-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="85e53-109">Jei pasirinksite **Excel**, galėsite konfigūruoti formatą, kad siunčiamas dokumentas būtų generuojami tik „Excel“ formatu.</span><span class="sxs-lookup"><span data-stu-id="85e53-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="85e53-110">Jei atributą paliksite tuščią, galėsite konfigūruoti formatą, kad siunčiamas dokumentas būtų generuojamas bet kokiu ER sistemos palaikomu formatu.</span><span class="sxs-lookup"><span data-stu-id="85e53-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="85e53-111">Norėdami sukonfigūruoti konfigūracijos ER formato komponentą, veiksmų srityje pasirinkite **Dizaino įrankis** ir ER operacijų kūrimo įrankyje atidarykite ER formato komponentą, kurį norite redaguoti.</span><span class="sxs-lookup"><span data-stu-id="85e53-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![Konfigūracijų puslapis](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="85e53-113">„Excel“ failo komponentas</span><span class="sxs-lookup"><span data-stu-id="85e53-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="85e53-114">Neautomatinis įrašas</span><span class="sxs-lookup"><span data-stu-id="85e53-114">Manual entry</span></span>

<span data-ttu-id="85e53-115">Jei siunčiamą dokumentą norite generuoti „Excel“ formatu, į sukonfigūruotą ER formatą turite įtraukti komponentą **Excel\\Failas**.</span><span class="sxs-lookup"><span data-stu-id="85e53-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Komponentas „Excel\Failas“](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="85e53-117">Norėdami nurodyti siunčiamo dokumento maketą, prie komponento **Excel\\Failas** kaip siunčiamų dokumentų šabloną pridėkite „Excel“ darbaknygę, kurios plėtinys – .xlsx.</span><span class="sxs-lookup"><span data-stu-id="85e53-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="85e53-118">Kai šabloną pridedate neautomatiniu būdu, turite naudoti [dokumento tipą](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types), kuris buvo sukonfigūruotas tam tikslui [ER parametruose](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span><span class="sxs-lookup"><span data-stu-id="85e53-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![Priedo pridėjimas prie komponento „Excel\Failas“](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="85e53-120">Jei norite nurodyti, kaip pridėtas šablonas bus pildomas vykdant sukonfigūruotą ER formatą, į komponentą **Excel\\Failas** turite įtraukti įterptuosius komponentus **Lapas**, **Diapazonas** ir **Langelis**.</span><span class="sxs-lookup"><span data-stu-id="85e53-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="85e53-121">Kiekvienas įterptasis komponentas turi būti susietas su „Excel“ įvardytuoju elementu.</span><span class="sxs-lookup"><span data-stu-id="85e53-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="85e53-122">Šablono importavimas</span><span class="sxs-lookup"><span data-stu-id="85e53-122">Template import</span></span>

<span data-ttu-id="85e53-123">Norėdami į tuščią ER formatą importuoti naują šabloną, veiksmų srities skirtuke **Importavimas** galite pasirinkti **Importuoti iš „Excel“**.</span><span class="sxs-lookup"><span data-stu-id="85e53-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="85e53-124">Šiame pavyzdyje komponentas **Excel\\Failas** bus sukurtas automatiškai, o importuotas šablonas bus pridėtas prie jo.</span><span class="sxs-lookup"><span data-stu-id="85e53-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="85e53-125">Visi būtinieji ER komponentai taip pat bus sukurti automatiškai, remiantis aptiktu „Excel“ įvardytųjų elementų sąrašu.</span><span class="sxs-lookup"><span data-stu-id="85e53-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![Importavimo pasirinkimas iš „Excel“](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="85e53-127">Jei redaguojamame ER formate norite sukurti pasirinktinį elementą **Lapas**, parinkties **Kurti „Excel“ lapo formato elementą** reikšmę nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="85e53-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="85e53-128">Lapo komponentas</span><span class="sxs-lookup"><span data-stu-id="85e53-128">Sheet component</span></span>

<span data-ttu-id="85e53-129">Komponentas **Lapas** nurodo pridėtos „Excel“ darbaknygės darbalapį, kurį reikia užpildyti.</span><span class="sxs-lookup"><span data-stu-id="85e53-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="85e53-130">„Excel“ šablone esančio darbalapio pavadinimas yra apbirėžtas šio komponento ypatybėje **Lapas**.</span><span class="sxs-lookup"><span data-stu-id="85e53-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="85e53-131">„Excel“ darbaknygėse, kuriose yra vienas darbalapis, šis komponentas yra pasirinktinis.</span><span class="sxs-lookup"><span data-stu-id="85e53-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="85e53-132">ER operacijų kūrimo įrankio skirtuke **Susiejimas** galite konfigūruoti komponento **Lapas** ypatybę **Įgalinta**, kad nustatytumėte, ar komponentas turi būti įtrauktas į sugeneruotą dokumentą.</span><span class="sxs-lookup"><span data-stu-id="85e53-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="85e53-133">Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Teisinga** arba jei nesukonfigūruota jokia išraiška, į sugeneruotą dokumentą bus įtrauktas atitinkamas darbalapis.</span><span class="sxs-lookup"><span data-stu-id="85e53-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="85e53-134">Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Klaidinga**, sugeneruotame dokumente darbalapio nebus.</span><span class="sxs-lookup"><span data-stu-id="85e53-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![Lapo komponento pavyzdys](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="85e53-136">Diapazono komponentas</span><span class="sxs-lookup"><span data-stu-id="85e53-136">Range component</span></span>

<span data-ttu-id="85e53-137">Komponentas **Diapazonas** nurodo „Excel“ diapazoną, kurį turi kontroliuoti šis ER komponentas.</span><span class="sxs-lookup"><span data-stu-id="85e53-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="85e53-138">Diapazono pavadinimas yra apbirėžtas šio komponento ypatybėje **„Excel“ diapazonas**.</span><span class="sxs-lookup"><span data-stu-id="85e53-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="85e53-139">Ypatybė **Dubliavimo kryptis** nurodo, ar diapazonas bus kartojamas sugeneruotame dokumente, ir kaip.</span><span class="sxs-lookup"><span data-stu-id="85e53-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="85e53-140">Jei ypatybės **Dubliavimo kryptis** reikšmė nustatyta kaip **Dubliavimo nėra**, atitinkamas „Excel“ diapazonas nebus kartojamas sugeneruotame dokumente.</span><span class="sxs-lookup"><span data-stu-id="85e53-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="85e53-141">Jei ypatybės **Dubliavimo kryptis** reikšmė nustatyta kaip **Vertikali**, atitinkamas „Excel“ diapazonas bus kartojamas sugeneruotame dokumente.</span><span class="sxs-lookup"><span data-stu-id="85e53-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="85e53-142">Kiekvienas dubliuojamas diapazonas „Excel“ šablone yra pateikiamas po pradiniu diapazonu.</span><span class="sxs-lookup"><span data-stu-id="85e53-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="85e53-143">Pasikartojimų skaičius apibrėžiamas duomenų šaltinio, kurio tipas – **Įrašų sąrašas** ir kuris yra susietas su šiuo ER komponentu, įrašų skaičiumi.</span><span class="sxs-lookup"><span data-stu-id="85e53-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="85e53-144">Jei ypatybės **Dubliavimo kryptis** reikšmė nustatyta kaip **Horizontali**, atitinkamas „Excel“ diapazonas bus kartojamas sugeneruotame dokumente.</span><span class="sxs-lookup"><span data-stu-id="85e53-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="85e53-145">Kiekvienas dubliuojamas diapazonas „Excel“ šablone yra pateikiamas pradinio diapazono dešinėje.</span><span class="sxs-lookup"><span data-stu-id="85e53-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="85e53-146">Pasikartojimų skaičius apibrėžiamas duomenų šaltinio, kurio tipas – **Įrašų sąrašas** ir kuris yra susietas su šiuo ER komponentu, įrašų skaičiumi.</span><span class="sxs-lookup"><span data-stu-id="85e53-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="85e53-147">Norėdami daugiau sužinoti apie horizontalų dubliavimą, atlikite veiksmus, aprašytus skyriuje [Horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas](tasks/er-horizontal-1.md).</span><span class="sxs-lookup"><span data-stu-id="85e53-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="85e53-148">Komponente **Diapazonas** gali būti kitų įterptųjų ER komponentų, kurie naudojami norint įvesti reikšmes atitinkamuose „Excel“ įvardytuose diapazonuose.</span><span class="sxs-lookup"><span data-stu-id="85e53-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="85e53-149">Jei reikšmėms įvesti naudojamas bet kuris grupės **Tekstas** komponentas, reikšmė „Excel“ diapazone įvedama kaip tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="85e53-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="85e53-150">Naudokite šį šabloną, kai norite formatuoti įvestas reikšmes pagal programoje apirbrėžtą lokalę.</span><span class="sxs-lookup"><span data-stu-id="85e53-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="85e53-151">Jei reikšmėms įvesti naudojamas grupės **Excel** komponentas **Langelis**, „Excel“ diapazone įvedama reikšmė yra duomenų tipo, kuris apibrėžiamas to komponento **Langelis** susiejimu (pavyzdžiui, **Eilutė**, **Realusis skaičius** arba **Sveikasis skaičius**).</span><span class="sxs-lookup"><span data-stu-id="85e53-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="85e53-152">Naudokite šį modelį, kad „Excel“ programa formatuotų įvestas reikšmes pagal vietinio kompiuterio, kuriame atidaromas siunčiamas dokumentas, lokalę.</span><span class="sxs-lookup"><span data-stu-id="85e53-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="85e53-153">ER operacijų kūrimo įrankio skirtuke **Susiejimas** galite konfigūruoti komponento **Diapazonas** ypatybę **Įgalinta**, kad nustatytumėte, ar komponentas turi būti įtrauktas į sugeneruotą dokumentą.</span><span class="sxs-lookup"><span data-stu-id="85e53-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="85e53-154">Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Teisinga** arba jei nesukonfigūruota jokia išraiška, sugeneruotame dokumente bus užpildytas atitinkamas diapazonas.</span><span class="sxs-lookup"><span data-stu-id="85e53-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="85e53-155">Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Klaidinga**, arba jei šis diapazonas neatitinka visų eilučių ar stulpelių, sugeneruotame dokumente atitinkamas diapazonas nebus užpildytas.</span><span class="sxs-lookup"><span data-stu-id="85e53-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="85e53-156">Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Klaidinga**, ir šis diapazonas atitinka visas eilutes ar stulpelius, sugeneruotame dokumente tos eilutės ir stulpeliai bus kaip paslėptos eilutės ir stulpeliai.</span><span class="sxs-lookup"><span data-stu-id="85e53-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="85e53-157">Langelio komponentas</span><span class="sxs-lookup"><span data-stu-id="85e53-157">Cell component</span></span>

<span data-ttu-id="85e53-158">Komponentas **Langelis** naudojamas įvardytiems „Excel“ langeliams, figūroms ir paveikslėliams užpildyti.</span><span class="sxs-lookup"><span data-stu-id="85e53-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="85e53-159">Jei norite nurodyti „Excel“ įvardytąjį objektą, kurį turi užpildyti ER komponentas **Langelis**, komponento **Langelis** ypatybėje **„Excel“ diapazonas** turite nurodyti to objekto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="85e53-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="85e53-160">ER operacijų kūrimo įrankio skirtuke **Susiejimas** galite konfigūruoti komponento **Langelis** ypatybę **Įgalinta**, kad nustatytumėte, ar objektas turi būti užpildytas sugeneruotame dokumente.</span><span class="sxs-lookup"><span data-stu-id="85e53-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="85e53-161">Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Teisinga** arba jei nesukonfigūruota jokia išraiška, sugeneruotame dokumente bus užpildytas atitinkamas objektas.</span><span class="sxs-lookup"><span data-stu-id="85e53-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="85e53-162">Šio komponento **Langelis** susiejimas nurodo reikšmę, kuri įvedama atitinkamam objektui.</span><span class="sxs-lookup"><span data-stu-id="85e53-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="85e53-163">Jei ypatybės **Įgalinta** išraiška sukonfigūruota vykdymo laiku grąžinti reikšmę **Klaidinga**, sugeneruotame dokumente atitinkamas objektas nebus užpildytas.</span><span class="sxs-lookup"><span data-stu-id="85e53-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="85e53-164">Kai komponentas **Langelis** yra sukonfigūruojamas taip, kad reikšmė būtų įvedama langelyje, jis gali būti susietas su duomenų šaltiniu, kuris grąžina primityviojo duomenų tipo reikšmę (pavyzdžiui, **Eilutė**, **Realusis skaičius** arba **Sveikasis skaičius**).</span><span class="sxs-lookup"><span data-stu-id="85e53-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="85e53-165">Šiuo atveju langelyje reikšmė įvedama kaip to paties duomenų tipo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="85e53-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="85e53-166">Kai komponentas **Langelis** yra sukonfigūruojamas taip, kad reikšmė būtų įvedama „Excel“ figūroje, jis gali būti susietas su duomenų šaltiniu, kuris grąžina primityviojo duomenų tipo reikšmę (pavyzdžiui, **Eilutė**, **Realusis skaičius** arba **Sveikasis skaičius**).</span><span class="sxs-lookup"><span data-stu-id="85e53-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="85e53-167">Šiuo atveju „Excel“ figūroje reikšmė įvedama kaip tos figūros tekstas.</span><span class="sxs-lookup"><span data-stu-id="85e53-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="85e53-168">Reikšmių, kurių duomenų tipai nėra **Eilutė**, konvertavimas į tekstą atliekamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="85e53-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="85e53-169">Galite konfigūruoti komponentą **Langelis**, kad figūra būtų užpildoma tik tais atvejais, kai palaikoma figūros teksto ypatybė.</span><span class="sxs-lookup"><span data-stu-id="85e53-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="85e53-170">Kai komponentas **Langelis** yra sukonfigūruojamas taip, kad reikšmė būtų įvedama „Excel“ paveikslėlyje, jis gali būti susietas su duomenų šaltiniu, kuris grąžina duomenų tipo **Konteineris**, atitinkančio dvejetainio formato vaizdą, reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85e53-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="85e53-171">Šiuo atveju reikšmė įvedama „Excel“ paveikslėlyje kaip vaizdas.</span><span class="sxs-lookup"><span data-stu-id="85e53-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="85e53-172">Laikoma, kad kiekvieno „Excel“ paveikslėlio ir figūros viršutinis kairysis kampas fiksuojamas prie konkretaus „Excel“ langelio arba diapazono.</span><span class="sxs-lookup"><span data-stu-id="85e53-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="85e53-173">Jei norite dubliuoti „Excel“ paveikslėlį arba figūrą, turite sukonfigūruoti langelį arba diapazoną, prie kurio jis fiksuojamas, kaip dubliuojamą langelį arba diapazoną.</span><span class="sxs-lookup"><span data-stu-id="85e53-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="85e53-174">Norėdami sužinoti daugiau, kaip įterpti paveikslėlius ir figūras, žr. [Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="85e53-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="85e53-175">Puslapio lūžio komponentas</span><span class="sxs-lookup"><span data-stu-id="85e53-175">Page break component</span></span>

<span data-ttu-id="85e53-176">Komponentas **Puslapio lūžis** priverčia programą „Excel“ pradėti naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="85e53-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="85e53-177">Šis komponentas nerekalingas, kai norite naudoti numatytąją „Excel“ puslapių kaitą, bet turite jį naudoti, jei norite, kad programa „Excel“ puslapių kaitai taikytų jūsų ER formatą.</span><span class="sxs-lookup"><span data-stu-id="85e53-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="85e53-178">Pridėto ER formato redagavimas</span><span class="sxs-lookup"><span data-stu-id="85e53-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="85e53-179">Šablono naujinimas</span><span class="sxs-lookup"><span data-stu-id="85e53-179">Update a template</span></span>

<span data-ttu-id="85e53-180">Norėdami į redaguojamą ER formatą importuoti atnaujintą šabloną, veiksmų srities skirtuke **Importavimas** galite pasirinkti **Naujinti iš „Excel‟**.</span><span class="sxs-lookup"><span data-stu-id="85e53-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="85e53-181">Šio proceso metu pasirinkto komponento **Excel\\Failas** šablonas bus pakeistas nauju šablonu.</span><span class="sxs-lookup"><span data-stu-id="85e53-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="85e53-182">Redaguojamo ER formato turinys bus sinchronizuojamas su atnaujinto ER šablono turiniu.</span><span class="sxs-lookup"><span data-stu-id="85e53-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="85e53-183">Jei redaguojamo formato ER formato komponentas nerandamas, kiekvienam „Excel“ pavadinimui bus automatiškai sukurtas naujas ER formato komponentas.</span><span class="sxs-lookup"><span data-stu-id="85e53-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="85e53-184">Neradus atitinkamo „Excel“ pavadinimo, iš redaguojamo ER formato bus panaikinti visi ER formato komponentai.</span><span class="sxs-lookup"><span data-stu-id="85e53-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="85e53-185">Jei redaguojamame ER formate norite sukurti pasirinktinį elementą **Lapas**, parinkties **Kurti „Excel“ lapo formato elementą** reikšmę nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="85e53-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="85e53-186">Jei redaguojamame ER formate iš pradžių buvo elementai **Lapas**, rekomenduojame importuojant atnaujintą šabloną parinkties **Kurti „Excel“ lapo formato elementą** reikšmę nustatyti kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="85e53-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="85e53-187">Priešingu atveju, visi įterptieji originalaus elemento **Lapas** elementai bus sukurti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="85e53-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="85e53-188">Todėl atnaujintame ER formate visi iš naujo sukurtų formato elementų susiejimai bus prarasti.</span><span class="sxs-lookup"><span data-stu-id="85e53-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![„Excel“ lapo formato elemento parinkties kūrimas dialogo lange „Naujinti iš „Excel‟](./media/er-excel-format-update-template.png)

<span data-ttu-id="85e53-190">Norėdami sužinoti daugiau apie šią funkciją, atlikite veiksmus, aprašytus skyriuje [Elektroninių ataskaitų formatų modifikavimas iš naujo pritaikant „Excel“ šablonus](modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="85e53-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="85e53-191">ER formato tikrinimas</span><span class="sxs-lookup"><span data-stu-id="85e53-191">Validate an ER format</span></span>

<span data-ttu-id="85e53-192">Kai tikrinate redaguojamą ER formatą, atliekama vientisumo patikra, siekiant įsitikinti, ar šiuo metu naudojamame „Excel“ šablone yra „Excel“ pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="85e53-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="85e53-193">Jums bus pranešta apie neatitikimus.</span><span class="sxs-lookup"><span data-stu-id="85e53-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="85e53-194">Kai kurių neatitikimų atveju bus pasiūlyta galimybė automatiškai ištaisyti problemas.</span><span class="sxs-lookup"><span data-stu-id="85e53-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![Tikrinimo klaidos pranešimas](./media/er-excel-format-validate.png)


## <a name="additional-resources"></a><span data-ttu-id="85e53-196">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="85e53-196">Additional resources</span></span>

[<span data-ttu-id="85e53-197">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="85e53-197">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="85e53-198">Konfigūracijos, skirtos ataskaitoms OPENXML formatu generuoti, kūrimas</span><span class="sxs-lookup"><span data-stu-id="85e53-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="85e53-199">Elektroninių ataskaitų formatų modifikavimas iš naujo pritaikant „Excel“ šablonus</span><span class="sxs-lookup"><span data-stu-id="85e53-199">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="85e53-200">Horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas</span><span class="sxs-lookup"><span data-stu-id="85e53-200">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="85e53-201">Vaizdų ir figūrų įterpimas generuojamuose dokumentuose naudojant ER</span><span class="sxs-lookup"><span data-stu-id="85e53-201">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="85e53-202">Elektroninių ataskaitų (ER) konfigūravimas duomenims perkelti į „Power BI“</span><span class="sxs-lookup"><span data-stu-id="85e53-202">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)