---
title: Galima atsiskaityti už prekes, kurių nėra atsargose
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti klientams įtraukti ne atsargose esančias prekes į savo krepšelį ir vykdyti pirkimo užbaigimą.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6df9c77248c7f4e16765b98327fe5838f0fce7e4
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585445"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="75ce8-103">Galima atsiskaityti už prekes, kurių nėra atsargose</span><span class="sxs-lookup"><span data-stu-id="75ce8-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75ce8-104">Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti klientams įtraukti ne atsargose esančias prekes į savo krepšelį ir vykdyti pirkimo užbaigimą.</span><span class="sxs-lookup"><span data-stu-id="75ce8-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="75ce8-105">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="75ce8-105">Description</span></span>

<span data-ttu-id="75ce8-106">Vartotojai gali įtraukti prekę į savo krepšelį, net jei parduotuvėje nėra turimų atsargų, o tada pereiti į pirkimo užbaigimo puslapį.</span><span class="sxs-lookup"><span data-stu-id="75ce8-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="75ce8-107">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="75ce8-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="75ce8-108">„Commerce” svetainių daryklėje įjungti ypatybę Rodyti neturimų atsargų klaidas</span><span class="sxs-lookup"><span data-stu-id="75ce8-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="75ce8-109">Norėdami „Commerce” svetainių daryklėje įjungti ypatybę **Rodyti neturimų atsargų klaidas**, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="75ce8-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="75ce8-110">Pasirinkite svetainę, su kuria dirbate.</span><span class="sxs-lookup"><span data-stu-id="75ce8-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="75ce8-111">Kairiojoje naršymo srityje pasirinkite **Puslapiai**.</span><span class="sxs-lookup"><span data-stu-id="75ce8-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="75ce8-112">Pasirinkite **Krepšelio puslapis**, kad jį atidarytumėte.</span><span class="sxs-lookup"><span data-stu-id="75ce8-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="75ce8-113">Pasirinkite vietą **Krepšelis 1**, pasirinkite **Redaguoti**, tada ypatybių srityje pažymėkite žymės langelį **Rodyti neturimų atsargų klaidas**.</span><span class="sxs-lookup"><span data-stu-id="75ce8-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="75ce8-114">Įrašykite ir publikuokite puslapį.</span><span class="sxs-lookup"><span data-stu-id="75ce8-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75ce8-115">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="75ce8-115">Additional resources</span></span>

[<span data-ttu-id="75ce8-116">Atsargų parametrų taikymas</span><span class="sxs-lookup"><span data-stu-id="75ce8-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="75ce8-117">Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas</span><span class="sxs-lookup"><span data-stu-id="75ce8-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="75ce8-118">Atsargų buferių ir atsargų lygių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="75ce8-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
