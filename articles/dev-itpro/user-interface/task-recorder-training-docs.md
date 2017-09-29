---
title: "Kurkite dokumentus ar mokymus naudodami Užduočių įrašus"
description: "Šioje temoje paaiškinama, kas yra užduočių įrašymo priemonė ir užduočių vedliai, kaip sukurti užduočių įrašus bei kaip tinkinti „Microsoft“ užduočių vedlius ir juos įtraukti į žinyną."
author: josaw1
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 17b2b4b69bfe62977e09d7bc7bc2e4ba025f0986
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="create-documentation-or-training-using-task-recordings"></a><span data-ttu-id="78beb-103">Kurkite dokumentus ar mokymus naudodami Užduočių įrašus</span><span class="sxs-lookup"><span data-stu-id="78beb-103">Create documentation or training using Task recordings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="78beb-104">Šioje temoje paaiškinama, kas yra užduočių įrašymo priemonė ir užduočių vedliai, kaip sukurti užduočių įrašus bei kaip tinkinti „Microsoft“ užduočių vedlius ir juos įtraukti į žinyną.</span><span class="sxs-lookup"><span data-stu-id="78beb-104">This topic explains what Task recorder and task guides are, how to create task recordings, and how to customize Microsoft task guides and include them in your Help.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78beb-105">Negalite kurti pasirinktinių „Dynamics 365 for Talent‟ užduočių vedlių.</span><span class="sxs-lookup"><span data-stu-id="78beb-105">You cannot create custom task guides for Dynamics 365 for Talent.</span></span> <span data-ttu-id="78beb-106">„Talent‟ žinyno sistema automatiškai prijungta prie produkto užduočių vedlių.</span><span class="sxs-lookup"><span data-stu-id="78beb-106">The Help system for Talent is automatically connected to task guides for the product.</span></span> 

<a name="learn-about-task-recorder"></a><span data-ttu-id="78beb-107">Sužinokite daugiau apie Užduočių įrašytuvą</span><span class="sxs-lookup"><span data-stu-id="78beb-107">Learn about Task recorder</span></span>
-------------------------

<span data-ttu-id="78beb-108">Užduočių įrašymo priemonė yra įrankis, naudojamas įrašyti veiksmams, kuriuos atliekate produkto vartotojo sąsajoje (UI).</span><span class="sxs-lookup"><span data-stu-id="78beb-108">Task recorder is a tool that you can use to record actions that you take in the product user interface (UI).</span></span> <span data-ttu-id="78beb-109">Kai naudojate Užduočių įrašytuvą, fiksuojami visi įvykiai, kuriuos atliekate naudotojo sąsajoje su serveriu, įskaitant reikšmių pridėjimą, nuostatų keitimą, duomenų šalinimą.</span><span class="sxs-lookup"><span data-stu-id="78beb-109">When you use Task recorder, all of the events that you perform in the UI that are executed against the server—including adding values, changing settings, removing data—are captured.</span></span> <span data-ttu-id="78beb-110">Veiksmai, kuriuos įrašote, bendrai vadinami *užduoties įrašu*.</span><span class="sxs-lookup"><span data-stu-id="78beb-110">The steps that you record are collectively called a *task recording*.</span></span> <span data-ttu-id="78beb-111">Užduočių įrašus galima naudoti įvairiais būdais.</span><span class="sxs-lookup"><span data-stu-id="78beb-111">Task recordings can be used in many ways:</span></span>

