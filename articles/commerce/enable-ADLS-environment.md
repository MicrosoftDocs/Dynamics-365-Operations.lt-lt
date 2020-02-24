---
title: ADLS įgalinimas „Dynamics 365 Commerce“ aplinkoje
description: Šioje temoje paaiškinama, kaip įjungti ir tikrinti „Azure Data Lake Storage“ (ADLS) „Dynamics 365 Commerce“ aplinkoje. Tai yra būtina sąlyga norint įgalinti produkto rekomendacijas.
author: bebeale
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 068eb522bd44e02dd31d3337a051691a956637fc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025266"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="b47e9-103">ADLS įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="b47e9-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b47e9-104">Šioje temoje paaiškinama, kaip įjungti ir tikrinti „Azure Data Lake Storage“ (ADLS) „Dynamics 365 Commerce“ aplinkoje. Tai yra būtina sąlyga norint įgalinti produkto rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="b47e9-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="b47e9-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="b47e9-105">Overview</span></span>

<span data-ttu-id="b47e9-106">Sprendime „Dynamics 365 Commerce“ visų produktų ir operacijų informacija sekama aplinkos objektų saugykloje.</span><span class="sxs-lookup"><span data-stu-id="b47e9-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="b47e9-107">Norint, kad šiuos duomenis būtų galima pasiekti naudojant kitas „Dynamics 365“ tarnybas, pvz., duomenų analizę, verslo įžvalgas ir personalizuotas rekomendacijas, reikia sujungti aplinką su klientui priklausančiu sprendimu „Azure Data Lake Storage“ „Gen 2“ (ADLS).</span><span class="sxs-lookup"><span data-stu-id="b47e9-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="b47e9-108">Kadangi ADLS konfigūruojamas aplinkoje, visi reikiami objektų saugyklos duomenys yra dubliuojami, apsaugomi ir valdomi kliento.</span><span class="sxs-lookup"><span data-stu-id="b47e9-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="b47e9-109">Jei produkto rekomendacijos arba personalizuotos rekomendacijos aplinkoje taip pat įgalintos, produkto rekomendacijų dėklui bus suteikta prieiga prie paskirto aplanko, esančio ADLS, kad būtų galima nuskaityti kliento duomenis ir apskaičiuoti jais pagrįstas rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="b47e9-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b47e9-110">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="b47e9-110">Prerequisites</span></span>

