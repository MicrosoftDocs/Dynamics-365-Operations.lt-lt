---
title: Integravimo su „Finance“ DUK
description: Šiame straipsnyje paaiškinama, kokie duomenys sinchronizuojami „Human Resources“ ir „Finance“ integravime.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5befac6c72153332319eefc1aaeab30c33f4c69
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892256"
---
# <a name="integration-with-finance-faq"></a><span data-ttu-id="39b54-103">Integravimo su „Finance“ DUK</span><span class="sxs-lookup"><span data-stu-id="39b54-103">Integration with Finance FAQ</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="39b54-104">Ši tema atsako į dažnai užduodamus klausimus apie tai, kokie duomenys sinchronizuojami, kai „Dynamics 365 Human Resources“ integruojama su „Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="39b54-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Human Resources is integrated with Dynamics 365 Finance.</span></span>

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a><span data-ttu-id="39b54-105">Ar galiu redaguoti „Dynamics 365 Talent“ programos naudotoją „Power Apps“?</span><span class="sxs-lookup"><span data-stu-id="39b54-105">Can I edit the Dynamics 365 Talent application user in Power Apps?</span></span>

<span data-ttu-id="39b54-106">Nr.</span><span class="sxs-lookup"><span data-stu-id="39b54-106">No.</span></span> <span data-ttu-id="39b54-107">Jei redaguojate „Human Resources“ programos vartotoją, integravimas tarp „Human Resources“ ir „Dataverse“ gali nepavykti.</span><span class="sxs-lookup"><span data-stu-id="39b54-107">If you edit the Human Resources application user, the integration between Human Resources and Dataverse might fail.</span></span> <span data-ttu-id="39b54-108">Tolesnė lentelė rodo nustatytuosius nustatymus „Talent“ programos naudotojui.</span><span class="sxs-lookup"><span data-stu-id="39b54-108">The following table shows the default settings for the Talent application user.</span></span>

| <span data-ttu-id="39b54-109">Vardas, pavardė</span><span class="sxs-lookup"><span data-stu-id="39b54-109">Full Name</span></span> | <span data-ttu-id="39b54-110">Programos ID</span><span class="sxs-lookup"><span data-stu-id="39b54-110">Application ID</span></span> | <span data-ttu-id="39b54-111">„Azure AD“ objekto ID</span><span class="sxs-lookup"><span data-stu-id="39b54-111">Azure AD Object ID</span></span> | <span data-ttu-id="39b54-112">Programos ID URI</span><span class="sxs-lookup"><span data-stu-id="39b54-112">Application ID URI</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="39b54-113">„Dynamics365“ skirtas „Talent“</span><span class="sxs-lookup"><span data-stu-id="39b54-113">Dynamics365 for Talent</span></span> | <span data-ttu-id="39b54-114">„f9be0c49-aa22-4ec6-911a-c5da515226ff“</span><span class="sxs-lookup"><span data-stu-id="39b54-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> | <span data-ttu-id="39b54-115">„27fd8129-4b3c-43f7-b1bf-47495d3a049b“</span><span class="sxs-lookup"><span data-stu-id="39b54-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span></span> | <span data-ttu-id="39b54-116">„f9be0c49-aa22-4ec6-911a-c5da515226ff“</span><span class="sxs-lookup"><span data-stu-id="39b54-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> |

