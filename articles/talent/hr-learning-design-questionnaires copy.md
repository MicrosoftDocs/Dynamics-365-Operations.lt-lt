---
title: Klausimynų sudarymas
description: Šioje temoje aprašomas klausimyno kūrimo procesas. Pirmasis veiksmas yra sukurti klausimyno dizainą. Kai kuriate klausimyno dizainą, ne tik rašote klausimus ir atsakymus, tačiau taip pat sukuriate struktūrą, kuri leidžia atsakymus įrašyti ir tabuliuoti.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 7559a986c1a112eb1ccc6069ba5b8eb5c6e5b72b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461950"
---
# <a name="design-questionnaires"></a><span data-ttu-id="fdc3b-105">Klausimynų sudarymas</span><span class="sxs-lookup"><span data-stu-id="fdc3b-105">Design questionnaires</span></span>

<span data-ttu-id="fdc3b-106">Šioje temoje aprašomas klausimyno kūrimo procesas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-106">This topic describes the process for creating a questionnaire.</span></span> <span data-ttu-id="fdc3b-107">Pirmasis veiksmas yra sukurti klausimyno dizainą.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-107">The first step is to design the questionnaire.</span></span> <span data-ttu-id="fdc3b-108">Kai kuriate klausimyno dizainą, ne tik rašote klausimus ir atsakymus, tačiau taip pat sukuriate struktūrą, kuri leidžia atsakymus įrašyti ir tabuliuoti.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-108">When you design a questionnaire, you not only write the questions and answers, but also create the structure that enables answers to be recorded and tabulated.</span></span> 

<span data-ttu-id="fdc3b-109">Kruopščiai sudarytas klausimynas gali padėti padidinti surenkamų duomenų kokybę.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-109">A carefully designed questionnaire can help increase the quality of the data that you collect.</span></span> <span data-ttu-id="fdc3b-110">Kruopščiai sudarydami klausimyną, galite geriau tinkamu laiku parinkti tinkamas klausimyno parinktis.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-110">Through careful design, you can better select the appropriate options at the appropriate time for a questionnaire.</span></span> <span data-ttu-id="fdc3b-111">Tolesni punktai gali padėti suplanuoti efektyvų klausimyną.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-111">The following points can help you plan an effective questionnaire:</span></span>

-   <span data-ttu-id="fdc3b-112">Aiškiai apibrėžkite klausimyno paskirtį, kad užtikrintumėte, jog klausimai atitinka paskirtį.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-112">Clearly define the purpose of the questionnaire to help guarantee that the questions support the purpose.</span></span>
-   <span data-ttu-id="fdc3b-113">Nustatykite atskirą asmenį arba asmenų grupę, kurie turėtų pildyti klausimyną.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-113">Determine the individual person or the group of people who should complete the questionnaire.</span></span>
-   <span data-ttu-id="fdc3b-114">Užrašykite klausimus, kurie bus rodomi klausimyne, ir, jei taikytina, pateikite atsakymų pasirinkimus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-114">Write questions that will appear on the questionnaire, and include answer choices, if applicable.</span></span>
-   <span data-ttu-id="fdc3b-115">Įsitikinkite, kad klausimyno tėkmė logiška, kad respondentai liktų įsitraukę.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-115">Be sure that the questionnaire flows logically, so that respondents remain engaged.</span></span>
-   <span data-ttu-id="fdc3b-116">Klausimus ir atsakymus išdėstykite tokia tvarka, kuria jie turėtų būti pateikti respondentams.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-116">Arrange questions and answers in the order that they should be presented to respondents in.</span></span>
-   <span data-ttu-id="fdc3b-117">Jei reikia, nuspręskite, kaip reikėtų vertinti rezultatus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-117">Decide how the results should be evaluated, if applicable.</span></span>
-   <span data-ttu-id="fdc3b-118">Nuspręskite, ar jums reikės papildomų funkcijų.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-118">Decide whether you’ll need additional features.</span></span> <span data-ttu-id="fdc3b-119">Pvz., nustatykite, ar ir kaip turėtų būti kategorizuojami rezultatai, ar reikalingas laiko limitas ir ar visi klausimai bus privalomi.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-119">For example, determine whether and how results should be categorized, whether a time limit is required, or whether all the questions will be mandatory.</span></span>

<span data-ttu-id="fdc3b-120">Dizaino etapas apima keturias kategorijas užduočių, kurias turite atlikti tolesne tvarka.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-120">The design phase includes four categories of tasks that you must complete in this order:</span></span>

1.  <span data-ttu-id="fdc3b-121">Pagal poreikį nustatykite būtinąsias sąlygas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-121">Set up prerequisites, as required.</span></span>
2.  <span data-ttu-id="fdc3b-122">Jei reikia, nustatykite atsakymų grupes ir atsakymus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-122">Set up answer groups and answers, if applicable.</span></span>
3.  <span data-ttu-id="fdc3b-123">Nustatykite klausimus ir jų susiejimą su atsakymų grupėmis.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-123">Set up questions and their association with the answer groups.</span></span>
4.  <span data-ttu-id="fdc3b-124">Nustatykite patį klausimyną ir prie jo pridėkite klausimų.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-124">Set up the questionnaire itself, and attach questions to it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fdc3b-125">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-125">Prerequisites</span></span>
<span data-ttu-id="fdc3b-126">Prieš kuriant klausimynus, atsakymus ir klausimus, turi būti nustatytos kai kurios būtinosios sąlygos.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-126">Some prerequisites must be in place before you can create questionnaires, answers, and questions.</span></span> <span data-ttu-id="fdc3b-127">Tačiau, norint naudoti visas funkcijas, visų būtinųjų salygų nereikia.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-127">However, not all prerequisites are required for full functionality.</span></span>

