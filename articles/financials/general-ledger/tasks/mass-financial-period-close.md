--- 
title: "Masinis finansinio laikotarpio uždarymas"
description: "Šioje procedūroje parodoma, kaip sulaikyti laikotarpį arba visam laikui uždaryti laikotarpį ar daugiau nei vieną juridinį subjektą tuo pat metu."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8d7151cbcd02f9312ca6b0de5e27231a0b0dc9d6
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="mass-financial-period-close"></a><span data-ttu-id="00f20-103">Masinis finansinio laikotarpio uždarymas</span><span class="sxs-lookup"><span data-stu-id="00f20-103">Mass financial period close</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00f20-104">Šioje procedūroje parodoma, kaip sulaikyti laikotarpį arba visam laikui uždaryti laikotarpį ar daugiau nei vieną juridinį subjektą tuo pat metu.</span><span class="sxs-lookup"><span data-stu-id="00f20-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="00f20-105">Be to, užduotyje parodoma, kaip apriboti vartotojų grupę registruoti naudojant konkrečius modulius.</span><span class="sxs-lookup"><span data-stu-id="00f20-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="00f20-106">Pasirinkite DK > Laikotarpio uždarymas > DK kalendoriai.</span><span class="sxs-lookup"><span data-stu-id="00f20-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="00f20-107">Atminkite, kad rodomų juridinių subjektų sąrašas priklauso nuo puslapyje pasirinkto finansinio kalendoriaus.</span><span class="sxs-lookup"><span data-stu-id="00f20-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="00f20-108">Bus rodomi tik tie juridiniai subjektai, kurie naudoja pasirinktą finansinį kalendorių.</span><span class="sxs-lookup"><span data-stu-id="00f20-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="00f20-109">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="00f20-109">Click Edit.</span></span>
3. <span data-ttu-id="00f20-110">Pasirinkite laikotarpį, kurio būseną norite keisti.</span><span class="sxs-lookup"><span data-stu-id="00f20-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="00f20-111">Pasirinkite juridinius subjektus, kurių būseną norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="00f20-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="00f20-112">Galite greitai pasirinkti visus juridinius subjektus, pažymėdami žymės langelį, esantį tinklelio viršuje, kairėje pusėje.</span><span class="sxs-lookup"><span data-stu-id="00f20-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="00f20-113">Pasirinkite Naujinti modulio prieigą, norėdami nustatyti registravimo prieigą prie pasirinkto modulio.</span><span class="sxs-lookup"><span data-stu-id="00f20-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="00f20-114">Kiekviena modulio būsena taip pat gali būti atnaujinta, redaguojant įrašus tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="00f20-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="00f20-115">Mygtukas yra naudingas, kai norite greitai atnaujinti kelis juridinio subjekto įrašus.</span><span class="sxs-lookup"><span data-stu-id="00f20-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="00f20-116">Lauke Programos modulis pasirinkite modulį, kurio būseną norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="00f20-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="00f20-117">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="00f20-117">Click Select.</span></span>
7. <span data-ttu-id="00f20-118">Lauke Prieigos lygis pasirinkite Visi, Nė vienas arba konkrečią vartotojų grupę.</span><span class="sxs-lookup"><span data-stu-id="00f20-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="00f20-119">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="00f20-119">Click Select.</span></span>
    * <span data-ttu-id="00f20-120">Visi reiškia, kad visi vartotojai, turintys prieigą redaguoti modulį, gali užregistruoti, jei laikotarpis atidarytas.</span><span class="sxs-lookup"><span data-stu-id="00f20-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="00f20-121">Niekas reiškia, kad nė vienas vartotojas negali registruoti į modulį, jei laikotarpis atidarytas.</span><span class="sxs-lookup"><span data-stu-id="00f20-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="00f20-122">Konkreti vartotojų grupė reiškia, kad į modulį registruoti gali tik grupės vartotojai, jei laikotarpis atidarytas.</span><span class="sxs-lookup"><span data-stu-id="00f20-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="00f20-123">Spustelėkite Naujinti.</span><span class="sxs-lookup"><span data-stu-id="00f20-123">Click Update.</span></span>
9. <span data-ttu-id="00f20-124">Pasirinkite kitą laikotarpį, kurio būseną naujinsite.</span><span class="sxs-lookup"><span data-stu-id="00f20-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="00f20-125">Pasirinkite juridinius subjektus, kurių laikotarpio būseną norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="00f20-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="00f20-126">Pasirinkite Naujinti laikotarpio būseną ir nustatykite būseną Sulaikyta, Atidaryta arba Uždaryta visam laikui.</span><span class="sxs-lookup"><span data-stu-id="00f20-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="00f20-127">Atidaryta reiškia, kad į laikotarpį galima registruoti, jei vartotojas turi prieigą.</span><span class="sxs-lookup"><span data-stu-id="00f20-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="00f20-128">Būsena Sulaikyta nurodo, kad laikotarpyje negalima registruoti, bet jį galima iš naujo atidaryti.</span><span class="sxs-lookup"><span data-stu-id="00f20-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="00f20-129">Būsena Uždaryta visam laikui nurodo, kad laikotarpis yra uždarytas ir nebebus galima jo atidaryti.</span><span class="sxs-lookup"><span data-stu-id="00f20-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="00f20-130">Koregavimų registruoti negalima.</span><span class="sxs-lookup"><span data-stu-id="00f20-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="00f20-131">Nerekomenduojama nustatyti laikotarpio būsenos Uždaryta visam laikui, kol nėra pabaigti visi koregavimai ir auditai.</span><span class="sxs-lookup"><span data-stu-id="00f20-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="00f20-132">Spustelėkite Naujinti.</span><span class="sxs-lookup"><span data-stu-id="00f20-132">Click Update.</span></span>


