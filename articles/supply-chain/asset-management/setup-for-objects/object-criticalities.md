---
title: Turto svarbos tipai
description: Šioje temoje pasakojama apie turto svarbos tipus, esančius modulyje „Turto valdymas“.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb2da2d58b7f98fad80d0ea63bf4445ec4d08163
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808357"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="4acc0-103">Turto svarbos tipai</span><span class="sxs-lookup"><span data-stu-id="4acc0-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4acc0-104">Šioje temoje pasakojama apie turto svarbos tipus, esančius modulyje „Turto valdymas“.</span><span class="sxs-lookup"><span data-stu-id="4acc0-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="4acc0-105">Turto svarba yra susijusi su turtu ir perkeliama į darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="4acc0-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="4acc0-106">Darbo užsakyme jos keisti negalima.</span><span class="sxs-lookup"><span data-stu-id="4acc0-106">It can't be changed on a work order.</span></span> <span data-ttu-id="4acc0-107">Planuojant darbo užsakymą turto svarba naudojama siekiant apskaičiuoti darbo užsakymo svarbą.</span><span class="sxs-lookup"><span data-stu-id="4acc0-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="4acc0-108">Kitaip tariant, ji naudojama apskaičiuoti, kokios įtakos turto priežiūros užduotis turi gamybos grafikui ir įmonės produktyvumui.</span><span class="sxs-lookup"><span data-stu-id="4acc0-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="4acc0-109">Daugiau informacijos apie konfigūraciją, susijusią su darbo užsakymo planavimo vertinimo rezultatų skaičiavimu, žr. [Turto valdymo parametrai](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4acc0-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="4acc0-110">Norėdami nustatyti svarbą, pirmiausia sukurkite svarbos tipus, kurie turėtų būti naudojami šioje turto konfigūracijoje.</span><span class="sxs-lookup"><span data-stu-id="4acc0-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="4acc0-111">Tada nustatykite svarbos tipus.</span><span class="sxs-lookup"><span data-stu-id="4acc0-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="4acc0-112">Nustatyti pasirinktinius darbo tipus</span><span class="sxs-lookup"><span data-stu-id="4acc0-112">Set up criticality types</span></span>

1. <span data-ttu-id="4acc0-113">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turtas** \> **Svarbos tipai**.</span><span class="sxs-lookup"><span data-stu-id="4acc0-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="4acc0-114">Pasirinkite **Naujas** pranešimui sukurti.</span><span class="sxs-lookup"><span data-stu-id="4acc0-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="4acc0-115">Lauke **Svarba** įveskite skaičių, nurodantį svarbą.</span><span class="sxs-lookup"><span data-stu-id="4acc0-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="4acc0-116">Lauke **Pavadinimas** įveskite unikalų darbo eigos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="4acc0-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="4acc0-117">Lauke **Koeficientas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="4acc0-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="4acc0-118">Šis koeficientas naudojamas skaičiuojant darbo užsakymo planavimą, siekiant nustatyti svarbos įrašą, kurį reikėtų naudoti.</span><span class="sxs-lookup"><span data-stu-id="4acc0-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="4acc0-119">(Visada naudojamas įrašas, turintis aukščiausią koeficientą.) Šis nustatymas yra svarbus, jei, kaip parodyta toliau pateiktoje iliustracijoje, sukuriamos tos pačios kritiškumo vertės kritiškumo eilutės.</span><span class="sxs-lookup"><span data-stu-id="4acc0-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![Puslapis Kritiškumo tipai](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="4acc0-121">Ilgalaikio turto knygos nustatymas</span><span class="sxs-lookup"><span data-stu-id="4acc0-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="4acc0-122">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turto kritiškumai**.</span><span class="sxs-lookup"><span data-stu-id="4acc0-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="4acc0-123">Pasirinkite **Naujas** pranešimui sukurti.</span><span class="sxs-lookup"><span data-stu-id="4acc0-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="4acc0-124">Atsižvelgdami į reikiamą turto svarbos informacijos lygį, pasirinkite atitinkamus duomenis laukuose **Funkcinė vieta**, **Turto tipas**, **Gamintojas**, **Modelis**, **Turtas**, **Užduoties tipo kategorija**, **Užduoties tipas**, **Užduoties tipo variantas** ir **Užduoties reikalavimas**.</span><span class="sxs-lookup"><span data-stu-id="4acc0-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4acc0-125">Kai pasirenkate turto svarbą, turto valdymo programa apdoroja visus turto svarbos įrašus, kad surastų galimų atitikčių</span><span class="sxs-lookup"><span data-stu-id="4acc0-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="4acc0-126">Jis visada pirmiausiai tikrina konkrečiausius derinius.</span><span class="sxs-lookup"><span data-stu-id="4acc0-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="4acc0-127">Kitaip tariant, turto valdymo programa pirmiausia tikrina **Užduoties reikalavimą**.</span><span class="sxs-lookup"><span data-stu-id="4acc0-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="4acc0-128">Jei atitikties rasti nepavyksta, ji patikrina **Užduoties tipo variantą**.</span><span class="sxs-lookup"><span data-stu-id="4acc0-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="4acc0-129">Jei atitikties rasti nepavyksta, ji patikrina **Darbo tipas** ir t. t.</span><span class="sxs-lookup"><span data-stu-id="4acc0-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="4acc0-130">Kaip matote pagal puslapio išdėstymą, toks paieškos metodas reiškia, kad, siekiant rasti konkrečiausią derinį modulyje „Turto valdymas“, kiekviename įraše atitikčių ieškoma iš dešinės į kairę.</span><span class="sxs-lookup"><span data-stu-id="4acc0-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="4acc0-131">Jei atitikties rasti nepavyksta, naudojamas numatytasis įrašas, kuris pasirinkčių neturi.</span><span class="sxs-lookup"><span data-stu-id="4acc0-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="4acc0-132">Lauke **Kritiškumas** pasirinkite pagreitinimo kodus, kuriuos sukūrėte 1 procedūroje. Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="4acc0-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="4acc0-133">Pastabos apie svarbos konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="4acc0-133">Notes about criticality setup</span></span>

- <span data-ttu-id="4acc0-134">Jei pakeisite turto svarbą konfigūracijoje, kurią jau naudojote darbo užsakyme, šio darbo užsakymo svarba nebus atitinkamai atnaujinta.</span><span class="sxs-lookup"><span data-stu-id="4acc0-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="4acc0-135">Darbo užsakymo svarba iš naujo apskaičiuojama kaskart, kai prie darbo užsakymo pridedama arba pašalinama darbo užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="4acc0-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="4acc0-136">Jei darbo užsakymą sudaro keletas darbo užsakymo užduočių, remiantis puslapyje **Svarbos tipai** esančiu lauku **Koeficientas**, didžiausia svarba visada teikiama darbo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="4acc0-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="4acc0-137">Paprastai per tam tikrą laiką turto svarba gali keistis.</span><span class="sxs-lookup"><span data-stu-id="4acc0-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="4acc0-138">Svarbai gali turėti įtakos naujos įrangos pirkimas, atnaujinimas ir t. t.</span><span class="sxs-lookup"><span data-stu-id="4acc0-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="4acc0-139">Apsvarstykite galimybę reguliariais intervalais (pvz., kartą per metus arba kas antrus metus) iš naujo įvertinti savo turto svarbą, siekdami įsitikinti, kad jūsų svarbos apibrėžtys atitinka dabartinę gamybos konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="4acc0-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]