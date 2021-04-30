---
title: Archyvuoti atsargų operacijas
description: Šioje temoje aprašoma, kaip archyvuoti atsargų operacijų duomenis, kad būtų pagerintas sistemos našumas.
author: sherry-zheng
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: b740da1a8a349f4a1a80b41bf717c388fd3db0c0
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881837"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="13899-103">Archyvuoti atsargų operacijas</span><span class="sxs-lookup"><span data-stu-id="13899-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="13899-104">Laikui bėgant atsargų operacijų lentelė (`InventTrans`) toliau plečiasi ir sunaudoja daugiau duomenų bazės vietos.</span><span class="sxs-lookup"><span data-stu-id="13899-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="13899-105">Todėl dėl lentelės pateiktos užklausos palaipsniui veiks lėčiau.</span><span class="sxs-lookup"><span data-stu-id="13899-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="13899-106">Šioje temoje aprašoma, kaip galima naudoti atsargų operacijų archyvo priemonę *duomenims apie atsargų operacijas archyvuoti* siekiant pagerinti sistemos našumą.</span><span class="sxs-lookup"><span data-stu-id="13899-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="13899-107">Tik finansiškai atnaujintas atsargų operacijas galima suarchyvuoti pasirinktu uždarytu DK laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="13899-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="13899-108">Norint suarchyvuoti, finansiškai atnaujintų siunčiamų atsargų operacijų išdavimo būsena turi būti *Parduota*, o gavimo atsargų operacijų gavimo būsena turi būti *Nupirkta*.</span><span class="sxs-lookup"><span data-stu-id="13899-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="13899-109">Archyvuojant atsargų operacijas, visos susijusios operacijos perkeliamos į lentelę `InventTransArchive`.</span><span class="sxs-lookup"><span data-stu-id="13899-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="13899-110">Atsargų išdavimo ir atsargų gavimo operacijos archyvuojamos atskirai, remiantis prekės ID (`itemId`) ir atsargų dimensijos ID (`inventDimId`) kombinacija, o tada jos pateikiamos į išdavimo ir gavimo operacijų suvestinę.</span><span class="sxs-lookup"><span data-stu-id="13899-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="13899-111">Jei `itemId` ir `inventDimId` kombinacijoje yra tik viena gavimo arba išdavimo operacija, operacija nebus archyvuota.</span><span class="sxs-lookup"><span data-stu-id="13899-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="13899-112">Funkcijos įjungimas sistemoje</span><span class="sxs-lookup"><span data-stu-id="13899-112">Turn on the feature in your system</span></span>

