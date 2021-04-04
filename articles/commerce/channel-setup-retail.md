---
title: Mažmeninės prekybos kanalo nustatymas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują mažmeninės prekybos kanalą.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a5d0a081cff9fab8dc0a513496e6a5eccd03c871
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478265"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="7fb33-103">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="7fb33-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7fb33-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują mažmeninės prekybos kanalą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7fb33-105">„Dynamics 365 Commerce“ palaiko kelis mažmeninės prekybos kanalus.</span><span class="sxs-lookup"><span data-stu-id="7fb33-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="7fb33-106">Šie mažmeninės prekybos kanalai apima interneto parduotuves, skambučių centrus ir mažmeninės prekybos parduotuves (taip pat vadinamas fizinėmis parduotuvėmis).</span><span class="sxs-lookup"><span data-stu-id="7fb33-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="7fb33-107">Kiekviename mažmeninės prekybos parduotuvės kanale gali būti naudojami savi mokėjimo būdai, kainų grupės, elektroninių kasos aparatų (EKA) registrai, pajamų ir išlaidų sąskaitos bei darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="7fb33-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="7fb33-108">Prieš kurdami mažmeninės prekybos parduotuvės kanalą, turite nustatyti visus šiuos elementus.</span><span class="sxs-lookup"><span data-stu-id="7fb33-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="7fb33-109">Prieš kurdami mažmeninės prekybos kanalą, įsitikinkite, kad išpildėte [kanalo būtinąsias sąlygas](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="7fb33-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="7fb33-110">Naujo mažmeninės prekybos kanalo kūrimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7fb33-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="7fb33-111">Naršymo srityje eikite **Moduliai \> Kanalai \> Parduotuvės \> Visos parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="7fb33-112">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7fb33-113">Lauke **Pavadinimas** įveskite naujo kanalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="7fb33-114">Lauke **Parduotuvės numeris** pateikite unikalų parduotuvės numerį.</span><span class="sxs-lookup"><span data-stu-id="7fb33-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="7fb33-115">Numeris gali būti raidinis-skaitinis, bet ne daugiau kaip iš 10 simbolių.</span><span class="sxs-lookup"><span data-stu-id="7fb33-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="7fb33-116">Išplečiamajame sąraše **Juridinis subjektas** įveskite atitinkamą juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="7fb33-117">Išplečiamajame sąraše **Sandėlis** įveskite atitinkamą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="7fb33-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="7fb33-118">Lauke **Parduotuvės laiko juosta** pasirinkite atitinkamą laiko juostą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="7fb33-119">Išplečiamajame sąraše **PVM grupė** pasirinkite atitinkamą parduotuvės PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="7fb33-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="7fb33-120">Lauke **Valiuta** pasirinkite atitinkamą valiutą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="7fb33-121">Lauke **Kliento adresų knygelė** nurodykite galiojančią adresų knygelę.</span><span class="sxs-lookup"><span data-stu-id="7fb33-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="7fb33-122">Lauke **Numatytasis klientas** pateikite galiojantį numatytąjį klientą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="7fb33-123">Lauke **Funkcijų šablonas** pasirinkite funkcijų šabloną, jei taikoma.</span><span class="sxs-lookup"><span data-stu-id="7fb33-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="7fb33-124">Lauke **El. paštu siunčiamo pranešimo šablonas** pateikite galiojantį el. siunčiamo pranešimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="7fb33-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="7fb33-125">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-125">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7fb33-126">Toliau pateiktame vaizde parodytas naujo mažmeninės prekybos kanalo kūrimas.</span><span class="sxs-lookup"><span data-stu-id="7fb33-126">The following image shows the creation of a new retail channel.</span></span>

![Naujas mažmeninės prekybos kanalas](media/channel-setup-retail-1.png)

<span data-ttu-id="7fb33-128">Toliau pateiktame vaizde parodytas mažmeninės prekybos kanalo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="7fb33-128">The following image shows an example retail channel.</span></span>

