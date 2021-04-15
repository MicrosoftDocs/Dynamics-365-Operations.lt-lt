---
title: Modulio Iškrovimo kaina ataskaitos
description: Šioje temoje aprašoma, kaip rasti ir naudoti modulio Iškrovimo kaina įvairių tipų ataskaitas.
author: sherry-zheng
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 565303a4f51d1726c62a85faaf8c4d8692c110fc
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500651"
---
# <a name="landed-cost-reports"></a><span data-ttu-id="9d1cf-103">Modulio Iškrovimo kaina ataskaitos</span><span class="sxs-lookup"><span data-stu-id="9d1cf-103">Landed cost reports</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="outstanding-invoices"></a><span data-ttu-id="9d1cf-104">Neapmokėtos sąskaitos faktūros</span><span class="sxs-lookup"><span data-stu-id="9d1cf-104">Outstanding invoices</span></span>

<span data-ttu-id="9d1cf-105">Neapmokėtų SF ataskaitoje yra įvairių išlaidų lygių, susijusių su kiekvienu reisu, visų neapmokėtų SF sąrašas.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-105">The outstanding invoices report contains a list of all outstanding invoices of the various cost levels that are associated with every voyage.</span></span> <span data-ttu-id="9d1cf-106">Jis naudojamas reisui ir reiso išlaidoms reguliariai suderinti su didžiosios knygos operacijų sąrašu.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-106">It's used to reconcile the voyage and voyage costs together with the ledger transactions list on a regular basis.</span></span> <span data-ttu-id="9d1cf-107">Išrašius pridėtinių išlaidų SF, ji pašalinama iš ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-107">After an overhead cost has been invoiced, it's removed from the report.</span></span>

<span data-ttu-id="9d1cf-108">Norėdami sugeneruoti neapmokėtų SF ataskaitą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-108">To generate an outstanding invoices report, follow these steps.</span></span>

1. <span data-ttu-id="9d1cf-109">Eikite į **Iškrovimo kaina \> Ataskaitos \> Sekimas \> Neapmokėtos SF**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-109">Go to **Landed cost \> Reports \> Tracking \> Outstanding invoices**.</span></span>
1. <span data-ttu-id="9d1cf-110">Dialogo lango **Neapmokėtos SF** lauke **Kaip data** nurodykite datą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-110">In the **Outstanding invoices** dialog box, in the **As at date** field, specify a date.</span></span> <span data-ttu-id="9d1cf-111">Bet kuri SF, kuri buvo neapmokėta tą datą arba anksčiau, bus įtraukta į išvestį.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-111">Any invoice that was outstanding on or before that date will be included in the output.</span></span>
1. <span data-ttu-id="9d1cf-112">Dalyje **Rodyti** pasirinkite vieną iš pateiktų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-112">Under **Show**, select one of the following options:</span></span>

    - <span data-ttu-id="9d1cf-113">**Išlaidos, kurių SF neišrašyta** – įtraukite siuntų, kurioms išrašytos SF ir kurių savikaina įvertinta, o faktinės išlaidos – ne, išlaidas.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-113">**Cost not invoiced** – Include costs for invoiced shipments that have an estimated cost value but no actual cost.</span></span>
    - <span data-ttu-id="9d1cf-114">**Atsargos, kurių SF neišrašyta** – įtraukite išlaidas, kurių SF išrašytos, bet pirkimo užsakymas dar negautas.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-114">**Stock not invoiced** – Include costs that have been invoiced, but that the purchase order hasn't yet been received for.</span></span>
    - <span data-ttu-id="9d1cf-115">**Viskas, kam SF neišrašyta** – įtraukite ir parinkties **Išlaidos, kurių SF neišrašyta**, ir parinkties **Atsargos, kurių SF neišrašyta** rezultatus.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-115">**All not invoiced** – Include the results of both the **Cost not invoiced** option and the **Stock not invoiced** option.</span></span>

