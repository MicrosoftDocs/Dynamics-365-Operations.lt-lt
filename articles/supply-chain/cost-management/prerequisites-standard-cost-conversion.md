---
title: "Būtinos standartinių išlaidų konvertavimo sąlygos"
description: "Šioje temoje aptariama užduotis, kurią reikia atlikti prieš vykdant standartinių išlaidų konvertavimą."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0ee55ef8a1d7ee47ff3b7d24b50da613dd2ac4ce
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="prerequisites-for-a-standard-cost-conversion"></a><span data-ttu-id="8283e-103">Būtinos standartinių išlaidų konvertavimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="8283e-103">Prerequisites for a standard cost conversion</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8283e-104">Šioje temoje aptariama užduotis, kurią reikia atlikti prieš vykdant standartinių išlaidų konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="8283e-104">This topic discusses tasks to perform before you run a standard cost conversion.</span></span> 

<span data-ttu-id="8283e-105">Prieš atlikdami standartinių išlaidų konvertavimą, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="8283e-105">Before you run a standard cost conversion, follow these steps:</span></span>

1.  <span data-ttu-id="8283e-106">Nustatykite standartinių išlaidų **prekių modelių grupę**.</span><span class="sxs-lookup"><span data-stu-id="8283e-106">Define an **item model group** for standard costs.</span></span> <span data-ttu-id="8283e-107">Naudokite puslapį Prekių modelio grupės, kad sukurtumėte prekių modelio grupę, kurioje naudojamas standartinių išlaidų atsargų modelis.</span><span class="sxs-lookup"><span data-stu-id="8283e-107">Use the Item model groups page to create an item model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="8283e-108">Nustatydami standartinių išlaidų konvertavimą, priskiriate šią prekių modelių grupę konvertuojamoms prekėms.</span><span class="sxs-lookup"><span data-stu-id="8283e-108">When setting up a standard cost conversion, you assign this item model group to the items that are being converted.</span></span>
2.  <span data-ttu-id="8283e-109">Kiekvienai prekei priskirkite **išlaidų grupę**.</span><span class="sxs-lookup"><span data-stu-id="8283e-109">Assign a **cost group** to each item.</span></span>
    -   <span data-ttu-id="8283e-110">Išlaidų grupė, priskirta nupirktai prekei, gali veikti kaip pagrindas priskiriant DK sąskaitas, susijusias su standartinėmis išlaidomis.</span><span class="sxs-lookup"><span data-stu-id="8283e-110">The cost group that is assigned to a purchased item can act as the basis for assigning ledger accounts that are related to standard costs.</span></span> <span data-ttu-id="8283e-111">Tai apima DK sąskaitų priskyrimą pirkimo kainų nuokrypiams.</span><span class="sxs-lookup"><span data-stu-id="8283e-111">This can include assigning ledger accounts for purchase price variances.</span></span> <span data-ttu-id="8283e-112">Gamybos aplinkoje nupirktiems komponentams priskirta išlaidų grupė taip pat suteikia išlaidų segmentavimą apskaičiuotose pagamintos prekės išlaidose.</span><span class="sxs-lookup"><span data-stu-id="8283e-112">In a manufacturing environment, the cost group that is assigned to purchased components also provides cost segmentation in the calculated costs of a manufactured item.</span></span>
    -   <span data-ttu-id="8283e-113">Pagamintai prekei priskirta išlaidų grupė gali veikti kaip pagrindas priskiriant DK sąskaitas, susijusias su standartinėmis išlaidomis, pvz., DK sąskaitų priskyrimas gamybos nuokrypiams.</span><span class="sxs-lookup"><span data-stu-id="8283e-113">The cost group that is assigned to a manufactured item can act as the basis for assigning ledger accounts that are related to standard costs, such as assigning ledger accounts for production variances.</span></span>

