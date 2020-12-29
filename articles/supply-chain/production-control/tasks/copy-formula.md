---
title: Nukopijuokite formulę
description: Šios procedūros tikslas yra sukurti formulę, kuri apimtų tuos pačius ingredientus, kaip ir esama formulė, tačiau su nedideliais skirtumais.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26524f886a8af545869bacef4d57bfc14c0ed225
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433320"
---
# <a name="copy-a-formula"></a><span data-ttu-id="b8d51-103">Nukopijuokite formulę</span><span class="sxs-lookup"><span data-stu-id="b8d51-103">Copy a formula</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8d51-104">Šios procedūros tikslas yra sukurti formulę, kuri apimtų tuos pačius ingredientus, kaip ir esama formulė, tačiau su nedideliais skirtumais.</span><span class="sxs-lookup"><span data-stu-id="b8d51-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="b8d51-105">Norėdami sukurti formulės eilutes, galite kopijavimo funkcijos pagalba nukopijuoti esamą formulę, kuri turi daugumą jums reikalingų ingredientų.</span><span class="sxs-lookup"><span data-stu-id="b8d51-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="b8d51-106">Tada galite atlikti būtinus atskirų eilučių pakeitimus naujojoje versijoje.</span><span class="sxs-lookup"><span data-stu-id="b8d51-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="b8d51-107">Naudojant kopijavimo funkciją nereikės sukurti keleto beveik identiškų formulių.</span><span class="sxs-lookup"><span data-stu-id="b8d51-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="b8d51-108">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USP2.</span><span class="sxs-lookup"><span data-stu-id="b8d51-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="b8d51-109">Kurti formulę</span><span class="sxs-lookup"><span data-stu-id="b8d51-109">Create a formula</span></span>
1. <span data-ttu-id="b8d51-110">Pasirinkite Produkto informacijos valdymas > Komplektavimo specifikacijos ir formulės > Formulės.</span><span class="sxs-lookup"><span data-stu-id="b8d51-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="b8d51-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b8d51-111">Click New.</span></span>
3. <span data-ttu-id="b8d51-112">Lauke „Formulė“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b8d51-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="b8d51-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b8d51-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b8d51-114">Įveskite prasmingą formulės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b8d51-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="b8d51-115">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b8d51-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b8d51-116">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b8d51-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b8d51-117">Lauke Prekių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b8d51-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b8d51-118">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b8d51-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="b8d51-119">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b8d51-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="b8d51-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b8d51-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="b8d51-121">Kopijuoti formulės eilutes</span><span class="sxs-lookup"><span data-stu-id="b8d51-121">Copy formula lines</span></span>
1. <span data-ttu-id="b8d51-122">Veiksmų srityje spustelėkite „Formulė“.</span><span class="sxs-lookup"><span data-stu-id="b8d51-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="b8d51-123">Spustelėkite Kopijuoti.</span><span class="sxs-lookup"><span data-stu-id="b8d51-123">Click Copy.</span></span>
3. <span data-ttu-id="b8d51-124">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b8d51-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b8d51-125">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b8d51-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b8d51-126">Lauke „Formulės versija“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b8d51-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b8d51-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b8d51-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b8d51-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b8d51-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="b8d51-129">Koreguoti nukopijuotas formulės eilutes</span><span class="sxs-lookup"><span data-stu-id="b8d51-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="b8d51-130">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b8d51-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="b8d51-131">Spustelėkite Naikinti.</span><span class="sxs-lookup"><span data-stu-id="b8d51-131">Click Delete.</span></span>
3. <span data-ttu-id="b8d51-132">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="b8d51-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="b8d51-133">Tvirtinti formulę</span><span class="sxs-lookup"><span data-stu-id="b8d51-133">Approve formula</span></span>
1. <span data-ttu-id="b8d51-134">Veiksmų srityje spustelėkite „Formulė“.</span><span class="sxs-lookup"><span data-stu-id="b8d51-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="b8d51-135">Spustelėkite „Tvirtinti formulę“.</span><span class="sxs-lookup"><span data-stu-id="b8d51-135">Click Approve formula.</span></span>
3. <span data-ttu-id="b8d51-136">Lauke Patvirtino spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b8d51-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b8d51-137">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b8d51-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b8d51-138">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="b8d51-138">Click Select.</span></span>
6. <span data-ttu-id="b8d51-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b8d51-139">Click OK.</span></span>

