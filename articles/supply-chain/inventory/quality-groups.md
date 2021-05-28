---
title: Prekių kokybės grupės
description: Šioje temoje aprašoma, kaip naudoti ir sukurti prekių kokybės grupes, norint logiškai grupuoti produktus, kad jie būtų priskirti automatinio kokybės užsakymų generavimo kokybės susiejimams.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022257"
---
# <a name="item-quality-groups"></a><span data-ttu-id="cc3aa-103">Prekių kokybės grupės</span><span class="sxs-lookup"><span data-stu-id="cc3aa-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc3aa-104">Kokybės grupė nurodo bendruosius prekių tikrinimo reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="cc3aa-105">Šioje temoje aprašoma, kaip naudoti ir sukurti prekių kokybės grupes, norint logiškai grupuoti produktus, kad jie būtų priskirti automatinio kokybės užsakymų generavimo kokybės susiejimams.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="cc3aa-106">Naudodami šį puslapį galite nustatyti, redaguoti ir peržiūrėti kokybės grupei priskirtas prekes arba kokybės grupes, priskirtas prekei, eikite į **Atsargų valdymas \> Nustatymai \> Kokybės grupės**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="cc3aa-107">**Bandymų grupių** puslapyje apibrėžę bandymų reikalavimus, galite apibrėžti taisykles, skirtas automatiškai generuoti kokybės užsakymams.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="cc3aa-108">Kad procesas būtų paprastesnis, nenustatinėjate taisyklių atskiroms prekėms.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="cc3aa-109">Vietoj to taisykles apibrėžiate kokybės grupei, naudodami **Kokybės susiejimų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="cc3aa-110">Prekių kokybės grupės pavyzdys</span><span class="sxs-lookup"><span data-stu-id="cc3aa-110">Example of an item quality group</span></span>

<span data-ttu-id="cc3aa-111">Gamybos įmonė perka įvairių žaliavų, kurių gaunamų objektų patikrinimo bandymų reikalavimai tokie patys.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="cc3aa-112">Dėl to, įmonė apibrėžia kokybės grupę ir tada tai grupei priskiria prekių numerius, susietus su žaliavomis.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="cc3aa-113">Vėliau įmonė perka naują žaliavos tipą, kurio bandymų reikalavimai tokie patys.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="cc3aa-114">Užuot nustatydama naujosios medžiagos naujus bandymų reikalavimus, įmonė naujos medžiagos prekės numerį prideda į esamą kokybės grupę.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="cc3aa-115">Ta pati gamybos įmonė taip pat gamina prekes, kurių gamybos bandymų reikalavimai tokie patys, ir siunčia prekes, kurių tie patys reikalavimai bandymams prieš siuntimą.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="cc3aa-116">Dėl to, įmonė apibrėžia dvi papildomas kokybės grupes ir tada kiekvienai grupei priskiria atitinkamus prekių numerius.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="cc3aa-117">Kurti kokybės grupę</span><span class="sxs-lookup"><span data-stu-id="cc3aa-117">Create a quality group</span></span>

<span data-ttu-id="cc3aa-118">Norėdami sukurti kokybės grupę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="cc3aa-119">Pasirinkite **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Kokybės grupės**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="cc3aa-120">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="cc3aa-121">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="cc3aa-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="cc3aa-122">**Kokybės grupė** – įveskite unikalų kokybės grupės ID arba pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="cc3aa-123">**Aprašas** – įveskite išsamų kokybės grupės aprašą.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="cc3aa-124">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="cc3aa-125">Rankiniu būdu įtraukite prekes į kokybės grupę</span><span class="sxs-lookup"><span data-stu-id="cc3aa-125">Manually add items to a quality group</span></span>

