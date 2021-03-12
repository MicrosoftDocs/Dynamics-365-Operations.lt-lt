---
title: Trikčių šalinimo grynųjų eigos prognozės nustatymai
description: Šioje temoje pateikti atskymai į klausimus, kuriuos galite turėti konfigūruodami grynų eigos prognozavimą. Jame aptariami dažnai užduodami klausimai (DUK) apie grynųjų eigos nustatymą, grynųjų eigos naujinimus ir grynųjų eigą „Power BI“.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985292"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="19bff-104">Trikčių šalinimo grynųjų eigos prognozės nustatymai</span><span class="sxs-lookup"><span data-stu-id="19bff-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19bff-105">Šioje temoje pateikti atskymai į klausimus, kuriuos galite turėti konfigūruodami grynų eigos prognozavimą.</span><span class="sxs-lookup"><span data-stu-id="19bff-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="19bff-106">Jame aptariami dažnai užduodami klausimai (DUK) apie grynųjų eigos nustatymą, grynųjų eigos naujinimus ir grynųjų eigą „Power BI“.</span><span class="sxs-lookup"><span data-stu-id="19bff-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="19bff-107">Kodėl grynųjų eida yra rodoma tik vienam juridiniam asmeniui?</span><span class="sxs-lookup"><span data-stu-id="19bff-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="19bff-108">Grynų eigos prognozės konfigūruojama ir skaičiuojama vienam juridiniam asmeniu.</span><span class="sxs-lookup"><span data-stu-id="19bff-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="19bff-109">„Power BI“ ataskaitos ir grynų eigos prognozės galimybės „Finance insights“ rodo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="19bff-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="19bff-110">Grynųjų eigos prognozės turi būti nustatytas kiekvienam juridiniam asmeniui, kuriam norite matyti prognozę.</span><span class="sxs-lookup"><span data-stu-id="19bff-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="19bff-111">Peržiūrėkite grynųjų eigos prognozės konfigūravimą visuose juridiniuose asmenyse.</span><span class="sxs-lookup"><span data-stu-id="19bff-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="19bff-112">Kitu atveju, peržiūrėkite visų juridinių asmenų konfigūravimą grynų eigos prognozei ir įsitikinkite, kad jie yra nustatyti kaip norite.</span><span class="sxs-lookup"><span data-stu-id="19bff-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="19bff-113">Kodėl „Power BI“ rodo visus darbo eigos duomenis?</span><span class="sxs-lookup"><span data-stu-id="19bff-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="19bff-114">Būtina atlikti kelis žingsnius prieš grynų eigos prognozes, kurios gali pasirodyti „Power BI“ rodiniuose.</span><span class="sxs-lookup"><span data-stu-id="19bff-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="19bff-115">Peržiūrėkite tolesnį patikrų sąrašą ir įsitikinkite, kad kiekvienas žingsnis buvo atliktas:</span><span class="sxs-lookup"><span data-stu-id="19bff-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="19bff-116">Nustatykite grynų eigą kiekvienam juridiniam asmeniui.</span><span class="sxs-lookup"><span data-stu-id="19bff-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="19bff-117">Bendros sąskaitų knygos parametruose nustatykite sistemos valiutą ir sistemos keitimo kurso tipą.</span><span class="sxs-lookup"><span data-stu-id="19bff-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="19bff-118">Nustatykite apskaitos knygos valiutą ir keitimo kurso tipą.</span><span class="sxs-lookup"><span data-stu-id="19bff-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="19bff-119">Įveskite keitimo kursus tarp transakcijos valiutos ir apskaitos valiutos.</span><span class="sxs-lookup"><span data-stu-id="19bff-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="19bff-120">Įveskite keitimo kursus tarp apskaitos valiutos ir sistemos valiutos.</span><span class="sxs-lookup"><span data-stu-id="19bff-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="19bff-121">Įveskite keitimo kursus tarp apskaitos valiutos ir kiekvienos tuščios valiutos.</span><span class="sxs-lookup"><span data-stu-id="19bff-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="19bff-122">Kodėl grynųjų eigos „Power BI“ veikia ankstesnėse versijose, o dabar yra tuščios?</span><span class="sxs-lookup"><span data-stu-id="19bff-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="19bff-123">Patikrinkite, ar „Grynųjų eigos matmuo V2" ir „LedgerCovLiquidityMeasurement" matmenys iš objekto parduotuvės buvo sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="19bff-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="19bff-124">Dėl daugiau informacijos tapi tai, kaip dirbti su duomenų objektų parduotuvėje, žr. [„Power BI“ integravimas su objekto parduotuve](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Tikrinkite, ar visi žingsniai, kurių reikia siekiant peržiūrėti „Power BI“ turinį buvo atlikti.</span><span class="sxs-lookup"><span data-stu-id="19bff-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="19bff-125">Daugiau informacijos žr. [„Power BI“ turinys Grynųjų pinigų apžvalga](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="19bff-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="19bff-126">Ar Objekto parduotuvės objektai buvo atnaujinti?</span><span class="sxs-lookup"><span data-stu-id="19bff-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="19bff-127">Turite periodiškai atnaujinti jūsų objektus siekiant užsitikrinti, kad duomenys būtų dabartiniai ir tikslūs.</span><span class="sxs-lookup"><span data-stu-id="19bff-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="19bff-128">Norėdami rankiniu būdu atnaujinti konkretų objektą, eikite į **Sistemos administravimas \> Nustatymai \> Objekto parduotuvė**, rinkitės objektą ir tada **Naujinti**.</span><span class="sxs-lookup"><span data-stu-id="19bff-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="19bff-129">Duomenys taip pat gali būti naujinami automatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="19bff-129">The data can also be updated automatically.</span></span> <span data-ttu-id="19bff-130">Puslapyje **Objekto parduotuvė** nustatykite **Automatinis naujinimas įjungtas** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="19bff-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>
