---
title: Mokestis nesuskaičiuotas arba mokesčio suma lygi nuliui
description: Šioje temoje pateikiama trikčių diagnostikos informacija, kuri gali padėti, kai mokesčio suma lygi 0 (nuliui) arba mokestis nėra apskaičiuojamas.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ead979081692d4dcee9812c89f5f10c7879d3f7e
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947680"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="198c1-103">Mokestis nesuskaičiuotas arba mokesčio suma lygi nuliui</span><span class="sxs-lookup"><span data-stu-id="198c1-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="198c1-104">Operacijoje gali būti eilutės suma, kuri nėra 0 (nulis), bet mokestis nėra apskaičiuotas arba apskaičiuota mokesčio suma yra 0.</span><span class="sxs-lookup"><span data-stu-id="198c1-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="198c1-105">Norėdami išspręsti šią problemą, atlikite tolesniuose skyriuose nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="198c1-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="198c1-106">Patikrinti, ar operacijos teisingai parinkti mokesčių kodai</span><span class="sxs-lookup"><span data-stu-id="198c1-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="198c1-107">Jei operacija nepasirinko teisingų mokesčių kodų arba nepasirinko jokių mokesčių kodų, pagal juos mokesčiai nebus skaičiuojami.</span><span class="sxs-lookup"><span data-stu-id="198c1-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="198c1-108">Imkitės šių veiksmų, kad patikrintumėte, ar operacijos teisingai parinkti mokesčių kodai.</span><span class="sxs-lookup"><span data-stu-id="198c1-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="198c1-109">Operacijos eilutės eilutės informacijos "FastTab" skirtuke Nustatymas, **PVM** **skyriuje** **patikrinkite**, **ar** **laukuose** Prekės PVM grupė ir PVM grupė pasirinktos tinkamos mokesčių grupės.</span><span class="sxs-lookup"><span data-stu-id="198c1-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="198c1-110">Jei tinkamos mokesčių grupės nepasirinktos, pasirinkite jas.</span><span class="sxs-lookup"><span data-stu-id="198c1-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="198c1-111">[![Prekės pardavimo mokesčio grupė ir pardavimo mokesčio grupės laukeliai](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="198c1-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="198c1-112">Eikite į **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **PVM grupės**.</span><span class="sxs-lookup"><span data-stu-id="198c1-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="198c1-113">Pasirinkite atitinkamą PVM grupę, tada sąrankos **„FastTab" atlikite pastabą apie PVM** **kodą lauke PVM** kodas.</span><span class="sxs-lookup"><span data-stu-id="198c1-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="198c1-114">[![PVM grupių puslapis](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="198c1-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="198c1-115">Eikite į **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **Prekės PVM grupės**.</span><span class="sxs-lookup"><span data-stu-id="198c1-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="198c1-116">Pasirinkite atitinkamą prekės PVM grupę, tada nustatymo **„FastTab" patikrinkite, ar PVM kodo lauke esantis mokesčio kodas atitinka PVM** **grupės mokesčio** kodą.</span><span class="sxs-lookup"><span data-stu-id="198c1-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="198c1-117">[![Prekės pardavimo mokesčių grupių puslapis](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="198c1-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="198c1-118">Jei mokesčių kodai nesutampa, atnaujinkite vienos iš grupių PVM kodą.</span><span class="sxs-lookup"><span data-stu-id="198c1-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="198c1-119">Patikrinti, ar pasirinkti mokesčių kodai nėra neapmokestinami ir ar jie turi teisingą mokesčio tarifo vertę</span><span class="sxs-lookup"><span data-stu-id="198c1-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="198c1-120">Jei mokesčio kodai yra neapmokestinami arba jei mokesčio tarifas yra 0 (nulis), mokesčio skaičiavimo rezultatas bus 0.</span><span class="sxs-lookup"><span data-stu-id="198c1-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="198c1-121">Norėdami nustatyti, ar pasirinkti mokesčių kodai yra neapmokestinami, ir patikrinti, ar jiems taikomas teisingas mokesčio tarifas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="198c1-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="198c1-122">Eikite į **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **PVM grupės**.</span><span class="sxs-lookup"><span data-stu-id="198c1-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="198c1-123">Pasirinkite atitinkamą PVM grupę, tada **nustatymo** „FastTab" patikrinkite, ar **išvalytas** žymės langelis Atleista.</span><span class="sxs-lookup"><span data-stu-id="198c1-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="198c1-124">Jei jis pažymėtas, išvalykite.</span><span class="sxs-lookup"><span data-stu-id="198c1-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="198c1-125">[![PVM grupių puslapio žymės langelis Atleidžiamas nuo mokesčių](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="198c1-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="198c1-126">Nueikite į **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **PVM kodai**.</span><span class="sxs-lookup"><span data-stu-id="198c1-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="198c1-127">Pasirinkite tinkamą PVM kodą, tada patikrinkite, ar mokesčio tarifo vertė **vertės lauke** nėra 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="198c1-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="198c1-128">Jei tai 0, atnaujinkite lauką, kad jis būtų nustatytas pagal teisingą mokesčio tarifą.</span><span class="sxs-lookup"><span data-stu-id="198c1-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="198c1-129">[![Vertės laukelis PVM kodų reikšmių puslapis](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="198c1-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="198c1-130">Nustatyti, ar nulis yra teisinga mokesčio suma</span><span class="sxs-lookup"><span data-stu-id="198c1-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="198c1-131">Kai kuriuose scenarijuose 0 (nulis) esanti mokesčių suma yra teisinga.</span><span class="sxs-lookup"><span data-stu-id="198c1-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="198c1-132">Norėdami nustatyti, ar 0 yra teisinga operacijos mokesčių suma, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="198c1-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="198c1-133">Eikite į **Didžioji knyga** \> **Didžiosios knygos nustatymas** \> **DK parametrai**.</span><span class="sxs-lookup"><span data-stu-id="198c1-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="198c1-134">Skirtuko **PVM** lauke Skaičiavimo būdas **patikrinkite**, ar **pasirinkta Bendroji** suma.</span><span class="sxs-lookup"><span data-stu-id="198c1-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="198c1-135">[![Skaičiavimo metodo laukelis Didžiosios knygos parametrų puslapyje](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="198c1-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="198c1-136">Nueikite į **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **PVM kodai**.</span><span class="sxs-lookup"><span data-stu-id="198c1-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="198c1-137">Pasirinkite atitinkamą PVM kodą, rinkitės **Skaičiavimas** \> **Maržos bazė** ir patikrinkite, ar maržos bazė yra nustatyta į **Grynoji sąskaitos balanso suma** ar **Bendra sąskaitos suma įskaičiuoja kitas mokesčių sumas**.</span><span class="sxs-lookup"><span data-stu-id="198c1-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="198c1-138">Daugiau informacijos rasite SF [sumą, įskaitant kitas PVM sumas](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span><span class="sxs-lookup"><span data-stu-id="198c1-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="198c1-139">Jei 2 ir 4 veiksmais nustatytos teisingos vertės, nustatykite, ar bendra operacijos suma yra 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="198c1-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="198c1-140">Jei bendroji suma yra 0, numatomas rezultatas yra 0 mokesčių suma.</span><span class="sxs-lookup"><span data-stu-id="198c1-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="198c1-141">Kadangi mokesčio skaičiavimas pagrįstas bendra SF balanso suma ir ši suma nėra eilutė pagal eilutę, mokesčio suma 0 bus priskirta kiekvienai eilutei po mokesčio skaičiavimo.</span><span class="sxs-lookup"><span data-stu-id="198c1-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="198c1-142">Nustatyti, ar yra tinkinimas</span><span class="sxs-lookup"><span data-stu-id="198c1-142">Determine whether customization exists</span></span>

<span data-ttu-id="198c1-143">Jei atlikote veiksmus ankstesniuose skyriuose, bet neradote problemos, nustatykite, ar yra tinkinimas.</span><span class="sxs-lookup"><span data-stu-id="198c1-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="198c1-144">Jei tinkinimo nėra, sukurkite „Microsoft" aptarnavimo užklausą, kad ji būtų tolimesnė.</span><span class="sxs-lookup"><span data-stu-id="198c1-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
