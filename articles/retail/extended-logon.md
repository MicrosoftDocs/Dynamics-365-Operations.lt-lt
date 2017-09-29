---
title: "„Cloud POS“ ir MPOS išplėstinės registracijos funkcijos nustatymas"
description: "Šioje temoje aprašomos „Cloud POS“ ir „Retail Modern POS“ (MPOS) išplėstinio prisijungimo nustatymo parinktys."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e29aea4509dd323c295b02f289fbcfa46fab3392
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a><span data-ttu-id="e904d-103">„Cloud POS“ ir MPOS išplėstinės registracijos funkcijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="e904d-103">Set up extended logon functionality for Cloud POS and MPOS</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="e904d-104">Šioje temoje aprašomos „Cloud POS“ ir „Retail Modern POS“ (MPOS) išplėstinio prisijungimo nustatymo parinktys.</span><span class="sxs-lookup"><span data-stu-id="e904d-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

<a name="setting-up-extended-logon"></a><span data-ttu-id="e904d-105">Išplėstinės registracijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="e904d-105">Setting up extended logon</span></span>
=========================

<span data-ttu-id="e904d-106">Brūkšninių kodų skaičių sekų sąranką galite rasti pasirinkdami **Mažmeninė prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA šablonai** &gt; **Funkcijų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="e904d-106">You can find the setup for bar code masks at **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="e904d-107">„FastTab“ **Funkcijos** pateikiamos toliau nurodytos parinktys, susijusios su išplėstine registracija.</span><span class="sxs-lookup"><span data-stu-id="e904d-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="e904d-108">Darbuotojo brūkšninio kodo registravimas</span><span class="sxs-lookup"><span data-stu-id="e904d-108">Staff bar code logon</span></span>

<span data-ttu-id="e904d-109">Kai parinktis **Darbuotojo brūkšninio kodo registravimas** įjungta, darbuotojai, kurių elektroninio kasos aparato (EKA) kredencialams priskirta išplėstinės registracijos funkcija, gali prisijungti naudodami brūkšninį kodą.</span><span class="sxs-lookup"><span data-stu-id="e904d-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="e904d-110">Darbuotojui registruojantis naudojant brūkšninį kodą reikia slaptažodžio</span><span class="sxs-lookup"><span data-stu-id="e904d-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="e904d-111">Kai parinktis **Darbuotojui registruojantis naudojant brūkšninį kodą reikia slaptažodžio** įjungta, darbuotojų brūkšninio kodo registracijos funkcija parenka tik tą darbuotoją, kuris yra priskirtas pateiktai išplėstinei registracijai.</span><span class="sxs-lookup"><span data-stu-id="e904d-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="e904d-112">Kai ši parinktis įjungta, darbuotojai vis tiek turi įvesti savo slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="e904d-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="e904d-113">Darbuotojo kortelės registravimas</span><span class="sxs-lookup"><span data-stu-id="e904d-113">Staff card logon</span></span>

<span data-ttu-id="e904d-114">Kai parinktis **Darbuotojo kortelės registravimas** įjungta, darbuotojai, kurių EKA kredencialams priskirta išplėstinės registracijos funkcija, gali prisijungti naudodami magnetinę juostelę.</span><span class="sxs-lookup"><span data-stu-id="e904d-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="e904d-115">Darbuotojui registruojantis naudojant kortelę reikia slaptažodžio</span><span class="sxs-lookup"><span data-stu-id="e904d-115">Staff card logon requires password</span></span>

<span data-ttu-id="e904d-116">Kai parinktis **Darbuotojui registruojantis naudojant kortelę reikia slaptažodžio** įjungta, darbuotojų kortelės registracijos funkcija parenka tik tą darbuotoją, kuris yra priskirtas pateiktai išplėstinei registracijai.</span><span class="sxs-lookup"><span data-stu-id="e904d-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="e904d-117">Kai ši parinktis įjungta, darbuotojai vis tiek turi įvesti savo slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="e904d-117">Workers must still enter their password when this option is enabled.</span></span>

