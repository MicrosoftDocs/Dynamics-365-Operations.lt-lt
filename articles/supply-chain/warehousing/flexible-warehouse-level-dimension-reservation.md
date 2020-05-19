---
title: Pritaikomų sandėlio lygio dimensijų rezervavimo strategija
description: Šioje temoje aprašoma atsargų rezervavimo strategija, kuria įmonės, prekiaujančios pagal paketą sekamais produktais ir vykdančios savo logistiką kaip palaikančias WMS operacijas, rezervuoja konkrečius kliento pardavimo užsakymų paketus, net jei rezervavimo hierarchija, kuri yra susieta su produktais, neleidžia rezervuoti tam tikrų paketų.
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 6c462a87494c434a6047542d448a85b3bce9f769
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346473"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="50d47-103">Pritaikomų sandėlio lygio dimensijų rezervavimo strategija</span><span class="sxs-lookup"><span data-stu-id="50d47-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50d47-104">Kai „Batch-below\[vieta\]“ tipo atsargų rezervavimo hierarchija, yra susieta su produktais, įmonėmis, kurios parduoda pagal paketą sekamus produktus ir valdo jų logistiką kaip operacijas, įjungtas „Microsoft Dynamics 365“, sandėlio valdymo sistema (WMS) negalima rezervuoti konkrečių tų produktų, skirtų kliento pardavimo užsakymams, paketų.</span><span class="sxs-lookup"><span data-stu-id="50d47-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="50d47-105">Šioje temoje aprašoma atsargų rezervavimo strategija, kuria šie verslai rezervuoja tam tikrus paketus, net jei produktai yra susieti su rezervavimo hierarchija „Batch-below\[vieta\]“.</span><span class="sxs-lookup"><span data-stu-id="50d47-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="50d47-106">Atsargų rezervavimo hierarchija</span><span class="sxs-lookup"><span data-stu-id="50d47-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="50d47-107">Šiame skyriuje apibendrinama esama atsargų rezervavimo hierarchija.</span><span class="sxs-lookup"><span data-stu-id="50d47-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="50d47-108">Jame apžvelgiama, kaip vykdomi pagal paketą ir pagal seriją sekami elementai.</span><span class="sxs-lookup"><span data-stu-id="50d47-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="50d47-109">Atsargų rezervavimo hierarchija nurodo, kad, kiek tai susiję su saugojimo dimensijomis, poreikio užsakymas perkelia privalomus vietos, sandėlio ir atsargų būsenos matmenis, tuo tarpu sandėlio logika yra atsakinga už vietos priskyrimą pageidaujamiems kiekiams ir vietos rezervavimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="50d47-110">Kitaip tariant, atliekant sąveiką tarp poreikio užsakymo ir sandėlio operacijų, tikimasi, kad poreikio užsakyme bus nurodyta iš kur užsakymas bus siunčiamas (t. y., kokios vietos ir sandėlio).</span><span class="sxs-lookup"><span data-stu-id="50d47-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="50d47-111">Tada sandėliui taikoma jo logika, kad būtų surastas reikiamas kiekis sandėlio patalpose.</span><span class="sxs-lookup"><span data-stu-id="50d47-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="50d47-112">Tačiau, siekiant atitikti verslo veiklos modelį, sekimo dimensijos (paketo ir serijos numeriai) yra lankstesnės.</span><span class="sxs-lookup"><span data-stu-id="50d47-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="50d47-113">Atsargų rezervavimo hierarchijoje gali tilpti scenarijai, kuriuose taikomos šios sąlygos:</span><span class="sxs-lookup"><span data-stu-id="50d47-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="50d47-114">Verslas priklauso nuo jo sandėlio operacijų, siekiant valdyti išrinkimo kiekius, kuriuose yra paketo ar serijos numerių, po to, kai sandėliavimo saugykloje buvo surasti kiekiai.</span><span class="sxs-lookup"><span data-stu-id="50d47-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="50d47-115">Šis modelis dažnai nurodomas kaip *Batch-below\[vieta\]*.</span><span class="sxs-lookup"><span data-stu-id="50d47-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="50d47-116">Jis paprastai naudojamas, kai produkto paketo ar serijos numerio identifikacija nėra svarbi klientams, kurie turi paklausą su parduodančiomis įmonėmis.</span><span class="sxs-lookup"><span data-stu-id="50d47-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="50d47-117">Jei paketo ar serijos numeriai yra kliento užsakymo specifikacijos dalis ir jie įrašomi poreikio užsakyme, sandėlio operacijos, kurios nustato sandėlio kiekius, yra suvaržytos konkrečių pageidaujamų numerių ir joms neleidžiama jų keisti.</span><span class="sxs-lookup"><span data-stu-id="50d47-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="50d47-118">Šis modelis dažnai nurodomas kaip *Batch-above\[vieta\]*.</span><span class="sxs-lookup"><span data-stu-id="50d47-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="50d47-119">Šiuose scenarijuose problema yra ta, kad kiekvienam išleistam produktui gali būti priskirta tik viena atsargų rezervavimo hierarchija.</span><span class="sxs-lookup"><span data-stu-id="50d47-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="50d47-120">Todėl, kad WMS galėtų dirbti su sekamomis prekėmis, po to, kai hierarchijos priskyrimas nustato, kada turi būti rezervuotas paketo ar serijos numeris (kai poreikio užsakymas jau užsakytas arba per sandėlio išrinkimo darbą), šis laikas negali būti pakeistas ad hoc pagrindu.</span><span class="sxs-lookup"><span data-stu-id="50d47-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="50d47-121">Lankstus pagal paketą sekamų prekių rezervavimas</span><span class="sxs-lookup"><span data-stu-id="50d47-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="50d47-122">Verslo scenarijus</span><span class="sxs-lookup"><span data-stu-id="50d47-122">Business scenario</span></span>

