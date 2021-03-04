---
title: Įplaukų pripažinimo apžvalga
description: Šioje temoje pateikiama informacija apie įplaukų pripažinimo funkciją. Šia funkcija teikiama lanksti sistema, leidžianti nustatyti įmonei būdingas taisykles, skirtas kelių elementų užsakymų tiek įplaukų vertei, tiek įplaukų grafikui pripažinti.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: a7e37a0800ec7909f79e5a2354f59c7450995641
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995619"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="7d160-104">Įplaukų pripažinimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="7d160-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d160-105">Pramonės šakų įmonės, prekiaujančios keliais elementais, pvz., produktais, paslaugomis, abonementais ir t. t., privalo galėti išskaidyti kelių elementų užsakymus, kad įplaukos galėtų būti pripažintos pagal konkrečios įmonės ir konkrečios pramonės šakos rekomendacijų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="7d160-105">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

> [!NOTE]
> <span data-ttu-id="7d160-106">Įplaukų pripažinimo funkcija negali būti įjungta naudojant funkcijų valdymą.</span><span class="sxs-lookup"><span data-stu-id="7d160-106">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="7d160-107">Dabar norėdami ją įjungti, turite naudoti konfigūracijos raktus.</span><span class="sxs-lookup"><span data-stu-id="7d160-107">Currently, you must use configuration keys to turn it on.</span></span>

> <span data-ttu-id="7d160-108">Įplaukų atpažinimas, įskaitant grupavimo funkcijas, nepalaikomas „Commerce“ kanaluose (el. prekyba, EKA, skambučių centras).</span><span class="sxs-lookup"><span data-stu-id="7d160-108">Revenue recognition, including bundle functionality, isn't supported for use in Commerce channels (e-commerce, POS, call center).</span></span> <span data-ttu-id="7d160-109">Prekės, sukonfigūruotos atpažinti įplaukas, neturėtų būti įtraukiamos į „Commerce“ kanaluose sukurtus užsakymus ar operacijas.</span><span class="sxs-lookup"><span data-stu-id="7d160-109">Items configured with revenue recognition should not be added to orders or transactions created in Commerce channels.</span></span>

