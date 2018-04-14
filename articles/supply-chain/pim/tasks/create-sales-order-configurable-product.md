--- 
title: "Sukonfigūruoto produkto pardavimo užsakymo kūrimas"
description: "Šioje procedūroje parodoma, kaip konfigūracijos šabloną taikyti pardavimo užsakymo produktui."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: db06eef916b1298470e51b8674fc0dee15184473
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="b054b-103">Sukonfigūruoto produkto pardavimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="b054b-103">Create a sales order for a configurable product</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b054b-104">Šioje procedūroje parodoma, kaip konfigūracijos šabloną taikyti pardavimo užsakymo produktui.</span><span class="sxs-lookup"><span data-stu-id="b054b-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="b054b-105">Šiame pavyzdyje naudojamas D0006 garsiakalbio modelis demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="b054b-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="b054b-106">Paprastai šią procedūrą naudoja pardavimo užsakymų procesorius.</span><span class="sxs-lookup"><span data-stu-id="b054b-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="b054b-107">Kurti pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="b054b-107">Create a sales order</span></span>
1. <span data-ttu-id="b054b-108">Spustelėkite Pardavimo užsakymo apdorojimas ir užklausa.</span><span class="sxs-lookup"><span data-stu-id="b054b-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="b054b-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b054b-109">Click New.</span></span>
3. <span data-ttu-id="b054b-110">Spustelėkite Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="b054b-110">Click Sales order.</span></span>
4. <span data-ttu-id="b054b-111">Lauke Kliento kodas pasirinkite US-001.</span><span class="sxs-lookup"><span data-stu-id="b054b-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="b054b-112">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b054b-112">Click OK.</span></span>
6. <span data-ttu-id="b054b-113">Lauke Prekės numeris pasirinkite D0006.</span><span class="sxs-lookup"><span data-stu-id="b054b-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="b054b-114">Šiai užduočiai atlikti turite pasirinkti konfigūruojamą produktą.</span><span class="sxs-lookup"><span data-stu-id="b054b-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="b054b-115">Spustelėkite Produktas ir tiekimas.</span><span class="sxs-lookup"><span data-stu-id="b054b-115">Click Product and supply.</span></span>
8. <span data-ttu-id="b054b-116">Spustelėkite Konfigūruoti eilutę.</span><span class="sxs-lookup"><span data-stu-id="b054b-116">Click Configure line.</span></span>
    * <span data-ttu-id="b054b-117">Atkreipkite dėmesį, kad kaina buvo pakeista pagal pasirinktą konfigūraciją, o laukas Įtraukti laidą dabar yra nustatytas į parinktį True.</span><span class="sxs-lookup"><span data-stu-id="b054b-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="b054b-118">Įsiminkite pasirinktus laido parametrus ir numatytąją kainą.</span><span class="sxs-lookup"><span data-stu-id="b054b-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="b054b-119">Spustelėkite Įkelti šabloną.</span><span class="sxs-lookup"><span data-stu-id="b054b-119">Click Load template.</span></span>
    * <span data-ttu-id="b054b-120">Šiame pavyzdyje parodoma, kaip galite pritaikyti šabloną, norėdami pasirinkti iš anksto nustatytą konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="b054b-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="b054b-121">Jei naudojate šią procedūrą kaip užduočių vedlį ir norite matyti kitas atributų reikšmes, kurias galima naudoti, turite spustelėti mygtuką Atrakinti.</span><span class="sxs-lookup"><span data-stu-id="b054b-121">If you’re using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="b054b-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b054b-122">Click OK.</span></span>
11. <span data-ttu-id="b054b-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b054b-123">Click OK.</span></span>
12. <span data-ttu-id="b054b-124">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="b054b-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="b054b-125">Spustelėkite skirtuką Produktas.</span><span class="sxs-lookup"><span data-stu-id="b054b-125">Click the Product tab.</span></span>
    * <span data-ttu-id="b054b-126">Dabar prekės konfigūracija yra pateikta produkto dimensijose.</span><span class="sxs-lookup"><span data-stu-id="b054b-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="b054b-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b054b-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="b054b-128">Produkto konfigūracijos pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="b054b-128">Select the product configuration</span></span>


