---
title: Pasirinktinių laukų naudojimas „Microsoft Dynamics 365 Project Timesheet“ mobiliojoje programoje (sistemose „iOS“ ir „Android“)
description: Šioje temoje pateikiami įprasti plėtinių naudojimo diegiant pasirinktinius laukus būdai.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174962"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="30cb1-103">Pasirinktinių laukų naudojimas „Microsoft Dynamics 365 Project Timesheet“ mobiliojoje programoje (sistemose „iOS“ ir „Android“)</span><span class="sxs-lookup"><span data-stu-id="30cb1-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30cb1-104">Šioje temoje pateikiami įprasti plėtinių naudojimo diegiant pasirinktinius laukus būdai.</span><span class="sxs-lookup"><span data-stu-id="30cb1-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="30cb1-105">Įtrauktos toliau nurodytos temos.</span><span class="sxs-lookup"><span data-stu-id="30cb1-105">The following topics are covered:</span></span>

- <span data-ttu-id="30cb1-106">Įvairių tipų duomenys, kuriuos palaiko pasirinktinių laukų sistema</span><span class="sxs-lookup"><span data-stu-id="30cb1-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="30cb1-107">Kaip rodyti tik skaitomus arba redaguojamus laukus tabelio įrašuose ir įrašyti vartotojo pateiktas vertes duomenų bazėje</span><span class="sxs-lookup"><span data-stu-id="30cb1-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="30cb1-108">Kaip rodyti tik skaitomus laukus tabelio antraštėje</span><span class="sxs-lookup"><span data-stu-id="30cb1-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="30cb1-109">Kaip integruoti kitą pasirinktinę verslo logiką, kad būtų galima įvesti numatytąsias vertes laukuose ir atlikti papildomą tikrinimą</span><span class="sxs-lookup"><span data-stu-id="30cb1-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="30cb1-110">Auditorija</span><span class="sxs-lookup"><span data-stu-id="30cb1-110">Audience</span></span>

