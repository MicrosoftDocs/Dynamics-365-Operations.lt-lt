---
title: Integravimo su „Finance“ DUK
description: Šiame straipsnyje paaiškinama, kokie duomenys sinchronizuojami „Human Resources“ ir „Finance“ integravime.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: b9cfc0964a532cd32dda029419c892fa8ae55e02
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009907"
---
# <a name="integration-with-finance-faq"></a><span data-ttu-id="7c886-103">Integravimo su „Finance“ DUK</span><span class="sxs-lookup"><span data-stu-id="7c886-103">Integration with Finance FAQ</span></span>

<span data-ttu-id="7c886-104">Ši tema atsako į dažnai užduodamus klausimus apie tai, kokie duomenys sinchronizuojami, kai „Dynamics 365 Human Resources“ integruojama su „Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="7c886-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Human Resources is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="7c886-105">Ar visi dokumentai sinchronizuojami, ar tik tam tikri duomenų objektai?</span><span class="sxs-lookup"><span data-stu-id="7c886-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="7c886-106">Sinchronizuojamas duomenų poaibis.</span><span class="sxs-lookup"><span data-stu-id="7c886-106">A subset of the data is synchronized.</span></span> <span data-ttu-id="7c886-107">Visų objektų sąrašo žr. [Integravimas su „Dynamics 365 Finance“](hr-admin-integration-finance.md).</span><span class="sxs-lookup"><span data-stu-id="7c886-107">For a list of all the entities, see [Integration with Dynamics 365 Finance](hr-admin-integration-finance.md).</span></span>

## <a name="why-dont-i-see-any-data-synced-to-common-data-service"></a><span data-ttu-id="7c886-108">Kodėl nematau jokių duomenų, sinchronizuotų su „Common Data Service“?</span><span class="sxs-lookup"><span data-stu-id="7c886-108">Why don't I see any data synced to Common Data Service?</span></span>

