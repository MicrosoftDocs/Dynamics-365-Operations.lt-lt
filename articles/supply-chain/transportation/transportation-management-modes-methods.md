---
title: Gabenimo valdymo būdai ir metodai
description: Šioje temoje parodyta, kaip nustatyti gabenimo valdymo būdus ir metodus.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b9b548212c6f1f3faac56cd7ca182d84cc339bd2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973915"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="a50a1-103">Gabenimo valdymo būdai ir metodai</span><span class="sxs-lookup"><span data-stu-id="a50a1-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a50a1-104">Gabenimo valdymo būdas parodo gabenimo tipą, kurį vežėjas naudoja krovinių pristatymams, tokius kaip mažesnis nei krovinys (LT), sunkvežimis (TL) ar dalinis.</span><span class="sxs-lookup"><span data-stu-id="a50a1-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="a50a1-105">Gabenimo metodas parodo gabenimo formą, kurią vežėjas naudoja krovinių pristatymui, tokį kaip oras, žemės, vandenynas ar geležinkelis.</span><span class="sxs-lookup"><span data-stu-id="a50a1-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="a50a1-106">Būdai ir gabenimo metodai yra naudojami keliuose kontekstuose.</span><span class="sxs-lookup"><span data-stu-id="a50a1-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="a50a1-107">Tik būdai yra naudojami maršruto planavimuose, o būdai ir gabenimo metodai yra naudojami nustatant siuntimo vežėjus ir vežėjų paslaugas.</span><span class="sxs-lookup"><span data-stu-id="a50a1-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="a50a1-108">Tarp gabenimo metodų ir būdų nėra jokios aiškios hierarchijos ir santykių.</span><span class="sxs-lookup"><span data-stu-id="a50a1-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="a50a1-109">Sukurit būdą</span><span class="sxs-lookup"><span data-stu-id="a50a1-109">Create a mode</span></span>

<span data-ttu-id="a50a1-110">Norėdami sukurti būdą, atlikite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="a50a1-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="a50a1-111">Eikite į **Transportavimo valdymas \> Sąranka \> Vežėjai \> Būdas**.</span><span class="sxs-lookup"><span data-stu-id="a50a1-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="a50a1-112">Pasirinkite **Naujas**, kad sukurtumėte naują būdą.</span><span class="sxs-lookup"><span data-stu-id="a50a1-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="a50a1-113">Įveskite unikalų ID ir būdo pavadinimo aprašą.</span><span class="sxs-lookup"><span data-stu-id="a50a1-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="a50a1-114">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a50a1-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="a50a1-115">Sukurkite gabenimo metodą</span><span class="sxs-lookup"><span data-stu-id="a50a1-115">Create a transportation method</span></span>

<span data-ttu-id="a50a1-116">Norėdami sukurti gabenimo metodą, atlikite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="a50a1-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="a50a1-117">Eikite į **Gabenimo valdymas \> Nustatymai \> Vežėjai \> Gabenimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="a50a1-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="a50a1-118">Pasirinkite **Naujas**, kad sukurtumėte naują gabenimo metodą.</span><span class="sxs-lookup"><span data-stu-id="a50a1-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="a50a1-119">Įveskite unikalų ID ir būdo pavadinimo aprašą gabenimo metodui.</span><span class="sxs-lookup"><span data-stu-id="a50a1-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="a50a1-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a50a1-120">Close the page.</span></span>
