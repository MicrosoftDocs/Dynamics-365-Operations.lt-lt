---
title: Pradėti su elektroninės sąskaitos priedo paslaugų administravimu
description: Ši tema paaiškina, kaip pradėti su elektroninės sąskaitos priedo paslaugų administravimu.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104413"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="11916-103">Pradėti su elektroninės sąskaitos priedo paslaugų administravimu</span><span class="sxs-lookup"><span data-stu-id="11916-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="11916-104">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="11916-104">Prerequisites</span></span>

<span data-ttu-id="11916-105">Prieš užbaigdami procedūrą šioje temoje, būtina atlikti tolesnes išankstines sąlygas:</span><span class="sxs-lookup"><span data-stu-id="11916-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="11916-106">Turite turėti savo „Microsoft Dynamics Lifecycle Services“ (LCS) paskyrą.</span><span class="sxs-lookup"><span data-stu-id="11916-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="11916-107">Turite turėti LCS projektą, kuris apima versiją 10.0.13 ar vėlesnę „Microsoft Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="11916-107">You must have an LCS project that includes version 10.0.13 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="11916-108">Taip pat, šios programos turi būti talpintos vienoje iš tolesnių „Azure“ geografijų:</span><span class="sxs-lookup"><span data-stu-id="11916-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="11916-109">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="11916-109">East US</span></span>
    - <span data-ttu-id="11916-110">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="11916-110">West US</span></span>
    - <span data-ttu-id="11916-111">Šiaurės ES</span><span class="sxs-lookup"><span data-stu-id="11916-111">North EU</span></span>
    - <span data-ttu-id="11916-112">Vakarų ES</span><span class="sxs-lookup"><span data-stu-id="11916-112">West EU</span></span>

