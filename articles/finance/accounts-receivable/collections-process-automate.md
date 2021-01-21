---
title: Mokėjimų priežiūros proceso automatizavimas
description: Šioje temoje aprašomas mokėjimų priežiūros proceso strategijų, kurios automatiškai identifikuoja klientų SF, kurioms reikalingas priminimas el. paštu, mokėjimų veikla (pvz., telefono skambutis) ar priminimo laiškas, kuris bus išsiųstas klientui, nustatymo procesas.
author: panolte
manager: AnnBe
ms.date: 08/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: db59bad2ed3caf38f22bd4d6059e57747d1d983f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760615"
---
# <a name="collections-process-automation"></a><span data-ttu-id="15199-103">Mokėjimų priežiūros proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-103">Collections process automation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15199-104">Šioje temoje aprašomas mokėjimų priežiūros proceso strategijų, kurios automatiškai identifikuoja klientų SF, kurioms reikalingas priminimas el. paštu, mokėjimų veikla (pvz., telefono skambutis) ar priminimo laiškas, kuris bus išsiųstas klientui, nustatymo procesas.</span><span class="sxs-lookup"><span data-stu-id="15199-104">This topic describes the process of setting up collections process strategies that automatically identify customer invoices that require an email reminder, collection activity (such as a phone call), or a collection letter to be sent to the customer.</span></span> 

<span data-ttu-id="15199-105">Organizacijos išleidžia daug laiko tirdamos suskirstytų pagal terminus balansų ataskaitas, klientų sąskaitas ir atviras SF, kad nustatytų, su kuriais klientais reikia susisiekti dėl atviros SF ar sąskaitos balanso.</span><span class="sxs-lookup"><span data-stu-id="15199-105">Organizations spend a significant amount of time researching aged balance reports, customer accounts, and open invoices to determine which customers need to be contacted about an open invoice or account balance.</span></span> <span data-ttu-id="15199-106">Šie tyrimai užima laiką, kurį mokėjimų priežiūros agentas galėtų praleisti bendraudamas su klientais, kad būtų surinkti pasibaigusio termino balansai, ar spręsdamas su SF susijusius konfliktus.</span><span class="sxs-lookup"><span data-stu-id="15199-106">This research takes times away from a collection agent’s time spent communicating with customers to collect past due balances or resolving invoice disputes.</span></span> <span data-ttu-id="15199-107">Mokėjimų priežiūros proceso automatizavimas leidžia nustatyti strategija pagrįstą jūsų mokėjimų priežiūros proceso metodą.</span><span class="sxs-lookup"><span data-stu-id="15199-107">Collections process automation lets you set up a strategy-based approach to your collection process.</span></span> <span data-ttu-id="15199-108">Tai padeda nuosekliai taikyti mokėjimų priežiūros veiklas pateikiant tinkintus priminimus el. paštu arba suprogramuotą priminimo laiškų siuntimo procesą.</span><span class="sxs-lookup"><span data-stu-id="15199-108">This helps you apply collection activities consistently by providing customized email reminders, or programmed process for sending collection letters.</span></span> 

## <a name="collections-process-setup"></a><span data-ttu-id="15199-109">Mokėjimų priežiūros proceso sąranka</span><span class="sxs-lookup"><span data-stu-id="15199-109">Collections process setup</span></span>
<span data-ttu-id="15199-110">Galite naudoti puslapį **Mokėjimų priežiūros proceso sąranka** (**Kredito ir mokėjimų priežiūra > Sąranka > Mokėjimų priežiūros proceso sąranka**), kad būtų sukurtas automatizuotas mokėjimų priežiūros procesas, skirtas veikloms planuoti, el. laiškams siųsti ir klientų priminimo laiškams kurti bei registruoti.</span><span class="sxs-lookup"><span data-stu-id="15199-110">You can use the **Collections process setup** page (**Credit and collections > Setup > Collections process setup**) to create an automated collections process that will schedule activities, send email messages, and create and post customer collection letters.</span></span> <span data-ttu-id="15199-111">Proceso veiksmai yra pagrįsti pagrindine arba seniausia atvira SF.</span><span class="sxs-lookup"><span data-stu-id="15199-111">The process steps are based on the leading or oldest open invoice.</span></span> <span data-ttu-id="15199-112">Kiekvienas veiksmas naudoja šią SF, kad nustatytų, kokie konkretaus kliento ryšiai ar veikla turi įvykti.</span><span class="sxs-lookup"><span data-stu-id="15199-112">Each step uses this invoice to determine what communication or activity should take place with a specific customer.</span></span>  

