---
title: Inžineriniai atributai ir inžinerinio atributo paieška
description: Šioje temoje paaiškinama, kaip galite naudoti inžinerinius atributus norėdami nurodyti visas nestandartines savybes ir užtikrinti, kad visi produkto pagrindiniai duomenys būtų registruoti sistemoje. Jis taip pat paaiškina, kaip galite naudoti inžinerinį atributo paiešką tam, kad nesunkiai rastumėte produktus pagal jų registruotas savybes.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5a4f31af3f76c1af6a0f5546955e810bd1cca375
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434051"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a><span data-ttu-id="be0a7-104">Inžineriniai atributai ir inžinerinio atributo paieška</span><span class="sxs-lookup"><span data-stu-id="be0a7-104">Engineering attributes and engineering attribute search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be0a7-105">Norėdami, kad visi produkto pagrindiniai duomenys būtų registruoti sistemoje, turėtumėte naudoti inžinerinius atributus tam, kad nurodytumėte visas nesatandartines savybes.</span><span class="sxs-lookup"><span data-stu-id="be0a7-105">To ensure that all product master data can be registered in the system, you should use engineering attributes to specify all non-standard characteristics.</span></span> <span data-ttu-id="be0a7-106">Tuomet galite naudoti inžinerinį atributo paiešką tam, kad nesunkiai rastumėte produktus pagal jų registruotas savybes.</span><span class="sxs-lookup"><span data-stu-id="be0a7-106">You can then use engineering attribute search to easily find products, based on those registered characteristics.</span></span>

## <a name="engineering-attributes"></a><span data-ttu-id="be0a7-107">Inžinerijos atributai</span><span class="sxs-lookup"><span data-stu-id="be0a7-107">Engineering attributes</span></span>

<span data-ttu-id="be0a7-108">Dažniausiai, inžinerijos produktai turi daug savybių ir ypatybių, kurias turite apimti.</span><span class="sxs-lookup"><span data-stu-id="be0a7-108">Typically, engineering products have many characteristics and properties that you must capture.</span></span> <span data-ttu-id="be0a7-109">Nepaisant to, kad galite registruoti kai kurias savybes naudodami standartinius produkto laukelius, galite taip pat kurti naujas inžinerines ypatybes, kaip reikia.</span><span class="sxs-lookup"><span data-stu-id="be0a7-109">Although you can register some of the properties by using the standard product fields, you can also create new engineering properties as required.</span></span> <span data-ttu-id="be0a7-110">Galite nurodyti savo *inžinerinius atributus* ir padaryti juos produkto sąvokos dalimi.</span><span class="sxs-lookup"><span data-stu-id="be0a7-110">You can define your own *engineering attributes* and make them part of the product definition.</span></span>

### <a name="create-engineering-attributes-and-attribute-types"></a><span data-ttu-id="be0a7-111">Sukurkite inžinerinius atributus ir jo tipus</span><span class="sxs-lookup"><span data-stu-id="be0a7-111">Create engineering attributes and attribute types</span></span>

<span data-ttu-id="be0a7-112">Bet kuris inžinerinis atributas turi priklausyti *atributo tipui*.</span><span class="sxs-lookup"><span data-stu-id="be0a7-112">Each engineering attribute must belong to an *attribute type*.</span></span> <span data-ttu-id="be0a7-113">Toks reikalavimas egzistuoja dėl to, kad visi inžineriniai atributai turi turėti *duomenų tipą*, kuris nustato jo turimus večių tipus.</span><span class="sxs-lookup"><span data-stu-id="be0a7-113">This requirement exists because each engineering attribute must have a *data type* that defines the types of values that it can hold.</span></span> <span data-ttu-id="be0a7-114">Inžinerinio atributo tipas gali būti standartinis tipas (toks kaip laisvas tekstas, integruojantis ar dešimtainė) arba tinkintas tipas (toks kaip tekstas turinti konkretų verčių rinkinį, iš kurių rinktis).</span><span class="sxs-lookup"><span data-stu-id="be0a7-114">An engineering attribute type can be a standard type (such as free text, integer, or decimal) or a custom type (such as text that has a specific set of values to select from).</span></span> <span data-ttu-id="be0a7-115">Galite dar kartą panaudoti kiekvieną atributo tipą su bet kuriuo inžinerinių atributų numeriu.</span><span class="sxs-lookup"><span data-stu-id="be0a7-115">You can reuse each attribute type with any number of engineering attributes.</span></span>