<span data-ttu-id="30cb1-111">Ši tema skirta kūrėjams, kurie integruoja savo pasirinktinius laukus į „Microsoft Dynamics 365 Project Timesheet“ mobiliąją programą, kuri pasiekiama „Apple iOS“ ir „Google. Android“.</span><span class="sxs-lookup"><span data-stu-id="30cb1-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="30cb1-112">Daroma prielaida, kad skaitytojai yra susipažinę su X++ programavimo ir projektų tabelio funkcijomis.</span><span class="sxs-lookup"><span data-stu-id="30cb1-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="30cb1-113">Duomenų sutartis – klasė TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="30cb1-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="30cb1-114">Klasė **TSTimesheetCustomField** yra X++ duomenų sutarties klasė, kuri nurodo informaciją apie pasirinktinį tabelio funkcijos lauką.</span><span class="sxs-lookup"><span data-stu-id="30cb1-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="30cb1-115">Pasirinktinio lauko objektų sąrašai perduodami į TSTimesheetDetails duomenų sutartį ir TSTimesheetEntry duomenų sutartį, kad pasirinktiniai laukai būtų rodomi mobilioje programoje.</span><span class="sxs-lookup"><span data-stu-id="30cb1-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="30cb1-116">**TSTimesheetDetails** – tabelio antraštės sutartis.</span><span class="sxs-lookup"><span data-stu-id="30cb1-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="30cb1-117">**TSTimesheetEntry** – tabelio operacijos sutartis.</span><span class="sxs-lookup"><span data-stu-id="30cb1-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="30cb1-118">Šių objektų, kurių projekto informacija ir **timesheetLineRecId** reikšmės sutampa, grupės sudaro eilutę.</span><span class="sxs-lookup"><span data-stu-id="30cb1-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="30cb1-119">fieldBaseType (tipai)</span><span class="sxs-lookup"><span data-stu-id="30cb1-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="30cb1-120">Ypatybė **FieldBaseType**, pateikta objekte **TsTimesheetCustom** nustato lauko, kuris rodomas programoje, tipą.</span><span class="sxs-lookup"><span data-stu-id="30cb1-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="30cb1-121">Palaikomos toliau nurodytos **tipų** vertės.</span><span class="sxs-lookup"><span data-stu-id="30cb1-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="30cb1-122">Tipų vertė</span><span class="sxs-lookup"><span data-stu-id="30cb1-122">Types value</span></span> | <span data-ttu-id="30cb1-123">Tipas</span><span class="sxs-lookup"><span data-stu-id="30cb1-123">Type</span></span>              | <span data-ttu-id="30cb1-124">Pastabos</span><span class="sxs-lookup"><span data-stu-id="30cb1-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="30cb1-125">0</span><span class="sxs-lookup"><span data-stu-id="30cb1-125">0</span></span>           | <span data-ttu-id="30cb1-126">Eilutė (ir išvardijimas)</span><span class="sxs-lookup"><span data-stu-id="30cb1-126">String (and Enum)</span></span> | <span data-ttu-id="30cb1-127">Laukas rodomas kaip teksto laukas.</span><span class="sxs-lookup"><span data-stu-id="30cb1-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="30cb1-128">1</span><span class="sxs-lookup"><span data-stu-id="30cb1-128">1</span></span>           | <span data-ttu-id="30cb1-129">Sveikasis skaičius</span><span class="sxs-lookup"><span data-stu-id="30cb1-129">Integer</span></span>           | <span data-ttu-id="30cb1-130">Reikšmė rodoma kaip skaičius be dešimtainių vietų.</span><span class="sxs-lookup"><span data-stu-id="30cb1-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="30cb1-131">2</span><span class="sxs-lookup"><span data-stu-id="30cb1-131">2</span></span>           | <span data-ttu-id="30cb1-132">Tikrasis</span><span class="sxs-lookup"><span data-stu-id="30cb1-132">Real</span></span>              | <span data-ttu-id="30cb1-133">Reikšmė rodoma kaip skaičius su skaitmenimis po kablelio.</span><span class="sxs-lookup"><span data-stu-id="30cb1-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="30cb1-134">Norėdami programoje rodyti realiąją vertę kaip valiutą, naudokite ypatybę **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="30cb1-135">Galite naudoti ypatybę **numberOfDecimals** norėdami nustatyti rodomų skaitmenų po kablelio skaičių.</span><span class="sxs-lookup"><span data-stu-id="30cb1-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="30cb1-136">3</span><span class="sxs-lookup"><span data-stu-id="30cb1-136">3</span></span>           | <span data-ttu-id="30cb1-137">Data</span><span class="sxs-lookup"><span data-stu-id="30cb1-137">Date</span></span>              | <span data-ttu-id="30cb1-138">Datos formatai nustatomi pagal vartotojo parametrą **Datos, laiko ir skaičių formatas**, kuris nurodytas lango **Kalbos ir šalies / regiono nuostata** skiltyje **Vartotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="30cb1-139">4</span><span class="sxs-lookup"><span data-stu-id="30cb1-139">4</span></span>           | <span data-ttu-id="30cb1-140">Būlio logika</span><span class="sxs-lookup"><span data-stu-id="30cb1-140">Boolean</span></span>           | |
| <span data-ttu-id="30cb1-141">15</span><span class="sxs-lookup"><span data-stu-id="30cb1-141">15</span></span>          | <span data-ttu-id="30cb1-142">GUID</span><span class="sxs-lookup"><span data-stu-id="30cb1-142">GUID</span></span>              | |
| <span data-ttu-id="30cb1-143">16</span><span class="sxs-lookup"><span data-stu-id="30cb1-143">16</span></span>          | <span data-ttu-id="30cb1-144">Int64</span><span class="sxs-lookup"><span data-stu-id="30cb1-144">Int64</span></span>             | |

