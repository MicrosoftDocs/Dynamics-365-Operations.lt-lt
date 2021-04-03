---
title: Klientas atsijungia
description: Šiame straipsnyje paaiškinama, ką daryti, jei klientas (-ė) atjungiamas (-a) nuo savo aplinkos ir nežino, kodėl.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6808132e182ea6fed4fb0605fd07c008d208e89f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468184"
---
# <a name="client-disconnects"></a><span data-ttu-id="39078-103">Klientas atsijungia</span><span class="sxs-lookup"><span data-stu-id="39078-103">Client disconnects</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="39078-104">**Aplinkos informacija**</span><span class="sxs-lookup"><span data-stu-id="39078-104">**Environment details**</span></span> 

<span data-ttu-id="39078-105">Ši problema gali kilti visose aplinkose.</span><span class="sxs-lookup"><span data-stu-id="39078-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="39078-106">**Požymis**</span><span class="sxs-lookup"><span data-stu-id="39078-106">**Symptom**</span></span> 

<span data-ttu-id="39078-107">Klientas (-ė) atjungiamas (-a) nuo savo aplinkos ir nežino, kodėl.</span><span class="sxs-lookup"><span data-stu-id="39078-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="39078-108">Klientui rodomas vienas iš toliau pateiktų klaidos pranešimų.</span><span class="sxs-lookup"><span data-stu-id="39078-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="39078-109">Nutrūko ryšys su jumis.</span><span class="sxs-lookup"><span data-stu-id="39078-109">We've lost your connection.</span></span> <span data-ttu-id="39078-110">Spustelėkite Uždaryti, kad galėtumėte tęsti darbą.</span><span class="sxs-lookup"><span data-stu-id="39078-110">Click Close to continue working.</span></span>
- <span data-ttu-id="39078-111">Atrodo, kad nutrūko tinklo ryšys. Spustelėkite Kartoti, jei norite bandyti dar kartą.</span><span class="sxs-lookup"><span data-stu-id="39078-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="39078-112">**Raudona vėliavėlė**</span><span class="sxs-lookup"><span data-stu-id="39078-112">**Red flag**</span></span>

<span data-ttu-id="39078-113">Taip dažnai nutinka, kai vartotojai, vykdydami įdiegimo etapą, lygina informaciją gamybos bei bandomojoje aplinkose ir pamiršta, kad tarp seansų jos persijungia.</span><span class="sxs-lookup"><span data-stu-id="39078-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="39078-114">Jei vartotojai vykdo šį etapą, jie greičiausiai susidurs su šia problema.</span><span class="sxs-lookup"><span data-stu-id="39078-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="39078-115">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="39078-115">**Issue**</span></span> 

<span data-ttu-id="39078-116">**Naršyklės tipai**: „Google Chrome“, „Internet Explorer“ ir „Microsoft Edge“</span><span class="sxs-lookup"><span data-stu-id="39078-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="39078-117">„Microsoft Dynamics 365 Human Resources“ atjungia vartotojus, kai vienu metu tam pačiam vartotojui ir tam pačiam naršyklės tipui atidaromi du skirtingi seansai.</span><span class="sxs-lookup"><span data-stu-id="39078-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="39078-118">(Pavyzdžiui, vartotojas A peržiūri 1 ir 2 aplinkas naršyklėje „Chrome“.) Nesvarbu, ar vartotojai atidaro skirtingus naršyklės langus, ar skirtingus skirtukus.</span><span class="sxs-lookup"><span data-stu-id="39078-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="39078-119">Naudojant to paties vartotojo kredencialus prisijungti prie 1 ir 2 aplinkų vienu metu ir tuo pačiu naršyklės tipu, „Human Resources“ atjungia vieną iš seansų.</span><span class="sxs-lookup"><span data-stu-id="39078-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="39078-120">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="39078-120">**Solution**</span></span>

<span data-ttu-id="39078-121">Įsitikinkite, kad naudojant nurodytą naršyklės tipą vienu metu atidaryta tik viena aplinka.</span><span class="sxs-lookup"><span data-stu-id="39078-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="39078-122">Vartotojai gali atidaryti kelis seansus toje pačioje aplinkoje (t. y. kelis skirtukus toje pačioje naršyklėje).</span><span class="sxs-lookup"><span data-stu-id="39078-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="39078-123">Vartotojai, norintys vienu metu pereiti iš vienos aplinkos į kitą, kiekvieną aplinką turi atidaryti naudodami kitą naršyklės tipą.</span><span class="sxs-lookup"><span data-stu-id="39078-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="39078-124">(Pavyzdžiui, vartotojas A gali peržiūrėti 1 aplinką naršyklėje „Chrome“, o 2 aplinką – naršyklėje „Microsoft Edge“.)</span><span class="sxs-lookup"><span data-stu-id="39078-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]