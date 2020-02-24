---
title: Konfigūruoti „Common Data Service“ integravimą
description: Galite įjungti arba išjungti integravimą tarp „Common Data Service“ ir „Microsoft Dynamics 365 Human Resources“ egzemplioriaus. Taip pat galite peržiūrėti sinchronizavimo išsamią informaciją, išvalyti sekimo duomenis ir iš naujo sinchronizuoti objektą, kad būtų lengviau diagnozuoti duomenų problemas tarp dviejų aplinkų.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009912"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="694d4-104">Konfigūruoti „Common Data Service“ integravimą</span><span class="sxs-lookup"><span data-stu-id="694d4-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="694d4-105">Galite įjungti arba išjungti integravimą tarp „Common Data Service“ ir „Microsoft Dynamics 365 Human Resources“ egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="694d4-105">You can turn integration between Common Data Service and an instance of Microsoft Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="694d4-106">Taip pat galite peržiūrėti sinchronizavimo išsamią informaciją, išvalyti sekimo duomenis ir iš naujo sinchronizuoti objektą, kad būtų lengviau diagnozuoti duomenų problemas tarp dviejų aplinkų.</span><span class="sxs-lookup"><span data-stu-id="694d4-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="694d4-107">Kai išjungiate integravimą, vartotojai gali vykdyti „Human Resources“ arba „Common Data Service“ keitimus, tačiau tie keitimai nėra sinchronizuojami tarp dviejų aplinkų.</span><span class="sxs-lookup"><span data-stu-id="694d4-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="694d4-108">Pagal numatytuosius parametrus integravimas tarp „Human Resources“ ir „Common Data Service“ yra arba išjungtas, arba įjungtas, atsižvelgiant į tai, ar aplinkose yra demonstracinių duomenų:</span><span class="sxs-lookup"><span data-stu-id="694d4-108">By default, integration between Human Resources and Common Data Service is turned either off or on, depending on the presence of demo data in the environments:</span></span>

- <span data-ttu-id="694d4-109">**Išjungta** naujoms aplinkoms, kuriose nėra demonstracinių duomenų</span><span class="sxs-lookup"><span data-stu-id="694d4-109">**Off** for new environments that don't include demo data</span></span>
- <span data-ttu-id="694d4-110">**Įjungta** naujoms aplinkoms, kuriose yra demonstracinių duomenų</span><span class="sxs-lookup"><span data-stu-id="694d4-110">**On** for new environments that include demo data</span></span>

<span data-ttu-id="694d4-111">Naujos aplinkos, kuriose yra demonstracinių duomenų, pradės sinchronizuoti duomenis, kai jie parengiami.</span><span class="sxs-lookup"><span data-stu-id="694d4-111">New environments that include demo data will start to sync data when they are provisioned.</span></span>

