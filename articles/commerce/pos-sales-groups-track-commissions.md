---
title: Elektroninio kasos aparato (EKA) komisinių sekimas naudojant pardavimo grupes
description: Mažmeninėje prekyboje įprasta sekti pardavimus pagal su klientu dirbusį atstovą, kuris teikė pagalbą, atliko papildomą pardavimą, kryžminį pardavimą ir operacijos apdorojimą.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: afbf69c072ae205e973203d97a5fbca7504ae04f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023468"
---
# <a name="track-commissions-in-the-point-of-sale-pos-by-using-sales-groups"></a><span data-ttu-id="ceda8-103">Elektroninio kasos aparato (EKA) komisinių sekimas naudojant pardavimo grupes</span><span class="sxs-lookup"><span data-stu-id="ceda8-103">Track commissions in the point of sale (POS) by using sales groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ceda8-104">Mažmeninėje prekyboje įprasta sekti pardavimus pagal su klientu dirbusį atstovą, kuris teikė pagalbą, atliko papildomą pardavimą, kryžminį pardavimą ir operacijos apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="ceda8-104">It's a common retail practice to track sales by the associate who worked with the customer by—providing assistance, up-selling, cross-selling, and processing the transaction.</span></span>

<span data-ttu-id="ceda8-105">Sekant pardavimo atstovo pardavimus matuojamos atstovo pardavimo galimybės, o iš kasininko pardavimų galima spręsti apie greitį ir našumą.</span><span class="sxs-lookup"><span data-stu-id="ceda8-105">Tracking sales by sales representative is a measure of the associates selling abilities, while sales by cashier is a measure of speed and efficiency.</span></span> <span data-ttu-id="ceda8-106">Pardavimo atstovo sekami pardavimai taip pat dažnai naudojami norint apskaičiuoti komisinius arba kitas paskatas.</span><span class="sxs-lookup"><span data-stu-id="ceda8-106">Sales tracked by sales representative are also often used to calculate commissions or other incentives.</span></span>

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a><span data-ttu-id="ceda8-107">Darbuotojo konfigūravimas būti EKA pardavimo atstovu</span><span class="sxs-lookup"><span data-stu-id="ceda8-107">Configuring a worker to be a sales representative in POS</span></span>

<span data-ttu-id="ceda8-108">Kai darbuotojas įtraukiamas į pardavimo grupę, jam gali būti paskiriami komisiniai ir sistemoje jis gali būti identifikuojamas kaip pardavimo atstovas.</span><span class="sxs-lookup"><span data-stu-id="ceda8-108">When a worker is added to a sales group, they become eligible for commission and can be identified as a sales representative in the system.</span></span> <span data-ttu-id="ceda8-109">Darbuotojui, kuris nėra pardavimo grupėje, komisiniai negali būti skiriami ir jis nebus įtraukiamas į elektroninio kasos aparato (EKA) programos sąrašus kaip pardavimo atstovas.</span><span class="sxs-lookup"><span data-stu-id="ceda8-109">A worker who isn't in a sales group isn't eligible for commission and won't be listed as a sales representative in the point of sale (POS) application.</span></span> <span data-ttu-id="ceda8-110">EKA pardavimo atstovų sąrašai sudaromi iš visų pardavimo grupių, kuriose yra bent vienas parduotuvei priskirtas darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="ceda8-110">In POS, the list of sales representatives is derived from all sales groups that contain at least one worker assigned to the store.</span></span> <span data-ttu-id="ceda8-111">Sąrašas rodomas EKA kaip pardavimo grupės ID ir pavadinimo (ID : Pavadinimas) derinys.</span><span class="sxs-lookup"><span data-stu-id="ceda8-111">The list is shown in POS as a combination of Sales group ID and Name (ID : Name).</span></span> <span data-ttu-id="ceda8-112">Numatytąją pardavimo grupę darbuotojams galima priskirti norint, kad būtų palaikomi scenarijai, kai mažmenininkas nusprendžia pardavimo atstovą nustatyti automatiškai EKA eilutėse.</span><span class="sxs-lookup"><span data-stu-id="ceda8-112">A default sales group can be assigned to workers to support scenarios where the retailer chooses to set the sales representative on POS lines automatically.</span></span> <span data-ttu-id="ceda8-113">Vartotojai gali pasirinkti bet kurią pardavimo grupę, kurioje darbuotojas yra narys.</span><span class="sxs-lookup"><span data-stu-id="ceda8-113">Users can select from any sales group that the worker is a member of.</span></span>

## <a name="functionality-profile-settings"></a><span data-ttu-id="ceda8-114">Funkcijų šablono parametrai</span><span class="sxs-lookup"><span data-stu-id="ceda8-114">Functionality profile settings</span></span>

