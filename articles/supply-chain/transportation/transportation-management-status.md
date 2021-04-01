---
title: Gabenimo valdymo būsenos
description: Šioje temoje paaiškinta, kaip sukurti gabenimo būseną ir žemėlapį, kuris nurodo vežėjo būseną.
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
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: fb0d98729046330037f96ab7e13a1bf897e35a1e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233348"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="08c29-103">Gabenimo valdymo būsenos</span><span class="sxs-lookup"><span data-stu-id="08c29-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08c29-104">Nustatykite pagrindinius kodus gabenimo būsenoms, kad interpretuotumėte kodus, kurie pateikti jūsų gabenimo vežėjų.</span><span class="sxs-lookup"><span data-stu-id="08c29-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="08c29-105">Jis leidžia jums integruoti su gabenimo vežėjais siekiant suteikti būseną.</span><span class="sxs-lookup"><span data-stu-id="08c29-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="08c29-106">Gabenimo būsena, kurią pateikiate gabenimo pagrindinės būsenos koduis, jums padeda sekti krovinio, siuntimo ar talpos būseną.</span><span class="sxs-lookup"><span data-stu-id="08c29-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="08c29-107">Konkreti gabenimo būsena kroviniui, siuntimui ar talpyklai gali būti naujinama per duomenų integravimą, o ne rankiniu būdu per vartotojo sąsają.</span><span class="sxs-lookup"><span data-stu-id="08c29-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="08c29-108">Sukurkite gabenimo būseną</span><span class="sxs-lookup"><span data-stu-id="08c29-108">Create a transportation status</span></span>

<span data-ttu-id="08c29-109">Norėdami sukurti gabenimo būseną, atlikite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="08c29-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="08c29-110">Eikite į **Gabenimo valdymas \> Nustatymai \> Gabenimo būsenos pagrindiniai duomenys**.</span><span class="sxs-lookup"><span data-stu-id="08c29-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="08c29-111">Pasirinkite **Naujas**, kad sukurtumėte gabenimo būsenos pagrindinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="08c29-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="08c29-112">Laukelyje **Gabenimo būsenos pagrindiniai duomenys** įveskite unikalų kodą gabenimo būsenai.</span><span class="sxs-lookup"><span data-stu-id="08c29-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="08c29-113">Laukelyje **Gabenimo tipas** pasirinkite  *Siunčiantis vežėjas* ar *Centras* kaip gabenimo tipą.</span><span class="sxs-lookup"><span data-stu-id="08c29-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="08c29-114">Įveskite gabenimo būseną ir pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="08c29-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="08c29-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="08c29-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="08c29-116">Sudarykite gabenimo būsenos žemėlapį vežėjo būsenai</span><span class="sxs-lookup"><span data-stu-id="08c29-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="08c29-117">Siekiant sudaryti gabenimo būsenos žemėlapį vežėjo būsenai, elkitės taip:</span><span class="sxs-lookup"><span data-stu-id="08c29-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="08c29-118">Eikite į **Gabenimo valdymas \> Nustatymai \> Vežėjai \> Vežėjo gabenimo būsena**.</span><span class="sxs-lookup"><span data-stu-id="08c29-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="08c29-119">Rinkitės **Naujas** siekiant sudaryti žemėlapį kodui iš gabenimo vežėjo į gabenimo būsenos pagrindinį kodą.</span><span class="sxs-lookup"><span data-stu-id="08c29-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="08c29-120">Pasirinkite unikalų ID gabenimo vežėjui ir vežėjo paslaugoms.</span><span class="sxs-lookup"><span data-stu-id="08c29-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="08c29-121">Pasirinkite gabenimo būsenos kodą, kuriam norite sudaryti žemėlapį ir pasirinkti gabenimo vežėjo kodą.</span><span class="sxs-lookup"><span data-stu-id="08c29-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="08c29-122">Įveskite išorės kodą, kurį naudoja gabenimo vežėjas.</span><span class="sxs-lookup"><span data-stu-id="08c29-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="08c29-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="08c29-123">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]