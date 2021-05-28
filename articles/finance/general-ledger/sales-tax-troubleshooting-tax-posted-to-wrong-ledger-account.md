---
title: Mokestis registruojamas neteisingame DK sąskaitoje kvite
description: Šioje temoje pateikiama trikčių diagnostikos informacija, kuri gali padėti, kai mokesčiai registruojami į netinkamą DK sąskaitą kvite.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020096"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="e1da6-103">Mokestis registruojamas neteisingame DK sąskaitoje kvite</span><span class="sxs-lookup"><span data-stu-id="e1da6-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1da6-104">Publikavimo metu, mokesčiai gali būti publikuoti į ne tą DK paskyrą kvite.</span><span class="sxs-lookup"><span data-stu-id="e1da6-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="e1da6-105">Norėdami išspręsti šią problemą, atlikite tolesniuose skyriuose nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e1da6-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="e1da6-106">Šios temos pavyzdžiuose kaip verslo dokumentą naudojamas pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="e1da6-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="e1da6-107">Rasti neteisingai užregistruotos mokesčio operacijos mokesčio kodą</span><span class="sxs-lookup"><span data-stu-id="e1da6-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="e1da6-108">Kvito **operacijų puslapyje pasirinkite** operaciją, su kuria norite dirbti, tada pasirinkite **Užregistruotas** PVM.</span><span class="sxs-lookup"><span data-stu-id="e1da6-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="e1da6-109">[![Užregistruotas PVM mygtukas kvito operacijų puslapyje](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="e1da6-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="e1da6-110">Lauke **PVM kodas** peržiūrėkite vertę.</span><span class="sxs-lookup"><span data-stu-id="e1da6-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="e1da6-111">Šiame pavyzdyje tai **19** PVM.</span><span class="sxs-lookup"><span data-stu-id="e1da6-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="e1da6-112">[![PVM kodo laukas užregistruoto PVM puslapyje](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="e1da6-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="e1da6-113">Patikrinti mokesčio kodo DK registravimo grupę</span><span class="sxs-lookup"><span data-stu-id="e1da6-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="e1da6-114">Nueikite į **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **PVM kodai**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="e1da6-115">Raskite ir pasirinkite mokesčio kodą, tada peržiūrėkite vertę lauke **DK registravimo** grupė.</span><span class="sxs-lookup"><span data-stu-id="e1da6-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="e1da6-116">Šiame pavyzdyje tai **PVM**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="e1da6-117">[![DK publikavimo grupės laukelis PVM kodo puslapyje](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="e1da6-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="e1da6-118">Lauke **DK registravimo grupė** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="e1da6-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="e1da6-119">Norėdami peržiūrėti išsamią grupės konfigūracijos informaciją, pasirinkite saitą.</span><span class="sxs-lookup"><span data-stu-id="e1da6-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="e1da6-120">Arba pasirinkite ir laikykite (arba spustelėkite dešiniuoju pelės mygtuku) lauke ir pasirinkite **Peržiūrėti** informaciją.</span><span class="sxs-lookup"><span data-stu-id="e1da6-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="e1da6-121">[![Papildomos informacijos komandos peržiūra](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="e1da6-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="e1da6-122">Mokėtino **PVM** lauke, atsižvelgiant į operacijos tipą, patikrinkite, ar sąskaitos numeris teisingas.</span><span class="sxs-lookup"><span data-stu-id="e1da6-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="e1da6-123">Jei jos nėra, pasirinkite tinkamą sąskaitą, į ją įregistruokite.</span><span class="sxs-lookup"><span data-stu-id="e1da6-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="e1da6-124">Šiame pavyzdyje pardavimo užsakymo PVM turi būti registruojamas mokėtino PVM sąskaitoje, 222200.</span><span class="sxs-lookup"><span data-stu-id="e1da6-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="e1da6-125">[![Mokėtino PVM laukas DK registravimo grupių puslapyje](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="e1da6-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="e1da6-126">Toliau esančioje lentelėje pateikiama informacija apie kiekvieną DK registravimo **grupių puslapio** lauką.</span><span class="sxs-lookup"><span data-stu-id="e1da6-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="e1da6-127">Laukas</span><span class="sxs-lookup"><span data-stu-id="e1da6-127">Field</span></span>                  | <span data-ttu-id="e1da6-128">Aprašas</span><span class="sxs-lookup"><span data-stu-id="e1da6-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="e1da6-129">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="e1da6-129">Sales tax payable</span></span>      | <span data-ttu-id="e1da6-130">Pagrindinė sąskaita išeinančiam PVM, kuris mokamas mokesčių įstaigai.</span><span class="sxs-lookup"><span data-stu-id="e1da6-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="e1da6-131">Gautinas PVM</span><span class="sxs-lookup"><span data-stu-id="e1da6-131">Sales tax receivable</span></span>   | <span data-ttu-id="e1da6-132">Pagrindinė sąskaita ateinantiems mokesčiams, kurie gaunami iš mokesčių įstaigos.</span><span class="sxs-lookup"><span data-stu-id="e1da6-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="e1da6-133">Naudojimo mokesčio išlaidos</span><span class="sxs-lookup"><span data-stu-id="e1da6-133">Use tax expense</span></span>        | <span data-ttu-id="e1da6-134">Pagrindinė sąskaita, naudojama atskaitomais naudojimo mokesčiais, kurių tiekėjai nepaiso mokesčių inspekcijos kaip Europos Sąjungos (ES) atvirkštinio apmokestinimo prekių ir paslaugų mokesčio (GST) / suderintos PVM (HST) dalimi.</span><span class="sxs-lookup"><span data-stu-id="e1da6-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="e1da6-135">**Naudoti mokestį** turi būti pažymėtas PVM kodas PVM mokesčio grupėje, naudojamoje operacijoje.</span><span class="sxs-lookup"><span data-stu-id="e1da6-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="e1da6-136">Šis laukas nepasiekiamas, jei puslapyje **Didžiosios knygos parametrai** pažymėta parinktis **Taikyti PVM apmokestinimo taisykles**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="e1da6-137">Mokėtinas naudojimo mokestis</span><span class="sxs-lookup"><span data-stu-id="e1da6-137">Use tax payable</span></span>        | <span data-ttu-id="e1da6-138">Pagrindinė sąskaita, naudojama gaunamiems naudojimo mokesčiams, mokėtinams mokesčių inspekcijai, registruoti.</span><span class="sxs-lookup"><span data-stu-id="e1da6-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="e1da6-139">Sudengimo sąskaita</span><span class="sxs-lookup"><span data-stu-id="e1da6-139">Settlement account</span></span>     | <span data-ttu-id="e1da6-140">Pagrindinė publikuoti grynąjį DK balansą naudojama sąskaita yra nurodyta **Naudoti PVM** ir **Gautinas PVM** laukelius.</span><span class="sxs-lookup"><span data-stu-id="e1da6-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="e1da6-141">Tiekėjo mokėjimo nuolaida</span><span class="sxs-lookup"><span data-stu-id="e1da6-141">Vendor cash discount</span></span>   | <span data-ttu-id="e1da6-142">Pagrindinė sąskaita naudojama publikuoti grynųjų nuolaidą PVM kodui, susietam su šios DK publikavimo grupe.</span><span class="sxs-lookup"><span data-stu-id="e1da6-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="e1da6-143">Kliento atvejo nuolaida</span><span class="sxs-lookup"><span data-stu-id="e1da6-143">Customer case discount</span></span> | <span data-ttu-id="e1da6-144">Pagrindinė sąskaita naudojama publikuoti grynųjų nuolaidą PVM kodui, susietam su šios DK publikavimo grupe.</span><span class="sxs-lookup"><span data-stu-id="e1da6-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="e1da6-145">Daugiau informacijos žr. [Didžiosios knygos registravimo grupių nustatymas pardavimo mokesčiui](tasks/set-up-ledger-posting-groups-sales-tax.md)</span><span class="sxs-lookup"><span data-stu-id="e1da6-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="e1da6-146">Suderinti kodą, norint patikrinti DK dimensijas</span><span class="sxs-lookup"><span data-stu-id="e1da6-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="e1da6-147">Kode registravimo sąskaitą nustato DK dimensija.</span><span class="sxs-lookup"><span data-stu-id="e1da6-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="e1da6-148">DK dimensija įrašo sąskaitos ID duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="e1da6-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="e1da6-149">Pardavimo užsakymui pridėkite stabdos tašką mokesčių **saveAndPost::()** ir **Tax ::post()** metoduose.</span><span class="sxs-lookup"><span data-stu-id="e1da6-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="e1da6-150">Skirti dėmesį į **\_ledgerDimension** vertę.</span><span class="sxs-lookup"><span data-stu-id="e1da6-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="e1da6-151">[![Pardavimo užsakymo kodo pavyzdys, kuriame yra stabdos taškas](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="e1da6-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="e1da6-152">Pirkimo užsakymui, įtraukite stabdos tašką **TaxPost::saveAndPost()** ir **TaxPost::postToTaxTrans()** metodus.</span><span class="sxs-lookup"><span data-stu-id="e1da6-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="e1da6-153">Skirti dėmesį į **\_ledgerDimension** vertę.</span><span class="sxs-lookup"><span data-stu-id="e1da6-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="e1da6-154">[![Pirkimo užsakymo kodo pavyzdys, kuriame yra stabdos taškas](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="e1da6-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="e1da6-155">Vykdykite šią SQL užklausą, kad duomenų bazėje surasti rodomą sąskaitos vertę, pagrįstą įrašo ID, kuris įrašytas DK dimensijos.</span><span class="sxs-lookup"><span data-stu-id="e1da6-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="e1da6-156">[![Rodyti įrašo ID vertę](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="e1da6-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="e1da6-157">Išnagrinėkite užduoties reikšmę, kad **_ledgerDimension** kur priskirta ši vertė.</span><span class="sxs-lookup"><span data-stu-id="e1da6-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="e1da6-158">Paprastai vertė yra iš **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="e1da6-159">Tokiu atveju turėtumėte įtraukti stabdos tašką **TmpTaxWorkTrans::insert()** ir **TmpTaxWorkTrans::update()** kad rastumėte, kur priskirta vertė.</span><span class="sxs-lookup"><span data-stu-id="e1da6-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="e1da6-160">Nustatyti, ar yra tinkinimas</span><span class="sxs-lookup"><span data-stu-id="e1da6-160">Determine whether customization exists</span></span>

<span data-ttu-id="e1da6-161">Jei atlikote veiksmus ankstesniuose skyriuose, bet neradote problemos, nustatykite, ar yra tinkinimas.</span><span class="sxs-lookup"><span data-stu-id="e1da6-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="e1da6-162">Jei tinkinimo nėra, sukurkite „Microsoft" aptarnavimo užklausą, kad ji būtų tolimesnė.</span><span class="sxs-lookup"><span data-stu-id="e1da6-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
