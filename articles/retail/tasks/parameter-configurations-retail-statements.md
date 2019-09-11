---
title: „Retail“ parametrų, kurie paveikia mažmeninės prekybos išrašus, konfigūravimas
description: Šioje temoje aptariamos „Retail“ parametrų konfigūracijos, kurios veikia, kaip kuriami ir registruojami „Retail“ išrašai.
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
ms.openlocfilehash: b9a0386a4d61395903e82d988244dd131c1febaf
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867276"
---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a><span data-ttu-id="ae48f-103">„Retail“ parametrų, kurie paveikia mažmeninės prekybos išrašus, konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ae48f-103">Configure Retail parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ae48f-104">Šioje temoje aptariamos „Retail“ parametrų konfigūracijos, kurios veikia, kaip kuriami ir registruojami „Retail“ išrašai.</span><span class="sxs-lookup"><span data-stu-id="ae48f-104">This topic demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="ae48f-105">Šioje procedūroje naudojama demonstracinė įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="ae48f-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="ae48f-106">Naršymo srityje eikite į **Moduliai > Mažmeninė prekyba ir prekyba > „Headquarters“ sąranka> Parametrai > Mažmeninės prekybos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ae48f-106">In the navigation pane, go to **Modules > Retail and commerce > Headquarters setup  > Parameters > Retail parameters**.</span></span>
2. <span data-ttu-id="ae48f-107">Pasirinkite skirtuką **Registravimas**.</span><span class="sxs-lookup"><span data-stu-id="ae48f-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="ae48f-108">Pasirinkite **Taip**, jei norite periodiškai skelbti būtent nuolaidų sumas.</span><span class="sxs-lookup"><span data-stu-id="ae48f-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="ae48f-109">Pasirinkite **Standartinis** norėdami naudoti šią funkciją numatytosioms sąskaitoms, arba pasirinkite **Periodiškai**, jei norite atskirai nurodyti, kuriai sąskaitai taikoma periodinė nuolaida.</span><span class="sxs-lookup"><span data-stu-id="ae48f-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="ae48f-110">Pasirinkite **Suvestinė**, kai norite, kad atsargų eilutės būtų bendrai sumuojamos, kai tik įmanoma.</span><span class="sxs-lookup"><span data-stu-id="ae48f-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="ae48f-111">Pasirinkite **Taip**, kai SF ir mokėjimai turi būti automatiškai vykdomi kaip dalis išrašų registravimo proceso.</span><span class="sxs-lookup"><span data-stu-id="ae48f-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="ae48f-112">Pasirinkite **Taip**, kai saugaus pristatymo operacijos turi būti sujungtos.</span><span class="sxs-lookup"><span data-stu-id="ae48f-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="ae48f-113">Pasirinkite **Taip**, kai inkasavimo operacijos turi būti sujungtos.</span><span class="sxs-lookup"><span data-stu-id="ae48f-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="ae48f-114">Pasirinkite **Taip**, kad įjungtumėte agregavimą išrašų registravimui.</span><span class="sxs-lookup"><span data-stu-id="ae48f-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="ae48f-115">Pasirinkite **Taip**, norėdami lygiagrečiai kurti ir apdoroti užsakymus, kai registruojate išrašus.</span><span class="sxs-lookup"><span data-stu-id="ae48f-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="ae48f-116">Įveskite maksimalų užsakymų, kurie bus apdoroti atliekant kiekvieną paketinę užduotį, skaičių.</span><span class="sxs-lookup"><span data-stu-id="ae48f-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="ae48f-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ae48f-117">Select **Save**.</span></span>