<span data-ttu-id="b47e9-111">Klientai turi sukonfigūruoti ADLS jiems priklausančioje „Azure“ prenumeratoje.</span><span class="sxs-lookup"><span data-stu-id="b47e9-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="b47e9-112">Šioje temoje neaprašomas „Azure“ prenumeratos pirkimas arba saugyklos abonemento, kuriame įgalintas ADLS, nustatymas.</span><span class="sxs-lookup"><span data-stu-id="b47e9-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="b47e9-113">Daugiau informacijos apie ADLS ieškokite [Oficialioje ADLS dokumentacijoje](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="b47e9-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="b47e9-114">Konfigūravimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="b47e9-114">Configuration steps</span></span>

<span data-ttu-id="b47e9-115">Šiame skyriuje aprašomi konfigūravimo veiksmai, kuriuos reikia atlikti, norint įgalinti ADLS aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="b47e9-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="b47e9-116">ADLS įgalinimas aplinkoje</span><span class="sxs-lookup"><span data-stu-id="b47e9-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="b47e9-117">Prisijunkite prie aplinkos tarnybinio biuro portalo.</span><span class="sxs-lookup"><span data-stu-id="b47e9-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="b47e9-118">Ieškokite **Sistemos parametrai** ir pereikite į skirtuką **Duomenų ryšiai**.</span><span class="sxs-lookup"><span data-stu-id="b47e9-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="b47e9-119">Parinktyje **Įjungti „Data Lake“ integraciją** nustatykite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b47e9-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="b47e9-120">Parinktyje **Nuolat naujinti „Data Lake“** nustatykite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b47e9-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="b47e9-121">Paskui įveskite toliau pateikiamą būtiną informaciją.</span><span class="sxs-lookup"><span data-stu-id="b47e9-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="b47e9-122">**Programos ID** // **Programos slapta informacija** // **DNS pavadinimas** – reikalinga, jungiantis prie KeyVault, kur saugoma slapta ADLS informacija.</span><span class="sxs-lookup"><span data-stu-id="b47e9-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="b47e9-123">**Slaptas pavadinimas** – slaptas pavadinimas, saugomas KeyVault ir naudojamas autentifikuojant ADLS.</span><span class="sxs-lookup"><span data-stu-id="b47e9-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="b47e9-124">Išsaugokite keitimus puslapio viršutiniame kairiajame kampe.</span><span class="sxs-lookup"><span data-stu-id="b47e9-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="b47e9-125">Toliau pateiktame vaizde parodytas ADLS konfigūracijos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="b47e9-125">The following image shows an example ADLS configuration.</span></span>

![ADLS konfigūracijos pavyzdys](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="b47e9-127">ADLS ryšio tikrinimas</span><span class="sxs-lookup"><span data-stu-id="b47e9-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="b47e9-128">Patikrinkite ryšį su KeyVault, naudodami saitą **Tikrinti „Azure Key Vault“**.</span><span class="sxs-lookup"><span data-stu-id="b47e9-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="b47e9-129">Patikrinkite ryšį su ADLS, naudodami saitą **Tikrinti „Azure Storage“**.</span><span class="sxs-lookup"><span data-stu-id="b47e9-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="b47e9-130">Jei tikrinimo rezultatai neigiami, dar kartą patikrinkite, ar visa pirmiau pateikiama KeyVault informacija yra tinkama, tada bandykite dar kartą.</span><span class="sxs-lookup"><span data-stu-id="b47e9-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="b47e9-131">Kai ryšis patikrinamas sėkmingai, turite įjungti automatinį objektų saugyklos atnaujinimą.</span><span class="sxs-lookup"><span data-stu-id="b47e9-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="b47e9-132">Norėdami įjungti automatinį objektų saugyklos atnaujinimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b47e9-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="b47e9-133">Ieškokite **Objektų saugykla**.</span><span class="sxs-lookup"><span data-stu-id="b47e9-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="b47e9-134">Kairėje esančiame sąraše pereikite prie įrašo **RetailSales** ir pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="b47e9-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="b47e9-135">Įsitikinkite, kad parinktyje **Automatinis atnaujinimas įjungtas** nustatyta **Taip**, pasirinkite **Atnaujinti**, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b47e9-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="b47e9-136">Toliau pateiktame vaizde parodytas objektų saugyklos pavyzdys, kai automatinis atnaujinimas įjungtas.</span><span class="sxs-lookup"><span data-stu-id="b47e9-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Objektų saugyklos pavyzdys, kai automatinis atnaujinimas įjungtas](./media/exampleADLSConfig2.png)

<span data-ttu-id="b47e9-138">Dabar ADLS aplinkoje sukonfigūruotas.</span><span class="sxs-lookup"><span data-stu-id="b47e9-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="b47e9-139">Jei dar jų neatlikote, atlikite veiksmus, skirtus [įgalinti produkto rekomendacijas ir personalizavimą](enable-product-recommendations.md) aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="b47e9-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b47e9-140">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b47e9-140">Additional resources</span></span>

[<span data-ttu-id="b47e9-141">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="b47e9-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b47e9-142">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="b47e9-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="b47e9-143">ĮProduktų rekomendacijų sąrašų įtraukimas į puslapius</span><span class="sxs-lookup"><span data-stu-id="b47e9-143">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="b47e9-144">Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="b47e9-144">Add a recommendations control to the transaction screen on POS devices</span></span>](../retail/add-recommendations-control-pos-screen.md?toc=/dynamics365/commerce/toc.json)


