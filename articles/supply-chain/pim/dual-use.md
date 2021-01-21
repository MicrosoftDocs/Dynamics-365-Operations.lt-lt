---
title: Dvigubo naudojimo prekės
description: Šiame skyriuje paaiškinama, kaip sekti gaminius, kurie laikomi dvigubo naudojimo prekėmis, kiekvienos prekės parduotuvės sertifikato numerį ir paskirties vietą bei kaip atspausdinti galiojančius sertifikato numerius reikiamose sąskaitose, pakavimo lipdukus ir (arba) prekybos užsakymus.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COODualUseCerts, COORules, COODualUseCountries
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 8f2b738fd87219be383b103eaf5fafeb971fc702
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895478"
---
# <a name="dual-use-goods"></a><span data-ttu-id="aa6f2-103">Dvigubo naudojimo prekės</span><span class="sxs-lookup"><span data-stu-id="aa6f2-103">Dual-use goods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa6f2-104">Dvigubo naudojimo prekės yra dažniausiai elementai turintys civilinį ir karinį pritaikymą.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-104">Dual-use goods are typically items that have both civilian and military applications.</span></span> <span data-ttu-id="aa6f2-105">Pavyzdžiui, cheminės medžiagos gali būti naudojamos kaip trąšos ar kaip sprogios medžiagos.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-105">For example, a chemical might be used as either a fertilizer or an explosive.</span></span> <span data-ttu-id="aa6f2-106">Daugelis šalių turi specialius įstatymus taikomis dvigubo naudojimo prekių eksportavimui, importavimui ir transportavimui.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-106">Many countries have special regulations that apply to the export, import, and transportation of dual-use goods.</span></span> <span data-ttu-id="aa6f2-107">Dėl to, svarbu, kad bendrovės įtrauktos į tarptautinę dvigubo naudojimo prekių prekybą sektų įvairius įstatymus ir sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-107">Therefore, it's important that companies that are involved in the international trade of dual-use goods keep track of the various policies and certificates.</span></span>

<span data-ttu-id="aa6f2-108">Dvigubo naudojimo savybė padeda bendrovėms sekti dvigubo naudojimo prekes, kiekvieno produkto ir paskirties šalies parduotuvių sertifikatų numerius bei spausdinti galiojančius sertifikatų numerius reikiamose sąskaitose, pakavimo lipdukus ir (arba) prekybos užsakymus.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-108">The dual-use feature helps companies keep track of products that are identified as dual-use goods, stores certificate numbers for each relevant product and destination country, and print valid certificate numbers on relevant invoices, packing slips, and/or sales orders.</span></span> <span data-ttu-id="aa6f2-109">Tai padeda užtikrinti, kad kai jūsų produktai yra siunčiami, jie visuomet turėtų atnaujintus sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-109">It helps ensure that, when your products are shipped, they always include up-to-date certifications.</span></span>

<span data-ttu-id="aa6f2-110">Apgalvokite šiuos scenarijus:</span><span class="sxs-lookup"><span data-stu-id="aa6f2-110">Consider the following scenario:</span></span>

