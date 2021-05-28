---
title: „Retail Modern POS“ (MPOS) ir „Cloud POS“ užduočių įrašymo priemonė bei žinynas
description: Šioje temoje aprašoma, kaip naudoti užduočių įrašymo priemonę „Retail Modern POS“ ir „Cloud POS“.
author: mugunthanm
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 02e8bb1bfb088a877ef23b7a81982868700f4ae2
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028112"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="08809-103">„Retail Modern POS“ (MPOS) ir „Cloud POS“ užduočių įrašymo priemonė bei žinynas</span><span class="sxs-lookup"><span data-stu-id="08809-103">Task recorder and Help for Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="08809-104">Šioje temoje aprašoma, kaip naudoti užduočių įrašymo priemonę „Retail Modern POS“ ir „Cloud POS“.</span><span class="sxs-lookup"><span data-stu-id="08809-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="08809-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="08809-105">Overview</span></span>

<span data-ttu-id="08809-106">Užduoties registratorius „Retail Modern POS“ ar „Cloud POS“ yra naujas sprendimas, kuris buvo sukurtas koncentruojantis į greitą reagavimą.</span><span class="sxs-lookup"><span data-stu-id="08809-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="08809-107">Ji pateikia lanksčią tarnybos programavimo sąsają (API), kuri užtikrina išplėtimą ir sklandų integravimą su verslo proceso įrašų vartotojais.</span><span class="sxs-lookup"><span data-stu-id="08809-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="08809-108">Be to, pristatytas užduočių įrašymo priemonės integravimas su „Microsoft Dynamics Lifecycle Services“ verslo procesų modeliavimo (BPM) įrankiu ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)).</span><span class="sxs-lookup"><span data-stu-id="08809-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="08809-109">Todėl vartotojai gali toliau iš įrašų kurti vaizdingas verslo procesų diagramas, kad galėtų analizuoti ir kurti savo programas.</span><span class="sxs-lookup"><span data-stu-id="08809-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="08809-110">Architektūra</span><span class="sxs-lookup"><span data-stu-id="08809-110">Architecture</span></span>

<span data-ttu-id="08809-111">Užduočių įrašymo priemonė gali labai tiksliai įrašyti vartotojo veiksmus kliente.</span><span class="sxs-lookup"><span data-stu-id="08809-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="08809-112">Kiekvienas valdiklis užduočių įrašymo priemonei praneša apie atliktą vartotojo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="08809-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="08809-113">Valdiklis praneša užduočių įrašymo priemonei, kad įvyko įvykis, ir perduoda visą reikiamą informaciją apie atitinkamą vartotojo veiksmą realiuoju laiku.</span><span class="sxs-lookup"><span data-stu-id="08809-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="08809-114">Pagal šią informaciją užduočių įrašymo priemonė gali fiksuoti vartotojo veiksmo tipą (pvz., mygtuko spustelėjimą, vertės įrašymą arba naršymą) ir bet kokius duomenis, kurie susiję su vartotojo veiksmais (pvz., įvesties duomenų vertę ir tipą, formos kontekstą arba įrašo konteksto).</span><span class="sxs-lookup"><span data-stu-id="08809-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="08809-115">Užduočių įrašymo priemonė įrašo informaciją pakankamai išsamiai ir užtikrina, kad atkuriant įrašą būtų galima atlikti įrašytus veiksmus lygiai taip pat, kaip juos atliko vartotojas.</span><span class="sxs-lookup"><span data-stu-id="08809-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="08809-116">(Atkūrimo funkcija dar nėra įdiegta „Retail modern POS“ arba „Cloud POS“.)</span><span class="sxs-lookup"><span data-stu-id="08809-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="08809-117">Pagrindinė konfigūracija</span><span class="sxs-lookup"><span data-stu-id="08809-117">Basic configuration</span></span>

<span data-ttu-id="08809-118">Norėdami įjungti užduočių įrašymą EKA, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="08809-118">To enable task recording in POS, follow these steps.</span></span>