- <span data-ttu-id="30cb1-145">Jei ypatybė **stringOptions** nėra pateikta objekte **TSTimesheetCustomField**, laisvos formos teksto laukas pateikiamas vartotojui.</span><span class="sxs-lookup"><span data-stu-id="30cb1-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="30cb1-146">Ypatybė **stringLength** gali būti naudojama norint nustatyti maksimalų eilutės ilgį, kurį vartotojai gali įvesti.</span><span class="sxs-lookup"><span data-stu-id="30cb1-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="30cb1-147">Jei ypatybė **stringOptions** pateikiama objekte **TSTimesheetCustomField**, šie sąrašo elementai yra vienintelės vertės, kurias vartotojai gali pasirinkti naudodami parinkčių mygtukus (išrinkimo mygtukus).</span><span class="sxs-lookup"><span data-stu-id="30cb1-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="30cb1-148">Šiuo atveju eilutės laukas gali būti naudojamas kaip išvardijimo vertė vartotojui įvedant informaciją.</span><span class="sxs-lookup"><span data-stu-id="30cb1-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="30cb1-149">Norėdami į duomenų bazę įrašyti vertę kaip išvardijimą, neautomatiniu būdu susiekite eilutės vertę su išvardijimo verte prieš įrašymą į duomenų bazę naudodami eiliškumo modelį (pavyzdžių žr. tolesniame šios temos skyriuje „Eiliškumo modelio naudojimas klasėje TSTimesheetEntryService norint įrašyti tabelio įrašą iš programos į duomenų bazę).</span><span class="sxs-lookup"><span data-stu-id="30cb1-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="30cb1-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="30cb1-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="30cb1-151">Šią ypatybę galite naudoti norėdami formatuoti realiąsias vertes kaip valiutą.</span><span class="sxs-lookup"><span data-stu-id="30cb1-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="30cb1-152">Šis metodas taikomas tik kai lauko **fieldBaseType** vertė yra **Realusis**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="30cb1-153">**TSCustomFieldExtendedType:None** – formatavimas netaikomas.</span><span class="sxs-lookup"><span data-stu-id="30cb1-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="30cb1-154">**TSCustomFieldExtendedType::Currency** – formatuokite vertę kaip valiutą</span><span class="sxs-lookup"><span data-stu-id="30cb1-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="30cb1-155">Kai valiutos formatavimas aktyvus, laukas **stringValue** gali būti naudojamas norint perduoti valiutos kodą, kuris turėtų būti rodomas programoje.</span><span class="sxs-lookup"><span data-stu-id="30cb1-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="30cb1-156">Vertė yra tik skaitoma vertė.</span><span class="sxs-lookup"><span data-stu-id="30cb1-156">The value is a read-only value.</span></span>

    <span data-ttu-id="30cb1-157">Lauke **realValue** pateikiama pinigų suma, kuri turi būti įrašyta duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="30cb1-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="30cb1-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="30cb1-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="30cb1-159">Šią ypatybę galite naudoti norėdami nurodyti, kuriose programos vietose pasirinktiniai laukai turėtų būti rodomi.</span><span class="sxs-lookup"><span data-stu-id="30cb1-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="30cb1-160">**TSCustomFieldSection::Header** – laukas bus rodomas programos skiltyje **Peržiūrėti daugiau informacijos**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="30cb1-161">Šie laukai visada yra tik skaitomi.</span><span class="sxs-lookup"><span data-stu-id="30cb1-161">These fields are always read-only.</span></span>
- <span data-ttu-id="30cb1-162">**TSCustomFieldSection::Line** – laukas bus rodomas po visais parengtais naudoti eilutės laukais tabelio įrašuose.</span><span class="sxs-lookup"><span data-stu-id="30cb1-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="30cb1-163">Šie laukai gali būti redaguojami arba tik skaitomi.</span><span class="sxs-lookup"><span data-stu-id="30cb1-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="30cb1-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="30cb1-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="30cb1-165">Ši ypatybė identifikuoja lauką, kai vertės, kurias pateikia programa, yra įrašomos į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="30cb1-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="30cb1-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="30cb1-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="30cb1-167">Ši ypatybė identifikuoja lauką, kai vertės, kurias pateikia programa, yra įrašomos į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="30cb1-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="30cb1-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="30cb1-168">isEditable (NoYes)</span></span>

<span data-ttu-id="30cb1-169">Nustatykite šios ypatybės vertę **Taip**, kad nurodytumėte, jog lauką, esantį tabelio įrašo skiltyje, vartotojai galės redaguoti.</span><span class="sxs-lookup"><span data-stu-id="30cb1-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="30cb1-170">Nustatykite ypatybės vertę **Ne**, jei laukas turi būti tik skaitomas.</span><span class="sxs-lookup"><span data-stu-id="30cb1-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="30cb1-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="30cb1-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="30cb1-172">Nustatykite šios ypatybės vertę **Taip**, kad nurodytumėte, jog laukas, esantis tabelio įrašo skiltyje, turi būti privalomas.</span><span class="sxs-lookup"><span data-stu-id="30cb1-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="30cb1-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="30cb1-173">label (str)</span></span>

<span data-ttu-id="30cb1-174">Ši ypatybė nurodo žymę, kuri rodoma šalia lauko programoje.</span><span class="sxs-lookup"><span data-stu-id="30cb1-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="30cb1-175">stringOptions (List of Strings)</span><span class="sxs-lookup"><span data-stu-id="30cb1-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="30cb1-176">Ši ypatybė taikoma tik kai nustatyta parametro **fieldBaseType** vertė **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="30cb1-177">Jei **stringOptions** nustatyta, eilutės vertes, kurias galima pasirinkti naudojant parinkčių mygtukus (išrinkimo mygtukus), nurodo eilutės sąraše.</span><span class="sxs-lookup"><span data-stu-id="30cb1-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="30cb1-178">Jei eilutės nepateikiamos, laisvos formos įrašas eilutės lauke yra leistinas (pavyzdžių žr. tolesniame šios temos skyriuje „Eiliškumo modelio naudojimas klasėje TSTimesheetEntryService norint įrašyti tabelio įrašą iš programos į duomenų bazę).</span><span class="sxs-lookup"><span data-stu-id="30cb1-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="30cb1-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="30cb1-179">stringLength (int)</span></span>