1. <span data-ttu-id="aa6f2-111">**Dvigubo naudojimo šalies nustatymų** puslapis jūsų sistemoje rodo, kad siuntimui į Prancūziją reikalingas sertifikatas.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-111">The **Dual use country setup** page in your system indicates that shipments to France require a certification.</span></span>
2. <span data-ttu-id="aa6f2-112">**Išleisto produkto informacijos** puslapis X-100 produktui rodo, kad tai dviejų naudojimų prekė.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-112">The **Released product details** page for product X-100 indicates that it's a dual-use good.</span></span> <span data-ttu-id="aa6f2-113">Kartu, kodas, kategorija, grupė ir režimas rodo eksportavimo valdymo klasifikavimą, kad produktas jiems priklauso.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-113">Together, the code, category, group, and regime indicate the export control classification that the product belongs to.</span></span>
3. <span data-ttu-id="aa6f2-114">**Dvigubo naudojimo sertifikatų** puslapis apima sertifikatą X-100 gaminiui, kai jis siunčiamas į Prancūziją.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-114">The **Dual use certificates** page includes a certificate for product X-100 when it's shipped to France.</span></span> <span data-ttu-id="aa6f2-115">Šis sertifikatas baigia galioti 2020 m sausio 1 d.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-115">This certificate expires January 1, 2020.</span></span>
4. <span data-ttu-id="aa6f2-116">2020 m. birželio 17 d. sukuriate prekybos užsakyma kliento bendrovei, kuri yra Prancūzijoje ir užsakymas apime X-100 produktą.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-116">On June 17, 2020, you create a sales order for a customer company that is based in France, and the order includes product X-100.</span></span>
5. <span data-ttu-id="aa6f2-117">Kai įrašote prekybos užsakymą, sistema nusprendžia šią informaciją:</span><span class="sxs-lookup"><span data-stu-id="aa6f2-117">When you save the sales order, the system determines the following information:</span></span>

    1. <span data-ttu-id="aa6f2-118">Ar užsakymas apima bet kokius produktus, kurie yra dvigubo panaudojimo prekės?</span><span class="sxs-lookup"><span data-stu-id="aa6f2-118">Does the order include any products that are dual-use goods?</span></span>
    2. <span data-ttu-id="aa6f2-119">Jei užsakymas apie dvigubo panaudojimo prekes, ar paskirties šalis reikalauja dvigubo panaudojimo sertifikatų?</span><span class="sxs-lookup"><span data-stu-id="aa6f2-119">If the order includes dual-use goods, does the destination country require dual-use certificates?</span></span>
    3. <span data-ttu-id="aa6f2-120">Jei šalis reikalauja dvigubo naudojimo sertifikatų, ar sertifikatas galioja dvigubo panaudojimo prekei paskirties šalyje?</span><span class="sxs-lookup"><span data-stu-id="aa6f2-120">If the country requires dual-use certificates, does a valid certificate exist for each dual-use good for the destination country?</span></span>

6. <span data-ttu-id="aa6f2-121">Užsakymas apima X-100 produktą, produktas siunčiamas į Prancūziją ir Prancūzijos serfikatas yra išduotas produktui.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-121">The order includes product X-100, the product is being shipped to France, and a French certificate exists for the product.</span></span> <span data-ttu-id="aa6f2-122">Nepaisant to, sertifikatas nebegalioja.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-122">However, the certificate has expired.</span></span> <span data-ttu-id="aa6f2-123">Dėl to, gaunate šią perspėjančią žinutę: „Dvigubo panaudojimo sertifikatas vienam ar keliems dvigubo panaudojimo elementas šiame užsakyme negalioja.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-123">Therefore, you receive the following warning message: "Dual use certificates for one or more dual-use items in this sales order aren't valid.</span></span> <span data-ttu-id="aa6f2-124">Ar norite tęsti patvirtinimą?“</span><span class="sxs-lookup"><span data-stu-id="aa6f2-124">Do you want to proceed with the confirmation?"</span></span>

<span data-ttu-id="aa6f2-125">Šiame skyriuje paaiškinama, kaip konfigūruoti visus nustatymus būtinus dvigubo panaudojimo prekių nustatymams ir šio scenarijaus palaikymui.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-125">This topic explains how to configure all the settings that are required to set up dual-use goods and support this scenario.</span></span>

## <a name="define-dual-use-requirements-for-each-relevant-country"></a><span data-ttu-id="aa6f2-126">Nustatykite dvigubo panaudojimo reikalavimus kiekvienai būtinai šaliai</span><span class="sxs-lookup"><span data-stu-id="aa6f2-126">Define dual-use requirements for each relevant country</span></span>

<span data-ttu-id="aa6f2-127">Skirtingos šalys turi skirtingus dvigubo prekių panaudojimo reikalavimams.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-127">Different countries have different requirements for dual-use goods.</span></span> <span data-ttu-id="aa6f2-128">Naudojate **Dvigubo panaudojimo šalies nustatymų** puslapį tam, kad sektumėte šalis, kurios reikalauja ar nereikalauja sertifikato:</span><span class="sxs-lookup"><span data-stu-id="aa6f2-128">You use the **Dual use country setup** page to keep track of the countries that do and don't require a certificate.</span></span> <span data-ttu-id="aa6f2-129">Informacija, kurią čia nurodote, yra patikrinama, kai kuriate prekybos užsakymus ir jums bus priminta apie būtinų sertifikatų pateikimą.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-129">The information that you specify here is checked when you create sales orders, and you will be reminded to provide the required certifications.</span></span>

<span data-ttu-id="aa6f2-130">Informacijos apie dvigubo panaudojimo reikalavimų nustatymą skirtingoms šalims, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-130">To set up the information about dual-use requirements for different countries, follow these steps.</span></span>

