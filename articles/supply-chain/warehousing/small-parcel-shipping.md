---
title: Mažų siuntinių siuntimas
description: Šioje temoje pateikiama informacija apie mažų siuntinių siuntimo (angl. SPS) funkciją. Ši funkcija leidžia „Microsoft Dynamics 365 Supply Chain Management” pateikti informaciją apie supakuotą konteinerį vežėjui ir gauti siuntimo žymę, siuntimo įkainį ir vežėjo pateiktą sekimo numerį.
author: Mirzaab
manager: tfehr
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 37f07139853c30da25c067a3d736b4b9bf4eb361
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501179"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="8752f-104">Mažų siuntinių siuntimas</span><span class="sxs-lookup"><span data-stu-id="8752f-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8752f-105">Mažų siuntinių siuntimo (SPS) funkcija leidžia „Microsoft Dynamics 365 Supply Chain Management” sąveikauti su siuntimo vežėjais per vežėjų API susisiekimo sistemą.</span><span class="sxs-lookup"><span data-stu-id="8752f-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="8752f-106">Ši funkcija naudinga, kai pavienius pardavimo užsakymus siųsite per komercinius vežėjus, o ne rinksitės konteinerio siuntimą, ar ne viso pakrovimo (LTL) siuntimą.</span><span class="sxs-lookup"><span data-stu-id="8752f-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="8752f-107">SPS funkcija sąveikauja su jūsų siuntinio vežėju per skirtą *Tarifų mechanizmas*.</span><span class="sxs-lookup"><span data-stu-id="8752f-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="8752f-108">Jūsų organizacija turi sukurti šį tarifo mechanizmą bendradarbiaujant su jūsų vežėju arba vežėjų centrų tarnyba.</span><span class="sxs-lookup"><span data-stu-id="8752f-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="8752f-109">Šis tarifų mechanizmas leidžia „Supply Chain Management” pateikti informaciją apie supakuotą konteinerį jūsų vežėjui ir gauti siuntimo etiketę, siuntimo įkainį ir vežėjo pateiktą sekimo numerį.</span><span class="sxs-lookup"><span data-stu-id="8752f-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="8752f-110">Grąžintas siuntimo tarifas įtraukiamas į susietą pardavimo užsakymą kaip papildomas mokestis.</span><span class="sxs-lookup"><span data-stu-id="8752f-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="8752f-111">Grąžintą siuntimo žymę galima automatiškai išspausdinti naudojant „Zebra” programavimo kalbos (ZPK) spausdintuvą ir pritaikyti siuntai.</span><span class="sxs-lookup"><span data-stu-id="8752f-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="8752f-112">Vežėjas nuskaitys šią siuntimo žymą, kai paima paketus iš jūsų sandėlio.</span><span class="sxs-lookup"><span data-stu-id="8752f-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="8752f-113">Paruoškite sistemą palaikyti SPS</span><span class="sxs-lookup"><span data-stu-id="8752f-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="8752f-114">Prieš pradedant naudotis SPS funkcija, turite įjungti SPS funkciją Funkcijų valdymo dalyje, pridėkite tarifų variklį, ir nustatykite **Transportavimo valdymas** ir **Sandėlio valdymas** modulius jam palaikyti.</span><span class="sxs-lookup"><span data-stu-id="8752f-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="8752f-115">SPS funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="8752f-115">Turn on the SPS feature</span></span>

