---
title: Ilgalaikio turto priedo įvedimas
description: Ši procedūra parodo, kaip prie esamo ilgalaikio turto pridėti priedą.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: baac842660b6231529349ec97bcdbcdb971a0ac0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975971"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="80b02-103">Ilgalaikio turto priedo įvedimas</span><span class="sxs-lookup"><span data-stu-id="80b02-103">Enter an addition to a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="80b02-104">Ši procedūra parodo, kaip prie esamo ilgalaikio turto pridėti priedą.</span><span class="sxs-lookup"><span data-stu-id="80b02-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="80b02-105">Ilgalaikio turto priedų paskirtis yra sekti prekių priedus, priežiūrą ar turto tobulinimus ir yra tik informacinė.</span><span class="sxs-lookup"><span data-stu-id="80b02-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="80b02-106">Bet kokius ilgalaikio turto vertės arba dėvėjimo laiko pakeitimus reikia atlikti atskirai.</span><span class="sxs-lookup"><span data-stu-id="80b02-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   

<span data-ttu-id="80b02-107">Ši procedūra naudoja vaidmenį Buhalteris ir USMF juridinio subjekto demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="80b02-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="80b02-108">Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Ilgalaikis turtas > Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="80b02-108">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="80b02-109">Sąraše raskite ir pasirinkite ilgalaikį turtą, kuriam skirtas priedas.</span><span class="sxs-lookup"><span data-stu-id="80b02-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="80b02-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="80b02-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="80b02-111">Veiksmų srityje spustelėkite **Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="80b02-111">On the Action Pane, click **Fixed asset**.</span></span>
5. <span data-ttu-id="80b02-112">Spustelėkite **Ilgalaikio turto papildymai**.</span><span class="sxs-lookup"><span data-stu-id="80b02-112">Click **Fixed asset additions**.</span></span>
6. <span data-ttu-id="80b02-113">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="80b02-113">Click **New**.</span></span>
7. <span data-ttu-id="80b02-114">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="80b02-114">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="80b02-115">Lauke **„Įsigijimo data“** nustatykite papildomo pirkimo arba aptarnavimo datą.</span><span class="sxs-lookup"><span data-stu-id="80b02-115">In the **Acquisition date** field, set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="80b02-116">**Vieneto kaina** įveskite prekės, priežiūros arba kito turto patobulinimo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="80b02-116">In the **Unit cost** field, enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="80b02-117">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="80b02-117">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="80b02-118">Bendra išlaidų suma ilgalaikio turto vertei įtakos neturės ir yra skirta tik sekimo ir informaciniams tikslams.</span><span class="sxs-lookup"><span data-stu-id="80b02-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="80b02-119">Jei išlaidos bus kapitalizuotos, tada reikia atskirai registruoti vertės didinimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="80b02-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="80b02-120">Spustelėkite skirtuką **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="80b02-120">Click the **General** tab.</span></span>

    * <span data-ttu-id="80b02-121">Jei priedas pailgina turto dėvėjimo laiką, nustatykite **Padidina dėvėjimo laiką** parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="80b02-121">Set **Increases service life** to **Yes** if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="80b02-122">Šis laukas skirtas tik informacijai.</span><span class="sxs-lookup"><span data-stu-id="80b02-122">This field is informational only.</span></span> <span data-ttu-id="80b02-123">Norėdami pailginti dėvėjimo laiką, modifikuokite dėvėjimo laiką, nurodytą turto vertinimo modeliuose ir (arba) nusidėvėjimo knygose.</span><span class="sxs-lookup"><span data-stu-id="80b02-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  

