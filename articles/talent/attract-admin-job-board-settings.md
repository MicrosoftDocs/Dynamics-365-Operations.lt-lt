---
title: „Broadbean“ integravimo įjungimas „Microsoft Dynamics 365 for Talent - Attract”
description: Šioje temoje paaiškinama, kaip sukonfigūruoti „Microsoft Dynamics 365 for Talent - Attract” registruoti užduotims išorinėse darbo skelbimų lentose, pvz., „Broadbean”.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 2334c2bd0edccf3000f8d91651afafd4619ad0b8
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739684"
---
# <a name="enable-broadbean-integration"></a><span data-ttu-id="e6edd-103">„Broadbean“ integravimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="e6edd-103">Enable Broadbean integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e6edd-104">Juk norite, kad apie jūsų siūlomas laisvas pareigas sužinotų kiek įmanoma daugiau kvalifikuotų kandidatų.</span><span class="sxs-lookup"><span data-stu-id="e6edd-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="e6edd-105">Įdarbinimo svetainės, pvz., „Broadbean“ gali padėti šį tikslą pasiekti.</span><span class="sxs-lookup"><span data-stu-id="e6edd-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="e6edd-106">Naudodamiesi „ Microsoft Dynamics 365 for Talent: Attract“ dabar galite registruoti darbo skelbimus „Broadbean“ ir šioje srityje „Microsoft“ nuolat teikia naujų pasiūlymų.</span><span class="sxs-lookup"><span data-stu-id="e6edd-106">Microsoft Dynamics 365 for Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="e6edd-107">Norėdami registruoti užduotis išorinėse svetainėse, turite turėti [išsamios įdarbinimo informacijos priedą](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="e6edd-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="e6edd-108">Norėdami registruoti darbo skelbimus „Broadbean“ naudodami „Attract“, turite turėti „Broadbean“ abonementą.</span><span class="sxs-lookup"><span data-stu-id="e6edd-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="e6edd-109">Šiuo metu ši funkcija yra peržiūrima.</span><span class="sxs-lookup"><span data-stu-id="e6edd-109">This feature is currently in preview.</span></span> <span data-ttu-id="e6edd-110">Jei norite ją išbandyti, turite [įjungti šią funkciją „Attract“ administratoriaus parametrų srityje](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="e6edd-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="e6edd-111">„Broadbean“ integravimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e6edd-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="e6edd-112">Prisijunkite prie „Attract“ kaip administratorius.</span><span class="sxs-lookup"><span data-stu-id="e6edd-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="e6edd-113">Paspauskite viršutiniame dešiniajame puslapio kampe esantį mygtuką **Parametrai** (krumpliaračio simbolis), o paskui pasirinkite **Administravimo centras**.</span><span class="sxs-lookup"><span data-stu-id="e6edd-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="e6edd-114">Susisiekite su „Broadbean“ ir srityse **Vartotojo vardas**, **Kliento ID** ir **Šifravimo raktas** įveskite savo informaciją.</span><span class="sxs-lookup"><span data-stu-id="e6edd-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="e6edd-115">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e6edd-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="e6edd-116">Jūsų „Broadbean“ kredencialai yra slapta ir konfidenciali informacija.</span><span class="sxs-lookup"><span data-stu-id="e6edd-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="e6edd-117">Todėl juos saugodami ir bendrindami elkitės atsakingai.</span><span class="sxs-lookup"><span data-stu-id="e6edd-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="e6edd-118">Šiuos kredencialus gali matyti visi, kuriems suteiktas „Attract“ administratoriaus vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="e6edd-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="e6edd-119">„Microsoft“ ir „Attract“ šių verčių nekuria ir jų netvarko.</span><span class="sxs-lookup"><span data-stu-id="e6edd-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="e6edd-120">Jūs esate atsakingi už jų atnaujinimą „Attract“ ir už tai, kad naudojantis „Broadbean“ būtų išspręstos visos su jūsų kredencialais susijusios problemos.</span><span class="sxs-lookup"><span data-stu-id="e6edd-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
