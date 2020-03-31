---
title: Autentifikavimas
description: Šiame straipsnyje pateikiama peržiūros informacija apie tai, kaip autentifikuoti „Microsoft Dynamics 365 Human Resources“ duomenų taikomojo programavimo sąsają (API).
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a0509ce99205d49d516e180203ffb65a1dc09a7c
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092111"
---
# <a name="authentication"></a><span data-ttu-id="9c1f1-103">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="9c1f1-103">Authentication</span></span>

<span data-ttu-id="9c1f1-104">Šiame straipsnyje pateikiama peržiūros informacija apie tai, kaip autentifikuoti „Microsoft Dynamics 365 Human Resources“ duomenų taikomojo programavimo sąsają (API).</span><span class="sxs-lookup"><span data-stu-id="9c1f1-104">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="9c1f1-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="9c1f1-105">Overview</span></span>

<span data-ttu-id="9c1f1-106">„Human Resources“ skirta duomenų API yra „OData“ diegimas.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-106">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="9c1f1-107">Daugiau informacijos žr. [„Open Data Protocol“ („OData“)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="9c1f1-107">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="9c1f1-108">Jūsų programą reikia autentifikuoti kaip įgaliotą kvietyklę, kad API galėtų atsakyti į užklausas, gautas iš jūsų programos.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-108">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="9c1f1-109">Pagrindai</span><span class="sxs-lookup"><span data-stu-id="9c1f1-109">Fundamentals</span></span>

<span data-ttu-id="9c1f1-110">Siekiant iškviesti duomenų API, programa turi gauti „Microsoft“ tapatumo platformos prieigos atpažinimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-110">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="9c1f1-111">Prieigos atpažinimo ženkle yra informacija apie jūsų programą ir teisė iškviesti „Human Resources“ išteklius.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-111">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="9c1f1-112">Prieigos atpažinimo ženklas</span><span class="sxs-lookup"><span data-stu-id="9c1f1-112">Access token</span></span>

