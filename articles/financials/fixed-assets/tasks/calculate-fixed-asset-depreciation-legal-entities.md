--- 
title: "Juridinių subjektų ilgalaikio turto nusidėvėjimo skaičiavimas"
description: "Šioje procedūroje rodoma, kaip nustatyti ir vykdyti kelių juridinių subjektų nusidėvėjimo procesą."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 662554b1b6bed63e5017aad3a292dad7a2f0bcea
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="9063f-103">Juridinių subjektų ilgalaikio turto nusidėvėjimo skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="9063f-103">Calculate fixed asset depreciation across legal entities</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9063f-104">Ilgalaikio turto nusidėvėjimą tarp juridinių subjektų galima vykdyti vienu veiksmu.</span><span class="sxs-lookup"><span data-stu-id="9063f-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="9063f-105">Šioje procedūroje rodoma, kaip nustatyti ir vykdyti kelių juridinių subjektų procesą.</span><span class="sxs-lookup"><span data-stu-id="9063f-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="9063f-106">Joje naudojamas buhalterio vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="9063f-106">It uses the accountant role.</span></span>  

<span data-ttu-id="9063f-107">Šiame įraše naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="9063f-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="9063f-108">Papildoma veiksmų (16) užduotis: visos įmonės nusidėvėjimo vykdymo žurnalų nustatymas.</span><span class="sxs-lookup"><span data-stu-id="9063f-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="9063f-109">Pirmiausia turite nustatyti atskiro juridinio subjekto žurnalus, kurie bus naudojami atliekant visos įmonės nusidėvėjimo vykdymą.</span><span class="sxs-lookup"><span data-stu-id="9063f-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="9063f-110">Eikite į Ilgalaikis turtas > Nustatymas > Ilgalaikio turto parametrai.</span><span class="sxs-lookup"><span data-stu-id="9063f-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="9063f-111">Išplėskite ilgalaikio turto pasiūlymų skyrių.</span><span class="sxs-lookup"><span data-stu-id="9063f-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="9063f-112">Sukurkite įrašą su žurnalo pavadinimu, kuris bus naudojamas kiekviename juridinio subjekto registravimo sluoksnyje.</span><span class="sxs-lookup"><span data-stu-id="9063f-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="9063f-113">Jei nusidėvėjimo knygos neregistruojamos didžiojoje knygoje, kartu su susietu žurnalu reikia pasirinkti registravimo sluoksnį Nėra.</span><span class="sxs-lookup"><span data-stu-id="9063f-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="9063f-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9063f-114">Click Add.</span></span> 
4. <span data-ttu-id="9063f-115">Lauke Registravimo sluoksnis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9063f-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="9063f-116">Lauke Žurnalo pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9063f-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="9063f-117">Žurnalo nustatymą pakartokite kiekvieno juridinio subjekto parametrų puslapyje Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="9063f-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="9063f-118">Papildoma užduotis: nusidėvėjimo apskaičiavimas</span><span class="sxs-lookup"><span data-stu-id="9063f-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="9063f-119">Norėdami pradėti nusidėvėjimo vykdymą tarp juridinių subjektų, pasinaudokite puslapiu Kurti nusidėvėjimo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="9063f-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="9063f-120">Pasirinkite Ilgalaikis turtas > Žurnalo įrašai > Kurti nusidėvėjimo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="9063f-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="9063f-121">Lauke Registravimo sluoksnis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9063f-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="9063f-122">Pagal numatytąsias nuostatas, bus naudojamas ilgalaikio turto parametruose nurodytas žurnalo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="9063f-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="9063f-123">Šioje parinktyje galima keisti kiekvieno esamo juridinio subjekto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="9063f-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="9063f-124">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="9063f-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="9063f-125">Pasirinkite juridinių subjektų, kurie bus įtraukti į nusidėvėjimo vykdymą.</span><span class="sxs-lookup"><span data-stu-id="9063f-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="9063f-126">Sąraše bus rodomi tik ilgalaikio turto parametrų puslapyje pateikti ilgalaikio turto pasiūlymams nustatyti žurnalai.</span><span class="sxs-lookup"><span data-stu-id="9063f-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="9063f-127">Kai ši parinktis įgalinta, sukūrus nusidėvėjimo žurnalų parinktis Registruoti žurnalus juos užregistruos automatiškai.</span><span class="sxs-lookup"><span data-stu-id="9063f-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="9063f-128">Nepasirinkus šios parinkties žurnalai bus sukurti, bet neužregistruoti, todėl prieš juos registruodami galėsite peržiūrėti išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="9063f-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="9063f-129">Lauke Registruoti žurnalus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="9063f-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="9063f-130">Filtravimo laukai apima visą šiam nusidėvėjimo vykdymui pasirinktų juridinių subjektų ilgalaikį turtą, grupes ir knygas.</span><span class="sxs-lookup"><span data-stu-id="9063f-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="9063f-131">Parinktis Paketinis vykdymas įgalinta pagal numatytuosius nustatymus.</span><span class="sxs-lookup"><span data-stu-id="9063f-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="9063f-132">Kai ši parinktis įgalinta, nusidėvėjimo žurnalo kūrimas ir registravimas bus vykdomi fone.</span><span class="sxs-lookup"><span data-stu-id="9063f-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="9063f-133">Spustelėkite Kurti žurnalą.</span><span class="sxs-lookup"><span data-stu-id="9063f-133">Click Create journal.</span></span> 
10. <span data-ttu-id="9063f-134">Atitinkamuose juridiniuose subjektuose sukurtus nusidėvėjimo žurnalus reikia peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="9063f-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="9063f-135">Eikite į Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas.</span><span class="sxs-lookup"><span data-stu-id="9063f-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

