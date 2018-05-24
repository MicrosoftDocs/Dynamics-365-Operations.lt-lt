---
title: "PVM skaičiavimo metodas lauke Kilmė"
description: "Šiame straipsnyje paaiškinamos PVM kodų puslapio lauko Kilmė parinktys ir tai, kaip PVM skaičiuojamas pagal pasirinktą PVM kodo parinktį."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1473eeb2950296f5ae6250d7a53794af3d9cba81
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="4f151-103">PVM skaičiavimo metodas lauke Kilmė</span><span class="sxs-lookup"><span data-stu-id="4f151-103">Sales tax calculation methods in the Origin field</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="4f151-104">Šiame straipsnyje paaiškinamos PVM kodų puslapio lauko Kilmė parinktys ir tai, kaip PVM skaičiuojamas pagal pasirinktą PVM kodo parinktį.</span><span class="sxs-lookup"><span data-stu-id="4f151-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="4f151-105">Turite pasirinkti kiekvieno puslapyje PVM kodai sukurto PVM kodo skaičiavimo metodą, taikomą mokesčio bazinei sumai lauke Kilmė.</span><span class="sxs-lookup"><span data-stu-id="4f151-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="4f151-106">Grynosios sumos procentai</span><span class="sxs-lookup"><span data-stu-id="4f151-106">Percentage of net amount</span></span>
<span data-ttu-id="4f151-107">Grynosios sumos procento skaičiavimo metodas yra numatytoji vertė lauke Kilmė.</span><span class="sxs-lookup"><span data-stu-id="4f151-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="4f151-108">PVM skaičiuojamas kaip pirkimo ar pardavimo sumos procentas, neįtraukiant visų kitų PVM.</span><span class="sxs-lookup"><span data-stu-id="4f151-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="4f151-109">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4f151-109">Example</span></span>

<span data-ttu-id="4f151-110">Mokesčio tarifas yra 25%.</span><span class="sxs-lookup"><span data-stu-id="4f151-110">The tax rate is 25%.</span></span> <span data-ttu-id="4f151-111">SF eilutėje rodoma 10 prekių, kiekvienos kaina 1,00, o klientui suteikiama 10 % eilutės nuolaida.</span><span class="sxs-lookup"><span data-stu-id="4f151-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="4f151-112">Grynoji suma: (10 x 1,00) – 10 % = 9,00 PVM: 9,00 x 25 % = 2,25 Bendroji suma: 9,00 + 2,25 = 11,25</span><span class="sxs-lookup"><span data-stu-id="4f151-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="4f151-113"> Procentas nuo bendros sumos</span><span class="sxs-lookup"><span data-stu-id="4f151-113">Percentage of gross amount</span></span>
<span data-ttu-id="4f151-114">Pasirinkus bendros sumos procento skaičiavimo metodą, PVM apskaičiuojamas kaip bendros pardavimo sumos procentas.</span><span class="sxs-lookup"><span data-stu-id="4f151-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="4f151-115">Bendra suma yra grynoji eilutės suma, pridėjus visus eilutei taikomus mokesčius, išskyrus lauke Kilmė nurodytą mokestį = bendros sumos procentas.</span><span class="sxs-lookup"><span data-stu-id="4f151-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="4f151-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4f151-116">Example</span></span>

