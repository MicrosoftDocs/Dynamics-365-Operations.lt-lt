---
title: Automatinis patvirtinimas su „Planning Optimization“
description: Šioje temoje paaiškinama, kaip naudoti automatinį patvirtinimą naudojant „Planning Optimization“.
author: ChristianRytt
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 3542e343de29c9fd9d19ed99cab4b4eebacd2899
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813008"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="3e8ad-103">Automatinis patvirtinimas su „Planning Optimization“</span><span class="sxs-lookup"><span data-stu-id="3e8ad-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e8ad-104">Automatinis patvirtinimas leidžia patvirtinti (tai yra, išleisti) suplanuotus užsakymus kaip bendrojo planavimo dalį.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="3e8ad-105">Kai patvirtinami suplanuoti užsakymai, jie paverčiami faktiniais pirkimo užsakymais, perkėlimo užsakymais arba gamybos užsakymais.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="3e8ad-106">Naudojant „Planning Optimization“, suplanuoti užsakymai patvirtinami bendrojo planavimo metu, kai užsakymo data (t. y. pradžios data) yra patvirtinimo laiko riboje.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="3e8ad-107">Automatinis suplanuoto pirkimo užsakymo patvirtinimas vykdomas tik jei prekė yra susieta su tiekėju.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>
> 
> <span data-ttu-id="3e8ad-108">Patvirtinti išvestiniai užsakymai (subrangos pirkimo užsakymai) rodys būseną *Peržiūrima*, kai įgalintas atvejų keitimų sekimas.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-108">Firmed derived orders (subcontract purchase orders) will show a status of *In-review* when case change tracking is enabled.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="3e8ad-109">Įjunkite automatinį patvirtinimą</span><span class="sxs-lookup"><span data-stu-id="3e8ad-109">Turn on autofirming</span></span>

<span data-ttu-id="3e8ad-110">Norėdami įjungti automatinį patvirtinimą atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-110">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="3e8ad-111">Darbo srityje **Funkcijos valdymas** skirtuke **Naujas** iš sąrašo pasirinkite **„Planning Optimization“ automatinis patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-111">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="3e8ad-112">Jei funkcija neatsiranda skirtuke **Naujas**, žiūrėkite skirtukus **Neįjungta** ir **Visi**.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-112">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="3e8ad-113">Pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-113">Select **Enable now**.</span></span> <span data-ttu-id="3e8ad-114">Arba pasirinkite **Grafikas** ir pasirinkite laiką, kada norite, kad funkcija būtų įjungta.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-114">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="3e8ad-115">Patvirtinimo laiko ribos nustatymas</span><span class="sxs-lookup"><span data-stu-id="3e8ad-115">Set up the firming time fence</span></span>

