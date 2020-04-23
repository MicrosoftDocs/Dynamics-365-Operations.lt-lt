---
title: Konteinerio svorio ir tūrio įtraukimas kraunant
description: Šioje temoje aprašoma, kaip nustatyti ir taikyti funkciją, kurią naudojant būtų galima įtraukti krovinių konteinerių svorį ir tūrį.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e6b29bf2e42ea2df3d36f39fa577078009aa584
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206293"
---
# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="530bf-103">Konteinerio svorio ir tūrio įtraukimas kraunant</span><span class="sxs-lookup"><span data-stu-id="530bf-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="530bf-104">Naudojant krovinio konteinerių svorio ir tūrio įtraukimo funkciją, aiškiai perteikiamas bendrasis į krovinį perkeliamų konteinerių ir prekių svoris bei tūris.</span><span class="sxs-lookup"><span data-stu-id="530bf-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="530bf-105">Krovinyje yra viena siunta arba kelios siuntos, o jose yra atskirų prekių, priklausančių vienam pardavimo užsakymui arba keliems pardavimo užsakymams.</span><span class="sxs-lookup"><span data-stu-id="530bf-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="530bf-106">Prekės saugomos konteineryje, o konteineriai pakraunami į krovinį.</span><span class="sxs-lookup"><span data-stu-id="530bf-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="530bf-107">Ne konteineryje esančios prekės taip pat gali būti krovinio dalis.</span><span class="sxs-lookup"><span data-stu-id="530bf-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="530bf-108">Pagal šias sąlygas sistema apskaičiuoja krovinio svorio ir tūrio reikšmes, atsižvelgdama į tiek konteinerių, tiek prekių svorį bei tūrį.</span><span class="sxs-lookup"><span data-stu-id="530bf-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="530bf-109">Jei apskaičiuotos reikšmės nėra tikslios, jas galite pakoreguoti įvesdami faktines krovinio svorio ir tūrio reikšmes.</span><span class="sxs-lookup"><span data-stu-id="530bf-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="530bf-110">Svorio ir tūrio reikšmės naudojamos vykdant transportavimo valdymo procesus.</span><span class="sxs-lookup"><span data-stu-id="530bf-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="530bf-111">Pavyzdžiui, šios reikšmės naudojamos tarifo ir maršruto darbo srityje, kurioje jos padeda apibrėžti krovinių tarifą ir maršrutą; reikšmės taip pat naudojamos su transportavimo mokėjimo priemonėmis ir registruojant vairuotojus.</span><span class="sxs-lookup"><span data-stu-id="530bf-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="530bf-112">Kai taikoma</span><span class="sxs-lookup"><span data-stu-id="530bf-112">Where it applies</span></span>

<span data-ttu-id="530bf-113">Krovinio konteinerių svorio ir tūrio įtraukimo funkcija taikoma vykdant transportavimo valdymo procesus, pvz., tarifo ir maršruto darbo srityje, su transportavimo mokėjimo priemonėmis ir registruojant vairuotojus.</span><span class="sxs-lookup"><span data-stu-id="530bf-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="530bf-114">Kaip tai nustatoma</span><span class="sxs-lookup"><span data-stu-id="530bf-114">How it is set up</span></span>

<span data-ttu-id="530bf-115">Kiek konteinerių turėtų reikėti kroviniui, apskaičiuojama pagal konteinerio svorį bei tūrį ir pagal konteinerio naudojimo procentą.</span><span class="sxs-lookup"><span data-stu-id="530bf-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="530bf-116">Norėdami nustatyti konteinerio svorį ir tūrį, spustelėkite **Sandėlio valdymas** \> **Sąranka** \> **Konteineriai** \> **Konteinerių tipai**.</span><span class="sxs-lookup"><span data-stu-id="530bf-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="530bf-117">Norėdami nustatyti konteinerio naudojimo procentą, spustelėkite **Sandėlio valdymas** \> **Sąranka** \> **Konteineriai** \> **Konteinerių grupės** ir lauke **Konteinerio naudojimo procentas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="530bf-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>