1. <span data-ttu-id="08809-119">Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **Registrai**.</span><span class="sxs-lookup"><span data-stu-id="08809-119">Click **Retail and Commerce** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="08809-120">Spustelėkite registrą, kuriame norite įjungti užduočių įrašymą.</span><span class="sxs-lookup"><span data-stu-id="08809-120">Click the register to enable task recording on.</span></span>
3. <span data-ttu-id="08809-121">Skirtuko **Registras** „FastTab“ **Bendra** nustatykite parinktį **Įjungti užduočių įrašymą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="08809-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4. <span data-ttu-id="08809-122">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="08809-122">Click **Save**.</span></span>
5. <span data-ttu-id="08809-123">Eikite į **„Retail and Commerce“** &gt; **„Retail and Commerce IT“** &gt; **Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="08809-123">Go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="08809-124">Pasirinkite užduotį **Registrai (1090)** ir tada spustelėkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="08809-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="08809-125">Įrašo kūrimas</span><span class="sxs-lookup"><span data-stu-id="08809-125">Create a recording</span></span>

<span data-ttu-id="08809-126">Atlikite šiuos veiksmus, jei norite kurti naują įrašą naudodami užduočių įrašymo priemonę.</span><span class="sxs-lookup"><span data-stu-id="08809-126">Follow these steps to create a new recording using Task recorder.</span></span>

