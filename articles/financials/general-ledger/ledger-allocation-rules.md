---
title: "DK paskirstymo taisyklės"
description: "Šiame straipsnyje pateikiama informacija apie didžiosios knygos paskirstymo taisykles. Jame aprašomi įvairūs šių paskirstymo taisyklių komponentai ir galimi naudoti jų paskirstymo metodai."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 87b98811dabb6a8593cd4a75ad9c5a028f653867
ms.contentlocale: lt-lt
ms.lasthandoff: 06/29/2017


---

# <a name="ledger-allocation-rules"></a><span data-ttu-id="dcb60-104">DK paskirstymo taisyklės</span><span class="sxs-lookup"><span data-stu-id="dcb60-104">Ledger allocation rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="dcb60-105">Šiame straipsnyje pateikiama informacija apie didžiosios knygos paskirstymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="dcb60-105">This article provides information about ledger allocation rules.</span></span> <span data-ttu-id="dcb60-106">Jame aprašomi įvairūs šių paskirstymo taisyklių komponentai ir galimi naudoti jų paskirstymo metodai.</span><span class="sxs-lookup"><span data-stu-id="dcb60-106">It describes the various components of these allocation rules and the allocation methods that can be used for them.</span></span>

<span data-ttu-id="dcb60-107">DK paskirstymo taisyklės naudojamos norint automatiškai apskaičiuoti ir generuoti paskirstymo žurnalus ir sąskaitos įrašus, kad būtų paskirstyti DK balansai arba fiksuotos sumos.</span><span class="sxs-lookup"><span data-stu-id="dcb60-107">Ledger allocation rules are used to automatically calculate and generate allocation journals and account entries for the allocation of ledger balances or fixed amounts.</span></span> <span data-ttu-id="dcb60-108">Paskirstymo metodai gali būti kintantys arba fiksuoti.</span><span class="sxs-lookup"><span data-stu-id="dcb60-108">Allocation methods can be variable or fixed.</span></span> <span data-ttu-id="dcb60-109">DK paskirstymo taisyklėms galima naudoti toliau nurodytus paskirstymo metodus.</span><span class="sxs-lookup"><span data-stu-id="dcb60-109">The following allocation methods can be used for ledger allocation rules:</span></span>

-   <span data-ttu-id="dcb60-110">**Pagrindas** – šis kintantis metodas naudojamas, kai paskirstymas priklauso nuo faktinio DK balanso, atsižvelgiant į filtro kriterijus.</span><span class="sxs-lookup"><span data-stu-id="dcb60-110">**Basis** – This variable method is used when the allocation depends on the actual ledger balance, based on filter criteria.</span></span> <span data-ttu-id="dcb60-111">Pavyzdžiui, reklamos išlaidas galima paskirstyti remiantis kiekvieno departamento pardavimais, proporcingais viso departamento pardavimams.</span><span class="sxs-lookup"><span data-stu-id="dcb60-111">For example, advertising expenses can be allocated based on each department's sales in proportion to the total departmental sales.</span></span>
-   <span data-ttu-id="dcb60-112">**Fiksuotas procentas** ir **Fiksuota dalis** – naudojant šiuos metodus, paskirstymo procentas arba dalis nustatoma tiesiogiai taisyklei.</span><span class="sxs-lookup"><span data-stu-id="dcb60-112">**Fixed percentage** and **Fixed weight** – For these methods, the allocation percentage or weight is defined directly for the rule.</span></span> <span data-ttu-id="dcb60-113">Pvz., reklamos išlaidas galima paskirstyti taip, kad A padalinys gautų 70 procentų, o B padalinys gautų 30 procentų reklamos išlaidų.</span><span class="sxs-lookup"><span data-stu-id="dcb60-113">For example, advertising expenses can be allocated so that Department A receives 70 percent of the advertising expense and Department B receives 30 percent.</span></span>
-   <span data-ttu-id="dcb60-114">**Tolygiai** – naudojant šį metodą suma tolygiai paskirstoma kiekvienoje nurodytoje paskirties vietoje.</span><span class="sxs-lookup"><span data-stu-id="dcb60-114">**Equally** – This method distributes the amount equally to each defined destination.</span></span> <span data-ttu-id="dcb60-115">Pvz., jei nurodytos A ir B padalinių paskirties vietos, reklamos išlaidas galima paskirstyti taip, kad A ir B padaliniai gautų po 50 procentų reklamos išlaidų.</span><span class="sxs-lookup"><span data-stu-id="dcb60-115">For example, if destinations are defined for Department A and Department B, advertising expenses can be allocated so that both Department A and Department B receive 50 percent of the advertising expense.</span></span>

<span data-ttu-id="dcb60-116">Jei Pagrindas naudojamas kaip paskirstymo taisyklės paskirstymo metodas, taip pat privalote nurodyti atskiras DK paskirstymo pagrindo taisykles.</span><span class="sxs-lookup"><span data-stu-id="dcb60-116">If Basis is used as the allocation method for an allocation rule, you must also define separate ledger allocation basis rules.</span></span> <span data-ttu-id="dcb60-117">Vykdydami procesą „Apdoroti paskirstymo užklausą“ vartotojai gali apdoroti DK paskirstymo taisyklę ir peržiūrėti gautus paskirstymo žurnalo įrašus prieš užregistruodami arba panaikindami apskaičiuotus paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="dcb60-117">The "Process allocation request" process lets users process the ledger allocation rule and preview the resulting allocation journal entries before they either post or delete the calculated allocations.</span></span>

