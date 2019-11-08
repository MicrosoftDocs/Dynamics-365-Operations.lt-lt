---
title: 'ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (4 dalis – Ataskaitos vykdymas)'
description: Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 27498fb8290fa18abd64d7f306e9c0bf4713a72f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550139"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="b71e3-103">ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (4 dalis – Ataskaitos vykdymas)</span><span class="sxs-lookup"><span data-stu-id="b71e3-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b71e3-104">Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="b71e3-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="b71e3-105">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="b71e3-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="b71e3-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (3 dalis: ataskaitos kūrimas)“.</span><span class="sxs-lookup"><span data-stu-id="b71e3-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="b71e3-107">Taip pat turite sukonfigūruoti numatytuosius dokumentų tipus puslapyje Elektroninių ataskaitų parametrai.</span><span class="sxs-lookup"><span data-stu-id="b71e3-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="b71e3-108">Numatytieji dokumentų tipai taip pat nustatomi, kai jūs atsisiunčiate ir importuojate ER konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="b71e3-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="b71e3-109">Ataskaitos vykdymas</span><span class="sxs-lookup"><span data-stu-id="b71e3-109">Run report</span></span>
1. <span data-ttu-id="b71e3-110">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="b71e3-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b71e3-111">Medyje išplėskite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="b71e3-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="b71e3-112">Medyje pasirinkite Financial dimensions sample model\Ledger journal report.</span><span class="sxs-lookup"><span data-stu-id="b71e3-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="b71e3-113">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="b71e3-113">Click Run.</span></span>
5. <span data-ttu-id="b71e3-114">Lauke Dimensijos pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b71e3-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="b71e3-115">Norėdami pasirinkti visas dabartinės įmonės dimensijas, įveskite toliau nurodytą informaciją: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project:</span><span class="sxs-lookup"><span data-stu-id="b71e3-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="b71e3-116">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="b71e3-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="b71e3-117">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="b71e3-117">Click Filter.</span></span>
8. <span data-ttu-id="b71e3-118">Pasirinkite eilutę DK žurnalo lentelės ir lauko Žurnalo paketo numeris eilutę.</span><span class="sxs-lookup"><span data-stu-id="b71e3-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="b71e3-119">Lauke Kriterijai įveskite 00057.</span><span class="sxs-lookup"><span data-stu-id="b71e3-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="b71e3-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b71e3-120">Click OK.</span></span>
11. <span data-ttu-id="b71e3-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b71e3-121">Click OK.</span></span>
    * <span data-ttu-id="b71e3-122">Peržiūrėkite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="b71e3-122">Review the generated output.</span></span> <span data-ttu-id="b71e3-123">Atkreipkite dėmesį, kad rodomos kiekvienos pasirinkto paketo operacijos finansinės dimensijos iš atitinkamo dimensijų rinkinio.</span><span class="sxs-lookup"><span data-stu-id="b71e3-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="b71e3-124">Vykdykite šią ataskaitą ir pasirinkite skirtingas dimensijas, norėdami pamatyti, ar ataskaita nepriklauso nuo pasirinktų dimensijų skaičiaus arba sukonfigūruotų šio egzemplioriaus dimensijų skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="b71e3-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

