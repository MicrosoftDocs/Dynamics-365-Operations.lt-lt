---
title: Pakoreguotos prognozės įgaliojimas
description: Ne visus prognozės duomenis reikia įgalioti iš karto. Šiame straipsnyje paaiškinama, kaip galite nurodyti laikotarpį, kurį prognozė yra įgaliojama. Taip pat jame paaiškinama, kaip galima leisti prognozę naudoti konkrečioms įmonėms ir prognozės modeliams.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de7384e94a4b97cf515bb437ad546a8a5f96aa77
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815231"
---
# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="aa312-105">Pakoreguotos prognozės įgaliojimas</span><span class="sxs-lookup"><span data-stu-id="aa312-105">Authorize an adjusted forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa312-106">Ne visus prognozės duomenis reikia įgalioti iš karto.</span><span class="sxs-lookup"><span data-stu-id="aa312-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="aa312-107">Šiame straipsnyje paaiškinama, kaip galite nurodyti laikotarpį, kurį prognozė yra įgaliojama.</span><span class="sxs-lookup"><span data-stu-id="aa312-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="aa312-108">Taip pat jame paaiškinama, kaip galima leisti prognozę naudoti konkrečioms įmonėms ir prognozės modeliams.</span><span class="sxs-lookup"><span data-stu-id="aa312-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="aa312-109">Ne visus prognozės duomenis reikia įgalioti iš karto.</span><span class="sxs-lookup"><span data-stu-id="aa312-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="aa312-110">Galite nurodyti laikotarpio, kurį prognozė turi būti įgaliota, pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="aa312-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="aa312-111">Ši funkcija suteikia galimybę blokuoti konkrečius rinkinius.</span><span class="sxs-lookup"><span data-stu-id="aa312-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="aa312-112">Nurodomos pradžios ir pabaigos datos turi atitikti rinkinio, kuriame prognozė generuojama, pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="aa312-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="aa312-113">Sistema taiko šį apribojimą ir automatiškai koreguoja datas, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="aa312-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="aa312-114">Puslapio **Autorizavimas** skirtuke **Informacija** galite peržiūrėti informaciją apie vėliausiai sugeneruotą prognozę.</span><span class="sxs-lookup"><span data-stu-id="aa312-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="aa312-115">Galite pasirinkti, kurioms įmonėms ir kuriems prognozės modeliams leisti prognozę naudoti.</span><span class="sxs-lookup"><span data-stu-id="aa312-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="aa312-116">Pagal numatytuosius parametrus tinklelyje yra įtrauktos visos įmonės, kurioms poreikio prognozė buvo sukurta.</span><span class="sxs-lookup"><span data-stu-id="aa312-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="aa312-117">Įvedamas kiekvienos įmonės prognozės modelis, kuris atitinka bendrojo planavimo parametruose nustatytą dabartinį prognozės planą.</span><span class="sxs-lookup"><span data-stu-id="aa312-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="aa312-118">Tačiau šį prognozės modelį galite pakeisti į bet kurį kitą šiai įmonei priklausantį prognozės modelį.</span><span class="sxs-lookup"><span data-stu-id="aa312-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="aa312-119">Jei nesugeneruota jokių pasirinktos įmonės poreikio prognozės duomenų, importavimo metu gausite perspėjimo pranešimą.</span><span class="sxs-lookup"><span data-stu-id="aa312-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="aa312-120">Labai svarbu suprasti, kokia yra žymės langelio **Įrašyti atliktus pagrindinės poreikio prognozės neautomatinius koregavimus** paskirtis.</span><span class="sxs-lookup"><span data-stu-id="aa312-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="aa312-121">Jei atlikote neautomatinių pagrindinės statistinės prognozės koregavimų, patikslintas reikšmes leidžiama naudoti, net jei šis žymės langelis išvalytas.</span><span class="sxs-lookup"><span data-stu-id="aa312-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="aa312-122">Tačiau po autorizavimo pakeitimai yra panaikinami.</span><span class="sxs-lookup"><span data-stu-id="aa312-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="aa312-123">Todėl kitą kartą generuojant prognozę ji bus tik statistinė prognozė ir neturės jokių neautomatinių perrašymų, net jei pasirinkta parinktis **Perkelti neautomatinius koregavimus į poreikio prognozę**.</span><span class="sxs-lookup"><span data-stu-id="aa312-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="aa312-124">Todėl žymės langelį **Įrašyti atliktus pagrindinės poreikio prognozės neautomatinius koregavimus** galima laikyti mechanizmu, kurį naudojant galima išsaugoti arba panaikinti visus neautomatinius pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="aa312-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="additional-resources"></a><span data-ttu-id="aa312-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="aa312-125">Additional resources</span></span>
--------

[<span data-ttu-id="aa312-126">Neautomatiniai pagrindinės prognozės koregavimai</span><span class="sxs-lookup"><span data-stu-id="aa312-126">Make manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="aa312-127">Prognozės tikslumo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="aa312-127">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)



