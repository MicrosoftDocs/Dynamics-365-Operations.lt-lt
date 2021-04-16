---
title: Programos metaduomenų, kurie bus naudojami RCS ir ER, paruošimas
description: Šioje temoje paaiškinama, kaip paruošti programos metaduomenis, skirtus „Regulatory Configuration Service“ (RCS) ir elektroninėms ataskaitoms (ER).
author: NickSelin
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f0501fd67da0cbc5c10171b55004cb7f4fd4fd16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743708"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a><span data-ttu-id="b8c35-103">Programos metaduomenų, kurie bus naudojami RCS ir ER, paruošimas</span><span class="sxs-lookup"><span data-stu-id="b8c35-103">Prepare application-specific metadata for RCS and ER</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b8c35-104">Šioje temoje pateikiama toliau nurodytų užduočių pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="b8c35-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="b8c35-105">Programos metaduomenų, kuriuos galima naudoti RCS, paruošimas</span><span class="sxs-lookup"><span data-stu-id="b8c35-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="b8c35-106">Prieiga prie programos metaduomenų naudojant ER konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="b8c35-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="b8c35-107">Prieiga prie programos metaduomenų naudojant prijungtas programas</span><span class="sxs-lookup"><span data-stu-id="b8c35-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="b8c35-108">Programos metaduomenų, kuriuos galima naudoti RCS, paruošimas</span><span class="sxs-lookup"><span data-stu-id="b8c35-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="b8c35-109">Toliau pateikta procedūra parodo, kaip vartotojas, turintis vaidmens **Sistemos administratorius** arba **Elektroninės ataskaitos kūrėjas** teises, gali sukurti elektroninės ataskaitos (ER) konfigūraciją, kurioje būtų programos metaduomenys ir kurią naudojant būtų kuriamos ER modelių susiejimo konfigūracijos naudojant „Regulatory Configuration Service“ (RCS).</span><span class="sxs-lookup"><span data-stu-id="b8c35-109">The following procedure shows how a user who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="b8c35-110">Šiame pavyzdyje sukurta ER modelio susiejimo konfigūracija bus naudojama norint pasiekti užsienio prekybos operacijas.</span><span class="sxs-lookup"><span data-stu-id="b8c35-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="b8c35-111">Šiame pavyzdyje jūs norite naudodami RCS sukurti ER sprendimą, skirtą programai, kurį naudojant bus generuojami elektroniniai dokumentai, kuriuose pateikiama informacija iš užsienio prekybos verslo srities.</span><span class="sxs-lookup"><span data-stu-id="b8c35-111">For this example, you want to use RCS to design an ER solution for the application that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="b8c35-112">Norint susieti ER duomenų modelį su reikiamų duomenų šaltiniais, reikia turėti prieigą prie RCS programos metaduomenų.</span><span class="sxs-lookup"><span data-stu-id="b8c35-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata in RCS.</span></span> <span data-ttu-id="b8c35-113">Todėl, norėdami sukurti ER sprendimą, turite sukonfigūruoti naują ER metaduomenų konfigūraciją, kurioje būtų visi metaduomenys, kurių šiuo metu reikia norint generuoti pasirinktos verslo srities ER ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="b8c35-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="b8c35-114">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="b8c35-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="b8c35-115">Eikite į **Organizacijos administravimas \> Darbo sritys \> Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="b8c35-116">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="b8c35-117">Jei nematote šio konfigūracijų teikėjo, atlikite [Konfigūracijų teikėjų kūrimas ir pažymėjimas kaip aktyvių](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedūrą.</span><span class="sxs-lookup"><span data-stu-id="b8c35-117">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="b8c35-118">Pasirinkite **Metaduomenų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="b8c35-119">Pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="b8c35-120">Išplečiamojo dialogo lango lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b8c35-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="b8c35-121">Šiame pavyzdyje įveskite **Užsienio prekybos metaduomenys**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="b8c35-122">Pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="b8c35-123">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-123">Select **Designer**.</span></span>
8. <span data-ttu-id="b8c35-124">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b8c35-125">Galite pasirinkti visus metaduomenis, skirtus visai programai arba skirtus pasirinktiems modeliams ar moduliams.</span><span class="sxs-lookup"><span data-stu-id="b8c35-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="b8c35-126">Atminkite, kad abiem atvejais šie metaduomenys bus įtraukti automatiškai: įrašų lentelės, išvardijimai ir išplėstiniai duomenų tipai (EDT).</span><span class="sxs-lookup"><span data-stu-id="b8c35-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="b8c35-127">Jei reikia papildomų metaduomenų tipų, juos reikia įtraukti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="b8c35-127">When additional types of metadata are required, they must be manually added.</span></span>

    <span data-ttu-id="b8c35-128">Turite įtraukti metaduomenų, susijusių su užsienio prekybos operacijomis, ir rankiniu būdu pasirinkti metaduomenų elementus.</span><span class="sxs-lookup"><span data-stu-id="b8c35-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="b8c35-129">Pasirinkite **Įtraukti duomenų šaltinį \> Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="b8c35-130">Filtruokite pagal **Intrastat** reikšmę lauke **Pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="b8c35-131">Pasirinkite **Intrastat** lentelės įrašą.</span><span class="sxs-lookup"><span data-stu-id="b8c35-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="b8c35-132">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-132">Select **OK**.</span></span>

    <span data-ttu-id="b8c35-133">Turite įtraukti metaduomenų informaciją apie „Intrastat“ įrašų lentelę.</span><span class="sxs-lookup"><span data-stu-id="b8c35-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="b8c35-134">Medyje pasirinkite **Lentelės įrašai „Intrastat“ \> \>Ryšiai \> IntrastatCommodity (lentelės įrašai EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="b8c35-135">Pasirinkite **Įtraukti metaduomenis**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b8c35-136">Metaduomenis apie reikalingus ryšius, skirtus pasirinktai įrašų lentelei, reikia įtraukti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="b8c35-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="b8c35-137">Pasirinkite **Įtraukti duomenų šaltinį**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="b8c35-138">Pasirinkite **Išvardijimas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="b8c35-139">Filtruokite pagal **IntrastatDirection** reikšmę lauke **Pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="b8c35-140">Pasirinkite **IntrastatDirection** išvardijimo įrašą.</span><span class="sxs-lookup"><span data-stu-id="b8c35-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="b8c35-141">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-141">Select **OK**.</span></span>