<span data-ttu-id="ceda8-115">Yra keletas parduotuvės funkcijų šablono parametrų, kuriuos naudojant nustatomas EKA srautas ir procesas ir kurie skirti pardavimo atstovams.</span><span class="sxs-lookup"><span data-stu-id="ceda8-115">There are a number of functionality profile settings for a store that will determine the flow and process in POS that involve sales representatives.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ceda8-116">Šablonas</span><span class="sxs-lookup"><span data-stu-id="ceda8-116">Profile</span></span></th>
<th><span data-ttu-id="ceda8-117">aprašymas</span><span class="sxs-lookup"><span data-stu-id="ceda8-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ceda8-118">Pagal numatytuosius nustatymus nustatyti kasininką, kai įmanoma</span><span class="sxs-lookup"><span data-stu-id="ceda8-118">Default to cashier when available</span></span></td>
<td><span data-ttu-id="ceda8-119">Jei ši parinktis įjungta, EKA automatiškai sukuria operacijų eilutes, kuriose nurodoma dabartinio kasininko numatytoji pardavimo grupė.</span><span class="sxs-lookup"><span data-stu-id="ceda8-119">If this option is enabled, POS will automatically populate transaction lines with the current cashier's default sales group.</span></span> <span data-ttu-id="ceda8-120">Jei numatytoji kasininko pardavimo grupė nenurodyta, vertė nenustatoma.</span><span class="sxs-lookup"><span data-stu-id="ceda8-120">If a cashier doesn't have a default sales group specified, the value won't be set.</span></span> <span data-ttu-id="ceda8-121">Vartotojas vis tiek gali pats nustatyti pardavimo grupę naudodamas EKA mygtukyno mygtuką.</span><span class="sxs-lookup"><span data-stu-id="ceda8-121">A user could still manually set the sales group by using a POS button grid button.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ceda8-122">Raginimas nurodyti pardavimo atstovą</span><span class="sxs-lookup"><span data-stu-id="ceda8-122">Prompt for sales representative</span></span></td>
<td><span data-ttu-id="ceda8-123">Galimos trys šios parinkties vertės:</span><span class="sxs-lookup"><span data-stu-id="ceda8-123">This option has three possible values:</span></span>
<ul>
<li><span data-ttu-id="ceda8-124"><strong>Ne</strong> – pasirinkus šią parinktį vartotojas nebus raginamas pasirinkti pardavimo grupės.</span><span class="sxs-lookup"><span data-stu-id="ceda8-124"><strong>No</strong> – If this option is selected, the user won't be prompted to select a sales group.</span></span> <span data-ttu-id="ceda8-125">Vertę vis tiek galima nustatyti naudojant numatytąją kasininko pardavimo grupę („Sales“) arba mechaniškai naudojant EKA mygtukyno mygtuką.</span><span class="sxs-lookup"><span data-stu-id="ceda8-125">The value could still be set by using a cashier's default Sales group or manually by using a POS button grid button.</span></span></li>
<li><span data-ttu-id="ceda8-126"><strong>Operacijos pradžia</strong> – jeigu pasirinkta ši parinktis ir arba neįjungta parinktis <strong>Pagal numatytuosius nustatymus nustatyti kasininką</strong>, arba dabartiniam kasininkui nepriskirta numatytoji pardavimo grupė, kiekvienos operacijos pradžioje vartotojas bus paragintas pasirinkti pardavimo grupę.</span><span class="sxs-lookup"><span data-stu-id="ceda8-126"><strong>Start of transaction</strong> – If this option is selected, and either the <strong>Default to cashier</strong> option isn't enabled or the current cashier doesn't have a default sales group, the user will be prompted to select a sales group at the beginning of each transaction.</span></span> <span data-ttu-id="ceda8-127">Pasirinkus pardavimo grupę pagal šį raginimą visos kitos pasirinktos pardavimo grupės eilutės bus numatytosios.</span><span class="sxs-lookup"><span data-stu-id="ceda8-127">Selecting a sales group from this prompt will default all subsequent lines to the selected sales group.</span></span> <span data-ttu-id="ceda8-128">Vartotojas vis tiek gali pats nustatyti pardavimo grupę naudodamas EKA mygtukyno mygtuką.</span><span class="sxs-lookup"><span data-stu-id="ceda8-128">A user could still manually set the sales group by using a POS button grid button.</span></span></li>
<li><span data-ttu-id="ceda8-129"><strong>Kiekvienai eilutei</strong> – jeigu pasirinkta ši parinktis ir arba neįjungta parinktis <strong>Pagal numatytuosius nustatymus nustatyti kasininką</strong>, arba dabartiniam kasininkui nepriskirta numatytoji pardavimo grupė, įtraukęs kiekvieną eilutę vartotojas bus paragintas pasirinkti pardavimo grupę.</span><span class="sxs-lookup"><span data-stu-id="ceda8-129"><strong>For each line</strong> – If this option is selected, and either the <strong>Default to cashier</strong> option isn't enabled or the current cashier doesn't have a default sales group, the user will be prompted to select a sales group after adding each line.</span></span> <span data-ttu-id="ceda8-130">Vartotojas vis tiek gali pats nustatyti pardavimo grupę („Sales“) naudodamas EKA mygtukyno mygtuką.</span><span class="sxs-lookup"><span data-stu-id="ceda8-130">A user could still manually set the Sales group by using a POS button grid button.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ceda8-131">Reikia</span><span class="sxs-lookup"><span data-stu-id="ceda8-131">Require</span></span></td>
<td><span data-ttu-id="ceda8-132">Ši parinktis taikoma tik tada, kai sukonfigūruota, jog EKA ragintų nurodyti pardavimo atstovą.</span><span class="sxs-lookup"><span data-stu-id="ceda8-132">This option is only applicable when POS is configured to prompt for a sales representative.</span></span> <span data-ttu-id="ceda8-133">Jei parinktis įjungta, norėdamas tęsti vartotojas turės pasirinkti pardavimo grupę.</span><span class="sxs-lookup"><span data-stu-id="ceda8-133">If enabled, the user will be required to choose a sales group before continuing.</span></span> <span data-ttu-id="ceda8-134">Priešingu atveju vartotojas paraginamas, bet gali atšaukti ir tęsti nepasirinkęs.</span><span class="sxs-lookup"><span data-stu-id="ceda8-134">Otherwise, the user will be prompted, but can cancel and continue without making a selection.</span></span> <span data-ttu-id="ceda8-135">Įtraukus eilutę reikiamą kiekį leidimų turintis vartotojas vis tiek gali pašalinti pardavimo grupę iš eilutės.</span><span class="sxs-lookup"><span data-stu-id="ceda8-135">After the line is added, a user with sufficient permissions could still remove the sales group from the line.</span></span> <span data-ttu-id="ceda8-136">Šiuo atveju parinktis „Prašyti pardavimo atstovo“ nėra priverstinė.</span><span class="sxs-lookup"><span data-stu-id="ceda8-136">"Require sales representative" is not enforced in this situation.</span></span></td>
</tr>
</tbody>
</table>

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a><span data-ttu-id="ceda8-137">Informacijos apie pardavimo atstovą rodymas EKA operacijų ekrane</span><span class="sxs-lookup"><span data-stu-id="ceda8-137">Displaying the Sales representative information on the POS transactions screen</span></span>