1. <span data-ttu-id="9d1cf-116">Nustatykite parinktį **Įtraukti naujas išlaidas** į *Taip*, norėdami įtraukti išlaidas, kurių faktinių išlaidų dar nėra ir kurių atsargos nėra gautos.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-116">Set the **Include new costs** option to *Yes* to include costs that don't yet have an actual cost, and that inventory hasn't been received for.</span></span> <span data-ttu-id="9d1cf-117">Jei nustatysite į *Ne*, ataskaitoje bus įtrauktos tik tos išlaidos, kurių SF išrašytos.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-117">If you set it to *No*, the report will include only costs that have been invoiced.</span></span>
1. <span data-ttu-id="9d1cf-118">Skyriuje **Peržiūra** įgalinkite kiekvieną informacijos tipą, kurį norite įtraukti į ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-118">In the **View** section, enable each type of detail that you want to include on the report.</span></span>
1. <span data-ttu-id="9d1cf-119">Kaip ir dirbdami su kitų tipų ataskaitomis programoje „Microsoft Dynamics 365 Supply Chain Management”, naudokite „FastTab” **Paskirties vieta**, norėdami pasirinkti ataskaitos išvesties formatą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-119">As you do for other types of reports in Microsoft Dynamics 365 Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="9d1cf-120">Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, norėdami toliau riboti įrašus, kurie bus įtraukti į ataskaitą, naudokite „FastTab” **Įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-120">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="9d1cf-121">Pasirinkite **Gerai**, kad sugeneruotumėte šią ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-121">Select **OK** to generate the report.</span></span>

## <a name="activityprovider-analysis-reports"></a><span data-ttu-id="9d1cf-122">Veiklos / teikėjų analizės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="9d1cf-122">Activity/provider analysis reports</span></span>

<span data-ttu-id="9d1cf-123">Veiklos / teikėjų analizės ataskaitos leidžia peržiūrėti kiekvieno teikėjo laiko įvertinimo tikslumą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-123">The activity/provider analysis reports let you review the accuracy of your time estimates for each provider.</span></span>

<span data-ttu-id="9d1cf-124">Norėdami sugeneruoti veiklos / teikėjų analizės ataskaitą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-124">To generate an activity/provider analysis report, follow these steps.</span></span>

1. <span data-ttu-id="9d1cf-125">Atsižvelgdami į norimos kurti ataskaitos tipą, atlikite vieną iš toliau pateiktų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-125">Depending on the type of report that you want to create, follow one of these steps:</span></span>

    - <span data-ttu-id="9d1cf-126">Eikite į **Iškrovimo kaina \> Ataskaitos \> Veiklos / teikėjų analizė pagal veiklą**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-126">Go to **Landed cost \> Reports \> Analysis of activity/provider by activity**.</span></span> <span data-ttu-id="9d1cf-127">Šiuo atveju laiko įvertinimai bus grupuojami pagal veiklą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-127">In this case, the time estimates will be grouped by activity.</span></span>
    - <span data-ttu-id="9d1cf-128">Eikite į **Iškrovimo kaina \> Ataskaitos \> Veiklos / teikėjų analizė pagal teikėją**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-128">Go to **Landed cost \> Reports \> Analysis of activity/provider by provider**.</span></span> <span data-ttu-id="9d1cf-129">Šiuo atveju laiko įvertinimai bus grupuojami pagal teikėją.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-129">In this case, the time estimates will be grouped by provider.</span></span>

    <span data-ttu-id="9d1cf-130">Rodomas dialogo langas **Veiklos / teikėjų analizė pagal veiklą** arba dialogo langas **Veiklos / teikėjų analizė pagal teikėją**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-130">Either the **Analysis of activity/provider by activity** dialog box or the **Analysis of activity/provider by provider** dialog box appears.</span></span> <span data-ttu-id="9d1cf-131">Abiejuose dialogo languose pateikiamos tos pačios parinktys.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-131">Both dialog boxes provide the same options.</span></span>

1. <span data-ttu-id="9d1cf-132">Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, naudokite „FastTab” **Paskirties vieta**, norėdami pasirinkti ataskaitos išvesties formatą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-132">As you do for other types of reports in Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="9d1cf-133">Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, norėdami toliau riboti įrašus, kurie bus įtraukti į ataskaitą, naudokite „FastTab” **Įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-133">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="9d1cf-134">Pasirinkite **Gerai**, kad sugeneruotumėte šią ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-134">Select **OK** to generate the report.</span></span>

