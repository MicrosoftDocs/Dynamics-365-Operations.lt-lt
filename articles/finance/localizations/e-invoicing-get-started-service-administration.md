---
title: Darbo su elektroninių SF priedu tarnybos administravimui pradžia
description: Ši tema paaiškina, kaip pradėti su elektroninės sąskaitos priedo paslaugų administravimu.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840153"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="30da6-103">Darbo su elektroninių SF priedu tarnybos administravimui pradžia</span><span class="sxs-lookup"><span data-stu-id="30da6-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="30da6-104">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="30da6-104">Prerequisites</span></span>

<span data-ttu-id="30da6-105">Prieš užbaigdami procedūrą šioje temoje, būtina atlikti tolesnes išankstines sąlygas:</span><span class="sxs-lookup"><span data-stu-id="30da6-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="30da6-106">Turite turėti savo „Microsoft Dynamics Lifecycle Services“ (LCS) paskyrą.</span><span class="sxs-lookup"><span data-stu-id="30da6-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="30da6-107">Turite turėti LCS projektą, kuris apima versiją 10.0.17 ar vėlesnę „Microsoft Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="30da6-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="30da6-108">Taip pat, šios programos turi būti talpintos vienoje iš tolesnių „Azure“ geografijų:</span><span class="sxs-lookup"><span data-stu-id="30da6-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="30da6-109">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="30da6-109">East US</span></span>
    - <span data-ttu-id="30da6-110">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="30da6-110">West US</span></span>
    - <span data-ttu-id="30da6-111">Šiaurės ES</span><span class="sxs-lookup"><span data-stu-id="30da6-111">North EU</span></span>
    - <span data-ttu-id="30da6-112">Vakarų ES</span><span class="sxs-lookup"><span data-stu-id="30da6-112">West EU</span></span>

