--- 
title: "Nustatyti nusidėvėjimo knygas "
description: "Šis užduočių vadovas sukurs naują nusidėvėjimo knygą ir ją susies su ilgalaikio turto grupe."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d06d5f92e91e33dc752bf45ab890c37dfea3888d
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-depreciation-books"></a><span data-ttu-id="23d24-103">Nustatyti nusidėvėjimo knygas </span><span class="sxs-lookup"><span data-stu-id="23d24-103">Set up depreciation books</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23d24-104">Šis užduočių vadovas sukurs naują nusidėvėjimo knygą ir ją susies su ilgalaikio turto grupe.</span><span class="sxs-lookup"><span data-stu-id="23d24-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="23d24-105">Jis naudoja vaidmenį Buhalteris ir USMF juridinio subjekto demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="23d24-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="23d24-106">Kurti nusidėvėjimo knygą</span><span class="sxs-lookup"><span data-stu-id="23d24-106">Create a depreciation book</span></span>
1. <span data-ttu-id="23d24-107">Pasirinkite Ilgalaikis turtas > Nustatymas > Nusidėvėjimo knygos.</span><span class="sxs-lookup"><span data-stu-id="23d24-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="23d24-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="23d24-108">Click New.</span></span>
3. <span data-ttu-id="23d24-109">Lauke Nusidėvėjimo knyga surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="23d24-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="23d24-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="23d24-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="23d24-111">Pažymėkite arba atžymėkite žymės langelį Skaičiuoti nusidėvėjimą.</span><span class="sxs-lookup"><span data-stu-id="23d24-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="23d24-112">Lauke Nusidėvėjimo šablonas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="23d24-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="23d24-113">Sąraše raskite ir pasirinkite norimą nusidėvėjimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="23d24-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="23d24-114">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="23d24-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="23d24-115">Lauke Alternatyvus nusidėvėjimo šablonas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="23d24-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="23d24-116">Sąraše pasirinkite norimą nusidėvėjimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="23d24-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="23d24-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="23d24-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="23d24-118">Visiško nusidėvėjimo šablonas naudojamas neįprastas atvejais papildomai skaičiuojant turto nusidėvėjimą.</span><span class="sxs-lookup"><span data-stu-id="23d24-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="23d24-119">Pavyzdžiui, galite tai naudoti norėdami įrašyti nusidėvėjimą įvykus gamtos katastrofai.</span><span class="sxs-lookup"><span data-stu-id="23d24-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="23d24-120">Pažymėkite arba atžymėkite žymės langelį Kurti nusidėvėjimo koregavimus su pagrindo koregavimais.</span><span class="sxs-lookup"><span data-stu-id="23d24-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="23d24-121">Lauke Kalendorius spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="23d24-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="23d24-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="23d24-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="23d24-123">Susieti nusidėvėjimo knygą su ilgalaikio turto grupe</span><span class="sxs-lookup"><span data-stu-id="23d24-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="23d24-124">Spustelėkite Ilgalaikio turto grupės.</span><span class="sxs-lookup"><span data-stu-id="23d24-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="23d24-125">Lauke Ilgalaikio turto grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="23d24-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="23d24-126">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="23d24-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="23d24-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="23d24-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="23d24-128">Lauke Nusidėvėjimo konvencija pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="23d24-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="23d24-129">Lauke Dėvėjimo laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="23d24-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="23d24-130">Atkreipkite dėmesį, kad lauko Nusidėvėjimo laikotarpiai reikšmė apskaičiuojama nustačius dėvėjimo laiką.</span><span class="sxs-lookup"><span data-stu-id="23d24-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  


