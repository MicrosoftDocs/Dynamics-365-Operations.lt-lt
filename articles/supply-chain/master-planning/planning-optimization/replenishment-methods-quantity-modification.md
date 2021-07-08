---
title: Papildymo metodai ir kiekio modifikavimas
description: Šioje temoje pateikiama informacija apie papildymo metodus Planavimo optimizavime. Joje taip pat paaiškinama, kaip keli produkto užsakymo kiekiai paveikia rezultatą.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261701"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="488b0-104">Papildymo metodai ir kiekio modifikavimas</span><span class="sxs-lookup"><span data-stu-id="488b0-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="488b0-105">Šioje temoje pateikiama informacija apie papildymo metodus Planavimo optimizavime.</span><span class="sxs-lookup"><span data-stu-id="488b0-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="488b0-106">Joje taip pat paaiškinama, kaip keli produkto užsakymo kiekiai paveikia rezultatą.</span><span class="sxs-lookup"><span data-stu-id="488b0-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="488b0-107">Papildymo metodai taip pat yra žinomi kaip padengimo ir partijos nustatymo metodai.</span><span class="sxs-lookup"><span data-stu-id="488b0-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="488b0-108">Padengimo kodai</span><span class="sxs-lookup"><span data-stu-id="488b0-108">Coverage codes</span></span>

