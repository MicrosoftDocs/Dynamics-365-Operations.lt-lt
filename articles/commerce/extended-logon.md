---
title: MPOS ir „Cloud POS“ išplėstinės registracijos funkcijos nustatymas
description: Šioje temoje aprašomos „Cloud POS“ ir „Retail Modern POS“ (MPOS) išplėstinio prisijungimo nustatymo parinktys.
author: rubencdelgado
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f9d8889581e2e11fa5261805c866a6014df57611
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027581"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a><span data-ttu-id="19513-103">MPOS ir „Cloud POS“ išplėstinės registracijos funkcijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="19513-103">Set up extended logon functionality for MPOS and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="19513-104">Šioje temoje aprašomos „Cloud POS“ ir „Retail Modern POS“ (MPOS) išplėstinio prisijungimo nustatymo parinktys.</span><span class="sxs-lookup"><span data-stu-id="19513-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

## <a name="setting-up-extended-logon"></a><span data-ttu-id="19513-105">Išplėstinės registracijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="19513-105">Setting up extended logon</span></span>

<span data-ttu-id="19513-106">Brūkšninių kodų skaičių sekų sąranką galite rasti pasirinkdami **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA šablonai** &gt; **Funkcijų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="19513-106">You can find the setup for bar code masks at **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="19513-107">„FastTab“ **Funkcijos** pateikiamos toliau nurodytos parinktys, susijusios su išplėstine registracija.</span><span class="sxs-lookup"><span data-stu-id="19513-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="19513-108">Darbuotojo brūkšninio kodo registravimas</span><span class="sxs-lookup"><span data-stu-id="19513-108">Staff bar code logon</span></span>

<span data-ttu-id="19513-109">Kai parinktis **Darbuotojo brūkšninio kodo registravimas** įjungta, darbuotojai, kurių elektroninio kasos aparato (EKA) kredencialams priskirta išplėstinės registracijos funkcija, gali prisijungti naudodami brūkšninį kodą.</span><span class="sxs-lookup"><span data-stu-id="19513-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="19513-110">Darbuotojui registruojantis naudojant brūkšninį kodą reikia slaptažodžio</span><span class="sxs-lookup"><span data-stu-id="19513-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="19513-111">Kai parinktis **Darbuotojui registruojantis naudojant brūkšninį kodą reikia slaptažodžio** įjungta, darbuotojų brūkšninio kodo registracijos funkcija parenka tik tą darbuotoją, kuris yra priskirtas pateiktai išplėstinei registracijai.</span><span class="sxs-lookup"><span data-stu-id="19513-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="19513-112">Kai ši parinktis įjungta, darbuotojai vis tiek turi įvesti savo slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="19513-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="19513-113">Darbuotojo kortelės registravimas</span><span class="sxs-lookup"><span data-stu-id="19513-113">Staff card logon</span></span>

<span data-ttu-id="19513-114">Kai parinktis **Darbuotojo kortelės registravimas** įjungta, darbuotojai, kurių EKA kredencialams priskirta išplėstinės registracijos funkcija, gali prisijungti naudodami magnetinę juostelę.</span><span class="sxs-lookup"><span data-stu-id="19513-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="19513-115">Darbuotojui registruojantis naudojant kortelę reikia slaptažodžio</span><span class="sxs-lookup"><span data-stu-id="19513-115">Staff card logon requires password</span></span>

<span data-ttu-id="19513-116">Kai parinktis **Darbuotojui registruojantis naudojant kortelę reikia slaptažodžio** įjungta, darbuotojų kortelės registracijos funkcija parenka tik tą darbuotoją, kuris yra priskirtas pateiktai išplėstinei registracijai.</span><span class="sxs-lookup"><span data-stu-id="19513-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="19513-117">Kai ši parinktis įjungta, darbuotojai vis tiek turi įvesti savo slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="19513-117">Workers must still enter their password when this option is enabled.</span></span>

## <a name="assigning-an-extended-logon"></a><span data-ttu-id="19513-118">Išplėstinės registracijos priskyrimas</span><span class="sxs-lookup"><span data-stu-id="19513-118">Assigning an extended logon</span></span>

