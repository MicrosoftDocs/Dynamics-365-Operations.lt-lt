---
title: Pradėti su elektroninės sąskaitos priedo paslaugų administravimu
description: Ši tema paaiškina, kaip pradėti su elektroninės sąskaitos priedo paslaugų administravimu.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592531"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="cbb4f-103">Pradėti su elektroninės sąskaitos priedo paslaugų administravimu</span><span class="sxs-lookup"><span data-stu-id="cbb4f-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="cbb4f-104">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="cbb4f-104">Prerequisites</span></span>

<span data-ttu-id="cbb4f-105">Prieš užbaigdami procedūrą šioje temoje, būtina atlikti tolesnes išankstines sąlygas:</span><span class="sxs-lookup"><span data-stu-id="cbb4f-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="cbb4f-106">Turite turėti savo „Microsoft Dynamics Lifecycle Services“ (LCS) paskyrą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="cbb4f-107">Turite turėti LCS projektą, kuris apima versiją 10.0.17 ar vėlesnę „Microsoft Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="cbb4f-108">Taip pat, šios programos turi būti talpintos vienoje iš tolesnių „Azure“ geografijų:</span><span class="sxs-lookup"><span data-stu-id="cbb4f-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="cbb4f-109">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="cbb4f-109">East US</span></span>
    - <span data-ttu-id="cbb4f-110">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="cbb4f-110">West US</span></span>
    - <span data-ttu-id="cbb4f-111">Šiaurės ES</span><span class="sxs-lookup"><span data-stu-id="cbb4f-111">North EU</span></span>
    - <span data-ttu-id="cbb4f-112">Vakarų ES</span><span class="sxs-lookup"><span data-stu-id="cbb4f-112">West EU</span></span>

