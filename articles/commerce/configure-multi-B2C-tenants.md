---
title: Kelių B2C nuomotojų konfigūravimas „Commerce“ aplinkoje
description: Šioje temoje aprašoma, kada ir kaip viename kanale nustatyti kelis „Microsoft Azure Active Directory“ („Azure AD“) verslas–vartotojui (B2C) nuomotojus, skirtus vartotojo autentifikavimui paskirtoje „Dynamics 365 Commerce“ aplinkoje.
author: BrianShook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: c813adb79ae1b78a052332e077393f125830633f
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027727"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="24608-103">Kelių B2C nuomotojų konfigūravimas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="24608-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="24608-104">Šioje temoje aprašoma, kada ir kaip viename kanale nustatyti kelis „Microsoft Azure Active Directory“ („Azure AD“) verslas–vartotojui (B2C) nuomotojus, skirtus vartotojo autentifikavimui paskirtoje „Dynamics 365 Commerce“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="24608-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="24608-105">„Dynamics 365 Commerce“ naudoja „Azure AD“ B2C debesies tapatumo paslaugą vartotojo kredencialams ir autentifikavimo srautams palaikyti.</span><span class="sxs-lookup"><span data-stu-id="24608-105">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="24608-106">Vartotojai gali naudoti autentifikavimo srautus, norėdami prisiregistruoti, prisijungti ir nustatyti slaptažodį iš naujo.</span><span class="sxs-lookup"><span data-stu-id="24608-106">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="24608-107">„Azure AD B2C“ saugoma vartotojo slapto autentifikavimo informacija, pvz., vartotojo vardas ir slaptažodis.</span><span class="sxs-lookup"><span data-stu-id="24608-107">Azure AD B2C stores a user's sensitive authentication information, such as the user name and password.</span></span> <span data-ttu-id="24608-108">Vartotojo įrašas yra unikalus kiekvienam B2C nuomotojui ir naudoja vartotojo vardą (el. pašto adresą), kredencialus arba socialinės tapatybės teikimo įrankio kredencialus.</span><span class="sxs-lookup"><span data-stu-id="24608-108">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="24608-109">Daugeliu atveju „Commerce“ aplinkoje naudojamas vienas „Azure AD“ B2C nuomotojas.</span><span class="sxs-lookup"><span data-stu-id="24608-109">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="24608-110">„Commerce“ klientai gali kurti ir publikuoti kelias svetaines toje pačioje „Commerce“ aplinkoje, o šiose svetainėse bus naudojami tie patys kliento kredencialai.</span><span class="sxs-lookup"><span data-stu-id="24608-110">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="24608-111">Tačiau jei aplinkoje esančios svetainės turi būti traktuojamos kaip skirtingi prekių ženklai ir rodomos vartotojams kaip atskiros įmonės, B2C nuomotoją galima sukonfigūruoti kanalui, kuris naudojamas svetainės / prekės ženklo atskyrimui.</span><span class="sxs-lookup"><span data-stu-id="24608-111">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="24608-112">Aplinkybės, kai vienam kanalui nustatyti keli B2C nuomotojai</span><span class="sxs-lookup"><span data-stu-id="24608-112">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="24608-113">Dažnai, kai kiekvienas kanalas ar svetainė traktuojami kaip atskiros įmonės, vartotojo autentifikavimo srautų „Commerce“ aplinkoje atžvilgiu geriausia yra naudoti atskirus juridinius subjektus.</span><span class="sxs-lookup"><span data-stu-id="24608-113">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="24608-114">Tačiau jei norite, kad kiekvienas kanalas / svetainė liktų toje pačioje aplinkoje ir juridiniame subjekte, bet kiekviena svetainė turėtų atskirą vartotojo autentifikavimą, svarbu, kad prieš tęsdami atsižvelgtumėte į šiuos punktus:</span><span class="sxs-lookup"><span data-stu-id="24608-114">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="24608-115">Vartotojai turės savo individualius kredencialus kiekvienam kanalui / svetainei.</span><span class="sxs-lookup"><span data-stu-id="24608-115">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="24608-116">Tas pats asmuo gali turėti dvi atskiras kiekvieno kanalo / svetainės paskyras, nes kiekviena paskyra bus unikalus įrašas atskiram B2C nuomotojui.</span><span class="sxs-lookup"><span data-stu-id="24608-116">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="24608-117">„Microsoft Dynamics“ aplinkoje į visuotines įrašų paieškas bus sugrąžinti atskiri kliento įrašai.</span><span class="sxs-lookup"><span data-stu-id="24608-117">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="24608-118">Jei vartotojas naudoja tą patį el. pašto adresą kanaluose / svetainėse, visuotinės klientų paieškos sugrąžins kiekvieno kanalo / svetainės rezultatus.</span><span class="sxs-lookup"><span data-stu-id="24608-118">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="24608-119">(Bus rodomas kanalo indikatorius.)</span><span class="sxs-lookup"><span data-stu-id="24608-119">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="24608-120">Adresų knygelė gali būti naudojama vartotojams grupuoti, kad juos būtų galima sekti per kanalą.</span><span class="sxs-lookup"><span data-stu-id="24608-120">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="24608-121">Kliento įrašų skaičius kanalui gali padidėti, o šis padidinimas gali paveikti visuotinių klientų paieškų efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="24608-121">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="24608-122">B2C nuomotojai turi būti rūpestingai susieti su kanalu siekiant padėti išvengti situacijų, kai klientai užsiregistruoja prie klaidingo nuomotojo.</span><span class="sxs-lookup"><span data-stu-id="24608-122">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="24608-123">Kitu atveju gali kilti neaiškumų arba sekimo problemų.</span><span class="sxs-lookup"><span data-stu-id="24608-123">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="24608-124">Toliau pateiktoje iliustracijoje parodomi keli B2C nuomotojai „Commerce“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="24608-124">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![Keli B2C nuomotojai „Commerce“ aplinkoje](media/MultiB2C_In_Environment.png)

