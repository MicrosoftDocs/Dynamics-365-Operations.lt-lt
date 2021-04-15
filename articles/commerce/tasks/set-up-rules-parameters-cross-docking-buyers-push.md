---
title: Nustatyti prekių skirstymo ir skirstymo pirkėjams taisykles ir parametrus
description: Ši procedūra nurodo veiksmus, skirtus papildymo taisyklėms kurti.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2d8e561273c2a573182259c2ceb45cebc072eca
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804166"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="8ea33-103">Nustatyti prekių skirstymo ir skirstymo pirkėjams taisykles ir parametrus</span><span class="sxs-lookup"><span data-stu-id="8ea33-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ea33-104">Ši procedūra nurodo veiksmus, skirtus papildymo taisyklėms kurti.</span><span class="sxs-lookup"><span data-stu-id="8ea33-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="8ea33-105">Papildymo taisykles galima naudoti, norint valdyti, kaip produktai yra paskirstomi į parduotuves, kai naudojamas prekių skirstymas ir skirstymas pirkėjams.</span><span class="sxs-lookup"><span data-stu-id="8ea33-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="8ea33-106">Galima nustatyti parduotuvių arba parduotuvių grupių papildymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="8ea33-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="8ea33-107">Kiekvienos eilutės svoris, nurodytas taisyklėje, lems, kaip produktų kiekiai bus paskirstyti parduotuvėse naudojant papildymo taisykles kaip prekių skirstymo arba skirstymo pirkėjams skirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="8ea33-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="8ea33-108">Šioje procedūroje naudojama demonstracinė įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="8ea33-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="8ea33-109">Pasirinkite Papildymo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="8ea33-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="8ea33-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8ea33-110">Click New.</span></span>
3. <span data-ttu-id="8ea33-111">Lauke Papildymo taisyklė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8ea33-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="8ea33-112">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8ea33-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8ea33-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8ea33-113">Click Save.</span></span>
6. <span data-ttu-id="8ea33-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8ea33-114">Click Add.</span></span>
7. <span data-ttu-id="8ea33-115">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8ea33-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8ea33-116">Galite pasirinkti tipą Papildymo hierarchija arba Kanalas.</span><span class="sxs-lookup"><span data-stu-id="8ea33-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="8ea33-117">Reikšmė nulemia, ar pasirinkimas lauke Pavadinimas bus kanalų hierarchija, ar konkretus kanalas.</span><span class="sxs-lookup"><span data-stu-id="8ea33-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="8ea33-118">Pavyzdžiui, nustatykite papildymo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="8ea33-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="8ea33-119">Lauke Pavadinimas pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8ea33-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="8ea33-120">Numatytoji svorio vertė įvedama naudojant sandėlio nurodytą svorį.</span><span class="sxs-lookup"><span data-stu-id="8ea33-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="8ea33-121">Šią vertę galite naudoti papildymo taisyklėje arba lauke Svoris galite įvesti naują svorį.</span><span class="sxs-lookup"><span data-stu-id="8ea33-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="8ea33-122">Lauke Svoris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8ea33-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="8ea33-123">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8ea33-123">Click Add.</span></span>
11. <span data-ttu-id="8ea33-124">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8ea33-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="8ea33-125">Lauke Tipas pasirinkite „Kanalas“ .</span><span class="sxs-lookup"><span data-stu-id="8ea33-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="8ea33-126">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8ea33-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="8ea33-127">Lauke Svoris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8ea33-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="8ea33-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8ea33-128">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]