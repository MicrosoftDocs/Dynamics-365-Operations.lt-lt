---
title: Klientų užsakymai naudojant „Modern POS“ (MPOS)
description: Šioje temoje pateikiama informacija apie klientų užsakymus naudojant „Modern POS“ (MPOS). Kliento užsakymai dar vadinami specialiais užsakymais. Šioje temoje pateikta susijusių parametrų ir operacijų srautų apžvalga.
author: josaw1
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a6fdc7b8d7ad65c9e4bf1d3b932b62918dea6e77
ms.sourcegitcommit: 7061a93f9f2b54aec4bc4bf0cc92691e86d383a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/20/2020
ms.locfileid: "3710264"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="ada81-105">Klientų užsakymai naudojant „Modern POS“ (MPOS)</span><span class="sxs-lookup"><span data-stu-id="ada81-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ada81-106">Šioje temoje pateikiama informacija apie klientų užsakymus naudojant „Modern POS“ (MPOS).</span><span class="sxs-lookup"><span data-stu-id="ada81-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="ada81-107">Kliento užsakymai dar vadinami specialiais užsakymais.</span><span class="sxs-lookup"><span data-stu-id="ada81-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="ada81-108">Šioje temoje pateikta susijusių parametrų ir operacijų srautų apžvalga.</span><span class="sxs-lookup"><span data-stu-id="ada81-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="ada81-109">Integruotų kanalų prekyboje dauguma pardavėjų suteikia galimybę kurti klientų užsakymus (arba specialius užsakymus) įvairiems produktų ir vykdymo reikalavimams įvykdyti.</span><span class="sxs-lookup"><span data-stu-id="ada81-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="ada81-110">Toliau nurodomi įprasti scenarijai.</span><span class="sxs-lookup"><span data-stu-id="ada81-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="ada81-111">Klientas nori, kad produktai būtų pristatyti konkrečią dieną konkrečiu adresu.</span><span class="sxs-lookup"><span data-stu-id="ada81-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="ada81-112">Klientas nori atsiimti produktus parduotuvėje arba vietoje, kuri nėra parduotuvė arba vieta, kurioje klientas tuos produktus nusipirko.</span><span class="sxs-lookup"><span data-stu-id="ada81-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="ada81-113">Klientas nori, kad kas nors kitas paimtų jo nupirktus produktus.</span><span class="sxs-lookup"><span data-stu-id="ada81-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="ada81-114">Pardavėjai taip pat naudoja kliento užsakymus, norėdami sumažinti prarasto pardavimo kiekius, kuriuos gali lemti atsargų stygius, kadangi prekes galima pristatyti arba atsiimti kitu laiku arba kitoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="ada81-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="ada81-115">Kliento užsakymų nustatymas</span><span class="sxs-lookup"><span data-stu-id="ada81-115">Set up customer orders</span></span>

<span data-ttu-id="ada81-116">Toliau pateikiama keletas parametrų, kuriuos galima nustatyti puslapyje **Prekybos parametrai** ir kurie nurodo, kaip kliento užsakymai yra vykdomi.</span><span class="sxs-lookup"><span data-stu-id="ada81-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="ada81-117">**Numatytasis depozito procentas** – nurodykite sumą, kurią klientas turi sumokėti kaip depozitą prieš patvirtinant užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ada81-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="ada81-118">Numatytoji depozito suma apskaičiuojama kaip užsakymo vertės procentas.</span><span class="sxs-lookup"><span data-stu-id="ada81-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="ada81-119">Atsižvelgiant į teises, parduotuvės atstovas gali perrašyti sumą naudodamas parinktį **Depozito perrašymas**.</span><span class="sxs-lookup"><span data-stu-id="ada81-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="ada81-120">**Atšaukimo mokesčio procentais** – jei atšaukiant kliento užsakymą taikomas mokestis, nurodykite to mokesčio sumą.</span><span class="sxs-lookup"><span data-stu-id="ada81-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="ada81-121">**Atšaukimo mokesčio kodas** – jei atšaukiant kliento užsakymą taikomas mokestis, tas mokestis bus nurodytas pardavimo užsakymo išlaidų kode.</span><span class="sxs-lookup"><span data-stu-id="ada81-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="ada81-122">Naudokite šį parametrą, kad nurodytumėte atšaukimo mokesčio kodą.</span><span class="sxs-lookup"><span data-stu-id="ada81-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="ada81-123">**Siuntimo mokesčio kodas** – pardavėjai gali taikyti papildomą mokestį už prekių siuntimą klientui.</span><span class="sxs-lookup"><span data-stu-id="ada81-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="ada81-124">To siuntimo mokesčio suma bus nurodyta pardavimo užsakymo išlaidų kode.</span><span class="sxs-lookup"><span data-stu-id="ada81-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="ada81-125">Naudokite šį parametrą, kad siuntimo mokesčio kodą susietumėte su siuntimo išlaidomis kliento užsakyme.</span><span class="sxs-lookup"><span data-stu-id="ada81-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="ada81-126">**Grąžinti siuntimo išlaidas** – nurodykite, ar siuntimo išlaidos, susietos su kliento užsakymų, yra grąžinamos.</span><span class="sxs-lookup"><span data-stu-id="ada81-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="ada81-127">**Maksimali suma, kuriai nereikia gauti patvirtinimo** – jei siuntimo išlaidos yra grąžinamos, nurodykite didžiausią visų grąžinimo užsakymų siuntimo išlaidų grąžinimo sumą.</span><span class="sxs-lookup"><span data-stu-id="ada81-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="ada81-128">Jei ši suma viršijama, vadovas turi ją perrašyti, kad būtų galima tęsti grąžinimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="ada81-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="ada81-129">Toliau nurodytais scenarijais siuntimo išlaidų grąžinimo suma gali viršyti anksčiau sumokėtą sumą.</span><span class="sxs-lookup"><span data-stu-id="ada81-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="ada81-130">Išlaidos taikomos pardavimo užsakymo antraštės lygyje ir, kai tam tikras produkto eilutės kiekis yra grąžinamas, didžiausios leidžiamos produktų ir kiekio siuntimo išlaidų grąžinimo sumos negalima nustatyti tokiu būdu, kuris tiktų visiems klientams.</span><span class="sxs-lookup"><span data-stu-id="ada81-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="ada81-131">Siuntimo išlaidos patiriamos kiekvieną kartą siunčiant prekes.</span><span class="sxs-lookup"><span data-stu-id="ada81-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="ada81-132">Jei klientas kelis kartus grąžina produktus, o pardavėjo strategijoje nurodyta, kad pardavėjas padengs grąžinimo siuntimo išlaidų sumą, grąžinimo siuntimo išlaidų suma bus didesnė nei faktinės siuntimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="ada81-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>
    

