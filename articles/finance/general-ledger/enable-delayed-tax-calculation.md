---
title: Atidėto mokesčių skaičiavimo įjungimas žurnaluose
description: Šioje temoje paaiškinama, kaip įjungti atidėto mokesčių skaičiavimo funkciją siekiant pagerinti mokesčių skaičiavimo efektyvumą, kai yra labai daug žurnalo eilučių.
author: ericwang
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: acf5ead6ed90d4dbb41de08520cde8085a7f3935
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823721"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="69735-103">Atidėto mokesčių skaičiavimo įjungimas žurnaluose</span><span class="sxs-lookup"><span data-stu-id="69735-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="69735-104">Šioje temoje paaiškinama, kaip galima atidėti PVM skaičiavimą žurnaluose.</span><span class="sxs-lookup"><span data-stu-id="69735-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="69735-105">Ši galimybė padeda pagerinti mokesčių skaičiavimo efektyvumą, kai yra daug žurnalo eilučių.</span><span class="sxs-lookup"><span data-stu-id="69735-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="69735-106">Esant numatytiesiems nustatymams, žurnalo eilučių PVM sumos apskaičiuojamos, kai atnaujinami su mokesčiais susiję laukai.</span><span class="sxs-lookup"><span data-stu-id="69735-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="69735-107">Šie laukai apima PVM grupių ir prekės PVM grupių laukus.</span><span class="sxs-lookup"><span data-stu-id="69735-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="69735-108">Atnaujinus bet kurią žurnalo eilutę, perskaičiuojamos visos žurnalo eilutės.</span><span class="sxs-lookup"><span data-stu-id="69735-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="69735-109">Nors toks veikimas leidžia vartotojui matyti realiu laiku apskaičiuojamas mokesčių sumas, tai taip pat gali turėti įtakos našumui, jei žurnalo eilučių skaičius yra labai didelis.</span><span class="sxs-lookup"><span data-stu-id="69735-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="69735-110">Atidėto mokesčių skaičiavimo funkcija leidžia atidėti mokesčių skaičiavimą žurnaluose, todėl padeda spręsti našumo problemas.</span><span class="sxs-lookup"><span data-stu-id="69735-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="69735-111">Kai ši funkcija įjungta, mokesčių sumos bus apskaičiuotos tik tada, kai vartotojas pasirinks **PVM** arba užregistruos žurnalą.</span><span class="sxs-lookup"><span data-stu-id="69735-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="69735-112">Galite atidėti PVM skaičiavimą trijuose lygiuose:</span><span class="sxs-lookup"><span data-stu-id="69735-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="69735-113">Juridinis subjektas</span><span class="sxs-lookup"><span data-stu-id="69735-113">Legal entity</span></span>
- <span data-ttu-id="69735-114">Žurnalo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="69735-114">Journal name</span></span>
- <span data-ttu-id="69735-115">Žurnalo antraštė</span><span class="sxs-lookup"><span data-stu-id="69735-115">Journal header</span></span>

<span data-ttu-id="69735-116">Sistema teikia prioritetą žurnalo antraštės parametrui.</span><span class="sxs-lookup"><span data-stu-id="69735-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="69735-117">Esant numatytiesiems parametrams, šis parametras gaunamas iš žurnalo pavadinimo.</span><span class="sxs-lookup"><span data-stu-id="69735-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="69735-118">Esant numatytiesiems parametrams, žurnalo pavadinimas gaunamas iš puslapio **DK parametrai**, kai sukuriamas žurnalo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="69735-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="69735-119">Tolesniuose skyriuose paaiškinama, kaip įjungti atidėtą mokesčių skaičiavimą juridiniams subjektams, žurnalų pavadinimams ir žurnalų antraštėms.</span><span class="sxs-lookup"><span data-stu-id="69735-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="69735-120">Atidėto mokesčių skaičiavimo įjungimas juridinio subjekto lygyje</span><span class="sxs-lookup"><span data-stu-id="69735-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="69735-121">Eikite į **Didžioji knyga \> Didžiosios knygos nustatymas \> DK parametrai**.</span><span class="sxs-lookup"><span data-stu-id="69735-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="69735-122">Skirtuke **PVM**, „FastTab“ **Bendra**, nustatykite parinkties **Uždelstas mokesčių skaičiavimas** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="69735-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Didžiosios knygos parametrų vaizdas](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="69735-124">Atidėto mokesčių skaičiavimo įjungimas žurnalo pavadinimo lygyje</span><span class="sxs-lookup"><span data-stu-id="69735-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="69735-125">Eikite į **Didžioji knyga \> Žurnalo nustatymas \> Žurnalo pavadinimai**.</span><span class="sxs-lookup"><span data-stu-id="69735-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="69735-126">„FastTab“ **Bendra**, dalyje **PVM**, nustatykite parinkties **Uždelstas mokesčių skaičiavimas** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="69735-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Žurnalų pavadinimų vaizdas](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="69735-128">Atidėto mokesčių skaičiavimo įjungimas žurnalo antraštės lygyje</span><span class="sxs-lookup"><span data-stu-id="69735-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="69735-129">Eikite į **Didžioji knyga \> Žurnalų įrašai \> Bendrieji žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="69735-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="69735-130">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="69735-130">Select **New**.</span></span>
3. <span data-ttu-id="69735-131">Pasirinkite žurnalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="69735-131">Select a journal name.</span></span>
4. <span data-ttu-id="69735-132">Skirtuke **Sąranka** nustatykite parinkties **Uždelstas mokesčių skaičiavimas** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="69735-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Bendrojo žurnalo puslapio vaizdas](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]