1. <span data-ttu-id="aa6f2-131">Eikite į **Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Dvigubo panaudojimo produktai \> Dvigubo panaudojimo šalies nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-131">Go to **Product information management \> Setup \> Product compliance \> Dual use products \> Dual use country setup**.</span></span>
2. <span data-ttu-id="aa6f2-132">Pasirinkite esančią šalies sąranką jos redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujos šalies sąranką.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-132">Select an existing country setup to edit it, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="aa6f2-133">Naujosios ar pasirinktos šalies nustatyme, nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="aa6f2-133">Set the following values for the selected or new country setup.</span></span>

    | <span data-ttu-id="aa6f2-134">Laukas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-134">Field</span></span> | <span data-ttu-id="aa6f2-135">aprašymas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-135">Description</span></span> |
    |---|---|
    | <span data-ttu-id="aa6f2-136">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-136">Country/region</span></span> | <span data-ttu-id="aa6f2-137">Pasirinkite šalį, kuriai sekate reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-137">Select the country that you're tracking requirements for.</span></span> |
    | <span data-ttu-id="aa6f2-138">Sertifikatas reikalingas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-138">Certificate Required</span></span> | <span data-ttu-id="aa6f2-139">Pasirinkite šį žymimą laukelį šalims, kurios reikalauja sertifikato dvigubo panaudojimo prekėms.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-139">Select this check box for countries that require a certification for dual-use goods.</span></span> <span data-ttu-id="aa6f2-140">Išvalykite jį šalims, kurios sertifikato nereikalauja.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-140">Clear it for countries that don't require this certification.</span></span> |

## <a name="create-dual-use-categories"></a><span data-ttu-id="aa6f2-141">Sukurkite dviejų panaudojimų kategorijas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-141">Create dual-use categories</span></span>

<span data-ttu-id="aa6f2-142">Dvigubo panaudojimo prekės turi būti dažnai suskirstytos į kategorijas pagal jų eksportavimo valdymo klasifikavimo nunmerį (ECCN).</span><span class="sxs-lookup"><span data-stu-id="aa6f2-142">Dual-use goods must often be categorized according to their export control classification number (ECCN).</span></span> <span data-ttu-id="aa6f2-143">ECCN yra skaitmeninis ir raidinis kodas, kuris suskirsto į kategorijas elementus pagal tokius faktorius kaip prekės ir technologija.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-143">The ECCN is an alphanumeric code that categorizes items based on factors such as the commodity and technology.</span></span> <span data-ttu-id="aa6f2-144">**Dvigubo panaudojimo kategorijų** puslapis jums padeda sudaryti jūsų naudojamų kategorijų sąrašą ataskaitų rengimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-144">The **Dual use categories** page helps you make a list of the categories that you use, for reporting purposes.</span></span>

<span data-ttu-id="aa6f2-145">Dviguvo panaudojimo kategorijų nustatymui, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-145">To set up dual-use categories, follow these steps.</span></span>

