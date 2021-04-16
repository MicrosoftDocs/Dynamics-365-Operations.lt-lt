---
title: Slankiojo vidurkio atsarginės savikainos seka
description: Šioje temoje pateikiama informacija apie slankiojo vidurkio skaičiavimų atsarginių savikainų sekas „Microsoft Dynamics 365 Supply Chain Management”.
author: AndersGirke
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 09da3c3a79b5540670db25d5466023132d2848f4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832279"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="417e8-103">Slankiojo vidurkio atsarginės savikainos seka</span><span class="sxs-lookup"><span data-stu-id="417e8-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="417e8-104">Vienas būdas apskaičiuoti savo atsargų savikainą yra naudoti _slankųjį vidurkį_.</span><span class="sxs-lookup"><span data-stu-id="417e8-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="417e8-105">Su kiekviena atsargų preke gali būti susietos daugiausiai trys savikainos reikšmės:</span><span class="sxs-lookup"><span data-stu-id="417e8-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="417e8-106">**Paskutinis išdavimas** – paskutinė išdavimo savikaina, priskirta prieš atsargoms tampant neigiamomis</span><span class="sxs-lookup"><span data-stu-id="417e8-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="417e8-107">**Aktyvi savikaina** – paskutinė savikaina, suaktyvinta įkainojimo versijoje</span><span class="sxs-lookup"><span data-stu-id="417e8-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="417e8-108">**Prekės kaina** – savikaina, nurodyta išleistam produktui</span><span class="sxs-lookup"><span data-stu-id="417e8-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="417e8-109">Norėdama nustatyti, kurią iš šių savikainos reikšmių naudoti slankiojo vidurkio skaičiavimuose, sistema naudoja _atsarginės savikainos seką_, kad nustatytų reikšmes prioriteto tvarka.</span><span class="sxs-lookup"><span data-stu-id="417e8-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="417e8-110">Jei pageidaujama savikainos reikšmė neprieinama, sistema naudoja sekančią pageidaujamą reikšmę ir t. t.</span><span class="sxs-lookup"><span data-stu-id="417e8-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="417e8-111">Ankstesnėse „Microsoft Dynamics 365 Supply Chain Management” versijose sistema naudojo fiksuotą atsarginės savikainos seką (_Paskutinis išdavimas, Aktyvi savikaina, Prekės kaina_).</span><span class="sxs-lookup"><span data-stu-id="417e8-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="417e8-112">10.0.11 versijoje ši seka vis dar yra numatytoji seka.</span><span class="sxs-lookup"><span data-stu-id="417e8-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="417e8-113">Tačiau, taip pat galite įjungti funkciją, leidžiančią pasirinkti iš trijų galimų atsarginių savikainų sekų.</span><span class="sxs-lookup"><span data-stu-id="417e8-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="417e8-114">Ši funkcija gali būti ypač naudinga organizacijoms, kurios reguliariai naudoja neigiamų atsargų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="417e8-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="417e8-115">Kad atsarginės savikainos sekos parinkiklis taptų pasiekiamas, jūs (arba administratorius) turite naudoti [funkcijų valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad įjungtumėte funkciją pavadinimu _Slankiojo vidurkio atsarginės savikainos seka_.</span><span class="sxs-lookup"><span data-stu-id="417e8-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="417e8-116">Norėdami pasirinkti slankiojo vidurkio skaičiavimų atsarginės savikainos seką, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="417e8-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="417e8-117">Atidarykite puslapį **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="417e8-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="417e8-118">Skirtuko **Atsargų apskaita** skyriuje **Slankusis vidurkis** nustatykite lauką **Atsarginės savikainos seka** į vieną iš toliau pateiktų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="417e8-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="417e8-119">**Paskutinis išdavimas, Aktyvi savikaina, Prekės kaina** – ši seka yra numatytoji seka.</span><span class="sxs-lookup"><span data-stu-id="417e8-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="417e8-120">Tai ta pati seka, kuri naudojama, jei funkcija _Slankiojo vidurkio atsarginės savikainos seka_ neįjungta.</span><span class="sxs-lookup"><span data-stu-id="417e8-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="417e8-121">**Aktyvi savikaina, Paskutinis leidimas**</span><span class="sxs-lookup"><span data-stu-id="417e8-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="417e8-122">**Aktyvi savikaina, Prekės kaina** – organizacijoms gali kilti našumo problemų, jei jos naudoja verslo procesus, kuriuose atsargos reguliariai tampa neigiamos, ir tuo pačiu metu yra didelis operacijų kiekis.</span><span class="sxs-lookup"><span data-stu-id="417e8-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="417e8-123">Šis parametras gali padėti sušvelninti šias našumo problemas.</span><span class="sxs-lookup"><span data-stu-id="417e8-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="417e8-124">![Atsargų apskaitos parametrai](media/inventory-accounting-parameters.png "Atsargų apskaitos parametrai")</span><span class="sxs-lookup"><span data-stu-id="417e8-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]