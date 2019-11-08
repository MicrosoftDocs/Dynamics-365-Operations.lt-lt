---
title: 'ER: horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas (2 dalis – Formato paleidimas)'
description: Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas ataskaitas generuoti kaip OPENXML darbalapių („Excel“) failus, kuriuose būtinus stulpelius galima dinamiškai kurti kaip horizontaliai išplečiamus diapazonus.
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
ms.openlocfilehash: b76a2df5cd7714ffda6d0563d3d9013f032db7c2
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550887"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="6fa7b-103">ER: horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas (2 dalis – Formato paleidimas)</span><span class="sxs-lookup"><span data-stu-id="6fa7b-103">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6fa7b-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas ataskaitas generuoti kaip OPENXML darbalapių („Excel“) failus, kuriuose būtinus stulpelius galima dinamiškai kurti kaip horizontaliai išplečiamus diapazonus.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="6fa7b-105">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="6fa7b-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite veiksmus, nurodytus procedūroje „ER: horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas (1 dalis: formato kūrimas)“.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="6fa7b-107">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="6fa7b-108">Sukurto formato radimas</span><span class="sxs-lookup"><span data-stu-id="6fa7b-108">Find created format</span></span>
1. <span data-ttu-id="6fa7b-109">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6fa7b-110">Medyje išplėskite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="6fa7b-111">Medyje pasirinkite Financial dimensions sample model\Sample report with horizontally expandable ranges.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="6fa7b-112">Formato paleidimas norint kurti „Excel“ išvestį</span><span class="sxs-lookup"><span data-stu-id="6fa7b-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="6fa7b-113">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-113">Click Run.</span></span>
2. <span data-ttu-id="6fa7b-114">Lauke Dimensijos pavadinimas įveskite BusinessUnit;CostCenter;Department.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="6fa7b-115">Lauke Dimensijos pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="6fa7b-116">Norėdami pasirinkti visas dabartinės įmonės dimensijas, įveskite toliau nurodytą informaciją: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project:</span><span class="sxs-lookup"><span data-stu-id="6fa7b-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="6fa7b-117">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="6fa7b-118">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-118">Click Filter.</span></span>
5. <span data-ttu-id="6fa7b-119">Pasirinkite eilutę DK žurnalo lentelės ir lauko Žurnalo paketo numeris eilutę.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="6fa7b-120">Lauke Kriterijai įveskite 00057..00058.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="6fa7b-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="6fa7b-121">00057..00058</span></span>  
7. <span data-ttu-id="6fa7b-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-122">Click OK.</span></span>
8. <span data-ttu-id="6fa7b-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-123">Click OK.</span></span>
    * <span data-ttu-id="6fa7b-124">Peržiūrėkite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-124">Review the generated output.</span></span> <span data-ttu-id="6fa7b-125">Atkreipkite dėmesį, kad naujai sukurtame „Excel“ faile yra tiek pat stulpelių, kiek jų pasirinkta finansinėms dimensijoms.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="6fa7b-126">Tų stulpelių ataskaitos antraštė nurodo finansinių dimensijų pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="6fa7b-127">Tų stulpelių operacijų eilutės nurodo finansines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="6fa7b-128">Vykdykite šią ataskaitą ir pasirinkite skirtingas dimensijas, norėdami pamatyti, ar ataskaita nepriklauso nuo pasirinktų dimensijų skaičiaus arba sukonfigūruotų šio egzemplioriaus dimensijų skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="6fa7b-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

