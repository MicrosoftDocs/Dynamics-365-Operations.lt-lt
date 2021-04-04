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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5afcb8171b674281faf8100d5c01fdff8d6ff764
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470790"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="3358a-103">Šabloninės KS kūrimas</span><span class="sxs-lookup"><span data-stu-id="3358a-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3358a-104">Galite sukurti šabloninę KS naudodamiesi bet kuriuo iš toliau pateiktų būdų.</span><span class="sxs-lookup"><span data-stu-id="3358a-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="3358a-105">Visiems būdams laukai **Pradžios data** ir **Pabaigos data** yra pasirenkamieji ir skirti tik informacijai.</span><span class="sxs-lookup"><span data-stu-id="3358a-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="3358a-106">KS ruošinio kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="3358a-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="3358a-107">Eikite į **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.</span><span class="sxs-lookup"><span data-stu-id="3358a-107">Go to **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="3358a-108">Pasirinkę **Naujas** atidarykite formą **Kurti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="3358a-108">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="3358a-109">Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite parinktį **Rankiniu būdu**.</span><span class="sxs-lookup"><span data-stu-id="3358a-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="3358a-110">Lauke **Prekės numeris** įveskite **KS** tipo prekę.</span><span class="sxs-lookup"><span data-stu-id="3358a-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="3358a-111">Lauke **Pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="3358a-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="3358a-112">Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="3358a-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="3358a-113">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3358a-113">Select **OK**.</span></span>

<span data-ttu-id="3358a-114">Sukuriama nauja tuščia šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="3358a-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="3358a-115">KS ruošinio, paremto kitu KS ruošiniu, kūrimas</span><span class="sxs-lookup"><span data-stu-id="3358a-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="3358a-116">Pasirinkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.</span><span class="sxs-lookup"><span data-stu-id="3358a-116">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="3358a-117">Pasirinkę **Naujas** atidarykite formą **Kurti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="3358a-117">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="3358a-118">Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite parinktį **Šabloninė KS**.</span><span class="sxs-lookup"><span data-stu-id="3358a-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="3358a-119">Lauke **Nuorodos numeris** pasirinkite esamą KS ruošinį, kurį norite kopijuoti į savo naują KS ruošinį.</span><span class="sxs-lookup"><span data-stu-id="3358a-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="3358a-120">Lauke **Pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="3358a-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="3358a-121">Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="3358a-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="3358a-122">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3358a-122">Select **OK**.</span></span>

<span data-ttu-id="3358a-123">Sukuriama nauja šabloninė KS su eilutėmis, atitinkančiomis eilutes originalioje šabloninėje KS.</span><span class="sxs-lookup"><span data-stu-id="3358a-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="3358a-124">KS ruošinio, paremto prekės KS kūrimas</span><span class="sxs-lookup"><span data-stu-id="3358a-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="3358a-125">Pasirinkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.</span><span class="sxs-lookup"><span data-stu-id="3358a-125">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="3358a-126">Pasirinkę **Naujas** atidarykite formą **Kurti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="3358a-126">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="3358a-127">Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite **KS**.</span><span class="sxs-lookup"><span data-stu-id="3358a-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="3358a-128">Lauke **Nuorodos numeris** pasirinkite KS versiją.</span><span class="sxs-lookup"><span data-stu-id="3358a-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="3358a-129">KS tipo prekė nukopijuojama į **Prekės numeris**.</span><span class="sxs-lookup"><span data-stu-id="3358a-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="3358a-130">Lauke **Pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="3358a-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="3358a-131">Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="3358a-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="3358a-132">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3358a-132">Select **OK**.</span></span>

<span data-ttu-id="3358a-133">Naujas KS ruošinys sukurtas, naudojant eilutes, atitinkančias KS eilutes, išvardytas **Komplektavimo specifikacijos**.</span><span class="sxs-lookup"><span data-stu-id="3358a-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="3358a-134">KS ruošinio, paremto gamybos KS, kūrimas</span><span class="sxs-lookup"><span data-stu-id="3358a-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="3358a-135">Pasirinkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.</span><span class="sxs-lookup"><span data-stu-id="3358a-135">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="3358a-136">Pasirinkę **Naujas** atidarykite formą **Kurti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="3358a-136">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="3358a-137">Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite **Gamyba**.</span><span class="sxs-lookup"><span data-stu-id="3358a-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="3358a-138">Lauke **Nuorodos numeris** pasirinkite gamybos KS.</span><span class="sxs-lookup"><span data-stu-id="3358a-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="3358a-139">Lauke **Pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="3358a-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="3358a-140">Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.</span><span class="sxs-lookup"><span data-stu-id="3358a-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="3358a-141">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3358a-141">Select **OK**.</span></span>

<span data-ttu-id="3358a-142">Naujas KS ruošinys sukurtas, naudojant eilutes, atitinkančias KS eilutes, išvardytas **KS**.</span><span class="sxs-lookup"><span data-stu-id="3358a-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="3358a-143">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="3358a-143">See also</span></span>

[<span data-ttu-id="3358a-144">Šabloninės KS</span><span class="sxs-lookup"><span data-stu-id="3358a-144">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]