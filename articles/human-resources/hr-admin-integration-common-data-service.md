---
title: „Common Data Service“ integravimo konfigūravimas
description: Galite įjungti arba išjungti integravimą tarp „Common Data Service“ ir „Dynamics 365 Human Resources“. Taip pat galite peržiūrėti sinchronizavimo išsamią informaciją, išvalyti sekimo duomenis ir iš naujo sinchronizuoti objektą, kad būtų lengviau diagnozuoti duomenų problemas tarp dviejų aplinkų.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7aad8217d48917d6855046a6810fe994f5564d94
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431319"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="41043-104">„Common Data Service“ integravimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="41043-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="41043-105">Galite įjungti arba išjungti integravimą tarp „Common Data Service“ ir „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="41043-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="41043-106">Taip pat galite peržiūrėti sinchronizavimo išsamią informaciją, išvalyti sekimo duomenis ir iš naujo sinchronizuoti objektą, kad būtų lengviau diagnozuoti duomenų problemas tarp dviejų aplinkų.</span><span class="sxs-lookup"><span data-stu-id="41043-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="41043-107">Kai išjungiate integravimą, vartotojai gali vykdyti „Human Resources“ arba „Common Data Service“ keitimus, tačiau tie keitimai nėra sinchronizuojami tarp dviejų aplinkų.</span><span class="sxs-lookup"><span data-stu-id="41043-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="41043-108">Pagal numatytuosius parametrus duomenų integravimas tarp „Human Resources“ ir „Common Data Service“ yra išjungtas.</span><span class="sxs-lookup"><span data-stu-id="41043-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="41043-109">Galbūt norėsite išjungti integravimą šiais atvejais:</span><span class="sxs-lookup"><span data-stu-id="41043-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="41043-110">Jūs užpildote duomenis naudodami duomenų valdymo sistemą ir turite importuoti duomenis kelis kartus, kad jie taptų tinkamos būsenos.</span><span class="sxs-lookup"><span data-stu-id="41043-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="41043-111">Yra problemų, susijusių su duomenimis, esančiais „Human Resources“ arba „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="41043-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="41043-112">Jei išjungsite integravimą, galite panaikinti įrašą vienoje aplinkoje, jo nepanaikindami kitoje.</span><span class="sxs-lookup"><span data-stu-id="41043-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="41043-113">Kai vėl įjungsite integraciją, įrašas aplinkoje, kurioje jis nebuvo panaikintas, sinchronizuojamas atgal į aplinką, kur jis buvo panaikintas.</span><span class="sxs-lookup"><span data-stu-id="41043-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="41043-114">Sinchronizavimas prasideda, kai kitą kartą paleidžiama paketinė užduotis **„Common Data Service“ integravimo praleistų užklausų sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="41043-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="41043-115">Kai išjungiate duomenų integravimą, įsitikinkite, kad neredaguojate to paties įrašo abiejose aplinkose.</span><span class="sxs-lookup"><span data-stu-id="41043-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="41043-116">Kai vėl įjungsite integravimą, paskutinis redaguotas įrašas bus sinchronizuojamas.</span><span class="sxs-lookup"><span data-stu-id="41043-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="41043-117">Todėl, jei abiejose aplinkose neatliekate tų pačių keitimų, gali būti prarasti duomenys.</span><span class="sxs-lookup"><span data-stu-id="41043-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="41043-118">Prieiga prie „Common Data Service“ integravimo puslapio</span><span class="sxs-lookup"><span data-stu-id="41043-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="41043-119">„Human Resources“ egzemplioriuje, kur norite peržiūrėti arba konfigūruoti parametrus integravimui su „Common Data Service“, pasirinkite plytelę **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="41043-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="41043-120">[![Plytelė Sistemos administravimas](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="41043-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="41043-121">Pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="41043-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="41043-122">[![Saitų skirtukas](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="41043-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="41043-123">Dalyje **Integravimai** pasirinkite **„Common Data Service“ konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="41043-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="41043-124">[![„Common Data Service“ konfigūracijos saitas](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="41043-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="41043-125">Duomenų integravimo tarp „Human Resources“ ir „Common Data Service“ įjungimas ir išjungimas</span><span class="sxs-lookup"><span data-stu-id="41043-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="41043-126">Norėdami įjungti integravimą, nustatykite parinktį **Įjungti integravimą į „Common Data Service“** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="41043-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="41043-127">Kai įjungiate integravimą, duomenys bus sinchronizuojami kitą kartą, kai vykdoma paketinė užduotis **„Common Data Service“ integravimo praleistų užklausų sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="41043-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="41043-128">Po to, kai paketinė užduotis bus baigta, visi duomenys turėtų būti pasiekiami.</span><span class="sxs-lookup"><span data-stu-id="41043-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="41043-129">Norėdami išjungti integravimą, nustatykite parinktį į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="41043-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="41043-130">[![„Common Data Service“ integravimo įjungimas arba išjungimas](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="41043-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="41043-131">Duomenų integravimo išsamios informacijos apžvalga</span><span class="sxs-lookup"><span data-stu-id="41043-131">View data integration details</span></span>