<span data-ttu-id="50d47-123">Šiame scenarijuje įmonė naudoja atsargų strategiją, kurioje pagamintos prekės sekamos pagal paketo numerius.</span><span class="sxs-lookup"><span data-stu-id="50d47-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="50d47-124">Ši įmonė taip pat naudoja WMS darbo krūvį.</span><span class="sxs-lookup"><span data-stu-id="50d47-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="50d47-125">Kadangi šis darbo krūvio logika tinkamai paruošta planuoti ir vykdyti sandėlio išrinkimo ir siuntimo operacijas, skirtas prekėms, kurioms įgalinti paketai, dauguma pagamintų prekių yra susietos su atsargų rezervavimo hierarchija „Batch-below\[vieta\]“.</span><span class="sxs-lookup"><span data-stu-id="50d47-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="50d47-126">Šio tipo veiklos sąrankos pranašumas yra tas, kad sprendimai (kurie iš esmės yra rezervavimo sprendimai) dėl to, kurie paketai turi būti paimti ir kur jie turi būti padėti sandėlyje, yra atidėti, kol bus pradėtos sandėlio išrinkimo operacijos.</span><span class="sxs-lookup"><span data-stu-id="50d47-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="50d47-127">Jos neatliekamos, kai kliento užsakymas pateikiamas.</span><span class="sxs-lookup"><span data-stu-id="50d47-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="50d47-128">Nors rezervavimo hierarchija „Batch-below\[vieta\]“ puikiai tenkina įmonės verslo tikslus, daugeliui įmonės nuolatinių klientų reikia to paties paketo, kurį jie anksčiau pirko, kai jie vėl užsako produktų.</span><span class="sxs-lookup"><span data-stu-id="50d47-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="50d47-129">Todėl įmonė ieško lankstumo taip, kad būtų tvarkomos paketo rezervavimo taisyklės, jog, atsižvelgiant į kliento norą įsigyti tą pačią prekę, galimi šie būdai:</span><span class="sxs-lookup"><span data-stu-id="50d47-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="50d47-130">Paketo numerį galima įrašyti ir rezervuoti, kai užsakymą priima pardavimo apdorojimo priemonė, ir jo negalima keisti vykdant sandėlio operacijas ir (arba) kitus reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="50d47-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="50d47-131">Tai padeda užtikrinti, kad užsakytas paketo numeris yra siunčiamas klientui.</span><span class="sxs-lookup"><span data-stu-id="50d47-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="50d47-132">Jei paketo numeris nėra svarbus klientui, sandėlio operacijomis galima nustatyti paketo numerį atliekant išrinkimo darbus, atlikus pardavimo užsakymų registravimą ir rezervavimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="50d47-133">Konkretaus paketo rezervavimo leidimas pardavimo užsakyme</span><span class="sxs-lookup"><span data-stu-id="50d47-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="50d47-134">Norint, kad prekių, susietų su atsargų rezervavimo hierarchija „Batch-below\[vieta\]“, paketo rezervavimo veikimas būtų pageidaujamo dinamiškumo, atsargų valdytojai turi pažymėti žymės langelį **Leisti rezervuoti užsakymą pagal poreikį**, skirtą **paketo numerio** lygiui, esančiam puslapyje **Atsargų rezervavimo hierarchijos**.</span><span class="sxs-lookup"><span data-stu-id="50d47-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Atsargų rezervavimo hierarchijos dinamiškumo išplėtimas](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="50d47-136">Pasirinkus **paketo numerio** lygį hierarchijoje, visos aukščiau nurodyto lygio dimensijos ir iki lygio **Vieta** bus pasirenkamos automatiškai.</span><span class="sxs-lookup"><span data-stu-id="50d47-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="50d47-137">(Pagal numatytuosius parametrus visos dimensijos virš lygio **Vieta** yra iš anksto atrinktos). Šis veikimas atspindi logiką, kai visos dimensijos, esančios tarp paketo numerio ir vietos, taip pat automatiškai rezervuojamos, kai užsakymo eilutėje rezervuojamas konkretus paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="50d47-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="50d47-138">Žymės langelis **Leisti rezervuoti užsakymą pagal poreikį** taikomas tik rezervavimo hierarchijos lygiui, kuris yra mažesnis nei sandėlio vietos dimensija.</span><span class="sxs-lookup"><span data-stu-id="50d47-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="50d47-139">**Paketo numeris** yra vienintelis hierarchijos lygis, kuris yra atidaromas naudojant dinamiškas rezervavimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="50d47-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="50d47-140">Kitaip tariant, negalite pasirinkti žymės langelio **Leisti rezervuoti užsakymą pagal poreikį**, skirto lygiui **Vieta**, **Numerio lentelė** ar **Serijos numeris**.</span><span class="sxs-lookup"><span data-stu-id="50d47-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="50d47-141">Jei jūsų rezervavimo hierarchijoje yra serijos numerio dimensija (kuri visada turi būti mažesnė už lygį **Paketo numeris**) ir jei jau įjungėte paketo numerio paketui būdingą rezervavimą, sistema toliau tvarkys serijos numerio rezervavimo ir išrinkimo operacijas pagal taisykles, taikomas „Serial-below\[vieta\]“ rezervavimo strategijai.</span><span class="sxs-lookup"><span data-stu-id="50d47-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="50d47-142">Bet kuriuo metu galite leisti atlikti paketui būdingą esamo „Batch-below\[vieta\]“ rezervavimo hierarchiją jūsų įdiegtyje.</span><span class="sxs-lookup"><span data-stu-id="50d47-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="50d47-143">Šis keitimas neturės įtakos jokiems rezervavimams ir atidarytiems sandėlio darbams, kurie buvo sukurti prieš keičiant.</span><span class="sxs-lookup"><span data-stu-id="50d47-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="50d47-144">Tačiau žymės langelio **Leisti rezervuoti užsakymą pagal poreikį** negalima išvalyti, jei problemų tipo **Rezervuotas užsakytas**, **Rezervuotas faktinis** ar **Užsakytas** atsargų operacijos yra vienai ar daugiau prekių, susijusių su ta rezervavimo hierarchija.</span><span class="sxs-lookup"><span data-stu-id="50d47-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="50d47-145">Jei prekės esama rezervavimo hierarchija neleidžia užsakyti paketo specifikacijos, galite ją iš naujo priskirti rezervavimo hierarchijai, kuri leidžia paketo specifikaciją, jei hierarchijos lygio struktūra vienoda abiejose hierarchijose.</span><span class="sxs-lookup"><span data-stu-id="50d47-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="50d47-146">Naudokite funkciją **Pakeisti prekių rezervavimo hierarchiją** atlikti priskyrimą iš naujo.</span><span class="sxs-lookup"><span data-stu-id="50d47-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="50d47-147">Šis keitimas gali būti svarbus, jei norite, kad būtų išvengti dinamiško paketo rezervavimo pagal paketą sekamų prekių porinkiniui, ir norite jį leisti naudoti likusiame produkto portfelyje.</span><span class="sxs-lookup"><span data-stu-id="50d47-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="50d47-148">Neatsižvelgiant į tai, ar pažymėjote žymės langelį **Leisti rezervuoti užsakymą pagal poreikį**, jei nenorite rezervuoti konkretaus prekės paketo numerio užsakymo eilutėje, numatytoji sandėlio operacijų logika, kuri galioja „Batch-below\[vieta\]“ rezervavimo hierarchijoje, vis tiek bus taikoma.</span><span class="sxs-lookup"><span data-stu-id="50d47-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="50d47-149">Kliento užsakymo konkretaus paketo numerio rezervavimas</span><span class="sxs-lookup"><span data-stu-id="50d47-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="50d47-150">Po to, kai pagal paketą sekamos prekės „Batch-below\[vieta\]“ atsargų rezervavimo hierarchija yra nustatyta taip, kad būtų leidžiama rezervuoti konkrečius paketų numerius pardavimo užsakymuose, pardavimo užsakymų procesorius gali atlikti kliento užsakymus tai pačiai prekei vienu iš šių būdų, atsižvelgiant į kliento užklausą:</span><span class="sxs-lookup"><span data-stu-id="50d47-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="50d47-151">**Įvesti užsakymo informaciją nenurodant paketo numerio** – šis metodas turėtų būti naudojamas, kai produkto paketo specifikacija nėra svarbi klientui.</span><span class="sxs-lookup"><span data-stu-id="50d47-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="50d47-152">Visi esami procesai, susieti su šio tipo užsakymo tvarkymu, sistemoje lieka nekeisti.</span><span class="sxs-lookup"><span data-stu-id="50d47-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="50d47-153">Vartotojui nereikia atlikti jokių papildomų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="50d47-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="50d47-154">**Įvesti užsakymo informaciją ir rezervuoti konkretų paketo numerį** – šis metodas turėtų būti naudojamas, kai klientas reikalauja konkretaus paketo.</span><span class="sxs-lookup"><span data-stu-id="50d47-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="50d47-155">Paprastai klientai reikalauja konkretaus paketo, kai jie vėl užsako anksčiau įsigytus produktus.</span><span class="sxs-lookup"><span data-stu-id="50d47-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="50d47-156">Šio tipo paketui būdingas rezervavimas nurodytas kaip *įvykdyto užsakymo rezervavimas*.</span><span class="sxs-lookup"><span data-stu-id="50d47-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="50d47-157">Šis taisyklių rinkinys galioja, kai apdorojami kiekiai, o paketo numeris yra vykdomas konkrečiam užsakymui:</span><span class="sxs-lookup"><span data-stu-id="50d47-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="50d47-158">Tam, kad būtų galima rezervuoti konkretų prekės paketo numerį, esantį „Batch-below\[vieta\]“ rezervavimo strategijoje, sistema turi rezervuoti visas dimensijas naudojant vietą.</span><span class="sxs-lookup"><span data-stu-id="50d47-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="50d47-159">Šiame intervale paprastai būna numerio lentelės dimensija.</span><span class="sxs-lookup"><span data-stu-id="50d47-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="50d47-160">Vietos nurodymai nenaudojami, kai kuriami išrinkimo darbai, skirti pardavimo eilutei, kuriai naudojama įvykdyto užsakymo paketo rezervacija.</span><span class="sxs-lookup"><span data-stu-id="50d47-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="50d47-161">Sandėlio darbo, skirto įvykdytų užsakymų paketams, apdorojimo metu, nei vartotojui, nei sistemai neleidžiama keisti paketo numerio.</span><span class="sxs-lookup"><span data-stu-id="50d47-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="50d47-162">(Šis apdorojimas apima išimčių tvarkymą.)</span><span class="sxs-lookup"><span data-stu-id="50d47-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="50d47-163">Toliau pateiktame pavyzdyje parodytas visapusis srautas.</span><span class="sxs-lookup"><span data-stu-id="50d47-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="50d47-164">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="50d47-164">Example scenario</span></span>