<span data-ttu-id="4f151-117">Mokesčių institucija taiko prekei specialius muito mokesčius.</span><span class="sxs-lookup"><span data-stu-id="4f151-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="4f151-118">Muito mokesčio sumos pridedamos prie grynosios sumos prieš PVM skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="4f151-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="4f151-119">Duoti šie PVM kodai:</span><span class="sxs-lookup"><span data-stu-id="4f151-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="4f151-120">1 MUITO MOKESTIS = 10 %, taikant grynosios sumos procento skaičiavimo metodą</span><span class="sxs-lookup"><span data-stu-id="4f151-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="4f151-121">2 MUITO MOKESTIS = 20 %, taikant grynosios sumos procento skaičiavimo metodą</span><span class="sxs-lookup"><span data-stu-id="4f151-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="4f151-122">PVM = 25 %, taikant bendros sumos procento skaičiavimo metodą</span><span class="sxs-lookup"><span data-stu-id="4f151-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="4f151-123">Jei grynoji suma yra 10,00, tada 1 MUITO MOKESTIS yra 1,00 (10,00 x 10 %) o 2 MUITO MOKESTIS = 2,00 (10,00 x 20 %)</span><span class="sxs-lookup"><span data-stu-id="4f151-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="4f151-124">Sumos turi būti tokios: bendra suma: grynoji suma + 1 MUITO MOKESČIO suma + 2 MUITO MOKESČIO suma (10,00 + 1,00 + 2,00) = 13,00 PVM = 13,00 x 25 % = 3,25 bendroji MUITO MOKESČIŲ ir PVM suma: 1,00 + 2,00 + 3,25 = 6,25 bendroji suma: 10,00 + 6,25 = 16,25</span><span class="sxs-lookup"><span data-stu-id="4f151-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="4f151-125">**Pastaba.**</span><span class="sxs-lookup"><span data-stu-id="4f151-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f151-126">Vienai operacijai gali būti naudojamas tik vienas mokesčio kodas su kilme = bendros sumos procentas.</span><span class="sxs-lookup"><span data-stu-id="4f151-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="4f151-127">Jei operacijai naudojamas daugiau nei vienas toks mokesčio kodas, bus rodomas klaidos pranešimas, informuojantis, kad negalima apskaičiuoti PVM.</span><span class="sxs-lookup"><span data-stu-id="4f151-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="4f151-128">PVM procentas</span><span class="sxs-lookup"><span data-stu-id="4f151-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="4f151-129">Kai lauke Kilmė pasirenkate PVM procentą, PVM yra apskaičiuojamas kaip PVM lauke, dalyje PVM, pasirinkto PVM procentas.</span><span class="sxs-lookup"><span data-stu-id="4f151-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="4f151-130">Pirmiausia yra apskaičiuojamas PVM, pasirinktas PVM lauke, dalyje PVM.</span><span class="sxs-lookup"><span data-stu-id="4f151-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="4f151-131">Tada skaičiuojamas antras PVM pagal pirmą PVM sumą.</span><span class="sxs-lookup"><span data-stu-id="4f151-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="4f151-132">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4f151-132">Example</span></span>

<span data-ttu-id="4f151-133">Duoti šie PVM kodai:</span><span class="sxs-lookup"><span data-stu-id="4f151-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="4f151-134">1 MUITO MOKESTIS = 10 %, taikant grynosios sumos procento metodą</span><span class="sxs-lookup"><span data-stu-id="4f151-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="4f151-135">2 MUITO MOKESTIS = 20 %, taikant PVM procento metodą, kai PVM dalyje, PVM lauke pasirinktas 1 muito mokestis</span><span class="sxs-lookup"><span data-stu-id="4f151-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="4f151-136">PVM = 25 %, taikant bendros sumos procento metodą</span><span class="sxs-lookup"><span data-stu-id="4f151-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="4f151-137">Grynoji suma: 10,00 1 MUITO MOKESTIS: 10,00 x 10 % = 1,00 2 MUITO MOKESTIS: 1,00 x 20 % = 0,20 Bendra suma: 10,00 + 1,00 + 0,20 = 11,20 PVM: 11,20 x 25 % = 2,80 Visa MUITO MOKESČIŲ ir PVM suma: 1,00 + 0,20 + 2,80 = 4,00 Visa suma: 10,00 + 4,00 = 14,00</span><span class="sxs-lookup"><span data-stu-id="4f151-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="4f151-138">**Pastaba.**</span><span class="sxs-lookup"><span data-stu-id="4f151-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f151-139">Mokesčių skaičiavimai neapima kelių lygių mokesčių apskaičiavimo galimybės.</span><span class="sxs-lookup"><span data-stu-id="4f151-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="4f151-140">Mokestis negali būti apskaičiuojamas pagal mokestį, kuris buvo apskaičiuotas remiantis kitu mokesčiu.</span><span class="sxs-lookup"><span data-stu-id="4f151-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="4f151-141">Gali būti apskaičiuoti keli vieno lygio tam tikros operacijos mokesčiai remiantis mokesčių kodais.</span><span class="sxs-lookup"><span data-stu-id="4f151-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="4f151-142"> Suma pagal vienetą</span><span class="sxs-lookup"><span data-stu-id="4f151-142">Amount per unit</span></span>
<span data-ttu-id="4f151-143">Pasirinkus lauke Kilmė sumą už vienetą, PVM yra apskaičiuojamas kaip fiksuota suma už vienetą, padauginta iš dokumento eilutėje nurodyto kiekio.</span><span class="sxs-lookup"><span data-stu-id="4f151-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="4f151-144">Vienetas turi būti pasirinktas lauke Vienetas.</span><span class="sxs-lookup"><span data-stu-id="4f151-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="4f151-145">Suma už vienetą nurodyta puslapyje PVM kodų vertės.</span><span class="sxs-lookup"><span data-stu-id="4f151-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="4f151-146">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4f151-146">Example</span></span>