-   <span data-ttu-id="78beb-112">**Užduočių įrašus galima paleisti kaip užduočių vadovus.**</span><span class="sxs-lookup"><span data-stu-id="78beb-112">**Task recordings can be played as task guides.**</span></span> <span data-ttu-id="78beb-113">Užduočių vedliai integruojami į žinyną.</span><span class="sxs-lookup"><span data-stu-id="78beb-113">Task guides are an integral piece of the Help experience.</span></span> <span data-ttu-id="78beb-114">Užduočių vedlys – tai kontroliuojama, valdoma, interaktyvi priemonė, kuri naudojama atliekant verslo proceso veiksmus.</span><span class="sxs-lookup"><span data-stu-id="78beb-114">A task guide is a controlled, guided, interactive experience through the steps of a business process.</span></span> <span data-ttu-id="78beb-115">Naudotojui atlikti kiekvieną veiksmą nurodoma iššokančiuoju raginimu („burbuliuku‟), kurio animacija rodoma visoje UI ir kuris nurodo į UI elementą, su kuriuo naudotojas turėtų sąveikauti.</span><span class="sxs-lookup"><span data-stu-id="78beb-115">The user is instructed to complete each step by way of a pop-up prompt (or "bubble"), which will animate across the UI and point to the UI element that the user should interact with.</span></span> <span data-ttu-id="78beb-116">Burbuliuke taip pat pateikiama informacija apie sąveikavimo su elementu būdą, pvz., „Spustelėkite čia“ ar „Šiame lauke įveskite reikšmę“.</span><span class="sxs-lookup"><span data-stu-id="78beb-116">The "bubble" also provides information about how to interact with the element, such as “Click here” or “In this field, enter a value.”</span></span> <span data-ttu-id="78beb-117">Užduočių vedlys veikia naudodamas dabartinių vartotojo duomenų rinkinį, o įvesti duomenys įrašomi vartotojo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="78beb-117">A task guide runs against the user’s current data set and the data that is entered is saved in the user’s environment.</span></span>
-   <span data-ttu-id="78beb-118">**Užduočių įrašai gali būti pateikiami kaip procedūros veiksmai žinyno srityje.**</span><span class="sxs-lookup"><span data-stu-id="78beb-118">**Task recordings can be displayed as procedural steps in the Help pane.**</span></span> <span data-ttu-id="78beb-119">Naudodami žinyno sritį galite ieškoti užduočių įrašų ir juos pateikti.</span><span class="sxs-lookup"><span data-stu-id="78beb-119">You can use the Help pane to search for and display task recordings.</span></span> <span data-ttu-id="78beb-120">Žinyno sritį galite pasiekti spustelėję piktogramą **?**,</span><span class="sxs-lookup"><span data-stu-id="78beb-120">You can access the Help pane by clicking the **?**</span></span> <span data-ttu-id="78beb-121">esančią viršutinėje naršymo juostoje, arba galite naudoti sparčiųjų klavišų derinį **Ctrl + Shift + ?**.</span><span class="sxs-lookup"><span data-stu-id="78beb-121">icon in the top navigation bar or you can use the shortcut key combination, **Ctrl+Shift+?**.</span></span> <span data-ttu-id="78beb-122">Žinyno srityje galite perskaityti užduoties įrašo veiksmus arba galite pasirinkti, kad įrašas būtų paleistas kaip užduočių vedlys – tuomet jį naudodami atliksite veiksmus vartotojo sąsajoje.</span><span class="sxs-lookup"><span data-stu-id="78beb-122">You can read the steps of a task recording in the Help pane, or you can opt to play the recording as a task guide so it guides you through the UI.</span></span>
-   <span data-ttu-id="78beb-123">**Užduočių įrašus galima įrašyti į BPM.**</span><span class="sxs-lookup"><span data-stu-id="78beb-123">**Task recordings can be saved to BPM.**</span></span> <span data-ttu-id="78beb-124">Savo užduoties įrašą galite įrašyti į „Lifecycle Services‟ (LCS) verslo procesų modeliavimo įrankio (BPM) bibliotekos hierarchijos eilutę.</span><span class="sxs-lookup"><span data-stu-id="78beb-124">You can save your task recording to a line of a hierarchy in a Business Process Modeler (BPM) library in Lifecycle Services (LCS).</span></span> <span data-ttu-id="78beb-125">Iš įrašo bus sugeneruotas veiksmų sąrašas ir verslo procesų srauto diagrama.</span><span class="sxs-lookup"><span data-stu-id="78beb-125">A list of steps and a business process flow chart will be generated from the recording.</span></span> <span data-ttu-id="78beb-126">Užduočių įrašai, įrašyti į BPM biblioteką, gali būti rodomi kaip žinyno elementai.</span><span class="sxs-lookup"><span data-stu-id="78beb-126">Task recordings that have been saved to a BPM library can be shown as Help.</span></span>
-   <span data-ttu-id="78beb-127">**Užduočių įrašus galima įrašyti kaip „Word‟ dokumentus.**</span><span class="sxs-lookup"><span data-stu-id="78beb-127">**Task recordings can be saved as Word documents.**</span></span> <span data-ttu-id="78beb-128">Taip galite lengvai kurti spausdinamus mokymo vadovus.</span><span class="sxs-lookup"><span data-stu-id="78beb-128">This allows you to easily produce printable training guides.</span></span>

