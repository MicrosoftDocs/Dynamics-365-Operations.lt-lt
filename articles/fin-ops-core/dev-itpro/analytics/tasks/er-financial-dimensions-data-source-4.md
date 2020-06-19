---
title: 'ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (4 dalis – Ataskaitos vykdymas)'
description: Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9a6f07d6c665097fabab4d3ec6d7fa5ba80b65d
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406479"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="1a6e9-103">ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (4 dalis – Ataskaitos vykdymas)</span><span class="sxs-lookup"><span data-stu-id="1a6e9-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a6e9-104">Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="1a6e9-105">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="1a6e9-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (3 dalis. Ataskaitos kūrimas)“.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="1a6e9-107">Taip pat turite sukonfigūruoti numatytuosius dokumentų tipus puslapyje Elektroninių ataskaitų parametrai.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="1a6e9-108">Numatytieji dokumentų tipai taip pat nustatomi, kai jūs atsisiunčiate ir importuojate ER konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="1a6e9-109">Ataskaitos vykdymas</span><span class="sxs-lookup"><span data-stu-id="1a6e9-109">Run report</span></span>
1. <span data-ttu-id="1a6e9-110">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1a6e9-111">Medyje išplėskite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="1a6e9-112">Medyje pasirinkite Financial dimensions sample model\Ledger journal report.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="1a6e9-113">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-113">Click Run.</span></span>
<span data-ttu-id="1a6e9-114">![ER konfigūracijų puslapis](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="1a6e9-114">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="1a6e9-115">Lauke Dimensijos pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-115">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="1a6e9-116">Norėdami pasirinkti visas dabartinės įmonės dimensijas, įveskite toliau nurodytą informaciją: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="1a6e9-116">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![ER konfigūracijų puslapis](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="1a6e9-118">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-118">Expand the Records to include section.</span></span>
7. <span data-ttu-id="1a6e9-119">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-119">Click Filter.</span></span>
8. <span data-ttu-id="1a6e9-120">Pasirinkite eilutę DK žurnalo lentelės ir lauko Žurnalo paketo numeris eilutę.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="1a6e9-121">Lauke Kriterijai įveskite 00057.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-121">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="1a6e9-122">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-122">Click OK.</span></span>
11. <span data-ttu-id="1a6e9-123">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-123">Click OK.</span></span>
<span data-ttu-id="1a6e9-124">![ER konfigūracijų puslapis](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="1a6e9-124">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="1a6e9-125">Peržiūrėkite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-125">Review the generated output.</span></span> <span data-ttu-id="1a6e9-126">Rodomos kiekvienos pasirinkto paketo operacijos finansinės dimensijos iš atitinkamo dimensijų rinkinio.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-126">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="1a6e9-127">Vykdykite šią ataskaitą ir pasirinkite skirtingas dimensijas, norėdami pamatyti, ar ataskaita nepriklauso nuo pasirinktų dimensijų skaičiaus arba sukonfigūruotų šio egzemplioriaus dimensijų skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="1a6e9-127">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![ER konfigūracijų puslapis](../media/er-financial-dimensions-guides-run4.png)
