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
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301655"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="f5d79-104">Retrospektyvinių duomenų importavimas į poreikio prognozėms generuoti</span><span class="sxs-lookup"><span data-stu-id="f5d79-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5d79-105">Norint užtikrinti poreikio prognozių tikslumą, jums reikia kiek įmanoma daugiau retrospektyvinių poreikio duomenų pagal prekę arba prekių paskirstymo raktą.</span><span class="sxs-lookup"><span data-stu-id="f5d79-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="f5d79-106">Jei retrospektyviniai poreikio duomenys dar neimportuoti, importuokite juos naudodami „Dynamics 365 Supply Chain Management“ duomenų objektą **Retrospektyvinis išorinis poreikis** (ReqDemPlanHistoricalExternalDemandEntity).</span><span class="sxs-lookup"><span data-stu-id="f5d79-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="f5d79-107">Darbo srityje **Duomenų valdymas** galite peržiūrėti visų objekto laukų apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="f5d79-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="f5d79-108">Atidarykite darbo sritį **Duomenų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="f5d79-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="f5d79-109">Pasirinkite **Duomenų objektai** plytelę.</span><span class="sxs-lookup"><span data-stu-id="f5d79-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="f5d79-110">Objektų sąraše ieškokite objekto **Retrospektyvinis išorinis poreikis**.</span><span class="sxs-lookup"><span data-stu-id="f5d79-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="f5d79-111">Pasirinkite **Paskirties laukai**.</span><span class="sxs-lookup"><span data-stu-id="f5d79-111">Select **Target fields**.</span></span> <span data-ttu-id="f5d79-112">Šie objekto laukai yra privalomi: teritorija (**DeliveringSiteId**), data (**DemandDate**), kiekis (**DemandQuantity**) ir prekės numeris (**ItemNumber**) arba prekių paskirstymo raktas (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="f5d79-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="f5d79-113">Norint naudoti duomenų objektą, reikalingas „Microsoft Excel“ failas arba kableliais atskirtų verčių (CSV) failas, kuriame yra retrospektyviniai poreikio duomenys.</span><span class="sxs-lookup"><span data-stu-id="f5d79-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="f5d79-114">Toliau pateikiamame pavyzdyje parodyta, kaip importuoti duomenis iš CSV failo.</span><span class="sxs-lookup"><span data-stu-id="f5d79-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="f5d79-115">Norėdami gauti daugiau informacijos apie duomenų importavimą, įskaitant duomenų valymą po importavimo, žiūrėkite [Duomenų importavimo ir eksportavimo užduočių apžvalga](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) ir susijusias temas.</span><span class="sxs-lookup"><span data-stu-id="f5d79-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="f5d79-116">Taip pat žiūrėkite [Pagrindinės statistinės prognozės generavimas](generate-statistical-baseline-forecast.md).</span><span class="sxs-lookup"><span data-stu-id="f5d79-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]