## <a name="disable-option-to-pay-later"></a><span data-ttu-id="ada81-133">Išjungti pasirinktį „mokėti vėliau”</span><span class="sxs-lookup"><span data-stu-id="ada81-133">Disable option to pay later</span></span>

<span data-ttu-id="ada81-134">„Commerce” versijoje 10.0.12 ir vėlesnėje, prekybininkai gali pašalinti pasirinktį „mokėti vėliau”, kai yra sukurtas kliento užsakymas EKA.</span><span class="sxs-lookup"><span data-stu-id="ada81-134">In Commerce version 10.0.12 and later, merchants can remove the option to pay later when a customer order is created at the POS.</span></span> <span data-ttu-id="ada81-135">Norėdami išjungti pasirinktį, atsidarykite **Funkcijų šabloną** kanalui, kur mokėjimas vėliau neleidžiamas, o tada pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="ada81-135">To disable the option, open the **Functionality profile** for the channel that paying later is not allowed in, and then select **Edit**.</span></span> <span data-ttu-id="ada81-136">Skirtuke **Bendra** iš išplečiamojo sąrašo pasirinkite **Reikalauti mokėjimo įvykdymo**.</span><span class="sxs-lookup"><span data-stu-id="ada81-136">On the **General** tab, select the dropdown for **Require payment for fulfillment**.</span></span> <span data-ttu-id="ada81-137">Jeigu mokėjimas vėliau negali būti leistinas EKA, pasirinkite **Reikiama kortelė** ir pasirinkite **Išsaugoti**.</span><span class="sxs-lookup"><span data-stu-id="ada81-137">If paying later should not be allowed at the POS, select **Card required** and select **Save**.</span></span> <span data-ttu-id="ada81-138">Paleiskite **1070** paskirstymo grafiką, kad sinchronizuotumėte šį pakeitimą kanale.</span><span class="sxs-lookup"><span data-stu-id="ada81-138">Run the **1070** distribution schedule to synchronize this change to the channel.</span></span> 

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="ada81-139">Kliento užsakymų operacijų srautas</span><span class="sxs-lookup"><span data-stu-id="ada81-139">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="ada81-140">Kliento užsakymo kūrimas naudojant „Modern POS“</span><span class="sxs-lookup"><span data-stu-id="ada81-140">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="ada81-141">Įtraukite į operaciją klientą.</span><span class="sxs-lookup"><span data-stu-id="ada81-141">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="ada81-142">Įtraukite produktų į krepšelį.</span><span class="sxs-lookup"><span data-stu-id="ada81-142">Add products to the cart.</span></span>
3. <span data-ttu-id="ada81-143">Spustelėkite **Kurti kliento užsakymą** ir tada pasirinkite užsakymo tipą.</span><span class="sxs-lookup"><span data-stu-id="ada81-143">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="ada81-144">Užsakymo tipas gali būti **Kliento užsakymas** arba **Pasiūlymas**.</span><span class="sxs-lookup"><span data-stu-id="ada81-144">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="ada81-145">Spustelėkite **Siųsti pasirinktus** arba **Siųsti viską**, norėdami siųsti produktus kliento sąskaitoje nurodytu adresu, nurodykite pageidaujamą siuntimą datą ir siuntimo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="ada81-145">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="ada81-146">Spustelėkite **Paimti pasirinktus** arba **Paimti viską**, norėdami pasirinkti produktus, kurie nurodytą dieną bus paimti iš dabartinės parduotuvės arba kitos parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="ada81-146">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="ada81-147">Surinkite depozito sumą, jei depozitas reikalingas.</span><span class="sxs-lookup"><span data-stu-id="ada81-147">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="ada81-148">Esamo kliento užsakymo redagavimas</span><span class="sxs-lookup"><span data-stu-id="ada81-148">Edit an existing customer order</span></span>

