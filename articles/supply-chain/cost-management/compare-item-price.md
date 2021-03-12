---
title: Prekių saugojimo kainų palyginimo ataskaita
description: Sužinokite, kaip sugeneruoti prekių saugojimo kainų palyginimo ataskaitą, tada peržiūrėkite ir (arba) eksportuokite rezultatą.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 6554aec1991080f4a14aedb3440ff3dfd32e9b61
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983979"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="28264-103">Prekių saugojimo kainų palyginimo ataskaita</span><span class="sxs-lookup"><span data-stu-id="28264-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28264-104">Šioje temoje paaiškinama, kaip vykdyti **Prekių saugojimo kainų palyginimo** ataskaitą ir nustatyti, kad rezultatas būtų prieinamas skaitmeniniu būdu kaip interaktyvus puslapis „Dynamics 365 Supply Chain Management“ arba kaip eksportuojamas dokumentas bet kuriuo iš kelių formatų.</span><span class="sxs-lookup"><span data-stu-id="28264-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="28264-105">Kai ataskaitą peržiūrite naršyklėje, stulpeliai ir kaupiamieji balansai yra dinamiškai koreguojami atsižvelgiant į jūsų sukonfigūruotą maketą.</span><span class="sxs-lookup"><span data-stu-id="28264-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="28264-106">Galite surikiuoti rezultatus, filtruoti juos, detalizuoti duomenis ir daugiau.</span><span class="sxs-lookup"><span data-stu-id="28264-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="28264-107">Ataskaitų rezultatai saugomi duomenų objekte **Lyginti prekių kainas**, kuris leidžia filtruoti ir eksportuoti rezultatus kitu formatu, pvz., CSV arba „Microsoft Excel“.</span><span class="sxs-lookup"><span data-stu-id="28264-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="28264-108">Ataskaita **Palyginti prekių saugojimo kainas** naudinga tais atvejais, kai rezultatas pateikia daug eilučių.</span><span class="sxs-lookup"><span data-stu-id="28264-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="28264-109">Pavyzdžiui, rezultate gausite daug eilučių, jei yra daugiau nei 40 000 prekių, kurių įkainojimo versijos kaina yra laukianti prekės kaina.</span><span class="sxs-lookup"><span data-stu-id="28264-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="28264-110">Prekių saugojimo kainų palyginimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="28264-110">Enable compare item prices storage</span></span>

<span data-ttu-id="28264-111">Kad galėtumėte naudoti šią funkciją, turite ją įjungti savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="28264-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="28264-112">Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įgalinti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="28264-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="28264-113">Čia funkcija yra nurodyta kaip:</span><span class="sxs-lookup"><span data-stu-id="28264-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="28264-114">**Modulis** – kaštų valdymas</span><span class="sxs-lookup"><span data-stu-id="28264-114">**Module** - Cost management</span></span>
- <span data-ttu-id="28264-115">**Funkcijos pavadinimas** — lyginti prekių saugojimo kainą</span><span class="sxs-lookup"><span data-stu-id="28264-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="28264-116">Generuoti prekių saugojimo kainų palyginimo ataskaitą</span><span class="sxs-lookup"><span data-stu-id="28264-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="28264-117">Atlikite šiuos veiksmus, norėdami sugeneruoti ir išsaugoti ataskaitą **Palyginti prekių saugojimo kainas**:</span><span class="sxs-lookup"><span data-stu-id="28264-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="28264-118">Eikite į **Išlaidų valdymas > Užklausos ir ataskaitos > Iš anksto nustatytos savikainos ataskaitos > Palyginti prekių saugojimo kainas**.</span><span class="sxs-lookup"><span data-stu-id="28264-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="28264-119">Pasirinkite **Naujas**, kad būtų atverta sritis **Palyginti prekių kainas**.</span><span class="sxs-lookup"><span data-stu-id="28264-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="28264-120">Nustatykite šias parinktis, apibrėžiančias, kurias kainas lyginti ataskaitoje:</span><span class="sxs-lookup"><span data-stu-id="28264-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="28264-121">„FastTab“ **Parametrai** suteikite ataskaitai unikalų **Pavadinimą** ir naudodami skyrių **Lyginti laukiančias kainas** ir **Lyginant naudotos kainos** laukus apibrėžkite, kurias kainas ir datas reikia lyginti.</span><span class="sxs-lookup"><span data-stu-id="28264-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="28264-122">„FastTab“ **Įtrauktini įrašai** nustatykite filtrus ir apribojimus, kad apibrėžtumėte, kuriuos duomenis reikia įtraukti į ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="28264-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="28264-123">„FastTab“ **Vykdyti fone** nustatykite, kaip, kada ir kokiu dažnumu norite generuoti ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="28264-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="28264-124">Ši ataskaita visada vykdoma kaip paketinės užduoties dalis.</span><span class="sxs-lookup"><span data-stu-id="28264-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="28264-125">Norėdami pritaikyti nustatymus ir uždaryti sritį, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="28264-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="28264-126">Sukūrus paketinę užduotį, ji bus įtraukta į puslapį **Palyginti prekių saugojimo kainas**.</span><span class="sxs-lookup"><span data-stu-id="28264-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="28264-127">Gali reikėti atnaujinti puslapį, kad matytumėte ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="28264-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="28264-128">Prekių saugojimo kainų palyginimo ataskaitos nagrinėjimas</span><span class="sxs-lookup"><span data-stu-id="28264-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="28264-129">Sukūrę ataskaitą galite ją peržiūrėti ir naršyti bet kuriuo metu:</span><span class="sxs-lookup"><span data-stu-id="28264-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="28264-130">Eikite į **Išlaidų valdymas > Užklausos ir ataskaitos > Iš anksto nustatytos savikainos ataskaitos > Palyginti prekių saugojimo kainas**.</span><span class="sxs-lookup"><span data-stu-id="28264-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="28264-131">Pasirinkti ataskaitą iš sąrašo.</span><span class="sxs-lookup"><span data-stu-id="28264-131">Select a report from the list.</span></span>