<span data-ttu-id="41043-132">„FastTab“ **Administravimas**, esančiame puslapyje **„Common Data Service“ integravimas**, galite matyti, kaip įrašai siejami tarpusavyje tarp „Human Resources” ir „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="41043-132">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="41043-133">Norėdami peržiūrėti objekto įrašus, pažymėkite objektą lauke **CDS objekto pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="41043-133">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="41043-134">Tinklelyje rodomi visi įrašai, kurie yra siejami su pasirinktu objektu.</span><span class="sxs-lookup"><span data-stu-id="41043-134">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="41043-135">[![Objekto įrašų peržiūra](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="41043-135">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="41043-136">Šiuo metu nurodyti ne visi „Common Data Service“ objektai.</span><span class="sxs-lookup"><span data-stu-id="41043-136">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="41043-137">Tinklelyje rodomi tik tie ojektai, kurie palaiko pasirinktinius laukus.</span><span class="sxs-lookup"><span data-stu-id="41043-137">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="41043-138">Nauji objektai tampa pasiekiami nuolatiniuose „Human Resources“ leidimuose.</span><span class="sxs-lookup"><span data-stu-id="41043-138">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="41043-139">Tinklelyje yra šie laukai:</span><span class="sxs-lookup"><span data-stu-id="41043-139">The grid includes the following fields:</span></span>

- <span data-ttu-id="41043-140">**CDS objekto pavadinimas** – objekto, esančio „Common Data Service“, pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="41043-140">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="41043-141">**CDS objekto nuoroda** – identifikatorius, kurį „Common Data Service“ naudoja įrašui identifikuoti.</span><span class="sxs-lookup"><span data-stu-id="41043-141">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="41043-142">Ši vertė atitinka „Human Resources“ vertę **RecId**.</span><span class="sxs-lookup"><span data-stu-id="41043-142">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="41043-143">Galite rasti identifikatorių, kai atidarote „Common Data Service“objektą, esantį „Microsoft Excel“.</span><span class="sxs-lookup"><span data-stu-id="41043-143">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="41043-144">**„Human Resources“ objekto pavadinimas** – objektas, kuris paskutinį kartą sinchronizavo duomenis į „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="41043-144">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="41043-145">Objektas gali būti arba „Common Data Service“ priešvardis, arba kitas priešvardis.</span><span class="sxs-lookup"><span data-stu-id="41043-145">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="41043-146">**„Human Resources“ nuoroda** – **RecId** vertė, susieta su „Human Resources“ įrašu.</span><span class="sxs-lookup"><span data-stu-id="41043-146">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="41043-147">**Panaikintas iš CDS** – reikšmė, nurodanti, ar įrašas buvo panaikintas iš „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="41043-147">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="41043-148">Įrašo, esančio „Human Resources“ susiejimo šalinimas iš „Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="41043-148">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="41043-149">Jei jums kyla problemų sinchronizuojant duomenis tarp „Human Resources“ ir „Common Data Service”, galite jas išspręsti išvalydami sekimą ir leisdami iš naujo nustatyti sekimo lentelę.</span><span class="sxs-lookup"><span data-stu-id="41043-149">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="41043-150">Jei pašalinsite susiejimą ir pakeisite arba panaikininsite įrašą, esantį „Common Data Service“, keitimai nebus sinchronizuojami su „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="41043-150">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="41043-151">Atlikus keitimų programoje „Human Resources“, sukuriamas naujas sekimo įrašas ir atnaujinamas įrašas, esantis „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="41043-151">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="41043-152">Norėdami pašalinti įrašo susiejimą tarp „Human Resources“ ir „Common Data Service“, lauke **CDS objekto pavadinimas** pasirinkite objektą, tada pasirinkite **Valyti sekimo informaciją**.</span><span class="sxs-lookup"><span data-stu-id="41043-152">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="41043-153">[![Sekimo informacijos valymas](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="41043-153">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="41043-154">Išvalę sekimą, norėdami vykdyti visišką objekto sinchronizavimą, žr. tolesnę procedūrą.</span><span class="sxs-lookup"><span data-stu-id="41043-154">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="41043-155">Objekto sinchronizavimas tarp „Human Resources“ ir „Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="41043-155">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="41043-156">Naudokite šią procedūrą, kai:</span><span class="sxs-lookup"><span data-stu-id="41043-156">Use this procedure when:</span></span>

- <span data-ttu-id="41043-157">„Common Data Service” keitimai atliekami per ilgai, kad būtų rodomi programoje „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="41043-157">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="41043-158">Išvalę sekimą turite atnaujinti sekimo lentelę.</span><span class="sxs-lookup"><span data-stu-id="41043-158">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="41043-159">Norėdami vykdyti visišką objekto sinchronizavimą tarp „Human Resources“ ir „Common Data Service”, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="41043-159">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="41043-160">Lauke **CDS objekto pavadinimas** pasirinkite objektą.</span><span class="sxs-lookup"><span data-stu-id="41043-160">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="41043-161">Pasirinkite **Sinchronizuoti dabar**.</span><span class="sxs-lookup"><span data-stu-id="41043-161">Select **Sync now**.</span></span>

<span data-ttu-id="41043-162">[![Visiško sinchronizavimo paleidimas](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="41043-162">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


