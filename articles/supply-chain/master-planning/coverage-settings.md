---
title: Padengimo parametrai
description: Šioje temoje pateikiama informacija apie padengimo parametrus, kurie bendrojo planavimo metu naudojami prekių poreikiui skaičiuoti.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538899"
---
# <a name="coverage-settings"></a><span data-ttu-id="9994c-103">Padengimo parametrai</span><span class="sxs-lookup"><span data-stu-id="9994c-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9994c-104">Bendrasis planavimas naudoja padengimo parametrus prekės poreikiui apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="9994c-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="9994c-105">Galite nurodyti padengimo parametrus keliais būdais:</span><span class="sxs-lookup"><span data-stu-id="9994c-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="9994c-106">Nurodykite padengimo grupės padengimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="9994c-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="9994c-107">Galite sukurti padengimo grupę, kurioje būtų visų su padengimo grupe susijusių produktų parametrai.</span><span class="sxs-lookup"><span data-stu-id="9994c-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="9994c-108">Norėdami sukurti padengimo grupę, eikite į **Bendrasis planavimas &gt; Sąranka &gt; Padengimas &gt; Padengimo grupės**.</span><span class="sxs-lookup"><span data-stu-id="9994c-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="9994c-109">Padengimo grupę galite susieti su produktu.</span><span class="sxs-lookup"><span data-stu-id="9994c-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="9994c-110">Jei saitas yra konkrečios teritorijos, sandėlio ar produkto dimensijos, naudokite puslapio **Prekės padengimas** lauką **Padengimo grupė**.</span><span class="sxs-lookup"><span data-stu-id="9994c-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="9994c-111">Jei saitas yra bendrasis, neatsižvelgdami į produkto dimensijas, naudokite puslapio **Produkto informacija** sparčiajame skirtuke **Planas** esantį lauką **Padengimo grupė**.</span><span class="sxs-lookup"><span data-stu-id="9994c-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="9994c-112">Pagal numatytuosius parametrus, jei padengimo grupės nesusiejate su produktu, bendrojo planavimo funkcija kaip numatytąją naudoja puslapyje **Bendrojo planavimo parametrai** nurodytą parinktį Bendroji padengimo grupė.</span><span class="sxs-lookup"><span data-stu-id="9994c-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="9994c-113">Nurodykite produkto padengimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="9994c-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="9994c-114">Galite sukurti konkretaus produkto padengimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="9994c-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="9994c-115">Eikite į **Produkto informacijos valdymas &gt; Produktai &gt; Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="9994c-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="9994c-116">Pasirinkite produktą ir Veiksmų srities skirtuko **Planas** lauke **Padengimo** grupėje pasirinkite **Prekės padengimas**, kad būtų atidarytas puslapis **Prekės padengimas**.</span><span class="sxs-lookup"><span data-stu-id="9994c-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="9994c-117">Jei produktas jau susietas su padengimo grupe, galite nepaisyti padengimo grupės parametrų, naudodami lauką **Nepaisyti**.</span><span class="sxs-lookup"><span data-stu-id="9994c-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="9994c-118">Padengimo parametrams puslapyje**Prekės padengimas** teikiama pirmenybė prieš parametrus puslapyje **Padengimo grupė**.</span><span class="sxs-lookup"><span data-stu-id="9994c-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="9994c-119">Nurodykite produkto padengimo parametrus naudodami vedlį.</span><span class="sxs-lookup"><span data-stu-id="9994c-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="9994c-120">Vediklis nuosekliai pademonstruos pagrindinių prekės padengimo parametrų sąrankos procesą.</span><span class="sxs-lookup"><span data-stu-id="9994c-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="9994c-121">Veiksmų srities puslapyje **Prekės padengimas** pasirinkite **Vedlys**, kad būtų atidarytas **Prekės padengimo vedlys**.</span><span class="sxs-lookup"><span data-stu-id="9994c-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="9994c-122">Nurodykite dimensijos grupės padengimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="9994c-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="9994c-123">Eikite į **Produkto informacijos valdymas &gt; Produktai &gt; Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="9994c-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="9994c-124">Puslapio **Patvirtinto produkto informacija** sparčiajame skirtuke **Bendra** esančioje sekcijoje **Administravimas** pasirinkite saitą lauke **Saugojimo dimensijų grupė**.</span><span class="sxs-lookup"><span data-stu-id="9994c-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="9994c-125">Puslapyje **Saugojimo dimensijų grupės** pasirinkite žymės laukelį **Padengimo planas dimensijomis**, kad sukurtumėte saugojimo dimensijų grupės dimensijos padengimo nustatymus.</span><span class="sxs-lookup"><span data-stu-id="9994c-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="9994c-126">Visose produkto dimensijose, pvz., konfigūracijos, spalvos, dydžio, stiliaus, turi būti pasirinktas laukas **Padengimo planas pagal dimensiją**.</span><span class="sxs-lookup"><span data-stu-id="9994c-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9994c-127">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9994c-127">Additional resources</span></span>

[<span data-ttu-id="9994c-128">Bendrieji planai</span><span class="sxs-lookup"><span data-stu-id="9994c-128">Master plans</span></span>](master-plans.md)
