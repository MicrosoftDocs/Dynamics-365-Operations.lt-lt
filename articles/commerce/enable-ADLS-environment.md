---
title: ADLS įgalinimas „Dynamics 365 Commerce“ aplinkoje
description: Šioje temoje paaiškinama, kaip įjungti ir tikrinti „Azure Data Lake Storage“ (ADLS) „Dynamics 365 Commerce“ aplinkoje. Tai yra būtina sąlyga norint įgalinti produkto rekomendacijas.
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
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ba428765babb9ca7566da7a457368959b1c29083
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259753"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="16826-103">ADLS įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="16826-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="16826-104">Šioje temoje paaiškinama, kaip įjungti ir tikrinti „Azure Data Lake Storage“ (ADLS) „Dynamics 365 Commerce“ aplinkoje. Tai yra būtina sąlyga norint įgalinti produkto rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="16826-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="16826-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="16826-105">Overview</span></span>

<span data-ttu-id="16826-106">Sprendime „Dynamics 365 Commerce“ visų produktų ir operacijų informacija sekama aplinkos objektų saugykloje.</span><span class="sxs-lookup"><span data-stu-id="16826-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="16826-107">Norint, kad šiuos duomenis būtų galima pasiekti naudojant kitas „Dynamics 365“ tarnybas, pvz., duomenų analizę, verslo įžvalgas ir personalizuotas rekomendacijas, reikia sujungti aplinką su klientui priklausančiu sprendimu „Azure Data Lake Storage“ „Gen 2“ (ADLS).</span><span class="sxs-lookup"><span data-stu-id="16826-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="16826-108">Kadangi ADLS konfigūruojamas aplinkoje, visi reikiami objektų saugyklos duomenys yra dubliuojami, apsaugomi ir valdomi kliento.</span><span class="sxs-lookup"><span data-stu-id="16826-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="16826-109">Jei produkto rekomendacijos arba personalizuotos rekomendacijos aplinkoje taip pat įgalintos, produkto rekomendacijų dėklui bus suteikta prieiga prie paskirto aplanko, esančio ADLS, kad būtų galima nuskaityti kliento duomenis ir apskaičiuoti jais pagrįstas rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="16826-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="16826-110">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="16826-110">Prerequisites</span></span>

