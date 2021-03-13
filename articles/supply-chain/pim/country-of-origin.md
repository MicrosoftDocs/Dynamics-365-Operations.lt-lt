---
title: Kilmės šalis / regionas
description: Daugelis organizacijų išduoda sertifikatus savo pardavėjams tam, kad užtikrintų, jog jų produktai atitiktų sertifikato standartus. Šie sertifikatai dažnai priklauso nuo kilmės šalies. Šiame skyriuje pateikiama informacija apie kilmės šalies savybes, kurios leidžia jums susieti gaminį su jo kilmės šalimi ir sekti gaminių sertifikatus.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 2eaf0057123cd2cbcad00f95038627291dada517
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007820"
---
# <a name="country-of-origin"></a><span data-ttu-id="1013d-105">Kilmės šalis / regionas</span><span class="sxs-lookup"><span data-stu-id="1013d-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="1013d-106">Daugelis organizacijų išduoda sertifikatus savo pardavėjams tam, kad užtikrintų, jog jų produktai atitiktų sertifikato standartus.</span><span class="sxs-lookup"><span data-stu-id="1013d-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="1013d-107">Šie sertifikatai dažnai priklauso nuo kilmės šalies.</span><span class="sxs-lookup"><span data-stu-id="1013d-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="1013d-108">Kilmės šalies savybės leidžia jums susieti gaminį su jo kilmės šalimi ir sekti gaminių sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="1013d-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="1013d-109">Kilmės šalies funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="1013d-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="1013d-110">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="1013d-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="1013d-111">Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją.</span><span class="sxs-lookup"><span data-stu-id="1013d-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="1013d-112">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="1013d-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1013d-113">**Modulis:** *Produkto informacijos valdymas*</span><span class="sxs-lookup"><span data-stu-id="1013d-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="1013d-114">**Funkcijos pavadinimas:** *Kilmės šalies tvarkymo funkcija*</span><span class="sxs-lookup"><span data-stu-id="1013d-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="1013d-115">Konfigūruoti šaltinį ir paskirties šalis</span><span class="sxs-lookup"><span data-stu-id="1013d-115">Configure source and destination countries</span></span>