3.  <span data-ttu-id="8283e-114">Pagamintai prekei, kurios išlaidos yra pastovios, priskirkite **standartinį užsakymo kiekį**.</span><span class="sxs-lookup"><span data-stu-id="8283e-114">Assign a **standard order quantity** to a manufactured item when it has constant costs.</span></span> <span data-ttu-id="8283e-115">Pagamintos prekės standartinis užsakymo kiekis veikia kaip amortizavimo, arba skirstymo, pastoviųjų išlaidų apskaitos partijos dydis.</span><span class="sxs-lookup"><span data-stu-id="8283e-115">The standard order quantity for a manufactured item acts as an accounting lot size for amortizing, or prorating, constant costs.</span></span> <span data-ttu-id="8283e-116">Tai apima nukreipimo operacijų nustatymo laiką arba pastovų komponentų kiekį komplektavimo specifikacijoje (KS).</span><span class="sxs-lookup"><span data-stu-id="8283e-116">These can include setup times in routing operations or a constant component quantity in a bill of material (BOM).</span></span>
4.  <span data-ttu-id="8283e-117">Priskirti **DK sąskaitas**, susijusias su standartinėmis išlaidomis, ypač su perkainojimo nuokrypiu.</span><span class="sxs-lookup"><span data-stu-id="8283e-117">Assign **general ledger accounts** that are related to standard costs, especially the revaluation variance.</span></span> <span data-ttu-id="8283e-118">Naudokite puslapį **Registravimas** (**Atsargų valdymas** &gt; **Sąranka**), kad priskirtumėte DK sąskaitas, susijusias su standartinėmis išlaidomis.</span><span class="sxs-lookup"><span data-stu-id="8283e-118">Use the **Posting** page (**Inventory management** &gt; **Setup**) to assign general ledger accounts that are related to standard costs.</span></span> <span data-ttu-id="8283e-119">Standartinių išlaidų konvertavimo procesui reikia bent priskirti sąskaitą visų prekių ir visų išlaidų grupių perkainojimo nuokrypiui.</span><span class="sxs-lookup"><span data-stu-id="8283e-119">As a minimum for the standard cost conversion process, you must assign the account for the revaluation variance for all items and all cost groups.</span></span> <span data-ttu-id="8283e-120">Naudokite puslapį **Sąskaitų planas**, norėdami apibrėžti DK sąskaitas, kurių reikės standartinėms išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="8283e-120">Use the **Chart of accounts** page to define the general ledger accounts that will be needed for standard costs.</span></span> <span data-ttu-id="8283e-121">Naudokite puslapį **Operacijų deriniai** norėdami įgalioti išlaidų santykius (lentelėms, grupėms ir viskam) prieš nustatydami prekių registravimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="8283e-121">Use the **Transaction combinations** page to enable cost relations (for tables, groups, and all) before you define the item posting rules.</span></span>
5.  <span data-ttu-id="8283e-122">Nustatykite atsargų parametrus, kurie yra susiję su standartinėmis išlaidomis.</span><span class="sxs-lookup"><span data-stu-id="8283e-122">Define the inventory parameters that are related to standard costs.</span></span> <span data-ttu-id="8283e-123">Naudokite puslapyje **Atsargų ir sandėlio valdymo parametrai** esantį skirtuką **Numeracija** norėdami priskirti numeraciją perkainojimo kvitams.</span><span class="sxs-lookup"><span data-stu-id="8283e-123">Use the **Number sequences** tab on the **Inventory and warehouse management parameters** page to assign a number sequence to revaluation vouchers.</span></span> <span data-ttu-id="8283e-124">Perkainojimo kvitas generuojamas tada, kai dėl standartinių išlaidų konvertavimo įvyksta prekės atsargų vertės pokytis.</span><span class="sxs-lookup"><span data-stu-id="8283e-124">A revaluation voucher is generated when the standard cost conversion creates a change of an item's inventory value.</span></span> <span data-ttu-id="8283e-125">Naudokite puslapį **Atsargų ir sandėlio valdymo parametrai** norėdami nustatyti išlaidų valdymo parametrus (skirtuke **Atsargų apskaita**), kad nustatytumėte du parametrus, kurie yra susiję su standartinėmis išlaidomis.</span><span class="sxs-lookup"><span data-stu-id="8283e-125">Use the **Inventory and warehouse management parameters** page to define Cost Control parameters (on the **Inventory accounting** tab) to define two parameters that are related to standard costs.</span></span>
    -   <span data-ttu-id="8283e-126">Lauke **Išlaidų paskirstymas** pasirinkite Ne arba Antrinė DK.</span><span class="sxs-lookup"><span data-stu-id="8283e-126">Use the **Cost breakdown** field to select No or Sub ledger.</span></span> <span data-ttu-id="8283e-127">Antrinės DK pasirinkimas vadinamas aktyviu išlaidų paskirstymu.</span><span class="sxs-lookup"><span data-stu-id="8283e-127">The selection of Sub ledger is termed an active cost breakdown.</span></span> <span data-ttu-id="8283e-128">Aktyvus išlaidų paskirstymas yra labai svarbus skaičiavimui, išlaikymui ir išlaidų grupės segmentavimo peržiūrai visoje standartinių išlaidų komponentų kelių lygių produkto struktūroje.</span><span class="sxs-lookup"><span data-stu-id="8283e-128">An active cost breakdown is very important for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="8283e-129">Kai išlaidų paskirstymas yra aktyvus, galite paskelbti ir analizuoti toliau nurodytus elementus vieno lygio, kelių lygių ar visu formatu:</span><span class="sxs-lookup"><span data-stu-id="8283e-129">When the cost breakdown is active, you can report and analyze the following in a single level, multi-level, or total format:</span></span>
        1.  <span data-ttu-id="8283e-130">Atsargos</span><span class="sxs-lookup"><span data-stu-id="8283e-130">Inventory</span></span>
        2.  <span data-ttu-id="8283e-131">Nebaigta gamyba (NG)</span><span class="sxs-lookup"><span data-stu-id="8283e-131">Work in process (WIP)</span></span>
        3.  <span data-ttu-id="8283e-132">Parduotų prekių savikaina (PPS) pagal išlaidų grupę</span><span class="sxs-lookup"><span data-stu-id="8283e-132">Cost of goods sold (COGS) per cost group</span></span>

        <span data-ttu-id="8283e-133">Aktyvus išlaidų paskirstymas reiškia, kad, suaktyvinus pagamintos prekės išlaidas, rezultatas bus saugomas išlaidų grupių segmentavime prekės išlaidų įraše.</span><span class="sxs-lookup"><span data-stu-id="8283e-133">An active cost breakdown means that if you enable a manufactured item's cost, the result will be stored in the cost group segmentation in the item's cost record.</span></span> <span data-ttu-id="8283e-134">Jei lauke **Išlaidų paskirstymas** neįvesite vertės, išlaidų grupės segmentavimas nebus išsaugotas standartinių išlaidų komponentams.</span><span class="sxs-lookup"><span data-stu-id="8283e-134">If you put no value in the **Cost breakdown** field, the cost group segmentation will not be maintained for standard cost items.</span></span> <span data-ttu-id="8283e-135">Vadinasi, pagamintų prekių standartinės išlaidos bus apskaičiuotos ir liks vienintelė suma be išlaidų grupių segmentavimo o pagamintų komponentų išlaidų įnašai bus sujungti į vieną sumą.</span><span class="sxs-lookup"><span data-stu-id="8283e-135">That is, a manufactured item's standard cost will be calculated and maintained as a single amount without cost group segmentation, and the cost contributions of manufactured components will be aggregated into the single amount.</span></span>
    -   <span data-ttu-id="8283e-136">Naudokite lauką **Nuokrypiai nuo standarto** norėdami pasirinkti susumuotą grupę ar grupę pagal išlaidas.</span><span class="sxs-lookup"><span data-stu-id="8283e-136">Use the **Variances to standard** field to select summarized or per cost group.</span></span> <span data-ttu-id="8283e-137">Pasirinkus grupę pagal išlaidas galima identifikuoti pirkimo kainų nuokrypius ir gamybos nuokrypius pagal išlaidų grupę.</span><span class="sxs-lookup"><span data-stu-id="8283e-137">The selection of per cost group enables you to identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="8283e-138">Tai taip pat leidžia identifikuoti keturis gamybos nuokrypių tipus (partijos dydis, kiekis, kaina ir pakaitalų nuokrypiai).</span><span class="sxs-lookup"><span data-stu-id="8283e-138">This also enables you to identify the four types of production variances (the lot size, quantity, price, and substitution variances).</span></span> <span data-ttu-id="8283e-139">Pasirinkę susumuotą grupę negalėsite identifikuoti nuokrypių pagal išlaidų grupę ir negalėsite identifikuoti keturių gamybos nuokrypių tipų.</span><span class="sxs-lookup"><span data-stu-id="8283e-139">If you select summarized, you cannot identify variances by cost group, and you cannot identify the four types of production variances.</span></span> <span data-ttu-id="8283e-140">Galėsite tik peržiūrėti susumuotus gamybos nuokrypius.</span><span class="sxs-lookup"><span data-stu-id="8283e-140">You can only view a summarized production variance.</span></span> <span data-ttu-id="8283e-141">Standartinė nuokrypių strategija yra nepriklausoma nuo išlaidų paskirstymo strategijos.</span><span class="sxs-lookup"><span data-stu-id="8283e-141">The policy about variance to standard is independent of the cost breakdown policy.</span></span> <span data-ttu-id="8283e-142">Tai reiškia, galite nepasirinkti jokios išlaidų paskirstymo strategijos ir pasirinkti išlaidų grupės nuokrypius taip, kad gamybos nuokrypiai pagal išlaidų grupę vis tiek bus užfiksuoti.</span><span class="sxs-lookup"><span data-stu-id="8283e-142">That is, you can select a cost breakdown policy of none, and select variances per cost group, so that production variances by cost group will still be captured.</span></span>





