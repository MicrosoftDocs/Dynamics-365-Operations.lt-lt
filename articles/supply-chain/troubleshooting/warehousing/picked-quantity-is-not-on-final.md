---
title: Negalima patvirtinti siuntos, nes prekės nebuvo paimtos
description: Negalima patvirtinti siuntos, nes prekės nebuvo paimtos
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301310"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="ab40d-103">Negalima patvirtinti siuntos, nes prekės nebuvo paimtos</span><span class="sxs-lookup"><span data-stu-id="ab40d-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="ab40d-104">Klaidos kodas: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="ab40d-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="ab40d-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="ab40d-105">Symptoms</span></span>

<span data-ttu-id="ab40d-106">Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="ab40d-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="ab40d-107">Kai kurios prekės, kurias reikia pakrauti %1, dar nepaimtos ir neperkeltos į galutinę siuntimo vietą.</span><span class="sxs-lookup"><span data-stu-id="ab40d-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="ab40d-108">Todėl negalite patvirtinti krovinio siuntimo.</span><span class="sxs-lookup"><span data-stu-id="ab40d-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="ab40d-109">Priežastis</span><span class="sxs-lookup"><span data-stu-id="ab40d-109">Cause</span></span>

<span data-ttu-id="ab40d-110">Dabartinės krovinio arba siuntos būsenos patvirtinti negalima, nes gali būti viena iš šių sąlygų:</span><span class="sxs-lookup"><span data-stu-id="ab40d-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="ab40d-111">Susijęs darbas dar neparinktas ir perkeltas į galutinę siuntimo vietą.</span><span class="sxs-lookup"><span data-stu-id="ab40d-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="ab40d-112">Paimtas darbo kiekis neatitinka sukurto darbo kiekio krovinio eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ab40d-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="ab40d-113">Vietos nurodymas buvo sukonfigūruotas su pakavimo vieta kaip galutine siuntimo vieta naudojant Bangos šablono krovimą į konteinerius.</span><span class="sxs-lookup"><span data-stu-id="ab40d-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="ab40d-114">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="ab40d-114">Resolution</span></span>

