---
title: Automatinis turto skaitiklių naujinimas
description: Šioje temoje aprašomas automatinis turto skaitiklių naujinimas turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875805"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="fecdc-103">Automatinis turto skaitiklių naujinimas</span><span class="sxs-lookup"><span data-stu-id="fecdc-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="fecdc-104">Ankstesniame skyriuje aprašytas turto skaitiklių rankinis generavimas.</span><span class="sxs-lookup"><span data-stu-id="fecdc-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="fecdc-105">Turto skaitiklių sąranka aprašyta [Skaitikliai](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="fecdc-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="fecdc-106">Skaitiklio reikšmes taip pat galima automatiškai naujinti iš gamybos registracijų pagal gamybos valandas arba gamybos kiekį.</span><span class="sxs-lookup"><span data-stu-id="fecdc-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="fecdc-107">Tai daroma **Naujinti turto skaitiklius**.</span><span class="sxs-lookup"><span data-stu-id="fecdc-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="fecdc-108">Galite naujinti vieną arba kelis turtus į **Nuo datos** įvesdami vieną parametrą.</span><span class="sxs-lookup"><span data-stu-id="fecdc-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="fecdc-109">Šis parametras nustato gamybos registracijų pradžios datą (valandas arba pagamintą kiekį) – pradžios datą, nuo kurios skaitiklio reikšmės turi būti naujintos.</span><span class="sxs-lookup"><span data-stu-id="fecdc-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="fecdc-110">Visas turtas, susijęs su ištekliais *ir* turi turto skaitiklius, kurie nustatyti, kad būtų naujinami pagal pagamintą kiekį arba gamybos valandas, bus įtrauktas į automatinį naujinimą, ir bus sukurta nauja skaitiklio reikšmė.</span><span class="sxs-lookup"><span data-stu-id="fecdc-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="fecdc-111">Naudojant gamybos kiekį, užregistruotas geras kiekis bei sugadintas kiekis yra įtraukiami į skaičių.</span><span class="sxs-lookup"><span data-stu-id="fecdc-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="fecdc-112">Jei pagaminto kiekio registracijos vienetas skiriasi nuo skaitiklio vieneto, kiekis yra konvertuojamas į atitinkamą skaitiklio vienetą.</span><span class="sxs-lookup"><span data-stu-id="fecdc-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="fecdc-113">Kaip minėta pirmiau, automatiniai skaitikliai gali būti naujinami iš gamybos registracijų.</span><span class="sxs-lookup"><span data-stu-id="fecdc-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="fecdc-114">Todėl turtas, kuriam norite automatiškai naujinti skaitiklius, turi būti susijęs su ištekliais (mašina).</span><span class="sxs-lookup"><span data-stu-id="fecdc-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="fecdc-115">Aprašuose toliau pateikiama sąrankos ir gamybos užsakymų, kurie yra naudojami kaip turto automatinio skaitiklių naujinimo pagrindas modulyje **Turto valdymas**, apdorojimo apžvalga (modulyje **Gamybos valdymas**).</span><span class="sxs-lookup"><span data-stu-id="fecdc-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="fecdc-116">Kai pagamintas kiekis arba gamybos valandos užregistruojamos ištekliuje, galite naujinti susijusius turto skaitiklius.</span><span class="sxs-lookup"><span data-stu-id="fecdc-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="fecdc-117">Spustelėkite **Turto valdymas** > **Periodinis** > **Turtas** > **Naujinti turto skaitiklius**.</span><span class="sxs-lookup"><span data-stu-id="fecdc-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="fecdc-118">Lauke **Pradžios data** pažymėkite automatinio naujinimo pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="fecdc-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="fecdc-119">Data šiame lauke yra vykdomo darbo data iš **Maršruto operacijos** (laukas **Gamybos valdymas** > **Užklausos ir ataskaitos** > **Gamyba** > **Maršruto operacijos** > **Fizinė data**).</span><span class="sxs-lookup"><span data-stu-id="fecdc-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="fecdc-120">Jei automatiniam naujinimui norite pažymėti konkretų turtą, turto tipą arba šaltinį, „FastTab“ **Įtrauktini įrašai** spustelėkite **Filtras** ir atlikite reikiamus pasirinkimus.</span><span class="sxs-lookup"><span data-stu-id="fecdc-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="fecdc-121">Jei reikia, galite nustatyti automatinio naujinimo paketinę užduotį FastTab **Vykdyti fone**.</span><span class="sxs-lookup"><span data-stu-id="fecdc-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![1 pav.](media/12-work-orders.png)

5. <span data-ttu-id="fecdc-123">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fecdc-123">Click **OK**.</span></span> <span data-ttu-id="fecdc-124">Kai automatinis turto skaitiklio naujinimas baigtas, galite matyti skaitiklio registracijas, susijusias su turtu **Turto skaitikliai** (mygtukas **Turto valdymas** > **Bendrieji dalykai** > **Turtas** > **Visas turtas** > pažymėti turtą> **Skaitikliai**).</span><span class="sxs-lookup"><span data-stu-id="fecdc-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="fecdc-125">**Turto skaitiklio suvestinė** galite peržiūrėti naujausias viso turto visų skaitiklių tipų registracijas.</span><span class="sxs-lookup"><span data-stu-id="fecdc-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="fecdc-126">Spustelėkite **Turto valdymas** > **Užklausos** > **Turtas** > **Turto sudėtinė reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="fecdc-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="fecdc-127">Rodinys labai panašus į **Turto skaitikliai**, tačiau **Turto sudėtinė reikšmė** negalite įtraukti arba redaguoti registracijų.</span><span class="sxs-lookup"><span data-stu-id="fecdc-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="fecdc-128">Jis skirtas tik peržiūrai.</span><span class="sxs-lookup"><span data-stu-id="fecdc-128">It is for overview only.</span></span>

![2 paveikslėlis](media/13-work-orders.png)


- <span data-ttu-id="fecdc-130">Tačiau skaitiklių tipams, kurie automatiškai atnaujinti, galima kurti rankines skaitiklio reikšmių registracijas.</span><span class="sxs-lookup"><span data-stu-id="fecdc-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="fecdc-131">Daugiau informacijos žr. skyriuje „Turto skaitiklių rankinis naujinimas“.</span><span class="sxs-lookup"><span data-stu-id="fecdc-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="fecdc-132">Galite nustatyti skaitiklius, susijusius su kitu skaitiklius. Tai reiškia, kad kai skaitiklis yra naujinamas, tuo pačiu metu naujinami susiję skaitikliai.</span><span class="sxs-lookup"><span data-stu-id="fecdc-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="fecdc-133">Dėl susijusių skaitiklių sąrankos, žr. [Skaitikliai](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="fecdc-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
