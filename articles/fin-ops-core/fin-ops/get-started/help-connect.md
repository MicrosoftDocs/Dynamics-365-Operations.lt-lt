---
title: Žinyno sistemos prijungimas
description: Šioje temoje aprašyti „Finance and Operations“ programų žinyno sistemos komponentai, apžvelgiama, kaip juos sujungti, ir pateikiama pasirinktinio žinyno kūrimo suvestinė.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4427388d75c1aef40a978ce35c831d5b714f2562
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006177"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="6341e-103">Žinyno sistemos prijungimas</span><span class="sxs-lookup"><span data-stu-id="6341e-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6341e-104">Šioje temoje aprašomi žinyno sistemos komponentai, naudojami „Finance and Operations“ programoms, pvz. „Dynamics 365 Finance“, „Supply Chain Management“, „Commerce“ ir „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="6341e-104">This topic describes the components of the Help system for Finance and Operations apps, such as Dynamics 365 Finance, Supply Chain Management, Commerce, and Human Resources.</span></span> <span data-ttu-id="6341e-105">Joje pateikiama apžvalga apie tai, kaip šiuos komponentus sujungti, ir pasirinktinio žinyno kūrimo suvestinė.</span><span class="sxs-lookup"><span data-stu-id="6341e-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="6341e-106">Žinyno architektūra</span><span class="sxs-lookup"><span data-stu-id="6341e-106">Help architecture</span></span>

<span data-ttu-id="6341e-107">Toliau esančiame paveikslėlyje pavaizduotos žinyno sistemos dalys.</span><span class="sxs-lookup"><span data-stu-id="6341e-107">The following illustration shows the parts of the Help system.</span></span> <span data-ttu-id="6341e-108">Vidinio žinyno sistema straipsnius ima iš https://docs.microsoft.com, o užduočių vadovus – iš „Lifecycle Services‟ (LCS) verslo procesų modeliavimo įrankio.</span><span class="sxs-lookup"><span data-stu-id="6341e-108">The in-product Help system pulls articles from https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="6341e-109">Žvaigždute (\*) pažymėtos diagramoje išvardytos funkcijos yra planuojamos, bet dar neprieinamos.</span><span class="sxs-lookup"><span data-stu-id="6341e-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="6341e-110">[![Žinyno architektūra](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="6341e-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="6341e-111">Žinyno sistemos prijungimas</span><span class="sxs-lookup"><span data-stu-id="6341e-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="6341e-112">Skirtukas **Užduočių vedliai** „Dynamics 365 Human Resources“ arba „Commerce“ šiuo metu nėra pasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="6341e-112">The **Task guides** tab is currently not available in Dynamics 365 Human Resources or Commerce.</span></span> <span data-ttu-id="6341e-113">Šiuo metu dirbame, kad įgalintume šią funkciją būsimame leidime.</span><span class="sxs-lookup"><span data-stu-id="6341e-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="6341e-114">Darbo su „Human Resources“ pradžioje išlieka pasiekiami pagrindinių funkcijų užduočių vedliai.</span><span class="sxs-lookup"><span data-stu-id="6341e-114">The Task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="6341e-115">„Human Resources“ ir „Commerce“ procedūrinis žinynas taip pat pasiekiamas svetainėje docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="6341e-115">Procedural help is also available on the docs.microsoft.com site for both Human Resources and Commerce.</span></span>

