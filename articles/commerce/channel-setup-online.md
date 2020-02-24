---
title: Interneto kanalo nustatymas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują interneto kanalą.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9b7a2b8fd157df8b39e9e227d188a3802cacb4e3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002432"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="05176-103">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="05176-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="05176-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują interneto kanalą.</span><span class="sxs-lookup"><span data-stu-id="05176-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="05176-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="05176-105">Overview</span></span>

<span data-ttu-id="05176-106">„Dynamics 365 Commerce“ palaiko kelis mažmeninės prekybos kanalus.</span><span class="sxs-lookup"><span data-stu-id="05176-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="05176-107">Šie mažmeninės prekybos kanalai apima interneto parduotuves, skambučių centrus ir mažmeninės prekybos parduotuves (taip pat vadinamas fizinėmis parduotuvėmis).</span><span class="sxs-lookup"><span data-stu-id="05176-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="05176-108">Internetinė parduotuvė suteikia klientams galimybę pirkti produktus internete, todėl klientai gali juos pirkti ne tik iš fizinės parduotuvės, bet ir iš internetinės parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="05176-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="05176-109">Norėdami sukurti internetinę parduotuvę „Commerce“, pirmiausia turite sukurti interneto kanalą.</span><span class="sxs-lookup"><span data-stu-id="05176-109">To create an online store in Commerce, you must first create an online channel.</span></span> 