<span data-ttu-id="ceda8-138">EKA operacijos ekraną ir turinį galima konfigūruoti naudojant ekrano išdėstymo kūrimo priemonę ir priskirti ekrano išdėstymus parduotuvėms, registrams arba darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="ceda8-138">The POS transaction screen layout and contents are configurable using the screen layout designer and assigned screen layouts to stores, registers, or workers.</span></span><span data-ttu-id="ceda8-139">Lauką **Pardavimo atstovas** galima įtraukti į Kvitų srities skirtuką Eilutės.</span><span class="sxs-lookup"><span data-stu-id="ceda8-139"> The **Sales representative** field can be added to the Lines tab of the Receipt pane.</span></span><span data-ttu-id="ceda8-140">Taip bus rodomas kiekvienos operacijos ekrano eilutės nurodytos pardavimo grupės ID.</span><span class="sxs-lookup"><span data-stu-id="ceda8-140">  This will display the ID of the specified Sales group for each line on the transaction screen.</span></span>

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a><span data-ttu-id="ceda8-141">Pardavimo atstovo operacijų įtraukimas į EKA mygtukynus</span><span class="sxs-lookup"><span data-stu-id="ceda8-141">Adding Sales representative operations to POS button grids</span></span>

<span data-ttu-id="ceda8-142">Naudodamiesi EKA vartotojai gali konfigūruoti į ekrano išdėstymus įtraukiamus mygtukynus, kad juose būtų pateikiama prieiga prie EKA operacijų.</span><span class="sxs-lookup"><span data-stu-id="ceda8-142">POS allows users to configure button grids, which are included in screen layouts to provide access to POS operations.</span></span> <span data-ttu-id="ceda8-143">Toliau nurodytas EKA operacijas galima priskirti pardavimo atstovams skirtiems mygtukyno mygtukams.</span><span class="sxs-lookup"><span data-stu-id="ceda8-143">The following POS operations can be assigned to button grid buttons that pertain to Sales representatives.</span></span>

