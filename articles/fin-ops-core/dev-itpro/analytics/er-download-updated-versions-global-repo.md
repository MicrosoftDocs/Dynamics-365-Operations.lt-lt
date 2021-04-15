---
title: Atnaujintų ER konfigūracijų versijų naujinimas
description: Šioje temoje paaiškinama, kaip importuoti elektroninių ataskaitų (ER) konfigūracijų atnaujintas versijas iš konfigūravimo tarnybos bendrosios saugyklos.
author: NickSelin
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 1e021105c19273db5ded7cb0902eca1d502ced8e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753365"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="724bd-103">Atnaujintų ER konfigūracijų versijų naujinimas</span><span class="sxs-lookup"><span data-stu-id="724bd-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="724bd-104">Elektroninių ataskaitų (ER) [saugyklos ](general-electronic-reporting.md#Repository) naudojamos norint bendrinti [ER konfigūracijas](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="724bd-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="724bd-105">Galite [importuoti](download-electronic-reporting-configuration-lcs.md) ER konfigūracijas iš skirtingų saugyklų į jūsų „Microsoft Dynamics 365 Finance” programą.</span><span class="sxs-lookup"><span data-stu-id="724bd-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="724bd-106">Importuojant ER konfigūracijas, [konfigūracijos teikėjai](general-electronic-reporting.md#Provider) gali publikuoti naujas [versijų](general-electronic-reporting.md#component-versioning) saugyklas, kad jas būtų galima bendrinti.</span><span class="sxs-lookup"><span data-stu-id="724bd-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="724bd-107">Šioje temoje paaiškinama, kaip importuoti ER konfigūracijų atnaujintas versijas iš konfigūravimo tarnybos bendrosios saugyklos.</span><span class="sxs-lookup"><span data-stu-id="724bd-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="724bd-108">Norėdami gauti daugiau informacijos, žr. [„Microsoft Dynamics 365 for Finance and Operations“ – „Regulatory Services“, konfigūravimo tarnybą](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="724bd-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="724bd-109">Galimų atnaujintų versijų peržiūra</span><span class="sxs-lookup"><span data-stu-id="724bd-109">Review the available updated versions</span></span>

1. <span data-ttu-id="724bd-110">Prisijunkite prie „Finance“ naudodami vieną iš tolesnių vaidmenų:</span><span class="sxs-lookup"><span data-stu-id="724bd-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="724bd-111">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="724bd-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="724bd-112">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="724bd-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="724bd-113">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="724bd-113">System administrator</span></span>

2. <span data-ttu-id="724bd-114">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="724bd-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="724bd-115">**Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Importuoti konfigūracijų versijų naujinimus**.</span><span class="sxs-lookup"><span data-stu-id="724bd-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![Lokalizavimo konfigūravimo puslapis](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="724bd-117">Dialogo lange **Importuoti elektroninių ataskaitų konfigūracijos versijų naujinimus** **Leidimo režimas** pasirinkite **Rodyti tik galimus naujinimus**.</span><span class="sxs-lookup"><span data-stu-id="724bd-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="724bd-118">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="724bd-118">Then select **OK**.</span></span> 

    ![Vykdymo režimo laukas nustatytas į „Rodyti tik galimus naujinimus”](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="724bd-120">Peržiūrėti gaunamus pranešimus.</span><span class="sxs-lookup"><span data-stu-id="724bd-120">Review the messages that you receive.</span></span> <span data-ttu-id="724bd-121">Šiuose pranešimuose pateikiama toliau nurodyta informacija apie ER konfigūracijas dabartinėje „Finance” programoje ir kuo jos panašios į bendros saugyklos turinį:</span><span class="sxs-lookup"><span data-stu-id="724bd-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="724bd-122">Bendras ER konfigūracijų skaičius</span><span class="sxs-lookup"><span data-stu-id="724bd-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="724bd-123">ER konfigūracijos, kurių nėra bendroje saugykloje</span><span class="sxs-lookup"><span data-stu-id="724bd-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="724bd-124">ER konfigūracijos, kurių naujausia versija jau prieinama dabartinėje „Finance” programoje (Norėdami peržiūrėti išsamų ER konfigūracijų sąrašą, pasirinkite **Pranešimų išsami informacija** .)</span><span class="sxs-lookup"><span data-stu-id="724bd-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![„Naujausios šių konfigūracijų versijos jau importuotos” pranešimas ir pranešimų išsami informacija](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="724bd-126">ER konfigūracijos, kurių naujausia versija jau prieinama Bendroje saugykloje, kuri gali būti importuota dabartinėje „Finance” programoje (Norėdami peržiūrėti išsamų ER konfigūracijų sąrašą, pasirinkite **Pranešimų išsami informacija** saitą.)</span><span class="sxs-lookup"><span data-stu-id="724bd-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![„Galimi naujinimai” pranešimas ir pranešimų išsami informacija](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="724bd-128">Importuokite galimas atnaujintas versijas</span><span class="sxs-lookup"><span data-stu-id="724bd-128">Import available updated versions</span></span>

1. <span data-ttu-id="724bd-129">Prisijunkite prie „Finance“ naudodami vieną iš tolesnių vaidmenų:</span><span class="sxs-lookup"><span data-stu-id="724bd-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="724bd-130">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="724bd-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="724bd-131">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="724bd-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="724bd-132">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="724bd-132">System administrator</span></span>

2. <span data-ttu-id="724bd-133">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="724bd-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="724bd-134">**Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Importuoti konfigūracijų versijų naujinimus**.</span><span class="sxs-lookup"><span data-stu-id="724bd-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="724bd-135">Dialogo lange **Importuoti elektroninių ataskaitų konfigūracijos versijų naujinimus** **Vykdymo režimas** pasirinkite **Importuoti naujausius naujinimus**, kad būtų importuotos naujausios ER konfigūracijos iš Bendrosios saugyklos į dabartinę „Finance” programą.</span><span class="sxs-lookup"><span data-stu-id="724bd-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="724bd-136">Norėdami suplanuoti, kad būtų importuojama paketinė užduotis, **Paleisti fone** „FastTab” skirtuke nustatykite **Paketo apdorojimas** pasirinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="724bd-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="724bd-137">Jei norite periodiškai kartoti importavimą, konfigūruokite reikiamą pasikartojimą.</span><span class="sxs-lookup"><span data-stu-id="724bd-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![Vykdymo režimo laukas nustatytas į „Importuoti naujausius naujinimus”](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="724bd-139">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="724bd-139">Select **OK**.</span></span>
7. <span data-ttu-id="724bd-140">Norėdami sužinoti, kokios konfigūracijų versijos importuotos, atlikite vieną iš šių veiksmų:</span><span class="sxs-lookup"><span data-stu-id="724bd-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="724bd-141">Jei importuosite interaktyviai, o ne naudodami paketinę užduotį, peržiūrėkite gaunamų pranešimų informaciją.</span><span class="sxs-lookup"><span data-stu-id="724bd-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![Pranešimai, gaunami interaktyviojo importavimo vykdymo metu](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="724bd-143">Jei paleidote importavimą paketo režimu, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="724bd-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="724bd-144">Eikite į **Bendra** \> **Užklausos** \> **Paketinės užduotys** \> **Mano paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="724bd-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="724bd-145">Ieškokite ir pasirinkite **Importuoti elektroninės ataskaitos konfigūracijų versijos naujinimus** užduotį, o tada Veiksmų srityje **Paketinė užduotis** skirtuke pasirinkite **Paketinės užduoties istorija**, kad peržiūrėtumėte užduoties istoriją.</span><span class="sxs-lookup"><span data-stu-id="724bd-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="724bd-146">**Paketinės užduoties istorija** puslapyje pasirinkite **Žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="724bd-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="724bd-147">Tada gautame pranešime pasirinkite **Pranešimų išsami informacija** saitą, kad peržiūrėtumėte užduoties žurnalą.</span><span class="sxs-lookup"><span data-stu-id="724bd-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![Užduoties žurnalas](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="724bd-149">Nerekomenduojame, kad suplanuotumėte pasikartojančią paketinę užduotį, kad importuotumėte atnaujintas ER konfigūracijos versijas tiesiogiai iš Bendrosios saugyklos į gamybos aplinką, nes importuotas versijas bus galima iš karto naudoti.</span><span class="sxs-lookup"><span data-stu-id="724bd-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="724bd-150">Užuot tai naudoję, naudokite šį metodą diegti ER konfigūracijų versijas į smėlio dėžės aplinką.</span><span class="sxs-lookup"><span data-stu-id="724bd-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="724bd-151">Tada jos gali būti vertinamos smėlio dėžės aplinkoje prieš jas įdiegiant gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="724bd-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="724bd-152">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="724bd-152">Additional resources</span></span>

- [<span data-ttu-id="724bd-153">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="724bd-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="724bd-154">ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos</span><span class="sxs-lookup"><span data-stu-id="724bd-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]