<span data-ttu-id="9c1f1-113">„Microsoft“ tapatumo platformos išduodami prieigos atpažinimo ženklai yra base64 užkoduoti „JavaScript Object Notation“ (JSON) žiniatinklio atpažinimo ženklai (JWT).</span><span class="sxs-lookup"><span data-stu-id="9c1f1-113">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="9c1f1-114">Jose yra informacija (paraiškos), kad duomenų API (ir kitos žiniatinklio API, saugomos „Microsoft“ tapatumo platformos) yra naudojamos kvietyklei patvirtinti ir įsitikinti, kad kvietyklė turi tinkamas teises prašomai operacijai atlikti.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-114">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="9c1f1-115">Skambučių metu galite laikyti prieigos atpažinimo ženklus nepermatomais.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-115">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="9c1f1-116">Prieigos atpažinimo ženklus visada turite perduoti saugiais kanalais, tokiais kaip transportavimo lygmens sauga (TLS) ir Hypertext Transfer Protocol Secure (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="9c1f1-116">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="9c1f1-117">Čia yra prieigos atpažinimo ženklo, kurį išdavė „Microsoft“ tapatumo platforma, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-117">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="9c1f1-118">Norėdami iškviesti duomenų API, pridėkite prieigos atpažinimo ženklą kaip pateikėjo atpažinimo ženklą prie autorizavimo antraštės savo HTTP užklausoje.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-118">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="9c1f1-119">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-119">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="9c1f1-120">Naudodami „Azure“ portalą, užregistruokite naują programą</span><span class="sxs-lookup"><span data-stu-id="9c1f1-120">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="9c1f1-121">Prisijunkite prie [„Microsoft Azure“ portalo](https://portal.azure.com) naudodami darbo ar mokyklos paskyrą arba asmeninę „Microsoft“ paskyrą.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-121">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="9c1f1-122">Jeigu jūsų paskyra suteikia prieigą prie daugiau nei vieno nuomotojo, viršutiniame dešiniajame kampe pasirinkite savo paskyrą ir nustatykite portalo sesiją į norimą „Azure Active Directory“ („Azure AD“) nuomotoją.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-122">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="9c1f1-123">Kairiojoje srityje pasirinkite paslaugą **„Azure Active Directory“**, tada pasirinkite **Programų registracijos \>Nauja registracija**.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-123">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="9c1f1-124">Kai pasirodys puslapis **Registruoti programą**, įveskite programos registracijos informaciją:</span><span class="sxs-lookup"><span data-stu-id="9c1f1-124">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="9c1f1-125">**Pavadinimas**: įveskite prasmingą programos pavadinimą, kuris bus rodomas programos vartotojams.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-125">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="9c1f1-126">**Palaikomi paskyrų tipai**: pasirinkite paskyrų tipus, kuriuos turi palaikyti programa.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-126">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="9c1f1-127">Palaikomi sąskaitų tipai</span><span class="sxs-lookup"><span data-stu-id="9c1f1-127">Supported account types</span></span> | <span data-ttu-id="9c1f1-128">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="9c1f1-128">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="9c1f1-129">Paskyros tik šiame organizaciniame kataloge</span><span class="sxs-lookup"><span data-stu-id="9c1f1-129">Accounts in this organizational directory only</span></span> | <span data-ttu-id="9c1f1-130">Pasirinkite šią pasirinktį, jei kuriate verslui skirtą programą.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-130">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="9c1f1-131">Ši parinktis pasiekiama tik tuo atveju, jei registruojate programą kataloge.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-131">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="9c1f1-132">Ši parinktis susieta tik su **vienu „Azure AD“ nuomotoju**.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-132">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="9c1f1-133">Ši parinktis yra numatytoji parinktis, nebent registruojate programą ne kataloge.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-133">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="9c1f1-134">Tokiu atveju numatytoji parinktis yra kelių nuomotojų **„Azure AD“ ir asmeninės „Microsoft“ paskyros**.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-134">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="9c1f1-135">Paskyros bet kokiame organizaciniame kataloge</span><span class="sxs-lookup"><span data-stu-id="9c1f1-135">Accounts in any organizational directory</span></span> | <span data-ttu-id="9c1f1-136">Pasirinkite šią parinktį, norėdami tiksline auditorija pasirinkti visus verslo ir mokslo klientus.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-136">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="9c1f1-137">Ši parinktis susieta tik su **keliais „Azure AD“ nuomotojais**.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-137">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="9c1f1-138">Jei užregistravote programą kaip **tik vieno nuomotojo „Azure AD“**, galite naudoti mentę **Autentifikavimas**, kad atnaujintumėte ją į **tik kelių nuomotojų „Azure AD“**, o tada vėl į **tik vieno nuomotojo „Azure AD“**.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-138">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="9c1f1-139">Bet kokio organizacinio katalogo paskyros ir asmeninės „Microsoft“ paskyros</span><span class="sxs-lookup"><span data-stu-id="9c1f1-139">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="9c1f1-140">Pasirinkite šia parinktį, kad tiksline auditorija pasirinktumėte didžiausią klientų grupę.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-140">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="9c1f1-141">Ši parinktis yra susieta su **kelių nuomotojų „Azure AD“ ir asmeninėmis „Microsoft“ paskyromis**.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-141">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="9c1f1-142">Jei užregistravę programą kaip **Kelių nuomotojų „Azure AD“ ir asmeninės „MIcrosoft“ paskyros**, negalite keisti šio parametro vartotojo sąsajoje (UI).</span><span class="sxs-lookup"><span data-stu-id="9c1f1-142">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="9c1f1-143">Vietoj to, turite naudoti programos deklaracijos doroklį, kad pakeistumėte palaikomus paskyrų tipus.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-143">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="9c1f1-144">**Nukreipimo URI (pasirinktinai)** – pasirinkite, kokio tipo programą kuriate: **Žiniatinklio** ar **Viešojo kliento (skirta mobiliesiems įrenginiams ir asmeniniams kompiuteriams)**.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-144">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="9c1f1-145">Tada įveskite programos nukreipimo URI (arba atsakymo URL).</span><span class="sxs-lookup"><span data-stu-id="9c1f1-145">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="9c1f1-146">Norėdami naudoti žiniatinklio programas, nurodykite pagrindinį programos URL.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-146">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="9c1f1-147">Pavyzdžiui, `http://localhost:31544`gali būti jūsų vietiniame kompiuteryje veikiančios žiniatinklio programos URL.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-147">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="9c1f1-148">Tada vartotojai naudoja šį URL, kad prisijungtų prie žiniatinklio kliento programos.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-148">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="9c1f1-149">Norėdami naudoti viešojo kliento programas, nurodykite URI, kurį „Azure AD“ naudoja, kad atsilieptų į atpažinimo ženklų atsakymus.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-149">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="9c1f1-150">Įveskite savo programai būdingą vertę, pvz., `myapp://auth`.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-150">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="9c1f1-151">Norėdami pamatyti konkrečius pavyzdžius, susijusius su žiniatinklio programomis ir vietinėmis programomis, žr. greitąjį pasirengimą darbui[ „Microsoft“ tapatumo platformoje (anksčiau vadinamoje „Azure Active Directory“, skirta kūrėjams)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span><span class="sxs-lookup"><span data-stu-id="9c1f1-151">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="9c1f1-152">Dalyje **API teisės**pasirinkite **Įtraukti teisę**.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-152">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="9c1f1-153">Tada skirtuke **Mano organizacijoje naudojamos API**, ieškokite **„Dynamics 365 Human Resources“** ir pridėkite teisę **vartotojas\_apsimetimas** prie savo programos.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-153">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="9c1f1-154">„Human Resources“ programos ID yra f9be0c49-aa22-4ec6-911a-c5da515226ff.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-154">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="9c1f1-155">Naudokite šį ID norėdami įsitikinti, kad pasirinkote tinkamą programą.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-155">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="9c1f1-156">Pasirinkite **Registruotis**.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-156">Select **Register**.</span></span>

   <span data-ttu-id="9c1f1-157">[![Naujos programos registravimas „Azure“ portale](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="9c1f1-157">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="9c1f1-158">„Azure AD“ priskiria jūsų programai unikalų programos ID (kliento ID) ir perkelia jus į programos puslapį **Apžvalga**.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-158">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="9c1f1-159">Norėdami pridėti daugiau galimybių prie programos, galite pasirinkti kitas konfigūravimo parinktis, pvz., prekių ženklų, sertifikatų ir slaptųjų raktų parinktis.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-159">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="9c1f1-160">Prieigos atpažinimo ženklo nuskaitymas</span><span class="sxs-lookup"><span data-stu-id="9c1f1-160">Retrieving an access token</span></span>

<span data-ttu-id="9c1f1-161">Konkreti informacija apie tai, kaip nuskaityti prieigos atpažinimo ženklą, kad būtų galima iškviesti „Human Resources“ duomenų API, priklausys nuo to, kokiomis technologijomis naudojatės kurdami kliento programą.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-161">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="9c1f1-162">Pavyzdžiui, galbūt [bandote trečiosios šalies priemonę](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (pvz., „Postman“), kuriate C# konsolės programą ar žiniatinklio paslaugą arba kuriate javascript / TypeScript klientą.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-162">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="9c1f1-163">C# kliento programos pavyzdys:</span><span class="sxs-lookup"><span data-stu-id="9c1f1-163">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="9c1f1-164">Nuskaitę prieigos atpažinimo ženklą, perduosite šį ženklą autorizavimo antraštėje kaip pateikėjo atpažinimo ženklą kartu su kiekviena užklausa, kurią siunčiate duomenų API, kaip aprašyta anksčiau.</span><span class="sxs-lookup"><span data-stu-id="9c1f1-164">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>