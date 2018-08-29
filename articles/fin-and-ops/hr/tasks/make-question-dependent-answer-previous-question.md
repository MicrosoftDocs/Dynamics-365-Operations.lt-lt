--- 
title: "Sukurti klausimus pagal atsakymą į ankstesnį klausimą"
description: "Sąlyginiai klausimai leidžia nurodyti, kokie kiti klausimai bus pateikiami respondentui, atsižvelgiant į atsakymą į ankstesnį klausimą."
author: ShylaThompson
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 3e0a6d63a266bf49764c8cdcfd407ff0733ea27c
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="make-questions-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="b39c6-103">Sukurti klausimus pagal atsakymą į ankstesnį klausimą</span><span class="sxs-lookup"><span data-stu-id="b39c6-103">Make questions dependent on the answer of the previous question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b39c6-104">Sąlyginiai klausimai leidžia nurodyti, kokie kiti klausimai bus pateikiami respondentui, atsižvelgiant į atsakymą į ankstesnį klausimą.</span><span class="sxs-lookup"><span data-stu-id="b39c6-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="b39c6-105">Pvz., jei klausiate „Kas labiau patinka, kava ar arbata?“, logiškas kitas klausimas gali būti nustatytas atsižvelgiant į tai, ar respondentas savo atsakyme pasirenka kavą ar arbatą.</span><span class="sxs-lookup"><span data-stu-id="b39c6-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="b39c6-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="b39c6-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="b39c6-107">Rasti esamą klausimyną</span><span class="sxs-lookup"><span data-stu-id="b39c6-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="b39c6-108">Pasirinkite Klausimynas > Kūrimas > Klausimynai.</span><span class="sxs-lookup"><span data-stu-id="b39c6-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="b39c6-109">Sąraše pasirinkite „WorkFH“ klaisimyną.</span><span class="sxs-lookup"><span data-stu-id="b39c6-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="b39c6-110">Įtraukti visus klausimus ir papildomus klausimus į klausimyną</span><span class="sxs-lookup"><span data-stu-id="b39c6-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="b39c6-111">Spustelėkite „Klausimai“.</span><span class="sxs-lookup"><span data-stu-id="b39c6-111">Click Questions.</span></span>
2. <span data-ttu-id="b39c6-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b39c6-112">Click New.</span></span>
3. <span data-ttu-id="b39c6-113">Lauke „Klausimas“ pasirinkite klausimą numeris 00016.</span><span class="sxs-lookup"><span data-stu-id="b39c6-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="b39c6-114">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b39c6-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b39c6-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b39c6-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b39c6-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b39c6-116">Click Save.</span></span>
7. <span data-ttu-id="b39c6-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b39c6-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="b39c6-118">Nustatyti sąlyginę klausimyno seką ir padaryti klausimą priklausomą nuo atitinkamo atsakymo</span><span class="sxs-lookup"><span data-stu-id="b39c6-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="b39c6-119">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="b39c6-119">Click Edit.</span></span>
2. <span data-ttu-id="b39c6-120">Išplėskite skyrių Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="b39c6-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="b39c6-121">Lauke „Klausimų tvarka“ pasirinkite „Sąlyginis“.</span><span class="sxs-lookup"><span data-stu-id="b39c6-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="b39c6-122">Spustelėkite „Sąlyginis klausimas“.</span><span class="sxs-lookup"><span data-stu-id="b39c6-122">Click Conditional question.</span></span>
5. <span data-ttu-id="b39c6-123">Medyje pasirinkite „Klausimai \ Paaiškinkite, kodėl pasirinkote tokį atsakymą į ankstesnį klausimą“.</span><span class="sxs-lookup"><span data-stu-id="b39c6-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="b39c6-124">Lauke „Pirminis klausimas“ pasirinkite klausimą 00009.</span><span class="sxs-lookup"><span data-stu-id="b39c6-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="b39c6-125">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b39c6-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b39c6-126">Lauke „Atsakymas“ įveskite atsakymo pasirinkimo, nuo kurio norite padaryti klausimą priklausomą, atsakymo sekos ID.</span><span class="sxs-lookup"><span data-stu-id="b39c6-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="b39c6-127">Pvz., įveskite 1 pasirinkdami pirmąjį atsakymą.</span><span class="sxs-lookup"><span data-stu-id="b39c6-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="b39c6-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b39c6-128">Click Save.</span></span>
10. <span data-ttu-id="b39c6-129">Medyje pasirinkite „Klausimai \ Ar man sąžiningai atlyginama už mano atliekamą darbą?“.</span><span class="sxs-lookup"><span data-stu-id="b39c6-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="b39c6-130">Atkreipkite dėmesį, kad atsinaujino klausimų medis parodydamas priklausomybę.</span><span class="sxs-lookup"><span data-stu-id="b39c6-130">Note that the question tree updated to show the dependency.</span></span>  