<span data-ttu-id="78beb-129">Galite kurti savo užduočių įrašus, leisti „Microsoft‟ pateiktus užduočių įrašus arba modifikuoti „Microsoft‟ pateiktus užduočių įrašus, kad jie atitiktų jūsų konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="78beb-129">You can create your own task recordings, play task recordings provided by Microsoft, or modify Microsoft-provided task recordings to reflect your configuration.</span></span> <span data-ttu-id="78beb-130">Norėdami gauti daugiau informacijos apie užduočių įrašymo priemonę, žr. [Užduočių įrašymo priemonė](task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="78beb-130">For more information about Task recorder, see [Task recorder](task-recorder.md).</span></span>

## <a name="plan-your-task-recording"></a><span data-ttu-id="78beb-131">Planuokite savo užduoties įrašą</span><span class="sxs-lookup"><span data-stu-id="78beb-131">Plan your task recording</span></span>
<span data-ttu-id="78beb-132">Kurdami naują užduoties įrašą ar savo įrašą kurdami pagal „Microsoft‟ užduoties įrašą, turėkite omenyje toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="78beb-132">Whether you’re creating a new task recording or basing your recording on a Microsoft task recording, keep the following information in mind.</span></span>

-   <span data-ttu-id="78beb-133">Įrašą planuokite taip, kaip planuotumėte vaizdo įrašą.</span><span class="sxs-lookup"><span data-stu-id="78beb-133">Plan your recording like you would a video.</span></span> <span data-ttu-id="78beb-134">Visus sprendimus priimkite iš anksto.</span><span class="sxs-lookup"><span data-stu-id="78beb-134">Make all your decisions ahead of time.</span></span>
-   <span data-ttu-id="78beb-135">Kartą ar du pereikite per verslo procesą jo neįrašydami, kad suprastumėte veiksmus.</span><span class="sxs-lookup"><span data-stu-id="78beb-135">Walk through the business process once or twice without recording it to understand the steps.</span></span>
-   <span data-ttu-id="78beb-136">Kai prieš įrašymą einate per procesą, atkreipkite dėmesį, kur naudojate sparčiuosius klavišus ar klavišą **Įvesti**, kad jų nenaudotumėte pačio įrašymo metu.</span><span class="sxs-lookup"><span data-stu-id="78beb-136">When you walk through the process before you record, notice where you use shortcut keys or the **Enter** key, so that you can avoid using them during the actual recording.</span></span>
-   <span data-ttu-id="78beb-137">Identifikuokite tolesnius dalykus.</span><span class="sxs-lookup"><span data-stu-id="78beb-137">Identify the following:</span></span>
    -   <span data-ttu-id="78beb-138">Ar norite veiksmus sugrupuoti į papildomas užduotis?</span><span class="sxs-lookup"><span data-stu-id="78beb-138">Do you want to group steps together into sub-tasks?</span></span> <span data-ttu-id="78beb-139">Papildomos užduotys vizualiai atskiria proceso dalis.</span><span class="sxs-lookup"><span data-stu-id="78beb-139">Sub-tasks visually set apart sections of a process.</span></span> <span data-ttu-id="78beb-140">Pavyzdžiui, jei kuriate įrašą, skirtą „Produkto kūrimui ir išleidimui‟, galbūt norėsite sugrupuoti veiksmus, kurių reikia norint sukurti produktą, o tada sugrupuoti veiksmus, kurių reikia norint produktą išleisti.</span><span class="sxs-lookup"><span data-stu-id="78beb-140">For example, if you are creating a recording for "Creating and releasing a product," you may want to group together the steps that are required to create a product, and then group together the steps that are required to release the product.</span></span> <span data-ttu-id="78beb-141">Papildomos užduotys taip pat palengvina ilgesnių procesų skaitymą.</span><span class="sxs-lookup"><span data-stu-id="78beb-141">Sub-tasks also make longer processes easier to read.</span></span>
    -   <span data-ttu-id="78beb-142">Ar norite pridėti komentarų ir, jei taip, kur?</span><span class="sxs-lookup"><span data-stu-id="78beb-142">Do you want to add annotations, and if so, where?</span></span> <span data-ttu-id="78beb-143">Daugiau informacijos rasite toliau: „Skirtingų komentarų tipų supratimas‟.</span><span class="sxs-lookup"><span data-stu-id="78beb-143">See "Understand the different types of annotations" below for more information.</span></span>
    -   <span data-ttu-id="78beb-144">Kokias reikšmes pridėsite įvairiuose laukuose, atlikdami verslo proceso veiksmus?</span><span class="sxs-lookup"><span data-stu-id="78beb-144">What values will you add in the various fields as you complete the steps of the business process?</span></span> <span data-ttu-id="78beb-145">Naudinga žinoti, ką toliau pasirinksite ar įvesite, kad įrašant nereikėtų grįžti ar taisyti klaidų.</span><span class="sxs-lookup"><span data-stu-id="78beb-145">It is a good idea to know what you'll select or enter as you proceed so that you don't backtrack or fix mistakes as you're recording.</span></span>

<span data-ttu-id="78beb-146">**Savo aprašus ir komentarus rašykite iš anksto**</span><span class="sxs-lookup"><span data-stu-id="78beb-146">**Write your description and annotations ahead of time**</span></span>

-   <span data-ttu-id="78beb-147">Kiekvieno užduoties įrašo pradžioje yra aprašo laukas, kuriame galite įvesti įrašo įvadą.</span><span class="sxs-lookup"><span data-stu-id="78beb-147">At the beginning of each task recording, there’s a description field that allows you to enter an introduction to the recording.</span></span> <span data-ttu-id="78beb-148">Naudinga aprašą parašyti ir įrašyti iš anksto atskirame dokumente, kad įrašydami galėtumėte jį nukopijuoti bei įklijuoti į įrašą.</span><span class="sxs-lookup"><span data-stu-id="78beb-148">It is a good idea to write and save the description ahead of time in a separate document so you can copy and paste it into the task recording when you are recording.</span></span> <span data-ttu-id="78beb-149">Tokiu būdu tikslinti tekstą galite ne įrašymo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="78beb-149">That way, you can spend time refining the text when you aren't in the process of recording.</span></span> <span data-ttu-id="78beb-150">Tekstą iškerpant ir įklijuojant, įrašymo procesą galima vykdyti greičiau ir sklandžiau.</span><span class="sxs-lookup"><span data-stu-id="78beb-150">Cutting and pasting the text makes the recording process go more quickly and smoothly.</span></span>
-   <span data-ttu-id="78beb-151">Prie kiekvieno užduoties įrašo veiksmo galite sukurti komentarų.</span><span class="sxs-lookup"><span data-stu-id="78beb-151">For each step in a task recording, you can create annotations.</span></span> <span data-ttu-id="78beb-152">Atkuriant užduoties vadovą, komentarai rodomi „burbuliuke‟ kaip pastabos virš ar žemiau veiksmo teksto.</span><span class="sxs-lookup"><span data-stu-id="78beb-152">During playback of a task guide, annotations appear in the "bubble" as notes above or below the text for the step.</span></span> <span data-ttu-id="78beb-153">Komentarus peržiūrint kaip tekstą žinyno srityje, jie rodomi kaip įdėtasis veiksmo tekstas.</span><span class="sxs-lookup"><span data-stu-id="78beb-153">When viewed as text in the Help pane, annotations appear as text inline in the step.</span></span> <span data-ttu-id="78beb-154">Kaip ir aprašą, komentarus naudinga parašyti ir įrašyti atskirame dokumente.</span><span class="sxs-lookup"><span data-stu-id="78beb-154">As with the description, it is a good idea to write and save your annotations in a separate document.</span></span> <span data-ttu-id="78beb-155">Įrašydami užduoties įrašą, komentarus iškirpkite ir įklijuokite iš to dokumento.</span><span class="sxs-lookup"><span data-stu-id="78beb-155">When you’re recording the task recording, cut and paste the annotations in from that document.</span></span>

<span data-ttu-id="78beb-156">**Supraskite skirtingus komentarų tipus** Visi komentarai nėra privalomi.</span><span class="sxs-lookup"><span data-stu-id="78beb-156">**Understand the different types of annotations** All annotations are optional.</span></span> <span data-ttu-id="78beb-157">Jų pridėkite tik kai jie naudotojui suteikia naudingos informacijos.</span><span class="sxs-lookup"><span data-stu-id="78beb-157">Only add them when they’ll provide helpful information to the user.</span></span>

-   <span data-ttu-id="78beb-158">**Pavadinimas**: pavadinimo komentaras bus pateikiamas prieš veiksmo tekstą, kurį automatiškai sugeneruoja užduočių įrašymo priemonė.</span><span class="sxs-lookup"><span data-stu-id="78beb-158">**Title**: A title annotation will appear before the step text that task recorder automatically generates.</span></span> <span data-ttu-id="78beb-159">Užduočių vedlyje pavadinimo komentaras pateikiamas virš automatiškai sugeneruoto teksto.</span><span class="sxs-lookup"><span data-stu-id="78beb-159">In the task guide, the title annotation appears above the automatically generated text.</span></span> <span data-ttu-id="78beb-160">Šį komentaro tipą naudokite norėdami paaiškinti, kodėl naudotojas atlieką veiksmą, arba norėdami suteikti papildomo konteksto.</span><span class="sxs-lookup"><span data-stu-id="78beb-160">Use this type of annotation to explain why the user is doing the step or to give additional context.</span></span>

<span data-ttu-id="78beb-161">Tai redagavimo sritis, kurią matote, kai kurdami įrašą pridedate komentarą.</span><span class="sxs-lookup"><span data-stu-id="78beb-161">This is the editing pane that you see when you add an annotation as you create your recording.</span></span> <span data-ttu-id="78beb-162">Įveskite komentaro pavadinimą lauke **Pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="78beb-162">Enter a title annotation in the **Title** box.</span></span> 

<span data-ttu-id="78beb-163">[![screen1](./media/screen1.png)](./media/screen1.png)</span><span class="sxs-lookup"><span data-stu-id="78beb-163">[![screen1](./media/screen1.png)](./media/screen1.png)</span></span> 

<span data-ttu-id="78beb-164">Taip atrodo pavadinimo komentaras užduočių vedlio „burbuliuke‟.</span><span class="sxs-lookup"><span data-stu-id="78beb-164">This is what the title annotation looks like in the "bubble" in the task guide.</span></span> 

<span data-ttu-id="78beb-165">[![screen2](./media/screen2.png)](./media/screen2.png)</span><span class="sxs-lookup"><span data-stu-id="78beb-165">[![screen2](./media/screen2.png)](./media/screen2.png)</span></span>

-   <span data-ttu-id="78beb-166">**Pastabos.** Pastabų komentaras bus rodomas po veiksmo teksto, kurį automatiškai sugeneruoja užduočių įrašytuvas.</span><span class="sxs-lookup"><span data-stu-id="78beb-166">**Notes:** A notes annotation will appear after the step text that task recorder automatically generates.</span></span> <span data-ttu-id="78beb-167">Jis užduoties vadove bus matomas tik jei naudotojas užduoties vadovo burbuliuke spustelės saitą **Rodyti daugiau**.</span><span class="sxs-lookup"><span data-stu-id="78beb-167">In the task guide it will only be visible if the user clicks the **Show more** link in the task guide bubble.</span></span> <span data-ttu-id="78beb-168">Šį komentaro tipą naudokite norėdami apibūdinti dalykus, kuriuos, norėdamas atlikti veiksmą, turi žinoti naudotojas.</span><span class="sxs-lookup"><span data-stu-id="78beb-168">Use this type of annotation to describe anything that a user needs to know to complete the step.</span></span>

<span data-ttu-id="78beb-169">Tai redagavimo sritis, kurią matote, kai kurdami įrašą pridedate komentarą.</span><span class="sxs-lookup"><span data-stu-id="78beb-169">This is the editing pane that you see when you add an annotation as you create your recording.</span></span> <span data-ttu-id="78beb-170">Įveskite pastabų komentarą lauke **Pastabos**.</span><span class="sxs-lookup"><span data-stu-id="78beb-170">Enter a notes annotation in the **Notes** box.</span></span> 

<span data-ttu-id="78beb-171">[![screen3](./media/screen3.png)](./media/screen3.png)</span><span class="sxs-lookup"><span data-stu-id="78beb-171">[![screen3](./media/screen3.png)](./media/screen3.png)</span></span> 

<span data-ttu-id="78beb-172">Taip atrodo pastabų komentaras užduočių vedlio „burbuliuke‟.</span><span class="sxs-lookup"><span data-stu-id="78beb-172">This is what the notes annotation looks like in the "bubble" in the task guide.</span></span>

<span data-ttu-id="78beb-173">[![screen4](./media/screen4.png)](./media/screen4.png)</span><span class="sxs-lookup"><span data-stu-id="78beb-173">[![screen4](./media/screen4.png)](./media/screen4.png)</span></span>

-   <span data-ttu-id="78beb-174">**Informacijos veiksmas**: šie komentarai sukuriami dešiniuoju pelės mygtuku spustelėjus valdiklį ar bet kurią vietą formoje &lt; **Užduočių įrašymo priemonė** &lt; **Įtraukti informacijos veiksmą.</span><span class="sxs-lookup"><span data-stu-id="78beb-174">**Info step**: These annotations are created by right clicking on a control or anywhere on a form &lt; **Task recorder** &lt; **Add info step.</span></span> <span data-ttu-id="78beb-175">**Informacijos veiksmas pateikiamas kaip sunumeruotas veiksmas bet kurioje vietoje, į kurią įterpsite šį veiksmą, nors vartotojo sąsajoje neįrašytas joks veiksmas.</span><span class="sxs-lookup"><span data-stu-id="78beb-175">**Info steps appear as a numbered step at whatever point you insert it, even though no action was recorded in the UI.</span></span> <span data-ttu-id="78beb-176">Galite pridėti formos lygio informacijos veiksmą arba su valdikliu susietą informacijos veiksmą.</span><span class="sxs-lookup"><span data-stu-id="78beb-176">You can add a form-level info step or an info step associated with a control.</span></span> <span data-ttu-id="78beb-177">Kai informacijos veiksmas susietas su forma, leidžiant užduoties vadovą, jo „burbuliukas‟ atsiras kažkur formoje, be žymeklio.</span><span class="sxs-lookup"><span data-stu-id="78beb-177">When an info step is associated with a form, the task guide “bubble” will appear someplace on the form, with no pointer, when the task guide is played.</span></span> <span data-ttu-id="78beb-178">Kai informacijos veiksmas susietas su valdikliu, leidžiant užduočių vedlį jo „burbuliukas‟ bus nukreiptas į valdiklį.</span><span class="sxs-lookup"><span data-stu-id="78beb-178">When an info step is associated with a control, the task guide “bubble” will point to the control when the task guide is played.</span></span> <span data-ttu-id="78beb-179">Žinyno srityje informacijos veiksmo komentaras bus pateikiamas kaip sunumeruotas veiksmas su bet kokiu įvestu tekstu.</span><span class="sxs-lookup"><span data-stu-id="78beb-179">In the Help pane, an info step annotation will appear as a numbered step with whatever text you entered.</span></span> <span data-ttu-id="78beb-180">Naudokite informacijos veiksmus, kad padėtumėte vartotojui pasirengti tolesniems veiksmams, aprašytumėte veiksmus, kuriuos reikia atlikti ne „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise‟ leidime, arba nurodytumėte kitus įrašus (nors komentaruose hipersaitų kurti negalite).</span><span class="sxs-lookup"><span data-stu-id="78beb-180">Use info steps to prepare the user for the next steps, to describe steps that need to be done outside of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, or to refer to other recordings (although you cannot create hyperinks in annotations.).</span></span>

<span data-ttu-id="78beb-181">**Nustatykite, kokia turėtų būti jūsų įrašo trukmė**</span><span class="sxs-lookup"><span data-stu-id="78beb-181">**Determine how long to make your recording**</span></span>

-   <span data-ttu-id="78beb-182">Naudotojas paprastai įrašą skaitys arba leis nuo pradžios iki pabaigos, todėl nejunkite veiksmų ar užduočių, kuriuos geriau atlikti atskirai.</span><span class="sxs-lookup"><span data-stu-id="78beb-182">The user will generally either read or play the recording from start to finish, so don’t combine steps or tasks that are better done separately.</span></span>
-   <span data-ttu-id="78beb-183">Stenkitės neįrašinėti ilgo scenarijaus, apimančio kelis antrinius procesus.</span><span class="sxs-lookup"><span data-stu-id="78beb-183">Try not to record a long scenario that spans multiple sub-processes.</span></span> <span data-ttu-id="78beb-184">Pvz., „Naudokite parduotuvės klientų aptarnavimo tarnybą‟ yra per platu; jį išskaidykite į trumpesnes užduotis, pvz., „Priimti grąžinimus‟ ir „Pridėti į dovanų kortelę‟.</span><span class="sxs-lookup"><span data-stu-id="78beb-184">For example, “Operate in-store customer service desk” is too broad; break it up into shorter tasks such as “Accept returns” and “Add to gift card.”</span></span>
-   <span data-ttu-id="78beb-185">Jei užduotis gali būti atlikta kaip kelių skirtingų verslo procesų dalis, sukurkite atskirą jos įrašą, į kurį nurodyti galite kituose įrašuose.</span><span class="sxs-lookup"><span data-stu-id="78beb-185">If a task can be carried out as part of several different business processes, create a separate recording for it, and you can refer to it in the other recordings.</span></span>
-   <span data-ttu-id="78beb-186">Jei procesas apima keletą užduočių, kurias asmuo greičiausiai atlieka visas vienu metu, jas galite išsaugoti viename įraše, pvz., „Nustatykite ir priskirkite funkcijų profilius‟.</span><span class="sxs-lookup"><span data-stu-id="78beb-186">If the process involves multiple tasks that the person likely does all at once, you can keep the tasks in one recording, for example, “Set up and assign functionality profiles.”</span></span>
-   <span data-ttu-id="78beb-187">Jei kokia nors užduotis atliekama vieną kartą (pvz., konfigūracija), o iš karto po to atliekama kita užduotis, tačiau ši gali būti atliekama pakartotinai ir savarankiškai, jas išskaidykite į du užduočių įrašus.</span><span class="sxs-lookup"><span data-stu-id="78beb-187">If it is something someone does once (such as configuration) and then another task that they can do immediately afterward but may do repeatedly, and on its own, break them up into two task recordings.</span></span>

<span data-ttu-id="78beb-188">**Nuspręskite, kurioje UI vietoje pradėti įrašą** Puslapis, kuriame esate pradėdami įrašyti užduoties įrašą, nulems puslapį, kurį pateiks užduočių vedlys.</span><span class="sxs-lookup"><span data-stu-id="78beb-188">**Decide where, in the UI, to start a recording** The page that you are on when you start recording a task recording affects which page the task guide is displayed for.</span></span> <span data-ttu-id="78beb-189">Pavyzdžiui, jei norite, kad užduoties įrašas žinyno srityje būtų pateikiamas vartotojui DK parametrų puslapyje spustelėjus žinyną, įrašą pradėti turite DK parametrų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="78beb-189">For example, if you want your task recording to be listed in the Help pane when a user clicks Help on the General ledger parameters page, you must start your recording on the General ledger parameters page.</span></span> <span data-ttu-id="78beb-190">**Įrašus įrašykite kaip .axtr failus** Kai baigiate kurti ar redaguoti užduoties įrašą, jums pateikiamos kelios parinktys, kaip įrašą atsisiųsti ar įrašyti.</span><span class="sxs-lookup"><span data-stu-id="78beb-190">**Save recordings as .axtr files** When you are done creating or editing a task recording, you are presented with several options for how you want to download, or save the recording.</span></span> <span data-ttu-id="78beb-191">Atsisiųsti failą galite kaip užduoties įrašo paketą (.axtr), kaip neapdorotą įrašo failą (.xml), kaip „Word‟ dokumentą arba jį įrašyti į LCS biblioteką.</span><span class="sxs-lookup"><span data-stu-id="78beb-191">You can download the file as a task recording package (.axtr), download it as a raw recording file (.xml), download it as a Word document, or save the file to an LCS library.</span></span> <span data-ttu-id="78beb-192">Naudinga užduoties įrašą visada įrašyti kaip užduoties įrašo paketo failą (.axtr).</span><span class="sxs-lookup"><span data-stu-id="78beb-192">It is a good idea to always save your task recording as a task recording package file (.axtr).</span></span> <span data-ttu-id="78beb-193">Taip bus lengviau failą prižiūrėti, jei vėliau reikėtų keisti procedūras ar komentarus.</span><span class="sxs-lookup"><span data-stu-id="78beb-193">This will help make maintenance of the file easier if procedures or annotations need to change later.</span></span> <span data-ttu-id="78beb-194">Jei failą norite atsisiųsti kaip „Word‟ dokumentą, taip pat jį įrašykite kaip užduoties įrašo paketo failą.</span><span class="sxs-lookup"><span data-stu-id="78beb-194">If you want to download the file as a Word document, also save it as a task recording package file.</span></span>

## <a name="create-your-task-recording"></a><span data-ttu-id="78beb-195">Kurkite užduoties įrašą</span><span class="sxs-lookup"><span data-stu-id="78beb-195">Create your task recording</span></span>
<span data-ttu-id="78beb-196">Jei norite peržiūrėti išsamius instrukcijų veiksmus, žr. straipsnį [Kaip sukurti užduoties įrašą](task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="78beb-196">For detailed walk-through steps, see [How to create a task recording](task-recorder.md).</span></span>

## <a name="copy-and-customize-microsofts-task-recordings"></a><span data-ttu-id="78beb-197">Kopijuokite ir tinkinkite „Microsoft‟ užduočių įrašus</span><span class="sxs-lookup"><span data-stu-id="78beb-197">Copy and customize Microsoft's task recordings</span></span>
<span data-ttu-id="78beb-198">Galite atsisiųsti bei redaguoti „Microsoft‟ užduočių įrašus ir juos naudoti žinyno dokumentacijoje ar mokymo medžiagoje.</span><span class="sxs-lookup"><span data-stu-id="78beb-198">You can download and edit Microsoft's task recordings to use them for your own Help documentation or training materials.</span></span> <span data-ttu-id="78beb-199">Norėdami atsisiųsti „Microsoft‟ užduoties įrašą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="78beb-199">To download a Microsoft task recording, follow these steps:</span></span>

1.  <span data-ttu-id="78beb-200">Atidarykite užduočių įrašymo priemonę.</span><span class="sxs-lookup"><span data-stu-id="78beb-200">Open Task recorder.</span></span> <span data-ttu-id="78beb-201">Užduočių įrašytuvas yra **Nuostatų** meniu.</span><span class="sxs-lookup"><span data-stu-id="78beb-201">Task recorder is located in the **Settings** menu.</span></span>
2.  <span data-ttu-id="78beb-202">Užduočių įrašytuvo srityje spustelėkite **Prižiūrėti įrašą**.</span><span class="sxs-lookup"><span data-stu-id="78beb-202">In the Task recorder pane, click **Maintain a recording.**</span></span>
3.  <span data-ttu-id="78beb-203">Srityje **Kur yra įrašas**, spustelėkite **Jis yra LCS bibliotekoje**.</span><span class="sxs-lookup"><span data-stu-id="78beb-203">Under **Where is the recording**, click **It is in an LCS library**.</span></span>
4.  <span data-ttu-id="78beb-204">Spustelėkite **Pasirinkti LCS biblioteką**.</span><span class="sxs-lookup"><span data-stu-id="78beb-204">Click **Select the LCS library**.</span></span>
5.  <span data-ttu-id="78beb-205">Pasirinkite „Microsoft“ visuotinę biblioteką.</span><span class="sxs-lookup"><span data-stu-id="78beb-205">Select the Microsoft global library.</span></span>
6.  <span data-ttu-id="78beb-206">Medyje pasirinkite verslo procesų bibliotekos mazgą, su kuriuo susietas užduoties įrašas.</span><span class="sxs-lookup"><span data-stu-id="78beb-206">In the tree, select the business process library node that the task recording is associated with.</span></span>
7.  <span data-ttu-id="78beb-207">Spustelėkite **GERAI**.</span><span class="sxs-lookup"><span data-stu-id="78beb-207">Click **OK**.</span></span>
8.  <span data-ttu-id="78beb-208">Spustelėkite **Pradėti**.</span><span class="sxs-lookup"><span data-stu-id="78beb-208">Click **Start**.</span></span>
9.  <span data-ttu-id="78beb-209">Šiame etape pereidami per įrašo veiksmus galite juos keisti – įrašas bus perrašytas.</span><span class="sxs-lookup"><span data-stu-id="78beb-209">At this point, step through the recording, changing any steps as you go to re-record it.</span></span> <span data-ttu-id="78beb-210">**Pastaba**. Jei reikia pakeisti tik įrašo tekstą, įrašą galite atidaryti esant režimui **Redaguoti įrašo komentarus** ir tada jį įrašyti.</span><span class="sxs-lookup"><span data-stu-id="78beb-210">**Note**: If you only need to change the text of a recording, you can open the recording in **Edit a recording's annotations** mode, and then save it.</span></span>
10. <span data-ttu-id="78beb-211">Įrašą atkūrę iki pabaigos, ekrano viršuje esančioje užduočių įrašytuvo juostoje spustelėkite **Sustabdyti**.</span><span class="sxs-lookup"><span data-stu-id="78beb-211">After the recording has played to the end, click **Stop** in the task recorder bar at the top of the screen.</span></span>
11. <span data-ttu-id="78beb-212">Pasirinkite, kaip norite įrašyti užduoties įrašą.</span><span class="sxs-lookup"><span data-stu-id="78beb-212">Choose how you want to save the task recording.</span></span>

## <a name="include-your-task-recordings-in-the-help-pane"></a><span data-ttu-id="78beb-213">Užduočių įrašus įtraukite į žinyno sritį</span><span class="sxs-lookup"><span data-stu-id="78beb-213">Include your task recordings in the Help pane</span></span>
<span data-ttu-id="78beb-214">Kad tinkinti užduočių įrašai būtų pateikiami žinyno srityje ir juos būtų galima atkurti kaip užduočių vedlius arba peržiūrėti kaip tekstą, užduočių įrašus turite įrašyti į savo BPM biblioteką, tada atnaujinti žinyno sistemos parametrus, kad būtų nurodoma BPM biblioteka.</span><span class="sxs-lookup"><span data-stu-id="78beb-214">To show your own custom task recordings in the Help pane so that they can be played back as task guides or viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="78beb-215">Jei reikia daugiau informacijos, žr. dalį [Žinyno sistemos prijungimas.](../get-started/help-connect.md)</span><span class="sxs-lookup"><span data-stu-id="78beb-215">For more information, see [Connect the Help system.](../get-started/help-connect.md)</span></span>

<a name="see-also"></a><span data-ttu-id="78beb-216">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="78beb-216">See also</span></span>
--------

[<span data-ttu-id="78beb-217">Pagalbos apžvalga</span><span class="sxs-lookup"><span data-stu-id="78beb-217">Help overview</span></span>](..\get-started\help-overview.md)

[<span data-ttu-id="78beb-218">Pagalbos prijungimas</span><span class="sxs-lookup"><span data-stu-id="78beb-218">Connect Help</span></span>](..\get-started\help-connect.md)

[<span data-ttu-id="78beb-219">Užduočių įrašymo priemonė</span><span class="sxs-lookup"><span data-stu-id="78beb-219">Task Recorder</span></span>](task-recorder.md)

[<span data-ttu-id="78beb-220">Naudingų žinyno temų kūrimas naudojant užduočių įrašymo priemonę (išorinis saitas)</span><span class="sxs-lookup"><span data-stu-id="78beb-220">Create Rich Help Topics with Task Recorder (external link)</span></span>](https://mbspartner.microsoft.com/AX/Videos/970)
