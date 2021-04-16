---
title: EKA operacija Atšaukti užsakymą
description: Šioje temoje paaiškinamos funkcijų galimybės, pasiekiamos patobulintuose užsakymų atšaukimo puslapiuose EKA.
author: hhainesms
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2f7ad4f53917bb607afe84a2c457518c3f8f7a08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799111"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="664ff-103">EKA operacija Atšaukti užsakymą</span><span class="sxs-lookup"><span data-stu-id="664ff-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="664ff-104">**Užsakymo atšaukimo** veiksmas komercijos prekybos taške (POS) leidžia naujinti užsakymo paiešką ir filtravimo funkcijas bei su konkrečiu užsakymu susijusią informaciją.</span><span class="sxs-lookup"><span data-stu-id="664ff-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="664ff-105">Ši funkcija pasiekiama 10.0.15 arba vėlesnės versijos „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="664ff-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="664ff-106">Norėdami įgalinti šią funkciją, įjunkite funkciją **Patobulinta EKA operacija Atšaukti užsakymą** „Commerce Headquarters“ darbo srityje **Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="664ff-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="664ff-107">Įjungę funkciją, apsvarstykite galimybę atnaujinti jūsų [ekrano maketus](pos-screen-layouts.md) EKA, kad pasinaudotumėte kai kuriomis pakitusiomis galimybėmis.</span><span class="sxs-lookup"><span data-stu-id="664ff-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="664ff-108">Operacijos **Atšaukti užsakymą** mygtuko konfigūracija leidžia organizacijoms diegti operaciją su iš anksto nustatytu rodiniu.</span><span class="sxs-lookup"><span data-stu-id="664ff-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Mygtukyno konfigūracija](media/recallorderbuttongrid.png)

<span data-ttu-id="664ff-110">Toliau nurodytos galimos rodymo parinktys.</span><span class="sxs-lookup"><span data-stu-id="664ff-110">The display options are as follows.</span></span>
- <span data-ttu-id="664ff-111">**Nėra** – ši parinktis įdiegia operaciją be konkretaus rodinio.</span><span class="sxs-lookup"><span data-stu-id="664ff-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="664ff-112">Kai vartotojas atidaro šios konfigūracijos operaciją, jis bus paragintas ieškoti užsakymų arba pasirinkti iš iš anksto nustatyto užsakymų filtro.</span><span class="sxs-lookup"><span data-stu-id="664ff-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="664ff-113">**Užsakymai, kuriuos reikia įvykdyti** – kai naudotojas paleidžia operaciją, užklausa automatiškai vykdys iešką ir parodys užsakymų, kuriuos turi įvykdyti dabartinė naudotojo parduotuvė, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="664ff-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the user's current store.</span></span> <span data-ttu-id="664ff-114">Šie užsakymai sukonfigūruoti paėmimui parduotuvėje arba parduotuvės siuntimui ir šių užsakymų eilutės dar nebuvo paimtos ar supakuotos.</span><span class="sxs-lookup"><span data-stu-id="664ff-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="664ff-115">**Užsakymai, kuriuos reikia paimti** – kai vartotojas paleidžia operaciją, užklausa automatiškai vykdys iešką ir parodys užsakymų, kurie sukonfigūruoti paėmimui vartotojo dabartinėje parduotuvėje, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="664ff-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="664ff-116">**Užsakymai, kuriuos reikia išsiųsti** – kai vartotojas paleidžia operaciją, užklausa automatiškai vykdys iešką ir parodys užsakymų, kurie sukonfigūruoti siuntimui iš vartotojo dabartinės parduotuvės, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="664ff-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="664ff-117">Paleidus operaciją **Atšaukti užsakymą** EKA, jei rodinys sukonfigūruotas pagal parinktį **Nėra**, vartotojas galės ieškoti ir nuskaityti užsakymus vienu iš toliau pateiktų būdų.</span><span class="sxs-lookup"><span data-stu-id="664ff-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="664ff-118">Nuskaityti užsakymo brūkšninius kodus.</span><span class="sxs-lookup"><span data-stu-id="664ff-118">Scan order barcodes.</span></span> <span data-ttu-id="664ff-119">Šiuo atveju bus ieškoma atitikimų užsakymo numerio, kanalo nuorodos ir kvitų ID laukų.</span><span class="sxs-lookup"><span data-stu-id="664ff-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="664ff-120">Norėdami naudoti filtravimo mechanizmą, kad būtų surasti užsakymai, atitinkantys filtro kriterijus, programų juostoje pasirinkite piktogramą **Ieškoti užsakymų** arba **Ieškoti ir filtruoti**.</span><span class="sxs-lookup"><span data-stu-id="664ff-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="664ff-121">Pasirinkite iš iš anksto nustatyto filtro išplečiamajame meniu **Rodyti užsakymus** (užsakymus, kuriuos reikia įvykdyti, paimti arba išsiųsti).</span><span class="sxs-lookup"><span data-stu-id="664ff-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="664ff-123">Pritaikius ieškos kriterijus, programoje bus rodomas atitinkančių pardavimo užsakymų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="664ff-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span> <span data-ttu-id="664ff-124">Svarbu pažymėti, kad naudojant ieškos / filtro parinktis, nuskaityti užsakymai neturi būti susieti su dabartine naudotojo parduotuve.</span><span class="sxs-lookup"><span data-stu-id="664ff-124">It's important to note that when using the search/filter options, the orders retrieved do not have to be orders linked to the user's current store.</span></span> <span data-ttu-id="664ff-125">Šis ieškos procesas nuskaitys ir rodys visus kliento užsakymus, atitinkančius paieškos kriterijus, net jei užsakymas buvo sukurtas arba nustatytas įvykdyti kitoje parduotuvės /kanalo ar sandėlio vietoje.</span><span class="sxs-lookup"><span data-stu-id="664ff-125">This search process will retrieve and display any customer order that matches the search criteria, even if the order was created or set to be fulfilled by another store/channel or warehouse location.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="664ff-127">Vartotojas gali pasirinkti sąrašo užsakymą, norėdamas peržiūrėti papildomą informaciją.</span><span class="sxs-lookup"><span data-stu-id="664ff-127">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="664ff-128">Informacijos skydas dešiniajame ekrano krašte rodo konkrečią pasirinkto užsakymo informaciją, įskaitant užsakymo eilutės, pristatymo ir įvykdymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="664ff-128">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="664ff-129">Programų juostoje vartotojas gali pasirinkti operaciją.</span><span class="sxs-lookup"><span data-stu-id="664ff-129">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="664ff-130">Atsižvelgiant į užsakymo būseną, tam tikros operacijos gali būti neįjungtos.</span><span class="sxs-lookup"><span data-stu-id="664ff-130">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="664ff-131">**Grąžinimas** – inicijuojamas bet kurio kliento užsakymo produktų, kuriems išrašyta SF, grąžinimo kūrimo procesas.</span><span class="sxs-lookup"><span data-stu-id="664ff-131">**Return** – Initiates the process of creating a return for any of the invoiced products on the selected customer order.</span></span>

