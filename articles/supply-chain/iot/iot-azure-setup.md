---
title: IoT analizės papildiniui skirtų „Azure“ išteklių konfigūravimas
description: Šioje temoje aiškinama, kaip kurti ir konfigūruoti „Microsoft Azure“ išteklius, reikalingus IoT analizės papildiniui.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1277d2ab8bb1f2925874f7469250e164f6bde62d
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4014917"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="783b2-103">IoT analizės papildiniui skirtų „Azure“ išteklių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="783b2-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="783b2-104">Šioje temoje aiškinama, kaip kurti ir konfigūruoti „Microsoft Azure“ išteklius, reikalingus IoT analizės papildiniui.</span><span class="sxs-lookup"><span data-stu-id="783b2-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="783b2-105">„Azure“ išteklių kūrimas</span><span class="sxs-lookup"><span data-stu-id="783b2-105">Create Azure resources</span></span>

<span data-ttu-id="783b2-106">Norėdami sukurti „IoT Hub“, „Redis“ talpyklą ir raktų saugyklą, kurias galėtų pasiekti „Microsoft Dynamics 365 Supply Chain Management“, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="783b2-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="783b2-107">Patikrinimas, ar „Microsoft Dynamics ERP Microservices“ pirmosios šalies programos ID yra jūsų nuomotojuje</span><span class="sxs-lookup"><span data-stu-id="783b2-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="783b2-108">Norėdami patikrinti, ar „Microsoft Dynamics ERP Microservices“ pirmosios šalies programos ID yra jūsų nuomotojuje, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="783b2-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="783b2-109">Prisijunkite prie „Azure“ portalo adresu <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="783b2-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="783b2-110">Eikite į **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="783b2-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="783b2-111">Eikite į **Įmonės programos**.</span><span class="sxs-lookup"><span data-stu-id="783b2-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="783b2-112">Lauke **Programos tipas** pasirinkite **„Microsoft“ programos**.</span><span class="sxs-lookup"><span data-stu-id="783b2-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="783b2-113">Ieškos lauke įveskite **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="783b2-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="783b2-114">Patikrinkite, ar **Microsoft Dynamics ERP Microservices** yra sąraše.</span><span class="sxs-lookup"><span data-stu-id="783b2-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="783b2-115">Kitų programų pavadinimai panašūs.</span><span class="sxs-lookup"><span data-stu-id="783b2-115">Other applications have similar names.</span></span> <span data-ttu-id="783b2-116">Todėl įsitikinkite, kad radote tinkamą programą.</span><span class="sxs-lookup"><span data-stu-id="783b2-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="783b2-117">Programos ID yra **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="783b2-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="783b2-118">Jei programos sąraše nėra, turite ją įtraukti į savo nuomotoją.</span><span class="sxs-lookup"><span data-stu-id="783b2-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="783b2-119">„Azure“ portalo įrankių juostoje pasirinkite mygtuką, kad atidarytumėte „Azure Cloud Shell“.</span><span class="sxs-lookup"><span data-stu-id="783b2-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="783b2-120">Vykdykite komandą **Install-Module AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="783b2-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="783b2-121">Įveskite **Y** , kad įdiegtumėte modulį.</span><span class="sxs-lookup"><span data-stu-id="783b2-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="783b2-122">Vykdykite komandą **Get-InstalledModule -Name "AzureAD"** , kad įsitikintumėte, jog modulis įdiegtas.</span><span class="sxs-lookup"><span data-stu-id="783b2-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="783b2-123">Norėdami vykdyti autentifikavimą, vykdykite komandą **Connect-AzureAD -Confirm**.</span><span class="sxs-lookup"><span data-stu-id="783b2-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="783b2-124">Vykdykite komandą **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="783b2-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="783b2-125">Dabar galite pakartoti 1–6 veiksmus, kad patikrintumėte, jog programos ID yra jūsų nuomotojuje.</span><span class="sxs-lookup"><span data-stu-id="783b2-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="783b2-126">Raktų saugyklos išteklių kūrimas</span><span class="sxs-lookup"><span data-stu-id="783b2-126">Create a key vault resource</span></span>

<span data-ttu-id="783b2-127">Norėdami kurti raktų saugyklos išteklius, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="783b2-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="783b2-128">„Azure“ portale, sukurkite arba eikite į išteklių grupę.</span><span class="sxs-lookup"><span data-stu-id="783b2-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="783b2-129">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-129">Select **Add**.</span></span>
3. <span data-ttu-id="783b2-130">Puslapio **Nauja** ieškos lauke įveskite **Raktų saugykla**.</span><span class="sxs-lookup"><span data-stu-id="783b2-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="783b2-131">Paskui paspauskite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-131">Then select **Create**.</span></span>
4. <span data-ttu-id="783b2-132">Puslapyje **Raktų saugyklos kūrimas** esančiame lauke **Raktų saugyklos pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="783b2-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="783b2-133">Peržiūrėkite numatytąsias reikšmes, tada pasirinkite **Peržiūrėti ir sukurti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="783b2-134">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-134">Select **Create**.</span></span>

