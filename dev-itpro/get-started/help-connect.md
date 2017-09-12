---
title: "Žinyno sistemos prijungimas"
description: "Šioje temoje aprašyti „Microsoft Dynamics 365 for Finance and Operations“ žinyno sistemos komponentai, apžvelgiama, kaip juos sujungti, ir pateikiama pasirinktinio žinyno kūrimo suvestinė."
author: margoc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: acb832c422ccb5ddb98d6ddd6b69d2e2c3e11057
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---

# <a name="connect-the-help-system"></a><span data-ttu-id="94f87-103">Žinyno sistemos prijungimas</span><span class="sxs-lookup"><span data-stu-id="94f87-103">Connect the Help system</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="94f87-104">Šioje temoje aprašomi „Microsoft Dynamics 365 for Finance and Operations“ žinyno sistemos komponentai.</span><span class="sxs-lookup"><span data-stu-id="94f87-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="94f87-105">Joje pateikiama apžvalga apie tai, kaip šiuos komponentus sujungti, ir pasirinktinio žinyno kūrimo suvestinė.</span><span class="sxs-lookup"><span data-stu-id="94f87-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="94f87-106">Žinyno architektūra</span><span class="sxs-lookup"><span data-stu-id="94f87-106">Help architecture</span></span>
<span data-ttu-id="94f87-107">Tolesnėje iliustracijoje rodomos „Finance and Operations‟ žinyno sistemos dalys.</span><span class="sxs-lookup"><span data-stu-id="94f87-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="94f87-108">Vidinio žinyno sistema straipsnius ima iš „Finance and Operations‟ svetainės adresu https://docs.microsoft.com, o užduočių vadovus – iš „Lifecycle Services‟ (LCS) verslo procesų modeliavimo įrankio.</span><span class="sxs-lookup"><span data-stu-id="94f87-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="94f87-109">Žvaigždute (\*) pažymėtos diagramoje išvardytos funkcijos yra planuojamos, bet dar neprieinamos.</span><span class="sxs-lookup"><span data-stu-id="94f87-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="94f87-110">[![Žinyno architektūra](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="94f87-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="94f87-111">Žinyno sistemos prijungimas</span><span class="sxs-lookup"><span data-stu-id="94f87-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="94f87-112">Skirtukas **Užduočių vedliai** programose „Microsoft Dynamics 365 for Talent“ ir „Microsoft Dynamics 365 for Retail‟ šiuo metu nepasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="94f87-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="94f87-113">Šiuo metu dirbame, kad įgalintume šią funkciją būsimame leidime.</span><span class="sxs-lookup"><span data-stu-id="94f87-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="94f87-114">Darbo su „Talent‟ pradžioje išlieka pasiekiami pagrindinių funkcijų užduočių gidai.</span><span class="sxs-lookup"><span data-stu-id="94f87-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="94f87-115">„Retail“ ir „Talent“ procedūrinį žinyną taip pat galite rasti svetainėje docs.microsoft.com ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)).</span><span class="sxs-lookup"><span data-stu-id="94f87-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) for both Retail and Talent.</span></span>
 

