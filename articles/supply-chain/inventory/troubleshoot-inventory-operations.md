---
title: Atsargų operacijų trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti klaidas, su kuriomis galite susidurti dirbdami su atsargų operacijomis.
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 24e41e35b3e810c509a16b91fffd1e796ab9d134
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832063"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="14bcf-103">Atsargų operacijų trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="14bcf-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14bcf-104">Šioje temoje aprašoma, kaip ištaisyti klaidas, su kuriomis galite susidurti dirbdami su atsargų operacijomis.</span><span class="sxs-lookup"><span data-stu-id="14bcf-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="14bcf-105">Nerandu atsargų žurnalų išplečiamojo dialogo lango „Darbo eiga”.</span><span class="sxs-lookup"><span data-stu-id="14bcf-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="14bcf-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="14bcf-106">Issue description</span></span>

<span data-ttu-id="14bcf-107">Nerandate išplečiamojo dialogo lango **Darbo eiga** žurnalo puslapyje arba susijusios darbo eigos operacijos negalimos.</span><span class="sxs-lookup"><span data-stu-id="14bcf-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="14bcf-108">Ši problema gali atsirasti dėl trijų priežasčių, pateikiamų šiuose poskyriuose.</span><span class="sxs-lookup"><span data-stu-id="14bcf-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="14bcf-109">Problemos sprendimo būdas Nr. 1</span><span class="sxs-lookup"><span data-stu-id="14bcf-109">Issue resolution 1</span></span>

<span data-ttu-id="14bcf-110">Jei su problema susiduria visi vartotojai, tikėtina, kad ji kartojasi, nes darbo eigos patvirtinimas nebuvo priskirtas žurnalo pavadinime.</span><span class="sxs-lookup"><span data-stu-id="14bcf-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="14bcf-111">Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="14bcf-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="14bcf-112">Eikite į **Atsargų valdymas &gt; Sąranka &gt; Žurnalo pavadinimai &gt; Atsargos**.</span><span class="sxs-lookup"><span data-stu-id="14bcf-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="14bcf-113">Sąrašo srityje pasirinkite žurnalo pavadinimą, kad atidarytumėte nustatymus.</span><span class="sxs-lookup"><span data-stu-id="14bcf-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="14bcf-114">**Bendras** „FastTab“ skirtuke nustatykite **Patvirtinimo darbo eiga** parinktį į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="14bcf-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="14bcf-115">Jei atsirado pranešimas, raginantis patvirtinti pakeitimą, pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="14bcf-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="14bcf-116">Lauke **Darbo eiga** lauke pasirinkite darbo eigą, kurią norite naudoti pasirinktam žurnalo pavadinimui.</span><span class="sxs-lookup"><span data-stu-id="14bcf-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="14bcf-117">Problemos sprendimo būdas Nr. 2</span><span class="sxs-lookup"><span data-stu-id="14bcf-117">Issue resolution 2</span></span>

<span data-ttu-id="14bcf-118">Jei jūsų darbo eigoje naudojamas pritaikytas kodas, atnaujinus sistemą, gali kilti problemų.</span><span class="sxs-lookup"><span data-stu-id="14bcf-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="14bcf-119">Pavyzdžiui, žurnalo darbo eigoje mygtukas **Pateikti** gali būti neaktyvus, kad negalėtumėte jo paspausti pateikimui patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="14bcf-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="14bcf-120">Jeigu mygtukas **Pateikti** neaktyvus, jūsų darbo eiga gali būti tinkinta, vadinasi, darbo eigos metodas `canSubmitToWorkflow()`  `FormDataUtil`buvo praplėstas.</span><span class="sxs-lookup"><span data-stu-id="14bcf-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="14bcf-121">Norėdami išspręsti šią problemą, pakeiskite būdą, kuriuo praplečiate `canSubmitToWorkflow()`metodą, kad naudotumėte struktūrą pagal šį pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="14bcf-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="14bcf-122">Problemos sprendimo būdas Nr. 3</span><span class="sxs-lookup"><span data-stu-id="14bcf-122">Issue resolution 3</span></span>

<span data-ttu-id="14bcf-123">Jei su problema susiduria tik keli konkretūs vartotojai, tie vartotojai gali neturėti saugos teisių, kurių reikia norint vykdyti darbo eigos operacijas atsargų žurnaluose.</span><span class="sxs-lookup"><span data-stu-id="14bcf-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="14bcf-124">Patikrinkite, ar kiekvienas su problema susidūręs vartotojas turi *Tvarkyti atsargų žurnalo darbo eigą* saugos teisę.</span><span class="sxs-lookup"><span data-stu-id="14bcf-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="14bcf-125">Pagal numatytuosius nustatymus, ši teisė priskiriama pareigai, užvadintai tuo pačiu pavadinimu, ir ši pareiga taikoma *Sandėlio darbuotojas* ir *Sandėlio vadovas* vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="14bcf-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="14bcf-126">Mano atsargų žurnalo būsena – užrakinta sistemoje, o darbo eigos paketinė užduotis neveikia.</span><span class="sxs-lookup"><span data-stu-id="14bcf-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="14bcf-127">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="14bcf-127">Issue description</span></span>