- <span data-ttu-id="cbb4f-113">Turite turėti savo „Dynamics 365 Regulatory Configuration Services“ (RCS) paskyrą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="cbb4f-114">Turite aktyvuoti globalizavimo funkciją savo RCS paskyrai funkcijos valdyme.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="cbb4f-115">Dėl daugiau informacijos, žr. [„Regulatory Configuration Services“ (RCS) - globalizavimo funkcijos](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="cbb4f-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="cbb4f-116">Turite sukurti pagrindinę vertę ir laikymo paskyrą „Azure“.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="cbb4f-117">Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir talpyklos raktą](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="cbb4f-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="cbb4f-118">Diekite priedą mikro paslaugoms „Lifecycle Services“</span><span class="sxs-lookup"><span data-stu-id="cbb4f-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="cbb4f-119">Prisijunkite prie jūsų LCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="cbb4f-120">Rinkitės **Išankstinis funkcijos valdymo** plytelę.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="cbb4f-121">Skyriuje **Viešo išankstinio rodymo funkcijos** rinkitės **el. sąskaitų paslaugos**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="cbb4f-122">Įsitikinkite, kad **Išankstinės funkcijos įjungimas** parinktis yra nustatyta į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="cbb4f-123">LCS skelbimų lentoje pasirinkite LCS diegimo projektą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="cbb4f-124">Turi būti vykdomas LCS projektas.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="cbb4f-125">„FastTab“ skirtuke **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="cbb4f-126">Pasirinkite **El. SF paslaugos** ir laukelyje **AAD programos ID** įveskite **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="cbb4f-127">Tai – fiksuota vertė.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-127">This is a fixed value.</span></span>
10. <span data-ttu-id="cbb4f-128">Lauke **AAD nuomotojo ID** įveskite savo „Azure” prenumeratos abonemento savininko ID.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="cbb4f-129">Peržiūrėkite sąlygas ir nuostatas, o tada pažymėkite žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="cbb4f-130">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="cbb4f-131">Nustatykite parametrus RCS integravimui su elektroninės sąskaitos priedu</span><span class="sxs-lookup"><span data-stu-id="cbb4f-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="cbb4f-132">Prisijunkite prie jūsų RCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="cbb4f-133">Darbo srities **Elektroninės ataskaitos** dalyje **Susiję saitai** pasirinkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="cbb4f-134">Skirtuke **el. sąskaitų paslaugos** laukelyje **Paslaugų galinis taškas URI** laukelyje, įveskite paslaugų galinį tašką „Azure“ geogarfijoje kaip parodyta šioje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="cbb4f-135">Duomenų centro „Azure“ geografija</span><span class="sxs-lookup"><span data-stu-id="cbb4f-135">Datacenter Azure geography</span></span> | <span data-ttu-id="cbb4f-136">Paslaugos galinio punkto URI</span><span class="sxs-lookup"><span data-stu-id="cbb4f-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="cbb4f-137">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="cbb4f-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="cbb4f-138">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="cbb4f-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="cbb4f-139">Šiaurės ES</span><span class="sxs-lookup"><span data-stu-id="cbb4f-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="cbb4f-140">Vakarų ES</span><span class="sxs-lookup"><span data-stu-id="cbb4f-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="cbb4f-141">Patvirtinkite, kad **Programos Id** laukelis yra nustatytas į **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="cbb4f-142">Ši vertė yra fiksuota vertė.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="cbb4f-143">Laukelyje **LCS aplinkos Id** įveskite savo LCS prenumeratos sąskaitos ID.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="cbb4f-144">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="cbb4f-145">Kurkite pagrindinį raktą</span><span class="sxs-lookup"><span data-stu-id="cbb4f-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="cbb4f-146">Prisijunkite prie jūsų RCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="cbb4f-147">Darbo srities **Globalizacijos funkcijos** dalyje **Aplinka** pasirinkite plytelę **Elektroninių SF išrašymo priedas**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="cbb4f-148">Puslapyje **Aplinkos nustatymai** veiksmų juostoje rinkitės **Paslaugų aplinka** ir tada rinkitės **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="cbb4f-149">Pasirinkite **Naujas** jei norite sukurti rakto saugyklos slaptą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="cbb4f-150">**Pavadinimas** laukelyje įveskite pagrindinės talpyklos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="cbb4f-151">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="cbb4f-152">Lauke **Rakto talpyklos URI** įklijuokite slaptą kodą iš „Azure Key Vault".</span><span class="sxs-lookup"><span data-stu-id="cbb4f-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="cbb4f-153">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="cbb4f-154">Kurti Saugyklos paskyros raktą</span><span class="sxs-lookup"><span data-stu-id="cbb4f-154">Create Storage account secret</span></span>

1. <span data-ttu-id="cbb4f-155">Eikite į **Sistemos administravimas** > **Sąranka** > **Raktų saugyklos parametrai** ir pasirinkite slaptą raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="cbb4f-156">Skyriuje **Sertifikatai** pasirinkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="cbb4f-157">Laukelyje **Pavadinimas** įveskite slaptos saugyklos paskyros pavadinimą ir laukelyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="cbb4f-158">Lauke **Tipas** pasirinkite **Sertifikatas**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="cbb4f-159">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="cbb4f-160">Slapto skaitmeninio sertifikato kūrimas</span><span class="sxs-lookup"><span data-stu-id="cbb4f-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="cbb4f-161">Eikite į **Sistemos administravimas** > **Sąranka** > **Raktų saugyklos parametrai** ir pasirinkite slaptą raktų saugyklą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="cbb4f-162">Skyriuje **Sertifikatai** pasirinkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="cbb4f-163">Laukelyje **Pavadinimas** įveskite slapto skaitmeninio sertifikato pavadinimą ir laukelyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="cbb4f-164">Lauke **Tipas** pasirinkite **Sertifikatas**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="cbb4f-165">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="cbb4f-166">Elektroninių SF išrašymo priedo aplinkos kūrimas</span><span class="sxs-lookup"><span data-stu-id="cbb4f-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="cbb4f-167">Prisijunkite prie jūsų RCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="cbb4f-168">Darbo srities **Globalizacijos funkcijos** dalyje **Aplinka** pasirinkite plytelę **Elektroninių SF išrašymo priedas**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="cbb4f-169">Aptarnavimo aplinkos kūrimas</span><span class="sxs-lookup"><span data-stu-id="cbb4f-169">Create a service environment</span></span>

1. <span data-ttu-id="cbb4f-170">Puslapyje **Aplinkos nustatymai**, veiksmų juostoje pasirinkite **Aptarnavimo aplinka**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="cbb4f-171">Pasirinkite **Nauja**, kad sukurtumėte naują paslaugų aplinką.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="cbb4f-172">**Pavadinimas** laukelyje įveskite vietos elektroninių sąskaitų aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="cbb4f-173">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="cbb4f-174">**Talpyklos SAS atpažinimo rakto** lauke pasirinkite slaptos saugyklos paskyros, kuri turi būti naudojama, jei norima autentifikuoti prieigą prie saugyklos sąskaitos, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="cbb4f-175">Skyriuje **Vartotojai** rinkitės **Įtraukti** norėdami įtraukti vartotoją, kuriam leidžiama pateikti elektronines SF naudojant aplinką, ir taip pat prisijungti prie saugojimo sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="cbb4f-176">Lauke **Vartotojo ID** įveskite vartotojo pravardę.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="cbb4f-177">Lauke **El. paštas** įveskite vartotojo el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="cbb4f-178">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-178">Select **Save**.</span></span>
8. <span data-ttu-id="cbb4f-179">Jei jūsų šalies ar regiono konkrečios sąskaitos reikalauja sertifikatų grandinės siekiant taikyti skaitmeninį parašą, veiksmų juostoje rinkitės **Pagrindiniai talpyklos parametrai**, tada rinkitės **Sertifikatų grandinė** ir alikite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="cbb4f-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="cbb4f-180">Pasirinkite **Naujas** tam, kad sukurtumėte sertifikatų grandinę.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="cbb4f-181">**Pavadinimas** laukelyje įveskite sertifikato grandinės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="cbb4f-182">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="cbb4f-183">Skyriuje **Sertifikatai** pasirinkite **Įtraukti** kad į grandinę būtų įtrauktas sertifikatas.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="cbb4f-184">Norėdami pakeisti **Aukštyn** arba **Žemyn** poziciją sertifikato grandinėje.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="cbb4f-185">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="cbb4f-186">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-186">Close the page.</span></span>
9. <span data-ttu-id="cbb4f-187">Puslapyje **Paslaugų aplinka** veiksmų juostoje rinkitės **Publikuoti** kad publikuotumėte aplinką debesyje.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="cbb4f-188">Vertė **Būsena** laukelyje pakeičiama į **Publikuota**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="cbb4f-189">Kurkite sujungtą programą</span><span class="sxs-lookup"><span data-stu-id="cbb4f-189">Create a connected application</span></span>

1. <span data-ttu-id="cbb4f-190">**Aplinkos nustatymų** puslapyje, veiksmų juostoje pasirinkite **Sujungtos programos**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="cbb4f-191">Pasirinkite **Naujas**, kad sujungtumėte programą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="cbb4f-192">**Pavadinimas** laukelyje įveskite sujungiamos programos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="cbb4f-193">Laukelyje **Programa** įveskite „Finance and Supply Chain Management“ sujungiamos aplinkos URL.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="cbb4f-194">Laukelyje **Nuomotojo** įveskite „Finance and Supply Chain Management“ nuomotojo aplinką.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="cbb4f-195">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-195">Select **Save**.</span></span>
6. <span data-ttu-id="cbb4f-196">Veiksmų srityje pasirinkite **Tikrinti ryšį** norėdami patikrinti ryšį su aplinka.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="cbb4f-197">Tada uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="cbb4f-198">Susieti prie aplinkos prijungtas programas</span><span class="sxs-lookup"><span data-stu-id="cbb4f-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="cbb4f-199">**Aplinkos nustatymų** puslapyje pasirinkite **Naujas** jei norite aplinkai priskirt prijungtą programą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="cbb4f-200">Laukelyje **Prijungta programa** pasirinkite sujungtą programą.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="cbb4f-201">Lauke **Aptarnavimo aplinka** pasirinkite darbo užsakymo aptarnavimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="cbb4f-202">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="cbb4f-203">Elektroninių SF išrašymo priedo integravimo nustatymas „Finance and Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="cbb4f-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="cbb4f-204">Elektroninių SF išrašymo priedo integravimo funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="cbb4f-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="cbb4f-205">Prisijunkite prie savo „Finance and Supply Chain Management“ elemento.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="cbb4f-206">Darbo srityje **Funkcijų valdymas** ieškokite naujos funkcijos **Elektroninių SF išrašymo priedo integravimas**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="cbb4f-207">Jei ši funkcija nebus rodoma puslapyje, pasirinkite **Tikrinti, ar yra naujinimų**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="cbb4f-208">Pasirinkite funkciją ir tada pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="cbb4f-209">Paslaugos galinio punkto URL nustatymas</span><span class="sxs-lookup"><span data-stu-id="cbb4f-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="cbb4f-210">Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="cbb4f-211">Skirtuke **Pateikimo paslaugos** laukelyje **Aptarnavimo galutinio taško URL** įveskite atitinkamą „Azure" geografijos paslaugos galinį punktą, kaip parodyta pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="cbb4f-212">Duomenų centras „Azure" geografijoje</span><span class="sxs-lookup"><span data-stu-id="cbb4f-212">Datacenter Azure geography</span></span> | <span data-ttu-id="cbb4f-213">Paslaugos galinio punkto URL</span><span class="sxs-lookup"><span data-stu-id="cbb4f-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="cbb4f-214">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="cbb4f-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="cbb4f-215">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="cbb4f-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="cbb4f-216">Šiaurės ES</span><span class="sxs-lookup"><span data-stu-id="cbb4f-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="cbb4f-217">Vakarų ES</span><span class="sxs-lookup"><span data-stu-id="cbb4f-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="cbb4f-218">Laukelyje **Aplinka** įveskite elektroninės sąskaitos priedo aplinką.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="cbb4f-219">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="cbb4f-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