<span data-ttu-id="8752f-116">Prieš naudodami SPS funkciją, turite ją įjungti savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="8752f-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="8752f-117">Administratoriai gali naudoti [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo erdvę tam, kad patikrintų funkcijos būseną, ir jei būtina, ją įjungtų.</span><span class="sxs-lookup"><span data-stu-id="8752f-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="8752f-118">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="8752f-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="8752f-119">**Modulis:** *Gabenimo valdymas*</span><span class="sxs-lookup"><span data-stu-id="8752f-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="8752f-120">**Funkcijos pavadinimas:** *Mažų siuntinių siuntimas*</span><span class="sxs-lookup"><span data-stu-id="8752f-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="8752f-121">Tarifų mechanizmo įdiegimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8752f-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="8752f-122">„Supply Chain Management” neapima jokių tarifų mechanizmų.</span><span class="sxs-lookup"><span data-stu-id="8752f-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="8752f-123">Turite įsigyti arba sukurti bet kuriuos tarifų modulius, kurių jums reikia, ir įtraukti juos į savo sistemą.</span><span class="sxs-lookup"><span data-stu-id="8752f-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="8752f-124">Tačiau „Microsoft” suteikia demonstracinę tarifų mechanizmo versiją, kurią galite naudoti testavimui.</span><span class="sxs-lookup"><span data-stu-id="8752f-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="8752f-125">Demonstracinės tarifų mechanizmo versijos atsisiuntimas ir įdiegimas</span><span class="sxs-lookup"><span data-stu-id="8752f-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="8752f-126">Norėdami gauti demonstracinę tarifų mechanizmo versiją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8752f-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="8752f-127">„GitHub” atsisiųskite [dinaminę saitų biblioteką (angl. DLL), skirtą demonstracinei tarifų mechanizmo versijai](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span><span class="sxs-lookup"><span data-stu-id="8752f-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="8752f-128">„Supply Chain Management” serveryje įrašykite DLL aplanke **\\AOSService\\ PackagesLocalDirectory\\ Application Dll\\bin**.</span><span class="sxs-lookup"><span data-stu-id="8752f-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="8752f-129">Funkcinių tarifų mechanizmų kūrimas ir diegimas</span><span class="sxs-lookup"><span data-stu-id="8752f-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="8752f-130">Informacijos apie tai, kaip sukurti ir įdiegti funkcinių tarifų mechanizmus, kad juos būtų galima naudoti gamybos arba tikrinimo aplinkoje, ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="8752f-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="8752f-131">Naujo transportavimo valdymo mechanizmo kūrimas</span><span class="sxs-lookup"><span data-stu-id="8752f-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="8752f-132">Transportavimo valdymo mechanizmų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8752f-132">Set up transportation management engines</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="8752f-133">Daugiau informacijos apie tai, kaip sukurti SPS tarifų mechanizmą, rasite šiame tinklaraščio įraše: [Mažų siuntinių siuntimas: kaip pagerinti mažų siuntinių siuntimo funkciją „Microsoft Dynamics 365”](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span><span class="sxs-lookup"><span data-stu-id="8752f-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="8752f-134">Tarifų mechanizmo konfigūravimas „Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="8752f-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="8752f-135">Sukūrę ir įdiegę SPS tarifų mechanizmą, atlikite šiuos veiksmus, norėdami jį nustatyti.</span><span class="sxs-lookup"><span data-stu-id="8752f-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="8752f-136">Eikite į **Transportavimo valdymas \> Sąranka \> Mechanizmai \> Tarifo mechanizmas**.</span><span class="sxs-lookup"><span data-stu-id="8752f-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="8752f-137">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="8752f-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="8752f-138">Naujoje eilutėje nustatykite šiuos laukus:</span><span class="sxs-lookup"><span data-stu-id="8752f-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="8752f-139">**Vertinimo mechanizmas** – įveskite unikalų tarifo mechanizmo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="8752f-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="8752f-140">Jei naudojate demonstracinę tarifo mechanizmo versiją, įveskite *Demonstracinė tarifo mechanizmo versija*.</span><span class="sxs-lookup"><span data-stu-id="8752f-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="8752f-141">**Pavadinimas** – įveskite trumpą tarifo mechanizmo aprašą.</span><span class="sxs-lookup"><span data-stu-id="8752f-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="8752f-142">Jei naudojate demonstracinę tarifo mechanizmo versiją, įveskite *Demonstracinė tarifo mechanizmo versija*.</span><span class="sxs-lookup"><span data-stu-id="8752f-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="8752f-143">**Vertinimo metaduomenų ID** – pasirinkite pagrindą, kuris turėtų būti naudojamas skaičiuojant tarifą.</span><span class="sxs-lookup"><span data-stu-id="8752f-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="8752f-144">Pavyzdžiui, jūsų tarifas gali būti apskaičiuojamas pagal atstumą.</span><span class="sxs-lookup"><span data-stu-id="8752f-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="8752f-145">Jei naudojate demonstracine tarifo mechanizmo versija, galite palikti šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="8752f-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="8752f-146">**Mechanizmo rinkinys** – įveskite įdiegto DLL paketo failo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="8752f-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="8752f-147">Jei naudojate demonstracinę tarifo mechanizmo versiją, įveskite *TMSSmallParcelShippingEngine.dll*.</span><span class="sxs-lookup"><span data-stu-id="8752f-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="8752f-148">**Mechanizmo klasė** – įveskite klasės pavadinimą, kuri buvo sukurta jūsų jūsų tarifo mechanizmui.</span><span class="sxs-lookup"><span data-stu-id="8752f-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="8752f-149">Jei naudojate demonstracinę tarifo mechanizmo versiją, įveskite *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span><span class="sxs-lookup"><span data-stu-id="8752f-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="8752f-150">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="8752f-150">Example scenario</span></span>

