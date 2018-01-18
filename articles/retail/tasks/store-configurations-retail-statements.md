--- 
title: " Mažmeninės prekybos išrašų parduotuvės konfigūracijos"
description: "Ši procedūra nurodo mažmeninės prekybos parduotuvės konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami mažmeninės prekybos išrašai."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 96aff33904c1de4a8b2642890eba7bf854d8e0c1
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="837ca-103"> Mažmeninės prekybos išrašų parduotuvės konfigūracijos</span><span class="sxs-lookup"><span data-stu-id="837ca-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="837ca-104">Ši procedūra nurodo mažmeninės prekybos parduotuvės konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami mažmeninės prekybos išrašai.</span><span class="sxs-lookup"><span data-stu-id="837ca-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="837ca-105">Mažmeninės prekybos parduotuvių finansinės dimensijos aprašytos kitoje procedūroje.</span><span class="sxs-lookup"><span data-stu-id="837ca-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="837ca-106">Šioje procedūroje naudojama demonstracinė įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="837ca-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="837ca-107">Eikite į Mažmeninė prekyba ir prekyba > Kanalai > Mažmeninės prekybos parduotuvės > Visos mažmeninės prekybos parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="837ca-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="837ca-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="837ca-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="837ca-109">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="837ca-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="837ca-110">Sekcijos Išrašas / uždarymas parametrai turi įtakos kuriant, tvirtinant ir registruojant parduotuvės išrašus.</span><span class="sxs-lookup"><span data-stu-id="837ca-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="837ca-111">Atidarykite sekciją Išrašas / uždarymas.</span><span class="sxs-lookup"><span data-stu-id="837ca-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="837ca-112">Pasirinkite būdą, kuriuo norite grupuoti išrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="837ca-112">Select the method you want to use to group the statement lines by.</span></span>  
    * <span data-ttu-id="837ca-113">Pasirinkite „Taip“, jei per dieną turi būti kuriamas tik vienas išrašas, kai išrašai kuriami atliekant išrašų kūrimo paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="837ca-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="837ca-114">Laukas Mokėjimo priemonių deklaravimo skaičiavimas nurodo, ar mokėjimo priemonių deklaravimai turi būti įtraukti kartu, ar paskutinysis turėtų būti naudojamas.</span><span class="sxs-lookup"><span data-stu-id="837ca-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="837ca-115">Pasirinkite, į kurią DK sąskaitą registruoti apvalinimo skirtumus.</span><span class="sxs-lookup"><span data-stu-id="837ca-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="837ca-116">Lauke Didžiausias apvalinimo skirtumas galite įvesti didžiausią galimą apvalinimo skirtumą.</span><span class="sxs-lookup"><span data-stu-id="837ca-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="837ca-117">Lauke Registravimas galite įvesti bendrą didžiausią galimą išrašo registravimo skirtumą.</span><span class="sxs-lookup"><span data-stu-id="837ca-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="837ca-118">Lauke Pamaina galite įvesti bendrą didžiausią galimą išrašo pamainos skirtumą.</span><span class="sxs-lookup"><span data-stu-id="837ca-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="837ca-119">Lauke Operacija galite įvesti bendrą didžiausią galimą išrašo eilutės skirtumą.</span><span class="sxs-lookup"><span data-stu-id="837ca-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="837ca-120">Lauke Uždarymo metodas galite nurodyti, ar operacijos, kurios bus įtrauktos į išrašą, turėtų būti uždarytos pamainos dalis, ar jos gali būti bet kurios nurodytos datos / laiko intervalo operacijos.</span><span class="sxs-lookup"><span data-stu-id="837ca-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="837ca-121">Lauke Darbo dienos pabaiga galite įvesti laiką, jei po vidurnakčio atliktos operacijos turėtų būti registruojamos su ankstesnės dienos data.</span><span class="sxs-lookup"><span data-stu-id="837ca-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="837ca-122">Pasirinkite „Taip“, jei po vidurnakčio atliktos operacijos turėtų būti registruojamos kaip ankstesnės dienos operacijos.</span><span class="sxs-lookup"><span data-stu-id="837ca-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="837ca-123">Pasirinkite „Taip“, jei norite, kad būtų sukurti kiekvieno nurodyto išrašo metodo išrašai.</span><span class="sxs-lookup"><span data-stu-id="837ca-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="837ca-124">Tai gali būti naudinga, jei registravimo efektyvumą reikia tobulinti parduotuvėse, kuriose atliekama daug operacijų, nes tokiu atveju būtų sukurta daug mažesnių išrašų, kuriuos galima apdoroti lygiagrečiai.</span><span class="sxs-lookup"><span data-stu-id="837ca-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="837ca-125">Lauke Numatytasis klientas galite pasirinkti kliento sąskaitą, skirtą naudoti pardavimo operacijose su į parduotuvę atėjusiais klientais.</span><span class="sxs-lookup"><span data-stu-id="837ca-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


