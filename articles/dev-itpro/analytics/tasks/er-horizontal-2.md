--- 
title: "Formato, naudojančio horizontaliai išplečiamus diapazonus, kad elektroninėse ataskaitose (ER) stulpeliai į „Excel“ ataskaitas būtų įtraukiami dinamiškai, paleidimas"
description: "Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas ataskaitas generuoti kaip OPENXML darbalapių („Excel“) failus, kuriuose būtinus stulpelius galima dinamiškai kurti kaip horizontaliai išplečiamus diapazonus."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8e5c53905b903bc5242625283f3b093144243cf9
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a><span data-ttu-id="5853d-103">Formato, naudojančio horizontaliai išplečiamus diapazonus, kad elektroninėse ataskaitose (ER) stulpeliai į „Excel“ ataskaitas būtų įtraukiami dinamiškai, paleidimas</span><span class="sxs-lookup"><span data-stu-id="5853d-103">Run a format that uses horizontally-expandable ranges to dynamically add columns in Excel reports for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5853d-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas ataskaitas generuoti kaip OPENXML darbalapių („Excel“) failus, kuriuose būtinus stulpelius galima dinamiškai kurti kaip horizontaliai išplečiamus diapazonus.</span><span class="sxs-lookup"><span data-stu-id="5853d-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="5853d-105">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="5853d-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="5853d-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite veiksmus, nurodytus procedūroje „ER: horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas (1 dalis: formato kūrimas)“.</span><span class="sxs-lookup"><span data-stu-id="5853d-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="5853d-107">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="5853d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="5853d-108">Sukurto formato radimas</span><span class="sxs-lookup"><span data-stu-id="5853d-108">Find created format</span></span>
1. <span data-ttu-id="5853d-109">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="5853d-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="5853d-110">Medyje išplėskite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="5853d-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="5853d-111">Medyje pasirinkite Financial dimensions sample model\Sample report with horizontally expandable ranges.</span><span class="sxs-lookup"><span data-stu-id="5853d-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="5853d-112">Formato paleidimas norint kurti „Excel“ išvestį</span><span class="sxs-lookup"><span data-stu-id="5853d-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="5853d-113">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="5853d-113">Click Run.</span></span>
2. <span data-ttu-id="5853d-114">Lauke Dimensijos pavadinimas įveskite BusinessUnit;CostCenter;Department.</span><span class="sxs-lookup"><span data-stu-id="5853d-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="5853d-115">Lauke Dimensijos pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5853d-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="5853d-116">Norėdami pasirinkti visas dabartinės įmonės dimensijas, įveskite toliau nurodytą informaciją: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project:</span><span class="sxs-lookup"><span data-stu-id="5853d-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="5853d-117">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="5853d-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="5853d-118">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="5853d-118">Click Filter.</span></span>
5. <span data-ttu-id="5853d-119">Pasirinkite eilutę DK žurnalo lentelės ir lauko Žurnalo paketo numeris eilutę.</span><span class="sxs-lookup"><span data-stu-id="5853d-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="5853d-120">Lauke Kriterijai įveskite 00057..00058.</span><span class="sxs-lookup"><span data-stu-id="5853d-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="5853d-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="5853d-121">00057..00058</span></span>  
7. <span data-ttu-id="5853d-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5853d-122">Click OK.</span></span>
8. <span data-ttu-id="5853d-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5853d-123">Click OK.</span></span>
    * <span data-ttu-id="5853d-124">Peržiūrėkite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="5853d-124">Review the generated output.</span></span> <span data-ttu-id="5853d-125">Atkreipkite dėmesį, kad naujai sukurtame „Excel“ faile yra tiek pat stulpelių, kiek jų pasirinkta finansinėms dimensijoms.</span><span class="sxs-lookup"><span data-stu-id="5853d-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="5853d-126">Tų stulpelių ataskaitos antraštė nurodo finansinių dimensijų pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="5853d-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="5853d-127">Tų stulpelių operacijų eilutės nurodo finansines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="5853d-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="5853d-128">Vykdykite šią ataskaitą ir pasirinkite skirtingas dimensijas, norėdami pamatyti, ar ataskaita nepriklauso nuo pasirinktų dimensijų skaičiaus arba sukonfigūruotų šio „Dynamics 365 for Finance and Operations“, „Enterprise“ leidimo egzemplioriaus dimensijų skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="5853d-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


