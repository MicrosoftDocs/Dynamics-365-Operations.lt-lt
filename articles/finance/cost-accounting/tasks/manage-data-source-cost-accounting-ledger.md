---
title: Tvarkyti savikainos apskaitos didžiosios knygos duomenų šaltinį
description: Naudokite šią procedūrą, norėdami valdyti didžiosios knygos duomenų šaltinį savikainos apskaitos didžiajai knygai.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMAXGeneralLedgerEntryProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7246d42b42404f0f1215bbf14b8ad168fe12691c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990722"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="87a92-103">Tvarkyti savikainos apskaitos didžiosios knygos duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="87a92-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="87a92-104">Naudokite šią procedūrą, norėdami valdyti didžiosios knygos duomenų šaltinį savikainos apskaitos didžiajai knygai.</span><span class="sxs-lookup"><span data-stu-id="87a92-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="87a92-105">Prieš atlikdami šią užduotį įsitikinkite, kad leidžiate „Sukurkite savikainos apskaitos didžiąją knygą“ ir „Apibrėžkite savikainos kontrolės įtaisus“ užduoties nuorodas.</span><span class="sxs-lookup"><span data-stu-id="87a92-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="87a92-106">Šiame įraše naudojama demonstracinių duomenų įmonė USP2.</span><span class="sxs-lookup"><span data-stu-id="87a92-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="87a92-107">Eikite į Savikainos apskaita > Didžiosios knygos nustatymas > Savikainos apskaitos didžiosios knygos.</span><span class="sxs-lookup"><span data-stu-id="87a92-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="87a92-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="87a92-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="87a92-109">Spustelėkite Faktinės versijos.</span><span class="sxs-lookup"><span data-stu-id="87a92-109">Click Actual versions.</span></span>
4. <span data-ttu-id="87a92-110">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="87a92-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="87a92-111">Spustelėkite Didžioji knyga.</span><span class="sxs-lookup"><span data-stu-id="87a92-111">Click General ledger.</span></span>
6. <span data-ttu-id="87a92-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="87a92-112">Click New.</span></span>
7. <span data-ttu-id="87a92-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87a92-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="87a92-114">Lauke Duomenų teikėjas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87a92-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="87a92-115">Šiam pavyzdžiui pasirinkite Dynamics 365 Finance – Didžiosios knygos įrašai.</span><span class="sxs-lookup"><span data-stu-id="87a92-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="87a92-116">Lauke Savikainos elementų dimensija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87a92-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="87a92-117">Šiam pavyzdžiui pasirinkite Išlaidų elementai.</span><span class="sxs-lookup"><span data-stu-id="87a92-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="87a92-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="87a92-118">Click Save.</span></span>
11. <span data-ttu-id="87a92-119">Spustelėkite Konfigūruoti duomenų teikėją.</span><span class="sxs-lookup"><span data-stu-id="87a92-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="87a92-120">Lauke Juridinis subjektas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87a92-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="87a92-121">Šiame pavyzdyje pasirinkite „USP2“.</span><span class="sxs-lookup"><span data-stu-id="87a92-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="87a92-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="87a92-122">Click New.</span></span>
14. <span data-ttu-id="87a92-123">Lauke Registravimo sluoksnis pasirinkite Dabartinis.</span><span class="sxs-lookup"><span data-stu-id="87a92-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="87a92-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="87a92-124">Click OK.</span></span>

