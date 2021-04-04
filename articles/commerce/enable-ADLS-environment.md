---
title: „Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje
description: Šioje temoje paaiškinama, kaip įjungti ir tikrinti „Azure Data Lake Storage“ „Dynamics 365 Commerce“ aplinkoje. Tai yra būtina sąlyga norint įgalinti produkto rekomendacijas.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5887ae7983fd817a929a185327671b301808b354
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478241"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="78187-103">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="78187-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="78187-104">Šioje temoje paaiškinama, kaip įjungti ir tikrinti „Azure Data Lake Storage“ „Dynamics 365 Commerce“ aplinkoje. Tai yra būtina sąlyga norint įgalinti produkto rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="78187-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

<span data-ttu-id="78187-105">Sprendime „Dynamics 365 Commerce“ visų produktų ir operacijų informacija sekama aplinkos objektų saugykloje.</span><span class="sxs-lookup"><span data-stu-id="78187-105">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="78187-106">Norint, kad šiuos duomenis būtų galima pasiekti naudojant kitas „Dynamics 365“ tarnybas, pvz., duomenų analizę, verslo įžvalgas ir personalizuotas rekomendacijas, reikia sujungti aplinką su klientui priklausančiu „Gen 2“ sprendimu „Azure Data Lake Storage“.</span><span class="sxs-lookup"><span data-stu-id="78187-106">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="78187-107">Kadangi „Azure Data Lake Storage“ konfigūruojama aplinkoje, visi reikiami objektų saugyklos duomenys yra dubliuojami, apsaugomi ir valdomi kliento.</span><span class="sxs-lookup"><span data-stu-id="78187-107">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="78187-108">Jei produkto rekomendacijos arba personalizuotos rekomendacijos aplinkoje taip pat įgalintos, produkto rekomendacijų dėklui bus suteikta prieiga prie paskirto aplanko, esančio „Azure Data Lake Storage“, kad būtų galima nuskaityti kliento duomenis ir apskaičiuoti jais pagrįstas rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="78187-108">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="78187-109">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="78187-109">Prerequisites</span></span>

