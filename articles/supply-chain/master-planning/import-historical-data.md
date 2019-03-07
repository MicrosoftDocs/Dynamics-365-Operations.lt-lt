---
title: Retrospektyvinių duomenų importavimas į poreikio prognozėms generuoti
description: Norint generuoti tikslias poreikio prognozes, reikia retrospektyvinių poreikio duomenų pagal prekę arba prekių paskirstymo raktą. Šioje temoje paaiškinama, kaip naudoti duomenų objektus norint importuoti retrospektyvinius poreikio duomenis iš bet kurios sistemos, kad turėtumėte ilgesnę poreikio prognozės duomenų retrospektyvą.
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 018694c79c6dd64e19b010848aad8acd36b0a9a8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "328613"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="f4e4c-104">Retrospektyvinių duomenų importavimas į poreikio prognozėms generuoti</span><span class="sxs-lookup"><span data-stu-id="f4e4c-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4e4c-105">Norint užtikrinti poreikio prognozių tikslumą, jums reikia kiek įmanoma daugiau retrospektyvinių poreikio duomenų pagal prekę arba prekių paskirstymo raktą.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="f4e4c-106">Jei retrospektyviniai poreikio duomenys dar neimportuoti, importuokite juos naudodami „Microsoft Dynamics 365 for Finance and Operations“ duomenų objektą **Retrospektyvinis išorinis poreikis** (ReqDemPlanHistoricalExternalDemandEntity).</span><span class="sxs-lookup"><span data-stu-id="f4e4c-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Microsoft Dynamics 365 for Finance and Operations to import it.</span></span>

<span data-ttu-id="f4e4c-107">Darbo srityje **Duomenų valdymas** galite peržiūrėti visų objekto laukų apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="f4e4c-108">Atidarykite darbo sritį **Duomenų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="f4e4c-109">Spustelėkite plytelę **Duomenų objektai**.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="f4e4c-110">Objektų sąraše ieškokite objekto **Retrospektyvinis išorinis poreikis**.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="f4e4c-111">Spustelėkite **Paskirties laukai**.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-111">Click **Target fields**.</span></span> <span data-ttu-id="f4e4c-112">Šie objekto laukai yra privalomi: teritorija (**DeliveringSiteId**), data (**DemandDate**), kiekis (**DemandQuantity**) ir prekės numeris (**ItemNumber**) arba prekių paskirstymo raktas (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="f4e4c-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="f4e4c-113">Norint naudoti duomenų objektą, reikalingas „Microsoft Excel“ failas arba kableliais atskirtų verčių (CSV) failas, kuriame yra retrospektyviniai poreikio duomenys.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="f4e4c-114">Toliau pateikiamame pavyzdyje parodyta, kaip importuoti duomenis iš CSV failo.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="f4e4c-115">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f4e4c-115">Example</span></span>

<span data-ttu-id="f4e4c-116">Kaip pavyzdį galite naudoti toliau nurodytą failą.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-116">You can use the following file as an example.</span></span> <span data-ttu-id="f4e4c-117">Atsisiųskite [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span><span class="sxs-lookup"><span data-stu-id="f4e4c-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="f4e4c-118">Šiame faile yra prekės D0001 retrospektyviniai poreikio duomenys.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="f4e4c-119">Jame yra tik šie privalomi laukai: teritorija, kiekis ir poreikio data.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="f4e4c-120">Pasirinkite įmonę, į kurią norite importuoti į retrospektyvinius poreikio duomenis.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="f4e4c-121">Atidarykite darbo sritį **Duomenų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="f4e4c-122">Spustelėkite plytelę **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="f4e4c-123">Įveskite importavimo projekto pavadinimą, pavyzdžiui, **Prekės D0001 retrospektyvinio poreikio importavimas**.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="f4e4c-124">Lauke **Šaltinio duomenų formatas** pasirinkite importuojamo failo formatą.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="f4e4c-125">Šiame pavyzdyje norėdami importuoti failą HistoricalDemandData, pvz., pasirinkite **CSV**.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="f4e4c-126">Lauke **Objekto pavadinimas** pasirinkite **Retrospektyvinis išorinis poreikis**.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="f4e4c-127">Įrašykite failą kompiuteryje ir tada jį įkelkite.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="f4e4c-128">Spustelėkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-128">Click **Import**.</span></span>
9. <span data-ttu-id="f4e4c-129">Automatiškai atidaromas puslapis **Vykdymo suvestinė**.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="f4e4c-130">Patikrinkite importuotus duomenis puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="f4e4c-131">Importavus retrospektyvinius poreikio duomenis, galima generuoti pagrindinę poreikio prognozę.</span><span class="sxs-lookup"><span data-stu-id="f4e4c-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4e4c-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f4e4c-132">Additional resources</span></span>

[<span data-ttu-id="f4e4c-133">Pagrindinės statistinės prognozės generavimas</span><span class="sxs-lookup"><span data-stu-id="f4e4c-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)
