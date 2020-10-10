---
title: Turto rodinys
description: Šioje temoje aprašomas turto rodinys Turto valdyme.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTree, EntAssetFunctionalLocationTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc4cd9ada9c1f64b434cd657eb5f5654c1328ef4
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888767"
---
# <a name="asset-view"></a><span data-ttu-id="63e8a-103">Turto rodinys</span><span class="sxs-lookup"><span data-stu-id="63e8a-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="63e8a-104">Šioje temoje aprašoma „“ paskirstytų užsakymų tvarkymo (DOM) funkcija.</span><span class="sxs-lookup"><span data-stu-id="63e8a-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="63e8a-105">Puslapyje **Turto rodinys** rodomas aktyvusis turtas ir funkcinės vietos medžio rodinyje.</span><span class="sxs-lookup"><span data-stu-id="63e8a-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="63e8a-106">Todėl galite lengvai gauti turto ryšių su funkcinėmis vietomis apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="63e8a-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="63e8a-107">Be to, galite peržiūrėti išsamią informaciją apie funkcines vietas, turtą ir susijusias komplektavimo specifikacijas (KS).</span><span class="sxs-lookup"><span data-stu-id="63e8a-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="63e8a-108">Taip pat galite greitai peržiūrėti aktyviąsias priežiūros užklausas ir darbo užsakymus, susijusius su turtu.</span><span class="sxs-lookup"><span data-stu-id="63e8a-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="63e8a-109">Pasirinkite **Turto valdymas** \> **Bendra** \> **Turtas** \> **Turto rodinys**.</span><span class="sxs-lookup"><span data-stu-id="63e8a-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="63e8a-110">Norėdami pakeisti puslapyje rodomą rodinį, lauke **Rodinys** pasirinkite naują reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63e8a-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="63e8a-111">Numatytasis rodinys, kuris rodomas atidarius puslapį **Turto rodinys**, priklauso nuo vertės, kuri pasirinkta puslapio **Turto valdymo parametrai** skirtuko **Turtas** lauke **Rodinys**  (**Turto valdymas** \> **Sąranka** \> **Turto valdymo parametrai**).</span><span class="sxs-lookup"><span data-stu-id="63e8a-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="63e8a-112">Dešiniojoje puslapio pusėje „FastTabs“ skirtukuose rodoma pasirinkto rodinio informacija.</span><span class="sxs-lookup"><span data-stu-id="63e8a-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="63e8a-113">Naršymo kelyje, kuris yra rodomas virš medžio rodinio, rodomas dabartinis žymėjimas medžio rodinyje.</span><span class="sxs-lookup"><span data-stu-id="63e8a-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="63e8a-114">Naudojamas toks šio naršymo kelio formatas:</span><span class="sxs-lookup"><span data-stu-id="63e8a-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="63e8a-115">Funkcinės vietos ID / Funkcinės vietos ID (jei yra daugiau nei viena funkcinė vieta) \> Turto ID / Turto ID (jei yra daugiau nei vienas turtas) – Elemento numeris.</span><span class="sxs-lookup"><span data-stu-id="63e8a-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="63e8a-116">Jei medžio rodinyje pasirinkote turtą, galite pasirinkti **Aktyviosios užklausos** arba **Aktyvieji darbo užsakymai**, kad peržiūrėtumėte priežiūros užklausas arba darbo užsakymus, susijusius su turtu.</span><span class="sxs-lookup"><span data-stu-id="63e8a-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="63e8a-117">Taip pat galite pasirinkti **Atidaryti** \> **Funkcinė vieta**, **Turtas** arba **Turto BOM,** kad būtų atidarytas susijęs vaizdas.</span><span class="sxs-lookup"><span data-stu-id="63e8a-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="63e8a-118">Parinktis **Turto funkcinės vietos**, kurią galite pasirinkti lauke **Rodinys**, taip pat yra pasiekiama visose turto peržvalgose, kuriose galite pasirinkti turtą.</span><span class="sxs-lookup"><span data-stu-id="63e8a-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="63e8a-119">Medžio rodinys yra rodomas skirtuke **Turto rodinys**, pavyzdžiui, ten, kur galite [kurti turtą](../objects/create-an-object.md), sukurti priežiūros užklausą arba sukurti darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="63e8a-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>