<span data-ttu-id="16826-111">Klientai turi sukonfigūruoti ADLS jiems priklausančioje „Azure“ prenumeratoje.</span><span class="sxs-lookup"><span data-stu-id="16826-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="16826-112">Šioje temoje neaprašomas „Azure“ prenumeratos pirkimas arba saugyklos abonemento, kuriame įgalintas ADLS, nustatymas.</span><span class="sxs-lookup"><span data-stu-id="16826-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="16826-113">Daugiau informacijos apie ADLS ieškokite [Oficialioje ADLS dokumentacijoje](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="16826-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="16826-114">Konfigūravimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="16826-114">Configuration steps</span></span>

<span data-ttu-id="16826-115">Šiame skyriuje aprašomi konfigūravimo veiksmai, kuriuos reikia atlikti, norint įgalinti ADLS aplinkoje, susijusioje su produktų rekomendacijomis.</span><span class="sxs-lookup"><span data-stu-id="16826-115">This section covers the configuration steps necessary for enabling ADLS in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="16826-116">Išsamesnės informacijos apie veiksmus, reikalingus įgalinti ADLS, žr. [Leidimas objektų saugyklą naudoti kaip „Data Lake“](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="16826-116">For a more in-depth overview of the steps required to enable ADLS, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="16826-117">ADLS įgalinimas aplinkoje</span><span class="sxs-lookup"><span data-stu-id="16826-117">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="16826-118">Prisijunkite prie aplinkos tarnybinio biuro portalo.</span><span class="sxs-lookup"><span data-stu-id="16826-118">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="16826-119">Ieškokite **Sistemos parametrai** ir pereikite į skirtuką **Duomenų ryšiai**.</span><span class="sxs-lookup"><span data-stu-id="16826-119">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="16826-120">Parinktyje **Įjungti „Data Lake“ integraciją** nustatykite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="16826-120">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="16826-121">Parinktyje **Nuolat naujinti „Data Lake“** nustatykite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="16826-121">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="16826-122">Paskui įveskite toliau pateikiamą būtiną informaciją.</span><span class="sxs-lookup"><span data-stu-id="16826-122">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="16826-123">**Programos ID** // **Programos slapta informacija** // **DNS pavadinimas** – reikalinga, jungiantis prie KeyVault, kur saugoma slapta ADLS informacija.</span><span class="sxs-lookup"><span data-stu-id="16826-123">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="16826-124">**Slaptas pavadinimas** – slaptas pavadinimas, saugomas KeyVault ir naudojamas autentifikuojant ADLS.</span><span class="sxs-lookup"><span data-stu-id="16826-124">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="16826-125">Išsaugokite keitimus puslapio viršutiniame kairiajame kampe.</span><span class="sxs-lookup"><span data-stu-id="16826-125">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="16826-126">Toliau pateiktame vaizde parodytas ADLS konfigūracijos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="16826-126">The following image shows an example ADLS configuration.</span></span>

![ADLS konfigūracijos pavyzdys](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="16826-128">ADLS ryšio tikrinimas</span><span class="sxs-lookup"><span data-stu-id="16826-128">Test the ADLS connection</span></span>

1. <span data-ttu-id="16826-129">Patikrinkite ryšį su KeyVault, naudodami saitą **Tikrinti „Azure Key Vault“**.</span><span class="sxs-lookup"><span data-stu-id="16826-129">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="16826-130">Patikrinkite ryšį su ADLS, naudodami saitą **Tikrinti „Azure Storage“**.</span><span class="sxs-lookup"><span data-stu-id="16826-130">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="16826-131">Jei tikrinimo rezultatai neigiami, dar kartą patikrinkite, ar visa pirmiau pateikiama KeyVault informacija yra tinkama, tada bandykite dar kartą.</span><span class="sxs-lookup"><span data-stu-id="16826-131">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="16826-132">Kai ryšis patikrinamas sėkmingai, turite įjungti automatinį objektų saugyklos atnaujinimą.</span><span class="sxs-lookup"><span data-stu-id="16826-132">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="16826-133">Norėdami įjungti automatinį objektų saugyklos atnaujinimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="16826-133">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="16826-134">Ieškokite **Objektų saugykla**.</span><span class="sxs-lookup"><span data-stu-id="16826-134">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="16826-135">Kairėje esančiame sąraše pereikite prie įrašo **RetailSales** ir pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="16826-135">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="16826-136">Įsitikinkite, kad parinktyje **Automatinis atnaujinimas įjungtas** nustatyta **Taip**, pasirinkite **Atnaujinti**, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="16826-136">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="16826-137">Toliau pateiktame vaizde parodytas objektų saugyklos pavyzdys, kai automatinis atnaujinimas įjungtas.</span><span class="sxs-lookup"><span data-stu-id="16826-137">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Objektų saugyklos pavyzdys, kai automatinis atnaujinimas įjungtas](./media/exampleADLSConfig2.png)

<span data-ttu-id="16826-139">Dabar ADLS aplinkoje sukonfigūruotas.</span><span class="sxs-lookup"><span data-stu-id="16826-139">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="16826-140">Jei dar jų neatlikote, atlikite veiksmus, skirtus [įgalinti produkto rekomendacijas ir personalizavimą](enable-product-recommendations.md) aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="16826-140">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16826-141">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="16826-141">Additional resources</span></span>

[<span data-ttu-id="16826-142">Leidimas objektų saugyklą naudoti kaip „Data Lake“</span><span class="sxs-lookup"><span data-stu-id="16826-142">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="16826-143">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="16826-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="16826-144">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="16826-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="16826-145">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="16826-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="16826-146">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="16826-146">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="16826-147">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="16826-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="16826-148">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="16826-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="16826-149">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="16826-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="16826-150">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="16826-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="16826-151">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="16826-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="16826-152">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="16826-152">Product recommendations FAQ</span></span>](faq-recommendations.md)
