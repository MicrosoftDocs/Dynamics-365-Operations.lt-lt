---
title: Pareigų atskyrimo nesuderinamumų nustatymas ir pašalinimas
description: Šioje temoje paaiškinama, kaip nustatyti ir pašalinti pareigų atskyrimo nesuderinamumus.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: daf303a6bc3115363b27a6ebf7cc1832fdb6229d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571034"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a><span data-ttu-id="e7a82-103">Pareigų atskyrimo nesuderinamumų nustatymas ir pašalinimas</span><span class="sxs-lookup"><span data-stu-id="e7a82-103">Identify and resolve conflicts in segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7a82-104">Šioje temoje paaiškinama, kaip nustatyti ir pašalinti pareigų atskyrimo nesuderinamumus.</span><span class="sxs-lookup"><span data-stu-id="e7a82-104">This topic explains how to identify and resolve conflicts in segregation of duties.</span></span> <span data-ttu-id="e7a82-105">Galite nustatyti taisykles, kad atskirtumėte pareigas, kurias turi atlikti skirtingi vartotojai.</span><span class="sxs-lookup"><span data-stu-id="e7a82-105">You can set up rules to separate duties that must be performed by different users.</span></span> <span data-ttu-id="e7a82-106">Ši koncepcija vadinama pareigų atskyrimu.</span><span class="sxs-lookup"><span data-stu-id="e7a82-106">This concept is named segregation of duties.</span></span> <span data-ttu-id="e7a82-107">Kai saugos vaidmens apibrėžimas arba vartotojo vaidmens priskyrimai pažeidžia taisykles, registruojamas neatitikimas.</span><span class="sxs-lookup"><span data-stu-id="e7a82-107">When the definition of a security role or the role assignments of a user violate the rules, the conflict is logged.</span></span> <span data-ttu-id="e7a82-108">Visus neatitikimus turi išspręsti administratorius.</span><span class="sxs-lookup"><span data-stu-id="e7a82-108">All conflicts must be resolved by the administrator.</span></span> <span data-ttu-id="e7a82-109">Norėdami identifikuoti ir išspręsti neatitikimus, atlikite šią procedūrą.</span><span class="sxs-lookup"><span data-stu-id="e7a82-109">Complete the following procedure to identify and resolve conflicts.</span></span>

<span data-ttu-id="e7a82-110">Pridėję taisyklę patikrinkite, ar visi esami vaidmenys yra suderinami.</span><span class="sxs-lookup"><span data-stu-id="e7a82-110">After a rule has been added, verify that all existing roles are compliant.</span></span> 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="e7a82-111">Patikrinkite, ar esami vaidmenys ir pareigos atitinka naujas pareigų atskyrimo taisykles</span><span class="sxs-lookup"><span data-stu-id="e7a82-111">Verify that existing roles and duties comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="e7a82-112">Eikite į **Sistemos administravimas** > **Sauga** > **Pareigų atskyrimas** > **Pareigų atskyrimo taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="e7a82-112">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
3. <span data-ttu-id="e7a82-113">Pasirinkite **Tikrinti pareigas ir vaidmenis**.</span><span class="sxs-lookup"><span data-stu-id="e7a82-113">Select **Validate duties and roles**.</span></span> <span data-ttu-id="e7a82-114">Jei esami vaidmenys pažeidžia taisykles, parodomas pranešimas, kuriame pateikiamas taisyklės pavadinimas, vaidmuo ir nesuderinamų pareigų pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="e7a82-114">If any roles violate the rules, a message is displayed that contains the name of the rule, the role, and the names of the conflicting duties.</span></span> <span data-ttu-id="e7a82-115">Nesuderinamus vaidmenis būtina redaguoti naudojant **Saugos konfigūravimas** ir jie negali turėti nesuderinamų pareigų.</span><span class="sxs-lookup"><span data-stu-id="e7a82-115">Conflicting roles must be modified using **Security configuration** and can't include conflicting duties.</span></span> <span data-ttu-id="e7a82-116">Jei nėra vaidmenų, kurie pažeistų pasirinktą taisyklę, pranešime rodoma, kad visi vaidmenys suderinami.</span><span class="sxs-lookup"><span data-stu-id="e7a82-116">If no roles violate the selected rule, a message indicates that all roles comply.</span></span>   

> [!NOTE]
> <span data-ttu-id="e7a82-117">Patvirtinimas atliekamas tik pasirinktai taisyklei.</span><span class="sxs-lookup"><span data-stu-id="e7a82-117">The validation is only performed for the selected rule.</span></span> <span data-ttu-id="e7a82-118">Svarbu patikrinti kiekvienos taisyklės atitikimą.</span><span class="sxs-lookup"><span data-stu-id="e7a82-118">It is important to validate compliance for each rule.</span></span>   

<span data-ttu-id="e7a82-119">Kuriant arba modifikuojant vaidmenį, automatiškai taikomos pareigų atskyrimo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="e7a82-119">When you create or modify a role, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="e7a82-120">Vaidmeniui negalima priskirti nesuderinamų pareigų.</span><span class="sxs-lookup"><span data-stu-id="e7a82-120">You cannot assign conflicting duties to a role.</span></span>

