--- 
title: "Ataskaitos, kuri finansines dimensijas naudoja kaip duomenų šaltinį, vykdymas elektroninėse ataskaitose (ER)"
description: "Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ee951d7f3f04e641f7bed767a2eebd1c180eb9f3
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="a8632-103">Ataskaitos, kuri finansines dimensijas naudoja kaip duomenų šaltinį, vykdymas elektroninėse ataskaitose (ER)</span><span class="sxs-lookup"><span data-stu-id="a8632-103">Run a report that uses financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8632-104">Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="a8632-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="a8632-105">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="a8632-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="a8632-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (3 dalis: ataskaitos kūrimas)“.</span><span class="sxs-lookup"><span data-stu-id="a8632-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="a8632-107">Taip pat turite sukonfigūruoti numatytuosius dokumentų tipus puslapyje Elektroninių ataskaitų parametrai.</span><span class="sxs-lookup"><span data-stu-id="a8632-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="a8632-108">Numatytieji dokumentų tipai taip pat nustatomi, kai jūs atsisiunčiate ir importuojate ER konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="a8632-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="a8632-109">Ataskaitos vykdymas</span><span class="sxs-lookup"><span data-stu-id="a8632-109">Run report</span></span>
1. <span data-ttu-id="a8632-110">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="a8632-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a8632-111">Medyje išplėskite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="a8632-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a8632-112">Medyje pasirinkite Financial dimensions sample model\Ledger journal report.</span><span class="sxs-lookup"><span data-stu-id="a8632-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="a8632-113">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="a8632-113">Click Run.</span></span>
5. <span data-ttu-id="a8632-114">Lauke Dimensijos pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a8632-114">In the Dimension name field, In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="a8632-115">Norėdami pasirinkti visas dabartinės įmonės dimensijas, įveskite toliau nurodytą informaciją: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project:</span><span class="sxs-lookup"><span data-stu-id="a8632-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="a8632-116">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="a8632-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="a8632-117">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="a8632-117">Click Filter.</span></span>
8. <span data-ttu-id="a8632-118">Pasirinkite eilutę DK žurnalo lentelės ir lauko Žurnalo paketo numeris eilutę.</span><span class="sxs-lookup"><span data-stu-id="a8632-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="a8632-119">Lauke Kriterijai įveskite 00057.</span><span class="sxs-lookup"><span data-stu-id="a8632-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="a8632-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a8632-120">Click OK.</span></span>
11. <span data-ttu-id="a8632-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a8632-121">Click OK.</span></span>
    * <span data-ttu-id="a8632-122">Peržiūrėkite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="a8632-122">Review the generated output.</span></span> <span data-ttu-id="a8632-123">Atkreipkite dėmesį, kad rodomos kiekvienos pasirinkto paketo operacijos finansinės dimensijos iš atitinkamo dimensijų rinkinio.</span><span class="sxs-lookup"><span data-stu-id="a8632-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="a8632-124">Vykdykite šią ataskaitą ir pasirinkite skirtingas dimensijas, norėdami pamatyti, ar ataskaita nepriklauso nuo pasirinktų dimensijų skaičiaus arba sukonfigūruotų šio „Dynamics 365 for Finance and Operations“ egzemplioriaus dimensijų skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="a8632-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


