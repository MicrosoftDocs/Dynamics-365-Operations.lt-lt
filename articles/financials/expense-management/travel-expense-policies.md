---
title: Išlaidų strategijų apibrėžimas
description: Galite apibrėžti išlaidų strategijas, kurių jūsų darbuotojai turi laikytis įvesdami ir pateikdami išlaidų ataskaitas ir kelionių paraiškas programoje „Microsoft Dynamics 365 for Finance and Operations“.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04eaff110fea021ddee32be650be540894eb703b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "342436"
---
# <a name="expense-policies"></a><span data-ttu-id="dd665-103">Išlaidų strategija</span><span class="sxs-lookup"><span data-stu-id="dd665-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd665-104">Galite apibrėžti strategijas, kurių jūsų darbuotojai turi laikytis įvesdami ir pateikdami išlaidų ataskaitas ir kelionių paraiškas.</span><span class="sxs-lookup"><span data-stu-id="dd665-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="dd665-105">Išlaidų strategijos įgyvendinimas gali padėti veiksmingai valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="dd665-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="dd665-106">Pavyzdžiui, galite nustatyti viešbučio išlaidų Niujorke strategiją, kad išlaidos viešbučiui vienai parai negali viršyti 250 USD.</span><span class="sxs-lookup"><span data-stu-id="dd665-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="dd665-107">Jei darbuotojas pateikia išlaidų ataskaitą ar kelionės paraišką, kurioje kambario tarifas viršija šią sumą, sistema praneš</span><span class="sxs-lookup"><span data-stu-id="dd665-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="dd665-108">kad pagal išlaidų strategiją suma yra viršyta.</span><span class="sxs-lookup"><span data-stu-id="dd665-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="dd665-109">Sukonfigūruoti pranešimą, kurį gaus darbuotojas, galite</span><span class="sxs-lookup"><span data-stu-id="dd665-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="dd665-110">apibrėždami strategiją.</span><span class="sxs-lookup"><span data-stu-id="dd665-110">define the policy.</span></span>      
        
<span data-ttu-id="dd665-111">Galite apibrėžti trijų tolesnių tipų strategijas.</span><span class="sxs-lookup"><span data-stu-id="dd665-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="dd665-112">Įspėjimas – darbuotojui leidžia pateikti išlaidų ataskaitą arba kelionės paraišką, tačiau išlaidos bus pažymėtos visiems tvirtintojams ir</span><span class="sxs-lookup"><span data-stu-id="dd665-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="dd665-113">vėlesnėms ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="dd665-113">for later reporting.</span></span>        

- <span data-ttu-id="dd665-114">Klaida – reikalauja, kad, prieš pateikdamas išlaidų ataskaitą arba kelionės paraišką, darbuotojas pagal strategiją peržiūrėtų išlaidas.</span><span class="sxs-lookup"><span data-stu-id="dd665-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
  - <span data-ttu-id="dd665-115">Pateisinimas – reikalauja, kad, prieš pateikdamas išlaidų ataskaitą ar kelionės paraišką, darbuotojas ar vadovas įvestų viršytos strategijos sumos pateisinimą.</span><span class="sxs-lookup"><span data-stu-id="dd665-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
  <span data-ttu-id="dd665-116">Be to, galite nustatyti laikotarpį, kurio metu galioja išlaidų strategija.</span><span class="sxs-lookup"><span data-stu-id="dd665-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="dd665-117">Pavyzdžiui, oro linijų skrydžiai iš Danijos</span><span class="sxs-lookup"><span data-stu-id="dd665-117">For example, airline fares for flights between Denmark</span></span>      
  <span data-ttu-id="dd665-118">į Niujorką gali būti brangesni atostogų kelionių piko metu</span><span class="sxs-lookup"><span data-stu-id="dd665-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="dd665-119">Galite nustatyti skrydžių išlaidų taisyklę, kuri apribotų</span><span class="sxs-lookup"><span data-stu-id="dd665-119">You can define a flight expense rule that restricts the</span></span>      
  <span data-ttu-id="dd665-120">skrydžių į Niujorką išlaidas iki 5000 Danijos kronų, ir galite nustatyti, kad ši taisyklė galiotų nuo kovo 15 d. iki</span><span class="sxs-lookup"><span data-stu-id="dd665-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
  <span data-ttu-id="dd665-121">rugsėjo 15 d.</span><span class="sxs-lookup"><span data-stu-id="dd665-121">September 15.</span></span>
