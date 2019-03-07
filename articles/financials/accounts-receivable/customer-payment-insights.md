---
title: Kliento mokėjimo įžvalgos (peržiūra)
description: Šioje temoje aprašoma, kaip kliento mokėjimo įžvalgos gali padėti prognozuoti, kada bus apmokėta sąskaita faktūra, ir organizacijoms padėti kurti optimizacijos strategijas, kurios padidintų apmokėjimo laiku tikimybę.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "344667"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="25281-103">Kliento mokėjimo įžvalgos (peržiūra)</span><span class="sxs-lookup"><span data-stu-id="25281-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="25281-104">Ši funkcija yra tikslinio leidimo dalis ir ja gali naudotis tik vartotojai, sutikę su privačiąja peržiūra.</span><span class="sxs-lookup"><span data-stu-id="25281-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="25281-105">Ši funkcija bus įtraukta į būsimą bendrai prieinamą leidimą.</span><span class="sxs-lookup"><span data-stu-id="25281-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="25281-106">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="25281-106">Overview</span></span>

<span data-ttu-id="25281-107">Organizacijoms dažnai sudėtinga prognozuoti, kada klientas apmokės sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="25281-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="25281-108">Kai neįmanoma to nuspėti, gali kilti šie padariniai – netikslios pinigų srautų prognozės, neefektyvūs surinkimo procesai, tikimybė pateikti užsakymus klientams, kurie kelia didelę kredito riziką.</span><span class="sxs-lookup"><span data-stu-id="25281-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="25281-109">Kliento mokėjimo įžvalgos (peržiūra) naudoja mašininį mokymąsi, kad nuspėtų, kada bus apmokėta sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="25281-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="25281-110">Be to, ji pateikia optimizavimo strategiją, kuri gali būti pritaikyta tam, kad būtų maksimaliai padidinta klientų apmokėjimo laiku tikimybė.</span><span class="sxs-lookup"><span data-stu-id="25281-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="25281-111">Prognozės</span><span class="sxs-lookup"><span data-stu-id="25281-111">Predictions</span></span>