### <a name="required"></a><span data-ttu-id="fdc3b-128">Būtina</span><span class="sxs-lookup"><span data-stu-id="fdc3b-128">Required</span></span>

| <span data-ttu-id="fdc3b-129">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="fdc3b-129">Prerequisite</span></span>        | <span data-ttu-id="fdc3b-130">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="fdc3b-130">Description</span></span>                |
|---------------------|----------------------------|
| <span data-ttu-id="fdc3b-131">Klausimynų tipai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-131">Questionnaire types</span></span> | <span data-ttu-id="fdc3b-132">Kategorizuokite klausimynus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-132">Categorize questionnaires.</span></span> |
| <span data-ttu-id="fdc3b-133">Klausimų tipai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-133">Question types</span></span>      | <span data-ttu-id="fdc3b-134">Kategorizuokite klausimus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-134">Categorize questions.</span></span>      |

### <a name="optional"></a><span data-ttu-id="fdc3b-135">Pasirinktinis</span><span class="sxs-lookup"><span data-stu-id="fdc3b-135">Optional</span></span>

| <span data-ttu-id="fdc3b-136">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="fdc3b-136">Prerequisite</span></span>             | <span data-ttu-id="fdc3b-137">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="fdc3b-137">Description</span></span>                                                    |
|--------------------------|----------------------------------------------------------------|
| <span data-ttu-id="fdc3b-138">Klausimynų parametrai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-138">Questionnaire parameters</span></span> | <span data-ttu-id="fdc3b-139">Modifikuokite pagrindinius klausimynų valdiklius ir numatytąsias nuostatas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-139">Modify basic controls and default settings for questionnaires.</span></span> |

### <a name="questionnaire-types"></a><span data-ttu-id="fdc3b-140">Klausimynų tipai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-140">Questionnaire types</span></span>

<span data-ttu-id="fdc3b-141">Kuriant klausimyną reikia priskirti jo tipą.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-141">Questionnaire types are required and must be assigned when you create a questionnaire.</span></span> <span data-ttu-id="fdc3b-142">Klausimynų tipai padeda juos lengviau valdyti ir klasifikuoti.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-142">Questionnaire types help you manage and classify questionnaires more easily.</span></span> <span data-ttu-id="fdc3b-143">Klausimynų tipus naudokite jiems klasifikuoti ir atskirti vienam nuo kito.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-143">Use questionnaire types to classify questionnaires and differentiate them from each other.</span></span> <span data-ttu-id="fdc3b-144">Pavyzdžiui, jei yra keli klausimynai, iš kurių galima rinktis, kad būtų lengviau rasti konkretų klausimyną, galite juos filtruoti pagal tipą.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-144">For example, if you have multiple questionnaires to select from, you can filter them by type to help make it easier to find a particular questionnaire.</span></span> <span data-ttu-id="fdc3b-145">Toliau pateikiami keli klausimynų tipų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-145">Here are some examples of questionnaire types:</span></span>

-   <span data-ttu-id="fdc3b-146">Personalo lavinimas</span><span class="sxs-lookup"><span data-stu-id="fdc3b-146">Human resource development</span></span>
-   <span data-ttu-id="fdc3b-147">Klientų apklausos</span><span class="sxs-lookup"><span data-stu-id="fdc3b-147">Customer surveys</span></span>
-   <span data-ttu-id="fdc3b-148">Peržiūros procesas</span><span class="sxs-lookup"><span data-stu-id="fdc3b-148">Review process</span></span>

### <a name="question-types"></a><span data-ttu-id="fdc3b-149">Klausimų tipai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-149">Question types</span></span>

<span data-ttu-id="fdc3b-150">Kuriant klasuimą reikia priskirti jo tipą.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-150">Question types are required and must be assigned when you create a question.</span></span> 

<span data-ttu-id="fdc3b-151">Klausimų tipus naudokite norėdami skirstyti klausimus į kategorijas, naudojamas ataskaitoms kurti.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-151">Use question types to categorize questions for reporting.</span></span> <span data-ttu-id="fdc3b-152">Naudojant klausimų tipus, taip pat lengviau rasti klausimus, nes **Klausimų** puslapyje tipus galite naudoti kaip filtrus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-152">Question types also make it easier to find questions, because you can use types as filters on the **Questions** page.</span></span> <span data-ttu-id="fdc3b-153">Toliau pateikiami keli klausimų tipų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-153">Here are some examples of question types:</span></span>

