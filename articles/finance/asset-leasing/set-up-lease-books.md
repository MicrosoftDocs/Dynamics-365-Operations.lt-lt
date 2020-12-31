---
title: Nuomos knygų nustatymas
description: Šioje temoje aprašoma informacija, palaikoma nuomos knygose. Nuomos knygose yra apskaitos strategijos, apibrėžiančios, kaip sistemoje atsiskaitoma už nuomos sutartis.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446191"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="350cb-104">Nuomos knygų nustatymas</span><span class="sxs-lookup"><span data-stu-id="350cb-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="350cb-105">Nuomos knygose yra apskaitos strategijos, apibrėžiančios, kaip sistemoje atsiskaitoma už nuomos sutartis.</span><span class="sxs-lookup"><span data-stu-id="350cb-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="350cb-106">Be grynųjų pinigų apskaitos, turto nuoma palaiko šiuos standartus.</span><span class="sxs-lookup"><span data-stu-id="350cb-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="350cb-107">Jungtinėse Valstijose bendrai priimami apskaitos principai (US GAAP)</span><span class="sxs-lookup"><span data-stu-id="350cb-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="350cb-108">Apskaitos standartų kodifikavimo tema Nr. 842 (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="350cb-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="350cb-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="350cb-109">ASC 840</span></span>
- <span data-ttu-id="350cb-110">Tarptautinis finansinių ataskaitų standartas Nr. 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="350cb-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="350cb-111">Tarptautinis apskaitos standartas Nr. 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="350cb-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="350cb-112">Norėdami sukurti nuomos knygą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="350cb-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="350cb-113">Eikite į **Turto nuoma \> Sąranka \> Nuomos knygos**.</span><span class="sxs-lookup"><span data-stu-id="350cb-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="350cb-114">Norėdami pridėti knygą, pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="350cb-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="350cb-115">Užpildykite toliau nurodytus laukus.</span><span class="sxs-lookup"><span data-stu-id="350cb-115">Set the following fields.</span></span>

    | <span data-ttu-id="350cb-116">Pavadinimas / vardas ir (arba) pavardė</span><span class="sxs-lookup"><span data-stu-id="350cb-116">Name</span></span>                                     | <span data-ttu-id="350cb-117">aprašymas</span><span class="sxs-lookup"><span data-stu-id="350cb-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="350cb-118">Registravimo sluoksnis</span><span class="sxs-lookup"><span data-stu-id="350cb-118">Posting layer</span></span>                            | <span data-ttu-id="350cb-119">Pasirinkite naudotiną registravimo sluoksnį.</span><span class="sxs-lookup"><span data-stu-id="350cb-119">Select the posting layer to use.</span></span> <span data-ttu-id="350cb-120">Visos prie nuomos pridėtos knygos nustatytos tam tikram registravimo sluoksniui.</span><span class="sxs-lookup"><span data-stu-id="350cb-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="350cb-121">Kiekvienas registravimo sluoksnis turi skirtingus registravimo tikslus.</span><span class="sxs-lookup"><span data-stu-id="350cb-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="350cb-122">Nuomos tipas</span><span class="sxs-lookup"><span data-stu-id="350cb-122">Lease type</span></span>                               | <span data-ttu-id="350cb-123">Pasirinkite, ar nuomos sutartis turi būti klasifikuojama automatiškai, ar turi būti iš anksto nurodyta kaip finansai ar veiklos nuoma.</span><span class="sxs-lookup"><span data-stu-id="350cb-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="350cb-124">Apskaitos sistema</span><span class="sxs-lookup"><span data-stu-id="350cb-124">Accounting framework</span></span>                     | <span data-ttu-id="350cb-125">Pasirinkite sistemą, kuri susieta su pagrindine knyga.</span><span class="sxs-lookup"><span data-stu-id="350cb-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="350cb-126">Nuomos laikotarpio / naudingo naudojimo laiko nustatymas</span><span class="sxs-lookup"><span data-stu-id="350cb-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="350cb-127">Sistema klasifikuos nuomą kaip finansinę, jei nustatytas **automatinis** nuomos tipas ir jei nuomos terminas per visą turto naudingo naudojimo laiką yra didesnis arba lygus šiame lauke apibrėžtai procentinei daliai.</span><span class="sxs-lookup"><span data-stu-id="350cb-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="350cb-128">Dabartinės vertės / turto tikrosios vertės nustatymas</span><span class="sxs-lookup"><span data-stu-id="350cb-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="350cb-129">Įveskite sveikąjį skaičių, nurodantį ribinę vertę, kuri nustatys nuomos tipą.</span><span class="sxs-lookup"><span data-stu-id="350cb-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="350cb-130">Jei dabartinė minimalių įmokų nuomos mokesčių vertė yra didesnė už vartotojo nustatytą vertę iš knygų nustatymo ir jei knygos nuomos klasifikacija nustatyta kaip automatinė, sistema suklasifikuos nuomos sutartį kaip finansinį nuomos sutartį.</span><span class="sxs-lookup"><span data-stu-id="350cb-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="350cb-131">Trumpojo laikotarpio ribinė reikšmė</span><span class="sxs-lookup"><span data-stu-id="350cb-131">Short-term threshold</span></span>                     | <span data-ttu-id="350cb-132">Įveskite dienų skaičių, kuris bus naudojamas kaip trumpalaikės nuomos ribos.</span><span class="sxs-lookup"><span data-stu-id="350cb-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="350cb-133">Jei nuomos sąlygos vertė yra mažesnė arba lygi čia įvesto mėnesių skaičiui, sistema suklasifikuos nuomą kaip trumpalaikę nuomą ir bus taikomas atidėtas nuomos režimas.</span><span class="sxs-lookup"><span data-stu-id="350cb-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="350cb-134">Mažos vertės ribinė reikšmė</span><span class="sxs-lookup"><span data-stu-id="350cb-134">Low value threshold</span></span>                      | <span data-ttu-id="350cb-135">Įveskite sumą, kuri bus naudojama kaip mažos vertės nuomos riba.</span><span class="sxs-lookup"><span data-stu-id="350cb-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="350cb-136">Jei turto tikroji vertė yra mažesnė arba lygi čia įvestai vertei, sistema suklasifikuos nuomą kaip mažos vertės turto nuomą ir bus taikomas atidėtas nuomos režimas.</span><span class="sxs-lookup"><span data-stu-id="350cb-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="350cb-137">Mokėti tiekėjui</span><span class="sxs-lookup"><span data-stu-id="350cb-137">Pay to vendor</span></span>                            | <span data-ttu-id="350cb-138">Nustatyti šią parinktį į **Taip**, kad būtų leidžiama registruoti nuomos mokėjimus, kaip SF, į tiekėjo sąskaitą, nurodytą kiekvienoje nuomos sutartyje.</span><span class="sxs-lookup"><span data-stu-id="350cb-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="350cb-139">Užregistravus nuomos apmokėjimą, tiekėjo sąskaita bus kredituota.</span><span class="sxs-lookup"><span data-stu-id="350cb-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="350cb-140">Jei ši pasirinktis nustatyta į **Ne**, sąskaita, kuri yra nurodyta puslapio **Nuomos registravimo parametrai** registravimo tipe **Nuomos mokestis** bus kredituojama.</span><span class="sxs-lookup"><span data-stu-id="350cb-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
