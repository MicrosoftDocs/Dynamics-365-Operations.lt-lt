---
title: Grąžinimo savikaina ir grąžinamos partijos ID
description: Galite norėti, kad grąžintų produktų savikaina būtų lygi produktų savikainai tuo metu, kai šiuos produktus pardavėte klientui. Tai galite nustatyti naudodami **Grąžinamos partijos ID**.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33cd3d50fe342ba12a17419f4e759c243a60b3e0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "335145"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="add08-104">Grąžinimo savikaina ir grąžinamos partijos ID</span><span class="sxs-lookup"><span data-stu-id="add08-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="add08-105">Į atsargas grąžintų produktų savaikaina skaičiuojama naudojant dabartinę šių produktų savikainą.</span><span class="sxs-lookup"><span data-stu-id="add08-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="add08-106">Tačiau galite norėti, kad grąžintų produktų savikaina būtų lygi produktų savikainai tuo metu, kai šiuos produktus pardavėte klientui.</span><span class="sxs-lookup"><span data-stu-id="add08-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="add08-107">Tai galite atlikti nustatyti formos **Pardavimo užsakymas** „FastTab“ skirtuko **Eilutės informacija** lauke **Grąžinamos partijos ID** .</span><span class="sxs-lookup"><span data-stu-id="add08-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="add08-108">Pvz., apsvarstykite toliau pateiktą scenarijų.</span><span class="sxs-lookup"><span data-stu-id="add08-108">For example, consider the following scenario.</span></span> <span data-ttu-id="add08-109">Klientui nusiunčiate SF.</span><span class="sxs-lookup"><span data-stu-id="add08-109">You invoice a customer.</span></span> <span data-ttu-id="add08-110">Tada klientas jums grąžina pristatytus produktus.</span><span class="sxs-lookup"><span data-stu-id="add08-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="add08-111">Jūs grąžinate produktus į atsargas.</span><span class="sxs-lookup"><span data-stu-id="add08-111">You return the products to stock.</span></span> <span data-ttu-id="add08-112">Tokiu atveju, kai kredituojate klientą už grąžintus produktus, šių produktų savikaina apskaičiuojama naudojant dabartinę savikainą.</span><span class="sxs-lookup"><span data-stu-id="add08-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="add08-113">Tačiau, jei naudosite lauką **Grąžinamos partijos ID**, grąžintų produktų savikaina bus apskaičiuojama naudojant savikainą, nurodytą pradinio pardavimo klientui SF.</span><span class="sxs-lookup"><span data-stu-id="add08-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="add08-114">Jei norite naudoti kitą nei dabartinę kliento grąžintų produktų savikainą, naudokite vieną iš toliau nurodytų būdų.</span><span class="sxs-lookup"><span data-stu-id="add08-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="add08-115">1 būdas: įveskite grąžinimo savikainą rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="add08-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="add08-116">Pagal numatytuosius nustatymus, kai įtraukiate prekes į grąžinimo užsakymą, šios prekės yra grąžinamos į atsargas nurodant dabartinę savikainą.</span><span class="sxs-lookup"><span data-stu-id="add08-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="add08-117">Jei norite nurodyti kitą grąžinimo savikainą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="add08-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="add08-118">Spustelėkite **Pardavimas ir rinkodara** \> **Bendra** \> **Grąžinimo užsakymai** \> **Visi grąžinimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="add08-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="add08-119">Dalies **Veiksmų sritis** grupėje **Naujas** spustelėkite **Grąžinimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="add08-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="add08-120">Formoje **Kurti grąžinimo užsakymą** pasirinkite kliento sąskaitą ir tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="add08-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="add08-121">Formoje **Grąžinimo užsakymas – RMA numeris: %1, %2** pasirinkite prekę ir tada įveskite neigiamą kiekį lauke **Kiekis**.</span><span class="sxs-lookup"><span data-stu-id="add08-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="add08-122">Spustelėkite „FastTab‟ skirtuką **Eilutės informacija**.</span><span class="sxs-lookup"><span data-stu-id="add08-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="add08-123">Skirtuko **Bendra** lauke **Grąžinimo savikaina** įveskitę vertę.</span><span class="sxs-lookup"><span data-stu-id="add08-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="add08-124">Ši vertė naudojama, kai prekės grąžinamos į atsargas.</span><span class="sxs-lookup"><span data-stu-id="add08-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="add08-125">Jei vertės neįvesite, grąžinant prekes į atsargas bus naudojama dabartinė savikaina.</span><span class="sxs-lookup"><span data-stu-id="add08-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="add08-126">2 būdas: automatiškas savikainos generavimas pagal kliento SF eilutę</span><span class="sxs-lookup"><span data-stu-id="add08-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="add08-127">Tai prioritetinis grąžinimo eilučių kūrimo būdas.</span><span class="sxs-lookup"><span data-stu-id="add08-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="add08-128">Norėdami naudoti produktų savikainą, kuri buvo tuo metu, kai šiuos produktus pardavėte klientui, sukurkite grąžinimo užsakymą ir nurodykite grąžintiną pardavimo eilutę.</span><span class="sxs-lookup"><span data-stu-id="add08-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="add08-129">Spustelėkite **Pardavimas ir rinkodara** \> **Bendra** \> **Grąžinimo užsakymai** \> **Visi grąžinimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="add08-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="add08-130">Dalies **Veiksmų sritis** grupėje **Naujas** spustelėkite **Grąžinimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="add08-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="add08-131">Formoje **Kurti grąžinimo užsakymą** pasirinkite kliento sąskaitą ir tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="add08-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="add08-132">Formos **Grąžinimo užsakymas – RMA numeris: %1, %2** dalyje **Veiksmų sritis** spustelėkite **Rasti pardavimo užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="add08-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="add08-133">Formoje **Rasti pardavimo užsakymą** pasirinkite grąžintiną SF eilutę ir tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="add08-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="add08-134">„FastTab“ skirtuko **Eilutės informacija** skirtuko **Bendra** lauke **Grąžinamos partijos ID** rodoma vertė iš pradinio pardavimo eilutės.</span><span class="sxs-lookup"><span data-stu-id="add08-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="add08-135">Be to, lauke **Grąžinimo savikaina** rodoma savikainos vertė iš pradinio pardavimo eilutės.</span><span class="sxs-lookup"><span data-stu-id="add08-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="add08-136">Savikainos skaičiavimo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="add08-136">Cost calculation example</span></span>