<span data-ttu-id="19513-119">Pagal numatytuosius parametrus tik vadovai gali darbuotojams priskirti išplėstinės registracijos funkciją.</span><span class="sxs-lookup"><span data-stu-id="19513-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="19513-120">Norėdami priskirti išplėstinės registracijos funkciją, EKA pasirinkite **Išplėstinė registracija**.</span><span class="sxs-lookup"><span data-stu-id="19513-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="19513-121">Tada ieškokite darbuotojo, ieškos lauke įvesdami darbuotojo operatoriaus ID.</span><span class="sxs-lookup"><span data-stu-id="19513-121">Then search for a worker by entering the worker's operator ID in the search field.</span></span> <span data-ttu-id="19513-122">Pasirinkite darbuotoją ir spustelėkite **Priskirti**.</span><span class="sxs-lookup"><span data-stu-id="19513-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="19513-123">Kitame puslapyje perbraukite arba nuskaitykite išplėstinę registraciją, kad priskirtumėte darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="19513-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="19513-124">Jei perbraukimas arba nuskaitymas sėkmingas, mygtukas **Gerai** tampa aktyvus.</span><span class="sxs-lookup"><span data-stu-id="19513-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="19513-125">Spustelėkite **Gerai**, norėdami įrašyti to darbuotojo išplėstinę registraciją.</span><span class="sxs-lookup"><span data-stu-id="19513-125">Click **OK** to save the extended logon for that worker.</span></span>

## <a name="deleting-an-extended-logon"></a><span data-ttu-id="19513-126">Išplėstinės registracijos naikinimas</span><span class="sxs-lookup"><span data-stu-id="19513-126">Deleting an extended logon</span></span>

<span data-ttu-id="19513-127">Norėdami panaikinti darbuotojui priskirtą išplėstinę registraciją, ieškokite darbuotojo naudodami operaciją **Išplėstinė registracija**.</span><span class="sxs-lookup"><span data-stu-id="19513-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="19513-128">Pasirinkite darbuotoją ir spustelėkite **Atšaukti priskyrimą**.</span><span class="sxs-lookup"><span data-stu-id="19513-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="19513-129">Pašalinami visi su tuo darbuotoju susieti išplėstinės registracijos kredencialai.</span><span class="sxs-lookup"><span data-stu-id="19513-129">All extended logon credentials that are associated with that worker are removed.</span></span>

## <a name="extending-extended-logon"></a><span data-ttu-id="19513-130">Išplėstinės registracijos išplėtimas</span><span class="sxs-lookup"><span data-stu-id="19513-130">Extending extended logon</span></span>

<span data-ttu-id="19513-131">Registravimosi paslaugą galima išplėsti, kad būtų palaikomi papildomi išplėstinės registracijos įrenginiai, pvz., delnų skaitytuvai.</span><span class="sxs-lookup"><span data-stu-id="19513-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="19513-132">Daugiau informacijos ieškokite EKA išplečiamumo dokumentuose.</span><span class="sxs-lookup"><span data-stu-id="19513-132">For more information, see the POS extensibility documentation.</span></span>

## <a name="using-extended-logon"></a><span data-ttu-id="19513-133">Išplėstinės registracijos naudojimas</span><span class="sxs-lookup"><span data-stu-id="19513-133">Using extended logon</span></span>

<span data-ttu-id="19513-134">Jei išplėstinė registracija yra sukonfigūruota, o darbuotojui buvo priskirtas brūkšninis kodas arba magnetinė juostelė, darbuotojas tiesiog turi perbraukti arba nuskaityti savo kortelę, kai rodomas EKA registracijos puslapis.</span><span class="sxs-lookup"><span data-stu-id="19513-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan the worker's card while the POS logon page is displayed.</span></span> <span data-ttu-id="19513-135">Jei prieš tęsiant registraciją būtina įvesti slaptažodį, darbuotojas bus paragintas įvesti savo slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="19513-135">If a password is also required before logon can proceed, the worker is prompted to enter the worker's password.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]