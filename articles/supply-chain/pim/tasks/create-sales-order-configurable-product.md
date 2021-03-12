---
title: Sukonfigūruoto produkto pardavimo užsakymo kūrimas
description: Šioje procedūroje parodoma, kaip konfigūracijos šabloną taikyti pardavimo užsakymo produktui.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77404694b3426f9ef051721191b607f91c908cc4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992325"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="ac4ba-103">Sukonfigūruoto produkto pardavimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="ac4ba-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac4ba-104">Šioje procedūroje parodoma, kaip konfigūracijos šabloną taikyti pardavimo užsakymo produktui.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="ac4ba-105">Šiame pavyzdyje naudojamas D0006 garsiakalbio modelis demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="ac4ba-106">Paprastai šią procedūrą naudoja pardavimo užsakymų procesorius.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="ac4ba-107">Kurti pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="ac4ba-107">Create a sales order</span></span>
1. <span data-ttu-id="ac4ba-108">Spustelėkite Pardavimo užsakymo apdorojimas ir užklausa.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="ac4ba-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-109">Click New.</span></span>
3. <span data-ttu-id="ac4ba-110">Spustelėkite Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-110">Click Sales order.</span></span>
4. <span data-ttu-id="ac4ba-111">Lauke Kliento kodas pasirinkite US-001.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="ac4ba-112">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-112">Click OK.</span></span>
6. <span data-ttu-id="ac4ba-113">Lauke Prekės numeris pasirinkite D0006.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="ac4ba-114">Šiai užduočiai atlikti turite pasirinkti konfigūruojamą produktą.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="ac4ba-115">Spustelėkite Produktas ir tiekimas.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-115">Click Product and supply.</span></span>
8. <span data-ttu-id="ac4ba-116">Spustelėkite Konfigūruoti eilutę.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-116">Click Configure line.</span></span>
    * <span data-ttu-id="ac4ba-117">Atkreipkite dėmesį, kad kaina buvo pakeista pagal pasirinktą konfigūraciją, o laukas Įtraukti laidą dabar yra nustatytas į parinktį True.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="ac4ba-118">Įsiminkite pasirinktus laido parametrus ir numatytąją kainą.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="ac4ba-119">Spustelėkite Įkelti šabloną.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-119">Click Load template.</span></span>
    * <span data-ttu-id="ac4ba-120">Šiame pavyzdyje parodoma, kaip galite pritaikyti šabloną, norėdami pasirinkti iš anksto nustatytą konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="ac4ba-121">Jei naudojate šią procedūrą kaip užduočių vedlį ir norite matyti kitas atributų reikšmes, kurias galima naudoti, turite spustelėti mygtuką Atrakinti.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="ac4ba-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-122">Click OK.</span></span>
11. <span data-ttu-id="ac4ba-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-123">Click OK.</span></span>
12. <span data-ttu-id="ac4ba-124">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="ac4ba-125">Spustelėkite skirtuką Produktas.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-125">Click the Product tab.</span></span>
    * <span data-ttu-id="ac4ba-126">Dabar prekės konfigūracija yra pateikta produkto dimensijose.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="ac4ba-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ac4ba-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="ac4ba-128">Produkto konfigūracijos pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="ac4ba-128">Select the product configuration</span></span>

