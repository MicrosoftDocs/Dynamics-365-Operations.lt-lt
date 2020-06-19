---
title: Kuruojamų rekomendacijų kūrimas rankiniu būdu
description: Šioje temoje paaiškinama, kaip prekybininkai gali rankiniu būdu kurti ir tvarkyti produktų sąrašus, skirtus „Microsoft Dynamics 365 Commerce“ klientams.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b866704b419fb07dcf1ddd386af2f7d6cfa02e2
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404121"
---
# <a name="manually-create-curated-recommendations"></a><span data-ttu-id="efc4e-103">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="efc4e-103">Manually create curated recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="efc4e-104">Šioje temoje paaiškinama, kaip prekybininkai gali rankiniu būdu kurti ir tvarkyti produktų rekomendacijų sąrašus, skirtus „Microsoft Dynamics 365 Commerce“ klientams.</span><span class="sxs-lookup"><span data-stu-id="efc4e-104">This topic explains how merchandizers can manually create and manage product recommendations lists for Microsoft Dynamics 365 Commerce customers.</span></span>

<span data-ttu-id="efc4e-105">Kuruojami sąrašai yra atskiro turinio, kurį sukūrė ir kuruoja žmonės, rinkiniai.</span><span class="sxs-lookup"><span data-stu-id="efc4e-105">Curated lists are collections of individual content, created and curated by people.</span></span>  

## <a name="create-a-new-list"></a><span data-ttu-id="efc4e-106">Naujo sąrašo sukūrimas</span><span class="sxs-lookup"><span data-stu-id="efc4e-106">Create a new list</span></span>

<span data-ttu-id="efc4e-107">Norėdami sukurti kuruojamą produktų rekomendacijų sąrašą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="efc4e-107">To create a curated product recommendation list, follow these steps.</span></span>

1. <span data-ttu-id="efc4e-108">Eikite į **Mažmeninė prekyba ir prekyba &gt; Produktų rekomendacijos &gt; Rekomendacijų sąrašai**.</span><span class="sxs-lookup"><span data-stu-id="efc4e-108">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation lists**.</span></span>
1. <span data-ttu-id="efc4e-109">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="efc4e-109">Select **New**.</span></span>
1. <span data-ttu-id="efc4e-110">Lauke **Sąrašo ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="efc4e-110">In the **List Id** field, enter a value.</span></span>
1. <span data-ttu-id="efc4e-111">Lauke **Sąrašo pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="efc4e-111">In the **List name** field, enter a value.</span></span>
    - <span data-ttu-id="efc4e-112">**Sąrašo pavadinimas** bus rodomas modulio **Produktų rinkinys** kuruojamų sąrašų skyriuje.</span><span class="sxs-lookup"><span data-stu-id="efc4e-112">The **List name** is the title of the list that will appear in the curated lists section of the **Product collection** module.</span></span>
1. <span data-ttu-id="efc4e-113">Norėdami į sąrašą įtraukti produktų, pasirinkite **įtraukti produktų**.</span><span class="sxs-lookup"><span data-stu-id="efc4e-113">To add products to the list, select **Add products**.</span></span>
1. <span data-ttu-id="efc4e-114">Norėdami pakeisti sąrašo produktų tvarką, įveskite reikšmę stulpelyje **Rodymo tvarka**.</span><span class="sxs-lookup"><span data-stu-id="efc4e-114">To change the order of the products in the list, enter a value in the **Display order** column.</span></span>
    - <span data-ttu-id="efc4e-115">Jei du produktai turi tokią pačią rodymo tvarkos reikšmę, tada galutinė tų dviejų rezultatų tvarka gali skirtis nuo esančios įmonės padalinyje.</span><span class="sxs-lookup"><span data-stu-id="efc4e-115">If two products have the same display order value, then the final order of those two results may differ from the back office.</span></span>
1. <span data-ttu-id="efc4e-116">Pasirinkite **Įrašyti**, kad įrašytumėte sąrašą.</span><span class="sxs-lookup"><span data-stu-id="efc4e-116">Select **Save** to save the list.</span></span>

## <a name="example-list"></a><span data-ttu-id="efc4e-117">Sąrašo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="efc4e-117">Example List</span></span>

![Kuruojamo sąrašo pavyzdys įmonės padalinyje](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a><span data-ttu-id="efc4e-119">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="efc4e-119">Additional resources</span></span>

[<span data-ttu-id="efc4e-120">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="efc4e-120">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="efc4e-121">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="efc4e-121">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="efc4e-122">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="efc4e-122">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="efc4e-123">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="efc4e-123">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="efc4e-124">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="efc4e-124">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="efc4e-125">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="efc4e-125">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="efc4e-126">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="efc4e-126">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="efc4e-127">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="efc4e-127">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="efc4e-128">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="efc4e-128">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="efc4e-129">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="efc4e-129">Product recommendations FAQ</span></span>](faq-recommendations.md)
