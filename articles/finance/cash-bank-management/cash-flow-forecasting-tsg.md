---
title: Trikčių šalinimo grynųjų eigos prognozės nustatymai
description: Šioje temoje pateikti atskymai į klausimus, kuriuos galite turėti konfigūruodami grynų eigos prognozavimą. Jame aptariami dažnai užduodami klausimai (DUK) apie grynųjų eigos nustatymą, grynųjų eigos naujinimus ir grynųjų eigą „Power BI“.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827319"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="6a6cd-104">Trikčių šalinimo grynųjų eigos prognozės nustatymai</span><span class="sxs-lookup"><span data-stu-id="6a6cd-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a6cd-105">Šioje temoje pateikti atskymai į klausimus, kuriuos galite turėti konfigūruodami grynų eigos prognozavimą.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="6a6cd-106">Jame aptariami dažnai užduodami klausimai (DUK) apie grynųjų eigos nustatymą, grynųjų eigos naujinimus ir grynųjų eigą „Power BI“.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="6a6cd-107">Kodėl grynųjų eida yra rodoma tik vienam juridiniam asmeniui?</span><span class="sxs-lookup"><span data-stu-id="6a6cd-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="6a6cd-108">Grynų eigos prognozės konfigūruojama ir skaičiuojama vienam juridiniam asmeniu.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="6a6cd-109">„Power BI“ ataskaitos ir grynų eigos prognozės galimybės „Finance insights“ rodo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="6a6cd-110">Grynųjų eigos prognozės turi būti nustatytas kiekvienam juridiniam asmeniui, kuriam norite matyti prognozę.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="6a6cd-111">Peržiūrėkite grynųjų eigos prognozės konfigūravimą visuose juridiniuose asmenyse.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="6a6cd-112">Kitu atveju, peržiūrėkite visų juridinių asmenų konfigūravimą grynų eigos prognozei ir įsitikinkite, kad jie yra nustatyti kaip norite.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="6a6cd-113">Kodėl „Power BI“ rodo visus darbo eigos duomenis?</span><span class="sxs-lookup"><span data-stu-id="6a6cd-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="6a6cd-114">Būtina atlikti kelis žingsnius prieš grynų eigos prognozes, kurios gali pasirodyti „Power BI“ rodiniuose.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="6a6cd-115">Peržiūrėkite tolesnį patikrų sąrašą ir įsitikinkite, kad kiekvienas žingsnis buvo atliktas:</span><span class="sxs-lookup"><span data-stu-id="6a6cd-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="6a6cd-116">Nustatykite grynų eigą kiekvienam juridiniam asmeniui.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="6a6cd-117">Bendros sąskaitų knygos parametruose nustatykite sistemos valiutą ir sistemos keitimo kurso tipą.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="6a6cd-118">Nustatykite apskaitos knygos valiutą ir keitimo kurso tipą.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="6a6cd-119">Įveskite keitimo kursus tarp transakcijos valiutos ir apskaitos valiutos.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="6a6cd-120">Įveskite keitimo kursus tarp apskaitos valiutos ir sistemos valiutos.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="6a6cd-121">Įveskite keitimo kursus tarp apskaitos valiutos ir kiekvienos tuščios valiutos.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="6a6cd-122">Kodėl grynųjų eigos „Power BI“ veikia ankstesnėse versijose, o dabar yra tuščios?</span><span class="sxs-lookup"><span data-stu-id="6a6cd-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="6a6cd-123">Patikrinkite, ar „Grynųjų eigos matmuo V2" ir „LedgerCovLiquidityMeasurement" matmenys iš objekto parduotuvės buvo sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="6a6cd-124">Daugiau informacijos apie tai, kaip dirbti su duomenimis įrašo saugykloje, žr. [„Power BI“ integravimas su objekto parduotuve](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="6a6cd-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="6a6cd-125">Patikrinkite, ar atlikti visi veiksmai, kurie „Power BI“ būtini turiniui peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="6a6cd-126">Daugiau informacijos žr. [„Power BI“ turinys Grynųjų pinigų apžvalga](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="6a6cd-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="6a6cd-127">Ar Objekto parduotuvės objektai buvo atnaujinti?</span><span class="sxs-lookup"><span data-stu-id="6a6cd-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="6a6cd-128">Turite periodiškai atnaujinti jūsų objektus siekiant užsitikrinti, kad duomenys būtų dabartiniai ir tikslūs.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="6a6cd-129">Norėdami rankiniu būdu atnaujinti konkretų objektą, eikite į **Sistemos administravimas \> Nustatymai \> Objekto parduotuvė**, rinkitės objektą ir tada **Naujinti**.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="6a6cd-130">Duomenys taip pat gali būti naujinami automatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-130">The data can also be updated automatically.</span></span> <span data-ttu-id="6a6cd-131">Puslapyje **Objekto parduotuvė** nustatykite **Automatinis naujinimas įjungtas** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="6a6cd-132">Kurį skaičiavimo metodą naudoti skaičiuojant pinigų srautų prognozes?</span><span class="sxs-lookup"><span data-stu-id="6a6cd-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="6a6cd-133">Pinigų srautų prognozės skaičiavimo metodas turi dvi svarbias pasirinkimo pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="6a6cd-134">Nauja pasirinktis apskaičiuos naujų dokumentų ir dokumentų, kurie pasikeitė po paskutinės paketinės užduoties **vykdymo**, pinigų srautų prognozes.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="6a6cd-135">Ši pasirinktis paleiskite greičiau, nes ji apdoroja mažesnį dokumentų pogrupį.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="6a6cd-136">Pasirinktis **Bendra** perskaičiuos kiekvieno sistemos dokumento pinigų srautų prognozes.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="6a6cd-137">Šiai pasirinktii atlikti reikia daugiau laiko, nes jai atlikti reikia daugiau darbo.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="6a6cd-138">Kaip pagerinti pasikartojančios paketinės užduoties pinigų srautų prognozavimo našumą?</span><span class="sxs-lookup"><span data-stu-id="6a6cd-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="6a6cd-139">Rekomenduojame kiekvieną dieną vykdyti savo pinigų srautų prognozę ne piko valandomis, naudojant **naują** skaičiavimo metodą.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="6a6cd-140">Mes patariame naudoti šį būdą šešias dienas per savaitę.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="6a6cd-141">Tada kiekvieną savaitę vykdyti pinigų srautų prognozę naudojant **bendrą** skaičiavimo metodą dieną, naudojant mažiausiai veiklos sumą.</span><span class="sxs-lookup"><span data-stu-id="6a6cd-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