<span data-ttu-id="1013d-116">Prieš jums išduodant sertifikatą gaminiui privalo susieti jį su jo paskirties šalimi ir kilmės šalimi.</span><span class="sxs-lookup"><span data-stu-id="1013d-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="1013d-117">Eikite į **Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Kilmės šalis \> Kilmės šalies taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="1013d-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="1013d-118">Pasirinkite esančią šalies sąranką redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujos šalies sąranką.</span><span class="sxs-lookup"><span data-stu-id="1013d-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="1013d-119">Naujosios politikos antraštėje, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="1013d-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="1013d-120">Laukas</span><span class="sxs-lookup"><span data-stu-id="1013d-120">Field</span></span> | <span data-ttu-id="1013d-121">aprašymas</span><span class="sxs-lookup"><span data-stu-id="1013d-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="1013d-122">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="1013d-122">Item number</span></span> | <span data-ttu-id="1013d-123">Pasirinkite elemento gaminio numerį.</span><span class="sxs-lookup"><span data-stu-id="1013d-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="1013d-124">Paskirties šalis</span><span class="sxs-lookup"><span data-stu-id="1013d-124">Destination country</span></span> | <span data-ttu-id="1013d-125">Pasirinkite šalį, į kurią siunčiate gaminį.</span><span class="sxs-lookup"><span data-stu-id="1013d-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="1013d-126">Kilmės šalis</span><span class="sxs-lookup"><span data-stu-id="1013d-126">Origin country</span></span> | <span data-ttu-id="1013d-127">Pasirinkite šalį, iš kurios siunčiate gaminį.</span><span class="sxs-lookup"><span data-stu-id="1013d-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="1013d-128">Šios sąrankos tikslas yra padėti jums sukurti medžiagų sąskaitos (BOM) ataskaitą, į kurią galite įtraukti kilmės šalį kiekvienai daliai, kuriai yra nustatytas šaltinis ir paskirties šalis.</span><span class="sxs-lookup"><span data-stu-id="1013d-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="1013d-129">Ši sąskaita padės jums gauti bendrą paveikslėlį, kuriame matysite, iš kur ateina jūsų dalys ir kur jos eina.</span><span class="sxs-lookup"><span data-stu-id="1013d-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="1013d-130">Sekite pardavėjų sertifikatus</span><span class="sxs-lookup"><span data-stu-id="1013d-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="1013d-131">Galite naudoti **Kilmės šalies pardavėjo sertifikatų** puslapį tam, kad sektumėte sertifikatus, kuriuos išduodate pardavėjams.</span><span class="sxs-lookup"><span data-stu-id="1013d-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="1013d-132">Privalote nuspręsti, kuriuos sertifikato dokumentus išduodate ir kaip apie juos pranešite klientams.</span><span class="sxs-lookup"><span data-stu-id="1013d-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="1013d-133">Ši funkcija padeda jums sekti jūsų sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="1013d-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="1013d-134">Ji taip pat padeda jums pasirinkti, ar atitinkami sertifikato numeriai bus rodomi sąskaitose, pakavimo lapeliuose ir (arba) užsakymo patvirtinimuose.</span><span class="sxs-lookup"><span data-stu-id="1013d-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="1013d-135">Sertifikato informacijos nustatymui, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="1013d-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="1013d-136">Eikite į **Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Kilmės šalis \> Pardavėjo kilmės šalies sertifikatai**.</span><span class="sxs-lookup"><span data-stu-id="1013d-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="1013d-137">Pasirinkite esančią sertifikato sąranką redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujo sertifikato sąranką.</span><span class="sxs-lookup"><span data-stu-id="1013d-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="1013d-138">Naujam ar pasirinktam sertifikatui nustatykite šiuose nustatymus.</span><span class="sxs-lookup"><span data-stu-id="1013d-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="1013d-139">Laukas</span><span class="sxs-lookup"><span data-stu-id="1013d-139">Field</span></span> | <span data-ttu-id="1013d-140">aprašymas</span><span class="sxs-lookup"><span data-stu-id="1013d-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="1013d-141">Tiekėjo kodas</span><span class="sxs-lookup"><span data-stu-id="1013d-141">Vendor account</span></span> | <span data-ttu-id="1013d-142">Pasirinkite pardavėją, kuriam išdavėte sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="1013d-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="1013d-143">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="1013d-143">Item number</span></span> | <span data-ttu-id="1013d-144">Pasirinkite elementą, kuriam išdavėte sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="1013d-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="1013d-145">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="1013d-145">Country/region</span></span> | <span data-ttu-id="1013d-146">Paskirties šalis ar regionas, kuriame privalote naudoti šį sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="1013d-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="1013d-147">Sertifikato numeris</span><span class="sxs-lookup"><span data-stu-id="1013d-147">Certificate number</span></span> | <span data-ttu-id="1013d-148">Įveskite jūsų išduoto sertifikato identifikavimo numerį.</span><span class="sxs-lookup"><span data-stu-id="1013d-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="1013d-149">Galioja</span><span class="sxs-lookup"><span data-stu-id="1013d-149">Effective</span></span> | <span data-ttu-id="1013d-150">Pasirinkite pirmą datą, kai esamas sertifikatas galioja.</span><span class="sxs-lookup"><span data-stu-id="1013d-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="1013d-151">Galiojimas</span><span class="sxs-lookup"><span data-stu-id="1013d-151">Expiration</span></span> | <span data-ttu-id="1013d-152">Pasirinkite paskutinę datą, kai esamas sertifikatas galioja.</span><span class="sxs-lookup"><span data-stu-id="1013d-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="1013d-153">Atspausdinkite sąskaitą</span><span class="sxs-lookup"><span data-stu-id="1013d-153">Print on invoice</span></span> | <span data-ttu-id="1013d-154">Pasirinkite žymimą laukelį, kad atspausdintumėte sertifikato numerį sąskaitose, kurios yra siunčiamos konkrečiai šaliai nurodytų duomenų intervale.</span><span class="sxs-lookup"><span data-stu-id="1013d-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="1013d-155">Atspausdinkite pakavimo lipduką</span><span class="sxs-lookup"><span data-stu-id="1013d-155">Print on packing slip</span></span> | <span data-ttu-id="1013d-156">Pasirinkite žymimą laukelį, kad atspausdintumėte pakavimo lipdukų numerį sąskaitose, kurios yra siunčiamos konkrečiai šaliai nurodytų duomenų intervale.</span><span class="sxs-lookup"><span data-stu-id="1013d-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="1013d-157">Prekybos užsakymo spausdinimas</span><span class="sxs-lookup"><span data-stu-id="1013d-157">Print on sales order</span></span> | <span data-ttu-id="1013d-158">Pasirinkite žymimą laukelį, kad atspausdintumėte sertifikato numerį ar prekybos užsakymus, kurie yra siunčiami konkrečiai šaliai nurodytų duomenų intervale.</span><span class="sxs-lookup"><span data-stu-id="1013d-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="1013d-159">Įtraukite kilmės šalį į BOM ataskaitas</span><span class="sxs-lookup"><span data-stu-id="1013d-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="1013d-160">Kai sukuriate BOM ataskaitą, galite įtraukti kilmės šalį kiekvienai daliai, kurią nurodėte šaltinyje ir kilmės šalyse **Kilmės šalies taisyklės** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="1013d-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="1013d-161">Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="1013d-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1013d-162">Pasirinkite ar sukurkite produktą, kad atidarytumėte jo **Išleisto produkto informacija** puslapį.</span><span class="sxs-lookup"><span data-stu-id="1013d-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="1013d-163">Veiksmų juostoje, **Inžinierius** skirtuke, **BOM** grupėje, pasirinkite **Projektuotojas**.</span><span class="sxs-lookup"><span data-stu-id="1013d-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="1013d-164">Pasirodžiusiame puslapyje Veiksmų juostoje pasirinkite **BOM \> Spausdinti**.</span><span class="sxs-lookup"><span data-stu-id="1013d-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="1013d-165">**Medžiagų linijų sąskaitos** teksto lange nustatykite **Paskirties šalies** laukelį į paskirties šalį, kurią norite peržiūrėti savo ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="1013d-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="1013d-166">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1013d-166">Select **OK**.</span></span>

<span data-ttu-id="1013d-167">Informaciją pateikianti ataskaita apie kiekvienos dalies kilmės šalį yra sukuriama ir rodoma.</span><span class="sxs-lookup"><span data-stu-id="1013d-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="1013d-168">Čia pateikiamas ataskaitos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="1013d-168">Here is an example of the report.</span></span>

<span data-ttu-id="1013d-169">![Kilmės šalies ataskaita](media/country-of-origin-report.png "Kilmės šalies ataskaita")</span><span class="sxs-lookup"><span data-stu-id="1013d-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