### <a name="process-hierarchy"></a><span data-ttu-id="15199-113">Proceso hierarchija</span><span class="sxs-lookup"><span data-stu-id="15199-113">Process hierarchy</span></span>
<span data-ttu-id="15199-114">Kiekvieną kliento telkinį galima priskirti tik vienai proceso hierarchijai.</span><span class="sxs-lookup"><span data-stu-id="15199-114">Each customer pool can only be assigned to one process hierarchy.</span></span> <span data-ttu-id="15199-115">Šio veiksmo hierarchijos rangas nurodo, kuris procesas bus viršesnis, jei klientas įtrauktas į daugiau nei vieną telkinį, kuriam priskirta proceso hierarchija.</span><span class="sxs-lookup"><span data-stu-id="15199-115">The hierarchy rank of this step identifies which process will take precedence if a customer is included in more than one pool that has a process hierarchy assigned.</span></span> <span data-ttu-id="15199-116">Telkinio ID nustato, kurie klientai bus priskirti procesui.</span><span class="sxs-lookup"><span data-stu-id="15199-116">The pool ID determines which customers will be assigned to the process.</span></span> 

<span data-ttu-id="15199-117">Ramios dienos naudojamos siekiant užtikrinti, kad automatizuotas procesas su klientu nesusisiektų per dažnai.</span><span class="sxs-lookup"><span data-stu-id="15199-117">The quiet days are used to ensure that a customer does not get contacted too frequently by the automated process.</span></span>  <span data-ttu-id="15199-118">Pavyzdžiui, jei nustatytos dvi ramios dienos, automatizuotas procesas su klientu nesusisieks bent dvi dienas, net jei pradinė pagrindinė SF yra visiškai sudengta.</span><span class="sxs-lookup"><span data-stu-id="15199-118">For example, if the quiet days are set to two, a customer will not be contacted by the automated process for at least two days, even if the original leading invoice has been settled in full.</span></span> 

<span data-ttu-id="15199-119">Norėdami pašalinti klientus iš proceso automatizavimo, jei sąskaitos balansas arba SF balansas yra mažesnis už nustatytą vertę, nustatykite lauką **Pašalinti iš proceso** į **Taip** ir įveskite sumos vertę.</span><span class="sxs-lookup"><span data-stu-id="15199-119">To exclude customers from the process automation if the account balance or invoice balance is less than a defined value, set the **Exclude from process** field to **Yes** and enter the amount value.</span></span>

## <a name="process-details"></a><span data-ttu-id="15199-120">Proceso informacija</span><span class="sxs-lookup"><span data-stu-id="15199-120">Process details</span></span>
<span data-ttu-id="15199-121">**Aprašas** naudojamas hierarchijos veiksmo paskirčiai arba pavadinimui nustatyti.</span><span class="sxs-lookup"><span data-stu-id="15199-121">**Description** is used to identify the purpose or name of the step in the hierarchy.</span></span>

<span data-ttu-id="15199-122">**Veiksmo tipas** apibrėžia, ar veiksmas sukurs veiklą, išsiųs el. laišką, ar sukurs priminimo laišką.</span><span class="sxs-lookup"><span data-stu-id="15199-122">**Action type** defines if the step will create an activity, send an email, or create a collection letter.</span></span>

<span data-ttu-id="15199-123">**Verslo dokumentas** apibrėžia šabloną, naudojamą kuriant veiksmo tipą.</span><span class="sxs-lookup"><span data-stu-id="15199-123">**Business document** defines the template used to create the action type.</span></span>  <span data-ttu-id="15199-124">Tai gali būti veiklos šablonas, el. laiško šablonas arba priminimo laiškas kiekvienam klientui.</span><span class="sxs-lookup"><span data-stu-id="15199-124">This can be an activity template, an email template, or a collection letter per customer.</span></span> 

<span data-ttu-id="15199-125">Veiksmų tipai gali būti kuriami prieš arba po SF apmokėjimo termino, remiantis parametru, kuris rodomas stulpelyje **Dienos, susijusios su SF apmokėjimo terminu**.</span><span class="sxs-lookup"><span data-stu-id="15199-125">The action types can be created on either before or after the invoice due date, based on the setting that's displayed in the **Days in relation to the invoice due date** column.</span></span>

