---
title: Juridinių subjektų ilgalaikio turto nusidėvėjimo skaičiavimas
description: Ilgalaikio turto nusidėvėjimą tarp juridinių subjektų galima vykdyti vienu veiksmu.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 074a1b80584050302920a95c20fb547523a4866c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142920"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="12246-103">Juridinių subjektų ilgalaikio turto nusidėvėjimo skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="12246-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12246-104">Ilgalaikio turto nusidėvėjimą tarp juridinių subjektų galima vykdyti vienu veiksmu.</span><span class="sxs-lookup"><span data-stu-id="12246-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="12246-105">Šioje procedūroje rodoma, kaip nustatyti ir vykdyti kelių juridinių subjektų procesą.</span><span class="sxs-lookup"><span data-stu-id="12246-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="12246-106">Joje naudojamas vaidmuo Buhalteris ir USMF juridinio subjekto demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="12246-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="12246-107">Visos įmonės nusidėvėjimo vykdymo žurnalų nustatymas</span><span class="sxs-lookup"><span data-stu-id="12246-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="12246-108">Eikite į Ilgalaikis turtas > Nustatymas > Ilgalaikio turto parametrai.</span><span class="sxs-lookup"><span data-stu-id="12246-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="12246-109">Išplėskite ilgalaikio turto pasiūlymų skyrių.</span><span class="sxs-lookup"><span data-stu-id="12246-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="12246-110">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="12246-110">Click Add.</span></span>
4. <span data-ttu-id="12246-111">Lauke Registravimo sluoksnis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="12246-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="12246-112">Lauke Žurnalo pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="12246-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="12246-113">Žurnalo nustatymą pakartokite kiekvieno juridinio subjekto parametrų puslapyje Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="12246-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="12246-114">Nusidėvėjimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="12246-114">Depreciation run</span></span>
1. <span data-ttu-id="12246-115">Pasirinkite Ilgalaikis turtas > Žurnalo įrašai > Kurti nusidėvėjimo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="12246-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="12246-116">Lauke Registravimo sluoksnis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="12246-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="12246-117">Pagal numatytąsias nuostatas, bus naudojamas ilgalaikio turto parametruose nurodytas žurnalo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="12246-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="12246-118">Šioje parinktyje galima keisti kiekvieno esamo juridinio subjekto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="12246-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="12246-119">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="12246-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="12246-120">Pasirinkite juridinių subjektų, kurie bus įtraukti į nusidėvėjimo vykdymą.</span><span class="sxs-lookup"><span data-stu-id="12246-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="12246-121">Sąraše bus rodomi tik ilgalaikio turto parametrų puslapyje pateikti ilgalaikio turto pasiūlymams nustatyti žurnalai.</span><span class="sxs-lookup"><span data-stu-id="12246-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="12246-122">Lauke Registruoti žurnalus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="12246-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="12246-123">Filtravimo laukai apima visą šiam nusidėvėjimo vykdymui pasirinktų juridinių subjektų ilgalaikį turtą, grupes ir knygas.</span><span class="sxs-lookup"><span data-stu-id="12246-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="12246-124">Parinktis Paketinis vykdymas įgalinta pagal numatytuosius nustatymus.</span><span class="sxs-lookup"><span data-stu-id="12246-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="12246-125">Kai ši parinktis įgalinta, nusidėvėjimo žurnalo kūrimas ir registravimas bus vykdomi fone.</span><span class="sxs-lookup"><span data-stu-id="12246-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="12246-126">Spustelėkite Kurti žurnalą.</span><span class="sxs-lookup"><span data-stu-id="12246-126">Click Create journal.</span></span>
6. <span data-ttu-id="12246-127">Eikite į Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas.</span><span class="sxs-lookup"><span data-stu-id="12246-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

