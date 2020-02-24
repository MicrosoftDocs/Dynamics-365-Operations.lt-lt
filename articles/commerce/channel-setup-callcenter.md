---
title: Skambučių centro kanalo nustatymas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują skambučių centro kanalą.
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
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002455"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="1ecaa-103">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="1ecaa-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1ecaa-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują skambučių centro kanalą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1ecaa-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="1ecaa-105">Overview</span></span>

<span data-ttu-id="1ecaa-106">Programoje „Dynamics 365 Commerce“ skambučių centras yra mažmeninės prekybos kanalo tipas, kurį galima nustatyti programoje.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-106">In Dynamics 365 Commerce, a call center is a type of retail channel that can be defined in the application.</span></span> <span data-ttu-id="1ecaa-107">Nustačius skambučių centro objektų kanalą, sistema leidžia susieti tam tikrus duomenis ir užsakymų apdorojimą pagal numatytuosius pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="1ecaa-108">Programoje „Commerce“ įmonė gali nurodyti keletą skambučių centro kanalų.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="1ecaa-109">Prieš kurdami naują skambučių centro kanalą, įsitikinkite, kad įvykdėte [Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="1ecaa-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="1ecaa-110">Naujo skambučių centro kanalo kūrimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1ecaa-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="1ecaa-111">Norėdami sukurti ir sukonfigūruoti naują skambučių centro kanalą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="1ecaa-112">Naršymo srityje eikite į **Moduliai \> Kanalai \> Skambučių centras \> Visi skambučių centrai**.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="1ecaa-113">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="1ecaa-114">Lauke **Pavadinimas** įveskite naujo kanalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="1ecaa-115">Pasirinkite atitinkamą **Juridinis asmuo** iš išplečiamojo meniu.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="1ecaa-116">Pasirinkite atitinkamą **Sandėlis** vieta iš išplečiamojo meniu.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="1ecaa-117">Lauke **Numatytasis klientas** pateikite galiojantį numatytąjį klientą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="1ecaa-118">Lauke **El. paštu siunčiamo pranešimo šablonas** pateikite galiojantį el. siunčiamo pranešimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="1ecaa-119">Pateikite **Kainos perrašymas** informacinį kodą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="1ecaa-120">Atkreipkite dėmesį, kad pirmiausia gali reikti sukurti informacinį kodą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="1ecaa-121">Nurodykite **Sulaikymo kodas** informacinį kodą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="1ecaa-122">Atkreipkite dėmesį, kad pirmiausia gali reikti sukurti informacinį kodą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="1ecaa-123">Nurodykite **Kreditas** informacinį kodą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="1ecaa-124">Atkreipkite dėmesį, kad pirmiausia gali reikti sukurti informacinį kodą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="1ecaa-125">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-125">Select **Save**.</span></span>

<span data-ttu-id="1ecaa-126">Toliau pateiktame vaizde parodytas naujo skambučių centro kanalo kūrimas.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-126">The following image shows the creation of a new call center channel.</span></span>

![Naujas skambučių centro kanalas](media/channel-setup-callcenter-1.png)

<span data-ttu-id="1ecaa-128">Toliau pateiktame vaizde parodytas skambučių centro kanalo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-128">The following image shows an example call center channel.</span></span>

![Skambučių centro kanalo pavyzdys](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="1ecaa-130">Papildoma kanalų sąranka</span><span class="sxs-lookup"><span data-stu-id="1ecaa-130">Additional channel setup</span></span>

<span data-ttu-id="1ecaa-131">Papildomos užduotys, reikalingos skambučių centro kanalo sąrankai, apima mokėjimo metodų ir pristatymo būdų nustatymą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="1ecaa-132">Toliau pateiktame paveiksle rodomi **Pristatymo būdai** ir **Mokėjimo metodai** nustatymo parinktys, esančios skirtuke **Nustatyti**.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![Papildomi skambučių centro kanalo nustatymo veiksmai](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="1ecaa-134">Nustatyti mokėjimo būdus</span><span class="sxs-lookup"><span data-stu-id="1ecaa-134">Set up payment methods</span></span>

<span data-ttu-id="1ecaa-135">Norėdami nustatyti kiekvieno mokėjimo tipo, palaikomo šiame kanale, mokėjimo metodus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="1ecaa-136">Veiksmų srityje pasirinkite skirtuką **Sąranka**, tada pasirinkite **Mokėjimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="1ecaa-137">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="1ecaa-138">Naršymo srityje pasirinkite pageidaujamą mokėjimo metodą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="1ecaa-139">Skyriuje **Bendri** nurodykite **Operacijos pavadinimas** ir konfigūruokite kitus pageidaujamus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="1ecaa-140">Konfigūruokite visus papildomus parametrus, kurių reikia mokėjimo tipui.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="1ecaa-141">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="1ecaa-142">Toliau pateiktame vaizde parodytas mokėjimas grynaisiais pinigais pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-142">The following image shows an example of a cash payment method.</span></span>

![Mokėjimo metodų pavyzdys](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="1ecaa-144">Nustatyti pristatymo būdus</span><span class="sxs-lookup"><span data-stu-id="1ecaa-144">Set up modes of delivery</span></span>

<span data-ttu-id="1ecaa-145">Galite peržiūrėti sukonfigūruotus pristatymo būdus pasirikdami **Pristatymo būdai** skirtuke **Nustatymas**, esančiame **Veiksmų sritis**.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="1ecaa-146">Norėdami pakeisti arba įtraukti pristatymo būdą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="1ecaa-147">Naršymo srityje eikite į **Moduliai \> Atsargų valdymas \> Pristatymo būdai**.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="1ecaa-148">Veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte naują pristatymo režimą, arba pasirinkite esamą režimą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="1ecaa-149">Skyriuje **Mažmeninės prekybos kanalai** pasirinkite **Įtraukti eilutę**, kad galėtumėte įtraukti kanalą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="1ecaa-150">Kanalų įtraukimas naudojant organizacijos mazgus, užuot įtraukus kiekvieną kanalą atskirai, gali racionalizuoti kanalų įtraukimą.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="1ecaa-151">Toliau pateiktame vaizde parodytas pristatymo būdo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="1ecaa-151">The following image shows an example of a mode of delivery.</span></span>

![Nustatyti pristatymo būdus](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="1ecaa-153">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1ecaa-153">Additional resources</span></span>

[<span data-ttu-id="1ecaa-154">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="1ecaa-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="1ecaa-155">Skambučių centro pardavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="1ecaa-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="1ecaa-156">Skambučių centro užsakymo apdorojimo parinkčių nustatymas</span><span class="sxs-lookup"><span data-stu-id="1ecaa-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="1ecaa-157">Skambučių centro katalogai</span><span class="sxs-lookup"><span data-stu-id="1ecaa-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="1ecaa-158">Įspėjimų dėl apgaulės nustatymas ir jų naudojimas</span><span class="sxs-lookup"><span data-stu-id="1ecaa-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="1ecaa-159">Skambučių centrų tęstinumo programų nustatymas</span><span class="sxs-lookup"><span data-stu-id="1ecaa-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
