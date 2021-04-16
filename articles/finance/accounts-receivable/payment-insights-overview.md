---
title: Kliento mokėjimo įžvalgos (peržiūra)
description: Šioje temoje aprašomi mokėjimo įžvalgų pajėgumas, kuris padeda geriau suprasti įprastas atskirų klientų atsiskaitymo praktikas. Funkcija gali padėti apibrėžti aplinkybes, kuriomis reikėtų inicijuoti pinigų surinkimo procesus anksčiau, nei galbūt būtumėte tai padarę.
author: ShivamPandey-msft
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: a1b3b6540a03dc85d5dcd813e8c41ac49ab36728
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822400"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="1fef3-104">Kliento mokėjimo įžvalgos (peržiūra)</span><span class="sxs-lookup"><span data-stu-id="1fef3-104">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="1fef3-105">Šioje temoje aprašomi mokėjimo įžvalgų pajėgumas, kuris padeda geriau suprasti įprastas atskirų klientų atsiskaitymo praktikas.</span><span class="sxs-lookup"><span data-stu-id="1fef3-105">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices.</span></span> <span data-ttu-id="1fef3-106">Funkcija gali padėti apibrėžti aplinkybes, kuriomis reikėtų inicijuoti pinigų surinkimo procesus anksčiau, nei galbūt būtumėte tai padarę.</span><span class="sxs-lookup"><span data-stu-id="1fef3-106">The feature can help you identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="1fef3-107">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="1fef3-107">Overview</span></span>

<span data-ttu-id="1fef3-108">Gali būti sudėtinga prognozuoti, kada klientai apmokės sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="1fef3-108">It can be hard to predict when customers will pay their invoices.</span></span> <span data-ttu-id="1fef3-109">Dėl šios įžvalgos stokos, prognozuojami mažiau tikslūs grynųjų pinigų srautai, išieškojimo procesai pradedami per vėlai, o užsakymai yra patvirtinami klientams, kurie gali nevykdyti mokėjimo įsipareigojimų.</span><span class="sxs-lookup"><span data-stu-id="1fef3-109">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="1fef3-110">Kliento mokėjimo įžvalgos (peržiūra) padeda organizacijoms nuspėti, kada kliento sąskaita faktūra bus apmokėta.</span><span class="sxs-lookup"><span data-stu-id="1fef3-110">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="1fef3-111">Ši informacija gali padėti organizacijoms sukurti surinkimo strategijas, kurios padidintų tikimybę, kad būtų sumokėta laiku.</span><span class="sxs-lookup"><span data-stu-id="1fef3-111">This information can help organizations create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="1fef3-112">Prognozės</span><span class="sxs-lookup"><span data-stu-id="1fef3-112">Predictions</span></span>

<span data-ttu-id="1fef3-113">Mokėjimo prognozės suteiks organizacijoms galimybę tobulinti savo verslo procesus padėdamos lengvai identifikuoti sąskaitas faktūras, kurios gali būti apmokėtos pavėluotai, ir imtis priemonių, kurios padidintų tikimybę apmokėjimą gauti laiku.</span><span class="sxs-lookup"><span data-stu-id="1fef3-113">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="1fef3-114">Naudodamosi mašininio mokymosi modeliu, kuris naudoja istorines sąskaitas-faktūras, mokėjimus ir kliento duomenis, kliento mokėjimo įžvalgos (peržiūra) tiksliau prognozuos, kada klientas apmokės neapmokėtą sąskaitą-faktūrą.</span><span class="sxs-lookup"><span data-stu-id="1fef3-114">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="1fef3-115">Kiekvienai atvirai sąskaitai faktūrai kliento mokėjimo įžvalgos (peržiūra) gali numatyti tris mokėjimo galimybes.</span><span class="sxs-lookup"><span data-stu-id="1fef3-115">For each open invoice, Customer payment insights (Preview) can predict three payment probabilities:</span></span>

-   <span data-ttu-id="1fef3-116">Tikimybė, kad mokėjimas bus atliktas laiku</span><span class="sxs-lookup"><span data-stu-id="1fef3-116">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="1fef3-117">Tikimybė, kad mokėjimas bus atliktas pavėluotai</span><span class="sxs-lookup"><span data-stu-id="1fef3-117">Probability of payment being made late</span></span>
-   <span data-ttu-id="1fef3-118">Tikimybė, kad mokėjimas bus atliktas labai pavėluotai</span><span class="sxs-lookup"><span data-stu-id="1fef3-118">Probability of payment being made very late</span></span>

<span data-ttu-id="1fef3-119">Kliento mokėjimo įžvalgos (peržiūra) taip pat pateikia bendrą kaupiamąjį numatomo mokėjimo rodinį, kad padėtų organizacijoms suprasti visą mokėjimo sumą, kurią jie gali tikėtis gauti iš kliento vienu iš trijų laikotarpiu – laiku, pavėluotai, labai pavėluotai.</span><span class="sxs-lookup"><span data-stu-id="1fef3-119">Customer payment insights (Preview) also provides an aggregated view of expected payments, which can help organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late.</span></span>