<span data-ttu-id="add08-137">Kai grąžinimo savikainą nurodote grąžinimo užsakymo eilutės lauke **Grąžinamos partijos ID**, naudojama grąžinimo užsakymo eilutėje nurodyta savikaina.</span><span class="sxs-lookup"><span data-stu-id="add08-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="add08-138">Įjungus atsargų uždarymo arba perskaičiavimo funkciją, pradinio pardavimo eilutėje nurodyta savikaina pakoreguojama.</span><span class="sxs-lookup"><span data-stu-id="add08-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="add08-139">Grąžinimo užsakymo eilutėje nurodyta savaikaina automatiškai pakoreguojama, kad atspindėtų tokią pačią vieneto savikainą.</span><span class="sxs-lookup"><span data-stu-id="add08-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="add08-140">Sukurkite ir išleiskite produktą pavadinimu Testas.</span><span class="sxs-lookup"><span data-stu-id="add08-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="add08-141">Formoje **Išleisto produkto informacija** nurodykite tokią informaciją:</span><span class="sxs-lookup"><span data-stu-id="add08-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="add08-142">„FastTab“ skirtuko **Tvarkyti savikainą** lauke **Prekių grupė** pasirinkite grupę **Dalys**.</span><span class="sxs-lookup"><span data-stu-id="add08-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="add08-143">„FastTab“ skirtuko **Bendra** lauke **Prekių modelių grupė** pasirinkite **DEF**.</span><span class="sxs-lookup"><span data-stu-id="add08-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="add08-144">„FastTab“ skirtuko **Pirkimas** lauke **Kaina** įveskite 10,00 kaip prekės savikainą.</span><span class="sxs-lookup"><span data-stu-id="add08-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="add08-145">Dalyje **Veiksmų sritis** spustelėkite **Dimensijų grupės**.</span><span class="sxs-lookup"><span data-stu-id="add08-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="add08-146">Lauke **Saugojimo dimensijų grupė** pasirinkite **Tik vieta ir sandėlis**.</span><span class="sxs-lookup"><span data-stu-id="add08-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="add08-147">Lauke **Sekimo dimensijų grupė** pasirinkite **Nėra aktyvių sekimo dimensijų**.</span><span class="sxs-lookup"><span data-stu-id="add08-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="add08-148">Sukurkite pirkimo užsakymą 10 testinės prekės vienetų po 6,00 už vienetą, tada užregistruokite pirkimo užsakymo SF.</span><span class="sxs-lookup"><span data-stu-id="add08-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="add08-149">Sukurkite antrą pirkimo užsakymą 10 testinės prekės vienetų po 8,00 už vienetą, tada užregistruokite pirkimo užsakymo SF.</span><span class="sxs-lookup"><span data-stu-id="add08-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="add08-150">Užregistruokite SF pardavimo užsakymui parduoti penkis testinės prekės vienetus.</span><span class="sxs-lookup"><span data-stu-id="add08-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="add08-151">Šiuo atveju pardavimo užsakymo eilutė bus įkainota 35,00 (5 vienetai \* 7,00 vidutinė vieneto savikaina).</span><span class="sxs-lookup"><span data-stu-id="add08-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="add08-152">Sukurkite grąžinimo užsakymą klientui.</span><span class="sxs-lookup"><span data-stu-id="add08-152">Create a return order for the customer.</span></span> <span data-ttu-id="add08-153">Formoje **Rasti pardavimo užsakymą** pasirinkite SF eilutę ir tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="add08-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="add08-154">Formoje **Grąžinimo užsakymas – RMA numeris: %1, %2** patikrinkite, ar testinės prekės grąžinimo užsakymas yra sugeneruotas.</span><span class="sxs-lookup"><span data-stu-id="add08-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="add08-155">Grąžinimo užsakymo kiekis nustatomas kaip -5,00.</span><span class="sxs-lookup"><span data-stu-id="add08-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="add08-156">Lauke **Grąžinamos partijos ID** rodomas partijos ID.</span><span class="sxs-lookup"><span data-stu-id="add08-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="add08-157">Šis partijos ID paimamas iš pradinio klientui parduotos prekės pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="add08-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="add08-158">Lauke **Grąžinimo savikaina** rodoma savikaina iš pradinio pardavimo eilutės.</span><span class="sxs-lookup"><span data-stu-id="add08-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="add08-159">Užregistruokite grąžintų prekių gavimą.</span><span class="sxs-lookup"><span data-stu-id="add08-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="add08-160">Užregistruokite grąžintų prekių važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="add08-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="add08-161">Užregistruokite grąžinimo užsakymo SF.</span><span class="sxs-lookup"><span data-stu-id="add08-161">Post an invoice for the return order.</span></span> <span data-ttu-id="add08-162">Sąrašo puslapyje **Visi pardavimo užsakymai** pasirinkite pardavimo užsakymą, kurio užsakymo tipas yra **Grąžintas užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="add08-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="add08-163">Atidarykite formą **Atsargų operacijos**.</span><span class="sxs-lookup"><span data-stu-id="add08-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="add08-164">Patikrinkite, ar grąžinimas įkainotas 7,00 už vienetą, pagal lauke **Grąžinimo savikaina** nurodytą vertę – iš viso lauke **Savikainos suma** turi būti 35,00.</span><span class="sxs-lookup"><span data-stu-id="add08-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="add08-165">Formą **Atsargų operacijos** galite atidaryti iš formos **Grąžinimo užsakymas – RMA numeris: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="add08-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="add08-166">Tinklelyje **Eilutės** spustelėkite **Atsargos** \> **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="add08-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="add08-167">Atsargų ir sandėlio valdymo formoje **Uždarymas ir koregavimas** vykdykite procedūrą **3. Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="add08-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="add08-168">Šis veiksmas pakoreguos pradinio pardavimo eilutėje nurodytą savikainą, iš -35,00 (5 vienetai \* 7,00) į -30,00 (5 vienetai \* 6,00).</span><span class="sxs-lookup"><span data-stu-id="add08-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="add08-169">Taip yra todėl, kad atsargų modelių grupė naudoja „pirmas ateina, pirmas išeina“ (FIFO) metodą ir 6,00 už vienetą yra FIFO kaina iš pirmojo pirkimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="add08-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="add08-170">Be to, šis veiksmas pakoreguoja savikainą grąžinimo pardavimo eilutėje, kad ji atitiktų vieneto savikainą pradinio pardavimo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="add08-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="add08-171">Todėl savikaina grąžinimo eilutėje pakoreguojama iš 35,00 į 30,00.</span><span class="sxs-lookup"><span data-stu-id="add08-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>