<span data-ttu-id="8752f-151">Šis pavyzdys rodo, kaip nustatyti ir naudoti SPS, kai jau paruošėte savo sistemą, kaip aprašyta anksčiau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="8752f-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="8752f-152">Šiame scenarijuje naudojamas anksčiau minėta demonstracinės tarifo mechanizmo versija.</span><span class="sxs-lookup"><span data-stu-id="8752f-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="8752f-153">Demonstracinių duomenų įgalinimas</span><span class="sxs-lookup"><span data-stu-id="8752f-153">Make demo data available</span></span>

<span data-ttu-id="8752f-154">Norėdami dirbti pagal šį scenarijų, naudojant čia nurodytus demonstracinius įrašus ir vertes, turite būti sistemoje, kurioje įdiegti standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8752f-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="8752f-155">Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="8752f-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="8752f-156">Scenarijaus nustatymas</span><span class="sxs-lookup"><span data-stu-id="8752f-156">Set up the scenario</span></span>

<span data-ttu-id="8752f-157">Šiame pavyzdyje scenarijuje turite turėti demonstracinį vežėją, vežėjų grupę, pakavimo strategiją ir pakavimo profilį.</span><span class="sxs-lookup"><span data-stu-id="8752f-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="8752f-158">Šiuose poskyriuose paaiškinama, kaip paruošti įrašus, reikalingus scenarijui.</span><span class="sxs-lookup"><span data-stu-id="8752f-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="8752f-159">Gamybos scenarijuje nustatymo procesas paprastai yra panašus į čia apibūdintą procesą.</span><span class="sxs-lookup"><span data-stu-id="8752f-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="8752f-160">Tačiau jūs nustatote skirtingas vertes.</span><span class="sxs-lookup"><span data-stu-id="8752f-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="8752f-161">Siuntų vežėjų nustatymas</span><span class="sxs-lookup"><span data-stu-id="8752f-161">Set up carriers</span></span>

