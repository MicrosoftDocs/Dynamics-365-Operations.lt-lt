---
title: „Finance and Operations“ programų žinyno funkcijų konfigūravimas
description: Šioje temoje pateikiama informacija apie kai kurių „Microsoft Dynamics 365“ programų žinyno sistemos komponentus.
author: margoc
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82bb9a09e6d302b0d453ceb5131da039769b58fb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745694"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="0aa2e-103">„Finance and Operations“ programų žinyno funkcijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="0aa2e-103">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0aa2e-104">Šioje temoje rasite tokių „Finance and Operations“ programų, kaip „Microsoft Dynamics 365 Finance“, „Dynamics 365 Supply Chain Management“, „Dynamics 365 Commerce“ ir „Dynamics 365 Human Resources“, žinyno sistemos komponentų apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-104">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0aa2e-105">Šioje temoje taip pat aiškinama, kaip sujungti šiuos komponentus, ir pateikiama pasirinktinio žinyno kūrimo proceso santrauka.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-105">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="0aa2e-106">Žinyno architektūra</span><span class="sxs-lookup"><span data-stu-id="0aa2e-106">Help architecture</span></span>

<span data-ttu-id="0aa2e-107">„Finance and Operations“ programose yra konceptualių apžvalgų ir kitų temų, kurios publikuojamos svetainėje [https://docs.microsoft.com/dynamics365](/dynamics365/).</span><span class="sxs-lookup"><span data-stu-id="0aa2e-107">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="0aa2e-108">Šį turinį galima pasiekti iš produkto srities **Žinynas**.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-108">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="0aa2e-109">Toliau esančiame paveikslėlyje pavaizduotos žinyno sistemos dalys.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-109">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="0aa2e-110">[![Žinyno architektūra](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="0aa2e-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="0aa2e-111">Produkto žinyno sistema gauna straipsnius iš docs.microsoft.com ir kitų prijungtų svetainių.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-111">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="0aa2e-112">Ji taip pat gauna užduočių vedlius, kurie saugomi verslo procesų modeliavimo įrankyje (BPM) portale „ Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="0aa2e-112">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="0aa2e-113">Užduočių vedlių įtraukimas</span><span class="sxs-lookup"><span data-stu-id="0aa2e-113">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="0aa2e-114">Skirtukas **Užduočių vedliai** šiuo metu „Human Resources“ arba „Commerce“ nepasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-114">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="0aa2e-115">Tačiau darbo su „Human Resources“ pradžioje išlieka pasiekiami pagrindinių funkcijų užduočių vedliai.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-115">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="0aa2e-116">„Human Resources“ ir „Commerce“ procedūrinis žinynas taip pat pasiekiamas svetainėje [https://docs.microsoft.com/dynamics365](/dynamics365/).</span><span class="sxs-lookup"><span data-stu-id="0aa2e-116">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="0aa2e-117">Puslapyje **Sistemos parametrai** sistemos administratoriai gali konfigūruoti prieigą prie atitinkamų diegimui skirtų užduoties vedlių bibliotekų.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-117">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="0aa2e-118">Norėdami konfigūruoti žinyną, turite prisijungti naudodami paskyrą tame pačiame nuomotojuje, kuriame įdiegta programa.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-118">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="0aa2e-119">LCS bibliotekos negalim prijungti iš programos egzemplioriaus, veikiančio vietiniame virtualiajame standžiajame diske (VHD).</span><span class="sxs-lookup"><span data-stu-id="0aa2e-119">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="0aa2e-120">[![Forma Sistemos parametrai su žinyno parametrais](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="0aa2e-120">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="0aa2e-121&quot;>Norėdami konfigūruoti sprendimo užduoties vedlius, atlikite puslapyje **Sistemos parametrai** nurodytus veiksmus.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;0aa2e-121&quot;>To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id=&quot;0aa2e-122&quot;>Pirmą kartą atidarę skirtuką **Žinynas**, turite prisijungti prie „Lifecycle Services“.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;0aa2e-122&quot;>The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id=&quot;0aa2e-123&quot;>Būtinai pasirinkite formos viduryje pateiktą saitą, palaukite, kol prisijungsite, uždarykite dialogo langą, tada pasirinkite **Gerai**, kad patektumėte į puslapį **Sistemos parametrai**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;0aa2e-123&quot;>Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id=&quot;0aa2e-124&quot;>[![Prisijungti prie LCS](./media/connect-to-lcs-crop-1024x365.png &quot;Prisijungti prie LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="0aa2e-124">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="0aa2e-125">Pasirinkite, prie kurio „Lifecycle Services‟ projekto prisijungti.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-125">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="0aa2e-126">Pasirinkite, iš kurių BPM bibliotekų (pasirinkto projekto) gauti užduočių įrašus.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-126">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="0aa2e-127">Nustatykite BPM bibliotekų rodymo tvarką.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="0aa2e-128">Rodymo tvarka apibrėžia tvarką, kuria užduočių įrašai iš bibliotekų bus rodomi srityje **Žinynas**.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-128">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="0aa2e-129">Atlikę šiuos veiksmus, galite atidaryti sritį **Žinynas** ir pasirinkti skirtuką **Užduočių vedliai**. Matysite užduočių vedlius, taikomus puslapiui, kuriame dabar esate „Finance and Operations“ programose.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-129">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="0aa2e-130">Jei nerasite nė vieno užduočių vedlio, galite įvedę raktažodžius patikslinti iešką.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="0aa2e-131">Išverstų užduočių vedlių rodymas</span><span class="sxs-lookup"><span data-stu-id="0aa2e-131">Showing translated task guides</span></span>

<span data-ttu-id="0aa2e-132">Išversti užduočių vedliai pirmiausia buvo išleisti APQC bendrojoje bibliotekoje (2016 m. gegužės mėn.) ir darbo pradžios bibliotekoje.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-132">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="0aa2e-133">Norėdami peržiūrėti lokalizuoto užduočių vedlio žinyną, įsitikinkite, kad jūsų „Dynamics 365“ sprendimas prijungtas prie 2016 m. gegužės mėn. bibliotekos.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-133">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="0aa2e-134">Vartotojai gali pakeisti kalbą, kuria rodomas užduočių vedlys: kalbos parametrai keičiami dalyje **Parinktys** &gt; **Nuostatos**.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-134">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="0aa2e-135">Nors daug užduočių vedlių yra išversti, šiuo metu kliente nerodomi išversti užduočių vedlių pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-135">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="0aa2e-136">Be to, 2016 m. gegužės mėn. bibliotekoje pateikiami tik 2016 m. vasario mėnesį išleistų užduočių vedlių vertimai.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-136">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="0aa2e-137">„Microsoft“ išleis atnaujintą biblioteką, kurioje bus papildomų vertimų.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-137">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="0aa2e-138">Jei užduočių vedlys yra išverstas, atidarius tą užduočių vedlį visas užduočių vedlio tekstas bus rodomas jūsų pasirinkta kalba.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="0aa2e-139">Jei užduočių vedlys dar neišverstas, jį atidarius tik dalis užduočių vedlio teksto (valdiklių tekstas) bus rodoma jūsų pasirinkta kalba.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="0aa2e-140">Pasirinktinio žinyno įtraukimas</span><span class="sxs-lookup"><span data-stu-id="0aa2e-140">Adding custom Help</span></span>

<span data-ttu-id="0aa2e-141">Norėdami sukurti pasirinktinį žinyną galite naudoti užduočių vedlius arba pasirinktinio žinyno svetainę galite prijungti prie srities **Žinynas**.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-141">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="0aa2e-142">Pasirinktinio žinyno kūrimas naudojant užduočių vedlius</span><span class="sxs-lookup"><span data-stu-id="0aa2e-142">Create custom Help by using task guides</span></span>

<span data-ttu-id="0aa2e-143">Pasirinktinį palaikomų programų žinyną galite kurti kurdami užduočių įrašus, kurie atspindi jūsų diegimą, ir tada įrašydami juos į LCS verslo procesų biblioteką.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-143">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="0aa2e-144">Programoje „Human Resources“ pasirinktinių užduočių vedlių kurti negalite.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-144">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="0aa2e-145">Jei esate partneris ir biblioteką paaukštinsite iki įmonės bibliotekos bei įtrauksite ją į sprendimą, biblioteką galės naudoti jūsų klientai.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-145">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="0aa2e-146">Taip pat galite sukurti APQC suvienodintos bibliotekos kopiją ir tada užduočių įrašus atidaryti kopijoje, juos redaguoti ir įrašyti savo pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-146">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="0aa2e-147">Daugiau informacijos žr. [Užduoties įrašymo ištekliai](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="0aa2e-147">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="0aa2e-148">Pasirinktinio žinyno svetainės prijungimas</span><span class="sxs-lookup"><span data-stu-id="0aa2e-148">Connect a custom Help site</span></span>

<span data-ttu-id="0aa2e-149">„Finance and Operations“ programos retai naudojamos savo parengtoje formoje.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-149">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="0aa2e-150">Vietoj to sprendimas yra pritaikomas ir išplečiamas, kad atitiktų organizacijos poreikius.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-150">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="0aa2e-151">Taip pat galite tinkinti ir išplėsti žinyno funkcijas.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-151">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="0aa2e-152">Pavyzdžiui, pasirinktinį žinyną galite įtraukti į produkto sritį **Žinynas**.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-152">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="0aa2e-153">„Microsoft“ pateikė priemonių rinkinį, kuris jums padės įdiegti ir prijungti pasirinktinį žinyną prie srities **Žinynas**.</span><span class="sxs-lookup"><span data-stu-id="0aa2e-153">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="0aa2e-154">Informacijos, kaip sukonfigūruoti pasirinktinį žinyno sprendimą, kuris yra prijungtas prie srities **Žinynas**, žr. [Pasirinktinio žinyno apžvalga](../../dev-itpro/help/custom-help-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0aa2e-154">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="0aa2e-155">Jei norite bendradarbiauti su „Microsoft“ įrankiais ir procesais, kad galėtumėte tinkinti žinyną, užpildykite formą apsilankę [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span><span class="sxs-lookup"><span data-stu-id="0aa2e-155">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="0aa2e-156">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="0aa2e-156">See also</span></span>

[<span data-ttu-id="0aa2e-157">Žinyno sistema</span><span class="sxs-lookup"><span data-stu-id="0aa2e-157">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="0aa2e-158">Pasirinktinio žinyno apžvalga</span><span class="sxs-lookup"><span data-stu-id="0aa2e-158">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="0aa2e-159">Užduoties įrašymo ištekliai</span><span class="sxs-lookup"><span data-stu-id="0aa2e-159">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="0aa2e-160">Dokumentų ar mokymų kūrimas naudojant užduočių įrašymo priemonę</span><span class="sxs-lookup"><span data-stu-id="0aa2e-160">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="0aa2e-161">Pasirinktinio žinyno „GitHub“ saugykla</span><span class="sxs-lookup"><span data-stu-id="0aa2e-161">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]