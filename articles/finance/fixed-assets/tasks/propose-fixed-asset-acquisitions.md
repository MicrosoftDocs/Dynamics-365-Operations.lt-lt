---
title: Ilgalaikio turto įsigijimų siūlymas
description: Šioje procedūroje parodoma, kaip įsigyti ilgalaikį turtą naudojant įsigijimo pasiūlymą, esantį žurnale Ilgalaikis turtas.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e08177aad2db2438c2d5d4ddd294c1056b88167c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142736"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="95d4e-103">Ilgalaikio turto įsigijimų siūlymas</span><span class="sxs-lookup"><span data-stu-id="95d4e-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95d4e-104">Šioje procedūroje parodoma, kaip įsigyti ilgalaikį turtą naudojant įsigijimo pasiūlymą, esantį žurnale Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="95d4e-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="95d4e-105">Joje naudojamas vaidmuo Buhalteris ir USMF juridinio subjekto demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="95d4e-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="95d4e-106">Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="95d4e-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="95d4e-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="95d4e-107">Select **New**.</span></span>
3. <span data-ttu-id="95d4e-108">Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="95d4e-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="95d4e-109">Veiksmų srityje pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="95d4e-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="95d4e-110">Pasirinkite **Pasiūlymai**.</span><span class="sxs-lookup"><span data-stu-id="95d4e-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="95d4e-111">Pasirinkite **Siūlymas įsigyti**. </span><span class="sxs-lookup"><span data-stu-id="95d4e-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="95d4e-112">Pasirinkite **Filtruoti**.</span><span class="sxs-lookup"><span data-stu-id="95d4e-112">Select **Filter**.</span></span> <span data-ttu-id="95d4e-113">Spustelėkite **Nustatyti iš naujo**, kad išvalytumėte ankstesnes reikšmes.</span><span class="sxs-lookup"><span data-stu-id="95d4e-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="95d4e-114">Pasirinkite eilutę **Ilgalaikio turto numeris**.</span><span class="sxs-lookup"><span data-stu-id="95d4e-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="95d4e-115">Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="95d4e-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="95d4e-116">Nustatykite likusius ilgalaikio turto, kurį norite įsigyti šiuo pasiūlymu, kriterijus.</span><span class="sxs-lookup"><span data-stu-id="95d4e-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="95d4e-117">Norėdami išeiti iš srities, dukart pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="95d4e-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="95d4e-118">Patikrinkite sukurtas operacijų eilutes.</span><span class="sxs-lookup"><span data-stu-id="95d4e-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="95d4e-119">Įsigijimo pasiūlyme bus įtrauktas tik ilgalaikis turtas su knygoje nustatyta įsigijimo data ir įsigijimo kaina.</span><span class="sxs-lookup"><span data-stu-id="95d4e-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="95d4e-120">Kurkite knygas puslapyje **Knygos**.</span><span class="sxs-lookup"><span data-stu-id="95d4e-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="95d4e-121">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="95d4e-121">Select **Post**.</span></span>