<span data-ttu-id="50d47-165">Šiam pavyzdžiui turite įdiegti demonstracinius duomenis ir naudoti **USMF** demonstracinių duomenų įmonę.</span><span class="sxs-lookup"><span data-stu-id="50d47-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="50d47-166">Atsargų rezervavimo hierarchijos nustatymas leisti paketui būdingą rezervaciją</span><span class="sxs-lookup"><span data-stu-id="50d47-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="50d47-167">Eiti į **Sandėlio valdymas** \> **Sąranka** \> **Atsargos \> Rezervavimo hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="50d47-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="50d47-168">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="50d47-168">Select **New**.</span></span>
3. <span data-ttu-id="50d47-169">Lauke **Pavadinimas** įveskite pavadinimą (pavyzdžiui, **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="50d47-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="50d47-170">Lauke **Aprašas** įveskite aprašą (pvz., **Mažiau dinamiškas paketas**).</span><span class="sxs-lookup"><span data-stu-id="50d47-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="50d47-171">Lauke **Pasirinkta** pažymėkite **Serijos numeris** ir **Savininkas**, tada pasirinkite kairiosios rodyklės mygtuką, kad perkeltumėte juos į lauką **Pasiekiama**.</span><span class="sxs-lookup"><span data-stu-id="50d47-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="50d47-172">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="50d47-172">Select **OK**.</span></span>
7. <span data-ttu-id="50d47-173">Dimensijos lygio **Paketo numeris** eilutėje pažymėkite žymės langelį **Leisti rezervuoti užsakymą pagal poreikį**.</span><span class="sxs-lookup"><span data-stu-id="50d47-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="50d47-174">Lygiai **Numerio lentelė** ir **Vieta** parenkami automatiškai, tad jūs negalite išvalyti jų žymės langelių.</span><span class="sxs-lookup"><span data-stu-id="50d47-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="50d47-175">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="50d47-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="50d47-176">Kurti naują išleistą produktą</span><span class="sxs-lookup"><span data-stu-id="50d47-176">Create a new released product</span></span>

1. <span data-ttu-id="50d47-177">Nustatykite tris bendrųjų produkto duomenų parametrus naudodami šias vertes:</span><span class="sxs-lookup"><span data-stu-id="50d47-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="50d47-178">Lauke **Saugojimo dimensijų grupė** pasirinkite **Sand**.</span><span class="sxs-lookup"><span data-stu-id="50d47-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="50d47-179">Lauke **Saugojimo dimensijų grupė** pasirinkite **Pak. fakt**.</span><span class="sxs-lookup"><span data-stu-id="50d47-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="50d47-180">Lauke **Rezervavimo hierarchija** pasirinkite **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="50d47-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="50d47-181">Sukurkite du paketo numerius, pvz., **B11** ir **B22**.</span><span class="sxs-lookup"><span data-stu-id="50d47-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="50d47-182">Įtraukite prekių kiekius į turimas atsargas, naudodami šias vertes.</span><span class="sxs-lookup"><span data-stu-id="50d47-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="50d47-183">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="50d47-183">Warehouse</span></span> | <span data-ttu-id="50d47-184">Paketo numeris</span><span class="sxs-lookup"><span data-stu-id="50d47-184">Batch number</span></span> | <span data-ttu-id="50d47-185">Vieta</span><span class="sxs-lookup"><span data-stu-id="50d47-185">Location</span></span> | <span data-ttu-id="50d47-186">Numerio lentelė</span><span class="sxs-lookup"><span data-stu-id="50d47-186">License plate</span></span> | <span data-ttu-id="50d47-187">Kiekis</span><span class="sxs-lookup"><span data-stu-id="50d47-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="50d47-188">24</span><span class="sxs-lookup"><span data-stu-id="50d47-188">24</span></span>        | <span data-ttu-id="50d47-189">B11</span><span class="sxs-lookup"><span data-stu-id="50d47-189">B11</span></span>          | <span data-ttu-id="50d47-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="50d47-190">BULK-001</span></span> | <span data-ttu-id="50d47-191">Jokia</span><span class="sxs-lookup"><span data-stu-id="50d47-191">None</span></span>          | <span data-ttu-id="50d47-192">10</span><span class="sxs-lookup"><span data-stu-id="50d47-192">10</span></span>       |
    | <span data-ttu-id="50d47-193">24</span><span class="sxs-lookup"><span data-stu-id="50d47-193">24</span></span>        | <span data-ttu-id="50d47-194">B11</span><span class="sxs-lookup"><span data-stu-id="50d47-194">B11</span></span>          | <span data-ttu-id="50d47-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="50d47-195">FL-001</span></span>   | <span data-ttu-id="50d47-196">LP11</span><span class="sxs-lookup"><span data-stu-id="50d47-196">LP11</span></span>          | <span data-ttu-id="50d47-197">10</span><span class="sxs-lookup"><span data-stu-id="50d47-197">10</span></span>       |
    | <span data-ttu-id="50d47-198">24</span><span class="sxs-lookup"><span data-stu-id="50d47-198">24</span></span>        | <span data-ttu-id="50d47-199">B22</span><span class="sxs-lookup"><span data-stu-id="50d47-199">B22</span></span>          | <span data-ttu-id="50d47-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="50d47-200">FL-002</span></span>   | <span data-ttu-id="50d47-201">LP22</span><span class="sxs-lookup"><span data-stu-id="50d47-201">LP22</span></span>          | <span data-ttu-id="50d47-202">10</span><span class="sxs-lookup"><span data-stu-id="50d47-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="50d47-203">Pardavimo užsakymo išsamios informacijos įvedimas</span><span class="sxs-lookup"><span data-stu-id="50d47-203">Enter sales order details</span></span>

1. <span data-ttu-id="50d47-204">Eikite į **Pardavimas ir rinkodara** \> **Pardavimo užsakymai** \> **Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="50d47-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="50d47-205">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="50d47-205">Select **New**.</span></span>
3. <span data-ttu-id="50d47-206">Pardavimo užsakymo antraštėje, lauke **Kliento sąskaita** įveskite **JAV-003**.</span><span class="sxs-lookup"><span data-stu-id="50d47-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="50d47-207">Pridėkite naujos prekės eilutę ir kaip kiekį įveskite **10**.</span><span class="sxs-lookup"><span data-stu-id="50d47-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="50d47-208">Įsitikinkite, kad laukas **Sandėlis** nustatytas į **24**.</span><span class="sxs-lookup"><span data-stu-id="50d47-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="50d47-209">„FastTab“ **Pardavimo užsakymo eilutės** pasirinkite **Atsargos**, tada grupėje **Tvarkyti** pasirinkite **Paketo rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="50d47-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="50d47-210">Puslapyje **Paketo rezervavimas** rodomas paketų, kuriuos galima rezervuoti užsakymo eilutėje, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="50d47-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="50d47-211">Šiame pavyzdyje rodomas kiekis **20** paketo numeriui **B11** ir kiekis **10** paketo numeriui **B22**.</span><span class="sxs-lookup"><span data-stu-id="50d47-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="50d47-212">Atkreipkite dėmesį, kad puslapio **Paketo rezervavimas** negalima pasiekti naudojant eilutę, jei tos eilutės prekė susieta su rezervavimo hierarchija „Batch-below\[vieta\]“, nebent ji nustatyta taip, kad leistų atlikti paketui būdingą rezervavimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="50d47-213">Norėdami rezervuoti konkretų pardavimo užsakymo paketą, turite naudoti puslapį **Paketo rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="50d47-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="50d47-214">Jei paketo numerį įvesite tiesiai į pardavimo užsakymo eilutę, sistema vykdys taip, lyg būtumėte įvedę konkrečią prekės, kuriai taikoma „Batch-below\[vieta\]“ rezervavimo strategija, paketo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="50d47-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="50d47-215">Įrašius eilutę, bus parodytas įspėjamasis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="50d47-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="50d47-216">Jei patvirtinate, kad paketo numeris turi būti nurodytas tiesiogiai užsakymo eilutėje, eilutė nebus apdorota naudojant įprastą sandėlio valdymo logiką.</span><span class="sxs-lookup"><span data-stu-id="50d47-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="50d47-217">Jei rezervuosite kiekį iš puslapio **Rezervavimas**, nebus rezervuotas joks konkretus paketas, o eilutės sandėlio operacijų vykdymas vadovausis taisyklėmis, kurios bus taikomos „Batch-below\[vieta\]“ rezervavimo strategijoje.</span><span class="sxs-lookup"><span data-stu-id="50d47-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="50d47-218">Paprastai šis puslapis veikia ir sąveikauja taip pat, kaip jis veikia ir sąveikauja su prekėmis, kurios turi su „Batch-above\[vieta\]“ tipu susijusią rezervavimo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="50d47-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="50d47-219">Tačiau taikomos šios išimtys:</span><span class="sxs-lookup"><span data-stu-id="50d47-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="50d47-220">„FastTab“**Paketo numeriai, įvykdyti šaltinio eilutei** nurodo paketo numerius, kurie rezervuoti užsakymo eilutei.</span><span class="sxs-lookup"><span data-stu-id="50d47-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="50d47-221">Paketo vertės tinklelyje bus rodomos viso užsakymo eilutės vykdymo ciklo metu, įskaitant sandėlio apdorojimo etapus.</span><span class="sxs-lookup"><span data-stu-id="50d47-221">The batch values in the grid will be shown throughout the fulfilment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="50d47-222">Priešingai, „FastTab“ **Peržiūra** įprastas užsakymo eilutės rezervavimas (t. y. rezervavimas, kuris atliekamas virš **vietos** lygio dimensijų) rodomas tinklelyje iki vietos, kai sukuriamas sandėlio darbas.</span><span class="sxs-lookup"><span data-stu-id="50d47-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="50d47-223">Tada darbo objektas perima eilutės rezervavimą, o eilutės rezervavimas puslapyje nebebus rodomas.</span><span class="sxs-lookup"><span data-stu-id="50d47-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="50d47-224">„FastTab“ **Paketo numeriai, vykdomi šaltinio eilutei** padeda užtikrinti, kad pardavimo užsakymo procesorius galėtų peržiūrėti paketo numerius, kurie buvo įvykdyti kliento užsakymui, bet kada ciklo metu iki sąskaitos faktūros išrašymo.</span><span class="sxs-lookup"><span data-stu-id="50d47-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="50d47-225">Be to, kad būtų galima rezervuoti tam tikrą paketą, vartotojas gali rankiniu būdu pasirinkti konkrečią paketo vietą ir numerio lentelę, užuot leidęs sistemai automatiškai jas parinkti.</span><span class="sxs-lookup"><span data-stu-id="50d47-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="50d47-226">Ši charakteristika susijusi su įvykdyto užsakymo paketo rezervavimo mechanizmo dizaino įrankiu.</span><span class="sxs-lookup"><span data-stu-id="50d47-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="50d47-227">Kaip jau minėta, kai paketo numeris rezervuojamas prekei, esančiai „Batch-below\[vieta\]“ rezervavimo strategijoje, sistema turi rezervuoti visas dimensijas naudojant vietą.</span><span class="sxs-lookup"><span data-stu-id="50d47-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="50d47-228">Todėl sandėlio darbas bus atliekamas tose pačiose saugojimo dimensijose, kurias rezervavo vartotojai, dirbę su užsakymais, ir ne visada gali nurodyti prekių saugojimo vietą, kuri yra patogi arba netgi įmanoma,kalbant apie išrinkimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="50d47-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="50d47-229">Jei užsakymo vykdytojai žino apie sandėlio apribojimus, jie gali norėti neautomatiniu būdu pasirinkti konkrečias vietas ir numerio lenteles, kai jie rezervuoja paketą.</span><span class="sxs-lookup"><span data-stu-id="50d47-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="50d47-230">Šiuo atveju vartotojas turi naudoti funkcijas **Rodyti dimensijas** puslapio antraštėje ir įtraukti vietą bei numerio lentelę į tinklelį, esantį „FastTab“ **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="50d47-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="50d47-231">Puslapyje **Paketo rezervavimas** pasirinkite paketo eilutę **B11** ir pažymėkite **Rezervuoti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="50d47-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="50d47-232">Nėra skirtosios logikos vietų ir numerio lentelių priskyrimo automatiniam rezervavimui.</span><span class="sxs-lookup"><span data-stu-id="50d47-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="50d47-233">Kiekį galite įvesti rankiniu būdu į lauką **Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="50d47-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="50d47-234">Atkreipkite dėmesį, kad „FastTab“ **Paketo numeriai, įvykdyti šaltinio eilutei** paketas **B11** rodomas kaip **Įvykdyta**.</span><span class="sxs-lookup"><span data-stu-id="50d47-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Konkretaus paketo numerio vykdymas pardavimo užsakymo eilutei paketo rezervavimo puslapyje](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="50d47-236">Pardavimo užsakymo eilutėje nurodytas kiekis gali būti rezervuojamas per kelis paketus.</span><span class="sxs-lookup"><span data-stu-id="50d47-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="50d47-237">Taip pat galite to pačio paketo rezervavimą galima atlikti keliose vietose ir numerio lentelėse (jei yra įjungtos vietų numerio lentelės).</span><span class="sxs-lookup"><span data-stu-id="50d47-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="50d47-238">Pardavimo užsakymo eilutėje esančio kiekio konkretaus paketo rezervavimas taip pat gali būti dalinis.</span><span class="sxs-lookup"><span data-stu-id="50d47-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="50d47-239">Pavyzdžiui, visas 100 vienetų kiekis gali būti rezervuojamas tam, kad konkretus paketas būtų vykdomas 20 vnt., o 80 vienetų būtų rezervuota bet kurio turimo paketo vietoje ir sandėlio lygiuose.</span><span class="sxs-lookup"><span data-stu-id="50d47-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="50d47-240">Šiuo atveju WMS atliks išrinkimų operacijas, naudodama dvi atskiras darbo eilutes.</span><span class="sxs-lookup"><span data-stu-id="50d47-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="50d47-241">Eikite į **Produkto informacijos valdymas** \> **Produktai** \> **Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="50d47-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="50d47-242">Pažymėkite prekę ir pasirinkite **Tvarkyti atsargas** \> **Rodinys** \> **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="50d47-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Įvykdyto užsakymo rezervavimas kaip atsargų operacijų tipas](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="50d47-244">Peržiūrėkite prekės atsargų operacijas, susijusias su pardavimo užsakymo eilutės rezervavimu.</span><span class="sxs-lookup"><span data-stu-id="50d47-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="50d47-245">Operacija, kai laukas **Nuoroda** nustatytas kaip **Pardavimo užsakymas**, o laukas **Išduoti** yra nustatytas kaip **Rezervuota faktiškai** nurodo atsargų dimensijų, esančių virš lygio **Vieta**, užsakymo eilutės rezervavimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="50d47-246">Pagal prekės atsargų rezervavimo hierarchiją tos dimensijos yra vieta, sandėlis ir atsargų būsena.</span><span class="sxs-lookup"><span data-stu-id="50d47-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="50d47-247">Operacija, kai laukas **Nuoroda** nustatytas kaip **Įvykdyto užsakymo rezervavimas**, o laukas **Išduoti** yra nustatytas kaip **Rezervuota faktiškai** nurodo konkretaus paketo ir virš jo esančių visų atsargų dimensijų užsakymo eilutės rezervavimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="50d47-248">Pagal prekės atsargų rezervavimo hierarchiją tos dimensijos yra paketo numeris ir vieta.</span><span class="sxs-lookup"><span data-stu-id="50d47-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="50d47-249">Šiame pavyzdyje vieta yra **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="50d47-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="50d47-250">Pardavimo užsakymo antraštėje pasirinkite **Sandėlis** \> **Veiksmai** \> **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="50d47-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="50d47-251">Užsakymo eilutė dabar yra banguota, ir sukuriami apkrovos ir darbai.</span><span class="sxs-lookup"><span data-stu-id="50d47-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="50d47-252">Sandėlio darbo su įvykdyto užsakymo paketo numeriai peržiūra ir apdorojimas</span><span class="sxs-lookup"><span data-stu-id="50d47-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="50d47-253">„FastTab“ **Pardavimo užsakymo eilutės** pasirinkite **Sandėlis** \> **Darbo informacija**.</span><span class="sxs-lookup"><span data-stu-id="50d47-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="50d47-254">Darbas, kuris tvarko paketo kiekio, kuris yra skirtas pardavimo užsakymo eilutei, išrinkimo operaciją, pasižymi šiomis savybėmis:</span><span class="sxs-lookup"><span data-stu-id="50d47-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="50d47-255">Kad sukurtų darbą, sistema naudoja darbo šablonus, o ne vietos nurodus.</span><span class="sxs-lookup"><span data-stu-id="50d47-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="50d47-256">Visi įprasti parametrai, apibrėžti darbo šablonams, pvz., maksimalus paėmimo eilučių skaičius arba konkretus matavimo vienetas, bus taikomi siekiant nustatyti, kada turi būti sukurtas naujas darbas.</span><span class="sxs-lookup"><span data-stu-id="50d47-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="50d47-257">Tačiau į taisykles, kurios susietos su vietos nurodymais identifikuojant paėmimo vietas, nėra atsižvelgiama, nes įvykdyto užsakymo rezervavimu jau nurodoma visų atsargų dimensijos.</span><span class="sxs-lookup"><span data-stu-id="50d47-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="50d47-258">Tose atsargų dimensijose yra dimensijų sandėlio sandėliavimo lygyje.</span><span class="sxs-lookup"><span data-stu-id="50d47-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="50d47-259">Todėl darbas perima šias dimensijas ir nereikia vadovautis vietos nurodymais.</span><span class="sxs-lookup"><span data-stu-id="50d47-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="50d47-260">Paketo numeris nerodomas paėmimo eilutėje (kaip tai yra su darbo eilute, sukurta prekei, kuri yra susieta su „Batch-above\[vieta\]“ rezervavimo hierarchija). Vietoje to, paketo numeris „nuo“ ir visos kitos saugojimo dimensijos rodomi darbo eilutės darbo atsargų operacijoje, kuri nurodoma iš susietų atsargų operacijų.</span><span class="sxs-lookup"><span data-stu-id="50d47-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Sandėlio atsargų operacija darbui, kuris yra iš įvykdyto užsakymo rezervavimo](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="50d47-262">Sukūrus darbą, prekės atsargų operacija, kai laukas **Nuoroda** nustatytas kaip **Įvykdyto užsakymo rezervavimas**, pašalinama.</span><span class="sxs-lookup"><span data-stu-id="50d47-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="50d47-263">Atsargų operacija, kai laukas **Nuoroda** kaip **Darbas**, dabar turi faktinį rezervavimą visose kiekio atsargų dimensijose.</span><span class="sxs-lookup"><span data-stu-id="50d47-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="50d47-264">Sandėlio operacijos gali tęsti darbo vykdymo tvarkymą įprastu būdu.</span><span class="sxs-lookup"><span data-stu-id="50d47-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="50d47-265">Tačiau mobiliojo įrenginio instrukcijose bus nurodyta, kad darbuotojas galės pasirinkti konkretų paketo numerį.</span><span class="sxs-lookup"><span data-stu-id="50d47-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="50d47-266">Sandėlio aplinkose, kur vietos yra kontroliuojamos pagal numerio lentelę, po to, kai darbuotojas pasiekia vietą, kurioje saugomas tas pats paketas keliose numerio lentelėse, jis ar ji gali paimti bet kirią numerio lentelę, kuri dar nerezervuota (pvz., kitu įvykdyto užsakymo rezervavimu arba darbu, kilusiu iš šio tipo rezervavimo).</span><span class="sxs-lookup"><span data-stu-id="50d47-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="50d47-267">Jei paaiškėja, kad nepraktiška paimti iš vietos, nurodytos darbo eilutėje, sandėlio operatoriai gali naudoti vieną iš toliau nurodytų veiksmų, kad nukreiptų konkretaus paketo paėmimą iš patogesnės vietos:</span><span class="sxs-lookup"><span data-stu-id="50d47-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="50d47-268">Įprastas veiksmas **Nepaisyti vietos** mobiliajame įrenginyje (jei sandėlio darbuotojo parametras **Leisti nepaisyti paėmimo vietos** įjungtas)</span><span class="sxs-lookup"><span data-stu-id="50d47-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="50d47-269">Veiksmas **Keisti vietą** puslapyje **Darbų sąrašo informacija**.</span><span class="sxs-lookup"><span data-stu-id="50d47-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="50d47-270">Mobiliajame įrenginyje baikite paėmimo ir dėjimo darbą.</span><span class="sxs-lookup"><span data-stu-id="50d47-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="50d47-271">Kiekis **10**, skirtas paketo numeriui **B11**, dabar paimamas pardavimo užsakymo eilutei ir padedamas į vietą **Galinės durys**.</span><span class="sxs-lookup"><span data-stu-id="50d47-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="50d47-272">Šiuo metu, jis paruoštas būti pakrautas į sunkvežimį ir išsiųstas kliento adresu.</span><span class="sxs-lookup"><span data-stu-id="50d47-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a><span data-ttu-id="50d47-273">Sandėlio darbo išimčių tvarkymas su įvykdyto užsakymo paketo numeriais</span><span class="sxs-lookup"><span data-stu-id="50d47-273">Exception handling of warehouse work thas has order-committed batch numbers</span></span>

<span data-ttu-id="50d47-274">Sandėlio darbas, skirtas paimti įvykdyto užsakymo paketo numerius, yra vykdomas su tuo pačiu standartiniu sandėlio išimties apdorojimu i veiksmais, kaip ir įprastas darbas.</span><span class="sxs-lookup"><span data-stu-id="50d47-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="50d47-275">Paprastai atidarytą darbą arba darbo eilutę galima atšaukti, juos galima pertraukti, nes vartotojo vieta pilna, juos galima trumpai paimti, ir juos galima naujinti dėl perkėlimo.</span><span class="sxs-lookup"><span data-stu-id="50d47-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="50d47-276">Taip pat gali būti sumažintas jau atlikto darbo paimtas kiekis, arba darbas gali būti atšauktas.</span><span class="sxs-lookup"><span data-stu-id="50d47-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="50d47-277">Ši pagrindinė taisyklė taikoma visiems šiems išimties tvarkymo veiksmams: klientui rezervuotas paketo numeris negali būti pakeistas kitu paketo numeriu, bet jo saugojimo dimensijos (vieta ir numerio lentelė) gali būti pakeistos arba vartotojui rankiniu būdu atnaujinant arba sistemai automatiškai atnaujinant.</span><span class="sxs-lookup"><span data-stu-id="50d47-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="50d47-278">Automatinis naujinimas paremtas tuo pačiu atsitiktiniu sandėliavimo dimensijų priskyrimu, kuris taikomas, kai konkretus paketas buvo rezervuotas automatiškai, tačiau nenurodytos sandėliavimo dimensijos.</span><span class="sxs-lookup"><span data-stu-id="50d47-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="50d47-279">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="50d47-279">Example scenario</span></span>

<span data-ttu-id="50d47-280">Šio scenarijaus pavyzdys yra atvejis, kai anksčiau baigtas darbas yra nepaimtas naudojant funkciją **Mažinti paimtą kiekį**.</span><span class="sxs-lookup"><span data-stu-id="50d47-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="50d47-281">Šiuo pavyzdžiu tęsiamas ankstesnis šios temos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="50d47-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="50d47-282">Eikite į **Sandėlio valdymas** \> **Kroviniai** \> **Aktyvūs kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="50d47-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="50d47-283">Pasirinkite krovinį, kuris buvo sukurtas siejant su pardavimo užsakymo siunta.</span><span class="sxs-lookup"><span data-stu-id="50d47-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="50d47-284">Iš „FastTab“ **Krovinio užsakymo eilutės** pasirinkite **Mažinti paimtą kiekį**.</span><span class="sxs-lookup"><span data-stu-id="50d47-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="50d47-285">Puslapyje **Mažinti paimtą kiekį** lauke **Perkelti į vietą** pasirinkite **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="50d47-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="50d47-286">Lauke **Perkelti į numerio lentelę** pasirinkite **LP33**.</span><span class="sxs-lookup"><span data-stu-id="50d47-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="50d47-287">Tinklelyje į lauką **Atsargų kiekis, kurio paėmimo reikia atsisakyti** įveskite **10**.</span><span class="sxs-lookup"><span data-stu-id="50d47-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="50d47-288">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="50d47-288">Select **OK**.</span></span>

<span data-ttu-id="50d47-289">Čia pateikiami paėmimo atsisakymo veiksmo rezultatai:</span><span class="sxs-lookup"><span data-stu-id="50d47-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="50d47-290">Anksčiau uždaryto darbo būsena nustatyta kaip **Atšaukta**.</span><span class="sxs-lookup"><span data-stu-id="50d47-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="50d47-291">Tipo **Atsargų perkėlimas** naujas darbas sukuriamas nepaimtam kiekiui **10** paketo numeriui **B11**.</span><span class="sxs-lookup"><span data-stu-id="50d47-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="50d47-292">Šis darbas vaizduoja perkėlimą iš vietos **Galinės durys** į numerio lentelę **LP33** vietoje **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="50d47-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="50d47-293">Būseną nustatyta kaip **Uždaryta**.</span><span class="sxs-lookup"><span data-stu-id="50d47-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="50d47-294">Sistema iš naujo rezervuoja iš pradžių užsakytą paketo numerį ir priskiria vietos ir valstybinio numerio ID.</span><span class="sxs-lookup"><span data-stu-id="50d47-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="50d47-295">(Šis procesas prilygsta nurodyto paketo numerio užsakymo eilutės funkcijai **Rezervuoti eilutę**).</span><span class="sxs-lookup"><span data-stu-id="50d47-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="50d47-296">Todėl paketas **B11** rodomas, kaip įvykdytas „FastTab“ **Paketo numeriai, įvykdyti šaltinio eilutei**, puslapyje **Paketo rezervavimas** ir lauke **Rezervavimas** nurodytas kiekis **10**, skirto paketo numeriui **B11**.</span><span class="sxs-lookup"><span data-stu-id="50d47-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="50d47-297">Be to, laukas **Vieta** nustatytas kaip **FL-001**, o laukas **Numerio lentelė** nustatytas kaip **LP11**.</span><span class="sxs-lookup"><span data-stu-id="50d47-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="50d47-298">(Jei jų nematote, šiuos laukus galima įtraukti į tinklelį.)</span><span class="sxs-lookup"><span data-stu-id="50d47-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="50d47-299">Toliau esančiose lentelėse pateikiama apžvalga, nurodanti, kaip sistema apdoroja konkrečių sandėlio veiksmų įvykdyto užsakymo paketo rezervavimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="50d47-300">Norėdami suprasti lentelių turinį, Įsivaizduokite, kad kiekvienas sandėlio veiksmas yra vykdomas esamo sandėlio darbo, kilusio iš įvykdyto užsakymo paketo rezervavimo, kontekste, ar kiekvieno sandėlio veiksmo vykdymas turi įtakos to tipo darbui.</span><span class="sxs-lookup"><span data-stu-id="50d47-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="50d47-301">Šiose lentelėse stulpelyje „Paketo kiekis pasiekiamas“ rodoma, ar yra pasiekiamas paketo kiekis, be kiekio, kuris jau rezervuotas dabartiniam įvykdyto užsakymo rezervavimams, arba jau rezervuotas pagal sandėlio darbą, kuris gaunamas iš to tipo rezervavimų.</span><span class="sxs-lookup"><span data-stu-id="50d47-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="50d47-302">Paėmimo vietos perrašymas atidarytame darbe</span><span class="sxs-lookup"><span data-stu-id="50d47-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="50d47-303">Pagrindinis sąrankos parametras</span><span class="sxs-lookup"><span data-stu-id="50d47-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="50d47-304">Paketo kiekis pasiekiamas</span><span class="sxs-lookup"><span data-stu-id="50d47-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="50d47-305">Pagrindiniai vartotojo veiksmai</span><span class="sxs-lookup"><span data-stu-id="50d47-305">Key user steps</span></span></th>
<th><span data-ttu-id="50d47-306">Sandėlio darbas</span><span class="sxs-lookup"><span data-stu-id="50d47-306">Warehouse work</span></span></th>
<th><span data-ttu-id="50d47-307">Įvykdyto užsakymo paketo rezervavimas</span><span class="sxs-lookup"><span data-stu-id="50d47-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="50d47-308">Parinktis <strong>Leisti nepaisyti paėmimo vietos</strong> darbininkui yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="50d47-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="50d47-309">Taip</span><span class="sxs-lookup"><span data-stu-id="50d47-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-310">Pasirinkite meniu elementą <strong>Nepaisyti vietos</strong>, esantį sandėliavimo programoje, paleidę paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="50d47-310">Select the <strong>Override location</strong> menu item on the warehousing app when you start picking work.</span></span></li>
<li><span data-ttu-id="50d47-311">Pasirinkite <strong>Siūlyti</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="50d47-312">Patvirtinkite naują vietą, kuri siūloma pagal paketo kiekio pasiekiamumą.</span><span class="sxs-lookup"><span data-stu-id="50d47-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="50d47-313">Dabartiniam darbui atsiranda šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="50d47-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="50d47-314">Vieta paėmimo eilutėje atnaujinama į naują vietą.</span><span class="sxs-lookup"><span data-stu-id="50d47-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="50d47-315">(Jei vieta yra kontroliuojama pagal numerio lentelę, atsitiktinė numerio lentelė priskiriama darbo atsargų operacijai, o darbuotojas gali rinktis iš bet kurios turimos numerio lentelės, kurios kiekis yra pasiekiamas.)</span><span class="sxs-lookup"><span data-stu-id="50d47-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="50d47-316">Jei naujoje vietoje yra daugiau nei viena numerio lentelė, pradinė paėmimo eilutė padalijama į kelias eilutes, kad atitiktų kiekvieną numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="50d47-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="50d47-317">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="50d47-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-318">nr.</span><span class="sxs-lookup"><span data-stu-id="50d47-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-319">Pasirinkite meniu elementą <strong>Nepaisyti vietos</strong>, esantį sandėliavimo programoje, paleidę paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="50d47-319">Select the <strong>Override location</strong> menu item on the warehousing app when you start picking work.</span></span></li>
<li><span data-ttu-id="50d47-320">Įveskite vietą rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="50d47-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="50d47-321">Veiksmas <strong>Nepaisyti vietos</strong> nėra galimas.</span><span class="sxs-lookup"><span data-stu-id="50d47-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="50d47-322">Jis nepavyksta ir rodoma klaida.</span><span class="sxs-lookup"><span data-stu-id="50d47-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="50d47-323">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="50d47-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="50d47-324">Visas mygtukas – skaidykite darbo eilutę dėl perpildos vartotojo vietoje</span><span class="sxs-lookup"><span data-stu-id="50d47-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="50d47-325">Pagrindinis sąrankos parametras</span><span class="sxs-lookup"><span data-stu-id="50d47-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="50d47-326">Paketo kiekis pasiekiamas</span><span class="sxs-lookup"><span data-stu-id="50d47-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="50d47-327">Pagrindiniai vartotojo veiksmai</span><span class="sxs-lookup"><span data-stu-id="50d47-327">Key user steps</span></span></th>
<th><span data-ttu-id="50d47-328">Sandėlio darbas</span><span class="sxs-lookup"><span data-stu-id="50d47-328">Warehouse work</span></span></th>
<th><span data-ttu-id="50d47-329">Įvykdyto užsakymo paketo rezervavimas</span><span class="sxs-lookup"><span data-stu-id="50d47-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="50d47-330">Parinktis <strong>Leisti skaidyti darbą</strong> įjungta mobiliojo įrenginio meniu elemente.</span><span class="sxs-lookup"><span data-stu-id="50d47-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="50d47-331">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="50d47-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-332">Pasirinkite meniu elementą <strong>Visas</strong>, esantį sandėliavimo programoje, apdoroję paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="50d47-332">Select the <strong>Full</strong> menu item on the warehousing app when you process picking work.</span></span></li>
<li><span data-ttu-id="50d47-333">Lauke <strong>Paimtas kiekis</strong> įveskite reikiamo paėmimo dalinį kiekį, kad nurodytumėte visą pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="50d47-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="50d47-334">Dabartiniame darbe kiekis atnaujinamas iki likusio kiekio, kuris turi būti paimtas.</span><span class="sxs-lookup"><span data-stu-id="50d47-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="50d47-335">Sukuriamas ir uždaromas naujas paimto kiekio darbas.</span><span class="sxs-lookup"><span data-stu-id="50d47-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="50d47-336">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="50d47-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="50d47-337">Baigto darbo paimto kiekio mažinimas (iš krovinio)</span><span class="sxs-lookup"><span data-stu-id="50d47-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="50d47-338">Pagrindinis sąrankos parametras</span><span class="sxs-lookup"><span data-stu-id="50d47-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="50d47-339">Paketo kiekis pasiekiamas</span><span class="sxs-lookup"><span data-stu-id="50d47-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="50d47-340">Pagrindiniai vartotojo veiksmai</span><span class="sxs-lookup"><span data-stu-id="50d47-340">Key user steps</span></span></th>
<th><span data-ttu-id="50d47-341">Sandėlio darbas</span><span class="sxs-lookup"><span data-stu-id="50d47-341">Warehouse work</span></span></th>
<th><span data-ttu-id="50d47-342">Įvykdyto užsakymo paketo rezervavimas</span><span class="sxs-lookup"><span data-stu-id="50d47-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="50d47-343">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="50d47-343">Not applicable</span></span></td>
<td><span data-ttu-id="50d47-344">Taip</span><span class="sxs-lookup"><span data-stu-id="50d47-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-345">Krovinio eilutėje atidarykite puslapį <strong>Sumažinti paimtą kiekį</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="50d47-346">Įveskite visą kiekį, kad panaikintumėte paėmimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="50d47-347">Pasirinkite „perkelti į“ vietą / numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="50d47-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="50d47-348">Su krovinio eilute susietas darbas atšaukiamas.</span><span class="sxs-lookup"><span data-stu-id="50d47-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="50d47-349">Sukuriamas ir uždaromas naujas atsargų perkėlimo darbas.</span><span class="sxs-lookup"><span data-stu-id="50d47-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="50d47-350">Kiekis dar kartą rezervuojamas tam pačiam paketui.</span><span class="sxs-lookup"><span data-stu-id="50d47-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="50d47-351">Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="50d47-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-352">Ne</span><span class="sxs-lookup"><span data-stu-id="50d47-352">No</span></span></td>
<td><span data-ttu-id="50d47-353">Peržiūrėkite ankstesnę eilutę.</span><span class="sxs-lookup"><span data-stu-id="50d47-353">See the previous row.</span></span></td>
<td><span data-ttu-id="50d47-354">Peržiūrėkite ankstesnę eilutę.</span><span class="sxs-lookup"><span data-stu-id="50d47-354">See the previous row.</span></span></td>
<td><span data-ttu-id="50d47-355">Kiekis yra dar kartą rezervuojamas tam pačiam paketui ir tai pačiai vietai bei numerio lentelei (jei vieta yra kontroliuojama pagal numerio lentelę), kurios buvo įvestos atšaukiant paėmimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="50d47-356">Sandėlyje esančios prekės perkėlimas</span><span class="sxs-lookup"><span data-stu-id="50d47-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="50d47-357">Šis sandėlio veiksmas taikomas tik **Darbo kūrimo procesas** tipo perkėlimui, o neperkėlimui pagal šabloną.</span><span class="sxs-lookup"><span data-stu-id="50d47-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="50d47-358">Pagrindinis sąrankos parametras</span><span class="sxs-lookup"><span data-stu-id="50d47-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="50d47-359">Paketo kiekis pasiekiamas</span><span class="sxs-lookup"><span data-stu-id="50d47-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="50d47-360">Pagrindiniai vartotojo veiksmai</span><span class="sxs-lookup"><span data-stu-id="50d47-360">Key user steps</span></span></th>
<th><span data-ttu-id="50d47-361">Sandėlio darbas</span><span class="sxs-lookup"><span data-stu-id="50d47-361">Warehouse work</span></span></th>
<th><span data-ttu-id="50d47-362">Įvykdyto užsakymo paketo rezervavimas</span><span class="sxs-lookup"><span data-stu-id="50d47-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="50d47-363">Parinktis <strong>Leisti perkelti atsargas su susijusiu darbu</strong> darbuotojui įjungiama.</span><span class="sxs-lookup"><span data-stu-id="50d47-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="50d47-364">Taip</span><span class="sxs-lookup"><span data-stu-id="50d47-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-365">Sandėliavimo programoje pradėkite perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-365">Start a movement on the warehousing app.</span></span></li>
<li><span data-ttu-id="50d47-366">Įveskite „iš“ ir „į“ vietas.</span><span class="sxs-lookup"><span data-stu-id="50d47-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="50d47-367">Visuose esamuose darbuose, paveiktuose perkėlimo, paėmimo vieta atnaujinama į naują vietą „į“.</span><span class="sxs-lookup"><span data-stu-id="50d47-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="50d47-368">Sukuriamas ir uždaromas naujas atsargų perkėlimo darbas.</span><span class="sxs-lookup"><span data-stu-id="50d47-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="50d47-369">Visi esami rezervavimai, kuriuos paveikė kiekio perkėlimas iš tam tikros vietos, yra rezervuojami iš naujo tam pačiam paketui.</span><span class="sxs-lookup"><span data-stu-id="50d47-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="50d47-370">Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="50d47-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-371">Ne</span><span class="sxs-lookup"><span data-stu-id="50d47-371">No</span></span></td>
<td><span data-ttu-id="50d47-372">Peržiūrėkite ankstesnę eilutę.</span><span class="sxs-lookup"><span data-stu-id="50d47-372">See the previous row.</span></span></td>
<td><span data-ttu-id="50d47-373">Peržiūrėkite ankstesnę eilutę.</span><span class="sxs-lookup"><span data-stu-id="50d47-373">See the previous row.</span></span></td>
<td><span data-ttu-id="50d47-374">Visi esami rezervavimai, kuriuos paveikė kiekio perkėlimas iš tam tikros vietos, yra rezervuojami iš naujo tam pačiam paketui ir naujai vietai „į“ bei numerio lentelei (jei vieta yra kontroliuojama pagal numerio lentelę).</span><span class="sxs-lookup"><span data-stu-id="50d47-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="50d47-375">Baigto darbo paimto kiekio atšaukimas (iš krovinio arba bangos)</span><span class="sxs-lookup"><span data-stu-id="50d47-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="50d47-376">Pagrindinis sąrankos parametras</span><span class="sxs-lookup"><span data-stu-id="50d47-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="50d47-377">Paketo kiekis pasiekiamas</span><span class="sxs-lookup"><span data-stu-id="50d47-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="50d47-378">Pagrindiniai vartotojo veiksmai</span><span class="sxs-lookup"><span data-stu-id="50d47-378">Key user steps</span></span></th>
<th><span data-ttu-id="50d47-379">Sandėlio darbas</span><span class="sxs-lookup"><span data-stu-id="50d47-379">Warehouse work</span></span></th>
<th><span data-ttu-id="50d47-380">Įvykdyto užsakymo paketo rezervavimas</span><span class="sxs-lookup"><span data-stu-id="50d47-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="50d47-381">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="50d47-381">Not applicable</span></span></td>
<td><span data-ttu-id="50d47-382">Taip</span><span class="sxs-lookup"><span data-stu-id="50d47-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-383">Atidarykite puslapį <strong>Atšaukti darbą</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="50d47-384">Užklausos puslapyje pasirinkite parinktį <strong>Palikti prekes dabartinėje vietoje</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="50d47-385">Su kroviniu susietas visas darbas atšaukiamas.</span><span class="sxs-lookup"><span data-stu-id="50d47-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="50d47-386">Kiekis dar kartą rezervuojamas tam pačiam paketui.</span><span class="sxs-lookup"><span data-stu-id="50d47-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="50d47-387">Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="50d47-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-388">Ne</span><span class="sxs-lookup"><span data-stu-id="50d47-388">No</span></span></td>
<td><span data-ttu-id="50d47-389">Peržiūrėkite ankstesnę eilutę.</span><span class="sxs-lookup"><span data-stu-id="50d47-389">See the previous row.</span></span></td>
<td><span data-ttu-id="50d47-390">Peržiūrėkite ankstesnę eilutę.</span><span class="sxs-lookup"><span data-stu-id="50d47-390">See the previous row.</span></span></td>
<td><span data-ttu-id="50d47-391">Kiekis yra dar kartą rezervuojamas tam pačiam paketui ir vietai bei numerio lentelei, kai kiekis buvo paliktas atšaukiant.</span><span class="sxs-lookup"><span data-stu-id="50d47-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-392">Taip</span><span class="sxs-lookup"><span data-stu-id="50d47-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-393">Atidarykite puslapį <strong>Atšaukti darbą</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="50d47-394">Užklausos puslapyje pasirinkite parinktį <strong>Priskirti prekes šiai vietai</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="50d47-395">Dabartinis darbas atšauktas.</span><span class="sxs-lookup"><span data-stu-id="50d47-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="50d47-396">Sukuriamas ir uždaromas naujas atsargų perkėlimo darbas.</span><span class="sxs-lookup"><span data-stu-id="50d47-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="50d47-397">Kiekis dar kartą rezervuojamas tam pačiam paketui.</span><span class="sxs-lookup"><span data-stu-id="50d47-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="50d47-398">Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="50d47-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-399">Ne</span><span class="sxs-lookup"><span data-stu-id="50d47-399">No</span></span></td>
<td><span data-ttu-id="50d47-400">Peržiūrėkite ankstesnę eilutę.</span><span class="sxs-lookup"><span data-stu-id="50d47-400">See the previous row.</span></span></td>
<td><span data-ttu-id="50d47-401">Peržiūrėkite ankstesnę eilutę.</span><span class="sxs-lookup"><span data-stu-id="50d47-401">See the previous row.</span></span></td>
<td><span data-ttu-id="50d47-402">Kiekis yra dar kartą rezervuojamas tam pačiam paketui ir vietai bei numerio lentelei, kurioms kiekis buvo priskirtas atšaukiant.</span><span class="sxs-lookup"><span data-stu-id="50d47-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-403">Taip/ne</span><span class="sxs-lookup"><span data-stu-id="50d47-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-404">Atidarykite puslapį <strong>Atšaukti darbą</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="50d47-405">Užklausos puslapyje pasirinkite parinktį <strong>Perkelti elementus į šią vietą</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="50d47-406">Atšaukimas nėra palaikomas.</span><span class="sxs-lookup"><span data-stu-id="50d47-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="50d47-407">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="50d47-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-408">Taip/ne</span><span class="sxs-lookup"><span data-stu-id="50d47-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-409">Atidarykite puslapį <strong>Atšaukti darbą</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="50d47-410">Užklausos puslapyje pasirinkite parinktį <strong>Perkelti prekes, atsižvelgiant į vietos nurodymus</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="50d47-411">Atšaukimas nėra palaikomas.</span><span class="sxs-lookup"><span data-stu-id="50d47-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="50d47-412">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="50d47-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="50d47-413">Nevisiškai paimkite kiekį – užregistruokite kiekį, kuris fiziškai nerastas vietoje / numerio lentelėje, kol atliekate paėmimo darbą</span><span class="sxs-lookup"><span data-stu-id="50d47-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="50d47-414">Pagrindinis sąrankos parametras</span><span class="sxs-lookup"><span data-stu-id="50d47-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="50d47-415">Paketo kiekis pasiekiamas</span><span class="sxs-lookup"><span data-stu-id="50d47-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="50d47-416">Pagrindiniai vartotojo veiksmai</span><span class="sxs-lookup"><span data-stu-id="50d47-416">Key user steps</span></span></th>
<th><span data-ttu-id="50d47-417">Sandėlio darbas</span><span class="sxs-lookup"><span data-stu-id="50d47-417">Warehouse work</span></span></th>
<th><span data-ttu-id="50d47-418">Įvykdyto užsakymo paketo rezervavimas</span><span class="sxs-lookup"><span data-stu-id="50d47-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="50d47-419">Tipo <strong>Nevisiškai paimta</strong> darbo išimtis nustatyta, kai <strong>Prekių perskirstymas</strong> = <strong>Nėra</strong>, <strong>Atsargų koregavimas</strong> = <strong>Taip</strong> ir <strong>Pašalinti rezervavimus</strong> = <strong>Ne</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="50d47-420">Taip</span><span class="sxs-lookup"><span data-stu-id="50d47-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-421">Pasirinkite meniu elementą <strong>Nevisiškai paimta</strong>, esantį sandėliavimo programoje, paleidę paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="50d47-421">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="50d47-422">Lauke <strong>Paimti kiekį</strong> įveskite <strong>0</strong> (nulį).</span><span class="sxs-lookup"><span data-stu-id="50d47-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="50d47-423">Lauke <strong>Priežastis</strong> įveskite <strong>Perskirstymo nėra</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="50d47-424">Dabartinis darbas uždaromas, o paimtas kiekis yra 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="50d47-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="50d47-425">Tipo <strong>Inventorizacija</strong> atsargų operacija ir <strong>Parduota</strong> išdavimo tipas, yra sukuriami, kad būtų galima nurodyti koregavimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="50d47-426">Kiekis dar kartą rezervuojamas tam pačiam paketui.</span><span class="sxs-lookup"><span data-stu-id="50d47-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="50d47-427">Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="50d47-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-428">Ne</span><span class="sxs-lookup"><span data-stu-id="50d47-428">No</span></span></td>
<td><span data-ttu-id="50d47-429">Peržiūrėkite ankstesnę eilutę.</span><span class="sxs-lookup"><span data-stu-id="50d47-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="50d47-430">Trumpo paėmimo veiksmas nepavyksta ir rodoma klaida.</span><span class="sxs-lookup"><span data-stu-id="50d47-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="50d47-431">Dabartinis darbas tebeatidarytas.</span><span class="sxs-lookup"><span data-stu-id="50d47-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="50d47-432">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="50d47-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="50d47-433">Tipo <strong>Nevisiškai paimta</strong> darbo išimtis nustatyta, kai <strong>Prekių perskirstymas</strong> = <strong>Nėra</strong>, <strong>Atsargų koregavimas</strong> = <strong>Taip</strong> ir <strong>Pašalinti rezervavimus</strong> = <strong>Taip</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="50d47-434">Taip</span><span class="sxs-lookup"><span data-stu-id="50d47-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-435">Pasirinkite meniu elementą <strong>Nevisiškai paimta</strong>, esantį sandėliavimo programoje, paleidę paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="50d47-435">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="50d47-436">Lauke <strong>Paimti kiekį</strong> įveskite <strong>0</strong> (nulį).</span><span class="sxs-lookup"><span data-stu-id="50d47-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="50d47-437">Lauke <strong>Priežastis</strong> įveskite <strong>Perskirstymo nėra</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="50d47-438">Dabartinis darbas uždaromas, o paimtas kiekis yra 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="50d47-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="50d47-439">Tipo <strong>Inventorizacija</strong> atsargų operacija ir <strong>Parduota</strong> išdavimo tipas, yra sukuriami, kad būtų galima nurodyti koregavimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="50d47-440">Visi esami rezervavimai, kuriuos paveikė kiekio koregavimas iš trumpo paėmimo vietos, yra rezervuojami iš naujo tam pačiam paketui.</span><span class="sxs-lookup"><span data-stu-id="50d47-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="50d47-441">Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="50d47-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-442">Ne</span><span class="sxs-lookup"><span data-stu-id="50d47-442">No</span></span></td>
<td><span data-ttu-id="50d47-443">Peržiūrėkite ankstesnę eilutę.</span><span class="sxs-lookup"><span data-stu-id="50d47-443">See the previous row.</span></span></td>
<td><span data-ttu-id="50d47-444">Peržiūrėkite ankstesnę eilutę.</span><span class="sxs-lookup"><span data-stu-id="50d47-444">See the previous row.</span></span></td>
<td><span data-ttu-id="50d47-445">Visi esami rezervavimai, kuriuos paveikė kiekio koregavimas iš trumpo paėmimo vietos, yra pašalinami.</span><span class="sxs-lookup"><span data-stu-id="50d47-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-446">Tipo <strong>Nevisiškai paimta</strong> darbo išimtis nustatyta, kai <strong>Prekių perskirstymas</strong> = <strong>Neautomatinis</strong>, <strong>Atsargų koregavimas</strong> = <strong>Taip</strong> ir <strong>Pašalinti rezervavimus</strong> = <strong>Ne / Taip</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="50d47-447">Be to, parinktis <strong>Leisti neautomatinį prekių perskirstymą</strong> darbuotojui yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="50d47-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="50d47-448">Taip</span><span class="sxs-lookup"><span data-stu-id="50d47-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-449">Pasirinkite meniu elementą <strong>Nevisiškai paimta</strong>, esantį sandėliavimo programoje, paleidę paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="50d47-449">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="50d47-450">Lauke <strong>Trumpai paimti kiekį</strong> įveskite <strong>0</strong> (nulį).</span><span class="sxs-lookup"><span data-stu-id="50d47-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="50d47-451">Lauke <strong>Priežastis</strong> pasirinkite <strong>Trumpas paėmimas su neautomatiniu perskirstymu iš naujo</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="50d47-452">Sąraše pasirinkite vietą / numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="50d47-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="50d47-453">Dabartiniam darbui atsiranda šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="50d47-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="50d47-454">Paėmimo eilutė uždaroma, o paimtas kiekis yra 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="50d47-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="50d47-455">Padėjimo eilutė atšaukiama.</span><span class="sxs-lookup"><span data-stu-id="50d47-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="50d47-456">Sukuriama nauja paėmimo eilutė.</span><span class="sxs-lookup"><span data-stu-id="50d47-456">A new pick line is created.</span></span> <span data-ttu-id="50d47-457">Ji naudoja vietą / numerio lentelę, kurią pasirinko vartotojas.</span><span class="sxs-lookup"><span data-stu-id="50d47-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="50d47-458">Sukuriama nauja padėjimo eilutė.</span><span class="sxs-lookup"><span data-stu-id="50d47-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="50d47-459">Tipo <strong>Inventorizacija</strong> atsargų operacija ir <strong>Parduota</strong> išdavimo tipas, yra sukuriami, kad būtų galima nurodyti koregavimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="50d47-460">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="50d47-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-461">Tipo <strong>Nevisiškai paimta</strong> darbo išimtis nustatyta, kai <strong>Prekių perskirstymas</strong> = <strong>Neautomatinis</strong>, <strong>Atsargų koregavimas</strong> = <strong>Taip</strong> ir <strong>Pašalinti rezervavimus</strong> = <strong>Ne</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="50d47-462">Be to, parinktis <strong>Leisti neautomatinį prekių perskirstymą</strong> darbuotojui yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="50d47-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="50d47-463">nr.</span><span class="sxs-lookup"><span data-stu-id="50d47-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-464">Pasirinkite meniu elementą <strong>Nevisiškai paimta</strong>, esantį sandėliavimo programoje, paleidę paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="50d47-464">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="50d47-465">Lauke <strong>Trumpai paimti kiekį</strong> įveskite <strong>0</strong> (nulį).</span><span class="sxs-lookup"><span data-stu-id="50d47-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="50d47-466">Lauke <strong>Priežastis</strong> pasirinkite <strong>Trumpas paėmimas su neautomatiniu perskirstymu iš naujo</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="50d47-467">Trumpo paėmimo veiksmas nepavyksta ir rodoma klaida.</span><span class="sxs-lookup"><span data-stu-id="50d47-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="50d47-468">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="50d47-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-469">Tipo <strong>Nevisiškai paimta</strong> darbo išimtis nustatyta, kai <strong>Prekių perskirstymas</strong> = <strong>Neautomatinis</strong>, <strong>Atsargų koregavimas</strong> = <strong>Taip</strong> ir <strong>Pašalinti rezervavimus</strong> = <strong>Taip</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="50d47-470">Be to, parinktis <strong>Leisti neautomatinį prekių perskirstymą</strong> darbuotojui yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="50d47-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="50d47-471">nr.</span><span class="sxs-lookup"><span data-stu-id="50d47-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-472">Pasirinkite meniu elementą <strong>Nevisiškai paimta</strong>, esantį sandėliavimo programoje, paleidę paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="50d47-472">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="50d47-473">Lauke <strong>Trumpai paimti kiekį</strong> įveskite <strong>0</strong> (nulį).</span><span class="sxs-lookup"><span data-stu-id="50d47-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="50d47-474">Lauke <strong>Priežastis</strong> pasirinkite <strong>Trumpas paėmimas su neautomatiniu perskirstymu iš naujo</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="50d47-475">Sąraše pasirinkite vietą / numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="50d47-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="50d47-476">Dabartiniam darbui atsiranda šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="50d47-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="50d47-477">Paėmimo eilutė uždaroma, o paimtas kiekis yra 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="50d47-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="50d47-478">Padėjimo eilutė atšaukiama.</span><span class="sxs-lookup"><span data-stu-id="50d47-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="50d47-479">Tipo <strong>Inventorizacija</strong> atsargų operacija ir <strong>Parduota</strong> išdavimo tipas, yra sukuriami, kad būtų galima nurodyti koregavimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="50d47-480">Visi esami rezervavimai, kuriuos paveikė kiekio koregavimas, iš trumpo paėmimo vietos numerio lentelės yra pašalinami.</span><span class="sxs-lookup"><span data-stu-id="50d47-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-481">Tipo <strong>Nevisiškai paimta</strong> darbo išimtis nustatyta, kai <strong>Prekių perskirstymas</strong> = <strong>Automatinis</strong>, <strong>Atsargų koregavimas</strong> = <strong>Taip / Ne</strong> ir <strong>Pašalinti rezervavimus</strong> = <strong>Taip / Ne</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="50d47-482">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="50d47-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-483">Pasirinkite meniu elementą <strong>Nevisiškai paimta</strong>, esantį sandėliavimo programoje, paleidę paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="50d47-483">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="50d47-484">Lauke <strong>Trumpai paimti kiekį</strong> įveskite <strong>0</strong> (nulį).</span><span class="sxs-lookup"><span data-stu-id="50d47-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="50d47-485">Lauke <strong>Priežastis</strong> pasirinkite <strong>Trumpas paėmimas su automatiniu perskirstymu iš naujo</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="50d47-486">Trumpas paėmimas, kuris apima automatinį priskyrimą iš naujo, nepalaikomas.</span><span class="sxs-lookup"><span data-stu-id="50d47-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="50d47-487">Trumpas paėmimas, kuris apima automatinį priskyrimą iš naujo, nepalaikomas.</span><span class="sxs-lookup"><span data-stu-id="50d47-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="50d47-488">Keisti atsargų būseną</span><span class="sxs-lookup"><span data-stu-id="50d47-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="50d47-489">Šį sandėlio veiksmą galima vykdyti iš kelių įvesties vietų.</span><span class="sxs-lookup"><span data-stu-id="50d47-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="50d47-490">Čia rodomas pavyzdys naudoja veiksmą **Atsargų būsenos keitimas** puslapyje **Turimos atsargos pagal vietą**.</span><span class="sxs-lookup"><span data-stu-id="50d47-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="50d47-491">Pagrindinis sąrankos parametras</span><span class="sxs-lookup"><span data-stu-id="50d47-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="50d47-492">Paketo kiekis pasiekiamas</span><span class="sxs-lookup"><span data-stu-id="50d47-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="50d47-493">Pagrindiniai vartotojo veiksmai</span><span class="sxs-lookup"><span data-stu-id="50d47-493">Key user steps</span></span></th>
<th><span data-ttu-id="50d47-494">Sandėlio darbas</span><span class="sxs-lookup"><span data-stu-id="50d47-494">Warehouse work</span></span></th>
<th><span data-ttu-id="50d47-495">Įvykdyto užsakymo paketo rezervavimas</span><span class="sxs-lookup"><span data-stu-id="50d47-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="50d47-496">Skirtuke <strong>Sandėlis</strong>, įraše <strong>Sandėlis</strong>, laukas <strong>Pašalinti rezervavimus ir žymėjimus</strong> yra nustatytas kaip <strong>Rezervavimai</strong> arba <strong>Žymėjimai ir rezervacijos</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="50d47-497">Taip</span><span class="sxs-lookup"><span data-stu-id="50d47-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-498">Pasirinkti konkrečią vietą.</span><span class="sxs-lookup"><span data-stu-id="50d47-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="50d47-499">Pasirinkite eilutę, kurioje yra konkreti prekė, vieta ir numerio lentelė (jei vieta yra kontroliuojama pagal numerio lentelę).</span><span class="sxs-lookup"><span data-stu-id="50d47-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="50d47-500">Pasirinkite <strong>Atsargų būsenos keitimas</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="50d47-501">Nustatyti lauką <strong>Atsargų būsena</strong> į <strong>Blokavimas</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="50d47-502">Atsargų būsenos keitimai neleidžiami kiekiams, kurie rezervuoti darbams.</span><span class="sxs-lookup"><span data-stu-id="50d47-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="50d47-503">Kiekis dar kartą rezervuojamas tam pačiam paketui.</span><span class="sxs-lookup"><span data-stu-id="50d47-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="50d47-504">Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="50d47-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="50d47-505">Yra sukuriamos dvi tipo <strong>Atsargų būsenos keitimas</strong> atsargų operacijos, kurios rodo atsargų būsenos dimensijos pokytį.</span><span class="sxs-lookup"><span data-stu-id="50d47-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="50d47-506">Tipo <strong>Atsargų blokavimas</strong> ir išleidimo tipo <strong>Rezervuota faktiškai</strong> atsargų operacija yra sukurta, kad būtų galima nurodyti užblokuoto kiekio rezervavimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="50d47-507">Ne</span><span class="sxs-lookup"><span data-stu-id="50d47-507">No</span></span></td>
<td><span data-ttu-id="50d47-508">Peržiūrėkite ankstesnę eilutę.</span><span class="sxs-lookup"><span data-stu-id="50d47-508">See the previous row.</span></span></td>
<td><span data-ttu-id="50d47-509">Atsargų būsenos keitimai neleidžiami kiekiams, kurie rezervuoti darbams.</span><span class="sxs-lookup"><span data-stu-id="50d47-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="50d47-510">Rezervavimas pašalinamas.</span><span class="sxs-lookup"><span data-stu-id="50d47-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="50d47-511">Yra sukuriamos dvi tipo <strong>Atsargų būsenos keitimas</strong> atsargų operacijos, kurios rodo atsargų būsenos dimensijos pokytį.</span><span class="sxs-lookup"><span data-stu-id="50d47-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="50d47-512">Tipo <strong>Atsargų blokavimas</strong> ir išleidimo tipo <strong>Rezervuota faktiškai</strong> atsargų operacija yra sukurta, kad būtų galima nurodyti užblokuoto kiekio rezervavimą.</span><span class="sxs-lookup"><span data-stu-id="50d47-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="50d47-513">Skirtuke <strong>Sandėlis</strong>, įraše <strong>Sandėlis</strong>, laukas <strong>Pašalinti rezervavimus ir žymėjimus</strong> yra nustatytas kaip <strong>Nėra</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="50d47-514">Taip</span><span class="sxs-lookup"><span data-stu-id="50d47-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="50d47-515">Pasirinkti konkrečią vietą.</span><span class="sxs-lookup"><span data-stu-id="50d47-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="50d47-516">Pasirinkite eilutę, kurioje yra konkreti prekė, vieta ir numerio lentelė (jei vieta yra kontroliuojama pagal numerio lentelę).</span><span class="sxs-lookup"><span data-stu-id="50d47-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="50d47-517">Pasirinkite <strong>Atsargų būsenos keitimas</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="50d47-518">Nustatyti lauką <strong>Atsargų būsena</strong> į <strong>Blokavimas</strong>.</span><span class="sxs-lookup"><span data-stu-id="50d47-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="50d47-519">Atsargų būsenos keitimai neleidžiami kiekiams, kurie rezervuoti darbams.</span><span class="sxs-lookup"><span data-stu-id="50d47-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="50d47-520">Kiekis dar kartą rezervuojamas tam pačiam paketui.</span><span class="sxs-lookup"><span data-stu-id="50d47-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="50d47-521">Sistema atsitiktine tvarka priskiria vietą ir numerio lentelę (jei vieta yra kontroliuojama pagal numerio lentelę), kurioje yra kiekis yra pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="50d47-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="50d47-522">Ne</span><span class="sxs-lookup"><span data-stu-id="50d47-522">No</span></span></td>
<td><span data-ttu-id="50d47-523">Peržiūrėkite ankstesnę eilutę.</span><span class="sxs-lookup"><span data-stu-id="50d47-523">See the previous row.</span></span></td>
<td><span data-ttu-id="50d47-524">Atsargų būsenos keitimai neleidžiami kiekiams, kurie rezervuoti darbams.</span><span class="sxs-lookup"><span data-stu-id="50d47-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="50d47-525">Atsargų būsenos keitimai neleidžiami.</span><span class="sxs-lookup"><span data-stu-id="50d47-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="50d47-526">Apribojimai</span><span class="sxs-lookup"><span data-stu-id="50d47-526">Limitations</span></span>

- <span data-ttu-id="50d47-527">Pritaikomų sandėlio lygio dimensijų rezervavimo funkcija nepalaiko šių funkcijų:</span><span class="sxs-lookup"><span data-stu-id="50d47-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="50d47-528">Esamo svorio valdymas</span><span class="sxs-lookup"><span data-stu-id="50d47-528">Catch weight management</span></span>
    - <span data-ttu-id="50d47-529">Faktinės neigiamos atsargos</span><span class="sxs-lookup"><span data-stu-id="50d47-529">Physical negative inventory</span></span>
    - <span data-ttu-id="50d47-530">Rezervavimas pagal užsakytą tiekimą</span><span class="sxs-lookup"><span data-stu-id="50d47-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="50d47-531">Perkėlimo užsakymai ir žaliavų paėmimas</span><span class="sxs-lookup"><span data-stu-id="50d47-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="50d47-532">Konteinerių konsolidavimo taisyklė, taikoma pakuotei pagal nurodomąjį vienetą, turi trūkumų.</span><span class="sxs-lookup"><span data-stu-id="50d47-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="50d47-533">Įvykdyto užsakymo rezervavimams rekomenduojame nenaudoti konteinerio kūrimo šablonų, kai laukas **Pakuoti pagal nurodomąjį vienetą** yra įjungtas.</span><span class="sxs-lookup"><span data-stu-id="50d47-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="50d47-534">Dabartiniame kūrimo įrankyje vietos nurodymai nenaudojami, kai sukuriamas sandėlio darbas.</span><span class="sxs-lookup"><span data-stu-id="50d47-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="50d47-535">Todėl per krovimo į konteinerius bangos veiksmą taikoma tik mažiausia vienetų sekų grupė (atsargų vienetas).</span><span class="sxs-lookup"><span data-stu-id="50d47-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