<span data-ttu-id="e7a82-121">Tada patikrinkite, ar visi esami vaidmenų priskyrimai yra suderinami.</span><span class="sxs-lookup"><span data-stu-id="e7a82-121">Next, verify that all existing role assignments are compliant.</span></span>

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="e7a82-122">Patikrinimas, ar vartotojo vaidmens priskyrimai atitinka naujas pareigų atskyrimo taisykles</span><span class="sxs-lookup"><span data-stu-id="e7a82-122">Verify that user role assignments comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="e7a82-123">Eikite į **Sistemos administravimas > Sauga > Pareigų atskyrimas > Tikrinti vartotojo vaidmenų priskyrimo atitikimą**.</span><span class="sxs-lookup"><span data-stu-id="e7a82-123">Go to **System administration > Security > Segregation of duties > Verify compliance of user-role assignments**.</span></span>
2. <span data-ttu-id="e7a82-124">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e7a82-124">Select **OK**.</span></span> <span data-ttu-id="e7a82-125">Pranešime rodomi tikrinimo rezultatai.</span><span class="sxs-lookup"><span data-stu-id="e7a82-125">A notification displays the results of the validation.</span></span> <span data-ttu-id="e7a82-126">Neatitikimai registruojami **Pareigų atskyrimo neišspręsti nesuderinamumai** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e7a82-126">Conflicts are logged on the **Segregation of duties unresolved conflicts** page.</span></span>   

<span data-ttu-id="e7a82-127">Priskiriant vartotojus vaidmenims, automatiškai taikomos pareigų atskyrimo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="e7a82-127">When you assign users to roles, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="e7a82-128">Jei bandysite priskirti vartotoją vaidmenims, kuriuose yra nesuderinamų pareigų, gausite klaidos pranešimą.</span><span class="sxs-lookup"><span data-stu-id="e7a82-128">If you try to assign a user to roles that contain conflicting duties, you receive an error message.</span></span> <span data-ttu-id="e7a82-129">Tada turite išspręsti nesuderinamumą leisdami arba neleisdami papildomą vaidmens priskyrimą.</span><span class="sxs-lookup"><span data-stu-id="e7a82-129">You must then resolve the conflict by denying or allowing the additional role assignment.</span></span> <span data-ttu-id="e7a82-130">Leidus priskyrimą bus priskirtas papildomas vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="e7a82-130">The additional role will be assigned after the assignment is allowed.</span></span> 

> [!NOTE]
> <span data-ttu-id="e7a82-131">Šiuo metu nėra tikrinami vartotojų, kuriems priskirti vaidmenys pagal „Active Directory” domenų grupes, nesuderinamumai.</span><span class="sxs-lookup"><span data-stu-id="e7a82-131">Conflicts are currently not verified for users that are assigned roles based on the Active Directory Domain groups.</span></span>

## <a name="view-and-resolve-conflicting-user-role-assignments"></a><span data-ttu-id="e7a82-132">Peržiūrėti ir išspręsti nesuderinamus vartotojo vaidmenų priskyrimus</span><span class="sxs-lookup"><span data-stu-id="e7a82-132">View and resolve conflicting user role assignments</span></span>
1. <span data-ttu-id="e7a82-133">Eikite į **Sistemos administravimas** > **Sauga** > **Pareigų atskyrimas** > **Neišspręsti pareigų atskyrimo nesuderinamumai**.</span><span class="sxs-lookup"><span data-stu-id="e7a82-133">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties unresolved conflicts**.</span></span> 
2. <span data-ttu-id="e7a82-134">Pasirinkite nesuderinamumą ir tada pasirinkite vieną iš tolesnių veiksmų:</span><span class="sxs-lookup"><span data-stu-id="e7a82-134">Select a conflict, and then select one of the following actions:</span></span> 

  - <span data-ttu-id="e7a82-135">**Atmesti priskyrimą**: Tai atmes papildomą saugos vaidmens priskyrimą vartotojui.</span><span class="sxs-lookup"><span data-stu-id="e7a82-135">**Deny assignment**: This will deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="e7a82-136">Jei atmesite automatinį vaidmens priskyrimą, vartotojas pažymimas kaip pašalintas iš vaidmens.</span><span class="sxs-lookup"><span data-stu-id="e7a82-136">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="e7a82-137">Pašalintam vartotojui nesuteikiama su vaidmeniu susieta prieiga ir jo negalima priskirti vaidmeniui tol, kol administratorius nepanaikins pašalinimo.</span><span class="sxs-lookup"><span data-stu-id="e7a82-137">The excluded user isn't granted the access associated with the role and can't be assigned to the role until the administrator removes the exclusion.</span></span> 
-  <span data-ttu-id="e7a82-138">**Leisti priskyrimą**: Tai nepaisys neatitikimo ir leis vartotoją priskirti papildomam saugos vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="e7a82-138">**Allow assignment**: This will override the conflict and allow the user to be assigned to the additional security role.</span></span> <span data-ttu-id="e7a82-139">Jei nepaisote neatitikimo, lauke **Nepaisymo priežastis** turite įvesti priežastį.</span><span class="sxs-lookup"><span data-stu-id="e7a82-139">If you override a conflict, you must enter a reason in the **Reason for override** field.</span></span> <span data-ttu-id="e7a82-140">Visus nepaisomus vaidmenų priskyrimus galima peržiūrėti **Pareigų atskyrimo nesuderinamumai** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e7a82-140">All overridden role assignments can be viewed on the **Segregation of duties conflicts** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="e7a82-141">Jei keli nesuderinamumai išvardyti tam pačiam vartotojui, pasirinkite vartotojo įrašą ir įvertinkite priskirtus vaidmenis **Vartotojai** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e7a82-141">If several conflicts are listed for the same user, select the user record and evaluate assigned roles on the **Users** page.</span></span> <span data-ttu-id="e7a82-142">Norėdami išvengti šio nesuderinamumo, patvirtinkite kiekvieną taisyklę ją pridėjus arba modifikavus.</span><span class="sxs-lookup"><span data-stu-id="e7a82-142">To avoid this conflict, validate each rule after it's added or modified.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]