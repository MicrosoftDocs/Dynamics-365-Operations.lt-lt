---
title: Aptarnavimo užsakymo etapai
description: Apibrėždami aptarnavimo užsakymo etapus ir juos priskirdami darbuotojams kontroliuojate aptarnavimo užsakymo eigą, sekdami užduotis, kurias aptarnavimo organizacijoje atlieka įvairūs žmonės.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b924be95c7e60598879e4d0cfd03193fe888dd7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569710"
---
# <a name="service-order-stages"></a><span data-ttu-id="18bbb-103">Aptarnavimo užsakymo etapai</span><span class="sxs-lookup"><span data-stu-id="18bbb-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="18bbb-104">Galite nustatyti aptarnavimo užsakymo etapus, kad nustatytumėte užduotis, kurias būtina atlikti, jų atlikimo tvarką ir už jų atlikimą atsakingus darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="18bbb-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="18bbb-105">Apibrėždami aptarnavimo užsakymo etapus ir juos priskirdami darbuotojams, galite kontroliuoti aptarnavimo užsakymo eigą sekdami užduotis, kurias aptarnavimo organizacijoje atlieka įvairūs žmonės.</span><span class="sxs-lookup"><span data-stu-id="18bbb-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="18bbb-106">Etapų sekoje turi būti pradinis etapas.</span><span class="sxs-lookup"><span data-stu-id="18bbb-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="18bbb-107">Taip pat galite nurodyti veiksmus, kurie leidžiami kiekviename etape.</span><span class="sxs-lookup"><span data-stu-id="18bbb-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="18bbb-108">Pvz., panaikinus visų etapų, išskyrus galutinio etapo, žymės langelio **Registravimas** žymėjimą, nebus registruojami jokie aptarnavimo užsakymai, kol aptarnavimo užsakymai nepereis visų etapų.</span><span class="sxs-lookup"><span data-stu-id="18bbb-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="18bbb-109">Skirstymas į aptarnavimo užsakymo etapus</span><span class="sxs-lookup"><span data-stu-id="18bbb-109">Branching in service order stages</span></span>

<span data-ttu-id="18bbb-110">Kai nustatote aptarnavimo etapą, galite sukurti kelis variantus arba šakas, iš kurių galima pasirinkti kitą aptarnavimo etapą.</span><span class="sxs-lookup"><span data-stu-id="18bbb-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="18bbb-111">Sukurtas šakas galima pasirinkti baigus pradinį etapą.</span><span class="sxs-lookup"><span data-stu-id="18bbb-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="18bbb-112">Pavyzdžiui, nustatėte etapą **Planavimas** kaip pradinį etapą.</span><span class="sxs-lookup"><span data-stu-id="18bbb-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="18bbb-113">Sukūrėte du etapus **Vykdoma** ir **Atšaukti**, tada pasirinkote etapą **Planavimas** kaip pirminį šių etapų etapą.</span><span class="sxs-lookup"><span data-stu-id="18bbb-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="18bbb-114">Priskyrėte etapą **Planavimas** pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="18bbb-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="18bbb-115">Baigę pardavimo užsakymo planavimo etapą galite pasirinkti etapą **Vykdoma**, jei pardavimo užsakymo galima imtis, arba galite pasirinkti etapą **Atšaukti** etapas, jei pardavimo užsakymas atšauktas.</span><span class="sxs-lookup"><span data-stu-id="18bbb-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="18bbb-116">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="18bbb-116">See also</span></span>

[<span data-ttu-id="18bbb-117">Nustatyti aptarnavimo užsakymų etapus</span><span class="sxs-lookup"><span data-stu-id="18bbb-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="18bbb-118">Aptarnavimo užsakymo etapo keitimas</span><span class="sxs-lookup"><span data-stu-id="18bbb-118">Change the service order stage</span></span>](change-service-order-stage.md)

  


