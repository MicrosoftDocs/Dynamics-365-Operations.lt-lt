---
title: " Mašininiu mokymu pagrįstų produktų rekomendacijų konfigūravimas"
description: Atliekant šią procedūrą atnaujinami duomenys objektų saugykloje, kurią naudoja mašininio mokymo sistema, teikianti produktų rekomendacijas, ir tada EKA klientams įjungiama produktų rekomendacijų funkcija.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BIMeasurementDeployManagementEntityStore, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 700af913f18e23c66db53a92033def06818af1ec
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "348531"
---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="18c17-103"> Mašininiu mokymu pagrįstų produktų rekomendacijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="18c17-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="18c17-104">Atliekant šią procedūrą atnaujinami duomenys objektų saugykloje, kurią naudoja mašininio mokymo sistema, teikianti produktų rekomendacijas, ir tada EKA klientams įjungiama produktų rekomendacijų funkcija.</span><span class="sxs-lookup"><span data-stu-id="18c17-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="18c17-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="18c17-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="18c17-106">Atidarykite Sistemos administravimas > Nustatymai > Objektų saugykla.</span><span class="sxs-lookup"><span data-stu-id="18c17-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="18c17-107">Sąraše raskite ir pasirinkite įrašą RetailSales.</span><span class="sxs-lookup"><span data-stu-id="18c17-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="18c17-108">Spustelėkite Atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="18c17-108">Click Refresh.</span></span>
4. <span data-ttu-id="18c17-109">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="18c17-109">Click OK.</span></span>
5. <span data-ttu-id="18c17-110">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="18c17-110">Close the page.</span></span>
6. <span data-ttu-id="18c17-111">Pasirinkite Mažmeninė prekyba ir prekyba > „Headquarters“ sąranka > Parametrai > Mažmeninės prekybos parametrai.</span><span class="sxs-lookup"><span data-stu-id="18c17-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="18c17-112">Spustelėkite skirtuką Mašininis mokymas.</span><span class="sxs-lookup"><span data-stu-id="18c17-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="18c17-113">Lauke Įjungti produktų rekomendacijas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="18c17-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="18c17-114">Jei rodomas pranešimas „Rekomendacijų modelių nepavyko nuskaityti“, taip greičiausiai yra todėl, kad neseniai atnaujinote objektų saugyklą ir sistema dar nebaigė sieti naujų duomenų.</span><span class="sxs-lookup"><span data-stu-id="18c17-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="18c17-115">Palaukite 2–3 valandas ir bandykite dar kartą.</span><span class="sxs-lookup"><span data-stu-id="18c17-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="18c17-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="18c17-116">Click Save.</span></span>
10. <span data-ttu-id="18c17-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="18c17-117">Close the page.</span></span>

