---
title: Grynųjų pinigų srautų prognozė (peržiūros versija)
description: Šioje temoje aprašoma priemonė Grynųjų pinigų srautų prognozavimas.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f97b8fc0896f0f7b95bf5609f94367b3a8230ca7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645253"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="d30b2-103">Grynųjų pinigų srautų prognozė (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="d30b2-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d30b2-104">Grynųjų pinigų srautai yra labai svarbūs bet kuriai įmonei.</span><span class="sxs-lookup"><span data-stu-id="d30b2-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="d30b2-105">Net pelningos įmonės gali susidurti su nemokumu, jei jos neprižiūri grynųjų pinigų srautų, kurie patenkina neatidėliotinus poreikius.</span><span class="sxs-lookup"><span data-stu-id="d30b2-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="d30b2-106">Modulio Finansinės įžvalgos grynųjų pinigų srautų prognozavimo priemonė gali padėti įmonėms efektyviai stebėti ir tvarkyti savo grynųjų pinigų balansus.</span><span class="sxs-lookup"><span data-stu-id="d30b2-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="d30b2-107">Ši funkcija naudoja mašininį mokymą, kad padėtų įmonėms prognozuoti grynųjų pinigų srautus tiksliau nei anksčiau.</span><span class="sxs-lookup"><span data-stu-id="d30b2-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="d30b2-108">Ji taip pat gali padėti vadovams priimti sprendimus, optimizančius galimybes, susijusias su dabartine grynųjų pinigų padėtimi.</span><span class="sxs-lookup"><span data-stu-id="d30b2-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="d30b2-109">Daugumai įmonių grynųjų pinigų srautų valdymas ir pinigų srautų prognozavimo vykdymas yra varginantis, pasikartojantis ir neautomatizuotas procesas.</span><span class="sxs-lookup"><span data-stu-id="d30b2-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="d30b2-110">Dauguma įmonių naudoja „Microsoft Excel“ sprendimus, kurių sudėtingumo laipsnis skirtingas.</span><span class="sxs-lookup"><span data-stu-id="d30b2-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="d30b2-111">Norint tiksliai prognozuoti grynųjų pinigų srautus, kyla tolesnių iššūkių.</span><span class="sxs-lookup"><span data-stu-id="d30b2-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="d30b2-112">Duomenys nepasiekiami sprendimų priėmėjams, nes jie yra išsibarstę keliose vietose, įskaitant nurodytas toliau.</span><span class="sxs-lookup"><span data-stu-id="d30b2-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="d30b2-113">Apskaitos arba įmonės išteklių planavimo sistema</span><span class="sxs-lookup"><span data-stu-id="d30b2-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="d30b2-114">Finansinio planavimo programinė įranga</span><span class="sxs-lookup"><span data-stu-id="d30b2-114">Financial planning software</span></span>
  - <span data-ttu-id="d30b2-115">Excel</span><span class="sxs-lookup"><span data-stu-id="d30b2-115">Excel</span></span>
  - <span data-ttu-id="d30b2-116">Papildomos programinės įrangos programos</span><span class="sxs-lookup"><span data-stu-id="d30b2-116">Additional software applications</span></span> 