20. <span data-ttu-id="b8c35-142">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-142">Select **Save**.</span></span>
21. <span data-ttu-id="b8c35-143">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b8c35-143">Close the page.</span></span>
22. <span data-ttu-id="b8c35-144">Užpildykite metaduomenų konfigūracijos juodraštinę versiją:</span><span class="sxs-lookup"><span data-stu-id="b8c35-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="b8c35-145">Pasirinkite **Keisti būseną \> Baigta**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="b8c35-146">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-146">Select **OK**.</span></span>
    3. <span data-ttu-id="b8c35-147">Pasirinkite baigtą versiją 1.</span><span class="sxs-lookup"><span data-stu-id="b8c35-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="b8c35-148">Eksportuokite baigtą metaduomenų konfigūracijos versiją iš programos kaip XML failą:</span><span class="sxs-lookup"><span data-stu-id="b8c35-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="b8c35-149">Pasirinkite **Keitimas \> Eksportuoti kaip XML failą**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="b8c35-150">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-150">Select **OK**.</span></span>

<span data-ttu-id="b8c35-151">Jūsų sukurta ER metaduomenų konfigūracija įrašoma kaip failas **Užsienio prekybos metaduomenys.xml**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="b8c35-152">Dabar galite jį importuoti į RCS ir naudoti kaip užsienio prekybos verslo srities metaduomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="b8c35-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain.</span></span> <span data-ttu-id="b8c35-153">Remdamiesi šia informacija, galite nurodyti susiejimą tarp programos metaduomenų ir ER duomenų modelio.</span><span class="sxs-lookup"><span data-stu-id="b8c35-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="b8c35-154">Prieiga prie programos metaduomenų naudojant ER konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="b8c35-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="b8c35-155">Toliau pateiktoje procedūroje parodoma, kaip RCS vartotojas, turintis vaidmens **Sistemos administratorius** arba **Elektroninės ataskaitos kūrėjas** teises, gali sukurti naują ER modelio susiejimą naudodamas programos metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="b8c35-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the application.</span></span> <span data-ttu-id="b8c35-156">Programos metaduomenys bus pasiekiami naudojant ER metaduomenų konfigūraciją, kurioje yra metaduomenų pavyzdžių rinkinys, skirtas užsienio prekybos operacijoms pasiekti.</span><span class="sxs-lookup"><span data-stu-id="b8c35-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="b8c35-157">Kad galėtumėte atlikti šią procedūrą, pirmiausia atlikite toliau nurodytas procedūras.</span><span class="sxs-lookup"><span data-stu-id="b8c35-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="b8c35-158">Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius</span><span class="sxs-lookup"><span data-stu-id="b8c35-158">Create configuration providers and mark them as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="b8c35-159">Programos metaduomenų, kuriuos galima naudoti RCS, paruošimas</span><span class="sxs-lookup"><span data-stu-id="b8c35-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="b8c35-160">Eikite į **Visos darbo sritys \> Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="b8c35-161">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="b8c35-162">Jei nematote šio konfigūracijų teikėjo, atlikite [Konfigūracijų teikėjų kūrimas ir pažymėjimas kaip aktyvių](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedūrą.</span><span class="sxs-lookup"><span data-stu-id="b8c35-162">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="b8c35-163">Importuokite ER metaduomenų konfigūraciją, kurioje yra programos metaduomenys ir kuri sukonfigūruota generuoti elektroninius dokumentus, skirtus užsienio prekybos verslo sričiai.</span><span class="sxs-lookup"><span data-stu-id="b8c35-163">Import the ER metadata configuration that contains metadata for the application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="b8c35-164">Jūs sukūrėte šią ER metaduomenų konfigūraciją ir eksportavote ją kaip XML failą atlikdami šioje temoje anksčiau pateiktą procedūrą [Programos metaduomenų, kuriuos galima naudoti RCS, paruošimas](#prepare-application-metadata-that-can-be-used-in-rcs).</span><span class="sxs-lookup"><span data-stu-id="b8c35-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="b8c35-165">Pasirinkite **Metaduomenų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="b8c35-166">Pasirinkite **Keitimas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="b8c35-167">Pasirinkite **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="b8c35-168">Raskite ir pasirinkite failą **Užsienio prekybos metaduomenys.xml**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="b8c35-169">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-169">Select **OK**.</span></span>
    6. <span data-ttu-id="b8c35-170">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b8c35-170">Close the page.</span></span>

