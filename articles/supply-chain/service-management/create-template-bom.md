---
title: Šabloninės KS kūrimas
description: Galite sukurti šabloninę KS naudodamiesi įvairiais būdais.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 781df7611ec1e3ee9d3013f971232700df38ada0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836307"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="897d8-103">Šabloninės KS kūrimas</span><span class="sxs-lookup"><span data-stu-id="897d8-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="897d8-104">Galite sukurti šabloninę KS naudodamiesi bet kuriuo iš toliau pateiktų būdų.</span><span class="sxs-lookup"><span data-stu-id="897d8-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="897d8-105">Visiems būdams laukai **Pradžios data** ir **Pabaigos data** yra pasirenkamieji ir skirti tik informacijai.</span><span class="sxs-lookup"><span data-stu-id="897d8-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="897d8-106">KS ruošinio kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="897d8-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="897d8-107">Eikite į **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.</span><span class="sxs-lookup"><span data-stu-id="897d8-107">Go to **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="897d8-108">Pasirinkę **Naujas** atidarykite formą **Kurti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="897d8-108">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="897d8-109">Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite parinktį **Rankiniu būdu**.</span><span class="sxs-lookup"><span data-stu-id="897d8-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="897d8-110">Lauke **Prekės numeris** įveskite **KS** tipo prekę.</span><span class="sxs-lookup"><span data-stu-id="897d8-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="897d8-111">Lauke **Pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="897d8-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="897d8-112">Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="897d8-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="897d8-113">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="897d8-113">Select **OK**.</span></span>

<span data-ttu-id="897d8-114">Sukuriama nauja tuščia šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="897d8-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="897d8-115">KS ruošinio, paremto kitu KS ruošiniu, kūrimas</span><span class="sxs-lookup"><span data-stu-id="897d8-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="897d8-116">Pasirinkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.</span><span class="sxs-lookup"><span data-stu-id="897d8-116">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="897d8-117">Pasirinkę **Naujas** atidarykite formą **Kurti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="897d8-117">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="897d8-118">Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite parinktį **Šabloninė KS**.</span><span class="sxs-lookup"><span data-stu-id="897d8-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="897d8-119">Lauke **Nuorodos numeris** pasirinkite esamą KS ruošinį, kurį norite kopijuoti į savo naują KS ruošinį.</span><span class="sxs-lookup"><span data-stu-id="897d8-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="897d8-120">Lauke **Pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="897d8-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="897d8-121">Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="897d8-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="897d8-122">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="897d8-122">Select **OK**.</span></span>

<span data-ttu-id="897d8-123">Sukuriama nauja šabloninė KS su eilutėmis, atitinkančiomis eilutes originalioje šabloninėje KS.</span><span class="sxs-lookup"><span data-stu-id="897d8-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="897d8-124">KS ruošinio, paremto prekės KS kūrimas</span><span class="sxs-lookup"><span data-stu-id="897d8-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="897d8-125">Pasirinkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.</span><span class="sxs-lookup"><span data-stu-id="897d8-125">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="897d8-126">Pasirinkę **Naujas** atidarykite formą **Kurti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="897d8-126">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="897d8-127">Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite **KS**.</span><span class="sxs-lookup"><span data-stu-id="897d8-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="897d8-128">Lauke **Nuorodos numeris** pasirinkite KS versiją.</span><span class="sxs-lookup"><span data-stu-id="897d8-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="897d8-129">KS tipo prekė nukopijuojama į **Prekės numeris**.</span><span class="sxs-lookup"><span data-stu-id="897d8-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="897d8-130">Lauke **Pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="897d8-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="897d8-131">Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="897d8-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="897d8-132">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="897d8-132">Select **OK**.</span></span>

<span data-ttu-id="897d8-133">Naujas KS ruošinys sukurtas, naudojant eilutes, atitinkančias KS eilutes, išvardytas **Komplektavimo specifikacijos**.</span><span class="sxs-lookup"><span data-stu-id="897d8-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="897d8-134">KS ruošinio, paremto gamybos KS, kūrimas</span><span class="sxs-lookup"><span data-stu-id="897d8-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="897d8-135">Pasirinkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.</span><span class="sxs-lookup"><span data-stu-id="897d8-135">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="897d8-136">Pasirinkę **Naujas** atidarykite formą **Kurti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="897d8-136">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="897d8-137">Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite **Gamyba**.</span><span class="sxs-lookup"><span data-stu-id="897d8-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="897d8-138">Lauke **Nuorodos numeris** pasirinkite gamybos KS.</span><span class="sxs-lookup"><span data-stu-id="897d8-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="897d8-139">Lauke **Pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="897d8-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="897d8-140">Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="897d8-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="897d8-141">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="897d8-141">Select **OK**.</span></span>

<span data-ttu-id="897d8-142">Naujas KS ruošinys sukurtas, naudojant eilutes, atitinkančias KS eilutes, išvardytas **KS**.</span><span class="sxs-lookup"><span data-stu-id="897d8-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="897d8-143">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="897d8-143">See also</span></span>

[<span data-ttu-id="897d8-144">Šabloninės KS</span><span class="sxs-lookup"><span data-stu-id="897d8-144">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]