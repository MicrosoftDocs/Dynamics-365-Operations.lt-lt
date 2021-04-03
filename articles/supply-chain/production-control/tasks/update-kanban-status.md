---
title: „Kanban“ būsenos naujinimas
description: Kai per klaidą ištuštinamas „kanban‟ arba reikia ištuštinti gautą „kanban“, turite atnaujinti „kanban“ būseną.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 055765452579b1de74f1c2158de9c6cb4ee80f16
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252827"
---
# <a name="update-kanban-status"></a><span data-ttu-id="c7f88-103">„Kanban“ būsenos naujinimas</span><span class="sxs-lookup"><span data-stu-id="c7f88-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7f88-104">Kai per klaidą ištuštinamas „kanban‟ arba reikia ištuštinti gautą „kanban“, turite atnaujinti „kanban“ būseną.</span><span class="sxs-lookup"><span data-stu-id="c7f88-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="c7f88-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="c7f88-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c7f88-106">Ši procedūra yra skirta parduotuvės prižiūrėtojui.</span><span class="sxs-lookup"><span data-stu-id="c7f88-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="c7f88-107">Suraskite „kanban“.</span><span class="sxs-lookup"><span data-stu-id="c7f88-107">Find the kanban.</span></span>
1. <span data-ttu-id="c7f88-108">Pasirinkite Gamybos kontrolė > Kanban > Kanban.</span><span class="sxs-lookup"><span data-stu-id="c7f88-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="c7f88-109">Atidarykite stulpelio filtrą Sandėliavimo vieneto būsena.</span><span class="sxs-lookup"><span data-stu-id="c7f88-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="c7f88-110">Spustelėkite Valyti.</span><span class="sxs-lookup"><span data-stu-id="c7f88-110">Click Clear.</span></span>
    * <span data-ttu-id="c7f88-111">Taip grąžinami filtrai.</span><span class="sxs-lookup"><span data-stu-id="c7f88-111">This resets the filters.</span></span>  
4. <span data-ttu-id="c7f88-112">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="c7f88-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c7f88-113">Pvz., filtruokite lauką Kortelės numeris reikšme „000149“.</span><span class="sxs-lookup"><span data-stu-id="c7f88-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="c7f88-114">Būsenos „ištuštintas‟ keitimas į „gautas‟</span><span class="sxs-lookup"><span data-stu-id="c7f88-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="c7f88-115">Spustelėkite Atšaukti tuščią sandėliavimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="c7f88-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="c7f88-116">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c7f88-116">Click OK.</span></span>
    * <span data-ttu-id="c7f88-117">Atkreipkite dėmesį, kad sandėliavimo vieneto būsena yra Gautas.</span><span class="sxs-lookup"><span data-stu-id="c7f88-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="c7f88-118">Būsenos „gautas‟ keitimas į „ištuštintas‟</span><span class="sxs-lookup"><span data-stu-id="c7f88-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="c7f88-119">Spustelėkite Ištuštinti „kanban“.</span><span class="sxs-lookup"><span data-stu-id="c7f88-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="c7f88-120">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c7f88-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c7f88-121">Atkreipkite dėmesį, kad sandėliavimo vieneto būsena yra Ištuštintas.</span><span class="sxs-lookup"><span data-stu-id="c7f88-121">Notice that the Handling unit status is Emptied.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]