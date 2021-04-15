---
title: Kurti uždarą klausimą
description: Uždari klausimai leidžia suteikti respondentui pasirinkimo variantų.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41e12e6f35237ea125756b502d5cebed58c6bf55
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790649"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="5226c-103">Kurti uždarą klausimą</span><span class="sxs-lookup"><span data-stu-id="5226c-103">Create a closed ended question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="5226c-104">Uždari klausimai leidžia suteikti respondentui pasirinkimo variantų.</span><span class="sxs-lookup"><span data-stu-id="5226c-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="5226c-105">Pirmiausia, turite sukurti atsakymų grupę su atsakymais, tada sukurkite klausimą, kuris naudos atsakymų grupę.</span><span class="sxs-lookup"><span data-stu-id="5226c-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="5226c-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="5226c-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="5226c-107">Kurti atsakymų grupę</span><span class="sxs-lookup"><span data-stu-id="5226c-107">Create an answer group</span></span>
1. <span data-ttu-id="5226c-108">Eikite į Klausimynas > Kūrimas > Atsakymų grupės.</span><span class="sxs-lookup"><span data-stu-id="5226c-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="5226c-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="5226c-109">Click New.</span></span>
3. <span data-ttu-id="5226c-110">Lauke „Atsakymų grupė“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5226c-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="5226c-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5226c-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="5226c-112">Naudokite funkciją „Atsitiktinė tvarka“, kad atsakymai būtų pateikiami atsitiktinai vis kitokia tvarka kiekvieną kartą, kai klausimui naudojama atsakymų grupė.</span><span class="sxs-lookup"><span data-stu-id="5226c-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="5226c-113">Spustelėkite „Atsakyti“.</span><span class="sxs-lookup"><span data-stu-id="5226c-113">Click Answer.</span></span>
6. <span data-ttu-id="5226c-114">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="5226c-114">Click New.</span></span>
    * <span data-ttu-id="5226c-115">Atsakymų rodymo tvarką valdo sekos numeris, nebent atsakymų grupui taikoma „Atsitiktinė tvarka“.</span><span class="sxs-lookup"><span data-stu-id="5226c-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="5226c-116">Klausimynas gali būti vertinamas atsakymams skiriant taškus.</span><span class="sxs-lookup"><span data-stu-id="5226c-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="5226c-117">Lauke „Taškai“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5226c-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="5226c-118">Galima pažymėti teisingą atsakymą parodant, kad pasirinktas atsakymas yra teisingas.</span><span class="sxs-lookup"><span data-stu-id="5226c-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="5226c-119">Tai gali būti naudojama vertinant klausimyną.</span><span class="sxs-lookup"><span data-stu-id="5226c-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="5226c-120">Lauke „Atsakymas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5226c-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="5226c-121">Toliau kurkite atsakymų pasirinkimo parinktis atsakymų grupei.</span><span class="sxs-lookup"><span data-stu-id="5226c-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="5226c-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="5226c-122">Click New.</span></span>
10. <span data-ttu-id="5226c-123">Lauke „Taškai“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5226c-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="5226c-124">Lauke „Atsakymas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5226c-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="5226c-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="5226c-125">Click New.</span></span>
13. <span data-ttu-id="5226c-126">Lauke „Taškai“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5226c-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="5226c-127">Lauke „Atsakymas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5226c-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="5226c-128">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="5226c-128">Click New.</span></span>
16. <span data-ttu-id="5226c-129">Lauke „Taškai“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5226c-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="5226c-130">Lauke „Atsakymas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5226c-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="5226c-131">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="5226c-131">Click New.</span></span>
19. <span data-ttu-id="5226c-132">Lauke „Taškai“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5226c-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="5226c-133">Lauke „Atsakymas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5226c-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="5226c-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="5226c-134">Close the page.</span></span>
22. <span data-ttu-id="5226c-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="5226c-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="5226c-136">Kurti klausimą</span><span class="sxs-lookup"><span data-stu-id="5226c-136">Create the question</span></span>
1. <span data-ttu-id="5226c-137">Pasirinkite Klausimynas > Kūrimas > Klausimai.</span><span class="sxs-lookup"><span data-stu-id="5226c-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="5226c-138">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="5226c-138">Click New.</span></span>
3. <span data-ttu-id="5226c-139">Naudokite lauką „Tipas“, kad sugrupuotumėte susijusius klausimus.</span><span class="sxs-lookup"><span data-stu-id="5226c-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="5226c-140">Galite naudoti įvesties tipo žymės langelį, alternatyvų mygtuką arba pasirinktinio įvedimo lauką uždariems klausimams.</span><span class="sxs-lookup"><span data-stu-id="5226c-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="5226c-141">Lauke „Įvesties tipas“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="5226c-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="5226c-142">Lauke Atsakymų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5226c-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="5226c-143">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5226c-143">In the Text field, type a value.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]