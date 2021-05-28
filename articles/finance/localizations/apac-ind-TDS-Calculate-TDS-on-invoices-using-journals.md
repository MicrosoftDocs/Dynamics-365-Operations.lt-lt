---
title: Skaičiuoti SF TDS naudojant žurnalus
description: Šioje temoje pateikiami žurnalų iš šaltinio (TDS) išskaityamų mokesčių skaičiavimo veiksmai.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023462"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="f1f01-103">Skaičiuoti SF TDS naudojant žurnalus</span><span class="sxs-lookup"><span data-stu-id="f1f01-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1f01-104">Šioje temoje pateikiami žurnalų iš šaltinio (TDS) išskaityamų mokesčių skaičiavimo veiksmai.</span><span class="sxs-lookup"><span data-stu-id="f1f01-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="f1f01-105">Pradėkite veiksmą atidarydami **Bendrųjų žurnalų** puslapį (**Didžioji knyga > Žurnalo įrašai > Bendrieji žurnalai**).</span><span class="sxs-lookup"><span data-stu-id="f1f01-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="f1f01-106">[![Pagrindiniai žurnalai](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="f1f01-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="f1f01-107">Kurti žurnalo eilutes, naudojant lentelėje pateiktas žurnalo formas.</span><span class="sxs-lookup"><span data-stu-id="f1f01-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="f1f01-108">Pasirinkite sąskaitos tipą bei korespondentinės sąskaitos tipą ir įveskite operacijos sumą.</span><span class="sxs-lookup"><span data-stu-id="f1f01-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="f1f01-109">SF **patvirtinimo žurnalo puslapyje** pasirinkite **Rasti kvitus** ir pasirinkite sąskaitas faktūras, kurioms norite apskaičiuoti TDS.</span><span class="sxs-lookup"><span data-stu-id="f1f01-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="f1f01-110">Peržiūrėti SF registro puslapyje **sukurtas SF** arba **Rasti kvitų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1f01-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="f1f01-111">Skirtuke **Bendri** puslapyje **Žurnalo kvitas** peržiūrėkite ir keiskite numatytąją TDS grupę, nustatytą tiekėjui ar klientui **TDS grupės** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="f1f01-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="f1f01-112">Žurnalo eilutėse apskaičiuota TDS suma pagrįsta TDS mokesčių kodų, išvardytų **TDS grupės** lauke formule.</span><span class="sxs-lookup"><span data-stu-id="f1f01-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="f1f01-113">Laukelis **Išskaitimo mokesčio grupė**  ir **TCS grupės** laukelis tampa neprieinamas jums pasirinkus TDS grupę **TDS grupės** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="f1f01-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="f1f01-114">Laukelis **Išskaitomo mokesčio grupė** galimas tik **bendrojo žurnalo** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f1f01-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="f1f01-115">TDS skaičiuojamas tik jei **Skaičiuoti išskaitomą mokestį** žymimas laukelis yra pažymėtas tiekėjui ar klientui **Visi tiekėjai** ar **Visi klientai** puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="f1f01-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="f1f01-116">Pasirinkite **mokesčių informacijo** skirtuką. Jei reikia, pasirinkite alternatyvius įmonės, nustatytos įmonės adresus šiame lauke.</span><span class="sxs-lookup"><span data-stu-id="f1f01-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="f1f01-117">Įmonės pavadinimą galite peržiūrėti lauke **Pavadinimas**, kuris yra **įmonės informacijos** laukų grupėje.</span><span class="sxs-lookup"><span data-stu-id="f1f01-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="f1f01-118">Peržiūrėkite tiekėjo arba kliento vertinimo kategorijos pobūdį lauke Gavėjo tikslas, kuris priklauso **išskaitomo mokesčio** laukų **grupei**.</span><span class="sxs-lookup"><span data-stu-id="f1f01-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="f1f01-119">Laukelyje **Mokesčio sąskaitos numeris** (**TAN**) peržiūrėkite pasirinktos įmonės pavadinimo TAN, kuris rodomas.</span><span class="sxs-lookup"><span data-stu-id="f1f01-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="f1f01-120">Rinkitės **Išskaitomo mokesčio meniu** esantį **Išskaitomo mokesčio** meniu, kad atidarytumėte **laikino išskaitomo mokesčio operacijų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1f01-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="f1f01-121">Šie laukai rodomi viršutinėje laikino išskaitomo **mokesčio operacijų puslapio** srityje.</span><span class="sxs-lookup"><span data-stu-id="f1f01-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="f1f01-122">**Bendroji išskaitomo mokesčio suma** – bendroji TDS grupės operacijos TDS suma.</span><span class="sxs-lookup"><span data-stu-id="f1f01-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="f1f01-123">**Vertė** – bendrasis procentas, naudojamas operacijos TDS apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="f1f01-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="f1f01-124">Bendrasis procentas remiasi formule, kuri nustatyta TDS mokesčių kodams, pridėtiems prie TDS grupės.</span><span class="sxs-lookup"><span data-stu-id="f1f01-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="f1f01-125">**Pakoreguota išskaitomo mokesčio suma visa** – bendroji koreguota TDS suma, skirta visiems TDS grupės mokesčių kodams.</span><span class="sxs-lookup"><span data-stu-id="f1f01-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="f1f01-126">**TDS** – jei pasirinkta, prie operacijos pridedama TDS grupė.</span><span class="sxs-lookup"><span data-stu-id="f1f01-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="f1f01-127">Laukeliai **Peržiūra**, **Bendra**, ir **Koregavimas** laikinų išskaitomo **mokesčių operacijų puslapyje** rodo apskaičiuotą TDS sumą ir pakoreguotos TDS sumos informaciją kiekvienam TDS mokesčių kodui, pridėtame prie TDS grupės.</span><span class="sxs-lookup"><span data-stu-id="f1f01-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="f1f01-128">Pasirinkite **Ribinės vertės** lauką, kad atidarytumėte **slenkstį**.</span><span class="sxs-lookup"><span data-stu-id="f1f01-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="f1f01-129">Peržiūrėkite šiame puslapyje nurodytą TDS mokesčio komponento, pridėto prie konkretaus TDS mokesčio kodo, ribinės vertės ir išimties ribą.</span><span class="sxs-lookup"><span data-stu-id="f1f01-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="f1f01-130">Norėdami **atidaryti formulės** konstruktoriaus **formą, pasirinkite** Formulės konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="f1f01-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="f1f01-131">Peržiūrėkite šiame puslapyje nurodytą konkretaus TDS mokesčio kodo formulę.</span><span class="sxs-lookup"><span data-stu-id="f1f01-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="f1f01-132">Užverkite **Formulės konstruktorių** ir **Laikino išskaitomo mokesčio operacijų** puslapius, kad grįžtumėte į **Žurnalo kvito** puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1f01-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="f1f01-133">Įveskite kitą reikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="f1f01-133">Enter the other required details.</span></span> <span data-ttu-id="f1f01-134">Patikrinkite ir užregistruokite žurnalą.</span><span class="sxs-lookup"><span data-stu-id="f1f01-134">Validate and post the journal.</span></span> <span data-ttu-id="f1f01-135">TDS suma, apskaičiuota pirkimo SF, užregistruojama mokėtinoje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="f1f01-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="f1f01-136">TDS suma, apskaičiuota pardavimo SF, užregistruojama gautinų sumų sąskaitoje, kuri nustatoma kiekvienam TDS mokesčio kodui TDS grupėje.</span><span class="sxs-lookup"><span data-stu-id="f1f01-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="f1f01-137">TDS mokesčių kodų mokėtinos sumos arba gautinos sąskaitos nustatomos puslapyje **Išskaitomo mokesčio kodai**.</span><span class="sxs-lookup"><span data-stu-id="f1f01-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="f1f01-138">Rinkitės **Publikuotas išskaitomas mokestis** norėdami atverti **Išskaitomo** **mokesčio** **perlaidų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1f01-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="f1f01-139">Laukelyje **Vertė** – bendrasis procentas, naudojamas rodomos operacijos TDS apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="f1f01-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="f1f01-140">Laukeliai **Peržiūra**, **Bendra** ir **Suma** skirtukuose išskaitomo mokesčių operacijų puslapyje rodo apskaičiuotą TDS sumą ir pakoreguotos TDS sumos informaciją kiekvienam TDS mokesčių kodui, pridėtame prie TDS grupės.</span><span class="sxs-lookup"><span data-stu-id="f1f01-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
