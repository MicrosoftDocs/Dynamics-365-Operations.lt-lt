---
title: Tvarkyti savikainos apskaitos didžiosios knygos duomenų šaltinį
description: Naudokite šią procedūrą, norėdami valdyti didžiosios knygos duomenų šaltinį savikainos apskaitos didžiajai knygai.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMAXGeneralLedgerEntryProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da4d351f4bce6494a107a55895866e4d3d43953f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841074"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="e82fa-103">Tvarkyti savikainos apskaitos didžiosios knygos duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="e82fa-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e82fa-104">Naudokite šią procedūrą, norėdami valdyti didžiosios knygos duomenų šaltinį savikainos apskaitos didžiajai knygai.</span><span class="sxs-lookup"><span data-stu-id="e82fa-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="e82fa-105">Prieš atlikdami šią užduotį įsitikinkite, kad leidžiate „Sukurkite savikainos apskaitos didžiąją knygą“ ir „Apibrėžkite savikainos kontrolės įtaisus“ užduoties nuorodas.</span><span class="sxs-lookup"><span data-stu-id="e82fa-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="e82fa-106">Šiame įraše naudojama demonstracinių duomenų įmonė USP2.</span><span class="sxs-lookup"><span data-stu-id="e82fa-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="e82fa-107">Eikite į Savikainos apskaita > Didžiosios knygos nustatymas > Savikainos apskaitos didžiosios knygos.</span><span class="sxs-lookup"><span data-stu-id="e82fa-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="e82fa-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="e82fa-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e82fa-109">Spustelėkite Faktinės versijos.</span><span class="sxs-lookup"><span data-stu-id="e82fa-109">Click Actual versions.</span></span>
4. <span data-ttu-id="e82fa-110">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="e82fa-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="e82fa-111">Spustelėkite Didžioji knyga.</span><span class="sxs-lookup"><span data-stu-id="e82fa-111">Click General ledger.</span></span>
6. <span data-ttu-id="e82fa-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e82fa-112">Click New.</span></span>
7. <span data-ttu-id="e82fa-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e82fa-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="e82fa-114">Lauke Duomenų teikėjas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e82fa-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="e82fa-115">Šiam pavyzdžiui pasirinkite Dynamics 365 Finance – Didžiosios knygos įrašai.</span><span class="sxs-lookup"><span data-stu-id="e82fa-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="e82fa-116">Lauke Savikainos elementų dimensija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e82fa-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="e82fa-117">Šiam pavyzdžiui pasirinkite Išlaidų elementai.</span><span class="sxs-lookup"><span data-stu-id="e82fa-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="e82fa-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="e82fa-118">Click Save.</span></span>
11. <span data-ttu-id="e82fa-119">Spustelėkite Konfigūruoti duomenų teikėją.</span><span class="sxs-lookup"><span data-stu-id="e82fa-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="e82fa-120">Lauke Juridinis subjektas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e82fa-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="e82fa-121">Šiame pavyzdyje pasirinkite „USP2“.</span><span class="sxs-lookup"><span data-stu-id="e82fa-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="e82fa-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e82fa-122">Click New.</span></span>
14. <span data-ttu-id="e82fa-123">Lauke Registravimo sluoksnis pasirinkite Dabartinis.</span><span class="sxs-lookup"><span data-stu-id="e82fa-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="e82fa-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e82fa-124">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]