<span data-ttu-id="15199-126">Pasirinkus el. pašto veiksmo tipą, gavėjas bus naudojamas nustatyti, ar tai klientas, pardavimo grupė, ar mokėjimų priežiūros agentas.</span><span class="sxs-lookup"><span data-stu-id="15199-126">When you select an email action type, the recipient will be used to define if that is a customer, sales group, or collections agent contact.</span></span> <span data-ttu-id="15199-127">Lauko **Verslo paskirties kontaktas** reikšmė nustatys, kuris tos klieno sąskaitos kontaktas gaus pranešimą.</span><span class="sxs-lookup"><span data-stu-id="15199-127">The value in the **Business purpose contact** field will then determine which contact from that customer's account will receive the communication.</span></span>

## <a name="business-document-details"></a><span data-ttu-id="15199-128">Verslo dokumento informacija</span><span class="sxs-lookup"><span data-stu-id="15199-128">Business document details</span></span>
<span data-ttu-id="15199-129">Verslo dokumento informacija skirsis pagal veiksmo tipą, pasirinktą proceso informacijoje.</span><span class="sxs-lookup"><span data-stu-id="15199-129">The business document details will vary based on the action type that's selected in the process details.</span></span>  <span data-ttu-id="15199-130">Kai veiksmo tipas yra veikla, bus rodoma veiklos šablono informacija.</span><span class="sxs-lookup"><span data-stu-id="15199-130">When the action type is an activity, the activity template details will be shown.</span></span>  <span data-ttu-id="15199-131">Šie duomenys apima veiklos šablono pavadinimą, veiklos, kuri bus sukurta, tipą, veiklos paskirtį, numatytą dienų, kurių reikės veiklos užbaigimui, skaičių ir informaciją apie veiklą.</span><span class="sxs-lookup"><span data-stu-id="15199-131">These details include the activity template name, the type of activity that will be created, the purpose of the activity, the number of days scheduled to complete the activity, and the details of the activity.</span></span>  <span data-ttu-id="15199-132">Ši veikla bus susieta su pagrindine SF, nurodančia gavėjui apie veiksmą, kurio reikia veiklai užbaigti.</span><span class="sxs-lookup"><span data-stu-id="15199-132">This activity will then link to the leading invoice that tells the recipient of the action that’s needed to complete the activity.</span></span>

<span data-ttu-id="15199-133">Jei veiksmo tipas yra el. laiškas proceso informacijoje, šiame skyriuje bus du „FastTab”.</span><span class="sxs-lookup"><span data-stu-id="15199-133">If the action type is an email in the process details, this section will contain two FastTabs.</span></span>  <span data-ttu-id="15199-134">Pirmasis naudojamas norint nurodyti šablono ID, el. pašto aprašą, numatytąją kalbą, vartotojo vardą, kuris bus priskirtas automatiškai siunčiamiems el. laiškams, ir susijusių siuntėjų el. pašto adresus.</span><span class="sxs-lookup"><span data-stu-id="15199-134">The first is used to define the template ID, email description, default language, the user name that will be assigned to email messages that are automatically sent, and the associated senders email address.</span></span> <span data-ttu-id="15199-135">Antrasis leis sukurti el. laišką po to, kai reikšmės laukuose **Kalba** ir **Tema** bus išsaugotos pasirinkus **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="15199-135">The second will allow the body of the email to be created after the values in the **Language** and **Subject** fields are saved by selecting **Edit**.</span></span>  <span data-ttu-id="15199-136">Atsidarys langas, kuris leis įkelti HTML turinį.</span><span class="sxs-lookup"><span data-stu-id="15199-136">This will open a window that allows HTML content to be uploaded.</span></span> <span data-ttu-id="15199-137">Taip pat galite įvesti pranešimą, sukuriamą rankiniu būdu apatiniame kairiajame lango lauke.</span><span class="sxs-lookup"><span data-stu-id="15199-137">You can also type the message that’s created manually in the lower left box of the window.</span></span>  

