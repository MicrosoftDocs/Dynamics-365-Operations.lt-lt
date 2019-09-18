---
title: Integravimo trikčių diagnostika naudojant „LinkedIn” ir „Microsoft Dynamics 365 for Talent - Attract”
description: Šioje temoje paaiškinama, kaip šalinti triktis, registruojant darbo skelbimą iš „Microsoft Dynamics 365 for Talent - Attract” į „LinkedIn”.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 82ba7c505ba09e47f3c517c74c22e6aef7cd4e65
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739362"
---
# <a name="troubleshoot-integration-with-linkedin"></a><span data-ttu-id="6e32b-103">Integravimo su „LinkedIn“ trikčių diagnostika</span><span class="sxs-lookup"><span data-stu-id="6e32b-103">Troubleshoot integration with LinkedIn</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e32b-104">Naudokite toliau nurodytą informaciją, norėdami išspręsti triktis, kurios gali kilti, registruojant darbo skelbimus iš „Microsoft Dynamics 365 for Talent: Attract” į „LinkedIn”.</span><span class="sxs-lookup"><span data-stu-id="6e32b-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 for Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="6e32b-105">Negalite prisijungti prie „LinkedIn” iš „Attract”</span><span class="sxs-lookup"><span data-stu-id="6e32b-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="6e32b-106">Jei kyla problemų prisijungiant prie „LinkedIn” iš „Attract”, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6e32b-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="6e32b-107">Patikrinkite, ar „Attract“ įvesti teisingi „LinkedIn“ kredencialai.</span><span class="sxs-lookup"><span data-stu-id="6e32b-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="6e32b-108">Jei kredencialai teisingi, susisiekite su [„LinkedIn“ pagalbos tarnyba](https://www.linkedin.com/help/linkedin).</span><span class="sxs-lookup"><span data-stu-id="6e32b-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="6e32b-109">Iškilus problemų, kreipkitės į [„Microsoft“ pagalbos tarnybą](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="6e32b-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="6e32b-110">„Attract” darbo skelbimai nerodomi „LinkedIn”</span><span class="sxs-lookup"><span data-stu-id="6e32b-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="6e32b-111">Jei po 24 valandų jūsų darbas neatsirado „LinkedIn”, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6e32b-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="6e32b-112">Įsitikinkite, kad jūsų „LinkedIn” įmonės ID siejasi su jūsų įmonės „LinkedIn” puslapiu ir yra tinkamai įvestas „Attract” administravimo centre.</span><span class="sxs-lookup"><span data-stu-id="6e32b-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="6e32b-113">Daugiau informacijos apie tai, kaip pakeisti „LinkedIn” parametrus administravimo centre, žr. [Integracijos su „LinkedIn” nustatymas](attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="6e32b-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn](attract-admin-linkedin.md).</span></span> <span data-ttu-id="6e32b-114">Daugiau informacijos apie „LinkedIn” įmonės ID, žr. [„LinkedIn” įmonės ID su „LinkedIn” darbo skelbimų lenta susiejimas – dažnai užduodami klausimai](https://www.linkedin.com/help/linkedin/answer/98972).</span><span class="sxs-lookup"><span data-stu-id="6e32b-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="6e32b-115">Patikrinkite „LinkedIn” darbo informaciją, kad įsitikintumėte, jog adresas baigtas.</span><span class="sxs-lookup"><span data-stu-id="6e32b-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="6e32b-116">„LinkedIn” turi būti įrašytas bent darbo miestas ir šalis ar regionas, kad sėkmingai registruotumėte darbo skelbimą.</span><span class="sxs-lookup"><span data-stu-id="6e32b-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="6e32b-117">Įsitikinkite, kad darbas nedubliuoja kito darbo, kuris buvo registruotas „LinkedIn”.</span><span class="sxs-lookup"><span data-stu-id="6e32b-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="6e32b-118">„LinkedIn” neregistruos darbo skelbimų, kurie yra „LinkedIn” „Premium” darbo vietų arba apribotų skelbimų dublikatai iš kito šaltinio.</span><span class="sxs-lookup"><span data-stu-id="6e32b-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="6e32b-119">Patikrinkite, ar kitas jūsų įmonės asmuo neregistravo darbo rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="6e32b-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e32b-120">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="6e32b-120">See also</span></span>

[<span data-ttu-id="6e32b-121">DUK apie „LinkedIn“</span><span class="sxs-lookup"><span data-stu-id="6e32b-121">LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="6e32b-122">Darbo skelbimų registravimas „LinkedIn“ iš „Attract“</span><span class="sxs-lookup"><span data-stu-id="6e32b-122">Post jobs to LinkedIn from Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="6e32b-123">Kandidatų ieška naudojant „LinkedIn Recruiter”</span><span class="sxs-lookup"><span data-stu-id="6e32b-123">Source candidates with LinkedIn Recruiter</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="6e32b-124">Darbo vietų kūrimas</span><span class="sxs-lookup"><span data-stu-id="6e32b-124">Create jobs</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="6e32b-125">Integravimo su „LinkedIn“ trikčių diagnostika</span><span class="sxs-lookup"><span data-stu-id="6e32b-125">Troubleshoot integration with LinkedIn</span></span>](./attract-troubleshoot-linkedin.md)