<span data-ttu-id="24608-126">Jei nuspręsite, kad jūsų verslui reikia individualių B2C nuomotojų vienam kanalui toje pačioje „Commerce“ aplinkoje, atlikite tolesniuose skyriuose esančias procedūras, kad galėtumėte užklausti šią funkciją.</span><span class="sxs-lookup"><span data-stu-id="24608-126">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="24608-127">B2C nuomotojų konfigūravimas savo aplinkoje</span><span class="sxs-lookup"><span data-stu-id="24608-127">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="24608-128">Norėdami sukonfigūruoti B2C nuomotojus savo aplinkoje, atlikite atitinkamas procedūras šiame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="24608-128">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="24608-129">„Azure AD“ B2C nuomotojo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="24608-129">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="24608-130">Norėdami pridėti „Azure AD“ B2C nuomotoją prie savo aplinkos, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="24608-130">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="24608-131">Prisijunkite prie savo aplinkos „Commerce“ svetainės kūrimo įrankio kaip sistemos administratorius. Norėdami sukonfigūruoti „Azure AD“ B2C nuomotojus, turite būti „Commerce“ sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="24608-131">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="24608-132">Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Nuomotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="24608-132">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="24608-133">Pasirinkite **B2C parametrai**, tada pasirinkite **Valdyti**.</span><span class="sxs-lookup"><span data-stu-id="24608-133">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="24608-134">Pasirinkite **Įtraukti B2C programą**, o tada įveskite šią informaciją:</span><span class="sxs-lookup"><span data-stu-id="24608-134">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="24608-135">**Programos pavadinimas**: įveskite pavadinimą, kuris turi būti naudojamas programoje valdymo „Commerce“ aplinkoje kontekste.</span><span class="sxs-lookup"><span data-stu-id="24608-135">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="24608-136">Rekomenduojame naudoti programos pavadinimą, kurį pasirinkote nustatydami „Azure AD“ B2C programą „Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="24608-136">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="24608-137">Tokiu būdu galite padėti išvengti neaiškumų, kai valdote B2C nuomotojus „Commerce“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="24608-137">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="24608-138">**Nuomotojo vardas**: įveskite B2C nuomotojo pavadinimą, kaip jis rodomas „Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="24608-138">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="24608-139">**Pamiršti slaptažodžio strategijos ID**: įveskite strategijos ID (strategijos pavadinimą „Azure“ portale).</span><span class="sxs-lookup"><span data-stu-id="24608-139">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="24608-140">**Registruoti / prijungti strategijos ID**: įveskite strategijos ID (strategijos pavadinimą „Azure“ portale).</span><span class="sxs-lookup"><span data-stu-id="24608-140">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="24608-141">**Kliento GUID**: įveskite „Azure AD“ B2C nuomotojo ID, kaip jis rodomas „Azure“ portale (ne programos ID B2C nuomotojui).</span><span class="sxs-lookup"><span data-stu-id="24608-141">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="24608-142">**Redaguoti profilio strategijos ID**: įveskite strategijos ID (strategijos pavadinimą „Azure“ portale).</span><span class="sxs-lookup"><span data-stu-id="24608-142">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="24608-143">Įvedę šią informaciją, pasirinkite **Gerai**, kad įrašytumėte pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="24608-143">When you've finished entering this information, select **OK** to save your changes.</span></span> <span data-ttu-id="24608-144">Dabar jūsų naujas „Azure AD“ B2C nuomotojas turi pasirodyti sąraše po **Tvarkyti B2C programas**.</span><span class="sxs-lookup"><span data-stu-id="24608-144">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