<span data-ttu-id="694d4-112">Galbūt norėsite išjungti integravimą šiais atvejais:</span><span class="sxs-lookup"><span data-stu-id="694d4-112">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="694d4-113">Jūs užpildote duomenis naudodami duomenų valdymo sistemą ir turite importuoti duomenis kelis kartus, kad jie taptų tinkamos būsenos.</span><span class="sxs-lookup"><span data-stu-id="694d4-113">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="694d4-114">Yra problemų, susijusių su duomenimis, esančiais „Human Resources“ arba „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="694d4-114">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="694d4-115">Jei išjungsite integravimą, galite panaikinti įrašą vienoje aplinkoje, jo nepanaikindami kitoje.</span><span class="sxs-lookup"><span data-stu-id="694d4-115">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="694d4-116">Kai vėl įjungsite integraciją, įrašas aplinkoje, kurioje jis nebuvo panaikintas, bus sinchronizuojamas atgal į aplinką, kur jis buvo panaikintas.</span><span class="sxs-lookup"><span data-stu-id="694d4-116">When you turn integration back on, the record in the environment where it wasn't deleted will be synced back to the environment where it was deleted.</span></span> <span data-ttu-id="694d4-117">Sinchronizavimas prasideda, kai kitą kartą paleidžiama paketinė užduotis **„Common Data Service“ integravimo praleistų užklausų sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="694d4-117">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="694d4-118">Kai išjungiate duomenų integravimą, įsitikinkite, kad neredaguojate to paties įrašo abiejose aplinkose.</span><span class="sxs-lookup"><span data-stu-id="694d4-118">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="694d4-119">Kai vėl įjungsite integravimą, paskutinis redaguotas įrašas bus sinchronizuojamas.</span><span class="sxs-lookup"><span data-stu-id="694d4-119">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="694d4-120">Todėl, jei abiejose aplinkose neatliekate tų pačių keitimų, gali būti prarasti duomenys.</span><span class="sxs-lookup"><span data-stu-id="694d4-120">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="694d4-121">Prieiga prie „Common Data Service“ integravimo puslapio</span><span class="sxs-lookup"><span data-stu-id="694d4-121">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="694d4-122">„Human Resources“ egzemplioriuje, kur norite peržiūrėti arba konfigūruoti parametrus integravimui su „Common Data Service“, pasirinkite plytelę **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="694d4-122">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="694d4-123">[![Plytelė Sistemos administravimas](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="694d4-123">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="694d4-124">Pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="694d4-124">Select the **Links** tab.</span></span>

    <span data-ttu-id="694d4-125">[![Saitų skirtukas](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="694d4-125">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="694d4-126">Dalyje **Integravimai** pasirinkite **„Common Data Service“ konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="694d4-126">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="694d4-127">[![„Common Data Service“ konfigūracijos saitas](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="694d4-127">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="694d4-128">Duomenų integravimo tarp „Human Resources“ ir „Common Data Service“ įjungimas ir išjungimas</span><span class="sxs-lookup"><span data-stu-id="694d4-128">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="694d4-129">Norėdami įjungti integravimą, nustatykite parinktį **Įjungti integravimą į „Common Data Service“** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="694d4-129">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="694d4-130">Kai įjungiate integravimą, duomenys bus sinchronizuojami kitą kartą, kai vykdoma paketinė užduotis **„Common Data Service“ integravimo praleistų užklausų sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="694d4-130">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="694d4-131">Po to, kai paketinė užduotis bus baigta, visi duomenys turėtų būti pasiekiami.</span><span class="sxs-lookup"><span data-stu-id="694d4-131">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="694d4-132">Norėdami išjungti integravimą, nustatykite parinktį į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="694d4-132">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="694d4-133">[![„Common Data Service“ integravimo įjungimas arba išjungimas](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="694d4-133">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="694d4-134">Duomenų integravimo išsamios informacijos apžvalga</span><span class="sxs-lookup"><span data-stu-id="694d4-134">View data integration details</span></span>

<span data-ttu-id="694d4-135">„FastTab“ **Administravimas**, esančiame puslapyje **„Common Data Service“ integravimas**, galite matyti, kaip įrašai siejami tarpusavyje tarp „Human Resources” ir „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="694d4-135">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="694d4-136">Norėdami peržiūrėti objekto įrašus, pažymėkite objektą lauke **CDS objekto pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="694d4-136">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="694d4-137">Tinklelyje rodomi visi įrašai, kurie yra siejami su pasirinktu objektu.</span><span class="sxs-lookup"><span data-stu-id="694d4-137">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="694d4-138">[![Objekto įrašų peržiūra](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="694d4-138">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="694d4-139">Šiuo metu nurodyti ne visi „Common Data Service“ objektai.</span><span class="sxs-lookup"><span data-stu-id="694d4-139">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="694d4-140">Tinklelyje rodomi tik tie ojektai, kurie palaiko pasirinktinius laukus.</span><span class="sxs-lookup"><span data-stu-id="694d4-140">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="694d4-141">Nauji objektai tampa pasiekiami nuolatiniuose „Human Resources“ leidimuose.</span><span class="sxs-lookup"><span data-stu-id="694d4-141">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="694d4-142">Tinklelyje yra šie laukai:</span><span class="sxs-lookup"><span data-stu-id="694d4-142">The grid includes the following fields:</span></span>

- <span data-ttu-id="694d4-143">**CDS objekto pavadinimas** – objekto, esančio „Common Data Service“, pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="694d4-143">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="694d4-144">**CDS objekto nuoroda** – identifikatorius, kurį „Common Data Service“ naudoja įrašui identifikuoti.</span><span class="sxs-lookup"><span data-stu-id="694d4-144">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="694d4-145">Ši vertė atitinka „Human Resources“ vertę **RecId**.</span><span class="sxs-lookup"><span data-stu-id="694d4-145">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="694d4-146">Galite rasti identifikatorių, kai atidarote „Common Data Service“objektą, esantį „Microsoft Excel“.</span><span class="sxs-lookup"><span data-stu-id="694d4-146">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="694d4-147">**„Human Resources“ objekto pavadinimas** – objektas, kuris paskutinį kartą sinchronizavo duomenis į „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="694d4-147">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="694d4-148">Objektas gali būti arba „Common Data Service“ priešvardis, arba kitas priešvardis.</span><span class="sxs-lookup"><span data-stu-id="694d4-148">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="694d4-149">**„Human Resources“ nuoroda** – **RecId** vertė, susieta su „Human Resources“ įrašu.</span><span class="sxs-lookup"><span data-stu-id="694d4-149">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="694d4-150">**Panaikintas iš CDS** – reikšmė, nurodanti, ar įrašas buvo panaikintas iš „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="694d4-150">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="694d4-151">Įrašo, esančio „Human Resources“ susiejimo šalinimas iš „Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="694d4-151">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="694d4-152">Jei jums kyla problemų sinchronizuojant duomenis tarp „Human Resources“ ir „Common Data Service”, galite jas išspręsti išvalydami sekimą ir leisdami iš naujo nustatyti sekimo lentelę.</span><span class="sxs-lookup"><span data-stu-id="694d4-152">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="694d4-153">Jei pašalinsite susiejimą ir pakeisite arba panaikininsite įrašą, esantį „Common Data Service“, keitimai nebus sinchronizuojami su „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="694d4-153">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="694d4-154">Atlikus keitimų programoje „Human Resources“, sukuriamas naujas sekimo įrašas ir atnaujinamas įrašas, esantis „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="694d4-154">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="694d4-155">Norėdami pašalinti įrašo susiejimą tarp „Human Resources“ ir „Common Data Service“, lauke **CDS objekto pavadinimas** pasirinkite objektą, tada pasirinkite **Valyti sekimo informaciją**.</span><span class="sxs-lookup"><span data-stu-id="694d4-155">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="694d4-156">[![Sekimo informacijos valymas](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="694d4-156">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="694d4-157">Išvalę sekimą, norėdami vykdyti visišką objekto sinchronizavimą, žr. tolesnę procedūrą.</span><span class="sxs-lookup"><span data-stu-id="694d4-157">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="694d4-158">Objekto sinchronizavimas tarp „Human Resources“ ir „Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="694d4-158">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="694d4-159">Naudokite šią procedūrą, jei „Common Data Service“ keitimai atliekami per ilgai, kad būtų rodomi programoje „Human Resources“, arba jei išvalę sekimą turite atnaujinti sekimo lentelę.</span><span class="sxs-lookup"><span data-stu-id="694d4-159">Use this procedure if changes from Common Data Service are taking too long to appear in Human Resources, or if you must refresh the tracking table after you clear the tracking.</span></span>

- <span data-ttu-id="694d4-160">Norėdami vykdyti visišką objekto sinchronizavimą tarp „Human Resources“ ir „Common Data Service“, lauke **CDS objekto pavadinimas** pasirinkite objektą, tada pasirinkite **Sinchronizuoti dabar**.</span><span class="sxs-lookup"><span data-stu-id="694d4-160">To run a full synchronization on an entity between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Sync now**.</span></span>

<span data-ttu-id="694d4-161">[![Visiško sinchronizavimo paleidimas](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="694d4-161">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


