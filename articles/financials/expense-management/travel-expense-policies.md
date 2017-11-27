---
title: "Išlaidų strategijų apibrėžimas"
description: "Galite apibrėžti išlaidų strategijas, kurių turi laikytis jūsų darbuotojai įvesdami ir pateikdami išlaidų ataskaitas bei kelionių paraiškas sprendime „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“."
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9a5ce1a3b6519b510c9f5aa5618ab91f77a2d91a
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="expense-policies"></a><span data-ttu-id="00b5d-103">Išlaidų strategija</span><span class="sxs-lookup"><span data-stu-id="00b5d-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="00b5d-104">Galite apibrėžti strategijas, kurių jūsų darbuotojai turi laikytis įvesdami ir pateikdami išlaidų ataskaitas ir kelionių paraiškas.</span><span class="sxs-lookup"><span data-stu-id="00b5d-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="00b5d-105">Išlaidų strategijos įgyvendinimas gali padėti veiksmingai valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="00b5d-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="00b5d-106">Pavyzdžiui, galite nustatyti viešbučio išlaidų Niujorke strategiją, kad išlaidos viešbučiui vienai parai negali viršyti 250 USD.</span><span class="sxs-lookup"><span data-stu-id="00b5d-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="00b5d-107">Jei darbuotojas pateikia išlaidų ataskaitą ar kelionės paraišką, kurioje kambario tarifas viršija šią sumą, sistema praneš darbuotojui, kad pagal išlaidų strategiją suma yra viršyta.</span><span class="sxs-lookup"><span data-stu-id="00b5d-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="00b5d-108">Apibrėždami strategiją galite sukonfigūruoti pranešimą, kurį gaus darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="00b5d-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="00b5d-109">Galite apibrėžti trijų tolesnių tipų strategijas.</span><span class="sxs-lookup"><span data-stu-id="00b5d-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="00b5d-110">Įspėjimas – darbuotojui leidžia pateikti išlaidų ataskaitą arba kelionės paraišką, tačiau išlaidos bus pažymėtos visiems tvirtintojams ir</span><span class="sxs-lookup"><span data-stu-id="00b5d-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="00b5d-111">vėlesnėms ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="00b5d-111">for later reporting.</span></span> 
 - <span data-ttu-id="00b5d-112">Klaida – reikalauja, kad, prieš pateikdamas išlaidų ataskaitą arba kelionės paraišką, darbuotojas pagal strategiją peržiūrėtų išlaidas.</span><span class="sxs-lookup"><span data-stu-id="00b5d-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="00b5d-113">Pateisinimas – reikalauja, kad, prieš pateikdamas išlaidų ataskaitą ar kelionės paraišką, darbuotojas ar vadovas įvestų viršytos strategijos sumos pateisinimą.</span><span class="sxs-lookup"><span data-stu-id="00b5d-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="00b5d-114">Be to, galite nustatyti laikotarpį, kurio metu galioja išlaidų strategija.</span><span class="sxs-lookup"><span data-stu-id="00b5d-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="00b5d-115">Pavyzdžiui, oro linijų skrydžiai iš Danijos į Niujorką gali būti brangesni atostogų kelionių piko metu.</span><span class="sxs-lookup"><span data-stu-id="00b5d-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="00b5d-116">Galite nustatyti skrydžių išlaidų taisyklę, kuri apribotų skrydžių į Niujorką išlaidas iki 5000 Danijos kronų, ir galite nustatyti, kad ši taisyklė galiotų nuo kovo 15 d. iki rugsėjo 15 d.</span><span class="sxs-lookup"><span data-stu-id="00b5d-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 

