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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8ac01f36912fa5e8a09bb4f324ef272cec737aa1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002386"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="ab9d6-103">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ab9d6-103">Set up a retail channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ab9d6-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują mažmeninės prekybos kanalą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ab9d6-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="ab9d6-105">Overview</span></span>

<span data-ttu-id="ab9d6-106">„Dynamics 365 Commerce“ palaiko kelis mažmeninės prekybos kanalus.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="ab9d6-107">Šie mažmeninės prekybos kanalai apima interneto parduotuves, skambučių centrus ir mažmeninės prekybos parduotuves (taip pat vadinamas fizinėmis parduotuvėmis).</span><span class="sxs-lookup"><span data-stu-id="ab9d6-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="ab9d6-108">Kiekviename mažmeninės prekybos parduotuvės kanale gali būti naudojami savi mokėjimo būdai, kainų grupės, elektroninių kasos aparatų (EKA) registrai, pajamų ir išlaidų sąskaitos bei darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="ab9d6-109">Prieš kurdami mažmeninės prekybos parduotuvės kanalą, turite nustatyti visus šiuos elementus.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="ab9d6-110">Prieš kurdami mažmeninės prekybos kanalą, įsitikinkite, kad išpildėte [kanalo būtinąsias sąlygas](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="ab9d6-110">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="ab9d6-111">Naujo mažmeninės prekybos kanalo kūrimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ab9d6-111">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="ab9d6-112">Naršymo srityje eikite **Moduliai \> Kanalai \> Parduotuvės \> Visos parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-112">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="ab9d6-113">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ab9d6-114">Lauke **Pavadinimas** įveskite naujo kanalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="ab9d6-115">Lauke **Parduotuvės numeris** pateikite unikalų parduotuvės numerį.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-115">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="ab9d6-116">Numeris gali būti raidinis-skaitinis, bet ne daugiau kaip iš 10 simbolių.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-116">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="ab9d6-117">Išplečiamajame sąraše **Juridinis subjektas** įveskite atitinkamą juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-117">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="ab9d6-118">Išplečiamajame sąraše **Sandėlis** įveskite atitinkamą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-118">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="ab9d6-119">Lauke **Parduotuvės laiko juosta** pasirinkite atitinkamą laiko juostą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-119">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="ab9d6-120">Išplečiamajame sąraše **PVM grupė** pasirinkite atitinkamą parduotuvės PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-120">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="ab9d6-121">Lauke **Valiuta** pasirinkite atitinkamą valiutą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="ab9d6-122">Lauke **Kliento adresų knygelė** nurodykite galiojančią adresų knygelę.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-122">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="ab9d6-123">Lauke **Numatytasis klientas** pateikite galiojantį numatytąjį klientą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-123">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="ab9d6-124">Lauke **Funkcijų šablonas** pasirinkite funkcijų šabloną, jei taikoma.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="ab9d6-125">Lauke **El. paštu siunčiamo pranešimo šablonas** pateikite galiojantį el. siunčiamo pranešimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="ab9d6-126">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ab9d6-127">Toliau pateiktame vaizde parodytas naujo mažmeninės prekybos kanalo kūrimas.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-127">The following image shows the creation of a new retail channel.</span></span>

![Naujas mažmeninės prekybos kanalas](media/channel-setup-retail-1.png)

<span data-ttu-id="ab9d6-129">Toliau pateiktame vaizde parodytas mažmeninės prekybos kanalo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-129">The following image shows an example retail channel.</span></span>

