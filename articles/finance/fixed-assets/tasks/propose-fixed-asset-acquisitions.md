---
title: Ilgalaikio turto įsigijimų siūlymas
description: Šioje procedūroje parodoma, kaip įsigyti ilgalaikį turtą naudojant įsigijimo pasiūlymą, esantį žurnale Ilgalaikis turtas.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817175"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="08065-103">Ilgalaikio turto įsigijimų siūlymas</span><span class="sxs-lookup"><span data-stu-id="08065-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="08065-104">Šioje procedūroje parodoma, kaip įsigyti ilgalaikį turtą naudojant įsigijimo pasiūlymą, esantį žurnale Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="08065-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="08065-105">Joje naudojamas vaidmuo Buhalteris ir USMF juridinio subjekto demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="08065-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="08065-106">Siekiant gauti fiksuotą turtą per fiksuoto turto pasiūlymo žurnalą, pirmiausia turite sukurti fiksuoto turto įrašą ir tuomet nustatyti įsigijimo kainą turto knygoje.</span><span class="sxs-lookup"><span data-stu-id="08065-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="08065-107">Kurti turto įsigijimo pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="08065-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="08065-108">Norėdami sukurti turto įsigijimo pasiūlymą atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="08065-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="08065-109">Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="08065-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="08065-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="08065-110">Select **New**.</span></span>
3. <span data-ttu-id="08065-111">Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="08065-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="08065-112">Veiksmų srityje pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="08065-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="08065-113">Pasirinkite **Pasiūlymai**.</span><span class="sxs-lookup"><span data-stu-id="08065-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="08065-114">Pasirinkite **Siūlymas įsigyti**. </span><span class="sxs-lookup"><span data-stu-id="08065-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="08065-115">Pasirinkite **Filtras**.</span><span class="sxs-lookup"><span data-stu-id="08065-115">Select **Filter**.</span></span> <span data-ttu-id="08065-116">Spustelėkite **Nustatyti iš naujo**, kad išvalytumėte ankstesnes reikšmes.</span><span class="sxs-lookup"><span data-stu-id="08065-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="08065-117">Pasirinkite eilutę **Ilgalaikio turto numeris**.</span><span class="sxs-lookup"><span data-stu-id="08065-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="08065-118">Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="08065-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="08065-119">Nustatykite likusius ilgalaikio turto, kurį norite įsigyti šiuo pasiūlymu, kriterijus.</span><span class="sxs-lookup"><span data-stu-id="08065-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="08065-120">Norėdami išeiti iš srities, dukart pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="08065-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="08065-121">Patikrinkite, ar operacijų eilutės buvo sukurtos.</span><span class="sxs-lookup"><span data-stu-id="08065-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="08065-122">Įsigijimo pasiūlyme bus įtrauktas tik ilgalaikis turtas su knygoje nustatyta įsigijimo data ir įsigijimo kaina.</span><span class="sxs-lookup"><span data-stu-id="08065-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="08065-123">Kurkite knygas puslapyje **Knygos**.</span><span class="sxs-lookup"><span data-stu-id="08065-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="08065-124">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="08065-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="08065-125">Įtraukti numatytąsias finansines dimensijas į įsigijimo pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="08065-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="08065-126">Įsigijimo operaciją galima sukurti naudojant Excel papildinį, nueidami į Ilgalaikis turtas > Žurnalo įrašai **> Ilgalaikio turto** žurnalas.</span><span class="sxs-lookup"><span data-stu-id="08065-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="08065-127">Sukurkite naują žurnalą ir perkelkite į puslapio skyrių Eilutės, pasirinkite **piktogramą** „Excel“, tada pasirinkite ilgalaikio turto žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="08065-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="08065-128">Sistema sukurs ir atidarys „Excel“ šabloną, nurodantį žurnalo eilutes.</span><span class="sxs-lookup"><span data-stu-id="08065-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="08065-129">Galite pridėti žurnalo eilučių, kurias įtraukiate į šabloną, duomenis ir paskelbti tą informaciją atgal į sistemą.</span><span class="sxs-lookup"><span data-stu-id="08065-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="08065-130">Jei nustatytos pasirinktos turto knygos ir atitinkamo ilgalaikio turto, įvesto Excel šablone, numatytosios finansinės dimensijos bus iškviestos iš turto knygos pagrindinių duomenų, kai žurnalas publikuojamas iš „Excel“ į sistemą.</span><span class="sxs-lookup"><span data-stu-id="08065-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="08065-131">Norint finansines dimensijas automatiškai įtraukti į turto knygą publikuojant ilgalaikio turto žurnalą iš „Excel" priedo, numatytosios dimensijos turi būti nustatytos iš anksto.</span><span class="sxs-lookup"><span data-stu-id="08065-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