> [!Note]
> <span data-ttu-id="15199-138">„Outlook” el. laišką galima įrašyti naudojant norimą pranešimo tekstą HTML formatu.</span><span class="sxs-lookup"><span data-stu-id="15199-138">An Outlook email can be saved with the desired body of the communication in HTML format.</span></span> <span data-ttu-id="15199-139">Tada galima įkelti, kad šablonas būtų įgyvendintas.</span><span class="sxs-lookup"><span data-stu-id="15199-139">This can then be uploaded to implement the template.</span></span> <br> <br> <span data-ttu-id="15199-140">Jei pasirinktas priminimo laiško veiksmo tipas, sąrankos formoje nebus verslo dokumento informacijos skyriaus.</span><span class="sxs-lookup"><span data-stu-id="15199-140">If the action type of collection letter is selected there will not be a business document detail section on the setup form.</span></span>


## <a name="fasttab-reference"></a><span data-ttu-id="15199-141">„FastTab” nuoroda</span><span class="sxs-lookup"><span data-stu-id="15199-141">FastTab reference</span></span>
<span data-ttu-id="15199-142">Toliau pateiktose lentelėse pateikiamas puslapių ir laukų, iš kurių galima pasiekti nurodytus „FastTab”, sąrašas ir to skirtuko informacijos aprašas.</span><span class="sxs-lookup"><span data-stu-id="15199-142">The following tables list the pages and fields that the specified FastTabs can be accessed from, along with a description of the information in that tab.</span></span> 

### <a name="process-hierarchy"></a><span data-ttu-id="15199-143">Proceso hierarchija</span><span class="sxs-lookup"><span data-stu-id="15199-143">Process hierarchy</span></span>

|     <span data-ttu-id="15199-144">Puslapis</span><span class="sxs-lookup"><span data-stu-id="15199-144">Page</span></span>                                                  |     <span data-ttu-id="15199-145">Laukas</span><span class="sxs-lookup"><span data-stu-id="15199-145">Field</span></span>                         |     <span data-ttu-id="15199-146">Aprašas</span><span class="sxs-lookup"><span data-stu-id="15199-146">Description</span></span>                           |
| --------------------------------------------------------  |-------------------------------    |---------------------------------------    |
|     <span data-ttu-id="15199-147">Mokėjimų priežiūros proceso sąranka</span><span class="sxs-lookup"><span data-stu-id="15199-147">Collections   process setup</span></span> <br> <span data-ttu-id="15199-148">Proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-148">Process automation</span></span>       |                                   |     <span data-ttu-id="15199-149">Kurkite ir tvarkykite mokėjimų priežiūros procesus, pagrįstus klientų telkinių priskyrimais.</span><span class="sxs-lookup"><span data-stu-id="15199-149">Create and   manage collections processes based on customer pool assignments.</span></span>                                                                                                                             |
|     <span data-ttu-id="15199-150">Mokėjimų priežiūros proceso sąranka</span><span class="sxs-lookup"><span data-stu-id="15199-150">Collections   process setup</span></span> <br> <span data-ttu-id="15199-151">Proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-151">Process automation</span></span>       |     <span data-ttu-id="15199-152">Hierarchija</span><span class="sxs-lookup"><span data-stu-id="15199-152">Hierarchy</span></span>                     |     <span data-ttu-id="15199-153">Apibrėžia proceso automatizavimo prioritetą, kad būtų galima priskirti klientą, jei jis priklauso keliems telkiniams.</span><span class="sxs-lookup"><span data-stu-id="15199-153">Defines the   priority of process automation to assign a customer if they belong in multiple pools.</span></span>                                                                                                   |
|     <span data-ttu-id="15199-154">Mokėjimų priežiūros proceso sąranka</span><span class="sxs-lookup"><span data-stu-id="15199-154">Collections   process setup</span></span> <br> <span data-ttu-id="15199-155">Proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-155">Process automation</span></span>       |     <span data-ttu-id="15199-156">Telkinio ID</span><span class="sxs-lookup"><span data-stu-id="15199-156">Pool ID</span></span>                       |     <span data-ttu-id="15199-157">Užklausos, apibrėžiančios klientų įrašų grupę.</span><span class="sxs-lookup"><span data-stu-id="15199-157">Queries that   define a group of customer records.</span></span>                                                                                                                                                        |
|     <span data-ttu-id="15199-158">Mokėjimų priežiūros proceso sąranka</span><span class="sxs-lookup"><span data-stu-id="15199-158">Collections   process setup</span></span> <br> <span data-ttu-id="15199-159">Proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-159">Process automation</span></span>       |     <span data-ttu-id="15199-160">Ramios dienos</span><span class="sxs-lookup"><span data-stu-id="15199-160">Quiet days</span></span>                    |     <span data-ttu-id="15199-161">Apribokite, kaip dažnai gali būti atliktas proceso veiksmas.</span><span class="sxs-lookup"><span data-stu-id="15199-161">Limit how frequently a process step can be completed.</span></span> <span data-ttu-id="15199-162">Pavyzdžiui, jei nustatytos dvi ramios dienos, kitas proceso veiksmas nebus vykdomas bent dvi dienas, jei keičiasi pagrindinė SF.</span><span class="sxs-lookup"><span data-stu-id="15199-162">For example, if two quiet days are set the next process step will not   occur for at least two days if the leading invoice changes.</span></span>     |
|     <span data-ttu-id="15199-163">Mokėjimų priežiūros proceso sąranka</span><span class="sxs-lookup"><span data-stu-id="15199-163">Collections   process setup</span></span> <br> <span data-ttu-id="15199-164">Proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-164">Process automation</span></span>       |     <span data-ttu-id="15199-165">Pašalinti iš proceso</span><span class="sxs-lookup"><span data-stu-id="15199-165">Exclude from   Process</span></span>        |     <span data-ttu-id="15199-166">Pasirinkus **Kliento skirstymo pagal terminus balansas mažesnis nei** arba **SF suma mažesnė nei**, klientas bus pašalintas iš proceso automatizavimo, jei nesilaikoma verčių kriterijų.</span><span class="sxs-lookup"><span data-stu-id="15199-166">Selecting either **Customer aging balance less than** or **Invoice amount less than** will exclude a customer from the process automation if the value criteria is not met.</span></span>                                   |

