---
title: Skambučių centro kanalo nustatymas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują skambučių centro kanalą.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
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
ms.openlocfilehash: 3f8c47c00b920dae01213d1d241ac8ee6a18d4e3
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107189"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="92c31-103">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="92c31-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="92c31-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują skambučių centro kanalą.</span><span class="sxs-lookup"><span data-stu-id="92c31-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="92c31-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="92c31-105">Overview</span></span>


<span data-ttu-id="92c31-106">Programoje „Dynamics 365 Commerce“ skambučių centras yra tam tikras „Commerce“ kanalas, kurį galima nustatyti programoje.</span><span class="sxs-lookup"><span data-stu-id="92c31-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="92c31-107">Nustačius skambučių centro objektų kanalą, sistema leidžia susieti tam tikrus duomenis ir užsakymų apdorojimą pagal numatytuosius pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="92c31-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="92c31-108">Nors įmonė gali nustatyti kelis skambučių centro kanalus programoje „Commerce“, svarbu pažymėti, kad atskiras vartotojas gali būti susietas tik su vienu skambučių centro kanalu.</span><span class="sxs-lookup"><span data-stu-id="92c31-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="92c31-109">Prieš kurdami naują skambučių centro kanalą, įsitikinkite, kad įvykdėte [būtinąsias kanalo nustatymo sąlygas](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="92c31-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="92c31-110">Naujo skambučių centro kanalo kūrimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="92c31-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="92c31-111">Norėdami sukurti ir sukonfigūruoti naują skambučių centro kanalą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="92c31-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="92c31-112">Naršymo srityje eikite į **Mažmeninė prekyba ir prekyba \> Kanalai \> Skambučių centrai \> Visi skambučių centrai**.</span><span class="sxs-lookup"><span data-stu-id="92c31-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="92c31-113">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="92c31-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="92c31-114">Lauke **Pavadinimas** įveskite naujo kanalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="92c31-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="92c31-115">Pasirinkite atitinkamą **juridinį subjektą** iš išplečiamojo meniu.</span><span class="sxs-lookup"><span data-stu-id="92c31-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="92c31-116">Pasirinkite atitinkamą **sandėlio** vietą iš išplečiamojo meniu.</span><span class="sxs-lookup"><span data-stu-id="92c31-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="92c31-117">Ši vieta bus naudojama kaip numatytoji pardavimo užsakymuose, sukurtuose šiam skambučių centro kanalui, tik tuo atveju, jei kliento arba prekės lygyje nebuvo nustatyta kitų numatytųjų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="92c31-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="92c31-118">Lauke **Numatytasis klientas** pateikite galiojantį numatytąjį klientą.</span><span class="sxs-lookup"><span data-stu-id="92c31-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="92c31-119">Šie duomenys naudojami, kai kuriami nauji kliento įrašai, kad būtų automatiškai užpildoma numatytosiomis reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="92c31-119">This data is used to assist in autopopulating defaults when new customer records are created.</span></span> <span data-ttu-id="92c31-120">Kuriant skambučių centro užsakymus, nėra patartina sukurti užsakymų numatytajam klientui.</span><span class="sxs-lookup"><span data-stu-id="92c31-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="92c31-121">Lauke **El. paštu siunčiamo pranešimo šablonas** pateikite galiojantį el. siunčiamo pranešimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="92c31-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="92c31-122">Kadangi skambučių centro užsakymai kuriami ir apdorojami, el. paštu siunčiamo pranešimo šablonas naudojamas suaktyvinti automatinių el. pašto įspėjimų siuntimą klientams su informacija apie jų užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="92c31-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="92c31-123">Pateikite **Kainos perrašymas** informacinį kodą.</span><span class="sxs-lookup"><span data-stu-id="92c31-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="92c31-124">Pirmiausia gali prireikti sukurti informacinį kodą.</span><span class="sxs-lookup"><span data-stu-id="92c31-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="92c31-125">Šis informacinis kodas pateikia priežasčių kodų rinkinį, kurį vartotojas bus raginamas pasirinkti, kai skambučių centro užsakyme naudojama kainos perrašymo funkcija.</span><span class="sxs-lookup"><span data-stu-id="92c31-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="92c31-126">Nurodykite **Sulaikymo kodas** informacinį kodą.</span><span class="sxs-lookup"><span data-stu-id="92c31-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="92c31-127">Pirmiausia gali prireikti sukurti informacinį kodą.</span><span class="sxs-lookup"><span data-stu-id="92c31-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="92c31-128">Šis informacinis kodas pateikia pasirinktinų priežasčių kodų rinkinį, iš kurio vartotojas bus raginamas pasirinkti, kai užsakymas yra sulaikomas.</span><span class="sxs-lookup"><span data-stu-id="92c31-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="92c31-129">Nurodykite **Kreditas** informacinį kodą.</span><span class="sxs-lookup"><span data-stu-id="92c31-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="92c31-130">Pirmiausia gali prireikti sukurti informacinį kodą.</span><span class="sxs-lookup"><span data-stu-id="92c31-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="92c31-131">Šis informacinis kodas pateikia priežasčių kodų rinkinį, iš kurio vartotojas gali pasirinkti, naudodamas skambučių centro užsakymo kredito funkcijas, kad klientas galėtų gauti įvairias grąžinamąsias išmokas dėl klientų aptarnavimo priežasčių.</span><span class="sxs-lookup"><span data-stu-id="92c31-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="92c31-132">Pasirinktinai: nustatykite finansines dimensijas „FastTab“ **Finansinės dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="92c31-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="92c31-133">Čia įvestos dimensijos bus numatytosios visuose pardavimo užsakymuose, sukurtuose šiame skambučių centro kanale.</span><span class="sxs-lookup"><span data-stu-id="92c31-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="92c31-134">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="92c31-134">Click **Save**.</span></span>

