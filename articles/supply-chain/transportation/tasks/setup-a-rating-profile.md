---
title: Vertinimo šablonai
description: Šioje temoja aprašoma, kaip nustatyti duomenis kainos profiliams.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f754a8b86b0d369af03812a831d77a8a6fa8154
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233516"
---
# <a name="rating-profiles"></a><span data-ttu-id="898e1-103">Vertinimo šablonai</span><span class="sxs-lookup"><span data-stu-id="898e1-103">Rating profiles</span></span>

<span data-ttu-id="898e1-104">Kainos profiliai rodo logistikos sutartį (bet ne teisinę sutartį).</span><span class="sxs-lookup"><span data-stu-id="898e1-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="898e1-105">Jis naudojamas siekiant nustatyti gabenimo kainas kroviniams.</span><span class="sxs-lookup"><span data-stu-id="898e1-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="898e1-106">Kiekvienas kainos profilis yra unikalus siuntimo vežėjui.</span><span class="sxs-lookup"><span data-stu-id="898e1-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="898e1-107">Profilyje susiesite siuntimo vežėją su pagrindinia kaina.</span><span class="sxs-lookup"><span data-stu-id="898e1-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="898e1-108">Pagrindinė kaina nustato pagrindinės kainos priskyrimą ir pagrindinę kainą.</span><span class="sxs-lookup"><span data-stu-id="898e1-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="898e1-109">Pagrindinė kaina nustato vežėjo kainą.</span><span class="sxs-lookup"><span data-stu-id="898e1-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="898e1-110">Galite nustatyti kainos profilį naudodami bendrą puslapį, kuriame rodoma esančių kainų profilių apžvalga.</span><span class="sxs-lookup"><span data-stu-id="898e1-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="898e1-111">Kitu būdu, galite nustatyti kainos profilį tiesiai iš gabenimo vežėjo.</span><span class="sxs-lookup"><span data-stu-id="898e1-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="898e1-112">Abiem atvejais, jūsų nustatyta informacija kainos profilyje yra tokia pati.</span><span class="sxs-lookup"><span data-stu-id="898e1-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="898e1-113">Kredito ar redagavimo kainos profilis kainos profilių puslapyje</span><span class="sxs-lookup"><span data-stu-id="898e1-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="898e1-114">Puslapyje **Kainų profiliai** galite peržiūrėti visus esamus kainų profilius.</span><span class="sxs-lookup"><span data-stu-id="898e1-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="898e1-115">Galite taip pat redaguoti esančius profilius ir sukurti naujus.</span><span class="sxs-lookup"><span data-stu-id="898e1-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="898e1-116">Eikite į **Gabenimo valdymą \> Nustatymyžus \> Kainas \> Kainų profilį**.</span><span class="sxs-lookup"><span data-stu-id="898e1-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="898e1-117">Veiksmų juostoje pasirinkite **Naujas** tam, kad įtrauktumėte naują kainų profilį į tinklelį ar pasirinkite **Redaguoti** siekiant redaguoti esantį profilį.</span><span class="sxs-lookup"><span data-stu-id="898e1-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="898e1-118">Naujo ar esančio kainų profilio eilutėje, nustatykite tolesnius laukelius:</span><span class="sxs-lookup"><span data-stu-id="898e1-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="898e1-119">**Kainų profilis** – Įveskite unikalų numerį (ID) kainų profiliui.</span><span class="sxs-lookup"><span data-stu-id="898e1-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="898e1-120">**Pavadinimas** – Įveskite kainų profilį aprašantį pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="898e1-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="898e1-121">**Gabenimo vežėjas** – Pasirinkite gabenimo vežėją.</span><span class="sxs-lookup"><span data-stu-id="898e1-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="898e1-122">Kainų profilis, kurį nustatote taip pat bus rodomas **Siuntimo vežėjų** puslapyje pasirinktam vežėjui.</span><span class="sxs-lookup"><span data-stu-id="898e1-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="898e1-123">**Vieta** ir **Sandėlis** – Pasirinkite vietą ir sandėlį.</span><span class="sxs-lookup"><span data-stu-id="898e1-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="898e1-124">**Kainos variklis** – Pasirinkite kainų variklį reitingo profiliui.</span><span class="sxs-lookup"><span data-stu-id="898e1-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="898e1-125">**Pagrindinė kaina** – Pasirinkite pagrindinę kainą reitingo profiliui.</span><span class="sxs-lookup"><span data-stu-id="898e1-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="898e1-126">Galite naudoti pagrindines kainas, kad nustatytumėte pagrindinės kainos tipą ir pagrindinę kainą.</span><span class="sxs-lookup"><span data-stu-id="898e1-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="898e1-127">Dėl daugiau informacijos, žr. [Nustatyti pagrindines kainas](set-up-rate-masters.md).</span><span class="sxs-lookup"><span data-stu-id="898e1-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="898e1-128">**Perdavimo laiko variklis** – Pasirinkite perdavimo laiko variklį reitingo profiliui.</span><span class="sxs-lookup"><span data-stu-id="898e1-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="898e1-129">**Vežėjo kuro indeksas** – Pasirinkite vežėjo kuro indeksą kainų profiliui.</span><span class="sxs-lookup"><span data-stu-id="898e1-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="898e1-130">**Įsigaliojimo pradžios data ir laikas** ir **Galiojimo pabaigos data ir laikas** – Nustatykite laikotarpį, per kurį kainos profilis turi būti įjungtas.</span><span class="sxs-lookup"><span data-stu-id="898e1-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="898e1-131">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="898e1-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="898e1-132">Sukurkite kainų profilį tiesiogiai siuntimo vežėjų puslapyje</span><span class="sxs-lookup"><span data-stu-id="898e1-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="898e1-133">Eikite į **Transportavimo valdymas \> Nustatymas \> Vežėjai \> Siuntų vežėjai**.</span><span class="sxs-lookup"><span data-stu-id="898e1-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="898e1-134">Pasirinkite gabenimo siuntėją sąraše.</span><span class="sxs-lookup"><span data-stu-id="898e1-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="898e1-135">„FastTab“ **Kainų profiliai** rinkitės **Naujas** tam, kad sukurtumėte kainų profilį.</span><span class="sxs-lookup"><span data-stu-id="898e1-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="898e1-136">Nustatykite laukelius naujam kainų profiliui.</span><span class="sxs-lookup"><span data-stu-id="898e1-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="898e1-137">Šie laukeliai atitinka laukelius **Kainų profilio** puslapyje, kaip aprašyta ankstesniame šios temos skyriuje.</span><span class="sxs-lookup"><span data-stu-id="898e1-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="898e1-138">Profiliai sukurti **Siuntimo vežėjų** puslapyje yra taip pat rodomi **Kainų profilių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="898e1-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]