<span data-ttu-id="4f151-147">PVM kodas nustatomas kaip: 1,20 JAV dol. už vienetą = langelį Pardavimo SF eilutėje parduoti 25 langeliai PVM apskaičiuojamas kaip 25 x 1,20 = 30,00</span><span class="sxs-lookup"><span data-stu-id="4f151-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="4f151-148">**Pastaba.**</span><span class="sxs-lookup"><span data-stu-id="4f151-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f151-149">Jei įvedant operaciją naudojami kitokie, nei PVM kodų dalyje nurodyti vienetai, jie automatiškai konvertuojami remiantis vienetų konvertavimo vertėmis, nustatytomis puslapyje Vienetų konvertavimas.</span><span class="sxs-lookup"><span data-stu-id="4f151-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="4f151-150"> Suma už vienetą (papildoma parinktis)</span><span class="sxs-lookup"><span data-stu-id="4f151-150">Amount per unit, additional option</span></span>

<span data-ttu-id="4f151-151">Skirtuke Skaičiavimas galite pasirinkti, ar sumos už vienetą mokestis bus apskaičiuojamas pirmiau, nei kiti mokesčių kodai, ir pridedamas prie grynosios sumos pirmiau, nei apskaičiuojami kiti mokesčių kodai su kilme = grynosios sumos procentu.</span><span class="sxs-lookup"><span data-stu-id="4f151-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="4f151-152">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="4f151-152">Examples</span></span>

<span data-ttu-id="4f151-153">Tarkime, turime apskaičiuoti 2 operacijos mokesčių kodus:</span><span class="sxs-lookup"><span data-stu-id="4f151-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="4f151-154">MUITO MOKESTIS: kilmė = suma už vienetą ir PVM, vertė nustatyta kaip 5,00 už vienetą = vnt.</span><span class="sxs-lookup"><span data-stu-id="4f151-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="4f151-155">SALESTAX: kilmė = kaip parodyta toliau pateikiamuose pavyzdžiuose, nustatyta vertė 25 %</span><span class="sxs-lookup"><span data-stu-id="4f151-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="4f151-156">Parduoti 1 prekės vienetą už 10,00</span><span class="sxs-lookup"><span data-stu-id="4f151-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="4f151-157">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4f151-157">Example 1</span></span>

<span data-ttu-id="4f151-158">SALESTAX: kilmė = bendrosios sumos procento metodas Parinktis Skaičiuoti prieš PVM neturi įtakos, nes PVM yra skaičiuojamas kaip bendros sumos procentas.</span><span class="sxs-lookup"><span data-stu-id="4f151-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="4f151-159">MUITO MOKESTIS: 1 x 5,00 = 5,00 Bendra suma: 10,00 + 5,00 = 15,00 PVM: 15,00 x 25 % = 3,75 Visa PVM suma: 5,00 + 3,75 = 8,75 Visa suma: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="4f151-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="4f151-160">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4f151-160">Example 2</span></span>

<span data-ttu-id="4f151-161">PVM: kilmė = grynosios sumos procentas Parinktis Skaičiuoti prieš PVM nepasirinkta MUITO MOKESČIUI skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="4f151-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="4f151-162">Grynoji suma: 10,00 MUITO MOKESTIS: 1 x 5,00 = 5,00 PVM: 10,00 x 25 % = 2,50 Visa PVM suma: 5,00 + 2,50 = 7,50 Visa suma: 10,00 + 7,50 = 17,50</span><span class="sxs-lookup"><span data-stu-id="4f151-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="4f151-163">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4f151-163">Example 3</span></span>

