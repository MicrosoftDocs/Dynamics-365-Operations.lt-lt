---
title: Kurkite ER konfigūracijas RCS ir įkelkite jas į bendrąją saugyklą
description: Šioje temoje aiškinama, kaip sukurti elektroninių ataskaitų (ER) konfigūraciją „Microsoft Regulatory Configuration Service“ (RCS) ir nusiųsti ją į bendrąją saugyklą.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
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
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371259"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="81658-103">ER konfigūracijų kūrimas „Regulatory Configuration Service“ (RCS) ir įkėlimas į bendrąją saugyklą</span><span class="sxs-lookup"><span data-stu-id="81658-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81658-104">Elektroninių ataskaitų (ER) konfigūracijoms kurti galite naudoti „Microsoft Regulatory Configuration Services“ (RCS), o tada publikuoti, kad jas būtų galima naudoti jūsų organizacijoje</span><span class="sxs-lookup"><span data-stu-id="81658-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="81658-105">Toliau pateiktos procedūros paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų programuotojo vaidmenį turintis vartotojas gali sukurti išvestinę ER konfigūracijos, sukonfigūruotos RCS egzemplioriuje, versiją, o tada nusiųsti išvestinę konfigūraciją į bendrąją saugyklą.</span><span class="sxs-lookup"><span data-stu-id="81658-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="81658-106">Kad galėtumėte atlikti šias procedūras, pirmiausia turite įgyvendinti toliau nurodytas būtinąsias sąlygas.</span><span class="sxs-lookup"><span data-stu-id="81658-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="81658-107">Pasiekti RCS egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="81658-107">Access an RCS instance.</span></span>
- <span data-ttu-id="81658-108">Sikurti aktyvų konfigūracijos teikėją.</span><span class="sxs-lookup"><span data-stu-id="81658-108">Create an active configuration provider.</span></span> <span data-ttu-id="81658-109">Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="81658-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="81658-110">Taip pat turite įsitikinti, kad RCS aplinka yra parengta jūsų įmonei.</span><span class="sxs-lookup"><span data-stu-id="81658-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="81658-111">Programoje „Finance and Operations“ eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="81658-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="81658-112">Jei jūsų įmonei RCS aplinka neparengta, pasirinkite **„Regulatory Services“ – išorinė konfigūracija** ir vykdykite instrukcijas, kad ją parengtumėte.</span><span class="sxs-lookup"><span data-stu-id="81658-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="81658-113">Jei RCS aplinka jūsų įmonei jau parengta, pasiekite ją naudodami puslapio URL ir pasirinkdami prisijungimo parinktį.</span><span class="sxs-lookup"><span data-stu-id="81658-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="81658-114">Išvestinės konfigūracijos versijos kūrimas RCS</span><span class="sxs-lookup"><span data-stu-id="81658-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="81658-115">Darbo srityje **Elektroninės ataskaitos** patvirtinkite, kad turite aktyvų savo organizacijos konfigūracijos teikėją.</span><span class="sxs-lookup"><span data-stu-id="81658-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="81658-116">Pasirinkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="81658-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="81658-117">Pasirinkite konfigūraciją, iš kurios norite išvesti naują versiją.</span><span class="sxs-lookup"><span data-stu-id="81658-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="81658-118">Ieškai susiaurinti galite naudoti virš medžio esantį filtravimo lauką.</span><span class="sxs-lookup"><span data-stu-id="81658-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="81658-119">Pasirinkite **Kurti konfigūraciją** \> **Kildinti iš pavadinimo**.</span><span class="sxs-lookup"><span data-stu-id="81658-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="81658-120">Įveskite pavadinimą ir aprašą, tada pasirinkite **Kurti konfigūraciją**, kad sukurtumėte naują išvestinę versiją.</span><span class="sxs-lookup"><span data-stu-id="81658-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="81658-121">Pasirinkite naujai išvestą konfigūraciją, įtraukite versijos aprašą, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="81658-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="81658-122">Konfigūracijos būsena pakeičiama į **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="81658-122">The status of the configuration to is changed to **Completed**.</span></span>

![Nauja konfigūracijos versija RCS](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="81658-124">Pakeitus konfigūracijos būseną, galite gauti tikrinimo klaidos pranešimą, susijusį su prijungtomis programomis.</span><span class="sxs-lookup"><span data-stu-id="81658-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="81658-125">Norėdami išjungti tikrinimą, veiksmų srities skirtuke **Konfigūracijos** pasirinkite **Vartotojo parametrai** ir nustatykite parinkties **Praleisti tikrinimą konfigūracijos būsenos keitimo ir pritaikymo kitoje vietoje metu** reikšmę kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="81658-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="81658-126">Konfigūracijos nusiuntimas į bendrąją saugyklą</span><span class="sxs-lookup"><span data-stu-id="81658-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="81658-127">Norėdami bendrinti naują arba išvestinę konfigūraciją su savo organizacija, galite nusiųsti ją į bendrąją saugyklą.</span><span class="sxs-lookup"><span data-stu-id="81658-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="81658-128">Pasirinkite užbaigtą konfigūracijos versiją, tada pasirinkite **Nusiųsti į saugyklą**.</span><span class="sxs-lookup"><span data-stu-id="81658-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="81658-129">Pasirinkite parinktį **Bendroji („Microsoft“)**, tada – **Nusiųsti**.</span><span class="sxs-lookup"><span data-stu-id="81658-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Nusiuntimo į saugyklą parinktys](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="81658-131">Patvirtinimo pranešimo lange pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="81658-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="81658-132">Jei reikia, atnaujinkite versijos aprašą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="81658-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="81658-133">Konfigūracijos būsena atnaujinama į **Bendrinama**, o konfigūracija nusiunčiama į bendrąją saugyklą.</span><span class="sxs-lookup"><span data-stu-id="81658-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="81658-134">Čia ją galite naudoti toliau nurodytais būdais.</span><span class="sxs-lookup"><span data-stu-id="81658-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="81658-135">Importuoti į savo „Dynamics 365“ egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="81658-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="81658-136">Daugiau informacijos žr. [(ER) Konfigūracijų importavimas iš RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="81658-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="81658-137">Bendrinti su trečiąja šalimi arba su išorine organizacija; žr. [RCS elektroninių ataskaitų (arba) konfigūracijų bendrinimas su išorinėmis organizacijomis](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="81658-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span></span>

![Išvestinė „Intrastat Contoso“ konfigūracijos versija bendrojoje saugykloje](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