4. <span data-ttu-id="b8c35-171">Sukurkite duomenų modelio konfigūraciją:</span><span class="sxs-lookup"><span data-stu-id="b8c35-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="b8c35-172">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="b8c35-173">Pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="b8c35-174">Išplečiamojo dialogo lango lauke **Pavadinimas** įveskite **Užsienio prekybos modelis**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="b8c35-175">Pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="b8c35-176">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="b8c35-177">Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b8c35-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="b8c35-178">Lauke **Pavadinimas** įveskite **Šaknis**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="b8c35-179">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="b8c35-180">Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b8c35-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="b8c35-181">Lauke **Pavadinimas** įveskite **Operacija**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="b8c35-182">Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="b8c35-183">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="b8c35-184">Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b8c35-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="b8c35-185">Lauke **Pavadinimas** įveskite **Prekės kodas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="b8c35-186">Lauke **Elemento tipas** pasirinkite **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="b8c35-187">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-187">Select **Add**.</span></span>

    9. <span data-ttu-id="b8c35-188">Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b8c35-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="b8c35-189">Lauke Pavadinimas įveskite **Sąskaitos faktūros suma**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="b8c35-190">Lauke **Elemento tipas** pasirinkite **Realusis skaičius**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="b8c35-191">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-191">Select **Add**.</span></span>

    10. <span data-ttu-id="b8c35-192">Pasirinkite **Naujas**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b8c35-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="b8c35-193">Lauke **Pavadinimas** įveskite **Data**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="b8c35-194">Lauke **Elemento tipas** pasirinkite **Data**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="b8c35-195">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="b8c35-196">Pasirinkite **Įtraukti \> Šakninė nuoroda**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="b8c35-197">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-197">Select **OK**.</span></span>
    13. <span data-ttu-id="b8c35-198">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-198">Select **Save**.</span></span>
    14. <span data-ttu-id="b8c35-199">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b8c35-199">Close the page.</span></span>
    15. <span data-ttu-id="b8c35-200">Pasirinkite **Keisti būseną \> Baigta**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="b8c35-201">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-201">Select **OK**.</span></span>

