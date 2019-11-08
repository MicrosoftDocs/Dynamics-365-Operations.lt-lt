---
title: Kelių lygių turtas
description: Šioje temoje paaiškinama, kaip kurti ir naikinti kelių lygių turtą.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c2a4052f9beca554932d7f2547288e02358b603
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571512"
---
# <a name="multi-level-assets"></a><span data-ttu-id="3aeeb-103">Kelių lygių turtas</span><span class="sxs-lookup"><span data-stu-id="3aeeb-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3aeeb-104">Šioje temoje paaiškinama, kaip kurti ir naikinti kelių lygių turtą.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="3aeeb-105">Galite kurti turtą ir susijusį antrinį turtą hierarchinėje medžio struktūroje.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="3aeeb-106">Tokiu būdu galite parodyti turto ryšius ir priklausomybes.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="3aeeb-107">Priežiūros užduotys gali būti susijusios su visais medžio struktūros lygiais.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="3aeeb-108">Statistiniai duomenys taip pat gali būti kuriami atskiram lygiui arba visų antrinio turto lygių sumai.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="3aeeb-109">Puslapyje **Visas turtas** (**Turto valdymas** \> **Bendra** \> **Turtas** \> **Visas turtas**), **Turtas** skiltyje nurodomi turto hierarchine tvarka.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="3aeeb-110">Stulpelyje **Pirminis** rodomas susijęs pirminis.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="3aeeb-111">Be to, jei turtas ir antrinis turtas jau sukurti, srities **Susijusi informacija** sekcijoje **Turto medis** turtas rodomas medžio struktūroje.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="3aeeb-112">Daugiau informacijos apie turto kūrimą ieškokite skyriuje [Turto kūrimas](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="3aeeb-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="3aeeb-113">Norėdami sukurti antrinį turtą, FastTab **Bendra** esančiame lauke **Pirminis** pasirinkite pirminį turtą.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="3aeeb-114">Turto arba turto struktūros kopijavimas</span><span class="sxs-lookup"><span data-stu-id="3aeeb-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="3aeeb-115">Jei jūsų įmonėje yra keletas panašių turto struktūrų, galite naudoti modulio Turto valdymas funkciją Kopijuoti, kad greitai jas sukurtumėte.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="3aeeb-116">Pasirinkite **Turto valdymas** \> **Bendra** \> **Turtas** \> **Visas turtas**.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="3aeeb-117">Sąrašo puslapyje **Visas turtas** pasirinkite norimą kopijuoti turtą.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="3aeeb-118">Pavyzdžiui, jei norite nukopijuoti visą turto struktūrą, įskaitant antrinį turtą, pasirinkite pirminį turtą.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="3aeeb-119">Pasirinkite **Kopijuoti turtą**.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-119">Select **Copy asset**.</span></span> <span data-ttu-id="3aeeb-120">Sekcijos **Kopijuoti iš** lauke **Turtas** nustatytas turtas, kurį pasirinkote sąrašo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="3aeeb-121">Sekcijos **Kopijuoti į** lauke **Turtas** įveskite naujo turto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="3aeeb-122">Jei kuriamas turtas turėtų būti esamos turto struktūros dalis, sekcijos **Pirminis turtas** lauke **Turtas** pasirinkite pirminį ID.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="3aeeb-123">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-123">Select **OK**.</span></span> <span data-ttu-id="3aeeb-124">Nauja turto struktūra rodoma sąrašo puslapyje **Visas turtas**.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="3aeeb-125">Visi turto atributai, priežiūros planai ir priežiūros etapai, kurie yra susiję su nukopijuotu turtu, perkeliami į naują turtą arba turto struktūrą.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="3aeeb-126">Kai kopijuojate turto struktūrą, antrinio turto pavadinimas naujoje struktūroje yra toks pat, kaip ir nukopijuoto antrinio turto pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="3aeeb-127">Kopijavimo procedūrai pasibaigus, galite lengvai pakeisti turto pavadinimą ir kitus parametrus.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="3aeeb-128">Sąrašo puslapyje **Visas turtas** pasirinkite turtą ir spustelėkite mygtuką **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="3aeeb-129">Kai kopijuojate turtą arba turto struktūrą, naujo turto ciklo būsena nustatoma iš naujo į būseną, kurią apibrėžėte kaip pradinę turto ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="3aeeb-130">Funkcinė vieta nustatoma iš naujo į numatytąją funkcinę vietą.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="3aeeb-131">Turto arba turto struktūros naikinimas</span><span class="sxs-lookup"><span data-stu-id="3aeeb-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="3aeeb-132">Jei yra su turtu susijusio antrinio turto, jį galite panaikinti tik tada, jei jokiame turte neužregistruota priežiūros užklausų, užduočių pagal darbo užsakymus, užregistruotų gedimų arba būklės vertinimų.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="3aeeb-133">Sąrašo puslapyje **Visas turtas** pasirinkite norimą naikinti turtą.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="3aeeb-134">Pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="3aeeb-135">Jei negalite panaikinti turto vadovaudamiesi šia procedūra, kitas naikinimo būdas yra nustatyti turto ciklo būseną šiuo tikslu.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="3aeeb-136">Pavyzdžiui, puslapyje **Turto ciklo būsenos** galite nustatyti ciklo būseną **Nurašytas** arba **Panaikintas**.</span><span class="sxs-lookup"><span data-stu-id="3aeeb-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