<span data-ttu-id="cc3aa-126">Norėdami rankiniu būdu įtraukti prekes į kokybės grupę, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="cc3aa-127">Pasirinkite **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Kokybės grupės**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="cc3aa-128">Pasirinkite kokybės grupę, į kurią norite įtraukti prekes.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="cc3aa-129">Veiksmų srityje pasirinkite **Prekės**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="cc3aa-130">Puslapyje **Prekių kokybės grupės** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="cc3aa-131">Tada nustatykite naujos eilutės **lauką** Prekės numeris kaip prekės numerį, kurį norite pridėti.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="cc3aa-132">Pakartokite ankstesnį veiksmą su kiekviena papildoma preke, kurią reikia pridėti.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="cc3aa-133">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="cc3aa-134">Įtraukite kelias prekes į kokybės grupę</span><span class="sxs-lookup"><span data-stu-id="cc3aa-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="cc3aa-135">Norėdami rankiniu būdu įtraukti kelias prekes į kokybės grupę, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="cc3aa-136">Pasirinkite **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Kokybės grupės**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="cc3aa-137">Kurkite ar rinkitės kokybės grupę, į kurią norite įtraukti prekes.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="cc3aa-138">Veiksmų srityje pasirinkite **Įtraukti prekes**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="cc3aa-139">Į **užklausos** dialogo langą įvesti elementų, kuriuos norite įtraukti, filtro kriterijus.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="cc3aa-140">Pavyzdžiui, galite filtruoti visas konkrečios prekių grupės prekes.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="cc3aa-141">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-141">Select **OK**.</span></span>
1. <span data-ttu-id="cc3aa-142">Dialogo lange **Įtraukti elementus rodomas visas** užklausą atitinkančias prekes.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="cc3aa-143">Peržiūrėkite rezultatus.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-143">Review the results.</span></span>

    <span data-ttu-id="cc3aa-144">Jei reikia atlikti kokius nors pakeitimus, **pasirinkite** Pasirinkti, norėdami grįžti į **užklausos dialogo langą ir** pakoreguokite savo užklausą.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="cc3aa-145">Kai rezultatuose yra visos norimos pridėti prekės, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="cc3aa-146">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="cc3aa-147">Rankiniu būdu susieti prekę su kokybės grupe</span><span class="sxs-lookup"><span data-stu-id="cc3aa-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="cc3aa-148">Norėdami rankiniu būdu susieti prekes su kokybės grupe, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="cc3aa-149">Pasirinkite **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Prekės kokybės grupės**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="cc3aa-150">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="cc3aa-151">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="cc3aa-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="cc3aa-152">**Prekės numeris** – pasirinkite norimą pridėti prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="cc3aa-153">**Kokybės grupė** – pasirinkite kokybės grupę, norimą priskirti prekei.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="cc3aa-154">Pakartokite ankstesnį veiksmą su kiekviena papildoma prekės ir kokybės grupės, kurią reikia pridėti, kombinacija.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="cc3aa-155">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="cc3aa-156">Rankiniu būdu įtraukti kokybės grupę iš puslapio Išleisti produktai</span><span class="sxs-lookup"><span data-stu-id="cc3aa-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="cc3aa-157">Norėdami rankiniu būdu įtraukti kokybės grupę iš **Išleistų produktų** puslapio, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="cc3aa-158">Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="cc3aa-159">Pasirinkite produktą, kuriam norite priskirti kokybės grupę.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="cc3aa-160">Veiksmų srityje, skirtuke **Tvarkyti atsargas**, grupėje **Kokybė**, pasirinkite **Prekės kokybės grupės**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="cc3aa-161">Puslapyje **Prekių kokybės grupės** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="cc3aa-162">Tada nustatykite naujos eilutės lauką **Kokybės grupė kaip kokybės** grupę, kurią norite priskirti produktui.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="cc3aa-163">Pakartokite ankstesnį veiksmą kiekvienai papildomai kokybės grupei, kurią norite priskirti produktui.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="cc3aa-164">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc3aa-165">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="cc3aa-165">Additional resources</span></span>

- [<span data-ttu-id="cc3aa-166">Kokybės valdymo bandymo instrumentai</span><span class="sxs-lookup"><span data-stu-id="cc3aa-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="cc3aa-167">Kokybės valdymo bandymai</span><span class="sxs-lookup"><span data-stu-id="cc3aa-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="cc3aa-168">Kokybės valdymo bandymo grupės</span><span class="sxs-lookup"><span data-stu-id="cc3aa-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="cc3aa-169">Kokybės valdymo bandymo kintamieji</span><span class="sxs-lookup"><span data-stu-id="cc3aa-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="cc3aa-170">Kokybės susiejimai</span><span class="sxs-lookup"><span data-stu-id="cc3aa-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
