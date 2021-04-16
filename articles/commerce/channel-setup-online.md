---
title: Interneto kanalo nustatymas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują interneto kanalą.
author: samjarawan
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b6bf158361f95b6551b29f195616cf21f908b802
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800644"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="ce0a6-103">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ce0a6-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ce0a6-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują interneto kanalą.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ce0a6-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="ce0a6-105">Overview</span></span>

<span data-ttu-id="ce0a6-106">„Dynamics 365 Commerce“ palaiko kelis mažmeninės prekybos kanalus.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="ce0a6-107">Šie mažmeninės prekybos kanalai apima interneto parduotuves, skambučių centrus ir mažmeninės prekybos parduotuves (taip pat vadinamas fizinėmis parduotuvėmis).</span><span class="sxs-lookup"><span data-stu-id="ce0a6-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="ce0a6-108">Internetinė parduotuvė suteikia klientams galimybę pirkti produktus internete, todėl klientai gali juos pirkti ne tik iš fizinės parduotuvės, bet ir iš internetinės parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="ce0a6-109">Norėdami sukurti internetinę parduotuvę „Commerce“, pirmiausia turite sukurti interneto kanalą.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-109">To create an online store in Commerce, you must first create an online channel.</span></span> <span data-ttu-id="ce0a6-110">Prieš kurdami naują interneto kanalą, įsitikinkite, kad įvykdėte [Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="ce0a6-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

<span data-ttu-id="ce0a6-111">Kad galėtumėte kurti naują svetainę, programoje „Commerce“ reikia sukurti bent vieną internetinę parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-111">Before you can create a new site, at least one online store must be created in Commerce.</span></span> <span data-ttu-id="ce0a6-112">Norėdami sužinoti daugiau, žr. [El. prekybos svetainės kūrimas](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="ce0a6-112">For more information, see [Create an e-Commerce site](create-ecommerce-site.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="ce0a6-113">Naujo interneto kanalo kūrimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ce0a6-113">Create and configure a new online channel</span></span>

<span data-ttu-id="ce0a6-114">Norėdami sukurti ir sukonfigūruoti naują interneto kanalą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-114">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="ce0a6-115">Naršymo srityje eikite **Moduliai \>Kanalai \>Internetinės parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-115">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="ce0a6-116">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-116">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ce0a6-117">Lauke **Pavadinimas** įveskite naujo kanalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-117">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="ce0a6-118">Išplečiamajame sąraše **Juridinis subjektas** įveskite atitinkamą juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-118">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="ce0a6-119">Išplečiamajame sąraše **Sandėlis** įveskite atitinkamą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-119">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="ce0a6-120">Lauke **Parduotuvės laiko juosta** pasirinkite atitinkamą laiko juostą.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-120">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="ce0a6-121">Lauke **Valiuta** pasirinkite atitinkamą valiutą.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="ce0a6-122">Lauke **Numatytasis klientas** pateikite galiojantį numatytąjį klientą.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="ce0a6-123">Lauke **Kliento adresų knygelė** nurodykite galiojančią adresų knygelę.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-123">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="ce0a6-124">Lauke **Funkcijų šablonas** pasirinkite funkcijų šabloną, jei taikoma.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="ce0a6-125">Lauke **El. paštu siunčiamo pranešimo šablonas** pateikite galiojantį el. siunčiamo pranešimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="ce0a6-126">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ce0a6-127">Toliau pateiktame vaizde parodytas naujo interneto kanalo kūrimas.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-127">The following image shows the creation of a new online channel.</span></span>

![Naujas interneto kanalas](media/channel-setup-online-1.png)

<span data-ttu-id="ce0a6-129">Toliau pateiktame vaizde parodytas interneto kanalo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-129">The following image shows an example online channel.</span></span>

![Interneto kanalo pavyzdys](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="ce0a6-131">Kalbų nustatymas</span><span class="sxs-lookup"><span data-stu-id="ce0a6-131">Set up languages</span></span>

<span data-ttu-id="ce0a6-132">Jei jūsų el. prekybos svetainė palaiko kelias kalbas, išplėskite skyrių **Kalbos** ir, jei reikia, įtraukite papildomų kalbų.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-132">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="ce0a6-133">Mokėjimo sąskaitos nustatymas</span><span class="sxs-lookup"><span data-stu-id="ce0a6-133">Set up payment account</span></span>

<span data-ttu-id="ce0a6-134">Iš skyriaus **Mokėjimo sąskaita** galite įtraukti trečiosios šalies mokėjimų teikėją.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-134">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="ce0a6-135">Informaciją, kaip nustatyti „Adyen“ mokėjimo jungtį, žr. [„Dynamics 365“ mokėjimo jungtis, skirta „Adyen“](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="ce0a6-135">For information on setting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-setup"></a><span data-ttu-id="ce0a6-136">Papildoma kanalų sąranka</span><span class="sxs-lookup"><span data-stu-id="ce0a6-136">Additional channel setup</span></span>

<span data-ttu-id="ce0a6-137">Papildomos užduotys, reikalingos interneto kanalo sąrankai, apima mokėjimo metodų, pristatymo būdų ir išpildymo grupių priskyrimo nustatymą.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-137">Additional tasks that are required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="ce0a6-138">Toliau pateiktame paveiksle rodomos sąrankos parinktys **Pristatymo būdai**, **Mokėjimo metodai** ir **Vykdymo grupių priskyrimas**, esančios skirtuke **Nustatyti**.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-138">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Papildomi interneto kanalo nustatymo veiksmai](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="ce0a6-140">Nustatyti mokėjimo būdus</span><span class="sxs-lookup"><span data-stu-id="ce0a6-140">Set up payment methods</span></span>

<span data-ttu-id="ce0a6-141">Norėdami nustatyti kiekvieno mokėjimo tipo, palaikomo šiame kanale, mokėjimo metodus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="ce0a6-142">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Mokėjimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="ce0a6-143">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ce0a6-144">Naršymo srityje pasirinkite pageidaujamą mokėjimo metodą.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="ce0a6-145">Skyriuje **Bendri** nurodykite **Operacijos pavadinimas** ir konfigūruokite kitus pageidaujamus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="ce0a6-146">Konfigūruokite visus papildomus parametrus, kurių reikia mokėjimo tipui.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="ce0a6-147">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ce0a6-148">Toliau pateiktame vaizde parodytas mokėjimas grynaisiais pinigais pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-148">The following image shows an example of a cash payment method.</span></span>

![Mokėjimo metodų pavyzdys](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="ce0a6-150">Nustatyti pristatymo būdus</span><span class="sxs-lookup"><span data-stu-id="ce0a6-150">Set up modes of delivery</span></span>

<span data-ttu-id="ce0a6-151">Galite peržiūrėti sukonfigūruotus pristatymo būdus pasirikdami **Pristatymo būdai** skirtuke **Nustatymas**, esančiame **Veiksmų sritis**.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-151">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="ce0a6-152">Norėdami pakeisti arba įtraukti pristatymo būdą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-152">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="ce0a6-153">Naršymo srityje eikite į **Moduliai \> Atsargų valdymas \> Pristatymo būdai**.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-153">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="ce0a6-154">Veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte naują pristatymo režimą, arba pasirinkite esamą režimą.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-154">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="ce0a6-155">Skyriuje **Mažmeninės prekybos kanalai** pasirinkite **Įtraukti eilutę**, kad galėtumėte įtraukti kanalą.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-155">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="ce0a6-156">Kanalų įtraukimas naudojant organizacijos mazgus, užuot įtraukus kiekvieną kanalą atskirai, gali racionalizuoti kanalų įtraukimą.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-156">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="ce0a6-157">Toliau pateiktame vaizde parodytas pristatymo būdo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-157">The following image shows an example of a mode of delivery.</span></span>

![Nustatyti pristatymo būdus](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="ce0a6-159">Vykdymo grupės priskyrimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ce0a6-159">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="ce0a6-160">Norėdami nustatyti vykdymo grupės priskyrimą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-160">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="ce0a6-161">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Vykdymo grupės priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-161">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="ce0a6-162">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-162">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ce0a6-163">Išplečiamajame sąraše **Vykdymo grupė** pasirinkite vykdymo grupę.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-163">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="ce0a6-164">Išplečiamajame sąraše **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-164">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="ce0a6-165">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-165">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ce0a6-166">Toliau pateiktame vaizde parodytas vykdymo grupės priskyrimo sąrankos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ce0a6-166">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Vykdymo grupės priskyrimo nustatymas](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="ce0a6-168">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ce0a6-168">Additional resources</span></span>

[<span data-ttu-id="ce0a6-169">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ce0a6-169">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ce0a6-170">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="ce0a6-170">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="ce0a6-171">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ce0a6-171">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="ce0a6-172">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ce0a6-172">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="ce0a6-173">„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“</span><span class="sxs-lookup"><span data-stu-id="ce0a6-173">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]