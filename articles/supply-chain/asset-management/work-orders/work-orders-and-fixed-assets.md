---
title: Darbo užsakymai ir ilgalaikis turtas
description: Šioje temoje aiškinami darbo užsakymai ir ilgalaikis turtas modulyje „Turto valdymas”.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 678bfae5d0b4ea469a91fc89306be40c39cb082d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223439"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="130cf-103">Darbo užsakymai ir ilgalaikis turtas</span><span class="sxs-lookup"><span data-stu-id="130cf-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="130cf-104">Modulyje „Turto valdymas” turtas gali būti susietas su ilgalaikiu turtu ir tokiam turtui galite sukurti darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="130cf-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="130cf-105">Naudodamiesi šiomis funkcijomis galite gauti išsamią ilgalaikio turto, susijusių investicijų projektų ir investiciniuose projektuose registruotų išlaidų apžvalgą moduliuose **Projektų valdymas ir apskaita** ir **Ilgalaikis turtas**, esančiuose „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="130cf-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="130cf-106">Darbo užsakymo užduoties projekto laukas **Ilgalaikio turto numeris** nurodomas tik tuo atveju, jeigu darbo užsakymo užduoties projekte pasirenkamas projekto tipas **Investicija**.</span><span class="sxs-lookup"><span data-stu-id="130cf-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="130cf-107">Toliau pateiktame paveikslėlyje parodytas ryšys tarp investicijų projekto modulyje **Projektų valdymas ir apskaita** ir darbo užsakymo užduoties projekto.</span><span class="sxs-lookup"><span data-stu-id="130cf-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![1 pav.](media/24-work-orders.png)

<span data-ttu-id="130cf-109">Toliau nurodyta procedūra apibūdinama turto, darbo užsakymų, darbo užsakymo užduočių projektų ir ilgalaikio turto sąsaja.</span><span class="sxs-lookup"><span data-stu-id="130cf-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="130cf-110">Kuriate turtą, kurį susiejate su ilgalaikiu turtu.</span><span class="sxs-lookup"><span data-stu-id="130cf-110">You create an asset that you relate to a fixed asset.</span></span>

![2 pav.](media/25-work-orders.png)

2. <span data-ttu-id="130cf-112">Kai puslapyje **Darbo užsakymų tipai** nustatote darbo užsakymų tipus (**Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Darbo užsakymų tipai**), kuriate darbo užsakymo tipą darbui su investicijomis.</span><span class="sxs-lookup"><span data-stu-id="130cf-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="130cf-113">Taip pat žr. [Darbo užsakymų tipai](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="130cf-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![3 pav.](media/26-work-orders.png)

3. <span data-ttu-id="130cf-115">Kai darbo užsakymų projektų grupes nustatote skirtuke **Projektų grupė**, esančiame puslapyje **Darbo užsakymo projekto sąranka** (**Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Projekto nustatymai**), kuriate ryšį tarp investicijoms naudojamo darbo užsakymo tipo ir projektų grupės, sukurtos investicijoms puslapyje **Projektų grupės**, priklausančiame moduliui **Projektų valdymas ir apskaita** (**Projektų valdymas ir apskaita** > **Sąranka** > **Registravimas** > **Projektų grupės**).</span><span class="sxs-lookup"><span data-stu-id="130cf-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![4 pav.](media/27-work-orders.png)

4. <span data-ttu-id="130cf-117">Kai kuriate darbo užsakymą, susijusį su ilgalaikiu turtu, pasirenkate darbui su investicijomis naudojamą darbo užsakymo tipą, pvz., **Investicija**.</span><span class="sxs-lookup"><span data-stu-id="130cf-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="130cf-118">Sukūrus darbo užsakymą, susijęs darbo užsakymo tipas rodomas puslapyje **Visi darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="130cf-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![5 pav.](media/28-work-orders.png)

6. <span data-ttu-id="130cf-120">Sukūrus darbo užsakymą, projektas, susijęs su darbo užsakymu, sukuriamas puslapyje **Visi projektai**, priklausančiame moduliui **Projektų valdymas ir apskaita** (**Projektų valdymas ir apskaita** > **Projektai** > **Visi projektai**).</span><span class="sxs-lookup"><span data-stu-id="130cf-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="130cf-121">Norėdami peržiūrėti su projektu susijusią informaciją, pasirinkite saitą lauke **Projekto ID**, esančiame skirtuke **Bendra**, „FastTab“ **Eilutės informacija**, puslapio **Visi darbo užsakymai** informacijos rodinyje, modulyje **Turto valdymas** (**Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Visi darbo užsakymai**).</span><span class="sxs-lookup"><span data-stu-id="130cf-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![6 pav.](media/29-work-orders.png)

7. <span data-ttu-id="130cf-123">Norėdami peržiūrėti projektus, susijusius su ilgalaikiu turtu, pasirinkite **Ilgalaikis turtas** > **Ilgalaikis turtas** > **Ilgalaikis turtas**, o tada lauke **Ilgalaikio turto numeris** pasirinkite ilgalaikio turto saitą, kad atidarytumėte informacijos rodinį.</span><span class="sxs-lookup"><span data-stu-id="130cf-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="130cf-124">Išskleiskite dešinėje puslapio pusėje esančią sritį **Susijusi informacija** ir pasirinkite „FastTab“ **Susiję projektai**.</span><span class="sxs-lookup"><span data-stu-id="130cf-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]