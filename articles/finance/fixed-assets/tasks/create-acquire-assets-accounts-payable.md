---
title: Kurti ir įsigyti turtą iš mokėtinų sumų
description: Šis užduočių vadovas apžvelgs ilgalaikio turto sukūrimą ir įsigyjimą, naudojant pirkimo procesą.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cb9a37c65fb8eab4db6084b91a71c13a45ba42c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446024"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="87f76-103">Kurti ir įsigyti turtą iš mokėtinų sumų</span><span class="sxs-lookup"><span data-stu-id="87f76-103">Create and acquire assets from Accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="87f76-104">Šis užduočių vadovas apžvelgs ilgalaikio turto sukūrimą ir įsigyjimą, naudojant pirkimo procesą.</span><span class="sxs-lookup"><span data-stu-id="87f76-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="87f76-105">Jis naudoja buhalterio ir mokėtinų sumų tarnautojus bei demonstracinę įmonę USMF.</span><span class="sxs-lookup"><span data-stu-id="87f76-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="87f76-106">Nustatyti ilgalaikio turto parametrus</span><span class="sxs-lookup"><span data-stu-id="87f76-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="87f76-107">**Naršymo sritis** eikite į **Moduliai > Ilgalaikis turtas > Sąranka > Ilgalaikio turto parametrai**.</span><span class="sxs-lookup"><span data-stu-id="87f76-107">In the **Navigation pane**, go to **Modules > Fixed assets > Setup > Fixed assets parameters**.</span></span>
2. <span data-ttu-id="87f76-108">Išplėskite „fastTab“ **Pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="87f76-108">Expand the **Purchase orders** fastTab.</span></span>
3. <span data-ttu-id="87f76-109">Pažymėkite žymės langelį **Leisti turto įsigijimą iš pirkimo**.</span><span class="sxs-lookup"><span data-stu-id="87f76-109">Check the **Allow asset acquisition from Purchasing** checkbox.</span></span>
4. <span data-ttu-id="87f76-110">Pažymėkite žymės langelį **Kurti turtą gaunant produktą arba registruojant sąskaitą faktūrą**.</span><span class="sxs-lookup"><span data-stu-id="87f76-110">Check the **Create asset during product receipt or invoice posting** checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="87f76-111">Kurti naują tiekėjo SF</span><span class="sxs-lookup"><span data-stu-id="87f76-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="87f76-112">**Naršymo sritis** eikite į **Moduliai > Mokėtinos sumos > Darbo sritys > Tiekėjo sąskaitos faktūros įrašas**.</span><span class="sxs-lookup"><span data-stu-id="87f76-112">In the **Navigation pane**, go to **Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="87f76-113">Spustelėkite **Nauja tiekėjo sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="87f76-113">Click **New vendor invoice**.</span></span>
3. <span data-ttu-id="87f76-114">Lauke **Sąskaitos faktūros sąskaita** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="87f76-114">In the **Invoice account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="87f76-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="87f76-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="87f76-116">Lauke **Numeris** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="87f76-116">In the **Number** field, type a value.</span></span>
6. <span data-ttu-id="87f76-117">Lauke **Registravimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="87f76-117">In the **Posting date** field, enter a date.</span></span>
7. <span data-ttu-id="87f76-118">Spustelėkite **Pridėti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="87f76-118">Click **Add line**.</span></span>
8. <span data-ttu-id="87f76-119">Lauke **Prekės numeris** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="87f76-119">In the **Item number** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="87f76-120">Norint įsigyti ilgalaikio turto, galima naudoti atsargose nelaikomų prekių arba įsigijimo kategorijas.</span><span class="sxs-lookup"><span data-stu-id="87f76-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="87f76-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="87f76-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="87f76-122">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="87f76-122">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="87f76-123">Viena SF eilutė sukurs tik vieną ilgalaikį turtą, neatsižvelgiant į kiekį.</span><span class="sxs-lookup"><span data-stu-id="87f76-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span> <span data-ttu-id="87f76-124">Į ilgalaikio turto kiekį bus perkelta SF kiekio lauko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="87f76-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="87f76-125">Lauke **Vieneto kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="87f76-125">In the **Unit price** field, enter a number.</span></span>
12. <span data-ttu-id="87f76-126">Išplėskite FastTab **Eilutės informacija**.</span><span class="sxs-lookup"><span data-stu-id="87f76-126">Expand the **Line details** fastTab.</span></span>
13. <span data-ttu-id="87f76-127">Spustelėkite skirtuką **Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="87f76-127">Click the **Fixed assets** tab.</span></span>
14. <span data-ttu-id="87f76-128">Pažymėkite žymės langelį **Kurti naują ilgalaikį turtą**.</span><span class="sxs-lookup"><span data-stu-id="87f76-128">Check the **Create a new fixed asset** checkbox.</span></span>
15. <span data-ttu-id="87f76-129">Lauke **Ilgalaikio turto grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="87f76-129">In the **Fixed asset group** field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="87f76-130">Sąraše pasirinkite ilgalaikio turto grupę, kuri bus naudojama kuriant naująjį ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="87f76-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="87f76-131">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="87f76-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="87f76-132">Spustelėkite **Registruoti.**</span><span class="sxs-lookup"><span data-stu-id="87f76-132">Click **Post**.</span></span> <span data-ttu-id="87f76-133">Ilgalaikis turtas bus sukurtas ir įsigytas užregistravus SF.</span><span class="sxs-lookup"><span data-stu-id="87f76-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