<span data-ttu-id="488b0-109">Planavimo optimizavimą galima konfigūruoti, kad būtų naudojami skirtingi papildymo metodai.</span><span class="sxs-lookup"><span data-stu-id="488b0-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="488b0-110">Papildymo metodai yra principai, kuriuos sistema naudoja produkto reikalavimams skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="488b0-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="488b0-111">Papildymo metodai apibrėžiami pagal padengimo kodus, kuriuos galite nustatyti padengimo grupėje arba produkte.</span><span class="sxs-lookup"><span data-stu-id="488b0-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="488b0-112">Planavimo optimizavime galima naudoti šiuos padengimo kodus:</span><span class="sxs-lookup"><span data-stu-id="488b0-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="488b0-113">**Laikotarpis** – papildymo metodas sujungia visą laikotarpio paklausą į vieną produkto užsakymą.</span><span class="sxs-lookup"><span data-stu-id="488b0-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="488b0-114">Užsakymas bus suplanuotas pirmai laikotarpio dienai ir jo kiekis patenkins grynuosius poreikius nustatyto laikotarpio metu.</span><span class="sxs-lookup"><span data-stu-id="488b0-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="488b0-115">Laikotarpis pradedamas nuo pirmo produkto poreikio ir apima nustatytą laiko trukmę.</span><span class="sxs-lookup"><span data-stu-id="488b0-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="488b0-116">Kitas laikotarpis prasidės nuo kitų produkto reikalavimų.</span><span class="sxs-lookup"><span data-stu-id="488b0-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="488b0-117">*Laikotarpio* padengimo kodas dažnai naudojamas nenuspėjamam atsargų paėmimui, sezoniniams arba aukštos savikainos produktams.</span><span class="sxs-lookup"><span data-stu-id="488b0-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="488b0-118">Toliau pateikiamoje iliustracijoje vaizduojamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="488b0-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="488b0-119">![Laikotarpio padengimo kodo naudojimo pavyzdys](./media/coverage-code-period.png "Laikotarpio padengimo kodo panaudojimo pavyzdys")</span><span class="sxs-lookup"><span data-stu-id="488b0-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="488b0-120">**Reikalavimas** – papildymo metode sistema sukuria suplanuotą pirkimo, perkėlimo ar gamybos užsakymą kiekvienam produkto reikalavimui.</span><span class="sxs-lookup"><span data-stu-id="488b0-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="488b0-121">Šis metodas naudojamas brangesniems produktams, turintiems pasikartojantį poreikį.</span><span class="sxs-lookup"><span data-stu-id="488b0-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="488b0-122">*Reikalavimo* padengimo kodas dažnai naudojamas konfigūruojamiems produktams arba gamybos pagal užsakymą scenarijams.</span><span class="sxs-lookup"><span data-stu-id="488b0-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="488b0-123">Toliau pateikiamoje iliustracijoje vaizduojamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="488b0-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="488b0-124">![Reikalavimų padengimo kodo panaudojimo pavyzdys](./media/coverage-code-requirement.png "Reikalavimų padengimo kodo panaudojimo pavyzdys")</span><span class="sxs-lookup"><span data-stu-id="488b0-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="488b0-125">**Min./maks.**</span><span class="sxs-lookup"><span data-stu-id="488b0-125">**Min./Max.**</span></span> <span data-ttu-id="488b0-126">– Papildymo metodas yra pagrįstas atsargų lygiu.</span><span class="sxs-lookup"><span data-stu-id="488b0-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="488b0-127">Jis apibrėžia atsargų papildymą iki konkretaus lygio, kai numatomas turimų atsargų lygis yra mažesnis nei konkreti ribinė vertė.</span><span class="sxs-lookup"><span data-stu-id="488b0-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="488b0-128">Papildymo kiekis bus skirtumas tarp maksimalaus lygio ir prognozuojamo turimų atsargų lygio.</span><span class="sxs-lookup"><span data-stu-id="488b0-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="488b0-129">*Min. / Maks.*</span><span class="sxs-lookup"><span data-stu-id="488b0-129">The *Min./Max.*</span></span> <span data-ttu-id="488b0-130">padengimo kodas dažnai naudojamas numatytajam atsargų paėmimui, aukšto lygio eigoms ar mažiau brangesniems produktams.</span><span class="sxs-lookup"><span data-stu-id="488b0-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="488b0-131">Toliau pateikiamoje iliustracijoje vaizduojamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="488b0-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="488b0-132">![Min. / Max. padengimo kodo panaudojimo pavyzdys](./media/coverage-code-min-max.png "Min. / Max. padengimo kodo panaudojimo pavyzdys")</span><span class="sxs-lookup"><span data-stu-id="488b0-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="488b0-133">**Rankinis** – Papildymo metodas, kai sistema nenurodo produkto pirkimo, perkėlimo ar gamybos užsakymų.</span><span class="sxs-lookup"><span data-stu-id="488b0-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="488b0-134">Vietoj to, produkto planuotojas yra atsakingas už produkto papildymui reikalingų užsakymų sukūrimą.</span><span class="sxs-lookup"><span data-stu-id="488b0-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="488b0-135">*Rankinis* padengimo kodas dažnai naudojamas produktams, kurių sistemos sugeneruoti suplanuoti užsakymai nenori.</span><span class="sxs-lookup"><span data-stu-id="488b0-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="488b0-136">Užsakymo kiekio iš numatytųjų užsakymo parametrų poveikis</span><span class="sxs-lookup"><span data-stu-id="488b0-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="488b0-137">Išleisto produkto **Numatytojo užsakymo parametrų** puslapyje galite nurodyti kiekvieną iš toliau pateiktų kiekio parametrų **Pirkimo užsakymo**, **Atsargų** ir **Pardavimo užsakymo** „FastTab” skirtukuose.</span><span class="sxs-lookup"><span data-stu-id="488b0-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="488b0-138">(„FastTab” **Atsargos** naudojamas ir perkėlimo užsakymams, ir gamybos užsakymams.)</span><span class="sxs-lookup"><span data-stu-id="488b0-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="488b0-139">**Kartotinis** – suplanuoti užsakymai bus šio kiekio kartotinis.</span><span class="sxs-lookup"><span data-stu-id="488b0-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="488b0-140">Pavyzdžiui, jei nustatytas **Kartotinis** laukas nustatytas į *5*, užsakymo kiekis gali būti 5, 10, 15, 20 ir taip toliau.</span><span class="sxs-lookup"><span data-stu-id="488b0-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="488b0-141">**Min. užsakymo kiekis** – suplanuoti užsakymai nebus mažesni už nurodytą vertę.</span><span class="sxs-lookup"><span data-stu-id="488b0-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="488b0-142">Pavyzdžiui, jei **Min. užsakymo kiekio** laukas nustatytas į *10*, bus sukurtas suplanuotas užsakymas, kurio kiekis yra 10, net jeigu poreikiui patenkinti reikalingi tik keturi.</span><span class="sxs-lookup"><span data-stu-id="488b0-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="488b0-143">**Max. užsakymo kiekis** – suplanuoti užsakymai neviršys nurodytos vertės.</span><span class="sxs-lookup"><span data-stu-id="488b0-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="488b0-144">Jei poreikis yra didesnis nei **Max. užsakymo kiekio** vertė, jo padengimui bus sukurti keli suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="488b0-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="488b0-145">Pavyzdžiui, jei **Maks. užsakymo kiekio** laukas nustatytas į *100*, o poreikis yra 450, bus sukurti keturi suplanuoti užsakymai, kurių kiekis yra 100, ir vienas suplanuotas užsakymas, kurio kiekis yra 50.</span><span class="sxs-lookup"><span data-stu-id="488b0-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="488b0-146">Papildymo pavyzdžiai, kuriame naudojamas Min. / Maks.</span><span class="sxs-lookup"><span data-stu-id="488b0-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="488b0-147">padengimo kodas</span><span class="sxs-lookup"><span data-stu-id="488b0-147">coverage code</span></span>