<span data-ttu-id="05176-110">Prieš kurdami naują interneto kanalą, įsitikinkite, kad įvykdėte [Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="05176-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="05176-111">Naujo interneto kanalo kūrimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="05176-111">Create and configure a new online channel</span></span>

<span data-ttu-id="05176-112">Norėdami sukurti ir sukonfigūruoti naują interneto kanalą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="05176-112">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="05176-113">Naršymo srityje eikite **Moduliai \>Kanalai \>Internetinės parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="05176-113">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="05176-114">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="05176-114">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="05176-115">Lauke **Pavadinimas** įveskite naujo kanalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="05176-115">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="05176-116">Išplečiamajame sąraše **Juridinis subjektas** įveskite atitinkamą juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="05176-116">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="05176-117">Išplečiamajame sąraše **Sandėlis** įveskite atitinkamą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="05176-117">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="05176-118">Lauke **Parduotuvės laiko juosta** pasirinkite atitinkamą laiko juostą.</span><span class="sxs-lookup"><span data-stu-id="05176-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="05176-119">Lauke **Valiuta** pasirinkite atitinkamą valiutą.</span><span class="sxs-lookup"><span data-stu-id="05176-119">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="05176-120">Lauke **Numatytasis klientas** pateikite galiojantį numatytąjį klientą.</span><span class="sxs-lookup"><span data-stu-id="05176-120">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="05176-121">Lauke **Kliento adresų knygelė** nurodykite galiojančią adresų knygelę.</span><span class="sxs-lookup"><span data-stu-id="05176-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="05176-122">Lauke **Funkcijų šablonas** pasirinkite funkcijų šabloną, jei taikoma.</span><span class="sxs-lookup"><span data-stu-id="05176-122">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="05176-123">Lauke **El. paštu siunčiamo pranešimo šablonas** pateikite galiojantį el. siunčiamo pranešimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="05176-123">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="05176-124">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="05176-124">On the action pane, select **Save**.</span></span>

<span data-ttu-id="05176-125">Toliau pateiktame vaizde parodytas naujo interneto kanalo kūrimas.</span><span class="sxs-lookup"><span data-stu-id="05176-125">The following image shows the creation of a new online channel.</span></span>

![Naujas interneto kanalas](media/channel-setup-online-1.png)

<span data-ttu-id="05176-127">Toliau pateiktame vaizde parodytas interneto kanalo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="05176-127">The following image shows an example online channel.</span></span>

![Interneto kanalo pavyzdys](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="05176-129">Kalbų nustatymas</span><span class="sxs-lookup"><span data-stu-id="05176-129">Set up languages</span></span>

<span data-ttu-id="05176-130">Jei jūsų el. prekybos svetainė palaiko kelias kalbas, išplėskite skyrių **Kalbos** ir, jei reikia, įtraukite papildomų kalbų.</span><span class="sxs-lookup"><span data-stu-id="05176-130">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="05176-131">Mokėjimo sąskaitos nustatymas</span><span class="sxs-lookup"><span data-stu-id="05176-131">Set up payment account</span></span>

<span data-ttu-id="05176-132">Iš skyriaus **Mokėjimo sąskaita** galite įtraukti trečiosios šalies mokėjimų teikėją.</span><span class="sxs-lookup"><span data-stu-id="05176-132">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="05176-133">Informaciją, kaip nustatyti „Adyen“ mokėjimo jungtį, žr. [„Dynamics 365“ mokėjimo jungtis, skirta „Adyen“](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="05176-133">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="05176-134">Papildoma kanalų sąranka</span><span class="sxs-lookup"><span data-stu-id="05176-134">Additional channel set up</span></span>

<span data-ttu-id="05176-135">Papildomos užduotys, reikalingos interneto kanalo sąrankai, apima mokėjimo metodų, pristatymo būdų ir išpildymo grupių priskyrimo nustatymą.</span><span class="sxs-lookup"><span data-stu-id="05176-135">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="05176-136">Toliau pateiktame paveiksle rodomos sąrankos parinktys **Pristatymo būdai**, **Mokėjimo metodai** ir **Vykdymo grupių priskyrimas**, esančios skirtuke **Nustatyti**.</span><span class="sxs-lookup"><span data-stu-id="05176-136">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Papildomi interneto kanalo nustatymo veiksmai](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="05176-138">Nustatyti mokėjimo būdus</span><span class="sxs-lookup"><span data-stu-id="05176-138">Set up payment methods</span></span>

<span data-ttu-id="05176-139">Norėdami nustatyti kiekvieno mokėjimo tipo, palaikomo šiame kanale, mokėjimo metodus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="05176-139">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="05176-140">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Mokėjimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="05176-140">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="05176-141">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="05176-141">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="05176-142">Naršymo srityje pasirinkite pageidaujamą mokėjimo metodą.</span><span class="sxs-lookup"><span data-stu-id="05176-142">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="05176-143">Skyriuje **Bendri** nurodykite **Operacijos pavadinimas** ir konfigūruokite kitus pageidaujamus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="05176-143">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="05176-144">Konfigūruokite visus papildomus parametrus, kurių reikia mokėjimo tipui.</span><span class="sxs-lookup"><span data-stu-id="05176-144">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="05176-145">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="05176-145">On the action pane, select **Save**.</span></span>

<span data-ttu-id="05176-146">Toliau pateiktame vaizde parodytas mokėjimas grynaisiais pinigais pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="05176-146">The following image shows an example of a cash payment method.</span></span>

![Mokėjimo metodų pavyzdys](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="05176-148">Nustatyti pristatymo būdus</span><span class="sxs-lookup"><span data-stu-id="05176-148">Set up modes of delivery</span></span>

<span data-ttu-id="05176-149">Galite peržiūrėti sukonfigūruotus pristatymo būdus pasirikdami **Pristatymo būdai** skirtuke **Nustatymas**, esančiame **Veiksmų sritis**.</span><span class="sxs-lookup"><span data-stu-id="05176-149">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="05176-150">Norėdami pakeisti arba įtraukti pristatymo būdą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="05176-150">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="05176-151">Naršymo srityje eikite į **Moduliai \> Atsargų valdymas \> Pristatymo būdai**.</span><span class="sxs-lookup"><span data-stu-id="05176-151">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="05176-152">Veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte naują pristatymo režimą, arba pasirinkite esamą režimą.</span><span class="sxs-lookup"><span data-stu-id="05176-152">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="05176-153">Skyriuje **Mažmeninės prekybos kanalai** pasirinkite **Įtraukti eilutę**, kad galėtumėte įtraukti kanalą.</span><span class="sxs-lookup"><span data-stu-id="05176-153">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="05176-154">Kanalų įtraukimas naudojant organizacijos mazgus, užuot įtraukus kiekvieną kanalą atskirai, gali racionalizuoti kanalų įtraukimą.</span><span class="sxs-lookup"><span data-stu-id="05176-154">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="05176-155">Toliau pateiktame vaizde parodytas pristatymo būdo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="05176-155">The following image shows an example of a mode of delivery.</span></span>

![Nustatyti pristatymo būdus](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="05176-157">Vykdymo grupės priskyrimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="05176-157">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="05176-158">Norėdami nustatyti vykdymo grupės priskyrimą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="05176-158">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="05176-159">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Vykdymo grupės priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="05176-159">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="05176-160">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="05176-160">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="05176-161">Išplečiamajame sąraše **Vykdymo grupė** pasirinkite vykdymo grupę.</span><span class="sxs-lookup"><span data-stu-id="05176-161">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="05176-162">Išplečiamajame sąraše **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="05176-162">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="05176-163">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="05176-163">On the action pane, select **Save**.</span></span>

<span data-ttu-id="05176-164">Toliau pateiktame vaizde parodytas vykdymo grupės priskyrimo sąrankos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="05176-164">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Vykdymo grupės priskyrimo nustatymas](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="05176-166">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="05176-166">Additional resources</span></span>

[<span data-ttu-id="05176-167">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="05176-167">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="05176-168">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="05176-168">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="05176-169">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="05176-169">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="05176-170">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="05176-170">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="05176-171">„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“</span><span class="sxs-lookup"><span data-stu-id="05176-171">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
