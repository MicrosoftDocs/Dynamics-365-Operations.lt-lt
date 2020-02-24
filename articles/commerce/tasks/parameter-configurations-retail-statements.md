---
title: Konfigūruokite parametrus, turinčius įtakos mažmeninės prekybos teiginiams
description: Šioje temoje parodomos „Commerce“ parametrų konfigūracijos, kurios turi įtakos ataskaitų kūrimui ir paskelbimui.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023404"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="05f00-103">Konfigūruokite parametrus, turinčius įtakos mažmeninės prekybos teiginiams</span><span class="sxs-lookup"><span data-stu-id="05f00-103">Configure parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="05f00-104">Šioje temoje parodomos „Commerce“ parametrų konfigūracijos, kurios turi įtakos ataskaitų kūrimui ir paskelbimui.</span><span class="sxs-lookup"><span data-stu-id="05f00-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="05f00-105">Šioje procedūroje naudojama demonstracinė įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="05f00-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="05f00-106">Naršymo srityje eikite į **Moduliai > „Retail and Commerce“ > Būstinės sąranka > Parametrai > „Commerce“ parametrai**.</span><span class="sxs-lookup"><span data-stu-id="05f00-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="05f00-107">Pasirinkite skirtuką **Registravimas**.</span><span class="sxs-lookup"><span data-stu-id="05f00-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="05f00-108">Pasirinkite **Taip**, jei norite periodiškai skelbti būtent nuolaidų sumas.</span><span class="sxs-lookup"><span data-stu-id="05f00-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="05f00-109">Pasirinkite **Standartinis** norėdami naudoti šią funkciją numatytosioms sąskaitoms, arba pasirinkite **Periodiškai**, jei norite atskirai nurodyti, kuriai sąskaitai taikoma periodinė nuolaida.</span><span class="sxs-lookup"><span data-stu-id="05f00-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="05f00-110">Pasirinkite **Suvestinė**, kai norite, kad atsargų eilutės būtų bendrai sumuojamos, kai tik įmanoma.</span><span class="sxs-lookup"><span data-stu-id="05f00-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="05f00-111">Pasirinkite **Taip**, kai SF ir mokėjimai turi būti automatiškai vykdomi kaip dalis išrašų registravimo proceso.</span><span class="sxs-lookup"><span data-stu-id="05f00-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="05f00-112">Pasirinkite **Taip**, kai saugaus pristatymo operacijos turi būti sujungtos.</span><span class="sxs-lookup"><span data-stu-id="05f00-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="05f00-113">Pasirinkite **Taip**, kai inkasavimo operacijos turi būti sujungtos.</span><span class="sxs-lookup"><span data-stu-id="05f00-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="05f00-114">Pasirinkite **Taip**, kad įjungtumėte agregavimą išrašų registravimui.</span><span class="sxs-lookup"><span data-stu-id="05f00-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="05f00-115">Pasirinkite **Taip**, norėdami lygiagrečiai kurti ir apdoroti užsakymus, kai registruojate išrašus.</span><span class="sxs-lookup"><span data-stu-id="05f00-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="05f00-116">Įveskite maksimalų užsakymų, kurie bus apdoroti atliekant kiekvieną paketinę užduotį, skaičių.</span><span class="sxs-lookup"><span data-stu-id="05f00-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="05f00-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="05f00-117">Select **Save**.</span></span>

