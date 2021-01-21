---
title: ER perkėlimo valymas
description: Šioje temoje paaiškinama, kaip galima naudoti funkciją ER perkėlimo valymas problemoms, esančioms ER šablonuose, išspręsti.
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 090badd48785dfacf5942426d0fe53629f3c0cda
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321807"
---
# <a name="er-migration-cleanup"></a><span data-ttu-id="911bd-103">ER perkėlimo valymas</span><span class="sxs-lookup"><span data-stu-id="911bd-103">ER migration cleanup</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="911bd-104">Valdydami „Finance“ egzempliorius, galbūt nuspręsite perkelti jūsų dabartinį egzempliorių į kitą vietą.</span><span class="sxs-lookup"><span data-stu-id="911bd-104">When you manage your Finance instances, you might decide to migrate your current instance to another location.</span></span> <span data-ttu-id="911bd-105">Pavyzdžiui, galite perkelti gamybos egzempliorių į naują smėlio dėžės aplinką.</span><span class="sxs-lookup"><span data-stu-id="911bd-105">For example, you might migrate your production instance to a new sandbox environment.</span></span> <span data-ttu-id="911bd-106">Jei sukonfigūruosite, kad Elektroninių ataskaitų (ER) sistema saugotų šablonus „Microsoft Azure” didelių dvejetainių objektų saugykloje, **DocuValue** lentelėje, esančioje naujojoje smėlio dėžės aplinkoje, bus nuoroda į didelių dvejetainių objektų saugyklos egzempliorių gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="911bd-106">If you configured the Electronic reporting (ER) framework to store templates in Microsoft Azure Blob storage, the **DocuValue** table in the new sandbox environment refers to the instance of Blob storage in the production environment.</span></span> <span data-ttu-id="911bd-107">Tačiau šio egzemplioriaus negalima pasiekti iš smėlio dėžės aplinkos, nes perkėlimo procesas nepalaiko artefaktų perkėlimo didelių dvejetainių objektų saugykloje.</span><span class="sxs-lookup"><span data-stu-id="911bd-107">However, this instance can't be accessed from the sandbox environment because the migration process doesn't support the migration of artifacts in Blob storage.</span></span> <span data-ttu-id="911bd-108">Vietoje to tikimasi, kad naujoje smėlio dėžės aplinkoje nurodysite smėlio dėžės aplinkos didelių dvejetainių objektų saugyklos egzempliorių, kuris dar negauna ER šablonų.</span><span class="sxs-lookup"><span data-stu-id="911bd-108">Rather, it's expected that in the new sandbox environment, you refer to the instance of Blob storage in the sandbox environment that does not yet obtain the ER templates.</span></span>

<span data-ttu-id="911bd-109">Pasirinkus ER formatą, kuris naudoja šabloną generuoti verslo dokumentams, įvyksta išimtis ir informuojama apie trūkstamą šabloną.</span><span class="sxs-lookup"><span data-stu-id="911bd-109">If you try to run an ER format that uses a template to generate business documents, an exception occurs, and you're notified about the missing template.</span></span> <span data-ttu-id="911bd-110">Taip pat rekomenduojama naudoti parinktį ER perkėlimo valymas, kad panaikintumėte, o tada iš naujo importuotumėte ER konfigūraciją, kurioje yra šablonas.</span><span class="sxs-lookup"><span data-stu-id="911bd-110">You're also guided to use the ER migration cleanup option to delete and then re-import the ER format configuration that contains the template.</span></span>