### <a name="process-details"></a><span data-ttu-id="15199-167">Proceso informacija</span><span class="sxs-lookup"><span data-stu-id="15199-167">Process details</span></span>
|     <span data-ttu-id="15199-168">Puslapis</span><span class="sxs-lookup"><span data-stu-id="15199-168">Page</span></span>                                                  |     <span data-ttu-id="15199-169">Laukas</span><span class="sxs-lookup"><span data-stu-id="15199-169">Field</span></span>                                         |      <span data-ttu-id="15199-170">Aprašas</span><span class="sxs-lookup"><span data-stu-id="15199-170">Description</span></span>                  |
|--------------------------------------------------------   |-----------------------------------------------    |----------------------------   |
|     <span data-ttu-id="15199-171">Mokėjimų priežiūros proceso sąranka</span><span class="sxs-lookup"><span data-stu-id="15199-171">Collections   process setup</span></span> <br> <span data-ttu-id="15199-172">Proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-172">Process automation</span></span>       |                                                   |     <span data-ttu-id="15199-173">Apibrėžkite veiksmus, kurių buvo imtasi pagal pagrindinę SF.</span><span class="sxs-lookup"><span data-stu-id="15199-173">Define the steps   taken based on the leading invoice.</span></span>                                                                                                |
|                                                           |     <span data-ttu-id="15199-174">Aprašas</span><span class="sxs-lookup"><span data-stu-id="15199-174">Description</span></span>                                   |     <span data-ttu-id="15199-175">Laisvos formos teksto laukas, naudojamas norint suteikti veiksmui pavadinimą ir (arba) aprašą.</span><span class="sxs-lookup"><span data-stu-id="15199-175">Free text   field used for providing a name and/or description of the step.</span></span>                                                                           |
|                                                           |     <span data-ttu-id="15199-176">Veiksmo tipas</span><span class="sxs-lookup"><span data-stu-id="15199-176">Action type</span></span>                                   |     <span data-ttu-id="15199-177">Veiklos, el. pašto ar priminimo laiškas, kuris bus sukurtas proceso veiksmo metu.</span><span class="sxs-lookup"><span data-stu-id="15199-177">Activity,   email, or collection letter that will be created by the process step.</span></span>                                                                     |
|                                                           |     <span data-ttu-id="15199-178">Verslo dokumentas</span><span class="sxs-lookup"><span data-stu-id="15199-178">Business   document</span></span>                           |     <span data-ttu-id="15199-179">Apibrėžia veiklą arba el. laiško šabloną, kuris naudojamas proceso veiksmo metu.</span><span class="sxs-lookup"><span data-stu-id="15199-179">Defines the   activity or email template that is used during the process step.</span></span>                                                                        |
|                                                           |     <span data-ttu-id="15199-180">Kada</span><span class="sxs-lookup"><span data-stu-id="15199-180">When</span></span>                                          |     <span data-ttu-id="15199-181">Nurodo, ar proceso veiksmas bus vykdomas prieš arba po pagrindinės SF apmokėjimo termino, ir nurodo lauką **Dienos, susijusios su SF apmokėjimo terminu**.</span><span class="sxs-lookup"><span data-stu-id="15199-181">Defines if   the process step will occur before or after the leading invoice due date   along with the **Days in relation to invoice due date** field.</span></span>        |
|                                                           |     <span data-ttu-id="15199-182">Dienos, susijusios su sąskaitos faktūros termino data</span><span class="sxs-lookup"><span data-stu-id="15199-182">Days in   relation to invoice due date</span></span>        |     <span data-ttu-id="15199-183">Kartu su lauku **Kada** nurodo proceso veiksmo laiką.</span><span class="sxs-lookup"><span data-stu-id="15199-183">Together   with the **When** field it identifies the timing of the process step.</span></span>                                                                          |
|                                                           |     <span data-ttu-id="15199-184">Gavėjas</span><span class="sxs-lookup"><span data-stu-id="15199-184">Recipient</span></span>                                     |     <span data-ttu-id="15199-185">Nurodo, ar el. laiškas bus išsiųstas klientui, pardavimo grupei ar mokėjimų priežiūros agentui.</span><span class="sxs-lookup"><span data-stu-id="15199-185">Identifies   if an email will be sent to a Customer, Sales group, or Collections Agent contact.</span></span>                                                   |
|                                                           |     <span data-ttu-id="15199-186">Verslo paskirties kontaktas</span><span class="sxs-lookup"><span data-stu-id="15199-186">Business   purpose contact</span></span>                    |     <span data-ttu-id="15199-187">Nurodo, kuris gavėjo el. pašto adresas naudojamas el. pašto pranešimams.</span><span class="sxs-lookup"><span data-stu-id="15199-187">Determines   which recipient’s email address is used in email communications.</span></span>                                                                                 |

