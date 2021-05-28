---
title: Duomenų srities nustatymas iš naujo
description: Šioje temoje išvardintos aplinkybės, kurias galima pagerinti iš naujo nustačius duomenų sritį, ir aplinkybės, kurių metų duomenų srities nustatymas iš naujo vargu, ar padės.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988997"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="06af6-103">Duomenų srities nustatymas iš naujo</span><span class="sxs-lookup"><span data-stu-id="06af6-103">When to reset a data mart</span></span>

<span data-ttu-id="06af6-104">Duomenų srities nustatymas iš naujo gali užimti daug laiko.</span><span class="sxs-lookup"><span data-stu-id="06af6-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="06af6-105">Atsižvelgiant į aplinkybes, šis veiksmas gali būti netinkamas sprendimas.</span><span class="sxs-lookup"><span data-stu-id="06af6-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="06af6-106">Šioje temoje išvardintos aplinkybės, kurias galima pagerinti iš naujo nustačius duomenų sritį, ir aplinkybės, kurių metų duomenų srities nustatymas iš naujo vargu, ar padės.</span><span class="sxs-lookup"><span data-stu-id="06af6-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="06af6-107">Kada reikia iš naujo nustatyti duomenų sritį?</span><span class="sxs-lookup"><span data-stu-id="06af6-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="06af6-108">Apsvarstykite šiuos dalykus prieš iš naujo nustatydami duomenų sritį.</span><span class="sxs-lookup"><span data-stu-id="06af6-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="06af6-109">Jei atsakysite „taip” į vieną ar daugiau klausimų, vadinasi, jūsų organizacijai gali būti naudinga iš naujo nustatant duomenų sritį.</span><span class="sxs-lookup"><span data-stu-id="06af6-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="06af6-110">Ar buvo atkurta programos duomenų bazė?</span><span class="sxs-lookup"><span data-stu-id="06af6-110">Was the application database restored?</span></span>
- <span data-ttu-id="06af6-111">Jei inicijavote pagalbos įvykį ir pagalbos inžinierius jums nurodė atlikti trikčių diagnostikos veiksmą – iš naujo nustatyti duomenų sritį?</span><span class="sxs-lookup"><span data-stu-id="06af6-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="06af6-112">Kada nėra tinkama iš naujo nustatyti duomenų sritį?</span><span class="sxs-lookup"><span data-stu-id="06af6-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="06af6-113">Tam tikrais atvejais nerekomenduojame iš naujo nustatyti duomenų sritį.</span><span class="sxs-lookup"><span data-stu-id="06af6-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="06af6-114">Šiais atvejais.</span><span class="sxs-lookup"><span data-stu-id="06af6-114">These include the following.</span></span> 

- <span data-ttu-id="06af6-115">Kyla našumo problemų, susietų su duomenų sinchronizavimu.</span><span class="sxs-lookup"><span data-stu-id="06af6-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="06af6-116">Jei turite pasikartojantį nustatymo iš naujo šabloną dėl šių priežasčių:</span><span class="sxs-lookup"><span data-stu-id="06af6-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="06af6-117">**Trūksta duomenų**</span><span class="sxs-lookup"><span data-stu-id="06af6-117">**Missing data**</span></span> 
  - <span data-ttu-id="06af6-118">**Įstrigti integravimo būsena**</span><span class="sxs-lookup"><span data-stu-id="06af6-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="06af6-119">**Pasenę įrašai** – vien dėl pasenusių įrašų nebūtinai atkurti duomenų sritį iš naujo.</span><span class="sxs-lookup"><span data-stu-id="06af6-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="06af6-120">Jei jūsų duomenų rinkinys didelis, atkūrimo procedūra užtruks, tačiau mažai tikėtina, kad tai išspręs problemą.</span><span class="sxs-lookup"><span data-stu-id="06af6-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="06af6-121">Kaip nustatyti iš naujo duomenis?</span><span class="sxs-lookup"><span data-stu-id="06af6-121">What is a data mart reset?</span></span>
- <span data-ttu-id="06af6-122">Nustatymas iš naujo bus pradedamas, tik tada, kai esamos užduotys bus įvykdytos.</span><span class="sxs-lookup"><span data-stu-id="06af6-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="06af6-123">Tai užtikrina, kad senieji duomenys nėra įtraukiami.</span><span class="sxs-lookup"><span data-stu-id="06af6-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="06af6-124">Šiuo metu gali pasirodyti pranešimas: „Nepavyko apdoroti duomenų srities nustatymo iš naujo dėl aktyvios užduoties.</span><span class="sxs-lookup"><span data-stu-id="06af6-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="06af6-125">Bandykite vėliau”.</span><span class="sxs-lookup"><span data-stu-id="06af6-125">Please try again later.”</span></span>
- <span data-ttu-id="06af6-126">Atkūrimo procedūra išjungs integravimo užduotis ir panaikins visus duomenų srities duomenis.</span><span class="sxs-lookup"><span data-stu-id="06af6-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="06af6-127">Integravimas įjungtas iš naujo.</span><span class="sxs-lookup"><span data-stu-id="06af6-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="06af6-128">Jei iš naujo nustatysite duomenų saugyklą, prarasite jau sukurtas ataskaitas?</span><span class="sxs-lookup"><span data-stu-id="06af6-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="06af6-129">Ne, jūsų ataskaitos saugomos SQL lentelėse, kurių neturi įtakos iš naujo nustatytas duomenų saugyklų nustatymas.</span><span class="sxs-lookup"><span data-stu-id="06af6-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="06af6-130">Jei susiję su bet kokių jūsų sukurtos ataskaitos praradimu, galite sukurti atsarginę dizainų, kuriuos nenorite prarasti, kopijas.</span><span class="sxs-lookup"><span data-stu-id="06af6-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="06af6-131">Norėdami sukurti atsarginę jų kopijas, atidarykite Ataskaitų konstruktorius ir pereikite į **Įmonė > Įmonės > Kūrimo blokai > Eksportavimas**.</span><span class="sxs-lookup"><span data-stu-id="06af6-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="06af6-132">Ar būtina visiems vartotojams išeiti iš sistemos norint iš naujo nustatyti duomenų saugyklą?</span><span class="sxs-lookup"><span data-stu-id="06af6-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="06af6-133">Ne, vartotojai gali toliau dirbti sistemoje per duomenų saugyklų iš naujo.</span><span class="sxs-lookup"><span data-stu-id="06af6-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="06af6-134">Tačiau, kol nebus baigtas nustatymas iš naujo, jie negalės pasiekti jokių ataskaitų, sukurtų su financial Reporter.</span><span class="sxs-lookup"><span data-stu-id="06af6-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