<span data-ttu-id="488b0-148">Jei nenurodote reikšmės lauke **Kartotinis** produktui puslapyje **Numatytieji užsakymo parametrai** ir naudojate *Min. /Maks.*</span><span class="sxs-lookup"><span data-stu-id="488b0-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="488b0-149">papildymo metodą, Planavimo optimizavimas papildys atsargas iki konkretaus lygio, kai numatomas turimų atsargų lygis yra mažesnis nei konkreti ribinė vertė.</span><span class="sxs-lookup"><span data-stu-id="488b0-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="488b0-150">Jei nustatote kartotinį kiekį produktui, *Min. / Maks.*</span><span class="sxs-lookup"><span data-stu-id="488b0-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="488b0-151">papildymo metodas pakeičia jo elgseną ir atsižvelgia į **Kartotinio** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="488b0-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="488b0-152">Kitaip tariant, Planavimo optimizavimas vis tiek papildys atsargas iki nustatyto didžiausio lygio, kai numatytas turimų atsargų lygis bus mažesnis nei nustatytas minimalus lygis.</span><span class="sxs-lookup"><span data-stu-id="488b0-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="488b0-153">Tačiau papildymo kiekis turi būti **Kartotinio** reikšmės kartotinis.</span><span class="sxs-lookup"><span data-stu-id="488b0-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="488b0-154">Jei papildymo kiekis (skirtumas tarp didžiausio lygio ir numatyto turimo kiekio lygio) nėra nustatyto kiekio kartotinis, Planavimo optimizavimas naudoja pirmą galimą vertę, kuri kartu su numatytu turimo kiekio lygiu bus mažesnė už maksimalų lygį.</span><span class="sxs-lookup"><span data-stu-id="488b0-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="488b0-155">Jei suma mažesnė nei minimalus lygis, Planavimo optimizavimas naudoja pirmąją vertę, kuri kartu su numatyta turimo kiekio verte, bus didesnė už maksimalų lygį.</span><span class="sxs-lookup"><span data-stu-id="488b0-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="488b0-156">Toliau pateikti poskyriai pateikia keletą pavyzdžių, kurie parodo, kaip keli produkto užsakymo kiekiai veikia *Min. / Maks.*</span><span class="sxs-lookup"><span data-stu-id="488b0-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="488b0-157">papildymo metodo rezultatą.</span><span class="sxs-lookup"><span data-stu-id="488b0-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="488b0-158">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="488b0-158">Example 1</span></span>

