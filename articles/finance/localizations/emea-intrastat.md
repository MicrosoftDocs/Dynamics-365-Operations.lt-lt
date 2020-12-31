---
title: Intrastat apžvalga
description: Šioje temoje pateikta informacija apie Intrastat ataskaitas už prekybą prekėmis ir, kai kuriais atvejais, paslaugomis Europos Sąjungos (ES) šalyse / regionuose. Jame pateikta ataskaitų proceso apžvalga ir aprašyti reikiami parametrai ir būtinosios sąlygos.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a70108696d6187126c23eca1779553210cd4a9d6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408243"
---
# <a name="intrastat-overview"></a><span data-ttu-id="68c0f-104">Intrastat apžvalga</span><span class="sxs-lookup"><span data-stu-id="68c0f-104">Intrastat overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68c0f-105">Šioje temoje pateikta informacija apie Intrastat ataskaitas už prekybą prekėmis ir, kai kuriais atvejais, paslaugomis Europos Sąjungos (ES) šalyse / regionuose.</span><span class="sxs-lookup"><span data-stu-id="68c0f-105">This topic provides information about Intrastat reporting for the trade of goods and, in some cases, services among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="68c0f-106">Jame pateikta ataskaitų proceso apžvalga ir aprašyti reikiami parametrai ir būtinosios sąlygos.</span><span class="sxs-lookup"><span data-stu-id="68c0f-106">It provides an overview of the reporting process, and describes the required settings and prerequisites.</span></span>

<span data-ttu-id="68c0f-107">Intrastat yra informacijos rinkimo ir statistikos generavimo apie prekybą prekėmis Europos Sąjungos (ES) šalyse / regionuose sistema.</span><span class="sxs-lookup"><span data-stu-id="68c0f-107">Intrastat is the system for collecting information and generating statistics about the trade of goods among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="68c0f-108">Intrastat ataskaitų reikia, kai produktas kerta kitos ES šalies / regiono sieną.</span><span class="sxs-lookup"><span data-stu-id="68c0f-108">Intrastat reporting is required whenever a product crosses the border of another EU country/region.</span></span> <span data-ttu-id="68c0f-109">Keliose šalyse / regionuose Intrastat ataskaitos taip pat taikomos paslaugoms.</span><span class="sxs-lookup"><span data-stu-id="68c0f-109">In several countries/regions, Intrastat reporting also applies to services.</span></span> <span data-ttu-id="68c0f-110">Intrastat ataskaitose gali būti renkami privalomi ir neprivalomi elementai.</span><span class="sxs-lookup"><span data-stu-id="68c0f-110">Mandatory and optional elements can be collected in Intrastat reporting.</span></span> <span data-ttu-id="68c0f-111">Privalomi yra šie elementai: šalies, kuri yra atsakinga už informacijos teikimą, pridėtinės vertės mokesčio (PVM) numeris, ataskaitinis laikotarpis, srautas (gavimo ar išsiuntimo), aštuonių skaitmenų prekės kodas, partnerė šalis narė (konsignacijos šalis narė gaunant ir paskirties šalis narė išsiunčiant), prekių vertė, prekių kiekis (neto svoris ir papildomas vienetas) ir operacijos pobūdis.</span><span class="sxs-lookup"><span data-stu-id="68c0f-111">The following elements are mandatory: the value-added tax (VAT) number of the party that is responsible for providing information, the reference period, the flow (arrival or dispatch), the eight-digit commodity code, the partner member state (member state of consignment on arrivals and member state of destination on dispatches), the value of the goods, the quantity of the goods (net mass and supplementary unit), and the nature of the transaction.</span></span> <span data-ttu-id="68c0f-112">Šalys / regionai taip pat gali įvairiomis sąlygomis rinkti neprivalomų elementų.</span><span class="sxs-lookup"><span data-stu-id="68c0f-112">Countries/regions can also collect optional elements under various conditions.</span></span> <span data-ttu-id="68c0f-113">Kai kurie neprivalomi elementai yra kilmės šalis / regionas, pristatymo sąlygos, transportavimo būdas, išsamesnis už CN8 prekės kodas, kilmės regionas išsiunčiant ir paskirties regionas gaunant, statistinė procedūra, statistinė vertė, prekių aprašas ir pakrovimo / iškrovimo uostas / oro uostas.</span><span class="sxs-lookup"><span data-stu-id="68c0f-113">Some optional elements are the country/region of origin, the delivery terms, the mode of transport, a more detailed commodity code than CN8, the region of origin on dispatches and the region of destination on arrivals, the statistical procedure, the statistical value, a description of the goods, and the port/airport of loading/unloading.</span></span>

## <a name="overview-of-the-intrastat-reporting-process"></a><span data-ttu-id="68c0f-114">Intrastat ataskaitų teikimo proceso apžvalga</span><span class="sxs-lookup"><span data-stu-id="68c0f-114">Overview of the Intrastat reporting process</span></span>
<span data-ttu-id="68c0f-115">Toliau pateikiamuose skyriuose aprašomas bendras informacijos, kuri naudojama teikti Intrastat ataskaitoms, srautas.</span><span class="sxs-lookup"><span data-stu-id="68c0f-115">The following sections describe the overall flow of information that is used for Intrastat reporting.</span></span>

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a><span data-ttu-id="68c0f-116">1. Įvesti operaciją, kuri kerta kitos ES šalies / regiono sieną</span><span class="sxs-lookup"><span data-stu-id="68c0f-116">1. Enter a transaction that crosses the border of another EU country/region</span></span>

