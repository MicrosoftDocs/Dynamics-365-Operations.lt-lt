---
title: Automatinis turto skaitiklių naujinimas
description: Šioje temoje aprašomas automatinis turto skaitiklių naujinimas turto valdyme.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9911d5b96bb58b5def3e7dfee0f36826d99f6ba1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263691"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="898c8-103">Automatinis turto skaitiklių atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="898c8-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="898c8-104">Informacijos apie turto skaitiklių registravimą neautomatiniu būdu žr. [Neautomatinis turto skaitiklių atnaujinimas](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="898c8-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="898c8-105">Informacijos, kaip nustatyti turto skaitiklius, žr. [Skaitikliai](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="898c8-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="898c8-106">Skaitiklio reikšmes taip pat galima automatiškai naujinti iš gamybos registracijų pagal gamybos valandas arba gamybos kiekį (t. y. pagamintą kiekį).</span><span class="sxs-lookup"><span data-stu-id="898c8-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="898c8-107">Šis naujinimas atliekamas puslapyje **Naujinti turto skaitiklius**.</span><span class="sxs-lookup"><span data-stu-id="898c8-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="898c8-108">Vieną arba kelis turtus galite atnaujinti nustatydami vieną parametrą **Pradžios data**.</span><span class="sxs-lookup"><span data-stu-id="898c8-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="898c8-109">Šis parametras nurodo gamybos registracijų (gamybos valandų arba gamybos kiekių) pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="898c8-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="898c8-110">Kitaip tariant, jis nurodo datą, nuo kada reikia atnaujinti skaitiklio vertes.</span><span class="sxs-lookup"><span data-stu-id="898c8-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="898c8-111">Visas turtas, susijęs su ištekliumi *ir* turintis turto skaitiklius, kurie nustatyti, kad būtų naujinami pagal gamybos valandas ar arba gamybos kiekį, bus įtrauktas į automatinį naujinimą.</span><span class="sxs-lookup"><span data-stu-id="898c8-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="898c8-112">Bus sukurtos naujos skaitiklio vertės.</span><span class="sxs-lookup"><span data-stu-id="898c8-112">New counter values will be created.</span></span>

<span data-ttu-id="898c8-113">Skaitikliams, kurie pagrįsti gamybos kiekiu, skaičius apima ir geros kokybės prekes, ir užregistruotus kiekius su klaidomis.</span><span class="sxs-lookup"><span data-stu-id="898c8-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="898c8-114">Jei gamybos kiekio registravimui naudotas vienetas skiriasi nuo skaitiklio naudojamo vieneto, kiekis yra konvertuojamas, kad atitiktų skaitiklio vienetą.</span><span class="sxs-lookup"><span data-stu-id="898c8-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="898c8-115">Kaip minėta pirmiau, automatiniai skaitikliai gali būti naujinami iš gamybos registracijų.</span><span class="sxs-lookup"><span data-stu-id="898c8-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="898c8-116">Todėl turtas, kuriam norite automatiškai naujinti skaitiklius, turi būti susijęs su ištekliais (mašina).</span><span class="sxs-lookup"><span data-stu-id="898c8-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="898c8-117">Kai pagamintas kiekis arba gamybos valandos užregistruojamos ištekliuje, galite naujinti susijusius turto skaitiklius.</span><span class="sxs-lookup"><span data-stu-id="898c8-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="898c8-118">Pasirinkite **Turto valdymas** > **Periodinis** > **Turtas** > **Naujinti turto skaitiklius**.</span><span class="sxs-lookup"><span data-stu-id="898c8-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="898c8-119">Lauke **Pradžios data** pasirinkite automatinio naujinimo pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="898c8-119">In the **From date** field, select the start date of the automatic update.</span></span>

    >[!NOTE]
    ><span data-ttu-id="898c8-120">Data šiame lauke yra vykdomo darbo data iš **Maršruto operacijos** (laukas **Gamybos valdymas** > **Užklausos ir ataskaitos** > **Gamyba** > **Maršruto operacijos** > **Fizinė data**).</span><span class="sxs-lookup"><span data-stu-id="898c8-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="898c8-121">„FastTab“ **Įtrauktini įrašai** galite pasirinkti konkretų turtą,turto tipą ar išteklius automatiniam naujinimui.</span><span class="sxs-lookup"><span data-stu-id="898c8-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="898c8-122">Pasirinkite **Filtras** ir atlikite reikiamus pasirinkimus.</span><span class="sxs-lookup"><span data-stu-id="898c8-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="898c8-123">FastTab **Vykdyti fone** pagal poreikį galite nustatyti automatinio naujinimo paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="898c8-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

    <span data-ttu-id="898c8-124">Toliau pateiktame paveikslėlyje parodytas dialogo lango **Naujinti turto skaitiklius** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="898c8-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

    ![1 pav.](media/12-work-orders.png)

5. <span data-ttu-id="898c8-126">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="898c8-126">Select **OK**.</span></span> 

<span data-ttu-id="898c8-127">Baigus automatinį turto skaitiklio naujinimą, puslapyje **Turto skaitikliai** galite peržiūrėti su turtu susijusias skaitiklio registracijas.</span><span class="sxs-lookup"><span data-stu-id="898c8-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="898c8-128">Pasirinkite **Turto valdymas** > **Bendra** > **Turtas** > **Visas turtas**, pasirinkite turtą, o tada veiksmų srityje, skirtuke **Turtas**, grupėje **Profilaktinė** pasirinkite **Skaitikliai**.</span><span class="sxs-lookup"><span data-stu-id="898c8-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="898c8-129">Puslapyje **Turto sudėtinė reikšmė** galite peržiūrėti naujausias viso turto visų skaitiklių tipų registracijas.</span><span class="sxs-lookup"><span data-stu-id="898c8-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="898c8-130">Pasirinkite **Turto valdymas** > **Užklausos** > **Turtas** > **Turto sudėtinė reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="898c8-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="898c8-131">Šis puslapis primena puslapį **Turto skaitikliai**, bet čia negalima pridėti arba redaguoti registracijų.</span><span class="sxs-lookup"><span data-stu-id="898c8-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="898c8-132">Jis skirtas tik peržiūrai.</span><span class="sxs-lookup"><span data-stu-id="898c8-132">It's for overview only.</span></span>

<span data-ttu-id="898c8-133">Toliau pateiktame paveikslėlyje parodytas puslapio **Turto sudėtinė reikšmė** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="898c8-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![2 pav.](media/13-work-orders.png)

<span data-ttu-id="898c8-135">Atkreipkite dėmesį į toliau nurodytus punktus.</span><span class="sxs-lookup"><span data-stu-id="898c8-135">Note the following points:</span></span>

- <span data-ttu-id="898c8-136">Tačiau skaitiklių tipams, kurie yra automatiškai atnaujinami, galite kurti rankines skaitiklio reikšmių registracijas.</span><span class="sxs-lookup"><span data-stu-id="898c8-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="898c8-137">Daugiau informacijos žr. [Neautomatinis turto skaitiklių atnaujinimas](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="898c8-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="898c8-138">Galite nustatyti skaitiklius, susietus su kitu skaitikliu.</span><span class="sxs-lookup"><span data-stu-id="898c8-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="898c8-139">Šiuo atveju, atnaujinus skaitiklį, tuo pačiu metu automatiškai atnaujinami susiję skaitikliai.</span><span class="sxs-lookup"><span data-stu-id="898c8-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="898c8-140">Daugiau informacijos, kaip nustatyti susijusius skaitiklius, žr. [Skaitikliai](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="898c8-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]