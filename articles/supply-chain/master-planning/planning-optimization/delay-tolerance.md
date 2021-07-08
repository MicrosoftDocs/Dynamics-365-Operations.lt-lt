---
title: Leistinas uždelsimo nuokrypis (neigiamos dienos)
description: Šioje temoje pateikiama informacija apie leistino uždelsimo nuokrypio skaičiavimą ir apie tai, kaip jis veikia suplanuoto užsakymo kūrimą planavimo optimizavime.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306468"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="aae93-103">Leistinas uždelsimo nuokrypis (neigiamos dienos)</span><span class="sxs-lookup"><span data-stu-id="aae93-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="aae93-104">Leistino uždelsimo nuokrypio funkcija įgalina Planavimo optimizavimą atsižvelgti į **Neigiamų dienų** vertę, nustatytą padengimo grupėms.</span><span class="sxs-lookup"><span data-stu-id="aae93-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="aae93-105">Ji naudojama norint pratęsti leistino uždelsimo nuokrypio laikotarpį, taikomą bendrojo planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="aae93-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="aae93-106">Tokiu būdu galite išvengti naujų tiekimo užsakymų kūrimo, jei po trumpo vėlavimo esamas tiekimas galės padengti poreikį.</span><span class="sxs-lookup"><span data-stu-id="aae93-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="aae93-107">Funkcijos paskirtis – nustatyti, ar apsimoka kurti naują konkrečios paklausos tiekimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aae93-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="aae93-108">Funkcijos įjungimas sistemoje</span><span class="sxs-lookup"><span data-stu-id="aae93-108">Turn on the feature in your system</span></span>

