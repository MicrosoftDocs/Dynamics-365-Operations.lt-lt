---
title: Padengimo parinkčių kūrimas
description: „Microsoft Dynamics 365 Human Resources“ padengimo parinktys yra padengimo lygiai, skirti išmokų plano ar programos dalyviams išrinkti, pvz., medicinos planas, skirtas tik darbuotojams, arba gyvybes draudimo planas, skirtas gaunantiems 2 x atlyginimus.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092711"
---
# <a name="create-coverage-options"></a><span data-ttu-id="c96dd-103">Padengimo parinkčių kūrimas</span><span class="sxs-lookup"><span data-stu-id="c96dd-103">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="c96dd-104">„Microsoft Dynamics 365 Human Resources“ padengimo parinktys yra padengimo lygiai, skirti išmokų plano ar programos dalyviams išrinkti, pvz., medicinos planas, skirtas tik darbuotojams, arba gyvybes draudimo planas, skirtas gaunantiems 2 x atlyginimus.</span><span class="sxs-lookup"><span data-stu-id="c96dd-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="c96dd-105">Apibrėžus išmokų padengimo parinktis, galima jas naudoti pakartotinai, taip pat galite susieti parinktį su vienu ar daugiau planų.</span><span class="sxs-lookup"><span data-stu-id="c96dd-105">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="c96dd-106">Apibrėžę padengimo parinktis, susiekite padengimo parinktis su išmokų plano tipu.</span><span class="sxs-lookup"><span data-stu-id="c96dd-106">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="c96dd-107">Tada plano tipas susiejamas su išmokų planu ar programa.</span><span class="sxs-lookup"><span data-stu-id="c96dd-107">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="c96dd-108">Su plano tipu susietas parinktis bus galima taikyti visiems planams, sukurtiems, naudojant šį plano tipą.</span><span class="sxs-lookup"><span data-stu-id="c96dd-108">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="c96dd-109">Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Padengimo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="c96dd-109">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="c96dd-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c96dd-110">Select **New**.</span></span>

