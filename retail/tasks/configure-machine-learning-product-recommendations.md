--- 
title: " Mašininiu mokymu pagrįstų produktų rekomendacijų konfigūravimas"
description: "Atliekant šią procedūrą atnaujinami duomenys objektų saugykloje, kurią naudoja mašininio mokymo sistema, teikianti produktų rekomendacijas, ir tada EKA klientams įjungiama produktų rekomendacijų funkcija."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e32c7cf1283487cb7a52f7d8e261b6b587b76364
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="d566d-103"> Mašininiu mokymu pagrįstų produktų rekomendacijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="d566d-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d566d-104">Atliekant šią procedūrą atnaujinami duomenys objektų saugykloje, kurią naudoja mašininio mokymo sistema, teikianti produktų rekomendacijas, ir tada EKA klientams įjungiama produktų rekomendacijų funkcija.</span><span class="sxs-lookup"><span data-stu-id="d566d-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="d566d-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="d566d-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="d566d-106">Atidarykite Sistemos administravimas > Nustatymai > Objektų saugykla.</span><span class="sxs-lookup"><span data-stu-id="d566d-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="d566d-107">Sąraše raskite ir pasirinkite įrašą RetailSales.</span><span class="sxs-lookup"><span data-stu-id="d566d-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="d566d-108">Spustelėkite Atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="d566d-108">Click Refresh.</span></span>
4. <span data-ttu-id="d566d-109">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d566d-109">Click OK.</span></span>
5. <span data-ttu-id="d566d-110">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d566d-110">Close the page.</span></span>
6. <span data-ttu-id="d566d-111">Pasirinkite Mažmeninė prekyba ir prekyba > „Headquarters“ sąranka > Parametrai > Mažmeninės prekybos parametrai.</span><span class="sxs-lookup"><span data-stu-id="d566d-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="d566d-112">Spustelėkite skirtuką Mašininis mokymas.</span><span class="sxs-lookup"><span data-stu-id="d566d-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="d566d-113">Lauke Įjungti produktų rekomendacijas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="d566d-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="d566d-114">Jei rodomas pranešimas „Rekomendacijų modelių nepavyko nuskaityti“, taip greičiausiai yra todėl, kad neseniai atnaujinote objektų saugyklą ir sistema dar nebaigė sieti naujų duomenų.</span><span class="sxs-lookup"><span data-stu-id="d566d-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="d566d-115">Palaukite 2–3 valandas ir bandykite dar kartą.</span><span class="sxs-lookup"><span data-stu-id="d566d-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="d566d-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d566d-116">Click Save.</span></span>
10. <span data-ttu-id="d566d-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d566d-117">Close the page.</span></span>