#### <a name="set-up-engineering-attribute-types"></a><span data-ttu-id="be0a7-116">Nustatykite inžinerijos atributo tipą</span><span class="sxs-lookup"><span data-stu-id="be0a7-116">Set up engineering attribute types</span></span>

<span data-ttu-id="be0a7-117">Norėdami peržiūrėti, sukurti ar redaguoti inžinerinių pakeitimų užklausą, atlikite vieną iš šių žingsnių.</span><span class="sxs-lookup"><span data-stu-id="be0a7-117">To view, create, or edit an engineering attribute type, follow these steps.</span></span>

1. <span data-ttu-id="be0a7-118">Eikite į **Inžinerijos keitimo valdymą \> Nustatymus \> Atributai \> Atributo tipai**.</span><span class="sxs-lookup"><span data-stu-id="be0a7-118">Go to **Engineering change management \> Setup \> Attributes \> Attribute types**.</span></span>
1. <span data-ttu-id="be0a7-119">Pasirinkite esamą atributo tipą sąrašo juostoje arba rinkitės **Naujas** tam, kad sukurtumėte naują atributo tipą.</span><span class="sxs-lookup"><span data-stu-id="be0a7-119">Select an existing attribute type in the list pane, or select **New** on the Action Pane to create a new attribute type.</span></span>
1. <span data-ttu-id="be0a7-120">Užpildykite toliau nurodytus laukus:</span><span class="sxs-lookup"><span data-stu-id="be0a7-120">Set the following fields:</span></span>

    - <span data-ttu-id="be0a7-121">**Atributo tipo pavadinimas** – Įveskite kainų profilį aprašantį tipą.</span><span class="sxs-lookup"><span data-stu-id="be0a7-121">**Attribute type name** – Enter a name for the attribute type.</span></span>
    - <span data-ttu-id="be0a7-122">**Tipas** – Pasirinkite standartinį duomenų tipą (*Valiuta*, *Data ir laikas*, *Dešimtainė*, *Integruojantis*, *Tekstas*, *Boolean* ar *Nuoroda*).</span><span class="sxs-lookup"><span data-stu-id="be0a7-122">**Type** – Select a standard data type (*Currency*, *DateTime*, *Decimal*, *Integer*, *Text*, *Boolean*, or *Reference*).</span></span>
    - <span data-ttu-id="be0a7-123">**Fiksuotas sąrašas** – Ši parinktis prieinama tik jei nustatėte **Tipo** laukelį į *Tekstas*.</span><span class="sxs-lookup"><span data-stu-id="be0a7-123">**Fixed list** – This option is available only if you set the **Type** field to *Text*.</span></span> <span data-ttu-id="be0a7-124">Nustatykite jį į *Taip* tam, kad nustatytumėte konkrečias vertes šio tipo atributams.</span><span class="sxs-lookup"><span data-stu-id="be0a7-124">Set it to *Yes* to define specific values for attributes of this type.</span></span> <span data-ttu-id="be0a7-125">Tokiu atveju, iškrentantis meniu bus sukurtas.</span><span class="sxs-lookup"><span data-stu-id="be0a7-125">In this case, a drop-down list will be created.</span></span> <span data-ttu-id="be0a7-126">Naudojate **Vertės** „FastTab“ siekiant sukurti vertes prieinamas šiam atributo tipui.</span><span class="sxs-lookup"><span data-stu-id="be0a7-126">You use the **Value** FastTab to establish the values that are available for this attribute type.</span></span> <span data-ttu-id="be0a7-127">Nustatykite šią parinktį į *Ne* norėdami leisti vartotojams įvesti bet kurią vertę.</span><span class="sxs-lookup"><span data-stu-id="be0a7-127">Set this option to *No* to allow users to enter any value.</span></span> <span data-ttu-id="be0a7-128">Tokiu atveju, įvesties laukelis bus sukurtas.</span><span class="sxs-lookup"><span data-stu-id="be0a7-128">In this case, an input field will be created.</span></span>
    - <span data-ttu-id="be0a7-129">**Vertės intervalas** – Ši parinktis prieinama tik jei nustatėte **Tipo** laukelį į *Integruojantis*, *Dešimtainė* ar *Valiuta*.</span><span class="sxs-lookup"><span data-stu-id="be0a7-129">**Value range** – This option is available only if you set the **Type** field to *Integer*, *Decimal*, or *Currency*.</span></span> <span data-ttu-id="be0a7-130">Nustatykite jį į *Taip* norėdami sukurti minimalias ir maksimalias vertes, kurios bus priimtos šio tipo atributams.</span><span class="sxs-lookup"><span data-stu-id="be0a7-130">Set it to *Yes* to establish minimum and maximum values that will be accepted for attributes of this type.</span></span> <span data-ttu-id="be0a7-131">Naudojate **Intervalo** „FastTab“ norėdami sukurti minimalias ir maks. vertes bei (valiutai) valiutą tiakomą jūsų įvestiems apribojimams.</span><span class="sxs-lookup"><span data-stu-id="be0a7-131">You use the **Range** FastTab to establish the minimum and maximum values, and (for currency) the currency that applies for the limits that you entered.</span></span> <span data-ttu-id="be0a7-132">Nustatykite šią parinktį į *Ne* norėdami priimti bet kurią vertę.</span><span class="sxs-lookup"><span data-stu-id="be0a7-132">Set this option to *No* to accept any value.</span></span> 
    - <span data-ttu-id="be0a7-133">**Matavimo vienetas** – Šis laukelis prieinamas tik jei nustatėte **Tipo** laukelį į *Integruojantis* ar *Dešimtainis*.</span><span class="sxs-lookup"><span data-stu-id="be0a7-133">**Unit of measure** – This field is available only if you set the **Type** field to *Integer* or *Decimal*.</span></span> <span data-ttu-id="be0a7-134">Pasirinkite matavimo vienetą taikomą šiam atributo tipui.</span><span class="sxs-lookup"><span data-stu-id="be0a7-134">Select the unit of measure that applies for this attribute type.</span></span> <span data-ttu-id="be0a7-135">Jei jokio vieneto nereikia, palikite laukelį tuščią.</span><span class="sxs-lookup"><span data-stu-id="be0a7-135">If no unit is required, leave this field blank.</span></span>

