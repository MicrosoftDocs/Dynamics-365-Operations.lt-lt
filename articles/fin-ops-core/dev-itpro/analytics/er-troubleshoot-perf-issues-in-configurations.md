---
title: ER konfigūracijų našumo trikčių šalinimas
description: Šioje temoje paaiškinama, kaip rasti ir išspręsti efektyvumo problemas elektroninių ataskaitų (ER) konfigūracijose.
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216870"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="782d8-103">ER konfigūracijų našumo trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="782d8-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="782d8-104">Šioje temoje paaiškinama, kaip rasti ir išspręsti efektyvumo problemas [Elektroninių ataskaitų](general-electronic-reporting.md) (ER) [konfigūravimus](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="782d8-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="782d8-105">Paprastai, našumo tyrimas susideda iš kelių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="782d8-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="782d8-106">[Rinkti](#collecting-data) duomenis.</span><span class="sxs-lookup"><span data-stu-id="782d8-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="782d8-107">Analizuoti surinktus duomenis.</span><span class="sxs-lookup"><span data-stu-id="782d8-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="782d8-108">Atsižvelgdami į analizės rezultatus, norėdami atlikti pakeitimus naudokite ER konfigūracijas [arba nuspręskite](#making-changes) surinkti daugiau duomenų.</span><span class="sxs-lookup"><span data-stu-id="782d8-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="782d8-109">Trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="782d8-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="782d8-110">Analizuoti vykdymo laiką</span><span class="sxs-lookup"><span data-stu-id="782d8-110">Analyze execution time</span></span>

<span data-ttu-id="782d8-111">Vykdymo laikas gali priklausyti nuo neprognozuojamo faktoriaus, pvz., nuo kitų užduočių, kurios vykdomos toje pačioje aplinkoje, ir duomenų kaupimo talpykloje, kuri naudoja duomenis pirmą kartą.</span><span class="sxs-lookup"><span data-stu-id="782d8-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="782d8-112">Todėl vykdymą ir matavimą turėtumėte kartoti kelis kartus.</span><span class="sxs-lookup"><span data-stu-id="782d8-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="782d8-113">Kartais efektyvumo problemų lemia ER formato konfigūracija, naudojama ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="782d8-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="782d8-114">Todėl juos lemia X++ kodas, naudojamas atidaryti tą ER formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="782d8-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="782d8-115">Veiksmų centre [arba įvykių žurnale](#infolog-time) ar [peržiūrėkite](#event-log-time) ataskaitos vykdymo laiką.</span><span class="sxs-lookup"><span data-stu-id="782d8-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="782d8-116">Palyginkite ataskaitos vykdymo laiką su viso scenarijaus vykdymo laiku.</span><span class="sxs-lookup"><span data-stu-id="782d8-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="782d8-117">Jei ataskaitos vykdymo laikas yra daug trumpesnis už bendrą vykdymo laiką, atsižvelkite į duomenų, kuriuos apdoroja ataskaita, kiekį:</span><span class="sxs-lookup"><span data-stu-id="782d8-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="782d8-118">Jei ataskaita apdoroja nepildą duomenų kiekį, problema gali apimti konfigūracijos įkėlimo laiką.</span><span class="sxs-lookup"><span data-stu-id="782d8-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="782d8-119">Jei ataskaitoje apdorojama daug duomenų, išdavimas gali apimti išankstinį X++apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="782d8-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="782d8-120">Šiam [atvejui analizuoti naudokite](#analyze-trace-parser-trace) „Trace pacer“.</span><span class="sxs-lookup"><span data-stu-id="782d8-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="782d8-121">Daugiau informacijos apie kitus atvejus rasite tolesniuose skyriuose.</span><span class="sxs-lookup"><span data-stu-id="782d8-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="782d8-122">Vykdykite keletą bandymų, kuriuose dalyvauja skirtingi duomenų kiekiai, kad nustatytumėte, kaip vykdymo laikas priklauso nuo duomenų kiekio.</span><span class="sxs-lookup"><span data-stu-id="782d8-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="782d8-123">Analizuoti „Trace parser“ sekimą</span><span class="sxs-lookup"><span data-stu-id="782d8-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="782d8-124">Parengti smulkų pavyzdį arba surinkti keletą sekimo duomenų atsitiktinėse ataskaitos generavimo dalyse.</span><span class="sxs-lookup"><span data-stu-id="782d8-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="782d8-125">Tada, [„trace parser“](#trace-parser) atlikite standartinę analizę "iš apačios į viršų" ir atsakykite į šiuos klausimus:</span><span class="sxs-lookup"><span data-stu-id="782d8-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="782d8-126">Kokie yra pagrindiniai laiko suvartojimo metodai?</span><span class="sxs-lookup"><span data-stu-id="782d8-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="782d8-127">Kokia viso laiko dalis naudojama šiais metodais?</span><span class="sxs-lookup"><span data-stu-id="782d8-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="782d8-128">Atsakyti į tuos pačius klausimus į užklausas.</span><span class="sxs-lookup"><span data-stu-id="782d8-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="782d8-129">Jei pamatysite, kad metodai su prefiksu „ER" pereis prie kito skyriaus.</span><span class="sxs-lookup"><span data-stu-id="782d8-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="782d8-130">Jei pamatysite, kad metodai arba užklausos kilę iš programų komplekto, apsvarstykite bendrąjį optimizavimą (pvz., sukurkite indeksus).</span><span class="sxs-lookup"><span data-stu-id="782d8-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="782d8-131">Analizuoti skambučių skaičių.</span><span class="sxs-lookup"><span data-stu-id="782d8-131">Analyze the number of calls.</span></span> <span data-ttu-id="782d8-132">Jei skaičius žymiai didesnis nei tikėtasi, galite kaupti talpykloje atitinkamus konfigūracijos mazgus.</span><span class="sxs-lookup"><span data-stu-id="782d8-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="782d8-133">Analizuoti duomenų bazės skambučius</span><span class="sxs-lookup"><span data-stu-id="782d8-133">Analyze database calls</span></span>

<span data-ttu-id="782d8-134">Paruoškite pavyzdį, kuriame yra mažas duomenų kiekis, kad jūs galite rinkti [ER sekimą](#electronic-reporting-traces).</span><span class="sxs-lookup"><span data-stu-id="782d8-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="782d8-135">Tada atidarykite sekimą ER modelio susiejimo konstruktoriuje ir pažiūrėkite puslapio apačioje.</span><span class="sxs-lookup"><span data-stu-id="782d8-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="782d8-136">Atsakyti į šiuos klausimus:</span><span class="sxs-lookup"><span data-stu-id="782d8-136">Answer the following questions:</span></span>

- <span data-ttu-id="782d8-137">Ar yra užklausų dubliavimo?</span><span class="sxs-lookup"><span data-stu-id="782d8-137">Is there any query duplication?</span></span> <span data-ttu-id="782d8-138">Jei yra, apsvarstykite vieną iš šių pataisų:</span><span class="sxs-lookup"><span data-stu-id="782d8-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="782d8-139">[Kaupimą talpykloje](#use-caching) naudokite, jei manote, kad viename pirminiame įraše yra keli skambučiai.</span><span class="sxs-lookup"><span data-stu-id="782d8-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="782d8-140">[Naudokite talpykloje parametruotą apskaičiuotą lauką,](#cached-parameterized) jei manote, kad yra to paties įrašo, esančio skirtinguose įrašuose, skambučių.</span><span class="sxs-lookup"><span data-stu-id="782d8-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="782d8-141">[Naudokite **JOIN** duomenų šaltinį](#use-join-datasource), jei jums reikia skaityti perskaitytą įvairių duomenų bazės įrašų skaičių.</span><span class="sxs-lookup"><span data-stu-id="782d8-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="782d8-142">Ar užklausų skaičius ir išrinktų įrašų skaičius atitinka bendrą duomenų kiekį?</span><span class="sxs-lookup"><span data-stu-id="782d8-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="782d8-143">Pavyzdžiui, jei dokumente yra 10 eilučių, ar statistika rodo, kad ataskaitoje išskleista 10 eilučių ar 1000 eilučių?</span><span class="sxs-lookup"><span data-stu-id="782d8-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="782d8-144">Jei turite daug išrinktų įrašų, apsvarstykite vieną iš šių pataisymų:</span><span class="sxs-lookup"><span data-stu-id="782d8-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="782d8-145">[Naudokite **FILTRO** funkciją, o ne **WHERE** funkciją](#filter) norėdami apdoroti duomenis SQL serverio pusėje.</span><span class="sxs-lookup"><span data-stu-id="782d8-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="782d8-146">Kaupdami talpykloje nenaudokite tų pačių duomenų.</span><span class="sxs-lookup"><span data-stu-id="782d8-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="782d8-147">[Naudokite surinktų duomenų](#collected-data) funkcijas, kad išvengtumėte tų pačių duomenų apibendrinimo duomenų.</span><span class="sxs-lookup"><span data-stu-id="782d8-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="782d8-148">Analizuoti „PerfView“ sekimą</span><span class="sxs-lookup"><span data-stu-id="782d8-148">Analyze PerfView traces</span></span>

<span data-ttu-id="782d8-149">[„PerfView“](#perfview) yra įrankis patyrusiems programuotojams.</span><span class="sxs-lookup"><span data-stu-id="782d8-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="782d8-150">Išsamesnės informacijos apie šiuos veiksmus žr. [„Wall Clock Time Investigation Basics“](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span><span class="sxs-lookup"><span data-stu-id="782d8-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="782d8-151">Surinkkite sekimą naudodami gijos laiką.</span><span class="sxs-lookup"><span data-stu-id="782d8-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="782d8-152">Įtraukite tik dėklus, kuriuose naudojamas **runUnattended** filtruoti tik gijas, kurios konfigūracijos vykdymas.</span><span class="sxs-lookup"><span data-stu-id="782d8-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="782d8-153">(Įtraukti **runUnattended** pridėjimą prie **IncPats** įvesties langelio.)</span><span class="sxs-lookup"><span data-stu-id="782d8-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="782d8-154">Atmeskite visus, tinklo ir užblokuotą laiką.</span><span class="sxs-lookup"><span data-stu-id="782d8-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="782d8-155">Įkelti [„PerfView/ įkėlimo ER išrašus](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml)i.</span><span class="sxs-lookup"><span data-stu-id="782d8-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="782d8-156">Pasirinkite **ER** \> **Kitą išankstinį rinkinį**.</span><span class="sxs-lookup"><span data-stu-id="782d8-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="782d8-157">Peržiūrėkite vardus:</span><span class="sxs-lookup"><span data-stu-id="782d8-157">Look at the names:</span></span>

    - <span data-ttu-id="782d8-158">Tikriausiai matysite platformos kodą, kuris suvartoja daugiausia laiko.</span><span class="sxs-lookup"><span data-stu-id="782d8-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="782d8-159">Galite du kartus spustelėti (arba du kartus spustelėti) ir eiti aukštyn **per dvipusį**.</span><span class="sxs-lookup"><span data-stu-id="782d8-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="782d8-160">Jei surandate klases, kuriose yra prefiksas „ERExpression", ir jei tai funkcijos, susijusios su formulėmis, galite pagal klasės pavadinimą paisyti funkcijos pavadinimo, o norėdami peržiūrėti atributus galite peržiūrėti ER repo.</span><span class="sxs-lookup"><span data-stu-id="782d8-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="782d8-161">Pataisymai</span><span class="sxs-lookup"><span data-stu-id="782d8-161">Fixes</span></span>

- <span data-ttu-id="782d8-162">Jei matote, kad didžiąją prekybos laiko sumą suvartoja užklausos, pabandykite sumažinti užklausų skaičių:</span><span class="sxs-lookup"><span data-stu-id="782d8-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="782d8-163">[Peržiūrėti besidubliuotų](#analyze-database-calls) užklausų ER sekimą.</span><span class="sxs-lookup"><span data-stu-id="782d8-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="782d8-164">Pažiūrėkite, kiek įrašų yra rasta, ir įvertinkite, kiek duomenų teoriškai reikia rasti.</span><span class="sxs-lookup"><span data-stu-id="782d8-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="782d8-165">Jei matote, kad didžiąją laiko dalis YRA suvartojama pagal naudojamas funkcijas, pabandykite rasti vietą konfigūracijoje, naudojančioje daugiausia išteklių.</span><span class="sxs-lookup"><span data-stu-id="782d8-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="782d8-166">Jei matote, kad didžiąją laiko dalis YRA suvartojama pagal duomenų rinkimo funkcijas, apsvarstykite galimybę pakeisti jas *SQL grupe* modelio susiejimo pusėje.</span><span class="sxs-lookup"><span data-stu-id="782d8-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="782d8-167">Rinkti duomenis</span><span class="sxs-lookup"><span data-stu-id="782d8-167">Collecting data</span></span>

<span data-ttu-id="782d8-168">Atsižvelgiant į aplinką, galimas duomenis galima rinkti keliais būdais:</span><span class="sxs-lookup"><span data-stu-id="782d8-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="782d8-169">Gauti visą darbo laiką:</span><span class="sxs-lookup"><span data-stu-id="782d8-169">Get the total running time:</span></span>

    - <span data-ttu-id="782d8-170">Iš veiksmų centro</span><span class="sxs-lookup"><span data-stu-id="782d8-170">From the Action center</span></span>
    - <span data-ttu-id="782d8-171">Iš įvykių žurnalo</span><span class="sxs-lookup"><span data-stu-id="782d8-171">From the event log</span></span>

- <span data-ttu-id="782d8-172">Vykdyti šabloną:</span><span class="sxs-lookup"><span data-stu-id="782d8-172">Profile the execution:</span></span>

    - <span data-ttu-id="782d8-173">Naudojant ER įrankius</span><span class="sxs-lookup"><span data-stu-id="782d8-173">By using ER tools</span></span>
    - <span data-ttu-id="782d8-174">Naudojant „Trace Parser“</span><span class="sxs-lookup"><span data-stu-id="782d8-174">By using Trace parser</span></span>
    - <span data-ttu-id="782d8-175">Naudojant „PerfView“</span><span class="sxs-lookup"><span data-stu-id="782d8-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="782d8-176">Duomenų rinkimas gamybos aplinkoje</span><span class="sxs-lookup"><span data-stu-id="782d8-176">Collecting data in a production environment</span></span>

<span data-ttu-id="782d8-177">Kartais problemos gali būti atkuriamos tik gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="782d8-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="782d8-178">Duomenis galima rinkti šiais būdais:</span><span class="sxs-lookup"><span data-stu-id="782d8-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="782d8-179">Naudojant [„Trace parser“](../perf-test/trace-trace-tutorial.md) sekimą</span><span class="sxs-lookup"><span data-stu-id="782d8-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="782d8-180">Naudojant [ER vykdymo](trace-execution-er-troubleshoot-perf.md) sekimą</span><span class="sxs-lookup"><span data-stu-id="782d8-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="782d8-181">Naudojant visą vykdymo laiką</span><span class="sxs-lookup"><span data-stu-id="782d8-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="782d8-182">Renkant duomenis vystymo aplinkoje</span><span class="sxs-lookup"><span data-stu-id="782d8-182">Collecting data in a development environment</span></span>

<span data-ttu-id="782d8-183">Be įrankių, kuriuos galima naudoti gamybos aplinkoje, dar yra keletas įrankių, kuriuos galima naudoti programavimo aplinkoje:</span><span class="sxs-lookup"><span data-stu-id="782d8-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="782d8-184">Įvykių žurnalas („Microsoft-Dynamics-ElectronicReporting“).</span><span class="sxs-lookup"><span data-stu-id="782d8-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="782d8-185">Šis žurnalas gali suteikti jums visą vykdymo laiką.</span><span class="sxs-lookup"><span data-stu-id="782d8-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="782d8-186">Į bendruosius .NET įrankius, pvz., „PerfView“.</span><span class="sxs-lookup"><span data-stu-id="782d8-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="782d8-187">Be to, programavimo aplinka suteikia jums daugiau lankstumo prie mokymosi.</span><span class="sxs-lookup"><span data-stu-id="782d8-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="782d8-188">Pavyzdžiui, norėdami pamatyti, kaip veikia vykdymo laikas, galima išjungti ataskaitų dalis.</span><span class="sxs-lookup"><span data-stu-id="782d8-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="782d8-189">Įrankiai</span><span class="sxs-lookup"><span data-stu-id="782d8-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="782d8-190">Vykdymo laikas veiksmų centre</span><span class="sxs-lookup"><span data-stu-id="782d8-190">Execution time in the Action center</span></span>

<span data-ttu-id="782d8-191">ER gali rodyti konfigūracijos vykdymo laiką veiksmų centre.</span><span class="sxs-lookup"><span data-stu-id="782d8-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="782d8-192">Ši pasirinktis veikia tik konkrečiam vartotojui ir konkrečiai įmonei bei tik interaktyviems seansams.</span><span class="sxs-lookup"><span data-stu-id="782d8-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="782d8-193">Norėdami, kad ši funkcija būtų pasiekiama, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="782d8-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="782d8-194">Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="782d8-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="782d8-195">Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="782d8-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="782d8-196">Dialogo lange **Vartotojo parametrai** nustatykite **Rodyti failo sukūrimo laiko** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="782d8-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="782d8-197">Vykdymo laikas įvykių žurnale</span><span class="sxs-lookup"><span data-stu-id="782d8-197">Execution time in the event log</span></span>

1. <span data-ttu-id="782d8-198">Atidarykite „Windows Event Viewer“.</span><span class="sxs-lookup"><span data-stu-id="782d8-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="782d8-199">Dalyje **Programų ir paslaugų žurnalai** atidarykite **Microsoft-Dynamics-ElectronicReporting/Operational**.</span><span class="sxs-lookup"><span data-stu-id="782d8-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="782d8-200">Ieškoti **„FormatMapingRun“** vykių, kuriuose **EventID=2**, nes šiuose įvykiams yra informacijos apie praleistą laiką.</span><span class="sxs-lookup"><span data-stu-id="782d8-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="782d8-201">Sekti „Trace parser“ sekimą</span><span class="sxs-lookup"><span data-stu-id="782d8-201">Trace parser traces</span></span> 

<span data-ttu-id="782d8-202">Kadangi ER yra įdiegtas X++, našumui analizuoti galite naudoti bendrus X++ įrankius.</span><span class="sxs-lookup"><span data-stu-id="782d8-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="782d8-203">Norėdami gauti daugiau informacijos, [žr. Sekti naudojant „Trace parser"](../perf-test/trace-trace-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="782d8-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="782d8-204">Yra keletas šio požiūrio apribojimų.</span><span class="sxs-lookup"><span data-stu-id="782d8-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="782d8-205">Kadangi ER dalis įdiegta C#, bus pateikta ne visa informacija.</span><span class="sxs-lookup"><span data-stu-id="782d8-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="782d8-206">Tačiau galite peržiūrėti išsamią duomenų naudojimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="782d8-206">However, you can view the data usage details.</span></span> <span data-ttu-id="782d8-207">Be to, ilgos ataskaitos trukmes galima viršyti sekimo saugojimo apribojimus.</span><span class="sxs-lookup"><span data-stu-id="782d8-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="782d8-208">ER sekimas</span><span class="sxs-lookup"><span data-stu-id="782d8-208">ER traces</span></span>

<span data-ttu-id="782d8-209">ER gali rinkti savo sekimo duomenis ir turi šių sekimą vizualizavimo ir analizės įrankių.</span><span class="sxs-lookup"><span data-stu-id="782d8-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="782d8-210">Daugiau informacijos, žr. [ER formatų vykdymo sekimas, siekiant pašalinti našumo problemas](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="782d8-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="782d8-211">„PerfView“</span><span class="sxs-lookup"><span data-stu-id="782d8-211">PerfView</span></span>

<span data-ttu-id="782d8-212">Kadangi X++ ir ER yra įdiegtas .NET platformoje, galite naudoti bendrus .NET įrankius.</span><span class="sxs-lookup"><span data-stu-id="782d8-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="782d8-213">Pavyzdžiui, galite naudoti nemokamą [„PerfView“](https://github.com/Microsoft/perfview) įrankį.</span><span class="sxs-lookup"><span data-stu-id="782d8-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="782d8-214">Taip pat galite rinkti duomenis iš komandų eilutės.</span><span class="sxs-lookup"><span data-stu-id="782d8-214">You can also collect data from the command line.</span></span> <span data-ttu-id="782d8-215">Pvz., toliau pateiktas „Windows PowerShell" scenarijus renka vykdymo laiką, kol kompiuteryje sustabdomas bet kokio formato vykdymas.</span><span class="sxs-lookup"><span data-stu-id="782d8-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="782d8-216">Yra keletas šio požiūrio apribojimų.</span><span class="sxs-lookup"><span data-stu-id="782d8-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="782d8-217">Turite administruoti prieigą prie mašinos.</span><span class="sxs-lookup"><span data-stu-id="782d8-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="782d8-218">Be to, turite būti patyrusio programuotojo, nes yra stačios mokymosi kreivės.</span><span class="sxs-lookup"><span data-stu-id="782d8-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="782d8-219">Keitimų atlikimas</span><span class="sxs-lookup"><span data-stu-id="782d8-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="782d8-220">Naudoti kaupimą talpykloje</span><span class="sxs-lookup"><span data-stu-id="782d8-220">Use caching</span></span>

<span data-ttu-id="782d8-221">Nors kaupimas talpykloje sumažina laiko, kuris reikalingas duomenims vėl surasti, kiekį, jis kainuoja atminties.</span><span class="sxs-lookup"><span data-stu-id="782d8-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="782d8-222">Kaupimą talpykloje naudokite atvejus, kai išrinktų duomenų kiekis nėra labai didelis.</span><span class="sxs-lookup"><span data-stu-id="782d8-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="782d8-223">Daugiau informacijos ir pavyzdį, kuriame parodyta, kaip naudoti kaupimą talpykloje, žr. Patobulinkite modelio susiejimą, [remiantis vykdymo sekimo informacija](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span><span class="sxs-lookup"><span data-stu-id="782d8-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="782d8-224">Naudoti talpykloje parametruotą apskaičiuotą lauką</span><span class="sxs-lookup"><span data-stu-id="782d8-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="782d8-225">Kartais vertės turi būti peržvalgos pakartotinai.</span><span class="sxs-lookup"><span data-stu-id="782d8-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="782d8-226">Pavyzdžiai gali būti sąskaitų pavadinimai ir sąskaitų numeriai.</span><span class="sxs-lookup"><span data-stu-id="782d8-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="782d8-227">Norėdami sutaupyti laiko, galite sukurti apskaičiuotą lauką, kuriame yra aukščiausio lygio parametrų, tada į talpyklą įtraukite lauką.</span><span class="sxs-lookup"><span data-stu-id="782d8-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="782d8-228">Šį būdą rekomenduojame naudoti tik tada, kai talpykloje saugomų duomenų dydis yra mažas.</span><span class="sxs-lookup"><span data-stu-id="782d8-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="782d8-229">Daugiau informacijos rasite patobulinkite [ER sprendimų našumą pridėdami parametrų APSKAIČIUOTO LAUKO duomenų šaltinius](er-calculated-field-ds-performance.md).</span><span class="sxs-lookup"><span data-stu-id="782d8-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="782d8-230">Naudoti JOIN duomenų šaltinį</span><span class="sxs-lookup"><span data-stu-id="782d8-230">Use a JOIN data source</span></span>

<span data-ttu-id="782d8-231">**JOIN** duomenų šaltinis leidžia vienoje užklausoje rasti kelis prijungtus įrašus.</span><span class="sxs-lookup"><span data-stu-id="782d8-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="782d8-232">Norint surasti kiekvieną prijungtą įrašą, nereikia naudoti atskiros užklausos.</span><span class="sxs-lookup"><span data-stu-id="782d8-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="782d8-233">Pavyzdžiui, jei turite 1000 eilučių, o kiekvienos eilutės prekės duomenis surasti pagal ryšį, turėsite 1001 užklausas (= 1000 + 1).</span><span class="sxs-lookup"><span data-stu-id="782d8-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="782d8-234">Jei naudojate **JOIN** duomenų šaltinį, norėdami surasti tuos pačius duomenis naudosite tik vieną užklausą.</span><span class="sxs-lookup"><span data-stu-id="782d8-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="782d8-235">Dėl daugiau informacijos, žr. [Naudoti JOIN duomenų šaltinius ER modelio žemėlapyje siekiant gauti kelias programos lenteles](er-join-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="782d8-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="782d8-236">Užuot naudojus funkciją WHERE, naudoti funkciją FILTER</span><span class="sxs-lookup"><span data-stu-id="782d8-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="782d8-237">Funkcija **[FILTER](er-functions-list-filter.md)** vykdoma SQL serveryje, o **WHERE** iš sąrašo išrenka visus duomenis, po vieną įrašą ir kiekvienam įrašui taiko sąlygą.</span><span class="sxs-lookup"><span data-stu-id="782d8-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="782d8-238">Pavyzdžiui, norite pasirinkti vieną įrašą iš 1000 įrašų.</span><span class="sxs-lookup"><span data-stu-id="782d8-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="782d8-239">Jei naudojate **WHERE**, bus išrinkta visa 1000 įrašų.</span><span class="sxs-lookup"><span data-stu-id="782d8-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="782d8-240">Tačiau jei naudosite **FILTER**, bus rastas tik vienas įrašas.</span><span class="sxs-lookup"><span data-stu-id="782d8-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="782d8-241">**FILTER** taip pat gali naudoti indeksus duomenų bazės pusėje.</span><span class="sxs-lookup"><span data-stu-id="782d8-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="782d8-242">Surinktų duomenų funkcijų arba sukauptų duomenų šaltinio naudojimas</span><span class="sxs-lookup"><span data-stu-id="782d8-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="782d8-243">Jei jūsų konfigūracijoje yra *grupė pagal* komponentą, kuris apibendrina anksčiau rastos ataskaitos duomenis, komponentas vėl surasti visus duomenis.</span><span class="sxs-lookup"><span data-stu-id="782d8-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="782d8-244">Naudodamiesi surinktų duomenų funkcijomis, įgalinate ER sukaupti duomenis pirmojo rinkimo metu.</span><span class="sxs-lookup"><span data-stu-id="782d8-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="782d8-245">Norėdami gauti daugiau informacijos, žr. [ER konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti](tasks/er-format-counting-summing-2.md).</span><span class="sxs-lookup"><span data-stu-id="782d8-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="782d8-246">Perrašyti konfigūracijos dalis, esantis X++</span><span class="sxs-lookup"><span data-stu-id="782d8-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="782d8-247">ER palaiko lentelių ir klasių, įskaitant plėtinius, iškviešiimą.</span><span class="sxs-lookup"><span data-stu-id="782d8-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="782d8-248">Apsvarstykite galimybę perrašyti modelio susiejimo dalis X++, kad būtų pagerintas našumas.</span><span class="sxs-lookup"><span data-stu-id="782d8-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="782d8-249">ER gali naudoti duomenis iš šių šaltinių:</span><span class="sxs-lookup"><span data-stu-id="782d8-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="782d8-250">Klasės (**objekto** ir **klasės** duomenų šaltiniai)</span><span class="sxs-lookup"><span data-stu-id="782d8-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="782d8-251">Lentelės (**lentelė** ir **lentelės įrašo** duomenų šaltiniai)</span><span class="sxs-lookup"><span data-stu-id="782d8-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="782d8-252">[ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) taip pat suteikia būdą iš anksto apskaičiuotims duomenims iš iškvietimo kodo siųsti.</span><span class="sxs-lookup"><span data-stu-id="782d8-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="782d8-253">Programos komplekte yra keletas šio požiūrio pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="782d8-253">The application suite contains numerous examples of this approach.</span></span>