<span data-ttu-id="68c0f-117">Kliento SF, laisvos formos SF, pirkimo SF, projekto SF, kliento važtaraštis, tiekėjo produkto kvitas ar perkėlimo užsakymas į Intrastat žurnalą perkeliami tik jei paskirties (išsiunčiant) arba konsignacijos (gaunant) šalies / regiono tipas yra **ES**.</span><span class="sxs-lookup"><span data-stu-id="68c0f-117">A customer invoice, free text invoice, purchase invoice, project invoice, customer packing slip, vendor product receipt, or transfer order is transferred to the Intrastat journal only if the country/region type of the destination (on dispatches) or consignment (on arrivals) is **EU**.</span></span> <span data-ttu-id="68c0f-118">Šią funkciją taip pat palaiko „Microsoft Dynamics 365 for Operations“ (1611). Funkcija suteikia galimybę nurodyti ES vidaus operacijos pakrovimo adresą.</span><span class="sxs-lookup"><span data-stu-id="68c0f-118">This feature was extended for Microsoft Dynamics 365 for Operations (1611) and allows you to specify lading addresses for an intra-community transaction.</span></span> <span data-ttu-id="68c0f-119">Jei pakrovimo adresas skiriasi nuo tiekėjo darbo adreso (arba grąžinimo užsakymo kliento darbo adreso), Intrastat ataskaitose bus naudojama ši informacija.</span><span class="sxs-lookup"><span data-stu-id="68c0f-119">If a lading address differs with a vendor business address (or customer business address for return order) the Intrastat reporting will operate with this information.</span></span> <span data-ttu-id="68c0f-120">Kai kuriate pardavimo užsakymą, laisvos formos SF, pirkimo užsakymą, tiekėjo SF, projekto SF ar perkėlimo užsakymą, dokumento antraštėje arba eilutėje kai kurių laukų, kurie yra susiję su užsienio prekyba, reikšmės yra numatytosios.</span><span class="sxs-lookup"><span data-stu-id="68c0f-120">When you create a sales order, free text invoice, purchase order, vendor invoice, project invoice, or transfer order, some fields that are related to foreign trade have default values in the document header or on the line.</span></span> <span data-ttu-id="68c0f-121">Numatytasis operacijos kodas yra paimamas iš atitinkamo lauko **Užsienio prekybos parametrų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="68c0f-121">The default transaction code is taken from the corresponding field on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="68c0f-122">Numatytasis prekės kodas, kilmės šalis / regionas ir kilmės apskritis / rajonas paimami iš prekės.</span><span class="sxs-lookup"><span data-stu-id="68c0f-122">The default commodity code, country/region of origin, and state/province of origin are taken from the item.</span></span> <span data-ttu-id="68c0f-123">Galite keisti numatytąsias reikšmes ir taip pat galite užpildyti kitą su užsienio prekyba susijusią informaciją: statistikos procedūrą, transportavimo būdą ir uostą.</span><span class="sxs-lookup"><span data-stu-id="68c0f-123">You can change the default values and can also fill in other foreign trade–related information: the statistics procedure, transport method, and port.</span></span>

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="68c0f-124">2. Naudoti Intrastat žurnalą, norint generuoti informaciją apie prekybą tarp ES šalių / regionų</span><span class="sxs-lookup"><span data-stu-id="68c0f-124">2. Use the Intrastat journal to generate information about trade among EU countries/regions</span></span>

