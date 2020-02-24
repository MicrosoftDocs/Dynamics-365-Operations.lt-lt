---
title: „Dynamics 365 Commerce“ peržiūros aplinkos konfigūravimas
description: Šioje temoje paaiškinama, kaip parengti „Microsoft Dynamics 365 Commerce“ peržiūros aplinką.
author: psimolin
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cbd4c118de2e91c8849461b20a01403049a07e66
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024641"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="3c933-103">„Dynamics 365 Commerce“ peržiūros aplinkos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="3c933-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3c933-104">Šioje temoje pateikiama informacija apie tai, kaip konfigūruoti „Dynamics 365 Commerce“ peržiūros aplinką.</span><span class="sxs-lookup"><span data-stu-id="3c933-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="3c933-105">Prieš pradedant konfigūraciją, rekomenduojame perskaityti šią temą, kad suprastumėte proceso eigą.</span><span class="sxs-lookup"><span data-stu-id="3c933-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="3c933-106">Jei jums dar nesuteikta prieiga prie „Dynamics 365 Commerce“ peržiūros, prisijungimą galite gauti [Dynamics 365 Commerce svetainėje](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="3c933-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="3c933-107">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="3c933-107">Overview</span></span>

<span data-ttu-id="3c933-108">Norėdami sėkmingai parengti savo „Commerce“ peržiūros aplinką, turite sukurti projektą, kuriame būtų konkretaus produkto pavadinimas ir tipas.</span><span class="sxs-lookup"><span data-stu-id="3c933-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="3c933-109">Aplinka ir „Commerce scale unit“ (CSU) taip pat turi keletą specifinių parametrų, kuriuos turėsite naudoti teikdami „e-Commerce“.</span><span class="sxs-lookup"><span data-stu-id="3c933-109">The environment and commerce scale unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="3c933-110">Šios temos instrukcijose aprašomi visi veiksmai, kuriuos reikia atlikti norint užbaigti konfigūravimą, ir parametrai, kuriuos turite naudoti.</span><span class="sxs-lookup"><span data-stu-id="3c933-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="3c933-111">Sėkmingai parengę „Commerce“ peržiūros aplinką, turite atlikti keletą veiksmų po parengimo, kad ją paruoštumėte.</span><span class="sxs-lookup"><span data-stu-id="3c933-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="3c933-112">Kai kurie veiksmai yra pasirinktiniai, atsižvelgiant į tai, kokius sistemos aspektus norite įvertinti.</span><span class="sxs-lookup"><span data-stu-id="3c933-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="3c933-113">Visada galite atlikti pasirinktinius veiksmus vėliau.</span><span class="sxs-lookup"><span data-stu-id="3c933-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="3c933-114">Informacijos apie tai, kaip sukonfigūruoti „Commerce“ peržiūros aplinką po to, kai ją parengsite, rasite skyriuje [„Commerce“ peržiūros aplinkos konfigūravimas](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="3c933-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="3c933-115">Informacijos apie tai, kaip sukonfigūruoti „Commerce“ peržiūros aplinkos pasirinktines funkcijas, rasite skyriuje [„Commerce“ peržiūros aplinkos pasirinktinių funkcijų konfigūravimas](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="3c933-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="3c933-116">Jei turite klausimų dėl parengimo veiksmų arba kyla problemų, praneškite apie tai „Microsoft“ [„Microsoft Dynamics 365 Commerce“ peržiūros „Yammer“ grupėje](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="3c933-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3c933-117">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="3c933-117">Prerequisites</span></span>

<span data-ttu-id="3c933-118">Toliau pateikiamos būtinosios sąlygos turi būti įvykdytos prieš parengiant „Commerce“ peržiūros aplinką.</span><span class="sxs-lookup"><span data-stu-id="3c933-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="3c933-119">Turite prieigą prie „Microsoft Dynamics Lifecycle Services“ (LCS) portalo.</span><span class="sxs-lookup"><span data-stu-id="3c933-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="3c933-120">Esate „Microsoft Dynamics“ 365 partneris ar klientas ir galite sukurti „Dynamics 365 Commerce“ projektą.</span><span class="sxs-lookup"><span data-stu-id="3c933-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="3c933-121">Buvote priimti į „Dynamics 365 Commerce“ peržiūros programą.</span><span class="sxs-lookup"><span data-stu-id="3c933-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="3c933-122">Turite reikiamus leidimus, kad galėtumėte sukurti projektą projektą, skirtą **Perkelti, rasti sprendimus ir mokytis**.</span><span class="sxs-lookup"><span data-stu-id="3c933-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="3c933-123">Esate vaidmens **Aplinkos administratorius** arba **Projekto savininkas** narys projekte, kuriame parengsite aplinką.</span><span class="sxs-lookup"><span data-stu-id="3c933-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="3c933-124">Turite administratoriaus prieigą prie savo „Microsoft Azure“ prenumeratos arba galite susisiekti su prenumeratos administratoriumi, kuris gali atlikti du veiksmus, reikalaujančius administratoriaus teisių, jūsų vardu.</span><span class="sxs-lookup"><span data-stu-id="3c933-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="3c933-125">Turite savo „Azure Active Directory“ („Azure AD“) nuomotojo ID.</span><span class="sxs-lookup"><span data-stu-id="3c933-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="3c933-126">Sukūrėte „Azure AD“ saugos grupę, kuri gali būti naudojama kaip „e-Commerce“ sistemos administratoriaus grupė, ir turite jos ID.</span><span class="sxs-lookup"><span data-stu-id="3c933-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="3c933-127">Sukūrėte „Azure AD“ saugos grupę, kuri gali būti naudojama kaip įvertinimų ir apžvalgų moderatoriaus grupė, ir turite jos ID.</span><span class="sxs-lookup"><span data-stu-id="3c933-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="3c933-128">(Ši saugos grupė gali sutapti su „e-Commerce“ sistemos administravimo grupe.)</span><span class="sxs-lookup"><span data-stu-id="3c933-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="3c933-129">Jūsų „Commerce“ peržiūros aplinkos parengimas</span><span class="sxs-lookup"><span data-stu-id="3c933-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="3c933-130">Šiose procedūrose paaiškinama, kaip parengti „Commerce“ peržiūros aplinką.</span><span class="sxs-lookup"><span data-stu-id="3c933-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="3c933-131">Sėkmingai jas atlikus, „Commerce“ peržiūros aplinka bus paruošta konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="3c933-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="3c933-132">Visos čia aprašytos veiklos vyksta LCS portale.</span><span class="sxs-lookup"><span data-stu-id="3c933-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c933-133">Peržiūros prieiga yra susieta su LCS paskyra ir organizacija, kurią nurodėte savo „Commerce“ peržiūros programoje.</span><span class="sxs-lookup"><span data-stu-id="3c933-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="3c933-134">Norėdami parengti „Commerce“ peržiūros aplinką, turite naudoti tą pačią paskyrą.</span><span class="sxs-lookup"><span data-stu-id="3c933-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="3c933-135">Jei „Commerce“ peržiūros aplinkoje turite naudoti kitą LCS paskyrą ar nuomininką, turite pateikti šią informaciją „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="3c933-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="3c933-136">Kontaktinės informacijos ieškokite toliau šioje temoje, skyriuje [„Commerce“ peržiūros aplinkos palaikymas](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="3c933-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="3c933-137">Patvirtinimas, kad peržiūros funkcijos prieinamos ir įjungtos LCS</span><span class="sxs-lookup"><span data-stu-id="3c933-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="3c933-138">Norėdami patvirtinti, kad peržiūros funkcijos yra prieinamos ir įjungtos LCS, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3c933-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="3c933-139">Prisijunkite prie [LCS portalo](https://lcs.dynamics.com), naudodami LCS paskyrą, kurią naudojote prašydami suteikti prieigą prie peržiūros.</span><span class="sxs-lookup"><span data-stu-id="3c933-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="3c933-140">LCS pagrindiniame puslapyje slinkite į dešinę iki pat galo ir pasirinkite plytelę **Peržiūros versijos funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="3c933-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Peržiūros versijos valdymo plytelė](./media/preview1.png)

1. <span data-ttu-id="3c933-142">Slinkite žemyn iki **Asmeninės peržiūros funkcijos** ir patvirtinkite, kad toliau pateikiamos funkcijos yra galimos ir įjungtos.</span><span class="sxs-lookup"><span data-stu-id="3c933-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="3c933-143">El. prekybos vertinimas</span><span class="sxs-lookup"><span data-stu-id="3c933-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="3c933-144">„Commerce“ peržiūros programos aplinkos</span><span class="sxs-lookup"><span data-stu-id="3c933-144">Commerce Preview Program Environments</span></span>

    ![Privačiosios vertinimo versijos funkcijos](./media/preview2.png)

1. <span data-ttu-id="3c933-146">Jei šios funkcijos sąraše nerodomos, susisiekite su „Microsoft“ ir pateikite savo darbo el. pašto adresą, LCS paskyrą ir nuomotojo informaciją.</span><span class="sxs-lookup"><span data-stu-id="3c933-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="3c933-147">Kontaktinės informacijos ieškokite skyriuje [„Commerce“ peržiūros aplinkos palaikymas](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="3c933-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="3c933-148">Kurti naują projektą</span><span class="sxs-lookup"><span data-stu-id="3c933-148">Create a new project</span></span>

<span data-ttu-id="3c933-149">Norėdami sukurti naują projektą LCS, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3c933-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="3c933-150">LCS pagrindiniame puslapyje pasirinkite pliuso ženklą (**„+“**), kad sukurtumėte projektą.</span><span class="sxs-lookup"><span data-stu-id="3c933-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="3c933-151">Dešiniojoje srityje atlikite vieną iš toliau pateikiamų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="3c933-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="3c933-152">Jei esate partneris, pasirinkite **Perkelti, kurti sprendimus ir sužinoti**.</span><span class="sxs-lookup"><span data-stu-id="3c933-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="3c933-153">Jei esate klientas, pasirinkite **Galimas išankstinis pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="3c933-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="3c933-154">Įveskite pavadinimą, aprašą ir pramonės šaką.</span><span class="sxs-lookup"><span data-stu-id="3c933-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="3c933-155">Lauke **Produkto pavadinimas** pasirinkite **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="3c933-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="3c933-156">Lauke **Produkto versija** pasirinkite **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="3c933-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="3c933-157">Lauke **Metodika** pasirinkite **„Dynamics Retail“ visuotinio diegimo metodika**.</span><span class="sxs-lookup"><span data-stu-id="3c933-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="3c933-158">Pasirinktinai: galite importuoti vaidmenis ir vartotojus iš esamo projekto.</span><span class="sxs-lookup"><span data-stu-id="3c933-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="3c933-159">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="3c933-159">Select **Create**.</span></span> <span data-ttu-id="3c933-160">Pateikiamas projekto rodinys.</span><span class="sxs-lookup"><span data-stu-id="3c933-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="3c933-161">„Azure“ jungties įtraukimas</span><span class="sxs-lookup"><span data-stu-id="3c933-161">Add the Azure Connector</span></span>

<span data-ttu-id="3c933-162">Norėdami įtraukti „Azure“ jungti į savo LCS projektą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3c933-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="3c933-163">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="3c933-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="3c933-164">Jei esate partneris, pasirinkite plytelę **Projekto parametrai** dešinės pusės gale.</span><span class="sxs-lookup"><span data-stu-id="3c933-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="3c933-165">Jei esate klientas, viršutiniame meniu pasirinkite **Projekto parametrai**.</span><span class="sxs-lookup"><span data-stu-id="3c933-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="3c933-166">Pasirinkite **„Azure“ jungtys**.</span><span class="sxs-lookup"><span data-stu-id="3c933-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="3c933-167">Pasirinkite **Įtraukti**, norėdami įtraukti „Azure“ jungtį.</span><span class="sxs-lookup"><span data-stu-id="3c933-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="3c933-168">Įvesti vardą.</span><span class="sxs-lookup"><span data-stu-id="3c933-168">Enter a name.</span></span>
1. <span data-ttu-id="3c933-169">Įveskite savo „Azure“ prenumeratos ID.</span><span class="sxs-lookup"><span data-stu-id="3c933-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="3c933-170">Įjunkite parinktį **Konfigūruoti, kad būtų galima naudoti „Azure“ išteklių tvarkytuvą (ARM)**.</span><span class="sxs-lookup"><span data-stu-id="3c933-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="3c933-171">Įsitikinkite, kad vertė **„Azure“ prenumeratos AAD nuomotojo domenas ( arba ID)** yra tinkama.</span><span class="sxs-lookup"><span data-stu-id="3c933-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="3c933-172">Pagal poreikį kreipkitės į „Azure“ prenumeratos administratorių.</span><span class="sxs-lookup"><span data-stu-id="3c933-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="3c933-173">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="3c933-173">Select **Next**.</span></span>
1. <span data-ttu-id="3c933-174">Sekite puslapyje pateikiamas instrukcijas, kad suteiktumėte reikiamoms programoms prieigą prie jūsų prenumeratos.</span><span class="sxs-lookup"><span data-stu-id="3c933-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="3c933-175">Pagal poreikį kreipkitės į „Azure“ prenumeratos administratorių.</span><span class="sxs-lookup"><span data-stu-id="3c933-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="3c933-176">Prisijunkite prie [„Azure“ portalo](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="3c933-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="3c933-177">Įsitikinkite, kad pasirinktas tinkamas katalogas, o tada kairėje esančiame meniu pasirinkite **Prenumeratos**.</span><span class="sxs-lookup"><span data-stu-id="3c933-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="3c933-178">Sąraše raskite tinkamą prenumeratą ir ją pasirinkite.</span><span class="sxs-lookup"><span data-stu-id="3c933-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="3c933-179">Pagal poreikį naudokite ieškos funkciją.</span><span class="sxs-lookup"><span data-stu-id="3c933-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="3c933-180">Meniu pasirinkite **Prieigos valdymas (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="3c933-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="3c933-181">Dešinėje, dalyje **Įtraukti vaidmens priskyrimą** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="3c933-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="3c933-182">Rodoma sritis **Įtraukti vaidmens priskyrimą**.</span><span class="sxs-lookup"><span data-stu-id="3c933-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="3c933-183">Lauke **Vaidmuo** pasirinkite **Bendraautorius**.</span><span class="sxs-lookup"><span data-stu-id="3c933-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="3c933-184">Lauke **Priskirti prieigą prie** palikite numatytąją reikšmę, **„Azure AD“ vartotojas, grupė arba paslaugos narys**.</span><span class="sxs-lookup"><span data-stu-id="3c933-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="3c933-185">Dalyje **Pasirinkti** įveskite **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="3c933-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="3c933-186">Sąraše pasirinkite **„Dynamics Deployment Services“ \[wsfed-enabled\]**.</span><span class="sxs-lookup"><span data-stu-id="3c933-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="3c933-187">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3c933-187">Select **Save**.</span></span>

1. <span data-ttu-id="3c933-188">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="3c933-188">Select **Next**.</span></span>
1. <span data-ttu-id="3c933-189">Sekite puslapyje pateikiamas instrukcijas, kad suteiktumėte reikiamoms programoms prieigą prie jūsų prenumeratos.</span><span class="sxs-lookup"><span data-stu-id="3c933-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="3c933-190">Pagal poreikį kreipkitės į „Azure“ prenumeratos administratorių.</span><span class="sxs-lookup"><span data-stu-id="3c933-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="3c933-191">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="3c933-191">Select **Next**.</span></span>
1. <span data-ttu-id="3c933-192">Lauke **„Azure“ regionas** pasirinkite **Rytų JAV**, **Rytų JAV 2**, **Vakarų JAV** arba **Vakarų JAV 2**.</span><span class="sxs-lookup"><span data-stu-id="3c933-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="3c933-193">Pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="3c933-193">Select **Connect**.</span></span> <span data-ttu-id="3c933-194">Jūsų „Azure“ jungtis turi pasirodyti sąraše.</span><span class="sxs-lookup"><span data-stu-id="3c933-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="3c933-195">„Commerce“ peržiūros demonstracinio pagrindinio plėtinio importavimas</span><span class="sxs-lookup"><span data-stu-id="3c933-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="3c933-196">Norėdami importuoti „Commerce“ peržiūros demonstracinį pagrindinį plėtinį į savo projektą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3c933-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="3c933-197">Atidarykite projekto pagrindinį puslapį, pasirinkę projekto pavadinimą viršuje.</span><span class="sxs-lookup"><span data-stu-id="3c933-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="3c933-198">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="3c933-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="3c933-199">Jei esate partneris, pasirinkite plytelę **Turto biblioteka** dešinės pusės gale.</span><span class="sxs-lookup"><span data-stu-id="3c933-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="3c933-200">Jei esate klientas, viršutiniame meniu pasirinkite **Turto biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="3c933-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="3c933-201">Pasirinkite **Programinės įrangos diegimo paketas** iš sąrašo kairėje pusėje.</span><span class="sxs-lookup"><span data-stu-id="3c933-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="3c933-202">Pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="3c933-202">Select **Import**.</span></span>
1. <span data-ttu-id="3c933-203">Dalyje **Bendrai naudojamo turto biblioteka** turto sąraše pasirinkite **„Commerce“ peržiūros demonstracinis pagrindinis plėtinys**.</span><span class="sxs-lookup"><span data-stu-id="3c933-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="3c933-204">Pasirinkite **Paimti**.</span><span class="sxs-lookup"><span data-stu-id="3c933-204">Select **Pick**.</span></span> <span data-ttu-id="3c933-205">Grįšite į turto biblioteką ir turėtumėte matyti plėtinį sąraše.</span><span class="sxs-lookup"><span data-stu-id="3c933-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="3c933-206">Toliau pateikiamoje iliustracijoje parodyti veiksmai, kurių reikia imtis LCS puslapyje **Turto biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="3c933-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![„Commerce“ peržiūros demonstracinio pagrindinio plėtinio importavimas](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="3c933-208">Aplinkos diegimas</span><span class="sxs-lookup"><span data-stu-id="3c933-208">Deploy the environment</span></span>

<span data-ttu-id="3c933-209">Atlikite toliau pateikiamus veiksmus, norėdami įdiegti aplinką.</span><span class="sxs-lookup"><span data-stu-id="3c933-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="3c933-210">Gali būti, kad nereikės atlikti 6, 7 ir (arba) 8 veiksmų, nes puslapiai, kuriuose yra viena parinktis, praleidžiami.</span><span class="sxs-lookup"><span data-stu-id="3c933-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="3c933-211">Kai esate rodinyje **Aplinkos parametrai**, įsitikinkite, kad tekstas **Dynamics 365 Commerce – Demo (10.0.* x* su platformos atnaujinimu *xx*)\*\* rodomas tiesiai virš lauko **Aplinkos pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="3c933-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="3c933-212">Norėdami gauti išsamesnės informacijos, žr. iliustraciją, pavaizduotą po 8 veiksmo.</span><span class="sxs-lookup"><span data-stu-id="3c933-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="3c933-213">Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.</span><span class="sxs-lookup"><span data-stu-id="3c933-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="3c933-214">Pasirinkite **Įtraukti**, kad įtrauktumėte aplinką.</span><span class="sxs-lookup"><span data-stu-id="3c933-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="3c933-215">Lauke **Programos versija** pasirinkite naujausią versiją.</span><span class="sxs-lookup"><span data-stu-id="3c933-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="3c933-216">Jei norite pasirinkti ne naujausią programos versiją, nesirinkite versijos, ankstesnės nei versija **10.0.8**.</span><span class="sxs-lookup"><span data-stu-id="3c933-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="3c933-217">Lauke **Platformos versija** naudokite platformos versiją, kuri automatiškai parenkama jūsų pasirinktai programos versijai.</span><span class="sxs-lookup"><span data-stu-id="3c933-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Programos ir platformos versijų pasirinkimas](./media/project1.png)

1. <span data-ttu-id="3c933-219">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="3c933-219">Select **Next**.</span></span>
1. <span data-ttu-id="3c933-220">Pasirinkite aplinkos topologiją **Demonstracinė versija**.</span><span class="sxs-lookup"><span data-stu-id="3c933-220">Select **Demo** as the environment topology.</span></span>

    ![1 aplinkos topologijos pasirinkimas](./media/project2.png)

1. <span data-ttu-id="3c933-222">Pasirinkite **Dynamics 365 Commerce – Demo** kaip aplinkos topologiją.</span><span class="sxs-lookup"><span data-stu-id="3c933-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="3c933-223">Jei anksčiau sukonfigūruosite vieną „Azure“ jungtį, ji bus naudojama šioje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="3c933-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="3c933-224">Jei sukonfigūravote keletą „Azure“ jungčių, galite pasirinkti, kurią jungtį naudoti: **Rytų JAV**, **Rytų JAV 2**, **Vakarų JAV** arba **Vakarų JAV 2**.</span><span class="sxs-lookup"><span data-stu-id="3c933-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="3c933-225">(Geriausiam betarpiškam našumui užtikrinti rekomenduojame pasirinkti **Vakarų JAV 2**.)</span><span class="sxs-lookup"><span data-stu-id="3c933-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![2 aplinkos topologijos pasirinkimas](./media/project3.png)

1. <span data-ttu-id="3c933-227">Puslapyje **Diegti aplinką** įveskite aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="3c933-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="3c933-228">Nekeiskite išplėstinių parametrų.</span><span class="sxs-lookup"><span data-stu-id="3c933-228">Leave the advanced settings as they are.</span></span>

    ![Puslapis Diegti aplinką](./media/project4.png)

1. <span data-ttu-id="3c933-230">Pagal poreikį pakoreguokite VM dydį.</span><span class="sxs-lookup"><span data-stu-id="3c933-230">Adjust the VM size as required.</span></span> <span data-ttu-id="3c933-231">(Rekomenduojame VM sandėliavimo vienetą \[SKU\] **„D13 v2“**.)</span><span class="sxs-lookup"><span data-stu-id="3c933-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="3c933-232">Peržiūrėkite kainodaros ir licencijavimo sąlygas, tada pažymėkite žymės langelį, kad patvirtintumėte, jog su jomis sutinkate.</span><span class="sxs-lookup"><span data-stu-id="3c933-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="3c933-233">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="3c933-233">Select **Next**.</span></span>
1. <span data-ttu-id="3c933-234">Diegimo patvirtinimo puslapyje patikrinkite, ar išsami informacija yra tiksli, ir pasirinkite **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="3c933-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="3c933-235">Grįšite į rodinį **Aplinkos diegimo debesyje įrankis**, o jūsų aplinka turėtų būti rodoma sąraše.</span><span class="sxs-lookup"><span data-stu-id="3c933-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="3c933-236">Jūsų pageidaujama aplinka bus rodoma eilėje ir paskui diegiama.</span><span class="sxs-lookup"><span data-stu-id="3c933-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="3c933-237">Aplinkos darbo eigoms užbaigti prireiks laiko.</span><span class="sxs-lookup"><span data-stu-id="3c933-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="3c933-238">Todėl patikrinkite vėl maždaug po šešių–devynių valandų.</span><span class="sxs-lookup"><span data-stu-id="3c933-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="3c933-239">Prieš tęsdami įsitikinkite, kad jūsų aplinkos būsena yra **Įdiegta**.</span><span class="sxs-lookup"><span data-stu-id="3c933-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-csu"></a><span data-ttu-id="3c933-240">Inicijuokite „Commerce scale unit“ (CSU)</span><span class="sxs-lookup"><span data-stu-id="3c933-240">Initialize the commerce scale unit (CSU)</span></span>

<span data-ttu-id="3c933-241">Norėdami inicijuoti CSU, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3c933-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="3c933-242">Rodinyje **Aplinkos diegimo debesyje įrankis** sąraše pasirinkite savo aplinką.</span><span class="sxs-lookup"><span data-stu-id="3c933-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="3c933-243">Aplinkos rodinyje dešinėje pasirinkite **Visa išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="3c933-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="3c933-244">Rodomas aplinkos išsamios informacijos rodinys.</span><span class="sxs-lookup"><span data-stu-id="3c933-244">The environment details view appears.</span></span>
1. <span data-ttu-id="3c933-245">Dalyje **Aplinkos funkcijos** pasirinkite **Valdyti**.</span><span class="sxs-lookup"><span data-stu-id="3c933-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="3c933-246">Skirtuke **„Commerce“** pasirinkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="3c933-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="3c933-247">Rodomas CSU inicijavimo parametrų rodinys.</span><span class="sxs-lookup"><span data-stu-id="3c933-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="3c933-248">Lauke **Regionas** pasirinkite **Rytų JAV**, **Rytų JAV 2**, **Vakarų JAV** arba **Vakarų JAV 2**.</span><span class="sxs-lookup"><span data-stu-id="3c933-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="3c933-249">Lauke **Versija** sąraše pasirinkite **Nurodykite versiją**, tada pasirodžiusiame lauke nurodykite **9.18.20014.4**.</span><span class="sxs-lookup"><span data-stu-id="3c933-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="3c933-250">Būtinai nurodykite būtent tą versiją, kuri nurodyta čia.</span><span class="sxs-lookup"><span data-stu-id="3c933-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="3c933-251">Priešingu atveju vėliau teks atnaujinti RCSU į tinkamą versiją.</span><span class="sxs-lookup"><span data-stu-id="3c933-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="3c933-252">Įjunkite parinktį **Taikyti plėtinį**.</span><span class="sxs-lookup"><span data-stu-id="3c933-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="3c933-253">Plėtinių sąraše pasirinkite **„Commerce“ peržiūros demonstracinis pagrindinis plėtinys**.</span><span class="sxs-lookup"><span data-stu-id="3c933-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="3c933-254">Pasirinkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="3c933-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="3c933-255">Diegimo patvirtinimo puslapyje patikrinkite, ar išsami informacija yra tiksli, ir pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="3c933-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="3c933-256">Vėl rodomas rodinys **„Commerce“ valdymas**, kuriame pasirinktas skirtukas **„Commerce“**.</span><span class="sxs-lookup"><span data-stu-id="3c933-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="3c933-257">Jūsų CSU jau buvo rengimo eilėje.</span><span class="sxs-lookup"><span data-stu-id="3c933-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="3c933-258">Prieš tęsdami įsitikinkite, kad jūsų CSU būsena yra **Pavyko**.</span><span class="sxs-lookup"><span data-stu-id="3c933-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="3c933-259">Inicijavimas trunka maždaug dvi–penkias valandas.</span><span class="sxs-lookup"><span data-stu-id="3c933-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="3c933-260">El. prekybos inicijavimas</span><span class="sxs-lookup"><span data-stu-id="3c933-260">Initialize e-Commerce</span></span>

<span data-ttu-id="3c933-261">Norėdami inicijuoti „e-Commerce“, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3c933-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="3c933-262">Skirtuke **„e-Commerce“** peržiūrėkite sutikimą dėl peržiūros ir pasirinkite **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="3c933-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="3c933-263">Lauke **„e-Commerce“ nuomotojo pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="3c933-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="3c933-264">Tačiau įsidėmėkite, kad šis pavadinimas bus rodomas kai kuriuose URL, nukreiptuose į jūsų „e-Commerce“ egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="3c933-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="3c933-265">Lauke **„Commerce scale unit“ pavadinimas** iš sąrašo pasirinkite savo CSU.</span><span class="sxs-lookup"><span data-stu-id="3c933-265">In the **Commerce scale unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="3c933-266">(Sąraše turėtų būti tik viena parinktis.)</span><span class="sxs-lookup"><span data-stu-id="3c933-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="3c933-267">Laukas **„e-Commerce“ geografija** nustatomas automatiškai ir vertės keisti negalima.</span><span class="sxs-lookup"><span data-stu-id="3c933-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="3c933-268">Pasirinkite **Pirmyn**, kad tęstumėte.</span><span class="sxs-lookup"><span data-stu-id="3c933-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="3c933-269">Lauke **Palaikomi pagrindinių kompiuterių vardai** įveskite bet kurį tinkamą domeną, pvz., `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="3c933-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="3c933-270">Lauke **AAD saugos grupė sistemos administratoriui** įveskite keletą pirmų norimos naudoti saugos grupės pavadinimo raidžių.</span><span class="sxs-lookup"><span data-stu-id="3c933-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="3c933-271">Pasirinkite padidinamojo stiklo piktogramą, kad būtų rodomi ieškos rezultatai.</span><span class="sxs-lookup"><span data-stu-id="3c933-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="3c933-272">Iš sąrašo pasirinkite teisingą saugos grupę.</span><span class="sxs-lookup"><span data-stu-id="3c933-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="3c933-273">Lauke **AAD saugos grupė įvertinimų ir apžvalgų moderatoriui** įveskite keletą pirmų norimos naudoti saugos grupės pavadinimo raidžių.</span><span class="sxs-lookup"><span data-stu-id="3c933-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="3c933-274">Pasirinkite padidinamojo stiklo piktogramą, kad būtų rodomi ieškos rezultatai.</span><span class="sxs-lookup"><span data-stu-id="3c933-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="3c933-275">Iš sąrašo pasirinkite teisingą saugos grupę.</span><span class="sxs-lookup"><span data-stu-id="3c933-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="3c933-276">Parinktį **Įjungti įvertinimų ir apžvalgų paslauga** palikite įjungtą.</span><span class="sxs-lookup"><span data-stu-id="3c933-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="3c933-277">Pasirinkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="3c933-277">Select **Initialize**.</span></span> <span data-ttu-id="3c933-278">Vėl rodomas rodinys **„Commerce“ valdymas**, kuriame pasirinktas skirtukas **„e-Commerce“**.</span><span class="sxs-lookup"><span data-stu-id="3c933-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="3c933-279">„E-Commerce“ inicijavimas pradėtas.</span><span class="sxs-lookup"><span data-stu-id="3c933-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="3c933-280">Prieš tęsdami, palaukite, kol „e-Commerce“ inicijavimo būsena bus **Inicijuota sėkmingai**.</span><span class="sxs-lookup"><span data-stu-id="3c933-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="3c933-281">Dalyje **Saitai** apatiniame dešiniajame kampe pasižymėkite toliau pateikiamų saitų URL.</span><span class="sxs-lookup"><span data-stu-id="3c933-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="3c933-282">**„e-Commerce“ svetainė** – saitas į jūsų „e-Commerce“ svetainės šaknį.</span><span class="sxs-lookup"><span data-stu-id="3c933-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="3c933-283">**„e-Commerce“ svetainės valdymo įrankis** – saitas į svetainės valdymo įrankį.</span><span class="sxs-lookup"><span data-stu-id="3c933-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="3c933-284">„Commerce“ peržiūros aplinkos palaikymas</span><span class="sxs-lookup"><span data-stu-id="3c933-284">Commerce preview environment support</span></span>

<span data-ttu-id="3c933-285">Jei atlikdami parengimo veiksmus patiriate problemų, apsilankykite [„Microsoft Dynamics 365 Commerce“ peržiūros versijos „Yammer“ grupėje](https://aka.ms/Dynamics365CommercePreviewYammer) dėl pagalbos.</span><span class="sxs-lookup"><span data-stu-id="3c933-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="3c933-286">Jei, bandant pasiekti „Yammer“ grupę, kyla problemų, su „Microsoft“ galite susisiekti el. pašto adresu <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="3c933-286">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="3c933-287">Šis el. pašto adresas nėra aktyviai stebimas.</span><span class="sxs-lookup"><span data-stu-id="3c933-287">This email address isn't actively monitored.</span></span> <span data-ttu-id="3c933-288">Todėl atsakyti galime ne iš karto.</span><span class="sxs-lookup"><span data-stu-id="3c933-288">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3c933-289">Kiti veiksmai</span><span class="sxs-lookup"><span data-stu-id="3c933-289">Next steps</span></span>

<span data-ttu-id="3c933-290">Norėdami tęsti „Commerce“ peržiūros aplinkos parengimo ir konfigūravimo procesą, žr. skyrių [„Commerce“ peržiūros aplinkos konfigūravimas](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="3c933-290">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c933-291">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3c933-291">Additional resources</span></span>

[<span data-ttu-id="3c933-292">„Dynamics 365 Commerce“peržiūros aplinkos apžvalga</span><span class="sxs-lookup"><span data-stu-id="3c933-292">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="3c933-293">„Dynamics 365 Commerce“ peržiūros aplinkos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="3c933-293">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="3c933-294">„Dynamics 365 Commerce“ peržiūros aplinkos pasirinktinių funkcijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="3c933-294">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="3c933-295">„Dynamics 365 Commerce“peržiūros aplinkos DUK</span><span class="sxs-lookup"><span data-stu-id="3c933-295">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="3c933-296">„Microsoft Lifecycle Services“ (LCS)</span><span class="sxs-lookup"><span data-stu-id="3c933-296">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="3c933-297">„Retail Cloud Scale Unit“ (RCSU)</span><span class="sxs-lookup"><span data-stu-id="3c933-297">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="3c933-298">„Microsoft Azure“ portalas</span><span class="sxs-lookup"><span data-stu-id="3c933-298">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="3c933-299">„Dynamics 365 Commerce“ svetainė</span><span class="sxs-lookup"><span data-stu-id="3c933-299">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

