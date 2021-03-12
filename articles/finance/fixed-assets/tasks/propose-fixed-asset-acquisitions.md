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
ms.openlocfilehash: f9259c9bbf52c1c09a7092db6976fc3fabca6601
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990444"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="35e57-103">Ilgalaikio turto įsigijimų siūlymas</span><span class="sxs-lookup"><span data-stu-id="35e57-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="35e57-104">Šioje procedūroje parodoma, kaip įsigyti ilgalaikį turtą naudojant įsigijimo pasiūlymą, esantį žurnale Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="35e57-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="35e57-105">Joje naudojamas vaidmuo Buhalteris ir USMF juridinio subjekto demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="35e57-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="35e57-106">Siekiant gauti fiksuotą turtą per fiksuoto turto pasiūlymo žurnalą, pirmiausia turite sukurti fiksuoto turto įrašą ir tuomet nustatyti įsigijimo kainą turto knygoje.</span><span class="sxs-lookup"><span data-stu-id="35e57-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="35e57-107">Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="35e57-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="35e57-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="35e57-108">Select **New**.</span></span>
3. <span data-ttu-id="35e57-109">Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="35e57-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="35e57-110">Veiksmų srityje pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="35e57-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="35e57-111">Pasirinkite **Pasiūlymai**.</span><span class="sxs-lookup"><span data-stu-id="35e57-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="35e57-112">Pasirinkite **Siūlymas įsigyti**. </span><span class="sxs-lookup"><span data-stu-id="35e57-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="35e57-113">Pasirinkite **Filtruoti**.</span><span class="sxs-lookup"><span data-stu-id="35e57-113">Select **Filter**.</span></span> <span data-ttu-id="35e57-114">Spustelėkite **Nustatyti iš naujo**, kad išvalytumėte ankstesnes reikšmes.</span><span class="sxs-lookup"><span data-stu-id="35e57-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="35e57-115">Pasirinkite eilutę **Ilgalaikio turto numeris**.</span><span class="sxs-lookup"><span data-stu-id="35e57-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="35e57-116">Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="35e57-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="35e57-117">Nustatykite likusius ilgalaikio turto, kurį norite įsigyti šiuo pasiūlymu, kriterijus.</span><span class="sxs-lookup"><span data-stu-id="35e57-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="35e57-118">Norėdami išeiti iš srities, dukart pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="35e57-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="35e57-119">Patikrinkite sukurtas operacijų eilutes.</span><span class="sxs-lookup"><span data-stu-id="35e57-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="35e57-120">Įsigijimo pasiūlyme bus įtrauktas tik ilgalaikis turtas su knygoje nustatyta įsigijimo data ir įsigijimo kaina.</span><span class="sxs-lookup"><span data-stu-id="35e57-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="35e57-121">Kurkite knygas puslapyje **Knygos**.</span><span class="sxs-lookup"><span data-stu-id="35e57-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="35e57-122">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="35e57-122">Select **Post**.</span></span>