5. <span data-ttu-id="b8c35-202">Sukurkite modelio susiejimo konfigūraciją:</span><span class="sxs-lookup"><span data-stu-id="b8c35-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="b8c35-203">Pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="b8c35-204">Išplečiamojo dialogo lango lauke **Naujas** įveskite **Modelio susiejimas remiantis duomenų modeliu Užsienio prekybos modelis**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="b8c35-205">Lauke **Pavadinimas** įveskite **Užsienio prekybos susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="b8c35-206">Pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="b8c35-207">„FastTab“ **Būtinieji komponentai** pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="b8c35-208">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-208">Select **New**.</span></span>
    7. <span data-ttu-id="b8c35-209">Lauke **Būtinojo komponento tipas** pasirinkite **Konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="b8c35-210">Pasirinkite konfigūraciją **Užsienio prekybos metaduomenys**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="b8c35-211">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-211">Select **Save**.</span></span> <span data-ttu-id="b8c35-212">Atkreipkite dėmesį, kad nuoroda įtraukiama į konfigūracijos **Užsienio prekybos metaduomenys** 1 versiją.</span><span class="sxs-lookup"><span data-stu-id="b8c35-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="b8c35-213">Kuriant modelio susiejimą bus siūlomi šios konfigūracijos programos metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="b8c35-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="b8c35-214">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b8c35-214">Close the page.</span></span>
    11. <span data-ttu-id="b8c35-215">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="b8c35-216">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="b8c35-217">Medyje pasirinkite **„Dynamics 365 for Operations“ \> Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="b8c35-218">Pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="b8c35-219">Lauke **Pavadinimas** įveskite **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="b8c35-220">Pasirinkite **Intrastat** lentelės įrašus.</span><span class="sxs-lookup"><span data-stu-id="b8c35-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="b8c35-221">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b8c35-222">Siūlomos tik dvi lentelės, nes tik dvi lentelės įtrauktos į šiuo metu naudojamą metaduomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="b8c35-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="b8c35-223">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="b8c35-224">Medyje pasirinkite **Intrastat \> AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="b8c35-225">Medyje pasirinkite **Operacija = „Intrastat“ \> Sąskaitos faktūros suma**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="b8c35-226">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="b8c35-227">Medyje pasirinkite **Intrastat \> TransDate**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="b8c35-228">Medyje pasirinkite **Operacija = „Intrastat“ \> Data**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="b8c35-229">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="b8c35-230">Medyje pasirinkite **„Intrastat“ \> \>Ryšiai \> IntrastatCommodity \> Kodas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="b8c35-231">Medyje pasirinkite **Operacija = „Intrastat“ \> Prekės kodas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="b8c35-232">Pasirinkite **Susieti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="b8c35-233">Pasirinkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="b8c35-234">Kai tikrinimas baigtas, sėkmingai susiejote duomenų modelio elementus su duomenų šaltinių elementais, kurie aprašomi naudojant programos metaduomenų informaciją iš nurodytos ER metaduomenų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="b8c35-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="b8c35-235">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-235">Select **Save**.</span></span>

<span data-ttu-id="b8c35-236">Jei reikia, galite išplėsti esamą programos metaduomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="b8c35-236">As you require, you can extend the existing set of metadata in the application.</span></span> <span data-ttu-id="b8c35-237">Tada galite eksportuoti naują baigtą ER metaduomenų konfigūracijos versiją, importuoti į RCS ir atnaujinti sukonfigūruotos modelio susiejimo konfigūracijos būtinuosius komponentus, kad būtų nurodoma nauja importuotos metaduomenų konfigūracijos versija.</span><span class="sxs-lookup"><span data-stu-id="b8c35-237">You can then export the new completed version of the ER metadata configuration, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="b8c35-238">Tai yra vienintelis būdas gauti informaciją apie programos metaduomenis naudojant vietinėje sistemoje įdiegtas programas (t. y. kai programai naudojamas vietos verslo duomenų \[LBD\] arba vietinio diegimo modelis).</span><span class="sxs-lookup"><span data-stu-id="b8c35-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for the application).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="b8c35-239">Prieiga prie programos metaduomenų naudojant prijungtas programas</span><span class="sxs-lookup"><span data-stu-id="b8c35-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="b8c35-240">Toliau pateiktoje procedūroje parodoma, kaip RCS vartotojas, turintis vaidmens **Sistemos administratorius** arba **Elektroninės ataskaitos kūrėjas** teises, gali sukurti naują ER modelio susiejimą naudodamas programos metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="b8c35-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the application.</span></span> <span data-ttu-id="b8c35-241">Programos metaduomenys bus pasiekiami tinkle naudojant programą, prijungtą prie RCS.</span><span class="sxs-lookup"><span data-stu-id="b8c35-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="b8c35-242">Bus sukonfigūruotas ER modelio susiejimo pavyzdys, siekiant pasiekti užsienio prekybos operacijas.</span><span class="sxs-lookup"><span data-stu-id="b8c35-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="b8c35-243">Norėdami atlikti šią procedūrą, pirmiausia turite atlikti [Konfigūracijų teikėjų kūrimas ir pažymėjimas kaip aktyvių](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedūrą RCS.</span><span class="sxs-lookup"><span data-stu-id="b8c35-243">To complete this procedure, you must first complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="b8c35-244">Jei dar neatlikote anksčiau šioje temoje pateiktos procedūros [Prieiga prie programos metaduomenų naudojant ER konfigūraciją](#access-application-metadata-by-using-an-er-configuration), eikite į puslapį [Elektroninių ataskaitų užduočių vedliai, skirti „Dynamics 365 for Finance and Operations 8.1“](https://go.microsoft.com/fwlink/?linkid=2082739) ir iš anksto atsisiųskite toliau nurodytus ER konfigūracijos failus ir įrašykite juos vietinėje sistemoje: **Užsienio prekybos metaduomenys.xml**, **Užsienio prekybos modelis.xml** ir **Užsienio prekybos susiejimas.xml**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="b8c35-245">Reikiamų ER konfigūracijų gavimas</span><span class="sxs-lookup"><span data-stu-id="b8c35-245">Get required ER configurations</span></span>

