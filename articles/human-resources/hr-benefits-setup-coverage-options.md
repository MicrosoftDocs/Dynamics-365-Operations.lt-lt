---
title: Padengimo parinkčių kūrimas
description: ''
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
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009884"
---
# <a name="create-coverage-options"></a><span data-ttu-id="cdec3-102">Padengimo parinkčių kūrimas</span><span class="sxs-lookup"><span data-stu-id="cdec3-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="cdec3-103">„Microsoft Dynamics 365 Human Resources“ padengimo parinktys yra padengimo lygiai, skirti išmokų plano ar programos dalyviams išrinkti, pvz., medicinos planas, skirtas tik darbuotojams, arba gyvybes draudimo planas, skirtas gaunantiems 2 x atlyginimus.</span><span class="sxs-lookup"><span data-stu-id="cdec3-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="cdec3-104">Apibrėžus išmokų padengimo parinktis, galima jas naudoti pakartotinai, taip pat galite susieti parinktį su vienu ar daugiau planų.</span><span class="sxs-lookup"><span data-stu-id="cdec3-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="cdec3-105">Apibrėžę padengimo parinktis, susiekite padengimo parinktis su išmokų plano tipu.</span><span class="sxs-lookup"><span data-stu-id="cdec3-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="cdec3-106">Tada plano tipas susiejamas su išmokų planu ar programa.</span><span class="sxs-lookup"><span data-stu-id="cdec3-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="cdec3-107">Su plano tipu susietas parinktis bus galima taikyti visiems planams, sukurtiems, naudojant šį plano tipą.</span><span class="sxs-lookup"><span data-stu-id="cdec3-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="cdec3-108">Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Padengimo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="cdec3-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="cdec3-109">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="cdec3-109">Select **New**.</span></span>

