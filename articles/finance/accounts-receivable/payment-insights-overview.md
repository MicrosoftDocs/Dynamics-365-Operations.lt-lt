---
title: Kliento mokėjimo įžvalgos (peržiūra)
description: Šioje temoje aprašomos mokėjimo įžvalgų galimybės, kurios padeda geriau suprasti įprastas atskirų klientų mokėjimo praktikas ir gali identifikuoti aplinkybes, pateisinančias išieškojimo procesus anksčiau nei jūs padarėte kitaip.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
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
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774010"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="c5ea1-103">Kliento mokėjimo įžvalgos (peržiūra)</span><span class="sxs-lookup"><span data-stu-id="c5ea1-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c5ea1-104">Šioje temoje aprašomos mokėjimo įžvalgų galimybės, kurios padeda geriau suprasti įprastas atskirų klientų mokėjimo praktikas ir kurios gali identifikuoti aplinkybes, pateisinančias išieškojimo procesus anksčiau nei jūs galėjote padaryti kitaip.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="c5ea1-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="c5ea1-105">Overview</span></span>

<span data-ttu-id="c5ea1-106">Organizacijoms dažnai sudėtinga prognozuoti, kada klientai apmokės sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="c5ea1-107">Dėl šios įžvalgos stokos, prognozuojami mažiau tikslūs grynųjų pinigų srautai, išieškojimo procesai pradedami per vėlai, o užsakymai yra patvirtinami klientams, kurie gali nevykdyti mokėjimo įsipareigojimų.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="c5ea1-108">Kliento mokėjimo įžvalgos (peržiūra) padeda organizacijoms numatyti, kada klientai apmokės sąskaitas faktūras, ir padeda sukurti išieškojimo strategijas, kurios padidina apmokėjimo laiku tikimybę.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="c5ea1-109">Prognozės</span><span class="sxs-lookup"><span data-stu-id="c5ea1-109">Predictions</span></span>

<span data-ttu-id="c5ea1-110">Mokėjimo prognozės suteiks organizacijoms galimybę tobulinti savo verslo procesus padėdamos lengvai identifikuoti sąskaitas faktūras, kurios gali būti apmokėtos pavėluotai, ir imtis priemonių, kurios padidintų tikimybę apmokėjimą gauti laiku.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="c5ea1-111">Naudodamosi mašininio mokymosi modeliu, kuris naudoja istorines sąskaitas-faktūras, mokėjimus ir kliento duomenis, kliento mokėjimo įžvalgos (peržiūra) tiksliau prognozuos, kada klientas apmokės neapmokėtą sąskaitą-faktūrą.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="c5ea1-112">Kiekvienai atvirai sąskaitai faktūrai kliento mokėjimo įžvalgos (peržiūra) numato tris mokėjimo galimybes:</span><span class="sxs-lookup"><span data-stu-id="c5ea1-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="c5ea1-113">Tikimybė, kad mokėjimas bus atliktas laiku</span><span class="sxs-lookup"><span data-stu-id="c5ea1-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="c5ea1-114">Tikimybė, kad mokėjimas bus atliktas pavėluotai</span><span class="sxs-lookup"><span data-stu-id="c5ea1-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="c5ea1-115">Tikimybė, kad mokėjimas bus atliktas labai  pavėluotai</span><span class="sxs-lookup"><span data-stu-id="c5ea1-115">Probability of payment being made very late</span></span>