#### <a name="set-up-engineering-attributes"></a><span data-ttu-id="be0a7-136">Nustatykite inžinerijos atributus</span><span class="sxs-lookup"><span data-stu-id="be0a7-136">Set up engineering attributes</span></span>

<span data-ttu-id="be0a7-137">Norėdami peržiūrėti, sukurti ar redaguoti inžinerinių pakeitimų užklausą, atlikite vieną iš šių žingsnių.</span><span class="sxs-lookup"><span data-stu-id="be0a7-137">To view, create, or edit an engineering attribute, follow these steps.</span></span>

1. <span data-ttu-id="be0a7-138">Eikite į **Inžinerijos keitimo valdymą \> Nustatymus \> Atributai \> Inžineriniai atributai**.</span><span class="sxs-lookup"><span data-stu-id="be0a7-138">Go to **Engineering change management \> Setup \> Attributes \> Engineering attributes**.</span></span>
1. <span data-ttu-id="be0a7-139">Pasirinkite esamą atributo tipą sąrašo juostoje arba rinkitės **Naujas** tam, kad sukurtumėte naują atributo tipą.</span><span class="sxs-lookup"><span data-stu-id="be0a7-139">Select an existing attribute in the list pane, or select **New** on the Action Pane to create a new attribute.</span></span>
1. <span data-ttu-id="be0a7-140">Užpildykite toliau nurodytus laukus:</span><span class="sxs-lookup"><span data-stu-id="be0a7-140">Set the following fields:</span></span>

    - <span data-ttu-id="be0a7-141">**Pavadinimas** – Įveskite kainų profilį aprašantį atributą.</span><span class="sxs-lookup"><span data-stu-id="be0a7-141">**Name** – Enter a name for the attribute.</span></span> <span data-ttu-id="be0a7-142">Šis vardas pasirodo tik **Inžinerijos atributų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="be0a7-142">This name appears only on the **Engineering attributes** page.</span></span> <span data-ttu-id="be0a7-143">Visu kitur sistemoje, vertė **Draugiškas pavadinimas** laukelis dažniausiai rodomas siekiant nustatyti atributą.</span><span class="sxs-lookup"><span data-stu-id="be0a7-143">Everywhere else in the system, the value of the **Friendly name** field is usually shown to identify the attribute.</span></span>
    - <span data-ttu-id="be0a7-144">**Atributo tipas** – Pasirinkite atributo tipą, kurį nustatėte ankstesniame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="be0a7-144">**Attribute type** – Select an attribute type that you defined in the previous section.</span></span>
    - <span data-ttu-id="be0a7-145">**Draugiškas pavadinimas** – Įveskite pavadinimą, kuris nustato atributą sistemoje (išskyrus **Inžinerijos atributų** puslapį).</span><span class="sxs-lookup"><span data-stu-id="be0a7-145">**Friendly name** – Enter a name that will identify the attribute in the system (except on the **Engineering attributes** page).</span></span> 
    - <span data-ttu-id="be0a7-146">**Aprašas** – Įveskite atributo aprašą.</span><span class="sxs-lookup"><span data-stu-id="be0a7-146">**Description** – Enter a description of the attribute.</span></span>
    - <span data-ttu-id="be0a7-147">**Pagalbos tekstas** – Įveskite pagalbos tekstą, kuris kitiems vartotojams sako, kam skirtas atributas.</span><span class="sxs-lookup"><span data-stu-id="be0a7-147">**Help text** – Enter Help text that tells other users what the attribute is for.</span></span>
    - <span data-ttu-id="be0a7-148">**Nustatytoji vertė** – Įveskite nustatytąją vertę atributui.</span><span class="sxs-lookup"><span data-stu-id="be0a7-148">**Default value** – Enter a default value for the attribute.</span></span> <span data-ttu-id="be0a7-149">Parinktys yra rodomos priklausomai nuo atributo tipo, kurį rinkotės.</span><span class="sxs-lookup"><span data-stu-id="be0a7-149">The options that are presented depend on the attribute type that you selected.</span></span>
    - <span data-ttu-id="be0a7-150">**Valiuta** – Jei atributo tipas, kurį pasirinkote yra valiuta, pasirinkite valiutą, kurią atributas priims ir rodys vertes.</span><span class="sxs-lookup"><span data-stu-id="be0a7-150">**Currency** – If the attribute type that you selected is a currency, select the currency that the attribute will accept and show values in.</span></span>