<span data-ttu-id="30cb1-180">Ši ypatybė nurodo maksimalų eilutės lauko ilgį.</span><span class="sxs-lookup"><span data-stu-id="30cb1-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="30cb1-181">Ji taikoma tik kai nustatyta parametro **fieldBaseType** vertė **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="30cb1-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="30cb1-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="30cb1-183">Ši ypatybė nurodo realiosios vertės lauke rodomų skaitmenų po kablelio skaičių.</span><span class="sxs-lookup"><span data-stu-id="30cb1-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="30cb1-184">Ji taikoma tik kai nustatyta parametro **fieldBaseType** vertė **Realusis**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="30cb1-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="30cb1-185">orderSequence (int)</span></span>

<span data-ttu-id="30cb1-186">Ši ypatybė valdo tvarką, kuria pasirinktiniai laukai rodomi programoje, kai nurodytas daugiau kaip vienas pasirinktinis laukas.</span><span class="sxs-lookup"><span data-stu-id="30cb1-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="30cb1-187">Pirmiau rodomi laukai, kurių skaičiai mažesni.</span><span class="sxs-lookup"><span data-stu-id="30cb1-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="30cb1-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="30cb1-188">booleanValue (boolean)</span></span>

<span data-ttu-id="30cb1-189">Tipo **Bulio logika** laukuose ši ypatybė perduoda lauko Bulio logikos vertę tarp serverio ir programos.</span><span class="sxs-lookup"><span data-stu-id="30cb1-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="30cb1-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="30cb1-190">guidValue (guid)</span></span>

<span data-ttu-id="30cb1-191">Tipo **GUID** laukuose ši ypatybė perduoda lauko visuotinai unikalų identifikatoriaus (GUID) vertę tarp serverio ir programos.</span><span class="sxs-lookup"><span data-stu-id="30cb1-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="30cb1-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="30cb1-192">int64Value (int64)</span></span>

<span data-ttu-id="30cb1-193">Tipo **Int64** laukuose ši ypatybė perduoda lauko „int64“ vertę tarp serverio ir programos.</span><span class="sxs-lookup"><span data-stu-id="30cb1-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="30cb1-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="30cb1-194">intValue (int)</span></span>

<span data-ttu-id="30cb1-195">Tipo **Int** laukuose ši ypatybė perduoda lauko „int“ vertę tarp serverio ir programos.</span><span class="sxs-lookup"><span data-stu-id="30cb1-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="30cb1-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="30cb1-196">realValue (real)</span></span>

<span data-ttu-id="30cb1-197">Tipo **Realusis** laukuose ši ypatybė perduoda lauko realiąją vertę tarp serverio ir programos.</span><span class="sxs-lookup"><span data-stu-id="30cb1-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="30cb1-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="30cb1-198">stringValue (str)</span></span>

<span data-ttu-id="30cb1-199">Tipo **Eilutė** laukuose ši ypatybė perduoda lauko eilutės vertę tarp serverio ir programos.</span><span class="sxs-lookup"><span data-stu-id="30cb1-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="30cb1-200">Ji taip pat naudojama tipo **Realusis** laukuose, kurie formatuojami kaip valiuta.</span><span class="sxs-lookup"><span data-stu-id="30cb1-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="30cb1-201">Šiuose laukuose ypatybė naudojama perduodant valiutos kodą programai.</span><span class="sxs-lookup"><span data-stu-id="30cb1-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="30cb1-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="30cb1-202">dateValue (date)</span></span>

