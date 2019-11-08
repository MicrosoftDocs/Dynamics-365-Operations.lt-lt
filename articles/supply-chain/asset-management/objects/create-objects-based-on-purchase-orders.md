---
title: Turto kūrimas pagal pirkimo užsakymus
description: Šioje temoje aiškinama, kaip galima sukurti turto elementų, kurie gali būti naudojami kaip pagrindas kuriant turto priežiūros užduotis modulyje Turto valdymas, sąrašą.
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
ms.openlocfilehash: 6eba14e285f23338cad0243fca567b30c6d4d3f2
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571581"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="ccb6b-103">Turto kūrimas pagal pirkimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="ccb6b-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ccb6b-104">Šioje temoje aiškinama, kaip galima sukurti turto elementų, kurie gali būti naudojami kaip pagrindas kuriant turto priežiūros užduotis modulyje Turto valdymas, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="ccb6b-105">Atsižvelgdami į turto elementus, galite peržiūrėti pirkimo užsakymo eilučių sąrašą, sukurtą konkretiems elementams.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="ccb6b-106">Ši funkcija padeda lengvai sukurti turtą modulyje Turto valdymas pagal pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="ccb6b-107">Pirmiausia nustatykite elementus, kurie bus naudojami kuriant turtą iš pirkimo užsakymo, esančio **Turto elementai**.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="ccb6b-108">Sukūrę pirkimo užsakymo eilutę, sukurkite turtą, naudodami **Turtas, laukiantis patvirtinimo**.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="ccb6b-109">Galite nuspręsti, kuriame pirkimo užsakymo etape norėsite sukurti turtą.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="ccb6b-110">Pasirinkite turto elementus</span><span class="sxs-lookup"><span data-stu-id="ccb6b-110">Select asset items</span></span>

1. <span data-ttu-id="ccb6b-111">Spustelėkite **Turto valdymas** > **Konfigūracija** > **Turtas** > **Elementai**.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="ccb6b-112">Spustelėję **Nauja** sukurkite naują prekių grupę.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="ccb6b-113">Lauke **Prekės numeris** pasirinkite prekę.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="ccb6b-114">Uždarius šį lauką, elemento pavadinimas automatiškai įterpiamas į lauką **Produkto pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="ccb6b-115">„FastTab“ skirtuke **Bendra** pasirinkite elemento turto tipą.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="ccb6b-116">Pasirinkite turto gamintoją ir elemento modelį.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="ccb6b-117">Įrašykite elementą.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="ccb6b-118">Turto sukūrimas naudojant turtą, laukiantį patvirtinimo</span><span class="sxs-lookup"><span data-stu-id="ccb6b-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="ccb6b-119">Spustelėkite **Turto valdymas** > **Bendra** > **Turtas** > **Turtas, laukiantis patvirtinimo**.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="ccb6b-120">Pamatysite atnaujintą pirkimo užsakymų sąrašą pagal elementus, pasirinktus modulyje **Turto elementai**.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="ccb6b-121">Galite filtruoti pirkimo užsakymų būseną, kad pasirinktumėte, kurioje ciklo būsenoje turtas turėtų būti sukurtas.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="ccb6b-122">Pavyzdžiui, galite pasirinkti sukurti turtą tik tada, kai produkto gavimo kvitas užregistruotas pirkimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="ccb6b-123">Daugiau informacijos apie elementą rasite paspaudę nuorodą **Nuorodos numeris**, esančią pirkimo užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="ccb6b-124">Jei norite redaguoti, kurios dimensijos yra rodomos „FastTab“ skirtuke **Atsargų dimensijos**, spustelėkite mygtuką **Rodyti dimensijas** ir redaguokite pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="ccb6b-125">Jei norite kurti turtą pagal pirkimo užsakymo eilutę, sąrašo puslapyje pažymėkite tos eilutės žymės langelį stulpelyje **Žyma** ir spustelėkite **Kurti turtą**.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="ccb6b-126">Pasirodys pranešimas apie turto ID.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="ccb6b-127">Sąraše **Visas turtas** pasirinkite turtą ir spustelėkite **Redaguoti**, kad pridėtumėte daugiau informacijos apie turtą.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="ccb6b-128">Jei lauke **Laukiantis turtas** norite panaikinti eilutę, nes nenorite sukurti turto, pasirinkite tos eilutės žymės langelį stulpelyje **Žymėti** ir spustelėkite **Atmesti laukiantį turtą**.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="ccb6b-129">Pasirodys pranešimas apie turto ID.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="ccb6b-130">Jūs nepanaikinate pirkimo užsakymo arba pardavimo užsakymo, panaikinamas tik įrašas, iš kurio galėjote sukurti turtą modulyje **Turto valdymas**.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="ccb6b-131">Visos produkto dimensijos (dydis, spalva, konfigūracija ir kt.) automatiškai perkeliamos į turto atributus.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="ccb6b-132">Sekimo dimensijos (serijos numeris) yra išsaugomos sukurtame turte.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="ccb6b-133">Turto, laukiančio patvirtinimo, paieška</span><span class="sxs-lookup"><span data-stu-id="ccb6b-133">Find pending assets</span></span>

<span data-ttu-id="ccb6b-134">Galite paleisti funkciją **Laukiančio turto skaičiavimas**, norėdami patikrinti, ar yra turto, laukiančio patvirtinimo.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="ccb6b-135">Pavyzdžiui, ši funkcija gali būti naudojama kiekvieną kartą gavus pranešimą apie tai, kad turtas, laukiantis patvirtinimo, yra parengtas būti sukurtas kaip turtas.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="ccb6b-136">Spustelėkite **Turto valdymas** > **Periodinis** > **Turtas** > **Turto, laukiančio patvirtinimo, skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="ccb6b-137">Spustelėkite **Gerai**, jei norite vykdyti užduotį ir atnaujinti sąrašą, esantį **Laukiantis turtas**.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="ccb6b-138">Galite nustatyti, kad ši užduotis būtų vykdoma kaip paketinė užduotis, pvz., kartą per dieną.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="ccb6b-139">**Atsargiai:** Įspėjimas: jei pirkimo užsakymo duomenys pakeičiami *jau* sukūrus turtą pagal jam priklausantį elementą, pakeitimai neturės turtui jokios įtakos.</span><span class="sxs-lookup"><span data-stu-id="ccb6b-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>
