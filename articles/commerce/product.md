---
title: Produktų rekomendacijų įtraukimas į EKA
description: Šioje temoje aprašomos produktų rekomendacijų naudojimas elektroniniame kasos aparate (EKA).
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7afe9225b8fc966ca154a5eb7421e8d4cc7c3023
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414457"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="49891-103">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="49891-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49891-104">Produktų rekomendacijos yra transformuojanti verslo programa, apimanti visas prekybos sritis ir sukurianti įdomią, patrauklią ir pritaikytą produktų atradimo patirtį.</span><span class="sxs-lookup"><span data-stu-id="49891-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="49891-105">Norėdami įdiegti šią funkciją EKA, atlikite veiksmus, atliktinus norint [įtraukti rekomendacijas į EKA įrenginius.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="49891-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="49891-106">Daugiau informacijos apie produktų rekomendacijų funkcijas rasite [produkto rekomendacijų apžvalgoje.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="49891-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="49891-107">Scenarijai</span><span class="sxs-lookup"><span data-stu-id="49891-107">Scenarios</span></span>

<span data-ttu-id="49891-108">Produktų rekomendacijas galima naudoti taikant toliau nurodytus EKA scenarijus.</span><span class="sxs-lookup"><span data-stu-id="49891-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="49891-109">Juos rasite naudodami „Cloud POS“ arba „Modern POS“ (MPOS).</span><span class="sxs-lookup"><span data-stu-id="49891-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="49891-110">Puslapyje **Produkto informacija**:</span><span class="sxs-lookup"><span data-stu-id="49891-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="49891-111">Jeigu parduotuvės atstovas puslapyje **Produkto informacija** apsilanko skirtinguose kanaluose žiūrėdamas į ankstesnes operacijas, rekomendacijų tarnyba siūlo papildomų prekių, kurios gali būti perkamos kartu.</span><span class="sxs-lookup"><span data-stu-id="49891-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="49891-112">[![Rekomendacijos puslapyje Produkto informacija](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="49891-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="49891-113">Puslapyje **Operacija**:</span><span class="sxs-lookup"><span data-stu-id="49891-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="49891-114">Rekomendacijų variklis pasiūlo prekes, pagrįstas visu krepšelio prekių, kurios dažnai perkamos kartu, sąrašu.</span><span class="sxs-lookup"><span data-stu-id="49891-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="49891-115">Norėdamas, kad rekomendacijos būtų rodomos puslapyje **Operacija**, pardavėjas turi atnaujinti „Dynamics 365 Commerce“ ekrano išdėstymą.</span><span class="sxs-lookup"><span data-stu-id="49891-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="49891-116">Valdiklis **Rekomendacijos** turi būti perkeltas į puslapį **Operacija**.</span><span class="sxs-lookup"><span data-stu-id="49891-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="49891-117">[![Rekomendacijos puslapyje Operacijos](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="49891-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="49891-118">Konfigūruokite „Commerce“, kad įgalintumėte EKA rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="49891-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="49891-119">Norėdami nustatyti produktų rekomendacijas, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="49891-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="49891-120">Užtikrinkite, kad jūsų tarnyba buvo atnaujinta į **10.0.6 komponavimo versiją.**</span><span class="sxs-lookup"><span data-stu-id="49891-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="49891-121">Sekite instrukcijas, kaip [įgalinti produktų rekomendacijas](../commerce/enable-product-recommendations.md) jūsų verslui.</span><span class="sxs-lookup"><span data-stu-id="49891-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="49891-122">Nebūtina: norėdami, kad rekomendacijos būtų rodomos operacijos ekrane, eikite į dalį **Ekrano išdėstymas**, pasirinkite savo ekrano išdėstymą, paleiskite **ekrano išdėstymo kūrimo priemonę**, o po to kur reikia perkelkite **rekomendacijų** valdiklį.</span><span class="sxs-lookup"><span data-stu-id="49891-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="49891-123">Eikite į **„Commerce“ parametrai**, pasirinkite **Mašininis mokymas** ir skyriuje **Įgalinti EKA rekomendacijas** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="49891-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="49891-124">Norėdami pamatyti rekomendacijas naudodami EKA, paleiskite visuotinės konfigūracijos užduotį **1110**.</span><span class="sxs-lookup"><span data-stu-id="49891-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="49891-125">Norėdami, kad būtų rodomi EKA ekrano išdėstymo kūrimo priemonei atlikti pakeitimai, paleiskite kanalo konfigūracijos užduotį **1070**.</span><span class="sxs-lookup"><span data-stu-id="49891-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="49891-126">Trikčių šalinimas, kai funkcija Produktų rekomendacijos jau įjungta</span><span class="sxs-lookup"><span data-stu-id="49891-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="49891-127">Eikite į **„Commerce“ parametrai** \> **Rekomendacijų sąrašai** \> **Išjungti produkto rekomendacijas** ir paleiskite **Bendra konfigūracijos užduotis\[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="49891-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="49891-128">Jei, naudodami **ekrano maketo dizaino įrankį**, į savo operacijų ekraną įtraukėte **rekomendacijų valdiklį**, jį taip pat pašalinkite.</span><span class="sxs-lookup"><span data-stu-id="49891-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="49891-129">Jei turite papildomų klausimų, norėdami gauti daugiau informacijos peržiūrėkite [Produkto rekomendacijų DUK](../commerce/faq-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="49891-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49891-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="49891-130">Additional resources</span></span>

[<span data-ttu-id="49891-131">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="49891-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="49891-132">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="49891-132">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="49891-133">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="49891-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="49891-134">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="49891-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="49891-135">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="49891-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="49891-136">Įjungti „apsipirkti panašia mada“ rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="49891-136">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="49891-137">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="49891-137">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="49891-138">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="49891-138">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="49891-139">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="49891-139">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="49891-140">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="49891-140">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="49891-141">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="49891-141">Product recommendations FAQ</span></span>](faq-recommendations.md)