<span data-ttu-id="8752f-162">Atlikite šiuos veiksmus vežėjui nustatyti.</span><span class="sxs-lookup"><span data-stu-id="8752f-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="8752f-163">Eikite į **Transportavimo valdymas \> Nustatymas \> Vežėjai \> Siuntų vežėjai**.</span><span class="sxs-lookup"><span data-stu-id="8752f-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="8752f-164">Veiksmų srityje pasirinkite **Nauja**, norėdami vežėją.</span><span class="sxs-lookup"><span data-stu-id="8752f-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="8752f-165">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="8752f-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="8752f-166">**Siuntimo vežėjas:** *Demonstracinis vežėjas*</span><span class="sxs-lookup"><span data-stu-id="8752f-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="8752f-167">**Pavadinimas:** *Demonstracinis vežėjas*</span><span class="sxs-lookup"><span data-stu-id="8752f-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="8752f-168">**Režimas:** *Žeme*</span><span class="sxs-lookup"><span data-stu-id="8752f-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="8752f-169">**Peržiūros** „FastTab“, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="8752f-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="8752f-170">**Aktyvuoti siuntimo vežėją:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="8752f-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="8752f-171">**Aktyvuoti siuntimo vertinimą:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="8752f-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="8752f-172">„FastTab“ skirtuke **Paslaugos** pasirinkite **Nauja**, kad pridėtumėte paslaugą į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="8752f-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="8752f-173">Nustatykite šias naujos paslaugos vertes:</span><span class="sxs-lookup"><span data-stu-id="8752f-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="8752f-174">**Vežėjo paslauga:** *Demonstracinio vežėjo paslauga*</span><span class="sxs-lookup"><span data-stu-id="8752f-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="8752f-175">**Pavadinimas:** *Demonstracinio vežėjo paslauga*</span><span class="sxs-lookup"><span data-stu-id="8752f-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="8752f-176">**Transportavimo būdas:** *Žeme*</span><span class="sxs-lookup"><span data-stu-id="8752f-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="8752f-177">Jei reikia, įveskite visų kitų laukų sutartines vertes.</span><span class="sxs-lookup"><span data-stu-id="8752f-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="8752f-178">(Kai įrašote naują siuntimo vežėjo įrašą, bus sukurtas naujas pristatymo būdas ir **Pristatymo režimas** laukas bus nustatytas automatiškai.)</span><span class="sxs-lookup"><span data-stu-id="8752f-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="8752f-179">„FastTab“ skirtuke **Vertinimo profiliai** rinkitės **Naujas**, kad sukurtumėte įvertinimų profilį tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="8752f-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="8752f-180">Nustatykite šias naujo profilio vertes:</span><span class="sxs-lookup"><span data-stu-id="8752f-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="8752f-181">**Įvertinimo šablonas:** *Demonstracinių vežėjų paslauga*</span><span class="sxs-lookup"><span data-stu-id="8752f-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="8752f-182">**Pavadinimas:** *Demonstracinio vežėjo paslauga*</span><span class="sxs-lookup"><span data-stu-id="8752f-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="8752f-183">**Tarifo mechanizmas** *Demonstracinis tarifų mechanizmas*</span><span class="sxs-lookup"><span data-stu-id="8752f-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="8752f-184">Jei reikia, įveskite visų kitų laukų sutartines vertes.</span><span class="sxs-lookup"><span data-stu-id="8752f-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="8752f-185">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="8752f-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="8752f-186">Daugiau informacijos apie tai, kaip nustatyti vežėjus, ieškokite [Siuntimo vežėjų nustatymas](../transportation/tasks/set-up-shipping-carriers.md).</span><span class="sxs-lookup"><span data-stu-id="8752f-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="8752f-187">Vežėjų paslaugų sąskaitų nustatymas</span><span class="sxs-lookup"><span data-stu-id="8752f-187">Set up carrier service accounts</span></span>

<span data-ttu-id="8752f-188">Atlikite šiuos veiksmus, kad sukonfigūruotumėte vežėjo paslaugos sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="8752f-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="8752f-189">Eikite į **Transportavimo valdymas \> Sąranka \> Įvertinimas \> Vežėjų paslaugos sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="8752f-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="8752f-190">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte vežėjo paslaugos sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="8752f-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="8752f-191">Nustatykite šias naujos sąskaitos vertes:</span><span class="sxs-lookup"><span data-stu-id="8752f-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="8752f-192">**Siuntimo vežėjas:** *Demonstracinis vežėjas*</span><span class="sxs-lookup"><span data-stu-id="8752f-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="8752f-193">**Vežėjo paslauga:** *Demonstracinio vežėjo paslauga*</span><span class="sxs-lookup"><span data-stu-id="8752f-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="8752f-194">**Vežėjo kliento sąskaitos numeris:** Vežėjo kliento sąskaitos numeris, naudojamas patikrinti ir autentifikuoti ryšį su siuntos vežėju.</span><span class="sxs-lookup"><span data-stu-id="8752f-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="8752f-195">Jūsų vežėjas teiks šią vertę.</span><span class="sxs-lookup"><span data-stu-id="8752f-195">Your carrier will provide this value.</span></span> <span data-ttu-id="8752f-196">Jei naudojate demonstracinę paslaugą, galite įvesti sutartinę vertę.</span><span class="sxs-lookup"><span data-stu-id="8752f-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="8752f-197">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="8752f-197">**Site:** *6*</span></span>
    - <span data-ttu-id="8752f-198">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="8752f-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="8752f-199">Dažnai **Vežėjo kliento sąskaitos numeris** yra vienintelė vertė, reikalinga autentifikuoti ryšį.</span><span class="sxs-lookup"><span data-stu-id="8752f-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="8752f-200">Tačiau jei jūsų vežėjui reikia papildomų autentifikavimo parametrų, jūsų organizacija turi pritaikyti šį puslapį, kad būtų atitinkamai pridėti papildomi laukai.</span><span class="sxs-lookup"><span data-stu-id="8752f-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="8752f-201">Konteinerio pakavimo strategijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="8752f-201">Set up a container packing policy</span></span>