- <span data-ttu-id="664ff-132">**Atšaukti** – išduoda visą pasirinkto pardavimo užsakymo atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="664ff-132">**Cancel** – Issue a full cancellation of the selected sales order.</span></span> <span data-ttu-id="664ff-133">Ši parinktis negalima užsakymams, inicijuojamiems skambučių centro kanalu, ir negali būti naudojama užsakymui iš dalies atšaukti.</span><span class="sxs-lookup"><span data-stu-id="664ff-133">This option will not be available for orders initiated through a call center channel and cannot be used to partially cancel an order.</span></span>

- <span data-ttu-id="664ff-134">**Įvykdyti** – perkelia vartotoją į užsakymo įvykdymo puslapį, iš anksto filtruotą pagal pasirinktą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="664ff-134">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="664ff-135">Bus rodomos tik tos pasirinkto užsakymo eilutės, kurias vartotojo parduotuvė atidarė įvykdymui.</span><span class="sxs-lookup"><span data-stu-id="664ff-135">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="664ff-136">**Redaguoti** – leidžia vartotojams atlikti pasirinkto kliento užsakymo keitimus.</span><span class="sxs-lookup"><span data-stu-id="664ff-136">**Edit** – Allows users to make changes to the selected customer order.</span></span> <span data-ttu-id="664ff-137">Užsakymus galima redaguoti tik [tam tikruose scenarijuose](customer-orders-overview.md#edit-an-existing-customer-order).</span><span class="sxs-lookup"><span data-stu-id="664ff-137">Orders are only editable in [certain scenarios](customer-orders-overview.md#edit-an-existing-customer-order).</span></span>

- <span data-ttu-id="664ff-138">**Paėmimas** – ši pasirinktis bus galima, jei užsakyme yra viena ar daugiau eilučių, kurias galima paimti esamoje naudotojo parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="664ff-138">**Pick up** – This option will be available if the order has one or more lines designated for pickup at the user's current store.</span></span> <span data-ttu-id="664ff-139">Ši operacija paleidžia paėmimo srautą, leidžiantį vartotojui pasirinkti produktus, kurie bus paimti, ir sukuria paėmimo pardavimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="664ff-139">This operation launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>

## <a name="add-notifications-to-the-recall-order-operation"></a><span data-ttu-id="664ff-140">Pranešimų, skirtų užsakymo operacijai atšaukti, pridėjimas</span><span class="sxs-lookup"><span data-stu-id="664ff-140">Add notifications to the recall order operation</span></span>

<span data-ttu-id="664ff-141">Prireikus, 10.0.18 ir vėlesnėse versijose galima konfigūruoti EKA pranešimus ir tiesioginės plytelės įspėjimus, skirtus operacijai **Užsakymo atšaukimas**.</span><span class="sxs-lookup"><span data-stu-id="664ff-141">In version 10.0.18 and later, you can configure POS notifications and live tile alerts for the **Order Recall** operation if desired.</span></span> <span data-ttu-id="664ff-142">Daugiau informacijos žr. skyriuje [Užsakymo pranešimų elektroniniame kasos aparate (EKA) rodymas](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="664ff-142">For more information, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
