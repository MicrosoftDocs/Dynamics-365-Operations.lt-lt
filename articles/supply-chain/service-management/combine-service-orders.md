---
title: "Jungti aptarnavimo užsakymus"
description: "Galite jungti aptarnavimo užsakymus."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8bc28d03d36d184e4bf41de2c50dac15e6d7813c
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="combine-service-orders"></a><span data-ttu-id="83c6e-103">Jungti aptarnavimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="83c6e-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="83c6e-104">Kurdami aptarnavimo užsakymo eilutes automatiškai, formoje **Aptarnavimo sutartys** galite pasirinkti vieną iš toliau pateiktų parinkčių, skirtų nurodyti, kaip juos norite grupuoti:</span><span class="sxs-lookup"><span data-stu-id="83c6e-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="83c6e-105">**Pagal aptarnavimo sutartį**</span><span class="sxs-lookup"><span data-stu-id="83c6e-105">**By service agreement**</span></span>

  - <span data-ttu-id="83c6e-106">**Pagal aptarnavimo užduotį**</span><span class="sxs-lookup"><span data-stu-id="83c6e-106">**By service task**</span></span>

  - <span data-ttu-id="83c6e-107">**Pagal darbuotoją**</span><span class="sxs-lookup"><span data-stu-id="83c6e-107">**By employee**</span></span>

  - <span data-ttu-id="83c6e-108">**Pagal aptarnavimo objektą**</span><span class="sxs-lookup"><span data-stu-id="83c6e-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="83c6e-109">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="83c6e-109">Example</span></span>

<span data-ttu-id="83c6e-110">Sukūrėte aptarnavimo sutartį, kurios pradžios data yra 2007-03-31.</span><span class="sxs-lookup"><span data-stu-id="83c6e-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="83c6e-111">Lauke **Jungti aptarnavimo užsakymus** nurodykite **Pagal aptarnavimo objektą**.</span><span class="sxs-lookup"><span data-stu-id="83c6e-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="83c6e-112">Tada sukuriate šias aptarnavimo sutarties eilutes:</span><span class="sxs-lookup"><span data-stu-id="83c6e-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="83c6e-113">Sutarties eilutės numeris</span><span class="sxs-lookup"><span data-stu-id="83c6e-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="83c6e-114">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="83c6e-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="83c6e-115">aprašymas</span><span class="sxs-lookup"><span data-stu-id="83c6e-115">Description</span></span></p></th>
<th><p><span data-ttu-id="83c6e-116">Intervalas</span><span class="sxs-lookup"><span data-stu-id="83c6e-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="83c6e-117">Aptarnavimo objektas</span><span class="sxs-lookup"><span data-stu-id="83c6e-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="83c6e-118">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="83c6e-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83c6e-119">1</span><span class="sxs-lookup"><span data-stu-id="83c6e-119">1</span></span></p></td>
<td><p><span data-ttu-id="83c6e-120"><strong>Valanda</strong></span><span class="sxs-lookup"><span data-stu-id="83c6e-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="83c6e-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="83c6e-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="83c6e-122">Savaitinis</span><span class="sxs-lookup"><span data-stu-id="83c6e-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="83c6e-123">X-1</span><span class="sxs-lookup"><span data-stu-id="83c6e-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="83c6e-124">2007-04-01</span><span class="sxs-lookup"><span data-stu-id="83c6e-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83c6e-125">2</span><span class="sxs-lookup"><span data-stu-id="83c6e-125">2</span></span></p></td>
<td><p><span data-ttu-id="83c6e-126"><strong>Valanda</strong></span><span class="sxs-lookup"><span data-stu-id="83c6e-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="83c6e-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="83c6e-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="83c6e-128">Kas dvi savaites</span><span class="sxs-lookup"><span data-stu-id="83c6e-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="83c6e-129">X-2</span><span class="sxs-lookup"><span data-stu-id="83c6e-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="83c6e-130">2007-04-01</span><span class="sxs-lookup"><span data-stu-id="83c6e-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83c6e-131">3</span><span class="sxs-lookup"><span data-stu-id="83c6e-131">3</span></span></p></td>
<td><p><span data-ttu-id="83c6e-132"><strong>Valanda</strong></span><span class="sxs-lookup"><span data-stu-id="83c6e-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="83c6e-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="83c6e-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="83c6e-134">Savaitinis</span><span class="sxs-lookup"><span data-stu-id="83c6e-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="83c6e-135">X-2</span><span class="sxs-lookup"><span data-stu-id="83c6e-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="83c6e-136">2007-04-01</span><span class="sxs-lookup"><span data-stu-id="83c6e-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="83c6e-137">Nenurodote jokios aptarnavimo sutarties eilutės laiko lango.</span><span class="sxs-lookup"><span data-stu-id="83c6e-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="83c6e-138">Dėl to aptarnavimo užsakymo eilutės nebus perkeltos iš apskaičiuotos dienos, į kurią jos patenka.</span><span class="sxs-lookup"><span data-stu-id="83c6e-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="83c6e-139">Toliau formoje **Kurti aptarnavimo užsakymus** sugeneruokite aptarnavimo užsakymo eilutes nuo 2007-04-01 iki 2007-04-30.</span><span class="sxs-lookup"><span data-stu-id="83c6e-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="83c6e-140">Iš viso sukuriama 10 aptarnavimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="83c6e-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="83c6e-141">Kadangi jūsų pasirinkti sujungti nustatymai buvo **Pagal aptarnavimo objektą**, visuose sukurtuose aptarnavimo užsakymuose yra tik tos aptarnavimo užsakymo eilutės, kuriose nurodytas vienas konkretus aptarnavimo objektas.</span><span class="sxs-lookup"><span data-stu-id="83c6e-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="83c6e-142">Aptarnavimo užsakymo eilutės, sugeneruotos aptarnavimo sutartyje, kurių aptarnavimo data ir objektas yra tokie patys, sujungiamos į vieną aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="83c6e-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="83c6e-143">Šiame pavyzdyje kalendoriuje, kuris nurodytas formoje <STRONG>Aptarnavimo valdymo parametrai</STRONG>, nėra uždarytų dienų.</span><span class="sxs-lookup"><span data-stu-id="83c6e-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="83c6e-144">Papildomas aptarnavimo užsakymo eilučių grupavimas į aptarnavimo užsakymus vykdomas pagal bet kokį laiko langą, kurį nurodote aptarnavimo sutarties eilutėse.</span><span class="sxs-lookup"><span data-stu-id="83c6e-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="83c6e-145">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="83c6e-145">See also</span></span>

[<span data-ttu-id="83c6e-146">Automatiškai kurkite aptarnavimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="83c6e-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  



