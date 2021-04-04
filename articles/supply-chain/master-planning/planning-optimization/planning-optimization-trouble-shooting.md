---
title: „Planning Optimization“ trikčių diagnostika
description: Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti dirbant su „Planning Optimization“.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 39583c244f09f54551d560e8b1dd9f1a5a1590cc
ms.sourcegitcommit: 72f70c81176e86cda714a4712525f73514c895b7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/16/2021
ms.locfileid: "5457334"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="f49b9-103">„Planning Optimization“ trikčių diagnostika</span><span class="sxs-lookup"><span data-stu-id="f49b9-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f49b9-104">Šioje temoje aprašoma, kaip spręsti bendrąsias problemas, kurios gali kilti dirbant su „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="f49b9-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="f49b9-105">„Planning Optimization“ papildinio diegimas nebaigtas</span><span class="sxs-lookup"><span data-stu-id="f49b9-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="f49b9-106">Norint naudoti „Planning Optimization“, reikalinga įgalinta „Lifecycle Services“ (LCS), plačiai pasiekiama 2 ar aukštesnės pakopos aplinka (ne „OneBox” aplinka), turinti „Dynamics 365 Supply Chain Management” 10.0.7 arba naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="f49b9-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="f49b9-107">Jei papildinį bandysite įdiegti „OneBox“ aplinkoje, diegimas nebus baigtas.</span><span class="sxs-lookup"><span data-stu-id="f49b9-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="f49b9-108">**Pataisymas**: atšaukite diegimą ir naudokite plačiai pasiekiamą 2 ar aukštesnės pakopos aplinką (ne „OneBox“ aplinką).</span><span class="sxs-lookup"><span data-stu-id="f49b9-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="f49b9-109">Kai „Planning Optimization“ įgalintas, nepavyksta suplanuoti paketinių užduočių</span><span class="sxs-lookup"><span data-stu-id="f49b9-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="f49b9-110">Kai įgalinate „Planning Optimization“, integruotas bendrojo planavimo mechanizmas yra automatiškai išjungiamas.</span><span class="sxs-lookup"><span data-stu-id="f49b9-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="f49b9-111">Bendrojo planavimo paketinių užduočių, kurios buvo sukurtos integruotam „Supply Chain Management“ planavimo mechanizmui, atlikti nepavyks, jei jos suaktyvinamos, kai „Planning Optimization“ yra įgalintas.</span><span class="sxs-lookup"><span data-stu-id="f49b9-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="f49b9-112">Galite gauti klaidos pranešimą, pvz., *Ši operacija suaktyvino bendrąjį planavimą, kuris nepalaikomas, kai įgalintas „Planning Optimization“*.</span><span class="sxs-lookup"><span data-stu-id="f49b9-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="f49b9-113">**Pataisymas**: atšaukti visas bendrojo planavimo paketines užduotis, kurios buvo sukurtos integruotam „Supply Chain Management“ planavimo mechanizmui.</span><span class="sxs-lookup"><span data-stu-id="f49b9-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="f49b9-114">„Planning Optimization“ rezultatai skiriasi nuo ankstesnių rezultatų</span><span class="sxs-lookup"><span data-stu-id="f49b9-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="f49b9-115">„Planning Optimization“ tam tikrose srityse skiriasi nuo integruoto bendrojo planavimo dizaino.</span><span class="sxs-lookup"><span data-stu-id="f49b9-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="f49b9-116">Tai gali lemti ir laukimo funkcijos.</span><span class="sxs-lookup"><span data-stu-id="f49b9-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="f49b9-117">**Pataisymas**: vykdyti „Planning Optimization“ tinkamumo analizę, tada analizuoti rezultatus nurodant susijusius dokumentus, kad būtų galima suprasti poveikį.</span><span class="sxs-lookup"><span data-stu-id="f49b9-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="f49b9-118">Daugiau informacijos žr. [„Planning Optimization“ tinkamumo analizė](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f49b9-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="f49b9-119">Nepavyksta įgalinti „Planning Optimization“</span><span class="sxs-lookup"><span data-stu-id="f49b9-119">Can't enable Planning Optimization</span></span>

<span data-ttu-id="f49b9-120">Jei parinkties **Naudoti „Planning Optimization“** reikšmę norite nustatytai kaip **Taip**, **Ryšio būsena** reikšmė turi būti **Prijungta**.</span><span class="sxs-lookup"><span data-stu-id="f49b9-120">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="f49b9-121">Daugiau informacijos žr. [Darbo su „Planning Optimization“ pradžia](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="f49b9-121">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="f49b9-122">**Pataisa**: įsitikinkite, kad papildinys „Planning Optimization“ buvo įdiegtas sėkmingai.</span><span class="sxs-lookup"><span data-stu-id="f49b9-122">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="f49b9-123">Klaidos pranešimas rodomas CTP metu</span><span class="sxs-lookup"><span data-stu-id="f49b9-123">Error message is shown during CTP</span></span>

<span data-ttu-id="f49b9-124">Jei galimas pateikti atsargas (CTP) bandysite vykdyti iš pardavimo užsakymo esant įgalintam „Planning Optimization“, gausite tokį klaidos pranešimą: *Ši operacija suaktyvino bendrąjį planavimą, kuris nepalaikomas, kai įgalintas „Planning Optimization“*.</span><span class="sxs-lookup"><span data-stu-id="f49b9-124">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="f49b9-125">Tai susiję su laukimo funkcija, kuri yra suplanuota kaip gamybos užsakymų palaikymo dalis.</span><span class="sxs-lookup"><span data-stu-id="f49b9-125">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="f49b9-126">**Pataisa:** venkite CTP skaičiavimų, kai įgalintas „Planning Optimization“, kol bus galima naudoti CTP palaikymą.</span><span class="sxs-lookup"><span data-stu-id="f49b9-126">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f49b9-127">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f49b9-127">Additional resources</span></span>

[<span data-ttu-id="f49b9-128">Darbo su planavimo optimizavimu pradžia</span><span class="sxs-lookup"><span data-stu-id="f49b9-128">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="f49b9-129">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="f49b9-129">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]