- <span data-ttu-id="30da6-113">Turite turėti savo „Dynamics 365 Regulatory Configuration Services“ (RCS) paskyrą.</span><span class="sxs-lookup"><span data-stu-id="30da6-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="30da6-114">Turite aktyvuoti globalizavimo funkciją savo RCS paskyrai funkcijos valdyme.</span><span class="sxs-lookup"><span data-stu-id="30da6-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="30da6-115">Dėl daugiau informacijos, žr. [„Regulatory Configuration Services“ (RCS) - globalizavimo funkcijos](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="30da6-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="30da6-116">Turite sukurti pagrindinę vertę ir laikymo paskyrą „Azure“.</span><span class="sxs-lookup"><span data-stu-id="30da6-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="30da6-117">Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir talpyklos raktą](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="30da6-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="30da6-118">Diekite priedą mikro paslaugoms „Lifecycle Services“</span><span class="sxs-lookup"><span data-stu-id="30da6-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="30da6-119">Prisijunkite prie jūsų LCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="30da6-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="30da6-120">Rinkitės **Išankstinis funkcijos valdymo** plytelę.</span><span class="sxs-lookup"><span data-stu-id="30da6-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="30da6-121">Skyriuje **Viešo išankstinio rodymo funkcijos** rinkitės **el. sąskaitų paslaugos**.</span><span class="sxs-lookup"><span data-stu-id="30da6-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="30da6-122">Įsitikinkite, kad **Išankstinės funkcijos įjungimas** parinktis yra nustatyta į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="30da6-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="30da6-123">LCS skelbimų lentoje pasirinkite LCS diegimo projektą.</span><span class="sxs-lookup"><span data-stu-id="30da6-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="30da6-124">Turi būti vykdomas LCS projektas.</span><span class="sxs-lookup"><span data-stu-id="30da6-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="30da6-125">„FastTab“ skirtuke **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="30da6-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="30da6-126">Pasirinkite **el. SF išrašymo** paslaugas.</span><span class="sxs-lookup"><span data-stu-id="30da6-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="30da6-127">Lauke **AAD programos ID** įveskite **„091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="30da6-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="30da6-128">Tai – fiksuota vertė.</span><span class="sxs-lookup"><span data-stu-id="30da6-128">This is a fixed value.</span></span>
10. <span data-ttu-id="30da6-129">Lauke **AAD nuomotojo ID** įveskite savo „Azure” prenumeratos abonemento savininko ID.</span><span class="sxs-lookup"><span data-stu-id="30da6-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="30da6-130">Peržiūrėkite sąlygas ir nuostatas, o tada pažymėkite žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="30da6-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="30da6-131">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="30da6-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="30da6-132">Nustatykite parametrus RCS integravimui su elektroninės sąskaitos priedu</span><span class="sxs-lookup"><span data-stu-id="30da6-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="30da6-133">Prisijunkite prie jūsų RCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="30da6-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="30da6-134">Darbo srities **Elektroninės ataskaitos** dalyje **Susiję saitai** pasirinkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="30da6-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="30da6-135">Skirtuke **el. sąskaitų paslaugos** laukelyje **Paslaugų galinis taškas URI** laukelyje, įveskite paslaugų galinį tašką „Azure“ geogarfijoje kaip parodyta šioje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="30da6-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="30da6-136">Duomenų centro „Azure“ geografija</span><span class="sxs-lookup"><span data-stu-id="30da6-136">Datacenter Azure geography</span></span> | <span data-ttu-id="30da6-137">Paslaugos galinio punkto URI</span><span class="sxs-lookup"><span data-stu-id="30da6-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="30da6-138">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="30da6-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="30da6-139">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="30da6-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="30da6-140">Šiaurės ES</span><span class="sxs-lookup"><span data-stu-id="30da6-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="30da6-141">Vakarų ES</span><span class="sxs-lookup"><span data-stu-id="30da6-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="30da6-142">Patvirtinkite, kad **Programos Id** laukelis yra nustatytas į **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="30da6-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="30da6-143">Ši vertė yra fiksuota vertė.</span><span class="sxs-lookup"><span data-stu-id="30da6-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="30da6-144">Laukelyje **LCS aplinkos Id** įveskite savo aplinkos LCS prenumeratos ID.</span><span class="sxs-lookup"><span data-stu-id="30da6-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="30da6-145">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="30da6-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="30da6-146">Raktų saugyklos nuorodų kūrimas</span><span class="sxs-lookup"><span data-stu-id="30da6-146">Create Key Vault references</span></span>

1. <span data-ttu-id="30da6-147">Prisijunkite prie jūsų RCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="30da6-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="30da6-148">Darbo srities **Globalizacijos funkcijos** dalyje **Aplinka** pasirinkite plytelę **Elektroninių SF išrašymo priedas**.</span><span class="sxs-lookup"><span data-stu-id="30da6-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="30da6-149">Puslapyje **Aplinkos nustatymai** veiksmų juostoje rinkitės **Paslaugų aplinka** ir tada rinkitės **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="30da6-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="30da6-150">Pasirinkite **Naujas** jei norite sukurti rakto saugyklos nuorodą.</span><span class="sxs-lookup"><span data-stu-id="30da6-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="30da6-151">**Pavadinimas** laukelyje įveskite pagrindinės talpyklos nuorodą.</span><span class="sxs-lookup"><span data-stu-id="30da6-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="30da6-152">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="30da6-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="30da6-153">Lauke **Rakto talpyklos URI** įklijuokite slaptą nuorodos saugyklą iš „Azure Key Vault".</span><span class="sxs-lookup"><span data-stu-id="30da6-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="30da6-154">Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir talpyklos raktą](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="30da6-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="30da6-155">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="30da6-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="30da6-156">Kurti Saugyklos paskyros raktą</span><span class="sxs-lookup"><span data-stu-id="30da6-156">Create Storage account secret</span></span>

1. <span data-ttu-id="30da6-157">Puslapyje **Aplinkos nustatymai** veiksmų juostoje rinkitės **Paslaugų aplinka** > **Pagrindiniai raktų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="30da6-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="30da6-158">Pasirinkite rakto **Saugyklos nuorodą** ir skyriuje  **Sertifikatai** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="30da6-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="30da6-159">**Pavadinimas** laukelyje įveskite tą patį talpyklos paskyros pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="30da6-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="30da6-160">Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir talpyklos raktą](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="30da6-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="30da6-161">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="30da6-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="30da6-162">Lauke **Tipas** pasirinkite **Raktas**.</span><span class="sxs-lookup"><span data-stu-id="30da6-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="30da6-163">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="30da6-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="30da6-164">Slapto skaitmeninio sertifikato kūrimas</span><span class="sxs-lookup"><span data-stu-id="30da6-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="30da6-165">Puslapyje **Aplinkos nustatymai** veiksmų juostoje rinkitės **Paslaugų aplinka** ir tada rinkitės **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="30da6-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="30da6-166">Pasirinkite rakto **Saugyklos nuorodą** ir tada skyriuje  **Sertifikatai** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="30da6-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="30da6-167">**Pavadinimas** laukelyje įveskite tą patį skaitmeninį sertifikato raktą.</span><span class="sxs-lookup"><span data-stu-id="30da6-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="30da6-168">Daugiau informacijos žr. [Kurti „Azure” saugyklos paskyrą ir talpyklos raktą](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="30da6-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="30da6-169">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="30da6-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="30da6-170">Lauke **Tipas** pasirinkite **Sertifikatas**.</span><span class="sxs-lookup"><span data-stu-id="30da6-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="30da6-171">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="30da6-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="30da6-172">Aptarnavimo aplinkos kūrimas</span><span class="sxs-lookup"><span data-stu-id="30da6-172">Create a service environment</span></span>

1. <span data-ttu-id="30da6-173">Prisijunkite prie jūsų RCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="30da6-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="30da6-174">Darbo srities **Globalizacijos funkcijos** dalyje **Aplinka** pasirinkite plytelę **Elektroninių SF išrašymo priedas**.</span><span class="sxs-lookup"><span data-stu-id="30da6-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="30da6-175">Puslapyje **Aplinkos nustatymai**, veiksmų juostoje pasirinkite **Aptarnavimo aplinka**.</span><span class="sxs-lookup"><span data-stu-id="30da6-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="30da6-176">Pasirinkite **Nauja**, kad sukurtumėte naują paslaugų aplinką.</span><span class="sxs-lookup"><span data-stu-id="30da6-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="30da6-177">**Pavadinimas** laukelyje įveskite vietos elektroninių sąskaitų aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="30da6-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="30da6-178">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="30da6-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="30da6-179">**Talpyklos SAS atpažinimo rakto** lauke pasirinkite slaptos saugyklos paskyros, kuri turi būti naudojama, jei norima autentifikuoti prieigą prie saugyklos sąskaitos, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="30da6-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="30da6-180">Skyriuje **Vartotojai** rinkitės **Įtraukti** norėdami įtraukti vartotoją, kuriam leidžiama pateikti elektronines SF naudojant aplinką, ir taip pat prisijungti prie saugojimo sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="30da6-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="30da6-181">Lauke **Vartotojo ID** įveskite vartotojo pravardę.</span><span class="sxs-lookup"><span data-stu-id="30da6-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="30da6-182">Lauke **El. paštas** įveskite vartotojo el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="30da6-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="30da6-183">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="30da6-183">Select **Save**.</span></span>
10. <span data-ttu-id="30da6-184">Jei jūsų šalies ar regiono konkrečios sąskaitos reikalauja sertifikatų grandinės siekiant taikyti skaitmeninį parašą, veiksmų juostoje rinkitės **Pagrindiniai talpyklos parametrai**, tada rinkitės **Sertifikatų grandinė** ir alikite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="30da6-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="30da6-185">Pasirinkite **Naujas** tam, kad sukurtumėte sertifikatų grandinę.</span><span class="sxs-lookup"><span data-stu-id="30da6-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="30da6-186">**Pavadinimas** laukelyje įveskite sertifikato grandinės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="30da6-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="30da6-187">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="30da6-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="30da6-188">Skyriuje **Sertifikatai** pasirinkite **Įtraukti** kad į grandinę būtų įtrauktas sertifikatas.</span><span class="sxs-lookup"><span data-stu-id="30da6-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="30da6-189">Norėdami pakeisti **Aukštyn** arba **Žemyn** poziciją sertifikato grandinėje.</span><span class="sxs-lookup"><span data-stu-id="30da6-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="30da6-190">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="30da6-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="30da6-191">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="30da6-191">Close the page.</span></span>
11. <span data-ttu-id="30da6-192">Puslapyje **Paslaugų aplinka** veiksmų juostoje rinkitės **Publikuoti** kad publikuotumėte aplinką debesyje.</span><span class="sxs-lookup"><span data-stu-id="30da6-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="30da6-193">Vertė **Būsena** laukelyje pakeičiama į **Publikuota**.</span><span class="sxs-lookup"><span data-stu-id="30da6-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="30da6-194">Kurkite sujungtą programą</span><span class="sxs-lookup"><span data-stu-id="30da6-194">Create a connected application</span></span>

1. <span data-ttu-id="30da6-195">**Aplinkos nustatymų** puslapyje, veiksmų juostoje pasirinkite **Sujungtos programos**.</span><span class="sxs-lookup"><span data-stu-id="30da6-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="30da6-196">Pasirinkite **Naujas**, kad sujungtumėte programą.</span><span class="sxs-lookup"><span data-stu-id="30da6-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="30da6-197">**Pavadinimas** laukelyje įveskite sujungiamos programos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="30da6-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="30da6-198">Laukelyje **Programa** įveskite „Finance and Supply Chain Management“ sujungiamos aplinkos URL.</span><span class="sxs-lookup"><span data-stu-id="30da6-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="30da6-199">Laukelyje **Nuomotojo** įveskite „Finance and Supply Chain Management“ nuomotojo aplinką.</span><span class="sxs-lookup"><span data-stu-id="30da6-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="30da6-200">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="30da6-200">Select **Save**.</span></span>
6. <span data-ttu-id="30da6-201">Veiksmų srityje pasirinkite **Tikrinti ryšį** norėdami patikrinti ryšį su aplinka.</span><span class="sxs-lookup"><span data-stu-id="30da6-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="30da6-202">Tada uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="30da6-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="30da6-203">Susieti prie aplinkos prijungtas programas</span><span class="sxs-lookup"><span data-stu-id="30da6-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="30da6-204">**Aplinkos nustatymų** puslapyje pasirinkite **Naujas** jei norite aplinkai priskirt prijungtą programą.</span><span class="sxs-lookup"><span data-stu-id="30da6-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="30da6-205">Laukelyje **Prijungta programa** pasirinkite sujungtą programą.</span><span class="sxs-lookup"><span data-stu-id="30da6-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="30da6-206">Lauke **Aptarnavimo aplinka** pasirinkite darbo užsakymo aptarnavimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="30da6-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="30da6-207">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="30da6-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="30da6-208">Elektroninių SF išrašymo priedo integravimo nustatymas „Finance and Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="30da6-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="30da6-209">Elektroninių SF išrašymo priedo integravimo funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="30da6-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="30da6-210">Prisijunkite prie savo „Finance and Supply Chain Management“ elemento.</span><span class="sxs-lookup"><span data-stu-id="30da6-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="30da6-211">Darbo srityje **Funkcijų valdymas** ieškokite naujos funkcijos **Elektroninių SF išrašymo priedo integravimas**.</span><span class="sxs-lookup"><span data-stu-id="30da6-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="30da6-212">Jei ši funkcija nebus rodoma puslapyje, pasirinkite **Tikrinti, ar yra naujinimų**.</span><span class="sxs-lookup"><span data-stu-id="30da6-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="30da6-213">Pasirinkite funkciją ir tada pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="30da6-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="30da6-214">Paslaugos galinio punkto URL nustatymas</span><span class="sxs-lookup"><span data-stu-id="30da6-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="30da6-215">Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="30da6-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="30da6-216">Skirtuke **Pateikimo paslaugos** laukelyje **Aptarnavimo galutinio taško URL** įveskite atitinkamą „Azure" geografijos paslaugos galinį punktą, kaip parodyta pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="30da6-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="30da6-217">Duomenų centras „Azure" geografijoje</span><span class="sxs-lookup"><span data-stu-id="30da6-217">Datacenter Azure geography</span></span> | <span data-ttu-id="30da6-218">Paslaugos galinio punkto URL</span><span class="sxs-lookup"><span data-stu-id="30da6-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="30da6-219">Rytų JAV</span><span class="sxs-lookup"><span data-stu-id="30da6-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="30da6-220">Vakarų JAV</span><span class="sxs-lookup"><span data-stu-id="30da6-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="30da6-221">Šiaurės ES</span><span class="sxs-lookup"><span data-stu-id="30da6-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="30da6-222">Vakarų ES</span><span class="sxs-lookup"><span data-stu-id="30da6-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="30da6-223">Laukelyje **Aplinka** įveskite paslaugų aplinkos publikuotos elektroninėse sąskaitos pavadinimą</span><span class="sxs-lookup"><span data-stu-id="30da6-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="30da6-224">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="30da6-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="30da6-225">Įgalinti skrydžio raktus</span><span class="sxs-lookup"><span data-stu-id="30da6-225">Enable Flighting keys</span></span>

<span data-ttu-id="30da6-226">Įgalinkite "Microsoft Dynamics 365 Finance“ ar "Microsoft Dynamics 365 Supply Chain Management“ 10.0.17 ar ankstesnių versijų skrydžio raktus.</span><span class="sxs-lookup"><span data-stu-id="30da6-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="30da6-227">Vykdykite toliau pateiktą SQL komandą.</span><span class="sxs-lookup"><span data-stu-id="30da6-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="30da6-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="30da6-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="30da6-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="30da6-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="30da6-230">Atlikite IISreset komandą visiems AOS.</span><span class="sxs-lookup"><span data-stu-id="30da6-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
