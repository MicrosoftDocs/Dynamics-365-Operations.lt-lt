---
title: Apibrėžti finansines dimensijas
description: Šiame užduoties vadove rodoma, kaip įtraukti objekto remiamą finansinę dimensiją ir pasirinktinę finansinę dimensiją.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20a7781486c6e0612c27af02a1bccbc48c55a932
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "353798"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="6baa7-103">Apibrėžti finansines dimensijas</span><span class="sxs-lookup"><span data-stu-id="6baa7-103">Define financial dimensions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6baa7-104">Šiame užduoties vadove rodoma, kaip įtraukti objekto remiamą finansinę dimensiją ir pasirinktinę finansinę dimensiją.</span><span class="sxs-lookup"><span data-stu-id="6baa7-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="6baa7-105">Šiame vadove naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="6baa7-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="6baa7-106">Objekto remiamos finansinės dimensijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="6baa7-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="6baa7-107">Eikite į Didžioji knyga > Sąskaitų planas > Dimensijos > Finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="6baa7-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="6baa7-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6baa7-108">Click New.</span></span>
3. <span data-ttu-id="6baa7-109">Lauke Vartotojo vertės nuo pasirinkite sistemos nurodytą objektą, kurio pagrindu bus sukurta finansinė dimensija.</span><span class="sxs-lookup"><span data-stu-id="6baa7-109">In the User values from field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="6baa7-110">Lauke Dimensijos pavadinimas įveskite finansinę dimensiją aprašančią vertę.</span><span class="sxs-lookup"><span data-stu-id="6baa7-110">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="6baa7-111">Pavadinimas gali skirtis nuo sistemos nurodyto objekto, tačiau jame negali būti tarpų arba specialiųjų simbolių.</span><span class="sxs-lookup"><span data-stu-id="6baa7-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>  
5. <span data-ttu-id="6baa7-112">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="6baa7-112">Click Activate.</span></span>
    * <span data-ttu-id="6baa7-113">Suaktyvinus finansinę dimensiją lentelė atnaujinama ir joje pateikiamas finansinės dimensijos pavadinimas, o panaikintos dimensijos pašalinamos.</span><span class="sxs-lookup"><span data-stu-id="6baa7-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="6baa7-114">Dimensijų reikšmes galima įvesti prieš suaktyvinant finansinę dimensiją, bet finansinės dimensijos negalima naudoti, kol ji yra suaktyvinta.</span><span class="sxs-lookup"><span data-stu-id="6baa7-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="6baa7-115">Aktyvinimo pranešime spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="6baa7-115">Click Close on the activation message.</span></span>
7. <span data-ttu-id="6baa7-116">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="6baa7-116">Click Activate.</span></span>
    * <span data-ttu-id="6baa7-117">Dimensijos aktyvinimą galima suplanuoti atlikti pakete, nurodant konkrečią dieną ir laiką.</span><span class="sxs-lookup"><span data-stu-id="6baa7-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="6baa7-118">Spustelėkite Dimensijos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="6baa7-118">Click Dimension values.</span></span>
    * <span data-ttu-id="6baa7-119">Kai kurios dimensijų reikšmės siejamos su konkrečia įmone.</span><span class="sxs-lookup"><span data-stu-id="6baa7-119">Some dimension values are company specific.</span></span> <span data-ttu-id="6baa7-120">Tai, ar jos siejamos su konkrečia įmone, sužinosite patikrinę, ar dimensijos reikšmių sąraše nurodomas įmonės pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="6baa7-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="6baa7-121">Pasirinktinės finansinės dimensijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="6baa7-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="6baa7-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6baa7-122">Close the page.</span></span>
2. <span data-ttu-id="6baa7-123">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6baa7-123">Click New.</span></span>
3. <span data-ttu-id="6baa7-124">Lauke Naudoti vertes iš pasirinkite <Custom dimension>.</span><span class="sxs-lookup"><span data-stu-id="6baa7-124">In the Use values from field, select <Custom dimension>.</span></span>
4. <span data-ttu-id="6baa7-125">Lauke Dimensijos pavadinimas įveskite finansinę dimensiją aprašančią vertę.</span><span class="sxs-lookup"><span data-stu-id="6baa7-125">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="6baa7-126">Pavadinime negali būti tarpų arba specialiųjų simbolių.</span><span class="sxs-lookup"><span data-stu-id="6baa7-126">The name cannot contain spaces or special characters.</span></span>  
    * <span data-ttu-id="6baa7-127">Taip pat galite nurodyti sąskaitos šabloną, ribojantį informacijos, kurią galite įvesti kaip dimensijos reikšmes, kiekį ir tipą.</span><span class="sxs-lookup"><span data-stu-id="6baa7-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    * <span data-ttu-id="6baa7-128">Galite įvesti simbolius, kurie išlieka vienodi visose dimensijos reikšmėse, pvz., raides arba brūkšnelį.</span><span class="sxs-lookup"><span data-stu-id="6baa7-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="6baa7-129">Taip pat galite įvesti skaičiaus ženklus (#) ir ampersandus (&) kaip vietos rezervavimo ženklus vietoj raidžių ir skaitmenų, kurie bus skirtingi kaskart sukūrus dimensijos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6baa7-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="6baa7-130">Naudokite skaičiaus ženklą (#) kaip skaitmens vietos rezervavimo ženklą, o ampersandą (&) kaip raidės vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="6baa7-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="6baa7-131">Pavyzdys: Norėdami apriboti dimensijos reikšmę iki raidžių CC ir trijų skaitmenų, kaip formato šabloną įveskite CC-###.</span><span class="sxs-lookup"><span data-stu-id="6baa7-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="6baa7-132">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="6baa7-132">Click Activate.</span></span>
    * <span data-ttu-id="6baa7-133">Suaktyvinus finansinę dimensiją lentelė atnaujinama ir joje pateikiamas finansinės dimensijos pavadinimas, o panaikintos dimensijos pašalinamos.</span><span class="sxs-lookup"><span data-stu-id="6baa7-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="6baa7-134">Dimensijų reikšmes galima įvesti prieš suaktyvinant finansinę dimensiją, bet finansinės dimensijos negalima naudoti, kol ji yra suaktyvinta.</span><span class="sxs-lookup"><span data-stu-id="6baa7-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="6baa7-135">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="6baa7-135">Click Activate.</span></span>
    * <span data-ttu-id="6baa7-136">Dimensijos aktyvinimą galima suplanuoti atlikti pakete, nurodant konkrečią dieną ir laiką.</span><span class="sxs-lookup"><span data-stu-id="6baa7-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
7. <span data-ttu-id="6baa7-137">Spustelėkite Dimensijos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="6baa7-137">Click Dimension values.</span></span>
8. <span data-ttu-id="6baa7-138">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6baa7-138">Click New.</span></span>
9. <span data-ttu-id="6baa7-139">Lauke Dimensijos reikšmė įveskite jūsų finansinės dimensijos reikšmę aprašantį pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="6baa7-139">In the Dimension value field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="6baa7-140">Lauke Aprašas įveskite aprašymą, kuris apibūdina jūsų finansinės dimensijos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6baa7-140">In the Description field, type a description that describes your financial dimension value.</span></span>

