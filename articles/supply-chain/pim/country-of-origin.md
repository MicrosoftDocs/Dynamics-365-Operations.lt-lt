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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0471785991a307de11147e9773d9abe1e02941d6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433257"
---
# <a name="country-of-origin"></a><span data-ttu-id="36454-105">Kilmės šalis / regionas</span><span class="sxs-lookup"><span data-stu-id="36454-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="36454-106">Daugelis organizacijų išduoda sertifikatus savo pardavėjams tam, kad užtikrintų, jog jų produktai atitiktų sertifikato standartus.</span><span class="sxs-lookup"><span data-stu-id="36454-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="36454-107">Šie sertifikatai dažnai priklauso nuo kilmės šalies.</span><span class="sxs-lookup"><span data-stu-id="36454-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="36454-108">Kilmės šalies savybės leidžia jums susieti gaminį su jo kilmės šalimi ir sekti gaminių sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="36454-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="36454-109">Kilmės šalies funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="36454-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="36454-110">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="36454-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="36454-111">Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją.</span><span class="sxs-lookup"><span data-stu-id="36454-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="36454-112">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="36454-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="36454-113">**Modulis:** *Produkto informacijos valdymas*</span><span class="sxs-lookup"><span data-stu-id="36454-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="36454-114">**Funkcijos pavadinimas:** *Kilmės šalies tvarkymo funkcija*</span><span class="sxs-lookup"><span data-stu-id="36454-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="36454-115">Konfigūruoti šaltinį ir paskirties šalis</span><span class="sxs-lookup"><span data-stu-id="36454-115">Configure source and destination countries</span></span>