<span data-ttu-id="14bcf-128">Vienas iš jūsų atsargų žurnalų užrakintas dėl tam tikros operacijos ir jis nėra atrakintas.</span><span class="sxs-lookup"><span data-stu-id="14bcf-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="14bcf-129">Pavyzdžiui, jei registruojant įvyksta nežinoma klaida (tai yra sistemos užrakto operacija), žurnalo būsena gali išlikti sistemos užrakinta.</span><span class="sxs-lookup"><span data-stu-id="14bcf-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="14bcf-130">Šiuo atveju darbo eigos darbo elementų apdorojimo programa parodys klaidą, kol tikrins užraktą.</span><span class="sxs-lookup"><span data-stu-id="14bcf-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="14bcf-131">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="14bcf-131">Issue resolution</span></span>

<span data-ttu-id="14bcf-132">Prisijunkite prie „Supply Chain Management” „SQL Server” programos ir patikrinkite, ar **InventJournalTable.SystemBlocked** yra nustatyta *1*.</span><span class="sxs-lookup"><span data-stu-id="14bcf-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="14bcf-133">Jei taip, įsitikinkite, kad žurnalo būsena nebūtų užrakinta, tada iš naujo nustatykite **InventJournalTable.SystemBlocked** *0*.</span><span class="sxs-lookup"><span data-stu-id="14bcf-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="14bcf-134">Mano atsargų žurnalo darbo eiga niekada neužbaigiama ir žurnalo negalima redaguoti ar registruoti.</span><span class="sxs-lookup"><span data-stu-id="14bcf-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="14bcf-135">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="14bcf-135">Issue description</span></span>

<span data-ttu-id="14bcf-136">Kai pateikiate žurnalo patvirtinimo darbo eigą, darbo eigos apdorojimas nustoja reaguoti ir jūs negalite redaguoti ar apdoroti savo žurnalų.</span><span class="sxs-lookup"><span data-stu-id="14bcf-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="14bcf-137">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="14bcf-137">Issue resolution</span></span>

<span data-ttu-id="14bcf-138">Yra kelios priežastys, kodėl gali būti nebaigimas darbo eigos apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="14bcf-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="14bcf-139">Patikrinkite, ar yra šios problemos:</span><span class="sxs-lookup"><span data-stu-id="14bcf-139">Check for the following issues:</span></span>

- <span data-ttu-id="14bcf-140">Eikite į **Atsargų valdymas &gt; Sąranka&gt;Atsargų valdymo darbo eigos** ir peržiūrėkite paveiktos darbo eigos konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="14bcf-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="14bcf-141">Daugiau informacijos žr. [Atsargų žurnalo patvirtinimo darbo eigos](inventory-journal-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="14bcf-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="14bcf-142">Gali įvykti darbo eigos išimtis arba klaida.</span><span class="sxs-lookup"><span data-stu-id="14bcf-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="14bcf-143">Peržiūrėkite paveiktos darbo eigos darbo elementų retrospektyvą ir sužinokite, ar joje yra programos klaida, nutraukusi darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="14bcf-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="14bcf-144">Atsargų žurnalą galima atnaujinti arba redaguoti, tik jei jis patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="14bcf-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="14bcf-145">Jei atšaukimas aktyvus, galite bandyti atšaukti žurnalą.</span><span class="sxs-lookup"><span data-stu-id="14bcf-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="14bcf-146">Darbo eigos paketinės užduoties vykdymas gali būti sustabdytas dėl kelių priežasčių.</span><span class="sxs-lookup"><span data-stu-id="14bcf-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="14bcf-147">Kai kurios iš šių priežasčių galėjo kilti dėl darbo eigos sistemos problemos.</span><span class="sxs-lookup"><span data-stu-id="14bcf-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="14bcf-148">Atsargų žurnalo darbo eigos sąlygos taikomos tik žurnalo, o ne eilutės lygmeniu</span><span class="sxs-lookup"><span data-stu-id="14bcf-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="14bcf-149">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="14bcf-149">Issue description</span></span>