<span data-ttu-id="8752f-202">Norėdami nustatyti konteinerio pakavimo strategiją, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8752f-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="8752f-203">Jei dar nenustatėte ZPL spausdintuvo apibrėžimo, norėdami jį nustatyti, naudokite Dokumento maršruto agento programą.</span><span class="sxs-lookup"><span data-stu-id="8752f-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="8752f-204">Daugiau informacijos žr. [Dokumentų spausdinimo apžvalga](../../fin-ops-core/dev-itpro/analytics/print-documents.md) ir susijusiose temose.</span><span class="sxs-lookup"><span data-stu-id="8752f-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="8752f-205">Eikite į **Sandėlio tvarkymas \> Sąranka \> Konteineriai \> Konteinerių pakavimo strategijos**.</span><span class="sxs-lookup"><span data-stu-id="8752f-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="8752f-206">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte konteinerio pakavimo strategiją.</span><span class="sxs-lookup"><span data-stu-id="8752f-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="8752f-207">Naujosios strategijos antraštėje, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="8752f-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="8752f-208">**Konteinerio pakavimo strategija:** *Demonstracinė pakavimo strategija*</span><span class="sxs-lookup"><span data-stu-id="8752f-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="8752f-209">**Aprašas:** Strategijos aprašas</span><span class="sxs-lookup"><span data-stu-id="8752f-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="8752f-210">**Peržiūros** „FastTab“, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="8752f-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="8752f-211">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="8752f-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="8752f-212">**Numatytoji galutinės siuntos vieta:** *Įlankos vartai*</span><span class="sxs-lookup"><span data-stu-id="8752f-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="8752f-213">**Svorio vienetas:** *kg*</span><span class="sxs-lookup"><span data-stu-id="8752f-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="8752f-214">**Talpyklos uždarymo politika:** *Automatinis išleidimas*</span><span class="sxs-lookup"><span data-stu-id="8752f-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="8752f-215">**Konteinerio išleidimo strategija:** *Pasiekiama galutinėje siuntimo vietoje*</span><span class="sxs-lookup"><span data-stu-id="8752f-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="8752f-216">„FastTab“ **Konteinerio deklaracija** nustatykite šias vertes.</span><span class="sxs-lookup"><span data-stu-id="8752f-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="8752f-217">**Automatinė deklaracija uždarius konteinerį:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="8752f-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="8752f-218">**Konteinerio deklaracijos reikalavimai:** *Transportavimo valdymas*</span><span class="sxs-lookup"><span data-stu-id="8752f-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="8752f-219">**Spausdinti konteinerių turinį:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="8752f-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="8752f-220">„FastTab“ **Siuntėjo žymos spausdinimas** nustatykite šias vertes.</span><span class="sxs-lookup"><span data-stu-id="8752f-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="8752f-221">**Spausdinti konteinerio siuntimo žymą:** *Visada*</span><span class="sxs-lookup"><span data-stu-id="8752f-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="8752f-222">**Spausdintuvo pavadinimas:** ZPL spausdintuvo, kuris turėtų spausdinti siuntimo žymas, pavadinimas</span><span class="sxs-lookup"><span data-stu-id="8752f-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="8752f-223">Pakavimo šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="8752f-223">Set up a packing profile</span></span>

