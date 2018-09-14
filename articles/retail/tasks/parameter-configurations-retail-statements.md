--- 
title: " Mažmeninės prekybos išrašų parametrų konfigūracijos"
description: "Ši procedūra nurodo mažmeninės prekybos parametrų konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami mažmeninės prekybos išrašai."
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6dacd2b80ca0d51d81d2bdf5bc2636b47da621ee
ms.contentlocale: lt-lt
ms.lasthandoff: 09/14/2018

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="44f5b-103"> Mažmeninės prekybos išrašų parametrų konfigūracijos</span><span class="sxs-lookup"><span data-stu-id="44f5b-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="44f5b-104">Ši procedūra nurodo mažmeninės prekybos parametrų konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami mažmeninės prekybos išrašai.</span><span class="sxs-lookup"><span data-stu-id="44f5b-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="44f5b-105">Šioje procedūroje naudojama demonstracinė įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="44f5b-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="44f5b-106">Pasirinkite Mažmeninė prekyba ir prekyba > „Headquarters“ sąranka > Parametrai > Mažmeninės prekybos parametrai.</span><span class="sxs-lookup"><span data-stu-id="44f5b-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="44f5b-107">Spustelėkite skirtuką Registravimas.</span><span class="sxs-lookup"><span data-stu-id="44f5b-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="44f5b-108">Pasirinkite „Taip“, jei norite konkrečiai registruoti laikotarpio nuolaidos sumas.</span><span class="sxs-lookup"><span data-stu-id="44f5b-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="44f5b-109">Pasirinkite „Standartinė“, jei norite naudoti numatytąsias sąskaitas, arba pasirinkite „Laikotarpio“, jei norite nurodyti, kurią kiekvienos laikotarpio nuolaidos sąskaitą naudoti.</span><span class="sxs-lookup"><span data-stu-id="44f5b-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="44f5b-110">Pasirinkite „Suvestinė“, jei norite sujungti atsargų eilutes, kai įmanoma.</span><span class="sxs-lookup"><span data-stu-id="44f5b-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="44f5b-111">Pasirinkite „Taip“, jei SF ir mokėjimai turėtų būti automatiškai sudengti kaip išrašų registravimo proceso dalis.</span><span class="sxs-lookup"><span data-stu-id="44f5b-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="44f5b-112">Pasirinkite „Taip“, jei norite sujungti pinigų įnešimo į įmonės kasą operacijas.</span><span class="sxs-lookup"><span data-stu-id="44f5b-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="44f5b-113">Pasirinkite „Taip“, jei norite sujungti inkasavimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="44f5b-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="44f5b-114">Pasirinkite „Taip“, norėdami įjungti išrašų registravimo telkimą.</span><span class="sxs-lookup"><span data-stu-id="44f5b-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="44f5b-115">Pasirinkite „Taip“, norėdami kurti ir apdoroti užsakymus, kai registruojate išrašus.</span><span class="sxs-lookup"><span data-stu-id="44f5b-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="44f5b-116">Įveskite maksimalų užsakymų, kurie bus apdoroti atliekant kiekvieną paketinę užduotį, skaičių.</span><span class="sxs-lookup"><span data-stu-id="44f5b-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="44f5b-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="44f5b-117">Click Save.</span></span>


