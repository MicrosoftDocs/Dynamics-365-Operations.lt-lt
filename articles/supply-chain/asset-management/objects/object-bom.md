---
title: Turto KS
description: Šioje temoje aprašomos turto KS turto valdyme.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: baaf516eb386c3cf63d72bf31800b8731121fe26
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019531"
---
# <a name="asset-boms"></a><span data-ttu-id="b4742-103">Turto KS</span><span class="sxs-lookup"><span data-stu-id="b4742-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b4742-104">Šioje temoje aprašomos turto KS turto valdyme.</span><span class="sxs-lookup"><span data-stu-id="b4742-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="b4742-105">Puslapyje **Turto KS** rodomas visų elementų (atsarginių dalių ir kitų elementų), naudojamų turtui visą jo ciklą, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="b4742-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="b4742-106">Kuriant naują turtą reikėtų apsvarstyti turto KS nustatymą kaip sąrankos procedūros dalį.</span><span class="sxs-lookup"><span data-stu-id="b4742-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="b4742-107">Tokiu būdu galima sekti turto elementų retrospektyvą nuo sukūrimo datos.</span><span class="sxs-lookup"><span data-stu-id="b4742-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="b4742-108">Atlikus priežiūros užduotį ir užregistravus elemento suvartojimą darbo užsakyme galima sekti turto atsarginių dalių ir kitų elementų suvartojimą.</span><span class="sxs-lookup"><span data-stu-id="b4742-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="b4742-109">Ši funkcija leidžia išlaikyti viso turto išsamų elementų suvartojimo įrašą.</span><span class="sxs-lookup"><span data-stu-id="b4742-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="b4742-110">Pavyzdžiui, galima naudoti įrašą siekiant stebėti, ar konkreti atsarginė dalis dažnai keičiama, sekti atsargines dalis ar kitus elementus, kurie šiuo metu naudojami turtui.</span><span class="sxs-lookup"><span data-stu-id="b4742-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="b4742-111">Darbo užsakyme elementų suvartojimas gali apimti atsargines dalis ir kitus papildomus elementus, pvz., tepalus, varžtus ir tarpiklius.</span><span class="sxs-lookup"><span data-stu-id="b4742-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="b4742-112">Turto KS galima automatiškai atnaujinti atsižvelgiant į turto valdymo sąranką.</span><span class="sxs-lookup"><span data-stu-id="b4742-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="b4742-113">Jei darbo užsakymo ciklo būsena sukurta tvarkyti baigtus darbo užsakymus ir jeigu tos darbo užsakymo ciklo būsenos parinktis **Naujinti turto KS** nustatyta į **Taip** puslapyje **Darbo užsakymo ciklo būsenos**, visi darbo užsakyme naudojami elementai bus automatiškai atnaujinti puslapyje **Turto KS**, kai darbo užsakymas atnaujinamas į tą ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="b4742-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="b4742-114">Taip pat galima atnaujinti turto KS rankiniu būdu sukuriant naujas elementų eilutes puslapyje **Turto KS**.</span><span class="sxs-lookup"><span data-stu-id="b4742-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="b4742-115">Užregistravus elemento suvartojimą darbo užsakyme, puslapyje **Turto KS** galima sekti turto atsarginių dalių retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="b4742-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="b4742-116">Jei norite naudoti šią funkciją, turite pasirinkti elementų grupes, kurios turėtų būti naudojamos atsarginių dalių registravimui puslapyje **Atsarginių dalių elementų grupės**.</span><span class="sxs-lookup"><span data-stu-id="b4742-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="b4742-117">Norėdami naudoti turto KS funkcijas, pirmiausia turite nustatyti reikiamas atsarginių dalių elementų grupes.</span><span class="sxs-lookup"><span data-stu-id="b4742-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="b4742-118">Jei norite, kad baigus darbo užsakymą turto KS būtų atnaujinama automatiškai, galite nustatyti, kad šį naujinimą valdytų darbo užsakymo ciklo būsena.</span><span class="sxs-lookup"><span data-stu-id="b4742-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="b4742-119">Atsarginių dalių elementų grupių nustatymas</span><span class="sxs-lookup"><span data-stu-id="b4742-119">Set up spare parts item groups</span></span>

<span data-ttu-id="b4742-120">Atsarginių dalių retrospektyvos nustatymas pagrįstas elementų grupėmis, sukurtomis modulyje **Atsargų ir sandėlio valdymas**.</span><span class="sxs-lookup"><span data-stu-id="b4742-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="b4742-121">Dalyje Turto valdymas nustatomos elementų grupės, kad būtų galima sekti pasirinktų elementų grupių atsarginių dalių retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="b4742-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="b4742-122">Pasirinkite **Turto valdymas** \> **Sąranka** \>**Turtas** \> **Atsarginių dalių elementų grupės**.</span><span class="sxs-lookup"><span data-stu-id="b4742-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="b4742-123">Pasirinkite **Nauja**, kad nustatytumėte elementų grupę.</span><span class="sxs-lookup"><span data-stu-id="b4742-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="b4742-124">Lauke **Elementų grupė** pasirinkite grupę.</span><span class="sxs-lookup"><span data-stu-id="b4742-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="b4742-125">Grupės pavadinimas automatiškai įvedamas lauke **Pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="b4742-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="b4742-126">Turto KS peržiūra ir naujinimas</span><span class="sxs-lookup"><span data-stu-id="b4742-126">View and update asset BOMs</span></span>

