---
title: Įjungti kiekio ir neatitikties valdymą
description: Šioje temoje pateikiama kokybės ir neatitikties valdymo funkcijų nustatymo ir konfigūravimo proceso „Microsoft Dynamics 365 Supply Chain Management“ apžvalga.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956259"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="840e0-103">Įjungti kiekio ir neatitikties valdymą</span><span class="sxs-lookup"><span data-stu-id="840e0-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="840e0-104">Šioje temoje pateikiama kokybės ir neatitikties valdymo funkcijų nustatymo ir konfigūravimo proceso „Microsoft Dynamics 365 Supply Chain Management“ apžvalga.</span><span class="sxs-lookup"><span data-stu-id="840e0-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="840e0-105">Įjungti kiekio ir neatitikties valdymą</span><span class="sxs-lookup"><span data-stu-id="840e0-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="840e0-106">Norėdami įjungti kokybės valdymą sistemoje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="840e0-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="840e0-107">Eikite į **Atsargų valdymas\> Sąranka \> Atsargų ir sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="840e0-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="840e0-108">Skirtuke **Kokybės** valdymas nustatykite parinktį Naudoti kokybės valdymą **kaip** *Taip*.</span><span class="sxs-lookup"><span data-stu-id="840e0-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="840e0-109">Lauke **Valandinis tarifas** įveskite valandinį darbo tarifą vietine valiuta.</span><span class="sxs-lookup"><span data-stu-id="840e0-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="840e0-110">Valandinis tarifas naudojamas apskaičiuojant su neatitikimu susijusias operacijų išlaidas.</span><span class="sxs-lookup"><span data-stu-id="840e0-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="840e0-111">Valandinis tarifas ir apskaičiuotos išlaidos suteikia nuorodinės informacijos apie neatitiktį.</span><span class="sxs-lookup"><span data-stu-id="840e0-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="840e0-112">Jie nesąveikauja su kitomis funkcijomis.</span><span class="sxs-lookup"><span data-stu-id="840e0-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="840e0-113">Rinkitės **Ataskaitos nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="840e0-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="840e0-114">Pridėti naujų eilučių įvairiems ataskaitų tipams ir pasirinkti dokumento tipą, kuris bus naudojamas kiekvienoje ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="840e0-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="840e0-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="840e0-115">Close the page.</span></span>
1. <span data-ttu-id="840e0-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="840e0-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="840e0-117">Kokybės valdymo konfigūravimo procesas</span><span class="sxs-lookup"><span data-stu-id="840e0-117">Quality management configuration process</span></span>

<span data-ttu-id="840e0-118">Prieš pradėdami naudoti kokybės valdymo funkcijas ir generuoti kokybės užsakymus, turite sukonfigūruoti sistemą ir būtinuosius komponentus.</span><span class="sxs-lookup"><span data-stu-id="840e0-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="840e0-119">Čia pateikiamas veiksmų, kurių reikia norint konfigūruoti kokybės valdymą, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="840e0-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="840e0-120">[Įjungti kiekio ir neatitikties valdymą](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="840e0-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="840e0-121">Pasirinktinai: [konfigūruokite bandymo](quality-test-instruments.md) priemones.</span><span class="sxs-lookup"><span data-stu-id="840e0-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="840e0-122">[Tarifų konfigūravimas](quality-tests.md).</span><span class="sxs-lookup"><span data-stu-id="840e0-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="840e0-123">[Konfigūruokite bandymo kintamuosius ir](quality-test-variables.md) rezultatus.</span><span class="sxs-lookup"><span data-stu-id="840e0-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="840e0-124">[Konfigūruoti bandymų](quality-test-groups.md) grupes.</span><span class="sxs-lookup"><span data-stu-id="840e0-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="840e0-125">Pasirinktinai: [konfigūruokite kokybės grupes ir sąsają su](quality-groups.md) produktais.</span><span class="sxs-lookup"><span data-stu-id="840e0-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="840e0-126">Pasirinktinai: [sukonfigūruokite kokybės](quality-associations.md) susiejimus.</span><span class="sxs-lookup"><span data-stu-id="840e0-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="840e0-127">Baigę konfigūruoti galite pradėti kurti ir apdoroti kokybės užsakymus.</span><span class="sxs-lookup"><span data-stu-id="840e0-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="840e0-128">Daugiau informacijos apie tai, kaip kurti ir dirbti su kokybės užsakymais rasite [Kokybės užsakymai](quality-orders.md).</span><span class="sxs-lookup"><span data-stu-id="840e0-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="840e0-129">Neatitikties valdymo konfigūravimo procesas</span><span class="sxs-lookup"><span data-stu-id="840e0-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="840e0-130">Prieš pradėdami naudoti neatitikties valdymo funkcijas ir generuoti neatitikties užsakymus, turite sukonfigūruoti sistemą ir būtinuosius komponentus.</span><span class="sxs-lookup"><span data-stu-id="840e0-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="840e0-131">Čia pateikiamas veiksmų, kurių reikia norint konfigūruoti neatitikties valdymą, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="840e0-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="840e0-132">[Įjungti kiekio ir neatitikties valdymą](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="840e0-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="840e0-133">[Konfigūruoti darbuotojus, atsakingus už neatitikties](quality-responsible-workers.md) tvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="840e0-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="840e0-134">[Konfigūruokite problemų](quality-problem-types.md) tipus.</span><span class="sxs-lookup"><span data-stu-id="840e0-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="840e0-135">[Konfigūruokite sulaikymo](quality-quarantine-zones.md) zonas.</span><span class="sxs-lookup"><span data-stu-id="840e0-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="840e0-136">[Konfigūruoti diagnostinius tipus](quality-diagnostic-types.md).</span><span class="sxs-lookup"><span data-stu-id="840e0-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="840e0-137">[Operacijų konfigūravimas](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="840e0-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="840e0-138">Pasirinktinai: [sukonfigūruokite kokybės](quality-charges.md) mokesčius.</span><span class="sxs-lookup"><span data-stu-id="840e0-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="840e0-139">Baigę konfigūruoti galite pradėti kurti ir apdoroti neatitikties užsakymus.</span><span class="sxs-lookup"><span data-stu-id="840e0-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="840e0-140">Daugiau informacijos apie tai, kaip kurti ir dirbti su neatitikimais, žr. dalį [Neatitikčių kūrimas ir darbas su jomis](tasks/create-process-non-conformance.md).</span><span class="sxs-lookup"><span data-stu-id="840e0-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="840e0-141">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="840e0-141">Additional resources</span></span>

- [<span data-ttu-id="840e0-142">Kokybės valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="840e0-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="840e0-143">Įjungti kiekio ir neatitikties valdymą</span><span class="sxs-lookup"><span data-stu-id="840e0-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="840e0-144">Sandėlio procesų kokybės valdymas</span><span class="sxs-lookup"><span data-stu-id="840e0-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
