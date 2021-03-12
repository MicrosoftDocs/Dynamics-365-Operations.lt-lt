---
title: Perkėlimo koregavimo žurnalo įrašų registravimas turto nuomoje
description: Šioje temoje aprašomos funkcijos, leidžiančios jums pereiti į nuomos portfelį pagal naujus nuomos apskaitos standartus, apskaitos standartų kodifikavimo temą Nr. 842 (ASC 842) ir tarptautinį finansinės atskaitomybės standartą Nr. 16 (IFRS 16).
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 51ae41e22507d77f32b8b0f4685cce797fd19cff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969558"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="be85d-103">Perkėlimo koregavimo žurnalo įrašų registravimas turto nuomoje</span><span class="sxs-lookup"><span data-stu-id="be85d-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be85d-104">Šioje temoje aprašomos funkcijos, leidžiančios jums pereiti į nuomos portfelį su naujais nuomos apskaitos standartais: apskaitos standartų kodifikavimo tema Nr. 842 (ASC 842), kuri yra standartas bendrai priimtuose apskaitos principuose JAV (US GAAO)., ir tarptautiniu finansinės atskaitomybės standartu Nr. 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="be85d-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="be85d-105">Norėdami gauti informacijos apie tai, kaip nustatyti perėjimo į naujus standartus knygą, žr. [Nuomos knygų nustatymas](set-up-lease-books.md).</span><span class="sxs-lookup"><span data-stu-id="be85d-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="be85d-106">Kuriant perėjimo derinimo žurnalo įrašą, generuojamas žurnalo įrašas.</span><span class="sxs-lookup"><span data-stu-id="be85d-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="be85d-107">Šis įrašas atspindi nuomos balansų poveikį, kuris yra įrašomas pagal naujus standartus tą dieną.</span><span class="sxs-lookup"><span data-stu-id="be85d-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="be85d-108">Atitinkama turto sąskaita debetuojama dėl tos datos balansinės vertės, o įsipareigojimo sąskaita kredituojama.</span><span class="sxs-lookup"><span data-stu-id="be85d-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="be85d-109">Skirtumas yra arba debetuojamas, arba kredituojamas į nepaskirstytąjį pelną.</span><span class="sxs-lookup"><span data-stu-id="be85d-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="be85d-110">Norėdami užregistruoti perėjimo derinimą, laikydamasis naujų apskaitos standartų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="be85d-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="be85d-111">Puslapyje **Nuomos suvestinė** pasirinkite nuomą, tada – **Knygos**.</span><span class="sxs-lookup"><span data-stu-id="be85d-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="be85d-112">Knygoje pasirinkite **Mokėjimo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="be85d-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="be85d-113">Dialogo lange **Mokėjimo grafikas** pasirinkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="be85d-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="be85d-114">Tada uždarykite dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="be85d-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="be85d-115">Pasirinkite **Perkėlimo koregavimas**.</span><span class="sxs-lookup"><span data-stu-id="be85d-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="be85d-116">Gali būti sukurtas tik nuomos knygų, priskirtų knygai, kurioje yra laukas **Perkėlimo knyga**, perkėlimo koregavimas.</span><span class="sxs-lookup"><span data-stu-id="be85d-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="be85d-117">Jei lauko **Nuomos pradžia** vertė yra vėlesnė už perkėlimo datą, lauko **Perkėlimo koregavimas** vertė nebus atnaujinta.</span><span class="sxs-lookup"><span data-stu-id="be85d-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="be85d-118">Norėdami peržiūrėti žurnalo įrašą, pasirinkite **Turto nuomos žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="be85d-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="be85d-119">Pasirinkite naują žurnalą ir pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="be85d-119">Select the new journal, and then select **Post**.</span></span>
