--- 
title: "Peržiūrėti taikytinas kainas ir nuolaidas"
description: "Ši procedūra nurodo, kaip rasti produkto kainą ir (arba) nuolaidą, kuri šiuo metu taikoma konkrečiam klientui, nesukuriant pardavimo užsakymo."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f372db3d2e358cde6a5e65b01f4dc499c69fe022
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="303eb-103">Peržiūrėti taikytinas kainas ir nuolaidas</span><span class="sxs-lookup"><span data-stu-id="303eb-103">Look up applicable prices and discounts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="303eb-104">Ši procedūra nurodo, kaip rasti produkto kainą ir (arba) nuolaidą, kuri šiuo metu taikoma konkrečiam klientui, nesukuriant pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="303eb-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="303eb-105">Procedūra žingsnis po žingsnio apžvelgia konkretų pavyzdį, kuriuo jums reikės vadovautis naudojant demonstracinę įmonę USMF, kad pasirinktumėte būtinas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="303eb-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="303eb-106">Rasti taikomą kainą</span><span class="sxs-lookup"><span data-stu-id="303eb-106">Find the applicable price</span></span>
1. <span data-ttu-id="303eb-107">Eikite į Pardavimas ir rinkodara > Kainos ir nuolaidos > Rasti kainas.</span><span class="sxs-lookup"><span data-stu-id="303eb-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="303eb-108">Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="303eb-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="303eb-109">Sąraše raskite ir pasirinkite klientą US-001.</span><span class="sxs-lookup"><span data-stu-id="303eb-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="303eb-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="303eb-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="303eb-111">Lauke „Prekės numeris“ įveskite „T0004“.</span><span class="sxs-lookup"><span data-stu-id="303eb-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="303eb-112">Numatyta, kad lauko „Kiekis“ reikšmė yra 1.</span><span class="sxs-lookup"><span data-stu-id="303eb-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="303eb-113">Tačiau, jei žinote kliento ketinamo pateikti susijusių produktų užsakymo dydį, tada įveskite šią reikšmę.</span><span class="sxs-lookup"><span data-stu-id="303eb-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="303eb-114">Ši informacija aktuali, jei su klientu sudarytose prekybos sutartyse numatytos kiekių ribos, t. y., produkto kaina priklauso nuo mažiausio perkamo kiekio.</span><span class="sxs-lookup"><span data-stu-id="303eb-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="303eb-115">Lauke „Data“ įveskite datą, kada klientas tikisi pateikti užsakymą.</span><span class="sxs-lookup"><span data-stu-id="303eb-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="303eb-116">Data gali būti šiandiena arba bet kuri kita data ateityje.</span><span class="sxs-lookup"><span data-stu-id="303eb-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="303eb-117">Dabar sistema nurodys kainą, kuri galioja pasirinktam produktui, kai jį perka pasirinktas klientas, pasirinktą dieną pagal nurodytą kiekį.</span><span class="sxs-lookup"><span data-stu-id="303eb-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="303eb-118">Šiame pavyzdyje, jei klientas US-001 šiandien perka 1 produkto T0004 vienetą, turėtų sumokėti 350 CAD už vienetą.</span><span class="sxs-lookup"><span data-stu-id="303eb-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="303eb-119">Ši kaina nustatoma pagal esamą ir galiojančią prekybos sutartį su klientu.</span><span class="sxs-lookup"><span data-stu-id="303eb-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="303eb-120">Kituose puslapio laukuose pateikiama daugiau informacijos apie produkto kainą, produkto savikainą (jei nustatyta bendrajame produkte) ir apskaičiuotą pelningumą.</span><span class="sxs-lookup"><span data-stu-id="303eb-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="303eb-121">Jei pasirinkta „Rodyti susijusius produkto variantus“, tai reiškia, kad yra papildomų prekybos sutarčių dėl produkto variantų.</span><span class="sxs-lookup"><span data-stu-id="303eb-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="303eb-122">Pažymėkite žymės langelį „Rodyti susijusius produkto variantus“.</span><span class="sxs-lookup"><span data-stu-id="303eb-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="303eb-123">Rodomas produkto variantų sąrašas su informacija apie jų dimensijas.</span><span class="sxs-lookup"><span data-stu-id="303eb-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="303eb-124">Sąraše pažymėkite baltą spalvą reprezentuojančią eilutę.</span><span class="sxs-lookup"><span data-stu-id="303eb-124">In the list, mark the line representing colour White.</span></span>
    * <span data-ttu-id="303eb-125">Atkreipkite dėmesį, kad produkto kaina dabar skiriasi nuo anksčiau rodytos, kai ji nebuvo apskaičiuota pagal dimensiją.</span><span class="sxs-lookup"><span data-stu-id="303eb-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="303eb-126">Spustelėkite „Peržiūrėti pardavimo kainas“.</span><span class="sxs-lookup"><span data-stu-id="303eb-126">Click View sales prices.</span></span>
    * <span data-ttu-id="303eb-127">Puslapyje „Kaina (pardavimai)“ rodomos visos produktui, įskaitant jo variantus, taikomos prekybos sutartys.</span><span class="sxs-lookup"><span data-stu-id="303eb-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="303eb-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="303eb-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="303eb-129">Rasti taikomą nuolaidą</span><span class="sxs-lookup"><span data-stu-id="303eb-129">Find the applicable discount</span></span>
    * <span data-ttu-id="303eb-130">Įsitikinkite, kad lauke „Kliento sąskaita“ yra kliento numeris US-001 </span><span class="sxs-lookup"><span data-stu-id="303eb-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="303eb-131">Lauke „Prekės numeris“ įveskite „T0012“.</span><span class="sxs-lookup"><span data-stu-id="303eb-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="303eb-132">Įsitikinkite, kad lauko „Kiekis“ reikšmė yra 1.</span><span class="sxs-lookup"><span data-stu-id="303eb-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="303eb-133">Tokie produktui T0012 taikomi įkainiai nustatyti pagal vieną ar daugiau prekybos sutarčių: vieneto kaina yra 1000 CAD, o nuolaidos procentas yra 5.</span><span class="sxs-lookup"><span data-stu-id="303eb-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="303eb-134">Nustatykite kiekį – 20.</span><span class="sxs-lookup"><span data-stu-id="303eb-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="303eb-135">Dėl didesnio užsakymo kiekio eilutei taikoma nuolaida – klientui bus pasiūlyta ją padidinti nuo 5 iki 7 procentų.</span><span class="sxs-lookup"><span data-stu-id="303eb-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="303eb-136">Grynoji suma apskaičiuojama pagal vieneto kainą, nuolaidą ir bendrą kiekį.</span><span class="sxs-lookup"><span data-stu-id="303eb-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="303eb-137">Spustelėkite „Peržiūrėti eilutės nuolaidą“.</span><span class="sxs-lookup"><span data-stu-id="303eb-137">Click View line discount.</span></span>
    * <span data-ttu-id="303eb-138">Yra dvi eilutės nuolaidos sutartys produktui T0012, nurodančios 5 proc. nuolaidą užsakymo eilutės kiekiui nuo 1 iki 10 ir 7 proc. nuolaidą užsakymams, viršijantiems 10.</span><span class="sxs-lookup"><span data-stu-id="303eb-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="303eb-139">Atkreipkite dėmesį, kad šiame pavyzdyje nuolaidos taikomos produktų grupei (grupės kodas 01), kurios narys yra T0012 produktas.</span><span class="sxs-lookup"><span data-stu-id="303eb-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="303eb-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="303eb-140">Close the page.</span></span>