<span data-ttu-id="8752f-224">Norėdami nustatyti pakavimo profilį, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="8752f-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="8752f-225">Eikite į **Sandėlio valdymas \> Sąranka \> Pakavimas \> Pakavimo profiliai**.</span><span class="sxs-lookup"><span data-stu-id="8752f-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="8752f-226">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte pakavimo profilį į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="8752f-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="8752f-227">Nustatykite šias naujo profilio vertes:</span><span class="sxs-lookup"><span data-stu-id="8752f-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="8752f-228">**Pakavimo profilio ID:** *Demonstracinis pakavimo profilis*</span><span class="sxs-lookup"><span data-stu-id="8752f-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="8752f-229">**Aprašas:** Profilio aprašas</span><span class="sxs-lookup"><span data-stu-id="8752f-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="8752f-230">**Konteinerio pakavimo strategija:** *Demonstracinė pakavimo strategija*</span><span class="sxs-lookup"><span data-stu-id="8752f-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="8752f-231">**Talpyklos identifikavimo numerio režimas:** *Automatinis*</span><span class="sxs-lookup"><span data-stu-id="8752f-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="8752f-232">**Konteinerio tipas:** *Maža dėžutė*</span><span class="sxs-lookup"><span data-stu-id="8752f-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="8752f-233">Nustatykite klientą, kad pasirinktumėte SPS vežėją</span><span class="sxs-lookup"><span data-stu-id="8752f-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="8752f-234">Norėdami nustatyti klientą, kad jis galėtų pasirinkti jūsų sukurtą vežėją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8752f-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="8752f-235">Eikite į **Gautos sąskaitos \> klientai \> Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="8752f-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="8752f-236">Tinklelyje suraskite ir pasirinkite *US-027*.</span><span class="sxs-lookup"><span data-stu-id="8752f-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="8752f-237">Veiksmų srities skirtuko **Bendra** **Nustatyti** pasirinkite **Vežėjo klientų sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="8752f-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="8752f-238">Vežėjo **Vežėjo klientų sąskaitos** puslapyje, veiksmų srityje, pasirinkite **Nauja**, kad pridėtumėte sąskaitą tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="8752f-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="8752f-239">Nustatykite šias naujos sąskaitos vertes:</span><span class="sxs-lookup"><span data-stu-id="8752f-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="8752f-240">**Siuntimo vežėjas:** *Demonstracinis vežėjas*</span><span class="sxs-lookup"><span data-stu-id="8752f-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="8752f-241">**Vežėjo kliento sąskaitos numeris:** *12345* (vertė šiame scenarijuje nėra svarbi, tačiau ji bus reikalinga kitame skyriuje.)</span><span class="sxs-lookup"><span data-stu-id="8752f-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="8752f-242">Pereikite per scenarijaus pavyzdį</span><span class="sxs-lookup"><span data-stu-id="8752f-242">Go through the example scenario</span></span>

<span data-ttu-id="8752f-243">Nustatę visus duomenų pavyzdžius, kaip aprašyta ankstesniame skyriuje, esate pasiruošę naudoti pavyzdinį scenarijų.</span><span class="sxs-lookup"><span data-stu-id="8752f-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="8752f-244">Pardavimo užsakymo sukūrimas ir darbo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="8752f-244">Create a sales order and process the work</span></span>

