---
title: Mažmeninės prekybos kanalo nustatymas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują mažmeninės prekybos kanalą.
author: samjarawan
ms.date: 04/23/2021
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
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937539"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="db474-103">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="db474-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="db474-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują mažmeninės prekybos kanalą.</span><span class="sxs-lookup"><span data-stu-id="db474-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="db474-105">„Dynamics 365 Commerce“ palaiko kelis mažmeninės prekybos kanalus.</span><span class="sxs-lookup"><span data-stu-id="db474-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="db474-106">Šie mažmeninės prekybos kanalai apima interneto parduotuves, skambučių centrus ir mažmeninės prekybos parduotuves (taip pat vadinamas fizinėmis parduotuvėmis).</span><span class="sxs-lookup"><span data-stu-id="db474-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="db474-107">Kiekviename mažmeninės prekybos parduotuvės kanale gali būti naudojami savi mokėjimo būdai, kainų grupės, elektroninių kasos aparatų (EKA) registrai, pajamų ir išlaidų sąskaitos bei darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="db474-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="db474-108">Prieš kurdami mažmeninės prekybos parduotuvės kanalą, turite nustatyti visus šiuos elementus.</span><span class="sxs-lookup"><span data-stu-id="db474-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="db474-109">Prieš kurdami mažmeninės prekybos kanalą, įsitikinkite, kad išpildėte [kanalo būtinąsias sąlygas](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="db474-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="db474-110">Naujo mažmeninės prekybos kanalo kūrimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="db474-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="db474-111">Naršymo srityje eikite **Moduliai \> Kanalai \> Parduotuvės \> Visos parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="db474-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="db474-112">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="db474-112">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="db474-113">Lauke **Pavadinimas** įveskite naujo kanalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="db474-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="db474-114">Lauke **Parduotuvės numeris** pateikite unikalų parduotuvės numerį.</span><span class="sxs-lookup"><span data-stu-id="db474-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="db474-115">Numeris gali būti raidinis-skaitinis, bet ne daugiau kaip iš 10 simbolių.</span><span class="sxs-lookup"><span data-stu-id="db474-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="db474-116">Išplečiamajame sąraše **Juridinis subjektas** įveskite atitinkamą juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="db474-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="db474-117">Išplečiamajame sąraše **Sandėlis** įveskite atitinkamą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="db474-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="db474-118">Lauke **Parduotuvės laiko juosta** pasirinkite atitinkamą laiko juostą.</span><span class="sxs-lookup"><span data-stu-id="db474-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="db474-119">Išplečiamajame sąraše **PVM grupė** pasirinkite atitinkamą parduotuvės PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="db474-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="db474-120">Lauke **Valiuta** pasirinkite atitinkamą valiutą.</span><span class="sxs-lookup"><span data-stu-id="db474-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="db474-121">Lauke **Kliento adresų knygelė** nurodykite galiojančią adresų knygelę.</span><span class="sxs-lookup"><span data-stu-id="db474-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="db474-122">Lauke **Numatytasis klientas** pateikite galiojantį numatytąjį klientą.</span><span class="sxs-lookup"><span data-stu-id="db474-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="db474-123">Lauke **Funkcijų šablonas** pasirinkite funkcijų šabloną, jei taikoma.</span><span class="sxs-lookup"><span data-stu-id="db474-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="db474-124">Lauke **El. paštu siunčiamo pranešimo šablonas** pateikite galiojantį el. siunčiamo pranešimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="db474-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="db474-125">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="db474-125">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="db474-126">Toliau pateiktame vaizde parodytas naujo mažmeninės prekybos kanalo kūrimas.</span><span class="sxs-lookup"><span data-stu-id="db474-126">The following image shows the creation of a new retail channel.</span></span>

![Naujas mažmeninės prekybos kanalas](media/channel-setup-retail-1.png)

<span data-ttu-id="db474-128">Toliau pateiktame vaizde parodytas mažmeninės prekybos kanalo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="db474-128">The following image shows an example retail channel.</span></span>

![Mažmeninės prekybos kanalas](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="db474-130">Kiti parametrai</span><span class="sxs-lookup"><span data-stu-id="db474-130">Other settings</span></span>

<span data-ttu-id="db474-131">Yra daug kitų pasirinktinių parametrų, kuriuos galima nustatyti skyriuose **Išrašas / uždarymas** ir **Įvairūs** pagal mažmeninės prekybos parduotuvės poreikius.</span><span class="sxs-lookup"><span data-stu-id="db474-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="db474-132">Be to, žr. [Elektroninio kasos aparato (EKA) ekrano maketai](pos-screen-layouts.md), kur pateikta informacijos, kaip nustatyti numatytąjį ekrano maketą skyriuje **Ekrano maketas** ir [„Retail Hardware Station“ konfigūravimas ir diegimas](retail-hardware-station-configuration-installation.md), kur pateikta skyriaus **Aparatūros stotys** sąrankos informacija.</span><span class="sxs-lookup"><span data-stu-id="db474-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="db474-133">Toliau pateiktame vaizde parodytas mažmeninės prekybos kanalo sąrankos konfigūravimas.</span><span class="sxs-lookup"><span data-stu-id="db474-133">The following image shows an example retail channel setup configuration.</span></span>

![Mažmeninės prekybos kanalo konfigūravimo pavyzdys](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="db474-135">Papildoma kanalų sąranka</span><span class="sxs-lookup"><span data-stu-id="db474-135">Additional channel set up</span></span>

<span data-ttu-id="db474-136">Yra papildomų kanalo elementų, kuriuos reikia nustatyti, juos galima rasti dalyje Veiksmų sritis skyriuje **Nustatyti**.</span><span class="sxs-lookup"><span data-stu-id="db474-136">There are additional items that need to be set up for a channel that can be found on the Action Pane under the **Set up** section.</span></span>

<span data-ttu-id="db474-137">Papildomos užduotys, reikalingos interneto kanalo sąrankai, apima mokėjimo metodų, grynųjų pinigų deklaracijų, pristatymo būdų, pajamų / išlaidų sąskaitų, skyrių, vykdymo grupių priskyrimo ir seifų nustatymą.</span><span class="sxs-lookup"><span data-stu-id="db474-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="db474-138">Šiame vaizde rodomos įvairios papildomos mažmeninės prekybos kanalo nustatymo parinktys skirtuke **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="db474-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanalo nustatymas](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="db474-140">Nustatyti mokėjimo būdus</span><span class="sxs-lookup"><span data-stu-id="db474-140">Set up payment methods</span></span>

<span data-ttu-id="db474-141">Norėdami nustatyti kiekvieno mokėjimo tipo, palaikomo šiame kanale, mokėjimo metodus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="db474-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="db474-142">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Mokėjimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="db474-142">On the Action Pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="db474-143">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="db474-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="db474-144">Naršymo srityje pasirinkite pageidaujamą mokėjimo metodą.</span><span class="sxs-lookup"><span data-stu-id="db474-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="db474-145">Skyriuje **Bendri** nurodykite **Operacijos pavadinimas** ir konfigūruokite kitus pageidaujamus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="db474-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="db474-146">Konfigūruokite visus papildomus parametrus, kurių reikia mokėjimo tipui.</span><span class="sxs-lookup"><span data-stu-id="db474-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="db474-147">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="db474-147">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="db474-148">Toliau pateiktame vaizde parodytas mokėjimas grynaisiais pinigais pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="db474-148">The following image shows an example of a cash payment method.</span></span>

![Mokėjimo metodų pavyzdys](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="db474-150">Grynųjų pinigų deklaravimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="db474-150">Set up cash declaration</span></span>

1. <span data-ttu-id="db474-151">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Grynųjų pinigų deklaracija**.</span><span class="sxs-lookup"><span data-stu-id="db474-151">On the Action Pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="db474-152">Veiksmų **srityje pasirinkite naujas** ir sukurkite visą **taikytiną monetų** ir **pastabų** nominalą.</span><span class="sxs-lookup"><span data-stu-id="db474-152">On the Action Pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="db474-153">Toliau pateiktame vaizde parodytas grynųjų pinigų deklaracijos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="db474-153">The following image shows an example of a cash declaration.</span></span>

![Grynųjų pinigų deklaravimo nustatymas](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="db474-155">Nustatyti pristatymo būdus</span><span class="sxs-lookup"><span data-stu-id="db474-155">Set up modes of delivery</span></span>

<span data-ttu-id="db474-156">Galite peržiūrėti sukonfigūruotus pristatymo būdus pasirikdami **Pristatymo būdai** skirtuke **Nustatymas** Veiksmų sritis.</span><span class="sxs-lookup"><span data-stu-id="db474-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the Action Pane.</span></span>  

<span data-ttu-id="db474-157">Norėdami pakeisti arba įtraukti pristatymo būdą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="db474-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="db474-158">Naršymo srityje eikite į **Moduliai \> Atsargų valdymas \> Pristatymo būdai**.</span><span class="sxs-lookup"><span data-stu-id="db474-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="db474-159">Veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte naują pristatymo režimą, arba pasirinkite esamą režimą.</span><span class="sxs-lookup"><span data-stu-id="db474-159">On the Action Pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="db474-160">Skyriuje **Mažmeninės prekybos kanalai** pasirinkite **Įtraukti eilutę**, kad galėtumėte įtraukti kanalą.</span><span class="sxs-lookup"><span data-stu-id="db474-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="db474-161">Kanalų įtraukimas naudojant organizacijos mazgus, užuot įtraukus kiekvieną kanalą atskirai, gali racionalizuoti kanalų įtraukimą.</span><span class="sxs-lookup"><span data-stu-id="db474-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="db474-162">Toliau pateiktame vaizde parodytas pristatymo būdo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="db474-162">The following image shows an example of a mode of delivery.</span></span>

![Nustatyti pristatymo būdus](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="db474-164">Pajamų/išlaidų sąskaitos nustatymas</span><span class="sxs-lookup"><span data-stu-id="db474-164">Set up income/expense account</span></span>

<span data-ttu-id="db474-165">Norėdami nustatyti produktų pajamų / išlaidų sąskaitą, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="db474-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="db474-166">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Pajamų / išlaidų sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="db474-166">On the Action Pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="db474-167">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="db474-167">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="db474-168">Dalyje **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="db474-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="db474-169">Dalyje **Ieškos pavadinimas** įveskite ieškos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="db474-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="db474-170">Dalyje **Sąskaitos tipas** įveskite sąskaitos tipą.</span><span class="sxs-lookup"><span data-stu-id="db474-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="db474-171">Įveskite tekstą **1 pranešimų eilutė**, **2 pranešimų eilutė**, **1 kvito tekstas** ir **2 kvito tekstas**, kaip reikia.</span><span class="sxs-lookup"><span data-stu-id="db474-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="db474-172">Dalyje **Registravimas** įveskite registravimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="db474-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="db474-173">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="db474-173">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="db474-174">Toliau pateiktame paveiksle parodytas pajamų / išlaidų sąskaitos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="db474-174">The following image shows an example of an income/expense account.</span></span>

![Pajamų / išlaidų sąskaitų nustatymas](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="db474-176">Skyrių nustatymas</span><span class="sxs-lookup"><span data-stu-id="db474-176">Set up sections</span></span>

<span data-ttu-id="db474-177">Norėdami nustatyti skyrius, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="db474-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="db474-178">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada spustelėkite **Skyriai**.</span><span class="sxs-lookup"><span data-stu-id="db474-178">On the Action Pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="db474-179">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="db474-179">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="db474-180">Dalyje **Skyriaus numeris** įveskite skyriaus numerį.</span><span class="sxs-lookup"><span data-stu-id="db474-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="db474-181">Dalyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="db474-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="db474-182">Dalyje **Skyriaus dydis** įveskite skyriaus dydį.</span><span class="sxs-lookup"><span data-stu-id="db474-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="db474-183">Jei reikia, konfigūruokite parametrus **Bendri** ir **Pardavimo statistika**.</span><span class="sxs-lookup"><span data-stu-id="db474-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="db474-184">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="db474-184">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="db474-185">Vykdymo grupės priskyrimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="db474-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="db474-186">Norėdami nustatyti vykdymo grupės priskyrimą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="db474-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="db474-187">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Vykdymo grupės priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="db474-187">On the Action Pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="db474-188">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="db474-188">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="db474-189">Išplečiamajame sąraše **Vykdymo grupė** pasirinkite vykdymo grupę.</span><span class="sxs-lookup"><span data-stu-id="db474-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="db474-190">Išplečiamajame sąraše **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="db474-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="db474-191">Veiksmų srityje pasirinkite **Įrašyti**</span><span class="sxs-lookup"><span data-stu-id="db474-191">On the Action Pane, select **Save**</span></span>

<span data-ttu-id="db474-192">Toliau pateiktame vaizde parodytas vykdymo grupės priskyrimo sąrankos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="db474-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Vykdymo grupės priskyrimų nustatymas](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="db474-194">Seifų nustatymas</span><span class="sxs-lookup"><span data-stu-id="db474-194">Set up safes</span></span>

<span data-ttu-id="db474-195">Norėdami nustatyti seifus, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="db474-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="db474-196">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada spustelėkite **Seifai**.</span><span class="sxs-lookup"><span data-stu-id="db474-196">On the Action Pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="db474-197">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="db474-197">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="db474-198">Įveskite seifo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="db474-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="db474-199">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="db474-199">On the Action Pane, select **Save**.</span></span>

### <a name="ensure-unique-transaction-ids"></a><span data-ttu-id="db474-200">Užtikrinkite unikalius operacijų ID</span><span class="sxs-lookup"><span data-stu-id="db474-200">Ensure unique transaction IDs</span></span>

<span data-ttu-id="db474-201">Naudojant „Commerce" 10.0.18 versiją, sugeneruoti elektroninį kasos numerį (EKA) operacijų ID yra nuoseklūs ir apima šias dalis:</span><span class="sxs-lookup"><span data-stu-id="db474-201">As of the Commerce version 10.0.18 , transaction IDs generated for the point of sale (POS) are sequential and include the following parts:</span></span>

- <span data-ttu-id="db474-202">Fiksuota dalis, kuri yra parduotuvės ID ir mokėjimo terminalo ID sąlaja.</span><span class="sxs-lookup"><span data-stu-id="db474-202">A fixed part, which is a concatenation of store ID and terminal ID.</span></span> 
- <span data-ttu-id="db474-203">Nuosekli dalis, kuri yra numeracija.</span><span class="sxs-lookup"><span data-stu-id="db474-203">A sequential part, which is a number sequence.</span></span> 

<span data-ttu-id="db474-204">Tiksliau šis formatas yra *{store} - {terminal} -{numbersequence}*.</span><span class="sxs-lookup"><span data-stu-id="db474-204">Specifically, the format is *{store}-{terminal}-{numbersequence}*.</span></span> 

<span data-ttu-id="db474-205">Dėl to, kad operacijų ID galima generuoti neprisijungus ir tinkle, generuojami besidubliuotų operacijų ID egzemplioriai.</span><span class="sxs-lookup"><span data-stu-id="db474-205">Because transaction IDs can be generated in offline and online modes, there have been instances of duplicate transaction IDs being generated.</span></span> <span data-ttu-id="db474-206">Šalinant dubliuotų operacijų ID, reikia rankiniu būdu taisymo partijos.</span><span class="sxs-lookup"><span data-stu-id="db474-206">Eliminating duplicate transaction IDs requires a lot of manual data fixing.</span></span> 

<span data-ttu-id="db474-207">Naudojant „Commerce" versiją 10.0.19, operacijos ID formatas buvo atnaujintas norint pašalinti nuoseklią dalį ir vietoj jo naudoja 13 skaitmenų skaičių, sugeneruotą skaičiuojant laiką milisekunde nuo 1970.</span><span class="sxs-lookup"><span data-stu-id="db474-207">With Commerce version 10.0.19, the transaction ID format has been updated to remove the sequential part and instead uses a 13-digit number generated by calculating the time in milliseconds since 1970.</span></span> <span data-ttu-id="db474-208">Naudojant šį pakeitimą, naujas operacijos ID formatas yra *{store}{terminal} -{millisecondsSince1970}*.</span><span class="sxs-lookup"><span data-stu-id="db474-208">With this change, the new transaction ID format is *{store}-{terminal}-{millisecondsSince1970}*.</span></span> <span data-ttu-id="db474-209">Dėl šio atnaujinimo operacijos ID yra nuosekli ir užtikrina, kad operacijų ID visada yra unikalūs.</span><span class="sxs-lookup"><span data-stu-id="db474-209">This update makes the transaction ID non-sequential and ensures that transaction IDs are always unique.</span></span> 

> [!NOTE]
> <span data-ttu-id="db474-210">Operacijų ID yra skirti tik vidiniam sistemos naudojimui, todėl jie nėra būtini nuosekliai.</span><span class="sxs-lookup"><span data-stu-id="db474-210">Transaction IDs are meant for internal system use only, so they are not required to be sequential.</span></span> <span data-ttu-id="db474-211">Tačiau daugelis šalių reikalauja, kad gavimo BŪTŲ nuoseklūs.</span><span class="sxs-lookup"><span data-stu-id="db474-211">However, many countries require receipt IDs to be sequential.</span></span>

<span data-ttu-id="db474-212">Nauja operacijos ID formato funkcija gali būti įgalinta funkcijų **valdymo darbo** srityje.</span><span class="sxs-lookup"><span data-stu-id="db474-212">The new transaction ID format feature can be enabled from the **Feature management** workspace.</span></span> 

<span data-ttu-id="db474-213">Norėdami įgalinti naujų operacijų ID naudojimą, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="db474-213">To enable the use of new transaction IDs, follow these steps:</span></span>

1. <span data-ttu-id="db474-214">„Commerce headquaters“ eikite į **Sistemos administravimas \> Darbo sritys \> Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="db474-214">In Commerce headquarters, go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="db474-215">„Retail ir Commerce" modulio filtras.</span><span class="sxs-lookup"><span data-stu-id="db474-215">Filter for the "retail and commerce" module.</span></span>
1. <span data-ttu-id="db474-216">Ieškokite funkcijos Įgalinti **naują operacijos ID, kad išvengtumėte pasikartojančių operacijų** ID funkcijos pavadinimo.</span><span class="sxs-lookup"><span data-stu-id="db474-216">Search for the **Enable new transaction id to avoid duplicate transaction ids** feature name.</span></span>
1. <span data-ttu-id="db474-217">Pasirinkite norimą įjungti funkciją, tada dešinioje juostoje pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="db474-217">Select the feature, and then select **Enable Now** in the right pane.</span></span>  
1. <span data-ttu-id="db474-218">Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="db474-218">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="db474-219">Paleiskite **1070 kanalo konfigūraciją ir** 1170 EKA užduočių įrašymo priemonės užduotis, kad būtų **sinchronizuojama įgalinta funkcija su** parduotuvėmis.</span><span class="sxs-lookup"><span data-stu-id="db474-219">Run the **1070 Channel configuration** and **1170 POS task recorder** jobs to synchronize the enabled feature to the stores.</span></span>
1. <span data-ttu-id="db474-220">Išsiuntus pakeitimus į parduotuves, EKA terminalai turi būti uždaryti ir atidaryti iš naujo, kad būtų naudojamas naujas operacijos ID formatas.</span><span class="sxs-lookup"><span data-stu-id="db474-220">After the changes have been sent to the stores, POS terminals must be closed and reopened to use the new transaction ID format.</span></span> 

> [!NOTE]
> <span data-ttu-id="db474-221">Įjungus naują operacijos ID formato priemonę, šios funkcijos išjungti negalėsite.</span><span class="sxs-lookup"><span data-stu-id="db474-221">After the new transaction ID format feature is enabled, you will not be able to disable this feature.</span></span> <span data-ttu-id="db474-222">Jei jį reikia išjungti, susisiekite su „Commerce Support".</span><span class="sxs-lookup"><span data-stu-id="db474-222">If it must be disabled, please contact Commerce Support.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db474-223">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="db474-223">Additional resources</span></span>

[<span data-ttu-id="db474-224">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="db474-224">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="db474-225">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="db474-225">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="db474-226">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="db474-226">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="db474-227">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="db474-227">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
