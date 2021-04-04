---
title: Duomenų srities nustatymas iš naujo
description: Šioje temoje išvardintos aplinkybės, kurias galima pagerinti iš naujo nustačius duomenų sritį, ir aplinkybės, kurių metų duomenų srities nustatymas iš naujo vargu, ar padės.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71324d4aa2d20dd6ae4729412a017d130ab0144f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563741"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="5046c-103">Duomenų srities nustatymas iš naujo</span><span class="sxs-lookup"><span data-stu-id="5046c-103">When to reset a data mart</span></span>

<span data-ttu-id="5046c-104">Duomenų srities nustatymas iš naujo gali užimti daug laiko.</span><span class="sxs-lookup"><span data-stu-id="5046c-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="5046c-105">Atsižvelgiant į aplinkybes, šis veiksmas gali būti netinkamas sprendimas.</span><span class="sxs-lookup"><span data-stu-id="5046c-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="5046c-106">Šioje temoje išvardintos aplinkybės, kurias galima pagerinti iš naujo nustačius duomenų sritį, ir aplinkybės, kurių metų duomenų srities nustatymas iš naujo vargu, ar padės.</span><span class="sxs-lookup"><span data-stu-id="5046c-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="5046c-107">Kada reikia iš naujo nustatyti duomenų sritį?</span><span class="sxs-lookup"><span data-stu-id="5046c-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="5046c-108">Apsvarstykite šiuos dalykus prieš iš naujo nustatydami duomenų sritį.</span><span class="sxs-lookup"><span data-stu-id="5046c-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="5046c-109">Jei atsakysite „taip” į vieną ar daugiau klausimų, vadinasi, jūsų organizacijai gali būti naudinga iš naujo nustatant duomenų sritį.</span><span class="sxs-lookup"><span data-stu-id="5046c-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="5046c-110">Programos duomenų bazė buvo atkurta, tačiau nebuvo atkurta duomenų srities duomenų bazė.</span><span class="sxs-lookup"><span data-stu-id="5046c-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="5046c-111">Jeigu matote neteisingus apskaitos laikotarpio duomenis, tai nėra ataskaitos maketo klaida.</span><span class="sxs-lookup"><span data-stu-id="5046c-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="5046c-112">Jeigu matote neteisingus ataskaitinio laikotarpio duomenis, ir Ataskaitų kūrimo įrankio **Integravimo būsena** puslapyje išvardinti integravimo bandymų įrašai (įjunkite Ataskaitų kūrimo įrankį ir pasirinkite **Įrankiai > Integravimo būsena**).</span><span class="sxs-lookup"><span data-stu-id="5046c-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="5046c-113">Inicijavote pagalbos įvykį ir pagalbos inžinierius jums nurodė atlikti trikčių diagnostikos veiksmą – iš naujo nustatyti duomenų sritį.</span><span class="sxs-lookup"><span data-stu-id="5046c-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="5046c-114">Kada nėra tinkama iš naujo nustatyti duomenų sritį?</span><span class="sxs-lookup"><span data-stu-id="5046c-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="5046c-115">Tam tikrais atvejais nerekomenduojame iš naujo nustatyti duomenų sritį.</span><span class="sxs-lookup"><span data-stu-id="5046c-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="5046c-116">Šiais atvejais.</span><span class="sxs-lookup"><span data-stu-id="5046c-116">These include the following.</span></span> 

- <span data-ttu-id="5046c-117">Kitais šioje temoje nenurodytais atvejais.</span><span class="sxs-lookup"><span data-stu-id="5046c-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="5046c-118">Kyla veikimo problemų, susijusių su duomenų sinchronizavimu. Šiuo atveju duomenų srities nustatymas iš naujo tikriausiai nebus veiksmingas.</span><span class="sxs-lookup"><span data-stu-id="5046c-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="5046c-119">Jei turite pasikartojantį nustatymo iš naujo šabloną dėl šių priežasčių:</span><span class="sxs-lookup"><span data-stu-id="5046c-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="5046c-120">**Trūksta duomenų** – pirma, pašalinkite ataskaitos kūrimo įrankio ir duomenų sinchronizacijos problemas, pavyzdžiui, pastebėjote, kad susiejimas neįvyko nuo to laiko, kai buvo paskelbti trūkstami duomenys.</span><span class="sxs-lookup"><span data-stu-id="5046c-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="5046c-121">**Užstrigusi integravimo būsena** – jeigu integracija vyksta lėtai arba sustojo, mažai tikėtina, kad duomenų srities nustatymas iš naujo išspręs problemą.</span><span class="sxs-lookup"><span data-stu-id="5046c-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="5046c-122">**Bandymai atkurti nepavyko** – jeigu nepavyko atkurti po kelių bandymų dėl trūkstamų duomenų, rekomenduojame inicijuoti pagalbos incidentą ir išanalizuoti situaciją su pagalbos inžinieriumi prieš dar kartą bandant atkurti duomenų sritį.</span><span class="sxs-lookup"><span data-stu-id="5046c-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="5046c-123">**Pasenę įrašai** – vien dėl pasenusių įrašų nebūtinai atkurti duomenų sritį iš naujo.</span><span class="sxs-lookup"><span data-stu-id="5046c-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="5046c-124">Jei jūsų duomenų rinkinys didelis, atkūrimo procedūra užtruks, tačiau mažai tikėtina, kad tai išspręs problemą.</span><span class="sxs-lookup"><span data-stu-id="5046c-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="5046c-125">Ko duomenų srities atkūrimas neatlieka</span><span class="sxs-lookup"><span data-stu-id="5046c-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="5046c-126">Nustatymas iš naujo bus pradedamas, tik tada, kai esamos užduotys bus įvykdytos.</span><span class="sxs-lookup"><span data-stu-id="5046c-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="5046c-127">Tai užtikrina, kad senieji duomenys nėra įtraukiami.</span><span class="sxs-lookup"><span data-stu-id="5046c-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="5046c-128">Šiuo metu gali pasirodyti pranešimas: „Nepavyko apdoroti duomenų srities nustatymo iš naujo dėl aktyvios užduoties.</span><span class="sxs-lookup"><span data-stu-id="5046c-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="5046c-129">Bandykite vėliau”.</span><span class="sxs-lookup"><span data-stu-id="5046c-129">Please try again later.”</span></span>
- <span data-ttu-id="5046c-130">Atkūrimo procedūra išjungs integravimo užduotis ir panaikins visus duomenų srities duomenis.</span><span class="sxs-lookup"><span data-stu-id="5046c-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="5046c-131">Integravimas įjungtas iš naujo.</span><span class="sxs-lookup"><span data-stu-id="5046c-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="5046c-132">Šie aspektai pabrėžia du dalykus, kurių duomenų srities atkūrimas *neatliks*.</span><span class="sxs-lookup"><span data-stu-id="5046c-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="5046c-133">Atkūrimo procedūra neišvalo ataskaitų kūrimo įrankių.</span><span class="sxs-lookup"><span data-stu-id="5046c-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="5046c-134">Atkūrimo procedūra neišvalo pasirinktų įmonės ar vartotojų duomenų.</span><span class="sxs-lookup"><span data-stu-id="5046c-134">Resets do not clear company data or user data unless selected.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]