<span data-ttu-id="c5ea1-116">Norėdami padėti organizacijoms suprasti visą mokėjimo sumą, kurią jie gali tikėtis gauti iš kliento vienu iš trijų laikotarpiu – laiku, pavėluotai, labai pavėluotai – kliento mokėjimų įžvalgos (peržiūra) taip pat pateikia bendrą kaupiamąjį numatomo mokėjimo rodinį.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="c5ea1-117">[![Kaupiamasis mokėjimo prognozių rodinys](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="c5ea1-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="c5ea1-118">Be to, kiekviena sąskaita faktūra yra priskirta tikimybei, kad bus apmokėta laiku.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="c5ea1-119">Jei apmokėjimo laiku tikimybė yra mažesnė nei 50 %, sąskaitos faktūros pažymimos raudonu apskritimu, kuris nurodo, kad šias sąskaitas faktūras gali reikėti išieškoti.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="c5ea1-120">[![Apmokėjimo tikimybių sąrašas](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="c5ea1-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="c5ea1-121">Kliento apmokėjimo įžvalgos (peržiūra) taip pat pateikia kontekstinę informaciją, siekiant paaiškinti prognozavimą, pavyzdžiui, svarbiausius faktorius, kurie turi įtakos prognozėms, dabartinę verslo padėtį su klientu ir informaciją apie istorinį kliento apmokėjimą elgesį.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="c5ea1-122">Daugelyje įmonių išieškojimo procesas buvo reaktyvi veikla; išieškojimas procesas neprasideda iki sąskaitų faktūrų apmokėjimo termino.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="c5ea1-123">Naudodamos kliento mokėjimo įžvalgas (peržiūra), organizacijos gali aktyviau taikyti išieškojimą.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="c5ea1-124">Joms nebereikės laukti, kol operacijos pradės vėluoti, kad galėtų pradėti išieškojimo procesą.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="c5ea1-125">Vietoje to, jos gali naudoti mokėjimo prognozės funkciją, kad galėtų nustatyti, ar iniciatyvūs išieškojimai pagerins tikimybę, kad bus sumokėta laiku.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="c5ea1-126">Be to, mokėjimo prognozė suteikia įmonėms informacijos, kurios reikia norint pateisinti ankstyvą išieškojimo proceso pradžią.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="c5ea1-127">Metodika</span><span class="sxs-lookup"><span data-stu-id="c5ea1-127">Methodology</span></span>

<span data-ttu-id="c5ea1-128">Kurti ir visuotinai diegti AI sprendimus yra sudėtinga.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="c5ea1-129">Reikia duomenų mokslininkų, temos ekspertų ir inžinierių komandos, kuri ilgą laiką dirba, kad suformuluotų, sukurtų, visuotinai įdiegtų ir išlaikytų naudotiną AI sprendimą.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="c5ea1-130">Mes stengiamės, kad AI sprendimus būtų lengva visuotinai įdiegti ir naudoti „Finance“.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="c5ea1-131">Iš anksto supakuojame AI sprendimus „Finance“, kurie yra įdiegti ant „Microsoft AI Builder“.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="c5ea1-132">Galutinis vartotojas vienu mygtuko paspaudimu gali visuotinai įdiegti AI sprendimą ir pradėti naudotis išmaniųjų prognozių privalumais.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="c5ea1-133">Jei organizacija nepatenkinta prognozių tikslumu, patyręs vartotojas vienu mygtuko paspaudimu gali įvesti „AI builder“ plėtinio patirtį, tada pasirinkti arba panaikinti laukų, skirtų generuoti prognozes, pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="c5ea1-134">Kai pasiruošta, jie gali išmokyti ir publikuoti keitimus, o naujai išmokytas modelis bus automatiškai pasirenkamas prognozėms „Finance“.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="c5ea1-135">Kaip gauti kliento mokėjimo įžvalgas (peržiūra)</span><span class="sxs-lookup"><span data-stu-id="c5ea1-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="c5ea1-136">Jei susidomėjote galimybe išbandyti kliento mokėjimo įžvalgas (peržiūra), siųskite el. laišką [Kliento mokėjimo įžvalgos (peržiūra)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="c5ea1-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="c5ea1-137">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="c5ea1-137">Privacy Notice</span></span>

<span data-ttu-id="c5ea1-138">Peržiūros (1) gali naudoti mažiau privatumo ir saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į susitarimą dėl šios paslaugos lygio, (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="c5ea1-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


