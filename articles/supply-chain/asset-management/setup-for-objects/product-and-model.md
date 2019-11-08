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
ms.openlocfilehash: 14a73f49064911a2b28c742cfc19469f4bf95e74
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569966"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="172a0-103">Turto gamintojai ir modeliai</span><span class="sxs-lookup"><span data-stu-id="172a0-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="172a0-104">Šioje temoje aprašoma, kaip nustatyti turto gamintojus ir susietus modelius modulyje „Turto valdymas“.</span><span class="sxs-lookup"><span data-stu-id="172a0-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="172a0-105">Modeliai gali būti susieti su turto tipais.</span><span class="sxs-lookup"><span data-stu-id="172a0-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="172a0-106">Nustatyti produktų ryšius</span><span class="sxs-lookup"><span data-stu-id="172a0-106">Set up product-model relations</span></span>

1. <span data-ttu-id="172a0-107">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turtas** \> **Gamintojas ir modelis**.</span><span class="sxs-lookup"><span data-stu-id="172a0-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="172a0-108">Pasirinkite **Naujas**, kad sukurtumėte naują produktą.</span><span class="sxs-lookup"><span data-stu-id="172a0-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="172a0-109">Lauke **Gamintojas** įveskite turto gamintojo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="172a0-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="172a0-110">Lauke **Aprašymas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="172a0-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="172a0-111">„FastTab“ skirtuke **Modeliai** pasirinkite **Įtraukti**, kad sukurtumėte turto modelį, kurį reikia susieti su turto gamintoju.</span><span class="sxs-lookup"><span data-stu-id="172a0-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="172a0-112">Lauke **Modelis** įveskite turto modelio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="172a0-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="172a0-113">Lauke **Aprašymas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="172a0-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="172a0-114">Lauke **Turto tipas** pasirinkite turto tipą, su kuriuo turėtų būti susietas gamintojo modelis.</span><span class="sxs-lookup"><span data-stu-id="172a0-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="172a0-115">Taip pat galite nustatyti turto tipų, gamintojų ir modelių ryšius peržvalgoje **Turto tipai**.</span><span class="sxs-lookup"><span data-stu-id="172a0-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="172a0-116">Daugiau informacijos žr. [Kurti ilgalaikį turtą](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="172a0-116">For more information, see [Create asset type](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="172a0-117">„FastTab“ skirtuke **Išsami informacija** lauke **Modeliai** rodomas turto modelių, kurie yra nustatyti pasirinktam turto gamintojui, skaičius.</span><span class="sxs-lookup"><span data-stu-id="172a0-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="172a0-118">Lauke **Turtas** rodomas turtų, naudojančių pasirinktą gamintoją, skaičius.</span><span class="sxs-lookup"><span data-stu-id="172a0-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="172a0-119">Lauke **Turtas** rodomas objektų, naudojančių šio gamintojo modelį, skaičius.</span><span class="sxs-lookup"><span data-stu-id="172a0-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="172a0-120">Turto tipas negali turėti jokio turto gamintojo modelio ryšių, jis gali būti susietas su vieno turto gamintojo modeliu arba su keliais turto gamintojų modeliais.</span><span class="sxs-lookup"><span data-stu-id="172a0-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="172a0-121">Jei turto tipas yra susijęs bent su vienu gamintojo modeliu, tik deriniai, nustatyti peržvalgoje **Gamintojo modelis**, gali būti pasirinkti tuose turto valdymo puslapiuose, kuriuose gali būti nustatytas turto tipo, gamintojo ir modelio derinys.</span><span class="sxs-lookup"><span data-stu-id="172a0-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="172a0-122">Šiuos puslapius sudaro **Visas turtas**, **Turto aptarnavimo lygis**, **Numatytieji užduočių tipai** ir **Priežiūros biudžeto eilutės**.</span><span class="sxs-lookup"><span data-stu-id="172a0-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="172a0-123">Jei tam tikri išteklių tipai nėra susieti su jokiu gamintojo modeliu, šiuose puslapiuose rodomi tik tie turto tipai ir gamintojo modeliai, kurie taip pat nėra susieti su turto tipais.</span><span class="sxs-lookup"><span data-stu-id="172a0-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="172a0-124">Objekto gamintojo ir modelio pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="172a0-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="172a0-125">Pasirinkite **Turto valdymas** \> **Bendra** \> **Turtas** \> **Visas turtas**.</span><span class="sxs-lookup"><span data-stu-id="172a0-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="172a0-126">Stulpelyje **Turtas** pasirinkite turto saitą.</span><span class="sxs-lookup"><span data-stu-id="172a0-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="172a0-127">Pasirodo puslapis **Detalės**.</span><span class="sxs-lookup"><span data-stu-id="172a0-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="172a0-128">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="172a0-128">Select **Edit**.</span></span>
4. <span data-ttu-id="172a0-129">„FastTab“ skirtuko **Bendra** laukuose **Gamintojas** ir **Modelis** pasirinkite reikšmes.</span><span class="sxs-lookup"><span data-stu-id="172a0-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>
