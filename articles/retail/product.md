---
title: Produktų rekomendacijos EKA
description: Šioje temoje aprašomos produktų rekomendacijų naudojimas elektroniniame kasos aparate (EKA).
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: c78fc1f2f1bb08d01828a8b71ad5d3c16ad31b86
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278390"
---
# <a name="product-recommendations-on-pos"></a><span data-ttu-id="9e34a-103">Produktų rekomendacijos EKA</span><span class="sxs-lookup"><span data-stu-id="9e34a-103">Product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9e34a-104">Iš esmės produktų rekomendacijos yra pokyčius lemianti verslo programa, kuri apima visas mažmeninės prekybos erdves, kad sukurtų turtingą, įtraukiančią ir pritaikytą produktų atradimo patirtį.</span><span class="sxs-lookup"><span data-stu-id="9e34a-104">At its core, product Recommendations are a transformative business application that span across all retail spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="9e34a-105">Norėdami įdiegti šią funkciją EKA, atlikite veiksmus, atliktinus norint [įtraukti rekomendacijas į EKA įrenginius.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="9e34a-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="9e34a-106">Daugiau informacijos apie produktų rekomendacijų funkcijas rasite [produkto rekomendacijų apžvalgoje.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="9e34a-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="9e34a-107">Scenarijai</span><span class="sxs-lookup"><span data-stu-id="9e34a-107">Scenarios</span></span>

<span data-ttu-id="9e34a-108">Produktų rekomendacijas galima naudoti taikant toliau nurodytus EKA scenarijus.</span><span class="sxs-lookup"><span data-stu-id="9e34a-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="9e34a-109">Juos rasite naudodami „Cloud POS“ arba „Modern POS“ (MPOS).</span><span class="sxs-lookup"><span data-stu-id="9e34a-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="9e34a-110">Puslapyje **Produkto informacija**:</span><span class="sxs-lookup"><span data-stu-id="9e34a-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="9e34a-111">• Jeigu parduotuvės atstovas puslapyje **Produkto informacija** apsilanko skirtinguose kanaluose žiūrėdamas į ankstesnes operacijas, rekomendacijų tarnyba siūlo papildomų prekių, kurios gali būti perkamos kartu.</span><span class="sxs-lookup"><span data-stu-id="9e34a-111">• If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="9e34a-112">[![Rekomendacijos puslapyje Produkto informacija](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="9e34a-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="9e34a-113">Puslapyje **Operacija**:</span><span class="sxs-lookup"><span data-stu-id="9e34a-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="9e34a-114">• Rekomendacijų variklis pasiūlo prekes, pagrįstas visu krepšelio prekių, kurios dažnai perkamos kartu, sąrašu.</span><span class="sxs-lookup"><span data-stu-id="9e34a-114">• The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9e34a-115">Norėdamas, kad rekomendacijos būtų rodomos puslapyje **Operacija**, pardavėjas turi atnaujinti „Dynamics 365 for Retail“ ekrano išdėstymą.</span><span class="sxs-lookup"><span data-stu-id="9e34a-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="9e34a-116">Valdiklis **Rekomendacijos** turi būti perkeltas į puslapį **Operacija**.</span><span class="sxs-lookup"><span data-stu-id="9e34a-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="9e34a-117">[![Rekomendacijos puslapyje Operacijos](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="9e34a-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a><span data-ttu-id="9e34a-118">Sukonfigūruokite „Dynamics 365 Retail“, kad būtų leidžiamos EKA rekomendacijos</span><span class="sxs-lookup"><span data-stu-id="9e34a-118">Configure Dynamics 365 Retail to enable POS recommendations</span></span>

<span data-ttu-id="9e34a-119">Norėdami nustatyti produktų rekomendacijas, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9e34a-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="9e34a-120">Užtikrinkite, kad jūsų tarnyba buvo atnaujinta į **10.0.6 komponavimo versiją.**</span><span class="sxs-lookup"><span data-stu-id="9e34a-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="9e34a-121">Sekite instrukcijas, kaip [įgalinti produktų rekomendacijas](../commerce/enable-product-recommendations.md) jūsų verslui.</span><span class="sxs-lookup"><span data-stu-id="9e34a-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="9e34a-122">Nebūtina: norėdami, kad rekomendacijos būtų rodomos operacijos ekrane, eikite į dalį **Ekrano išdėstymas**, pasirinkite savo ekrano išdėstymą, paleiskite **ekrano išdėstymo kūrimo priemonę**, o po to kur reikia perkelkite **rekomendacijų** valdiklį.</span><span class="sxs-lookup"><span data-stu-id="9e34a-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="9e34a-123">Eikite į **Mažmeninės prekybos parametrai**, pasirinkite **Mašininis mokymas**, dalyje **Įjungti EKA rekomendacijas** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="9e34a-123">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="9e34a-124">Norėdami pamatyti rekomendacijas naudodami EKA, paleiskite visuotinės konfigūracijos užduotį **1110**.</span><span class="sxs-lookup"><span data-stu-id="9e34a-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="9e34a-125">Norėdami, kad būtų rodomi EKA ekrano išdėstymo kūrimo priemonei atlikti pakeitimai, paleiskite kanalo konfigūracijos užduotį **1070**.</span><span class="sxs-lookup"><span data-stu-id="9e34a-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="9e34a-126">Trikčių šalinimas, kai funkcija Produktų rekomendacijos jau įjungta</span><span class="sxs-lookup"><span data-stu-id="9e34a-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="9e34a-127">Eikite į **Mažmeninės prekybos parametrai** \> **Rekomendacijų sąrašai** \> **Išjungti produktų rekomendacijas** ir paleiskite **visuotinės konfigūracijos užduotį \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="9e34a-127">Navigate to **Retail Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="9e34a-128">Jei, naudodami **ekrano maketo dizaino įrankį**, į savo operacijų ekraną įtraukėte **rekomendacijų valdiklį**, jį taip pat pašalinkite.</span><span class="sxs-lookup"><span data-stu-id="9e34a-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="9e34a-129">Jei turite papildomų klausimų, norėdami gauti daugiau informacijos peržiūrėkite [rekomendacijų DUK](../commerce/faq-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="9e34a-129">If you have additional questions, check out the [Recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e34a-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9e34a-130">Additional resources</span></span>

<span data-ttu-id="9e34a-131">[Pridėti rekomendacijų valdiklį prie operacijos puslapio, esančio EKA įrenginyje](add-recommendations-control-pos-screen.md)
[Produktų rekomendacijų apžvalga](../commerce/product-recommendations.md)
[Įgalinti produkto rekomendacijas](../commerce/enable-product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="9e34a-131">[Add a recommendations control to the transaction page on a POS device](add-recommendations-control-pos-screen.md)
[Product recommendations overview](../commerce/product-recommendations.md)
[Enable product recommendations](../commerce/enable-product-recommendations.md)</span></span> 