| <span data-ttu-id="ceda8-144">Operacija</span><span class="sxs-lookup"><span data-stu-id="ceda8-144">Operation</span></span>                                 | <span data-ttu-id="ceda8-145">aprašymas</span><span class="sxs-lookup"><span data-stu-id="ceda8-145">Description</span></span> |
|-------------------------------------------|-------------|
| <span data-ttu-id="ceda8-146">Nustatyti pardavimo atstovą eilutėje</span><span class="sxs-lookup"><span data-stu-id="ceda8-146">Set sales representative on line</span></span>          | <span data-ttu-id="ceda8-147">EKA operacijoje rodomas tinkamų parduotuvės pardavimo grupių (ID : Pavadinimas) sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ceda8-147">This POS operation displays a list of eligible Sales groups (ID : Name) for the store.</span></span><span data-ttu-id="ceda8-148">Šiame sąraše pasirinkus pardavimo grupę („Sales“) nustatoma dabartinės operacijos eilutės vertė.</span><span class="sxs-lookup"><span data-stu-id="ceda8-148"> Selecting a Sales group from this list will set the value on the current transaction line.</span></span> |
| <span data-ttu-id="ceda8-149">Išvalyti pardavimo atstovą eilutėje</span><span class="sxs-lookup"><span data-stu-id="ceda8-149">Clear sales representative on line</span></span>        | <span data-ttu-id="ceda8-150">Atliekant šią EKA operaciją iš dabartinės operacijos eilutės pašalinama dabartinė pardavimo grupės („Sales“) vertė.</span><span class="sxs-lookup"><span data-stu-id="ceda8-150">This POS operation removes the current Sales group value from the current transaction line.</span></span> |
| <span data-ttu-id="ceda8-151">Nustatyti operacijos pardavimo atstovą</span><span class="sxs-lookup"><span data-stu-id="ceda8-151">Set sales representative on transaction</span></span>   | <span data-ttu-id="ceda8-152">EKA operacijoje rodomas tinkamų parduotuvės pardavimo grupių (ID : Pavadinimas) sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ceda8-152">This POS operation displays a list of eligible Sales groups (ID : Name) for the store.</span></span><span data-ttu-id="ceda8-153">Šiame sąraše pasirinkus pardavimo grupę („Sales“) nustatoma numatytoji dabartinės operacijos vertė.</span><span class="sxs-lookup"><span data-stu-id="ceda8-153"> Selecting a Sales group from this list will set the default value on the current transaction.</span></span> <span data-ttu-id="ceda8-154">Nustatomos visos esamos eilutės, kurioms nepriskirta pardavimo grupė, taip pat visos vėliau įtrauktos eilutės.</span><span class="sxs-lookup"><span data-stu-id="ceda8-154">Any existing lines without a sales group assigned will be set, as well as any subsequently added lines.</span></span> |
| <span data-ttu-id="ceda8-155">Išvalyti operacijos pardavimo atstovą</span><span class="sxs-lookup"><span data-stu-id="ceda8-155">Clear sales representative on transaction</span></span> | <span data-ttu-id="ceda8-156">Atliekant šią EKA operaciją iš dabartinės operacijos pašalinama dabartinė numatytoji pardavimo grupės („Sales“) vertė.</span><span class="sxs-lookup"><span data-stu-id="ceda8-156">This POS operation removes the current default Sales group value from the current transaction.</span></span> <span data-ttu-id="ceda8-157">Tai neturi įtakos kitoms jau esamoms operacijos eilutėms.</span><span class="sxs-lookup"><span data-stu-id="ceda8-157">It does not impact any lines already existing in the transaction.</span></span> |

## <a name="calculating-commissions"></a><span data-ttu-id="ceda8-158">Komisinių skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="ceda8-158">Calculating commissions</span></span>

<span data-ttu-id="ceda8-159">Nurodytų pardavimo grupių darbuotojų komisiniai skaičiuojami registruojant išrašą arba pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ceda8-159">Commission is calculated for the workers in the specified sales groups at the time of statement posting or sales order posting.</span></span><span data-ttu-id="ceda8-160">Komisinių suma nustatoma pagal pardavimo grupėje nurodytą darbuotojo komisinių dalį ir susijusius klientui ir (arba) operacijos produktams taikomus komisinių skaičiavimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="ceda8-160"> The commission amount is determined based on the worker's commission share, as defined in the sales group and the associated commission calculation settings for the customer and/or products on the transaction.</span></span>