<span data-ttu-id="13899-113">Jei jūsų sistemoje dar nėra funkcijų, aprašytų šioje temoje, eikite į [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir įjunkite funkciją *Atsargų operacijų archyvas*.</span><span class="sxs-lookup"><span data-stu-id="13899-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span> <span data-ttu-id="13899-114">Atkreipkite dėmesį, kad įjungus šią funkciją, jos išjungti nebegalima.</span><span class="sxs-lookup"><span data-stu-id="13899-114">Note that this feature cannot be disabled once it has been enabled.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="13899-115">Dalykai, į kuriuos reikia atsižvelgti archyvuojant atsargų operacijas</span><span class="sxs-lookup"><span data-stu-id="13899-115">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="13899-116">Prieš archyvuojant atsargų operacijas reikia atsižvelgti į šiuos verslo scenarijus, nes juos paveiks operacija:</span><span class="sxs-lookup"><span data-stu-id="13899-116">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="13899-117">Kai audituojate atsargų operacijas iš susijusių dokumentų, pvz., pirkimo užsakymo eilučių, jos bus rodomos kaip suarchyvuotos.</span><span class="sxs-lookup"><span data-stu-id="13899-117">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="13899-118">Norėdami peržiūrėti suarchyvuotas operacijas, turite eiti į **Atsargų valdymas\>Periodinės užduotys \>Valyti \> Atsargų operacijų archyvas**.</span><span class="sxs-lookup"><span data-stu-id="13899-118">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="13899-119">Negalima atšaukti suarchyvuotų laikotarpių atsargų uždarymo.</span><span class="sxs-lookup"><span data-stu-id="13899-119">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="13899-120">Prieš atšaukdami atsargų uždarymą, turite atšaukti atitinkamo laikotarpio atsargų operacijų archyvą.</span><span class="sxs-lookup"><span data-stu-id="13899-120">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="13899-121">Suarchyvuotų laikotarpių standartinių išlaidų konvertuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="13899-121">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="13899-122">Prieš atlikdami standartinį savikainos konvertavimą, turite atšaukti atitinkamo laikotarpio atsargų operacijų archyvą.</span><span class="sxs-lookup"><span data-stu-id="13899-122">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="13899-123">Atsargų ataskaitos, išgaunamos iš atsargų operacijų, bus paveiktos archyvuojant atsargų operacijas.</span><span class="sxs-lookup"><span data-stu-id="13899-123">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="13899-124">Šios ataskaitos apima atsargų skirstymo ataskaitą ir atsargų vertės ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="13899-124">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="13899-125">Atsargų prognozės gali būti paveiktos, jei jos paleidžiamos archyvuotų laikotarpių laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="13899-125">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="13899-126">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="13899-126">Prerequisites</span></span>

<span data-ttu-id="13899-127">Atsargų operacijos gali būti suarchyvuotos tik per laikotarpius, kai tenkinamos šios sąlygos:</span><span class="sxs-lookup"><span data-stu-id="13899-127">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="13899-128">DK laikotarpis turi būti uždarytas.</span><span class="sxs-lookup"><span data-stu-id="13899-128">The ledger period must be closed.</span></span>
- <span data-ttu-id="13899-129">Atsargų uždarymas turi būti vykdomas archyvo dieną arba laikotarpiu po jos.</span><span class="sxs-lookup"><span data-stu-id="13899-129">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="13899-130">Laikotarpis turi būti bent metus prieš archyvo pradžios laikotarpio datą.</span><span class="sxs-lookup"><span data-stu-id="13899-130">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="13899-131">Neturi būti jokių esamų atsargų perskaičiavimų.</span><span class="sxs-lookup"><span data-stu-id="13899-131">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="13899-132">Archyvuoti atsargų operacijas</span><span class="sxs-lookup"><span data-stu-id="13899-132">Archive inventory transactions</span></span>

<span data-ttu-id="13899-133">Norėdami archyvuoti atsargų operacijas, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="13899-133">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="13899-134">Eikite į **Atsargų valdymas** \> **Periodinės užduotys** \> **Valymas** \> **Atsargų operacijų archyvų**.</span><span class="sxs-lookup"><span data-stu-id="13899-134">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="13899-135">Rodomas puslapis **Atsargų operacijų archyvas** bei archyvuotų proceso įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="13899-135">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="13899-136">![Atsargų operacijų archyvo puslapis](media/archive-inventory-empty.png "Atsargų operacijų archyvo puslapis")</span><span class="sxs-lookup"><span data-stu-id="13899-136">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="13899-137">Veiksmų srityje pasirinkite **Atsargų operacijų archyvas**, kad sukurtumėte atsargų operacijų archyvas.</span><span class="sxs-lookup"><span data-stu-id="13899-137">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="13899-138">Dialogo lange **Atsargų operacijų archyvas** „FastTab“ skirtuke **Parametrai** nustatykite šiuos laukelius:</span><span class="sxs-lookup"><span data-stu-id="13899-138">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="13899-139">**Nuo uždarymo DK laikotarpio pradžios datos** – pasirinkite anksčiausią operacijos datą, kuri bus įtraukta į archyvą.</span><span class="sxs-lookup"><span data-stu-id="13899-139">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="13899-140">**Iki uždarymo DK laikotarpio pradžios datos** – pasirinkite vėliausią operacijos datą, kuri bus įtraukta į archyvą.</span><span class="sxs-lookup"><span data-stu-id="13899-140">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="13899-141">![Atsargų operacijų archyvo dialogo langas](media/archive-inventory-dates.png "Atsargų operacijų archyvo dialogo langas")</span><span class="sxs-lookup"><span data-stu-id="13899-141">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="13899-142">Bus galima pasirinkti tik laikotarpius, kurie atitinka [būtinas sąlygas](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="13899-142">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="13899-143">Prireikus, „FastTab“ skirtuke **Vykdyti fone** nustatykite paketinio vykdymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="13899-143">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="13899-144">Atlikite įprastus „Microsoft Dynamics 365 Supply Chain Management“ paketinių užduočių veiksmus.</span><span class="sxs-lookup"><span data-stu-id="13899-144">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="13899-145">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="13899-145">Select **OK**.</span></span>
1. <span data-ttu-id="13899-146">Gaunate pranešimą, kuriuo prašoma patvirtinti, kad norite tęsti.</span><span class="sxs-lookup"><span data-stu-id="13899-146">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="13899-147">Atidžiai perskaitykite pranešimą ir pasirinkite **Taip**, jei norite tęsti.</span><span class="sxs-lookup"><span data-stu-id="13899-147">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="13899-148">Gaunate pranešimą, kuriame teigiama, kad jūsų atsargų operacijų archyvo užduotis buvo įtraukta į paketinių užduočių eilę.</span><span class="sxs-lookup"><span data-stu-id="13899-148">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="13899-149">Dabar užduotis pradės archyvuoti atsargų operacijas nuo pasirinkto laikotarpio.</span><span class="sxs-lookup"><span data-stu-id="13899-149">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="13899-150">Peržiūrėti archyvuotas atsargų operacijas</span><span class="sxs-lookup"><span data-stu-id="13899-150">View archived inventory transactions</span></span>

<span data-ttu-id="13899-151">Puslapyje **Atsargų operacijų archyvas** rodoma visa archyvavimo retrospektyva.</span><span class="sxs-lookup"><span data-stu-id="13899-151">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="13899-152">Kiekvienoje tinklelio eilutėje rodoma tokia informacija kaip archyvo sukūrimo data, jį sukūręs naudotojas ir jo būsena.</span><span class="sxs-lookup"><span data-stu-id="13899-152">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="13899-153">![Atsargų operacijų archyvavimo retrospektyvos puslapis](media/archive-inventory-full.png "Atsargų operacijų archyvavimo retrospektyvos puslapis")</span><span class="sxs-lookup"><span data-stu-id="13899-153">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="13899-154">Norėdami filtruoti tinklelyje rodomus archyvus, puslapio viršuje pateiktame išskleidžiamajame sąraše pasirinkite vieną iš nurodytų verčių:</span><span class="sxs-lookup"><span data-stu-id="13899-154">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="13899-155">**Aktyvūs** – rodyti tik aktyvius archyvus, bet ne atšauktus archyvus.</span><span class="sxs-lookup"><span data-stu-id="13899-155">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="13899-156">**Visi** – rodyti visus archyvus – tiek aktyvius, tiek atšaukus.</span><span class="sxs-lookup"><span data-stu-id="13899-156">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="13899-157">Kiekvienam tinklelio archyvui pateikiama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="13899-157">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="13899-158">**Aktyvus** – varnelė rodo, kad archyvas yra aktyvus.</span><span class="sxs-lookup"><span data-stu-id="13899-158">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="13899-159">**Pradžios data** – seniausios operacijos, kurią galima įtraukti į archyvą, data.</span><span class="sxs-lookup"><span data-stu-id="13899-159">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="13899-160">**Pabaigos data** – naujausios operacijos, kurią galima įtraukti į archyvą, data.</span><span class="sxs-lookup"><span data-stu-id="13899-160">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="13899-161">**Suplanuota** – naudotojo, sukūrusio archyvą, paskyra.</span><span class="sxs-lookup"><span data-stu-id="13899-161">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="13899-162">**Įvykdyta** – archyvo sukūrimo data.</span><span class="sxs-lookup"><span data-stu-id="13899-162">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="13899-163">**Atšauktas** – varnelė rodo, kad archyvas buvo atšauktas.</span><span class="sxs-lookup"><span data-stu-id="13899-163">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="13899-164">**Stabdyti dabartinį atnaujinimą** – varnelė rodo, kad archyvavimas vyksta, bet buvo pristabdytas.</span><span class="sxs-lookup"><span data-stu-id="13899-164">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="13899-165">**Būsena** – archyvo apdorojimo būsena.</span><span class="sxs-lookup"><span data-stu-id="13899-165">**State** – The processing status of the archive.</span></span> <span data-ttu-id="13899-166">Galimos vertės: *Laukiama*, *Vykdoma* ir *Baigta*.</span><span class="sxs-lookup"><span data-stu-id="13899-166">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="13899-167">Įrankių juostoje virš tinklelio yra šie mygtukai, kuriuos galima naudoti darbui su pasirinktu archyvu:</span><span class="sxs-lookup"><span data-stu-id="13899-167">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="13899-168">**Archyvuotos operacijos** – visos pasirinkto archyvo informacijos peržiūra.</span><span class="sxs-lookup"><span data-stu-id="13899-168">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="13899-169">Rodomame puslapyje **Archyvuotos operacijos** rodomos visos archyvo operacijos.</span><span class="sxs-lookup"><span data-stu-id="13899-169">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="13899-170">![Archyvuotų operacijų puslapis](media/archive-inventory-transactions.png "Archyvuotų operacijų puslapis")</span><span class="sxs-lookup"><span data-stu-id="13899-170">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="13899-171">Norėdami peržiūrėti daugiau informacijos apie konkrečias operacijas puslapyje **Archyvuotos operacijos**, pasirinkite tinklelį, o tada, veiksmų srityje pasirinkite **Archyvuotos operacijos duomenys**.</span><span class="sxs-lookup"><span data-stu-id="13899-171">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="13899-172">Rodomame puslapyje **Archyvuotos operacijos duomenys** rodoma tokia informacija kaip DK registravimas, susijusios papildomos DK nuorodos ir finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="13899-172">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="13899-173">**Archyvavimo pristabdymas** – šiuo metu apdorojamo pasirinkto archyvavimo pristabdymas.</span><span class="sxs-lookup"><span data-stu-id="13899-173">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="13899-174">Pristabdymas vykdomas tik sugeneravus archyvavimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="13899-174">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="13899-175">Todėl prieš įsigaliojant pauzei galimas nedidelis uždelsimas.</span><span class="sxs-lookup"><span data-stu-id="13899-175">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="13899-176">Pristabdžius archyvavimą laukelyje **Stabdyti dabartinį atnaujinimą** pasirodo varnelė.</span><span class="sxs-lookup"><span data-stu-id="13899-176">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="13899-177">**Archyvavimo tęsimas** – šiuo metu apdorojamo pasirinkto archyvavimo vykdymo tęsimas.</span><span class="sxs-lookup"><span data-stu-id="13899-177">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="13899-178">**Atšaukti** – pasirinkto archyvavimo atšaukimas.</span><span class="sxs-lookup"><span data-stu-id="13899-178">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="13899-179">Archyvavimą galima atšaukti tik jei jo laukelis **Būsena** nustatytas kaip *Baigta*.</span><span class="sxs-lookup"><span data-stu-id="13899-179">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="13899-180">Atšaukus archyvavimą laukelyje **Atšaukti** pasirodo varnelė.</span><span class="sxs-lookup"><span data-stu-id="13899-180">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