### <a name="business-process-activity-template-details"></a><span data-ttu-id="15199-188">Verslo procesų veiklos šablono informacija</span><span class="sxs-lookup"><span data-stu-id="15199-188">Business process activity template details</span></span> 
|     <span data-ttu-id="15199-189">Puslapis</span><span class="sxs-lookup"><span data-stu-id="15199-189">Page</span></span>                                                  |     <span data-ttu-id="15199-190">Laukas</span><span class="sxs-lookup"><span data-stu-id="15199-190">Field</span></span>                     |      <span data-ttu-id="15199-191">Aprašas</span><span class="sxs-lookup"><span data-stu-id="15199-191">Description</span></span>                  |
|--------------------------------------------------------   |----------------------------   |-------------------------  |
|     <span data-ttu-id="15199-192">Mokėjimų priežiūros proceso sąranka</span><span class="sxs-lookup"><span data-stu-id="15199-192">Collections   process setup</span></span> <br> <span data-ttu-id="15199-193">Proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-193">Process automation</span></span>       |                               |     <span data-ttu-id="15199-194">Sąrankos proceso skyrius, nurodantis veiklos šablono informaciją.</span><span class="sxs-lookup"><span data-stu-id="15199-194">Section of   the setup process that identifies the details of the activity template.</span></span>                                                                      |
|     <span data-ttu-id="15199-195">Mokėjimų priežiūros proceso sąranka</span><span class="sxs-lookup"><span data-stu-id="15199-195">Collections   process setup</span></span> <br> <span data-ttu-id="15199-196">Proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-196">Process automation</span></span>       |     <span data-ttu-id="15199-197">Veiklos šablonas</span><span class="sxs-lookup"><span data-stu-id="15199-197">Activity   template</span></span>       |     <span data-ttu-id="15199-198">Nurodo tipą, paskirtį, dienų, kurių reikia atlikimui, skaičių ir pateikia informaciją apie veiklą, kuri bus sukurta veiklos proceso veiksmo metu.</span><span class="sxs-lookup"><span data-stu-id="15199-198">Identifies   the type, purpose, number of days to complete, and provides details about the   activity that will be created during an activity process step.</span></span>       |

