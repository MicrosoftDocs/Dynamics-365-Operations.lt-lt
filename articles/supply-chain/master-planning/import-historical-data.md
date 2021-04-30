---
title: Retrospektyvinių duomenų importavimas į poreikio prognozėms generuoti
description: Norint generuoti tikslias poreikio prognozes, reikia retrospektyvinių poreikio duomenų pagal prekę arba prekių paskirstymo raktą. Šioje temoje paaiškinama, kaip naudoti duomenų objektus norint importuoti retrospektyvinius poreikio duomenis iš bet kurios sistemos, kad turėtumėte ilgesnę poreikio prognozės duomenų retrospektyvą.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de380113fe951f75c15f9e5526ad2f1f5cc84334
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908885"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="233cc-104">Retrospektyvinių duomenų importavimas į poreikio prognozėms generuoti</span><span class="sxs-lookup"><span data-stu-id="233cc-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="233cc-105">Norint užtikrinti poreikio prognozių tikslumą, jums reikia kiek įmanoma daugiau retrospektyvinių poreikio duomenų pagal prekę arba prekių paskirstymo raktą.</span><span class="sxs-lookup"><span data-stu-id="233cc-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="233cc-106">Jei retrospektyviniai poreikio duomenys dar neimportuoti, importuokite juos naudodami „Dynamics 365 Supply Chain Management“ duomenų objektą **Retrospektyvinis išorinis poreikis** (ReqDemPlanHistoricalExternalDemandEntity).</span><span class="sxs-lookup"><span data-stu-id="233cc-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="233cc-107">Darbo srityje **Duomenų valdymas** galite peržiūrėti visų objekto laukų apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="233cc-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="233cc-108">Atidarykite darbo sritį **Duomenų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="233cc-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="233cc-109">Pasirinkite **Duomenų objektai** plytelę.</span><span class="sxs-lookup"><span data-stu-id="233cc-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="233cc-110">Objektų sąraše ieškokite objekto **Retrospektyvinis išorinis poreikis**.</span><span class="sxs-lookup"><span data-stu-id="233cc-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="233cc-111">Pasirinkite **Paskirties laukai**.</span><span class="sxs-lookup"><span data-stu-id="233cc-111">Select **Target fields**.</span></span> <span data-ttu-id="233cc-112">Šie objekto laukai yra privalomi: teritorija (**DeliveringSiteId**), data (**DemandDate**), kiekis (**DemandQuantity**) ir prekės numeris (**ItemNumber**) arba prekių paskirstymo raktas (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="233cc-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="233cc-113">Norint naudoti duomenų objektą, reikalingas „Microsoft Excel“ failas arba kableliais atskirtų verčių (CSV) failas, kuriame yra retrospektyviniai poreikio duomenys.</span><span class="sxs-lookup"><span data-stu-id="233cc-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="233cc-114">Toliau pateikiamame pavyzdyje parodyta, kaip importuoti duomenis iš CSV failo.</span><span class="sxs-lookup"><span data-stu-id="233cc-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="233cc-115">Norėdami gauti daugiau informacijos apie duomenų importavimą, įskaitant duomenų valymą po importavimo, žiūrėkite [Duomenų importavimo ir eksportavimo užduočių apžvalga](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) ir susijusias temas.</span><span class="sxs-lookup"><span data-stu-id="233cc-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="233cc-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="233cc-116">Example</span></span>

<span data-ttu-id="233cc-117">Kaip pavyzdį galite naudoti toliau nurodytą failą.</span><span class="sxs-lookup"><span data-stu-id="233cc-117">You can use the following file as an example.</span></span> <span data-ttu-id="233cc-118">Atsisiųskite [HistoricalDemandData](/dynamics/s-e/).</span><span class="sxs-lookup"><span data-stu-id="233cc-118">Download the [HistoricalDemandData](/dynamics/s-e/).</span></span> <span data-ttu-id="233cc-119">Šiame faile yra prekės D0001 retrospektyviniai poreikio duomenys.</span><span class="sxs-lookup"><span data-stu-id="233cc-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="233cc-120">Jame yra tik šie privalomi laukai: teritorija, kiekis ir poreikio data.</span><span class="sxs-lookup"><span data-stu-id="233cc-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="233cc-121">Pasirinkite įmonę, į kurią norite importuoti į retrospektyvinius poreikio duomenis.</span><span class="sxs-lookup"><span data-stu-id="233cc-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="233cc-122">Atidarykite darbo sritį **Duomenų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="233cc-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="233cc-123">Pasirinkite **Importuoti** plytelę.</span><span class="sxs-lookup"><span data-stu-id="233cc-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="233cc-124">Įveskite importavimo projekto pavadinimą, pavyzdžiui, **Prekės D0001 retrospektyvinio poreikio importavimas**.</span><span class="sxs-lookup"><span data-stu-id="233cc-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="233cc-125">Lauke **Šaltinio duomenų formatas** pasirinkite importuojamo failo formatą.</span><span class="sxs-lookup"><span data-stu-id="233cc-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="233cc-126">Šiame pavyzdyje norėdami importuoti failą HistoricalDemandData, pvz., pasirinkite **CSV**.</span><span class="sxs-lookup"><span data-stu-id="233cc-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="233cc-127">Lauke **Objekto pavadinimas** pasirinkite **Retrospektyvinis išorinis poreikis**.</span><span class="sxs-lookup"><span data-stu-id="233cc-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="233cc-128">Įrašykite failą kompiuteryje ir tada jį įkelkite.</span><span class="sxs-lookup"><span data-stu-id="233cc-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="233cc-129">Pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="233cc-129">Select **Import**.</span></span>
9. <span data-ttu-id="233cc-130">Automatiškai atidaromas puslapis **Vykdymo suvestinė**.</span><span class="sxs-lookup"><span data-stu-id="233cc-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="233cc-131">Patikrinkite importuotus duomenis puslapyje.</span><span class="sxs-lookup"><span data-stu-id="233cc-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="233cc-132">Importavus retrospektyvinius poreikio duomenis, galima generuoti pagrindinę poreikio prognozę.</span><span class="sxs-lookup"><span data-stu-id="233cc-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="233cc-133">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="233cc-133">Additional resources</span></span>

[<span data-ttu-id="233cc-134">Pagrindinės statistinės prognozės generavimas</span><span class="sxs-lookup"><span data-stu-id="233cc-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="233cc-135">Duomenų importavimo ir eksportavimo užduočių apžvalga</span><span class="sxs-lookup"><span data-stu-id="233cc-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]