<span data-ttu-id="4f151-164">PVM: kilmė = grynosios sumos procentas Parinktis Skaičiuoti prieš PVM pasirinkta MUITO MOKESČIUI skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="4f151-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="4f151-165">Grynoji suma: 10,00 MUITO MOKESTIS: 1 x 5,00 = 5,00 PVM: (10,00 + 5,00) x 25 % = 3,75 Visa PVM suma: 5,00 + 3,75 = 8,75 Visa suma: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="4f151-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="4f151-166">4 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4f151-166">Example 4</span></span>

<span data-ttu-id="4f151-167">3 ir 1 pavyzdžio rezultatas yra toks pat, nes yra tik vienas muito mokestis.</span><span class="sxs-lookup"><span data-stu-id="4f151-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="4f151-168">Tarkime, kad turite du muito mokesčius ir tik vienas iš jų įtrauktas į grynoji suma, PVM skaičiavimas: muito mokestį 1: 5,00, naudojant vieneto metodą sumą ir toliau skaičiuoti prieš PVM pasirinktis yra pažymėtas muito 2: 2,50, naudojant vieneto metodą sumą ir toliau skaičiuoti prieš PVM pasirinktis nėra pasirinkto PVM : 25 %, naudojant grynoji suma metodas grynosios sumos procentai: 10,00 muito mokestį 1: 1 x 5,00 = 5,00 muito 2: 1 x 2,50 = 2,50 grynosios sumos, kurioms taikomas PVM: 10,00 + 5,00 = 15,00 SALESTAX: 15,00 x 25 % = 3,75 bendroji PVM, įskaitant mokesčius: 5,00 + 2,50 + 3,75 = 11,25 bendroji suma: 10,00 + 11,25 = 21,25 sumų grynoji suma (10,00) + 1 (5,00) muito mokestis skaičiuojamas SALESTAX 25 % = 15,00.</span><span class="sxs-lookup"><span data-stu-id="4f151-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="4f151-169">2 MUITO MOKESTIS pridedamas prie PVM sumos, kai PVM apskaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="4f151-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="4f151-170"> Apskaičiuotas grynosios sumos procentas</span><span class="sxs-lookup"><span data-stu-id="4f151-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="4f151-171">Apskaičiuojant grynosios sumos procentą mokesčių apskaičiavimas priklauso nuo dokumento ar žurnalo parametro Sumos, įskaitant PVM.</span><span class="sxs-lookup"><span data-stu-id="4f151-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="4f151-172">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4f151-172">Example 1</span></span>

<span data-ttu-id="4f151-173">Dokumento / žurnalo parametras Sumos, įskaitant PVM = Taip Operacijos eilutės suma: 10,00 Mokesčio tarifas: 25 % PVM: operacijos eilutės suma x mokesčio tarifas (10,00 x 25 %) = 2,50 Mokesčio bazinė suma (kilmės suma): operacijos eilutės suma – PVM (10,00 – 2,50) = 7,50</span><span class="sxs-lookup"><span data-stu-id="4f151-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="4f151-174">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4f151-174">Example 2</span></span>

<span data-ttu-id="4f151-175">Dokumento / žurnalo parametras Sumos, įskaitant PVM = Ne Operacijos eilutės suma: 10,00 Mokesčio tarifas: 25 % PVM: (operacijos eilutės suma x mokesčio tarifas) / (100 – mokesčio tarifas) (10,00 x 25 %) / (100 % – 25 %) = 3,33 Mokesčio bazinė suma (kilmės suma): operacijos eilutės suma = 10,00</span><span class="sxs-lookup"><span data-stu-id="4f151-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="additional-resources"></a><span data-ttu-id="4f151-176">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="4f151-176">Additional resources</span></span>
--------

[<span data-ttu-id="4f151-177">PVM tarifų nustatymas pagal Bazinės ribos ir Skaičiavimo metodo laukus</span><span class="sxs-lookup"><span data-stu-id="4f151-177">Determining sale tax rates based on the Marginal base and Calculation method fields</span></span>](marginal-base-field.md)

[<span data-ttu-id="4f151-178">Visa suma ir PVM kodų intervalo skaičiavimo parinktys</span><span class="sxs-lookup"><span data-stu-id="4f151-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)