1. <span data-ttu-id="be0a7-151">Jei atributo tipas, kurį pasirinkote yra integruojantis ar dešimtainė, **Intervalas** „FastTab“ yra rodomas.</span><span class="sxs-lookup"><span data-stu-id="be0a7-151">If the attribute type that you selected is an integer or a decimal, the **Range** FastTab is shown.</span></span> <span data-ttu-id="be0a7-152">Šiame „FastTab“, nustatykite tolesnius laukelius, kaip būtina:</span><span class="sxs-lookup"><span data-stu-id="be0a7-152">On this FastTab, set the following fields as required:</span></span>

    - <span data-ttu-id="be0a7-153">**Paklaidos veiksmas** – Nustatykite, kaip sistema turi atsakyti, jei vartotojas įveda vertę ne nustatytame intervale.</span><span class="sxs-lookup"><span data-stu-id="be0a7-153">**Tolerance action** – Select how the system should respond if a user enters a value outside the specified range.</span></span> <span data-ttu-id="be0a7-154">Jei pasirinkote *Įspėjimas*, įspėjimas rodo, tačiau vartotojas gali įrašyti vertę.</span><span class="sxs-lookup"><span data-stu-id="be0a7-154">If you select *Warning*, a warning is shown, but the user can save the value.</span></span> <span data-ttu-id="be0a7-155">Jei pasirenkate *Neleidžiama*, įspėjimas rodomas ir vertė negali būti įrašyta kol vartotojas jos neištaiso.</span><span class="sxs-lookup"><span data-stu-id="be0a7-155">If you select *Not allowed*, a warning is shown, and the value can't be saved until the user corrects it.</span></span>
    - <span data-ttu-id="be0a7-156">**Minimalus** – Įveskite minimalią vertę rekomenduojamą ar priimtą.</span><span class="sxs-lookup"><span data-stu-id="be0a7-156">**Minimum** – Enter the minimum recommended or accepted value.</span></span>
    - <span data-ttu-id="be0a7-157">**Maksimalus** – Įveskite maksimalią vertę rekomenduojamą ar priimtą.</span><span class="sxs-lookup"><span data-stu-id="be0a7-157">**Maximum** – Enter the maximum recommended or accepted value.</span></span>