![Mažmeninės prekybos kanalas](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="7fb33-130">Kiti parametrai</span><span class="sxs-lookup"><span data-stu-id="7fb33-130">Other settings</span></span>

<span data-ttu-id="7fb33-131">Yra daug kitų pasirinktinių parametrų, kuriuos galima nustatyti skyriuose **Išrašas / uždarymas** ir **Įvairūs** pagal mažmeninės prekybos parduotuvės poreikius.</span><span class="sxs-lookup"><span data-stu-id="7fb33-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="7fb33-132">Be to, žr. [Elektroninio kasos aparato (EKA) ekrano maketai](pos-screen-layouts.md), kur pateikta informacijos, kaip nustatyti numatytąjį ekrano maketą skyriuje **Ekrano maketas** ir [„Retail Hardware Station“ konfigūravimas ir diegimas](retail-hardware-station-configuration-installation.md), kur pateikta skyriaus **Aparatūros stotys** sąrankos informacija.</span><span class="sxs-lookup"><span data-stu-id="7fb33-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="7fb33-133">Toliau pateiktame vaizde parodytas mažmeninės prekybos kanalo sąrankos konfigūravimas.</span><span class="sxs-lookup"><span data-stu-id="7fb33-133">The following image shows an example retail channel setup configuration.</span></span>

![Mažmeninės prekybos kanalo konfigūravimo pavyzdys](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="7fb33-135">Papildoma kanalų sąranka</span><span class="sxs-lookup"><span data-stu-id="7fb33-135">Additional channel set up</span></span>

<span data-ttu-id="7fb33-136">Yra papildomų kanalo elementų, kuriuos reikia nustatyti, juos galima rasti dalyje **Veiksmų sritis** skyriuje **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-136">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="7fb33-137">Papildomos užduotys, reikalingos interneto kanalo sąrankai, apima mokėjimo metodų, grynųjų pinigų deklaracijų, pristatymo būdų, pajamų / išlaidų sąskaitų, skyrių, vykdymo grupių priskyrimo ir seifų nustatymą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="7fb33-138">Šiame vaizde rodomos įvairios papildomos mažmeninės prekybos kanalo nustatymo parinktys skirtuke **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanalo nustatymas](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="7fb33-140">Nustatyti mokėjimo būdus</span><span class="sxs-lookup"><span data-stu-id="7fb33-140">Set up payment methods</span></span>

<span data-ttu-id="7fb33-141">Norėdami nustatyti kiekvieno mokėjimo tipo, palaikomo šiame kanale, mokėjimo metodus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7fb33-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="7fb33-142">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Mokėjimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="7fb33-143">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7fb33-144">Naršymo srityje pasirinkite pageidaujamą mokėjimo metodą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="7fb33-145">Skyriuje **Bendri** nurodykite **Operacijos pavadinimas** ir konfigūruokite kitus pageidaujamus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="7fb33-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="7fb33-146">Konfigūruokite visus papildomus parametrus, kurių reikia mokėjimo tipui.</span><span class="sxs-lookup"><span data-stu-id="7fb33-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="7fb33-147">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7fb33-148">Toliau pateiktame vaizde parodytas mokėjimas grynaisiais pinigais pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="7fb33-148">The following image shows an example of a cash payment method.</span></span>

![Mokėjimo metodų pavyzdys](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="7fb33-150">Grynųjų pinigų deklaravimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="7fb33-150">Set up cash declaration</span></span>

1. <span data-ttu-id="7fb33-151">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Grynųjų pinigų deklaracija**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-151">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="7fb33-152">Veiksmų **srityje pasirinkite naujas** ir sukurkite visą **taikytiną monetų** ir **pastabų** nominalą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-152">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="7fb33-153">Toliau pateiktame vaizde parodytas grynųjų pinigų deklaracijos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="7fb33-153">The following image shows an example of a cash declaration.</span></span>

![Grynųjų pinigų deklaravimo nustatymas](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="7fb33-155">Nustatyti pristatymo būdus</span><span class="sxs-lookup"><span data-stu-id="7fb33-155">Set up modes of delivery</span></span>

<span data-ttu-id="7fb33-156">Galite peržiūrėti sukonfigūruotus pristatymo būdus pasirikdami **Pristatymo būdai** skirtuke **Nustatymas**, esančiame **Veiksmų sritis**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="7fb33-157">Norėdami pakeisti arba įtraukti pristatymo būdą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7fb33-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="7fb33-158">Naršymo srityje eikite į **Moduliai \> Atsargų valdymas \> Pristatymo būdai**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="7fb33-159">Veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte naują pristatymo režimą, arba pasirinkite esamą režimą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-159">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="7fb33-160">Skyriuje **Mažmeninės prekybos kanalai** pasirinkite **Įtraukti eilutę**, kad galėtumėte įtraukti kanalą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="7fb33-161">Kanalų įtraukimas naudojant organizacijos mazgus, užuot įtraukus kiekvieną kanalą atskirai, gali racionalizuoti kanalų įtraukimą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="7fb33-162">Toliau pateiktame vaizde parodytas pristatymo būdo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="7fb33-162">The following image shows an example of a mode of delivery.</span></span>

![Nustatyti pristatymo būdus](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="7fb33-164">Pajamų/išlaidų sąskaitos nustatymas</span><span class="sxs-lookup"><span data-stu-id="7fb33-164">Set up income/expense account</span></span>

<span data-ttu-id="7fb33-165">Norėdami nustatyti produktų pajamų / išlaidų sąskaitą, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7fb33-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="7fb33-166">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Pajamų / išlaidų sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-166">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="7fb33-167">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-167">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7fb33-168">Dalyje **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="7fb33-169">Dalyje **Ieškos pavadinimas** įveskite ieškos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="7fb33-170">Dalyje **Sąskaitos tipas** įveskite sąskaitos tipą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="7fb33-171">Įveskite tekstą **1 pranešimų eilutė**, **2 pranešimų eilutė**, **1 kvito tekstas** ir **2 kvito tekstas**, kaip reikia.</span><span class="sxs-lookup"><span data-stu-id="7fb33-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="7fb33-172">Dalyje **Registravimas** įveskite registravimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="7fb33-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="7fb33-173">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-173">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7fb33-174">Toliau pateiktame paveiksle parodytas pajamų / išlaidų sąskaitos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="7fb33-174">The following image shows an example of an income/expense account.</span></span>

![Pajamų / išlaidų sąskaitų nustatymas](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="7fb33-176">Skyrių nustatymas</span><span class="sxs-lookup"><span data-stu-id="7fb33-176">Set up sections</span></span>

<span data-ttu-id="7fb33-177">Norėdami nustatyti skyrius, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7fb33-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="7fb33-178">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada spustelėkite **Skyriai**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-178">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="7fb33-179">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-179">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7fb33-180">Dalyje **Skyriaus numeris** įveskite skyriaus numerį.</span><span class="sxs-lookup"><span data-stu-id="7fb33-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="7fb33-181">Dalyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="7fb33-182">Dalyje **Skyriaus dydis** įveskite skyriaus dydį.</span><span class="sxs-lookup"><span data-stu-id="7fb33-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="7fb33-183">Jei reikia, konfigūruokite parametrus **Bendri** ir **Pardavimo statistika**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="7fb33-184">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-184">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="7fb33-185">Vykdymo grupės priskyrimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="7fb33-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="7fb33-186">Norėdami nustatyti vykdymo grupės priskyrimą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7fb33-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="7fb33-187">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Vykdymo grupės priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-187">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="7fb33-188">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-188">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7fb33-189">Išplečiamajame sąraše **Vykdymo grupė** pasirinkite vykdymo grupę.</span><span class="sxs-lookup"><span data-stu-id="7fb33-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="7fb33-190">Išplečiamajame sąraše **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="7fb33-191">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-191">On the action pane, select **Save**</span></span>

<span data-ttu-id="7fb33-192">Toliau pateiktame vaizde parodytas vykdymo grupės priskyrimo sąrankos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="7fb33-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Vykdymo grupės priskyrimų nustatymas](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="7fb33-194">Seifų nustatymas</span><span class="sxs-lookup"><span data-stu-id="7fb33-194">Set up safes</span></span>

<span data-ttu-id="7fb33-195">Norėdami nustatyti seifus, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7fb33-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="7fb33-196">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada spustelėkite **Seifai**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-196">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="7fb33-197">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-197">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7fb33-198">Įveskite seifo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7fb33-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="7fb33-199">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7fb33-199">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fb33-200">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7fb33-200">Additional resources</span></span>

[<span data-ttu-id="7fb33-201">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="7fb33-201">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7fb33-202">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="7fb33-202">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="7fb33-203">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="7fb33-203">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="7fb33-204">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="7fb33-204">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
