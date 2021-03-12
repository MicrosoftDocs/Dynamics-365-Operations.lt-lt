---
title: Produktų paskirstymas iš gavimo sandėlio į parduotuves
description: Ši procedūra padeda atlikti žingsnius, norint kurti ir vykdyti paskirstymą produktams iš pirkimo užsakymo gavimo vietos į vieną ar kelias parduotuves paskirstyti.
author: ShylaThompson
manager: tfehr
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPushPerPackage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac93806bc85be92840548e160ddf803e63adbbc4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977193"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="81c10-103">Produktų paskirstymas iš gavimo sandėlio į parduotuves</span><span class="sxs-lookup"><span data-stu-id="81c10-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81c10-104">Ši procedūra padeda atlikti žingsnius, norint kurti ir vykdyti paskirstymą produktams iš pirkimo užsakymo gavimo vietos į vieną ar kelias parduotuves paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="81c10-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="81c10-105">Vartotojas gali nustatyti kelias konfigūracijas ir nurodyti sistemai siūlyti, kaip paskirstyti produktus, arba patys įvesti, kur produktai turi būti paskirstomi ir koks jų kiekis paskirstomas į kiekvieną parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="81c10-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="81c10-106">Į procedūrą neįtraukiamas duomenų, kuriuos galima naudoti paskirstyme, pvz., papildymo taisyklių, organizacijos hierarchijų ir parduotuvės reikšmės, nustatymas.</span><span class="sxs-lookup"><span data-stu-id="81c10-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="81c10-107">Procedūroje naudojama demonstracinė įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="81c10-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="81c10-108">Eikite į Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="81c10-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="81c10-109">Sąraše pasirinkite pirkimo užsakymą ir spustelėję saitą atidarykite užsakymą..</span><span class="sxs-lookup"><span data-stu-id="81c10-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="81c10-110">Veiksmų srityje spustelėkite Mažmeninė prekyba ir prekyba.</span><span class="sxs-lookup"><span data-stu-id="81c10-110">On the Action Pane, click Retail and Commerce.</span></span>
4. <span data-ttu-id="81c10-111">Spustelėkite Prekių skirstymas.</span><span class="sxs-lookup"><span data-stu-id="81c10-111">Click Cross docking.</span></span>
5. <span data-ttu-id="81c10-112">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="81c10-112">Click Edit.</span></span>
    * <span data-ttu-id="81c10-113">Kategoriją galima naudoti norint filtruoti prekes sekcijoje Eilutės.</span><span class="sxs-lookup"><span data-stu-id="81c10-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="81c10-114">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="81c10-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="81c10-115">Lauke Prekių skirstymo kiekis įveskite reikšmę, norėdami nurodyti, koks pasirinkto perkamo produkto kiekis turi būti paskirstytas.</span><span class="sxs-lookup"><span data-stu-id="81c10-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="81c10-116">Lauke Papildomas prekių skirstymo kiekis įveskite vertę, norėdami nurodyti perkamų galimų produktų kiekius, kuriuos reikia paskirstyti</span><span class="sxs-lookup"><span data-stu-id="81c10-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="81c10-117">Lauke Paskirstymas įveskite „Vietos reikšmė“.</span><span class="sxs-lookup"><span data-stu-id="81c10-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="81c10-118">Galite pasirinkti kitus tipus ir naudoti kitas paskirstymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="81c10-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="81c10-119">Lauke Papildymo hierarchija pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="81c10-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="81c10-120">Lauke Pagal asortimentus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="81c10-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="81c10-121">Spustelėkite Skaičiuoti kiekius.</span><span class="sxs-lookup"><span data-stu-id="81c10-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="81c10-122">Spustelėkite Kurti užsakymą.</span><span class="sxs-lookup"><span data-stu-id="81c10-122">Click Create order.</span></span>
14. <span data-ttu-id="81c10-123">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="81c10-123">Click Yes.</span></span>
15. <span data-ttu-id="81c10-124">Sąraše raskite ir pasirinkite produktus gavusį sandėlį</span><span class="sxs-lookup"><span data-stu-id="81c10-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="81c10-125">Spustelėkite Užsakymas, norėdami peržiūrėti sukurtus pasirinkto sandėlio užsakymus</span><span class="sxs-lookup"><span data-stu-id="81c10-125">Click Order to view the orders that got created for the selected warehouse</span></span>

