---
title: Programos metaduomenų, kurie bus naudojami RCS, parengimas
description: Šioje temoje apibūdinama, kaip sukurti naują ataskaitos konfigūraciją, kurioje yra programos metaduomenys.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9609da50482f39bafe65d3a7b655e5047c74bdba
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560122"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="159a2-103">Programos metaduomenų, kurie bus naudojami RCS, parengimas</span><span class="sxs-lookup"><span data-stu-id="159a2-103">Prepare application metadata to be used in RCS</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="159a2-104">Toliau nurodyti veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali kurti naują elektroninės ataskaitos (ER) konfigūraciją, kurioje yra programos metaduomenys, skirti ER modelio susiejimo konfigūracijoms kurti naudojant „Regulatory Configuration Service“ (RCS).</span><span class="sxs-lookup"><span data-stu-id="159a2-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="159a2-105">Naudojantis šia konfigūracija sukuriamas ER modelio susiejimo konfigūracijos, naudojamos norint pasiekti užsienio prekybos operacijas, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="159a2-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="159a2-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="159a2-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="159a2-107">Norint atlikti šiuos veiksmus, pirmiausia reikia atlikti veiksmus, nurodytus temoje [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="159a2-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="159a2-108">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="159a2-108">Prerequisites</span></span>
1.    <span data-ttu-id="159a2-109">Eikite į **Organizacijos administravimas** > **Darbo sritys** > **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="159a2-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.    <span data-ttu-id="159a2-110">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="159a2-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="159a2-111">Jei nematote šio konfigūracijos teikėjo, atlikite procedūros [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md) veiksmus.</span><span class="sxs-lookup"><span data-stu-id="159a2-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.    <span data-ttu-id="159a2-112">Spustelėkite **Metaduomenų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="159a2-112">Click **Metadata configurations**.</span></span> 
4.    <span data-ttu-id="159a2-113">Tarkime, kad naudojantis RCS sukuriamas programai „Finance and Operations“ skirtas sprendimas, kuris generuoja elektroninius dokumentus, kuriuose pateikiama informacija iš užsienio prekybos verslo srities.</span><span class="sxs-lookup"><span data-stu-id="159a2-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="159a2-114">Norint susieti ER duomenų modelį su reikiamų duomenų šaltiniais, naudojantis RCS reikia turėti prieigą prie programos „Finance and Operations“ metaduomenų.</span><span class="sxs-lookup"><span data-stu-id="159a2-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="159a2-115">Todėl, norėdami sukurti ER sprendimą, mes sukonfigūruojame naują ER metaduomenų konfigūraciją, kurioje yra visi metaduomenys, kurių šiuo metu reikia generuojant pasirinktos verslo srities ER ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="159a2-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="159a2-116">Metaduomenų konfigūracijos įtraukimas</span><span class="sxs-lookup"><span data-stu-id="159a2-116">Add metadata configuration</span></span> 
1.    <span data-ttu-id="159a2-117">Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="159a2-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.    <span data-ttu-id="159a2-118">Lauke **Pavadinimas** įveskite „Užsienio prekybos metaduomenys“.</span><span class="sxs-lookup"><span data-stu-id="159a2-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.    <span data-ttu-id="159a2-119">Spustelėkite **Sukurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="159a2-119">Click **Create configuration**.</span></span> 
4.    <span data-ttu-id="159a2-120">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="159a2-120">Click **Designer**.</span></span> 
5.    <span data-ttu-id="159a2-121">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="159a2-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="159a2-122">Galite pasirinkti visus metaduomenis, skirtus visai programai arba pasirinktiems modeliams ar moduliams.</span><span class="sxs-lookup"><span data-stu-id="159a2-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="159a2-123">Atminkite, kad šiuo atveju šie metaduomenys bus įtraukti automatiškai: įrašų lentelės, išvardijimai ir išplėstiniai duomenų tipai.</span><span class="sxs-lookup"><span data-stu-id="159a2-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="159a2-124">Jei reikia papildomų metaduomenų tipų, juos reikia įtraukti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="159a2-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="159a2-125">Siūlome tam tikrų su užsienio prekybos operacijomis susijusių metaduomenų, kai metaduomenų elementai pasirenkami rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="159a2-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.    <span data-ttu-id="159a2-126">Spustelėkite **Įtraukti duomenų šaltinį**.</span><span class="sxs-lookup"><span data-stu-id="159a2-126">Click **Add data source**.</span></span> 
7.    <span data-ttu-id="159a2-127">Spustelėkite **Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="159a2-127">Click **Table records**.</span></span> 
8.    <span data-ttu-id="159a2-128">Naudokite spartųjį filtrą, kad atfiltruotumėte lauką **Pavadinimas** pagal reikšmę „Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="159a2-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.    <span data-ttu-id="159a2-129">Pasirinkite **Intrastat** lentelės įrašą.</span><span class="sxs-lookup"><span data-stu-id="159a2-129">Select the **Intrastat** table record.</span></span> 
10.    <span data-ttu-id="159a2-130">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="159a2-130">Click **OK**.</span></span>
  
