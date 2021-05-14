---
title: Sukonfigūruoto produkto pardavimo užsakymo kūrimas
description: Šioje procedūroje parodoma, kaip konfigūracijos šabloną taikyti pardavimo užsakymo produktui.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921294"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="e5196-103">Sukonfigūruoto produkto pardavimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="e5196-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5196-104">Šioje procedūroje parodoma, kaip konfigūracijos šabloną taikyti pardavimo užsakymo produktui.</span><span class="sxs-lookup"><span data-stu-id="e5196-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="e5196-105">Šiame pavyzdyje naudojamas D0006 garsiakalbio modelis demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="e5196-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="e5196-106">Paprastai šią procedūrą naudoja pardavimo užsakymų procesorius.</span><span class="sxs-lookup"><span data-stu-id="e5196-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="e5196-107">Kurti pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="e5196-107">Create a sales order</span></span>

1. <span data-ttu-id="e5196-108">Eikite **į pardavimo ir rinkodaros darbo sričių pardavimo užsakymo \> \> apdorojimą ir užklausą**.</span><span class="sxs-lookup"><span data-stu-id="e5196-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="e5196-109">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e5196-109">Select **New**.</span></span>
1. <span data-ttu-id="e5196-110">Pasirinkite **Pardavimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="e5196-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="e5196-111">Lauke **Kliento kodas** pasirinkite *„US-001”*.</span><span class="sxs-lookup"><span data-stu-id="e5196-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="e5196-112">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e5196-112">Select **OK**.</span></span>
1. <span data-ttu-id="e5196-113">Lauke **Prekės numeris** pasirinkite *D0006*.</span><span class="sxs-lookup"><span data-stu-id="e5196-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="e5196-114">Šiai užduočiai atlikti turite pasirinkti konfigūruojamą produktą.</span><span class="sxs-lookup"><span data-stu-id="e5196-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="e5196-115">Rinkitės **Produktas ir tiekimas**.</span><span class="sxs-lookup"><span data-stu-id="e5196-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="e5196-116">Pasirinkite **Eilutės konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="e5196-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="e5196-117">Atkreipkite dėmesį, kad kaina buvo pakeista pagal pasirinktą konfigūraciją, o laukas Įtraukt **laidą** laukelis dabar nustatytas į parinktį *Teisnga*.</span><span class="sxs-lookup"><span data-stu-id="e5196-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="e5196-118">Įsiminkite pasirinktus laido parametrus ir numatytąją kainą.</span><span class="sxs-lookup"><span data-stu-id="e5196-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="e5196-119">Pasirinkite **Įkelti šabloną**.</span><span class="sxs-lookup"><span data-stu-id="e5196-119">Select **Load template**.</span></span>
    * <span data-ttu-id="e5196-120">Šiame pavyzdyje parodoma, kaip galite pritaikyti šabloną, norėdami pasirinkti iš anksto nustatytą konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="e5196-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="e5196-121">Jei naudojate šią procedūrą kaip užduočių vedlį ir norite matyti kitas atributų reikšmes, kurias galima naudoti, turite spustelėti mygtuką **Atrakinti**.</span><span class="sxs-lookup"><span data-stu-id="e5196-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="e5196-122">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e5196-122">Select **OK**.</span></span>
1. <span data-ttu-id="e5196-123">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e5196-123">Select **OK**.</span></span>
1. <span data-ttu-id="e5196-124">Išplėskite skyrių **Eilutės informacija** section.</span><span class="sxs-lookup"><span data-stu-id="e5196-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="e5196-125">Produkto **skirtuko** pasirinkimas.</span><span class="sxs-lookup"><span data-stu-id="e5196-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="e5196-126">Dabar prekės konfigūracija yra pateikta produkto dimensijose.</span><span class="sxs-lookup"><span data-stu-id="e5196-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="e5196-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e5196-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]