-   <span data-ttu-id="fdc3b-154">Žmogiškieji ištekliai.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-154">Human resource</span></span>
-   <span data-ttu-id="fdc3b-155">Verslo valdymas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-155">Managing business</span></span>
-   <span data-ttu-id="fdc3b-156">Kursų vertinimas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-156">Course evaluation</span></span>

### <a name="questionnaire-parameters"></a><span data-ttu-id="fdc3b-157">Klausimynų parametrai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-157">Questionnaire parameters</span></span>

<span data-ttu-id="fdc3b-158">Klausimynų parametrų nėra privalomi.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-158">Questionnaire parameters are optional.</span></span> <span data-ttu-id="fdc3b-159">Galite jų ir naudoti – tai priklauso nuo jūsų įmonės poreikių.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-159">You might not use them, depending on your company’s requirements.</span></span> 

<span data-ttu-id="fdc3b-160">Klausimynų parametrai apibrėžia klausimyno anonimiškumą, numeracijos kodus ir nuorodos tipus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-160">Questionnaire parameters define the anonymity, number sequence codes, and reference types of a questionnaire.</span></span> <span data-ttu-id="fdc3b-161">Kai organizacija platina klausimyną, gali tekti atsižvelgti į parinktį respondentams leisti likti anonimiškiems.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-161">When an organization distributes a questionnaire, the option to allow respondents to remain anonymous might be of concern.</span></span> 

<span data-ttu-id="fdc3b-162">Numeracijos kodai naudojami tvarkyti klausimams ir atsakymams.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-162">The number sequence codes are used to organize questions and answers.</span></span> <span data-ttu-id="fdc3b-163">Pagal šiuos numeracijos kodus elementams automatiškai priskiriamos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-163">Based on these number sequence codes, values are automatically assigned to items.</span></span> 

<span data-ttu-id="fdc3b-164">Prieš pradėdami kurti savo duomenis, turėtumėte apibrėžti visus parametrus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-164">You should define all parameters before you begin to create your data.</span></span> <span data-ttu-id="fdc3b-165">Klausimyno parametrų nuostatas modifikuoti galite bet kuriuo metu.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-165">You can modify the questionnaire parameter settings at any time.</span></span>

## <a name="questionnaire-components"></a><span data-ttu-id="fdc3b-166">Klausimynų komponentai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-166">Questionnaire components</span></span>
<span data-ttu-id="fdc3b-167">Klausimynus sudaro trys pagrindiniai elementai: atsakymų grupės, kuriose pateikiami atsakymai į klausimus su keliais pasirinkimas, klausimai ir pats klausimynas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-167">Questionnaires comprise three main elements: answer groups that contain the answers for multiple choice questions, questions, and the questionnaire itself.</span></span><span data-ttu-id="fdc3b-168">Neprivaloma: klausimyno klausimus galite grupuoti į rezultatų grupes.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-168"> You can optionally group the questions on a questionnaire into result groups.</span></span> <span data-ttu-id="fdc3b-169">Rezultatų grupės leidžia kategorizuoti klausimus ir pateikti išsamesnę klausimyno analizę.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-169">Result groups let you categorize questions and provide further analysis on the questionnaire.</span></span> 