<span data-ttu-id="25281-112">Mokėjimo prognozės leidžia organizacijoms pagerinti verslo procesus šiais būdais:</span><span class="sxs-lookup"><span data-stu-id="25281-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="25281-113">Nesunkiai nustatant sąskaitas faktūras, kurios, remiantis prognozėmis, bus apmokėtos pavėluotai.</span><span class="sxs-lookup"><span data-stu-id="25281-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="25281-114">Imkitės reikiamų priemonių, kad padidintumėte sąskaitos apmokėjimo laiku šansus.</span><span class="sxs-lookup"><span data-stu-id="25281-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="25281-115">Kliento mokėjimo įžvalgos (peržiūra) naudoja mašininį mokymąsi, kad nuspėtų, kada bus apmokėta sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="25281-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="25281-116">Ji naudoja retrospektyvinius sąskaitų faktūrų, mokėjimų ir klientų duomenis, kad sukurtų mašininio mokymosi modelį, kuris naudojamas nuspėti, kada sąskaita faktūra bus apmokėta.</span><span class="sxs-lookup"><span data-stu-id="25281-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="25281-117">Kliento mokėjimo įžvalgos (peržiūra) numato tris kiekvienos neapmokėtos sąskaitos faktūros apmokėjimo galimybes:</span><span class="sxs-lookup"><span data-stu-id="25281-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="25281-118">Galimybę, kad mokėjimas bus atliktas laiku (neviršijus sąskaitos faktūros apmokėjimo termino).</span><span class="sxs-lookup"><span data-stu-id="25281-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="25281-119">Galimybę, kad mokėjimas bus atliktas per 30 dienų nuo sąskaitos faktūros apmokėjimo termino.</span><span class="sxs-lookup"><span data-stu-id="25281-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="25281-120">Galimybę, kad mokėjimas bus atliktas vėliau nei per 30 dienų nuo sąskaitos faktūros apmokėjimo termino.</span><span class="sxs-lookup"><span data-stu-id="25281-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="25281-121">Mokėjimų galimybę galima peržiūrėti prognozių srityje.</span><span class="sxs-lookup"><span data-stu-id="25281-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="25281-122">[![Mokėjimų prognozės](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="25281-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="25281-123">Kiekvienai sąskaitai faktūrai taip pat priskiriama tikimybė, kad mokėjimas bus įvykdytas, naudojant vieną iš anksčiau pateiktų trijų prognozuojamų mokėjimo scenarijų.</span><span class="sxs-lookup"><span data-stu-id="25281-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="25281-124">Scenarijus, kurio mokėjimo tikimybė yra didžiausia, yra labiausiai tikėtinas scenarijus.</span><span class="sxs-lookup"><span data-stu-id="25281-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="25281-125">Pavyzdžiui, tarkime, kad sąskaitai faktūrai prognozuojama 71 procentų tikimybė, jog ji bus apmokėta laiku, 13 procentų – jog ji bus apmokėta per 30 dienų nuo apmokėjimo termino ir 16 procentų – jog ji bus apmokėta per vėliau nei 30 dienų nuo apmokėjimo termino.</span><span class="sxs-lookup"><span data-stu-id="25281-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="25281-126">Remiantis didžiausia tikimybė – kad sąskaita faktūra bus apmokėta laiku, todėl sąskaita faktūra bus pažymėta tikimybe, jog ji bus apmokėta laiku.</span><span class="sxs-lookup"><span data-stu-id="25281-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="25281-127">[![Mokėjimų prognozės](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="25281-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="25281-128">Optimizavimo strategijos</span><span class="sxs-lookup"><span data-stu-id="25281-128">Optimization strategies</span></span>

<span data-ttu-id="25281-129">Neskaitant mokėjimo prognozių, kliento mokėjimo įžvalgos (peržiūra) gali naudoti optimizavimo strategijas, kad pagerintų apmokėjimo laiku šansus.</span><span class="sxs-lookup"><span data-stu-id="25281-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="25281-130">Dėl to organizacijos gali atlikti galimų situacijų analizes, leisdamos vartotojams pakoreguoti sąskaitų faktūrų ir klientų parametrus ir tada palyginti atitinkamą poveikį sąskaitų faktūrų apmokėjimui laiku.</span><span class="sxs-lookup"><span data-stu-id="25281-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="25281-131">Pavyzdžiui, organizacija gali norėti įvertinti sąskaitų faktūrų mokėjimo nuolaidos poveikį mokėjimo laiku tikimybei.</span><span class="sxs-lookup"><span data-stu-id="25281-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="25281-132">Kai sąskaitos faktūros yra optimizuotos naudoti naują nuolaidą, vartotojai gali patikrinti nuolaidos taikymo poveikį sąskaitų faktūrų apmokėjimo laiku tikimybei.</span><span class="sxs-lookup"><span data-stu-id="25281-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="25281-133">Jei nuolaidos taikymo kaina yra minimali, lyginant ją su nauda, kai mokėjimai bus surinkti laiku, organizacija gali pasirinkti ateityje taikyti pasirinktą nuolaidą visiems atviriems užsakymams.</span><span class="sxs-lookup"><span data-stu-id="25281-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="25281-134">Šiuo metu kliento mokėjimo įžvalgose (peržiūra) kaip optimizavimo strategija galima tik nuolaida.</span><span class="sxs-lookup"><span data-stu-id="25281-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="25281-135">[![Optimizuotos prognozės](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="25281-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="25281-136">Kliento mokėjimo įžvalgų (peržiūra) gavimas</span><span class="sxs-lookup"><span data-stu-id="25281-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="25281-137">Jei susidomėjote galimybe išbandyti kliento mokėjimo įžvalgas (peržiūra), rašykite [Finansinių įžvalgų peržiūros komandai](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="25281-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="25281-138">Privatumo patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="25281-138">Privacy Statement</span></span>

<span data-ttu-id="25281-139">Peržiūros saugo klientų duomenis JAV.</span><span class="sxs-lookup"><span data-stu-id="25281-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="25281-140">Be to, peržiūros (1) gali naudoti mažiau privatumo ir saugos priemonių nei „Dynamics 365 for Finance and Operations“ paslauga, (2) jos nėra įtrauktos į susitarimą dėl šios paslaugos lygio, (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="25281-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>
