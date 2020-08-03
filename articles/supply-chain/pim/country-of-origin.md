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
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596258"
---
# <a name="country-of-origin"></a><span data-ttu-id="8408e-105">Kilmės šalis / regionas</span><span class="sxs-lookup"><span data-stu-id="8408e-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8408e-106">Daugelis organizacijų išduoda sertifikatus savo pardavėjams tam, kad užtikrintų, jog jų produktai atitiktų sertifikato standartus.</span><span class="sxs-lookup"><span data-stu-id="8408e-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="8408e-107">Šie sertifikatai dažnai priklauso nuo kilmės šalies.</span><span class="sxs-lookup"><span data-stu-id="8408e-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="8408e-108">Kilmės šalies savybės leidžia jums susieti gaminį su jo kilmės šalimi ir sekti gaminių sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="8408e-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="8408e-109">Konfigūruoti šaltinį ir paskirties šalis</span><span class="sxs-lookup"><span data-stu-id="8408e-109">Configure source and destination countries</span></span>

<span data-ttu-id="8408e-110">Prieš jums išduodant sertifikatą gaminiui privalo susieti jį su jo paskirties šalimi ir kilmės šalimi.</span><span class="sxs-lookup"><span data-stu-id="8408e-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="8408e-111">Eikite į**Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Kilmės šalis \> Kilmės šalies taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="8408e-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="8408e-112">Pasirinkite esančią šalies sąranką redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujos šalies sąranką.</span><span class="sxs-lookup"><span data-stu-id="8408e-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="8408e-113">Naujosios politikos antraštėje, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="8408e-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="8408e-114">Laukas</span><span class="sxs-lookup"><span data-stu-id="8408e-114">Field</span></span> | <span data-ttu-id="8408e-115">aprašymas</span><span class="sxs-lookup"><span data-stu-id="8408e-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="8408e-116">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="8408e-116">Item number</span></span> | <span data-ttu-id="8408e-117">Pasirinkite elemento gaminio numerį.</span><span class="sxs-lookup"><span data-stu-id="8408e-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="8408e-118">Paskirties šalis</span><span class="sxs-lookup"><span data-stu-id="8408e-118">Destination country</span></span> | <span data-ttu-id="8408e-119">Pasirinkite šalį, į kurią siunčiate gaminį.</span><span class="sxs-lookup"><span data-stu-id="8408e-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="8408e-120">Kilmės šalis</span><span class="sxs-lookup"><span data-stu-id="8408e-120">Origin country</span></span> | <span data-ttu-id="8408e-121">Pasirinkite šalį, iš kurios siunčiate gaminį.</span><span class="sxs-lookup"><span data-stu-id="8408e-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="8408e-122">Šios sąrankos tikslas yra padėti jums sukurti medžiagų sąskaitos (BOM) ataskaitą, į kurią galite įtraukti kilmės šalį kiekvienai daliai, kuriai yra nustatytas šaltinis ir paskirties šalis.</span><span class="sxs-lookup"><span data-stu-id="8408e-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="8408e-123">Ši sąskaita padės jums gauti bendrą paveikslėlį, kuriame matysite, iš kur ateina jūsų dalys ir kur jos eina.</span><span class="sxs-lookup"><span data-stu-id="8408e-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="8408e-124">Sekite pardavėjų sertifikatus</span><span class="sxs-lookup"><span data-stu-id="8408e-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="8408e-125">Galite naudoti **Kilmės šalies pardavėjo sertifikatų** puslapį tam, kad sektumėte sertifikatus, kuriuos išduodate pardavėjams.</span><span class="sxs-lookup"><span data-stu-id="8408e-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="8408e-126">Privalote nuspręsti, kuriuos sertifikato dokumentus išduodate ir kaip apie juos pranešite klientams.</span><span class="sxs-lookup"><span data-stu-id="8408e-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="8408e-127">Ši funkcija padeda jums sekti jūsų sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="8408e-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="8408e-128">Ji taip pat padeda jums pasirinkti, ar atitinkami sertifikato numeriai bus rodomi sąskaitose, pakavimo lapeliuose ir (arba) užsakymo patvirtinimuose.</span><span class="sxs-lookup"><span data-stu-id="8408e-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="8408e-129">Sertifikato informacijos nustatymui, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="8408e-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="8408e-130">Eikite į**Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Kilmės šalis \> Pardavėjo kilmės šalies sertifikatai**.</span><span class="sxs-lookup"><span data-stu-id="8408e-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="8408e-131">Pasirinkite esančią sertifikato sąranką redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujo sertifikato sąranką.</span><span class="sxs-lookup"><span data-stu-id="8408e-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="8408e-132">Naujam ar pasirinktam sertifikatui nustatykite šiuose nustatymus.</span><span class="sxs-lookup"><span data-stu-id="8408e-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="8408e-133">Laukas</span><span class="sxs-lookup"><span data-stu-id="8408e-133">Field</span></span> | <span data-ttu-id="8408e-134">aprašymas</span><span class="sxs-lookup"><span data-stu-id="8408e-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="8408e-135">Tiekėjo kodas</span><span class="sxs-lookup"><span data-stu-id="8408e-135">Vendor account</span></span> | <span data-ttu-id="8408e-136">Pasirinkite pardavėją, kuriam išdavėte sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="8408e-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="8408e-137">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="8408e-137">Item number</span></span> | <span data-ttu-id="8408e-138">Pasirinkite elementą, kuriam išdavėte sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="8408e-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="8408e-139">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="8408e-139">Country/region</span></span> | <span data-ttu-id="8408e-140">Paskirties šalis ar regionas, kuriame privalote naudoti šį sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="8408e-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="8408e-141">Sertifikato numeris</span><span class="sxs-lookup"><span data-stu-id="8408e-141">Certificate number</span></span> | <span data-ttu-id="8408e-142">Įveskite jūsų išduoto sertifikato identifikavimo numerį.</span><span class="sxs-lookup"><span data-stu-id="8408e-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="8408e-143">Galioja</span><span class="sxs-lookup"><span data-stu-id="8408e-143">Effective</span></span> | <span data-ttu-id="8408e-144">Pasirinkite pirmą datą, kai esamas sertifikatas galioja.</span><span class="sxs-lookup"><span data-stu-id="8408e-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="8408e-145">Galiojimas</span><span class="sxs-lookup"><span data-stu-id="8408e-145">Expiration</span></span> | <span data-ttu-id="8408e-146">Pasirinkite paskutinę datą, kai esamas sertifikatas galioja.</span><span class="sxs-lookup"><span data-stu-id="8408e-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="8408e-147">Atspausdinkite sąskaitą</span><span class="sxs-lookup"><span data-stu-id="8408e-147">Print on invoice</span></span> | <span data-ttu-id="8408e-148">Pasirinkite žymimą laukelį, kad atspausdintumėte sertifikato numerį sąskaitose, kurios yra siunčiamos konkrečiai šaliai nurodytų duomenų intervale.</span><span class="sxs-lookup"><span data-stu-id="8408e-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="8408e-149">Atspausdinkite pakavimo lipduką</span><span class="sxs-lookup"><span data-stu-id="8408e-149">Print on packing slip</span></span> | <span data-ttu-id="8408e-150">Pasirinkite žymimą laukelį, kad atspausdintumėte pakavimo lipdukų numerį sąskaitose, kurios yra siunčiamos konkrečiai šaliai nurodytų duomenų intervale.</span><span class="sxs-lookup"><span data-stu-id="8408e-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="8408e-151">Prekybos užsakymo spausdinimas</span><span class="sxs-lookup"><span data-stu-id="8408e-151">Print on sales order</span></span> | <span data-ttu-id="8408e-152">Pasirinkite žymimą laukelį, kad atspausdintumėte sertifikato numerį ar prekybos užsakymus, kurie yra siunčiami konkrečiai šaliai nurodytų duomenų intervale.</span><span class="sxs-lookup"><span data-stu-id="8408e-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="8408e-153">Įtraukite kilmės šalį į BOM ataskaitas</span><span class="sxs-lookup"><span data-stu-id="8408e-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="8408e-154">Kai sukuriate BOM ataskaitą, galite įtraukti kilmės šalį kiekvienai daliai, kurią nurodėte šaltinyje ir kilmės šalyse **Kilmės šalies taisyklės** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="8408e-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="8408e-155">Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="8408e-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8408e-156">Pasirinkite ar sukurkite produktą, kad atidarytumėte jo **Išleisto produkto informacija** puslapį.</span><span class="sxs-lookup"><span data-stu-id="8408e-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="8408e-157">Veiksmų juostoje, **Inžinierius** skirtuke, **BOM** grupėje, pasirinkite **Projektuotojas**.</span><span class="sxs-lookup"><span data-stu-id="8408e-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="8408e-158">Pasirodžiusiame puslapyje Veiksmų juostoje pasirinkite **BOM \> Spausdinti**.</span><span class="sxs-lookup"><span data-stu-id="8408e-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="8408e-159">**Medžiagų linijų sąskaitos** teksto lange nustatykite **Paskirties šalies** laukelį į paskirties šalį, kurią norite peržiūrėti savo ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="8408e-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="8408e-160">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8408e-160">Select **OK**.</span></span>

<span data-ttu-id="8408e-161">Informaciją pateikianti ataskaita apie kiekvienos dalies kilmės šalį yra sukuriama ir rodoma.</span><span class="sxs-lookup"><span data-stu-id="8408e-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="8408e-162">Čia pateikiamas ataskaitos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="8408e-162">Here is an example of the report.</span></span>

<span data-ttu-id="8408e-163">![Kilmės šalies ataskaita](media/country-of-origin-report.png "Kilmės šalies ataskaita")</span><span class="sxs-lookup"><span data-stu-id="8408e-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