<span data-ttu-id="7d160-110">Paprastai įplaukų pripažinimo procesas gali būti naudojamas šioms užduotims atlikti:</span><span class="sxs-lookup"><span data-stu-id="7d160-110">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="7d160-111">Įplaukoms paskirstyti, siekiant padėti užtikrinti, kad tinkama įplaukų vertė būtų pripažinta remiantis kelių elementų užsakymų komponentų verte.</span><span class="sxs-lookup"><span data-stu-id="7d160-111">Allocate revenue, to help ensure that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="7d160-112">Įplaukoms atidėti pagal įplaukų grafiką, nurodantį sutartinius laikotarpius ir procentus, skirtus įplaukoms per tam tikrą laikotarpį pripažinti.</span><span class="sxs-lookup"><span data-stu-id="7d160-112">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="7d160-113">[Įplaukų pripažinimo funkcijos naudojimo „Dynamics 365 Finance“](https://youtu.be/v3amIsiqvoo) vaizdo įrašas (pateiktas pirmiau) yra įtrauktas į [„Finance and Operations“ grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), kurį galima rasti „YouTube“.</span><span class="sxs-lookup"><span data-stu-id="7d160-113">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="7d160-114">Įplaukų pripažinimo funkcija teikiama lanksti sistema, leidžianti nustatyti įmonei būdingas taisykles, skirtas tiek įplaukų vertei, tiek įplaukų grafikui pripažinti.</span><span class="sxs-lookup"><span data-stu-id="7d160-114">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="7d160-115">Patvirtinti produktai naudojami įplaukų pripažinimui pardavimo užsakymų dokumentuose palaikyti.</span><span class="sxs-lookup"><span data-stu-id="7d160-115">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="7d160-116">Išleisti produktai apima sąranką, kurios reikia įplaukų vertei ir įplaukų grafikui apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="7d160-116">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="7d160-117">Pardavimo užsakymas gali būti sukurtas iš laiko ir medžiagų projekto.</span><span class="sxs-lookup"><span data-stu-id="7d160-117">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="7d160-118">Įmonės gali naudoti įplaukų grafiko funkcijas nenaudodamos įplaukų vertės funkcijos.</span><span class="sxs-lookup"><span data-stu-id="7d160-118">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="7d160-119">Todėl pardavimo užsakymo eilutėse nurodyta kaina bus naudojama arba kaip įplaukos, arba kaip atidėtos įplaukos.</span><span class="sxs-lookup"><span data-stu-id="7d160-119">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="7d160-120">Jei pardavimo užsakymo eilutėje nurodytas įplaukų grafikas, pardavimo užsakymo eilutėje nurodyta kaina bus atidėta.</span><span class="sxs-lookup"><span data-stu-id="7d160-120">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="7d160-121">Jei pardavimo užsakymo eilutėje įplaukų grafikas nenurodytas, pardavimo eilutėje nurodyta kaina įplaukų sąskaitoje bus užregistruota išrašius sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="7d160-121">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="7d160-122">Įplaukų vertė apskaičiuojama patvirtinus pardavimo užsakymą arba užregistravus sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="7d160-122">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="7d160-123">Norėdami peržiūrėti įplaukų vertę prieš tai, kai sąskaita faktūra yra užregistruojama, turite patvirtinti pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="7d160-123">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="7d160-124">Patvirtinus pardavimo užsakymą, taip pat sukuriamas numatomas įplaukų grafikas, jei bet kurioje pardavimo užsakymo eilutėje nurodytas įplaukų grafikas.</span><span class="sxs-lookup"><span data-stu-id="7d160-124">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="7d160-125">Išrašius pardavimo užsakymo sąskaitą faktūrą, numatomas įplaukų grafikas panaikinamas ir numatomas įplaukų grafikas keičiamas faktiniu įplaukų pripažinimo grafiku.</span><span class="sxs-lookup"><span data-stu-id="7d160-125">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="7d160-126">Išlaikoma kiekvienos pardavimo užsakymo eilutės išsami įplaukų pripažinimo grafiko informacija.</span><span class="sxs-lookup"><span data-stu-id="7d160-126">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="7d160-127">Todėl pajamų pripažinimo vadybininkas gali peržiūrėti išsamią informaciją ir išleisti eilutes į įplaukas, kai yra įvykdytas sutartinis įsipareigojimas.</span><span class="sxs-lookup"><span data-stu-id="7d160-127">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="7d160-128">Kiekvieno laikotarpio pabaigoje pajamų pripažinimo vadybininkas gali sukurti įplaukų žurnalą ir išleisti bet kokias grafiko eilutes, kurias reikia įvykdyti vadybininko nustatytą datą arba prieš ją.</span><span class="sxs-lookup"><span data-stu-id="7d160-128">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="7d160-129">Šis įplaukų žurnalas nėra užregistruojamas iš karto.</span><span class="sxs-lookup"><span data-stu-id="7d160-129">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="7d160-130">Todėl pajamų pripažinimo vadybininkas gali patikrinti, ar tinkamos sumos išleidžiamos iš atidėtų įplaukų į faktines įplaukas.</span><span class="sxs-lookup"><span data-stu-id="7d160-130">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="7d160-131">Jeigu dėl sutarties pakeitimų nauja pardavimo užsakymo eilutė įtraukiama arba į esamą pardavimo užsakymą, arba į naują pardavimo užsakymą, gali būti vykdomas perskirstymo procesas siekiant ištaisyti visų pardavimo užsakymų eilučių įplaukų vertę.</span><span class="sxs-lookup"><span data-stu-id="7d160-131">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
