--- 
title: "Likviduoti ilgalaikį turtą naudojant laisvos formos SF"
description: "Šioje procedūroje parodoma, kaip įsigyti ilgalaikį turtą naudojant įsigijimo pasiūlymą, esantį žurnale Ilgalaikis turtas."
author: saraschi2
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: bf449be5f9b79c1e6bf7d9a5dd6d7cdede20eea9
ms.contentlocale: lt-lt
ms.lasthandoff: 09/11/2018

---
# <a name="dispose-of-a-fixed-asset-using-a-free-text-invoice"></a><span data-ttu-id="a038f-103">Likviduoti ilgalaikį turtą naudojant laisvos formos SF</span><span class="sxs-lookup"><span data-stu-id="a038f-103">Dispose of a fixed asset using a free text invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a038f-104">Šioje procedūroje parodoma, kaip įsigyti ilgalaikį turtą naudojant įsigijimo pasiūlymą, esantį žurnale Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="a038f-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="a038f-105">Joje naudojamas vaidmuo Buhalteris ir USMF juridinio subjekto demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="a038f-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="a038f-106">Eikite į Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas.</span><span class="sxs-lookup"><span data-stu-id="a038f-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="a038f-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a038f-107">Click New.</span></span>
3. <span data-ttu-id="a038f-108">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a038f-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="a038f-109">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="a038f-109">Click Lines.</span></span>
5. <span data-ttu-id="a038f-110">Spustelėkite Pasiūlymai.</span><span class="sxs-lookup"><span data-stu-id="a038f-110">Click Proposals.</span></span>
6. <span data-ttu-id="a038f-111">Spustelėkite Įsigijimo pasiūlymas.</span><span class="sxs-lookup"><span data-stu-id="a038f-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="a038f-112">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="a038f-112">Click Filter.</span></span>
8. <span data-ttu-id="a038f-113">Spustelėkite Nustatyti iš naujo, kad išvalytumėte ankstesnes reikšmes.</span><span class="sxs-lookup"><span data-stu-id="a038f-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="a038f-114">Pasirinkite eilutę Ilgalaikio turto numeris.</span><span class="sxs-lookup"><span data-stu-id="a038f-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="a038f-115">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a038f-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="a038f-116">Nustatykite likusius ilgalaikio turto, kurį norite įsigyti šiuo pasiūlymu, kriterijus.</span><span class="sxs-lookup"><span data-stu-id="a038f-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="a038f-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a038f-117">Click OK.</span></span>
12. <span data-ttu-id="a038f-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a038f-118">Click OK.</span></span>
    * <span data-ttu-id="a038f-119">Patikrinkite sukurtas operacijų eilutes.</span><span class="sxs-lookup"><span data-stu-id="a038f-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="a038f-120">Įsigijimo pasiūlyme bus įtrauktas tik ilgalaikis turtas su knygoje nustatyta įsigijimo data ir įsigijimo kaina.</span><span class="sxs-lookup"><span data-stu-id="a038f-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="a038f-121">Spustelėkite skirtuką Knygos.</span><span class="sxs-lookup"><span data-stu-id="a038f-121">Click the Books tab.</span></span>
14. <span data-ttu-id="a038f-122">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="a038f-122">Click Post.</span></span>