<span data-ttu-id="911bd-111">[![ER formato vykdymas](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)</span><span class="sxs-lookup"><span data-stu-id="911bd-111">[![Running an ER format](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)</span></span>

<span data-ttu-id="911bd-112">Gausite panašią klaidą, jei pereisite į puslapį **Konfigūracijos** (**Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**) ir konfigūracijų medyje bandysite panaikinti ER formato konfigūraciją, naudojančią šabloną.</span><span class="sxs-lookup"><span data-stu-id="911bd-112">You will receive a similar error if you navigate to the **Configurations** page (**Organization administration** \> **Electronic reporting** \> **Configurations**) and in the configurations tree, try to delete an ER format configuration that uses a template.</span></span>

<span data-ttu-id="911bd-113">[![ER formato naikinimas](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)</span><span class="sxs-lookup"><span data-stu-id="911bd-113">[![Deletion an ER format](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)</span></span>

<span data-ttu-id="911bd-114">Atlikite toliau pateiktus veiksmus, kad išspręstumėte ER šablonų problemas, kurių negalite pasiekti.</span><span class="sxs-lookup"><span data-stu-id="911bd-114">Complete the following steps to resolve issues with ER templates that you are unable to access.</span></span>

1.  <span data-ttu-id="911bd-115">Eikite į puslapį **Organizacijos administravimas** \> **Periodinis** \> **Perkėlimo valymas**.</span><span class="sxs-lookup"><span data-stu-id="911bd-115">Go to **Organization administration** \> **Periodic** \> **Migration cleanup** page.</span></span>
2.  <span data-ttu-id="911bd-116">Pasirinkite ER formato konfigūraciją, kurios negalima įvykdyti arba panaikinti.</span><span class="sxs-lookup"><span data-stu-id="911bd-116">Select an ER format configuration that can’t be executed or deleted.</span></span>
3.  <span data-ttu-id="911bd-117">Pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="911bd-117">Select **Delete**.</span></span>
4.  <span data-ttu-id="911bd-118">Patvirtinkite pasirinktos ER formato konfigūracijos naikinimą.</span><span class="sxs-lookup"><span data-stu-id="911bd-118">Confirm the deletion of the selected ER format configuration.</span></span>
5.  <span data-ttu-id="911bd-119">[Importuokite](download-electronic-reporting-configuration-lcs.md) panaikintas ER formato konfigūracijas į dabartinį „Finance“ egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="911bd-119">[Import](download-electronic-reporting-configuration-lcs.md) the deleted ER format configuration to the current Finance instance.</span></span>

## <a name="applicability"></a><span data-ttu-id="911bd-120">Taikymas</span><span class="sxs-lookup"><span data-stu-id="911bd-120">Applicability</span></span>

> <span data-ttu-id="911bd-121">[Svarbu] Parinktis **Perkėlimo valymas** taikoma tik toms ER formato konfigūracijoms, kuriose yra neprieinamų ER šablonų.</span><span class="sxs-lookup"><span data-stu-id="911bd-121">[Important] The **Migration cleanup** option is targeted only for ER format configurations that contain non-accessible ER templates.</span></span> <span data-ttu-id="911bd-122">Kai panaikinate ER formato konfigūraciją naudodami parinktį **Perkėlimo valymas**, ER panaikina šablonus, susijusius su konfigūracijos artefaktais vienintelėje programos duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="911bd-122">When you delete an ER format configuration by using the **Migration cleanup** option, ER deletes the templates that are related to the configuration artifacts in the only application database.</span></span> <span data-ttu-id="911bd-123">Tinkamų fizinių failų didelių dvejetainių objektų saugykloje buvimas netikrinamas.</span><span class="sxs-lookup"><span data-stu-id="911bd-123">The existence of the appropriate physical files in Blob storage are not validated.</span></span> <span data-ttu-id="911bd-124">Vietoje to laikoma, kad jų nėra.</span><span class="sxs-lookup"><span data-stu-id="911bd-124">Instead, it is assumed that there are none.</span></span> <span data-ttu-id="911bd-125">Todėl nenaudokite parinkties **Perkėlimo valymas** kaip ER konfigūracijos naikinimo parinkties puslapyje **Konfigūracijos** alternatyvos.</span><span class="sxs-lookup"><span data-stu-id="911bd-125">Therefore, do not use the **Migration cleanup** option as an alternative to the ER configuration deletion option on the **Configurations** page.</span></span> <span data-ttu-id="911bd-126">Naudokite parinktį **Perkėlimo valymas** tik tada, kai ER konfigūracijos naikinimo parinktis puslapyje **Konfigūracijos** žlunga.</span><span class="sxs-lookup"><span data-stu-id="911bd-126">Use the **Migration cleanup** option only when the ER configuration deletion option on the **Configurations** page failed.</span></span>
>
> <span data-ttu-id="911bd-127">Jei naudojate parinktį **Perkėlimo valymas** panaikinti ER formato konfigūraciją, kai nurodytas šablonas pasiekiamas didelių dvejetainių objektų saugykloje, panaikinate tik susijusius konfigūracijos artefaktus programos duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="911bd-127">If you use the **Migration cleanup** option to delete an ER format configuration when the referred template is available in the Blob storage, you only delete related configuration artifacts in the application database.</span></span> <span data-ttu-id="911bd-128">Fizinis šablono failas išlieka didelių dvejetainių objektų saugykloje.</span><span class="sxs-lookup"><span data-stu-id="911bd-128">The physical file of the template in the Blob storage remains.</span></span> <span data-ttu-id="911bd-129">Didelių dvejetainių objektų saugykloje nebeleidžiamas failų perrašymas.</span><span class="sxs-lookup"><span data-stu-id="911bd-129">File overwriting in Blob storage is no longer allowed.</span></span> <span data-ttu-id="911bd-130">Daugiau informacijos rasite [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217).</span><span class="sxs-lookup"><span data-stu-id="911bd-130">For more information, see [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217).</span></span> <span data-ttu-id="911bd-131">Be to, nebegalėsite iš naujo importuoti konfigūracijų, panaikintų šioje aplinkoje naudojant parinktį Perkėlimo valymas.</span><span class="sxs-lookup"><span data-stu-id="911bd-131">Additionally, you will no longer be able to re-import the configurations deleted by using the Migration cleanup in this environment.</span></span> <span data-ttu-id="911bd-132">Norėdami išspręsti šią problemą, turite rasti atitinkamą failą didelių dvejetainių objektų saugykloje ir jį panaikinti neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="911bd-132">To resolve this issue, you need to find the corresponding file in Blob storage and manually delete it.</span></span>

<span data-ttu-id="911bd-133">[![ER formato importavimas](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)</span><span class="sxs-lookup"><span data-stu-id="911bd-133">[![Importing an ER format](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)</span></span>

<span data-ttu-id="911bd-134">Panaši problema gali kilti, jei perkeliate programos egzempliorių į kitą vietą, kuri buvo naudojama kaip perkėlimo paskirtis daugiau nei vieną kartą ir kurios didelių dvejetainių objektų saugykloje jau yra ER šablono failai.</span><span class="sxs-lookup"><span data-stu-id="911bd-134">A similar issue may occur if you migrate your application instance to another location that has been used as a migration target more than once and for which the Blob storage already contains ER template files.</span></span>

<span data-ttu-id="911bd-135">Kadangi gali būti kelios ER formato konfigūracijos, šis procesas gali užtrukti.</span><span class="sxs-lookup"><span data-stu-id="911bd-135">Because you can have several ER format configurations, this process can be time consuming.</span></span> <span data-ttu-id="911bd-136">Todėl pageidaujama naudoti funkciją [ER šablonų atsarginių kopijų saugykla](er-backup-storage-templates.md) automatiškai atkurti šablonus, kuriuose yra neveikiančių nuorodų.</span><span class="sxs-lookup"><span data-stu-id="911bd-136">Therefore, using the [Backup storage of ER templates](er-backup-storage-templates.md) feature to automatically recover templates with broken references is preferred.</span></span>