<span data-ttu-id="7c886-109">Esant numatytiesiems parametrams, naujose aplinkose, kuriose nėra pateiktų demonstracinių duomenų, „Common Data Service“ integravimas yra išjungtas.</span><span class="sxs-lookup"><span data-stu-id="7c886-109">By default, the Common Data Service integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="7c886-110">Esant numatytiesiems nustatymams, jis įjungiamas naujose aplinkose, kuriose yra demonstracinių duomenų, o duomenų sinchronizavimas pradedamas sukonfigūravus aplinką.</span><span class="sxs-lookup"><span data-stu-id="7c886-110">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="7c886-111">Kai jūsų aplinka yra pasiruošta sinchronizuoti duomenis, galite įjungti integravimą.</span><span class="sxs-lookup"><span data-stu-id="7c886-111">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="7c886-112">Daugiau informacijos žr. [„Common Data Service“ integravimo konfigūravimas](hr-admin-integration-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="7c886-112">For more information, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="7c886-113">Ar galiu sukurti naują susiejimą nenaudodamas šablonų?</span><span class="sxs-lookup"><span data-stu-id="7c886-113">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="7c886-114">Šablonai yra pradinis taškas.</span><span class="sxs-lookup"><span data-stu-id="7c886-114">Templates are the starting point.</span></span> <span data-ttu-id="7c886-115">Galite sukurti savo šabloną, tačiau šablonas visada reikalingas kuriant integracijos projektą.</span><span class="sxs-lookup"><span data-stu-id="7c886-115">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="7c886-116">Daugiau informacijos apie duomenų integratorių (DI), šablonus ir projektus žr. [Duomenų integravimas į „Common Data Service“](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="7c886-116">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a><span data-ttu-id="7c886-117">Ar galiu susieti finansines dimensijas ir perkelti iš „Human Resources“ į „Finance“ arba atvirkščiai?</span><span class="sxs-lookup"><span data-stu-id="7c886-117">Can I map financial dimensions to transfer between Human Resources and Finance?</span></span>

<span data-ttu-id="7c886-118">„Common Data Service“ finansinių dimensijų šiuo metu naudoti negalima, todėl jos neįtrauktos į numatytąjį šabloną.</span><span class="sxs-lookup"><span data-stu-id="7c886-118">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="7c886-119">Šis objektas suplanuotas, bet šiuo metu nepateikiama jokia išleidimo laiko juosta.</span><span class="sxs-lookup"><span data-stu-id="7c886-119">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="7c886-120">Jei duomenys yra „Finance“, bet net „Human Resources“, susiekite abi sistemas kartu naudodami „Human Resources“ funkciją **Konfigūruoti saitus**.</span><span class="sxs-lookup"><span data-stu-id="7c886-120">For data that resides in Finance but does not exist in Human Resources, link the two systems together by using **Configure Links** in Human Resources.</span></span>

![Susieti finansines dimensijas](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="7c886-122">Kartais, kai importuoju darbuotojus, „Finance“ jie tampa neaktyviais darbuotojais.</span><span class="sxs-lookup"><span data-stu-id="7c886-122">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="7c886-123">Kodėl?</span><span class="sxs-lookup"><span data-stu-id="7c886-123">Why?</span></span>

<span data-ttu-id="7c886-124">Šią klaidą galite gauti, jei „Human Resources“ nėra aktyvių darbuotojų įdarbinimo informacijos įrašų.</span><span class="sxs-lookup"><span data-stu-id="7c886-124">You may get this error if employees don’t have an active employment detail record in Human Resources.</span></span> <span data-ttu-id="7c886-125">Norėdami išspręsti šią problemą, pasirinkite **Personalo valdymas \> Darbuotojai \> Įdarbinimo retrospektyva \> Duomenų tvarkytuvas** ir patikrinkite, ar yra aktyvus įdarbinimo informacijos įrašas.</span><span class="sxs-lookup"><span data-stu-id="7c886-125">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="7c886-126">Jei pasirinksiu susieti tik antrinį laukų rinkinį, ar nesusietuose laukuose atlikti pakeitimai suaktyvins sinchronizavimą?</span><span class="sxs-lookup"><span data-stu-id="7c886-126">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="7c886-127">Duomenų sinchronizavimas vykdomas pagal vykdymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="7c886-127">Data sync follows the execution schedule.</span></span> <span data-ttu-id="7c886-128">Integracija paims įrašą, jei bet kuris įrašo laukas pakeičiamas, neatsižvelgiant į tai, ar laukas priskirtas integracijos susiejimui.</span><span class="sxs-lookup"><span data-stu-id="7c886-128">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="7c886-129">Kaip siųsti tik aktyvius darbuotojų pakeitimus, o ne atleistų asmenų įrašų pakeitimus?</span><span class="sxs-lookup"><span data-stu-id="7c886-129">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="7c886-130">Naudodami parinktį „Išplėstinė užklausa“ galite filtruoti ir pertvarkyti šaltinio duomenis prieš perduodami juos į paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="7c886-130">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Aktyvių darbininkų išplėstinė užklausa](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="7c886-132">Ar galiu nurodyti, kokius laukus siųsti į „Finance“ dėl konkretaus objekto?</span><span class="sxs-lookup"><span data-stu-id="7c886-132">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="7c886-133">Laukai gali būti įtraukti arba pašalinti iš integracijos užduoties.</span><span class="sxs-lookup"><span data-stu-id="7c886-133">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="7c886-134">Ne visi duomenų laukai, kurie yra „Common Data Service“ objekte, bus užpildomi iš „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="7c886-134">Not all data fields that exist on the Common Data Service entity will be populated from Human Resources.</span></span>
<span data-ttu-id="7c886-135">Papildomi duomenys gali būti užpildomi naudojant „Power Apps“.</span><span class="sxs-lookup"><span data-stu-id="7c886-135">Additional data can be populated via Power Apps.</span></span>

![Laukų įtraukimas arba pašalinimas iš integracijos užduoties](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="7c886-137">Nustačiau integravimą kaip paketinę užduotį, bet „Human Resources“ prarado ryšį su paskirties sistema.</span><span class="sxs-lookup"><span data-stu-id="7c886-137">I set up integration as a batch job, but Human Resources lost connection to the destination system.</span></span> <span data-ttu-id="7c886-138">Kaip į paskirties sistemą išsiųsti tuos pačius pakeitimus?</span><span class="sxs-lookup"><span data-stu-id="7c886-138">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="7c886-139">Tvarkant išimtis speciali sąranka nereikalinga.</span><span class="sxs-lookup"><span data-stu-id="7c886-139">No special setup is required for exception handling.</span></span> <span data-ttu-id="7c886-140">Duomenų integratorius automatiškai ieškos ir praneš apie klaidas, kurios įvyksta šaltinyje ir paskirties vietoje, ir leis neautomatiškai bandyti dar kartą.</span><span class="sxs-lookup"><span data-stu-id="7c886-140">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="7c886-141">Tačiau jis neleidžia neautomatiškai koreguoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="7c886-141">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="7c886-142">Jei duomenų naujinimai būtini, jie turėtų būti įdiegti šaltinyje arba paskirties vietoje.</span><span class="sxs-lookup"><span data-stu-id="7c886-142">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="7c886-143">Ar galiu nustatyti dvikryptį integravimą?</span><span class="sxs-lookup"><span data-stu-id="7c886-143">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="7c886-144">Ne, integravimas šiuo metu yra vienkryptis (iš „Human Resources“ į „Finance and Operations“).</span><span class="sxs-lookup"><span data-stu-id="7c886-144">No, integration is currently one-way (Human Resources to Finance and Operations).</span></span> <span data-ttu-id="7c886-145">Tačiau galima naudoti numatytąjį šabloną ir siųsti duomenis iš „Human Resources“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="7c886-145">However, there is a default template available to send data from Human Resources to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="7c886-146">Ar integracijoje galima leisti naikinti įrašus?</span><span class="sxs-lookup"><span data-stu-id="7c886-146">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="7c886-147">Ne, duomenų integratorius neįtrauks panaikintų įrašų į duomenų perkėlimą.</span><span class="sxs-lookup"><span data-stu-id="7c886-147">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="7c886-148">Šiuo metu įtraukti tik duomenų kūrimas ir naujinimai (UPSERT).</span><span class="sxs-lookup"><span data-stu-id="7c886-148">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="7c886-149">Ar galiu iš naujo vykdyti, jei vykdymas buvo klaidingas?</span><span class="sxs-lookup"><span data-stu-id="7c886-149">Can I rerun the errored execution?</span></span> <span data-ttu-id="7c886-150">Jei taip, ar man atsiųs visą failą, ar tik pakeitimus?</span><span class="sxs-lookup"><span data-stu-id="7c886-150">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="7c886-151">Pirmasis duomenų integratoriaus paleidimas visada yra išsamus.</span><span class="sxs-lookup"><span data-stu-id="7c886-151">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="7c886-152">Vėlesni paleidimai paremti keitimų sekimu.</span><span class="sxs-lookup"><span data-stu-id="7c886-152">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="7c886-153">Kai vykdomas klaidingas paleidimas, įrašai išskleidžiami vykdymo aprėptimi ir naujausi pakeitimai siunčiami „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="7c886-153">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="7c886-154">Įrašius projekto gaunu klaidą: „Projekte yra susiejimo klaidų.“</span><span class="sxs-lookup"><span data-stu-id="7c886-154">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="7c886-155">Ką daryti?</span><span class="sxs-lookup"><span data-stu-id="7c886-155">What do I do?</span></span>

<span data-ttu-id="7c886-156">Patikrinkite integravimo raktų sąranką, atlikite reikiamus sąrankos pakeitimus, tada atnaujinkite projekto objektus.</span><span class="sxs-lookup"><span data-stu-id="7c886-156">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="7c886-157">Kai naudojamas numatytasis šablonas, integravimo raktai importuojami automatiškai.</span><span class="sxs-lookup"><span data-stu-id="7c886-157">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="7c886-158">Ši problema gali kilti, kai naujos užduotys yra įtraukiamos į esamą šabloną.</span><span class="sxs-lookup"><span data-stu-id="7c886-158">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="7c886-159">Jei aš turiu N skaičių juridinių subjektų, kuriuose darbuotojai yra įdarbinti, ar turiu sukurti kiekvienam iš jų skirtą susiejimą?</span><span class="sxs-lookup"><span data-stu-id="7c886-159">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="7c886-160">Taip, kiekvienam „Finance“ juridiniam subjektui reikia atskiro integravimo projekto duomenų integravime.</span><span class="sxs-lookup"><span data-stu-id="7c886-160">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="7c886-161">Noriu perkelti duomenis, kurie nepriklauso „Microsoft“ teikiamam numatytajam šablonui.</span><span class="sxs-lookup"><span data-stu-id="7c886-161">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="7c886-162">Ar galiu tai padaryti?</span><span class="sxs-lookup"><span data-stu-id="7c886-162">Can I do this?</span></span>

<span data-ttu-id="7c886-163">Taip, laukai gali būti įtraukti į esamą šabloną arba iš jo pašalinti.</span><span class="sxs-lookup"><span data-stu-id="7c886-163">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="7c886-164">Šabloną galima modifikuoti įtraukiant papildomų duomenų iš kitų programų „Common Data Service“ objektų.</span><span class="sxs-lookup"><span data-stu-id="7c886-164">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="7c886-165">Objektas turi būti „Common Data Service“, kad jis būtų įtrauktas į šabloną.</span><span class="sxs-lookup"><span data-stu-id="7c886-165">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="7c886-166">Ką tik sukūriau naujas „Finance“ ir „Human Resources“ aplinkas ir matau klaidą „Duomenų reikšmė pažeidžia vientisumo apribojimus“.</span><span class="sxs-lookup"><span data-stu-id="7c886-166">I just created new Finance and Human Resources environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="7c886-167">Kodėl?</span><span class="sxs-lookup"><span data-stu-id="7c886-167">Why?</span></span>

<span data-ttu-id="7c886-168">Šios klaidos priežastys gali būti</span><span class="sxs-lookup"><span data-stu-id="7c886-168">Reasons for this error can include:</span></span>

- <span data-ttu-id="7c886-169">Duomenų perdavimo metu išgaunami įrašų dublikatai šaltinyje („Common Data Service“).</span><span class="sxs-lookup"><span data-stu-id="7c886-169">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="7c886-170">Duomenų perdavimo „null“ reikšmė rodomos tuose laukuose, kurie būtini „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="7c886-170">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="7c886-171">Įsitikinkite, kad duomenys yra „Common Data Service“ ir jie atitinka „Finance and Operations“ reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="7c886-171">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="7c886-172">Jei kilo vykdymo klaidų ir nesinchronizuojamas Darbuotojo ID, kaip rasti retrospektyvos užduotį, kurioje yra nepavykęs darbuotojo įrašas?</span><span class="sxs-lookup"><span data-stu-id="7c886-172">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="7c886-173">Duomenų integratorius „Finance“ sukurs keletą projektų.</span><span class="sxs-lookup"><span data-stu-id="7c886-173">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="7c886-174">Ryšys tarp Duomenų integratoriaus užduoties ir „Finance“ projekto yra vienas su vienu.</span><span class="sxs-lookup"><span data-stu-id="7c886-174">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="7c886-175">Atsekite laiką iš Duomenų integratoriaus vykdymo retrospektyvos ir programoje „Finance“ ieškokite projekto su –1 indeksu.</span><span class="sxs-lookup"><span data-stu-id="7c886-175">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="7c886-176">Jei Duomenų integratoriuje užduoties numeris yra 9, „Finance“ indeksas yra 8.</span><span class="sxs-lookup"><span data-stu-id="7c886-176">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="7c886-177">Užfiksuokite užduoties indeksą iš duomenų integratoriaus (šiame pavyzdyje tai „9“).</span><span class="sxs-lookup"><span data-stu-id="7c886-177">Capture the task index from Data Integrator (in this example it is "9").</span></span>

    ![Užfiksuokite užduoties indeksą iš duomenų integratoriaus](media/CaptureTaskIndex.png)

2. <span data-ttu-id="7c886-179">Stebėkite projekto vykdymo laiką.</span><span class="sxs-lookup"><span data-stu-id="7c886-179">Track the execution time of the project.</span></span>

    ![Stebėkite projekto vykdymo laiką](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="7c886-181">Programoje „Finance“ raskit –1 indeksą.</span><span class="sxs-lookup"><span data-stu-id="7c886-181">In Finance, identify index - 1.</span></span> <span data-ttu-id="7c886-182">Šiame pavyzdyje projektas su priesaga „8“ ir indekso vykdymo laikas „0“ sutampa su 2 veiksmo vykdymo laiku.</span><span class="sxs-lookup"><span data-stu-id="7c886-182">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

    ![Indekso identifikavimas](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a><span data-ttu-id="7c886-184">Integravęs „Human Resources“ ir „Finance“ nematau savo „Human Resources“ duomenų „Finance“ programoje.</span><span class="sxs-lookup"><span data-stu-id="7c886-184">After integrating Human Resources and Finance, I don’t see my Human Resources data in Finance.</span></span> <span data-ttu-id="7c886-185">Ką daryti?</span><span class="sxs-lookup"><span data-stu-id="7c886-185">What do I do?</span></span>

<span data-ttu-id="7c886-186">Integravimo su „Finance“ procesą sudaro du veiksmai.</span><span class="sxs-lookup"><span data-stu-id="7c886-186">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="7c886-187">Pirmiausia, patikrinkite, ar „Human Resources“ yra atnaujinta ir teikiama „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="7c886-187">First, verify that the Human Resources data is updated and available in Common Data Service.</span></span> <span data-ttu-id="7c886-188">Sinchronizuojama beveik realiuoju laiku, todėl galima patikrinti „Power Apps“ duomenų objektuose ieškant duomenų.</span><span class="sxs-lookup"><span data-stu-id="7c886-188">This is a near real-time sync and can be verified in Power Apps by looking at the data within the data entities.</span></span>

![Duomenys „Common Data Service“](media/DataInCDS.png)

<span data-ttu-id="7c886-190">Jei duomenys nėra rodomi „Common Data Service“, kaip tikėtasi, patikrinkite, ar objektas palaikomas integracijoje.</span><span class="sxs-lookup"><span data-stu-id="7c886-190">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="7c886-191">Norint įtraukti papildomų duomenų į „Common Data Service“, pakeitimą turi atlikti „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="7c886-191">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="7c886-192">Jei objektas yra palaikomas ir duomenys yra teikiami „Common Data Service“, patikrinkite, ar susiejimas yra tinkamas duomenų integratoriuje.</span><span class="sxs-lookup"><span data-stu-id="7c886-192">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="7c886-193">Jei integratoriaus susiejimas atrodo tinkamai, tada patikrinkite, ar duomenų valdymo užduotys sėkmingai įvykdytos.</span><span class="sxs-lookup"><span data-stu-id="7c886-193">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="7c886-194">Paketinių užduočių vykdymo metu gali kilti klaidų.</span><span class="sxs-lookup"><span data-stu-id="7c886-194">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="7c886-195">Daugiau informacijos apie duomenų valdymą žr. [Duomenų valdymas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7c886-195">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="7c886-196">Mano darbuotojų adresai yra netikslūs juos importavus į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="7c886-196">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="7c886-197">Ką daryti?</span><span class="sxs-lookup"><span data-stu-id="7c886-197">What should I do?</span></span>

<span data-ttu-id="7c886-198">**Vietos ID** numeracija naudoja tą patį modelį programose „Human Resources“ ir „Finance“.</span><span class="sxs-lookup"><span data-stu-id="7c886-198">The number sequence for **Location ID** uses the same pattern in both Human Resources and Finance.</span></span> <span data-ttu-id="7c886-199">Numeracija turi būti unikali abiejose pusėse, kad adresai nesusikirstų integruojant duomenis iš „Common Data Service“ į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="7c886-199">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="7c886-200">„Human Resources“ diegimo metu patikrinkite, kad „Human Resources“ ir „Finance“ numeracijos nesutaptų.</span><span class="sxs-lookup"><span data-stu-id="7c886-200">During implementation of Human Resources, verify that the number sequences are not the same in Human Resources and Finance.</span></span> <span data-ttu-id="7c886-201">Įsitikinkite, kad visos numeracijos neidentiškos ir duomenys gali būti tvarkomi abiejose sistemose.</span><span class="sxs-lookup"><span data-stu-id="7c886-201">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="7c886-202">Kuriant jungčių rinkinį man nepavyksta matyti jungties išplečiamajame sąraše Jungtis.</span><span class="sxs-lookup"><span data-stu-id="7c886-202">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="7c886-203">Ką daryti?</span><span class="sxs-lookup"><span data-stu-id="7c886-203">What do I do?</span></span>

<span data-ttu-id="7c886-204">Įsitikinkite, kad kurdami jungtis pasirenkate „Dynamics 365 Finance“ ir „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="7c886-204">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="7c886-205">Sinchronizuojant įdiegtis gaunamos klaidos „CompanyInfo_FK doesn’t exist“ arba „The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.“ Ką daryti?</span><span class="sxs-lookup"><span data-stu-id="7c886-205">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="7c886-206">Įsitikinkite, kuria siejate tinkamus juridinius subjektus.</span><span class="sxs-lookup"><span data-stu-id="7c886-206">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="7c886-207">Juridinių subjektų sinchronizavimas nėra numatytojo šablono dalis, todėl tikimasi, kad kiekvienas juridinis subjektas, esantis „Human Resources“ ir „Common Data Service“, taip pat bus ir „Finance“.</span><span class="sxs-lookup"><span data-stu-id="7c886-207">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Human Resources and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="7c886-208">Taip pat įsitikinkite, kad, esate pasirinkę tinkamus susieto jungčių rinkinio juridinius subjektus.</span><span class="sxs-lookup"><span data-stu-id="7c886-208">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="7c886-209">Nustačius projektą atrodo, kad laukų susiejimas „Finance“ yra tuščias.</span><span class="sxs-lookup"><span data-stu-id="7c886-209">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="7c886-210">Ką daryti?</span><span class="sxs-lookup"><span data-stu-id="7c886-210">What should I do?</span></span>

<span data-ttu-id="7c886-211">Atnaujinkite duomenų objektus programoje „Finance“, pasirinkdami **Duomenų valdymas \> Sistemos parametrai \> Objekto parametrai \> Naujinti objektų sąrašą.**</span><span class="sxs-lookup"><span data-stu-id="7c886-211">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="7c886-212">Tai turėtų užtrukti porą minučių, tada turėtumėte matyti tuos susiejimus.</span><span class="sxs-lookup"><span data-stu-id="7c886-212">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="7c886-213">Taip atsitinka, kai kuriami nauji projektai.</span><span class="sxs-lookup"><span data-stu-id="7c886-213">This issue occurs when new projects are created.</span></span>

![Nenurodytas laukų susiejimas](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="7c886-215">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7c886-215">Additional resources</span></span>

- <span data-ttu-id="7c886-216">Duomenų integratorius (DI):</span><span class="sxs-lookup"><span data-stu-id="7c886-216">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="7c886-217">Duomenų integravimas į „Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="7c886-217">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="7c886-218">Duomenų integratoriaus klaidų valdymas ir trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="7c886-218">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="7c886-219">Atsakymas į DSR užklausas, sistemai sugeneruojant žurnalus „Power Apps“, „Microsoft Power Automate“ ir „Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="7c886-219">Responding to DSR requests for system-generated logs in Power Apps, Microsoft Power Automate, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="7c886-220">Duomenų valdymas:</span><span class="sxs-lookup"><span data-stu-id="7c886-220">Data Management:</span></span>

  - [<span data-ttu-id="7c886-221">Duomenų valdymas</span><span class="sxs-lookup"><span data-stu-id="7c886-221">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)