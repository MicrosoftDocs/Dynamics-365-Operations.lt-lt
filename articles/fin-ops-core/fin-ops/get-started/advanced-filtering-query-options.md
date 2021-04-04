---
title: Išplėstinio filtravimo ir užklausų sintaksė
description: Šioje temoje aprašomos filtravimo ir užklausos parinktys, kurios pasiekiamos naudojant dialogo langą Išplėstinis filtravimas / rūšiavimas arba filtro srityje esantį atitikimo operatorių, arba tinklelio stulpelių antraščių filtrus.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15805e24c46603afd34d40c5f94c1422b01cab4c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566071"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="4d8bd-103">Išplėstinio filtravimo ir užklausų sintaksė</span><span class="sxs-lookup"><span data-stu-id="4d8bd-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d8bd-104">Šioje temoje aprašomos filtravimo ir užklausos parinktys, kurios pasiekiamos naudojant dialogo langą Išplėstinis filtravimas / rūšiavimas arba filtro srityje esantį **atitikimo** operatorių, arba tinklelio stulpelių antraščių filtrus.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-104">This topic describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="4d8bd-105">Išplėstinės užklausos sintaksė</span><span class="sxs-lookup"><span data-stu-id="4d8bd-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4d8bd-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="4d8bd-106">Syntax</span></span></th>
<th><span data-ttu-id="4d8bd-107">Simbolio aprašymas</span><span class="sxs-lookup"><span data-stu-id="4d8bd-107">Character description</span></span></th>
<th><span data-ttu-id="4d8bd-108">aprašymas</span><span class="sxs-lookup"><span data-stu-id="4d8bd-108">Description</span></span></th>
<th><span data-ttu-id="4d8bd-109">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4d8bd-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4d8bd-110"><em>vertė</em></span><span class="sxs-lookup"><span data-stu-id="4d8bd-110"><em>value</em></span></span></td>
<td><span data-ttu-id="4d8bd-111">Lygi įvestai vertei</span><span class="sxs-lookup"><span data-stu-id="4d8bd-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="4d8bd-112">Įveskite vertę, kurią norite rasti.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="4d8bd-113">Įvedus <strong>Smith</strong> randama &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-114">!<em>vertė</em> (šauktuko ženklas)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="4d8bd-115">Nelygi įvestai vertei</span><span class="sxs-lookup"><span data-stu-id="4d8bd-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="4d8bd-116">Prieš vertę, kurią norite pašalinti, įveskite šauktuko ženklą.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="4d8bd-117">Įvedus <strong>!Smith</strong> randamos visos vertės, išskyrus &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-118"><em>„Nuo“ vertė</em>..<em>„Iki“ vertė</em> (dvigubas taškas)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="4d8bd-119">Vertė, esanti tarp dviejų įvestų verčių, atskirtų dvigubais taškais.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="4d8bd-120">Įveskite vertę Nuo, tada du taškus, tada vertę Iki.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="4d8bd-121">Įvedus <strong>1..10</strong> randamos visos vertės nuo 1 iki 10.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="4d8bd-122">Tačiau eilutės lauke <strong>A..C</strong> atsiranda visos vertės, prasidedančios &quot;A&quot; ir &quot;B&quot;, ir vertės, tiksliai lygios &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="4d8bd-123">Pvz., pagal šią užklausą nebus rasta &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="4d8bd-124">Norėdami surasti visas vertes įskaitytinai nuo &quot;A<em>&quot; iki &quot;C</em>&quot;, įrašykite <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-125">..<em>vertė</em> (dvigubas taškas)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="4d8bd-126">Mažesnė nei įvesta vertė arba lygi įvestai vertei</span><span class="sxs-lookup"><span data-stu-id="4d8bd-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="4d8bd-127">Įveskite du taškus, tada vertę.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="4d8bd-128">Įvedus <strong>..1000</strong> randamas bet kuris skaičius, mažesnis nei 1000 arba lygus 1000, pvz., &quot;100&quot;, &quot;999,95&quot; ir &quot;1000&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-129"><em>vertė</em>..</span><span class="sxs-lookup"><span data-stu-id="4d8bd-129"><em>value</em>..</span></span> <span data-ttu-id="4d8bd-130">dvigubas laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4d8bd-130">(double period)</span></span></td>
<td><span data-ttu-id="4d8bd-131">Didesnė nei įvesta vertė arba lygi įvestai vertei</span><span class="sxs-lookup"><span data-stu-id="4d8bd-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="4d8bd-132">Įveskite vertę, tada du taškus.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="4d8bd-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="4d8bd-133"><strong>1000..</strong></span></span> <span data-ttu-id="4d8bd-134">randamas bet kuris skaičius, didesnis nei 1000 arba lygus 1000, pvz., &quot;1000&quot;, &quot;1000,01&quot; ir &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-135">&gt;<em>vertė</em> („daugiau nei“ ženklas)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="4d8bd-136">Didesnė už įvestą vertę</span><span class="sxs-lookup"><span data-stu-id="4d8bd-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="4d8bd-137">Įveskite „daugiau nei“ ženklą (<strong>&gt;</strong>), tada – vertę.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="4d8bd-138">Įvedus <strong>&gt; 1000</strong> randamas bet kuris skaičius, kuris yra didesnis nei 1000, pvz., &quot;1000,01&quot;, &quot;20 000&quot;, and &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-139">&lt;<em>vertė</em> („mažiau nei“ ženklas)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="4d8bd-140">Mažesnė už įvestą vertę</span><span class="sxs-lookup"><span data-stu-id="4d8bd-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="4d8bd-141">Įveskite „mažiau nei“ ženklą (<strong>&lt;</strong>), tada – vertę.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="4d8bd-142">Įvedus <strong>&lt; 1000</strong> randamas bet kuris skaičius, kuris yra mažesnis nei 1000, pvz., &quot;999,99&quot;, &quot;1&quot; ir &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-143"><em>vertė</em>\* (žvaigždutė)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="4d8bd-144">Prasideda įvesta verte</span><span class="sxs-lookup"><span data-stu-id="4d8bd-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="4d8bd-145">Įveskite pradžios vertę, tada – žvaigždutę (<strong>\*</strong>).</span><span class="sxs-lookup"><span data-stu-id="4d8bd-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="4d8bd-146">Įvedus <strong>S\*</strong> randama bet kuri eilutė, prasidedanti &quot;S&quot;, pvz.,  &quot;Stockholm&quot;, &quot;Sydney&quot; ir &quot;San Francisco&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-147">\*<em>vertė</em> (žvaigždutė)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="4d8bd-148">Baigiasi įvesta verte</span><span class="sxs-lookup"><span data-stu-id="4d8bd-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="4d8bd-149">Įveskite žvaigždutę ir pabaigos vertę.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="4d8bd-150">Įvedus <strong>\*east</strong> randamos visos eilutės, besibaigiančios &quot;east&quot;, pvz., &quot;Northeast&quot; ir &quot;Southeast&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-151">*<em>vertė</em>* (žvaigždutė)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="4d8bd-152">Įeina įvesta vertė</span><span class="sxs-lookup"><span data-stu-id="4d8bd-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="4d8bd-153">Įveskite žvaigždutę, tada vertę ir kitą žvaigždutę.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="4d8bd-154">Įvedus <strong>*th*</strong> randamos visos eilutės, kuriose yra &quot;th&quot;, pvz. &quot;Northeast&quot; ir &quot;Southeast&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-155">?</span><span class="sxs-lookup"><span data-stu-id="4d8bd-155">?</span></span> <span data-ttu-id="4d8bd-156">klaustuko ženklas</span><span class="sxs-lookup"><span data-stu-id="4d8bd-156">(question mark)</span></span></td>
<td><span data-ttu-id="4d8bd-157">Turi vieną ar daugiau nežinomų simbolių</span><span class="sxs-lookup"><span data-stu-id="4d8bd-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="4d8bd-158">Įveskite klaustuko ženklą nežinomo vertės simbolio vietoje.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="4d8bd-159">Įvedus <strong>Sm?th</strong> randama &quot;Smith&quot; ir &quot;Smyth&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-160"><em>vertė</em>,<em>vertė</em> (kablelis)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="4d8bd-161">Ieškoma verčių, atskirtų kableliais</span><span class="sxs-lookup"><span data-stu-id="4d8bd-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="4d8bd-162">Įveskite visus kriterijus ir atskirkite juos kableliais.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="4d8bd-163"><strong>Įvedus A, D, F, G</strong> surandama būtent &quot;A&quot;, &quot;D&quot;, &quot;F&quot; ir &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="4d8bd-164"><strong>Įvedus 10, 20, 30, 100</strong> surandama būtent &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-165">"" (dvi dvigubos kabutės)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="4d8bd-166">Tuščios reikšmės gretinimas</span><span class="sxs-lookup"><span data-stu-id="4d8bd-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="4d8bd-167">Jei norite tame lauke filtruodami rasti tuščias reikšmes , iš eilės įveskite dvi dvigubas kabutes.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="4d8bd-168">Naudojant dvi iš eilės įvestas dvigubas kabutes (<strong>""</strong>), randamos eilutės, kuriose dabartinio stulpelio reikšmių nėra.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-169">(<span class="code">„Finance and Operations” užklausa</span>) („Finance and Operations” užklausa skliausteliuose)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-169">(<span class="code">Finance and Operations query</span>) (Finance and Operations query between parentheses)</span></span></td>
<td><span data-ttu-id="4d8bd-170">Ieškoma užklausos, atitinkančios nustatytą</span><span class="sxs-lookup"><span data-stu-id="4d8bd-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="4d8bd-171">Įveskite užklausą kaip SQL sakinį tarp skliaustelių naudodami „Finance and Operations” užklausos kalbą.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-171">Type a query as an SQL statement between parentheses using the Finance and Operations query language.</span></span></td>
  <td><span data-ttu-id="4d8bd-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span><span class="sxs-lookup"><span data-stu-id="4d8bd-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span></span><br><br> 
       <span data-ttu-id="4d8bd-173">tai pavyzdys sintaksės, naudojamos šakninio duomenų šalitinio lauko ir kito duomenų šaltinio (skirto puslapiui Visi klientai) lauko filtro sąlygai</span><span class="sxs-lookup"><span data-stu-id="4d8bd-173">as an example of syntax for a filter condition on a field from the root datasource as well as a field from a different datasource (for the All customers page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-174">A</span><span class="sxs-lookup"><span data-stu-id="4d8bd-174">T</span></span></td>
<td><span data-ttu-id="4d8bd-175">Šiandienos data</span><span class="sxs-lookup"><span data-stu-id="4d8bd-175">Today's date</span></span></td>
<td><span data-ttu-id="4d8bd-176">Įveskite <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-176">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="4d8bd-177"><strong>T</strong> atitinka šiandienos datą.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-177"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> metodas tarp skliaustelių)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="4d8bd-179">Ieškoma vertė arba diapazonas verčių, kurias nurodo <strong>SysQueryRangeUtil</strong> metodo parametras</span><span class="sxs-lookup"><span data-stu-id="4d8bd-179">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="4d8bd-180">Įveskite <strong>SysQueryRangeUtil</strong> metodą su parametrais, nurodančiais vertę arba verčių diapazoną.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-180">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="4d8bd-181">Spustelėkite <strong>Gautinos sumos</strong> &gt; <strong>Sąskaitos faktūros</strong> &gt; <strong>Atviros kliento SF</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-181">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="4d8bd-182">Paspauskite Ctrl + Shift + F3, kad atidarytumėte puslapį <strong>Užklausa</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-182">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="4d8bd-183">Skirtuke <strong>Diapazonas</strong> spustelėkite <strong>Pridėti</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-183">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="4d8bd-184">Lauke <strong>Lentelė</strong> pasirinkite <strong>Atviros kliento operacijos</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-184">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="4d8bd-185">Lauke <strong>Laukas</strong> pasirinkite <strong>Terminas</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-185">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="4d8bd-186">Lauke <strong>Kriterijai</strong> įveskite <strong>(yearRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-186">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="4d8bd-187">Spustelėkite <strong>GERAI</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-187">Click <strong>OK</strong>.</span></span> <span data-ttu-id="4d8bd-188">Sąrašo puslapis atnaujinamas ir pateikiamos įvestus kriterijus atitinkančios SF.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-188">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="4d8bd-189">Šiame pavyzdyje sąrašo puslapyje rodomos SF, kurias reikėjo apmokėti ankstesniais dvejais metais.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-189">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="4d8bd-190">Jei reikia papildomos informacijos apie <strong>SysQueryRangeUtil</strong> datos metodus, žr. lentelę kitame skyriuje, kuriame pateikta ir keletas pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-190">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="4d8bd-191">Išplėstinės datos užklausos, kurios naudoja SysQueryRangeUtil metodus</span><span class="sxs-lookup"><span data-stu-id="4d8bd-191">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4d8bd-192">Metodas</span><span class="sxs-lookup"><span data-stu-id="4d8bd-192">Method</span></span></th>
<th><span data-ttu-id="4d8bd-193">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="4d8bd-193">Description</span></span></th>
<th><span data-ttu-id="4d8bd-194">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4d8bd-194">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4d8bd-195">Diena (_relativeDays = 0)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-195">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="4d8bd-196">Randama data, susijusi su seanso data.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-196">Find a date relative to the session date.</span></span> <span data-ttu-id="4d8bd-197">Teigiamos vertės reiškia būsimas datas, o neigiamos vertės reiškia praeities datas.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-197">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4d8bd-198"><strong>Rytojaus diena</strong> – įveskite <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-198"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="4d8bd-199"><strong>Šiandiena</strong> – įveskite <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-199"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="4d8bd-200"><strong>Vakar diena</strong> – įveskite <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-200"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-201">DayRange (_relativeDaysFrom = 0, _relativeDaysTo = 0)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="4d8bd-202">Randamos datos, susijusios su seanso data.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-202">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="4d8bd-203">Teigiamos vertės reiškia būsimas datas, o neigiamos vertės reiškia praeities datas.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-203">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4d8bd-204"><strong>Pastarosios 30 dienų</strong> – įveskite <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-204"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="4d8bd-205"><strong>Ankstesnės 30 dienų ir ateinančios 30 dienų</strong> – įveskite <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-205"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-206">GreaterThanDate (_relativeDays = 0) GreaterThanUtcDate (_relativeDays = 0)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="4d8bd-207">Randamos visos datos, kurios yra vėlesnės nei nurodytos santykinės datos.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-207">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4d8bd-208"><strong>Daugiau nei 30 dienų nuo šiol</strong> – įveskite <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-208"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-209">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="4d8bd-209">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="4d8bd-210">Randami visi datos / laiko įrašai, kurie yra vėlesni už dabartinį laiką.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-210">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4d8bd-211"><strong>Visos būsimos datos / laikai</strong> – įveskite <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-211"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="4d8bd-213">Randamos visos datos, kurios yra ankstesnės nei nurodyta santykinė data.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-213">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4d8bd-214"><strong>Mažiau nei septynios dienas nuo šiol</strong> – įveskite <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-214"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-215">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="4d8bd-215">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="4d8bd-216">Randami visi datos / laiko įrašai, kurie yra ankstesni už dabartinį laiką.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-216">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4d8bd-217"><strong>Visos praeities datos / laikai</strong> – įveskite <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-217"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-218">MonthRange (_relativeFrom = 0, _relativeTo = 0)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="4d8bd-219">Randamos datos pagal mėnesius, susijusius su dabartiniu mėnesiu.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-219">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4d8bd-220"><strong>Du praėję mėnesiai</strong> – įveskite <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-220"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="4d8bd-221"><strong>Ateinantys trys mėnesiai</strong> – įveskite <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-221"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4d8bd-222">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="4d8bd-222">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="4d8bd-223">Randamos datos pagal metus, susijusius su dabartiniais metais.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-223">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="4d8bd-224"><strong>Ateinantys metai</strong> – įveskite <strong>(YearRange(0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-224"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="4d8bd-225"><strong>Ankstesni metai</strong> – įveskite <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="4d8bd-225"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]