## <a name="voyage-costing-reports"></a><span data-ttu-id="9d1cf-135">Reiso įkainojimo ataskaitos</span><span class="sxs-lookup"><span data-stu-id="9d1cf-135">Voyage costing reports</span></span>

<span data-ttu-id="9d1cf-136">Reiso įkainojimo ataskaitos nurodo prekių išlaidas ir importavimo išlaidas pagal sąskaitos lapą, gabenimo konteinerį ar reisą, atsižvelgiant į parinktis, kurias pažymėjote generuodami ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-136">The voyage costing reports show the cost of the items and the import costs per folio, shipping container, or voyage, depending on the options that you select when you generate the report.</span></span> <span data-ttu-id="9d1cf-137">Kiekviena reiso įkainojimo ataskaita leidžia palyginti reiso įvertintą savikainą su faktinėmis išlaidomis ir ataskaitą galima išskaidyti pagal keletą identifikavimo veiksnių.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-137">Each voyage costing report lets you view the estimated cost of a voyage versus the actual cost, and it can be broken down by the several identifying factors.</span></span>

<span data-ttu-id="9d1cf-138">Norėdami sugeneruoti reiso įkainojimo ataskaitą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-138">To generate a voyage costing report, follow these steps.</span></span>

1. <span data-ttu-id="9d1cf-139">Atsižvelgdami į norimos kurti ataskaitos tipą, atlikite vieną iš toliau pateiktų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-139">Depending on the type of report that you want to create, follow one of these steps:</span></span>

    - <span data-ttu-id="9d1cf-140">Eikite į **Iškrovimo kaina \> Ataskaitos \> Įkainojimas \> Reiso įkainojimas pagal atskiras išlaidas**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-140">Go to **Landed cost \> Reports \> Costing \> Voyage costing by individual cost**.</span></span> <span data-ttu-id="9d1cf-141">Šiuo atveju atskirų išlaidų parinktis nurodys kiekvieno išlaidų tipo kodo ir išlaidų srities importo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-141">In this case, the individual cost option will show import costs per cost area per cost type code.</span></span>
    - <span data-ttu-id="9d1cf-142">Eikite į **Iškrovimo kaina \> Ataskaitos \> Įkainojimas \> Reiso įkainojimas pagal ataskaitos kategoriją**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-142">Go to **Landed cost \> Reports \> Costing \> Voyage costing by reporting category**.</span></span> <span data-ttu-id="9d1cf-143">Šiuo atveju importo išlaidos bus išskaidytos į įvairias ataskaitų kategorijas.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-143">In this case, the import cost will be broken down into the various reporting categories.</span></span> <span data-ttu-id="9d1cf-144">Išlaidų tipai grupuojami pagal ataskaitų kategorijas.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-144">Cost types are grouped by reporting categories.</span></span>

    <span data-ttu-id="9d1cf-145">Atsiranda dialogo langas **Reiso įkainojimas pagal atskiras išlaidas** arba dialogo langas **Reiso įkainojimas pagal ataskaitos kategoriją**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-145">Either the **Voyage costing by individual cost** dialog box or the **Voyage costing by reporting category** dialog box appears.</span></span> <span data-ttu-id="9d1cf-146">Šie dialogo langai panašūs.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-146">These dialog boxes are similar.</span></span> <span data-ttu-id="9d1cf-147">Bet kokie skirtumai pažymimi likusioje šios procedūros dalyje.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-147">Any differences are noted in the rest of this procedure.</span></span>

