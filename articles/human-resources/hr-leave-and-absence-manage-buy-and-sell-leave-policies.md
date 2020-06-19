---
title: Atostogų pirkimo ir pardavimo strategijų valdymas
description: Galite suteikti darbuotojams galimybę pirkti ir parduoti atostogas programoje „Dynamics 365 Human Resources“.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429018"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="7159c-103">Atostogų pirkimo ir pardavimo strategijų valdymas</span><span class="sxs-lookup"><span data-stu-id="7159c-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="7159c-104">Galite suteikti darbuotojams galimybę pirkti atostogas, kurdami pirkimo atostogų strategiją.</span><span class="sxs-lookup"><span data-stu-id="7159c-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="7159c-105">Suteikite darbuotojams galimybę pirkti ir parduoti atostogas</span><span class="sxs-lookup"><span data-stu-id="7159c-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="7159c-106">Puslapyje **Atostogų parametrai** pasirinkite **Taip**, jei norite **Leisti darbuotojams pirkti atostogas**.</span><span class="sxs-lookup"><span data-stu-id="7159c-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="7159c-107">Atostogų pirkimo strategijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="7159c-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="7159c-108">Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="7159c-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="7159c-109">Pasirinkite **Atostogų pirkimo ir pardavimo strategija**.</span><span class="sxs-lookup"><span data-stu-id="7159c-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="7159c-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7159c-110">Select **New**.</span></span>

4. <span data-ttu-id="7159c-111">Įveskite strategijos **Pavadinimą** ir **Aprašą** dalyje **Atostogų pirkimo ir pardavimo strategija**.</span><span class="sxs-lookup"><span data-stu-id="7159c-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="7159c-112">Pasirinkite **Strategijos tipas**.</span><span class="sxs-lookup"><span data-stu-id="7159c-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="7159c-113">Galimi strategijos tipai yra **Kiekis** ir **Valandos per savaitę**.</span><span class="sxs-lookup"><span data-stu-id="7159c-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="7159c-114">Pasirinkite **Kiekis**, kad įvestumėte **Fiksuotą kiekį** maksimaliam kiekiui, kurį gali pirkti ir parduoti darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="7159c-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="7159c-115">Jei pasirinksite **Valandos per savaitę**, darbo laikas, nurodytas darbuotojo priskirtame darbo laiko kalendoriuje, naudojamas nustatyti maksimaliam strategijos kiekiui.</span><span class="sxs-lookup"><span data-stu-id="7159c-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="7159c-116">Pasirinkite strategijos **Pradžios datą** ir **Pabaigos datą**.</span><span class="sxs-lookup"><span data-stu-id="7159c-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="7159c-117">Atostogų pirkimo ir pardavimo prašymus bus galima pateikti tik šiuo laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="7159c-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="7159c-118">Dalyje **Pirkimo strategija** pasirinkite **Visos darbo dienos ekvivalentiškumas** (FTE), norėdami proporcingai paskirstyti maksimalų kiekį pagal FTE, apibrėžtą darbuotojo pareigose.</span><span class="sxs-lookup"><span data-stu-id="7159c-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="7159c-119">Jei strategijos tipas yra **Kiekis**, įveskite **Maksimalus fiksuotas kiekis**.</span><span class="sxs-lookup"><span data-stu-id="7159c-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="7159c-120">Pasirinkite **Įtraukti**, kad įtrauktumėte darbuotojų atostogų tipus, kad būtų galima pirkti atostogas.</span><span class="sxs-lookup"><span data-stu-id="7159c-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="7159c-121">Prie strategijos galite pridėti keletą atostogų tipų.</span><span class="sxs-lookup"><span data-stu-id="7159c-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="7159c-122">Norėdami nustatyti maksimalų kiekį, kurį gali įsigyti darbuotojas, įveskite **Darbo mėnesiai**, kad būtų įjungti skirtingi paslaugų mėnesiai.</span><span class="sxs-lookup"><span data-stu-id="7159c-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="7159c-123">Įveskite atostogų tipo **Maksimalų kiekį**.</span><span class="sxs-lookup"><span data-stu-id="7159c-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="7159c-124">Įveskite **Įkainį**, kuriuo darbuotojas įsigys atostogų.</span><span class="sxs-lookup"><span data-stu-id="7159c-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="7159c-125">Pasirinktinai įveskite **Uždarbio kodą,** kuris bus naudojamas perkant atostogas.</span><span class="sxs-lookup"><span data-stu-id="7159c-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="7159c-126">Pasirinktinai nustatykite, ar naudoti FTE, kad būtų galima nustatyti maksimalų atostogų tipo kiekį.</span><span class="sxs-lookup"><span data-stu-id="7159c-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="7159c-127">Atostogų pirkimo ir pardavimo strategijos įtraukimas į atostogų planą</span><span class="sxs-lookup"><span data-stu-id="7159c-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="7159c-128">Puslapyje **Atostogos** pasirinkite atostogų planą.</span><span class="sxs-lookup"><span data-stu-id="7159c-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="7159c-129">Dalyje **Taisyklės** pasirinkite **Atostogų pirkimo ir pardavimo strategija**.</span><span class="sxs-lookup"><span data-stu-id="7159c-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="7159c-130">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="7159c-130">See also</span></span>

[<span data-ttu-id="7159c-131">Atostogų ir neatvykimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="7159c-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="7159c-132">Atostogų ir neatvykimų tipų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7159c-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="7159c-133">Sukauptų atostogų ir neatvykimų planai</span><span class="sxs-lookup"><span data-stu-id="7159c-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="7159c-134">Atostogų pirkimas ir pardavimas</span><span class="sxs-lookup"><span data-stu-id="7159c-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

