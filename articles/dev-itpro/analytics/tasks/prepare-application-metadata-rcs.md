---
title: Programos metaduomenų, kurie bus naudojami RCS, parengimas
description: Šios temos veiksmai paaiškina, kaip vartotojas gali kurti naują elektroninės ataskaitos (ER) konfigūraciją, kurioje yra programos „Finance and Operations“ metaduomenys, skirti ER modelio susiejimo konfigūracijoms kurti naudojant „Regulatory Configuration Service“ (RCS).
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1bd2298240fa789762a350e90888201c5a7ce45
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726988"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="1d912-103">Programos metaduomenų, kurie bus naudojami RCS, parengimas</span><span class="sxs-lookup"><span data-stu-id="1d912-103">Prepare application metadata to be used in RCS</span></span>
[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d912-104">Toliau nurodyti veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali kurti naują elektroninės ataskaitos (ER) konfigūraciją, kurioje yra „Microsoft Dynamics 365 for Finance and Operations“ programos metaduomenys, skirti ER modelio susiejimo konfigūracijoms kurti naudojant „Regulatory configuration service“ (RCS).</span><span class="sxs-lookup"><span data-stu-id="1d912-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains Microsoft Dynamics 365 for Finance and Operations application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="1d912-105">Naudojantis šia konfigūracija sukuriamas ER modelio susiejimo konfigūracijos, naudojamos norint pasiekti užsienio prekybos operacijas, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="1d912-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="1d912-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="1d912-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="1d912-107">Norint atlikti šiuos veiksmus, pirmiausia reikia atlikti veiksmus, nurodytus temoje [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="1d912-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1d912-108">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="1d912-108">Prerequisites</span></span>
1.  <span data-ttu-id="1d912-109">Eikite į **Organizacijos administravimas** > **Darbo sritys** > **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="1d912-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.  <span data-ttu-id="1d912-110">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="1d912-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="1d912-111">Jei nematote šio konfigūracijos teikėjo, atlikite procedūros [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md) veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1d912-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.  <span data-ttu-id="1d912-112">Spustelėkite **Metaduomenų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="1d912-112">Click **Metadata configurations**.</span></span> 
4.  <span data-ttu-id="1d912-113">Tarkime, kad naudojantis RCS sukuriamas programai „Finance and Operations“ skirtas sprendimas, kuris generuoja elektroninius dokumentus, kuriuose pateikiama informacija iš užsienio prekybos verslo srities.</span><span class="sxs-lookup"><span data-stu-id="1d912-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="1d912-114">Norint susieti ER duomenų modelį su reikiamų duomenų šaltiniais, naudojantis RCS reikia turėti prieigą prie programos „Finance and Operations“ metaduomenų.</span><span class="sxs-lookup"><span data-stu-id="1d912-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="1d912-115">Todėl, norėdami sukurti ER sprendimą, mes sukonfigūruojame naują ER metaduomenų konfigūraciją, kurioje yra visi metaduomenys, kurių šiuo metu reikia generuojant pasirinktos verslo srities ER ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="1d912-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="1d912-116">Metaduomenų konfigūracijos įtraukimas</span><span class="sxs-lookup"><span data-stu-id="1d912-116">Add metadata configuration</span></span> 
1.  <span data-ttu-id="1d912-117">Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1d912-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.  <span data-ttu-id="1d912-118">Lauke **Pavadinimas** įveskite „Užsienio prekybos metaduomenys“.</span><span class="sxs-lookup"><span data-stu-id="1d912-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.  <span data-ttu-id="1d912-119">Spustelėkite **Sukurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="1d912-119">Click **Create configuration**.</span></span> 
4.  <span data-ttu-id="1d912-120">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="1d912-120">Click **Designer**.</span></span> 
5.  <span data-ttu-id="1d912-121">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="1d912-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1d912-122">Galite pasirinkti visus metaduomenis, skirtus visai programai arba pasirinktiems modeliams ar moduliams.</span><span class="sxs-lookup"><span data-stu-id="1d912-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="1d912-123">Atminkite, kad šiuo atveju šie metaduomenys bus įtraukti automatiškai: įrašų lentelės, išvardijimai ir išplėstiniai duomenų tipai.</span><span class="sxs-lookup"><span data-stu-id="1d912-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="1d912-124">Jei reikia papildomų metaduomenų tipų, juos reikia įtraukti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="1d912-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="1d912-125">Siūlome tam tikrų su užsienio prekybos operacijomis susijusių metaduomenų, kai metaduomenų elementai pasirenkami rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="1d912-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.  <span data-ttu-id="1d912-126">Spustelėkite **Įtraukti duomenų šaltinį**.</span><span class="sxs-lookup"><span data-stu-id="1d912-126">Click **Add data source**.</span></span> 
7.  <span data-ttu-id="1d912-127">Spustelėkite **Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="1d912-127">Click **Table records**.</span></span> 
8.  <span data-ttu-id="1d912-128">Naudokite spartųjį filtrą, kad atfiltruotumėte lauką **Pavadinimas** pagal reikšmę „Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="1d912-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.  <span data-ttu-id="1d912-129">Pasirinkite **Intrastat** lentelės įrašą.</span><span class="sxs-lookup"><span data-stu-id="1d912-129">Select the **Intrastat** table record.</span></span> 
10. <span data-ttu-id="1d912-130">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1d912-130">Click **OK**.</span></span>
  
<span data-ttu-id="1d912-131">Įtraukėme metaduomenų informaciją apie „Intrastat“ įrašų lentelę.</span><span class="sxs-lookup"><span data-stu-id="1d912-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11. <span data-ttu-id="1d912-132">Medyje išplėskite **Lentelės įrašai „Intrastat“**\>**Ryšiai**.</span><span class="sxs-lookup"><span data-stu-id="1d912-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12. <span data-ttu-id="1d912-133">Medyje pasirinkite **Lentelės įrašai „Intrastat“**\>**Ryšiai\IntrastatCommodity (lentelės įrašai EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="1d912-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>   
13. <span data-ttu-id="1d912-134">Spustelėkite **Įtraukti metaduomenis**.</span><span class="sxs-lookup"><span data-stu-id="1d912-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1d912-135">Metaduomenis apie reikalingus ryšius, skirtus pasirinktai įrašų lentelei, reikia įtraukti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="1d912-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16. <span data-ttu-id="1d912-136">Spustelėkite **Įtraukti duomenų šaltinį**.</span><span class="sxs-lookup"><span data-stu-id="1d912-136">Click **Add data source**.</span></span> 
17. <span data-ttu-id="1d912-137">Spustelėkite **Išvardijimas**.</span><span class="sxs-lookup"><span data-stu-id="1d912-137">Click **Enumeration**.</span></span> 
18. <span data-ttu-id="1d912-138">Naudokite spartųjį filtrą, kad atfiltruotumėte lauką **Pavadinimas** pagal reikšmę „IntrastatDirection“.</span><span class="sxs-lookup"><span data-stu-id="1d912-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19. <span data-ttu-id="1d912-139">Pasirinkite įrašą **IntrastatDirection išvardijimas**.</span><span class="sxs-lookup"><span data-stu-id="1d912-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20. <span data-ttu-id="1d912-140">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1d912-140">Click **OK**.</span></span> 
21. <span data-ttu-id="1d912-141">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1d912-141">Click **Save**.</span></span>  
22. <span data-ttu-id="1d912-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1d912-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="1d912-143">Metaduomenų konfigūracijos juodraštinės versijos užpildymas</span><span class="sxs-lookup"><span data-stu-id="1d912-143">Complete the draft version of metadata configuration</span></span>
1.  <span data-ttu-id="1d912-144">Spustelėkite **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="1d912-144">Click **Change status**.</span></span> 
2.  <span data-ttu-id="1d912-145">Spustelėkite **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="1d912-145">Click **Complete**.</span></span> 
3.  <span data-ttu-id="1d912-146">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1d912-146">Click **OK**.</span></span> 
4.  <span data-ttu-id="1d912-147">Pasirinkite baigtą versiją **1**.</span><span class="sxs-lookup"><span data-stu-id="1d912-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="1d912-148">Baigtos metaduomenų konfigūracijos versijos eksportavimas iš programos XML formatu</span><span class="sxs-lookup"><span data-stu-id="1d912-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.  <span data-ttu-id="1d912-149">Spustelėkite **Keitimas**.</span><span class="sxs-lookup"><span data-stu-id="1d912-149">Click **Exchange**.</span></span> 
2.  <span data-ttu-id="1d912-150">Spustelėkite **Eksportuoti kaip XML failą**.</span><span class="sxs-lookup"><span data-stu-id="1d912-150">Click **Export as XML file**.</span></span> 
3.  <span data-ttu-id="1d912-151">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1d912-151">Click **OK**.</span></span> 
    
<span data-ttu-id="1d912-152">Sukurta ERA metaduomenų konfigūracija įrašyta kaip XML failas, kurį galima importuoti į RCS ir naudoti „Finance and Operations“ kaip užsienio prekybos verslo srities metaduomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="1d912-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain in Finance and Operations.</span></span> <span data-ttu-id="1d912-153">Remdamiesi šia informacija, galime nurodyti susiejimą tarp programos metaduomenų ir ER duomenų modelio.</span><span class="sxs-lookup"><span data-stu-id="1d912-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