<span data-ttu-id="783b2-135">Raktų saugykla sukuriama fone.</span><span class="sxs-lookup"><span data-stu-id="783b2-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="783b2-136">„IoT Hub“ išteklių kūrimas</span><span class="sxs-lookup"><span data-stu-id="783b2-136">Create an IoT hub resource</span></span>

<span data-ttu-id="783b2-137">Norėdami kurti „IoT Hub“ išteklius, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="783b2-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="783b2-138">Kurkite arba eikite į išteklių grupę.</span><span class="sxs-lookup"><span data-stu-id="783b2-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="783b2-139">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-139">Select **Add**.</span></span>
3. <span data-ttu-id="783b2-140">Puslapio **Nauja** ieškos lauke įveskite **IoT Hub**.</span><span class="sxs-lookup"><span data-stu-id="783b2-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="783b2-141">Paskui paspauskite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-141">Then select **Create**.</span></span>
4. <span data-ttu-id="783b2-142">Lauke **„IoT Hub“ pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="783b2-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="783b2-143">Peržiūrėkite numatytąsias reikšmes, tada pasirinkite **Peržiūrėti ir sukurti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="783b2-144">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-144">Select **Create**.</span></span>

<span data-ttu-id="783b2-145">„IoT Hub“ sukuriamas fone.</span><span class="sxs-lookup"><span data-stu-id="783b2-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="783b2-146">Rekomenduojame vienai aplinkai kurti tik vieną „IoT Hub“ išteklių.</span><span class="sxs-lookup"><span data-stu-id="783b2-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="783b2-147">„Redis“ talpyklos išteklių kūrimas</span><span class="sxs-lookup"><span data-stu-id="783b2-147">Create a Redis cache resource</span></span>

<span data-ttu-id="783b2-148">Norėdami kurti „Redis“ talpyklos išteklius, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="783b2-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="783b2-149">Kurkite arba eikite į išteklių grupę.</span><span class="sxs-lookup"><span data-stu-id="783b2-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="783b2-150">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-150">Select **Add**.</span></span>
3. <span data-ttu-id="783b2-151">Puslapio **Nauja** ieškos lauke įveskite **„Azure“ talpykla, skirta „Redis“**.</span><span class="sxs-lookup"><span data-stu-id="783b2-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="783b2-152">Paskui paspauskite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-152">Then select **Create**.</span></span>
4. <span data-ttu-id="783b2-153">Tada lauke **DNS pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="783b2-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="783b2-154">Peržiūrėkite numatytąsias reikšmes, tada pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="783b2-155">„Redis“ talpykla sukuriama fone.</span><span class="sxs-lookup"><span data-stu-id="783b2-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="783b2-156">Rekomenduojame vienai aplinkai kurti tik vieną „Redis“ talpyklą.</span><span class="sxs-lookup"><span data-stu-id="783b2-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="783b2-157">Dabar sukurti visi ištekliai.</span><span class="sxs-lookup"><span data-stu-id="783b2-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="783b2-158">„Azure“ išteklių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="783b2-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="783b2-159">„IoT Hub“ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="783b2-159">Configure the IoT hub</span></span>

<span data-ttu-id="783b2-160">Norėdami konfigūruoti „IoT Hub“, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="783b2-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="783b2-161">Savo ištekliuose pasirinkite „IoT Hub“ išteklius.</span><span class="sxs-lookup"><span data-stu-id="783b2-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="783b2-162">Kairiojoje naršymo srityje pasirinkite **Įtaisytieji galiniai punktai**.</span><span class="sxs-lookup"><span data-stu-id="783b2-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="783b2-163">Dalyje **Vartotojų grupės** įklijuokite toliau nurodytas vartotojų grupes.</span><span class="sxs-lookup"><span data-stu-id="783b2-163">Under **Consumer groups** , paste the following consumer groups.</span></span> <span data-ttu-id="783b2-164">Šios vartotojų grupės atitinka parengtus naudoti scenarijus.</span><span class="sxs-lookup"><span data-stu-id="783b2-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="783b2-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="783b2-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="783b2-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="783b2-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="783b2-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="783b2-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="783b2-168">Raktų saugyklos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="783b2-168">Configure the key vault</span></span>