![Mažmeninės prekybos kanalas](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="ab9d6-131">Kiti parametrai</span><span class="sxs-lookup"><span data-stu-id="ab9d6-131">Other settings</span></span>

<span data-ttu-id="ab9d6-132">Yra daug kitų pasirinktinių parametrų, kuriuos galima nustatyti skyriuose **Išrašas / uždarymas** ir **Įvairūs** pagal mažmeninės prekybos parduotuvės poreikius.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-132">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="ab9d6-133">Be to, žr. [Elektroninio kasos aparato (EKA) ekrano maketai](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json), kur pateikta informacijos, kaip nustatyti numatytąjį ekrano maketą skyriuje **Ekrano maketas** ir [„Retail Hardware Station“ konfigūravimas ir diegimas](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation), kur pateikta skyriaus **Aparatūros stotys** sąrankos informacija.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-133">In addition, see [Screen layouts for the point of sale (POS)](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="ab9d6-134">Toliau pateiktame vaizde parodytas mažmeninės prekybos kanalo sąrankos konfigūravimas.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-134">The following image shows an example retail channel setup configuration.</span></span>

![Mažmeninės prekybos kanalo konfigūravimo pavyzdys](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="ab9d6-136">Papildoma kanalų sąranka</span><span class="sxs-lookup"><span data-stu-id="ab9d6-136">Additional channel set up</span></span>

<span data-ttu-id="ab9d6-137">Yra papildomų kanalo elementų, kuriuos reikia nustatyti, juos galima rasti dalyje **Veiksmų sritis** skyriuje **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-137">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="ab9d6-138">Papildomos užduotys, reikalingos interneto kanalo sąrankai, apima mokėjimo metodų, grynųjų pinigų deklaracijų, pristatymo būdų, pajamų / išlaidų sąskaitų, skyrių, vykdymo grupių priskyrimo ir seifų nustatymą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-138">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="ab9d6-139">Šiame vaizde rodomos įvairios papildomos mažmeninės prekybos kanalo nustatymo parinktys skirtuke **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-139">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanalo nustatymas](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="ab9d6-141">Nustatyti mokėjimo būdus</span><span class="sxs-lookup"><span data-stu-id="ab9d6-141">Set up payment methods</span></span>

<span data-ttu-id="ab9d6-142">Norėdami nustatyti kiekvieno mokėjimo tipo, palaikomo šiame kanale, mokėjimo metodus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-142">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="ab9d6-143">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Mokėjimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-143">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="ab9d6-144">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-144">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ab9d6-145">Naršymo srityje pasirinkite pageidaujamą mokėjimo metodą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-145">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="ab9d6-146">Skyriuje **Bendri** nurodykite **Operacijos pavadinimas** ir konfigūruokite kitus pageidaujamus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-146">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="ab9d6-147">Konfigūruokite visus papildomus parametrus, kurių reikia mokėjimo tipui.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-147">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="ab9d6-148">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ab9d6-149">Toliau pateiktame vaizde parodytas mokėjimas grynaisiais pinigais pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-149">The following image shows an example of a cash payment method.</span></span>

![Mokėjimo metodų pavyzdys](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="ab9d6-151">Grynųjų pinigų deklaravimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ab9d6-151">Set up cash declaration</span></span>

1. <span data-ttu-id="ab9d6-152">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Grynųjų pinigų deklaracija**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-152">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="ab9d6-153">Veiksmų **srityje pasirinkite naujas**ir sukurkite visą **taikytiną monetų** ir **pastabų** nominalą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-153">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="ab9d6-154">Toliau pateiktame vaizde parodytas grynųjų pinigų deklaracijos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-154">The following image shows an example of a cash declaration.</span></span>

![Grynųjų pinigų deklaravimo nustatymas](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="ab9d6-156">Nustatyti pristatymo būdus</span><span class="sxs-lookup"><span data-stu-id="ab9d6-156">Set up modes of delivery</span></span>

<span data-ttu-id="ab9d6-157">Galite peržiūrėti sukonfigūruotus pristatymo būdus pasirikdami **Pristatymo būdai** skirtuke **Nustatymas**, esančiame **Veiksmų sritis**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="ab9d6-158">Norėdami pakeisti arba įtraukti pristatymo būdą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-158">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="ab9d6-159">Naršymo srityje eikite į **Moduliai \> Atsargų valdymas \> Pristatymo būdai**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-159">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="ab9d6-160">Veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte naują pristatymo režimą, arba pasirinkite esamą režimą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="ab9d6-161">Skyriuje **Mažmeninės prekybos kanalai** pasirinkite **Įtraukti eilutę**, kad galėtumėte įtraukti kanalą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-161">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="ab9d6-162">Kanalų įtraukimas naudojant organizacijos mazgus, užuot įtraukus kiekvieną kanalą atskirai, gali racionalizuoti kanalų įtraukimą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="ab9d6-163">Toliau pateiktame vaizde parodytas pristatymo būdo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-163">The following image shows an example of a mode of delivery.</span></span>

![Nustatyti pristatymo būdus](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="ab9d6-165">Pajamų/išlaidų sąskaitos nustatymas</span><span class="sxs-lookup"><span data-stu-id="ab9d6-165">Set up income/expense account</span></span>

<span data-ttu-id="ab9d6-166">Norėdami nustatyti produktų pajamų / išlaidų sąskaitą, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-166">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="ab9d6-167">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Pajamų / išlaidų sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-167">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="ab9d6-168">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-168">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ab9d6-169">Dalyje **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-169">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="ab9d6-170">Dalyje **Ieškos pavadinimas** įveskite ieškos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-170">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="ab9d6-171">Dalyje **Sąskaitos tipas** įveskite sąskaitos tipą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-171">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="ab9d6-172">Įveskite tekstą **1 pranešimų eilutė**, **2 pranešimų eilutė**, **1 kvito tekstas** ir **2 kvito tekstas**, kaip reikia.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-172">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="ab9d6-173">Dalyje **Registravimas** įveskite registravimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-173">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="ab9d6-174">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-174">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ab9d6-175">Toliau pateiktame paveiksle parodytas pajamų / išlaidų sąskaitos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-175">The following image shows an example of an income/expense account.</span></span>

![Pajamų / išlaidų sąskaitų nustatymas](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="ab9d6-177">Skyrių nustatymas</span><span class="sxs-lookup"><span data-stu-id="ab9d6-177">Set up sections</span></span>

<span data-ttu-id="ab9d6-178">Norėdami nustatyti skyrius, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-178">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="ab9d6-179">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada spustelėkite **Skyriai**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-179">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="ab9d6-180">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-180">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ab9d6-181">Dalyje **Skyriaus numeris** įveskite skyriaus numerį.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-181">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="ab9d6-182">Dalyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-182">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="ab9d6-183">Dalyje **Skyriaus dydis** įveskite skyriaus dydį.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-183">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="ab9d6-184">Jei reikia, konfigūruokite parametrus **Bendri** ir **Pardavimo statistika**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-184">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="ab9d6-185">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-185">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="ab9d6-186">Vykdymo grupės priskyrimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ab9d6-186">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="ab9d6-187">Norėdami nustatyti vykdymo grupės priskyrimą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-187">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="ab9d6-188">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Vykdymo grupės priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-188">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="ab9d6-189">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-189">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ab9d6-190">Išplečiamajame sąraše **Vykdymo grupė** pasirinkite vykdymo grupę.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-190">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="ab9d6-191">Išplečiamajame sąraše **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-191">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="ab9d6-192">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-192">On the action pane, select **Save**</span></span>

<span data-ttu-id="ab9d6-193">Toliau pateiktame vaizde parodytas vykdymo grupės priskyrimo sąrankos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-193">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Vykdymo grupės priskyrimų nustatymas](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="ab9d6-195">Seifų nustatymas</span><span class="sxs-lookup"><span data-stu-id="ab9d6-195">Set up safes</span></span>

<span data-ttu-id="ab9d6-196">Norėdami nustatyti seifus, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-196">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="ab9d6-197">Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada spustelėkite **Seifai**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-197">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="ab9d6-198">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-198">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ab9d6-199">Įveskite seifo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-199">Enter a name for the safe.</span></span>
1. <span data-ttu-id="ab9d6-200">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ab9d6-200">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab9d6-201">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ab9d6-201">Additional resources</span></span>

[<span data-ttu-id="ab9d6-202">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ab9d6-202">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ab9d6-203">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="ab9d6-203">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="ab9d6-204">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ab9d6-204">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="ab9d6-205">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ab9d6-205">Set up a call center channel</span></span>](channel-setup-callcenter.md)