<span data-ttu-id="68c0f-125">Statistikos tikslais informacija apie prekybą tarp ES šalių / regionų generuojama kas mėnesį.</span><span class="sxs-lookup"><span data-stu-id="68c0f-125">For statistical purposes, you generate information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="68c0f-126">Operacijas iš laisvos formos SF, kliento SF, kliento važtaraščio, tiekėjo SF, tiekėjo važtaraščio, projekto SF ar perkėlimo užsakymo galite perkelti pagal perkėlimo kriterijus, kurie nustatomi **Užsienio prekybos parametrų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="68c0f-126">You can transfer transactions from a free text invoice, customer invoice, customer packing slip, vendor invoice, vendor packing slip, project invoice, or transfer order, according to the transfer criteria that are set up on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="68c0f-127">Operacijas galite įvesti ir rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="68c0f-127">Alternatively, you can enter transactions manually.</span></span> <span data-ttu-id="68c0f-128">Jei reikia ką naujinti, galite rankiniu būdu atnaujinti perkeltas operacijas Intrastat žurnale.</span><span class="sxs-lookup"><span data-stu-id="68c0f-128">You can manually update transferred transactions in the Intrastat journal, if any updates are required.</span></span> <span data-ttu-id="68c0f-129">Konkrečiomis aplinkybėmis, nustatomomis **Intrastat glaudinimo** puslapyje, Intrastat žurnale galite glaudinti operacijas.</span><span class="sxs-lookup"><span data-stu-id="68c0f-129">Under specific conditions that are set up on the **Compression of Intrastat** page, you can compress the transactions in the Intrastat journal.</span></span> <span data-ttu-id="68c0f-130">Kai kuriose šalyse / regionuose leidžiama taikyti operacijos ribinę reikšmę.</span><span class="sxs-lookup"><span data-stu-id="68c0f-130">Some countries/regions let you apply a small transaction threshold.</span></span> <span data-ttu-id="68c0f-131">Tada operacijas, esančias žemiau tos ribinės reikšmės, galite pateikti nurodytu prekės kodu.</span><span class="sxs-lookup"><span data-stu-id="68c0f-131">You can then report transactions that are below that threshold under the specified commodity code.</span></span> <span data-ttu-id="68c0f-132">Prekės kodą galite atnaujinti atitinkamose Intrastat žurnalo eilutėse, atsižvelgdami į **Minimalios ribos** nuostatą **Užsienio prekybos parametrų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="68c0f-132">You can update the commodity code on the corresponding Intrastat journal lines, based on the **Minimum limit** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="68c0f-133">Pagal **Intrastat glaudinimo** nuostatą taip pat galite tas operacijas glaudinti.</span><span class="sxs-lookup"><span data-stu-id="68c0f-133">You can also compress those transactions, based on the **Compression of Intrastat** setting.</span></span> <span data-ttu-id="68c0f-134">Intrastat žurnale tikrinti operacijų užbaigtumą galite pagal nuostatą **Tikrinti sąranką**, esančią **Užsienio prekybos parametrų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="68c0f-134">You can validate the completeness of the transactions in the Intrastat journal, based on the **Check setup** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="68c0f-135">Galima tikrinti atitinkamų laukų duomenų užbaigtumą: šalies / regiono, apskrities ar rajono, svorio, prekės kodo, operacijos kodo, papildomo vieneto, uosto, kilmės, pristatymo sąlygų, transportavimo būdo ir mokesčių lengvatos numerio.</span><span class="sxs-lookup"><span data-stu-id="68c0f-135">The data in corresponding fields might be validated for completeness: country/region, state or province, weight, commodity code, transaction code, additional unit, port, origin, terms of delivery, transport method, and tax exempt number.</span></span> <span data-ttu-id="68c0f-136">Operacijos, kurios nėra užbaigtos, bus pažymėtos kaip negaliojančios.</span><span class="sxs-lookup"><span data-stu-id="68c0f-136">Transactions that aren't completed will be marked as not valid.</span></span>

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="68c0f-137">3. Naudoti Intrastat žurnalą, norint pranešti informaciją apie prekybą tarp ES šalių / regionų</span><span class="sxs-lookup"><span data-stu-id="68c0f-137">3. Use the Intrastat journal to report information about trade among EU countries/regions</span></span>

<span data-ttu-id="68c0f-138">Statistikos tikslais informacija apie prekybą tarp ES šalių / regionų skelbiama kas mėnesį.</span><span class="sxs-lookup"><span data-stu-id="68c0f-138">For statistical purposes, you report information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="68c0f-139">Intrastat ataskaitą galite spausdinti pagal **Ataskaitų formatų susiejimo** nuostatas **Užsienio prekybos parametrų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="68c0f-139">You can print the Intrastat report, based on the **Report format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="68c0f-140">Taip pat pagal **Failų formatų susiejimo** nuostatas **Užsienio prekybos parametrų** puslapyje galite generuoti elektroninį failą.</span><span class="sxs-lookup"><span data-stu-id="68c0f-140">You can also generate an electronic file, based on the **File format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="68c0f-141">Norėdami daugiau informacijos apie Intrastat ataskaitas, įskaitant būtinąsias sąlygas, žr. toliau nurodytus Intrastat ataskaitų užduočių įrašus.</span><span class="sxs-lookup"><span data-stu-id="68c0f-141">For more information about Intrastat reporting, including required prerequisites, see the Intrastat reporting task recordings:</span></span>

