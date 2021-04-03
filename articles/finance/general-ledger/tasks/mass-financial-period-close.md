---
title: Masinis finansinio laikotarpio uždarymas
description: Šioje temoje aptariama, kaip nustatyti laikotarpį vykdyti fone arba vienu metu visiškai panaikinti laikotarpį arba daugiau nei vieną juridinį asmenį.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4db0f68a22f9129041c7a7c081f397c34c2b07eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254444"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="9c0e5-103">Masinis finansinio laikotarpio uždarymas</span><span class="sxs-lookup"><span data-stu-id="9c0e5-103">Mass financial period close</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9c0e5-104">Šioje temoje aptariama, kaip nustatyti laikotarpį vykdyti fone arba vienu metu visiškai panaikinti laikotarpį arba daugiau nei vieną juridinį asmenį.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-104">This topic shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="9c0e5-105">Be to, užduotyje parodoma, kaip apriboti vartotojų grupę registruoti naudojant konkrečius modulius.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="9c0e5-106">Naršymo srityje eikite į **Moduliai > Didžioji knyga > Laikotarpio naikinimas > DK kalendoriai**.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-106">In the navigation pane, go to **Modules > General ledger > Period close > Ledger calendars**.</span></span> <span data-ttu-id="9c0e5-107">Atminkite, kad rodomų juridinių subjektų sąrašas priklauso nuo puslapyje pasirinkto finansinio kalendoriaus.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="9c0e5-108">Bus rodomi tik tie juridiniai subjektai, kurie naudoja pasirinktą finansinį kalendorių.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-108">Only legal entities using the selected fiscal calendar will display.</span></span>
2. <span data-ttu-id="9c0e5-109">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-109">Select **Edit**.</span></span>
3. <span data-ttu-id="9c0e5-110">Pasirinkite laikotarpį, kurio būseną norite keisti.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="9c0e5-111">Pasirinkite juridinius subjektus, kurių būseną norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-111">Select the legal entities for which you want to update the status.</span></span> <span data-ttu-id="9c0e5-112">Galite greitai pasirinkti visus juridinius asmenis užžymėję varnelę tinklelio viršutinėje kairėje pusėje.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-112">You can quickly select all legal entities by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="9c0e5-113">Pažymėkite **Naujinti modulio prieigą**, kad nurodytumėte registravimo prieigą pasirinktam moduliui.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-113">Select **Update module access** to define the posting access to a selected module.</span></span> <span data-ttu-id="9c0e5-114">Kiekviena modulio būsena taip pat gali būti atnaujinta, redaguojant įrašus tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="9c0e5-115">Mygtukas yra naudingas, kai norite greitai atnaujinti kelis juridinio subjekto įrašus.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="9c0e5-116">Modulyje **Taikymas** pasirinkite modulį, kuriam norite naujinti būseną.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-116">In the **Application** module, select the module that you want to update the status.</span></span> <span data-ttu-id="9c0e5-117">Spustelėkite **Pažymėti**.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-117">Click **Select**.</span></span>
7. <span data-ttu-id="9c0e5-118">Lygyje **Prieiga** pasirinkite **Visa**, **Nė vienas** arba konkrečią vartotojų grupę.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-118">In the **Access** level, select **All**, **None**, or a specific user group.</span></span> <span data-ttu-id="9c0e5-119">Spustelėkite **Pažymėti**.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-119">Click **Select**.</span></span> <span data-ttu-id="9c0e5-120">Visi reiškia, kad visi vartotojai, turintys prieigą redaguoti modulį, gali užregistruoti, jei laikotarpis atidarytas.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="9c0e5-121">Niekas reiškia, kad nė vienas vartotojas negali registruoti į modulį, jei laikotarpis atidarytas.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="9c0e5-122">Konkreti vartotojų grupė reiškia, kad į modulį registruoti gali tik grupės vartotojai, jei laikotarpis atidarytas.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="9c0e5-123">Pasirinkite **Naujinti**.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-123">Select **Update**.</span></span>
9. <span data-ttu-id="9c0e5-124">Pasirinkite kitą laikotarpį, kurio būseną naujinsite.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="9c0e5-125">Pasirinkite juridinius subjektus, kurių laikotarpio būseną norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="9c0e5-126">Pasirinkite **Naujinti laikotarpio būseną** ir nustatykite būseną į **Atidėtas**, **Atviras** arba **Panaikintas visam laikui**.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-126">Select **Update period status** and set the status of **On hold**, **Open**, or **Permanently closed**.</span></span> <span data-ttu-id="9c0e5-127">**Atviras** nurodo, kad laikotarpį galima registruoti, jei naudotojas turi prie jo prieigą.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-127">**Open** indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="9c0e5-128">**Atidėtas** reiškia, jog laikotarpį negalima registruoti, tačiau laikotarpį galima vėl atverti.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-128">**On hold** means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="9c0e5-129">**Panaikintas visam laikui** reiškia, jog laikotarpis yra panaikintas ir negali būti atvertas.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-129">**Permanently closed** means the period is closed and can never be opened.</span></span> <span data-ttu-id="9c0e5-130">Koregavimų registruoti negalima.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="9c0e5-131">Nėra rekomenduotina nustatyti laikotarpį į **Panaikintas visam laikui**, kol visos korekcijos ir patikrinimai nėra baigti.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-131">We do not recommend setting a period to **Permanently closed** until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="9c0e5-132">Pasirinkite **Naujinti**.</span><span class="sxs-lookup"><span data-stu-id="9c0e5-132">Select **Update**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]