<span data-ttu-id="aae93-109">Norėdami, kad jūsų sistemoje leistino uždelsimo nuokrypio funkcija būtų galima, eikite į [Funkcijų valdymas](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir įjunkite *Negatyvios dienos Planavimo optimizavimui* funkciją.</span><span class="sxs-lookup"><span data-stu-id="aae93-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="aae93-110">Leidžiamas atidėjimas Planavimo optimizavime</span><span class="sxs-lookup"><span data-stu-id="aae93-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="aae93-111">Leistinas uždelsimo nuokrypis nurodo dienų skaičių po gamybos laiko, kurį galite laukti prieš užsakę naują papildymą, kai esamas tiekimas jau yra suplanuotas.</span><span class="sxs-lookup"><span data-stu-id="aae93-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="aae93-112">Leistinas uždelsimo nuokrypis apibrėžiamas naudojant kalendorines, o ne darbo dienas.</span><span class="sxs-lookup"><span data-stu-id="aae93-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="aae93-113">Bendrojo planavimo metu, kai sistema apskaičiuoja leistiną uždelsimo nuokrypį, atsižvelgiama į **Neigiamų dienų** nustatymą.</span><span class="sxs-lookup"><span data-stu-id="aae93-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="aae93-114">Galite nustatyti **Neigiamų dienų** reikšmę **Padengimo grupių** arba **Prekės padengimo** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="aae93-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="aae93-115">Sistema susieja atidėjimo nuokrypio skaičiavimą su *anksčiausia papildymo data*, kuri yra lygi šiandienos datai pridėjus gamybos laiką.</span><span class="sxs-lookup"><span data-stu-id="aae93-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="aae93-116">Leistinas uždelsimo nuokrypis apskaičiuojamas naudojant šią formulę, kurioje *maks()* suranda didesnę iš dviejų verčių:</span><span class="sxs-lookup"><span data-stu-id="aae93-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="aae93-117">*maks(Anksčiausia papildymo data, Poreikio terminas)* – *Poreikio terminas* + *Neigiamos dienos*</span><span class="sxs-lookup"><span data-stu-id="aae93-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="aae93-118">Ši formulė užtikrina, kad bendrasis planavimas nekuria naujų tiekimo užsakymų, kai tiekimas yra pakankamas produkto gamybos laiku.</span><span class="sxs-lookup"><span data-stu-id="aae93-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="aae93-119">Leistino uždelsimo nuokrypio skaičiavimas Planavimo optimizavime visada naudoja dinaminį neigiamų dienų skaičiavimą iš įtaisytojo bendrojo planavimo.</span><span class="sxs-lookup"><span data-stu-id="aae93-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="aae93-120">Parametras **Naudoti dinamines neigiamas dienas** puslapyje **Bendrojo planavimo parametrai** neturi įtakos šiai elgsenai.</span><span class="sxs-lookup"><span data-stu-id="aae93-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="aae93-121">Jei esamas tiekimas numano poreikio atidėjimą, kuris yra mažesnis arba lygus apskaičiuotam leistinam uždelsimo nuokrypiui, Planavimo optimizavimas iškviestų esamą tiekimą pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="aae93-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="aae93-122">Kai kuriais atvejais geriau atidėti poreikį nei turėti tiekimo perviršį.</span><span class="sxs-lookup"><span data-stu-id="aae93-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="aae93-123">Toliau pateikti poskyriai pateikia pavyzdžių, kurie parodo, kaip leistinas uždelsimo nuokrypis paveikia suplanuotų užsakymų kūrimą Planavimo optimizavime.</span><span class="sxs-lookup"><span data-stu-id="aae93-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="aae93-124">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="aae93-124">Example 1</span></span>

<span data-ttu-id="aae93-125">Produktas turi šią konfigūraciją:</span><span class="sxs-lookup"><span data-stu-id="aae93-125">A product has the following configuration:</span></span>

- <span data-ttu-id="aae93-126">**Gamybos laikas:** *10*</span><span class="sxs-lookup"><span data-stu-id="aae93-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="aae93-127">**Neigiamos dienos:** *2*</span><span class="sxs-lookup"><span data-stu-id="aae93-127">**Negative days:** *2*</span></span>

<span data-ttu-id="aae93-128">Yra toks produkto tiekimas ir poreikis:</span><span class="sxs-lookup"><span data-stu-id="aae93-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="aae93-129">**Poreikis šiandien:** Pardavimo užsakymas, kurio kiekis yra 10</span><span class="sxs-lookup"><span data-stu-id="aae93-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="aae93-130">**Tiekimas per 12 dienų:** Pirkimo užsakymas, kurio kiekis yra 10</span><span class="sxs-lookup"><span data-stu-id="aae93-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="aae93-131">Esamas tiekimas gali padengti poreikį per 12 dienų, o šis laikotarpis yra lygus leistinam uždelsimo nuokrypiui.</span><span class="sxs-lookup"><span data-stu-id="aae93-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="aae93-132">Todėl, kai vykdomas bendrasis planavimas, nesukuriami jokie suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="aae93-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="aae93-133">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="aae93-133">Example 2</span></span>

<span data-ttu-id="aae93-134">Produktas turi šią konfigūraciją:</span><span class="sxs-lookup"><span data-stu-id="aae93-134">A product has the following configuration:</span></span>

- <span data-ttu-id="aae93-135">**Gamybos laikas:** *10*</span><span class="sxs-lookup"><span data-stu-id="aae93-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="aae93-136">**Neigiamos dienos:** *0*</span><span class="sxs-lookup"><span data-stu-id="aae93-136">**Negative days:** *0*</span></span>

<span data-ttu-id="aae93-137">Yra toks produkto tiekimas ir poreikis:</span><span class="sxs-lookup"><span data-stu-id="aae93-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="aae93-138">**Poreikis šiandien:** Pardavimo užsakymas, kurio kiekis yra 10</span><span class="sxs-lookup"><span data-stu-id="aae93-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="aae93-139">**Tiekimas per 12 dienų:** Pirkimo užsakymas, kurio kiekis yra 10</span><span class="sxs-lookup"><span data-stu-id="aae93-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="aae93-140">Esamas tiekimas gali padengti poreikį tik po 12 dienų.</span><span class="sxs-lookup"><span data-stu-id="aae93-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="aae93-141">Tačiau leistinas uždelsimo nuokrypis yra 10 dienų.</span><span class="sxs-lookup"><span data-stu-id="aae93-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="aae93-142">Todėl, kai vykdomas bendrasis planavimas, sukuriamas suplanuotas užsakymas, kurio kiekis yra 10.</span><span class="sxs-lookup"><span data-stu-id="aae93-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="aae93-143">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="aae93-143">Example 3</span></span>

<span data-ttu-id="aae93-144">Produktas turi šią konfigūraciją:</span><span class="sxs-lookup"><span data-stu-id="aae93-144">A product has the following configuration:</span></span>

- <span data-ttu-id="aae93-145">**Gamybos laikas:** *10*</span><span class="sxs-lookup"><span data-stu-id="aae93-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="aae93-146">**Neigiamos dienos:** *2*</span><span class="sxs-lookup"><span data-stu-id="aae93-146">**Negative days:** *2*</span></span>

<span data-ttu-id="aae93-147">Yra toks produkto tiekimas ir poreikis:</span><span class="sxs-lookup"><span data-stu-id="aae93-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="aae93-148">**Poreikis per 11 dienų:** Pardavimo užsakymas, kurio kiekis yra 10</span><span class="sxs-lookup"><span data-stu-id="aae93-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="aae93-149">**Tiekimas per 14 dienų:** Pirkimo užsakymas, kurio kiekis yra 10</span><span class="sxs-lookup"><span data-stu-id="aae93-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="aae93-150">Esamas tiekimas gali padengti poreikį tik po trijų dienų.</span><span class="sxs-lookup"><span data-stu-id="aae93-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="aae93-151">Tačiau leistinas uždelsimo nuokrypis yra dvi dienos.</span><span class="sxs-lookup"><span data-stu-id="aae93-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="aae93-152">Šiuo atveju leistinas uždelsimo nuokrypis apima tik dvi neigiamas dienas.</span><span class="sxs-lookup"><span data-stu-id="aae93-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="aae93-153">Poreikio data neįtraukiama, nes ji yra pasibaigus produkto gamybos laikui. Todėl, kai vykdomas bendrasis planavimas, sukuriamas suplanuotas užsakymas, kurio kiekis yra 10.</span><span class="sxs-lookup"><span data-stu-id="aae93-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