<span data-ttu-id="488b0-159">Produktas turi šią konfigūraciją:</span><span class="sxs-lookup"><span data-stu-id="488b0-159">A product has the following configuration:</span></span>

- <span data-ttu-id="488b0-160">**Padengimo kodas:** *Min. / Max.*</span><span class="sxs-lookup"><span data-stu-id="488b0-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="488b0-161">**Mažiausia:** *15*</span><span class="sxs-lookup"><span data-stu-id="488b0-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="488b0-162">**Didžiausia:** *22*</span><span class="sxs-lookup"><span data-stu-id="488b0-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="488b0-163">**Keli:** *0*</span><span class="sxs-lookup"><span data-stu-id="488b0-163">**Multiple:** *0*</span></span>

<span data-ttu-id="488b0-164">Yra 10 produkto vienetų turimose atsargose ir nėra kito poreikio arba tiekimo.</span><span class="sxs-lookup"><span data-stu-id="488b0-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="488b0-165">Kai vykdomas bendrasis planavimas, sukuriamas 12 vienetų suplanuotas užsakymas, kad atsargos būtų papildytos iki didžiausio kiekio.</span><span class="sxs-lookup"><span data-stu-id="488b0-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="488b0-166">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="488b0-166">Example 2</span></span>

<span data-ttu-id="488b0-167">Produktas turi šią konfigūraciją:</span><span class="sxs-lookup"><span data-stu-id="488b0-167">A product has the following configuration:</span></span>

- <span data-ttu-id="488b0-168">**Padengimo kodas:** *Min. / Max.*</span><span class="sxs-lookup"><span data-stu-id="488b0-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="488b0-169">**Mažiausia:** *15*</span><span class="sxs-lookup"><span data-stu-id="488b0-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="488b0-170">**Didžiausia:** *22*</span><span class="sxs-lookup"><span data-stu-id="488b0-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="488b0-171">**Keli:** *5*</span><span class="sxs-lookup"><span data-stu-id="488b0-171">**Multiple:** *5*</span></span>

<span data-ttu-id="488b0-172">Yra 10 produkto vienetų turimose atsargose ir nėra kito poreikio arba tiekimo.</span><span class="sxs-lookup"><span data-stu-id="488b0-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="488b0-173">Kai vykdomas bendrasis planavimas, sukuriamas 10 vienetų suplanuotas užsakymas (kadangi 15 papildymo vienetų pridėjus 10 turimų atsargų vienetų viršys didžiausią kiekį).</span><span class="sxs-lookup"><span data-stu-id="488b0-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="488b0-174">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="488b0-174">Example 3</span></span>

<span data-ttu-id="488b0-175">Produktas turi šią konfigūraciją:</span><span class="sxs-lookup"><span data-stu-id="488b0-175">A product has the following configuration:</span></span>

- <span data-ttu-id="488b0-176">**Padengimo kodas:** *Min. / Max.*</span><span class="sxs-lookup"><span data-stu-id="488b0-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="488b0-177">**Mažiausia:** *21*</span><span class="sxs-lookup"><span data-stu-id="488b0-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="488b0-178">**Didžiausia:** *24*</span><span class="sxs-lookup"><span data-stu-id="488b0-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="488b0-179">**Keli:** *5*</span><span class="sxs-lookup"><span data-stu-id="488b0-179">**Multiple:** *5*</span></span>

<span data-ttu-id="488b0-180">Yra 10 produkto vienetų turimose atsargose ir nėra kito poreikio arba tiekimo.</span><span class="sxs-lookup"><span data-stu-id="488b0-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="488b0-181">Kai vykdomas bendrasis planavimas, sukuriamas 15 vienetų suplanuotas užsakymas (kadangi 10 papildymo vienetų pridėjus 10 turimų atsargų vienetų bus mažesnis nei mažiausias kiekis).</span><span class="sxs-lookup"><span data-stu-id="488b0-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