1. <span data-ttu-id="ada81-149">Pagrindiniame puslapyje spustelėkite **Rasti užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="ada81-149">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="ada81-150">Raskite ir pasirinkite užsakymą, kurį norite redaguoti.</span><span class="sxs-lookup"><span data-stu-id="ada81-150">Find and select the order to edit.</span></span> <span data-ttu-id="ada81-151">Puslapio apačioje spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="ada81-151">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="ada81-152">Užsakymo paėmimas</span><span class="sxs-lookup"><span data-stu-id="ada81-152">Pick up an order</span></span>

1. <span data-ttu-id="ada81-153">Pagrindiniame puslapyje spustelėkite **Rasti užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="ada81-153">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="ada81-154">Pasirinkite paimtiną užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ada81-154">Select the order to pick up.</span></span> <span data-ttu-id="ada81-155">Puslapio apačioje spustelėkite **Paėmimas ir pakavimas**.</span><span class="sxs-lookup"><span data-stu-id="ada81-155">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="ada81-156">Spustelėkite **Paimti**.</span><span class="sxs-lookup"><span data-stu-id="ada81-156">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="ada81-157">Užsakymo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="ada81-157">Cancel an order</span></span>

1. <span data-ttu-id="ada81-158">Pagrindiniame puslapyje spustelėkite **Rasti užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="ada81-158">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="ada81-159">Pasirinkite atšauktiną užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ada81-159">Select the order to cancel.</span></span> <span data-ttu-id="ada81-160">Puslapio apačioje spustelėkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="ada81-160">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="ada81-161">Grąžinimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="ada81-161">Create a return order</span></span>

1. <span data-ttu-id="ada81-162">Pagrindiniame puslapyje spustelėkite **Rasti užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="ada81-162">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="ada81-163">Pasirinkite grąžintiną užsakymą, pasirinkite užsakymo SF ir tada pasirinkite grąžintinų prekių produkto eilutę.</span><span class="sxs-lookup"><span data-stu-id="ada81-163">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="ada81-164">Puslapio apačioje spustelėkite **Grąžinimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="ada81-164">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="ada81-165">Kliento užsakymų asinchroninių operacijų srautas</span><span class="sxs-lookup"><span data-stu-id="ada81-165">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="ada81-166">Klientų užsakymus galima kurti iš elektroninio kasos aparato (EKA) kliento sinchroniniu arba asinchroniniu režimu.</span><span class="sxs-lookup"><span data-stu-id="ada81-166">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="ada81-167">Kliento užsakymų kūrimo asinchroniniu režimu funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="ada81-167">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="ada81-168">Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA šablonas** &gt; **Funkcijų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="ada81-168">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="ada81-169">„FastTab“ **Bendra** nustatykite parinktį **Kurti kliento užsakymą asinchroniniu režimu** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ada81-169">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="ada81-170">Kai parinktis **Kurti kliento užsakymą asinchroniniu režimu** nustatyta į **Taip**, kliento užsakymai visada kuriami asinchroniniu režimu, net jei galima naudoti „Retail Transaction Service“ (RTS).</span><span class="sxs-lookup"><span data-stu-id="ada81-170">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="ada81-171">Jei šią parinktį nustatysite į **Ne**, kliento užsakymai bus visada kuriami sinchroniniu režimu naudojant RTS.</span><span class="sxs-lookup"><span data-stu-id="ada81-171">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="ada81-172">Kai kliento užsakymai kuriami asinchroniniu režimu, jie perkeliami ir įterpiami į „Commerce“ naudojant perkėlimo (P) užduotis.</span><span class="sxs-lookup"><span data-stu-id="ada81-172">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="ada81-173">Atitinkami pardavimo užsakymai sukuriami, kai parinktis **Sinchronizuoti užsakymus** paleidžiama neautomatiškai arba paketinio vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="ada81-173">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ada81-174">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ada81-174">Additional resources</span></span>

[<span data-ttu-id="ada81-175">Hibridiniai kliento užsakymai</span><span class="sxs-lookup"><span data-stu-id="ada81-175">Hybrid customer orders</span></span>](hybrid-customer-orders.md)
