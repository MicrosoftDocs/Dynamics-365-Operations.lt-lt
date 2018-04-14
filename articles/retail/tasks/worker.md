--- 
title: " Konfigūruoti darbininką"
description: "Šioje procedūroje parodoma, kaip mažmeninės prekybos darbuotoją sukonfigūruoti kaip pardavimo atstovą, kuriam taikomi EKA pardavimo komisiniai."
author: jblucher
manager: AnnBe
ms.date: 02/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5e168c4d0b4e48b73d4a31ca8525e2aeb288846c
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="configure-a-worker"></a><span data-ttu-id="610c4-103"> Konfigūruoti darbininką</span><span class="sxs-lookup"><span data-stu-id="610c4-103">Configure a worker</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="610c4-104">Šioje procedūroje parodoma, kaip mažmeninės prekybos darbuotoją sukonfigūruoti kaip pardavimo atstovą, kuriam taikomi EKA pardavimo komisiniai.</span><span class="sxs-lookup"><span data-stu-id="610c4-104">This procedure demonstrates how to configure a retail worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="610c4-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="610c4-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="610c4-106">Darbuotojo pardavimo komisinių grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="610c4-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="610c4-107">Pasirinkite Pardavimai ir rinkodara > Komisiniai > Pardavimo grupės.</span><span class="sxs-lookup"><span data-stu-id="610c4-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="610c4-108">Darbuotojus galima priskirti vienai arba kelioms pardavimo grupėms.</span><span class="sxs-lookup"><span data-stu-id="610c4-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="610c4-109">EKA galite pasirinkti bet kurią pardavimo grupę, kurioje yra darbuotojų iš parduotuvės adresų knygelės.</span><span class="sxs-lookup"><span data-stu-id="610c4-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="610c4-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="610c4-110">Click New.</span></span>
3. <span data-ttu-id="610c4-111">Lauke Grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="610c4-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="610c4-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="610c4-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="610c4-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="610c4-113">Click Save.</span></span>
6. <span data-ttu-id="610c4-114">Veiksmų srityje spustelėkite Bendra.</span><span class="sxs-lookup"><span data-stu-id="610c4-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="610c4-115">Spustelėkite Pardavimo atstovas.</span><span class="sxs-lookup"><span data-stu-id="610c4-115">Click Sales rep.</span></span>
    * <span data-ttu-id="610c4-116">Pardavimo grupėje gali būti daugiau nei vienas darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="610c4-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="610c4-117">Komisinius darbuotojams galima paskirstyti pagal nustatytą komisinių dalį.</span><span class="sxs-lookup"><span data-stu-id="610c4-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="610c4-118">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="610c4-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="610c4-119">Lauke Komisinių dalis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="610c4-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="610c4-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="610c4-120">Click Save.</span></span>
11. <span data-ttu-id="610c4-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="610c4-121">Close the page.</span></span>
12. <span data-ttu-id="610c4-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="610c4-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="610c4-123">Darbuotojų priskyrimas prie numatytosios pardavimo grupės</span><span class="sxs-lookup"><span data-stu-id="610c4-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="610c4-124">Eikite į Mažmeninė prekyba ir prekyba > Darbuotojai > Darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="610c4-124">Go to Retail and commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="610c4-125">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="610c4-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="610c4-126">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="610c4-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="610c4-127">Spustelėkite skirtuką Mažmeninė prekyba.</span><span class="sxs-lookup"><span data-stu-id="610c4-127">Click the Retail tab.</span></span>
    * <span data-ttu-id="610c4-128">Darbuotoją galima priskirti numatytajai pardavimo grupei.</span><span class="sxs-lookup"><span data-stu-id="610c4-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="610c4-129">Numatytoji pardavimo grupė bus automatiškai įtraukti į EKA pardavimo eilutes, jei ši parinktis įjungta parduotuvės funkcijų profilyje.</span><span class="sxs-lookup"><span data-stu-id="610c4-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="610c4-130">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="610c4-130">Click Edit.</span></span>
6. <span data-ttu-id="610c4-131">Lauke Numatytoji grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="610c4-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="610c4-132">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="610c4-132">Click Save.</span></span>


