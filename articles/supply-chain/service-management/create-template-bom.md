---
title: Šabloninės KS kūrimas
description: Galite sukurti šabloninę KS naudodamiesi įvairiais būdais.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2e06283f3b95c5ff6b4376bba63cf5a42d5feeb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433714"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="07af8-103">Šabloninės KS kūrimas</span><span class="sxs-lookup"><span data-stu-id="07af8-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="07af8-104">Galite sukurti šabloninę KS naudodamiesi bet kuriuo iš toliau pateiktų būdų.</span><span class="sxs-lookup"><span data-stu-id="07af8-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="07af8-105">Visiems būdams laukai **Pradžios data** ir **Pabaigos data** yra pasirenkamieji ir skirti tik informacijai.</span><span class="sxs-lookup"><span data-stu-id="07af8-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="07af8-106">KS ruošinio kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="07af8-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="07af8-107">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.</span><span class="sxs-lookup"><span data-stu-id="07af8-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="07af8-108">Paspaudę CTRL+N atidarykite formą **Kurti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="07af8-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="07af8-109">Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite parinktį **Rankiniu būdu**.</span><span class="sxs-lookup"><span data-stu-id="07af8-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="07af8-110">Lauke **Prekės numeris** įveskite **KS** tipo prekę.</span><span class="sxs-lookup"><span data-stu-id="07af8-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="07af8-111">Lauke **Pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="07af8-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="07af8-112">Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="07af8-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="07af8-113">Spustelėkite **GERAI**.</span><span class="sxs-lookup"><span data-stu-id="07af8-113">Click **OK**.</span></span>

<span data-ttu-id="07af8-114">Sukuriama nauja tuščia šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="07af8-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="07af8-115">KS ruošinio, paremto kitu KS ruošiniu, kūrimas</span><span class="sxs-lookup"><span data-stu-id="07af8-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="07af8-116">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.</span><span class="sxs-lookup"><span data-stu-id="07af8-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="07af8-117">Paspaudę CTRL+N atidarykite formą **Kurti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="07af8-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="07af8-118">Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite parinktį **Šabloninė KS**.</span><span class="sxs-lookup"><span data-stu-id="07af8-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="07af8-119">Lauke **Nuorodos numeris** pasirinkite esamą KS ruošinį, kurį norite kopijuoti į savo naują KS ruošinį.</span><span class="sxs-lookup"><span data-stu-id="07af8-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="07af8-120">Lauke **Pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="07af8-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="07af8-121">Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="07af8-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="07af8-122">Spustelėkite **GERAI**.</span><span class="sxs-lookup"><span data-stu-id="07af8-122">Click **OK**.</span></span>

<span data-ttu-id="07af8-123">Sukuriama nauja šabloninė KS su eilutėmis, atitinkančiomis eilutes originalioje šabloninėje KS.</span><span class="sxs-lookup"><span data-stu-id="07af8-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="07af8-124">KS ruošinio, paremto prekės KS kūrimas</span><span class="sxs-lookup"><span data-stu-id="07af8-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="07af8-125">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.</span><span class="sxs-lookup"><span data-stu-id="07af8-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="07af8-126">Paspaudę CTRL+N atidarykite formą **Kurti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="07af8-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="07af8-127">Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite **KS**.</span><span class="sxs-lookup"><span data-stu-id="07af8-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="07af8-128">Lauke **Nuorodos numeris** pasirinkite KS versiją.</span><span class="sxs-lookup"><span data-stu-id="07af8-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="07af8-129">KS tipo prekė nukopijuojama į **Prekės numeris**.</span><span class="sxs-lookup"><span data-stu-id="07af8-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="07af8-130">Lauke **Pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="07af8-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="07af8-131">Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="07af8-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="07af8-132">Spustelėkite **GERAI**.</span><span class="sxs-lookup"><span data-stu-id="07af8-132">Click **OK**.</span></span>

<span data-ttu-id="07af8-133">Naujas KS ruošinys sukurtas, naudojant eilutes, atitinkančias KS eilutes, išvardytas **Komplektavimo specifikacijos**.</span><span class="sxs-lookup"><span data-stu-id="07af8-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="07af8-134">KS ruošinio, paremto gamybos KS, kūrimas</span><span class="sxs-lookup"><span data-stu-id="07af8-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="07af8-135">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.</span><span class="sxs-lookup"><span data-stu-id="07af8-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="07af8-136">Paspaudę CTRL+N atidarykite formą **Kurti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="07af8-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="07af8-137">Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite **Gamyba**.</span><span class="sxs-lookup"><span data-stu-id="07af8-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="07af8-138">Lauke **Nuorodos numeris** pasirinkite gamybos KS.</span><span class="sxs-lookup"><span data-stu-id="07af8-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="07af8-139">Lauke **Pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="07af8-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="07af8-140">Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="07af8-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="07af8-141">Spustelėkite **GERAI**.</span><span class="sxs-lookup"><span data-stu-id="07af8-141">Click **OK**.</span></span>

<span data-ttu-id="07af8-142">Naujas KS ruošinys sukurtas, naudojant eilutes, atitinkančias KS eilutes, išvardytas **KS**.</span><span class="sxs-lookup"><span data-stu-id="07af8-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="07af8-143">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="07af8-143">See also</span></span>

[<span data-ttu-id="07af8-144">Šabloninės KS</span><span class="sxs-lookup"><span data-stu-id="07af8-144">Template BOMs</span></span>](template-boms.md)

  