1. <span data-ttu-id="9d1cf-148">Jei atidarėte dialogo langą **Reiso įkainojimas pagal ataskaitos kategoriją**, lauke **Išlaidos** pasirinkite vieną iš toliau pateiktų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-148">If you opened the **Voyage costing by reporting category** dialog box, in the **Cost** field, select one of the following values:</span></span>

    - <span data-ttu-id="9d1cf-149">**Išlaidų vertė** – vertė skaičiuojama naudojant automatines išlaidas arba rankiniu būdu sukuriama išlaidų srityje.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-149">**Cost value** – The value is either calculated by using auto costs or manually created in the cost area.</span></span>
    - <span data-ttu-id="9d1cf-150">**Įvertinta** – kai prekės gautos, nustatoma įvertinta savikaina.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-150">**Estimated** – After the goods have been received, the estimated cost is set.</span></span>
    - <span data-ttu-id="9d1cf-151">**Faktinės išlaidos** – kai užsakymo SF išrašyta, faktinės išlaidos nustatomos pagal SF nurodytas išlaidas.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-151">**Actual** – After the order has been invoiced, the actual cost is set to the cost on the invoice.</span></span>
    - <span data-ttu-id="9d1cf-152">**Tinkamiausia** – sistema naudos tinkamiausią iš aukščiau pateiktų trijų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-152">**Best** – The system will use whichever of the previous three options is most accurate.</span></span> <span data-ttu-id="9d1cf-153">(Rekomenduojame pažymėti šią parinktį.)</span><span class="sxs-lookup"><span data-stu-id="9d1cf-153">(We recommend that you select this option.)</span></span>

1. <span data-ttu-id="9d1cf-154">Norėdami parodyti kiekvienos prekės išlaidas, nustatykite parinktį **Kiekvienos prekės** į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-154">Set the **Per item** option to *Yes* to show the cost of each item.</span></span> <span data-ttu-id="9d1cf-155">Nustatykite į *Ne*, kad išlaidos būtų rodomos pagal reisą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-155">Set it to *No* to show costs per voyage.</span></span>
1. <span data-ttu-id="9d1cf-156">Skyriuje **Peržiūra** pasirinkite kategorijas, pagal kurias norite išskaidyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-156">In the **View** section, select the categories to break down the cost by.</span></span>
1. <span data-ttu-id="9d1cf-157">Skyriuje **Dimensijos** pasirinkite dimensijas, kurios bus įtrauktos į ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-157">In the **Dimensions** section, select the dimensions to include on the report.</span></span>
1. <span data-ttu-id="9d1cf-158">Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, naudokite „FastTab” **Paskirties vieta**, norėdami pasirinkti ataskaitos išvesties formatą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-158">As you do for other types of reports in Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="9d1cf-159">Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, norėdami toliau riboti įrašus, kurie bus įtraukti į ataskaitą, naudokite „FastTab” **Įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-159">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="9d1cf-160">Pasirinkite **Gerai**, kad sugeneruotumėte šią ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-160">Select **OK** to generate the report.</span></span>

## <a name="shipping-container-receipts-list"></a><span data-ttu-id="9d1cf-161">Gabenimo konteinerio gavimo kvitų sąrašas</span><span class="sxs-lookup"><span data-stu-id="9d1cf-161">Shipping container receipts list</span></span>

<span data-ttu-id="9d1cf-162">Gabenimo konteinerio gavimo kvitų sąraše pateikiami visi negauti kiekiai, kurių terminas yra numatytą datą arba anksčiau.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-162">The shipping container receipts list contains all unreceived quantities that are due on or before an expected date.</span></span> <span data-ttu-id="9d1cf-163">Sandėlio darbuotojai šią ataskaitą gali naudoti norėdami identifikuoti numatomas prekes gabenimo konteineryje.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-163">Warehouse staff can use this report to identify the expected goods on a shipping container.</span></span> <span data-ttu-id="9d1cf-164">Ją taip pat galima naudoti prekėms, gautoms gabenimo konteineryje, tikrinti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-164">It can also be used to manually validate goods as they are received on a shipping container.</span></span>

<span data-ttu-id="9d1cf-165">Norėdami sugeneruoti gabenimo konteinerio gavimo kvitų sąrašą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-165">To generate a shipping container receipts list, follow these steps.</span></span>