![Nustatytieji nustatymai „Talent“ programos naudotojui](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="39b54-118">Ar visi dokumentai sinchronizuojami, ar tik tam tikri duomenų objektai?</span><span class="sxs-lookup"><span data-stu-id="39b54-118">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="39b54-119">Sinchronizuojamas duomenų poaibis.</span><span class="sxs-lookup"><span data-stu-id="39b54-119">A subset of the data is synchronized.</span></span> <span data-ttu-id="39b54-120">Visų objektų sąrašo žr. [Integravimas su „Dynamics 365 Finance“](hr-admin-integration-finance.md).</span><span class="sxs-lookup"><span data-stu-id="39b54-120">For a list of all the entities, see [Integration with Dynamics 365 Finance](hr-admin-integration-finance.md).</span></span>

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a><span data-ttu-id="39b54-121">Kodėl nematau jokių duomenų, sinchronizuotų su „Dataverse“?</span><span class="sxs-lookup"><span data-stu-id="39b54-121">Why don't I see any data synced to Dataverse?</span></span>

<span data-ttu-id="39b54-122">Esant numatytiesiems parametrams, naujose aplinkose, kuriose nėra pateiktų demonstracinių duomenų, „Dataverse“ integravimas yra išjungtas.</span><span class="sxs-lookup"><span data-stu-id="39b54-122">By default, the Dataverse integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="39b54-123">Esant numatytiesiems nustatymams, jis įjungiamas naujose aplinkose, kuriose yra demonstracinių duomenų, o duomenų sinchronizavimas pradedamas sukonfigūravus aplinką.</span><span class="sxs-lookup"><span data-stu-id="39b54-123">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="39b54-124">Kai jūsų aplinka yra pasiruošta sinchronizuoti duomenis, galite įjungti integravimą.</span><span class="sxs-lookup"><span data-stu-id="39b54-124">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="39b54-125">Daugiau informacijos žr. [„Dataverse“ integravimo konfigūravimas](hr-admin-integration-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="39b54-125">For more information, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="39b54-126">Ar galiu sukurti naują susiejimą nenaudodamas šablonų?</span><span class="sxs-lookup"><span data-stu-id="39b54-126">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="39b54-127">Šablonai yra pradinis taškas.</span><span class="sxs-lookup"><span data-stu-id="39b54-127">Templates are the starting point.</span></span> <span data-ttu-id="39b54-128">Galite sukurti savo šabloną, tačiau šablonas visada reikalingas kuriant integracijos projektą.</span><span class="sxs-lookup"><span data-stu-id="39b54-128">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="39b54-129">Daugiau informacijos apie duomenų integratorių (DI), šablonus ir projektus žr. [Duomenų integravimas į „Microsoft Dataverse“](/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="39b54-129">For more information about data integrator (DI), templates, and projects, see [Integrate data into Microsoft Dataverse](/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a><span data-ttu-id="39b54-130">Ar galiu susieti finansines dimensijas ir perkelti iš „Human Resources“ į „Finance“ arba atvirkščiai?</span><span class="sxs-lookup"><span data-stu-id="39b54-130">Can I map financial dimensions to transfer between Human Resources and Finance?</span></span>

<span data-ttu-id="39b54-131">„Dataverse“ finansinių dimensijų šiuo metu naudoti negalima, todėl jos neįtrauktos į numatytąjį šabloną.</span><span class="sxs-lookup"><span data-stu-id="39b54-131">Financial dimensions aren’t currently in Dataverse and as a result aren’t part of the default template.</span></span> <span data-ttu-id="39b54-132">Šis objektas suplanuotas, bet šiuo metu nepateikiama jokia išleidimo laiko juosta.</span><span class="sxs-lookup"><span data-stu-id="39b54-132">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="39b54-133">Jei duomenys yra „Finance“, bet net „Human Resources“, susiekite abi sistemas kartu naudodami „Human Resources“ funkciją **Konfigūruoti saitus**.</span><span class="sxs-lookup"><span data-stu-id="39b54-133">For data that resides in Finance but does not exist in Human Resources, link the two systems together by using **Configure Links** in Human Resources.</span></span>

![Susieti finansines dimensijas](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="39b54-135">Kartais, kai importuoju darbuotojus, „Finance“ jie tampa neaktyviais darbuotojais.</span><span class="sxs-lookup"><span data-stu-id="39b54-135">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="39b54-136">Kodėl?</span><span class="sxs-lookup"><span data-stu-id="39b54-136">Why?</span></span>

<span data-ttu-id="39b54-137">Šią klaidą galite gauti, jei „Human Resources“ nėra aktyvių darbuotojų įdarbinimo informacijos įrašų.</span><span class="sxs-lookup"><span data-stu-id="39b54-137">You may get this error if employees don’t have an active employment detail record in Human Resources.</span></span> <span data-ttu-id="39b54-138">Norėdami išspręsti šią problemą, pasirinkite **Personalo valdymas \> Darbuotojai \> Įdarbinimo retrospektyva \> Duomenų tvarkytuvas** ir patikrinkite, ar yra aktyvus įdarbinimo informacijos įrašas.</span><span class="sxs-lookup"><span data-stu-id="39b54-138">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="39b54-139">Jei pasirinksiu susieti tik antrinį laukų rinkinį, ar nesusietuose laukuose atlikti pakeitimai suaktyvins sinchronizavimą?</span><span class="sxs-lookup"><span data-stu-id="39b54-139">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="39b54-140">Duomenų sinchronizavimas vykdomas pagal vykdymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="39b54-140">Data sync follows the execution schedule.</span></span> <span data-ttu-id="39b54-141">Integracija paims įrašą, jei bet kuris įrašo laukas pakeičiamas, neatsižvelgiant į tai, ar laukas priskirtas integracijos susiejimui.</span><span class="sxs-lookup"><span data-stu-id="39b54-141">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="39b54-142">Kaip siųsti tik aktyvius darbuotojų pakeitimus, o ne atleistų asmenų įrašų pakeitimus?</span><span class="sxs-lookup"><span data-stu-id="39b54-142">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="39b54-143">Naudodami parinktį „Išplėstinė užklausa“ galite filtruoti ir pertvarkyti šaltinio duomenis prieš perduodami juos į paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="39b54-143">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Aktyvių darbininkų išplėstinė užklausa](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="39b54-145">Ar galiu nurodyti, kokius laukus siųsti į „Finance“ dėl konkretaus objekto?</span><span class="sxs-lookup"><span data-stu-id="39b54-145">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="39b54-146">Laukai gali būti įtraukti arba pašalinti iš integracijos užduoties.</span><span class="sxs-lookup"><span data-stu-id="39b54-146">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="39b54-147">Ne visi duomenų laukeliai esantys „Dataverse“ lentelėje bus užpildyti iš „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="39b54-147">Not all data fields that exist on the Dataverse table will be populated from Human Resources.</span></span>
<span data-ttu-id="39b54-148">Papildomi duomenys gali būti užpildomi naudojant „Power Apps“.</span><span class="sxs-lookup"><span data-stu-id="39b54-148">Additional data can be populated via Power Apps.</span></span>

![Laukų įtraukimas arba pašalinimas iš integracijos užduoties](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="39b54-150">Nustačiau integravimą kaip paketinę užduotį, bet „Human Resources“ prarado ryšį su paskirties sistema.</span><span class="sxs-lookup"><span data-stu-id="39b54-150">I set up integration as a batch job, but Human Resources lost connection to the destination system.</span></span> <span data-ttu-id="39b54-151">Kaip į paskirties sistemą išsiųsti tuos pačius pakeitimus?</span><span class="sxs-lookup"><span data-stu-id="39b54-151">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="39b54-152">Tvarkant išimtis speciali sąranka nereikalinga.</span><span class="sxs-lookup"><span data-stu-id="39b54-152">No special setup is required for exception handling.</span></span> <span data-ttu-id="39b54-153">Duomenų integratorius automatiškai ieškos ir praneš apie klaidas, kurios įvyksta šaltinyje ir paskirties vietoje, ir leis neautomatiškai bandyti dar kartą.</span><span class="sxs-lookup"><span data-stu-id="39b54-153">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="39b54-154">Tačiau jis neleidžia neautomatiškai koreguoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="39b54-154">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="39b54-155">Jei duomenų naujinimai būtini, jie turėtų būti įdiegti šaltinyje arba paskirties vietoje.</span><span class="sxs-lookup"><span data-stu-id="39b54-155">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="39b54-156">Ar galiu nustatyti dvikryptį integravimą?</span><span class="sxs-lookup"><span data-stu-id="39b54-156">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="39b54-157">Ne, integravimas šiuo metu yra vienkryptis (iš „Human Resources“ į „Finance and Operations“).</span><span class="sxs-lookup"><span data-stu-id="39b54-157">No, integration is currently one-way (Human Resources to Finance and Operations).</span></span> <span data-ttu-id="39b54-158">Tačiau galima naudoti numatytąjį šabloną ir siųsti duomenis iš „Human Resources“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="39b54-158">However, there is a default template available to send data from Human Resources to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="39b54-159">Ar integracijoje galima leisti naikinti įrašus?</span><span class="sxs-lookup"><span data-stu-id="39b54-159">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="39b54-160">Ne, duomenų integratorius neįtrauks panaikintų įrašų į duomenų perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="39b54-160">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="39b54-161">Šiuo metu įtraukti tik duomenų kūrimas ir naujinimai (UPSERT).</span><span class="sxs-lookup"><span data-stu-id="39b54-161">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="39b54-162">Ar galiu iš naujo vykdyti, jei vykdymas buvo klaidingas?</span><span class="sxs-lookup"><span data-stu-id="39b54-162">Can I rerun the errored execution?</span></span> <span data-ttu-id="39b54-163">Jei taip, ar man atsiųs visą failą, ar tik pakeitimus?</span><span class="sxs-lookup"><span data-stu-id="39b54-163">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="39b54-164">Pirmasis duomenų integratoriaus paleidimas visada yra išsamus.</span><span class="sxs-lookup"><span data-stu-id="39b54-164">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="39b54-165">Vėlesni paleidimai paremti keitimų sekimu.</span><span class="sxs-lookup"><span data-stu-id="39b54-165">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="39b54-166">Kai vykdomas klaidingas paleidimas, įrašai išskleidžiami vykdymo aprėptimi ir naujausi pakeitimai siunčiami „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="39b54-166">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Dataverse.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="39b54-167">Įrašius projekto gaunu klaidą: „Projekte yra susiejimo klaidų.“</span><span class="sxs-lookup"><span data-stu-id="39b54-167">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="39b54-168">Ką daryti?</span><span class="sxs-lookup"><span data-stu-id="39b54-168">What do I do?</span></span>

<span data-ttu-id="39b54-169">Patikrinkite integravimo raktų sąranką, atlikite reikiamus sąrankos pakeitimus, tada atnaujinkite projekto objektus.</span><span class="sxs-lookup"><span data-stu-id="39b54-169">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="39b54-170">Kai naudojamas numatytasis šablonas, integravimo raktai importuojami automatiškai.</span><span class="sxs-lookup"><span data-stu-id="39b54-170">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="39b54-171">Ši problema gali kilti, kai naujos užduotys yra įtraukiamos į esamą šabloną.</span><span class="sxs-lookup"><span data-stu-id="39b54-171">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="39b54-172">Jei aš turiu N skaičių juridinių subjektų, kuriuose darbuotojai yra įdarbinti, ar turiu sukurti kiekvienam iš jų skirtą susiejimą?</span><span class="sxs-lookup"><span data-stu-id="39b54-172">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="39b54-173">Taip, kiekvienam „Finance“ juridiniam subjektui reikia atskiro integravimo projekto duomenų integravime.</span><span class="sxs-lookup"><span data-stu-id="39b54-173">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="39b54-174">Noriu perkelti duomenis, kurie nepriklauso „Microsoft“ teikiamam numatytajam šablonui.</span><span class="sxs-lookup"><span data-stu-id="39b54-174">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="39b54-175">Ar galiu tai padaryti?</span><span class="sxs-lookup"><span data-stu-id="39b54-175">Can I do this?</span></span>

<span data-ttu-id="39b54-176">Taip, laukai gali būti įtraukti į esamą šabloną arba iš jo pašalinti.</span><span class="sxs-lookup"><span data-stu-id="39b54-176">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="39b54-177">Šablonas gali būti modifikuotas taip, kad apimtų papildomus duomenis iš kitų „Dataverse“ lentelių.</span><span class="sxs-lookup"><span data-stu-id="39b54-177">The template can be modified to include additional data from other Dataverse tables.</span></span> <span data-ttu-id="39b54-178">Objektas turi būti „Dataverse“, kad jis būtų įtrauktas į šabloną.</span><span class="sxs-lookup"><span data-stu-id="39b54-178">The entity must be in Dataverse for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="39b54-179">Ką tik sukūriau naujas „Finance“ ir „Human Resources“ aplinkas ir matau klaidą „Duomenų reikšmė pažeidžia vientisumo apribojimus“.</span><span class="sxs-lookup"><span data-stu-id="39b54-179">I just created new Finance and Human Resources environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="39b54-180">Kodėl?</span><span class="sxs-lookup"><span data-stu-id="39b54-180">Why?</span></span>

<span data-ttu-id="39b54-181">Šios klaidos priežastys gali būti</span><span class="sxs-lookup"><span data-stu-id="39b54-181">Reasons for this error can include:</span></span>

- <span data-ttu-id="39b54-182">Duomenų perdavimo metu išgaunami įrašų dublikatai šaltinyje („Dataverse“).</span><span class="sxs-lookup"><span data-stu-id="39b54-182">The data transfer resulted in duplicate records extraction at the source (Dataverse).</span></span>

- <span data-ttu-id="39b54-183">Duomenų perdavimo „null“ reikšmė rodomos tuose laukuose, kurie būtini „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="39b54-183">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="39b54-184">Įsitikinkite, kad duomenys yra „Dataverse“ ir jie atitinka „Finance and Operations“ reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="39b54-184">Verify the data that is in Dataverse and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="39b54-185">Jei kilo vykdymo klaidų ir nesinchronizuojamas Darbuotojo ID, kaip rasti retrospektyvos užduotį, kurioje yra nepavykęs darbuotojo įrašas?</span><span class="sxs-lookup"><span data-stu-id="39b54-185">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="39b54-186">Duomenų integratorius „Finance“ sukurs keletą projektų.</span><span class="sxs-lookup"><span data-stu-id="39b54-186">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="39b54-187">Ryšys tarp Duomenų integratoriaus užduoties ir „Finance“ projekto yra vienas su vienu.</span><span class="sxs-lookup"><span data-stu-id="39b54-187">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="39b54-188">Atsekite laiką iš Duomenų integratoriaus vykdymo retrospektyvos ir programoje „Finance“ ieškokite projekto su –1 indeksu.</span><span class="sxs-lookup"><span data-stu-id="39b54-188">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="39b54-189">Jei Duomenų integratoriuje užduoties numeris yra 9, „Finance“ indeksas yra 8.</span><span class="sxs-lookup"><span data-stu-id="39b54-189">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="39b54-190">Užfiksuokite užduoties indeksą iš duomenų integratoriaus (šiame pavyzdyje tai „9“).</span><span class="sxs-lookup"><span data-stu-id="39b54-190">Capture the task index from Data Integrator (in this example it is "9").</span></span>

    ![Užfiksuokite užduoties indeksą iš duomenų integratoriaus](media/CaptureTaskIndex.png)

2. <span data-ttu-id="39b54-192">Stebėkite projekto vykdymo laiką.</span><span class="sxs-lookup"><span data-stu-id="39b54-192">Track the execution time of the project.</span></span>

    ![Stebėkite projekto vykdymo laiką](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="39b54-194">Programoje „Finance“ raskit –1 indeksą.</span><span class="sxs-lookup"><span data-stu-id="39b54-194">In Finance, identify index - 1.</span></span> <span data-ttu-id="39b54-195">Šiame pavyzdyje projektas su priesaga „8“ ir indekso vykdymo laikas „0“ sutampa su 2 veiksmo vykdymo laiku.</span><span class="sxs-lookup"><span data-stu-id="39b54-195">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

    ![Indekso identifikavimas](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a><span data-ttu-id="39b54-197">Integravęs „Human Resources“ ir „Finance“ nematau savo „Human Resources“ duomenų „Finance“ programoje.</span><span class="sxs-lookup"><span data-stu-id="39b54-197">After integrating Human Resources and Finance, I don’t see my Human Resources data in Finance.</span></span> <span data-ttu-id="39b54-198">Ką daryti?</span><span class="sxs-lookup"><span data-stu-id="39b54-198">What do I do?</span></span>

<span data-ttu-id="39b54-199">Integravimo su „Finance“ procesą sudaro du veiksmai.</span><span class="sxs-lookup"><span data-stu-id="39b54-199">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="39b54-200">Pirmiausia, patikrinkite, ar „Human Resources“ yra atnaujinta ir teikiama „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="39b54-200">First, verify that the Human Resources data is updated and available in Dataverse.</span></span> <span data-ttu-id="39b54-201">Tai yra artimas realaus laiko sinchronizavimas ir gali būti tikrinamas „Power Apps“ ieškant duomenų duomenų lentelėse.</span><span class="sxs-lookup"><span data-stu-id="39b54-201">This is a near real-time sync and can be verified in Power Apps by looking at the data within the data tables.</span></span>

![Duomenys „Dataverse“](media/DataInCDS.png)

<span data-ttu-id="39b54-203">Jei duomenys nėra rodomi „Dataverse“, kaip tikėtasi, patikrinkite, ar objektas palaikomas integracijoje.</span><span class="sxs-lookup"><span data-stu-id="39b54-203">If the data is not appearing as expected in Dataverse, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="39b54-204">Norint įtraukti papildomų duomenų į „Dataverse“, pakeitimą turi atlikti „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="39b54-204">To include additional data in Dataverse, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="39b54-205">Jei objektas yra palaikomas ir duomenys yra teikiami „Dataverse“, patikrinkite, ar susiejimas yra tinkamas duomenų integratoriuje.</span><span class="sxs-lookup"><span data-stu-id="39b54-205">If the entity is supported and the data is available in Dataverse, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="39b54-206">Jei integratoriaus susiejimas atrodo tinkamai, tada patikrinkite, ar duomenų valdymo užduotys sėkmingai įvykdytos.</span><span class="sxs-lookup"><span data-stu-id="39b54-206">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="39b54-207">Paketinių užduočių vykdymo metu gali kilti klaidų.</span><span class="sxs-lookup"><span data-stu-id="39b54-207">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="39b54-208">Daugiau informacijos apie duomenų valdymą žr. [Duomenų valdymas](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="39b54-208">For more information about Data Management, see [Data management](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="39b54-209">Mano darbuotojų adresai yra netikslūs juos importavus į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="39b54-209">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="39b54-210">Ką daryti?</span><span class="sxs-lookup"><span data-stu-id="39b54-210">What should I do?</span></span>

<span data-ttu-id="39b54-211">**Vietos ID** numeracija naudoja tą patį modelį programose „Human Resources“ ir „Finance“.</span><span class="sxs-lookup"><span data-stu-id="39b54-211">The number sequence for **Location ID** uses the same pattern in both Human Resources and Finance.</span></span> <span data-ttu-id="39b54-212">Numeracija turi būti unikali abiejose pusėse, kad adresai nesusikirstų integruojant duomenis iš „Dataverse“ į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="39b54-212">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Dataverse to Finance and Operations.</span></span>

<span data-ttu-id="39b54-213">„Human Resources“ diegimo metu patikrinkite, kad „Human Resources“ ir „Finance“ numeracijos nesutaptų.</span><span class="sxs-lookup"><span data-stu-id="39b54-213">During implementation of Human Resources, verify that the number sequences are not the same in Human Resources and Finance.</span></span> <span data-ttu-id="39b54-214">Įsitikinkite, kad visos numeracijos neidentiškos ir duomenys gali būti tvarkomi abiejose sistemose.</span><span class="sxs-lookup"><span data-stu-id="39b54-214">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="39b54-215">Kuriant jungčių rinkinį man nepavyksta matyti jungties išplečiamajame sąraše Jungtis.</span><span class="sxs-lookup"><span data-stu-id="39b54-215">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="39b54-216">Ką daryti?</span><span class="sxs-lookup"><span data-stu-id="39b54-216">What do I do?</span></span>

<span data-ttu-id="39b54-217">Įsitikinkite, kad kurdami jungtis pasirenkate „Dynamics 365 Finance“ ir „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="39b54-217">Make sure when creating your connections, you choose Dynamics 365 Finance and Dataverse.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="39b54-218">Sinchronizuojant įdiegtis gaunamos klaidos „CompanyInfo_FK doesn’t exist“ arba „The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.“ Ką daryti?</span><span class="sxs-lookup"><span data-stu-id="39b54-218">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="39b54-219">Įsitikinkite, kuria siejate tinkamus juridinius subjektus.</span><span class="sxs-lookup"><span data-stu-id="39b54-219">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="39b54-220">Juridinių subjektų sinchronizavimas nėra numatytojo šablono dalis, todėl tikimasi, kad kiekvienas juridinis subjektas, esantis „Human Resources“ ir „Dataverse“, taip pat bus ir „Finance“.</span><span class="sxs-lookup"><span data-stu-id="39b54-220">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Human Resources and Dataverse is also present in Finance.</span></span>
<span data-ttu-id="39b54-221">Taip pat įsitikinkite, kad, esate pasirinkę tinkamus susieto jungčių rinkinio juridinius subjektus.</span><span class="sxs-lookup"><span data-stu-id="39b54-221">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="39b54-222">Nustačius projektą atrodo, kad laukų susiejimas „Finance“ yra tuščias.</span><span class="sxs-lookup"><span data-stu-id="39b54-222">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="39b54-223">Ką daryti?</span><span class="sxs-lookup"><span data-stu-id="39b54-223">What should I do?</span></span>

<span data-ttu-id="39b54-224">Atnaujinkite duomenų objektus programoje „Finance“, pasirinkdami **Duomenų valdymas \> Sistemos parametrai \> Objekto parametrai \> Naujinti objektų sąrašą.**</span><span class="sxs-lookup"><span data-stu-id="39b54-224">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="39b54-225">Tai turėtų užtrukti porą minučių, tada turėtumėte matyti tuos susiejimus.</span><span class="sxs-lookup"><span data-stu-id="39b54-225">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="39b54-226">Taip atsitinka, kai kuriami nauji projektai.</span><span class="sxs-lookup"><span data-stu-id="39b54-226">This issue occurs when new projects are created.</span></span>

![Nenurodytas laukų susiejimas](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="39b54-228">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="39b54-228">Additional resources</span></span>

- <span data-ttu-id="39b54-229">Duomenų integratorius (DI):</span><span class="sxs-lookup"><span data-stu-id="39b54-229">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="39b54-230">Duomenų integravimas į „Microsoft Dataverse“</span><span class="sxs-lookup"><span data-stu-id="39b54-230">Integrate data into Microsoft Dataverse</span></span>](/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="39b54-231">Duomenų integratoriaus klaidų valdymas ir trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="39b54-231">Data Integrator error management and troubleshooting</span></span>](/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="39b54-232">Atsakymas į DSR užklausas, sistemai sugeneruojant žurnalus „Power Apps“, „Microsoft Power Automate“ ir „Dataverse“</span><span class="sxs-lookup"><span data-stu-id="39b54-232">Responding to DSR requests for system-generated logs in Power Apps, Microsoft Power Automate, and Dataverse</span></span>](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="39b54-233">Duomenų valdymas:</span><span class="sxs-lookup"><span data-stu-id="39b54-233">Data Management:</span></span>

  - [<span data-ttu-id="39b54-234">Duomenų valdymas</span><span class="sxs-lookup"><span data-stu-id="39b54-234">Data management</span></span>](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]