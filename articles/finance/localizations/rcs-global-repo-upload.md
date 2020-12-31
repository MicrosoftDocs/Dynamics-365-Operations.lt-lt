---
title: Kurkite ER konfigūracijas RCS ir įkelkite jas į bendrąją saugyklą
description: Šioje temoje aiškinama, kaip sukurti elektroninių ataskaitų (ER) konfigūraciją „Microsoft Regulatory Configuration Service“ (RCS) ir nusiųsti ją į bendrąją saugyklą.
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 5b2b8f35b9931f8fd1824c20e9045da68af33ad5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446052"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="d9ebb-103">ER konfigūracijų kūrimas „Regulatory Configuration Service“ (RCS) ir įkėlimas į bendrąją saugyklą</span><span class="sxs-lookup"><span data-stu-id="d9ebb-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9ebb-104">Elektroninių ataskaitų (ER) konfigūracijoms kurti galite naudoti „Microsoft Regulatory Configuration Services“ (RCS), o tada publikuoti, kad jas būtų galima naudoti jūsų organizacijoje</span><span class="sxs-lookup"><span data-stu-id="d9ebb-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="d9ebb-105">Toliau pateiktos procedūros paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų programuotojo vaidmenį turintis vartotojas gali sukurti išvestinę ER konfigūracijos, sukonfigūruotos RCS egzemplioriuje, versiją, o tada nusiųsti išvestinę konfigūraciją į bendrąją saugyklą.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="d9ebb-106">Kad galėtumėte atlikti šias procedūras, pirmiausia turite įgyvendinti toliau nurodytas būtinąsias sąlygas.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="d9ebb-107">Pasiekti RCS egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-107">Access an RCS instance.</span></span>
- <span data-ttu-id="d9ebb-108">Sikurti aktyvų konfigūracijos teikėją.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-108">Create an active configuration provider.</span></span> <span data-ttu-id="d9ebb-109">Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d9ebb-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="d9ebb-110">Taip pat turite įsitikinti, kad RCS aplinka yra parengta jūsų įmonei.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="d9ebb-111">Programoje „Finance and Operations“ eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d9ebb-112">Jei jūsų įmonei RCS aplinka neparengta, pasirinkite **„Regulatory Services“ – išorinė konfigūracija** ir vykdykite instrukcijas, kad ją parengtumėte.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="d9ebb-113">Jei RCS aplinka jūsų įmonei jau parengta, pasiekite ją naudodami puslapio URL ir pasirinkdami prisijungimo parinktį.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="d9ebb-114">Išvestinės konfigūracijos versijos kūrimas RCS</span><span class="sxs-lookup"><span data-stu-id="d9ebb-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="d9ebb-115">Darbo srityje **Elektroninės ataskaitos** patvirtinkite, kad turite aktyvų savo organizacijos konfigūracijos teikėją.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="d9ebb-116">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="d9ebb-117">Pasirinkite konfigūraciją, iš kurios norite išvesti naują versiją.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="d9ebb-118">Ieškai susiaurinti galite naudoti virš medžio esantį filtravimo lauką.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="d9ebb-119">Pasirinkite **Kurti konfigūraciją** \> **Kildinti iš pavadinimo**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="d9ebb-120">Įveskite pavadinimą ir aprašą, tada pasirinkite **Kurti konfigūraciją**, kad sukurtumėte naują išvestinę versiją.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="d9ebb-121">Pasirinkite naujai išvestą konfigūraciją, įtraukite versijos aprašą, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="d9ebb-122">Konfigūracijos būsena pakeičiama į **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-122">The status of the configuration to is changed to **Completed**.</span></span>

![Nauja konfigūracijos versija RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="d9ebb-124">Pakeitus konfigūracijos būseną, galite gauti tikrinimo klaidos pranešimą, susijusį su prijungtomis programomis.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="d9ebb-125">Norėdami išjungti tikrinimą, veiksmų srities skirtuke **Konfigūracijos** pasirinkite **Vartotojo parametrai** ir nustatykite parinkties **Praleisti tikrinimą konfigūracijos būsenos keitimo ir pritaikymo kitoje vietoje metu** reikšmę kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="d9ebb-126">Konfigūracijos nusiuntimas į bendrąją saugyklą</span><span class="sxs-lookup"><span data-stu-id="d9ebb-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="d9ebb-127">Norėdami bendrinti naują arba išvestinę konfigūraciją su savo organizacija, galite nusiųsti ją į bendrąją saugyklą.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="d9ebb-128">Pasirinkite užbaigtą konfigūracijos versiją, tada pasirinkite **Nusiųsti į saugyklą**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="d9ebb-129">Pasirinkite parinktį **Bendroji („Microsoft“)**, tada – **Nusiųsti**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Nusiuntimo į saugyklą parinktys](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="d9ebb-131">Patvirtinimo pranešimo lange pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="d9ebb-132">Jei reikia, atnaujinkite versijos aprašą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="d9ebb-133">Konfigūracijos būsena atnaujinama į **Bendrinama**, o konfigūracija nusiunčiama į bendrąją saugyklą.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="d9ebb-134">Čia ją galite naudoti toliau nurodytais būdais.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="d9ebb-135">Importuoti į savo „Dynamics 365“ egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="d9ebb-136">Daugiau informacijos žr. [(ER) Konfigūracijų importavimas iš RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="d9ebb-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="d9ebb-137">Bendrinti su trečiąja šalimi arba su išorine organizacija; žr. [RCS elektroninių ataskaitų (arba) konfigūracijų bendrinimas su išorinėmis organizacijomis](rcs-global-repo-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="d9ebb-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![Išvestinė „Intrastat Contoso“ konfigūracijos versija bendrojoje saugykloje](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="d9ebb-139">Konfigūracijos naikinimas iš bendrosios saugyklos</span><span class="sxs-lookup"><span data-stu-id="d9ebb-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="d9ebb-140">Norėdami panaikinti konfigūraciją, kurią sukūrė jūsų organizacija, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="d9ebb-141">Darbo srityje **Elektroninės ataskaitos** patvirtinkite, kad jūsų konfigūracijos teikėjo yra **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="d9ebb-142">Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d9ebb-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="d9ebb-143">Prie savo aktyvaus konfigūracijos teikėjo pasirinkite **saugykla**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="d9ebb-144">Pasirinkite **Visuotinį** saugyklos tipą ir tada pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="d9ebb-145">„FastTab ”skirtuke **Filtras** suraskite konfigūraciją, kurią norite naikinti, naudodami **Filtro** funkciją.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="d9ebb-146">„FastTab” **Versija** pasirinkite norimos naikinti konfigūracijos versiją ir pasirinkite **Naikinti**:</span><span class="sxs-lookup"><span data-stu-id="d9ebb-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![Naikinti konfigūraciją iš bendrosios saugyklos](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="d9ebb-148">Patvirtinimo pranešimo lange pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-148">In the confirmation message box, select **Yes**.</span></span>

    ![Konfigūracijos versijos patvirtinimo pranešimo naikinimas](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="d9ebb-150">Konfigūracijos versija panaikinama ir parodomas patvirtinimo pranešimas.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="d9ebb-151">Konfigūracijas panaikinti gali tik jas sukūręs konfigūracijos teikėjas.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="d9ebb-152">Jei konfigūracija buvo bendrai naudojama su kita organizacija, turėsite atsieti konfigūraciją, prieš ją naikindami.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 
