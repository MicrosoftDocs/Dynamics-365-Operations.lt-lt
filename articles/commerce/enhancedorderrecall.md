---
title: EKA operacija Atšaukti užsakymą
description: Šioje temoje paaiškinamos funkcijų galimybės, pasiekiamos patobulintuose užsakymų atšaukimo puslapiuose EKA.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 21e8045d754006345f5ad68e1e67579386c6df4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010079"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="1fddf-103">EKA operacija Atšaukti užsakymą</span><span class="sxs-lookup"><span data-stu-id="1fddf-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1fddf-104">**Užsakymo atšaukimo** veiksmas komercijos prekybos taške (POS) leidžia naujinti užsakymo paiešką ir filtravimo funkcijas bei su konkrečiu užsakymu susijusią informaciją.</span><span class="sxs-lookup"><span data-stu-id="1fddf-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="1fddf-105">Ši funkcija pasiekiama 10.0.15 arba vėlesnės versijos „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="1fddf-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="1fddf-106">Norėdami įgalinti šią funkciją, įjunkite funkciją **Patobulinta EKA operacija Atšaukti užsakymą** „Commerce Headquarters“ darbo srityje **Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="1fddf-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="1fddf-107">Įjungę funkciją, apsvarstykite galimybę atnaujinti jūsų [ekrano maketus](pos-screen-layouts.md) EKA, kad pasinaudotumėte kai kuriomis pakitusiomis galimybėmis.</span><span class="sxs-lookup"><span data-stu-id="1fddf-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="1fddf-108">Operacijos **Atšaukti užsakymą** mygtuko konfigūracija leidžia organizacijoms diegti operaciją su iš anksto nustatytu rodiniu.</span><span class="sxs-lookup"><span data-stu-id="1fddf-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Mygtukyno konfigūracija](media/recallorderbuttongrid.png)

<span data-ttu-id="1fddf-110">Toliau nurodytos galimos rodymo parinktys.</span><span class="sxs-lookup"><span data-stu-id="1fddf-110">The display options are as follows.</span></span>
- <span data-ttu-id="1fddf-111">**Nėra** – ši parinktis įdiegia operaciją be konkretaus rodinio.</span><span class="sxs-lookup"><span data-stu-id="1fddf-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="1fddf-112">Kai vartotojas atidaro šios konfigūracijos operaciją, jis bus paragintas ieškoti užsakymų arba pasirinkti iš iš anksto nustatyto užsakymų filtro.</span><span class="sxs-lookup"><span data-stu-id="1fddf-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="1fddf-113">**Užsakymai, kuriuos reikia įvykdyti** – kai vartotojas paleidžia operaciją, užklausa automatiškai vykdys iešką ir parodys užsakymų, kuriuos turi įvykdyti parduotuvė, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1fddf-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="1fddf-114">Šie užsakymai sukonfigūruoti paėmimui parduotuvėje arba parduotuvės siuntimui ir šių užsakymų eilutės dar nebuvo paimtos ar supakuotos.</span><span class="sxs-lookup"><span data-stu-id="1fddf-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="1fddf-115">**Užsakymai, kuriuos reikia paimti** – kai vartotojas paleidžia operaciją, užklausa automatiškai vykdys iešką ir parodys užsakymų, kurie sukonfigūruoti paėmimui vartotojo dabartinėje parduotuvėje, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1fddf-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="1fddf-116">**Užsakymai, kuriuos reikia išsiųsti** – kai vartotojas paleidžia operaciją, užklausa automatiškai vykdys iešką ir parodys užsakymų, kurie sukonfigūruoti siuntimui iš vartotojo dabartinės parduotuvės, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1fddf-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="1fddf-117">Paleidus operaciją **Atšaukti užsakymą** EKA, jei rodinys sukonfigūruotas pagal parinktį **Nėra**, vartotojas galės ieškoti ir nuskaityti užsakymus vienu iš toliau pateiktų būdų.</span><span class="sxs-lookup"><span data-stu-id="1fddf-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="1fddf-118">Nuskaityti užsakymo brūkšninius kodus.</span><span class="sxs-lookup"><span data-stu-id="1fddf-118">Scan order barcodes.</span></span> <span data-ttu-id="1fddf-119">Šiuo atveju bus ieškoma atitikimų užsakymo numerio, kanalo nuorodos ir kvitų ID laukų.</span><span class="sxs-lookup"><span data-stu-id="1fddf-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="1fddf-120">Norėdami naudoti filtravimo mechanizmą, kad būtų surasti užsakymai, atitinkantys filtro kriterijus, programų juostoje pasirinkite piktogramą **Ieškoti užsakymų** arba **Ieškoti ir filtruoti**.</span><span class="sxs-lookup"><span data-stu-id="1fddf-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="1fddf-121">Pasirinkite iš iš anksto nustatyto filtro išplečiamajame meniu **Rodyti užsakymus** (užsakymus, kuriuos reikia įvykdyti, paimti arba išsiųsti).</span><span class="sxs-lookup"><span data-stu-id="1fddf-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="1fddf-123">Pritaikius ieškos kriterijus, programoje bus rodomas atitinkančių pardavimo užsakymų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="1fddf-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="1fddf-125">Vartotojas gali pasirinkti sąrašo užsakymą, norėdamas peržiūrėti papildomą informaciją.</span><span class="sxs-lookup"><span data-stu-id="1fddf-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="1fddf-126">Informacijos skydas dešiniajame ekrano krašte rodo konkrečią pasirinkto užsakymo informaciją, įskaitant užsakymo eilutės, pristatymo ir įvykdymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="1fddf-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="1fddf-127">Programų juostoje vartotojas gali pasirinkti operaciją.</span><span class="sxs-lookup"><span data-stu-id="1fddf-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="1fddf-128">Atsižvelgiant į užsakymo būseną, tam tikros operacijos gali būti neįjungtos.</span><span class="sxs-lookup"><span data-stu-id="1fddf-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="1fddf-129">**Grąžinti** – vykdo vienos ar daugiau SF, susijusių su pasirinktu kliento užsakymu, grąžinimą.</span><span class="sxs-lookup"><span data-stu-id="1fddf-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="1fddf-130">**Atšaukti** – išduoda visą pasirinkto pardavimo užsakymo atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="1fddf-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="1fddf-131">**Įvykdyti** – perkelia vartotoją į užsakymo įvykdymo puslapį, iš anksto filtruotą pagal pasirinktą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1fddf-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="1fddf-132">Bus rodomos tik tos pasirinkto užsakymo eilutės, kurias vartotojo parduotuvė atidarė įvykdymui.</span><span class="sxs-lookup"><span data-stu-id="1fddf-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="1fddf-133">**Redaguoti** – leidžia vartotojams atlikti pasirinkto kliento užsakymo keitimus.</span><span class="sxs-lookup"><span data-stu-id="1fddf-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="1fddf-134">**Paimti** – paleidžia paėmimo srautą, leidžiantį vartotojui pasirinkti produktus, kurie bus paimti, ir sukuria paėmimo pardavimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="1fddf-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
