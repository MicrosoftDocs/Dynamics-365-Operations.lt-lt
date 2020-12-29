---
title: Būtinųjų sąlygų standartinėms savikainoms apžvalga
description: Šioje temoje aprašomi pagrindiniai standartinių savikainų naudojimo veiksmai.
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f66f7061c608379689016e3c0b9c5ba4ad23dc9e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433766"
---
# <a name="prerequisites-for-standard-costs-overview"></a><span data-ttu-id="77835-103">Būtinųjų sąlygų standartinėms savikainoms apžvalga</span><span class="sxs-lookup"><span data-stu-id="77835-103">Prerequisites for standard costs overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77835-104">Šioje temoje aprašomi pagrindiniai standartinių savikainų naudojimo veiksmai.</span><span class="sxs-lookup"><span data-stu-id="77835-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="77835-105">Vėlesni veiksmai priklauso nuo įmonės operacijų.</span><span class="sxs-lookup"><span data-stu-id="77835-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="77835-106">Pavyzdžiui, veiksmai skiriasi negamybinėje aplinkoje, gamybinėje aplinkoje, nenaudojančioje nukreipimų, ir gamybinėje aplinkoje, naudojančioje nukreipimus.</span><span class="sxs-lookup"><span data-stu-id="77835-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="77835-107">Norėdami nustatyti standartines savikainas, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="77835-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="77835-108">**1. Sukurkite standartinių savikainų prekių modelių grupę.**</span><span class="sxs-lookup"><span data-stu-id="77835-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="77835-109">Naudokite puslapį **Prekių modelių grupės**, norėdami sukurti naują standartinių savikainų grupę ir priskirti atsargų modelį **Standartinė savikaina**.</span><span class="sxs-lookup"><span data-stu-id="77835-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="77835-110">Prekių modelio grupės identifikatorius turi turėti prasmę, pvz., **Stand. išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="77835-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="77835-111">Norėdami nurodyti, kad grupė turėtų leisti neigiamas finansines atsargas, ir kad ji turėtų registruoti faktines atsargas bei finansines atsargas, pažymėkite žymės langelius.</span><span class="sxs-lookup"><span data-stu-id="77835-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="77835-112">Ši standartinių savikainų grupė bus paskirta prekėms.</span><span class="sxs-lookup"><span data-stu-id="77835-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="77835-113">**2. Nustatykite DK sąskaitas, kurios yra susijusios su nuokrypiu nuo standartinės savikainos.**</span><span class="sxs-lookup"><span data-stu-id="77835-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="77835-114">Norėdami nustatyti DK sąskaitas, kurios yra susijusios su nuokrypiu nuo standartinės savikainos, naudokite puslapį **Sąskaitų planas**.</span><span class="sxs-lookup"><span data-stu-id="77835-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="77835-115">Šios DK sąskaitos turi būti nustatytos prieš jas priskiriant puslapyje **Registravimas**.</span><span class="sxs-lookup"><span data-stu-id="77835-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="77835-116">DK sąskaitos gali atspindėti prekių grupes ir savikainų grupes.</span><span class="sxs-lookup"><span data-stu-id="77835-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="77835-117">**3. Prekių registravimui priskirkite DK sąskaitas, kurios yra susijusios su nuokrypiu nuo standartinės savikainos.**</span><span class="sxs-lookup"><span data-stu-id="77835-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="77835-118">Norėdami priskirti DK sąskaitas, kurios yra susijusios su nuokrypiu nuo standartinės savikainos, naudokite puslapį **Registravimas**.</span><span class="sxs-lookup"><span data-stu-id="77835-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="77835-119">Nuokrypio DK sąskaitą galite nurodyti pagal prekę (ar prekių grupę) ir pagal savikainos grupę (ar kainos grupės tipą), arba galite nurodyti, kad DK sąskaita taikoma visoms prekėms ir visoms savikainų grupėms.</span><span class="sxs-lookup"><span data-stu-id="77835-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="77835-120">Šios parinktys atitinka lentelių, grupių ir visų savikainų santykiams.</span><span class="sxs-lookup"><span data-stu-id="77835-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="77835-121">Prieš nustatydami prekių registravimo taisykles, naudokite puslapį **Operacijų deriniai**, kad įjungtumėte išlaidų santykius (lentelėms, grupėms ir viskam).</span><span class="sxs-lookup"><span data-stu-id="77835-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="77835-122">**4. Nustatykite atsargų parametrus, kurie yra susiję su standartine savikaina.**</span><span class="sxs-lookup"><span data-stu-id="77835-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="77835-123">Norėdami nustatyti du kaštų kontrolės parametrus, kurie yra susiję su standartiniais kaštais, naudokite puslapio **Atsargų apskaitos strategijų sąranka > Parametrai** skirtuką **Atsargų apskaita**.</span><span class="sxs-lookup"><span data-stu-id="77835-123">Use the **Inventory accounting** tab on the **Inventory accounting policies setup > Parameters** page to define two cost control parameters that are related to standard costs.</span></span>

    -  <span data-ttu-id="77835-124">Lauke **Išlaidų paskirstymas** pasirinkite **Nėra** arba **Antrinė DK**.</span><span class="sxs-lookup"><span data-stu-id="77835-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="77835-125">Jei pasirenkate **Antrinė DK**, išlaidų paskirstymas yra *aktyvus*.</span><span class="sxs-lookup"><span data-stu-id="77835-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="77835-126">Aktyvus išlaidų paskirstymas yra svarbus skaičiavimui, išlaikymui ir išlaidų grupės segmentavimo peržiūrai visoje standartinių išlaidų komponentų kelių lygių produkto struktūroje.</span><span class="sxs-lookup"><span data-stu-id="77835-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="77835-127">Kai išlaidų paskirstymas yra aktyvus, galite pateikti ir analizuoti atsargas, nebaigtą gamybą (NG) ir parduotų prekių išlaidas išlaidų grupei viename lygyje, keliuose lygiuose ar visame formate.</span><span class="sxs-lookup"><span data-stu-id="77835-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="77835-128">Kai išlaidų paskirstymas yra aktyvus, suaktyvinus pagamintos prekės išlaidas, išlaidų grupių segmentavimas bus saugomas prekės išlaidų įraše.</span><span class="sxs-lookup"><span data-stu-id="77835-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="77835-129">Jei pasirinksite **Nėra**, standartinių savikainų prekių išlaidų grupės segmentavimas nebus tvarkomas.</span><span class="sxs-lookup"><span data-stu-id="77835-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="77835-130">Kitaip tariant, pagamintos prekės standartinė savikaina bus apskaičiuota ir tvarkoma kaip viena suma be išlaidų grupių segmentavimo.</span><span class="sxs-lookup"><span data-stu-id="77835-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="77835-131">Pagamintų komponentų išlaidų įnašai bus sujungti į vieną sumą.</span><span class="sxs-lookup"><span data-stu-id="77835-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="77835-132">Lauke **Nuokrypiai nuo standarto** pasirinkite **Susumuota** arba **Pagal išlaidų grupę**.</span><span class="sxs-lookup"><span data-stu-id="77835-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="77835-133">Jei pasirenkate **Pagal išlaidų grupę**, galite nustatyti pirkimo kainų nuokrypius ir gamybos nuokrypius pagal išlaidų grupę.</span><span class="sxs-lookup"><span data-stu-id="77835-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="77835-134">Tai taip pat galite nustatyti keturis gamybos nuokrypių tipus: partijos dydis, kiekis, kaina ir pakaitalų nuokrypiai.</span><span class="sxs-lookup"><span data-stu-id="77835-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="77835-135">Jei pasirenkate **Susumuota**, negalite nustatyti nuokrypių pagal išlaidų grupę ir negalite nustatyti keturių gamybos nuokrypių tipų.</span><span class="sxs-lookup"><span data-stu-id="77835-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="77835-136">Galite peržiūrėti tik susumuotus gamybos nuokrypius.</span><span class="sxs-lookup"><span data-stu-id="77835-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="77835-137">Standartinė nuokrypių strategija veikia nepriklausomai nuo išlaidų paskirstymo strategijos.</span><span class="sxs-lookup"><span data-stu-id="77835-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="77835-138">Kitaip tariant, galite pasirinkti išlaidų paskirstymo strategiją **Nėra** ir pasirinkti išlaidų grupės nuokrypius taip, kad gamybos nuokrypiai pagal išlaidų grupę vis tiek bus užfiksuoti.</span><span class="sxs-lookup"><span data-stu-id="77835-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="77835-139">**5. Sukurkite standartinių savikainų įkainojimo versijas.**</span><span class="sxs-lookup"><span data-stu-id="77835-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="77835-140">Norėdami sukurti vieną ar kelias standartinių savikainų įkainojimo versijas, naudokite puslapį **Įkainojimo versijos nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="77835-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="77835-141">Kiekviena įkainojimo versija turi būti sukurta pagal įkainojimo tipą **Standartinė savikaina** ir turi leisti į turinį įtraukti išlaidų duomenis.</span><span class="sxs-lookup"><span data-stu-id="77835-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="77835-142">**6. Paruoškite esamą klientą naudoti standartines savikainas.**</span><span class="sxs-lookup"><span data-stu-id="77835-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="77835-143">Klientai, norintys pakeisti savo esamus komponentus į standartinių savikainų atsargų modelį, turi naudoti puslapį **Standartinių išlaidų konvertavimai**.</span><span class="sxs-lookup"><span data-stu-id="77835-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="77835-144">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="77835-144">Related topics</span></span>
--------

[<span data-ttu-id="77835-145">Standartinės savikainos konvertavimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="77835-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)

### <a name="blogs"></a><span data-ttu-id="77835-146">Tinklaraščiai</span><span class="sxs-lookup"><span data-stu-id="77835-146">Blogs</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="77835-147">Bendruomenės tinklaraščiai</span><span class="sxs-lookup"><span data-stu-id="77835-147">Community blogs</span></span>

- [<span data-ttu-id="77835-148">Kaip „Dynamics 365 for Finance and Operations“ nustatyti tiesioginių medžiagų standartines išlaidas</span><span class="sxs-lookup"><span data-stu-id="77835-148">How to set up standard costs for direct materials in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [<span data-ttu-id="77835-149">„Dynamics 365 for Finance and Operations“ tiesioginio darbo standartinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="77835-149">Standard direct labor costs in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)
