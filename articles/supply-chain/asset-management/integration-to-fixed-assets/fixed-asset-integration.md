---
title: Turto valdymo integravimas naudojant ilgalaikį turtą
description: Šioje temoje paaiškinama, kaip integruoti turto valdymo ir ilgalaikio turto modulius, kad galėtumėte susieti ilgalaikį turtą su prižiūrimu turtu.
author: kamaybac
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: a45bf1f62cdcc8abed2ec157a223e7f3fddec7ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809859"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="85a0e-103">Turto valdymo integravimas naudojant ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="85a0e-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85a0e-104">Integruodami **turto valdymo** ir **ilgalaikio turto** modulius, galite susieti ilgalaikį turtą su prižiūrimu turtu.</span><span class="sxs-lookup"><span data-stu-id="85a0e-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="85a0e-105">Tada ilgalaikio turto vartotojai gali sukurti prižiūrimą turtą iš naujo arba esamo ilgalaikio turto, o turto valdymo vartotojai gali susieti prižiūrimą turtą su esamu ilgalaikiu turtu.</span><span class="sxs-lookup"><span data-stu-id="85a0e-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="85a0e-106">Ši funkcija taip pat palengvina ilgalaikio turto vartotojų išlaidų, užregistruotų iš susijusio prižiūrimo turto darbo užsakymų, peržiūrą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="85a0e-107">Šioje temoje *prižiūrimas turtas* nurodo **turto valdymo** modulio turtą, o *ilgalaikis turtas* nurodo **ilgalaikio turto** modulio turtą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="85a0e-108">Numatytosios naujo prižiūrimo turto, sukurto iš ilgalaikio turto, vietos nustatymas (nebūtina)</span><span class="sxs-lookup"><span data-stu-id="85a0e-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="85a0e-109">Ši papildoma konfigūracija leidžia nustatyti numatytąją naujo prižiūrimo turto, sukurto iš ilgalaikio turto, funkcinę vietą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="85a0e-110">Paprastai šią konfigūraciją atliekate tik vieną kartą, jei užbaigiate ją visą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="85a0e-111">Norėdami užbaigti konfigūraciją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="85a0e-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="85a0e-112">Eikite į **Turto valdymas \> Sąranka \> Turto valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="85a0e-113">Skirtuko **Ilgalaikis turtas** lauke **Funkcinės vieta** pasirinkite numatytąją vietą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="85a0e-114">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="85a0e-115">Darbas su integruotu prižiūrimu turtu ir ilgalaikiu turtu</span><span class="sxs-lookup"><span data-stu-id="85a0e-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="85a0e-116">Šiame skyriuje pateikiama procedūrų, rodančių įvairius būdus, kaip galima dirbti su integruotomis turto valdymo ir ilgalaikio turto funkcijomis, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="85a0e-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="85a0e-117">Esamo prižiūrimo turto susiejimas su ilgalaikiu turtu</span><span class="sxs-lookup"><span data-stu-id="85a0e-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="85a0e-118">Norėdami susieti esamą prižiūrimą turtą su ilgalaikiu turtu, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="85a0e-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="85a0e-119">Eikite į **Turto valdymas \> Turtas \> Visas turtas** (arba **Aktyvus turtas**).</span><span class="sxs-lookup"><span data-stu-id="85a0e-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="85a0e-120">Pasirinkite turtą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-120">Select an asset.</span></span>
1. <span data-ttu-id="85a0e-121">„FastTab“ konteinerio **Ilgalaikis turtas** lauke **Ilgalaikio turto numeris** pasirinkite esamą ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="85a0e-122">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="85a0e-123">Ilgalaikio turto, susieto su pasirinktu prižiūrimu turtu, peržiūra</span><span class="sxs-lookup"><span data-stu-id="85a0e-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="85a0e-124">Norėdami peržiūrėti ilgalaikį turtą, susietą su pasirinktu prižiūrimu turtu, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="85a0e-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="85a0e-125">Eikite į **Turto valdymas \> Turtas \> Visas turtas** (arba **Aktyvus turtas**).</span><span class="sxs-lookup"><span data-stu-id="85a0e-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="85a0e-126">Pasirinkite turtą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-126">Select an asset.</span></span>
1. <span data-ttu-id="85a0e-127">„FastTab“ konteinerio **Ilgalaikis turtas** lauke **Ilgalaikio turto numeris** pasirinkite saitą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="85a0e-128">Atidaromas pasirinkto turto puslapis **Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="85a0e-129">(Paprastai šis puslapis randamas **Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.)</span><span class="sxs-lookup"><span data-stu-id="85a0e-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="85a0e-130">Prižiūrimo turto, susieto su pasirinktu ilgalaikiu turtu, peržiūra</span><span class="sxs-lookup"><span data-stu-id="85a0e-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="85a0e-131">Norėdami peržiūrėti prižiūrimą turtą, susietą su pasirinktu ilgalaikiu turtu, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="85a0e-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="85a0e-132">Eikite į **Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="85a0e-133">Pasirinkite turtą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-133">Select an asset.</span></span>
1. <span data-ttu-id="85a0e-134">Veiksmų srityje, skirtuke **Turto valdymas**, grupėje **Peržiūrėti**, pasirinkite **Prižiūrimas turtas**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="85a0e-135">Atidaromas turto, susieto su pasirinktu ilgalaikiu turtu, puslapis **Prižiūrimas turtas**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="85a0e-136">(Paprastai šis puslapis randamas **Turto valdymas \> Turtas \> Visas turtas**.)</span><span class="sxs-lookup"><span data-stu-id="85a0e-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="85a0e-137">Priežiūros išlaidų, susijusių su ilgalaikiu turtu, peržiūra</span><span class="sxs-lookup"><span data-stu-id="85a0e-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="85a0e-138">Prižiūrimo turto valdymo darbo užsakymai gali būti registruojami, o kiekvienam iš šių darbo užsakymų paprastai taikomos išlaidos.</span><span class="sxs-lookup"><span data-stu-id="85a0e-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="85a0e-139">Kai ilgalaikis turtas susiejamas su prižiūrimu turtu, galite pereiti tiesiai iš ilgalaikio turto į susijusių išlaidų peržiūrą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="85a0e-140">Norėdami peržiūrėti priežiūros išlaidas, susietas su ilgalaikiu turtu, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="85a0e-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="85a0e-141">Eikite į **Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="85a0e-142">Pasirinkite turtą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-142">Select an asset.</span></span>
1. <span data-ttu-id="85a0e-143">Veiksmų srityje, skirtuke **Turto valdymas**, grupėje **Peržiūrėti**, pasirinkite **Priežiūros išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="85a0e-144">Atidaromas puslapis **Priežiūros išlaidos** ir parodomos susijusios išlaidos.</span><span class="sxs-lookup"><span data-stu-id="85a0e-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="85a0e-145">Esamo ilgalaikio turto prižiūrimo turto kūrimas</span><span class="sxs-lookup"><span data-stu-id="85a0e-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="85a0e-146">Norėdami sukurti naują esamo ilgalaikio turto prižiūrimą turtą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="85a0e-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="85a0e-147">Eikite į **Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="85a0e-148">Pasirinkite turtą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-148">Select an asset.</span></span>
1. <span data-ttu-id="85a0e-149">Veiksmų srityje, skirtuke **Turto valdymas**, grupėje **Naujas**, pasirinkite **Kurti prižiūrimą turtą**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="85a0e-150">(Jei ši pasirinktis neprieinama, gali būti, kad prižiūrimas turtas jau susietas su pasirinktu ilgalaikiu turtu.)</span><span class="sxs-lookup"><span data-stu-id="85a0e-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="85a0e-151">Baikite turto kūrimą, kaip nurodyta [Turto kūrimas](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="85a0e-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="85a0e-152">Naujo ilgalaikio turto kūrimas ir naujo prižiūrimo turto įtraukimas į jį</span><span class="sxs-lookup"><span data-stu-id="85a0e-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="85a0e-153">Norėdami sukurti naują ilgalaikį turtą ir į jį įtraukti naują prižiūrimą turtą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="85a0e-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="85a0e-154">Eikite į **Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="85a0e-155">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="85a0e-156">Baikite ilgalaikio turto kūrimą, kaip nurodyta [Ilgalaikio turto kūrimas](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="85a0e-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="85a0e-157">Veiksmų srityje, skirtuke **Turto valdymas**, grupėje **Naujas**, pasirinkite **Kurti prižiūrimą turtą**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="85a0e-158">Baikite turto kūrimą, kaip nurodyta [Turto kūrimas](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="85a0e-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="85a0e-159">Dviejų turto vienetų susiejimo šalinimas</span><span class="sxs-lookup"><span data-stu-id="85a0e-159">Remove the association between two assets</span></span>

<span data-ttu-id="85a0e-160">Kai kuriais atvejais gali reikėti atsieti prižiūrimą turtą nuo jo ilgalaikio turto.</span><span class="sxs-lookup"><span data-stu-id="85a0e-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="85a0e-161">Pavyzdžiui, jei norite [sukurti naują prižiūrimą turtą](#new-maintenance-from-fixed) iš ilgalaikio turto, pirmiausia turite pašalinti visus esamus susiejimus.</span><span class="sxs-lookup"><span data-stu-id="85a0e-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="85a0e-162">Norėdami pašalinti esamą prižiūrimo turto ir ilgalaikio turto susiejimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="85a0e-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="85a0e-163">Eikite į **Turto valdymas \> Turtas \> Visas turtas** (arba **Aktyvus turtas**).</span><span class="sxs-lookup"><span data-stu-id="85a0e-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="85a0e-164">Raskite ir atidarykite ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="85a0e-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="85a0e-165">„FastTab“ konteineryje **Ilgalaikis turtas** išvalykite lauko **Funkcinė vieta** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85a0e-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="85a0e-166">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="85a0e-166">On the Action Pane, select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]