<span data-ttu-id="1fef3-120">[![Kaupiamasis mokėjimo prognozių rodinys](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="1fef3-120">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="1fef3-121">Be to, kiekviena sąskaita faktūra yra priskirta tikimybei, kad bus apmokėta laiku.</span><span class="sxs-lookup"><span data-stu-id="1fef3-121">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="1fef3-122">Jei apmokėjimo laiku tikimybė yra mažesnė nei 50 %, sąskaitos faktūros pažymimos raudonu apskritimu, kuris nurodo, kad šias sąskaitas faktūras gali reikėti išieškoti.</span><span class="sxs-lookup"><span data-stu-id="1fef3-122">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="1fef3-123">[![Apmokėjimo tikimybių sąrašas](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="1fef3-123">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="1fef3-124">Kliento apmokėjimo įžvalgos (peržiūra) taip pat pateikia kontekstinę informaciją, siekiant paaiškinti prognozavimą, pavyzdžiui, svarbiausius faktorius, kurie turi įtakos prognozėms, dabartinę verslo padėtį su klientu ir informaciją apie istorinį kliento apmokėjimą elgesį.</span><span class="sxs-lookup"><span data-stu-id="1fef3-124">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="1fef3-125">Daugelyje įmonių išieškojimo procesas buvo reaktyvi veikla; išieškojimas procesas neprasideda iki sąskaitų faktūrų apmokėjimo termino.</span><span class="sxs-lookup"><span data-stu-id="1fef3-125">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="1fef3-126">Naudodamos kliento mokėjimo įžvalgas (peržiūra), organizacijos gali aktyviau taikyti išieškojimą.</span><span class="sxs-lookup"><span data-stu-id="1fef3-126">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="1fef3-127">Joms nebereikės laukti, kol operacijos pradės vėluoti, kad galėtų pradėti išieškojimo procesą.</span><span class="sxs-lookup"><span data-stu-id="1fef3-127">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="1fef3-128">Vietoje to, jos gali naudoti mokėjimo prognozės funkciją, kad galėtų nustatyti, ar iniciatyvūs išieškojimai pagerins tikimybę, kad bus sumokėta laiku.</span><span class="sxs-lookup"><span data-stu-id="1fef3-128">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="1fef3-129">Be to, mokėjimo prognozė suteikia įmonėms informacijos, kurios reikia norint pateisinti ankstyvą išieškojimo proceso pradžią.</span><span class="sxs-lookup"><span data-stu-id="1fef3-129">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="1fef3-130">Metodika</span><span class="sxs-lookup"><span data-stu-id="1fef3-130">Methodology</span></span>

<span data-ttu-id="1fef3-131">Kurti ir visuotinai diegti AI sprendimus yra sudėtinga.</span><span class="sxs-lookup"><span data-stu-id="1fef3-131">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="1fef3-132">Reikia duomenų mokslininkų, temos ekspertų ir inžinierių komandos, kuri ilgą laiką dirba, kad suformuluotų, sukurtų, visuotinai įdiegtų ir išlaikytų naudotiną DI sprendimą.</span><span class="sxs-lookup"><span data-stu-id="1fef3-132">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="1fef3-133">Mes stengiamės, kad AI sprendimus būtų lengva visuotinai įdiegti ir naudoti „Finance“.</span><span class="sxs-lookup"><span data-stu-id="1fef3-133">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="1fef3-134">Iš anksto supakuojame AI sprendimus „Finance“, kurie yra įdiegti ant „Microsoft AI Builder“.</span><span class="sxs-lookup"><span data-stu-id="1fef3-134">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="1fef3-135">Galutinis vartotojas vienu mygtuko paspaudimu gali visuotinai įdiegti AI sprendimą ir pradėti naudotis išmaniųjų prognozių privalumais.</span><span class="sxs-lookup"><span data-stu-id="1fef3-135">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="1fef3-136">Jei organizacija nepatenkinta prognozių tikslumu, patyręs vartotojas vienu mygtuko paspaudimu gali įvesti „AI builder“ plėtinio patirtį, tada pasirinkti arba panaikinti laukų, skirtų generuoti prognozes, pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="1fef3-136">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="1fef3-137">Kai pasiruošta, jie gali išmokyti ir publikuoti keitimus, o naujai išmokytas modelis bus automatiškai pasirenkamas prognozėms „Finance“.</span><span class="sxs-lookup"><span data-stu-id="1fef3-137">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="1fef3-138">Kaip gauti kliento mokėjimo įžvalgas (peržiūra)</span><span class="sxs-lookup"><span data-stu-id="1fef3-138">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="1fef3-139">Jei susidomėjote galimybe išbandyti kliento mokėjimo įžvalgas (peržiūra), siųskite el. laišką [Kliento mokėjimo įžvalgos (peržiūra)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="1fef3-139">Send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="1fef3-140">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="1fef3-140">Privacy Notice</span></span>

<span data-ttu-id="1fef3-141">Peržiūros (1) gali naudoti mažiau privatumo ir saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į susitarimą dėl šios paslaugos lygio, (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="1fef3-141">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]