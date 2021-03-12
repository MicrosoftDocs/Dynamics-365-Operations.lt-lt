---
title: Įtraukti skaičiavimą į produktų konfigūravimo modelį
description: Ši procedūra nurodo, kaip į produkto konfigūracijos modelį įtraukti naują skaičiavimą.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49d09a3544631960e3f6b292dbdd8927dd499f07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987059"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="109e2-103">Įtraukti skaičiavimą į produktų konfigūravimo modelį</span><span class="sxs-lookup"><span data-stu-id="109e2-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="109e2-104">Ši procedūra nurodo, kaip į produkto konfigūracijos modelį įtraukti naują skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="109e2-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="109e2-105">Joje rodoma, kaip sukurti loginę išraišką naudojant „If“ operatorių, norint nustatyti baltų garsiakalbių aukštį į 10, o visų likusių – 15.</span><span class="sxs-lookup"><span data-stu-id="109e2-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="109e2-106">Procedūros metu naudojamas aukščiausios klasės garsiakalbio komponentas demonstracinės įmonės USMF.</span><span class="sxs-lookup"><span data-stu-id="109e2-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="109e2-107">Įtraukti skaičiavimą</span><span class="sxs-lookup"><span data-stu-id="109e2-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="109e2-108">Kurti skaičiavimo išraišką</span><span class="sxs-lookup"><span data-stu-id="109e2-108">Create calculation expression</span></span>
1. <span data-ttu-id="109e2-109">Spustelėkite Redaguoti išraišką.</span><span class="sxs-lookup"><span data-stu-id="109e2-109">Click Edit expression.</span></span>
2. <span data-ttu-id="109e2-110">Lauke „ConstraintBody“ įveskite 'If[CabinetFinish=="White", 10, 15]'.</span><span class="sxs-lookup"><span data-stu-id="109e2-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="109e2-111">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="109e2-111">Click Validate.</span></span>
4. <span data-ttu-id="109e2-112">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="109e2-112">Click Close.</span></span>
5. <span data-ttu-id="109e2-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="109e2-113">Click OK.</span></span>

