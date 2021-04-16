---
title: Eksportuoti papildomus duomenis į failus
description: Šioje temoje paaiškinta, kaip paruošti duomenų eksportavimą iš „Microsoft Dynamics 365 Finance“ ir tada importuoti juos į konsoliduotą juridinį asmenį.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: bae0a28c59f327e47378eef6392d5e304bbde9a8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826183"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="213f2-103">Eksportuoti papildomus duomenis į failus</span><span class="sxs-lookup"><span data-stu-id="213f2-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="213f2-104">Naudojate **Eksportuoti** puslapį (**Sistemos administravimas \> Darbo aplinkos \> Importuoti/Eksportuoti**) tam, kad parengtumėte eksportuoti papildomus duomenis į failus, kurie tuomet gali būti importuoti į konsoliduotą juridinį asmenį.</span><span class="sxs-lookup"><span data-stu-id="213f2-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="213f2-105">Dėl daugiau informacijos apie importavimo ir eksportavimo procesus, žr. [Duomenų importavimo ir eksportavimo darbų peržiūra](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="213f2-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="213f2-106">Sukurti juridinį asmenį konsolidavimo procesui.</span><span class="sxs-lookup"><span data-stu-id="213f2-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="213f2-107">Dėl informacijos apie tai, kaip sukurti juridinius asmenis, žr. [Kurti juridinius asmenis](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="213f2-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="213f2-108">Dėl daugiau informacijos, žr. [Parengti juridinį asmenį naudojimui konsolidavimo procese](prepare-company-for-consolidation.md) ir [Nustatyti papildomą juridinį asmenį konsolidavimui](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="213f2-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="213f2-109">Eiktie į **Konsolidavimai \> Eksportuoti įmonių balansus**.</span><span class="sxs-lookup"><span data-stu-id="213f2-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="213f2-110">Puslapyje **Eksportuoti įmonių balansus** skirtuke **Kriterijai** nurodykite išsamią konsolidavimo informaciją nustatydami tolesnius laukelius.</span><span class="sxs-lookup"><span data-stu-id="213f2-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="213f2-111">Laukas</span><span class="sxs-lookup"><span data-stu-id="213f2-111">Field</span></span>                             | <span data-ttu-id="213f2-112">aprašymas</span><span class="sxs-lookup"><span data-stu-id="213f2-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="213f2-113">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="213f2-113">Main account</span></span>                      | <span data-ttu-id="213f2-114">Nustatykite konsoliduotinas sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="213f2-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="213f2-115">Norėdami įtraukti visas sąskaitas, palikite laukelį tuščią.</span><span class="sxs-lookup"><span data-stu-id="213f2-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="213f2-116">Naudokite konsolidavimo sąskaitą</span><span class="sxs-lookup"><span data-stu-id="213f2-116">Use consolidation account</span></span>         | <span data-ttu-id="213f2-117">Jei nustatėte konsolidavimo sąskaitas, nustatykite parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="213f2-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="213f2-118">Pasirinkti konsolidacijos sąskaitą iš</span><span class="sxs-lookup"><span data-stu-id="213f2-118">Select consolidation account from</span></span> | <span data-ttu-id="213f2-119">Rinkitės **Pagrindinę sąskaitą** ar **Konsoliduotos sąskaitos grupę**.</span><span class="sxs-lookup"><span data-stu-id="213f2-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="213f2-120">Konsolidacijos sąskaitų grupė</span><span class="sxs-lookup"><span data-stu-id="213f2-120">Consolidation account group</span></span>       | <span data-ttu-id="213f2-121">Rinkitės konsolidavimo sąskaitos grupę jūsų pasirinktai konsolidavimo sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="213f2-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="213f2-122">Konsolidacijos laikotarpis</span><span class="sxs-lookup"><span data-stu-id="213f2-122">Consolidation period</span></span>              | <span data-ttu-id="213f2-123">Nurodykite „nuo“ ir „iki“ datas konsolidavimui.</span><span class="sxs-lookup"><span data-stu-id="213f2-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="213f2-124">Įtraukti faktines sumas</span><span class="sxs-lookup"><span data-stu-id="213f2-124">Include actual amounts</span></span>            | <span data-ttu-id="213f2-125">Nustatykite parinktį į **Taip** norėdami įtraukti esamas sumas.</span><span class="sxs-lookup"><span data-stu-id="213f2-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="213f2-126">Įtraukti biudžeto sumas</span><span class="sxs-lookup"><span data-stu-id="213f2-126">Include budget amounts</span></span>            | <span data-ttu-id="213f2-127">Nustatykite parinktį į **Taip** norėdami įtraukti biudžeto sumas konsolidavimuose.</span><span class="sxs-lookup"><span data-stu-id="213f2-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="213f2-128">Biudžeto modeliai</span><span class="sxs-lookup"><span data-stu-id="213f2-128">Budget models</span></span>                     | <span data-ttu-id="213f2-129">Nurodykite įtraukiamą biudežto modelį.</span><span class="sxs-lookup"><span data-stu-id="213f2-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="213f2-130">Skirtuke **Finansinės dimensijos**, nurodykite išsamią konsolidavimo informaciją:</span><span class="sxs-lookup"><span data-stu-id="213f2-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="213f2-131">Nurodykite finansinės dimensijos informaciją, kuri turi būti perduodamas iš transakcijos į papildomas sąskaitas į transakcijas konsoliduotame juridiniame asmenyje.</span><span class="sxs-lookup"><span data-stu-id="213f2-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="213f2-132">Rinkitės finansines dimensijas sąraše.</span><span class="sxs-lookup"><span data-stu-id="213f2-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="213f2-133">Nurodykite tinkamą specifikaciją kiekvienai konsoliduotai finansinei dimensijai.</span><span class="sxs-lookup"><span data-stu-id="213f2-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="213f2-134">Esamos parinktys apima **Dimensiją**, **Grupės dimensiją**, **Kompanijos sąskaitas** ir **Paskyrą**.</span><span class="sxs-lookup"><span data-stu-id="213f2-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="213f2-135">Parinktis **Grupės dimensija** leidžia jums nustatyti dimensijos vertę, kurią naudoja konsoliduojama įmonių grupė.</span><span class="sxs-lookup"><span data-stu-id="213f2-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="213f2-136">Nurodykite segmento užsakymą, kuriame konsoliduojate.</span><span class="sxs-lookup"><span data-stu-id="213f2-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="213f2-137">Skirtuke **Juridiniai asmenys**, atlikite šiuos žingsnius, kad nurodytumėte juridinį asmenį, kurį eksportuojate:</span><span class="sxs-lookup"><span data-stu-id="213f2-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="213f2-138">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="213f2-138">Select **New**.</span></span>
    2. <span data-ttu-id="213f2-139">Laukelyje **Šaltinio juridinis asmuo**, įveskite juridinį asmenį.</span><span class="sxs-lookup"><span data-stu-id="213f2-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="213f2-140">Jei tie patys kriterijai taikomi keliems papildiniams, kurie yra toje pačioje duomenų bazėje, galite perduoti duomenis iš tų papildinių į atskirus eksportuojamus failus viena operacija:</span><span class="sxs-lookup"><span data-stu-id="213f2-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="213f2-141">Sukurkite kiekvienam papildomam juridiniam asmeniui eilutę, kuriam sąskaitos turi būti eksportuojamos į failus.</span><span class="sxs-lookup"><span data-stu-id="213f2-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="213f2-142">Šie failai bus importuojami į konsoliduotą juridinį asmenį vėliau.</span><span class="sxs-lookup"><span data-stu-id="213f2-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="213f2-143">Kiekvienam papildiniui įveskite papildinio pavadinimą ir eksportuojamo failo pavadinimą, kuris bus sukuriamas eksportavimo darbo metu.</span><span class="sxs-lookup"><span data-stu-id="213f2-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="213f2-144">Laukelyje **Konvertuojamų skirtumų sąskaitos tipas** laukelyje, rinkitės **Pelnas ir nuostoliai** ar **Balansas**.</span><span class="sxs-lookup"><span data-stu-id="213f2-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="213f2-145">Įveskite pavadinimą eksportuojamam failui, kuris bus sukurtas.</span><span class="sxs-lookup"><span data-stu-id="213f2-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="213f2-146">Rinkitės **Gerai** tam, kad vykdytumėte eksportavimą.</span><span class="sxs-lookup"><span data-stu-id="213f2-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="213f2-147">Užbaigus eksportavimą, gausite pranešimą, kuriame bus rodomas įrašų skaičius, įrašytas į kiekvieną failą.</span><span class="sxs-lookup"><span data-stu-id="213f2-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="213f2-148">Tuomet galite importuoti failus į konsoliduotą juridinį asmenį.</span><span class="sxs-lookup"><span data-stu-id="213f2-148">You can then import the files into the consolidated legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]