<span data-ttu-id="159a2-131">Įtraukėme metaduomenų informaciją apie „Intrastat“ įrašų lentelę.</span><span class="sxs-lookup"><span data-stu-id="159a2-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11.    <span data-ttu-id="159a2-132">Medyje išplėskite **Lentelės įrašai „Intrastat“**\>**Ryšiai**.</span><span class="sxs-lookup"><span data-stu-id="159a2-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12.    <span data-ttu-id="159a2-133">Medyje pasirinkite **Lentelės įrašai „Intrastat“**\>**Ryšiai\IntrastatCommodity (lentelės įrašai EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="159a2-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>     
13.    <span data-ttu-id="159a2-134">Spustelėkite **Įtraukti metaduomenis**.</span><span class="sxs-lookup"><span data-stu-id="159a2-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="159a2-135">Metaduomenis apie reikalingus ryšius, skirtus pasirinktai įrašų lentelei, reikia įtraukti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="159a2-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16.    <span data-ttu-id="159a2-136">Spustelėkite **Įtraukti duomenų šaltinį**.</span><span class="sxs-lookup"><span data-stu-id="159a2-136">Click **Add data source**.</span></span> 
17.    <span data-ttu-id="159a2-137">Spustelėkite **Išvardijimas**.</span><span class="sxs-lookup"><span data-stu-id="159a2-137">Click **Enumeration**.</span></span> 
18.    <span data-ttu-id="159a2-138">Naudokite spartųjį filtrą, kad atfiltruotumėte lauką **Pavadinimas** pagal reikšmę „IntrastatDirection“.</span><span class="sxs-lookup"><span data-stu-id="159a2-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19.    <span data-ttu-id="159a2-139">Pasirinkite įrašą **IntrastatDirection išvardijimas**.</span><span class="sxs-lookup"><span data-stu-id="159a2-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20.    <span data-ttu-id="159a2-140">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="159a2-140">Click **OK**.</span></span> 
21.    <span data-ttu-id="159a2-141">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="159a2-141">Click **Save**.</span></span>  
22.    <span data-ttu-id="159a2-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="159a2-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="159a2-143">Metaduomenų konfigūracijos juodraštinės versijos užpildymas</span><span class="sxs-lookup"><span data-stu-id="159a2-143">Complete the draft version of metadata configuration</span></span>
1.    <span data-ttu-id="159a2-144">Spustelėkite **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="159a2-144">Click **Change status**.</span></span> 
2.    <span data-ttu-id="159a2-145">Spustelėkite **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="159a2-145">Click **Complete**.</span></span> 
3.    <span data-ttu-id="159a2-146">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="159a2-146">Click **OK**.</span></span> 
4.    <span data-ttu-id="159a2-147">Pasirinkite baigtą versiją **1**.</span><span class="sxs-lookup"><span data-stu-id="159a2-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="159a2-148">Baigtos metaduomenų konfigūracijos versijos eksportavimas iš programos XML formatu</span><span class="sxs-lookup"><span data-stu-id="159a2-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.    <span data-ttu-id="159a2-149">Spustelėkite **Keitimas**.</span><span class="sxs-lookup"><span data-stu-id="159a2-149">Click **Exchange**.</span></span> 
2.    <span data-ttu-id="159a2-150">Spustelėkite **Eksportuoti kaip XML failą**.</span><span class="sxs-lookup"><span data-stu-id="159a2-150">Click **Export as XML file**.</span></span> 
3.    <span data-ttu-id="159a2-151">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="159a2-151">Click **OK**.</span></span> 
    
<span data-ttu-id="159a2-152">Sukurta ER metaduomenų konfigūracija įrašyta kaip XML failas, kurį galima importuoti į RCS ir naudoti kaip užsienio prekybos verslo srities metaduomenų informacijos šaltinį.</span><span class="sxs-lookup"><span data-stu-id="159a2-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="159a2-153">Remdamiesi šia informacija, galime nurodyti susiejimą tarp programos metaduomenų ir ER duomenų modelio.</span><span class="sxs-lookup"><span data-stu-id="159a2-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]