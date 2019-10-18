---
title: Darbo užsakymai ir ilgalaikis turtas
description: Šioje temoje aiškinami darbo užsakymai ir ilgalaikis turtas modulyje „Turto valdymas”.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250834"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="0b4be-103">Darbo užsakymai ir ilgalaikis turtas</span><span class="sxs-lookup"><span data-stu-id="0b4be-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="0b4be-104">Modulyje „Turto valdymas” turtas gali būti susietas su ilgalaikiu turtu ir tokiam turtui galite sukurti darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="0b4be-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="0b4be-105">Jei naudojate šią funkciją, galite matyti visą ilgalaikio turto, susijusių investavimo projektų ir investavimo projektuose užregistruotų išlaidų modulyje **Projektų valdymas ir apskaita** ir modulyje **Ilgalaikis turtas** vaizdą.</span><span class="sxs-lookup"><span data-stu-id="0b4be-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module.</span></span>

>[!NOTE]
><span data-ttu-id="0b4be-106">Darbo užsakymo užduoties projekto laukas **Ilgalaikio turto numeris** pildomas tik tuo atveju, jeigu darbo užsakymo užduoties projekte pasirenkamas projekto tipas „Investicija”.</span><span class="sxs-lookup"><span data-stu-id="0b4be-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![1 pav.](media/24-work-orders.png)

<span data-ttu-id="0b4be-108">Toliau nurodyta procedūra apibūdinama turto, darbo užsakymų, darbo užsakymo užduočių projektų ir ilgalaikio turto sąsaja.</span><span class="sxs-lookup"><span data-stu-id="0b4be-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="0b4be-109">Toliau pateiktame paveikslėlyje parodyta, kaip sukurti turtą, kuris siejamas su ilgalaikiu turtu.</span><span class="sxs-lookup"><span data-stu-id="0b4be-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![2 pav.](media/25-work-orders.png)

2. <span data-ttu-id="0b4be-111">Kai nustatomi darbo užsakymų tipai (**Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Darbo užsakymų tipai**), sukuriamas investicijų valdymo darbo užsakymo tipas.</span><span class="sxs-lookup"><span data-stu-id="0b4be-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="0b4be-112">Taip pat žr. [Darbo užsakymų tipai](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="0b4be-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![3 pav.](media/26-work-orders.png)

3. <span data-ttu-id="0b4be-114">Kai nustatomos darbo užsakymų projektų grupės (nuoroda **Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Projekto sąranka** > **Projektų grupė**), modulyje **Projektų valdymas ir apskaita** sukuriama investicijoms naudojamo darbo užsakymo tipo ir investicijoms sukurtos projektų grupės sąsaja (**Projektų valdymas ir apskaita** > **Sąranka** > **Registravimas** > **Projektų grupės**).</span><span class="sxs-lookup"><span data-stu-id="0b4be-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![4 pav.](media/27-work-orders.png)

4. <span data-ttu-id="0b4be-116">Kai nustatomas darbo užsakymas, susijęs su ilgalaikio turto objektu, pasirenkamas investicijų valdymo darbo užsakymo tipas, pvz., „Investicija”.</span><span class="sxs-lookup"><span data-stu-id="0b4be-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="0b4be-117">Kai sukuriamas darbo užsakymas, susijęs darbo užsakymo tipas rodomas pasirinkus **Visi darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0b4be-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![5 pav.](media/28-work-orders.png)

6. <span data-ttu-id="0b4be-119">Kai sukuriamas darbo užsakymas, su darbo užsakymu susijęs projektas sukuriamas **Projektų valdymas ir apskaita** > **Visi projektai**.</span><span class="sxs-lookup"><span data-stu-id="0b4be-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="0b4be-120">Su projektu susijusią informaciją galite rasti darbo užsakyme spustelėję nuorodą **Projekto ID** (modulyje **Turto valdymas** pasirinkite rodinį „Išsami informacija apie darbo užsakymą” > „FastTab” **Eilutės informacija** > skirtukas **Bendroji informacija** > laukas **Projekto ID**).</span><span class="sxs-lookup"><span data-stu-id="0b4be-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![6 pav.](media/29-work-orders.png)

7. <span data-ttu-id="0b4be-122">Pasirinkę **Ilgalaikis turtas**, galite pamatyti su ilgalaikiu turtu susijusių projektų apžvalgą (**Ilgalaikis turtas** > **Ilgalaikis turtas** > **Ilgalaikis turtas** > pasirinkite ilgalaikį turtą lauke **Ilgalaikio turto numeris** > peržiūrėkite turinį srityje **Susijusi informacija** > skyrius **Susiję projektai**).</span><span class="sxs-lookup"><span data-stu-id="0b4be-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