<span data-ttu-id="b4742-127">Užregistravus elemento suvartojimą darbo užsakyme galima peržiūrėti užregistruoto elemento suvartojimą puslapyje **Turto KS**.</span><span class="sxs-lookup"><span data-stu-id="b4742-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="b4742-128">Pasirinkite **Turto valdymas** \> **Bendra** \> **Turtas** \> **Aktyvus turtas**.</span><span class="sxs-lookup"><span data-stu-id="b4742-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="b4742-129">Sąraše pasirinkite turtą, tada pasirinkite **Turto KS**.</span><span class="sxs-lookup"><span data-stu-id="b4742-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b4742-130">Norėdami peržiūrėti visas elemento suvartojimo registracijas visuose turtuose, pasirinkite **Turto valdymas** \> **Užklausos** \> **Turtas** \> **Turto KS**.</span><span class="sxs-lookup"><span data-stu-id="b4742-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="b4742-131">Pasirinkite **Naujinti turto KS**.</span><span class="sxs-lookup"><span data-stu-id="b4742-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="b4742-132">Pasirinkus **Pasirinkti** į naujinimą galima įtraukti turtą, turto tipus ir išteklius.</span><span class="sxs-lookup"><span data-stu-id="b4742-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="b4742-133">Pasirinkite **Gerai**, kad pradėtumėte naujinimą.</span><span class="sxs-lookup"><span data-stu-id="b4742-133">Select **OK** to start the update.</span></span> <span data-ttu-id="b4742-134">Taip pat galite nustatyti funkciją Naujinti kaip paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="b4742-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="b4742-135">Jei norite matyti daugiau su elementais susijusios informacijos, galite įtraukti atsargų dimensijas.</span><span class="sxs-lookup"><span data-stu-id="b4742-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="b4742-136">Pasirinkite **Atsargos** \> **Dimensijų rodymas**, tada pažymėkite dimensijų, kurias norite matyti, žymės langelius.</span><span class="sxs-lookup"><span data-stu-id="b4742-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="b4742-137">Jei norite, kad šis nustatymas būtų taikomas visam turtui puslapyje **Turto KS**, parinktį **Įrašyti sąranką** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b4742-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="b4742-138">Jei norite apžvelgti, kur turto valdyme naudojamas elementas pasirinktoje eilutėje atsižvelgiant į turtą, užduoties tipo numatytąsias reikšmes, atsargines dalis ir darbo užsakymus, pasirinkite **Elementas, kuris naudojamas**.</span><span class="sxs-lookup"><span data-stu-id="b4742-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="b4742-139">Jei norite matyti tik aktyvių elementų eilutes, pasirinkite **Rodinys** \> **Dabartinis**.</span><span class="sxs-lookup"><span data-stu-id="b4742-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="b4742-140">Norėdami peržiūrėti visų elementų eilutes, įskaitant eilutes, kuriose galiojimo pabaigos data yra ankstesnė už dabartinę datą, pasirinkite **Rodinys** \> **Visi**.</span><span class="sxs-lookup"><span data-stu-id="b4742-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="b4742-141">Jeigu baigus darbo užsakymą baigėsi kai kurių elementų ar atsarginių dalių, susijusių su tuo turtu, galiojimas arba jos buvo pakeistos kitais elementais ar atsarginėmis dalimis, rekomenduojame atitinkamai atnaujinti turto KS.</span><span class="sxs-lookup"><span data-stu-id="b4742-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="b4742-142">Naujos elemento eilutės turto KS kūrimas</span><span class="sxs-lookup"><span data-stu-id="b4742-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="b4742-143">Turto elementų eilutes galima kurti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="b4742-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="b4742-144">Puslapyje **Turto KS** pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="b4742-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="b4742-145">Lauke **turtas** pasirinkite turtą, į kurį norite įtraukti elemento eilutę.</span><span class="sxs-lookup"><span data-stu-id="b4742-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="b4742-146">Lauke **Eilutės numeris** įveskite eilutės sekos numerį.</span><span class="sxs-lookup"><span data-stu-id="b4742-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="b4742-147">Lauke **Galioja** įveskite elemento pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="b4742-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="b4742-148">Jei elementas nustos galioti, lauke **Galiojimo pabaiga** įveskite pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="b4742-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="b4742-149">Lauke **Elemento numeris** pasirinkite elementą.</span><span class="sxs-lookup"><span data-stu-id="b4742-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="b4742-150">Pavadinimas automatiškai įvedamas lauke **Produkto pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="b4742-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="b4742-151">Lauke **Kiekis** įveskite naudojamą kiekį.</span><span class="sxs-lookup"><span data-stu-id="b4742-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="b4742-152">Laukas **Vienetas** atnaujinamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="b4742-152">The **Unit** field is automatically updated.</span></span>