3. <span data-ttu-id="c96dd-111">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="c96dd-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c96dd-112">Laukas</span><span class="sxs-lookup"><span data-stu-id="c96dd-112">Field</span></span> | <span data-ttu-id="c96dd-113">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="c96dd-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c96dd-114">**Padengimo parinktis**</span><span class="sxs-lookup"><span data-stu-id="c96dd-114">**Coverage option**</span></span> | <span data-ttu-id="c96dd-115">Unikalus padengimo parinkties pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="c96dd-115">A unique coverage option name.</span></span> |
   | <span data-ttu-id="c96dd-116">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="c96dd-116">**Description**</span></span> | <span data-ttu-id="c96dd-117">Padengimo parinkties aprašas.</span><span class="sxs-lookup"><span data-stu-id="c96dd-117">A description of the coverage option.</span></span> |
   | <span data-ttu-id="c96dd-118">**Padengimo kodas**</span><span class="sxs-lookup"><span data-stu-id="c96dd-118">**Coverage code**</span></span> | <span data-ttu-id="c96dd-119">Pagal padengimo kodus kiekvienam reikalavimus atitinkančiam dengiamam asmens tipui priskiriama mažiausia ir didžiausia suma.</span><span class="sxs-lookup"><span data-stu-id="c96dd-119">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="c96dd-120">Padengimo kodas nurodo, kas yra dengiamas, arba plano tipui leidžiamą padengimo sumą.</span><span class="sxs-lookup"><span data-stu-id="c96dd-120">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="c96dd-121">Padengimo suma galima išreikšti doleriais arba procentais.</span><span class="sxs-lookup"><span data-stu-id="c96dd-121">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="c96dd-122">Pavyzdys:</span><span class="sxs-lookup"><span data-stu-id="c96dd-122">For example:</span></span></br></br><span data-ttu-id="c96dd-123">- **„Emp+1“** – kad būtų tinkamas, darbuotojas turi būti pasirinkęs vieną priklausomąjį (jei pasirinkta daugiau nei vienas, darbuotojas nebetinka).</span><span class="sxs-lookup"><span data-stu-id="c96dd-123">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="c96dd-124">- **„Emp+family“** – kad būtų tinkamas, darbuotojas turi būti pasirinkęs bent du priklausomuosius.</span><span class="sxs-lookup"><span data-stu-id="c96dd-124">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="c96dd-125">**Didžiausias skaičius**</span><span class="sxs-lookup"><span data-stu-id="c96dd-125">**Maximum number**</span></span> | <span data-ttu-id="c96dd-126">Didžiausias priklausomųjų skaičius.</span><span class="sxs-lookup"><span data-stu-id="c96dd-126">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="c96dd-127">**Būsena**</span><span class="sxs-lookup"><span data-stu-id="c96dd-127">**Status**</span></span> | <span data-ttu-id="c96dd-128">Padengimo parinkties būsena.</span><span class="sxs-lookup"><span data-stu-id="c96dd-128">The status of the coverage option.</span></span> <span data-ttu-id="c96dd-129">Jei padengimo parinkties būsena nustatyta kaip neaktyvi, plano tipų padengimo parinkčių pasirinkti negalima.</span><span class="sxs-lookup"><span data-stu-id="c96dd-129">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="c96dd-130">**Procentas**</span><span class="sxs-lookup"><span data-stu-id="c96dd-130">**Percent**</span></span> | <span data-ttu-id="c96dd-131">Procentinė suma.</span><span class="sxs-lookup"><span data-stu-id="c96dd-131">The percent amount.</span></span> <span data-ttu-id="c96dd-132">Šis laukas yra aktyvus tik tada, kai padengimo kodo lauke buvo pasirinkta % x atlyginimas.</span><span class="sxs-lookup"><span data-stu-id="c96dd-132">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="c96dd-133">**Daliklis**</span><span class="sxs-lookup"><span data-stu-id="c96dd-133">**Divisor**</span></span> | <span data-ttu-id="c96dd-134">Skaičiuojant naudojamas daliklis, kai pasirenkamas padengimo kodas % x atlyginimas.</span><span class="sxs-lookup"><span data-stu-id="c96dd-134">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="c96dd-135">**Mažiausias procentas**</span><span class="sxs-lookup"><span data-stu-id="c96dd-135">**Percent minimum**</span></span> | <span data-ttu-id="c96dd-136">Mažiausias procentinis dydis, kai pasirenkamas padengimo kodas procentais.</span><span class="sxs-lookup"><span data-stu-id="c96dd-136">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="c96dd-137">**Didžiausias procentas**</span><span class="sxs-lookup"><span data-stu-id="c96dd-137">**Percent maximum**</span></span> | <span data-ttu-id="c96dd-138">Didžiausias procentinis dydis, kai pasirenkamas padengimo kodas procentais.</span><span class="sxs-lookup"><span data-stu-id="c96dd-138">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="c96dd-139">Dalyje **Asmeninio kontakto tinkamumo parinktys**pridėkite tinkamą asmeninių kontaktų tinkamumo parinktį, skirtą kiekvienai padengimo parinkčiai.</span><span class="sxs-lookup"><span data-stu-id="c96dd-139">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="c96dd-140">Dalyje **Savitarna** nurodykite šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="c96dd-140">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="c96dd-141">Laukas</span><span class="sxs-lookup"><span data-stu-id="c96dd-141">Field</span></span> | <span data-ttu-id="c96dd-142">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="c96dd-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c96dd-143">**Leisti darbuotojo įnašo sumą**</span><span class="sxs-lookup"><span data-stu-id="c96dd-143">**Allow employee contribution amount**</span></span> | <span data-ttu-id="c96dd-144">Nurodo, ar leisti darbuotojams keisti įnašo sumą išmokų savitarnoje, kai jie renkasi išmokas.</span><span class="sxs-lookup"><span data-stu-id="c96dd-144">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="c96dd-145">Jei pažymėsite šį žymės langelį, sistema apskaičiuos išmokų plano parametrus pagal įnašo sumą, kurią darbuotojas įveda išmokų savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="c96dd-145">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="c96dd-146">**Leisti darbuotojo padengimo sumą**</span><span class="sxs-lookup"><span data-stu-id="c96dd-146">**Allow employee coverage amount**</span></span> | <span data-ttu-id="c96dd-147">Nurodo, ar leisti darbuotojams keisti padengimo sumą išmokų savitarnoje, kai jie renkasi išmokas.</span><span class="sxs-lookup"><span data-stu-id="c96dd-147">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="c96dd-148">Jei pažymėsite šį žymės langelį, sistema apskaičiuos išmokų plano parametrus pagal padengimo sumą, kurią darbuotojas įveda darbuotojų savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="c96dd-148">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="c96dd-149">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c96dd-149">Select **Save**.</span></span> 