<span data-ttu-id="14bcf-150">Ši problema gali kilti jei, pvz., bandysite išlaidų sumai nustatyti atsargų žurnalo darbo eigos sąlygą.</span><span class="sxs-lookup"><span data-stu-id="14bcf-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="14bcf-151">Nustatykite sąlygą, kad 1-as veiksmas būtų vykdomas tik tada, kai išlaidų suma yra mažesnė nei 100.</span><span class="sxs-lookup"><span data-stu-id="14bcf-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="14bcf-152">Tada nustatykite kitą sąlygą, kad 2-as veiksmas būtų vykdomas tik tada, kai išlaidų suma yra didesnė arba lygi 100.</span><span class="sxs-lookup"><span data-stu-id="14bcf-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="14bcf-153">Tada, kai darbo eiga vykdoma, darbo eigos retrospektyvoje rodoma tik viena eilutė, o pirmoji sąlyga visuomet vertinama kaip *true* nepaisant pateiktosios vertės.</span><span class="sxs-lookup"><span data-stu-id="14bcf-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="14bcf-154">Problemos sprendimas</span><span class="sxs-lookup"><span data-stu-id="14bcf-154">Issue workaround</span></span>

<span data-ttu-id="14bcf-155">Dabartiniame leidime atsargų žurnalo darbo eigos sąlygos taikomos tik žurnalo, o ne eilutės lygmeniu.</span><span class="sxs-lookup"><span data-stu-id="14bcf-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="14bcf-156">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="14bcf-156">This behavior is by design.</span></span> <span data-ttu-id="14bcf-157">Rekomenduojame nustatyti sąlygos kriterijus tik žurnalo lygio atributams.</span><span class="sxs-lookup"><span data-stu-id="14bcf-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="14bcf-158">Turimų atsargų sąrašo puslapio filtravimo sritis nefiltruoja rezultatų, kurių tikiuosi.</span><span class="sxs-lookup"><span data-stu-id="14bcf-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="14bcf-159">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="14bcf-159">Issue description</span></span>

<span data-ttu-id="14bcf-160">Filtro srities filtrai **Turimas sąrašas**  puslapyje nefiltruoja rezultatų, kurių tikitės.</span><span class="sxs-lookup"><span data-stu-id="14bcf-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="14bcf-161">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="14bcf-161">Issue resolution</span></span>

<span data-ttu-id="14bcf-162">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="14bcf-162">This behavior is by design.</span></span>