<span data-ttu-id="6341e-116">Naudodami puslapį **Sistemos parametrai**, sistemos administratoriai prijungia žinyno sistemos dalis diegti.</span><span class="sxs-lookup"><span data-stu-id="6341e-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="6341e-117">[![Forma Sistemos parametrai su žinyno parametrais](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="6341e-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="6341e-118">Puslapyje **Sistemos parametrai** atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6341e-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6341e-119">Pirmą kartą atidarę skirtuką **Žinynas**, turite prisijungti prie „Lifecycle Services“.</span><span class="sxs-lookup"><span data-stu-id="6341e-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="6341e-120">Būtinai spustelėkite formos viduryje pateiktą saitą, palaukite, kol prisijungsite, uždarykite dialogo langą ir tada spustelėkite **Gerai**, norėdami atidaryti puslapį **Sistemos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6341e-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="6341e-121">[![Prisijungti prie LCS](./media/connect-to-lcs-crop-1024x365.png "Prisijungti prie LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="6341e-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="6341e-122">Pasirinkite, prie kurio „Lifecycle Services‟ projekto prisijungti.</span><span class="sxs-lookup"><span data-stu-id="6341e-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="6341e-123">Pasirinkite, iš kurių BPM bibliotekų (pasirinkto projekto) gauti užduočių įrašus.</span><span class="sxs-lookup"><span data-stu-id="6341e-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="6341e-124">Nustatykite BPM bibliotekų rodymo tvarką.</span><span class="sxs-lookup"><span data-stu-id="6341e-124">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="6341e-125">Taip nustatoma tvarka, kuria užduočių įrašai iš bibliotekų bus rodomi **Žinyno** srityje.</span><span class="sxs-lookup"><span data-stu-id="6341e-125">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="6341e-126">Atlikę šiuos veiksmus, galite atidaryti sritį **Žinynas** ir spustelėti skirtuką **Užduočių vedliai**. Matysite užduočių vedlius, taikomus „Finance and Operations“ programose puslapiui, kuriame dabar esate.</span><span class="sxs-lookup"><span data-stu-id="6341e-126">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="6341e-127">Jei nerasite nė vieno užduočių vedlio, galite įvedę raktažodžius patikslinti iešką.</span><span class="sxs-lookup"><span data-stu-id="6341e-127">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="6341e-128">Išverstų užduočių vedlių rodymas</span><span class="sxs-lookup"><span data-stu-id="6341e-128">Showing translated task guides</span></span>

<span data-ttu-id="6341e-129">Išversti užduočių vedliai pirmiausia buvo nusiųsti į APQC bendrąją biblioteką (2016 m. gegužės mėn.) ir darbo pradžios biblioteką.</span><span class="sxs-lookup"><span data-stu-id="6341e-129">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="6341e-130">Norėdami „Finance and Operations“ programose peržiūrėti lokalizuotą užduočių vedlį, įsitikinkite, kad esate prisijungę prie gegužės mėn. bibliotekos.</span><span class="sxs-lookup"><span data-stu-id="6341e-130">In Finance and Operations apps, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="6341e-131">Ta kalba, kuria atskiram vartotojui rodomas užduočių vedlys, priklauso nuo kalbos parametrų, nustatytų dalyje **Parinktys** &gt; **Nuostatos**.</span><span class="sxs-lookup"><span data-stu-id="6341e-131">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="6341e-132">Nors daug užduočių vedlių yra išversti, šiuo metu kliente nerodomi išversti užduočių vedlių pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="6341e-132">Even though many task guides have been translated, right now the client is not showing the translated task guide names.</span></span> <span data-ttu-id="6341e-133">Be to, šiuo metu gegužės mėn. bibliotekoje galima rasti tik tuos išverstus užduočių vedlius, kurie buvo išleisti 2016 m. vasario mėnesį.</span><span class="sxs-lookup"><span data-stu-id="6341e-133">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="6341e-134">Mes išleisime atnaujintą biblioteką su papildomais vertimais.</span><span class="sxs-lookup"><span data-stu-id="6341e-134">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="6341e-135">Jei užduočių vedlys yra išverstas, atidarius tą užduočių vedlį visas užduočių vedlio tekstas bus rodomas jūsų pasirinkta kalba.</span><span class="sxs-lookup"><span data-stu-id="6341e-135">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="6341e-136">Jei užduočių vedlys dar neišverstas, jį atidarius tik dalis užduočių vedlio teksto (valdiklių tekstas) bus rodoma jūsų pasirinkta kalba.</span><span class="sxs-lookup"><span data-stu-id="6341e-136">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="6341e-137">Pasirinktinio žinyno kūrimas</span><span class="sxs-lookup"><span data-stu-id="6341e-137">Creating custom help</span></span>

<span data-ttu-id="6341e-138">Norėdami sukurti pasirinktinį žinyną, galite naudoti užduočių vedlius arba susieti žiniatinklio svetainę su sritimi Žinynas.</span><span class="sxs-lookup"><span data-stu-id="6341e-138">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="6341e-139">Pasirinktinio žinyno kūrimas naudojant užduočių vedlius</span><span class="sxs-lookup"><span data-stu-id="6341e-139">Create custom help with task guides</span></span>

<span data-ttu-id="6341e-140">Kurdami užduočių įrašus, kurie atspindi jūsų diegimą, ir juos įrašydami į LCS verslo procesų biblioteką, galite sukurti pasirinktinį „Finance“, „Supply Chain Management“ ir „Commerce“ žinyną.</span><span class="sxs-lookup"><span data-stu-id="6341e-140">You can create custom help for Finance, Supply Chain Management, and Commerce by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="6341e-141">Programoje „Human Resources“ negalima sukurti pasirinktinių užduočių vedlių.</span><span class="sxs-lookup"><span data-stu-id="6341e-141">You cannot create custom task guides for Human Resources.</span></span>

<span data-ttu-id="6341e-142">Jei esate partneris ir biblioteką paaukštinsite iki įmonės bibliotekos bei įtrauksite ją į sprendimą, biblioteką galės naudoti jūsų klientai.</span><span class="sxs-lookup"><span data-stu-id="6341e-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="6341e-143">Taip pat galite kopijuoti APQC suvienodintą visuotinę biblioteką ir tada savo kopiją atidaryti, iš jos atidaryti užduočių įrašus ir juos modifikuoti bei įrašus įrašyti su savo pakeitimais.</span><span class="sxs-lookup"><span data-stu-id="6341e-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="6341e-144">Daugiau informacijos žr. [Užduoties įrašymo ištekliai](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="6341e-144">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="6341e-145">Pasirinktinės žiniatinklio svetainės susiejimas</span><span class="sxs-lookup"><span data-stu-id="6341e-145">Connect a custom site</span></span>

<span data-ttu-id="6341e-146">„Microsoft“ yra pateikusi techninę dokumentaciją ir pavyzdinį kodą, kuriuo aprašoma, kaip kurti ir susieti pasirinktinę žinyno žiniatinklio svetainę su sritimi Žinynas.</span><span class="sxs-lookup"><span data-stu-id="6341e-146">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="6341e-147">Daugiau informacijos ieškokite:</span><span class="sxs-lookup"><span data-stu-id="6341e-147">For more information, see:</span></span>

- [<span data-ttu-id="6341e-148">„Finance and Operations“programų pasirinktinio žinyno kūrimas (techninė dokumentacija)</span><span class="sxs-lookup"><span data-stu-id="6341e-148">Create Custom Help for Finance and Operations apps (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="6341e-149">Pasirinktinio žinyno „GitHub“ saugykla</span><span class="sxs-lookup"><span data-stu-id="6341e-149">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="6341e-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6341e-150">Additional resources</span></span>

[<span data-ttu-id="6341e-151">Žinyno sistema</span><span class="sxs-lookup"><span data-stu-id="6341e-151">Help system</span></span>](help-overview.md)

[<span data-ttu-id="6341e-152">Užduoties įrašymo ištekliai</span><span class="sxs-lookup"><span data-stu-id="6341e-152">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="6341e-153">Dokumentų ar mokymų kūrimas naudojant užduočių įrašymo priemonę</span><span class="sxs-lookup"><span data-stu-id="6341e-153">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