<span data-ttu-id="30cb1-203">Tipo **Data** laukuose ši ypatybė perduoda lauko datos vertę tarp serverio ir programos.</span><span class="sxs-lookup"><span data-stu-id="30cb1-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="30cb1-204">Pasirinktinio lauko rodymas ir įrašymas tabelio įrašo skiltyje</span><span class="sxs-lookup"><span data-stu-id="30cb1-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="30cb1-205">Toliau pateikiama mobiliosios programos tabelio įrašo kūrimo ekrano kopija.</span><span class="sxs-lookup"><span data-stu-id="30cb1-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="30cb1-206">Joje galima matyti parengtus naudoti laukus ir skiltyje Laiko įrašas pateiktą pasirinktinį pavadinimu Tikrinimo eilutė, kai tipo Antroji parinktis išvardijimo vertė jau nustatyta.</span><span class="sxs-lookup"><span data-stu-id="30cb1-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Tikrinimo eilutės pasirinktinis laukas programoje](media/timesheet-entry.jpg)



<span data-ttu-id="30cb1-208">Toliau pateikiama mobiliosios programos ekrano kopija, kurioje vartotojas pasirinko vieną iš išvardijimo parinkčių, kurios pateikiamos pasirinktiniame lauke Tikrinimo eilutė.</span><span class="sxs-lookup"><span data-stu-id="30cb1-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="30cb1-209">Šios pasirinktys yra Pirmoji parinktis ir Antroji parinktis, rodomos kaip išrinkimo mygtukai.</span><span class="sxs-lookup"><span data-stu-id="30cb1-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="30cb1-210">Šiuo metu pasirinkta antroji parinktis.</span><span class="sxs-lookup"><span data-stu-id="30cb1-210">The second option is currently selected.</span></span>