### <a name="connect-engineering-attributes-to-an-engineering-product-category"></a><span data-ttu-id="be0a7-158">Sujunkite inžinerijos atributus su inžinerijos produkto kategorija</span><span class="sxs-lookup"><span data-stu-id="be0a7-158">Connect engineering attributes to an engineering product category</span></span>

<span data-ttu-id="be0a7-159">Kai kurie inžinerijos atributai taikomi visiems produktams, tuo tarpu kiti yra konkretūs atskiriems produktams ar jų kategorijoms.</span><span class="sxs-lookup"><span data-stu-id="be0a7-159">Some engineering attributes apply to all products, whereas others are specific to individual products or product categories.</span></span> <span data-ttu-id="be0a7-160">Pavyzdžiui, elektriniai atributai nereikalingi mechaniniams produktams.</span><span class="sxs-lookup"><span data-stu-id="be0a7-160">For example, electrical attributes aren't required for mechanical products.</span></span> <span data-ttu-id="be0a7-161">Dėl to, galite nustatyti *inžinerijos produkto kategorijas*.</span><span class="sxs-lookup"><span data-stu-id="be0a7-161">Therefore, you can set up *engineering product categories*.</span></span> <span data-ttu-id="be0a7-162">Inžinerijos produkto kategorija nustato inžinerijos atributų kolekciją, kuri turi būti sąvokos produktams dalis, priklausanti tai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="be0a7-162">An engineering product category establishes the collection of engineering attributes that must be part of the definition for products that belong to that category.</span></span> <span data-ttu-id="be0a7-163">Galite taip pat nurodyti, kurie inžinerijos atributai yra privalomi ir ar yra numatytoji vertė.</span><span class="sxs-lookup"><span data-stu-id="be0a7-163">You can also specify which engineering attributes are mandatory and whether there is a default value.</span></span>

<span data-ttu-id="be0a7-164">Dėl daugiau informacijos apie tai, kaip dirbti su inžinerijos produktų kategorijomis, įskaitant informaciją apie tai, kaip sujungti atributus su jomis, žr.  [INžinerijos versijos ir inžinerijos produktų kategorijos](engineering-versions-product-category.md).</span><span class="sxs-lookup"><span data-stu-id="be0a7-164">For more information about how to work with engineering product categories, including information about how to connect attributes to categories, see [Engineering versions and engineering product categories](engineering-versions-product-category.md).</span></span>

### <a name="set-values-for-engineering-attributes"></a><span data-ttu-id="be0a7-165">Nustatykite vertes inžinerijos atributams</span><span class="sxs-lookup"><span data-stu-id="be0a7-165">Set values for engineering attributes</span></span>