3. <span data-ttu-id="cdec3-110">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="cdec3-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="cdec3-111">Laukas</span><span class="sxs-lookup"><span data-stu-id="cdec3-111">Field</span></span> | <span data-ttu-id="cdec3-112">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="cdec3-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="cdec3-113">**Padengimo parinktis**</span><span class="sxs-lookup"><span data-stu-id="cdec3-113">**Coverage option**</span></span> | <span data-ttu-id="cdec3-114">Unikalus padengimo parinkties pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="cdec3-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="cdec3-115">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="cdec3-115">**Description**</span></span> | <span data-ttu-id="cdec3-116">Padengimo parinkties aprašas.</span><span class="sxs-lookup"><span data-stu-id="cdec3-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="cdec3-117">**Padengimo kodas**</span><span class="sxs-lookup"><span data-stu-id="cdec3-117">**Coverage code**</span></span> | <span data-ttu-id="cdec3-118">Pagal padengimo kodus kiekvienam reikalavimus atitinkančiam dengiamam asmens tipui priskiriama mažiausia ir didžiausia suma.</span><span class="sxs-lookup"><span data-stu-id="cdec3-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="cdec3-119">Padengimo kodas nurodo, kas yra dengiamas, arba plano tipui leidžiamą padengimo sumą.</span><span class="sxs-lookup"><span data-stu-id="cdec3-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="cdec3-120">Padengimo suma galima išreikšti doleriais arba procentais.</span><span class="sxs-lookup"><span data-stu-id="cdec3-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="cdec3-121">Pavyzdys:</span><span class="sxs-lookup"><span data-stu-id="cdec3-121">For example:</span></span></br></br><span data-ttu-id="cdec3-122">- **„Emp+1“** – kad būtų tinkamas, darbuotojas turi būti pasirinkęs vieną priklausomąjį (jei pasirinkta daugiau nei vienas, darbuotojas nebetinka).</span><span class="sxs-lookup"><span data-stu-id="cdec3-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="cdec3-123">- **„Emp+family“** – kad būtų tinkamas, darbuotojas turi būti pasirinkęs bent du priklausomuosius.</span><span class="sxs-lookup"><span data-stu-id="cdec3-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="cdec3-124">**Didžiausias skaičius**</span><span class="sxs-lookup"><span data-stu-id="cdec3-124">**Maximum number**</span></span> | <span data-ttu-id="cdec3-125">Didžiausias priklausomųjų skaičius.</span><span class="sxs-lookup"><span data-stu-id="cdec3-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="cdec3-126">**Būsena**</span><span class="sxs-lookup"><span data-stu-id="cdec3-126">**Status**</span></span> | <span data-ttu-id="cdec3-127">Padengimo parinkties būsena.</span><span class="sxs-lookup"><span data-stu-id="cdec3-127">The status of the coverage option.</span></span> <span data-ttu-id="cdec3-128">Jei padengimo parinkties būsena nustatyta kaip neaktyvi, plano tipų padengimo parinkčių pasirinkti negalima.</span><span class="sxs-lookup"><span data-stu-id="cdec3-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="cdec3-129">**Procentas**</span><span class="sxs-lookup"><span data-stu-id="cdec3-129">**Percent**</span></span> | <span data-ttu-id="cdec3-130">Procentinė suma.</span><span class="sxs-lookup"><span data-stu-id="cdec3-130">The percent amount.</span></span> <span data-ttu-id="cdec3-131">Šis laukas yra aktyvus tik tada, kai padengimo kodo lauke buvo pasirinkta % x atlyginimas.</span><span class="sxs-lookup"><span data-stu-id="cdec3-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="cdec3-132">**Daliklis**</span><span class="sxs-lookup"><span data-stu-id="cdec3-132">**Divisor**</span></span> | <span data-ttu-id="cdec3-133">Skaičiuojant naudojamas daliklis, kai pasirenkamas padengimo kodas % x atlyginimas.</span><span class="sxs-lookup"><span data-stu-id="cdec3-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="cdec3-134">**Mažiausias procentas**</span><span class="sxs-lookup"><span data-stu-id="cdec3-134">**Percent minimum**</span></span> | <span data-ttu-id="cdec3-135">Mažiausias procentinis dydis, kai pasirenkamas padengimo kodas procentais.</span><span class="sxs-lookup"><span data-stu-id="cdec3-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="cdec3-136">**Didžiausias procentas**</span><span class="sxs-lookup"><span data-stu-id="cdec3-136">**Percent maximum**</span></span> | <span data-ttu-id="cdec3-137">Didžiausias procentinis dydis, kai pasirenkamas padengimo kodas procentais.</span><span class="sxs-lookup"><span data-stu-id="cdec3-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="cdec3-138">Dalyje **Asmeninio kontakto tinkamumo parinktys**pridėkite tinkamą asmeninių kontaktų tinkamumo parinktį, skirtą kiekvienai padengimo parinkčiai.</span><span class="sxs-lookup"><span data-stu-id="cdec3-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="cdec3-139">Dalyje **Savitarna** nurodykite šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="cdec3-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="cdec3-140">Laukas</span><span class="sxs-lookup"><span data-stu-id="cdec3-140">Field</span></span> | <span data-ttu-id="cdec3-141">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="cdec3-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="cdec3-142">**Leisti darbuotojo įnašo sumą**</span><span class="sxs-lookup"><span data-stu-id="cdec3-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="cdec3-143">Nurodo, ar leisti darbuotojams keisti įnašo sumą išmokų savitarnoje, kai jie renkasi išmokas.</span><span class="sxs-lookup"><span data-stu-id="cdec3-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="cdec3-144">Jei pažymėsite šį žymės langelį, sistema apskaičiuos išmokų plano parametrus pagal įnašo sumą, kurią darbuotojas įveda išmokų savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="cdec3-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="cdec3-145">**Leisti darbuotojo padengimo sumą**</span><span class="sxs-lookup"><span data-stu-id="cdec3-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="cdec3-146">Nurodo, ar leisti darbuotojams keisti padengimo sumą išmokų savitarnoje, kai jie renkasi išmokas.</span><span class="sxs-lookup"><span data-stu-id="cdec3-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="cdec3-147">Jei pažymėsite šį žymės langelį, sistema apskaičiuos išmokų plano parametrus pagal padengimo sumą, kurią darbuotojas įveda darbuotojų savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="cdec3-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="cdec3-148">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="cdec3-148">Select **Save**.</span></span> 
