---
title: " Konfigūruoti darbininką"
description: Šioje procedūroje parodoma, kaip darbininką sukonfigūruoti kaip pardavimo atstovą, kuriam taikomi EKA pardavimo komisiniai.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 73c200f7f6ff0aa5672e50c539bfaa5e30213185
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003608"
---
# <a name="configure-a-worker"></a><span data-ttu-id="22be5-103"> Konfigūruoti darbininką</span><span class="sxs-lookup"><span data-stu-id="22be5-103">Configure a worker</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22be5-104">Šioje procedūroje parodoma, kaip darbininką sukonfigūruoti kaip pardavimo atstovą, kuriam taikomi EKA pardavimo komisiniai.</span><span class="sxs-lookup"><span data-stu-id="22be5-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="22be5-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="22be5-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="22be5-106">Darbininko pardavimo komisinių grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="22be5-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="22be5-107">Pasirinkite Pardavimai ir rinkodara > Komisiniai > Pardavimo grupės.</span><span class="sxs-lookup"><span data-stu-id="22be5-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="22be5-108">Darbininkus galima priskirti vienai arba kelioms pardavimo grupėms.</span><span class="sxs-lookup"><span data-stu-id="22be5-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="22be5-109">EKA galite pasirinkti bet kurią pardavimo grupę, kurioje yra darbininkų iš parduotuvės adresų knygelės.</span><span class="sxs-lookup"><span data-stu-id="22be5-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="22be5-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="22be5-110">Click New.</span></span>
3. <span data-ttu-id="22be5-111">Lauke Grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="22be5-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="22be5-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="22be5-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="22be5-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="22be5-113">Click Save.</span></span>
6. <span data-ttu-id="22be5-114">Veiksmų srityje spustelėkite Bendra.</span><span class="sxs-lookup"><span data-stu-id="22be5-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="22be5-115">Spustelėkite Pardavimo atstovas.</span><span class="sxs-lookup"><span data-stu-id="22be5-115">Click Sales rep.</span></span>
    * <span data-ttu-id="22be5-116">Pardavimo grupėje gali būti daugiau nei vienas darbininkas.</span><span class="sxs-lookup"><span data-stu-id="22be5-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="22be5-117">Komisinius darbininkams galima paskirstyti pagal nustatytą komisinių dalį.</span><span class="sxs-lookup"><span data-stu-id="22be5-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="22be5-118">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="22be5-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="22be5-119">Lauke Komisinių dalis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="22be5-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="22be5-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="22be5-120">Click Save.</span></span>
11. <span data-ttu-id="22be5-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="22be5-121">Close the page.</span></span>
12. <span data-ttu-id="22be5-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="22be5-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="22be5-123">Darbininkų priskyrimas prie numatytosios pardavimo grupės</span><span class="sxs-lookup"><span data-stu-id="22be5-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="22be5-124">Eikite į Mažmeninė prekyba ir prekyba > Darbuotojai > Darbininkai.</span><span class="sxs-lookup"><span data-stu-id="22be5-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="22be5-125">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="22be5-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="22be5-126">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="22be5-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="22be5-127">Spustelėkite skirtuką Prekyba.</span><span class="sxs-lookup"><span data-stu-id="22be5-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="22be5-128">Darbininką galima priskirti numatytajai pardavimo grupei.</span><span class="sxs-lookup"><span data-stu-id="22be5-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="22be5-129">Numatytoji pardavimo grupė bus automatiškai įtraukti į EKA pardavimo eilutes, jei ši parinktis įjungta parduotuvės funkcijų profilyje.</span><span class="sxs-lookup"><span data-stu-id="22be5-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="22be5-130">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="22be5-130">Click Edit.</span></span>
6. <span data-ttu-id="22be5-131">Lauke Numatytoji grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="22be5-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="22be5-132">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="22be5-132">Click Save.</span></span>

