---
title: RCS / bendrosios saugyklos ER konfigūracijų bendrinimas su išorinėmis organizacijomis
description: Šioje temoje paaiškinama, kaip „Microsoft Regulatory Configuration Service“ (RCS) / bendrojoje saugykloje esančių elektroninių ataskaitų (ER) konfigūracijas tiesiogiai bendrinti su išorinėmis organizacijomis.
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
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
ms.openlocfilehash: 04c46824123906eccbfff18a03974c8043729e0a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446053"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="e81d1-103">„Regulatory Configuration Service“ (RCS) bendrojoje saugykloje esančių elektroninių ataskaitų (ER) konfigūracijų bendrinimas su išorinėmis organizacijomis</span><span class="sxs-lookup"><span data-stu-id="e81d1-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e81d1-104">Elektroninių ataskaitų (ER) konfigūracijoms bendrinti galite naudoti „Microsoft Regulatory Configuration Services“ (RCS), o tada publikuoti jas išorinėse organizacijose.</span><span class="sxs-lookup"><span data-stu-id="e81d1-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="e81d1-105">Toliau aprašytos procedūros paaiškina, kaip RCS vartotojas gali bendrinti RCS egzemplioriuje sukonfigūruotą ER konfigūracijos versiją su išorine organizacija.</span><span class="sxs-lookup"><span data-stu-id="e81d1-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="e81d1-106">Kad galėtumėte atlikti šias procedūras, pirmiausia turite įgyvendinti toliau nurodytas būtinąsias sąlygas.</span><span class="sxs-lookup"><span data-stu-id="e81d1-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="e81d1-107">Pasiekti RCS egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="e81d1-107">Access an RCS instance.</span></span>
- <span data-ttu-id="e81d1-108">Sikurti aktyvų konfigūracijos teikėją.</span><span class="sxs-lookup"><span data-stu-id="e81d1-108">Create an active configuration provider.</span></span> <span data-ttu-id="e81d1-109">Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e81d1-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="e81d1-110">Sukurti ir nusiųsti naują ER konfigūracijos versiją.</span><span class="sxs-lookup"><span data-stu-id="e81d1-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="e81d1-111">Daugiau informacijos žr. [Naujos elektroninės ataskaitos (ER) konfigūracijos versijos kūrimas ir nusiuntimas](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="e81d1-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="e81d1-112">Taip pat turite įsitikinti, kad RCS aplinka yra parengta jūsų įmonei.</span><span class="sxs-lookup"><span data-stu-id="e81d1-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="e81d1-113">Programoje „Finance and Operations“ eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="e81d1-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e81d1-114">Jei jūsų įmonei RCS aplinka neparengta, pasirinkite **„Regulatory Services“ – išorinė konfigūracija** ir vykdykite instrukcijas, kad ją parengtumėte.</span><span class="sxs-lookup"><span data-stu-id="e81d1-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="e81d1-115">Jei RCS aplinka jūsų įmonei jau parengta, pasiekite ją naudodami puslapio URL ir pasirinkdami prisijungimo parinktį.</span><span class="sxs-lookup"><span data-stu-id="e81d1-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="e81d1-116">Konfigūracijos, kurią norite bendrinti, patikrinimas</span><span class="sxs-lookup"><span data-stu-id="e81d1-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="e81d1-117">Norėdami patikrinti, ar konfigūracija, kurią norite bendrinti, jau nusiųsta į bendrąją saugyklą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e81d1-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="e81d1-118">Darbo srityje **Elektroninės ataskaitos** prie savo konfigūracijos teikėjo pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="e81d1-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![Konfigūracijos teikėjai](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="e81d1-120">Pasirinkite **Bendroji saugykla** \> **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="e81d1-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="e81d1-121">Ieškoktie konfigūracijos, kurią norite bendrinti.</span><span class="sxs-lookup"><span data-stu-id="e81d1-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="e81d1-122">Ieškai susiaurinti galite naudoti filtravimo lauką.</span><span class="sxs-lookup"><span data-stu-id="e81d1-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="e81d1-123">Jei bendrojoje saugykloje negalite rasti konfigūracijos, atlikite veiksmus, pateiktus dalyje [Naujos elektroninės ataskaitos (ER) konfigūracijos versijos kūrimas ir nusiuntimas](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="e81d1-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="e81d1-124">ER konfigūracijų bendrinimas su išorinėmis organizacijomis</span><span class="sxs-lookup"><span data-stu-id="e81d1-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="e81d1-125">Sukūrus jūsų konfigūracijos teikėjo konfigūraciją, galite ją tiesiogiai bendrinti su išorinėmis organizacijomis, naudodami „FastTab“ konteinerį **Bendrinama su**, esantį puslapyje **Bendroji konfigūracijos saugykla**.</span><span class="sxs-lookup"><span data-stu-id="e81d1-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="e81d1-126">Darbo srityje **Elektroninės ataskaitos** prie savo konfigūracijos teikėjo pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="e81d1-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="e81d1-127">Pasirinkite **Bendroji saugykla** \> **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="e81d1-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="e81d1-128">Pasirinkite konfigūraciją, kurią norite bendrinti.</span><span class="sxs-lookup"><span data-stu-id="e81d1-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="e81d1-129">„FastTab“ konteineryje **Bendrinama su** pasirinkite **Organizacija**.</span><span class="sxs-lookup"><span data-stu-id="e81d1-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![Bendrinama su „FastTab“](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="e81d1-131">Dialogo lange įveskite išorinės organizacijos domeno pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e81d1-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![Konfigūracijos versijos bendrinimo su išorine organizacija dialogo langas](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="e81d1-133">Konfigūracija yra bendrinama su išorine organizacija ir šiai organizacijai pasiekiama bendrojoje saugykloje.</span><span class="sxs-lookup"><span data-stu-id="e81d1-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="e81d1-134">Iš ten ji gali būti importuota į organizacijos RCS egzempliorių arba į „Finance and Operations“ programų egzempliorius.</span><span class="sxs-lookup"><span data-stu-id="e81d1-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

![Su išorine organizacija bendrinama konfigūracija](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_test.com)

6. <span data-ttu-id="e81d1-136">Norėdami atšaukti anksčiau su išorine organizacija bendrintos konfigūracijos bendrinimą, pasirinkite konfigūraciją ir spustelėkite **Atšaukti bendrinimą**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e81d1-136">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>
