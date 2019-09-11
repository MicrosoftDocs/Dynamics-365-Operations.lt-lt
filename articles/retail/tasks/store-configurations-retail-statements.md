---
title: " Mažmeninės prekybos išrašų parduotuvės konfigūracijos"
description: Ši procedūra nurodo mažmeninės prekybos parduotuvės konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami mažmeninės prekybos išrašai.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbedcda59f503b103d5448e59038e4ed8ca0b51d
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916535"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="1f782-103"> Mažmeninės prekybos išrašų parduotuvės konfigūracijos</span><span class="sxs-lookup"><span data-stu-id="1f782-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1f782-104">Ši procedūra nurodo mažmeninės prekybos parduotuvės konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami mažmeninės prekybos išrašai.</span><span class="sxs-lookup"><span data-stu-id="1f782-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="1f782-105">Mažmeninės prekybos parduotuvių finansinės dimensijos aprašytos kitoje procedūroje.</span><span class="sxs-lookup"><span data-stu-id="1f782-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="1f782-106">Šioje procedūroje naudojama demonstracinė įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="1f782-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="1f782-107">**Naršymo srityje** eikite į **Moduliai > Mažmeninė prekyba ir komercija > Kanalai > Mažmeninės prekybos parduotuvės > Visos mažmeninės prekybos parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="1f782-107">In the **Navgiation pane**, go to **Modules > Retail and commerce > Channels > Retail stores > All retail stores**.</span></span>
2. <span data-ttu-id="1f782-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1f782-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1f782-109">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1f782-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1f782-110">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="1f782-110">Click **Edit**.</span></span>
5. <span data-ttu-id="1f782-111">„fastTab“ **Išrašas / uždarymas** parametrai taikomi kuriant, tikrinant ir skelbiant parduotuvės išrašus.</span><span class="sxs-lookup"><span data-stu-id="1f782-111">The settings in the **Statement/closing** fastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="1f782-112">Išplėskite „fastTab“ **Išrašas / uždarymas**.</span><span class="sxs-lookup"><span data-stu-id="1f782-112">Expand the **Statement/closing** fastTab.</span></span>  
6. <span data-ttu-id="1f782-113">Lauke **Išrašo metodas** pasirinkite metodą, kurį norite naudoti išrašo eilutėms grupuoti.</span><span class="sxs-lookup"><span data-stu-id="1f782-113">In the **Statement method** field, select the method you want to use to to group the statement lines by.</span></span>  
7. <span data-ttu-id="1f782-114">Lauke **Vienas išrašas per dieną** pasirinkite Taip, jei kuriant išrašus pagal išrašų kūrimo paketinę užduotį per dieną turėtų būti sukuriamas tik vienas išrašas.</span><span class="sxs-lookup"><span data-stu-id="1f782-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="1f782-115">Lauke **Mokėjimo priemonių deklaravimo skaičiavimas** nustatyta, ar mokėjimo priemonių deklaracijos turėtų būti sudedamos kartu, ar turėtų būti naudojama paskutinė deklaracija.</span><span class="sxs-lookup"><span data-stu-id="1f782-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="1f782-116">Lauke **Apvalinimas** pasirinkite didžiosios knygos sąskaitą, kurioje bus skelbiami apvalinimo skirtumai.</span><span class="sxs-lookup"><span data-stu-id="1f782-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="1f782-117">Lauke **Didžiausias apvalinimo skirtumas** įveskite didžiausią leidžiamą apvalinimo skirtumą.</span><span class="sxs-lookup"><span data-stu-id="1f782-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="1f782-118">Lauke **Registravimas** įveskite didžiausią bendrą registravimo skirtumą, leidžiamą išrašui.</span><span class="sxs-lookup"><span data-stu-id="1f782-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="1f782-119">Lauke **Pamaina** įveskite didžiausią bendrą pamainos skirtumą išraše.</span><span class="sxs-lookup"><span data-stu-id="1f782-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="1f782-120">Lauke **Operacija** įveskite didžiausią bendrą skirtumą išrašo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1f782-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="1f782-121">Lauke **Uždarymo metodas** nustatykite, ar operacijos, kurios bus įtrauktos į išrašą, turėtų priklausyti uždarytai pamainai, ar tai gali būti bet kokios operacijos nustatytu datos ir (arba) laiko intervalu.</span><span class="sxs-lookup"><span data-stu-id="1f782-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="1f782-122">Lauke **Darbo dienos pabaiga** įveskite laiką, jei operacijos, įvykusios po vidurnakčio, turėtų būti registruojamos ankstesnę dieną.</span><span class="sxs-lookup"><span data-stu-id="1f782-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="1f782-123">Pasirinkite parinkties **Registruoti kaip darbo dieną** nuostatą Taip, jei operacijos, įvykusios po vidurnakčio, turėtų būti registruojamos ankstesnę dieną.</span><span class="sxs-lookup"><span data-stu-id="1f782-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="1f782-124">Pasirinkite parinkties **Skaidyti pagal išrašo metodą** nuostatą Taip, kad išrašai būtų sukurti pagal kiekvieną nustatytą išrašų metodą.</span><span class="sxs-lookup"><span data-stu-id="1f782-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="1f782-125">Tai gali būti naudinga, jei registravimo efektyvumą reikia tobulinti parduotuvėse, kuriose atliekama daug operacijų, nes tokiu atveju būtų sukurta daug mažesnių išrašų, kuriuos galima apdoroti lygiagrečiai.</span><span class="sxs-lookup"><span data-stu-id="1f782-125">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="1f782-126">„fastTab“ **Bendra**, lauke **Numatytasis klientas**, galite pasirinkti kliento sąskaitą, skirtą naudoti pardavimui atėjusiems klientams.</span><span class="sxs-lookup"><span data-stu-id="1f782-126">In the **General** fastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  