<span data-ttu-id="78187-110">Klientai turi sukonfigūruoti „Azure Data Lake Storage“ jiems priklausančioje „Azure“ prenumeratoje.</span><span class="sxs-lookup"><span data-stu-id="78187-110">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="78187-111">Šioje temoje neaprašomas „Azure“ prenumeratos pirkimas arba saugyklos abonemento, kuriame įgalintas „Azure Data Lake Storage“, nustatymas.</span><span class="sxs-lookup"><span data-stu-id="78187-111">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="78187-112">Daugiau informacijos apie „Azure Data Lake Storage“ ieškokite [„Azure Data Lake Storage“ oficialioje „Gen2“ dokumentacijoje](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="78187-112">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="78187-113">Konfigūravimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="78187-113">Configuration steps</span></span>

<span data-ttu-id="78187-114">Šiame skyriuje aprašomi konfigūravimo veiksmai, kuriuos reikia atlikti, norint įgalinti „Azure Data Lake Storage“ aplinkoje, susijusioje su produktų rekomendacijomis.</span><span class="sxs-lookup"><span data-stu-id="78187-114">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="78187-115">Išsamesnės informacijos apie veiksmus, reikalingus įgalinti „Azure Data Lake Storage“, žr. [Leidimas objektų saugyklą naudoti kaip „Data Lake“](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="78187-115">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="78187-116">„Azure Data Lake Storage“ įgalinimas aplinkoje</span><span class="sxs-lookup"><span data-stu-id="78187-116">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="78187-117">Prisijunkite prie aplinkos tarnybinio biuro portalo.</span><span class="sxs-lookup"><span data-stu-id="78187-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="78187-118">Ieškokite **Sistemos parametrai** ir pereikite į skirtuką **Duomenų ryšiai**.</span><span class="sxs-lookup"><span data-stu-id="78187-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="78187-119">Parinktyje **Įjungti „Data Lake“ integraciją** nustatykite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="78187-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="78187-120">Parinktyje **Nuolat naujinti „Data Lake“** nustatykite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="78187-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="78187-121">Paskui įveskite toliau pateikiamą būtiną informaciją.</span><span class="sxs-lookup"><span data-stu-id="78187-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="78187-122">**Programos ID** // **Programos slapta informacija** // **DNS pavadinimas** – reikalinga, jungiantis prie „KeyVault“, kur saugoma slapta „Azure Data Lake Storage“ informacija.</span><span class="sxs-lookup"><span data-stu-id="78187-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="78187-123">**Slaptas pavadinimas** – slaptas pavadinimas, saugomas „KeyVault“ ir naudojamas autentifikuojant „Azure Data Lake Storage“.</span><span class="sxs-lookup"><span data-stu-id="78187-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="78187-124">Išsaugokite keitimus puslapio viršutiniame kairiajame kampe.</span><span class="sxs-lookup"><span data-stu-id="78187-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="78187-125">Toliau pateiktame vaizde parodytas „Azure Data Lake Storage“ konfigūracijos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="78187-125">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![„Azure Data Lake Storage“ konfigūracijos pavyzdys](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="78187-127">„Azure Data Lake Storage“ ryšio tikrinimas</span><span class="sxs-lookup"><span data-stu-id="78187-127">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="78187-128">Patikrinkite ryšį su KeyVault, naudodami saitą **Tikrinti „Azure Key Vault“**.</span><span class="sxs-lookup"><span data-stu-id="78187-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="78187-129">Patikrinkite ryšį su „Azure Data Lake Storage“, naudodami saitą **Tikrinti „Azure Storage“**.</span><span class="sxs-lookup"><span data-stu-id="78187-129">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="78187-130">Jei tikrinimo rezultatai neigiami, dar kartą patikrinkite, ar visa pirmiau pateikiama KeyVault informacija yra tinkama, tada bandykite dar kartą.</span><span class="sxs-lookup"><span data-stu-id="78187-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="78187-131">Kai ryšis patikrinamas sėkmingai, turite įjungti automatinį objektų saugyklos atnaujinimą.</span><span class="sxs-lookup"><span data-stu-id="78187-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="78187-132">Norėdami įjungti automatinį objektų saugyklos atnaujinimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="78187-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="78187-133">Ieškokite **Objektų saugykla**.</span><span class="sxs-lookup"><span data-stu-id="78187-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="78187-134">Kairėje esančiame sąraše pereikite prie įrašo **RetailSales** ir pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="78187-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="78187-135">Įsitikinkite, kad parinktyje **Automatinis atnaujinimas įjungtas** nustatyta **Taip**, pasirinkite **Atnaujinti**, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="78187-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="78187-136">Toliau pateiktame vaizde parodytas objektų saugyklos pavyzdys, kai automatinis atnaujinimas įjungtas.</span><span class="sxs-lookup"><span data-stu-id="78187-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Objektų saugyklos pavyzdys, kai automatinis atnaujinimas įjungtas](./media/exampleADLSConfig2.png)

<span data-ttu-id="78187-138">Dabar „Azure Data Lake Storage“ sukonfigūruota aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="78187-138">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="78187-139">Jei dar jų neatlikote, atlikite veiksmus, skirtus [įgalinti produkto rekomendacijas ir personalizavimą](enable-product-recommendations.md) aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="78187-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="78187-140">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="78187-140">Additional resources</span></span>

[<span data-ttu-id="78187-141">Leidimas objektų saugyklą naudoti kaip „Data Lake“</span><span class="sxs-lookup"><span data-stu-id="78187-141">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="78187-142">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="78187-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="78187-143">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="78187-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="78187-144">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="78187-144">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="78187-145">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="78187-145">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="78187-146">Įjungti „apsipirkti panašia mada“ rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="78187-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="78187-147">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="78187-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="78187-148">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="78187-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="78187-149">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="78187-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="78187-150">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="78187-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="78187-151">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="78187-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="78187-152">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="78187-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
