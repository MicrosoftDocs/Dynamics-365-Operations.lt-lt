---
title: Atsijungia „Talent“ klientas
description: Šioje temoje paaiškinama, ką daryti, jei klientas (-ė) atjungiamas (-a) nuo savo aplinkos ir nežino, kodėl.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6d174a8acac3863fb6d9f9431c6bc777cb717470
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008180"
---
# <a name="talent-client-disconnects"></a><span data-ttu-id="0a9bf-103">Atsijungia „Talent“ klientas</span><span class="sxs-lookup"><span data-stu-id="0a9bf-103">Talent client disconnects</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0a9bf-104">**Aplinkos informacija**</span><span class="sxs-lookup"><span data-stu-id="0a9bf-104">**Environment details**</span></span> 

<span data-ttu-id="0a9bf-105">Ši problema gali kilti visose aplinkose.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="0a9bf-106">**Požymis**</span><span class="sxs-lookup"><span data-stu-id="0a9bf-106">**Symptom**</span></span> 

<span data-ttu-id="0a9bf-107">Klientas (-ė) atjungiamas (-a) nuo savo aplinkos ir nežino, kodėl.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="0a9bf-108">Klientui rodomas vienas iš toliau pateiktų klaidos pranešimų.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="0a9bf-109">Nutrūko ryšys su jumis.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-109">We've lost your connection.</span></span> <span data-ttu-id="0a9bf-110">Spustelėkite Uždaryti, kad galėtumėte tęsti darbą.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-110">Click Close to continue working.</span></span>
- <span data-ttu-id="0a9bf-111">Atrodo, kad nutrūko tinklo ryšys. Spustelėkite Kartoti, jei norite bandyti dar kartą.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="0a9bf-112">**Raudona vėliavėlė**</span><span class="sxs-lookup"><span data-stu-id="0a9bf-112">**Red flag**</span></span>

<span data-ttu-id="0a9bf-113">Taip dažnai nutinka, kai vartotojai, vykdydami įdiegimo etapą, lygina informaciją gamybos bei bandomojoje aplinkose ir pamiršta, kad tarp seansų jos persijungia.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="0a9bf-114">Jei vartotojai vykdo šį etapą, jie greičiausiai susidurs su šia problema.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="0a9bf-115">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="0a9bf-115">**Issue**</span></span> 

<span data-ttu-id="0a9bf-116">**Naršyklės tipai**: „Google Chrome“, „Internet Explorer“ ir „Microsoft Edge“</span><span class="sxs-lookup"><span data-stu-id="0a9bf-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="0a9bf-117">„Microsoft Dynamics 365 Talent“ atjungia vartotojus, kai vienu metu tam pačiam vartotojui ir tam pačiam naršyklės tipui atidaromi du skirtingi seansai.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-117">Microsoft Dynamics 365 Talent disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="0a9bf-118">(Pavyzdžiui, vartotojas A peržiūri 1 ir 2 aplinkas naršyklėje „Chrome“.) Nesvarbu, ar vartotojai atidaro skirtingus naršyklės langus, ar skirtingus skirtukus.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="0a9bf-119">Naudojant to paties vartotojo kredencialus prisijungti prie 1 ir 2 aplinkų vienu metu ir tuo pačiu naršyklės tipu, „Talent“ atjungia vieną iš seansų.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Talent disconnects one of the sessions.</span></span>

<span data-ttu-id="0a9bf-120">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="0a9bf-120">**Solution**</span></span>

<span data-ttu-id="0a9bf-121">Įsitikinkite, kad naudojant nurodytą naršyklės tipą vienu metu atidaryta tik viena aplinka.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="0a9bf-122">Vartotojai gali atidaryti kelis seansus toje pačioje aplinkoje (t. y. kelis skirtukus toje pačioje naršyklėje).</span><span class="sxs-lookup"><span data-stu-id="0a9bf-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="0a9bf-123">Vartotojai, norintys vienu metu pereiti iš vienos aplinkos į kitą, kiekvieną aplinką turi atidaryti naudodami kitą naršyklės tipą.</span><span class="sxs-lookup"><span data-stu-id="0a9bf-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="0a9bf-124">(Pavyzdžiui, vartotojas A gali peržiūrėti 1 aplinką naršyklėje „Chrome“, o 2 aplinką – naršyklėje „Microsoft Edge“.)</span><span class="sxs-lookup"><span data-stu-id="0a9bf-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