<span data-ttu-id="ab40d-115">Krovinio ar siuntimo būsena šiuo metu yra, kai siuntos patvirtinimas nesėkmingas.</span><span class="sxs-lookup"><span data-stu-id="ab40d-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="ab40d-116">Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:</span><span class="sxs-lookup"><span data-stu-id="ab40d-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="ab40d-117">Peržiūrėkite savo krovinio eilutes bei įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka.</span><span class="sxs-lookup"><span data-stu-id="ab40d-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="ab40d-118">Atšaukite darbo ID, kurios buvo sukurtos su pakavimo vieta kaip galutine siuntimo vieta, perkonfigūruokite vietos nurodymą ir iš naujo išleiskite krovinį.</span><span class="sxs-lookup"><span data-stu-id="ab40d-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="ab40d-119">Peržiūrėkite savo krovinio eilutes bei įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka</span><span class="sxs-lookup"><span data-stu-id="ab40d-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="ab40d-120">Naudokite toliau pateiktą procedūrą savo krovinio eilučių peržiūrai ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka.</span><span class="sxs-lookup"><span data-stu-id="ab40d-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="ab40d-121">Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="ab40d-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="ab40d-122">Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="ab40d-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="ab40d-123">„FastTab” **Krovinio eilutės** patikrinkite pakrovimo eilutę.</span><span class="sxs-lookup"><span data-stu-id="ab40d-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="ab40d-124">Pasižymėkite lauko Darbo **sukurtas kiekis** vertę.</span><span class="sxs-lookup"><span data-stu-id="ab40d-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="ab40d-125">Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.</span><span class="sxs-lookup"><span data-stu-id="ab40d-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="ab40d-126">Patikrinkite, ar darbas užbaigtas galutinėje siuntimo vietoje ir ar paimtas darbo kiekis atitinka krovinio eilutėje sukurtą darbo kiekį.</span><span class="sxs-lookup"><span data-stu-id="ab40d-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="ab40d-127">Pakartokite šią procedūrą visose krovinio eilutėse, norėdami įsitikinti, kad visi kriterijai yra įvykdyti.</span><span class="sxs-lookup"><span data-stu-id="ab40d-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="ab40d-128">Atšaukite darbo ID, kurios buvo sukurtos su pakavimo vieta kaip galutine siuntimo vieta, perkonfigūruokite vietos nurodymą ir iš naujo išleiskite krovinį</span><span class="sxs-lookup"><span data-stu-id="ab40d-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="ab40d-129">Naudokite toliau pateiktą procedūrą, kad atšauktumėte darbo ID, kurių pakavimo vieta yra ir galutinė išdavimo vietą, kai naudojamas automatinis krovimas į konteinerius.</span><span class="sxs-lookup"><span data-stu-id="ab40d-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="ab40d-130">Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="ab40d-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="ab40d-131">Atidaromas **Atšaukti darbą** dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="ab40d-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="ab40d-132">Lauke **Darbo ID** nurodykite darbo, kurį norite atšaukti, ID.</span><span class="sxs-lookup"><span data-stu-id="ab40d-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="ab40d-133">Pasirinkto darbo ID privalo turėti vieną iš šių **Darbo būsenos** reikšmių: *Atidaryta*, *Progresuojanti*, *Atšaukta*, *Sujungta* ar *Uždaryta*.</span><span class="sxs-lookup"><span data-stu-id="ab40d-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="ab40d-134">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ab40d-134">Select **OK**.</span></span>
1. <span data-ttu-id="ab40d-135">Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.</span><span class="sxs-lookup"><span data-stu-id="ab40d-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="ab40d-136">Pakartokite šią procedūrą kitoms darbo ID, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="ab40d-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="ab40d-137">Dėl platesnės informacijos, žr. [Darbo sandėlyje atšaukimas dėl išimčių tvarkymo](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="ab40d-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="ab40d-138">Naudokite tolesnę procedūrą, kad iš naujo sukonfigūruotumėte vietos nurodymą, jog jis nebenaudotų pakavimo vietos kaip galutinės siuntimo vietos, kai nustatytas bangos šablono automatinis krovimas į konteinerius.</span><span class="sxs-lookup"><span data-stu-id="ab40d-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="ab40d-139">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="ab40d-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="ab40d-140">Lauke **Darbo užsakymo tipas** pasirinkite *Pardavimo užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="ab40d-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="ab40d-141">Pasirinkite vietos nurodymą, kurį naudojate automatiniam krovimui į konteinerius.</span><span class="sxs-lookup"><span data-stu-id="ab40d-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="ab40d-142">„FastTab“ įrankių juostoje **Vietos nurodymo veiksmai** pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="ab40d-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="ab40d-143">Užklausų rengyklės dialogo lango skirtuke **Diapazonas** suraskite eilutę, kurios **Laukas** nustatytas į *Vietos profilį* ir patikrinkite, ar tos eilutės laukas **Kriterijai** nėra nustatytas į vietos profilį, kurio **Vietos tipas** yra *Pakavimas*.</span><span class="sxs-lookup"><span data-stu-id="ab40d-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="ab40d-144">Pakoreguokite lauką **Kriterijai**, kad pataisytumėte galutinę padėjimo vietą.</span><span class="sxs-lookup"><span data-stu-id="ab40d-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="ab40d-145">Naudokite toliau pateiktą procedūrą, kad iš naujo išleistumėte krovinį ir sukurtumėte darbo ID su teisinga galutine siuntimo vieta.</span><span class="sxs-lookup"><span data-stu-id="ab40d-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="ab40d-146">Eikite į **Sandėlio valdymas \> Kroviniai \> Krovinio planavimo darbo sritis**.</span><span class="sxs-lookup"><span data-stu-id="ab40d-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="ab40d-147">Skyriuje **Kroviniai** raskite krovinį, kurį reikia išleisti.</span><span class="sxs-lookup"><span data-stu-id="ab40d-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="ab40d-148">Skyriaus **Kroviniai** įrankių juostoje pasirinkite **Išleidimas \> Išleidimas į sandėlį**, kad išleistumėte pasirinktą krovinį į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="ab40d-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="ab40d-149">Pakartokite šią procedūrą kitiems kroviniams, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="ab40d-149">Repeat this procedure for the other loads as needed.</span></span>