### <a name="business-document-email-template-details"></a><span data-ttu-id="15199-199">Verslo dokumento el. laiško šablono išsami informacija</span><span class="sxs-lookup"><span data-stu-id="15199-199">Business document email template details</span></span> 
|     <span data-ttu-id="15199-200">Puslapis</span><span class="sxs-lookup"><span data-stu-id="15199-200">Page</span></span>                                                  |     <span data-ttu-id="15199-201">Laukas</span><span class="sxs-lookup"><span data-stu-id="15199-201">Field</span></span>     |      <span data-ttu-id="15199-202">Aprašas</span><span class="sxs-lookup"><span data-stu-id="15199-202">Description</span></span>                  |
|--------------------------------------------------------   |-------------- |-----------------------------  |
|     <span data-ttu-id="15199-203">Mokėjimų priežiūros proceso sąranka</span><span class="sxs-lookup"><span data-stu-id="15199-203">Collections   process setup</span></span> <br> <span data-ttu-id="15199-204">Proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-204">Process automation</span></span>       |               |     <span data-ttu-id="15199-205">Nurodo el. pašto aprašą, numatytąją kalbą, siuntėjo vardą ir el. pašto adresą, kuris bus sukurtas el. pašto proceso veiksmo metu.</span><span class="sxs-lookup"><span data-stu-id="15199-205">Identifies   the email description, default language, senders name, and email address that will be   created during an email process step.</span></span>        |


### <a name="collections-history"></a><span data-ttu-id="15199-206">Mokėjimų retrospektyva</span><span class="sxs-lookup"><span data-stu-id="15199-206">Collections history</span></span> 
|     <span data-ttu-id="15199-207">Puslapis</span><span class="sxs-lookup"><span data-stu-id="15199-207">Page</span></span>                              |     <span data-ttu-id="15199-208">Laukas</span><span class="sxs-lookup"><span data-stu-id="15199-208">Field</span></span>     |      <span data-ttu-id="15199-209">Aprašas</span><span class="sxs-lookup"><span data-stu-id="15199-209">Description</span></span>                                                          |
|------------------------------------   |-------------- |---------------------------------------------------------------------  |
|     <span data-ttu-id="15199-210">Mokėjimų priežiūros proceso sąranka</span><span class="sxs-lookup"><span data-stu-id="15199-210">Collections   process setup</span></span>       |               |     <span data-ttu-id="15199-211">Peržiūrėkite naujausią pasirinktos proceso hierarchijos retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="15199-211">View the   recent history for the selected process hierarchy.</span></span>     |

### <a name="collection-process-assignment"></a><span data-ttu-id="15199-212">Mokėjimų priežiūros proceso priskyrimas</span><span class="sxs-lookup"><span data-stu-id="15199-212">Collection process assignment</span></span>
|     <span data-ttu-id="15199-213">Puslapis</span><span class="sxs-lookup"><span data-stu-id="15199-213">Page</span></span>                              |     <span data-ttu-id="15199-214">Laukas</span><span class="sxs-lookup"><span data-stu-id="15199-214">Field</span></span>     |      <span data-ttu-id="15199-215">Aprašas</span><span class="sxs-lookup"><span data-stu-id="15199-215">Description</span></span>                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|     <span data-ttu-id="15199-216">Mokėjimų priežiūros proceso sąranka</span><span class="sxs-lookup"><span data-stu-id="15199-216">Collections   process setup</span></span>       |               |     <span data-ttu-id="15199-217">Peržiūrėkite klientus, priskirtus mokėjimų priežiūros procesui.</span><span class="sxs-lookup"><span data-stu-id="15199-217">View   customers assigned to a collections process.</span></span>  
|     <span data-ttu-id="15199-218">Priskyrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="15199-218">Manual assignment</span></span>               |               |     <span data-ttu-id="15199-219">Peržiūrėkite klientus, kurie buvo priskirti procesui rankiniu būdu arba pasirinkite klientus, kurie bus priskirti procesui.</span><span class="sxs-lookup"><span data-stu-id="15199-219">View customers that have been manually assigned to a process or select customers to be assigned to a process.</span></span> |
|     <span data-ttu-id="15199-220">Peržiūrėti proceso priskyrimą</span><span class="sxs-lookup"><span data-stu-id="15199-220">Preview process assignment</span></span>      |               |     <span data-ttu-id="15199-221">Peržiūrėkite klientus, kurie bus priskirti vykdomai strategijai.</span><span class="sxs-lookup"><span data-stu-id="15199-221">Preview the customers that will be assigned to a strategy when it is run.</span></span>   |
|     <span data-ttu-id="15199-222">Peržiūrėti kliento priskyrimą</span><span class="sxs-lookup"><span data-stu-id="15199-222">Preview customer assignment</span></span>     |               |     <span data-ttu-id="15199-223">Peržiūrėkite strategiją, kuriai priskirtas konkretus klientas.</span><span class="sxs-lookup"><span data-stu-id="15199-223">View the strategy that a specific customer is assigned.</span></span>    |
 
