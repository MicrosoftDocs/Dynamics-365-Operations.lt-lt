---
title: Nustatykite ir naudokite bangos žymos spausdinimą
description: Šioje temoje aprašytas bangos žymos spausdinimas ir paaiškinta, kaip ją nustatyti.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: configure-wave-label-printing
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 1f51ed9f05caede3d4f320ddb6b705e67df9aa1f
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016960"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="195a2-103">Nustatykite ir naudokite bangos žymos spausdinimą</span><span class="sxs-lookup"><span data-stu-id="195a2-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="195a2-104">Bangos žymos spausdinimas siūlo alternatyvią prieigą prie žymos spausdinimo įtraukiant naują bangos žingsnio metodą, leidžiantį jums sukurti ir spausdinti žymos tiesiogiai iš bango šablono bangos vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="195a2-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="195a2-105">Dėl to, žymės visuomet bus prieinamos prieš tai, kai darbuotojai vykdys darbo užsakymą mobiliame prietaise.</span><span class="sxs-lookup"><span data-stu-id="195a2-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="195a2-106">Darbuotojai gali įtraukti reikiamas žymes paėmimo metu, o ne po jo.</span><span class="sxs-lookup"><span data-stu-id="195a2-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="195a2-107">Bangos žymos spausdinimas naudoja „Zebra Programming Language“ (ZPL) žymos maketo kūrimui.</span><span class="sxs-lookup"><span data-stu-id="195a2-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="195a2-108">Žymos maketas yra padalintas į tris skyrius (antraštė, vidurye ir poraštė) ir leidžia kurti pasikartojančią struktūra turinčias žymes.</span><span class="sxs-lookup"><span data-stu-id="195a2-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="195a2-109">Bangos žymos šablonai sako sistemai, kurią žymos maketą reikia naudoti.</span><span class="sxs-lookup"><span data-stu-id="195a2-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="195a2-110">Vartotojai gali nurodyti, kurį spausdintuvą naudoti.</span><span class="sxs-lookup"><span data-stu-id="195a2-110">Users can specify which printer is used.</span></span> <span data-ttu-id="195a2-111">Jie taip pat gali atspausdinti žymes keliuose spausdintuvuose tuo pačiu metu, jei to reikia.</span><span class="sxs-lookup"><span data-stu-id="195a2-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="195a2-112">**Bangos žymos istorijos** puslapis rodo žymių, kurios buvo sukurtos naudojant šį nustatymą, įrašą.</span><span class="sxs-lookup"><span data-stu-id="195a2-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="195a2-113">Galite atspausdinti ir palyginti žymes pagal darbo antraštes, nes galite atspausdinti padalintas žymes pagal darbo antraštes ir atspausdinti talpyklos turinio žymes, dėžės žymes ir kitas panašias žymes.</span><span class="sxs-lookup"><span data-stu-id="195a2-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="195a2-114">Ši funkcija nepakeičia esančios žymos spausdinimo funkcijos, kuri yra pagrįsta dokumento maršrutu.</span><span class="sxs-lookup"><span data-stu-id="195a2-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="195a2-115">Bangos žymos spausdinimas siūlo šiuo pagerinimus:</span><span class="sxs-lookup"><span data-stu-id="195a2-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="195a2-116">Spausdinkite žymos pagal dėžių numerį vienoje darbo linijoje nenaudojant talpinimo į talpyklas.</span><span class="sxs-lookup"><span data-stu-id="195a2-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="195a2-117">(„dėžė“ yra objektas sukurtas objekto sekos grupės linijose.)</span><span class="sxs-lookup"><span data-stu-id="195a2-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="195a2-118">Atspausdinkite keletą skirtingų žymių sekų (pavyzdžiui, dėžės ir padėklo žymes).</span><span class="sxs-lookup"><span data-stu-id="195a2-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="195a2-119">Įtraukite žymos numeravimą (pavyzdžiui, 1/124, 2/124, ... 124/124) ir nustatykite numeravimo intervalą (pavyzdžiui, darbo liniją, apkrovos liniją ar siuntimą).</span><span class="sxs-lookup"><span data-stu-id="195a2-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="195a2-120">Sukurkite ir atspausdinkite važtarščio identifikavimo numerį žymėse prieš važtaraščio sugeneravimą.</span><span class="sxs-lookup"><span data-stu-id="195a2-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="195a2-121">Sukurkite unikalų serijinį siuntimo talpyklos kodą (SSCC) kiekvienai dėžėi ir įtraukite jį į kiekvieną žymę.</span><span class="sxs-lookup"><span data-stu-id="195a2-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="195a2-122">Sukurkite GS1-atitinkančias numerio sekas važtaraščio identifikavimo kodamas ir SSCC kodams.</span><span class="sxs-lookup"><span data-stu-id="195a2-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="195a2-123">Etikečių naujas spausdinimas mobiliame prietaise ir praturtintame kliente.</span><span class="sxs-lookup"><span data-stu-id="195a2-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="195a2-124">Panaikinkite žymes (pavyzdžiui, trumpo paėmimo scenarijuose) ir spausdinkite juos dar kartą.</span><span class="sxs-lookup"><span data-stu-id="195a2-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="195a2-125">Išvalykite bangos žymės istoriją.</span><span class="sxs-lookup"><span data-stu-id="195a2-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="195a2-126">Dokumento maršruto pagerinimais yra dalijimasi tarp dokumento maršruto maketų ir bangos žymos maketų.</span><span class="sxs-lookup"><span data-stu-id="195a2-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="195a2-127">(Dėl išsamesnės informacijos, žr. [Dokumento maršruto maketas licencijų numeriams](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="195a2-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="195a2-128">Šie pagerinimai padaro žymos dėžes efektyvesnes prieš sudėjimą ant padėklų.</span><span class="sxs-lookup"><span data-stu-id="195a2-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="195a2-129">Jie ypač pasitarnauja bendrovėms siunčiančioms dideliems prekybininkams, kurie automatiškai patvirtina užsakymo kvitą nuskaitydami kiekvieną dėžę atskirai.</span><span class="sxs-lookup"><span data-stu-id="195a2-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="195a2-130">Galite įgyvendinti konfigūraciją scenarijams, kurie aprašyti šiame skyriuje atskirai ar kartu, priklausomai nuo verslo reikalavimų.</span><span class="sxs-lookup"><span data-stu-id="195a2-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="195a2-131">Galite suprojektuoti keletą bangos žymos šablonų, kurie dirba sekoje (kaip parodyta scenarijuje 3).</span><span class="sxs-lookup"><span data-stu-id="195a2-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="195a2-132">Pavyzdžiui, galite naudoti scenarijų 1 tam, kad atspausdintumėte dėžės žymes ir scnearijų 2, kad atspausdintumėte padėklo žymes (jei padėklai sandėlyje skiriasi dydžiu ir sudėtimi).</span><span class="sxs-lookup"><span data-stu-id="195a2-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="195a2-133">Įjunkite bangos žymos spausdinimo savybę</span><span class="sxs-lookup"><span data-stu-id="195a2-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="195a2-134">Prieš naudodami šią funkciją, *Bangos žymos spausdinimas* savybę, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="195a2-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="195a2-135">Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="195a2-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="195a2-136">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="195a2-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="195a2-137">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="195a2-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="195a2-138">**Savybės pavadinimas:** *Bangos žymos spausdinimas*</span><span class="sxs-lookup"><span data-stu-id="195a2-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="195a2-139">Scenarijus 1: Bangos žymos spausdinimas, kai atskira bangos žymė yra sukuriama</span><span class="sxs-lookup"><span data-stu-id="195a2-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="195a2-140">Šis scenarijus rodo, kaip bendrovė gali spausdinti siuntimo žymes dideliems prekybininkams, kurie automatiškai tvirtina užsakymo kvitus nuskaitydami kiekvieną dėžę atskirai.</span><span class="sxs-lookup"><span data-stu-id="195a2-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="195a2-141">Šis scenarijus parodo srautą nuo pradžios iki galo.</span><span class="sxs-lookup"><span data-stu-id="195a2-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="195a2-142">Demonstracinių duomenų įgalinimas</span><span class="sxs-lookup"><span data-stu-id="195a2-142">Make demo data available</span></span>

<span data-ttu-id="195a2-143">Šio scenarijaus įgyvendinimui, privalote turėti įdiegtus demo duomenis ir pasirinkti **USMF** juridinį asmenį.</span><span class="sxs-lookup"><span data-stu-id="195a2-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="195a2-144">Įsitikinkite, kad bangos žymos metodas yra prieinamas</span><span class="sxs-lookup"><span data-stu-id="195a2-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="195a2-145">Jums gali reikėti iš naujo sukurti bangos proceso metodus tam, kad padarytumėte prieinamą bangos etiketės spausdinimo metodą.</span><span class="sxs-lookup"><span data-stu-id="195a2-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="195a2-146">Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos apdorojimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="195a2-147">Patvirinkite, kad **bangos žymos spausdinimas** yra sąraše.</span><span class="sxs-lookup"><span data-stu-id="195a2-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="195a2-148">Jei jo nėra, pasirinkite **Iš naujo kurti metodu** veiksmų juostoje ir juos įtraukite.</span><span class="sxs-lookup"><span data-stu-id="195a2-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="195a2-149">Sukonfigūruokite bangos šabloną</span><span class="sxs-lookup"><span data-stu-id="195a2-149">Configure a wave template</span></span>

<span data-ttu-id="195a2-150">Bangos šablonas leidžia jums susieti konkrečius bangų metodų atvejus pagal atitinkantį bangos žymos šabloną.</span><span class="sxs-lookup"><span data-stu-id="195a2-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="195a2-151">Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="195a2-152">Pasirinkite šabloną, tokį kaip **62 siuntimo nustatytąjį**.</span><span class="sxs-lookup"><span data-stu-id="195a2-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="195a2-153">**Metodai** „FastTab“, patraukite **bangos žymosspausdinimo** metodą į **Pasirinkti metodai** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="195a2-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="195a2-154">**Pasirinkti metodai** stulpelyje, pasirinkite **bangos žymosspausdinimo** metodą ir nustatykite jo **Bangos žingsnio kodo** laukelį į *Spausdinti žymę*.</span><span class="sxs-lookup"><span data-stu-id="195a2-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="195a2-155">Dėl išsamesnės informacijos apie bangos žingsnio kodus, žr. [Bangos žingsnio kodai](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="195a2-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="195a2-156">Sukurkite bangos žymosmaketą</span><span class="sxs-lookup"><span data-stu-id="195a2-156">Create a wave label layout</span></span>

<span data-ttu-id="195a2-157">Žymos maketas kontroliuoja, kokia informacija yra spausdinama žymėje ir kaip ji yra padėta. Čia galite įvesti ZPL kodą, kuris nusiunčiamas spausdintuvui.</span><span class="sxs-lookup"><span data-stu-id="195a2-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="195a2-158">Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymos maketai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="195a2-159">Sukurkite įrašą, kuris turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="195a2-160">**Žymos maketo identifikavimo numeris:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="195a2-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="195a2-161">**Aprašas:** *Dėžė (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="195a2-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="195a2-162">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="195a2-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="195a2-163">Veiksmų juostoje pasirinkite **bangos žymoseilutės nustatymai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="195a2-164">Pasirodo **bangos žymoseilutės nustatymai** langas.</span><span class="sxs-lookup"><span data-stu-id="195a2-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="195a2-165">Čia galite sukonfigūruoti dinaminę žymos dalį.</span><span class="sxs-lookup"><span data-stu-id="195a2-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="195a2-166">Įtraukite eilutę, kuri turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-167">**Eilutės Identifikavimo kodas:** *Bangos žymė*</span><span class="sxs-lookup"><span data-stu-id="195a2-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="195a2-168">**Eilutės lentelės pavadinimas:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="195a2-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="195a2-169">**Eilutės pradžios padėtis:** *0*</span><span class="sxs-lookup"><span data-stu-id="195a2-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="195a2-170">Šis laukelis apibrėžia vertikalią padėtį, kurioje eilutė prasideda žymėje.</span><span class="sxs-lookup"><span data-stu-id="195a2-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="195a2-171">**Eilutės aukštis:** *0*</span><span class="sxs-lookup"><span data-stu-id="195a2-171">**Row height:** *0*</span></span>

        <span data-ttu-id="195a2-172">Laukelis apibrėžia kiekvienos eilutės aukštį (taškais) pagal ZPL standartą.</span><span class="sxs-lookup"><span data-stu-id="195a2-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="195a2-173">Eilutės aukštis yra teigiamas horizontalioms žymėms ir neigiamas vertikalioms.</span><span class="sxs-lookup"><span data-stu-id="195a2-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="195a2-174">Kadangi yra tik viena eilutė šiame pavyzdyje, galite nustatyti vertę į *0* (nulį).</span><span class="sxs-lookup"><span data-stu-id="195a2-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="195a2-175">**Eilutės puslapyje:** *1*</span><span class="sxs-lookup"><span data-stu-id="195a2-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="195a2-176">Šis laukelis parodo eilučių skaičių, kuris gali būti atspausdintas kiekvienoje žymėje.</span><span class="sxs-lookup"><span data-stu-id="195a2-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="195a2-177">Šis nustatymas nulems, kad atskira ZPL žymė bus spausdinima kiekvienam įrašui bangos žymių lentelėje.</span><span class="sxs-lookup"><span data-stu-id="195a2-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="195a2-178">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="195a2-178">Close the page.</span></span>
1. <span data-ttu-id="195a2-179">Veiksmų srityje pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="195a2-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="195a2-180">Užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:</span><span class="sxs-lookup"><span data-stu-id="195a2-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-181">**Lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-182">**Išvestinė lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-183">**Laukas:** *Darbo tipas*</span><span class="sxs-lookup"><span data-stu-id="195a2-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="195a2-184">**Kriterijai:** *Paėmimas*</span><span class="sxs-lookup"><span data-stu-id="195a2-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="195a2-185">Ši užklausa užtikrina, kad tik paėmimo tipo darbo linijos bus atspausdintos žymėje, o ne padėjimo tipo darbo linijos.</span><span class="sxs-lookup"><span data-stu-id="195a2-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="195a2-186">Jei norite galėti atspausdinti važtaraščio identifikavimo kodą **Sujungimai** skirtuke, pasirinkite **Darbo linijų** lentelę ir prijunkite prie jo **Siuntimai** lentelę.</span><span class="sxs-lookup"><span data-stu-id="195a2-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="195a2-187">Uždarykite užklausos tvarkylės teksto laukelį.</span><span class="sxs-lookup"><span data-stu-id="195a2-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="195a2-188">**Spausdintuvo teksto maketas** „FastTab“ turi tris skyrius, kuriuose galite rašyti spausdintuvo kodą: **Antraštės skyrius** , **Vidurinės dalies skyrius** ir **Poraštės skyrius**.</span><span class="sxs-lookup"><span data-stu-id="195a2-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="195a2-189">**Antraštės skyrius** skyriuje, **Žymos antraštė** laukelyje įveskite ZPL kodą būtinai antraštei.</span><span class="sxs-lookup"><span data-stu-id="195a2-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="195a2-190">Pavyzdžiui, jei naudojate „Zebra“ spaudintuvus, galite naudoti šį kodą.</span><span class="sxs-lookup"><span data-stu-id="195a2-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="195a2-191">**Vidurinės dalies skyrius** skyriuje, **Žymos vidurinė dalis** laukelyje įveskite ZPL kodą būtinai vidurinei daliai.</span><span class="sxs-lookup"><span data-stu-id="195a2-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="195a2-192">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="195a2-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="195a2-193">**Vidurinės dalies skyrius** skyriuje, **Žymos apatinė dalis** laukelyje įveskite ZPL kodą būtinai apatinei daliai.</span><span class="sxs-lookup"><span data-stu-id="195a2-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="195a2-194">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="195a2-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="195a2-195">Šie nustatymai atspausdins vieną kiekvienos žymos kopiją.</span><span class="sxs-lookup"><span data-stu-id="195a2-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="195a2-196">Jei jums reikia daugiau kopijų (pavyzdžiui, vienos kopijos vienai padėklo pusei), nustatykite **n** vertę **\^PQn** skyriui poraštėje reikiamam kopijų skaičiui.</span><span class="sxs-lookup"><span data-stu-id="195a2-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="195a2-197">Pavyzdžiui, keturių kiekvienos žymos kopijų spausdinimui, nustatykite **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="195a2-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="195a2-198">Jūsų žymė dabar paruošta naudojimui.</span><span class="sxs-lookup"><span data-stu-id="195a2-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="195a2-199">Sukurkite bangos žymostipą</span><span class="sxs-lookup"><span data-stu-id="195a2-199">Create a wave label type</span></span>

<span data-ttu-id="195a2-200">bangos žymostipai naudojami susieti bangos žymosšablonus su padalinio esančio jo sekos grupės linijose.</span><span class="sxs-lookup"><span data-stu-id="195a2-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="195a2-201">Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymostipai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="195a2-202">Įtraukite bangos etiketės tipą, kuris turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="195a2-203">**Žymos tipas:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="195a2-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="195a2-204">**Aprašas:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="195a2-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="195a2-205">Nustatyti vienetų sekų grupes</span><span class="sxs-lookup"><span data-stu-id="195a2-205">Set up unit sequence groups</span></span>

<span data-ttu-id="195a2-206">Po to, nustatykite objekto sekos grupę bangos žymostipui.</span><span class="sxs-lookup"><span data-stu-id="195a2-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="195a2-207">Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Padalinio sekos grupės**.</span><span class="sxs-lookup"><span data-stu-id="195a2-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="195a2-208">Pasirinkite **Ea Box PL** grupę.</span><span class="sxs-lookup"><span data-stu-id="195a2-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="195a2-209">**Dėžutė** linijoje nustatykite **Bangos lygio tipas** laukelį į *Dėžė*.</span><span class="sxs-lookup"><span data-stu-id="195a2-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="195a2-210">Sukurkite bangos žymosšabloną</span><span class="sxs-lookup"><span data-stu-id="195a2-210">Create a wave label template</span></span>

<span data-ttu-id="195a2-211">Po to, sukurkite bangos žymosšabloną bangos žymostipui.</span><span class="sxs-lookup"><span data-stu-id="195a2-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="195a2-212">Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymosšablonai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="195a2-213">Įtraukite bangos lygio šabloną ir nustatykite šias vertes antraštėje:</span><span class="sxs-lookup"><span data-stu-id="195a2-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="195a2-214">**Žymos šablono pavadinimas:** *Dėžių žymės*</span><span class="sxs-lookup"><span data-stu-id="195a2-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="195a2-215">**Aprašas:** *Dėžės žymės*</span><span class="sxs-lookup"><span data-stu-id="195a2-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="195a2-216">**Bangos žingsnio kodas:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="195a2-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="195a2-217">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="195a2-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="195a2-218">**Bendra** „FastTab“, nustatykite **bangos žymostipas** laukelį į *Dėžė*.</span><span class="sxs-lookup"><span data-stu-id="195a2-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="195a2-219">**bangos žymosšablono informacijoje** „FastTab“, įtraukite naują eilutę turinčią šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-220">**Žymos maketo identifikavimo numeris:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="195a2-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="195a2-221">**Spausdintuvo pavadinimas:** Pasirinkite tinkamą ZPL spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="195a2-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="195a2-222">**Vykdykite užklausą:** *Taip* (Šis pasirinkimas yra pasirenkamas, tačiau rekomenduojamas optimaliam veikimui.)</span><span class="sxs-lookup"><span data-stu-id="195a2-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="195a2-223">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="195a2-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="195a2-224">Pasirenkamas: Jei nustatote klientui konkretų žymos maketą, privalote sukurti užklausą tam, kad rastumėte kliento paskyrą.</span><span class="sxs-lookup"><span data-stu-id="195a2-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="195a2-225">**bangos žymos šablono informacijoje** „FastTab“, pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="195a2-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="195a2-226">Tuomet, užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:</span><span class="sxs-lookup"><span data-stu-id="195a2-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-227">**Lentelė:** *Siuntos*</span><span class="sxs-lookup"><span data-stu-id="195a2-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="195a2-228">**Išvestinė lentelė:** *Siuntos*</span><span class="sxs-lookup"><span data-stu-id="195a2-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="195a2-229">**Laukelis:** *Paskyros numeris*</span><span class="sxs-lookup"><span data-stu-id="195a2-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="195a2-230">**Kriterijai:** Įveskite reikiamą kliento paskyros numerį.</span><span class="sxs-lookup"><span data-stu-id="195a2-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="195a2-231">Kai baigsite, pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="195a2-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="195a2-232">Veiksmų juostoje pasirinkite **Redaguoti užklausą** tam, kad atvertumėte užklausos tvarkyklės teksto laukelį visam žymos šablonui.</span><span class="sxs-lookup"><span data-stu-id="195a2-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="195a2-233">Užklausos tvarkyklės teksto laukelyje, **Rūšiavimas** skirtuke įtraukite eilutę su šiais nustatymais:</span><span class="sxs-lookup"><span data-stu-id="195a2-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-234">**Lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-235">**Išvestinė lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-236">**Laukelis:** *Nuorodos krovimo linijos identifikavimo numeris (Record-ID)*</span><span class="sxs-lookup"><span data-stu-id="195a2-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="195a2-237">**Paieškos kryptis:** *Didėjanti*</span><span class="sxs-lookup"><span data-stu-id="195a2-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="195a2-238">Pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="195a2-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="195a2-239">Pranšimo laukelis paskatins jus patvirtinti grupavimo perkrovimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="195a2-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="195a2-240">Pasirinkite **taip** tam, kad tęstumėte.</span><span class="sxs-lookup"><span data-stu-id="195a2-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="195a2-241">Veiksmų juostoje pasirinkite **bangos žymos šablono grupė**.</span><span class="sxs-lookup"><span data-stu-id="195a2-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="195a2-242">**bangos žymos šablono grupės** teksto laukelyje, pasirinkite eilutę, kurioje **Nuorodos laukelio pavadinimas** laukelis nustatytas į *Nuorodos krovimo linijos identifikavimo kodas* ir tuomet pasirinkite **Žymos kūrėjo identifikavimo kodas** žymimą laukelį šioje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="195a2-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id* , and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="195a2-243">Šie nustatyimai sukurs vieną žymos seką („Dėžė 1 X“) vienai krovimo linijai bangoje nepriklausomai nuo darbo grupės nustatymų.</span><span class="sxs-lookup"><span data-stu-id="195a2-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="195a2-244">Ši žymės seka gali būti atspausdinta žymos makete.</span><span class="sxs-lookup"><span data-stu-id="195a2-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="195a2-245">Konfigūruokite numerio sekos plėtinius</span><span class="sxs-lookup"><span data-stu-id="195a2-245">Configure number sequence extensions</span></span>

<span data-ttu-id="195a2-246">Numerio sekos plėtiniai valdo GS1 atitiktį su specifinėmis numerio sekomis.</span><span class="sxs-lookup"><span data-stu-id="195a2-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="195a2-247">Konfigūravimas yra pasirenkamas esamam scenarijui.</span><span class="sxs-lookup"><span data-stu-id="195a2-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="195a2-248">Dėl platesnės informacijos ir konfigūravimo instrukcijų, žr. [Konfigūruoti numerio sekos plėtinius](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="195a2-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="195a2-249">Sukuria prekybos užsakymą ir išleidžia jį į sandėlį</span><span class="sxs-lookup"><span data-stu-id="195a2-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="195a2-250">Eikite į **Prekyba ir komercija \> Prekybos užsakymas \> Visi prekybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="195a2-251">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="195a2-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="195a2-252">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="195a2-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="195a2-253">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="195a2-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="195a2-254">Įtraukite dvi prekybos užsakymo eilutes, turinčias šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="195a2-255">Prekybos užsakymo linija 1:</span><span class="sxs-lookup"><span data-stu-id="195a2-255">Sales order line 1:</span></span>

        - <span data-ttu-id="195a2-256">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="195a2-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="195a2-257">**Kiekis:** *9024*</span><span class="sxs-lookup"><span data-stu-id="195a2-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="195a2-258">**Padalinys:** *ea* (9024 ea = 376 dėžė = 47 padėklai)</span><span class="sxs-lookup"><span data-stu-id="195a2-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="195a2-259">Prekybos užsakymo linija 2:</span><span class="sxs-lookup"><span data-stu-id="195a2-259">Sales order line 2:</span></span>

        - <span data-ttu-id="195a2-260">**Prekės numeris:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="195a2-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="195a2-261">**Kiekis:** *9016*</span><span class="sxs-lookup"><span data-stu-id="195a2-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="195a2-262">**Padalinys:** *ea* (9016 ea = 322 Box = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="195a2-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="195a2-263">Čia pateikiami objektai ir kiekiai yra tik pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="195a2-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="195a2-264">Jie privalo naudoti objekto sekos grupę, kurią nustatėte anksčiau, atitinkantys objekto pakeitimai iš *ea* į *Box* į *PL* turi būti jiems nustatyti ir jie privalo turėti prekių sandėlyje  *62*.</span><span class="sxs-lookup"><span data-stu-id="195a2-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="195a2-265">Dėl platesnės informacijos, žr. [Matavimo vienetas ir sandėliavimo politika](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="195a2-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="195a2-266">Pasirinkite prekybos užsakymo liniją 1:</span><span class="sxs-lookup"><span data-stu-id="195a2-266">Select sales order line 1.</span></span> <span data-ttu-id="195a2-267">Vėliau **Prekybos užsakymo linijos** skyriuje, **Inventoriaus** meniu, pasirinkite **Rezervacijos**.</span><span class="sxs-lookup"><span data-stu-id="195a2-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="195a2-268">**Rezervacijos** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** ir tuomet uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="195a2-268">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="195a2-269">Pakartokite 4 ir 5 žingsnius kiekvienai prekybos užsakymo eilutei 2.</span><span class="sxs-lookup"><span data-stu-id="195a2-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="195a2-270">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="195a2-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="195a2-271">Atistinka šis įvykis:</span><span class="sxs-lookup"><span data-stu-id="195a2-271">The following events occur:</span></span>

    - <span data-ttu-id="195a2-272">Sistema apdoroja sukurtą siuntimą naudodama šabloną apimantį žymos spausdinimo žingsnį.</span><span class="sxs-lookup"><span data-stu-id="195a2-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="195a2-273">Žymos maketas bus naudojamas nustatant žymos formatą ir galutinis rezultatas bus žymė turinti penkias eilutes ir ji yra atspausdinta spausdintuve pasirinktame žymos šablone.</span><span class="sxs-lookup"><span data-stu-id="195a2-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="195a2-274">Bangos žymės yra sukuriamos ir atspausdinamos.</span><span class="sxs-lookup"><span data-stu-id="195a2-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="195a2-275">Žymių skaičius bus lygus dėžių skaičiui (šiame pavyzdyje, 376 dėžės linijai 1 ir 322 dėžės linijai 2).</span><span class="sxs-lookup"><span data-stu-id="195a2-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="195a2-276">Naujas važtaraščio identifikavimo kodas sukuriamas siuntimams.</span><span class="sxs-lookup"><span data-stu-id="195a2-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="195a2-277">Jei sukonfigūravote numerio sekos plėtinius, bangos žymos identifikavimo kodas seks **SSCC-18** numerio formatą.</span><span class="sxs-lookup"><span data-stu-id="195a2-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="195a2-278">Galite peržiūrėti ir iš naujo atspausdinti bangos žymes tolesniuose puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="195a2-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="195a2-279">Veiksmų juostoje kiekviename puslapyje, **Siuntimai** skirtuke, **Susijusi informacija** grupėje, pasirinkite **Bangos žymės**.</span><span class="sxs-lookup"><span data-stu-id="195a2-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="195a2-280">Visi siuntimai \> Siuntimo informacija</span><span class="sxs-lookup"><span data-stu-id="195a2-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="195a2-281">Visi krovimai \> Krovimo informacija</span><span class="sxs-lookup"><span data-stu-id="195a2-281">All loads \> Load details</span></span>
- <span data-ttu-id="195a2-282">Visos bangos</span><span class="sxs-lookup"><span data-stu-id="195a2-282">All waves</span></span>
- <span data-ttu-id="195a2-283">Bangos žymės</span><span class="sxs-lookup"><span data-stu-id="195a2-283">Wave labels</span></span>
- <span data-ttu-id="195a2-284">Bangos žymos retrospektyva</span><span class="sxs-lookup"><span data-stu-id="195a2-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="195a2-285">Scenarijus 2: Bangos žymos spausdinimas talpinimui į talpyklas (be bangos žymos įrašų)</span><span class="sxs-lookup"><span data-stu-id="195a2-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="195a2-286">Šis scenarijus leidžia jums spausdinti bangos žymes naudojant talpinimą į talpyklas automatiškai skaidyti elementus į dėžės ir dėl to nereikalauja bangos žymos įrašo.</span><span class="sxs-lookup"><span data-stu-id="195a2-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="195a2-287">Šiuo atveju, talpyklos identifikavimo kodas veikia kaip SSCC žymuo.</span><span class="sxs-lookup"><span data-stu-id="195a2-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="195a2-288">Čia pateikiami pagrindiniai skirtumai tarp šio scenarijaus ir scenarijaus 1:</span><span class="sxs-lookup"><span data-stu-id="195a2-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="195a2-289">**Bangos žymos šablonai:** Nepasirinksite bangos žymos tipo bangos žymos šablone ir jums nereikės žymos kūrimo grupavimo.</span><span class="sxs-lookup"><span data-stu-id="195a2-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="195a2-290">Kitu atveju, jūs konfigūruosite bangos žymos šabloną ir susiesite bangos šabloną tokiu pačiu būdu aprašytu scenarijuje 1.</span><span class="sxs-lookup"><span data-stu-id="195a2-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="195a2-291">Privalote palikti bangos žymos tipą tuščią, kad apsaugotumėte bangos žymą nuo sukūrimo.</span><span class="sxs-lookup"><span data-stu-id="195a2-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="195a2-292">**Bangos žymos maketai** Sukonfigūruosite bangos žymos maketo eilutės nustatymus darbo linijai vietoje bangos žymos įrašų.</span><span class="sxs-lookup"><span data-stu-id="195a2-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="195a2-293">Privalote sukonfigūruoti eilutės nustatymus žymos maketui naudodami **WHSWorkLine** lentelę vietoje **WHSWaveLabel** lentelės.</span><span class="sxs-lookup"><span data-stu-id="195a2-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="195a2-294">**Eilutės puslapyje** nustatymai kontroliuoja eilutės numerius, kuriuos turi vidurinė sritis.</span><span class="sxs-lookup"><span data-stu-id="195a2-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="195a2-295">Šis konfigiūravimas taip pat tinkamas verslo scenarijams, kai daugelis skirtingų objektų yra supakuojami į vieną žymos dėžę ar į padėklą ir toks pakavimo procesas gali būti nustatytas sukuriant darbą (pavyzdžiui, darbą sugrupuotą siuntimo).</span><span class="sxs-lookup"><span data-stu-id="195a2-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="195a2-296">Šis scenarijus parodo srautą nuo pradžios iki galo.</span><span class="sxs-lookup"><span data-stu-id="195a2-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="195a2-297">Demonstracinių duomenų įgalinimas</span><span class="sxs-lookup"><span data-stu-id="195a2-297">Make demo data available</span></span>

<span data-ttu-id="195a2-298">Šio scenarijaus įgyvendinimui, privalote turėti įdiegtus demo duomenis ir pasirinkti **USMF** juridinį asmenį.</span><span class="sxs-lookup"><span data-stu-id="195a2-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="195a2-299">Įsitikinkite, kad bangos žymos metodas yra prieinamas</span><span class="sxs-lookup"><span data-stu-id="195a2-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="195a2-300">Jums gali reikėti iš naujo sukurti bangos proceso metodus tam, kad padarytumėte prieinamą bangos etiketės spausdinimo metodą.</span><span class="sxs-lookup"><span data-stu-id="195a2-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="195a2-301">Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos apdorojimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="195a2-302">Patvirinkite, kad **bangos žymos spausdinimas** yra sąraše.</span><span class="sxs-lookup"><span data-stu-id="195a2-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="195a2-303">Jei jo nėra, pasirinkite **Iš naujo kurti metodu** veiksmų juostoje ir juos įtraukite.</span><span class="sxs-lookup"><span data-stu-id="195a2-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="195a2-304">Bangos šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="195a2-304">Set up a wave template</span></span>

<span data-ttu-id="195a2-305">Bangos šablonas leidžia jums susieti konkrečius bangų metodų atvejus pagal atitinkantį bangos žymos šabloną.</span><span class="sxs-lookup"><span data-stu-id="195a2-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="195a2-306">Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="195a2-307">Pasirinkite šabloną, tokį kaip **63 talpinimas į talpyklas**.</span><span class="sxs-lookup"><span data-stu-id="195a2-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="195a2-308">**Metodai** „FastTab“, patraukite **bangos žymosspausdinimo** metodą į **Pasirinkti metodai** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="195a2-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="195a2-309">**Pasirinkti metodai** stulpelyje, pasirinkite **bangos žymosspausdinimo** metodą ir nustatykite jo **Bangos žingsnio kodo** laukelį į *Spausdinti žymę*.</span><span class="sxs-lookup"><span data-stu-id="195a2-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="195a2-310">Dėl išsamesnės informacijos apie bangos žingsnio kodus, žr. [Bangos žingsnio kodai](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="195a2-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="195a2-311">Sukurkite bangos žymosmaketą</span><span class="sxs-lookup"><span data-stu-id="195a2-311">Create a wave label layout</span></span>

1. <span data-ttu-id="195a2-312">Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymos maketai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="195a2-313">Sukurkite įrašą, kuris turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="195a2-314">**Žymos maketo identifikavimo numeris:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="195a2-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="195a2-315">**Aprašas:** *Dėžė (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="195a2-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="195a2-316">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="195a2-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="195a2-317">Veiksmų juostoje pasirinkite **bangos žymoseilutės nustatymai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="195a2-318">Pasirodo **bangos žymoseilutės nustatymai** langas.</span><span class="sxs-lookup"><span data-stu-id="195a2-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="195a2-319">Čia galite sukonfigūruoti dinaminę žymos dalį.</span><span class="sxs-lookup"><span data-stu-id="195a2-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="195a2-320">Įtraukite eilutę, kuri turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-321">**Eilutės identifikavimo kodas:** *Darbo eilutė*</span><span class="sxs-lookup"><span data-stu-id="195a2-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="195a2-322">**Eilutės lentelės pavadinimas:** *WHSWaveLine*</span><span class="sxs-lookup"><span data-stu-id="195a2-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="195a2-323">**Eilutės pradžios padėtis:** *500*</span><span class="sxs-lookup"><span data-stu-id="195a2-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="195a2-324">Šis laukelis apibrėžia vertikalią padėtį, kurioje eilutė prasideda žymėje.</span><span class="sxs-lookup"><span data-stu-id="195a2-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="195a2-325">**Eilutės aukštis:** *50*</span><span class="sxs-lookup"><span data-stu-id="195a2-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="195a2-326">Šis laukelis nulemia kiekvienos eilutės aukštį.</span><span class="sxs-lookup"><span data-stu-id="195a2-326">This field defines the height of each row.</span></span> <span data-ttu-id="195a2-327">Eilutės aukštis yra teigiamas horizontalioms žymėms ir neigiamas vertikalioms.</span><span class="sxs-lookup"><span data-stu-id="195a2-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="195a2-328">**Eilutės puslapyje:** *5*</span><span class="sxs-lookup"><span data-stu-id="195a2-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="195a2-329">Šis laukelis parodo eilučių skaičių, kuris gali būti atspausdintas kiekvienoje žymėje.</span><span class="sxs-lookup"><span data-stu-id="195a2-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="195a2-330">Šie nustatymai atspausdins keletą ZPL žymių darbui, kuriose kiekvienas puslapis gali turėti iki penkių darbo eilučių.</span><span class="sxs-lookup"><span data-stu-id="195a2-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="195a2-331">Pavyzdžiui, jei žymė atspausdinama talpyklai turinčiai 12 eilučių, trys eilutės bus atspausdintos.</span><span class="sxs-lookup"><span data-stu-id="195a2-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="195a2-332">Jei norite atspausdinti atskirą žymę kiekvienai paėmimo linijai, nustatykite jos vertę į *1*.</span><span class="sxs-lookup"><span data-stu-id="195a2-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="195a2-333">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="195a2-333">Close the page.</span></span>
1. <span data-ttu-id="195a2-334">Veiksmų srityje pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="195a2-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="195a2-335">Užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:</span><span class="sxs-lookup"><span data-stu-id="195a2-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-336">**Lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-337">**Išvestinė lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-338">**Laukas:** *Darbo tipas*</span><span class="sxs-lookup"><span data-stu-id="195a2-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="195a2-339">**Kriterijai:** *Paėmimas*</span><span class="sxs-lookup"><span data-stu-id="195a2-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="195a2-340">Jei norite galėti atspausdinti važtaraščio identifikavimo kodą **Sujungimai** skirtuke, pasirinkite **Darbo linijų** lentelę ir prijunkite prie jo **Siuntimai** lentelę.</span><span class="sxs-lookup"><span data-stu-id="195a2-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="195a2-341">Uždarykite užklausos tvarkylės teksto laukelį.</span><span class="sxs-lookup"><span data-stu-id="195a2-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="195a2-342">**Spausdintuvo teksto maketas** „FastTab“ turi tris skyrius, kuriuose galite rašyti spausdintuvo kodą: **Antraštės skyrius** , **Vidurinės dalies skyrius** ir **Poraštės skyrius**.</span><span class="sxs-lookup"><span data-stu-id="195a2-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="195a2-343">**Antraštės skyrius** skyriuje, **Žymos antraštė** laukelyje įveskite ZPL kodą būtinai antraštei.</span><span class="sxs-lookup"><span data-stu-id="195a2-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="195a2-344">Pavyzdžiui, jei naudojate „Zebra“ spaudintuvus, galite naudoti šį kodą.</span><span class="sxs-lookup"><span data-stu-id="195a2-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="195a2-345">**Vidurinės dalies skyrius** skyriuje, **Žymos vidurinė dalis** laukelyje įveskite ZPL kodą būtinai vidurinei daliai.</span><span class="sxs-lookup"><span data-stu-id="195a2-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="195a2-346">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="195a2-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="195a2-347">**Vidurinės dalies skyrius** skyriuje, **Žymos apatinė dalis** laukelyje įveskite ZPL kodą būtinai apatinei daliai.</span><span class="sxs-lookup"><span data-stu-id="195a2-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="195a2-348">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="195a2-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="195a2-349">Šie nustatymai atspausdins vieną kiekvienos žymos kopiją.</span><span class="sxs-lookup"><span data-stu-id="195a2-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="195a2-350">Jei jums reikia daugiau kopijų (pavyzdžiui, vienos kopijos vienai padėklo pusei), nustatykite **n** vertę **\^PQn** skyriui poraštėje reikiamam kopijų skaičiui.</span><span class="sxs-lookup"><span data-stu-id="195a2-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="195a2-351">Pavyzdžiui, keturių kiekvienos žymos kopijų spausdinimui, nustatykite **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="195a2-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="195a2-352">Jūsų žymė dabar paruošta naudojimui.</span><span class="sxs-lookup"><span data-stu-id="195a2-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="195a2-353">Sukurkite bangos žymosšabloną</span><span class="sxs-lookup"><span data-stu-id="195a2-353">Create a wave label template</span></span>

1. <span data-ttu-id="195a2-354">Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymosšablonai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="195a2-355">Įtraukite bangos lygio šabloną ir nustatykite šias vertes antraštėje:</span><span class="sxs-lookup"><span data-stu-id="195a2-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="195a2-356">**Žymos šablono pavadinimas:** *Talpyklų žymės*</span><span class="sxs-lookup"><span data-stu-id="195a2-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="195a2-357">**Aprašas:** *Talpyklų žymės*</span><span class="sxs-lookup"><span data-stu-id="195a2-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="195a2-358">**Bangos žingsnio kodas:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="195a2-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="195a2-359">**Sandėlis:** *63*</span><span class="sxs-lookup"><span data-stu-id="195a2-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="195a2-360">**Bangos žymos šablono informacijoje** „FastTab“, įtraukite eilutę turinčią šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-361">**Žymos maketo identifikavimo numeris:** *Talpykla*</span><span class="sxs-lookup"><span data-stu-id="195a2-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="195a2-362">**Spausdintuvo pavadinimas:** Pasirinkite tinkamą ZPL spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="195a2-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="195a2-363">**Vykdykite užklausą:** *Taip* (Šis pasirinkimas yra pasirenkamas, tačiau rekomenduojamas optimaliam veikimui.)</span><span class="sxs-lookup"><span data-stu-id="195a2-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="195a2-364">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="195a2-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="195a2-365">Pasirenkamas: Jei nustatote klientui konkretų žymos maketą, privalote sukurti užklausą tam, kad rastumėte kliento paskyrą.</span><span class="sxs-lookup"><span data-stu-id="195a2-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="195a2-366">**bangos žymos šablono informacijoje** „FastTab“, pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="195a2-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="195a2-367">Tuomet, užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:</span><span class="sxs-lookup"><span data-stu-id="195a2-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-368">**Lentelė:** *Siuntos*</span><span class="sxs-lookup"><span data-stu-id="195a2-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="195a2-369">**Išvestinė lentelė:** *Siuntos*</span><span class="sxs-lookup"><span data-stu-id="195a2-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="195a2-370">**Laukelis:** *Paskyros numeris*</span><span class="sxs-lookup"><span data-stu-id="195a2-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="195a2-371">**Kriterijai:** Įveskite reikiamą kliento paskyros numerį.</span><span class="sxs-lookup"><span data-stu-id="195a2-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="195a2-372">Kai baigsite, pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="195a2-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="195a2-373">Konfigūruokite numerio sekos plėtinius</span><span class="sxs-lookup"><span data-stu-id="195a2-373">Configure number sequence extensions</span></span>

<span data-ttu-id="195a2-374">Numerio sekos plėtiniai valdo GS1 atitiktį su specifinėmis numerio sekomis.</span><span class="sxs-lookup"><span data-stu-id="195a2-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="195a2-375">Konfigūravimas yra pasirenkamas esamam scenarijui.</span><span class="sxs-lookup"><span data-stu-id="195a2-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="195a2-376">Dėl platesnės informacijos ir konfigūravimo instrukcijų, žr. [Konfigūruoti numerio sekos plėtinius](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="195a2-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="195a2-377">Sukuria prekybos užsakymą ir išleidžia jį į sandėlį</span><span class="sxs-lookup"><span data-stu-id="195a2-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="195a2-378">Eikite į **Prekyba ir komercija \> Prekybos užsakymas \> Visi prekybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="195a2-379">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="195a2-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="195a2-380">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="195a2-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="195a2-381">**Sandėlis:** *63*</span><span class="sxs-lookup"><span data-stu-id="195a2-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="195a2-382">Įtraukite penkias prekybos užsakymo eilutes:</span><span class="sxs-lookup"><span data-stu-id="195a2-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="195a2-383">Prekybos užsakymo linija 1:</span><span class="sxs-lookup"><span data-stu-id="195a2-383">Sales order line 1:</span></span>

        - <span data-ttu-id="195a2-384">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="195a2-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="195a2-385">**Kiekis:** *10*</span><span class="sxs-lookup"><span data-stu-id="195a2-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="195a2-386">Prekybos užsakymo linija 2:</span><span class="sxs-lookup"><span data-stu-id="195a2-386">Sales order line 2:</span></span>

        - <span data-ttu-id="195a2-387">**Prekės numeris:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="195a2-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="195a2-388">**Kiekis:** *20*</span><span class="sxs-lookup"><span data-stu-id="195a2-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="195a2-389">Prekybos užsakymo linija 3:</span><span class="sxs-lookup"><span data-stu-id="195a2-389">Sales order line 3:</span></span>

        - <span data-ttu-id="195a2-390">**Prekės numeris:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="195a2-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="195a2-391">**Kiekis:** *20*</span><span class="sxs-lookup"><span data-stu-id="195a2-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="195a2-392">Prekybos užsakymo linija 4:</span><span class="sxs-lookup"><span data-stu-id="195a2-392">Sales order line 4:</span></span>

        - <span data-ttu-id="195a2-393">**Prekės numeris:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="195a2-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="195a2-394">**Kiekis:** *40*</span><span class="sxs-lookup"><span data-stu-id="195a2-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="195a2-395">Prekybos užsakymo linija 5:</span><span class="sxs-lookup"><span data-stu-id="195a2-395">Sales order line 5:</span></span>

        - <span data-ttu-id="195a2-396">**Prekės numeris:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="195a2-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="195a2-397">**Kiekis:** *50*</span><span class="sxs-lookup"><span data-stu-id="195a2-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="195a2-398">Čia pateikiami objektai ir kiekiai yra tik pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="195a2-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="195a2-399">Jie turi turėti prekių nurodytame sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="195a2-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="195a2-400">Pasirinkite prekybos užsakymo liniją 1:</span><span class="sxs-lookup"><span data-stu-id="195a2-400">Select sales order line 1.</span></span> <span data-ttu-id="195a2-401">Vėliau **Prekybos užsakymo linijos** skyriuje, **Inventoriaus** meniu, pasirinkite **Rezervacijos**.</span><span class="sxs-lookup"><span data-stu-id="195a2-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="195a2-402">**Rezervacijos** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** ir tuomet uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="195a2-402">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="195a2-403">Pakartokite 4 ir 5 žingsnius kiekvienai prekybos užsakymo eilutei.</span><span class="sxs-lookup"><span data-stu-id="195a2-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="195a2-404">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="195a2-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="195a2-405">Atistinka šis įvykis:</span><span class="sxs-lookup"><span data-stu-id="195a2-405">The following events occur:</span></span>

    - <span data-ttu-id="195a2-406">Sistema apdoroja sukurtą siuntimą naudodama šabloną apimantį žymos spausdinimo žingsnį.</span><span class="sxs-lookup"><span data-stu-id="195a2-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="195a2-407">Žymos maketas bus naudojamas nustatant žymos formatą ir galutinis rezultatas bus žymė turinti penkias eilutes ir ji yra atspausdinta spausdintuve pasirinktame žymos šablone.</span><span class="sxs-lookup"><span data-stu-id="195a2-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="195a2-408">Naujas važtaraščio identifikavimo kodas sukuriamas siuntimams.</span><span class="sxs-lookup"><span data-stu-id="195a2-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="195a2-409">Jei sukonfigūravote numerio sekos plėtinius, bangos žymos identifikavimo kodas seks **SSCC-18** numerio formatą.</span><span class="sxs-lookup"><span data-stu-id="195a2-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="195a2-410">Galite atspausdinti iš naujo šias bangos žymes eidami į **Sandėlio valdymas \> Užklausos ir atsakymai \> Bangos žymos istorija**.</span><span class="sxs-lookup"><span data-stu-id="195a2-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="195a2-411">Scenarijus 3: Bangos žymos spausdinimas kelių kainų žymėms</span><span class="sxs-lookup"><span data-stu-id="195a2-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="195a2-412">Šis scenarijus rodo, kaip naudoti bangos žymos spausdinimo funkciją, kai sandėlio procesai reikalauja kelių kainų siuntimo žymėms.</span><span class="sxs-lookup"><span data-stu-id="195a2-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="195a2-413">Pavyzdžiui, atskiros žymos gali turėti spausdinamas dėžės ir padėklus bei tarpo žymė gali būti atspausdinta visam siuntimui.</span><span class="sxs-lookup"><span data-stu-id="195a2-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="195a2-414">Tarpo žymos yra atskiro tipo žymos, kurios gali būti naudojamos kaip skirtukai tarp ritinių ir konteinerių, tokių kaip žymės siuntimo identifikavimo kodui ir brūkšniniam kodui taip, kad žymės gali būti lengvai rūšiuojamos po jų spausdinimo.</span><span class="sxs-lookup"><span data-stu-id="195a2-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="195a2-415">Pagrindinis skirtumas tarp šio scenarijaus konfigūravimo ir scenarijus 1 konfigūravimo, kartu su tuo, kad tarpo žymės yra įjungtos, yra tas, kad daugelis bangos žymių tipų turi būti susieti su bangos žymos šablonais ir padalinio sekos grupės linijomis.</span><span class="sxs-lookup"><span data-stu-id="195a2-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="195a2-416">Konfigūravimo užbaigimui, nustatykite toliau apteiktus elementus šiame scenarijui:</span><span class="sxs-lookup"><span data-stu-id="195a2-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="195a2-417">**Bangos apdorojimo metodai:** Pažymėsite bangos žymos metodą kaip „pasikartojantį“, įtrauksite jį du (ar daugiau) laikų bangos šablone ir nustatysite skirtingus bangos žingsnio kodus.</span><span class="sxs-lookup"><span data-stu-id="195a2-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="195a2-418">**Bangos žymos šablonai:** Sukonfigūruosite bangos žymos šablonus ir susiesite juos su bangos šablonu.</span><span class="sxs-lookup"><span data-stu-id="195a2-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="195a2-419">Kiekvienas bangos žymos šablonas turi savo bangos žymostipą.</span><span class="sxs-lookup"><span data-stu-id="195a2-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="195a2-420">**Bangos žymos maketai:** Sukursite keletą bangos žymos maketų.</span><span class="sxs-lookup"><span data-stu-id="195a2-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="195a2-421">Bus atskiras žymos maketas kiekvienai žymos kainai ir taip pat bus atstumo žymos maketas.</span><span class="sxs-lookup"><span data-stu-id="195a2-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="195a2-422">Šis scenarijus parodo srautą nuo pradžios iki galo.</span><span class="sxs-lookup"><span data-stu-id="195a2-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="195a2-423">Demonstracinių duomenų įgalinimas</span><span class="sxs-lookup"><span data-stu-id="195a2-423">Make demo data available</span></span>

<span data-ttu-id="195a2-424">Šio scenarijaus įgyvendinimui, privalote turėti įdiegtus demo duomenis ir pasirinkti **USMF** juridinį asmenį.</span><span class="sxs-lookup"><span data-stu-id="195a2-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="195a2-425">Nustatykite bangos proceso metodą</span><span class="sxs-lookup"><span data-stu-id="195a2-425">Set up a wave process method</span></span>

1. <span data-ttu-id="195a2-426">Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos apdorojimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="195a2-427">Patvirinkite, kad **bangos žymos spausdinimas** yra sąraše.</span><span class="sxs-lookup"><span data-stu-id="195a2-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="195a2-428">Jei jo nėra, pasirinkite **Iš naujo kurti metodu** veiksmų juostoje ir juos įtraukite.</span><span class="sxs-lookup"><span data-stu-id="195a2-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="195a2-429">**Bangos žymos spausdinimo** metodui pasirinkite **Padaryti metodą pasikartojantį** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="195a2-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="195a2-430">Bangos šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="195a2-430">Set up a wave template</span></span>

1. <span data-ttu-id="195a2-431">Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="195a2-432">Pasirinkite šabloną, tokį kaip **62 siuntimo nustatytąjį**.</span><span class="sxs-lookup"><span data-stu-id="195a2-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="195a2-433">**Metodai** „FastTab“, patraukite **bangos žymosspausdinimo** metodą į **Pasirinkti metodai** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="195a2-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="195a2-434">**Pasirinkti metodai** stulpelyje priskirkite **Bangos žingsnio kodo** vertę, tokią kaip *Dėžė* prie **Bangos žymos spausdinimo** metodo.</span><span class="sxs-lookup"><span data-stu-id="195a2-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton* , to the **Wave label printing** method.</span></span> <span data-ttu-id="195a2-435">Dėl išsamesnės informacijos apie bangos žingsnio kodus, žr. [Bangos žingsnio kodai](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="195a2-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="195a2-436">Patraukite **Bangos žymos spausdinimo** metodą į **Pasirinkti metodai** stulpelį antrą kartą.</span><span class="sxs-lookup"><span data-stu-id="195a2-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="195a2-437">**Pasirinkti metodai** stulpelyje priskirkite kitą **Bangos žingsnio kodo** vertę, tokią kaip *Padėklas* prie antrojo **Bangos žymos spausdinimo** metodo.</span><span class="sxs-lookup"><span data-stu-id="195a2-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet* , to the second **Wave label printing** method.</span></span> <span data-ttu-id="195a2-438">Dėl išsamesnės informacijos apie bangos žingsnio kodus, žr. [Bangos žingsnio kodai](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="195a2-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="195a2-439">Sukurkite tris bangos žymių maketus</span><span class="sxs-lookup"><span data-stu-id="195a2-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="195a2-440">Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymos maketai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="195a2-441">Sukurkite įrašą, kuris turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="195a2-442">**Žymos maketo identifikavimo numeris:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="195a2-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="195a2-443">**Aprašas:** *Dėžė (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="195a2-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="195a2-444">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="195a2-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="195a2-445">Veiksmų juostoje pasirinkite **bangos žymoseilutės nustatymai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="195a2-446">Pasirodo **bangos žymoseilutės nustatymai** langas.</span><span class="sxs-lookup"><span data-stu-id="195a2-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="195a2-447">Čia galite sukonfigūruoti dinaminę žymos dalį.</span><span class="sxs-lookup"><span data-stu-id="195a2-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="195a2-448">Įtraukite eilutę, kuri turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-449">**Eilutės Identifikavimo kodas:** *Bangos žymė*</span><span class="sxs-lookup"><span data-stu-id="195a2-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="195a2-450">**Eilutės lentelės pavadinimas:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="195a2-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="195a2-451">**Eilutės pradžios padėtis:** *0*</span><span class="sxs-lookup"><span data-stu-id="195a2-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="195a2-452">Šis laukelis apibrėžia vertikalią padėtį, kurioje eilutė prasideda žymėje.</span><span class="sxs-lookup"><span data-stu-id="195a2-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="195a2-453">**Eilutės aukštis:** *0*</span><span class="sxs-lookup"><span data-stu-id="195a2-453">**Row height:** *0*</span></span>

        <span data-ttu-id="195a2-454">Laukelis apibrėžia kiekvienos eilutės aukštį (taškais) pagal ZPL standartą.</span><span class="sxs-lookup"><span data-stu-id="195a2-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="195a2-455">Eilutės aukštis yra teigiamas horizontalioms žymėms ir neigiamas vertikalioms.</span><span class="sxs-lookup"><span data-stu-id="195a2-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="195a2-456">Kadangi yra tik viena eilutė šiame pavyzdyje, galite nustatyti vertę į *0* (nulį).</span><span class="sxs-lookup"><span data-stu-id="195a2-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="195a2-457">**Eilutės puslapyje:** *1*</span><span class="sxs-lookup"><span data-stu-id="195a2-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="195a2-458">Šis laukelis parodo eilučių skaičių, kuris gali būti atspausdintas kiekvienoje žymėje.</span><span class="sxs-lookup"><span data-stu-id="195a2-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="195a2-459">Šis nustatymas nulems, kad atskira ZPL žymė bus spausdinima kiekvienam įrašui bangos žymių lentelėje.</span><span class="sxs-lookup"><span data-stu-id="195a2-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="195a2-460">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="195a2-460">Close the page.</span></span>
1. <span data-ttu-id="195a2-461">Veiksmų srityje pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="195a2-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="195a2-462">Užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:</span><span class="sxs-lookup"><span data-stu-id="195a2-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-463">**Lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-464">**Išvestinė lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-465">**Laukas:** *Darbo tipas*</span><span class="sxs-lookup"><span data-stu-id="195a2-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="195a2-466">**Kriterijai:** *Paėmimas*</span><span class="sxs-lookup"><span data-stu-id="195a2-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="195a2-467">Ši užklausa užtikrina, kad tik paėmimo tipo darbo linijos bus atspausdintos žymėje, o ne padėjimo tipo darbo linijos.</span><span class="sxs-lookup"><span data-stu-id="195a2-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="195a2-468">Jei norite galėti atspausdinti važtaraščio identifikavimo kodą **Sujungimai** skirtuke, pasirinkite **Darbo linijų** lentelę ir prijunkite prie jo **Siuntimai** lentelę.</span><span class="sxs-lookup"><span data-stu-id="195a2-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="195a2-469">Uždarykite užklausos tvarkylės teksto laukelį.</span><span class="sxs-lookup"><span data-stu-id="195a2-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="195a2-470">**Spausdintuvo teksto maketas** „FastTab“ turi tris skyrius, kuriuose galite rašyti spausdintuvo kodą: **Antraštės skyrius** , **Vidurinės dalies skyrius** ir **Poraštės skyrius**.</span><span class="sxs-lookup"><span data-stu-id="195a2-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="195a2-471">**Antraštės skyrius** skyriuje, **Žymos antraštė** laukelyje įveskite ZPL kodą būtinai antraštei.</span><span class="sxs-lookup"><span data-stu-id="195a2-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="195a2-472">Pavyzdžiui, jei naudojate „Zebra“ spaudintuvus, galite naudoti šį kodą.</span><span class="sxs-lookup"><span data-stu-id="195a2-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="195a2-473">**Vidurinės dalies skyrius** skyriuje, **Žymos vidurinė dalis** laukelyje įveskite ZPL kodą būtinai vidurinei daliai.</span><span class="sxs-lookup"><span data-stu-id="195a2-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="195a2-474">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="195a2-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="195a2-475">**Vidurinės dalies skyrius** skyriuje, **Žymos apatinė dalis** laukelyje įveskite ZPL kodą būtinai apatinei daliai.</span><span class="sxs-lookup"><span data-stu-id="195a2-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="195a2-476">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="195a2-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="195a2-477">Šie nustatymai atspausdins vieną kiekvienos žymos kopiją.</span><span class="sxs-lookup"><span data-stu-id="195a2-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="195a2-478">Jei jums reikia daugiau kopijų (pavyzdžiui, vienos kopijos vienai padėklo pusei), nustatykite **n** vertę **\^PQn** skyriui poraštėje reikiamam kopijų skaičiui.</span><span class="sxs-lookup"><span data-stu-id="195a2-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="195a2-479">Pavyzdžiui, keturių kiekvienos žymos kopijų spausdinimui, nustatykite **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="195a2-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="195a2-480">Pirmoji žymė dabar paruošta naudojimui.</span><span class="sxs-lookup"><span data-stu-id="195a2-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="195a2-481">Sukurkite antrą maketo įrašą, kuris turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="195a2-482">**Žymėas maketo identifikavimo numeris:** *Padėklas*</span><span class="sxs-lookup"><span data-stu-id="195a2-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="195a2-483">**Aprašas:** *Padėklas*</span><span class="sxs-lookup"><span data-stu-id="195a2-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="195a2-484">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="195a2-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="195a2-485">Veiksmų juostoje pasirinkite **bangos žymoseilutės nustatymai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="195a2-486">Pasirodo **bangos žymoseilutės nustatymai** langas.</span><span class="sxs-lookup"><span data-stu-id="195a2-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="195a2-487">Čia galite sukonfigūruoti dinaminę žymos dalį.</span><span class="sxs-lookup"><span data-stu-id="195a2-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="195a2-488">Įtraukite eilutę, kuri turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-489">**Eilutės Identifikavimo kodas:** *Bangos žymė*</span><span class="sxs-lookup"><span data-stu-id="195a2-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="195a2-490">**Eilutės lentelės pavadinimas:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="195a2-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="195a2-491">**Eilutės pradžios padėtis:** *0*</span><span class="sxs-lookup"><span data-stu-id="195a2-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="195a2-492">Šis laukelis apibrėžia vertikalią padėtį, kurioje eilutė prasideda žymėje.</span><span class="sxs-lookup"><span data-stu-id="195a2-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="195a2-493">**Eilutės aukštis:** *0*</span><span class="sxs-lookup"><span data-stu-id="195a2-493">**Row height:** *0*</span></span>

        <span data-ttu-id="195a2-494">Laukelis apibrėžia kiekvienos eilutės aukštį (taškais) pagal ZPL standartą.</span><span class="sxs-lookup"><span data-stu-id="195a2-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="195a2-495">Eilutės aukštis yra teigiamas horizontalioms žymėms ir neigiamas vertikalioms.</span><span class="sxs-lookup"><span data-stu-id="195a2-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="195a2-496">Kadangi yra tik viena eilutė šiame pavyzdyje, galite nustatyti vertę į *0* (nulį).</span><span class="sxs-lookup"><span data-stu-id="195a2-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="195a2-497">**Eilutės puslapyje:** *1*</span><span class="sxs-lookup"><span data-stu-id="195a2-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="195a2-498">Šis laukelis parodo eilučių skaičių, kuris gali būti atspausdintas kiekvienoje žymėje.</span><span class="sxs-lookup"><span data-stu-id="195a2-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="195a2-499">Šis nustatymas nulemia, kad atskira ZPL žymė bus spausdinima kiekvienam įrašui bangos žymių lentelėje.</span><span class="sxs-lookup"><span data-stu-id="195a2-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="195a2-500">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="195a2-500">Close the page.</span></span>
1. <span data-ttu-id="195a2-501">Veiksmų srityje pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="195a2-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="195a2-502">Užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:</span><span class="sxs-lookup"><span data-stu-id="195a2-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-503">**Lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-504">**Išvestinė lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-505">**Laukas:** *Darbo tipas*</span><span class="sxs-lookup"><span data-stu-id="195a2-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="195a2-506">**Kriterijai:** *Paėmimas*</span><span class="sxs-lookup"><span data-stu-id="195a2-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="195a2-507">Ši užklausa užtikrina, kad tik paėmimo tipo darbo linijos bus atspausdintos žymėje, o ne padėjimo tipo darbo linijos.</span><span class="sxs-lookup"><span data-stu-id="195a2-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="195a2-508">Jei norite galėti atspausdinti važtaraščio identifikavimo kodą **Sujungimai** skirtuke, pasirinkite **Darbo linijų** lentelę ir prijunkite prie jo **Siuntimai** lentelę.</span><span class="sxs-lookup"><span data-stu-id="195a2-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="195a2-509">Uždarykite užklausos tvarkylės teksto laukelį.</span><span class="sxs-lookup"><span data-stu-id="195a2-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="195a2-510">**Spausdintuvo teksto maketas** „FastTab“ turi tris skyrius, kuriuose galite rašyti spausdintuvo kodą: **Antraštės skyrius** , **Vidurinės dalies skyrius** ir **Poraštės skyrius**.</span><span class="sxs-lookup"><span data-stu-id="195a2-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="195a2-511">**Antraštės skyrius** skyriuje, **Žymos antraštė** laukelyje įveskite ZPL kodą būtinai antraštei.</span><span class="sxs-lookup"><span data-stu-id="195a2-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="195a2-512">Pavyzdžiui, jei naudojate „Zebra“ spaudintuvus, galite naudoti šį kodą.</span><span class="sxs-lookup"><span data-stu-id="195a2-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="195a2-513">**Vidurinės dalies skyrius** skyriuje, **Žymos vidurinė dalis** laukelyje įveskite ZPL kodą būtinai vidurinei daliai.</span><span class="sxs-lookup"><span data-stu-id="195a2-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="195a2-514">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="195a2-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="195a2-515">**Vidurinės dalies skyrius** skyriuje, **Žymos apatinė dalis** laukelyje įveskite ZPL kodą būtinai apatinei daliai.</span><span class="sxs-lookup"><span data-stu-id="195a2-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="195a2-516">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="195a2-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="195a2-517">Šie nustatymai atspausdins vieną kiekvienos žymos kopiją.</span><span class="sxs-lookup"><span data-stu-id="195a2-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="195a2-518">Jei jums reikia daugiau kopijų (pavyzdžiui, vienos kopijos vienai padėklo pusei), nustatykite **n** vertę **\^PQn** skyriui poraštėje reikiamam kopijų skaičiui.</span><span class="sxs-lookup"><span data-stu-id="195a2-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="195a2-519">Pavyzdžiui, keturių kiekvienos žymos kopijų spausdinimui, nustatykite **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="195a2-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="195a2-520">Antroji žymė dabar paruošta naudojimui.</span><span class="sxs-lookup"><span data-stu-id="195a2-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="195a2-521">Sukurkite trečią maketo įrašą, kuris turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="195a2-522">**Žymėas maketo identifikavimo numeris:** *Tarpas*</span><span class="sxs-lookup"><span data-stu-id="195a2-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="195a2-523">**Aprašas:** *Tarpo žymė*</span><span class="sxs-lookup"><span data-stu-id="195a2-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="195a2-524">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="195a2-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="195a2-525">**Spausdintuvo teksto maketas** „FastTab“ turi tris skyrius, kuriuose galite rašyti spausdintuvo kodą: **Antraštės skyrius** , **Vidurinės dalies skyrius** ir **Poraštės skyrius**.</span><span class="sxs-lookup"><span data-stu-id="195a2-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="195a2-526">**Antraštės skyrius** skyriuje, **Žymos antraštė** laukelyje įveskite ZPL kodą būtinai antraštei.</span><span class="sxs-lookup"><span data-stu-id="195a2-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="195a2-527">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="195a2-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="195a2-528">Šįkart, nereikia jokios vidurinės dalies.</span><span class="sxs-lookup"><span data-stu-id="195a2-528">This time, no body is required.</span></span> <span data-ttu-id="195a2-529">Dėl to, tiesiog įveskite būtiną tekstą **Poraštės skyrius** skyriuje.</span><span class="sxs-lookup"><span data-stu-id="195a2-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="195a2-530">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="195a2-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="195a2-531">Trečioji žymė dabar paruošta naudojimui.</span><span class="sxs-lookup"><span data-stu-id="195a2-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="195a2-532">Ši trečioji etiketė yra žymos tarpas, kuris bus naudojamas atskirti žymių ritinius.</span><span class="sxs-lookup"><span data-stu-id="195a2-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="195a2-533">Sukurkite du bangos žymių tipus</span><span class="sxs-lookup"><span data-stu-id="195a2-533">Create two wave label types</span></span>

1. <span data-ttu-id="195a2-534">Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymostipai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="195a2-535">Sukurkite įrašą, kuris turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="195a2-536">**Žymos tipas:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="195a2-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="195a2-537">**Aprašas:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="195a2-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="195a2-538">Sukurkite antrą įrašą, kuris turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="195a2-539">**Žymos tipas:** *Padėklas*</span><span class="sxs-lookup"><span data-stu-id="195a2-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="195a2-540">**Aprašas:** *Padėklas*</span><span class="sxs-lookup"><span data-stu-id="195a2-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="195a2-541">Nustatyti vienetų sekų grupes</span><span class="sxs-lookup"><span data-stu-id="195a2-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="195a2-542">Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Padalinio sekos grupės**.</span><span class="sxs-lookup"><span data-stu-id="195a2-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="195a2-543">Pasirinkite ar sukurkite **Ea Box PL** grupę.</span><span class="sxs-lookup"><span data-stu-id="195a2-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="195a2-544">**Dėžutė** linijoje nustatykite **Bangos lygio tipas** laukelį į *Dėžė*.</span><span class="sxs-lookup"><span data-stu-id="195a2-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="195a2-545">**PL** linijoje nustatykite **Bangos lygio tipas** laukelį į *Padėklas*.</span><span class="sxs-lookup"><span data-stu-id="195a2-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="195a2-546">Sukurkite bangos žymos šablonus</span><span class="sxs-lookup"><span data-stu-id="195a2-546">Create wave label templates</span></span>

1. <span data-ttu-id="195a2-547">Eikite į **Sandėlio tvarkymas \> Sąranka \> Dokumento maršrutas \> bangos žymosšablonai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="195a2-548">Sukurkite žymos šabloną, kuris turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="195a2-549">**Žymos šablono pavadinimas:** *Dėžių žymės*</span><span class="sxs-lookup"><span data-stu-id="195a2-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="195a2-550">**Aprašas:** *Dėžės žymės*</span><span class="sxs-lookup"><span data-stu-id="195a2-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="195a2-551">**Bangos žingsnio kodas:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="195a2-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="195a2-552">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="195a2-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="195a2-553">**Bendra** „FastTab“, nustatykite **Bangos žymos tipas** laukelyje pasirinkite vertę, tokią kaip *Dėžė*.</span><span class="sxs-lookup"><span data-stu-id="195a2-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="195a2-554">**Bangos žymos šablono informacijoje** „FastTab“, įtraukite eilutę turinčią šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-555">**Žymos maketo identifikavimo numeris:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="195a2-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="195a2-556">**Spausdintuvo pavadinimas:** Pasirinkite tinkamą ZPL spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="195a2-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="195a2-557">**Vykdykite užklausą:** *Taip* (Šis pasirinkimas yra pasirenkamas, tačiau rekomenduojamas optimaliam veikimui.)</span><span class="sxs-lookup"><span data-stu-id="195a2-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="195a2-558">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="195a2-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="195a2-559">Pasirenkamas: Jei nustatote klientui konkretų žymos maketą, privalote sukurti užklausą tam, kad rastumėte kliento paskyrą.</span><span class="sxs-lookup"><span data-stu-id="195a2-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="195a2-560">**bangos žymos šablono informacijoje** „FastTab“, pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="195a2-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="195a2-561">Tuomet, užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:</span><span class="sxs-lookup"><span data-stu-id="195a2-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-562">**Lentelė:** *Siuntos*</span><span class="sxs-lookup"><span data-stu-id="195a2-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="195a2-563">**Išvestinė lentelė:** *Siuntos*</span><span class="sxs-lookup"><span data-stu-id="195a2-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="195a2-564">**Laukelis:** *Paskyros numeris*</span><span class="sxs-lookup"><span data-stu-id="195a2-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="195a2-565">**Kriterijai:** Įveskite reikiamą kliento paskyros numerį.</span><span class="sxs-lookup"><span data-stu-id="195a2-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="195a2-566">Kai baigsite, pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="195a2-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="195a2-567">Veiksmų juostoje pasirinkite **Redaguoti užklausą** tam, kad atvertumėte užklausos tvarkyklės teksto laukelį visam žymos šablonui.</span><span class="sxs-lookup"><span data-stu-id="195a2-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="195a2-568">Užklausos tvarkyklės teksto laukelyje, **Rūšiavimas** skirtuke įtraukite eilutę su šiais nustatymais:</span><span class="sxs-lookup"><span data-stu-id="195a2-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-569">**Lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-570">**Išvestinė lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-571">**Laukelis:** *Nuorodos krovimo linijos identifikavimo numeris (Record-ID)*</span><span class="sxs-lookup"><span data-stu-id="195a2-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="195a2-572">**Paieškos kryptis:** *Didėjanti*</span><span class="sxs-lookup"><span data-stu-id="195a2-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="195a2-573">Įtraukite antrą eilutę, kuri turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-574">**Lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-575">**Išvestinė lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-576">**Laukas:** *Siuntos ID*</span><span class="sxs-lookup"><span data-stu-id="195a2-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="195a2-577">**Paieškos kryptis:** *Didėjanti*</span><span class="sxs-lookup"><span data-stu-id="195a2-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="195a2-578">Pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="195a2-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="195a2-579">Pranšimo laukelis paskatins jus patvirtinti grupavimo perkrovimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="195a2-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="195a2-580">Pasirinkite **taip** tam, kad tęstumėte.</span><span class="sxs-lookup"><span data-stu-id="195a2-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="195a2-581">Veiksmų juostoje pasirinkite **bangos žymos šablono grupė**.</span><span class="sxs-lookup"><span data-stu-id="195a2-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="195a2-582">**Bangos žymos šablono grupės** teksto laukelyje, pasirinkite eilutę, kurioje **Nuorodos laukelio pavadinimas** laukelis nustatytas į *Siuntimo identifikavimo kodas* , nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="195a2-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID* , set the following values:</span></span>

    - <span data-ttu-id="195a2-583">**Spausdinimo tarpo žymė:** Pasirinkite šį žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="195a2-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="195a2-584">**Žymos maketo identifikavimo kodas:** Pasirinkite tarpo žymę.</span><span class="sxs-lookup"><span data-stu-id="195a2-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="195a2-585">(Pavyzdžiui, pasirinkite *Tarpo* žymos maketą, kurį sukūrėte anksčiau šiame scnarijuje.)</span><span class="sxs-lookup"><span data-stu-id="195a2-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="195a2-586">**Spausdintuvo pavadinimas:** Pasirinkite spausdintuvą tarpo žymei.</span><span class="sxs-lookup"><span data-stu-id="195a2-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="195a2-587">(Dažniausiai, dėl žymių ritinių skaidymo tikslų, turite pasirinkti tą patį spausdintuvą, kuris pasirinktas **Bangos žymos šablono informacijos** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="195a2-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="195a2-588">Nepaisant to, kiti scenarijai yra galimi.)</span><span class="sxs-lookup"><span data-stu-id="195a2-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="195a2-589">Eilutėje, kurioje **Nuorodos žymos pavadinimas** laukelis nustatytas *Nuorodos krovimo linijos identifikavimo kodas* , pasirinkite **Žymos kūrėjo identifikavimo kodas** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="195a2-589">For the row where the **Reference field name** field is set to *Reference load line id* , select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="195a2-590">Šie nustatyimai sukurs vieną žymos seką („Dėžė 1 X“) vienai krovimo linijai bangoje nepriklausomai nuo darbo grupės nustatymų.</span><span class="sxs-lookup"><span data-stu-id="195a2-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="195a2-591">Ši žymos seka gali būti atspausdinta viename žymos makete.</span><span class="sxs-lookup"><span data-stu-id="195a2-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="195a2-592">Taip pat, žymos skirtingiems siuntimams bus atskirtos pasirinkta tarpo žyme.</span><span class="sxs-lookup"><span data-stu-id="195a2-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="195a2-593">Pasirinkite **OK** tam, kad uždarytumėte **Bangos žymos šablono grupės** teksto laukelį.</span><span class="sxs-lookup"><span data-stu-id="195a2-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="195a2-594">Sukurkite antrą žymos šabloną, kuris turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="195a2-595">**Žymos šablono pavadinimas:** *Padėklo žymės*</span><span class="sxs-lookup"><span data-stu-id="195a2-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="195a2-596">**Aprašas:** *Padėklo žymos*</span><span class="sxs-lookup"><span data-stu-id="195a2-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="195a2-597">**Bangos žingsnio kodas:** *Padėklas*</span><span class="sxs-lookup"><span data-stu-id="195a2-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="195a2-598">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="195a2-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="195a2-599">**Bendra** „FastTab“, nustatykite **Bangos žymos tipas** laukelyje pasirinkite vertę, tokią kaip *Padėklas*.</span><span class="sxs-lookup"><span data-stu-id="195a2-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="195a2-600">**Bangos žymos šablono informacijoje** „FastTab“, įtraukite eilutę turinčią šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-601">**Žymėas maketo identifikavimo numeris:** *Padėklas*</span><span class="sxs-lookup"><span data-stu-id="195a2-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="195a2-602">**Spausdintuvo pavadinimas:** Pasirinkite tinkamą ZPL spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="195a2-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="195a2-603">**Vykdykite užklausą:** *Taip* (Šis pasirinkimas yra pasirenkamas, tačiau rekomenduojamas optimaliam veikimui.)</span><span class="sxs-lookup"><span data-stu-id="195a2-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="195a2-604">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="195a2-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="195a2-605">Pasirenkamas: Jei nustatote klientui konkretų žymos maketą, privalote sukurti užklausą tam, kad rastumėte kliento paskyrą.</span><span class="sxs-lookup"><span data-stu-id="195a2-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="195a2-606">**bangos žymos šablono informacijoje** „FastTab“, pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="195a2-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="195a2-607">Tuomet, užklausos tvarkyklės teksto laukelyje, **Intervalas** skirtuke įtraukite eilutę su šiais nustatymais:</span><span class="sxs-lookup"><span data-stu-id="195a2-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-608">**Lentelė:** *Siuntos*</span><span class="sxs-lookup"><span data-stu-id="195a2-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="195a2-609">**Išvestinė lentelė:** *Siuntos*</span><span class="sxs-lookup"><span data-stu-id="195a2-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="195a2-610">**Laukelis:** *Paskyros numeris*</span><span class="sxs-lookup"><span data-stu-id="195a2-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="195a2-611">**Kriterijai:** Įveskite reikiamą kliento paskyros numerį.</span><span class="sxs-lookup"><span data-stu-id="195a2-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="195a2-612">Kai baigsite, pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="195a2-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="195a2-613">Veiksmų juostoje pasirinkite **Redaguoti užklausą** tam, kad atvertumėte užklausos tvarkyklės teksto laukelį visam žymos šablonui.</span><span class="sxs-lookup"><span data-stu-id="195a2-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="195a2-614">Užklausos tvarkyklės teksto laukelyje, **Rūšiavimas** skirtuke įtraukite eilutę su šiais nustatymais:</span><span class="sxs-lookup"><span data-stu-id="195a2-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-615">**Lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-616">**Išvestinė lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-617">**Laukelis:** *Nuorodos krovimo linijos identifikavimo numeris (Record-ID)*</span><span class="sxs-lookup"><span data-stu-id="195a2-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="195a2-618">**Paieškos kryptis:** *Didėjanti*</span><span class="sxs-lookup"><span data-stu-id="195a2-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="195a2-619">Įtraukite antrą eilutę, kuri turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="195a2-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="195a2-620">**Lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-621">**Išvestinė lentelė:** *Darbo eilutės*</span><span class="sxs-lookup"><span data-stu-id="195a2-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="195a2-622">**Laukas:** *Siuntos ID*</span><span class="sxs-lookup"><span data-stu-id="195a2-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="195a2-623">**Paieškos kryptis:** *Didėjanti*</span><span class="sxs-lookup"><span data-stu-id="195a2-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="195a2-624">Pasirinkite **OK** užklausos tvarkyklės teksto langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="195a2-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="195a2-625">Pranšimo laukelis paskatins jus patvirtinti grupavimo perkrovimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="195a2-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="195a2-626">Pasirinkite **taip** tam, kad tęstumėte.</span><span class="sxs-lookup"><span data-stu-id="195a2-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="195a2-627">Veiksmų juostoje pasirinkite **bangos žymos šablono grupė**.</span><span class="sxs-lookup"><span data-stu-id="195a2-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="195a2-628">**Bangos žymos šablono grupės** teksto laukelyje, pasirinkite eilutę, kurioje **Nuorodos laukelio pavadinimas** laukelis nustatytas į *Siuntimo identifikavimo kodas* , nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="195a2-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID* , set the following values:</span></span>

    - <span data-ttu-id="195a2-629">**Spausdinimo tarpo žymė:** Pasirinkite šį žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="195a2-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="195a2-630">**Žymos maketo identifikavimo kodas:** Pasirinkite tarpo žymę.</span><span class="sxs-lookup"><span data-stu-id="195a2-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="195a2-631">(Pavyzdžiui, pasirinkite *Tarpo* žymos maketą, kurį sukūrėte anksčiau šiame scnarijuje.)</span><span class="sxs-lookup"><span data-stu-id="195a2-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="195a2-632">**Spausdintuvo pavadinimas:** Pasirinkite spausdintuvą tarpo žymei.</span><span class="sxs-lookup"><span data-stu-id="195a2-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="195a2-633">(Dažniausiai, dėl žymių ritinių skaidymo tikslų, turite pasirinkti tą patį spausdintuvą, kuris pasirinktas **Bangos žymos šablono informacijos** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="195a2-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="195a2-634">Nepaisant to, kiti scenarijai yra galimi.)</span><span class="sxs-lookup"><span data-stu-id="195a2-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="195a2-635">Eilutėje, kurioje **Nuorodos žymos pavadinimas** laukelis nustatytas *Nuorodos krovimo linijos identifikavimo kodas* , pasirinkite **Žymos kūrėjo identifikavimo kodas** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="195a2-635">For the row where the **Reference field name** field is set to *Reference load line id* , select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="195a2-636">Šie nustatyimai sukurs vieną žymos seką („Dėžė 1 X“) vienai krovimo linijai bangoje nepriklausomai nuo darbo grupės nustatymų.</span><span class="sxs-lookup"><span data-stu-id="195a2-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="195a2-637">Ši žymos seka gali būti atspausdinta viename žymos makete.</span><span class="sxs-lookup"><span data-stu-id="195a2-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="195a2-638">Taip pat, žymos skirtingiems siuntimams bus atskirtos pasirinkta tarpo žyme.</span><span class="sxs-lookup"><span data-stu-id="195a2-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="195a2-639">Konfigūruokite numerio sekos plėtinius</span><span class="sxs-lookup"><span data-stu-id="195a2-639">Configure number sequence extensions</span></span>

<span data-ttu-id="195a2-640">Numerio sekos plėtiniai valdo GS1 atitiktį su specifinėmis numerio sekomis.</span><span class="sxs-lookup"><span data-stu-id="195a2-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="195a2-641">Konfigūravimas yra pasirenkamas esamam scenarijui.</span><span class="sxs-lookup"><span data-stu-id="195a2-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="195a2-642">Dėl platesnės informacijos ir konfigūravimo instrukcijų, žr. [Konfigūruoti numerio sekos plėtinius](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="195a2-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="195a2-643">Sukuria prekybos užsakymą ir išleidžia jį į sandėlį</span><span class="sxs-lookup"><span data-stu-id="195a2-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="195a2-644">Eikite į **Prekyba ir komercija \> Prekybos užsakymas \> Visi prekybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="195a2-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="195a2-645">Sukurkite pardavimo užsakymą, kuriam nustatyti tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="195a2-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="195a2-646">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="195a2-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="195a2-647">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="195a2-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="195a2-648">Įtraukite dvi prekybos užsakymo eilutes:</span><span class="sxs-lookup"><span data-stu-id="195a2-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="195a2-649">Prekybos užsakymo linija 1:</span><span class="sxs-lookup"><span data-stu-id="195a2-649">Sales order line 1:</span></span>

        - <span data-ttu-id="195a2-650">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="195a2-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="195a2-651">**Kiekis:** *9024*</span><span class="sxs-lookup"><span data-stu-id="195a2-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="195a2-652">**Padalinys:** *ea* (9024 ea = 376 dėžė = 47 padėklai)</span><span class="sxs-lookup"><span data-stu-id="195a2-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="195a2-653">Prekybos užsakymo linija 2:</span><span class="sxs-lookup"><span data-stu-id="195a2-653">Sales order line 2:</span></span>

        - <span data-ttu-id="195a2-654">**Prekės numeris:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="195a2-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="195a2-655">**Kiekis:** *9016*</span><span class="sxs-lookup"><span data-stu-id="195a2-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="195a2-656">**Padalinys:** *ea* (9016 ea = 322 Box = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="195a2-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="195a2-657">Čia pateikiami objektai ir kiekiai yra tik pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="195a2-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="195a2-658">Jie privalo naudoti objekto sekos grupę, kurią nustatėte anksčiau, atitinkantys objekto pakeitimai iš *ea* į *Box* į *PL* turi būti jiems nustatyti ir jie privalo turėti prekių sandėlyje  *62*.</span><span class="sxs-lookup"><span data-stu-id="195a2-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="195a2-659">Dėl platesnės informacijos, žr. [Matavimo vienetas ir sandėliavimo politika](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="195a2-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="195a2-660">Pasirinkite prekybos užsakymo liniją 1:</span><span class="sxs-lookup"><span data-stu-id="195a2-660">Select sales order line 1.</span></span> <span data-ttu-id="195a2-661">Vėliau **Prekybos užsakymo linijos** skyriuje, **Inventoriaus** meniu, pasirinkite **Rezervacijos**.</span><span class="sxs-lookup"><span data-stu-id="195a2-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="195a2-662">**Rezervacijos** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** ir tuomet uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="195a2-662">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="195a2-663">Pakartokite 4 ir 5 žingsnius kiekvienai prekybos užsakymo eilutei 2.</span><span class="sxs-lookup"><span data-stu-id="195a2-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="195a2-664">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="195a2-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="195a2-665">Atistinka šis įvykis:</span><span class="sxs-lookup"><span data-stu-id="195a2-665">The following events occur:</span></span> 

    - <span data-ttu-id="195a2-666">Sistema apdoroja sukurtą siuntimą naudodama šabloną apimantį žymos spausdinimo žingsnį.</span><span class="sxs-lookup"><span data-stu-id="195a2-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="195a2-667">Žymos maketas bus naudojamas nustatant žymos formatą ir galutinis rezultatas bus žymė turinti penkias eilutes ir ji yra atspausdinta spausdintuve pasirinktame žymos šablone.</span><span class="sxs-lookup"><span data-stu-id="195a2-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="195a2-668">Bangos žymės yra sukuriamos ir atspausdinamos.</span><span class="sxs-lookup"><span data-stu-id="195a2-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="195a2-669">Žymių skaičius bus lygus dėžių skaičiui (pavyzdžiui, šiuo atveju 376 dėžės žymai eilutėje 1, 322 dėžės žymei linijoje 2, 47 padėklai žymos linijoje 1, 47 padėklai žymos linijoje 2 ir dvi tarpų žymos turinčios siuntimo identifikavimo kodą).</span><span class="sxs-lookup"><span data-stu-id="195a2-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="195a2-670">Naujas važtaraščio identifikavimo kodas sukuriamas siuntimams.</span><span class="sxs-lookup"><span data-stu-id="195a2-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="195a2-671">Jei sukonfigūravote numerio sekos plėtinius, bangos žymos identifikavimo kodas seks **SSCC-18** numerio formatą.</span><span class="sxs-lookup"><span data-stu-id="195a2-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="195a2-672">Galite peržiūrėti ir iš naujo atspausdinti bangos etiketes tolesniuose puslapiuose:</span><span class="sxs-lookup"><span data-stu-id="195a2-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="195a2-673">Visi siuntimai \> Siuntimo informacija</span><span class="sxs-lookup"><span data-stu-id="195a2-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="195a2-674">Visi krovimai \> Krovimo informacija</span><span class="sxs-lookup"><span data-stu-id="195a2-674">All loads \> Load details</span></span>
- <span data-ttu-id="195a2-675">Visos bangos</span><span class="sxs-lookup"><span data-stu-id="195a2-675">All waves</span></span>
- <span data-ttu-id="195a2-676">Bangos žymės</span><span class="sxs-lookup"><span data-stu-id="195a2-676">Wave labels</span></span>
- <span data-ttu-id="195a2-677">Bangos žymos retrospektyva</span><span class="sxs-lookup"><span data-stu-id="195a2-677">Wave label history</span></span>

<span data-ttu-id="195a2-678">Didžiojoje dalyje šių puslapių, galite rasti atitinkamą funkciją pasirinkę **Bangos žymės**  **Susijusi informacija** grupėje **Siuntimai** skirtuke veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="195a2-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>