<span data-ttu-id="783b2-169">Norėdami konfigūruoti raktų saugyklą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="783b2-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="783b2-170">Savo ištekliuose pasirinkite raktų saugyklos išteklių.</span><span class="sxs-lookup"><span data-stu-id="783b2-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="783b2-171">Kairiojoje naršymo srityje pasirinkite **Prieigos strategijos**.</span><span class="sxs-lookup"><span data-stu-id="783b2-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="783b2-172">Pasirinkite **Įtraukti prieigos strategiją**.</span><span class="sxs-lookup"><span data-stu-id="783b2-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="783b2-173">Puslapyje **Įtraukti prieigos strategiją** esančiame lauke **Slaptos teisės** pasirinkite **Gauti** ir **Sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="783b2-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="783b2-174">Spustelėkite **Pasirinkti pagrindinę**.</span><span class="sxs-lookup"><span data-stu-id="783b2-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="783b2-175">Dialogo lange **Pagrindis** raskite ir pasirinkite **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="783b2-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="783b2-176">Tada pasirinkite **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-176">Then select **Select**.</span></span>
7. <span data-ttu-id="783b2-177">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-177">Select **Add**.</span></span>
8. <span data-ttu-id="783b2-178">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-178">Select **Save**.</span></span>

<span data-ttu-id="783b2-179">Dabar programa turi prieigą prie slaptųjų raktų, esančių raktų saugykloje.</span><span class="sxs-lookup"><span data-stu-id="783b2-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="783b2-180">„IoT Hub“ ryšio eilutės slaptojo rakto įrašymas</span><span class="sxs-lookup"><span data-stu-id="783b2-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="783b2-181">Norėdami įrašyti „IoT Hub“ ryšio eilutės slaptąjį raktą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="783b2-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="783b2-182">Savo ištekliuose pasirinkite „IoT Hub“ išteklius.</span><span class="sxs-lookup"><span data-stu-id="783b2-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="783b2-183">Kairiojoje naršymo srityje pasirinkite **Įtaisytieji galiniai punktai**.</span><span class="sxs-lookup"><span data-stu-id="783b2-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="783b2-184">Kopijuokite reikšmę, esančią lauke **Su „Event Hub“ suderinamas galinis punktas**.</span><span class="sxs-lookup"><span data-stu-id="783b2-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="783b2-185">Eikite į raktų saugyklos išteklius.</span><span class="sxs-lookup"><span data-stu-id="783b2-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="783b2-186">Kairiojoje naršymo srityje pasirinkite **Slaptieji raktai**.</span><span class="sxs-lookup"><span data-stu-id="783b2-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="783b2-187">Pasirinkite **Generuoti / importuoti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="783b2-188">Tada lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="783b2-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="783b2-189">Lauke **Reikšmė** įklijuokite anksčiau nukopijuotą galinio punkto reikšmę.</span><span class="sxs-lookup"><span data-stu-id="783b2-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="783b2-190">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="783b2-191">„Redis“ talpyklos ryšio eilutės slaptojo rakto įrašymas</span><span class="sxs-lookup"><span data-stu-id="783b2-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="783b2-192">Norėdami įrašyti „Redis“ talpyklos ryšio eilutės slaptąjį raktą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="783b2-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="783b2-193">Savo ištekliuose pasirinkite „Redis“ talpyklos išteklių.</span><span class="sxs-lookup"><span data-stu-id="783b2-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="783b2-194">Pasirinkite **Prieigos raktai**.</span><span class="sxs-lookup"><span data-stu-id="783b2-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="783b2-195">Nukopijuokite lauke **Pagrindinė ryšio eilutė** esančią reikšmę.</span><span class="sxs-lookup"><span data-stu-id="783b2-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="783b2-196">Eikite į raktų saugyklos išteklius.</span><span class="sxs-lookup"><span data-stu-id="783b2-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="783b2-197">Kairiojoje naršymo srityje pasirinkite **Slaptieji raktai**.</span><span class="sxs-lookup"><span data-stu-id="783b2-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="783b2-198">Pasirinkite **Generuoti / importuoti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="783b2-199">Tada lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="783b2-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="783b2-200">Lauke **Reikšmė** įklijuokite anksčiau nukopijuotą ryšio eilutę.</span><span class="sxs-lookup"><span data-stu-id="783b2-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="783b2-201">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="783b2-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="783b2-202">Atnaujindami vieną iš ryšio eilučių, taip pat turite atnaujinti slaptųjų raktų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="783b2-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="783b2-203">Dabar baigėte rengti reikiamus „Azure“ išteklius.</span><span class="sxs-lookup"><span data-stu-id="783b2-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="783b2-204">Kitas veiksmas – [portale „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegti IoT analizės papildinį](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="783b2-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>