-   <span data-ttu-id="68c0f-142">ES Intrastat deklaracijos generavimas,</span><span class="sxs-lookup"><span data-stu-id="68c0f-142">Generate an EU Intrastat declaration,</span></span>
-   <span data-ttu-id="68c0f-143">Operacijų perkėlimas į Intrastat,</span><span class="sxs-lookup"><span data-stu-id="68c0f-143">Transfer transactions to the Intrastat,</span></span>
-   <span data-ttu-id="68c0f-144">ES vidaus operacijos pakrovimo adreso nurodymas.</span><span class="sxs-lookup"><span data-stu-id="68c0f-144">Specifying lading address for an intra-community transaction.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="68c0f-145">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="68c0f-145">Prerequisites</span></span>
<span data-ttu-id="68c0f-146">Toliau pateikiamoje lentelėje nurodytos Intrastat ataskaitų būtinosios sąlygos.</span><span class="sxs-lookup"><span data-stu-id="68c0f-146">The following table lists the prerequisites for Intrastat reporting.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68c0f-147">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="68c0f-147">Prerequisite</span></span></th>
<th><span data-ttu-id="68c0f-148">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="68c0f-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68c0f-149">Adreso sąranka</span><span class="sxs-lookup"><span data-stu-id="68c0f-149">Address setup</span></span></td>
<td><span data-ttu-id="68c0f-150">Nustatykite šalių / regionų Tarptautinės standartizacijos organizacijos (ISO) kodus.</span><span class="sxs-lookup"><span data-stu-id="68c0f-150">Set up International Organization for Standardization (ISO) codes for countries/regions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68c0f-151">Juridinis subjektas</span><span class="sxs-lookup"><span data-stu-id="68c0f-151">Legal entity</span></span></td>
<td><span data-ttu-id="68c0f-152">Nustatykite importavimo / eksportavimo mokesčių lengvatų numerius, importavimo / eksportavimo filialo numerio plėtinį ir Intrastat kodą, priskirtą juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="68c0f-152">Set up tax exempt numbers for import/export, the branch number extension for import/export, and the Intrastat code that is assigned to the legal entity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68c0f-153">Produktų kategorijų hierarchija (pardavimo hierarchija, įsigijimo hierarchija)</span><span class="sxs-lookup"><span data-stu-id="68c0f-153">Product category hierarchy (sales hierarchy, procurement hierarchy)</span></span></td>
<td><span data-ttu-id="68c0f-154"><strong>Kategorijų hierarchijos</strong> puslapio skirtuke <strong>Prekių kodai</strong> kategorijų mazgams priskirkite Intrastat prekių kodus.</span><span class="sxs-lookup"><span data-stu-id="68c0f-154">Assign the Intrastat commodity codes to the category nodes on the <strong>Commodity codes</strong> tab of the <strong>Category hierarchy</strong> page.</span></span> <span data-ttu-id="68c0f-155">Kai prekės kodą priskiriate pirminės kategorijos mazgui, tas kodas taikomas visiems antrinių kategorijų mazgams.</span><span class="sxs-lookup"><span data-stu-id="68c0f-155">When you assign a commodity code to a parent category node, that code is applicable to all child category nodes.</span></span> <span data-ttu-id="68c0f-156">Prekės kodą pasirinkus išleisto produkto informacijoje ir pardavimo užsakymo, pirkimo užsakymo bei perkėlimo užsakymo eilutėse, pasirinkti prekių kodai bus prieinami rodinyje <strong>Pasirinkta</strong>.</span><span class="sxs-lookup"><span data-stu-id="68c0f-156">The selected commodity codes will be available in the <strong>Selected</strong> view when you select a commodity code in the released product details, and on sales order, purchase order, and transfer order lines.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68c0f-157">Patvirtinto produkto informacija</span><span class="sxs-lookup"><span data-stu-id="68c0f-157">Released product details</span></span></td>
<td><span data-ttu-id="68c0f-158">Nustatykite toliau nurodytus išleistų produktų užsienio prekybos duomenis.</span><span class="sxs-lookup"><span data-stu-id="68c0f-158">Set up the following foreign trade data for released products:</span></span>
<ul>
<li><span data-ttu-id="68c0f-159"><strong>Prekės kodas</strong> – pasirinkite iš pasirinktų prekių sąrašo, gauto iš priskirtų produktų kategorijų, arba iš viso Intrastat prekių kodų sąrašo.</span><span class="sxs-lookup"><span data-stu-id="68c0f-159"><strong>Commodity code</strong> – Select from either the list of selected commodities that is retrieved from assigned product categories or the full list of Intrastat commodity codes.</span></span></li>
<li><span data-ttu-id="68c0f-160"><strong>Statistinis išlaidų procentinis dydis</strong></span><span class="sxs-lookup"><span data-stu-id="68c0f-160"><strong>Statistical charges percentage</strong></span></span></li>
<li><span data-ttu-id="68c0f-161"><strong>Kilmės šalis / regionas</strong> – pasirinkite numatytąją šalį / regioną, kur buvo gautos ar pagamintos visos prekės.</span><span class="sxs-lookup"><span data-stu-id="68c0f-161"><strong>Country/region of origin</strong> – Select the default country/region where the goods were completely obtained or produced.</span></span></li>
<li><span data-ttu-id="68c0f-162"><strong>Kilmės / paskirties apskritis / rajonas</strong> – pasirinkite numatytąją gavimo paskirties apskritį / rajoną ir išsiuntimo kilmės rajoną / apskritį.</span><span class="sxs-lookup"><span data-stu-id="68c0f-162"><strong>State/province of origin/destination</strong> – Select the default state/province of destination for arrivals and the state/province of origin for dispatches.</span></span></li>
<li><span data-ttu-id="68c0f-163"><strong>Grynasis svoris, kg</strong></span><span class="sxs-lookup"><span data-stu-id="68c0f-163"><strong>Net weight in kg</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68c0f-164">Klientai</span><span class="sxs-lookup"><span data-stu-id="68c0f-164">Customers</span></span></td>
<td><span data-ttu-id="68c0f-165">Nustatykite kliento pristatymo adresą ES šalyje / regione.</span><span class="sxs-lookup"><span data-stu-id="68c0f-165">Set up the customer delivery address in the EU country/region.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68c0f-166">Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="68c0f-166">Vendors</span></span></td>
<td><span data-ttu-id="68c0f-167">Nustatykite tiekėjo adresą ES šalyje / regione.</span><span class="sxs-lookup"><span data-stu-id="68c0f-167">Set up the vendor address in the EU country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68c0f-168">Papildomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="68c0f-168">Miscellaneous charges</span></span></td>
<td><span data-ttu-id="68c0f-169">Nustatykite papildomų išlaidų kodą, kurį reikia įtraukti į SF sumą, į statistinę sumą arba į jas abi.</span><span class="sxs-lookup"><span data-stu-id="68c0f-169">Set up the miscellaneous charges code to include in the invoice amount, the statistical amount, or both.</span></span> <span data-ttu-id="68c0f-170"><strong>Išlaidų kodų</strong> puslapyje, <strong>Užsienio prekybos</strong> skirtuke įgalinkite <strong>Intrastat SF vertę</strong>, kad išlaidų suma būtų įtraukta į SF vertę, ir įgalinkite <strong>Intrastat statistinę vertę</strong>, kad išlaidų suma būtų įtraukta į statistinę vertę.</span><span class="sxs-lookup"><span data-stu-id="68c0f-170">On the <strong>Charges codes</strong> page, on the <strong>Foreign trade</strong> tab, enable <strong>Intrastat invoice value</strong> to include the charges amount in the invoice value, and enable <strong>Intrastat statistical value</strong> to include the charges amount in the statistical value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68c0f-171">Elektroninė ataskaita</span><span class="sxs-lookup"><span data-stu-id="68c0f-171">Electronic reporting</span></span></td>
<td><span data-ttu-id="68c0f-172">Nustatykite elektroninių ataskaitų konfigūracijas, kad Intrastat duomenys būtų eksportuojami elektroninio failo formatu, kurio reikalauja aktualios institucijos, ir kad Intrastat duomenis peržiūrėtumėte naudotojui patogiu, įskaitomu formatu (pvz., „Microsoft Excel“).</span><span class="sxs-lookup"><span data-stu-id="68c0f-172">Set up electronic reporting configurations to export Intrastat data in an electronic file that has the format that is requested by the relevant authorities, and to preview Intrastat data in a user-friendly, readable format (for example, in Microsoft Excel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68c0f-173">Sandėliavimas</span><span class="sxs-lookup"><span data-stu-id="68c0f-173">Warehousing</span></span></td>
<td><span data-ttu-id="68c0f-174">Tiekėjų sąskaitas susieti su sandėlio kodais, kad būtų galima įvesti mokesčių lengvatos numerį perkeliant perkėlimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="68c0f-174">Associate vendor accounts with warehouse codes for filling tax exempt number when transferring Transfer order.</span></span></td>
</tr>
</tbody>
</table>

## <a name="setup"></a><span data-ttu-id="68c0f-175">Sąranka</span><span class="sxs-lookup"><span data-stu-id="68c0f-175">Setup</span></span>
<span data-ttu-id="68c0f-176">Toliau pateikiamuose skyriuose aprašomos nuostatos, kurios reikalingos kuriant Intrastat ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="68c0f-176">The following sections describe the settings that are required for Intrastat reporting.</span></span>

### <a name="set-up-all-required-intrastat-related-lists"></a><span data-ttu-id="68c0f-177">Nustatyti visus reikiamus su Intrastat susijusius sąrašus</span><span class="sxs-lookup"><span data-stu-id="68c0f-177">Set up all required Intrastat-related lists</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68c0f-178">Sąrašas</span><span class="sxs-lookup"><span data-stu-id="68c0f-178">List</span></span></th>
<th><span data-ttu-id="68c0f-179">Papildoma informacija</span><span class="sxs-lookup"><span data-stu-id="68c0f-179">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68c0f-180">Prekių kodai</span><span class="sxs-lookup"><span data-stu-id="68c0f-180">Commodity codes</span></span></td>
<td><span data-ttu-id="68c0f-181">Nustatykite <strong>Prekės kodo</strong> tipo kategorijų hierarchiją ir pagal jungtinį nomenklatūrų sąrašą įveskite visų prekių kodus.</span><span class="sxs-lookup"><span data-stu-id="68c0f-181">Set up a category hierarchy of type <strong>Commodity code</strong>, and enter all commodity codes according to the combined nomenclature list.</span></span> <span data-ttu-id="68c0f-182">Kiekvienai prekei nustatykite toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="68c0f-182">For each commodity, you set up the following information:</span></span>
<ul>
<li><span data-ttu-id="68c0f-183">Prekės pavadinimas ir prekės kodas.</span><span class="sxs-lookup"><span data-stu-id="68c0f-183">The name of the commodity and the commodity code</span></span></li>
<li><span data-ttu-id="68c0f-184">Patogus pavadinimas ir (arba) išverstas pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="68c0f-184">The friendly name and/or translated name</span></span></li>
<li><span data-ttu-id="68c0f-185">Papildomų vienetų skelbimo parametrai skirtuke <strong>Užsienio prekyba</strong>. Papildomą vienetą galite pasirinkti vienetų sąraše.</span><span class="sxs-lookup"><span data-stu-id="68c0f-185">Settings for reporting additional (supplementary) units on the <strong>Foreign trade</strong> tab. You can select the additional unit in the unit list.</span></span> <span data-ttu-id="68c0f-186">Taip pat galite nurodyti, ar be pasirinkto papildomo vieneto reikia skelbti prekių svorį.</span><span class="sxs-lookup"><span data-stu-id="68c0f-186">You can also specify whether the weight of commodities must be reported in addition to the selected additional unit.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68c0f-187">Operacijų kodai</span><span class="sxs-lookup"><span data-stu-id="68c0f-187">Transaction codes</span></span></td>
<td><span data-ttu-id="68c0f-188">Pagal savo šalies / regiono reikalavimus nustatykite operacijos pobūdį.</span><span class="sxs-lookup"><span data-stu-id="68c0f-188">Set up the nature of the transaction according to your country&#39;s/region&#39;s requirements.</span></span> <span data-ttu-id="68c0f-189">Kiekvienam operacijos kodui, kurį nustatote, turite nustatyti taisykles, skirtas skaičiuoti perkėlimo užsakymų ir pardavimo / pirkimo užsakymų SF sumoms ir statistinėms sumoms.</span><span class="sxs-lookup"><span data-stu-id="68c0f-189">For each transaction code that you set up, you must set up the rules for calculating invoice amounts and statistical amounts for transfer orders and sales/purchase orders.</span></span>
<ul>
<li><span data-ttu-id="68c0f-190">Perkėlimo užsakymams nustatote vieną iš toliau pateiktų SF sumų ir statistinių sumų skaičiavimo taisyklių.</span><span class="sxs-lookup"><span data-stu-id="68c0f-190">For transfer orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="68c0f-191"><strong>Tuščia</strong> – suma bus 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="68c0f-191"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="68c0f-192"><strong>Finansinių išlaidų suma</strong> – suma bus lygi finansinėms išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="68c0f-192"><strong>Financial cost amount</strong> – The amount will be equal to the financial cost.</span></span></li>
<li><span data-ttu-id="68c0f-193"><strong>Bendrosios išlaidos</strong> – suma bus lygi benrosioms operacijos išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="68c0f-193"><strong>Total cost</strong> – The amount will be equal to the total cost of the transaction.</span></span></li>
<li><span data-ttu-id="68c0f-194"><strong>Rankin.</strong> – suma bus lygi sumai, kuri rankiniu būdu nurodyta perkėlimo užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="68c0f-194"><strong>Manual</strong> – The amount will be equal to the amount that is manually specified on the transfer order line.</span></span></li>
</ul></li>
<li><span data-ttu-id="68c0f-195">Pardavimo užsakymams ir pirkimo užsakymams nustatote vieną iš toliau pateiktų SF sumų ir statistinių sumų skaičiavimo taisyklių.</span><span class="sxs-lookup"><span data-stu-id="68c0f-195">For sales orders and purchase orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="68c0f-196"><strong>Tuščia</strong> – suma bus 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="68c0f-196"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="68c0f-197"><strong>SF suma</strong> – suma bus lygi prekės sumai, kuriai išrašyta SF.</span><span class="sxs-lookup"><span data-stu-id="68c0f-197"><strong>Invoice amount</strong> – The amount will be equal to the amount that is invoiced for the commodity.</span></span></li>
<li><span data-ttu-id="68c0f-198"><strong>Bazinė suma</strong> – suma bus lygi sumai, kuriai būtų išrašoma SF prieš taikant bet kokią nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="68c0f-198"><strong>Base amount</strong> – The amount will be equal to the amount that would be invoiced before any discount is applied.</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68c0f-199">Transportavimo metodai</span><span class="sxs-lookup"><span data-stu-id="68c0f-199">Transport methods</span></span></td>
<td><span data-ttu-id="68c0f-200">Pagal savo šalies / regiono reikalavimus nustatykite transportavimo būdą.</span><span class="sxs-lookup"><span data-stu-id="68c0f-200">Set up the transport mode according to your country&#39;s/region&#39;s requirements.</span></span> <span data-ttu-id="68c0f-201">Kiekvieno pristatymo būdo numatytąjį transportavimo būdą galite nustatyti <strong>Užsienio prekybos</strong> skirtuke.</span><span class="sxs-lookup"><span data-stu-id="68c0f-201">For each delivery mode, you can set up a default transport method on the <strong>Foreign trade</strong> tab.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68c0f-202">Uostai</span><span class="sxs-lookup"><span data-stu-id="68c0f-202">Ports</span></span></td>
<td><span data-ttu-id="68c0f-203">Jei toki informacija yra renkama jūsų šalyje / regione, nustatykite pakrovimo / iškrovimo uostą / oro uostą.</span><span class="sxs-lookup"><span data-stu-id="68c0f-203">Set up the port/airport of loading/unloading if this information is collected by your country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68c0f-204">Statistikos procedūros</span><span class="sxs-lookup"><span data-stu-id="68c0f-204">Statistics procedures</span></span></td>
<td><span data-ttu-id="68c0f-205">Jei tokia informacija yra renkama jūsų šalyje / regione, nustatykite statistinę procedūrą.</span><span class="sxs-lookup"><span data-stu-id="68c0f-205">Set up the statistical procedure if this information is collected by your country/region.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a><span data-ttu-id="68c0f-206">Nustatyti Intrastat operacijų glaudinimo taisykles</span><span class="sxs-lookup"><span data-stu-id="68c0f-206">Set up rules for compressing Intrastat transactions</span></span>

<span data-ttu-id="68c0f-207">**Intrastat glaudinimo** puslapyje galite pasirinkti laukus, kurie bus naudojami glaudinant.</span><span class="sxs-lookup"><span data-stu-id="68c0f-207">On the **Compression of Intrastat** page, you can select the fields to use for compression.</span></span> <span data-ttu-id="68c0f-208">Intrastat žurnale paleidus funkciją Glaudinti, visos operacijos, kurių Intrastat žurnale pasirinktų laukų reikšmių deriniai bus tokie patys, bus suglaudintos į vieną operaciją.</span><span class="sxs-lookup"><span data-stu-id="68c0f-208">All transactions that have the same combination of values for the selected fields in the Intrastat journal will be compressed into a single transaction when you run the Compress function in the Intrastat journal.</span></span>

### <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="68c0f-209">Nustatyti užsienio prekybos parametrus</span><span class="sxs-lookup"><span data-stu-id="68c0f-209">Set up foreign trade parameters</span></span>

<span data-ttu-id="68c0f-210">Norėdami nustatyti toliau pateiktos lentelės parametrus, naudokite **Užsienio prekybos parametrų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="68c0f-210">Use the **Foreign trade parameters** page to set up the parameters in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68c0f-211">Tabuliavimo ženklas</span><span class="sxs-lookup"><span data-stu-id="68c0f-211">Tab</span></span></th>
<th><span data-ttu-id="68c0f-212">Parametrai</span><span class="sxs-lookup"><span data-stu-id="68c0f-212">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68c0f-213">Bendra</span><span class="sxs-lookup"><span data-stu-id="68c0f-213">General</span></span></td>
<td><ul>
<li><span data-ttu-id="68c0f-214"><strong>Bendra</strong> – nurodykite toliau pateiktą informaciją.</span><span class="sxs-lookup"><span data-stu-id="68c0f-214"><strong>General</strong> – Specify the following information:</span></span>
<ul>
<li><span data-ttu-id="68c0f-215">Pardavimo užsakymų, pirkimo užsakymų, kredito pažymų ir perkėlimo užsakymų numatytuosius operacijų kodus.</span><span class="sxs-lookup"><span data-stu-id="68c0f-215">The default transaction codes for sales orders, purchase orders, credit notes, and transfer orders.</span></span> <span data-ttu-id="68c0f-216">Nustatytas kredito pažymų operacijų kodas taip pat naudojamas kaip fizinių prekių grąžinimo kodas bei naudojamas gretinti nuokrypio fizinių prekių grąžinimams ir koregavimo kredito pažymoms.</span><span class="sxs-lookup"><span data-stu-id="68c0f-216">The transaction code that is set up for credit notes is also used as the code for physical goods return and is used for deviating physical returns versus correction credit notes.</span></span></li>
<li><span data-ttu-id="68c0f-217">Darbuotojas, atsakingas už Intrastat ataskaitų rengimą.</span><span class="sxs-lookup"><span data-stu-id="68c0f-217">The employee who is responsible for preparing Intrastat reports.</span></span></li>
</ul></li>
<li><span data-ttu-id="68c0f-218"><strong>Minimali riba</strong> – nurodykite nuostatas, skirtas naujinti operacijoms, kurios yra žemiau ribinės reikšmės.</span><span class="sxs-lookup"><span data-stu-id="68c0f-218"><strong>Minimum limit</strong> – Specify the settings for updating transactions that are below the threshold:</span></span>
<ul>
<li><span data-ttu-id="68c0f-219">Ribinė suma ir svoris.</span><span class="sxs-lookup"><span data-stu-id="68c0f-219">The threshold amount and weight</span></span></li>
<li><span data-ttu-id="68c0f-220">Prekės kodas, taikytinas operacijoms, esančioms žemiau ribinės reikšmės</span><span class="sxs-lookup"><span data-stu-id="68c0f-220">The commodity code to apply to transactions that are under the threshold</span></span></li>
</ul></li>
<li><span data-ttu-id="68c0f-221"><strong>Perkėlimas</strong> – nurodykite operacijų perkėlimo į Intrastat žurnalą kriterijus.</span><span class="sxs-lookup"><span data-stu-id="68c0f-221"><strong>Transfer</strong> – Specify the criteria for transferring transactions to the Intrastat journal.</span></span> <span data-ttu-id="68c0f-222">Galite nurodyti, kad operacijos būtų perkeliamos tik tada, kai prekės atitinka vieną ar visus toliau nurodytus kriterijus.</span><span class="sxs-lookup"><span data-stu-id="68c0f-222">You can specify that transactions are transferred only when the items meet one or all of the following criteria:</span></span>
<ul>
<li><span data-ttu-id="68c0f-223">Prekės nėra aptarnavimo prekės.</span><span class="sxs-lookup"><span data-stu-id="68c0f-223">The items aren&#39;t service items.</span></span></li>
<li><span data-ttu-id="68c0f-224">Prekės turi prekės kodą.</span><span class="sxs-lookup"><span data-stu-id="68c0f-224">The items have a commodity code.</span></span></li>
<li><span data-ttu-id="68c0f-225">Prekės turi svorį.</span><span class="sxs-lookup"><span data-stu-id="68c0f-225">The items have a weight.</span></span></li>
<li><span data-ttu-id="68c0f-226">Prekės turi papildomų vienetų.</span><span class="sxs-lookup"><span data-stu-id="68c0f-226">The items have additional units.</span></span></li>
</ul></li>
<li><span data-ttu-id="68c0f-227"><strong>Tikrinti sąranką</strong> – nurodykite taisykles, skirtas tikrinti Intrastat duomenų užbaigtumui.</span><span class="sxs-lookup"><span data-stu-id="68c0f-227"><strong>Check setup</strong> – Specify the rules for validating the completeness of Intrastat data.</span></span> <span data-ttu-id="68c0f-228">Galite pasirinkti, kuriuos duomenis tikrinti.</span><span class="sxs-lookup"><span data-stu-id="68c0f-228">You can select which data is validated.</span></span></li>
<li><span data-ttu-id="68c0f-229"><strong>Apvalinimo taisyklės</strong> – nurodykite toliau pateiktas sumų ir svorių apvalinimo Intrastat ataskaitose nuostatas.</span><span class="sxs-lookup"><span data-stu-id="68c0f-229"><strong>Rounding rules</strong> – Specify the following settings for rounding amounts and weights in Intrastat reporting:</span></span>
<ul>
<li><span data-ttu-id="68c0f-230">Apvalinimo taisyklė (tikslumas).</span><span class="sxs-lookup"><span data-stu-id="68c0f-230">The rounding rule (precision)</span></span></li>
<li><span data-ttu-id="68c0f-231">Apvalinimo būdas: aukštyn, žemyn arba įprastas.</span><span class="sxs-lookup"><span data-stu-id="68c0f-231">The rounding method: up, down, or normal</span></span></li>
<li><span data-ttu-id="68c0f-232">Sumų ir svorių skaitmenų po kablelio skaičius.</span><span class="sxs-lookup"><span data-stu-id="68c0f-232">The number of decimal places for amounts and weights</span></span></li>
<li><span data-ttu-id="68c0f-233">Svorių, mažesnių nei 1 kilogramas (kg), apvalinimo instrukcijos: iki 1 kg, įprastai arba neapvalinti.</span><span class="sxs-lookup"><span data-stu-id="68c0f-233">Instructions for rounding weights that are less than 1 kilogram (kg): up to 1 kg, normal, or no rounding</span></span></li>
</ul></li>
<li><span data-ttu-id="68c0f-234"><strong>Elektroninės ataskaitos</strong> – nurodykite nuorodas į elektroninių ataskaitų konfigūracijas, kad galėtumėte generuoti elektroninį failą ir ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="68c0f-234"><strong>Electronic reporting</strong> – Specify references to electronic reporting configurations, so that you can generate an electronic file and report.</span></span></li>
<li><span data-ttu-id="68c0f-235"><strong>Prekių kodų hierarchija</strong> – nurodykite <strong>Prekės kodo</strong> tipo, kuris atstoja Intrastat prekės kodą CN8, kategorijų hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="68c0f-235"><strong>Commodity code hierarchy</strong> – Specify the category hierarchy of the <strong>Commodity code</strong> type that represents Intrastat commodity code CN8.</span></span></li>
  <li> <span data-ttu-id="68c0f-236"><strong>Valiutos kurso tipas</strong> – (pasirinktinai) nurodykite valiutos kursą, kuris bus naudojamas Intrastat pardavimo ir pirkimo operacijų ataskaitoms užsienio valiutomis.</span><span class="sxs-lookup"><span data-stu-id="68c0f-236"><strong>Exchange rate type</strong> – Optionally, specify an exchange rate to be used to report Intrastat sales and purchase transactions in foreign currencies.</span></span> <span data-ttu-id="68c0f-237">Tai naudojama, jei tarifas yra kitoks, nei taikomas registruojant operaciją.</span><span class="sxs-lookup"><span data-stu-id="68c0f-237">This is used if the rate is different than the one applied when posting the transaction.</span></span></li>  
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68c0f-238">Agento kontaktinė informacija</span><span class="sxs-lookup"><span data-stu-id="68c0f-238">Agent contact information</span></span></td>
<td><span data-ttu-id="68c0f-239">Nurodykite agento vardą ir pavardę, adresą, mokesčių lengvatos numerį, telefono numerį ir fakso numerį.</span><span class="sxs-lookup"><span data-stu-id="68c0f-239">Specify the agent&#39;s name, address, tax exempt number, telephone number, and fax number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68c0f-240">Šalies / regiono ypatybės</span><span class="sxs-lookup"><span data-stu-id="68c0f-240">Country/region properties</span></span></td>
<td><span data-ttu-id="68c0f-241">Dabartinio juridinio subjekto šalį / regioną nustatykite į <strong>Vietin.</strong>.</span><span class="sxs-lookup"><span data-stu-id="68c0f-241">Set the country/region of the current legal entity to <strong>Domestic</strong>.</span></span> <span data-ttu-id="68c0f-242">ES šalių / regionų, dalyvaujančių ES prekyboje su dabartiniu juridiniu subjektu, šalį / regioną nustatykite į <strong>ES</strong>.</span><span class="sxs-lookup"><span data-stu-id="68c0f-242">Set the country/region of EU countries/regions that participate in EU trade with the current legal entity to <strong>EU</strong>.</span></span> <span data-ttu-id="68c0f-243">Taip pat identifikuojate kiekvienos šalies / regiono kodą, skirtą užsienio prekybai.</span><span class="sxs-lookup"><span data-stu-id="68c0f-243">For each country/region, you also identify country/region code for foreign trade purposes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68c0f-244">Numeravimas</span><span class="sxs-lookup"><span data-stu-id="68c0f-244">Number sequence</span></span></td>
<td><span data-ttu-id="68c0f-245">Nurodykite Intrastat žurnalo numeraciją.</span><span class="sxs-lookup"><span data-stu-id="68c0f-245">Specify the number sequence for the Intrastat journal.</span></span></td>
</tr>
</tbody>
</table>