<span data-ttu-id="8752f-245">Norėdami sukurti pardavimo užsakymą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8752f-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="8752f-246">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="8752f-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="8752f-247">Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="8752f-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="8752f-248">Dialogo lango **Kurti pardavimo užsakymą** lauke nustatykite **Kliento paskyra** lauką į *US-027*.</span><span class="sxs-lookup"><span data-stu-id="8752f-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="8752f-249">Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="8752f-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="8752f-250">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="8752f-250">The new sales order is opened.</span></span> <span data-ttu-id="8752f-251">„FastTab” skirtuke **Pardavimo užsakymo antraštė** nustatykite lauke **Vežėjo kliento sąskaitos numeris** jūsų anksčiau šiam klientui (*12345*) pasirinktą vertę.</span><span class="sxs-lookup"><span data-stu-id="8752f-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="8752f-252">Dalyje **Pardavimo užsakymo eilutės** pridėkite pardavimų eilutę ir nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="8752f-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="8752f-253">**Prekės numeris:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="8752f-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="8752f-254">**Kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="8752f-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="8752f-255">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="8752f-255">**Site:** *6*</span></span>
    - <span data-ttu-id="8752f-256">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="8752f-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="8752f-257">Perjunkite **Antraštės** rodinį.</span><span class="sxs-lookup"><span data-stu-id="8752f-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="8752f-258">„FastTab” skirtuke **Pristatymas** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="8752f-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="8752f-259">**Siuntimo vežėjas:** *Demonstracinis vežėjas*</span><span class="sxs-lookup"><span data-stu-id="8752f-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="8752f-260">**Vežėjo paslauga:** *Demonstracinio vežėjo paslauga*</span><span class="sxs-lookup"><span data-stu-id="8752f-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="8752f-261">Grįžkite į **Eilučių** rodinį.</span><span class="sxs-lookup"><span data-stu-id="8752f-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="8752f-262">Jei būsite paraginti atnaujinti pardavimo eilučių pristatymo būdą, pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="8752f-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="8752f-263">Dalyje **Pardavimų užsakymų eilutės** pasirinkite jūsų anksčiau nustatytą užsakymo eilutę ir pasirinkite **Atsargos \> Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="8752f-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="8752f-264">Puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** rezervuoti visam pasirinktos eilutės kiekiui sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="8752f-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="8752f-265">Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="8752f-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="8752f-266">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="8752f-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="8752f-267">Sukurtas darbas, skirtas prekėms iš paėmimo vietos į pakavimo stotį perkelti.</span><span class="sxs-lookup"><span data-stu-id="8752f-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="8752f-268">Dalyje **Pardavimų užsakymų eilutės** pasirinkite **Sandėlis \> Siuntimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="8752f-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="8752f-269">**Siuntimo informacija** puslapyje pateikite pastabą apie siuntos ID.</span><span class="sxs-lookup"><span data-stu-id="8752f-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="8752f-270">Jums jos prireiks, kai pakuosite siuntinį pakavimo stotyje.</span><span class="sxs-lookup"><span data-stu-id="8752f-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="8752f-271">Uždarykite **Siuntimo informacija** puslapį, kad sugrįžtumėte į pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="8752f-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="8752f-272">Pasižymėkite pardavimo užsakymo numerį, tada eikite į **Sandėlio valdymas \>Darbas \> Visi darbai**.</span><span class="sxs-lookup"><span data-stu-id="8752f-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="8752f-273">Pardavimo užsakymo numerį naudokite surasti ir pasirinkti užsakymui sukurtą darbą.</span><span class="sxs-lookup"><span data-stu-id="8752f-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="8752f-274">Veiksmų srityje, **Darbas** skirtuke, pasirinkite **Visas darbas**.</span><span class="sxs-lookup"><span data-stu-id="8752f-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="8752f-275">**Darbo užbaigimas** puslapyje **Vartotojo ID** pasirinkite vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="8752f-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="8752f-276">Tada veiksmų srityje pasirinkite **Patvirtinti darbą**.</span><span class="sxs-lookup"><span data-stu-id="8752f-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="8752f-277">Jei darbas patvirtinamas, veiksmų srityje pasirinkite **Baigti darbą**.</span><span class="sxs-lookup"><span data-stu-id="8752f-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="8752f-278">Darbas pažymimas kaip baigtas, modeliuojant prekių judėjimą į pakavimo stotį.</span><span class="sxs-lookup"><span data-stu-id="8752f-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="8752f-279">Siuntos pakavimas</span><span class="sxs-lookup"><span data-stu-id="8752f-279">Pack the shipment</span></span>

<span data-ttu-id="8752f-280">Norėdami supakuoti siuntą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8752f-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="8752f-281">Eikite į **Sandėlio valdymas \> Sąranka \> Darbuotojas** ir įsitikinkite, kad sandėlio valdymui vartotojo paskyra yra susieta su darbuotojo paskyra.</span><span class="sxs-lookup"><span data-stu-id="8752f-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="8752f-282">Eikite į **Sandėlio valdymas \> Atsiėmimas ir talpinimas į konteinerį \> Pakuoti**.</span><span class="sxs-lookup"><span data-stu-id="8752f-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="8752f-283">Dialogo lange **Pasirinkite pakavimo stotį** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="8752f-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="8752f-284">**Vieta:** *6*</span><span class="sxs-lookup"><span data-stu-id="8752f-284">**Site:** *6*</span></span>
    - <span data-ttu-id="8752f-285">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="8752f-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="8752f-286">**Vieta:** *Pakavimas*</span><span class="sxs-lookup"><span data-stu-id="8752f-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="8752f-287">**Pakavimo profilio ID:** *Demonstracinis pakavimo profilis*</span><span class="sxs-lookup"><span data-stu-id="8752f-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="8752f-288">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8752f-288">Select **OK**.</span></span>
