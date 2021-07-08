---
title: Duomenų srities nustatymo iš naujo DUK
description: Šioje temoje pateikiami atsakymai į kai kuriuos dažnai užduodamus klausimus apie duomenų srities nustatymą iš naujo.
author: jinniew
ms.date: 06/09/2021
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
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266614"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="d8a28-103">Duomenų srities nustatymo iš naujo DUK</span><span class="sxs-lookup"><span data-stu-id="d8a28-103">Data mart resets FAQ</span></span>

<span data-ttu-id="d8a28-104">Šioje temoje pateikiami atsakymai į kai kuriuos dažnai užduodamus klausimus apie duomenų srities nustatymą iš naujo.</span><span class="sxs-lookup"><span data-stu-id="d8a28-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="d8a28-105">Duomenų srities nustatymas iš naujo gali būti ilgai trunkantis procesas ir, atsižvelgiant į aplinkybes, gali nebūti reikalingas sprendimas.</span><span class="sxs-lookup"><span data-stu-id="d8a28-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="d8a28-106">Todėl šioje temoje pateikiama informacija apie aplinkybes, kai duomenų srities nustatymas iš naujo gali padėti, taip pat apie aplinkybes, kuomet jis padėti negali.</span><span class="sxs-lookup"><span data-stu-id="d8a28-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="d8a28-107">Kaip nustatyti iš naujo duomenis?</span><span class="sxs-lookup"><span data-stu-id="d8a28-107">What is a data mart reset?</span></span>

<span data-ttu-id="d8a28-108">Duomenų srities nustatymas iš naujo išjungs integravimo užduotis, panaikins visus duomenų srities duomenis ir tada iš naujo įgalins integravimą.</span><span class="sxs-lookup"><span data-stu-id="d8a28-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="d8a28-109">Norint užtikrinti, kad seni duomenys nėra įterpti, duomenų srities nustatymą iš naujo galima pradėti tik atlikus esamas užduotis.</span><span class="sxs-lookup"><span data-stu-id="d8a28-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="d8a28-110">Jei bandysite iš naujo nustatyti duomenų sritį neatlikę visų užduočių, galite gauti pranešimą, pavyzdžiui, „Duomenų srities nustatymo iš naujo nustatyti nepavyko apdoroti dėl aktyvios užduoties.</span><span class="sxs-lookup"><span data-stu-id="d8a28-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="d8a28-111">Bandykite vėliau.“</span><span class="sxs-lookup"><span data-stu-id="d8a28-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="d8a28-112">Kada turiu iš naujo nustatyti duomenų sritį?</span><span class="sxs-lookup"><span data-stu-id="d8a28-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="d8a28-113">Jei jūsų situacijai tinka vienas ar daugiau iš šių sakinių, jūsų organizacijai gali būti naudinga iš naujo nustatyti duomenų sritį:</span><span class="sxs-lookup"><span data-stu-id="d8a28-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="d8a28-114">Programos duomenų bazė buvo atkurta.</span><span class="sxs-lookup"><span data-stu-id="d8a28-114">The application database was restored.</span></span>
- <span data-ttu-id="d8a28-115">Atidarėte pagalbos kvitą, o pagalbos inžinierius jums nurodė iš naujo nustatyti duomenų sritį kaip trikčių diagnostikos veiksmo dalį.</span><span class="sxs-lookup"><span data-stu-id="d8a28-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="d8a28-116">Kada duomenų srities nustatymas iš naujo yra netinkamas?</span><span class="sxs-lookup"><span data-stu-id="d8a28-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="d8a28-117">Šiomis tam tikromis aplinkybėmis nerekomenduojame jums iš naujo nustatyti duomenų sritį:</span><span class="sxs-lookup"><span data-stu-id="d8a28-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="d8a28-118">Kyla našumo problemų, susijusių su duomenų sinchronizavimu.</span><span class="sxs-lookup"><span data-stu-id="d8a28-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="d8a28-119">Turite pasikartojantį nustatymo iš naujo šabloną dėl bet kurios iš šių priežasčių:</span><span class="sxs-lookup"><span data-stu-id="d8a28-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="d8a28-120">**Trūkstami duomenys** – Jei pastebite, kad trūksta duomenų, atidarykite palaikymo kvitą su „Microsoft”, kad peržiūrėtumėte savo ataskaitos formatą ir galimas duomenų sinchronizavimo problemas.</span><span class="sxs-lookup"><span data-stu-id="d8a28-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="d8a28-121">**Įstrigti integravimo būsena**</span><span class="sxs-lookup"><span data-stu-id="d8a28-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="d8a28-122">**Pasenę įrašai** – Vien pasenę įrašai nebūtinai pateisina duomenų srities atkūrimą iš naujo.</span><span class="sxs-lookup"><span data-stu-id="d8a28-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="d8a28-123">Jei jūsų duomenų rinkinys didelis, atkūrimo procedūra užtruks, tačiau mažai tikėtina, kad kažkas bus patobulinta.</span><span class="sxs-lookup"><span data-stu-id="d8a28-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="d8a28-124">Jei iš naujo nustatysite duomenų saugyklą, prarasite jau sukurtas ataskaitas?</span><span class="sxs-lookup"><span data-stu-id="d8a28-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="d8a28-125">Ne.</span><span class="sxs-lookup"><span data-stu-id="d8a28-125">No.</span></span> <span data-ttu-id="d8a28-126">Jūsų ataskaitos saugomos SQL lentelėse, kurių nepaveikia duomenų srities nustatymas iš naujo.</span><span class="sxs-lookup"><span data-stu-id="d8a28-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="d8a28-127">Jei esate susirūpinę, kad prarasite savo sukurtas ataskaitas, galite sukurti atsargines dizainų, kurių nenorite prarasti, kopijas.</span><span class="sxs-lookup"><span data-stu-id="d8a28-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="d8a28-128">Norėdami sukurti atsargines kopijas, atidarykite „Report Designer” ir eikite į **Įmonė \> Įmonės \> Kūrimo blokai \> Eksportavimas**.</span><span class="sxs-lookup"><span data-stu-id="d8a28-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="d8a28-129">Ar visi vartotojai turi išeiti iš sistemos, kad galėčiau iš naujo nustatyti duomenų sritį?</span><span class="sxs-lookup"><span data-stu-id="d8a28-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="d8a28-130">Ne.</span><span class="sxs-lookup"><span data-stu-id="d8a28-130">No.</span></span> <span data-ttu-id="d8a28-131">Vartotojai gali ir toliau dirbti sistemoje duomenų srities nustatymo iš naujo metu.</span><span class="sxs-lookup"><span data-stu-id="d8a28-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="d8a28-132">Tačiau, kol nebus baigtas nustatymas iš naujo, vartotojai negalės pasiekti jokių ataskaitų, sukurtų naudojant „Financial Reporter”.</span><span class="sxs-lookup"><span data-stu-id="d8a28-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
