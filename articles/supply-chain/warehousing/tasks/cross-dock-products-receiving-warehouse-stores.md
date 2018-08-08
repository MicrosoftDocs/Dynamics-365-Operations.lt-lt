--- 
title: "Produktų paskirstymas iš gavimo sandėlio į parduotuves"
description: "Ši procedūra padeda atlikti žingsnius, norint kurti ir vykdyti paskirstymą produktams iš pirkimo užsakymo gavimo vietos į vieną ar kelias parduotuves paskirstyti."
author: ShylaThompson
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 6c8e25007cc4a204aeaf73a2e819c129fa8fa29d
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="d38df-103">Produktų paskirstymas iš gavimo sandėlio į parduotuves</span><span class="sxs-lookup"><span data-stu-id="d38df-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d38df-104">Ši procedūra padeda atlikti žingsnius, norint kurti ir vykdyti paskirstymą produktams iš pirkimo užsakymo gavimo vietos į vieną ar kelias parduotuves paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="d38df-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="d38df-105">Vartotojas gali nustatyti kelias konfigūracijas ir nurodyti sistemai siūlyti, kaip paskirstyti produktus, arba patys įvesti, kur produktai turi būti paskirstomi ir koks jų kiekis paskirstomas į kiekvieną parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="d38df-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="d38df-106">Į procedūrą neįtraukiamas duomenų, kuriuos galima naudoti paskirstyme, pvz., papildymo taisyklių, organizacijos hierarchijų ir parduotuvės reikšmės, nustatymas.</span><span class="sxs-lookup"><span data-stu-id="d38df-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="d38df-107">Procedūroje naudojama demonstracinė įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="d38df-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="d38df-108">Eikite į Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="d38df-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="d38df-109">Sąraše pasirinkite pirkimo užsakymą ir spustelėję saitą atidarykite užsakymą..</span><span class="sxs-lookup"><span data-stu-id="d38df-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="d38df-110">Veiksmų srityje spustelėkite Mažmeninė prekyba.</span><span class="sxs-lookup"><span data-stu-id="d38df-110">On the Action Pane, click Retail.</span></span>
4. <span data-ttu-id="d38df-111">Spustelėkite Prekių skirstymas.</span><span class="sxs-lookup"><span data-stu-id="d38df-111">Click Cross docking.</span></span>
5. <span data-ttu-id="d38df-112">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="d38df-112">Click Edit.</span></span>
    * <span data-ttu-id="d38df-113">Kategoriją galima naudoti norint filtruoti prekes sekcijoje Eilutės.</span><span class="sxs-lookup"><span data-stu-id="d38df-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="d38df-114">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="d38df-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d38df-115">Lauke Prekių skirstymo kiekis įveskite reikšmę, norėdami nurodyti, koks pasirinkto perkamo produkto kiekis turi būti paskirstytas.</span><span class="sxs-lookup"><span data-stu-id="d38df-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="d38df-116">Lauke Papildomas prekių skirstymo kiekis įveskite vertę, norėdami nurodyti perkamų galimų produktų kiekius, kuriuos reikia paskirstyti</span><span class="sxs-lookup"><span data-stu-id="d38df-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="d38df-117">Lauke Paskirstymas įveskite „Vietos reikšmė“.</span><span class="sxs-lookup"><span data-stu-id="d38df-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="d38df-118">Galite pasirinkti kitus tipus ir naudoti kitas paskirstymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="d38df-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="d38df-119">Lauke Papildymo hierarchija pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d38df-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="d38df-120">Lauke Pagal asortimentus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="d38df-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="d38df-121">Spustelėkite Skaičiuoti kiekius.</span><span class="sxs-lookup"><span data-stu-id="d38df-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="d38df-122">Spustelėkite Kurti užsakymą.</span><span class="sxs-lookup"><span data-stu-id="d38df-122">Click Create order.</span></span>
14. <span data-ttu-id="d38df-123">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="d38df-123">Click Yes.</span></span>
15. <span data-ttu-id="d38df-124">Sąraše raskite ir pasirinkite produktus gavusį sandėlį</span><span class="sxs-lookup"><span data-stu-id="d38df-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="d38df-125">Spustelėkite Užsakymas, norėdami peržiūrėti sukurtus pasirinkto sandėlio užsakymus</span><span class="sxs-lookup"><span data-stu-id="d38df-125">Click Order to view the orders that got created for the selected warehouse</span></span>