<span data-ttu-id="fdc3b-170">[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span><span class="sxs-lookup"><span data-stu-id="fdc3b-170">[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)</span></span>

### <a name="answer-groups-and-answers"></a><span data-ttu-id="fdc3b-171">Atsakymų grupės ir atsakymai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-171">Answer groups and answers</span></span>

<span data-ttu-id="fdc3b-172">Respondentai į klausimą gali atsakyti dvejopai; tai priklauso nuo klausimo temos.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-172">Respondents can answer a question in two ways, depending on the subject of the question:</span></span>

-   <span data-ttu-id="fdc3b-173">Į atvirus klausimus konkrečiu formatu atsakyti nebūtina.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-173">Open-ended questions don’t require responses in a specific format.</span></span> <span data-ttu-id="fdc3b-174">Respondentai atsakymą surinkti gali kaip tekstą, skaičių, datą ar laiką.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-174">Respondents can type a response as text, a number, a date, or a time.</span></span> <span data-ttu-id="fdc3b-175">Užduodant tokius klausimus paprastai reikalaujama, kad respondentai atsakydami pateiktų subjektyvią informaciją, pvz., savo nuomonę, apibūdinimą, įvertinimą ar apskaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-175">These questions typically require that the respondents provide subjective information in their answers, such as an opinion, description, evaluation, or estimate.</span></span>
-   <span data-ttu-id="fdc3b-176">Į uždarus klausimus respondentas turi atsakyti pasirinkdamas atsakymą iš galimų teisingų atsakymų sąrašo.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-176">Closed-ended questions require that the respondent select an answer in a list of possible correct answers.</span></span>

<span data-ttu-id="fdc3b-177">Kurti galimų atsakymų į uždarus klausimus sąrašą galite **Atsakymų grupių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-177">To provide a list of possible answers for closed-ended questions, you can create answers on the **Answer groups** page.</span></span> 

<span data-ttu-id="fdc3b-178">Atsakymų grupės ir atsakymai yra komponentai, kurie sudaro informacijos pagrindą, iš kurio kuriami klausimai.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-178">Answer groups and answers are components that make up the main body of information that questions are created from.</span></span> <span data-ttu-id="fdc3b-179">Sukūrę atsakymų grupę, **Klausimų** puslapio lauke **Atsakymų grupė** ją galite susieti su klausimu.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-179">After you create an answer group, you can associate the answer group with a question in the **Answer group** field on the **Questions** page.</span></span> 

<span data-ttu-id="fdc3b-180">Atsakymų grupė gali būti naudojama daugiau nei vienam to paties klausimyno klausimui ir taip pat gali būt naudojama daugiau nei viename klausimyne.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-180">An answer group can be used for more than one question on the same questionnaire, and can also be used on more than one questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="fdc3b-181">Jei atsakymo tekstą modifikuojate atsakymų grupėse, kurios jau panaudotos užpildytuose klausimynuose, gali tapti sunku įvertinti duomenis, o klausimyno rezultatai gali nebegalioti.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-181">If you modify answer text in answer groups that have already been used on completed questionnaires, data can become difficult to evaluate, and questionnaire results might no longer be valid.</span></span> <span data-ttu-id="fdc3b-182">Jei reikia pakeisti atsakymų grupę, pagalvokite, ar ne geriau, užuot keičiant esamą atsakymų grupę, sukurti naują.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-182">If you must change an answer group, consider creating a new answer group instead of changing an existing one.</span></span> <span data-ttu-id="fdc3b-183">Atsakymų grupių, pridėtų prie klausimo ar atsakymo, arba atsakytų atsakymų grupių naikinti negalima.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-183">You can't delete answer groups that are attached to a question or answer, or that have been answered.</span></span>

### <a name="questions"></a><span data-ttu-id="fdc3b-184">Klausimai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-184">Questions</span></span>

<span data-ttu-id="fdc3b-185">Klausimyne turi būti klausimų.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-185">A questionnaire must contain questions.</span></span> <span data-ttu-id="fdc3b-186">Klausimai gali būti atviri arba uždari.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-186">Questions can be either open-ended or closed-ended.</span></span>

-   <span data-ttu-id="fdc3b-187">Atsakymai į atvirus klausimus nėra kontroliuojami, ir respondentai gali surinkti savo atsakymus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-187">The responses to open-ended questions aren't controlled, and respondents can type their answers.</span></span>
-   <span data-ttu-id="fdc3b-188">Uždariems klausimams reikalingas iš anksto apibrėžtų atsakymų parinkčių sąrašas, ir klausimus galima sukurti taip, kad respondentas galėtų pasirinkti kelis atsakymus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-188">Closed-ended questions require a list of predefined response options, and the questions can be structured to let a respondent select multiple responses.</span></span> <span data-ttu-id="fdc3b-189">Klausimai turėtų būti sudaryti taip, kad iš respondento išgautų konkrečią informaciją ir juos reikia susieti su atsakymų grupe, kurioje pateikiamos kiekvieno uždaro klausimo atsakymų parinktys.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-189">Questions should be designed to elicit specific information from a respondent and must be linked to an answer group that provides the response options for each closed-ended question.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="fdc3b-190">Prieš nustatydami uždarus klausimus, turite sukurti atsakymų grupes ir atsakymus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-190">Before you can set up closed-ended questions, you must create answer groups and answers.</span></span>

<span data-ttu-id="fdc3b-191">Klausimai gali būti išdėstyti sąlyginių klausimų hierarchija, kad antriniai klausimai priklausytų nuo atsakymo, kurį respondentas pasirenka į ankstesnį klausimą.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-191">Questions can be arranged in a conditional question hierarchy, so that secondary questions depend on the answer that the respondent selects for the previous question.</span></span> <span data-ttu-id="fdc3b-192">Pirmiausia galite parašyti klausimus, o juos išdėstyti į hierarchiją vėliau.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-192">You can write the questions first and then arrange them into a hierarchy later.</span></span>

## <a name="setting-up-questionnaires"></a><span data-ttu-id="fdc3b-193">Klausimynų nustatymas</span><span class="sxs-lookup"><span data-stu-id="fdc3b-193">Setting up questionnaires</span></span>

> [!NOTE]
> <span data-ttu-id="fdc3b-194">Prieš nustatydami klausimyną, turite nustatyti atsakymus, klausimus ir būtinąsias sąlygas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-194">Before you can set up a questionnaire, you must set up answers, questions, and prerequisites.</span></span> 

<span data-ttu-id="fdc3b-195">Kiekvienam klausimynui galite nurodyti tolesnę informaciją.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-195">For each questionnaire, you can specify the following information:</span></span>

-   <span data-ttu-id="fdc3b-196">Bendrą laiką arba laiko ribą, skirtą atsakyti į privalomus klausimus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-196">The total time or time limit to answer mandatory questions.</span></span>
-   <span data-ttu-id="fdc3b-197">Ar visi klausimai privalomi.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-197">Whether all questions are mandatory.</span></span>
-   <span data-ttu-id="fdc3b-198">Ar klausimyne skaičiuoti taškus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-198">Whether to calculate points on a questionnaire.</span></span>
-   <span data-ttu-id="fdc3b-199">Kaip kategorizuoti rezultatus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-199">How to categorize results.</span></span>
-   <span data-ttu-id="fdc3b-200">Ar klausimynas bus prieinamas tik ribotam respondentų skaičiui.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-200">Whether the questionnaire will be available to a restricted set of respondents.</span></span>
-   <span data-ttu-id="fdc3b-201">Ar kaip kiekvieno klausimyno puslapio fonas turėtų būti rodomas formos šablonas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-201">Whether a form template should be displayed as a background behind each page of the questionnaire.</span></span>
-   <span data-ttu-id="fdc3b-202">Ar, siekiant respondentams paaiškinti klausimyno tikslą, reikalingos papildomos pastabos.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-202">Whether additional notes are required in order to clarify the intent of the questionnaire for the respondents.</span></span>
-   <span data-ttu-id="fdc3b-203">Ar klausimus rodyti fiksuota tvarka, ar juos atsitiktinai pasirinkti iš telkinio.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-203">Whether to display questions in a fixed order or randomly select them from a pool.</span></span>
-   <span data-ttu-id="fdc3b-204">Ar klausimai bus užduoti tik jei į ankstesnius klausimus pateikiami konkretus atsakymai.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-204">Whether questions will be asked only if specific responses are given for previous answers.</span></span>

### <a name="set-up-a-questionnaire"></a><span data-ttu-id="fdc3b-205">Nustatyti klausimyną</span><span class="sxs-lookup"><span data-stu-id="fdc3b-205">Set up a questionnaire</span></span>

<span data-ttu-id="fdc3b-206">Pagrindinis puslapis, naudojamas nustatyti klausimynui, yra **Klausimynų** puslapis.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-206">The primary page that you use to set up a questionnaire is the **Questionnaires** page.</span></span> <span data-ttu-id="fdc3b-207">Norėdami nustatyti klausimyną, nurodyta tvarka atlikite tolesnes užduotis.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-207">To set up a questionnaire, complete the following tasks in order:</span></span>

1.  <span data-ttu-id="fdc3b-208">Sukurkite klausimyną.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-208">Create a questionnaire.</span></span>
2.  <span data-ttu-id="fdc3b-209">Norėdami į klausimyną pridėti klausimų, atlikite vieną iš tolesnių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-209">Follow one of these steps to attach questions to the questionnaire:</span></span>
    -   <span data-ttu-id="fdc3b-210">Jei naudojate rezultatų grupes, pridėti klausimų į klausimyną galite naudodami jas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-210">If you're using result groups, you can attach questions to a questionnaire by using result groups.</span></span> <span data-ttu-id="fdc3b-211">Pirmiausia nustatykite klausimyno rezultatų grupes ir tada į jas pridėkite klausimų.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-211">First set up the result groups for the questionnaire, and then add questions to the result groups.</span></span>
    -   <span data-ttu-id="fdc3b-212">Jei rezultatų grupių nenaudojate, klausimus galite pridėti tiesiai į klausimyną.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-212">If you aren't using result groups, you can attach questions directly to the questionnaire.</span></span>

3.  <span data-ttu-id="fdc3b-213">Jei reikia sąlyginių klausimų hierarchijos, ją nustatykite.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-213">Set up a conditional question hierarchy, if it's required.</span></span>
4.  <span data-ttu-id="fdc3b-214">Išbandykite klausimyną.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-214">Test the questionnaire.</span></span>

<span data-ttu-id="fdc3b-215">Norėdami išbandyti, ar klausimynas tinkamai sudarytas, puslapyje **Klausimynai** spustelėkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-215">On the **Questionnaires** page, click **Validate** to test whether the questionnaire is assembled correctly.</span></span> <span data-ttu-id="fdc3b-216">Tačiau taip pat yra naudinga prieš klausimyną platinant, jį užpildyti ir išbandyti patiems.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-216">However, it's also a good idea to complete the questionnaire and test it yourself before you distribute it.</span></span>

### <a name="modify-a-questionnaire"></a><span data-ttu-id="fdc3b-217">Modifikuoti klausimyną</span><span class="sxs-lookup"><span data-stu-id="fdc3b-217">Modify a questionnaire</span></span>

<span data-ttu-id="fdc3b-218">Tolesnes užduotis galite atlikti **Klausimynų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-218">You can complete the following tasks on the **Questionnaires** page:</span></span>

-   <span data-ttu-id="fdc3b-219">Modifikuoti klausimyno informaciją, pvz., rezultatų grupes ir klausimus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-219">Modify information in the questionnaire, such as the result groups and questions.</span></span>
-   <span data-ttu-id="fdc3b-220">Naikinti ir pridėti klausimų.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-220">Delete and add questions.</span></span>
-   <span data-ttu-id="fdc3b-221">Keisti rezultatų grupes ir sekos numerį.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-221">Make changes in the result groups and sequence number.</span></span> 

> [!CAUTION]
> <span data-ttu-id="fdc3b-222">Būkite atsargūs keisdami jau atsakytus klausimynus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-222">Be careful when you change questionnaires that have already been answered.</span></span> <span data-ttu-id="fdc3b-223">Keitimai gali sumažinti statistikos tikslumą, o tai gali būti prasto įvertinimo pagrindas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-223">Changes can reduce the accuracy of statistics and therefore make them a poor basis for evaluation.</span></span> <span data-ttu-id="fdc3b-224">Užuot keitę jau atsakytą klausimą, apsvarstykite galimybę sukurti naują.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-224">Consider creating a new question instead of changing a question that has already been answered.</span></span>

<span data-ttu-id="fdc3b-225">Klausimyne negalite panaikinti tolesnių klausimų tipų.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-225">In a questionnaire, you can't delete the following types of questions:</span></span>

-   <span data-ttu-id="fdc3b-226">Klausimai, pridėti prie klausimyno</span><span class="sxs-lookup"><span data-stu-id="fdc3b-226">Questions that are attached to a questionnaire</span></span>
-   <span data-ttu-id="fdc3b-227">Klausimai, į kuriuos jau atsakyta, ir kurie todėl rodomi **Atsakymų** dialogo lange.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-227">Questions that have already been answered and therefore appear in the **Answers** dialog box.</span></span>

### <a name="result-groups"></a><span data-ttu-id="fdc3b-228">Rezultatų grupės</span><span class="sxs-lookup"><span data-stu-id="fdc3b-228">Result groups</span></span>

<span data-ttu-id="fdc3b-229">Į klausimyną pridedant klausimų, rezultatų grupės nėra privalomos.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-229">Result groups are optional when you attach questions to a questionnaire.</span></span> 

<span data-ttu-id="fdc3b-230">Rezultatų grupė naudojama skaičiuoti klausimyno taškams ir kategorizuoti jo rezultatams.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-230">A result group is used to calculate points and categorize the results of a questionnaire.</span></span> <span data-ttu-id="fdc3b-231">Jei naudojate rezultatų grupės, galite atlikti tolesnes užduotis.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-231">If you use result groups, you can perform the following tasks:</span></span>

-   <span data-ttu-id="fdc3b-232">Remiantis taškų statistika įvertinti klausimyno rezultatus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-232">Evaluate questionnaire results, based on point statistics.</span></span>
-   <span data-ttu-id="fdc3b-233">Įvertinti kiekvienos nustatytos rezultatų grupės respondento rezultatą.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-233">Evaluate a respondent’s score for each result group that you set up.</span></span>
-   <span data-ttu-id="fdc3b-234">Generuoti kiekvienos rezultatų grupės statistiką, kuri padeda analizuoti rezultatus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-234">Generate statistics for each result group to help you analyze results.</span></span>
-   <span data-ttu-id="fdc3b-235">Spausdinti ataskaitą, kurioje rodomi kiekvienos rezultatų grupės rezultatai ir pasirinktiniai taškai / tekstai, paremti taškais, gaunamais kiekvienoje rezultatų grupėje.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-235">Print a report that shows results for each result group, and also optional points/texts that are based on points that are earned in each result group.</span></span>

> [!NOTE]
> <span data-ttu-id="fdc3b-236">Prieš nustatydami rezultatų grupes, turite atlikti tolesnes užduotis.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-236">Before you can set up result groups, you must complete the following tasks:</span></span>

-   <span data-ttu-id="fdc3b-237">Nustatyti uždarus klausimus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-237">Set up closed-ended questions.</span></span> <span data-ttu-id="fdc3b-238">Uždarų klausimų įvesties tipas **Klausimų** puslapyje turi būti **Žymės langelis**, **Alternatyvus mygtukas** arba **Pasirinktinio įvedimo laukas**.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-238">For a closed-ended question, the input type on the **Questions** page must be **Check box**, **Alternative button**, or **Combo box**.</span></span>
-   <span data-ttu-id="fdc3b-239">Apibrėžti kiekvienam klausimui priskirtų atsakymų grupių atsakymų taškus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-239">Define points for answers in the answer groups that are assigned to each question.</span></span>
-   <span data-ttu-id="fdc3b-240">Nustatyti klausimyną.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-240">Set up a questionnaire.</span></span>

<span data-ttu-id="fdc3b-241">Norėdami į klausimyną pridėti klausimų naudojant rezultatų grupes, pirmiausia nustatykite klausimyno rezultatų grupes ir tada į jas pridėkite klausimų.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-241">To attach questions to a questionnaire by using result groups, first set up the result groups for the questionnaire, and then add questions to the result groups.</span></span> <span data-ttu-id="fdc3b-242">Jei rezultatų grupių nenaudojate, klausimų pridėti galite tiesiai į klausimyną.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-242">If you don't use result groups, you can attach questions directly to a questionnaire.</span></span> 

<span data-ttu-id="fdc3b-243">Galite nustatyti kelias rezultatų grupes, kad įvertintumėte taškus, kuriuos respondentas gauna kiekvienoje kategorijoje.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-243">You can set up multiple result groups to evaluate the points that a respondent earns in each category.</span></span> <span data-ttu-id="fdc3b-244">Kai klausimynas baigtas, galite peržiūrėti surinktus kiekvienos rezultatų grupės taškus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-244">After a questionnaire is completed, you can view the points that have been achieved for each result group.</span></span> 

> [!TIP]
> <span data-ttu-id="fdc3b-245">Norėdami klausimyną įvertinti naudodami taškus, bet ne atskiras kategorijas, visus klausimus galite pridėti į vieną rezultatų grupę.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-245">To evaluate a questionnaire by using points but not separate categories, you can add all questions to a single result group.</span></span> 

<span data-ttu-id="fdc3b-246">Kiekvienai rezultatų grupei taip pat galite nustatyti vieną ar kelis taškais paremtus pranešimus, kuriuos užpildę klausimyną gauna respondentai.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-246">For each result group, you can also set up one or more point-based messages that respondents receive after they complete a questionnaire.</span></span> <span data-ttu-id="fdc3b-247">Rodomas tekstas gali skirtis – tai priklauso nuo rezultatų grupės rezultato, kurį respondentas pasiekia.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-247">The text that is shown can vary, depending on the score that a respondent achieves in a result group.</span></span> <span data-ttu-id="fdc3b-248">Norėdami naudoti taškais paremtus pranešimus, turite apibrėžti taškų intervalus ir kiekvieno intervalo aprašą.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-248">To use point-based messages, you must define point intervals and a description of each interval.</span></span> <span data-ttu-id="fdc3b-249">Kai respondentas pasiekia rezultatų konkrečiame intervale, to intervalo tekstas yra įtraukiamas rezultatų ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-249">When a respondent achieves a score in a specific interval, the text for that interval is included on the results report.</span></span> 

<span data-ttu-id="fdc3b-250">Kadangi rezultatų grupė yra susijusi su taškais, susietais su konkrečiais klausimyno klausimų rinkiniais, klausimyne galite naudoti tik konkrečią rezultatų grupę.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-250">Because a result group is related to the points that are associated with specific sets of questions on a questionnaire, you can use only a specific result group for a questionnaire.</span></span>

#### <a name="example-pointstexts-for-result-group-3"></a><span data-ttu-id="fdc3b-251">Pavyzdys: 3 rezultatų grupės taškai / tekstai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-251">Example: Points/texts for result group 3</span></span>

<span data-ttu-id="fdc3b-252">Naudojate lyderystei tikrinti skirtą klausimyną, kuriame 3 kategorijose yra 15 klausimų.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-252">You're using a questionnaire for a leadership test that has 15 questions in three categories.</span></span> <span data-ttu-id="fdc3b-253">Sukuriate tris rezultatų grupes ir į kiekvieną grupę pridedate penkis klausimus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-253">You create three result groups and add five questions to each result group.</span></span> <span data-ttu-id="fdc3b-254">Tada tose trijose grupėse sumuojami taškai.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-254">Points are then totaled in the three groups.</span></span> <span data-ttu-id="fdc3b-255">Šios trys rezultatų grupės nurodytos toliau.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-255">The three result groups are as follows:</span></span>

-   <span data-ttu-id="fdc3b-256">Kūrybiniai gebėjimai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-256">Creative abilities</span></span>
-   <span data-ttu-id="fdc3b-257">Vadovavimo gebėjimai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-257">Leadership abilities</span></span>
-   <span data-ttu-id="fdc3b-258">Techniniai gebėjimai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-258">Technical abilities</span></span>

<span data-ttu-id="fdc3b-259">Norint naudoti taškais paremtus pranešimus, nustatomi kiekvienos rezultatų grupės teksto intervalai.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-259">To use point-based messages, you set up text intervals for each result group.</span></span> <span data-ttu-id="fdc3b-260">Kiekvienam klausimui priskiriami du taškai.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-260">Each question is assigned two points.</span></span> <span data-ttu-id="fdc3b-261">Todėl maksimali kiekvienos rezultatų grupės taškų suma yra 10.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-261">Therefore, the maximum point total in each result group is 10.</span></span> 

<span data-ttu-id="fdc3b-262">Toliau pateikiamoje lentelėje rodomi taškais paremti pranešimai, apibrėžiami „lyderystės gebėjimų‟ rezultatų grupei.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-262">The following table shows the point-based messages that you define for the “leadership abilities” result group.</span></span>

| <span data-ttu-id="fdc3b-263">Taškų intervalas</span><span class="sxs-lookup"><span data-stu-id="fdc3b-263">Point interval</span></span> | <span data-ttu-id="fdc3b-264">Tekstas</span><span class="sxs-lookup"><span data-stu-id="fdc3b-264">Text</span></span>                                       |
|----------------|--------------------------------------------|
| <span data-ttu-id="fdc3b-265">Nuo 1 iki 3</span><span class="sxs-lookup"><span data-stu-id="fdc3b-265">1 to 3</span></span>         | <span data-ttu-id="fdc3b-266">Jūsų lyderystės gebėjimai vidutiniai.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-266">You have average leadership abilities.</span></span>     |
| <span data-ttu-id="fdc3b-267">Nuo 4 iki 7</span><span class="sxs-lookup"><span data-stu-id="fdc3b-267">4 to 7</span></span>         | <span data-ttu-id="fdc3b-268">Jūsų lyderystės gebėjimai geri.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-268">You have good leadership abilities.</span></span>        |
| <span data-ttu-id="fdc3b-269">Nuo 8 iki 10</span><span class="sxs-lookup"><span data-stu-id="fdc3b-269">8 to 10</span></span>        | <span data-ttu-id="fdc3b-270">Jūsų lyderystės gebėjimai puikūs.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-270">You have outstanding leadership abilities.</span></span> |

<span data-ttu-id="fdc3b-271">Galite nustatyti kiekvienos klausimyno rezultatų grupės taškų intervalus ir tekstus.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-271">You can set up point intervals and texts for each result group on a questionnaire.</span></span> <span data-ttu-id="fdc3b-272">Rodomi kiekvienos rezultatų grupės tekstai, atitinkantys kiekvieno respondento rezultatą.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-272">Texts that correspond to each respondent’s score are displayed for each result group.</span></span> 

> [!NOTE]
> <span data-ttu-id="fdc3b-273">Intervalus ir tekstus galite keisti.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-273">You can change intervals and texts.</span></span> <span data-ttu-id="fdc3b-274">Tačiau, jei klausimynas baigtas, pakeitimai gali sukelti skirtumų tarp ankstesnių ir naujų rezultatų ataskaitų.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-274">However, if a questionnaire has been completed, changes might cause differences between previous and new result reports.</span></span>

### <a name="conditional-question-hierarchies"></a><span data-ttu-id="fdc3b-275">Sąlyginių klausimų hierarchijos</span><span class="sxs-lookup"><span data-stu-id="fdc3b-275">Conditional question hierarchies</span></span>

<span data-ttu-id="fdc3b-276">Nustatant klausimyną, sąlyginių klausimų hierarchijos nėra privalomos.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-276">Conditional question hierarchies are optional when you set up a questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="fdc3b-277">Prieš nustatydami sąlyginių klausimų hierarchiją, į klausimyną turite pridėti klausimų, kuriems priskirtos atsakymų grupės.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-277">Before you can set up a conditional question hierarchy, you must attach questions that have assigned answer groups to the questionnaire.</span></span> 

<span data-ttu-id="fdc3b-278">Norėdami naudoti sąlyginius klausimus sukurti klausimyno klausimų hierarchijai, galite nustatyti, kad seka, kuria pateikiami klausimai, priklausytų nuo atsakymo, kurį respondentas pasirenka kiekviename klausime.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-278">To use conditional questions to create a question hierarchy in a questionnaire, you can make the sequence that questions are presented in depend on the answer that a respondent selects for each question.</span></span> <span data-ttu-id="fdc3b-279">Klausimų seką grįsdami respondento atsakymu, klausimyną galite modifikuoti respondentui jį pildant.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-279">By basing the question sequence on a respondent’s answer, you can modify the questionnaire as the respondent completes it.</span></span>

#### <a name="examples"></a><span data-ttu-id="fdc3b-280">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-280">Examples</span></span>

<span data-ttu-id="fdc3b-281">Juridinis subjektas savo klientams siūlo tiek prekes, tiek paslaugas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-281">A legal entity offers both items and services to its customers.</span></span> <span data-ttu-id="fdc3b-282">Kaip paprastai būna tokiais atvejais, kai kurie klientai perka tik prekes, kai kurie perka tik paslaugas, o kai kurie perka ir prekes, ir paslaugas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-282">As typically occurs in such cases, some customers purchase only items, some purchase only services, and some purchase both items and services.</span></span> <span data-ttu-id="fdc3b-283">Todėl, kai juridinis subjektas išplatina klientų pasitenkinimo apklausą, klausimynui jis pritaiko sąlyginę struktūrą, kad klientams, perkantiems tik paslaugas, nereikėtų atsakinėti į klausimus apie prekes.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-283">Therefore, when the legal entity distributes a customer satisfaction survey, it applies a conditional structure to the questionnaire, so that customers who purchase only services don't have to answer questions about items.</span></span> 

<span data-ttu-id="fdc3b-284">Arba klausimyną galite nustatyti taip, kad, jei 1 klausime respondentas pasirenka atsakymą A, klausimų sekoje kitas būtų 2 klausimas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-284">Alternatively, you set up a questionnaire so that if a respondent selects answer A for question 1, question 2 is next in the question sequence.</span></span> <span data-ttu-id="fdc3b-285">Tačiau, jei 1 klausime respondentas pasirenka atsakymą B, kitas yra 5 klausimas.</span><span class="sxs-lookup"><span data-stu-id="fdc3b-285">However, if the respondent selects answer B for question 1, question 5 is next.</span></span>

<a name="additional-resources"></a><span data-ttu-id="fdc3b-286">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-286">Additional resources</span></span>
--------

[<span data-ttu-id="fdc3b-287">Klausimynai</span><span class="sxs-lookup"><span data-stu-id="fdc3b-287">Questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="fdc3b-288">Klausimynų platinimas ir planavimas</span><span class="sxs-lookup"><span data-stu-id="fdc3b-288">Distribute and schedule questionnaires</span></span>](distribute-questionnaires.md)

[<span data-ttu-id="fdc3b-289">Klausimynų rezultatų peržiūra ir įvertinimas</span><span class="sxs-lookup"><span data-stu-id="fdc3b-289">View and evaluate the results of questionnaires</span></span>](evaluate-questionnaire-results.md)

