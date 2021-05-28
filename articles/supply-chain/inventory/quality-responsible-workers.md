---
title: Darbuotojai, atsakingi už neatitikties tvirtinimą
description: Šioje temoje aprašoma, kaip konfigūruoti darbuotojus, atsakingus už neatitikimų tvirtinimą.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d3f647de2c188661c2c9c5f31e2642c3f8ca0b5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021785"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="f0a01-103">Darbuotojai, atsakingi už neatitikties tvirtinimą</span><span class="sxs-lookup"><span data-stu-id="f0a01-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0a01-104">Šioje temoje aprašoma, kaip konfigūruoti darbuotojus, atsakingus už neatitikimų tvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="f0a01-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="f0a01-105">Neatitiktis turi būti patvirtintos prieš tai, kai vartotojai gali pradėti įvesti informaciją, pvz., taisymus ar operacijas.</span><span class="sxs-lookup"><span data-stu-id="f0a01-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="f0a01-106">Kad vartotojai galėtų patvirtinti arba atmesti neatitiktis, jų vartotojo ID (vartotojo įrašas) turi būti susietas su darbuotojo įrašu.</span><span class="sxs-lookup"><span data-stu-id="f0a01-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="f0a01-107">Galite pasirinktinai konfigūruoti už kokybę atsakingus darbuotojus ir leisti vienam darbuotojui patvirtinti darbą kito darbuotojo vardu.</span><span class="sxs-lookup"><span data-stu-id="f0a01-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="f0a01-108">Leidimas vartotojui apdoroti neatitiktis</span><span class="sxs-lookup"><span data-stu-id="f0a01-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="f0a01-109">Kad vartotojas galėtų patvirtinti arba atmesti neatitiktis, susiekite jų vartotojo ID (vartotojo įrašas) su darbuotojo įrašu.</span><span class="sxs-lookup"><span data-stu-id="f0a01-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="f0a01-110">Tada patvirtinimo laukus galima nustatyti automatiškai, o dabartiniam vartotojui galima automatiškai įvesti tabelį.</span><span class="sxs-lookup"><span data-stu-id="f0a01-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="f0a01-111">Prieš vartotojui naudojant dokumento įrašus, turite taip pat suaktyvinti dokumento tvarkymą jų vartotojų parinktyse.</span><span class="sxs-lookup"><span data-stu-id="f0a01-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="f0a01-112">Eikite į **Sistemos administravimas \> Vartotojai \> Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="f0a01-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="f0a01-113">Raskite ir atidarykite vartotoją, kuris turėtų patvirtinti arba atmesti neatitiktis.</span><span class="sxs-lookup"><span data-stu-id="f0a01-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="f0a01-114">Lauke **Asmuo** nustatykite darbuotojo, susijusio su dabartiniu vartotojo įrašu, vardą.</span><span class="sxs-lookup"><span data-stu-id="f0a01-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="f0a01-115">Veiksmų srityje pasirinkite **Vartotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="f0a01-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="f0a01-116">Dabartinio **vartotojo** įrašo pasirinkčių puslapyje skirtuke **Nuostatos** nustatykite **pasirinktį Įgalinti dokumentų tvarkymą** kaip *Taip*.</span><span class="sxs-lookup"><span data-stu-id="f0a01-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="f0a01-117">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="f0a01-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="f0a01-118">Nustatyti už kokybę atsakingus darbuotojus</span><span class="sxs-lookup"><span data-stu-id="f0a01-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="f0a01-119">Eikite į **Atsargų valdymas \> Nustatymas \> Kokybės kontrolė \> Darbuotojo atsakomybė už kokybę**.</span><span class="sxs-lookup"><span data-stu-id="f0a01-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="f0a01-120">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f0a01-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="f0a01-121">Lauke **Darbuotojas** pasirinkite darbuotoją, kuris įveda kokybės duomenis.</span><span class="sxs-lookup"><span data-stu-id="f0a01-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="f0a01-122">Lauke **Atsakingas darbuotojas** pasirinkite darbuotoją, kurio vardu įveda darbą pasirinktas darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="f0a01-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="f0a01-123">Kai neatitiktis sukuriamos ir atnaujinamos, šis darbuotojas bus įvestas pagal numatytuosius parametrus **darbuotojo** laukuose.</span><span class="sxs-lookup"><span data-stu-id="f0a01-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0a01-124">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f0a01-124">Additional resources</span></span>

- [<span data-ttu-id="f0a01-125">Kokybės valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="f0a01-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="f0a01-126">Įjungti kiekio ir neatitikties valdymą</span><span class="sxs-lookup"><span data-stu-id="f0a01-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="f0a01-127">Kokybės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f0a01-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="f0a01-128">Neatitikimų sulaikymo zonos</span><span class="sxs-lookup"><span data-stu-id="f0a01-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="f0a01-129">Neatitikimų diagnostikos tipai</span><span class="sxs-lookup"><span data-stu-id="f0a01-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="f0a01-130">Neatitikimų kokybės mokesčiai</span><span class="sxs-lookup"><span data-stu-id="f0a01-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="f0a01-131">Neatitikties operacijos</span><span class="sxs-lookup"><span data-stu-id="f0a01-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="f0a01-132">Sandėlio procesų kokybės valdymas</span><span class="sxs-lookup"><span data-stu-id="f0a01-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