1. <span data-ttu-id="28264-132">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="28264-132">Do one of the following:</span></span>

    - <span data-ttu-id="28264-133">Norėdami peržiūrėti ataskaitos rezultatus, pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="28264-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="28264-134">Norėdami gauti išsamesnį ataskaitos rodinį, pasirinkite **Peržiūrėti informaciją**</span><span class="sxs-lookup"><span data-stu-id="28264-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="28264-135">Atsivėrus pasirinktam rodiniui galite atlikti toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="28264-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="28264-136">Pasirinkti beveik bet kurio stulpelio antraštę, kurio reikšmes norite rikiuoti arba filtruoti lentelėje, kaip tai darote su dauguma standartinių „Supply Chain Management“ formų.</span><span class="sxs-lookup"><span data-stu-id="28264-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="28264-137">Įsidėmėkite, kad negalite rikiuoti arba filtruoti stulpelio **Grynasis kainos pokytis %**, nes tai yra apskaičiuotasis laukas.</span><span class="sxs-lookup"><span data-stu-id="28264-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="28264-138">Pasirinkite **Dimensijos rodinys**, kad būtų atidaryta sritis, kurioje galėtumėte pasirinkti, kurį dimensijos stulpelį įterpti į formą.</span><span class="sxs-lookup"><span data-stu-id="28264-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="28264-139">Nustatykite **Įrašyti sąranką** kaip **Taip**, jei norite įrašyti šiuos parametrus, kad jie būtų išsaugoti, kai kitą kartą atidarysite ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="28264-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="28264-140">Norėdami pritaikyti nustatymus ir uždaryti pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="28264-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="28264-141">Pasirinkite bet kurią formos eilutę ir pasirinkite **Peržiūrėti informaciją**, kad pamatytumėte daugiau informacijos apie pasirinktą prekę.</span><span class="sxs-lookup"><span data-stu-id="28264-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="28264-142">Čia galėsite detalizuoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="28264-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="28264-143">Pasirinkite bet kurią formos eilutę ir pasirinkite **Peržiūrėti palyginimo diagramą**, kad matytumėte interaktyvų grafinį rezultatų pateikimą, kaip jie susiję su pasirinkta preke.</span><span class="sxs-lookup"><span data-stu-id="28264-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="28264-144">Šiuos rezultatus galite analizuoti pasirinkdami įvairius grafinius elementus diagramoje ir diagramos legendoje.</span><span class="sxs-lookup"><span data-stu-id="28264-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="28264-145">Pasirinkite bet kurią formos eilutę ir pasirinkite **Peržiūrėti skaičiavimo informaciją**, kad pamatytumėte daugiau informacijos apie skaičiavimus, susijusius su pasirinkta preke.</span><span class="sxs-lookup"><span data-stu-id="28264-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="28264-146">Čia galėsite detalizuoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="28264-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="28264-147">Prekių saugojimo kainų palyginimo ataskaitos eksportavimas</span><span class="sxs-lookup"><span data-stu-id="28264-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="28264-148">Kiekviena sugeneruota ataskaita saugoma duomenų objekte **Palyginti prekių kainas**.</span><span class="sxs-lookup"><span data-stu-id="28264-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="28264-149">Norėdami eksportuoti duomenis iš šio objekto bet kokiu palaikomu duomenų formatu, įskaitant CSV arba „Microsoft Excel“, galite naudoti standartines „Supply Chain Management“ duomenų tvarkymo funkcijas.</span><span class="sxs-lookup"><span data-stu-id="28264-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="28264-150">Toliau pateikiamas pavyzdys, kaip eksportuoti ataskaitą **Palyginti prekių saugojimo kainas**.</span><span class="sxs-lookup"><span data-stu-id="28264-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="28264-151">Eikite į **Sistemos administravimas > Darbo sritys > Duomenų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="28264-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="28264-152">Pasirinkite mygtuką **Eksportuoti**, esantį skyriuje **Duomenų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="28264-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="28264-153">Atidaromas puslapis **Eksportavimas**, kurį naudosite savo eksportavimo užduočiai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="28264-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="28264-154">Pirmiausia turite suteikti savo užduočiai **Grupės pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="28264-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="28264-155">Skyriuje **Pasirinkti objektai** pasirinkite **Įtraukti objektą**, kad būtų atidarytas dialogo langas, kuriame galite nustatyti šias pasirinktis:</span><span class="sxs-lookup"><span data-stu-id="28264-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="28264-156">**Objekto pavadinimas** – pasirinkite **Lyginti prekių kainas**.</span><span class="sxs-lookup"><span data-stu-id="28264-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="28264-157">**Paskirties duomenų formatas** – pasirinkite formatą, kuriuo norite eksportuoti.</span><span class="sxs-lookup"><span data-stu-id="28264-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="28264-158">Norėdami pridėti naują eilutę pasirinkite **Įtraukti**, tada pasirinkite **Uždaryti**, kad uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="28264-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="28264-159">Paprastai vienu metu eksportuojate vieną ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="28264-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="28264-160">Norėdami tai padaryti, eilutei, kurią ką tik įtraukėte į sritį **Užklausa**, nustatykite **Filtras**.</span><span class="sxs-lookup"><span data-stu-id="28264-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="28264-161">Tai leis jums nurodyti, kurias ataskaitas iš objekto **Lyginti prekių kainas** norite įtraukti į eksportą.</span><span class="sxs-lookup"><span data-stu-id="28264-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="28264-162">Nustatykite šias filtro pasirinktis vienai ataskaitai eksportuoti:</span><span class="sxs-lookup"><span data-stu-id="28264-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="28264-163">Skirtuke **Diapazonas** pasirinkite **Įtraukti**, kad įtrauktumėte naują eilutę.</span><span class="sxs-lookup"><span data-stu-id="28264-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="28264-164">Nustatykite **Lentelė** reikšmę kaip **Lyginti prekių kainas**.</span><span class="sxs-lookup"><span data-stu-id="28264-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="28264-165">Nustatykite **Išvestinė lentelė** reikšmę kaip **Lyginti prekių kainas**.</span><span class="sxs-lookup"><span data-stu-id="28264-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="28264-166">Nustatykite **Laukas** reikšmę kaip lauką, pagal kurį norite filtruoti.</span><span class="sxs-lookup"><span data-stu-id="28264-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="28264-167">Paprastai naudosite **Vykdymo pavadinimas** arba **Vykdymo laikas**.</span><span class="sxs-lookup"><span data-stu-id="28264-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="28264-168">Nustatykite **Kriterijus** reikšmę kaip pasirinkto lauko, kurio norite ieškoti, reikšmę (arba ataskaitos pavadinimas, arba laikas, kada ataskaita buvo sugeneruota).</span><span class="sxs-lookup"><span data-stu-id="28264-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="28264-169">Jei reikia, įtraukite daugiau eilučių į lentelę **Diapazonas**, kol gausite tiksliai tokią unikalią ataskaitą, kokios reikėjo.</span><span class="sxs-lookup"><span data-stu-id="28264-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="28264-170">Norėdami išsaugoti nustatymus ir uždaryti pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="28264-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="28264-171">Pasirinkite **Įrašyti**, kad įrašytumėte eksporto sąranką.</span><span class="sxs-lookup"><span data-stu-id="28264-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="28264-172">Atidarykite skirtuką **Eksportavimo parinktys** ir pasirinkite **Eksportuoti dabar**, kad būtų sugeneruotas eksporto failas.</span><span class="sxs-lookup"><span data-stu-id="28264-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="28264-173">Atidaromas puslapis **Vykdymo suvestinė**, kuriame galite matyti savo eksportavimo užduoties būseną ir eksportuotų objektų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="28264-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="28264-174">Pasirinkite objektą **Lyginti prekių kainas**, esantį srityje **Objekto apdorojimo būsena**, tada pasirinkite **Atsisiųsti failą**, kad atsisiųstumėte iš to objekto eksportuotus duomenis.</span><span class="sxs-lookup"><span data-stu-id="28264-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="28264-175">Norėdami gauti daugiau informacijos apie tai, kaip naudoti duomenų valdymo funkciją duomenims eksportuoti, žr. [Duomenų importavimo ir eksportavimo užduočių apžvalga](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="28264-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