> [!NOTE]
> <span data-ttu-id="24608-145">Turite palikti laukus, pvz., **Aprėptis**, **Neinteraktyvios strategijos ID**, **Neinteraktyvaus kliento ID**, **Prisijungimo pasirinktinis domenas** ir **Registruoti strategijos ID**, tuščius, nebent „Dynamics 365 Commerce“ komanda nurodo jas nustatyti.</span><span class="sxs-lookup"><span data-stu-id="24608-145">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>


### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="24608-146">„Azure AD“ B2C nuomotojo tvarkymas arba naikinimas</span><span class="sxs-lookup"><span data-stu-id="24608-146">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="24608-147">Prisijunkite prie savo aplinkos „Commerce“ svetainės kūrimo įrankio kaip sistemos administratorius. Norėdami sukonfigūruoti „Azure AD“ B2C nuomotojus, turite būti „Commerce“ sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="24608-147">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="24608-148">Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Nuomotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="24608-148">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="24608-149">Pasirinkite **B2C parametrai**, tada pasirinkite **Valdyti**.</span><span class="sxs-lookup"><span data-stu-id="24608-149">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="24608-150">Norėdami redaguoti B2C nuomotoją, pasirinkite šalia jo esantį pieštuko simbolį.</span><span class="sxs-lookup"><span data-stu-id="24608-150">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="24608-151">Norėdami panaikinti B2C nuomotoją, pasirinkite šalia jo esantį šiukšliadėžės simbolį.</span><span class="sxs-lookup"><span data-stu-id="24608-151">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="24608-152">Norėdami suaktyvinti savo keitimus, paspauskite **Įrašyti** ir pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="24608-152">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="24608-153">Kai B2C nuomotojas sukonfigūruotas paleistoje / publikuotoje svetainėje, vartotojai gali būti prisiregistravę naudojant su nuomotoju esančias paskyras.</span><span class="sxs-lookup"><span data-stu-id="24608-153">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="24608-154">Jei panaikinsite sukonfigūruotą nuomotoją meniu **Nuomotojo parametrai\> B2C nuomotojas**, jūs pašalinsite to B2C nuomotojo svetainių, kurios susietos su bet kuriuo nuomotojo kanalu, susiejimą.</span><span class="sxs-lookup"><span data-stu-id="24608-154">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="24608-155">Šiuo atveju vartotojai gali nebegalėti prisijungti prie savo paskyrų.</span><span class="sxs-lookup"><span data-stu-id="24608-155">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="24608-156">Todėl kai panaikinate sukonfigūruotą nuomotoją, būkite itin atsargūs.</span><span class="sxs-lookup"><span data-stu-id="24608-156">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="24608-157">Kai sukonfigūruotas nuomotojas panaikinamas, B2C nuomotojas ir jo įrašai bus išlaikyti, tačiau to nuomotojo „Commerce“ sistemos konfigūracija bus pakeista arba pašalinta.</span><span class="sxs-lookup"><span data-stu-id="24608-157">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="24608-158">Vartotojai, kurie bando užsiregistruoti ar prisijungti prie svetainės, sukurs naują paskyros įrašą numatytame arba naujai susietame B2C, kuris sukonfigūruotas svetainės kanalui.</span><span class="sxs-lookup"><span data-stu-id="24608-158">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>

## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="24608-159">Savo kanalo konfigūravimas su B2C nuomotoju</span><span class="sxs-lookup"><span data-stu-id="24608-159">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="24608-160">Prisijunkite prie savo aplinkos „Commerce“ svetainės kūrimo įrankio kaip sistemos administratorius. Norėdami sukonfigūruoti „Azure AD“ B2C nuomotojus, turite būti „Commerce“ sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="24608-160">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="24608-161">Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Svetainės parametrai**.</span><span class="sxs-lookup"><span data-stu-id="24608-161">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="24608-162">Pasirinkite **Kanalai** ir pasirinkite kanalą, kurį norite konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="24608-162">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="24608-163">Dešinėje esančioje ypatybių srityje esančiame lauke **Pasirinkti B2C programą** pasirinkite sukonfigūruotą „Azure AD“ B2C nuomotoją, kurį norite naudoti šiam kanalui.</span><span class="sxs-lookup"><span data-stu-id="24608-163">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="24608-164">Komandų juostoje pasirinkite **Įrašyti ir publikuoti**, kad patvirtintumėte naują arba atnaujintą konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="24608-164">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="24608-165">Pakeitus B2C programą, priskirtą kanalui, pašalinamos dabartinės nuorodos, kurios buvo nustatytos visiems vartotojams, kurie jau yra užsiregistravę aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="24608-165">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="24608-166">Šiuo atveju bet kokie kredencialai, susieti su šiuo metu priskirta B2C programa, nebus prieinami vartotojams.</span><span class="sxs-lookup"><span data-stu-id="24608-166">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="24608-167">Todėl keiskite kanalo „Azure AD“ B2C konfigūraciją tik jei nustatote kanalą pirmą kartą ir nėra užsiregistravusių vartotojų.</span><span class="sxs-lookup"><span data-stu-id="24608-167">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="24608-168">Kitu atveju vartotojams gali reikėti registruotis iš naujo, kad būtų sukurtas įrašas naujame „Azure AD“ B2C nuomotoje.</span><span class="sxs-lookup"><span data-stu-id="24608-168">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="24608-169">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="24608-169">Additional resources</span></span>

[<span data-ttu-id="24608-170">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="24608-170">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="24608-171">Talpinkite naują e-komercijos nuomotoją</span><span class="sxs-lookup"><span data-stu-id="24608-171">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="24608-172">Sukurkite e-komercijos saitą</span><span class="sxs-lookup"><span data-stu-id="24608-172">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="24608-173">Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu</span><span class="sxs-lookup"><span data-stu-id="24608-173">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="24608-174">robots.txt failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="24608-174">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="24608-175">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="24608-175">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="24608-176">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="24608-176">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="24608-177">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="24608-177">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="24608-178">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="24608-178">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="24608-179">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="24608-179">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
