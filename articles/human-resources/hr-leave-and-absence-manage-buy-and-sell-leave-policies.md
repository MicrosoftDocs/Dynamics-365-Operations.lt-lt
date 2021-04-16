---
title: Atostogų pirkimo ir pardavimo strategijų valdymas
description: Galite suteikti darbuotojams galimybę pirkti ir parduoti atostogas programoje „Dynamics 365 Human Resources“.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f03d6055c407b2c3e13831c8b5a6f8b0d6c47897
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794714"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="828e4-103">Atostogų pirkimo ir pardavimo strategijų valdymas</span><span class="sxs-lookup"><span data-stu-id="828e4-103">Manage buy and sell leave policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="828e4-104">Galite įgalinti darbuotojus pirkti ir parduoti atostogas, sukuriant atostogų pirkimo ir pardavimo strategiją.</span><span class="sxs-lookup"><span data-stu-id="828e4-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="828e4-105">Galite konfigūruoti šias strategijas, kad galėtumėte naudotis darbo eiga patvirtinimams, nustatyti maksimalias sumas bei tarifus, ir nustatyti pirkimo ir pardavimo tarifus. </span><span class="sxs-lookup"><span data-stu-id="828e4-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="828e4-106">Suteikite darbuotojams galimybę pirkti ir parduoti atostogas</span><span class="sxs-lookup"><span data-stu-id="828e4-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="828e4-107">**Atostogų ir neatvykimų parametrų** puslapyje, **Leisti darbuotojams pirkti atostogas** ir **Leisti darbuotojams parduoti atostogas** dalyse, pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="828e4-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="828e4-108">Sukurkite atostogų pirkimo ir pardavimo strategiją </span><span class="sxs-lookup"><span data-stu-id="828e4-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="828e4-109">Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="828e4-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="828e4-110">Pasirinkite **Atostogų pirkimo ir pardavimo strategija**.</span><span class="sxs-lookup"><span data-stu-id="828e4-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="828e4-111">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="828e4-111">Select **New**.</span></span>

4. <span data-ttu-id="828e4-112">Įveskite strategijos **Pavadinimą** ir **Aprašą** dalyje **Atostogų pirkimo ir pardavimo strategija**.</span><span class="sxs-lookup"><span data-stu-id="828e4-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="828e4-113">Pasirinkite **Strategijos tipas**.</span><span class="sxs-lookup"><span data-stu-id="828e4-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="828e4-114">Galimi strategijos tipai yra **Kiekis** ir **Valandos per savaitę**.</span><span class="sxs-lookup"><span data-stu-id="828e4-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="828e4-115">Pasirinkite **Kiekis**, kad įvestumėte **Fiksuotą kiekį** maksimaliam kiekiui, kurį gali pirkti ir parduoti darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="828e4-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="828e4-116">Jei pasirinksite **Valandos per savaitę**, darbo laikas, nurodytas darbuotojo priskirtame darbo laiko kalendoriuje, naudojamas nustatyti maksimaliam strategijos kiekiui.</span><span class="sxs-lookup"><span data-stu-id="828e4-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="828e4-117">Pasirinkite strategijos **Pradžios datą** ir **Pabaigos datą**.</span><span class="sxs-lookup"><span data-stu-id="828e4-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="828e4-118">Atostogų pirkimo ir pardavimo prašymus bus galima pateikti tik šiuo laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="828e4-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="828e4-119">Parinkite **Darbo eigos ID** strategijai.</span><span class="sxs-lookup"><span data-stu-id="828e4-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="828e4-120">Bet kurioms pirkimo ir pardavimo užklausoms bus naudojama ši darbo eiga peržiūrai ir patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="828e4-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="828e4-121">Dalyje **Pirkimo strategija** pasirinkite **Visos darbo dienos ekvivalentiškumas** (FTE), norėdami proporcingai paskirstyti maksimalų kiekį pagal FTE, apibrėžtą darbuotojo pareigose.</span><span class="sxs-lookup"><span data-stu-id="828e4-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="828e4-122">Jei strategijos tipas yra **Kiekis**, įveskite **Maksimalus fiksuotas kiekis**.</span><span class="sxs-lookup"><span data-stu-id="828e4-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="828e4-123">Pasirinkite **Įtraukti**, kad įtrauktumėte darbuotojų atostogų tipus, kad būtų galima pirkti atostogas.</span><span class="sxs-lookup"><span data-stu-id="828e4-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="828e4-124">Prie strategijos galite pridėti keletą atostogų tipų.</span><span class="sxs-lookup"><span data-stu-id="828e4-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="828e4-125">Norėdami nustatyti maksimalų kiekį, kurį gali įsigyti darbuotojas, įveskite **Darbo mėnesiai**, kad būtų įjungti skirtingi paslaugų mėnesiai.</span><span class="sxs-lookup"><span data-stu-id="828e4-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="828e4-126">Įveskite atostogų tipo **Maksimalų kiekį**.</span><span class="sxs-lookup"><span data-stu-id="828e4-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="828e4-127">Įveskite **Įkainį**, kuriuo darbuotojas įsigys atostogų.</span><span class="sxs-lookup"><span data-stu-id="828e4-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="828e4-128">Pasirinktinai įveskite **Uždarbio kodą,** kuris bus naudojamas perkant atostogas.</span><span class="sxs-lookup"><span data-stu-id="828e4-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="828e4-129">Pasirinktinai nustatykite, ar naudoti FTE, kad būtų galima nustatyti maksimalų atostogų tipo kiekį.</span><span class="sxs-lookup"><span data-stu-id="828e4-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="828e4-130">Tam, kad sukurtumėte ir parduotumėte strategiją, sekite 8–14 žingsnius, esančius po **Parduoti strategiją**.</span><span class="sxs-lookup"><span data-stu-id="828e4-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="828e4-131">Atostogų pirkimo ir pardavimo strategijos įtraukimas į atostogų planą</span><span class="sxs-lookup"><span data-stu-id="828e4-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="828e4-132">Puslapyje **Atostogos** pasirinkite atostogų planą.</span><span class="sxs-lookup"><span data-stu-id="828e4-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="828e4-133">Dalyje **Taisyklės** pasirinkite **Atostogų pirkimo ir pardavimo strategija**.</span><span class="sxs-lookup"><span data-stu-id="828e4-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="828e4-134">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="828e4-134">See also</span></span>

[<span data-ttu-id="828e4-135">Atostogų ir neatvykimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="828e4-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="828e4-136">Atostogų ir neatvykimų tipų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="828e4-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="828e4-137">Sukauptų atostogų ir neatvykimų planai</span><span class="sxs-lookup"><span data-stu-id="828e4-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="828e4-138">Atostogų pirkimas ir pardavimas</span><span class="sxs-lookup"><span data-stu-id="828e4-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]