<span data-ttu-id="3e8ad-116">Patvirtinimo laiko ribos skaičiuojamos į priekį nuo pagrindinio planavimo vykdymo datos.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-116">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="3e8ad-117">Ji nustatoma pagal įvestą dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-117">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="3e8ad-118">Galite valdyti patvirtinimo laiko ribą toliau nurodytais būdais.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-118">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="3e8ad-119">Norėdami nustatyti numatytąją patvirtinimo laiko ribą padengimo grupei, eikite į **Pagrindinis planavimas** \> **Sąranka** \> **Padengimas** \> **Padengimo grupės** ir pasirinkite padengimo grupę.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-119">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="3e8ad-120">Tada „FastTab“ **Kita** lauke **Automatinio patvirtinimo laiko riba (dienos)** įveskite dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-120">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="3e8ad-121">Norėdami perrašyti patvirtinimo laiko ribą, kuri nustatyta padengimo grupei dėl konkrečios prekės, eikite į **Produkto informacijos valdymas** \> **Išleisti produktai**, tada veiksmų skyde pasirinkite **Planas** ir pasirinkite **Prekės padengimas**.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-121">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="3e8ad-122">Tada skirtuke **Bendroji informacija** pasirinkite **Perrašyti laiko ribą** ir lauke **Automatinio patvirtinimo laiko riba (dienos)** įveskite dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-122">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="3e8ad-123">Jei norite perrašyti patvirtinimo laiko ribą, nustatytą padengimo grupei ir konkretaus bendrojo plano prekės padengimui, eikite į **Bendrasis planavimas** \> **Sąranka** \> **Bendrieji planai** ir pasirinkite bendrąjį planą.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-123">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="3e8ad-124">Tada **Laiko tvoros dienomis** „FastTab“, nustatytas **Patvirtinimas** į **Taip** ir įveskite dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-124">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="3e8ad-125">Jei automatinis patvirtinimas yra įjungtas „Planning Optimization“ vykdymui, naudojančiam planavimo optimizavimą, automatinio patvirtinimo procesas atliekamas pagal jo nustatymus.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-125">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="3e8ad-126">Jei automatinis patvirtinimas yra įjungtas arba jei planavimas yra iš **Grynųjų reikalavimų** puslapio, automatinio patvirtinimo procesas praleidžiamas.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-126">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="3e8ad-127">„Planning Optimization“ ir įdiegtas „Supply Chain Management“ planavimo mechanizmas</span><span class="sxs-lookup"><span data-stu-id="3e8ad-127">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="3e8ad-128">„Planning Optimization“ ir planavimo variklis yra įdėti į „Microsoft Dynamics 365 Supply Chain Management“ ir gali būti naudojami automatiškai patvirtintiems suplanuotiems užsakymams.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-128">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="3e8ad-129">Tačiau yra keletas svarbių skirtumų.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-129">However, there are some important differences.</span></span> <span data-ttu-id="3e8ad-130">Pavyzdžiui, jei „Planning Optimization“ naudoja užsakymo datą (tai yra, pradžios datą), kad nustatytų, kuriuos suplanuotus užsakymus patvirtinti, įdiegtas „Supply Chain Management“ mechanizmas naudoja poreikio datą (tai yra, pabaigos datą).</span><span class="sxs-lookup"><span data-stu-id="3e8ad-130">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="3e8ad-131">Toliau pateikiama skirtumų santrauka.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-131">Here is a summary of the differences.</span></span>

<span data-ttu-id="3e8ad-132">**Planavimo optimizavimas**</span><span class="sxs-lookup"><span data-stu-id="3e8ad-132">**Planning Optimization**</span></span>

- <span data-ttu-id="3e8ad-133">Automatinis patvirtinimas yra pagrįstas užsakymo data (pradžios data).</span><span class="sxs-lookup"><span data-stu-id="3e8ad-133">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="3e8ad-134">Kadangi užsakymo data (pradžios data) suaktyvina patvirtinimą, nebūtina atsižvelgti į gamybos laiką kaip patvirtinimo laiko ribos dalį.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-134">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="3e8ad-135">Jei norite patvirtinti visus užsakymus, kurie turi prasidėti šią savaitę, patvirtinimo laiko riba turi būti viena savaitė.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-135">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="3e8ad-136">**Įdiegtas „Supply Chain Management“ planavimo mechanizmas“**</span><span class="sxs-lookup"><span data-stu-id="3e8ad-136">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="3e8ad-137">Automatinis patvirtinimas yra pagrįstas reikalavimo data (pabaigos data).</span><span class="sxs-lookup"><span data-stu-id="3e8ad-137">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="3e8ad-138">Siekiant užtikrinti, kad užsakymai būtų patvirtinti laiku, patvirtinimo laiko riba turi būti ilgesnė už gamybos laiką.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-138">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="3e8ad-139">Jei norite patvirtinti visus užsakymus, kurie turi prasidėti šią savaitę, patvirtinimo laiko riba turi būti gamybos laikas ir viena savaitė.</span><span class="sxs-lookup"><span data-stu-id="3e8ad-139">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