<span data-ttu-id="b8c35-246">Jei jau atlikote anksčiau šioje temoje nurodytos procedūros [Prieiga prie programos metaduomenų naudojant ER konfigūraciją](#access-application-metadata-by-using-an-er-configuration) veiksmus, jūs jau turite visas reikiamas ER konfigūracijas (užsienio prekybos metaduomenų, modelio ir susiejimo konfigūracijas) dabartiniame RCS egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="b8c35-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="b8c35-247">Tokiu atveju galite praleisti šią procedūrą.</span><span class="sxs-lookup"><span data-stu-id="b8c35-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="b8c35-248">Eikite į **Visos darbo sritys \> Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="b8c35-249">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="b8c35-250">Įkelkite konfigūracijos failus **Užsienio prekybos metaduomenys.xml**, **Užsienio prekybos modelis.xml** ir **Užsienio prekybos susiejimas.xml**, su kiekvienu failu atlikdami toliau nurodytus veiksmus:</span><span class="sxs-lookup"><span data-stu-id="b8c35-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="b8c35-251">Pasirinkite **Keitimas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="b8c35-252">Pasirinkite **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="b8c35-253">Pasirinkite **Naršyti** ir pasirinkite failą.</span><span class="sxs-lookup"><span data-stu-id="b8c35-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="b8c35-254">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-the-application"></a><span data-ttu-id="b8c35-255">Užregistruokite ryšį su programa</span><span class="sxs-lookup"><span data-stu-id="b8c35-255">Register the connection with the application</span></span>

1. <span data-ttu-id="b8c35-256">Eikite į **Visos darbo sritys \> Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="b8c35-257">Pasirinkite **Prijungtos programos**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="b8c35-258">Įsitikinkite, kad sukonfigūruota programa veikia „Microsoft Azure“ pagrindu ir kad ji apskritai pasiekiama RCS vartotojams.</span><span class="sxs-lookup"><span data-stu-id="b8c35-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="b8c35-259">Esamas RCS vartotojas turi turėti prieigą prie registruojamos sukonfigūruotos programos kaip programos vartotojas, kuriam priskirtas vaidmuo suteikia teises pasiekti programos metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="b8c35-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives them privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="b8c35-260">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-260">Select **New**.</span></span>
5. <span data-ttu-id="b8c35-261">Lauke **Pavadinimas** įveskite **MyConnectedApp** kaip prijungtos programos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b8c35-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="b8c35-262">Lauke **Programa** nurodykite programos URL.</span><span class="sxs-lookup"><span data-stu-id="b8c35-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="b8c35-263">Lauke **Nuomotojas** nurodykite programos teikėją.</span><span class="sxs-lookup"><span data-stu-id="b8c35-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="b8c35-264">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-264">Select **Save**.</span></span> 
9. <span data-ttu-id="b8c35-265">Kai tikrinate ryšį su sukonfigūruota programa, puslapyje **Prisijungti prie nuotolinės programos** pasirinkite saitą **Pasirinkite čia, kad prisijungtumėte prie pasirinktos nuotolinės programos**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="b8c35-266">Pasirinkite **Tikrinti ryšį**, kad patikrintumėte prieigą prie sukonfigūruotos programos.</span><span class="sxs-lookup"><span data-stu-id="b8c35-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="b8c35-267">Pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-267">Select **Close**.</span></span>

<span data-ttu-id="b8c35-268">Atlikus šią procedūrą ir sėkmingai atlikus ryšio patikrą, sukonfigūruotos programos versijos ir nuomotojo informacija bus atnaujinta dabartiniame tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="b8c35-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="b8c35-269">Esamo modelio susiejimo konfigūracijos peržiūra</span><span class="sxs-lookup"><span data-stu-id="b8c35-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="b8c35-270">Eikite į **Visos darbo sritys \> Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="b8c35-271">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="b8c35-272">Medyje pasirinkite **Užsienio prekybos modelis \> Užsienio prekybos susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="b8c35-273">Pasirinkite „FastTab“ **Būtinieji komponentai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b8c35-274">Šiuo metu šis susiejimas nurodo metaduomenų konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="b8c35-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="b8c35-275">Kuriant šį modelio susiejimą bus siūlomi šios konfigūracijos programos metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="b8c35-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="b8c35-276">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-276">Select **Designer**.</span></span>
5. <span data-ttu-id="b8c35-277">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-277">Select **Designer**.</span></span>
6. <span data-ttu-id="b8c35-278">Medyje pasirinkite **„Dynamics 365 for Operations“ \> Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="b8c35-279">Pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-279">Select **Add root**.</span></span>
8. <span data-ttu-id="b8c35-280">Lauke **Lentelė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b8c35-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b8c35-281">Šiuo metu šis susiejimas nurodo metaduomenų konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="b8c35-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="b8c35-282">Kuriant šį modelio susiejimą bus siūlomi šios konfigūracijos programos metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="b8c35-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="b8c35-283">Pasirinkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="b8c35-284">Prijungtos programos priskyrimas modelio susiejimui</span><span class="sxs-lookup"><span data-stu-id="b8c35-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="b8c35-285">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-285">Select **Edit**.</span></span>
2. <span data-ttu-id="b8c35-286">**Prijungtos programos lauke** pasirinkite programą **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b8c35-287">Šis susiejimas nurodo pasirinktos prijungtos programos metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="b8c35-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="b8c35-288">Jei tas pats susiejimas tuo pačiu metu nurodo metaduomenų konfigūraciją ir prijungtą programą, bus naudojami prijungtos programos metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="b8c35-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="b8c35-289">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-289">Select **Designer**.</span></span>
4. <span data-ttu-id="b8c35-290">Pasirinkite **Dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-290">Select **Designer**.</span></span>
5. <span data-ttu-id="b8c35-291">Medyje pasirinkite **„Dynamics 365 for Operations“ \> Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="b8c35-292">Pasirinkite **Įtraukti šaknį**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-292">Select **Add root**.</span></span>
7. <span data-ttu-id="b8c35-293">Lauke **Lentelė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b8c35-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b8c35-294">Šiuo metu siūlomos daugiau nei dvi programos lentelės, nes šis susiejimas naudoja visus prijungtos programos, kuri buvo priskirta, metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="b8c35-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="b8c35-295">Pasirinkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="b8c35-296">Pasirinkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-296">Select **Validate**.</span></span>

<span data-ttu-id="b8c35-297">Jūs susiejote duomenų modelio elementus su duomenų šaltinių elementais, kurie aprašomi naudojant prijungtos programos, priskirtos šiam susiejimui, metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="b8c35-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="b8c35-298">Jei reikia įvertinti šio modelio susiejimą naudojant skirtingos programos versijos metaduomenis, užregistruokite kitą prijungtą programą, priskirkite ją šiam modelio susiejimui ir patikrinkite ją naudodami naujus metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="b8c35-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b8c35-299">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b8c35-299">Additional resources</span></span>

<span data-ttu-id="b8c35-300">Arba galite programoje paleisti užduočių vedlį **Programos metaduomenų, kuriuos galima naudoti RCS, paruošimas** ir taip pat RCS galite paleisti užduočių vedlius **Prieiga prie programos metaduomenų naudojant ER konfigūraciją** ir **Prieiga prie programos metaduomenų naudojant prijungtas programas**.</span><span class="sxs-lookup"><span data-stu-id="b8c35-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in the application as as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="b8c35-301">Šiuos užduočių vedlius galima atsisiųsti iš puslapio [Elektroninių ataskaitų užduočių vedliai, skirti „Dynamics 365 for Finance and Operations 8.1“](https://go.microsoft.com/fwlink/?linkid=2082739).</span><span class="sxs-lookup"><span data-stu-id="b8c35-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]