1. <span data-ttu-id="08809-127">Paleiskite „Retail Modern POS“ arba „Cloud POS“ ir prisijunkite.</span><span class="sxs-lookup"><span data-stu-id="08809-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2. <span data-ttu-id="08809-128">Puslapio **Parametrai** dalyje **Užduočių įrašymo priemonė** spustelėkite **Atidaryti užduočių įrašymo priemonę**.</span><span class="sxs-lookup"><span data-stu-id="08809-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="08809-129">Pasirodo sritis **Užduočių įrašymo priemonė**.</span><span class="sxs-lookup"><span data-stu-id="08809-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="08809-130">Galite spustelėti mygtuką **Uždaryti** (**X**) viršutiniame dešiniajame kampe, kad prieš pradėdami naują įrašymo veiksmą uždarytumėte sritį **Užduočių įrašymo priemonė**.</span><span class="sxs-lookup"><span data-stu-id="08809-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="08809-131">Norėdami atidaryti juostą dar kartą, kartokite žingsnį 2.</span><span class="sxs-lookup"><span data-stu-id="08809-131">To reopen the pane, repeat step 2.</span></span>

    <span data-ttu-id="08809-132">[![Sritis Užduočių įrašymo priemonė](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="08809-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3. <span data-ttu-id="08809-133">Įveskite įrašo pavadinimą bei aprašą ir spustelėkite **Pradėti**.</span><span class="sxs-lookup"><span data-stu-id="08809-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="08809-134">Įrašymo sesija prasideda iškart, kai spustelėjate **Pradėti**.</span><span class="sxs-lookup"><span data-stu-id="08809-134">The recording session begins as soon as you click **Start**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="08809-135">Viršutiniame dešiniajame kampe spustelėjus mygtuką **Uždaryti** (**X**), kai vyksta įrašymas, sritis **Užduočių įrašymo priemonė** uždaroma, bet įrašymo seansas tęsiamas.</span><span class="sxs-lookup"><span data-stu-id="08809-135">If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="08809-136">Norėdami vėl atidaryti sritį Užduočių įrašymo priemonė, ekrano viršuje spustelėkite mygtuką **Žinynas** (klaustuko ženklas).</span><span class="sxs-lookup"><span data-stu-id="08809-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span>
    >
    > <span data-ttu-id="08809-137">[![Klaustuko ženklas](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="08809-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4. <span data-ttu-id="08809-138">Kai spustelėsite **Pradėti**, įjungiamas užduočių įrašymo priemonės įrašymo režimas.</span><span class="sxs-lookup"><span data-stu-id="08809-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="08809-139">Srityje **Užduočių įrašymo priemonė** rodoma informacija ir valdikliai, kurie susiję su įrašymo procesu.</span><span class="sxs-lookup"><span data-stu-id="08809-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5. <span data-ttu-id="08809-140">Atlikti veiksmus, kuriuos norite atlikti „Retail Modern POS“ arba „Cloud POS“ vartotojo sąsajoje (UI).</span><span class="sxs-lookup"><span data-stu-id="08809-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6. <span data-ttu-id="08809-141">Norėdami baigti įrašymo seansą, spustelėkite **Stabdyti**.</span><span class="sxs-lookup"><span data-stu-id="08809-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="08809-142">Atsisiuntimo parinktys</span><span class="sxs-lookup"><span data-stu-id="08809-142">Download options</span></span>

<span data-ttu-id="08809-143">Užbaigus įrašymo seansą, rodomos kelios parinktys, kad galėtumėte atsisiųsti savo įrašą.</span><span class="sxs-lookup"><span data-stu-id="08809-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span>

<span data-ttu-id="08809-144">[![Atsisiuntimo parinktys](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="08809-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="08809-145">Įrašyti šiame kompiuteryje</span><span class="sxs-lookup"><span data-stu-id="08809-145">Save to this PC</span></span>

<span data-ttu-id="08809-146">Galite naudoti įrašo paketą, norėdami atkurti užduočių vedlį, tvarkyti įrašą arba redaguoti įrašo komentarus.</span><span class="sxs-lookup"><span data-stu-id="08809-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="08809-147">(Ši funkcija dar nėra įdiegta „Retail Modern POS“ arba „Cloud POS“.)</span><span class="sxs-lookup"><span data-stu-id="08809-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="08809-148">Eksportuoti kaip „Word“ dokumentą</span><span class="sxs-lookup"><span data-stu-id="08809-148">Export as Word document</span></span>

<span data-ttu-id="08809-149">Įrašą galite įrašyti kaip „Microsoft Word“ dokumentą.</span><span class="sxs-lookup"><span data-stu-id="08809-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="08809-150">Dokumente bus įrašyti veiksmai ir užfiksuotos ekrano kopijos.</span><span class="sxs-lookup"><span data-stu-id="08809-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="08809-151">Įrašyti kaip kūrėjo įrašą</span><span class="sxs-lookup"><span data-stu-id="08809-151">Save as developer recording</span></span>

<span data-ttu-id="08809-152">Neapdorotas įrašo failas naudingas kūrėjo scenarijams, pvz., norint patikrinti kodo generavimą.</span><span class="sxs-lookup"><span data-stu-id="08809-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="08809-153">(Ši funkcija nėra dar neįdiegta.)</span><span class="sxs-lookup"><span data-stu-id="08809-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="08809-154">Įrašymo valdikliai</span><span class="sxs-lookup"><span data-stu-id="08809-154">Recording controls</span></span>

<span data-ttu-id="08809-155">[![Įrašymo valdikliai](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="08809-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="08809-156">Sustabdyti</span><span class="sxs-lookup"><span data-stu-id="08809-156">Stop</span></span>

<span data-ttu-id="08809-157">Norėdami baigti įrašymo seansą, spustelėkite **Stabdyti**.</span><span class="sxs-lookup"><span data-stu-id="08809-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="08809-158">Atminkite, kad baigę seansą negalite jo paleisti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="08809-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="08809-159">Todėl prieš baigdami seansą įsitikinkite, kad įrašymas atliktas.</span><span class="sxs-lookup"><span data-stu-id="08809-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="08809-160">Pauzė</span><span class="sxs-lookup"><span data-stu-id="08809-160">Pause</span></span>

<span data-ttu-id="08809-161">Spustelėkite **Pristabdyti**, kad laikinai sustabdytumėte (pristabdytumėte) įrašymo seansą ir tęstumėte operaciją.</span><span class="sxs-lookup"><span data-stu-id="08809-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="08809-162">Veiksmai, atlikti po to, kai spustelėjama **Pristabdyti**, neįrašomi.</span><span class="sxs-lookup"><span data-stu-id="08809-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="08809-163">Tęsti</span><span class="sxs-lookup"><span data-stu-id="08809-163">Continue</span></span>

<span data-ttu-id="08809-164">Norėdami tęsti įrašymo seansą po to, kai jį pristabdėte, spustelėkite **Tęsti**.</span><span class="sxs-lookup"><span data-stu-id="08809-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="08809-165">Užfiksuoti ekrano kopijas</span><span class="sxs-lookup"><span data-stu-id="08809-165">Capture screenshots</span></span>

<span data-ttu-id="08809-166">Užduočių įrašymo priemonė gali fiksuoti „Retail Modern POS“ vartotojo sąsajos ekrano kopijas įrašinėjant verslo procesus.</span><span class="sxs-lookup"><span data-stu-id="08809-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="08809-167">Norėdami įjungti ekrano kopijų fiksavimo funkciją, nustatykite parinktį **Fiksuoti ekrano kopijas** į **Taip**, o tada pradėkite įrašymą.</span><span class="sxs-lookup"><span data-stu-id="08809-167">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes** and then make the recording.</span></span> <span data-ttu-id="08809-168">Kai įrašymas baigtas, spustelėkite **Sustabdyti** ir atsisiųskite „Word“ dokumentą.</span><span class="sxs-lookup"><span data-stu-id="08809-168">Once the recording is completed, click **Stop** and download the Word document.</span></span> <span data-ttu-id="08809-169">Dokumente bus nurodyti veiksmai ir atitinkamos ekrano kopijos.</span><span class="sxs-lookup"><span data-stu-id="08809-169">The document will contain the steps with relevant screenshots.</span></span>

> [!NOTE]
> <span data-ttu-id="08809-170">Ekrano kopijų fiksavimo funkcija nepalaikoma „Cloud POS“.</span><span class="sxs-lookup"><span data-stu-id="08809-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="08809-171">Užduoties pradėjimas ir baigimas</span><span class="sxs-lookup"><span data-stu-id="08809-171">Start task and End task</span></span>

<span data-ttu-id="08809-172">Galite nurodyti sugrupuotų veiksmų rinkinio pradžią ir pabaigą, naudodami mygtukus **Pradėti užduotį** ir **Baigti** **užduotį**.</span><span class="sxs-lookup"><span data-stu-id="08809-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="08809-173">Spustelėkite **Pradėti užduotį**, kad įtrauktumėte veiksmą „Pradėti užduotį“, tada atlikite veiksmus, kuriuos reikia įtraukti į grupę.</span><span class="sxs-lookup"><span data-stu-id="08809-173">Click **Start task** to add a "Start Task" step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="08809-174">Atlikę grupės veiksmus, spustelėkite **Baigti užduotį**.</span><span class="sxs-lookup"><span data-stu-id="08809-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="08809-175">Užduotys padeda tvarkyti savo procedūras.</span><span class="sxs-lookup"><span data-stu-id="08809-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="08809-176">Užduotis galima įterpti į kitas užduotis.</span><span class="sxs-lookup"><span data-stu-id="08809-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="08809-177">Tokiu būdu galima geriau tvarkyti labai ilgus ir sudėtingus verslo procesus.</span><span class="sxs-lookup"><span data-stu-id="08809-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="08809-178">Komentarų įtraukimas</span><span class="sxs-lookup"><span data-stu-id="08809-178">Adding annotations</span></span>

<span data-ttu-id="08809-179">Komentaras yra papildomas tekstas, įtraukiamas į įrašo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="08809-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="08809-180">Pavyzdžiui, galite naudoti komentarus, norėdami vartotojui suteikti daugiau konteksto arba instrukcijų.</span><span class="sxs-lookup"><span data-stu-id="08809-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="08809-181">Galite įtraukti komentarų prieš arba po veiksmo.</span><span class="sxs-lookup"><span data-stu-id="08809-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="08809-182">Galite įtraukti komentarą į bet kurį veiksmą, spustelėdami mygtuką **Redaguoti** (pieštuko simbolis) dešinėje veiksmo pusėje.</span><span class="sxs-lookup"><span data-stu-id="08809-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span>

<span data-ttu-id="08809-183">[![Veiksmo mygtukas Redaguoti](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="08809-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="08809-184">Tekstas ir pastabos</span><span class="sxs-lookup"><span data-stu-id="08809-184">Texts and notes</span></span>

<span data-ttu-id="08809-185">Galite naudoti laukus **Tekstas** ir **Pastabos**, norėdami įtraukti tekstą, kuris turi būti susietas su užduočių vedlio veiksmu.</span><span class="sxs-lookup"><span data-stu-id="08809-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>

<span data-ttu-id="08809-186">[![Laukai Tekstas ir Pastabos](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="08809-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="08809-187">Tekstas</span><span class="sxs-lookup"><span data-stu-id="08809-187">Text</span></span>

<span data-ttu-id="08809-188">Lauke **Tekstas** įvestas tekstas rodomas *virš* veiksmo teksto užduočių vedlyje.</span><span class="sxs-lookup"><span data-stu-id="08809-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="08809-189">Ši vieta tinka tekstui, kurį vartotojas turėtų perskaityti prieš atlikdamas veiksmą.</span><span class="sxs-lookup"><span data-stu-id="08809-189">This location is appropriate for text that you want the user to read before the user completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="08809-190">Pastabos</span><span class="sxs-lookup"><span data-stu-id="08809-190">Notes</span></span>

<span data-ttu-id="08809-191">Lauke **Pastabos** įvestas tekstas rodomas *po* veiksmo teksto užduočių vedlyje.</span><span class="sxs-lookup"><span data-stu-id="08809-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="08809-192">Norėdamas perskaityti pastabų tekstą, vartotojas turi išplėsti veiksmo tekstą iššokančiajame lange.</span><span class="sxs-lookup"><span data-stu-id="08809-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="08809-193">Ši vieta tinka norint pateikti pasirinktinę skaitomą medžiagą arba kitą informaciją, kuri gali būti naudinga vartotojui, bet nėra privaloma norint atlikti veiksmą.</span><span class="sxs-lookup"><span data-stu-id="08809-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="08809-194">„Retail Modern POS“ ir „Cloud POS“ žinynas</span><span class="sxs-lookup"><span data-stu-id="08809-194">Help in Retail Modern POS and Cloud POS</span></span>

<span data-ttu-id="08809-195">Tam, kad tinkinti užduočių įrašai būtų pateikiami „Retail Modern POS“ ir „Cloud POS“ žinyno srityje ir juos būtų galima peržiūrėti kaip tekstą, užduočių įrašus turite įrašyti į savo BPM biblioteką, tada atnaujinti žinyno sistemos parametrus, kad būtų nurodoma BPM biblioteka.</span><span class="sxs-lookup"><span data-stu-id="08809-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="08809-196">Norėdami gauti daugiau informacijos, žr. [Žinyno sistemos prijungimas](../fin-ops-core/fin-ops/get-started/help-connect.md).</span><span class="sxs-lookup"><span data-stu-id="08809-196">For more information, see [Connecting the Help system](../fin-ops-core/fin-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="08809-197">„Retail Modern POS“ ir „Cloud POS“ žinynas atlieka iešką LCS realiuoju laiku.</span><span class="sxs-lookup"><span data-stu-id="08809-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="08809-198">Ieška vykdoma visose BPM bibliotekose, kurios pasirinktos „Commerce“ žinyno sistemos parametruose, ir rodomi atitinkami rezultatai.</span><span class="sxs-lookup"><span data-stu-id="08809-198">It searches across all the BPM libraries that are selected in the Commerce Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="08809-199">Norėdami pasiekti meniu **Žinynas**, ekrano viršuje spustelėkite mygtuką **Žinynas** (klaustukas) ir ieškos lauke įveskite savo proceso pavadinimą bei spustelėkite ieškos mygtuką.</span><span class="sxs-lookup"><span data-stu-id="08809-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span>

<span data-ttu-id="08809-200">[![Mygtukas Pagalba](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="08809-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span>

<span data-ttu-id="08809-201">Ieškos rezultatuose spustelėjus užduočių vedlį, veiksmus galima peržiūrėti kaip žinyno temą arba eksportuoti į „Word“ dokumentą.</span><span class="sxs-lookup"><span data-stu-id="08809-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span>

> [!NOTE]
> <span data-ttu-id="08809-202">„Retail Modern POS“ ir „Cloud POS“ žinyno sistema neatidarys užduočių vedlių pagal jūsų atidarytą formą ar atliekamą operaciją.</span><span class="sxs-lookup"><span data-stu-id="08809-202">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="08809-203">Proceso pavadinimą turite įvesti į ieškos lauką ir spustelėti **Ieškoti**.</span><span class="sxs-lookup"><span data-stu-id="08809-203">You have to type the process name in the search box and then click **Search**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]