![Tikrinimo eilutės pasirinktinio lauko parinkčių mygtukai (išrinkimo mygtukai)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="30cb1-212">Lentelės TSTimesheetLine išplėtimas, kad joje būtų pasirinktinis laukas</span><span class="sxs-lookup"><span data-stu-id="30cb1-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="30cb1-213">Esant įprastam scenarijui, tikėtina, kad lentelėje TSTimesheetLine bus įrašytas pasirinktinis laukas, esantis tabelio įrašo skiltyje.</span><span class="sxs-lookup"><span data-stu-id="30cb1-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="30cb1-214">Tačiau galima naudoti kitas lenteles, jei duomenis galima nuskaityti pagal pateiktą TSTimesheetTrans įrašą arba jei nėra konkretaus įrašo konteksto (pvz., projekto parametruose laukas nustatytas kaip tik skaitomas).</span><span class="sxs-lookup"><span data-stu-id="30cb1-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="30cb1-215">Atkreipkite dėmesį, kad pasirinktiniuose laukuose neprivalo būti jokių atsarginių duomenų bazės įrašų.</span><span class="sxs-lookup"><span data-stu-id="30cb1-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="30cb1-216">Jie gali būti dinamiškai generuojami pagal X++ logiką.</span><span class="sxs-lookup"><span data-stu-id="30cb1-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="30cb1-217">Šis metodas gali būti naudingas tik skaitomų laukų scenarijuose (dinamiškai generuojamų pasirinktinių laukų verčių pavyzdžių žr. tolesniame šios temos skyriuje „Eiliškumo modelio naudojimas klasėje TSTimesheetDetails, metode buildCustomFieldListForHeader norint užpildyti tabelio informaciją“).</span><span class="sxs-lookup"><span data-stu-id="30cb1-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="30cb1-218">Toliau pateikta „Visual Studio“ programos objektų medžio ekrano kopija.</span><span class="sxs-lookup"><span data-stu-id="30cb1-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="30cb1-219">Joje rodomas lentelės TSTimesheetLine plėtinys ir laukas TestLineString, įtrauktas kaip pasirinktinis laukas.</span><span class="sxs-lookup"><span data-stu-id="30cb1-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Eilutės eilutė](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="30cb1-221">Norėdami rodyti lauką tabelio įrašo skiltyje naudokite eiliškumo modelį klasės buildCustomFieldList metode TSTimesheetSettings.</span><span class="sxs-lookup"><span data-stu-id="30cb1-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="30cb1-222">Šis kodas valdo programos lauko rodymo parametrus.</span><span class="sxs-lookup"><span data-stu-id="30cb1-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="30cb1-223">Pavyzdžiui, jis valdo lauko tipą, žymą, nustatymus, nurodančius, ar šis laukas yra privalomas ir kokioje skiltyje laukas rodomas.</span><span class="sxs-lookup"><span data-stu-id="30cb1-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="30cb1-224">Toliau pateiktame pavyzdyje rodomas eilutės laukas laiko įrašuose.</span><span class="sxs-lookup"><span data-stu-id="30cb1-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="30cb1-225">Šiame lauke yra dvi parinktys, **Pirmoji parinktis** ir **Antroji pasirinktis**, kurios pateikiamos naudojant parinkčių mygtukus (išrinkimo mygtukus).</span><span class="sxs-lookup"><span data-stu-id="30cb1-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="30cb1-226">Programos laukas yra susietas lauku **TestLineString**, kuris yra įtrauktas į lentelę TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="30cb1-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="30cb1-227">Atkreipkite dėmesį, kad galite naudoti metodą **TSTimesheetCustomField::newFromMetatdata()** norėdami supaprastinti pasirinktinių laukų ypatybių inicijavimą: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ir **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="30cb1-228">Šiuos parametrus taip pat galite nustatyti neautomatiniu būdu, kaip pageidaujate.</span><span class="sxs-lookup"><span data-stu-id="30cb1-228">You can also set these parameters manually, as you prefer.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="30cb1-229">Eiliškumo modelio naudojimas klasės TSTimesheetEntry metode buildCustomFieldListForEntry norint įvesti vertes į tabelio įrašą.</span><span class="sxs-lookup"><span data-stu-id="30cb1-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="30cb1-230">Metodas **buildCustomFieldListForEntry** naudojamas norint įvesti vertes įrašytose tabelio eilutėse mobilioje programoje.</span><span class="sxs-lookup"><span data-stu-id="30cb1-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="30cb1-231">Įrašas TSTimesheetTrans naudojamas kaip parametras.</span><span class="sxs-lookup"><span data-stu-id="30cb1-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="30cb1-232">Šio įrašo laukai gali būti naudojami norint užpildyti pasirinktinę lauko vertę programoje.</span><span class="sxs-lookup"><span data-stu-id="30cb1-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="30cb1-233">Eiliškumo modelio naudojimas klasėje TSTimesheetEntryService norint įrašyti tabelio įrašą iš programos į duomenų bazę</span><span class="sxs-lookup"><span data-stu-id="30cb1-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="30cb1-234">Norėdami įrašyti pasirinktinį lauką į duomenų bazę įprasto naudojimo sąlygomis, turite išplėsti kelis toliau nurodytus metodus.</span><span class="sxs-lookup"><span data-stu-id="30cb1-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="30cb1-235">Metodas **timesheetLineNeedsUpdating** naudojamas siekiant nustatyti, ar vartotojas pakeitė eilutės įrašą programoje, ir turi būti įrašytas į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="30cb1-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="30cb1-236">Jei našumas nėra svarbu, šį metodą galima supaprastinti, kad jis visuomet pateiktų **true**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="30cb1-237">Metodus **populateTimesheetLineFromEntryDuringCreate** ir **populateTimesheetLineFromEntryDuringUpdate** galima išplėsti, kad jie įvestų vertes duomenų bazės įraše TSTimesheetLine iš pateikto duomenų sutarties įrašo TSTimesheetEntry.</span><span class="sxs-lookup"><span data-stu-id="30cb1-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="30cb1-238">Toliau pateiktame pavyzdyje atkreipkite dėmesį, kaip duomenų bazės lauko ir įrašo lauko susiejimas atliekamas neautomatiniu būdu naudojant X++ kodą.</span><span class="sxs-lookup"><span data-stu-id="30cb1-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="30cb1-239">Metodą **populateTimesheetWeekFromEntry** taip pat galima išplėsti, jei pasirinktinis laukas, kuris yra susietas su objektu **TSTimesheetEntry**, tiro būti įrašytas į duomenų bazės lentelę TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="30cb1-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="30cb1-240">Toliau pateiktame pavyzdyje įrašoma vertė **firstOption** arba **firstOption**, kurią vartotojas pasirenka duomenų bazėje kaip neapdorotą eilutės vertę.</span><span class="sxs-lookup"><span data-stu-id="30cb1-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="30cb1-241">Jei duomenų bazės laukas yra tipo **Išvardijimas** laukas, šias vertes galima neautomatiniu būdu susieti su išvardijimo verte ir įrašyti į duomenų bazės lentelės išvardijimo lauką.</span><span class="sxs-lookup"><span data-stu-id="30cb1-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="30cb1-242">Pasirinktinio lauko rodymas tabelio antraštės skiltyje</span><span class="sxs-lookup"><span data-stu-id="30cb1-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="30cb1-243">Toliau pateikiama mobiliosios programos tabelio vartotojo peržiūra.</span><span class="sxs-lookup"><span data-stu-id="30cb1-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="30cb1-244">Mygtukas Daugiau informacijos pasirinktas viršutiniame dešiniajame kampe, kad būtų rodoma parinktis Rodyti daugiau informacijos.</span><span class="sxs-lookup"><span data-stu-id="30cb1-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Papildomos informacijos komandos peržiūra](media/show-more.png)



<span data-ttu-id="30cb1-246">Toliau pateikiama mobiliosios programos tabelio skilties Daugiau peržiūra.</span><span class="sxs-lookup"><span data-stu-id="30cb1-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="30cb1-247">Pasirinktinis laukas pavadinimu Šio tabelio naudojimo koeficientas (apskaičiuotas pasirinktinis laukas) buvo įtrauktas į tabelio antraštės skiltį.</span><span class="sxs-lookup"><span data-stu-id="30cb1-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="30cb1-248">Tik skaitoma vertė 0,667 nustatoma pasirinktiniame lauke.</span><span class="sxs-lookup"><span data-stu-id="30cb1-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Skiltis Daugiau](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="30cb1-250">Lentelės TSTimesheetTable išplėtimas, kad joje būtų pasirinktinis laukas</span><span class="sxs-lookup"><span data-stu-id="30cb1-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="30cb1-251">Esant įprastam scenarijui, tikėtina, kad pasirinktinis laukas, esantis antraštės skiltyje, bus nuskaitytas iš lentelės TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="30cb1-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="30cb1-252">Tačiau galima naudoti kitas lenteles, jei duomenis galima nuskaityti pagal pateiktą TSTimesheetTable įrašą arba jei nėra konkretaus įrašo konteksto (pvz., projekto parametruose laukas nustatytas kaip tik skaitomas).</span><span class="sxs-lookup"><span data-stu-id="30cb1-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="30cb1-253">Atkreipkite dėmesį, kad pasirinktiniuose laukuose neprivalo būti jokių atsarginių duomenų bazės įrašų.</span><span class="sxs-lookup"><span data-stu-id="30cb1-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="30cb1-254">Jie gali būti dinamiškai generuojami pagal X++ logiką.</span><span class="sxs-lookup"><span data-stu-id="30cb1-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="30cb1-255">Šis metodas nurodytas tolesniame pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="30cb1-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="30cb1-256">Antraštės skilties laukai programoje visada tik skaitomi.</span><span class="sxs-lookup"><span data-stu-id="30cb1-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="30cb1-257">Norėdami rodyti lauką antraštės skiltyje naudokite eiliškumo modelį klasės buildCustomFieldList metode TSTimesheetSettings.</span><span class="sxs-lookup"><span data-stu-id="30cb1-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="30cb1-258">Šis kodas valdo programos lauko rodymo parametrus.</span><span class="sxs-lookup"><span data-stu-id="30cb1-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="30cb1-259">Pavyzdžiui, jis valdo lauko tipą, žymą, nustatymus, nurodančius, ar šis laukas yra privalomas ir kokioje skiltyje laukas rodomas.</span><span class="sxs-lookup"><span data-stu-id="30cb1-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="30cb1-260">Toliau pateiktame pavyzdyje rodoma apskaičiuota vertė programos antraštės skiltyje.</span><span class="sxs-lookup"><span data-stu-id="30cb1-260">The following example shows a computed value in the header section in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="30cb1-261">Eiliškumo modelio naudojimas klasės TSTimesheetDetails metode buildCustomFieldListForHeader norint užpildyti tabelio informaciją</span><span class="sxs-lookup"><span data-stu-id="30cb1-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="30cb1-262">Metodas **buildCustomFieldListForHeader** naudojamas norint užpildyti tabelio antraštės informaciją mobilioje programoje.</span><span class="sxs-lookup"><span data-stu-id="30cb1-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="30cb1-263">Įrašas TSTimesheetTable naudojamas kaip parametras.</span><span class="sxs-lookup"><span data-stu-id="30cb1-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="30cb1-264">Šio įrašo laukai gali būti naudojami norint užpildyti pasirinktinę lauko vertę programoje.</span><span class="sxs-lookup"><span data-stu-id="30cb1-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="30cb1-265">Toliau pateiktame pavyzdyje nenuskaitomos jokios vertės iš duomenų bazės.</span><span class="sxs-lookup"><span data-stu-id="30cb1-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="30cb1-266">Tačiau naudojama X++ logika siekiant generuoti apskaičiuotą vertę, kuri rodoma programoje.</span><span class="sxs-lookup"><span data-stu-id="30cb1-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="30cb1-267">Kitos konfigūravimo / išplėtimo galimybės</span><span class="sxs-lookup"><span data-stu-id="30cb1-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="30cb1-268">Papildomo programos tikrinimo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="30cb1-268">Adding additional validation for the app</span></span>

<span data-ttu-id="30cb1-269">Esama tabelio funkcijos logika duomenų bazės lygiu vis tiek veiks, kaip tikėtasi.</span><span class="sxs-lookup"><span data-stu-id="30cb1-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="30cb1-270">Norėdami nutraukti įrašymo arba pateikimo operacijų užbaigimą ir rodyti konkretų klaidos pranešimą, galite įtraukti kodą **throw error("message to user")** naudodami eiliškumo modelio plėtinį.</span><span class="sxs-lookup"><span data-stu-id="30cb1-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="30cb1-271">Toliau pateikti naudingų išplečiamų metodų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="30cb1-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="30cb1-272">Jei lentelės TSTimesheetLine parametras **validateWrite** pateikia **false** tabelio eilutės įrašymo operacijos metu, mobiliojoje programoje rodomas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="30cb1-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="30cb1-273">Jei lentelės TSTimesheetTable parametras **validateSubmit** pateikia **false** tabelio pateikimo programoje metu, vartotojui rodomas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="30cb1-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="30cb1-274">Logika, pagal kurią užpildomi laukai (pvz., **Eilutės ypatybė**) naudojant **įterpimo** metodą lentelėje TSTimesheetLine, vis tiek veiks.</span><span class="sxs-lookup"><span data-stu-id="30cb1-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="30cb1-275">Parengtų naudoti laukų slėpimas ir žymėjimas tik skaitomais naudojant konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="30cb1-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="30cb1-276">Projekto parametruose galite nustatyti, kad parengti naudoti laukai būtų tik skaitomi arba paslėpti mobiliojoje programoje.</span><span class="sxs-lookup"><span data-stu-id="30cb1-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="30cb1-277">Parinktis nustatykite puslapio **Projekto valdymo ir apskaitos parametrai** skirtuko **Tabelis** skiltyje **Mobilieji tabeliai**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projekto parametrai](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="30cb1-279">Veiklų, kurias galima pasirinkti naudojant plėtinius, keitimas</span><span class="sxs-lookup"><span data-stu-id="30cb1-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="30cb1-280">Projekto veiklos, kurias galima pasirinkti, užpildomos naudojant metodus **getActivitiesForProject()** bei **getActivityQuery()** ir klasę **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="30cb1-281">Norėdami keisti šį veikimą, kad veiklos, kurias galima pasirinkti konkrečiame projekte, atitiktų jūsų verslo scenarijų, galite naudoti eiliškumo modelį.</span><span class="sxs-lookup"><span data-stu-id="30cb1-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="30cb1-282">Numatytosios projekto kategorijos įvedimas tabelio įrašuose</span><span class="sxs-lookup"><span data-stu-id="30cb1-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="30cb1-283">Numatytosios projekto kategorijos įrašymas tabelio įrašuose vykdomas trimis lygiais.</span><span class="sxs-lookup"><span data-stu-id="30cb1-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="30cb1-284">Galite naudoti eiliškumo metodą, kad koreguotumėte veikimą bet kuriame arba visuose šiuose lygiuose ir užtikrintumėte pageidaujamą veikimą.</span><span class="sxs-lookup"><span data-stu-id="30cb1-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="30cb1-285">Naudojama toliau nurodyta hierarchija.</span><span class="sxs-lookup"><span data-stu-id="30cb1-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="30cb1-286">Programa bando pateikti numatytąją kategoriją iš projekto ištekliaus.</span><span class="sxs-lookup"><span data-stu-id="30cb1-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="30cb1-287">Ši numatytoji kategorija nustatyta klasės **TSTimesheetSettingsService** metoduose **getCurrentUserResource** ir **getDelegatedResourcesForCurrentUser**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="30cb1-288">Jei numatytoji kategorija nepateikta projekto išteklių lygiu, programa bandys nuskaityti ją iš projekto veiklos.</span><span class="sxs-lookup"><span data-stu-id="30cb1-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="30cb1-289">Ši numatytoji kategorija nustatoma klasės **TSTimesheetProjectService** metode **getActivitiesForProject**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="30cb1-290">Jei numatytoji kategorija nepateikta projekto veiklos lygiu, numatytoji kategorija nuskaitoma projekto parametrų.</span><span class="sxs-lookup"><span data-stu-id="30cb1-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="30cb1-291">Ši numatytoji kategorija nustatoma klasės **TSTimesheetProjectService** metode **getProjectDetailsbyRule**.</span><span class="sxs-lookup"><span data-stu-id="30cb1-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
