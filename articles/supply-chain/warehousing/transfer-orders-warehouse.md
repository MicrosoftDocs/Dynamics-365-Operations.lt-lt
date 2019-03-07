---
title: Sandėlių perkėlimo užsakymų nustatymas
description: Šioje temoje aprašoma, kaip galite nustatyti sandėlių perkėlimo užsakymus.
author: Mirzaab
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 8111601cb2948c66097b0f5b2f261b7462b279f9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "337468"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="dedf6-103">Sandėlių perkėlimo užsakymų nustatymas</span><span class="sxs-lookup"><span data-stu-id="dedf6-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dedf6-104">Kurdami hierarchiją, palaikančią perkėlimo iš vieno sandėlio į kitą užsakymus, galite naudoti sandėlio lygius.</span><span class="sxs-lookup"><span data-stu-id="dedf6-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="dedf6-105">Šiuo nustatymu paremtas bendrasis planavimas apskaičiuoja atskiro sandėlio lygio prekių poreikį ir nustatytame pagrindiniame sandėlyje sugeneruoja suplanuotus perkėlimo užsakymus, kad būtų galima juos vykdyti.</span><span class="sxs-lookup"><span data-stu-id="dedf6-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="dedf6-106">Spustelėkite **Atsargų valdymas > Sąranka > Atsargų paskirstymas > Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="dedf6-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="dedf6-107">Pasirinkite norimą papildyti sandėlį.</span><span class="sxs-lookup"><span data-stu-id="dedf6-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="dedf6-108">„FastTab“ **Bendrasis planavimas** pasirinkite žymės langelį **Papildymas**.</span><span class="sxs-lookup"><span data-stu-id="dedf6-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="dedf6-109">Lauke **Pagrindinis sandėlis** pasirinkite sandėlį, kurį norite nustatyti kaip pildomą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="dedf6-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="dedf6-110">Bendrasis planavimas apskaičiuoja, kokį kiekį perkelti į pasirinktą sandėlį, ir naudodamas objektą **Pagrindinis sandėlis** sugeneruoja suplanuotą perkėlimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="dedf6-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="dedf6-111">Jei žymės langelis <STRONG>Papildymas</STRONG> išvalomas, pasirinktam sandėliui priskiriamas su parinktimi <STRONG>Pagrindinis sandėlis</STRONG> susietas sandėlio lygis, tačiau <STRONG>Pagrindinis sandėlis</STRONG> nenustatomas kaip papildymo sandėlis.</span><span class="sxs-lookup"><span data-stu-id="dedf6-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="dedf6-112">Uždarykite puslapį, kad būtų pritaikytas naujas nustatymas.</span><span class="sxs-lookup"><span data-stu-id="dedf6-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="dedf6-113">Jei norite priskirti papildymo sandėlį, prieš tai formoje puslapyje <STRONG>Saugojimo dimensijų grupės</STRONG> turite nustatyti saugojimo dimensiją kaip atsargų dimensiją.</span><span class="sxs-lookup"><span data-stu-id="dedf6-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="dedf6-114">Šiame puslapyje pasirinkite sandėlio lauką <STRONG>Aktyvus</STRONG> ir lauką <STRONG>Padengimo planas dimensijomis</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="dedf6-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="dedf6-115">Transportavimo vykdymo laiko nustatymas</span><span class="sxs-lookup"><span data-stu-id="dedf6-115">Set up transport lead time</span></span>

<span data-ttu-id="dedf6-116">Turite taip pat nustatyti transportavimo tarp sandėlių vykdymo laiką puslapyje **Transportavimo dienos**.</span><span class="sxs-lookup"><span data-stu-id="dedf6-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="dedf6-117">Pasirinkite **Atsargų valdymas > Sąranka > Paskirstymas > Transportavimo dienos**.</span><span class="sxs-lookup"><span data-stu-id="dedf6-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="dedf6-118">Lauke **Gavimo vieta** pasirinkite **sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="dedf6-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="dedf6-119">Pasirinkite **Siuntimo sandėlis**, **Gavimo sandėlis** ir **Transportavimo dienos**.</span><span class="sxs-lookup"><span data-stu-id="dedf6-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="dedf6-120">(Pasirinktinai) Taip pat galite nustatyti transportavimo laiką, atsižvelgdami į pristatymo būdą, skirtuke **Transportavimo dienos pagal pristatymo būdą**.</span><span class="sxs-lookup"><span data-stu-id="dedf6-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>