- <span data-ttu-id="11916-113">Turite turėti savo „Dynamics 365 Regulatory Configuration Services“ (RCS) paskyrą.</span><span class="sxs-lookup"><span data-stu-id="11916-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="11916-114">Turite aktyvuoti globalizavimo funkciją savo RCS paskyrai funkcijos valdyme.</span><span class="sxs-lookup"><span data-stu-id="11916-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="11916-115">Dėl daugiau informacijos, žr. [„Regulatory Configuration Services“ (RCS) - globalizavimo funkcijos](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="11916-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="11916-116">Turite sukurti pagrindinę vertę ir laikymo paskyrą „Azure“.</span><span class="sxs-lookup"><span data-stu-id="11916-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="11916-117">Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir talpyklos raktą](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="11916-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="11916-118">Diekite priedą mikro paslaugoms „Lifecycle Services“</span><span class="sxs-lookup"><span data-stu-id="11916-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="11916-119">Prisijunkite prie jūsų LCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="11916-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="11916-120">Rinkitės **Išankstinis funkcijos valdymo** plytelę.</span><span class="sxs-lookup"><span data-stu-id="11916-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="11916-121">Skyriuje **Viešo išankstinio rodymo funkcijos** rinkitės **el. sąskaitų paslaugos**.</span><span class="sxs-lookup"><span data-stu-id="11916-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="11916-122">Įsitikinkite, kad **Išankstinės funkcijos įjungimas** parinktis yra nustatyta į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="11916-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="11916-123">Nustatykite parametrus RCS integravimui su elektroninės sąskaitos priedu</span><span class="sxs-lookup"><span data-stu-id="11916-123">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="11916-124">Prisijunkite prie jūsų RCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="11916-124">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="11916-125">Darbo srities **Elektroninės ataskaitos** dalyje **Susiję saitai** pasirinkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="11916-125">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="11916-126">Skirtuke **el. sąskaitų paslaugos** laukelyje **Paslaugų galinis taškas URI** laukelyje, įveskite paslaugų galinį tašką „Azure“ geogarfijoje kaip parodyta šioje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="11916-126">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="11916-127">Duomenų centro „Azure“ geografija</span><span class="sxs-lookup"><span data-stu-id="11916-127">Datacenter Azure geography</span></span> | <span data-ttu-id="11916-128">Paslaugos galinio punkto URI</span><span class="sxs-lookup"><span data-stu-id="11916-128">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="11916-129">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="11916-129">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="11916-130">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="11916-130">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="11916-131">Šiaurės ES</span><span class="sxs-lookup"><span data-stu-id="11916-131">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="11916-132">Vakarų ES</span><span class="sxs-lookup"><span data-stu-id="11916-132">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="11916-133">Patvirtinkite, kad **Programos Id** laukelis yra nustatytas į **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="11916-133">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="11916-134">Ši vertė yra fiksuota vertė.</span><span class="sxs-lookup"><span data-stu-id="11916-134">This value is a fixed value.</span></span>
5. <span data-ttu-id="11916-135">Laukelyje **LCS aplinkos Id** įveskite savo LCS prenumeratos sąskaitos ID.</span><span class="sxs-lookup"><span data-stu-id="11916-135">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="11916-136">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="11916-136">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="11916-137">Kurkite pagrindinį raktą</span><span class="sxs-lookup"><span data-stu-id="11916-137">Create Key Vault secret</span></span>

1. <span data-ttu-id="11916-138">Prisijunkite prie jūsų RCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="11916-138">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="11916-139">Darbo srityje **Globalizavimo funkcija** rinkitės **Aplinka** skyriuje rinkitės **E-sąskaitos** pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="11916-139">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="11916-140">Puslapyje **Aplinkos nustatymai** veiksmų juostoje rinkitės **Paslaugų aplinka** ir tada rinkitės **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="11916-140">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="11916-141">Pasirinkite **Naujas** jei norite sukurti rakto saugyklos slaptą.</span><span class="sxs-lookup"><span data-stu-id="11916-141">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="11916-142">**Pavadinimas** laukelyje įveskite pagrindinės talpyklos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="11916-142">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="11916-143">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="11916-143">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="11916-144">Lauke **Rakto talpyklos URI** įklijuokite slaptą kodą iš „Azure Key Vault".</span><span class="sxs-lookup"><span data-stu-id="11916-144">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="11916-145">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="11916-145">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="11916-146">Kurti Saugyklos paskyros raktą</span><span class="sxs-lookup"><span data-stu-id="11916-146">Create Storage account secret</span></span>

1. <span data-ttu-id="11916-147">**Rakto saugyklos parametrų** puslapyje, skyriuje **Sertifikatai** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="11916-147">On **Key vault parameters** page, in the **Certificates** section, select **Add**.</span></span>
2. <span data-ttu-id="11916-148">**Pavadinimas** laukelyje įveskite tą patį talpyklos paskyros raktą.</span><span class="sxs-lookup"><span data-stu-id="11916-148">In the **Name** field, enter the same of the storage account secret.</span></span> <span data-ttu-id="11916-149">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="11916-149">In the **Description** field, enter a description.</span></span>
3. <span data-ttu-id="11916-150">Lauke **Tipas** pasirinkite **Sertifikatas**.</span><span class="sxs-lookup"><span data-stu-id="11916-150">In the **Type** field, select **Certificate**.</span></span>
4. <span data-ttu-id="11916-151">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="11916-151">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="11916-152">Elektroninių SF išrašymo priedo aplinkos kūrimas</span><span class="sxs-lookup"><span data-stu-id="11916-152">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="11916-153">Prisijunkite prie jūsų RCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="11916-153">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="11916-154">Darbo srityje **Globalizavimo funkcija** rinkitės **Aplinka** skyriuje rinkitės **E-sąskaitos** pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="11916-154">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="11916-155">Aptarnavimo aplinkos kūrimas</span><span class="sxs-lookup"><span data-stu-id="11916-155">Create a service environment</span></span>

1. <span data-ttu-id="11916-156">**Aplinkos nustatymų** puslapyje, veiksmų juostoje pasirinkite **Aptarnavimo aplinka**.</span><span class="sxs-lookup"><span data-stu-id="11916-156">On the **Environment setups** page, on the action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="11916-157">Pasirinkite **Nauja**, kad sukurtumėte naują paslaugų aplinką.</span><span class="sxs-lookup"><span data-stu-id="11916-157">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="11916-158">**Pavadinimas** laukelyje įveskite vietos elektroninių sąskaitų aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="11916-158">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="11916-159">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="11916-159">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="11916-160">**Talpyklos SAS atpažinimo rakto** lauke pasirinkite sertifikato, kuris turi būti naudojamas, jei norima autentifikuoti prieigą prie saugyklos sąskaitos, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="11916-160">In the **Storage SAS token secret** field, select the name of the certificate that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="11916-161">Skyriuje **Vartotojai** rinkitės **Įtraukti** norėdami įtraukti vartotoją, kuriam leidžiama pateikti elektronines SF naudojant aplinką, ir taip pat prisijungti prie saugojimo sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="11916-161">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="11916-162">Lauke **Vartotojo ID** įveskite vartotojo pravardę.</span><span class="sxs-lookup"><span data-stu-id="11916-162">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="11916-163">Lauke **El. paštas** įveskite vartotojo el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="11916-163">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="11916-164">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="11916-164">Select **Save**.</span></span>
8. <span data-ttu-id="11916-165">Jei jūsų šalies ar regiono konkrečios sąskaitos reikalauja sertifikatų grandinės siekiant taikyti skaitmeninį parašą, veiksmų juostoje rinkitės **Pagrindiniai talpyklos parametrai**, tada rinkitės **Sertifikatų grandinė** ir alikite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="11916-165">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="11916-166">Pasirinkite **Naujas** tam, kad sukurtumėte sertifikatų grandinę.</span><span class="sxs-lookup"><span data-stu-id="11916-166">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="11916-167">**Pavadinimas** laukelyje įveskite sertifikato grandinės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="11916-167">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="11916-168">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="11916-168">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="11916-169">Skyriuje **Sertifikatai** pasirinkite **Įtraukti** kad į grandinę būtų įtrauktas sertifikatas.</span><span class="sxs-lookup"><span data-stu-id="11916-169">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="11916-170">Norėdami pakeisti **Aukštyn** arba **Žemyn** poziciją sertifikato grandinėje.</span><span class="sxs-lookup"><span data-stu-id="11916-170">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="11916-171">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="11916-171">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="11916-172">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="11916-172">Close the page.</span></span>
9. <span data-ttu-id="11916-173">Puslapyje **Paslaugų aplinka** veiksmų juostoje rinkitės **Publikuoti** kad publikuotumėte aplinką debesyje.</span><span class="sxs-lookup"><span data-stu-id="11916-173">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="11916-174">Vertė **Būsena** laukelyje pakeičiama į **Publikuota**.</span><span class="sxs-lookup"><span data-stu-id="11916-174">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="11916-175">Kurkite sujungtą programą</span><span class="sxs-lookup"><span data-stu-id="11916-175">Create a connected application</span></span>

1. <span data-ttu-id="11916-176">**Aplinkos nustatymų** puslapyje, veiksmų juostoje pasirinkite **Sujungtos programos**.</span><span class="sxs-lookup"><span data-stu-id="11916-176">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="11916-177">Pasirinkite **Naujas**, kad sujungtumėte programą.</span><span class="sxs-lookup"><span data-stu-id="11916-177">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="11916-178">**Pavadinimas** laukelyje įveskite sujungiamos programos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="11916-178">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="11916-179">Laukelyje **Programa** įveskite „Finance and Supply Chain Management“ sujungiamos aplinkos URL.</span><span class="sxs-lookup"><span data-stu-id="11916-179">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="11916-180">Laukelyje **Nuomotojo** įveskite „Finance and Supply Chain Management“ nuomotojo aplinką.</span><span class="sxs-lookup"><span data-stu-id="11916-180">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="11916-181">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="11916-181">Select **Save**.</span></span>
6. <span data-ttu-id="11916-182">Veiksmų srityje pasirinkite **Tikrinti ryšį** norėdami patikrinti ryšį su aplinka.</span><span class="sxs-lookup"><span data-stu-id="11916-182">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="11916-183">Tada uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="11916-183">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="11916-184">Susieti prie aplinkos prijungtas programas</span><span class="sxs-lookup"><span data-stu-id="11916-184">Link connected applications to environments</span></span>

1. <span data-ttu-id="11916-185">**Aplinkos nustatymų** puslapyje pasirinkite **Naujas** jei norite aplinkai priskirt prijungtą programą.</span><span class="sxs-lookup"><span data-stu-id="11916-185">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="11916-186">Laukelyje **Prijungta programa** pasirinkite sujungtą programą.</span><span class="sxs-lookup"><span data-stu-id="11916-186">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="11916-187">Lauke **Aptarnavimo aplinka** pasirinkite darbo užsakymo aptarnavimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="11916-187">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="11916-188">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="11916-188">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="11916-189">Elektroninių SF išrašymo priedo integravimo nustatymas „Finance and Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="11916-189">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="11916-190">Elektroninių SF išrašymo priedo integravimo funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="11916-190">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="11916-191">Prisijunkite prie savo „Finance and Supply Chain Management“ elemento.</span><span class="sxs-lookup"><span data-stu-id="11916-191">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="11916-192">Darbo srityje **Funkcijų valdymas** ieškokite naujos funkcijos **Elektroninių SF išrašymo priedo integravimas**.</span><span class="sxs-lookup"><span data-stu-id="11916-192">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="11916-193">Jei ši funkcija nebus rodoma puslapyje, pasirinkite **Tikrinti, ar yra naujinimų**.</span><span class="sxs-lookup"><span data-stu-id="11916-193">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="11916-194">Pasirinkite funkciją ir tada pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="11916-194">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="11916-195">Paslaugos galinio punkto URL nustatymas</span><span class="sxs-lookup"><span data-stu-id="11916-195">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="11916-196">Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="11916-196">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="11916-197">Skirtuke **Pateikimo paslaugos** laukelyje **Aptarnavimo galutinio taško URL** įveskite atitinkamą „Azure" geografijos paslaugos galinį punktą, kaip parodyta pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="11916-197">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="11916-198">Duomenų centras „Azure" geografijoje</span><span class="sxs-lookup"><span data-stu-id="11916-198">Datacenter Azure geography</span></span> | <span data-ttu-id="11916-199">Paslaugos galinio punkto URL</span><span class="sxs-lookup"><span data-stu-id="11916-199">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="11916-200">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="11916-200">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="11916-201">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="11916-201">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="11916-202">Šiaurės ES</span><span class="sxs-lookup"><span data-stu-id="11916-202">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="11916-203">Vakarų ES</span><span class="sxs-lookup"><span data-stu-id="11916-203">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="11916-204">Laukelyje **Aplinka** įveskite elektroninės sąskaitos priedo aplinką.</span><span class="sxs-lookup"><span data-stu-id="11916-204">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="11916-205">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="11916-205">Select **Save**, and then close the page.</span></span>