<span data-ttu-id="be0a7-166">Inžinerijos atributai sujungti su inžinerijos produkto kategorijomis yra rodomi, kai kuriate naują inžinerijos produktą paremtą ta kategorija.</span><span class="sxs-lookup"><span data-stu-id="be0a7-166">The engineering attributes that are connected to an engineering product category are presented when you create a new engineering product that is based on that category.</span></span> <span data-ttu-id="be0a7-167">Tuo metu, galite nustatyti vertes atributams.</span><span class="sxs-lookup"><span data-stu-id="be0a7-167">At that time, you can set values for the attributes.</span></span> <span data-ttu-id="be0a7-168">Vėliau, tos vertės gali būti pakeitos **Inžinerijos versijos** puslapyje arba kaip inžinerijos keitimų valdymo dalis inžinerijos keitimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="be0a7-168">Later, those values can be changed on the **Engineering version** page or as part of engineering change management in an engineering change order.</span></span> <span data-ttu-id="be0a7-169">Dėl daugiau informacijos, žr. [Valdyti keitimus inžinerijos produktams](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="be0a7-169">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>

### <a name="create-an-engineering-product"></a><span data-ttu-id="be0a7-170">Sukurkite inžinerijos produktą</span><span class="sxs-lookup"><span data-stu-id="be0a7-170">Create an engineering product</span></span>

<span data-ttu-id="be0a7-171">Norėdami sukurti inžinerijos produktą, atidarykite **Išleisti produktai** puslapį.</span><span class="sxs-lookup"><span data-stu-id="be0a7-171">To create an engineering product, open the **Released products** page.</span></span> <span data-ttu-id="be0a7-172">Tuomet, veiksmų juostoje skirtuke **Produktas** grupėje **Naujas** pasirinkite **Inžinerijos produktas**.</span><span class="sxs-lookup"><span data-stu-id="be0a7-172">Then, on the Action Pane, on **Product** tab, in the **New** group, select **Engineering product**.</span></span>

<span data-ttu-id="be0a7-173">Privalote nurodyti inžinerijos kategoriją, kuriai priklauso produktas.</span><span class="sxs-lookup"><span data-stu-id="be0a7-173">You must specify the engineering category that the product belongs to.</span></span> <span data-ttu-id="be0a7-174">Kategorija nustatys numatytąsias vertes ir produkto savybes.</span><span class="sxs-lookup"><span data-stu-id="be0a7-174">The category will set all the default values and characteristics for the product.</span></span> <span data-ttu-id="be0a7-175">Taip pat ji nustatys atributus taikomus produktui.</span><span class="sxs-lookup"><span data-stu-id="be0a7-175">It will also set the attributes that are applicable to the product.</span></span> <span data-ttu-id="be0a7-176">Pasirinkus kategoriją, vertės bus nustatytos atributams.</span><span class="sxs-lookup"><span data-stu-id="be0a7-176">After the category is selected, values will be set for the attributes.</span></span> <span data-ttu-id="be0a7-177">Tuomet galite modifikuoti tas vertes.</span><span class="sxs-lookup"><span data-stu-id="be0a7-177">You can then modify those values.</span></span>

## <a name="search-for-products-by-using-engineering-attribute-values"></a><span data-ttu-id="be0a7-178">Ieškokite produktų naudodami inžinerijos atributų vertes</span><span class="sxs-lookup"><span data-stu-id="be0a7-178">Search for products by using engineering attribute values</span></span>

<span data-ttu-id="be0a7-179">Galite naudoti inžinerijos atributo paiešką, kad rastumėte produktus ieškodami jų inžinerijos atributų verčių.</span><span class="sxs-lookup"><span data-stu-id="be0a7-179">You can use engineering attribute search to find products by searching for their engineering attributes values.</span></span> <span data-ttu-id="be0a7-180">Dėl to, galite paprastai rasti inžinerijos produktus pagal jų savybes.</span><span class="sxs-lookup"><span data-stu-id="be0a7-180">Therefore, you can easily find engineering products, based on their characteristics.</span></span> <span data-ttu-id="be0a7-181">Galite ieškoti produktų priklausančių inžinerijos produktų kategorijai arba galite ieškoti visų inžinerijos produktų.</span><span class="sxs-lookup"><span data-stu-id="be0a7-181">You can search in the products that belong to an engineering product category, or you can search across all engineering products.</span></span>

<span data-ttu-id="be0a7-182">Paieška prieinama pagal produkto pagrindinius duomenų puslapius ir perdavimo prekes sistemoje, tokias kaip prekybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="be0a7-182">The search is available on product master data pages and from transactional items in the system, such as sales orders.</span></span> <span data-ttu-id="be0a7-183">Perlaidos prekei, galite naudoti **Inžinerijos atributo paieškos** puslapį, kad ieškotumėte produkto.</span><span class="sxs-lookup"><span data-stu-id="be0a7-183">For a transactional item, you can use the **Engineering attribute search** page to search for a product.</span></span> <span data-ttu-id="be0a7-184">Tada galite naudoti **Įtraukti kaip naują eilutę** mygtuką, kad įtrauktumėte produktą į prekybos užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="be0a7-184">You can then use the **Add as new line** button to add the product to the sales order lines.</span></span> <span data-ttu-id="be0a7-185">Produktai paieškos rezultatuose taip pat gali būti įtraukti tiesiogiai į užsakymą.</span><span class="sxs-lookup"><span data-stu-id="be0a7-185">Products in the search results can also be added directly to the order.</span></span>