<span data-ttu-id="36454-116">Prieš jums išduodant sertifikatą gaminiui privalo susieti jį su jo paskirties šalimi ir kilmės šalimi.</span><span class="sxs-lookup"><span data-stu-id="36454-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="36454-117">Eikite į **Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Kilmės šalis \> Kilmės šalies taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="36454-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="36454-118">Pasirinkite esančią šalies sąranką redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujos šalies sąranką.</span><span class="sxs-lookup"><span data-stu-id="36454-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="36454-119">Naujosios politikos antraštėje, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="36454-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="36454-120">Laukas</span><span class="sxs-lookup"><span data-stu-id="36454-120">Field</span></span> | <span data-ttu-id="36454-121">aprašymas</span><span class="sxs-lookup"><span data-stu-id="36454-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="36454-122">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="36454-122">Item number</span></span> | <span data-ttu-id="36454-123">Pasirinkite elemento gaminio numerį.</span><span class="sxs-lookup"><span data-stu-id="36454-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="36454-124">Paskirties šalis</span><span class="sxs-lookup"><span data-stu-id="36454-124">Destination country</span></span> | <span data-ttu-id="36454-125">Pasirinkite šalį, į kurią siunčiate gaminį.</span><span class="sxs-lookup"><span data-stu-id="36454-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="36454-126">Kilmės šalis</span><span class="sxs-lookup"><span data-stu-id="36454-126">Origin country</span></span> | <span data-ttu-id="36454-127">Pasirinkite šalį, iš kurios siunčiate gaminį.</span><span class="sxs-lookup"><span data-stu-id="36454-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="36454-128">Šios sąrankos tikslas yra padėti jums sukurti medžiagų sąskaitos (BOM) ataskaitą, į kurią galite įtraukti kilmės šalį kiekvienai daliai, kuriai yra nustatytas šaltinis ir paskirties šalis.</span><span class="sxs-lookup"><span data-stu-id="36454-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="36454-129">Ši sąskaita padės jums gauti bendrą paveikslėlį, kuriame matysite, iš kur ateina jūsų dalys ir kur jos eina.</span><span class="sxs-lookup"><span data-stu-id="36454-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="36454-130">Sekite pardavėjų sertifikatus</span><span class="sxs-lookup"><span data-stu-id="36454-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="36454-131">Galite naudoti **Kilmės šalies pardavėjo sertifikatų** puslapį tam, kad sektumėte sertifikatus, kuriuos išduodate pardavėjams.</span><span class="sxs-lookup"><span data-stu-id="36454-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="36454-132">Privalote nuspręsti, kuriuos sertifikato dokumentus išduodate ir kaip apie juos pranešite klientams.</span><span class="sxs-lookup"><span data-stu-id="36454-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="36454-133">Ši funkcija padeda jums sekti jūsų sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="36454-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="36454-134">Ji taip pat padeda jums pasirinkti, ar atitinkami sertifikato numeriai bus rodomi sąskaitose, pakavimo lapeliuose ir (arba) užsakymo patvirtinimuose.</span><span class="sxs-lookup"><span data-stu-id="36454-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="36454-135">Sertifikato informacijos nustatymui, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="36454-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="36454-136">Eikite į **Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Kilmės šalis \> Pardavėjo kilmės šalies sertifikatai**.</span><span class="sxs-lookup"><span data-stu-id="36454-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="36454-137">Pasirinkite esančią sertifikato sąranką redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujo sertifikato sąranką.</span><span class="sxs-lookup"><span data-stu-id="36454-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="36454-138">Naujam ar pasirinktam sertifikatui nustatykite šiuose nustatymus.</span><span class="sxs-lookup"><span data-stu-id="36454-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="36454-139">Laukas</span><span class="sxs-lookup"><span data-stu-id="36454-139">Field</span></span> | <span data-ttu-id="36454-140">aprašymas</span><span class="sxs-lookup"><span data-stu-id="36454-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="36454-141">Tiekėjo kodas</span><span class="sxs-lookup"><span data-stu-id="36454-141">Vendor account</span></span> | <span data-ttu-id="36454-142">Pasirinkite pardavėją, kuriam išdavėte sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="36454-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="36454-143">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="36454-143">Item number</span></span> | <span data-ttu-id="36454-144">Pasirinkite elementą, kuriam išdavėte sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="36454-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="36454-145">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="36454-145">Country/region</span></span> | <span data-ttu-id="36454-146">Paskirties šalis ar regionas, kuriame privalote naudoti šį sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="36454-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="36454-147">Sertifikato numeris</span><span class="sxs-lookup"><span data-stu-id="36454-147">Certificate number</span></span> | <span data-ttu-id="36454-148">Įveskite jūsų išduoto sertifikato identifikavimo numerį.</span><span class="sxs-lookup"><span data-stu-id="36454-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="36454-149">Galioja</span><span class="sxs-lookup"><span data-stu-id="36454-149">Effective</span></span> | <span data-ttu-id="36454-150">Pasirinkite pirmą datą, kai esamas sertifikatas galioja.</span><span class="sxs-lookup"><span data-stu-id="36454-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="36454-151">Galiojimas</span><span class="sxs-lookup"><span data-stu-id="36454-151">Expiration</span></span> | <span data-ttu-id="36454-152">Pasirinkite paskutinę datą, kai esamas sertifikatas galioja.</span><span class="sxs-lookup"><span data-stu-id="36454-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="36454-153">Atspausdinkite sąskaitą</span><span class="sxs-lookup"><span data-stu-id="36454-153">Print on invoice</span></span> | <span data-ttu-id="36454-154">Pasirinkite žymimą laukelį, kad atspausdintumėte sertifikato numerį sąskaitose, kurios yra siunčiamos konkrečiai šaliai nurodytų duomenų intervale.</span><span class="sxs-lookup"><span data-stu-id="36454-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="36454-155">Atspausdinkite pakavimo lipduką</span><span class="sxs-lookup"><span data-stu-id="36454-155">Print on packing slip</span></span> | <span data-ttu-id="36454-156">Pasirinkite žymimą laukelį, kad atspausdintumėte pakavimo lipdukų numerį sąskaitose, kurios yra siunčiamos konkrečiai šaliai nurodytų duomenų intervale.</span><span class="sxs-lookup"><span data-stu-id="36454-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="36454-157">Prekybos užsakymo spausdinimas</span><span class="sxs-lookup"><span data-stu-id="36454-157">Print on sales order</span></span> | <span data-ttu-id="36454-158">Pasirinkite žymimą laukelį, kad atspausdintumėte sertifikato numerį ar prekybos užsakymus, kurie yra siunčiami konkrečiai šaliai nurodytų duomenų intervale.</span><span class="sxs-lookup"><span data-stu-id="36454-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="36454-159">Įtraukite kilmės šalį į BOM ataskaitas</span><span class="sxs-lookup"><span data-stu-id="36454-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="36454-160">Kai sukuriate BOM ataskaitą, galite įtraukti kilmės šalį kiekvienai daliai, kurią nurodėte šaltinyje ir kilmės šalyse **Kilmės šalies taisyklės** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="36454-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="36454-161">Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="36454-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="36454-162">Pasirinkite ar sukurkite produktą, kad atidarytumėte jo **Išleisto produkto informacija** puslapį.</span><span class="sxs-lookup"><span data-stu-id="36454-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="36454-163">Veiksmų juostoje, **Inžinierius** skirtuke, **BOM** grupėje, pasirinkite **Projektuotojas**.</span><span class="sxs-lookup"><span data-stu-id="36454-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="36454-164">Pasirodžiusiame puslapyje Veiksmų juostoje pasirinkite **BOM \> Spausdinti**.</span><span class="sxs-lookup"><span data-stu-id="36454-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="36454-165">**Medžiagų linijų sąskaitos** teksto lange nustatykite **Paskirties šalies** laukelį į paskirties šalį, kurią norite peržiūrėti savo ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="36454-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="36454-166">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="36454-166">Select **OK**.</span></span>

<span data-ttu-id="36454-167">Informaciją pateikianti ataskaita apie kiekvienos dalies kilmės šalį yra sukuriama ir rodoma.</span><span class="sxs-lookup"><span data-stu-id="36454-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="36454-168">Čia pateikiamas ataskaitos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="36454-168">Here is an example of the report.</span></span>

<span data-ttu-id="36454-169">![Kilmės šalies ataskaita](media/country-of-origin-report.png "Kilmės šalies ataskaita")</span><span class="sxs-lookup"><span data-stu-id="36454-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