<span data-ttu-id="94f87-116">Naudodami puslapį **Sistemos parametrai**, sistemos administratoriai prijungia žinyno sistemos dalis diegti.</span><span class="sxs-lookup"><span data-stu-id="94f87-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="94f87-117">[![Sistemos parametrų forma su žinyno parametrais](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Puslapyje **Sistemos parametrai** atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="94f87-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94f87-118">Pirmą kartą atidarę skirtuką **Žinynas**, turite prisijungti prie „Lifecycle Services“.</span><span class="sxs-lookup"><span data-stu-id="94f87-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="94f87-119">Būtinai spustelėkite formos viduryje pateiktą saitą, palaukite, kol prisijungsite, uždarykite dialogo langą ir tada spustelėkite **Gerai**, norėdami atidaryti puslapį **Sistemos parametra**.[![Prisijungimas prie LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="94f87-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="94f87-120">Pasirinkite, prie kurio „Lifecycle Services‟ projekto prisijungti.</span><span class="sxs-lookup"><span data-stu-id="94f87-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="94f87-121">Pasirinkite, iš kurių BPM bibliotekų (pasirinkto projekto) gauti užduočių įrašus.</span><span class="sxs-lookup"><span data-stu-id="94f87-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="94f87-122">Programoje „Finance and Operations” norėdami pasiekti „Microsoft” turinį, pasirinkite „Microsoft Dynamics 365 for Finance and Operations“ 2017 m. vasario mėn. QPC bendrąją biblioteką.</span><span class="sxs-lookup"><span data-stu-id="94f87-122">For Finance and Operations, for Microsoft content, select the February 2017 QPC Unified Library for Microsoft Dynamics 365 for Finance and Operations.</span></span> 
    - <span data-ttu-id="94f87-123">Programai „Retail“ biblioteką išleisime liepos mėn.</span><span class="sxs-lookup"><span data-stu-id="94f87-123">For Retail, we will be releasing a library in July.</span></span> 
    - <span data-ttu-id="94f87-124">Jums nereikia pasirinkti bibliotekos „Talent“ atveju – ryšys su tinkama biblioteka jau sukurtas.</span><span class="sxs-lookup"><span data-stu-id="94f87-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="94f87-125">Nustatykite BPM bibliotekų rodymo tvarką.</span><span class="sxs-lookup"><span data-stu-id="94f87-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="94f87-126">Taip nustatoma tvarka, kuria užduočių įrašai iš bibliotekų bus rodomi **Žinyno** srityje.</span><span class="sxs-lookup"><span data-stu-id="94f87-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="94f87-127">Atlikę šiuos veiksmus, galite atidaryti **Žinyno** sritį ir spustelėti **Užduočių vadovų** skirtuką.</span><span class="sxs-lookup"><span data-stu-id="94f87-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab.</span></span> <span data-ttu-id="94f87-128">Dabar matysite užduočių vedlius, taikomus tam „Finance and Operations“ puslapiui, kuriame dabar esate.</span><span class="sxs-lookup"><span data-stu-id="94f87-128">You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="94f87-129">Jei nerasite nė vieno užduočių vedlio, galite įvedę raktažodžius patikslinti iešką.</span><span class="sxs-lookup"><span data-stu-id="94f87-129">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="94f87-130">Išverstų užduočių vedlių rodymas</span><span class="sxs-lookup"><span data-stu-id="94f87-130">Showing translated task guides</span></span>

<span data-ttu-id="94f87-131">Išversti užduočių vedliai pirmiausia buvo nusiųsti į APQC bendrąją biblioteką (2016 m. gegužės mėn.) ir darbo pradžios biblioteką.</span><span class="sxs-lookup"><span data-stu-id="94f87-131">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="94f87-132">Norėdami „Finance and Operations“ peržiūrėti lokalizuotą užduočių vedlį, įsitikinkite, kad esate prisijungę prie gegužės mėn. bibliotekos.</span><span class="sxs-lookup"><span data-stu-id="94f87-132">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="94f87-133">Ta kalba, kuria atskiram vartotojui rodomas užduočių vedlys, priklauso nuo kalbos parametrų, nustatytų dalyje **Parinktys** &gt; **Nuostatos**.</span><span class="sxs-lookup"><span data-stu-id="94f87-133">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="94f87-134">Nors daug užduočių vedlių yra išversti, šiuo metu „Finance and Operations“ kliente nerodomi išversti užduočių vedlių pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="94f87-134">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="94f87-135">Be to, šiuo metu gegužės mėn. bibliotekoje galima rasti tik tuos išverstus užduočių vedlius, kurie buvo išleisti 2016 m. vasario mėnesį.</span><span class="sxs-lookup"><span data-stu-id="94f87-135">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="94f87-136">Mes išleisime atnaujintą biblioteką su papildomais vertimais.</span><span class="sxs-lookup"><span data-stu-id="94f87-136">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="94f87-137">Jei užduočių vedlys yra išverstas, atidarius tą užduočių vedlį visas užduočių vedlio tekstas bus rodomas jūsų pasirinkta kalba.</span><span class="sxs-lookup"><span data-stu-id="94f87-137">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="94f87-138">Jei užduočių vedlys dar neišverstas, jį atidarius tik dalis užduočių vedlio teksto (valdiklių tekstas) bus rodoma jūsų pasirinkta kalba.</span><span class="sxs-lookup"><span data-stu-id="94f87-138">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="94f87-139">Pasirinktinio žinyno kūrimas</span><span class="sxs-lookup"><span data-stu-id="94f87-139">Creating custom help</span></span>
<span data-ttu-id="94f87-140">Kurdami užduočių įrašus, kurie atspindi jūsų diegimą, ir juos įrašydami į LCS verslo procesų biblioteką, galite sukurti pasirinktinį „Finance and Operations‟ ir „Retail“ žinyną.</span><span class="sxs-lookup"><span data-stu-id="94f87-140">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="94f87-141">„Talent“ pasirinktinių užduočių vedlių sukurti negalima.</span><span class="sxs-lookup"><span data-stu-id="94f87-141">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="94f87-142">Jei esate partneris ir biblioteką paaukštinsite iki įmonės bibliotekos bei įtrauksite ją į sprendimą, biblioteką galės naudoti jūsų klientai.</span><span class="sxs-lookup"><span data-stu-id="94f87-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="94f87-143">Taip pat galite kopijuoti APQC suvienodintą visuotinę biblioteką ir tada savo kopiją atidaryti, iš jos atidaryti užduočių įrašus ir juos modifikuoti bei įrašus įrašyti su savo pakeitimais.</span><span class="sxs-lookup"><span data-stu-id="94f87-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="94f87-144">Daugiau informacijos žr. temoje [Kaip sukurti užduoties įrašą ir jį naudoti kaip dokumentaciją ar mokymą](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="94f87-144">For more information, see [How to create a task recording to use as documentation or training](../user-interface/task-recorder.md).</span></span>

<a name="see-also"></a><span data-ttu-id="94f87-145">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="94f87-145">See also</span></span>
--------

[<span data-ttu-id="94f87-146">Žinyno apžvalga</span><span class="sxs-lookup"><span data-stu-id="94f87-146">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="94f87-147">Užduočių įrašymo priemonės apžvalga</span><span class="sxs-lookup"><span data-stu-id="94f87-147">Task recorder overview</span></span>](../user-interface/task-recorder.md)

[<span data-ttu-id="94f87-148">Kaip kurti užduoties įrašą ir naudoti kaip dokumentus ar mokymą</span><span class="sxs-lookup"><span data-stu-id="94f87-148">How to create a task recording to use as documentation or training</span></span>](../user-interface/task-recorder-training-docs.md)