<a name="assigning-an-extended-logon"></a><span data-ttu-id="e904d-118">Išplėstinės registracijos priskyrimas</span><span class="sxs-lookup"><span data-stu-id="e904d-118">Assigning an extended logon</span></span>
===========================

<span data-ttu-id="e904d-119">Pagal numatytuosius parametrus tik vadovai gali darbuotojams priskirti išplėstinės registracijos funkciją.</span><span class="sxs-lookup"><span data-stu-id="e904d-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="e904d-120">Norėdami priskirti išplėstinės registracijos funkciją, EKA pasirinkite **Išplėstinė registracija**.</span><span class="sxs-lookup"><span data-stu-id="e904d-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="e904d-121">Tada ieškokite darbuotojo, ieškos lauke įvesdami jo operatoriaus ID.</span><span class="sxs-lookup"><span data-stu-id="e904d-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="e904d-122">Pasirinkite darbuotoją ir spustelėkite **Priskirti**.</span><span class="sxs-lookup"><span data-stu-id="e904d-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="e904d-123">Kitame puslapyje perbraukite arba nuskaitykite išplėstinę registraciją, kad priskirtumėte darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="e904d-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="e904d-124">Jei perbraukimas arba nuskaitymas sėkmingas, mygtukas **Gerai** tampa aktyvus.</span><span class="sxs-lookup"><span data-stu-id="e904d-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="e904d-125">Spustelėkite **Gerai**, norėdami įrašyti to darbuotojo išplėstinę registraciją.</span><span class="sxs-lookup"><span data-stu-id="e904d-125">Click **OK** to save the extended logon for that worker.</span></span>

<a name="deleting-an-extended-logon"></a><span data-ttu-id="e904d-126">Išplėstinės registracijos naikinimas</span><span class="sxs-lookup"><span data-stu-id="e904d-126">Deleting an extended logon</span></span>
==========================

<span data-ttu-id="e904d-127">Norėdami panaikinti darbuotojui priskirtą išplėstinę registraciją, ieškokite darbuotojo naudodami operaciją **Išplėstinė registracija**.</span><span class="sxs-lookup"><span data-stu-id="e904d-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="e904d-128">Pasirinkite darbuotoją ir spustelėkite **Atšaukti priskyrimą**.</span><span class="sxs-lookup"><span data-stu-id="e904d-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="e904d-129">Pašalinami visi su tuo darbuotoju susieti išplėstinės registracijos kredencialai.</span><span class="sxs-lookup"><span data-stu-id="e904d-129">All extended logon credentials that are associated with that worker are removed.</span></span>

<a name="extending-extended-logon"></a><span data-ttu-id="e904d-130">Išplėstinės registracijos išplėtimas</span><span class="sxs-lookup"><span data-stu-id="e904d-130">Extending extended logon</span></span>
========================

<span data-ttu-id="e904d-131">Registravimosi paslaugą galima išplėsti, kad būtų palaikomi papildomi išplėstinės registracijos įrenginiai, pvz., delnų skaitytuvai.</span><span class="sxs-lookup"><span data-stu-id="e904d-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="e904d-132">Daugiau informacijos ieškokite EKA išplečiamumo dokumentuose.</span><span class="sxs-lookup"><span data-stu-id="e904d-132">For more information, see the POS extensibility documentation.</span></span>

<a name="using-extended-logon"></a><span data-ttu-id="e904d-133">Išplėstinės registracijos naudojimas</span><span class="sxs-lookup"><span data-stu-id="e904d-133">Using extended logon</span></span>
====================

<span data-ttu-id="e904d-134">Jei išplėstinė registracija yra sukonfigūruota, o darbuotojui buvo priskirtas brūkšninis kodas arba magnetinė juostelė, darbuotojas tiesiog turi perbraukti arba nuskaityti savo kortelę, kai rodomas EKA registracijos puslapis.</span><span class="sxs-lookup"><span data-stu-id="e904d-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="e904d-135">Jei prieš tęsiant registraciją būtina įvesti slaptažodį, darbuotojas bus paragintas įvesti savo slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="e904d-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>