1. <span data-ttu-id="aa6f2-146">Eikite į**Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Dvigubo panaudojimo produktai \> Dvigubo panaudojimo kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-146">Go to **Product information management \> Setup \> Product compliance \> Dual use products \> Dual use categories**.</span></span>
2. <span data-ttu-id="aa6f2-147">Pasirinkite esančią šalies kategoriją jos redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujos šalies kategoriją.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-147">Select an existing category to edit it, or select **New** on the Action Pane to create a new category.</span></span>
3. <span data-ttu-id="aa6f2-148">Naujoje kategorije ar pasirinktoje kategorijoje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="aa6f2-148">Set the following values for the selected or new category.</span></span>

    | <span data-ttu-id="aa6f2-149">Laukai</span><span class="sxs-lookup"><span data-stu-id="aa6f2-149">Fields</span></span> | <span data-ttu-id="aa6f2-150">aprašymas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-150">Description</span></span> |
    |---|---|
    | <span data-ttu-id="aa6f2-151">Dvigubo naudojimo kodas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-151">Dual use code</span></span> | <span data-ttu-id="aa6f2-152">Įveskite visą ECCN kodą (pavyzdžiui, *3A001*).</span><span class="sxs-lookup"><span data-stu-id="aa6f2-152">Enter the full ECCN code (for example, *3A001*).</span></span>|
    | <span data-ttu-id="aa6f2-153">Dvigubo naudojimo kategorija</span><span class="sxs-lookup"><span data-stu-id="aa6f2-153">Dual use category</span></span> | <span data-ttu-id="aa6f2-154">Įveskite komercijos kontroliavimo sąrašą (CCL) ECCN kodo kategorijos daliai.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-154">Enter the commerce control list (CCL) category part of the ECCN code.</span></span> <span data-ttu-id="aa6f2-155">Pavyzdžiui, ECCN kodui *3A001*, ši vertė yra *3*.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-155">For example, for the ECCN code *3A001*, this value is *3*.</span></span> |
    | <span data-ttu-id="aa6f2-156">Dvigubo naudojimo grupė</span><span class="sxs-lookup"><span data-stu-id="aa6f2-156">Dual use group</span></span> | <span data-ttu-id="aa6f2-157">Įveskite ECCN kodo produkto grupės dalį.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-157">Enter the product group part of the ECCN code.</span></span> <span data-ttu-id="aa6f2-158">Pavyzdžiui, ECCN kodui *3A001*, ši vertė yra *A*.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-158">For example, for the ECCN code *3A001*, this value is *A*.</span></span> |
    | <span data-ttu-id="aa6f2-159">Dvigubo naudojimo režimas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-159">Dual use regime</span></span> | <span data-ttu-id="aa6f2-160">Įveskite režimo kodą elementui.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-160">Enter the regime code for the item.</span></span> <span data-ttu-id="aa6f2-161">Šis kodas nustato priežastį, kodėl elementas yra klasifikuojamas kaip dvigubo naudojimo prekė.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-161">This code identifies the reason why the item is classified as a dual-use good.</span></span> <span data-ttu-id="aa6f2-162">Pavyzdžiui, ECCN kodui *3A001*, ši vertė yra *001*.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-162">For example, for the ECCN code *3A001*, this value is *001*.</span></span> |

## <a name="apply-dual-use-categories-to-products"></a><span data-ttu-id="aa6f2-163">Pritaikykite dvigubo panaudojimo kategorijas produktams</span><span class="sxs-lookup"><span data-stu-id="aa6f2-163">Apply dual-use categories to products</span></span>

<span data-ttu-id="aa6f2-164">Produkto kaip dvigubo panaudojimo prekės nustatymui ir dvigubo panaudojimo kategorijos pritaikymui, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-164">To identify a product as a dual-use good and apply a dual-use category to it, follow these steps.</span></span>

1. <span data-ttu-id="aa6f2-165">Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-165">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="aa6f2-166">Pasirinkite ar sukurkite produktą, kad atidarytumėte jo **Išleisto produkto informacija** puslapį.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-166">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="aa6f2-167">**Užsienio prekybos** „FastTab“, nustatykite **Dvigubo naudojimo produktų** prainktį į **Taip** tam, kad nustatytumėte esamą produktą kaip dvigubo panaudojimo prekę.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-167">On the **Foreign trade** FastTab, set the **Dual use products** option to **Yes** to identify the current product as a dual-use good.</span></span>
1. <span data-ttu-id="aa6f2-168">Nustatykite **Dvigubo panaudojimo kodo** laukelį, kuris taikomas dabartiniam produktui.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-168">Set the **Dual use code** field to the code that applies to the current product.</span></span> <span data-ttu-id="aa6f2-169">(Jūs šį kodą nustatėte **Dvigubo panaudojimo kategorijų** puslapyje.)</span><span class="sxs-lookup"><span data-stu-id="aa6f2-169">(You defined this code on the **Dual use categories** page.)</span></span>

<span data-ttu-id="aa6f2-170">Šis nustatymas yra tikrinamas, kai kuriate prekybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-170">This setup is checked when you create a sales order.</span></span>

## <a name="set-up-dual-use-certificates"></a><span data-ttu-id="aa6f2-171">Dvigubo panaudojimo sertifikatų nustatymas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-171">Set up dual-use certificates</span></span>

