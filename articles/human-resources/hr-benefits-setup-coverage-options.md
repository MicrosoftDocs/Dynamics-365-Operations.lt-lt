---
title: Padengimo parinkčių kūrimas
description: „Microsoft Dynamics 365 Human Resources” padengimo parinktys yra padengimo lygiai, skirti išmokų plano ar programos dalyviams išrinkti.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 021fea7604af2fff833ddc6868d55a316ef70aae
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230182"
---
# <a name="create-coverage-options"></a><span data-ttu-id="5cf98-103">Padengimo parinkčių kūrimas</span><span class="sxs-lookup"><span data-stu-id="5cf98-103">Create coverage options</span></span>

<span data-ttu-id="5cf98-104">„Microsoft Dynamics 365 Human Resources” padengimo parinktys yra padengimo lygiai, skirti išmokų plano ar programos dalyviams išrinkti.</span><span class="sxs-lookup"><span data-stu-id="5cf98-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="5cf98-105">Pvz., padengimo parinktys gali apimti medicinos planą, skirtą **tik darbuotojams**, arba gyvybės draudimo planą, skirtą gaunantiems **2 x atlyginimus**.</span><span class="sxs-lookup"><span data-stu-id="5cf98-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="5cf98-106">Apibrėžus išmokų padengimo parinktis, jas galima naudoti pakartotinai.</span><span class="sxs-lookup"><span data-stu-id="5cf98-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="5cf98-107">Galite susieti parinktį su vienu ar daugiau planų.</span><span class="sxs-lookup"><span data-stu-id="5cf98-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="5cf98-108">Apibrėžę padengimo parinktis, susiekite padengimo parinktis su išmokų plano tipu.</span><span class="sxs-lookup"><span data-stu-id="5cf98-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="5cf98-109">Tada plano tipas susiejamas su išmokų planu ar programa.</span><span class="sxs-lookup"><span data-stu-id="5cf98-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="5cf98-110">Su plano tipu susietas parinktis galima taikyti visiems planams, sukurtiems, naudojant šį plano tipą.</span><span class="sxs-lookup"><span data-stu-id="5cf98-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="5cf98-111">Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Padengimo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="5cf98-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="5cf98-112">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="5cf98-112">Select **New**.</span></span>

3. <span data-ttu-id="5cf98-113">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="5cf98-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5cf98-114">Laukas</span><span class="sxs-lookup"><span data-stu-id="5cf98-114">Field</span></span> | <span data-ttu-id="5cf98-115">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="5cf98-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5cf98-116">**Padengimo parinktis**</span><span class="sxs-lookup"><span data-stu-id="5cf98-116">**Coverage option**</span></span> | <span data-ttu-id="5cf98-117">Unikalus padengimo parinkties pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="5cf98-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="5cf98-118">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="5cf98-118">**Description**</span></span> | <span data-ttu-id="5cf98-119">Padengimo parinkties aprašas.</span><span class="sxs-lookup"><span data-stu-id="5cf98-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="5cf98-120">**Padengimo kodas**</span><span class="sxs-lookup"><span data-stu-id="5cf98-120">**Coverage code**</span></span> | <span data-ttu-id="5cf98-121">Pagal padengimo kodus kiekvienam reikalavimus atitinkančiam dengiamam asmens tipui priskiriama mažiausia ir didžiausia suma.</span><span class="sxs-lookup"><span data-stu-id="5cf98-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="5cf98-122">Padengimo kodas nurodo, kas yra dengiamas, arba plano tipui leidžiamą padengimo sumą.</span><span class="sxs-lookup"><span data-stu-id="5cf98-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="5cf98-123">Padengimo suma galima išreikšti doleriais arba procentais.</span><span class="sxs-lookup"><span data-stu-id="5cf98-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="5cf98-124">Pavyzdys:</span><span class="sxs-lookup"><span data-stu-id="5cf98-124">For example:</span></span></br></br><span data-ttu-id="5cf98-125">- **„Emp+1“** – kad būtų tinkamas, darbuotojas turi būti pasirinkęs vieną priklausomąjį (jei pasirinkta daugiau nei vienas, darbuotojas nebetinka).</span><span class="sxs-lookup"><span data-stu-id="5cf98-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="5cf98-126">- **„Emp+family“** – kad būtų tinkamas, darbuotojas turi būti pasirinkęs bent du priklausomuosius.</span><span class="sxs-lookup"><span data-stu-id="5cf98-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="5cf98-127">**Didžiausias skaičius**</span><span class="sxs-lookup"><span data-stu-id="5cf98-127">**Maximum number**</span></span> | <span data-ttu-id="5cf98-128">Didžiausias priklausomųjų skaičius.</span><span class="sxs-lookup"><span data-stu-id="5cf98-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="5cf98-129">**Būsena**</span><span class="sxs-lookup"><span data-stu-id="5cf98-129">**Status**</span></span> | <span data-ttu-id="5cf98-130">Padengimo parinkties būsena.</span><span class="sxs-lookup"><span data-stu-id="5cf98-130">The status of the coverage option.</span></span> <span data-ttu-id="5cf98-131">Jei padengimo parinkties būsena nustatyta kaip neaktyvi, plano tipų padengimo parinkčių pasirinkti negalima.</span><span class="sxs-lookup"><span data-stu-id="5cf98-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="5cf98-132">**Procentas**</span><span class="sxs-lookup"><span data-stu-id="5cf98-132">**Percent**</span></span> | <span data-ttu-id="5cf98-133">Procentinė suma.</span><span class="sxs-lookup"><span data-stu-id="5cf98-133">The percent amount.</span></span> <span data-ttu-id="5cf98-134">Šis laukas yra aktyvus tik tada, kai padengimo kodo lauke buvo pasirinkta % x atlyginimas.</span><span class="sxs-lookup"><span data-stu-id="5cf98-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="5cf98-135">**Daliklis**</span><span class="sxs-lookup"><span data-stu-id="5cf98-135">**Divisor**</span></span> | <span data-ttu-id="5cf98-136">Skaičiuojant naudojamas daliklis, kai pasirenkamas padengimo kodas % x atlyginimas.</span><span class="sxs-lookup"><span data-stu-id="5cf98-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="5cf98-137">**Mažiausias procentas**</span><span class="sxs-lookup"><span data-stu-id="5cf98-137">**Percent minimum**</span></span> | <span data-ttu-id="5cf98-138">Mažiausias procentinis dydis, kai pasirenkamas padengimo kodas procentais.</span><span class="sxs-lookup"><span data-stu-id="5cf98-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="5cf98-139">**Didžiausias procentas**</span><span class="sxs-lookup"><span data-stu-id="5cf98-139">**Percent maximum**</span></span> | <span data-ttu-id="5cf98-140">Didžiausias procentinis dydis, kai pasirenkamas padengimo kodas procentais.</span><span class="sxs-lookup"><span data-stu-id="5cf98-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="5cf98-141">Dalyje **Asmeninio kontakto tinkamumo parinktys**pridėkite tinkamą asmeninių kontaktų tinkamumo parinktį, skirtą kiekvienai padengimo parinkčiai.</span><span class="sxs-lookup"><span data-stu-id="5cf98-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="5cf98-142">Dalyje **Savitarna** nurodykite šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="5cf98-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="5cf98-143">Laukas</span><span class="sxs-lookup"><span data-stu-id="5cf98-143">Field</span></span> | <span data-ttu-id="5cf98-144">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="5cf98-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5cf98-145">**Leisti darbuotojo įnašo sumą**</span><span class="sxs-lookup"><span data-stu-id="5cf98-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="5cf98-146">Nurodo, ar leisti darbuotojams keisti įnašo sumą išmokų savitarnoje, kai jie renkasi išmokas.</span><span class="sxs-lookup"><span data-stu-id="5cf98-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="5cf98-147">Jei pažymėsite šį žymės langelį, sistema apskaičiuos išmokų plano parametrus pagal įnašo sumą, kurią darbuotojas įveda išmokų savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="5cf98-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="5cf98-148">**Leisti darbuotojo padengimo sumą**</span><span class="sxs-lookup"><span data-stu-id="5cf98-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="5cf98-149">Nurodo, ar leisti darbuotojams keisti padengimo sumą išmokų savitarnoje, kai jie renkasi išmokas.</span><span class="sxs-lookup"><span data-stu-id="5cf98-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="5cf98-150">Jei pažymėsite šį žymės langelį, sistema apskaičiuos išmokų plano parametrus pagal padengimo sumą, kurią darbuotojas įveda darbuotojų savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="5cf98-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="5cf98-151">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5cf98-151">Select **Save**.</span></span> 