### <a name="parameters"></a><span data-ttu-id="15199-224">Parametrai</span><span class="sxs-lookup"><span data-stu-id="15199-224">Parameters</span></span>
|     <span data-ttu-id="15199-225">Puslapis</span><span class="sxs-lookup"><span data-stu-id="15199-225">Page</span></span>                                                                  |     <span data-ttu-id="15199-226">Laukas</span><span class="sxs-lookup"><span data-stu-id="15199-226">Field</span></span>                                             |      <span data-ttu-id="15199-227">Aprašas</span><span class="sxs-lookup"><span data-stu-id="15199-227">Description</span></span>                              |
|-------------------------------------------------------------------------- |------------------------------------------------------ |-------------------------------------  |
|     <span data-ttu-id="15199-228">Gautinų sumų parametrai > Mokėjimų priežiūros proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-228">Accounts   receivable parameters > Collections process automation</span></span>     |     <span data-ttu-id="15199-229">Procentas klientų vienai paketinei užduočiai</span><span class="sxs-lookup"><span data-stu-id="15199-229">Percentage   of customers per batch task</span></span>          |     <span data-ttu-id="15199-230">Parametras, skirtas nustatyti paketinių užduočių skaičių viename automatizavimo procese.</span><span class="sxs-lookup"><span data-stu-id="15199-230">Setting to   determine the number of batch tasks per automation process.</span></span>                                          |
|     <span data-ttu-id="15199-231">Gautinų sumų parametrai > Mokėjimų priežiūros proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-231">Accounts   receivable parameters > Collections process automation</span></span>     |     <span data-ttu-id="15199-232">Registruoti priminimo laiškus automatiškai</span><span class="sxs-lookup"><span data-stu-id="15199-232">Post   Collection letters automatically</span></span>           |     <span data-ttu-id="15199-233">Priminimo laiškų veiksmų tipai užregistruos laišką automatizavimo metu.</span><span class="sxs-lookup"><span data-stu-id="15199-233">Collection   letter action types will post the letter during the automation.</span></span>                                      |
|     <span data-ttu-id="15199-234">Gautinų sumų parametrai > Mokėjimų priežiūros proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-234">Accounts   receivable parameters > Collections process automation</span></span>     |     <span data-ttu-id="15199-235">Automatizavimo veiklų kūrimas</span><span class="sxs-lookup"><span data-stu-id="15199-235">Create   activities for automation</span></span>                |     <span data-ttu-id="15199-236">Kurkite ir uždarykite ne veiklų veiksmo tipų veiklas, kad būtų galima peržiūrėti visus automatizuotus veiksmus, atliktus sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="15199-236">Create and   close activities for non-activity action types to view all automated steps   taken on an account.</span></span>        |
|     <span data-ttu-id="15199-237">Gautinų sumų parametrai > Mokėjimų priežiūros proceso automatizavimas</span><span class="sxs-lookup"><span data-stu-id="15199-237">Accounts   receivable parameters > Collections process automation</span></span>     |     <span data-ttu-id="15199-238">Dienų, kiek truks mokėjimų priežiūros proceso automatizavimas, skaičius</span><span class="sxs-lookup"><span data-stu-id="15199-238">Days to keep   collections process automation</span></span>     |     <span data-ttu-id="15199-239">Apibrėžia dienų, kiek saugoma mokėjimų priežiūros retrospektyva, skaičių.</span><span class="sxs-lookup"><span data-stu-id="15199-239">Defines the   number of days collections history is stored.</span></span>                                                       |