## <a name="components-of-ledger-allocation-rules"></a><span data-ttu-id="dcb60-118">DK paskirstymo taisyklių komponentai</span><span class="sxs-lookup"><span data-stu-id="dcb60-118">Components of ledger allocation rules</span></span>
<span data-ttu-id="dcb60-119">Kiekviena paskirstymo taisyklė turi keturis komponentus: bendrą, šaltinio, paskirties ir korespondentinį.</span><span class="sxs-lookup"><span data-stu-id="dcb60-119">Each allocation rule has four components: general, source, destination, and offset.</span></span> <span data-ttu-id="dcb60-120">Papildomas komponentas, DK paskirstymo pagrindo taisyklės, yra reikalingos, jei Pagrindas naudojamas kaip paskirstymo metodas.</span><span class="sxs-lookup"><span data-stu-id="dcb60-120">An additional component, ledger allocation bases rules, is required if Basis is used as the allocation method.</span></span> <span data-ttu-id="dcb60-121">Kiekvienas komponentas suteikia svarbią informacijos dalį, reikalingą paskirstymams apdoroti.</span><span class="sxs-lookup"><span data-stu-id="dcb60-121">Each component provides a critical piece of the information that is required in order to process allocations.</span></span>

-   <span data-ttu-id="dcb60-122">**Bendra** – šiame komponente vartotojas nurodo parinktis, pvz., paskirstymo metodą, vidinės įmonės taisyklių parametrus ir tai, ar taisyklė yra aktyvi.</span><span class="sxs-lookup"><span data-stu-id="dcb60-122">**General** – This component is where the user specifies options such as the allocation method, intercompany rule settings, and whether the rule is active.</span></span>
-   <span data-ttu-id="dcb60-123">**Šaltinis** – šiame komponente vartotojas nurodo paskirstymo šaltinio duomenis.</span><span class="sxs-lookup"><span data-stu-id="dcb60-123">**Source** – This component is where the user specifies the source data for the allocation.</span></span> <span data-ttu-id="dcb60-124">Paskirstymas gali būti pagrįstas DK balansais (**Duomenų šaltinis** = **DK**) arba fiksuotomis sumomis (**Duomenų šaltinis** = **Fiksuota reikšmė**).</span><span class="sxs-lookup"><span data-stu-id="dcb60-124">Allocation can be based on ledger balances (**Data source** = **Ledger**) or fixed amounts (**Data source** = **Fixed value**).</span></span> <span data-ttu-id="dcb60-125">Kai **Duomenų šaltinis** nustatytas kaip **DK**, turi būti nurodyti DK paskirstymo taisyklės šaltinio filtro kriterijai (pvz., reklamos išlaidos).</span><span class="sxs-lookup"><span data-stu-id="dcb60-125">When **Data source** is set to **Ledger**, source filter criteria must be defined for the ledger allocation rule (for example, for the advertising expenses).</span></span>
-   <span data-ttu-id="dcb60-126">**Paskirties vieta** – šis komponentas apibrėžia, kaip paskirstymo skaičiavimų rezultatas turi būti paskirstytas ir kaip už jį turi būti atsiskaityta.</span><span class="sxs-lookup"><span data-stu-id="dcb60-126">**Destination** – This component defines how the result of the allocation calculation should be distributed and accounted for.</span></span> <span data-ttu-id="dcb60-127">Pvz., galima sukurti vieną kiekvieno padalinio paskirties eilutę.</span><span class="sxs-lookup"><span data-stu-id="dcb60-127">For example, there can be one destination line for each department.</span></span>
-   <span data-ttu-id="dcb60-128">**Korespondentinis** – šis komponentas apibrėžia, kaip pagrindinės sąskaitos ir dimensijos turėtų būti nustatytos korespondentinėms įvestims, kurios subalansuoja paskirties įrašus.</span><span class="sxs-lookup"><span data-stu-id="dcb60-128">**Offset** – This component defines how main accounts and dimensions should be determined for the offset entries that balance the destination entries.</span></span> <span data-ttu-id="dcb60-129">Paprastai naudojamos vartotojo nurodytos parinktys, o ne šaltinyje nurodytos sąskaitos ir dimensijos.</span><span class="sxs-lookup"><span data-stu-id="dcb60-129">User-defined options are typically used instead of accounts and dimensions that are based on the source.</span></span> <span data-ttu-id="dcb60-130">Kai **Duomenų šaltinis** nustatytas kaip **Fiksuota reikmė**, **Šaltinis** negali būti naudojamas kaip parinktis.</span><span class="sxs-lookup"><span data-stu-id="dcb60-130">When **Data source** is set to **Fixed value**, **Source** can't be used as an option.</span></span>
-   <span data-ttu-id="dcb60-131">**DK paskirstymo pagrindo taisyklės** – šios taisyklės naudoja savo šaltinio filtro kriterijus, kad nustatytų, kurie DK balansai turi būti naudojami paskirstant (pvz., įplaukos pagal padalinį).</span><span class="sxs-lookup"><span data-stu-id="dcb60-131">**Ledger allocation basis rules** – These rules use their own source filter criteria to determine which ledger balances should be used for allocation (for example, the revenue per department).</span></span> <span data-ttu-id="dcb60-132">Kiekviena paskirstymo pagrindo taisyklė gali būti taikoma su daugeliu paskirstymo taisyklių.</span><span class="sxs-lookup"><span data-stu-id="dcb60-132">Each allocation basis rule can be used with multiple allocation rules.</span></span>




