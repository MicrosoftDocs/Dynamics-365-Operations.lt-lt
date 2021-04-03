---
title: Elektroninių ataskaitų (ER) konfigūracijų ciklo valdymas
description: Šioje temoje aprašoma, kaip valdyti „Microsoft Dynamics 365 Finance“ sprendimo elektroninių ataskaitų (ER) konfigūracijų ciklą.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b1b5ac8e256835332a4c53ed2872ee609253ad9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568730"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="96450-103">Elektroninių ataskaitų (ER) konfigūracijų ciklo valdymas</span><span class="sxs-lookup"><span data-stu-id="96450-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96450-104">Šioje temoje aprašoma, kaip valdyti „Microsoft Dynamics 365 Finance“ elektroninių ataskaitų (ER) konfigūracijų ciklą.</span><span class="sxs-lookup"><span data-stu-id="96450-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for Microsoft Dynamics 365 Finance.</span></span>

## <a name="overview"></a><span data-ttu-id="96450-105">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="96450-105">Overview</span></span>

<span data-ttu-id="96450-106">Elektroninės ataskaitos (ER) yra mechanizmas, palaikantis įstatymiškai privalomus ir šaliai būdingus elektroninius dokumentus.</span><span class="sxs-lookup"><span data-stu-id="96450-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents.</span></span> <span data-ttu-id="96450-107">Apskritai, ER suteikia galimybę atlikti tolesnes su vienu elektroniniu dokumentu susijusias užduotis.</span><span class="sxs-lookup"><span data-stu-id="96450-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="96450-108">Išsamią informaciją žr. [Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="96450-108">For more details, see [Electronic reporting (ER) overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="96450-109">Sukurti elektroninio dokumento šabloną.</span><span class="sxs-lookup"><span data-stu-id="96450-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="96450-110">Identifikuoti toliau nurodytus reikiamus duomenų šaltinius, kuriuos galima pateikti dokumente.</span><span class="sxs-lookup"><span data-stu-id="96450-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="96450-111">Pagrindiniai duomenys, pvz., duomenų lentelės, duomenų objektai ir klasės.</span><span class="sxs-lookup"><span data-stu-id="96450-111">Underlying data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="96450-112">Konkretaus proceso ypatybės, pvz., vykdymo data ir laikas bei laiko juosta.</span><span class="sxs-lookup"><span data-stu-id="96450-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="96450-113">Vartotojo įvesties parametrai, kuriuos vykdymo metu nurodė galutinis vartotojas.</span><span class="sxs-lookup"><span data-stu-id="96450-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="96450-114">Apibrėžti reikiamus dokumento elementus ir jų topologiją siekiant nurodyti galutinį dokumento formatą.</span><span class="sxs-lookup"><span data-stu-id="96450-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="96450-115">Konfigūruoti norimą duomenų srautą iš pasirinktų duomenų šaltinių į nustatytus dokumento elementus (naudojant duomenų šaltinių susiejimus su dokumento formato komponentais) ir nurodyti proceso kontrolės logiką.</span><span class="sxs-lookup"><span data-stu-id="96450-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="96450-116">Sukurkite šabloną, kurį būtų galima naudoti kituose egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="96450-116">Make a template available so that it can be used in other instances:</span></span>

    - <span data-ttu-id="96450-117">Sukurtą dokumento šabloną transformuokite į ER konfigūraciją ir eksportuokite iš dabartinio programos egzemplioriaus kaip XML paketą, kurį būtų galima išsaugoti vietoje arba LCS.</span><span class="sxs-lookup"><span data-stu-id="96450-117">Transform a document template that was created into an ER configuration, and export the configuration from the current application instance as an XML package that can be stored either locally or in LCS.</span></span>
    - <span data-ttu-id="96450-118">Transformuokite ER konfigūraciją programos dokumento šabloną.</span><span class="sxs-lookup"><span data-stu-id="96450-118">Transform an ER configuration into an application document template.</span></span>
    - <span data-ttu-id="96450-119">Importuokite XML paketą, saugomą vietoje arba LCS, į dabartinį egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="96450-119">Import an XML package that is stored either locally or in LCS into the current instance.</span></span>

- <span data-ttu-id="96450-120">Tinkinti elektroninio dokumento šabloną.</span><span class="sxs-lookup"><span data-stu-id="96450-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="96450-121">Šabloną iš LCS perduokite į dabartinį egzempliorių kaip ER konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="96450-121">Bring a template from LCS into the current instance as an ER configuration.</span></span>
    - <span data-ttu-id="96450-122">Kurti pasirinktinę ER konfigūracijos versiją ir išsaugoti nuorodą į pagrindinę versiją.</span><span class="sxs-lookup"><span data-stu-id="96450-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="96450-123">Šabloną integruokite su konkrečiu verslo procesu, kad jį būtų galima naudoti programoje.</span><span class="sxs-lookup"><span data-stu-id="96450-123">Integrate a template with a particular business process, so that it's available in the application:</span></span>

    - <span data-ttu-id="96450-124">Konfigūruokite parametrus, kad programa pradėtų naudoti ER konfigūraciją, ją nurodant su procesu susijusiu parametru.</span><span class="sxs-lookup"><span data-stu-id="96450-124">Configure settings so that the application starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="96450-125">Pvz., į ER konfigūraciją nurodyti konkrečiu mokėtinų sumų mokėjimo metodu, kad būtų generuojamas elektroninio mokėjimo pranešimas apie SF apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="96450-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="96450-126">Šabloną naudoti konkrečiame verslo procese.</span><span class="sxs-lookup"><span data-stu-id="96450-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="96450-127">ER konfigūraciją paleisti konkrečiame verslo procese.</span><span class="sxs-lookup"><span data-stu-id="96450-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="96450-128">Pvz., siekiant generuoti SF apdorojimo elektroninio mokėjimo pranešimą, kai pasirenkamas mokėjimo metodas, nurodantis į ER konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="96450-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="96450-129">Koncepcijos</span><span class="sxs-lookup"><span data-stu-id="96450-129">Concepts</span></span>
<span data-ttu-id="96450-130">Su ER konfigūracijos ciklu susieti tolesni vaidmenys ir susijusios veiklos.</span><span class="sxs-lookup"><span data-stu-id="96450-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="96450-131">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="96450-131">Role</span></span>                                       | <span data-ttu-id="96450-132">Veikla</span><span class="sxs-lookup"><span data-stu-id="96450-132">Activities</span></span>                                                      | <span data-ttu-id="96450-133">aprašymas</span><span class="sxs-lookup"><span data-stu-id="96450-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="96450-134">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="96450-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="96450-135">Kurti ir valdyti ER komponentus (modelius ir formatus).</span><span class="sxs-lookup"><span data-stu-id="96450-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="96450-136">Verslininkas, kuriantis konkrečių ER domenų duomenų modelius, kuria reikiamus elektroninių dokumentų šablonus ir atitinkamai juos susieja.</span><span class="sxs-lookup"><span data-stu-id="96450-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="96450-137">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="96450-137">Electronic reporting developer</span></span>             | <span data-ttu-id="96450-138">Kurti ir valdyti duomenų modelių susiejimus.</span><span class="sxs-lookup"><span data-stu-id="96450-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="96450-139">Specialistas, kuris parenka reikiamus „Finance‟ duomenų šaltinius ir juos susieja su konkrečių ER domenų duomenų modeliais.</span><span class="sxs-lookup"><span data-stu-id="96450-139">A specialist who selects the required Finance data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="96450-140">Apskaitos prižiūrėtojas</span><span class="sxs-lookup"><span data-stu-id="96450-140">Accounting supervisor</span></span>                      | <span data-ttu-id="96450-141">Konfigūruoti su procesu susijusius parametrus, nurodančius į ER artefaktus.</span><span class="sxs-lookup"><span data-stu-id="96450-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="96450-142">Pavyzdžiui, **Apskaitos prižiūrėtojo** vaidmuo, leidžiantis ER konfigūracijos parametrus naudoti su konkrečiu mokėtinų sumų mokėjimo metodu, kad būtų galima generuoti elektroninio mokėjimo pranešimą apie SF apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="96450-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="96450-143">Mokėtinų sumų mokėjimo klerkas</span><span class="sxs-lookup"><span data-stu-id="96450-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="96450-144">ER artefaktus naudoti konkrečiame verslo procese.</span><span class="sxs-lookup"><span data-stu-id="96450-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="96450-145">Pvz., **Mokėtinų sumų mokėjimo klerko** vaidmuo, leidžiantis pagal sukonfigūruotą konkretaus mokėjimo metodo ER formatą generuoti elektroninio mokėjimo pranešimus apie SF apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="96450-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="96450-146">ER konfigūracijos plėtros ciklas</span><span class="sxs-lookup"><span data-stu-id="96450-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="96450-147">Dėl tolesnių su ER susijusių priežasčių rekomenduojame ER konfigūracijas kurti programavimo aplinkoje kaip atskirame „Finance and Operations“ egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="96450-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="96450-148">Vartotojai, kurių vaidmuo yra **Elektroninių ataskaitų kūrėjas** arba **Elektroninių ataskaitų funkcijų konsultantas**, gali konfigūracijas redaguoti ir vykdyti bandymams.</span><span class="sxs-lookup"><span data-stu-id="96450-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="96450-149">Tokiu atveju gali būti iškviesti klasių ir lentelių, kurios gali būti potencialiai kenksmingos verslo duomenims ir egzemplioriaus naudojimo efektyvumui, metodai.</span><span class="sxs-lookup"><span data-stu-id="96450-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the instance.</span></span>
- <span data-ttu-id="96450-150">Įvesties vietos neapriboja klasių ir lentelių kaip ER konfigūracijų ER duomenų šaltinių metodų iškvietimų ir jie yra užregistruoti įmonės turinyje.</span><span class="sxs-lookup"><span data-stu-id="96450-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by entry points and logged company content.</span></span> <span data-ttu-id="96450-151">Todėl slaptus verslo duomenis gali pasiekti vartotojai, kurių vaidmuo yra **Elektroninių ataskaitų kūrėjas** arba **Elektroninių ataskaitų funkcijų konsultantas**.</span><span class="sxs-lookup"><span data-stu-id="96450-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="96450-152">Programavimo aplinkoje sukurtas ER konfigūracijas galima nusiųsti į tikrinimo aplinką konfigūracijai (tinkamam proceso integravimui, rezultatų tikslumui ir našumui) įvertinti ir kokybei (vaidmenų valdomų prieigos teisių teisingumui ir pareigų atskyrimui) užtikrinti.</span><span class="sxs-lookup"><span data-stu-id="96450-152">ER configurations that are designed in the development environment can be uploaded to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="96450-153">Šiuo tikslu galima naudoti funkcijas, leidžiančias mainytis ER konfigūracijomis.</span><span class="sxs-lookup"><span data-stu-id="96450-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="96450-154">Galiausiai patvirtintas ER konfigūracijas galima įkelti į LCS, kur jas būtų galima bendrinti su paslaugų prenumeratoriais arba į gamybos aplinką ir naudoti viduje, kaip parodyta tolesniame paveikslėlyje.</span><span class="sxs-lookup"><span data-stu-id="96450-154">Finally, proven ER configurations can be uploaded either to LCS, where they can be shared with service subscribers, or to the production environment for internal use, such as shown in the following illustration.</span></span>

![ER konfigūracijos ciklas](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a><span data-ttu-id="96450-156">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="96450-156">Additional resources</span></span>

[<span data-ttu-id="96450-157">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="96450-157">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]