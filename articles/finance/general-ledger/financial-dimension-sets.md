---
title: Finansinių dimensijų rinkiniai
description: Šioje temoje aprašomi finansinių dimensijų rinkiniai ir pateikiami jų naudojimo optimizavimo patarimai.
author: yukonpeegs
manager: AnnBe
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b719d8eb868cb1722b470be4443d01181078ce21
ms.sourcegitcommit: 97ada5d52ed1829dcf030dad254096cd8df25da8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2021
ms.locfileid: "5864417"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="492a0-103">Finansinių dimensijų rinkiniai</span><span class="sxs-lookup"><span data-stu-id="492a0-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="492a0-104">Šioje temoje aprašomi finansinių dimensijų rinkiniai ir pateikiami jų naudojimo optimizavimo patarimai.</span><span class="sxs-lookup"><span data-stu-id="492a0-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="492a0-105">Dimensijų rinkinys yra surikiuotas finansinių dimensijų sąrašas, kurį galima naudoti Didžiosios knygos duomenims apibendrinti vartotojo apibrėžtu būdu.</span><span class="sxs-lookup"><span data-stu-id="492a0-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="492a0-106">Pirminis dimensijų rinkinių naudojimas yra apibrėžti bandomąjį balansą.</span><span class="sxs-lookup"><span data-stu-id="492a0-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="492a0-107">Vienintelis standartinis dimensijų rinkinys yra tas dimensijų rinkinys, kuriame yra tik pagrindinė sąskaita.</span><span class="sxs-lookup"><span data-stu-id="492a0-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="492a0-108">Naudokite puslapį **Finansinių dimensijų rinkiniai** kurti ir valdyti finansinių dimensijų rinkinius.</span><span class="sxs-lookup"><span data-stu-id="492a0-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="492a0-109">Dimensijų rinkinio balansai</span><span class="sxs-lookup"><span data-stu-id="492a0-109">Dimension set balances</span></span>

<span data-ttu-id="492a0-110">Dimensijų rinkinys gali turėti balansus, pagrįstus jo finansinėmis dimensijomis.</span><span class="sxs-lookup"><span data-stu-id="492a0-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="492a0-111">Balansai yra Didžiojoje knygoje ir yra pagrįsti dimensijų rinkinio apibrėžimu.</span><span class="sxs-lookup"><span data-stu-id="492a0-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="492a0-112">Balansai yra apibendrinami iš Didžiosios knygos duomenų, kad būtų pagerintas operacijų efektyvumas, kai jos nuskaitomos (pavyzdžiui, kai generuojamas bandomasis balansas).</span><span class="sxs-lookup"><span data-stu-id="492a0-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="492a0-113">Balansų kūrimas</span><span class="sxs-lookup"><span data-stu-id="492a0-113">Create balances</span></span>

<span data-ttu-id="492a0-114">Naudokite mygtuką **Kurti balansus** norėdami inicijuoti dimensijų rinkinio, kuris šiuo metu neturi balansų, balansus.</span><span class="sxs-lookup"><span data-stu-id="492a0-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="492a0-115">Rekomenduojame riboti balansus turinčių dimensijų rinkinių skaičių, nes balanso atnaujinimai paveikia visas Didžiosios knygos registravimo veiklas.</span><span class="sxs-lookup"><span data-stu-id="492a0-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="492a0-116">Atnaujinti balansus</span><span class="sxs-lookup"><span data-stu-id="492a0-116">Update balances</span></span>

<span data-ttu-id="492a0-117">Naudokite mygtuką **Atnaujinti balansus** norėdami į balansus įtraukti naujausią Didžiosios knygos registravimo veiklą.</span><span class="sxs-lookup"><span data-stu-id="492a0-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="492a0-118">Balanso atnaujinimai yra lengvos operacijos.</span><span class="sxs-lookup"><span data-stu-id="492a0-118">Balance updates are light operations.</span></span> <span data-ttu-id="492a0-119">Jie turi apdoroti tik Didžiosios knygos registravimo veiklą, kuri įvyko po paskutinio atnaujinimo.</span><span class="sxs-lookup"><span data-stu-id="492a0-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="492a0-120">Bandomojo balanso rodymas sukelia atnaujinimą, siekiant užtikrinti, kad rodomi balansai yra dabartiniai.</span><span class="sxs-lookup"><span data-stu-id="492a0-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="492a0-121">Apsvarstykite galimybę naudoti pasikartojančią paketinę užduotį, kad dažniausiai naudojamų dimensijų rinkinių naujinimai būtų spartieji.</span><span class="sxs-lookup"><span data-stu-id="492a0-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="492a0-122">Tokiu būdu galite sumažinti bandomojo balanso vartotojų laukimo laiką.</span><span class="sxs-lookup"><span data-stu-id="492a0-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="492a0-123">Perkurti balansus</span><span class="sxs-lookup"><span data-stu-id="492a0-123">Rebuild balances</span></span>

<span data-ttu-id="492a0-124">Naudokite mygtuką **Perkurti balansus**, kad iš naujo sukurtumėte balansus nuo pradžių.</span><span class="sxs-lookup"><span data-stu-id="492a0-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="492a0-125">Tokiu būdu galite užtikrinti, kad jie atitinka Didžiosios knygos duomenis.</span><span class="sxs-lookup"><span data-stu-id="492a0-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="492a0-126">Balansų perkūrimui reikia daug apdorojimo ir paprastai jis neturėtų būti reikalaujamas.</span><span class="sxs-lookup"><span data-stu-id="492a0-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="492a0-127">Jei naudojate scenarijų, kuriame reguliariai reikalaujama perkurti balansus, rekomenduojame kreiptis į klientų aptarnavimo tarnybą.</span><span class="sxs-lookup"><span data-stu-id="492a0-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="492a0-128">Klientų aptarnavimo tarnyba gali padėti nustatyti, kodėl balansai neatitinka Didžiosios knygos duomenų.</span><span class="sxs-lookup"><span data-stu-id="492a0-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="492a0-129">Valyti balansus</span><span class="sxs-lookup"><span data-stu-id="492a0-129">Clear balances</span></span>

<span data-ttu-id="492a0-130">Naudokite mygtuką **Valyti balansus**, kad pašalintumėte balansus ir sustabdytumėte bet kokius tolesnius atnaujinimus.</span><span class="sxs-lookup"><span data-stu-id="492a0-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="492a0-131">Dimensijų rinkinys nebeturės įtakos Didžiosios knygos registravimo veikloms.</span><span class="sxs-lookup"><span data-stu-id="492a0-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="492a0-132">Daugiau informacijos rasite [Finansinės dimensijos](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="492a0-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
