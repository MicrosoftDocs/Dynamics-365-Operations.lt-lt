---
title: Išlaidų strategijų apibrėžimas
description: Galite apibrėžti išlaidų strategijas, kurių jūsų darbuotojai turi laikytis įvesdami ir pateikdami išlaidų ataskaitas ir kelionių paraiškas programoje „Microsoft Dynamics 365 for Finance and Operations“.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f0ff56f0ff106bc168b6a27612e08743a539a07
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1514444"
---
# <a name="expense-policies"></a><span data-ttu-id="53a33-103">Išlaidų strategija</span><span class="sxs-lookup"><span data-stu-id="53a33-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53a33-104">Galite apibrėžti strategijas, kurių jūsų darbuotojai turi laikytis įvesdami ir pateikdami išlaidų ataskaitas ir kelionių paraiškas.</span><span class="sxs-lookup"><span data-stu-id="53a33-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="53a33-105">Išlaidų strategijos įgyvendinimas gali padėti veiksmingai valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="53a33-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="53a33-106">Pavyzdžiui, galite nustatyti viešbučio išlaidų Niujorke strategiją, kad išlaidos viešbučiui vienai parai negali viršyti 250 USD.</span><span class="sxs-lookup"><span data-stu-id="53a33-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="53a33-107">Jei darbuotojas pateikia išlaidų ataskaitą ar kelionės paraišką, kurioje kambario tarifas viršija šią sumą, sistema praneš</span><span class="sxs-lookup"><span data-stu-id="53a33-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="53a33-108">kad pagal išlaidų strategiją suma yra viršyta.</span><span class="sxs-lookup"><span data-stu-id="53a33-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="53a33-109">Sukonfigūruoti pranešimą, kurį gaus darbuotojas, galite</span><span class="sxs-lookup"><span data-stu-id="53a33-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="53a33-110">apibrėždami strategiją.</span><span class="sxs-lookup"><span data-stu-id="53a33-110">define the policy.</span></span>      
        
<span data-ttu-id="53a33-111">Galite apibrėžti trijų tolesnių tipų strategijas.</span><span class="sxs-lookup"><span data-stu-id="53a33-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="53a33-112">Įspėjimas – darbuotojui leidžia pateikti išlaidų ataskaitą arba kelionės paraišką, tačiau išlaidos bus pažymėtos visiems tvirtintojams ir</span><span class="sxs-lookup"><span data-stu-id="53a33-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="53a33-113">vėlesnėms ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="53a33-113">for later reporting.</span></span>        

- <span data-ttu-id="53a33-114">Klaida – reikalauja, kad, prieš pateikdamas išlaidų ataskaitą arba kelionės paraišką, darbuotojas pagal strategiją peržiūrėtų išlaidas.</span><span class="sxs-lookup"><span data-stu-id="53a33-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="53a33-115">Pateisinimas – reikalauja, kad, prieš pateikdamas išlaidų ataskaitą ar kelionės paraišką, darbuotojas ar vadovas įvestų viršytos strategijos sumos pateisinimą.</span><span class="sxs-lookup"><span data-stu-id="53a33-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

# <a name="policy-tips"></a><span data-ttu-id="53a33-116">Strategijos patarimai</span><span class="sxs-lookup"><span data-stu-id="53a33-116">Policy tips</span></span>
<span data-ttu-id="53a33-117">Pateikiame kelis pasiūlymus, kurie gali padėti sukurti naujas išlaidų valdymo strategijas.</span><span class="sxs-lookup"><span data-stu-id="53a33-117">Here are a few suggestions that can assist you whe creating new policies for expense management.</span></span> 
* <span data-ttu-id="53a33-118">Strategijos įsigalioja nuo nurodytos datos ir neturi įtakos, jei strategija sukurta po patirtų išlaidų.</span><span class="sxs-lookup"><span data-stu-id="53a33-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="53a33-119">Pavyzdžiui, jei šiandien kuriate naują strategiją, kad išlaidos maistui neviršytų 50 USD, bet kurios esamos išlaidos, įvestos vakar, nebus tikrinamos pagal šią strategiją.</span><span class="sxs-lookup"><span data-stu-id="53a33-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="53a33-120">Kuriant išlaidų kategorijos strategiją, kurią galima detaliai išvardyti eilutėmis, siūlome pridėti sąlygą dėl išlaidų eilutės tipo.</span><span class="sxs-lookup"><span data-stu-id="53a33-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="53a33-121">Kai kurios strategijos, pvz., kvito reikalavimas, gali netikti detaliam išvardijimui eilutėmis ir turėtų būti taikomas tik antraštės eilutei arba nedetaliai eilutei.</span><span class="sxs-lookup"><span data-stu-id="53a33-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 

# <a name="when-to-evaluate-policies"></a><span data-ttu-id="53a33-122">Kada vertinti strategijas</span><span class="sxs-lookup"><span data-stu-id="53a33-122">When to evaluate policies</span></span>

<span data-ttu-id="53a33-123">Išlaidų valdymo parametruose yra parinktis vertinti išlaidų valdymo strategijas, kai eilutė įrašoma, arba kai pateikiama išlaidų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="53a33-123">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="53a33-124">Jei pasirinksite įvertinti, kai eilutė įrašoma, užtikrinsite, kad vartotojai iš anksto matys, ką reikia padaryti, kad iš karto užbaigtų savo išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="53a33-124">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="53a33-125">Kitu atveju, galite atidėti strategijos vertinimą ir sutaupyti laiko, jei patikrinimas atliekamas pabaigoje, pateikimo į darbo eigą metu.</span><span class="sxs-lookup"><span data-stu-id="53a33-125">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