<span data-ttu-id="92c31-135">Toliau pateiktame vaizde parodytas naujo skambučių centro kanalo kūrimas.</span><span class="sxs-lookup"><span data-stu-id="92c31-135">The following image shows the creation of a new call center channel.</span></span>

![Naujas skambučių centro kanalas](media/channel-setup-callcenter-1.png)

<span data-ttu-id="92c31-137">Toliau pateiktame vaizde parodytas skambučių centro kanalo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="92c31-137">The following image shows an example call center channel.</span></span>

![Skambučių centro kanalo pavyzdys](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="92c31-139">Papildoma kanalų sąranka</span><span class="sxs-lookup"><span data-stu-id="92c31-139">Additional channel setup</span></span>

<span data-ttu-id="92c31-140">Papildomos užduotys, reikalingos skambučių centro kanalo sąrankai, apima mokėjimo metodų ir pristatymo būdų nustatymą.</span><span class="sxs-lookup"><span data-stu-id="92c31-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="92c31-141">Toliau pateiktame atvaizde rodomos sąrankos parinktys **Pristatymo būdai** ir **Mokėjimo metodai** , esančios skirtuke **Nustatyti**.</span><span class="sxs-lookup"><span data-stu-id="92c31-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![Papildomi skambučių centro kanalo nustatymo veiksmai](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="92c31-143">Nustatyti mokėjimo būdus</span><span class="sxs-lookup"><span data-stu-id="92c31-143">Set up payment methods</span></span>

<span data-ttu-id="92c31-144">Atlikite toliau nurodytus veiksmus, norėdami nustatyti kiekvieno mokėjimo tipo, palaikomo šiame kanale, mokėjimo metodus.</span><span class="sxs-lookup"><span data-stu-id="92c31-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="92c31-145">Vartotojams reikės pasirinkti iš anksto nustatytų mokėjimo metodų, kuriuos reikia susieti su skambučių centro kanalu.</span><span class="sxs-lookup"><span data-stu-id="92c31-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="92c31-146">Prieš nustatydami savo skambučių centro mokėjimo metodus, pirmiausia nustatykite savo pagrindinius atsiskaitymo būdus dalyje **Mažmeninė prekyba ir prekyba \>Kanalų sąranka \> Mokėjimo metodai \> Mokėjimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="92c31-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="92c31-147">Veiksmų srityje pasirinkite skirtuką **Sąranka** , tada pasirinkite **Mokėjimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="92c31-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="92c31-148">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="92c31-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="92c31-149">Naršymo srityje pasirinkite mokėjimo metodą iš anksto nustatytų galimų mokėjimų.</span><span class="sxs-lookup"><span data-stu-id="92c31-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="92c31-150">Konfigūruokite visus papildomus parametrus, kurių reikia mokėjimo tipui.</span><span class="sxs-lookup"><span data-stu-id="92c31-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="92c31-151">Kredito kortelėms, dovanų kortelėms ar lojalumo kortelėms reikalingi papildomi parametrai pasirenkant funkciją **Kortelės sąranka**.</span><span class="sxs-lookup"><span data-stu-id="92c31-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="92c31-152">Konfigūruokite tinkamas mokėjimo tipo registravimo sąskaitas skyriuje **Registravimas**.</span><span class="sxs-lookup"><span data-stu-id="92c31-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="92c31-153">Veiksmų srityje spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="92c31-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="92c31-154">Toliau pateiktame vaizde parodytas mokėjimas grynaisiais pinigais pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="92c31-154">The following image shows an example of a cash payment method.</span></span>

![Mokėjimo metodų pavyzdys](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="92c31-156">Nustatyti pristatymo būdus</span><span class="sxs-lookup"><span data-stu-id="92c31-156">Set up modes of delivery</span></span>

<span data-ttu-id="92c31-157">Galite peržiūrėti sukonfigūruotus pristatymo būdus pasirikdami **Pristatymo būdai** skirtuke **Nustatymas** , esančiame **Veiksmų sritis**.</span><span class="sxs-lookup"><span data-stu-id="92c31-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="92c31-158">Norėdami pakeisti arba pridėti pristatymo būdą, kuris bus susietas su skambučių centro kanalu, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="92c31-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="92c31-159">Skambučių centro pristatymo būdo parinktyse pasirinkite **Valdyti pristatymo būdus**</span><span class="sxs-lookup"><span data-stu-id="92c31-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="92c31-160">Veiksmų srityje pasirinkite **Naujas** , kad sukurtumėte naują pristatymo režimą, arba pasirinkite esamą režimą.</span><span class="sxs-lookup"><span data-stu-id="92c31-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="92c31-161">Skyriuje **Mažmeninės prekybos kanalai** spustelėkite **Įtraukti eilutę** , kad galėtumėte įtraukti skambučių centro kanalą.</span><span class="sxs-lookup"><span data-stu-id="92c31-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="92c31-162">Kanalų įtraukimas naudojant organizacijos mazgus, užuot įtraukus kiekvieną kanalą atskirai, gali racionalizuoti kanalų įtraukimą.</span><span class="sxs-lookup"><span data-stu-id="92c31-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="92c31-163">Įsitikinkite, kad pristatymo būdas sukonfigūruotas su duomenimis, nurodytais „FastTab“ **Produkai** ir „FastTab“ **Adresai**.</span><span class="sxs-lookup"><span data-stu-id="92c31-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="92c31-164">Jei pristatymo būdui nėra tinkamų prekių ar pristatymo adresų, pasirenkant jį užsakymo įvedimo metu atsiras klaidų.</span><span class="sxs-lookup"><span data-stu-id="92c31-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="92c31-165">Po to, kai buvo atlikti bet kokie skambučių centro pristatymo būdo konfigūracijų keitimai, užduotis **Apdoroti pristatymo būdus** turi būti vykdoma, kad išskleistumėte keitimo matricą.</span><span class="sxs-lookup"><span data-stu-id="92c31-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="92c31-166">Šią užduotį galima surasti pereinant į **Mažmeninė prekyba ir prekyba \>Mažmeninės prekybos ir prekybos IT \>Apdoroti pristatymo būdus**.</span><span class="sxs-lookup"><span data-stu-id="92c31-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="92c31-167">Toliau pateiktame vaizde parodytas pristatymo būdo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="92c31-167">The following image shows an example of a mode of delivery.</span></span>

![Nustatyti pristatymo būdus](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="92c31-169">Kanalo vartotojų nustatymas</span><span class="sxs-lookup"><span data-stu-id="92c31-169">Set up channel users</span></span>

<span data-ttu-id="92c31-170">Norėdamas sukurti pardavimo užsakymą, kuris yra susietas su skambučių centro kanalu iš „Commerce Headquarters”, pardavimo užsakymą kuriantis vartotojas turi būti susietas su skambučių centro kanalu.</span><span class="sxs-lookup"><span data-stu-id="92c31-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="92c31-171">Vartotojas rankiniu būdu negali susieti pardavimo užsakymo, sukurto „Commerce Headquarters”, su skambučių centro kanalu.</span><span class="sxs-lookup"><span data-stu-id="92c31-171">The user cannot manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="92c31-172">Saitas yra sistemingas, jis paremtas vartotoju ir vartotojo ryšiu su skambučių centro kanalu.</span><span class="sxs-lookup"><span data-stu-id="92c31-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="92c31-173">Vartotojas gali būti susietas tik su vienu skambučių centro kanalu.</span><span class="sxs-lookup"><span data-stu-id="92c31-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="92c31-174">Veiksmų srityje pasirinkite skirtuką **Kanalas** , tada pasirinkite **Kanalo vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="92c31-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="92c31-175">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="92c31-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="92c31-176">Pasirinkite esamą **Vartotojo ID** iš išplečiamojo pasirinkimo sąrašo, jei norite susieti šį vartotoją su skambučių centro kanalu</span><span class="sxs-lookup"><span data-stu-id="92c31-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="92c31-177">Kai kanalo vartotojų sąranka baigta ir vartotojas sukūrė naują pardavimo užsakymą programoje „Commerce Headquarters”, pardavimo užsakymas bus susietas su jo susietu skambučių centro kanalu.</span><span class="sxs-lookup"><span data-stu-id="92c31-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="92c31-178">Visos šio kanalo konfigūracijos bus sistemingai taikomos pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="92c31-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="92c31-179">Vartotojas gali patvirtinti, su kuriuo skambučių centro kanalu pardavimo užsakymas yra susietas, pardavimo užsakymo antraštėje peržiūrėdamas kanalo pavadinimo nuorodą.</span><span class="sxs-lookup"><span data-stu-id="92c31-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="92c31-180">Nustatyti kainų grupes</span><span class="sxs-lookup"><span data-stu-id="92c31-180">Set up price groups</span></span>

<span data-ttu-id="92c31-181">Kainos grupės yra pasirinktinės, tačiau, jei jos naudojamos, galima kontroliuoti, kurios pardavimo kainos bus siūlomos klientams, pateikiantiems užsakymus skambučių centro kanale.</span><span class="sxs-lookup"><span data-stu-id="92c31-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="92c31-182">Jei kainos grupė nesukonfigūruota klientui, arba jei katalogo kainos grupės nėra taikomos pardavimo užsakymui (skambučių centro užsakymo antraštėje naudojant lauką **Šaltinio kodo ID** ), tada kanalo kainos grupė naudojama prekių kainoms rasti.</span><span class="sxs-lookup"><span data-stu-id="92c31-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="92c31-183">Jei kainos grupė skambučių centro kanale nerasta, naudojamos numatytosios pagrindinės prekės kainos.</span><span class="sxs-lookup"><span data-stu-id="92c31-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="92c31-184">Norėdami nustatyti kainos grupę, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="92c31-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="92c31-185">Veiksmų srityje spustelėkite skirtuką **Kanalas** , tada pasirinkite **Kainos grupės**.</span><span class="sxs-lookup"><span data-stu-id="92c31-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="92c31-186">Veiksmų srityje spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="92c31-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="92c31-187">Išplečiamajame pasirinkimo sąraše pažymėkite **Mažmeninės kainos grupė**.</span><span class="sxs-lookup"><span data-stu-id="92c31-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92c31-188">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="92c31-188">Additional resources</span></span>

[<span data-ttu-id="92c31-189">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="92c31-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="92c31-190">Skambučių centro pardavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="92c31-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="92c31-191">Skambučių centro užsakymo apdorojimo parinkčių nustatymas</span><span class="sxs-lookup"><span data-stu-id="92c31-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="92c31-192">Skambučių centro katalogai</span><span class="sxs-lookup"><span data-stu-id="92c31-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="92c31-193">Įspėjimų dėl apgaulės nustatymas ir jų naudojimas</span><span class="sxs-lookup"><span data-stu-id="92c31-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="92c31-194">Skambučių centrų tęstinumo programų nustatymas</span><span class="sxs-lookup"><span data-stu-id="92c31-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
