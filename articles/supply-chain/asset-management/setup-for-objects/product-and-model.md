---
title: Turto gamintojai ir modeliai
description: Šioje temoje aprašoma, kaip nustatyti turto gamintojus ir susietus modelius modulyje „Turto valdymas“.
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
ms.openlocfilehash: e20ccf16bc751898b239214771821fd2872638d1
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783467"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="7dc6a-103">Turto gamintojai ir modeliai</span><span class="sxs-lookup"><span data-stu-id="7dc6a-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="7dc6a-104">Šioje temoje aprašoma, kaip nustatyti turto gamintojus ir susietus modelius modulyje „Turto valdymas“.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="7dc6a-105">Modeliai gali būti susieti su turto tipais.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="7dc6a-106">Nustatyti produktų ryšius</span><span class="sxs-lookup"><span data-stu-id="7dc6a-106">Set up product-model relations</span></span>

1. <span data-ttu-id="7dc6a-107">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turtas** \> **Gamintojas ir modelis**.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="7dc6a-108">Pasirinkite **New**, kad sukurtumėte naują produktą.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="7dc6a-109">Lauke **Gamintojas** įveskite turto gamintojo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="7dc6a-110">Lauke **Description** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="7dc6a-111">„FastTab“ skirtuke **Modeliai** pasirinkite **Įtraukti**, kad sukurtumėte turto modelį, kurį reikia susieti su turto gamintoju.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="7dc6a-112">Lauke **Modelis** įveskite turto modelio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="7dc6a-113">Lauke **Description** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="7dc6a-114">Lauke **Turto tipas** pasirinkite turto tipą, su kuriuo turėtų būti susietas gamintojo modelis.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7dc6a-115">Taip pat galite nustatyti turto tipų, gamintojų ir modelių ryšius peržvalgoje **Asset types**.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="7dc6a-116">Daugiau informacijos žr. [Kurti ilgalaikį turtą](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="7dc6a-116">For more information, see [Create asset type](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="7dc6a-117">„FastTab“ skirtuke **Išsami informacija** lauke **Modeliai** rodomas turto modelių, kurie yra nustatyti pasirinktam turto gamintojui, skaičius.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="7dc6a-118">Lauke **Turtas** rodomas turtų, naudojančių pasirinktą gamintoją, skaičius.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="7dc6a-119">Lauke **Turtas** rodomas objektų, naudojančių šio gamintojo modelį, skaičius.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="7dc6a-120">Turto tipas negali turėti jokio turto gamintojo modelio ryšių, jis gali būti susietas su vieno turto gamintojo modeliu arba su keliais turto gamintojų modeliais.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="7dc6a-121">Jei turto tipas yra susijęs bent su vienu gamintojo modeliu, tik deriniai, nustatyti peržvalgoje **Manufacturer model**, gali būti pasirinkti tuose turto valdymo puslapiuose, kuriuose gali būti nustatytas turto tipo, gamintojo ir modelio derinys.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="7dc6a-122">Šiuos puslapius sudaro **Visas turtas**, **Turto aptarnavimo lygis**, **Numatytieji užduočių tipai** ir **Priežiūros biudžeto eilutės**.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="7dc6a-123">Jei tam tikri išteklių tipai nėra susieti su jokiu gamintojo modeliu, šiuose puslapiuose rodomi tik tie turto tipai ir gamintojo modeliai, kurie taip pat nėra susieti su turto tipais.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="7dc6a-124">Objekto gamintojo ir modelio pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="7dc6a-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="7dc6a-125">Pasirinkite **Asset management** \> **Common** \> **Assets** \> **All assets**.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="7dc6a-126">Stulpelyje **Turtas** pasirinkite turto saitą.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="7dc6a-127">Pasirodo puslapis **Details**.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="7dc6a-128">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-128">Select **Edit**.</span></span>
4. <span data-ttu-id="7dc6a-129">„FastTab“ skirtuko **Bendra** laukuose **Gamintojas** ir **Modelis** pasirinkite reikšmes.</span><span class="sxs-lookup"><span data-stu-id="7dc6a-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>
