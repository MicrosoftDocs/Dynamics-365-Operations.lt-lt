---
title: Ilgalaikio turto įsigijimų siūlymas
description: Šioje procedūroje parodoma, kaip įsigyti ilgalaikį turtą naudojant įsigijimo pasiūlymą, esantį žurnale Ilgalaikis turtas.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 426a5e42c1fc26958ab37eddd915334f8b0e19cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205033"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="ee6ee-103">Ilgalaikio turto įsigijimų siūlymas</span><span class="sxs-lookup"><span data-stu-id="ee6ee-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee6ee-104">Šioje procedūroje parodoma, kaip įsigyti ilgalaikį turtą naudojant įsigijimo pasiūlymą, esantį žurnale Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="ee6ee-105">Joje naudojamas vaidmuo Buhalteris ir USMF juridinio subjekto demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="ee6ee-106">Siekiant gauti fiksuotą turtą per fiksuoto turto pasiūlymo žurnalą, pirmiausia turite sukurti fiksuoto turto įrašą ir tuomet nustatyti įsigijimo kainą turto knygoje.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="ee6ee-107">Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="ee6ee-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-108">Select **New**.</span></span>
3. <span data-ttu-id="ee6ee-109">Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="ee6ee-110">Veiksmų srityje pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="ee6ee-111">Pasirinkite **Pasiūlymai**.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="ee6ee-112">Pasirinkite **Siūlymas įsigyti**. </span><span class="sxs-lookup"><span data-stu-id="ee6ee-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="ee6ee-113">Pasirinkite **Filtruoti**.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-113">Select **Filter**.</span></span> <span data-ttu-id="ee6ee-114">Spustelėkite **Nustatyti iš naujo**, kad išvalytumėte ankstesnes reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="ee6ee-115">Pasirinkite eilutę **Ilgalaikio turto numeris**.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="ee6ee-116">Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="ee6ee-117">Nustatykite likusius ilgalaikio turto, kurį norite įsigyti šiuo pasiūlymu, kriterijus.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="ee6ee-118">Norėdami išeiti iš srities, dukart pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="ee6ee-119">Patikrinkite sukurtas operacijų eilutes.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="ee6ee-120">Įsigijimo pasiūlyme bus įtrauktas tik ilgalaikis turtas su knygoje nustatyta įsigijimo data ir įsigijimo kaina.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="ee6ee-121">Kurkite knygas puslapyje **Knygos**.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="ee6ee-122">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="ee6ee-122">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]