1. <span data-ttu-id="9d1cf-166">Eikite į **Iškrovimo kaina \> Ataskaitos \> Sekimas \> Gabenimo konteinerio gavimo kvitų sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-166">Go to **Landed cost \> Reports \> Tracking \> Shipping container receipts list**.</span></span>
1. <span data-ttu-id="9d1cf-167">Dialogo lango **Gabenimo konteinerio gavimo kvitų sąrašas** lauke **Numatyta data** nurodykite datą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-167">In the **Shipping container receipts list** dialog box, in the **Expected date** field, specify a date.</span></span> <span data-ttu-id="9d1cf-168">Visi kiekiai, kurie nebuvo gauti tą datą arba anksčiau, bus įtraukti į išvestį.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-168">Any quantities that were unreceived on or before that date will be included in the output.</span></span>
1. <span data-ttu-id="9d1cf-169">Skyriuje **Dimensijos** pasirinkite dimensijas, kurios bus įtrauktos į ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-169">In the **Dimensions** section, select the dimensions to include on the report.</span></span>
1. <span data-ttu-id="9d1cf-170">Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, naudokite „FastTab” **Paskirties vieta**, norėdami pasirinkti ataskaitos išvesties formatą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-170">As you do for other types of reports in Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="9d1cf-171">Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, norėdami toliau riboti įrašus, kurie bus įtraukti į ataskaitą, naudokite „FastTab” **Įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-171">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="9d1cf-172">Pasirinkite **Gerai**, kad sugeneruotumėte šią ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-172">Select **OK** to generate the report.</span></span>

## <a name="expected-delivery-report"></a><span data-ttu-id="9d1cf-173">Numatomo pristatymo ataskaita</span><span class="sxs-lookup"><span data-stu-id="9d1cf-173">Expected delivery report</span></span>

<span data-ttu-id="9d1cf-174">Numatomo pristatymo ataskaitoje yra pagrindinė informacija apie reisą, gabenimo konteinerį, sąskaitos lapą, prekes ir numatomą pristatymo datą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-174">The expected delivery report contains basic information about the voyage, shipping container, folio, items, and expected date of delivery.</span></span>

<span data-ttu-id="9d1cf-175">Norėdami sugeneruoti numatomo pristatymo ataskaitą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-175">To generate an expected delivery report, follow these steps.</span></span>

1. <span data-ttu-id="9d1cf-176">Eikite į **Iškrovimo kaina \> Ataskaitos \> Sekimas \> Numatomas pristatymas**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-176">Go to **Landed cost \> Reports \> Tracking \> Expected Delivery**.</span></span>
1. <span data-ttu-id="9d1cf-177">Dialogo lango **Numatytas pristatymas** lauke **Numatyta data** pasirinkite datą, kada tikimasi prekių pristatymo į galutinį paskirties sandėlį.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-177">In the **Expected delivery** dialog box, in the **Expected date** field, select the date when delivery of the goods to the final destination warehouse is expected.</span></span> <span data-ttu-id="9d1cf-178">Į išvestį bus įtraukta bet kuri reiso eilutė, kurios numatoma data yra tą datą arba anksčiau, tačiau ji dar nėra gauta.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-178">Any voyage line that has an expected date on or before that date, and that hasn't yet been received, will be included in the output.</span></span>
1. <span data-ttu-id="9d1cf-179">Pasirinktinai: lauke **Tiekėjo sąskaita** pasirinkite tiekėjo sąskaitą, norėdami įtraukti tik konkretaus tiekėjo pristatymus.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-179">Optional: In the **Vendor account** field, select a vendor account to include only deliveries from a specific vendor.</span></span>
1. <span data-ttu-id="9d1cf-180">Skyriuje **Dimensijos** pasirinkite dimensijas, kurios bus įtrauktos į ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-180">In the **Dimensions** section, select the dimensions to include on the report.</span></span>
1. <span data-ttu-id="9d1cf-181">Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, naudokite „FastTab” **Paskirties vieta**, norėdami pasirinkti ataskaitos išvesties formatą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-181">As you do for other types of reports in Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="9d1cf-182">Kaip ir dirbdami su kitų tipų ataskaitomis „Supply Chain Management”, norėdami toliau riboti įrašus, kurie bus įtraukti į ataskaitą, naudokite „FastTab” **Įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-182">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="9d1cf-183">Pasirinkite **Gerai**, kad sugeneruotumėte šią ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="9d1cf-183">Select **OK** to generate the report.</span></span>