- <span data-ttu-id="d30b2-117">Prognozavimas paremtas vidinėmis žiniomis, esančiomis atskirose kiekvieno domeno ar padalinio srityse.</span><span class="sxs-lookup"><span data-stu-id="d30b2-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="d30b2-118">Grynųjų pinigų srautų prognozavimo tikslumo vertinimas po to, kai finansiniai duomenys jau realizuoti, yra neaišku ir sunkus procesas.</span><span class="sxs-lookup"><span data-stu-id="d30b2-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="d30b2-119">Priemonįs Grynųjų pinigų srautų prognozės informacija</span><span class="sxs-lookup"><span data-stu-id="d30b2-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="d30b2-120">Priemonė Grynųjų pinigų srautų prognozės apima tolesnes funkcijas.</span><span class="sxs-lookup"><span data-stu-id="d30b2-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="d30b2-121">Leidžia lengvai integruoti grynųjų pinigų srautų duomenis iš išorinių sistemų į „Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="d30b2-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="d30b2-122">Pinigų srautų prognozėms taip pat gali būti naudojama duomenų importavimo-eksportavimo sistema.</span><span class="sxs-lookup"><span data-stu-id="d30b2-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="d30b2-123">Ši sistema leidžia lengvai integruoti su „Excel“ „OData“.</span><span class="sxs-lookup"><span data-stu-id="d30b2-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="d30b2-124">Taip pat galite sujungti duomenis iš kelių šaltinių, kad sukurtumėte išsamų grynųjų pinigų srautų sprendimą.</span><span class="sxs-lookup"><span data-stu-id="d30b2-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="d30b2-125">Įdiegiama sumanios grynųjų pinigų padėties funkcija.</span><span class="sxs-lookup"><span data-stu-id="d30b2-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="d30b2-126">Grynųjų pinigų padėtis sukuriama remiantis kliento mokėjimo būdu, siekiant numatyti, kada įmonė gali tikėtis, kad sąskaitoje atsiras grynųjų pinigų.</span><span class="sxs-lookup"><span data-stu-id="d30b2-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="d30b2-127">Ji taip pat analizuoja istorinius mokėjimo tiekėjų modelius, kad būtų galima prognozuoti, kada bus apmokamos būsimos SF ir užsakymai.</span><span class="sxs-lookup"><span data-stu-id="d30b2-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="d30b2-128">Įdiegiama sumanaus ilgalaikio grynųjų pinigų srautų prognozavimo funkcija, naudojanti laiko serijos prognozavimą per automatinę integraciją su „AI Builder“.</span><span class="sxs-lookup"><span data-stu-id="d30b2-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="d30b2-129">Suteikia galimybę įrašyti konkrečią grynųjų pinigų srauto padėtį ar prognozes, jas redaguoti, tada lengvai palyginti ir išmatuoti prognozavimo našumą su faktiniais finansiniais rodikliais.</span><span class="sxs-lookup"><span data-stu-id="d30b2-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="d30b2-130">Suteikia galimybę naudoti sąlyginę analizę, lyginant momentines kopijas.</span><span class="sxs-lookup"><span data-stu-id="d30b2-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="d30b2-131">Pavyzdžiui, galite sukurti kelias momentines kopijas, kurios rodo optimistinį, pesimistinį ir realistiškiausią jūsų grynųjų pinigų srauto rodinius, o tada juos palyginti ir peržiūrėti skirtumus.</span><span class="sxs-lookup"><span data-stu-id="d30b2-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="d30b2-132">Suteikia galimybę peržiūrėti grynųjų pinigų srautų prognozę keliomis valiutomis, visuose juridiniuose subjektuose ir filtruoti bei peržiūrėti grynųjų pinigų srautą, susijusį su tam tikra banko sąskaita.</span><span class="sxs-lookup"><span data-stu-id="d30b2-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="d30b2-133">Leidžia filtruoti ir peržiūrėti banko sąskaitas, susijusias su finansinėmis dimensijomis.</span><span class="sxs-lookup"><span data-stu-id="d30b2-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="d30b2-134">Grynųjų pinigų srautų prognozavimo funkcija programoje „Dynamics 365 Finance“ suteiks jūsų organizacijai galimybę transformuoti varginantį, sudėtingą ir pasikartojantį grynųjų pinigų srautų prognozavimą į paprastą, automatizuotą procesą.</span><span class="sxs-lookup"><span data-stu-id="d30b2-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="d30b2-135">Automatizuojant labiausiai varginančius grynųjų pinigų srautų prognozavimo aspektus, galima sutelkti dėmesį į svarbių sprendimų priėmimą siekiant norimų verslo rezultatų.</span><span class="sxs-lookup"><span data-stu-id="d30b2-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="d30b2-136">Grynųjų pinigų srautų prognozavimo dimensijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="d30b2-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="d30b2-137">Naujas skirtukas puslapyje **Grynųjų pinigų srautų prognozavimo sąranka** leidžia kontroliuoti, kokios finansinės dimensijos gali būti naudojamos filtruojant darbo sritį **Grynųjų pinigų srautų prognozavimas**.</span><span class="sxs-lookup"><span data-stu-id="d30b2-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="d30b2-138">Šis skirtukas bus rodomas tik tada, kai bus įjungta funkcija Grynųjų pinigų srautų prognozės.</span><span class="sxs-lookup"><span data-stu-id="d30b2-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="d30b2-139">Skirtuke **Dimensijos** pasirinkite iš dimensijų, kurias naudosite filtruodami, sąrašo ir naudokite rodyklių klavišus, kad perkeltumėte jas į dešinįjį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="d30b2-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="d30b2-140">Grynųjų pinigų srautų prognozavimo duomenims filtruoti galima pasirinkti tik dvi dimensijas.</span><span class="sxs-lookup"><span data-stu-id="d30b2-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

#### <a name="privacy-notice"></a><span data-ttu-id="d30b2-141">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="d30b2-141">Privacy notice</span></span>
<span data-ttu-id="d30b2-142">Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="d30b2-142">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
