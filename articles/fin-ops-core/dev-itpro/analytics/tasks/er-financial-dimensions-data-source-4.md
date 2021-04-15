---
title: 'ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (4 dalis – Ataskaitos vykdymas)'
description: Šioje temoje aprašoma, kaip konfigūruoti elektroninės ataskaitos (ER) modelį, kad būtų galima naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį. (4 dalis)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a06936da71d7b05f312a99c8c11d148403d29c3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752393"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="fe443-104">ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (4 dalis – Ataskaitos vykdymas)</span><span class="sxs-lookup"><span data-stu-id="fe443-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe443-105">Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="fe443-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="fe443-106">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="fe443-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="fe443-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (3 dalis. Ataskaitos kūrimas)“.</span><span class="sxs-lookup"><span data-stu-id="fe443-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="fe443-108">Taip pat turite sukonfigūruoti numatytuosius dokumentų tipus puslapyje Elektroninių ataskaitų parametrai.</span><span class="sxs-lookup"><span data-stu-id="fe443-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="fe443-109">Numatytieji dokumentų tipai taip pat nustatomi, kai jūs atsisiunčiate ir importuojate ER konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="fe443-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="fe443-110">Ataskaitos vykdymas</span><span class="sxs-lookup"><span data-stu-id="fe443-110">Run report</span></span>
1. <span data-ttu-id="fe443-111">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="fe443-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="fe443-112">Medyje išplėskite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="fe443-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="fe443-113">Medyje pasirinkite Financial dimensions sample model\Ledger journal report.</span><span class="sxs-lookup"><span data-stu-id="fe443-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="fe443-114">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="fe443-114">Click Run.</span></span>
<span data-ttu-id="fe443-115">![ER konfigūracijų puslapis](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="fe443-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="fe443-116">Lauke Dimensijos pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe443-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="fe443-117">Norėdami pasirinkti visas dabartinės įmonės dimensijas, įveskite toliau nurodytą informaciją: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="fe443-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![ER konfigūracijų puslapis](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="fe443-119">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="fe443-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="fe443-120">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="fe443-120">Click Filter.</span></span>
8. <span data-ttu-id="fe443-121">Pasirinkite eilutę DK žurnalo lentelės ir lauko Žurnalo paketo numeris eilutę.</span><span class="sxs-lookup"><span data-stu-id="fe443-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="fe443-122">Lauke Kriterijai įveskite 00057.</span><span class="sxs-lookup"><span data-stu-id="fe443-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="fe443-123">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="fe443-123">Click OK.</span></span>
11. <span data-ttu-id="fe443-124">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="fe443-124">Click OK.</span></span>
<span data-ttu-id="fe443-125">![ER konfigūracijų puslapis](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="fe443-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="fe443-126">Peržiūrėkite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="fe443-126">Review the generated output.</span></span> <span data-ttu-id="fe443-127">Rodomos kiekvienos pasirinkto paketo operacijos finansinės dimensijos iš atitinkamo dimensijų rinkinio.</span><span class="sxs-lookup"><span data-stu-id="fe443-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="fe443-128">Vykdykite šią ataskaitą ir pasirinkite skirtingas dimensijas, norėdami pamatyti, ar ataskaita nepriklauso nuo pasirinktų dimensijų skaičiaus arba sukonfigūruotų šio egzemplioriaus dimensijų skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="fe443-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![ER konfigūracijų puslapis](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]