---
title: Nustatyti tranzito punktų papildomų paslaugų išlaidas ir papildomų paslaugų šablonus
description: Ši procedūra nurodo, kaip sukurti tranzito punkto papildomų paslaugų šabloną ir jį panaudoti tranzito punkto papildomų paslaugų mokesčiui sukurti.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2e9125c7a38d1dc5e6866a056fb71f25e40928
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233684"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="fc86b-103">Nustatyti tranzito punktų papildomų paslaugų išlaidas ir papildomų paslaugų šablonus</span><span class="sxs-lookup"><span data-stu-id="fc86b-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fc86b-104">Ši procedūra nurodo, kaip sukurti tranzito punkto papildomų paslaugų šabloną ir jį panaudoti tranzito punkto papildomų paslaugų mokesčiui sukurti.</span><span class="sxs-lookup"><span data-stu-id="fc86b-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="fc86b-105">Procedūra naudoja USMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="fc86b-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="fc86b-106">Šį nustatymą paprastai atlieka transportavimo koordinatorius.</span><span class="sxs-lookup"><span data-stu-id="fc86b-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="fc86b-107">Pagrindinio tranzito punkto nustatymas</span><span class="sxs-lookup"><span data-stu-id="fc86b-107">Set up a hub master</span></span>
1. <span data-ttu-id="fc86b-108">Pasirinkite Transportavimo valdymas > Nustatymas > Vertinimas > Papildomų paslaugų šablonai.</span><span class="sxs-lookup"><span data-stu-id="fc86b-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="fc86b-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fc86b-109">Click New.</span></span>
3. <span data-ttu-id="fc86b-110">Lauke „Papildomų paslaugų šablonas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fc86b-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="fc86b-111">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fc86b-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="fc86b-112">Lauke „Papildomų paslaugų tipas“ pasirinkite „Tranzito punktas“.</span><span class="sxs-lookup"><span data-stu-id="fc86b-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="fc86b-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="fc86b-113">Click Save.</span></span>
7. <span data-ttu-id="fc86b-114">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fc86b-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="fc86b-115">Nustatyti tranzito punkto papildomų paslaugų mokestį</span><span class="sxs-lookup"><span data-stu-id="fc86b-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="fc86b-116">Pasirinkite Transportavimo valdymas > Nustatymas > Vertinimas > Tranzito punkto papildomų paslaugų mokesčiai.</span><span class="sxs-lookup"><span data-stu-id="fc86b-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="fc86b-117">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fc86b-117">Click New.</span></span>
3. <span data-ttu-id="fc86b-118">Lauke „Tranzito punkto papildomų paslaugų ID“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fc86b-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="fc86b-119">Lauke „Tranzito punktas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="fc86b-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="fc86b-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="fc86b-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="fc86b-121">Lauke „Tranzito punkto padėtis“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="fc86b-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="fc86b-122">Galite sukurti mokestį už paėmimą arba atidavimą.</span><span class="sxs-lookup"><span data-stu-id="fc86b-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="fc86b-123">Atsižvelgiant į jūsų pasirinkimą, mokestis bus taikomas atitinkamam transportavimo segmentui jūsų maršrute.</span><span class="sxs-lookup"><span data-stu-id="fc86b-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="fc86b-124">Lauke „Papildomų paslaugų šablonas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="fc86b-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="fc86b-125">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="fc86b-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fc86b-126">Pasirinkite šabloną, kurį ką tik sukurėte.</span><span class="sxs-lookup"><span data-stu-id="fc86b-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="fc86b-127">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="fc86b-127">Click Save.</span></span>
10. <span data-ttu-id="fc86b-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fc86b-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]