<span data-ttu-id="14bcf-163">Puslapis  **Turimas sąrašas** sudėliotas iš detalizuotos turimų atsargų lentelės, kurioje pateiktos visos galimos dimensijos.</span><span class="sxs-lookup"><span data-stu-id="14bcf-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="14bcf-164">Nepaisant to, sąrašas šiame puslapyje santrauka.</span><span class="sxs-lookup"><span data-stu-id="14bcf-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="14bcf-165">Dėl to, tai gali apimti eilutes iš šaltinio lentelės apimant vertes pagal rodomas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="14bcf-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="14bcf-166">Filtrai, nustatyti filtrų srityje, taikomi šaltinio lentelei, tačiau ne apibendrintam sąrašui.</span><span class="sxs-lookup"><span data-stu-id="14bcf-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="14bcf-167">Šis veikimas kartais gali lemti netikėtus rezultatus kaip nurodyta [šiuose pavyzdžiuose](inventory-on-hand-list.md#examples).</span><span class="sxs-lookup"><span data-stu-id="14bcf-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="14bcf-168">Tačiau  [tinklelyje pateikti filtrai](inventory-on-hand-list.md#grid-filters) *atlikti*  taikomas apibendrintam sąrašui.</span><span class="sxs-lookup"><span data-stu-id="14bcf-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="14bcf-169">Šie filtrai apima tiek „QuickFilter“ tinklelio viršuje, tiek filtrą kiekvieno stulpelio antraštėje.</span><span class="sxs-lookup"><span data-stu-id="14bcf-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="14bcf-170">Vienetas ir vienetų kiekis atsargų žurnale veikia netinkamai.</span><span class="sxs-lookup"><span data-stu-id="14bcf-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="14bcf-171">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="14bcf-171">Issue description</span></span>

<span data-ttu-id="14bcf-172">Kai dirbate su atsargų žurnalo vienetais ir kiekiais atsargų žurnale, galite susidurti su viena ar abiem problemomis.</span><span class="sxs-lookup"><span data-stu-id="14bcf-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="14bcf-173">Nematote vienetų arba vienetų kiekių atsargų žurnale, kol vienetų konvertavimas nustatytas išleistam produktui, ir negalite pakeisti vieneto atsargų žurnale.</span><span class="sxs-lookup"><span data-stu-id="14bcf-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="14bcf-174">Matote **Kiekis** ir **Vienetas** laukus atsargų žurnale, bet nematote lauko **Vieneto kiekis**.</span><span class="sxs-lookup"><span data-stu-id="14bcf-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="14bcf-175">Jei pakeisite vienetą, įvesite kiekį ir užregistruosite žurnalą, žurnale vis tiek bus rodomas pradinis to kiekio matavimo vienetas.</span><span class="sxs-lookup"><span data-stu-id="14bcf-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="14bcf-176">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="14bcf-176">Issue resolution</span></span>

<span data-ttu-id="14bcf-177">Norėdami ištaisyti šią problemą, vykdykite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="14bcf-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="14bcf-178">Darbo eigoje **Funkcijų valdymas** įsitikinkite, kad funkcija *Matavimo vienetų ir vienetų kiekio naudojimas atsargų žurnaluose* yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="14bcf-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="14bcf-179">Ši funkcija prideda laukus **Vienetas** ir **Vieneto kiekis** į žurnalą.</span><span class="sxs-lookup"><span data-stu-id="14bcf-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="14bcf-180">Įjungus šią funkciją, naudokite laukus **Kiekis**, **Vieneto kiekis** ir **Vienetas** laukus tokiu būdu:</span><span class="sxs-lookup"><span data-stu-id="14bcf-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="14bcf-181">**Kiekis** – nurodykite kiekį, naudodami numatytąjį vienetą, nurodytą išleistam produktui.</span><span class="sxs-lookup"><span data-stu-id="14bcf-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="14bcf-182">Tačiau numatytasis vienetas čia nerodomas.</span><span class="sxs-lookup"><span data-stu-id="14bcf-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="14bcf-183">Jei konvertavimas nustatytas tarp numatytojo vieneto ir vieneto, pasirinkto lauke **Vienetas**, laukas **Kiekis** yra automatiškai atnaujinimas pagal pasirinkimus laukuose **Vieneto kiekis** ir **Vienetas**.</span><span class="sxs-lookup"><span data-stu-id="14bcf-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="14bcf-184">**Vieneto kiekis** – nurodykite kiekį naudodami kiekį, pasirinktą lauke **Vienetas**.</span><span class="sxs-lookup"><span data-stu-id="14bcf-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="14bcf-185">**Vienetas** – pasirinkite vienetą, kurį norite taikyti vertei lauke **Vieneto kiekis**.</span><span class="sxs-lookup"><span data-stu-id="14bcf-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="14bcf-186">Gaunu tokį klaidos pranešimą: „Didžiausias atsargų saugojimo vieneto dešimtainių dalių skaičius yra 0.”</span><span class="sxs-lookup"><span data-stu-id="14bcf-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="14bcf-187">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="14bcf-187">Issue description</span></span>

<span data-ttu-id="14bcf-188">Kai bandote užregistruoti atsargų operaciją arba atsargų rezervavimą, gaunate tokį klaidos pranešimą: „Didžiausias atsargų saugojimo vieneto dešimtainių dalių skaičius yra 0.”</span><span class="sxs-lookup"><span data-stu-id="14bcf-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="14bcf-189">Ši problema kyla tada, kai atsargų operacijos kiekis nurodomas kaip dešimtainė vertė, kuri yra mažesnė už lauke palaikomą tikslumo lygį.</span><span class="sxs-lookup"><span data-stu-id="14bcf-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="14bcf-190">Pavyzdžiui, nurodytas atsargų operacijos *0,5* kiekis, bet tik sveikųjų skaičių kiekiai yra palaikomi.</span><span class="sxs-lookup"><span data-stu-id="14bcf-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="14bcf-191">Todėl vertė turi būti *1* vietoje *0,5*.</span><span class="sxs-lookup"><span data-stu-id="14bcf-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="14bcf-192">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="14bcf-192">Issue resolution</span></span>

1. <span data-ttu-id="14bcf-193">Paleiskite šį scenarijų „SQL Server” programoje, kad suapvalintumėte kiekius atsargų operacijose.</span><span class="sxs-lookup"><span data-stu-id="14bcf-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="14bcf-194">Šis scenarijus pataisys lentelės **inventTrans** vertes.</span><span class="sxs-lookup"><span data-stu-id="14bcf-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="14bcf-195">Paleiskite turimo vientisumo patikrą, kai **taisyti klaidą** parinktis yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="14bcf-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="14bcf-196">Šis patikrinimas ištaisys vertes lentelėje **inventSum**.</span><span class="sxs-lookup"><span data-stu-id="14bcf-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14bcf-197">Itin rekomenduojame, kad atidžiai redaguotumėte scenarijų, kaip to reikalaujama jūsų aplinkoje, atliktumėte testavimą testavimo aplinkoje ir patikrintumėte rezultatų duomenis prieš paleisdami scenarijų gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="14bcf-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]