<span data-ttu-id="aa6f2-172">Naudojate **Dvigubo panaudojimo sertifikatų** puslapį, kad nustatytumėte ir valdytumėte būtinus dvigubo panaudojimo sertifikatus kiekvienam produktui ir šaliai.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-172">You use the **Dual use certificates** page to set up and manage the required dual-use certificates for each product and country.</span></span> <span data-ttu-id="aa6f2-173">Galite sekti visų sertifikatų informaciją, tokių kaip šalies ir duomenų galiojimą.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-173">You can track each certificate's details, such as the country and the dates of validity.</span></span> <span data-ttu-id="aa6f2-174">Galite taip pat nustatyti pasirinkimus tam, kad nurodytumėte, kur ši informacija turi būti atspausdinta.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-174">You can also set options to specify where this information should be printed.</span></span> <span data-ttu-id="aa6f2-175">Pavyzdžiui, informacija gali būti atspausdinta sąskaitoje, pakavimo lipduke ir (arba) prekybos užsakyme.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-175">For example, the information can be printed on the invoice, packing slip, and/or sales order.</span></span> <span data-ttu-id="aa6f2-176">Šis nustatymas yra tikrinamas, kai kuriate prekybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-176">This setup is checked when you create a sales order.</span></span>

1. <span data-ttu-id="aa6f2-177">Eikite į**Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Dvigubo panaudojimo produktai \> Dvigubo panaudojimo sertifikatai**.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-177">Go to **Product information management \> Setup \> Product compliance \> Dual use products \> Dual use certificates**.</span></span>
2. <span data-ttu-id="aa6f2-178">Pasirinkite esančią sertifikato sąranką jos redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujo sertifikato sąranką.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-178">Select an existing certificate to edit it, or select **New** on the Action Pane to create a new certificate.</span></span>
3. <span data-ttu-id="aa6f2-179">Naujam ar pasirinktam sertifikatui nustatykite šias vertes.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-179">Set the following values for the selected or new certificate.</span></span>

    | <span data-ttu-id="aa6f2-180">Laukas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-180">Field</span></span> | <span data-ttu-id="aa6f2-181">aprašymas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-181">Description</span></span> |
    |---|---|
    | <span data-ttu-id="aa6f2-182">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-182">Item number</span></span> | <span data-ttu-id="aa6f2-183">Pasirinkite dvigubo panaudojimo prekės elemento numerį, kuriam taikomas šis sertifiktas.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-183">Select the item number of the dual-use good that this certificate applies to.</span></span> |
    | <span data-ttu-id="aa6f2-184">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-184">Country/region</span></span> | <span data-ttu-id="aa6f2-185">Paskirties šalis ar regionas, kuriame privalote naudoti šį sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-185">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="aa6f2-186">Sertifikato numeris</span><span class="sxs-lookup"><span data-stu-id="aa6f2-186">Certificate number</span></span> | <span data-ttu-id="aa6f2-187">Skaičius pasirodantis sertifikate, kuris yra išduotas pardavėjui ar klientui.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-187">The number that appears on the certificate that is issued to the vendor or customer.</span></span> |
    | <span data-ttu-id="aa6f2-188">Galioja</span><span class="sxs-lookup"><span data-stu-id="aa6f2-188">Effective</span></span> | <span data-ttu-id="aa6f2-189">Pasirinkite pirmą datą, kai esamas sertifikatas galioja.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-189">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="aa6f2-190">Galiojimas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-190">Expiration</span></span> | <span data-ttu-id="aa6f2-191">Pasirinkite paskutinę datą, kai esamas sertifikatas galioja.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-191">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="aa6f2-192">Atspausdinkite sąskaitą</span><span class="sxs-lookup"><span data-stu-id="aa6f2-192">Print on invoice</span></span> | <span data-ttu-id="aa6f2-193">Pasirinkite žymimą laukelį, kad atspausdintumėte sertifikato numerį sąskaitose, kurios yra siunčiamos konkrečiai šaliai nurodytų duomenų intervale.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-193">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="aa6f2-194">Atspausdinkite pakavimo lipduką</span><span class="sxs-lookup"><span data-stu-id="aa6f2-194">Print on packing slip</span></span> | <span data-ttu-id="aa6f2-195">Pasirinkite žymimą laukelį, kad atspausdintumėte pakavimo lipdukų numerį sąskaitose, kurios yra siunčiamos konkrečiai šaliai nurodytų duomenų intervale.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-195">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="aa6f2-196">Prekybos užsakymo spausdinimas</span><span class="sxs-lookup"><span data-stu-id="aa6f2-196">Print on sales order</span></span> | <span data-ttu-id="aa6f2-197">Pasirinkite žymimą laukelį, kad atspausdintumėte sertifikato numerį ar prekybos užsakymus, kurie yra siunčiami konkrečiai šaliai nurodytų duomenų intervale.</span><span class="sxs-lookup"><span data-stu-id="aa6f2-197">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |