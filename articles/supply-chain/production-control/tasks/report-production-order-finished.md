---
title: Gamybos užsakymų skelbimą baigtais
description: Ši procedūra nurodo, kaip gamybos užsakymą paskelbti kaip baigtą.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93193e6365bcf82fbbf93af81e2581a358899fa1
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826291"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="34564-103">Gamybos užsakymų skelbimą baigtais</span><span class="sxs-lookup"><span data-stu-id="34564-103">Report a production order as finished</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34564-104">Ši procedūra nurodo, kaip gamybos užsakymą paskelbti kaip baigtą.</span><span class="sxs-lookup"><span data-stu-id="34564-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="34564-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="34564-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="34564-106">Tai yra šešta procedūra iš septynių, kurioje paaiškinamas gamybos užsakymo ciklas.</span><span class="sxs-lookup"><span data-stu-id="34564-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="34564-107">Gamybos užsakymų skelbimą baigtais</span><span class="sxs-lookup"><span data-stu-id="34564-107">Report a production order as finished</span></span>
1. <span data-ttu-id="34564-108">Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="34564-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="34564-109">Pasirinkite gamybos užsakymą, kurio būsena yra Pradėta.</span><span class="sxs-lookup"><span data-stu-id="34564-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="34564-110">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="34564-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="34564-111">Spustelėkite Paskelbti baigtu.</span><span class="sxs-lookup"><span data-stu-id="34564-111">Click Report as finished.</span></span>
    * <span data-ttu-id="34564-112">Šiame puslapyje galite patvirtinti baigto produkto kiekį, kurį norite paskelbti kaip baigtą.</span><span class="sxs-lookup"><span data-stu-id="34564-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="34564-113">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="34564-113">Click the General tab.</span></span>
5. <span data-ttu-id="34564-114">Nustatykite Prekių kiekį į '18'.</span><span class="sxs-lookup"><span data-stu-id="34564-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="34564-115">Nustatykite Klaidų kiekį į '2'.</span><span class="sxs-lookup"><span data-stu-id="34564-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="34564-116">Lauke Klaidos priežastis pasirinkite 'Medžiaga'.</span><span class="sxs-lookup"><span data-stu-id="34564-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="34564-117">Pažymėkite arba išvalykite žymės langelį Galutinė užduotis.</span><span class="sxs-lookup"><span data-stu-id="34564-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="34564-118">Pažymėkite arba išvalykite žymės langelį Leisti klaidą.</span><span class="sxs-lookup"><span data-stu-id="34564-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="34564-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="34564-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="34564-120">Patikrinti žurnalą Skelbti baigtu</span><span class="sxs-lookup"><span data-stu-id="34564-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="34564-121">Veiksmų srityje spustelėkite Peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="34564-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="34564-122">Spustelėkite Paskelbta baigtu.</span><span class="sxs-lookup"><span data-stu-id="34564-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="34564-123">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="34564-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="34564-124">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="34564-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="34564-125">Žurnalas Skelbti baigtu užregistruotas.</span><span class="sxs-lookup"><span data-stu-id="34564-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="34564-126">Jei norite koreguoti žurnalą, galite rankiniu būdu sukurti naują žurnalą, kuriame galite atlikti keitimus.</span><span class="sxs-lookup"><span data-stu-id="34564-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  

