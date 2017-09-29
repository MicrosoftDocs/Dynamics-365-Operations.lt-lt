--- 
title: "Įtraukti skaičiavimą į produktų konfigūravimo modelį"
description: "Ši procedūra nurodo, kaip į produkto konfigūracijos modelį įtraukti naują skaičiavimą."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2db8fb922b085a7f118822ef4fd974ac338f4d99
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="b1ad3-103">Įtraukti skaičiavimą į produktų konfigūravimo modelį</span><span class="sxs-lookup"><span data-stu-id="b1ad3-103">Add a calculation to a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1ad3-104">Ši procedūra nurodo, kaip į produkto konfigūracijos modelį įtraukti naują skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="b1ad3-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="b1ad3-105">Joje rodoma, kaip sukurti loginę išraišką naudojant „If“ operatorių, norint nustatyti baltų garsiakalbių aukštį į 10, o visų likusių – 15.</span><span class="sxs-lookup"><span data-stu-id="b1ad3-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="b1ad3-106">Procedūros metu naudojamas aukščiausios klasės garsiakalbio komponentas demonstracinės įmonės USMF.</span><span class="sxs-lookup"><span data-stu-id="b1ad3-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="b1ad3-107">Įtraukti skaičiavimą</span><span class="sxs-lookup"><span data-stu-id="b1ad3-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="b1ad3-108">Kurti skaičiavimo išraišką</span><span class="sxs-lookup"><span data-stu-id="b1ad3-108">Create calculation expression</span></span>
1. <span data-ttu-id="b1ad3-109">Spustelėkite Redaguoti išraišką.</span><span class="sxs-lookup"><span data-stu-id="b1ad3-109">Click Edit expression.</span></span>
2. <span data-ttu-id="b1ad3-110">Lauke „ConstraintBody“ įveskite 'If[CabinetFinish=="White", 10, 15]'.</span><span class="sxs-lookup"><span data-stu-id="b1ad3-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="b1ad3-111">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="b1ad3-111">Click Validate.</span></span>
4. <span data-ttu-id="b1ad3-112">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="b1ad3-112">Click Close.</span></span>
5. <span data-ttu-id="b1ad3-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b1ad3-113">Click OK.</span></span>