1. <span data-ttu-id="8752f-289">Pasirodo puslapis **Pakuoti**.</span><span class="sxs-lookup"><span data-stu-id="8752f-289">The **Pack** page appears.</span></span> <span data-ttu-id="8752f-290">Gamybos scenarijuje darbuotojas nuskaitys numerio lentelę arba siuntos ID.</span><span class="sxs-lookup"><span data-stu-id="8752f-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="8752f-291">Tačiau šiam scenarijui atidarykite **Visos siuntos** puslapį ir suraskite jūsų sukurtos siuntos numerį.</span><span class="sxs-lookup"><span data-stu-id="8752f-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="8752f-292">Tada įveskite šią vertę lauke **Numerio lentelė arba siunta** **Pakuoti** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="8752f-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="8752f-293">Kitu atveju įveskite anksčiau pasižymėtos siuntos ID.</span><span class="sxs-lookup"><span data-stu-id="8752f-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="8752f-294">Veiksmų juostoje pasirinkite **Naujas talpykla**.</span><span class="sxs-lookup"><span data-stu-id="8752f-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="8752f-295">Dialogo lange rodoma išsami informacija apie naują konteinerį.</span><span class="sxs-lookup"><span data-stu-id="8752f-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="8752f-296">Palikite numatytąsias reikšmes, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8752f-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="8752f-297">**Pakuoti** puslapyje **Prekės pakavimas** „FastTab” skirtuke pasirinkite **Identifikatorius** lauką, pasirinkite *A0002*, kad supakuotumėte prekę.</span><span class="sxs-lookup"><span data-stu-id="8752f-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="8752f-298">Prekė pridėta į konteinerį.</span><span class="sxs-lookup"><span data-stu-id="8752f-298">The item is added to the container.</span></span>
1. <span data-ttu-id="8752f-299">Veiksmų srityje pasirinkite **Konteineriai siuntai**.</span><span class="sxs-lookup"><span data-stu-id="8752f-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="8752f-300">Pasirodžiusiame **Konteineriai siuntai** puslapyje pateikiama jūsų sukurta eilutė.</span><span class="sxs-lookup"><span data-stu-id="8752f-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="8752f-301">Tačiau **Konteinerių deklaracijos ID** laukas eilutėje šiuo metu yra tuščias, nes negavote siuntimo žymos ir sekimo numerio iš vežėjo.</span><span class="sxs-lookup"><span data-stu-id="8752f-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="8752f-302">Veiksmų juostoje pasirinkite **Uždaryti talpyklą**.</span><span class="sxs-lookup"><span data-stu-id="8752f-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="8752f-303">Dialogo lange **Uždaryti konteinerį** nustatykite **Bruto svoris** lauką į *1 kg* ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8752f-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="8752f-304">Siuntimo žymė dabar turi būti išspausdinta ant anksčiau pasirinkto ZPL spausdintuvo.</span><span class="sxs-lookup"><span data-stu-id="8752f-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="8752f-305">Ji turi atitikti šį pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="8752f-305">It should resemble the following example.</span></span>

    <span data-ttu-id="8752f-306">![Siuntimo žymės pavyzdys](media/sps-label-example.png "Siuntimo žymės pavyzdys")</span><span class="sxs-lookup"><span data-stu-id="8752f-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="8752f-307">Atkreipkite dėmesį, kad **Konteinerio deklaracijos ID** ir **Bendras krovinys** vertės pridėtos tokios, kokios gautos iš vežėjo.</span><span class="sxs-lookup"><span data-stu-id="8752f-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]