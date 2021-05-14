---
title: Kokybės valdymo bandymo kintamieji
description: Šioje temoje aprašoma, kaip sukurti tikrinimo priemones, kurias galima naudoti kokybės užsakymų „Microsoft Dynamics 365 Supply Chain Management“ bandymams.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e94972b41baf3f59a633fa7bbc7434abfb90460
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956759"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="8a244-103">Kokybės valdymo bandymo kintamieji</span><span class="sxs-lookup"><span data-stu-id="8a244-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a244-104">Šioje temoje aprašoma, kaip sukurti tikrinimo priemones, kurias galima naudoti kokybės užsakymų „Microsoft Dynamics 365 Supply Chain Management“ bandymams.</span><span class="sxs-lookup"><span data-stu-id="8a244-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="8a244-105">Turite apibrėžti kiekvieno kokybinio bandymo, kuris apibrėžtas puslapyje **Bandymai**, turite nustatyti kintamąjį ir galimus rezultatus.</span><span class="sxs-lookup"><span data-stu-id="8a244-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="8a244-106">(Kokybinių bandymų **tipas** laukelis **Bandymų** puslapyje nustatytas į *Parinktis*.)</span><span class="sxs-lookup"><span data-stu-id="8a244-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="8a244-107">Naudokitee **Bandymo kintamųjų** puslapį siekiant nustatyti, redaguoti ir peržiūrėti galimus rezultatus testo kintamajam, susietam su kokybės testu.</span><span class="sxs-lookup"><span data-stu-id="8a244-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="8a244-108">Kiekvienam rezultatui priskiriate rezultato būseną Teigiamas arba Nesėkmingas, kad nurodytų, ar tikrinimas buvo perduotas ar nesėkmingas, kai šis rezultatas pasirenkamas *kaip* tikrinimo *rezultatas*.</span><span class="sxs-lookup"><span data-stu-id="8a244-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="8a244-109">Naudokite **Bandymų grupių** puslapį, kad atskiram kokybiniam bandymui priskirtumėte bandymų kintamąjį ir numatytąjį rezultatą.</span><span class="sxs-lookup"><span data-stu-id="8a244-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="8a244-110">Kiekvienam bandymo kintamajam rekomenduojame nustatyti bent du rezultatus: vieno rezultato būsena yra Perdavimas, o jo rezultato *būsena* – *Nepavyko*.</span><span class="sxs-lookup"><span data-stu-id="8a244-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="8a244-111">Nėra bendro kintamųjų arba pasekmių, kurias galima nustatyti, skaičiaus limito.</span><span class="sxs-lookup"><span data-stu-id="8a244-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="8a244-112">Be to, norėdami įrašyti rezultatus, keliuose bandymuose gali būti naudojami tie patys bandymo kintamieji.</span><span class="sxs-lookup"><span data-stu-id="8a244-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="8a244-113">Bandymo kintamųjų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="8a244-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="8a244-114">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="8a244-114">Example 1</span></span>

<span data-ttu-id="8a244-115">Gamybos įmonė atlieka du pagamintų medžiagų bandymus.</span><span class="sxs-lookup"><span data-stu-id="8a244-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="8a244-116">Vieno bandymo metu pH lygis siejamas su spalvos juostelėmis.</span><span class="sxs-lookup"><span data-stu-id="8a244-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="8a244-117">Priimtini pH lygiai yra šviesesnės spalvos, o nepriimtina pH lygiai yra tamsesnės spalvos.</span><span class="sxs-lookup"><span data-stu-id="8a244-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="8a244-118">Atliekant kitą tikrinimą atliekami keli vaizdiniai tikrinimai, o kokybės darbuotojai naudoja savo patikrą, norėdami nustatyti, ar prekė įeina, ar neiš tikrina vaizdinio tikrinimo.</span><span class="sxs-lookup"><span data-stu-id="8a244-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="8a244-119">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="8a244-119">Example 2</span></span>

<span data-ttu-id="8a244-120">Gamybos įmonė, kepanti sausainius, naudoja galutinio produkto bandymą.</span><span class="sxs-lookup"><span data-stu-id="8a244-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="8a244-121">Šis bandymas turi keletą kintamųjų.</span><span class="sxs-lookup"><span data-stu-id="8a244-121">This inspection test has several variables.</span></span> <span data-ttu-id="8a244-122">Vienas kintamasis yra skonis, ir galimi šio kintamojo rezultatai yra „geras“ ir „blogas“.</span><span class="sxs-lookup"><span data-stu-id="8a244-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="8a244-123">Antras kintamasis yra spalva, ir galimi rezultatai yra „per tamsūs“, „per šviesūs“ ir „tinkami“.</span><span class="sxs-lookup"><span data-stu-id="8a244-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="8a244-124">Naujo bandymo kintamojo kūrimas</span><span class="sxs-lookup"><span data-stu-id="8a244-124">Create a test variable</span></span>

<span data-ttu-id="8a244-125">Atlikite šiuos žingsnius, kad sukurtumėte bandymo kintamąjį.</span><span class="sxs-lookup"><span data-stu-id="8a244-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="8a244-126">Pasirinkite **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Kintamųjų testavimas**.</span><span class="sxs-lookup"><span data-stu-id="8a244-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="8a244-127">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="8a244-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="8a244-128">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="8a244-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8a244-129">**Kintamasis** – įveskite unikalų kintamojo prietaiso ID arba pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="8a244-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="8a244-130">**Aprašas** – įveskite išsamų bandymo kintamojo aprašą.</span><span class="sxs-lookup"><span data-stu-id="8a244-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="8a244-131">Kol nauja eilutė vis dar pasirinkta, **Rezultatai** Neatitikties tipai.</span><span class="sxs-lookup"><span data-stu-id="8a244-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="8a244-132">Puslapyje **Bandymo kintamojo rezultatai** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="8a244-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="8a244-133">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="8a244-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="8a244-134">**Išvados** – įveskite unikalų išvados ID arba pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="8a244-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="8a244-135">**Aprašas** – įveskite išsamų išvados aprašą.</span><span class="sxs-lookup"><span data-stu-id="8a244-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="8a244-136">**Išvados būsena** – Rinkitės *atitiko* ar *neatitikol* kad nurodytumėte, ar tikrinimas buvo perduotas ar nesėkmingas, kai šis rezultatas pasirenkamas.</span><span class="sxs-lookup"><span data-stu-id="8a244-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="8a244-137">Pakartokite ankstesnį veiksmą kiekvienam papildomam rezultatui.</span><span class="sxs-lookup"><span data-stu-id="8a244-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="8a244-138">Įsitikinkite, kad bent vieno rezultato būsena yra *Perdavimas, o bent vieno* rezultato būsena yra *Nepavyko*.</span><span class="sxs-lookup"><span data-stu-id="8a244-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="8a244-139">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="8a244-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a244-140">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="8a244-140">Additional resources</span></span>

- [<span data-ttu-id="8a244-141">Kokybės valdymo bandymo instrumentai</span><span class="sxs-lookup"><span data-stu-id="8a244-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="8a244-142">Kokybės valdymo bandymai</span><span class="sxs-lookup"><span data-stu-id="8a244-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="8a244-143">Kokybės valdymo bandymo grupės</span><span class="sxs-lookup"><span data-stu-id="8a244-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
