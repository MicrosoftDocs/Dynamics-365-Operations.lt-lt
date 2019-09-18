---
title: Supažindinimo vadovų ir šablonų redagavimas „Dynamics 365 for Talent - Onboard”
description: Šioje temoje paaiškinama, kaip įtraukti veiklas ir kitą informaciją į supažindinimo vadovus ir šablonus „Microsoft Dynamics 365 for Talent - Onboard”.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 68afc5d789d1f4af67cd2ec73eb0e073efad0761
ms.sourcegitcommit: 4ff8c2c2f3705d8045df66f2c4393253e05b49ed
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864398"
---
# <a name="edit-onboarding-guides-and-templates-in-dynamics-365-for-talent-onboard"></a><span data-ttu-id="61854-103">Supažindinimo vadovų ir šablonų redagavimas „Dynamics 365 for Talent: Onboard”</span><span class="sxs-lookup"><span data-stu-id="61854-103">Edit onboarding guides and templates in Dynamics 365 for Talent: Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="61854-104">Sukūrę supažindinimo vadovą arba šabloną „Microsoft Dynamics 365 for Talent: Onboard”, turite pridėti įžangą, veiklas, kontaktus ir išteklius.</span><span class="sxs-lookup"><span data-stu-id="61854-104">After you create an onboarding guide or template in Microsoft Dynamics 365 for Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="61854-105">Naudodami „Onboard” į supažindinimo vadovus galite įtraukti toliau nurodytą raiškųjį turinį.</span><span class="sxs-lookup"><span data-stu-id="61854-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="61854-106">YouTube vaizdo įrašai</span><span class="sxs-lookup"><span data-stu-id="61854-106">YouTube videos</span></span>
- <span data-ttu-id="61854-107">„Microsoft Sway” pateiktys</span><span class="sxs-lookup"><span data-stu-id="61854-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="61854-108">„Microsoft PowerApps” programėlės</span><span class="sxs-lookup"><span data-stu-id="61854-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="61854-109">Microsoft Stream vaizdo įrašai</span><span class="sxs-lookup"><span data-stu-id="61854-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="61854-110">„Microsoft Forms” formos</span><span class="sxs-lookup"><span data-stu-id="61854-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="61854-111">„Iframe”, kuriuose yra žiniatinklio turinio</span><span class="sxs-lookup"><span data-stu-id="61854-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="61854-112">Iš šablono importuotų įžangų ar veiklų redagavimas</span><span class="sxs-lookup"><span data-stu-id="61854-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="61854-113">Jei kuriate supažindinimo vadovą iš šablono arba importuojate veiklas iš vieno šablono į kitą, importuotose veiklose pastebėsite mygtuką **Užrakinti**.</span><span class="sxs-lookup"><span data-stu-id="61854-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="61854-114">Šios veiklos vadinamos *valdomosiomis veiklomis*.</span><span class="sxs-lookup"><span data-stu-id="61854-114">These are called *managed activities*.</span></span>

<span data-ttu-id="61854-115">[![Valdomosios veiklos](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="61854-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="61854-116">Pasirinkę valdomąją veiklą, veiklos viršuje galite matyti šaltinio šabloną.</span><span class="sxs-lookup"><span data-stu-id="61854-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="61854-117">[![Valdomosios veiklos šaltinis](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="61854-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="61854-118">Jei redaguojate veiklą šablone, „Onboard” atliks keitimus visuose šablonuose ir neišsiųstuose vadovuose, kurie sukurti pagal tą šabloną.</span><span class="sxs-lookup"><span data-stu-id="61854-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="61854-119">Jei pasirinksite neišsiųstą vadovą, kuris sukurtas remiantis jūsų redaguotu šablonu, o tada vadove pasirinksite skirtuką **Veiklos**, pamatysite pranešimą, kad jūsų vadovas buvo pakeistas.</span><span class="sxs-lookup"><span data-stu-id="61854-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="61854-120">Norėdami atmesti pranešimą, pasirinkite **Gerai.**</span><span class="sxs-lookup"><span data-stu-id="61854-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="61854-121">[![Pranešimas apie pakeitimą](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="61854-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="61854-122">Šalia atnaujintų veiklų pamatysite juodą tašką.</span><span class="sxs-lookup"><span data-stu-id="61854-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="61854-123">[![Pakeista veika](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="61854-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="61854-124">Negalite redaguoti valdomosios veiklos ne pagrindiniame šablone, nebent norite į dešiniąją veiklos dalį įtraukti priėmėją, terminą ar kitą informaciją.</span><span class="sxs-lookup"><span data-stu-id="61854-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="61854-125">Jei norite redaguoti valdomą veiklą arba jei nenorite, kad veikla gautų naujinimus iš šablono, iš kurio ji atsirado, pasirinkite tos veiklos mygtuką **Užrakinti**.</span><span class="sxs-lookup"><span data-stu-id="61854-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="61854-126">Mygtukas **Užrakinti** išnyks.</span><span class="sxs-lookup"><span data-stu-id="61854-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="61854-127">Veikla nebebus valdoma pradiniame šablone ir ji daugiau negaus to šablono naujinimų.</span><span class="sxs-lookup"><span data-stu-id="61854-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="61854-128">Jūsų atlikti veiklos naujinimai neturi įtakos pradiniam šablonui.</span><span class="sxs-lookup"><span data-stu-id="61854-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="61854-129">Jei naikinate veiklą iš vadovo ir paskelbiate to vadovo šablono keitimus, veikla vadove liks panaikinta.</span><span class="sxs-lookup"><span data-stu-id="61854-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="61854-130">Kontaktai ir ištekliai nėra valdomi naudojant šablonus.</span><span class="sxs-lookup"><span data-stu-id="61854-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="61854-131">Be to, skyriai nėra valdomi, todėl jei pridėsite arba redaguosite skyrių šablone, keitimai nebus skelbiami jokiuose vadovuose ar šablonuose, kurie naudoja tą šabloną.</span><span class="sxs-lookup"><span data-stu-id="61854-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="61854-132">Jei į šabloną įtraukiate naujų veiklų, jos yra paskelbiamos vadovuose ir šablonuose, pagrįstuose tuo šablonu, ir rodomos viršuje.</span><span class="sxs-lookup"><span data-stu-id="61854-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="61854-133">Veiklų iš kito šablono importavimas</span><span class="sxs-lookup"><span data-stu-id="61854-133">Import activities from another template</span></span>

<span data-ttu-id="61854-134">Veiklas į vadovą arba šabloną galite importuoti iš vieno ar daugiau šablonų.</span><span class="sxs-lookup"><span data-stu-id="61854-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="61854-135">Pasirinkite vadovą ar šabloną, kurį norite redaguoti.</span><span class="sxs-lookup"><span data-stu-id="61854-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="61854-136">Pažymėkite skirtuką **Veiklos**.</span><span class="sxs-lookup"><span data-stu-id="61854-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="61854-137">Dešinėje esančiame skyriuje pasirinkite skirtuką **Importavimas**.</span><span class="sxs-lookup"><span data-stu-id="61854-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="61854-138">[![Veiklų importavimas](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="61854-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="61854-139">Jei norite peržiūrėti užduotis naujame naršyklės skirtuke, bet kuriame šablone pasirinkite mygtuką **Atidaryti naujame skirtuke**.</span><span class="sxs-lookup"><span data-stu-id="61854-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="61854-140">[![Veiklų importavimas](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="61854-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="61854-141">Nuvilkite norimą šabloną į vietą, esančią vadovo šablone, kur norite, kad veiklos būtų rodomos.</span><span class="sxs-lookup"><span data-stu-id="61854-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="61854-142">Toliau redaguokite vadovą ar šabloną.</span><span class="sxs-lookup"><span data-stu-id="61854-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="61854-143">Importuotose veiklose bus mygtukas **Užrakinti**, kuris nurodo, kad tas veiklas valdo šablonas, iš kurio importavote.</span><span class="sxs-lookup"><span data-stu-id="61854-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="61854-144">Atlikus keitimus importuotame šablone, veiklos bus atnaujintos šablone, į kurį importavote.</span><span class="sxs-lookup"><span data-stu-id="61854-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="61854-145">Tačiau keitimai nebus automatiškai paskelbti vadovuose, sukurtuose iš šablono, į kurį buvo importuota.</span><span class="sxs-lookup"><span data-stu-id="61854-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="61854-146">Keitimų iš šablono į kitus šablonus arba vadovus skelbimas</span><span class="sxs-lookup"><span data-stu-id="61854-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="61854-147">Jei redaguojate šabloną, kuriame yra veiklų, naudojamų kituose šablonuose arba vadovuose, turite paskelbti keitimus, jei norite, kad jie ten būtų rodomi.</span><span class="sxs-lookup"><span data-stu-id="61854-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="61854-148">Jei nesate tikri, ar šablono veiklos yra naudojamos kituose šablonuose ar vadovuose, pasirinkite skirtuką **Naudojama**, kad peržiūrėtumėte, kur tos veiklos yra rodomos.</span><span class="sxs-lookup"><span data-stu-id="61854-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="61854-149">[![Vadovų ir šablonų, kuriuose veiklos naudojamos, rodinys](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="61854-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="61854-150">Toliau nurodyti veiksmai, kuriuos turite atlikti norėdami paskelbti keitimus.</span><span class="sxs-lookup"><span data-stu-id="61854-150">To push your changes:</span></span>

1. <span data-ttu-id="61854-151">Išsaugokite keitimus pasirinkdami mygtuką **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="61854-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="61854-152">Jei to nepadarysite, būsite paraginti įrašyti keitimus kitame veiksme.</span><span class="sxs-lookup"><span data-stu-id="61854-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="61854-153">Pasirinkite **Skelbti šiuos pakeitimus**.</span><span class="sxs-lookup"><span data-stu-id="61854-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="61854-154">Įžangos įtraukimas arba redagavimas</span><span class="sxs-lookup"><span data-stu-id="61854-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="61854-155">Skirtuke **Įžanga** įveskite vadovo pavadinimą ir pradinį pranešimą.</span><span class="sxs-lookup"><span data-stu-id="61854-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="61854-156">Norėdami naudoti pavyzdinį tekstą, pasirinkite **Naudoti šį pranešimą**.</span><span class="sxs-lookup"><span data-stu-id="61854-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="61854-157">[![Skirtukas „Įžanga” „Onboard” šablone](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="61854-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="61854-158">Jei norite redaguoti tekstą pagal savo poreikius arba pridėti vaizdų ar saitų, naudokite formatavimo mygtukus.</span><span class="sxs-lookup"><span data-stu-id="61854-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="61854-159">Pasirinkite **Įrašyti**, kad įrašytumėte savo darbą.</span><span class="sxs-lookup"><span data-stu-id="61854-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="61854-160">Veiklų įtraukimas ir redagavimas</span><span class="sxs-lookup"><span data-stu-id="61854-160">Add or edit activities</span></span>

1. <span data-ttu-id="61854-161">Skirtuke **Veiklos** nuvilkite elementus iš dešinės į redagavimo sritį.</span><span class="sxs-lookup"><span data-stu-id="61854-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="61854-162">Norėdami sutvarkyti savo vadovą, suskirstydami jį į skyrius, nuvilkite elementą **Naujas skyrius** į redagavimo sritį ir įveskite skyriaus pavadinimą bei pasirenkamą aprašą.</span><span class="sxs-lookup"><span data-stu-id="61854-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="61854-163">Naujo skyriaus įtraukimas į supažindinimo vadovą ar šabloną</span><span class="sxs-lookup"><span data-stu-id="61854-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="61854-164">Jei norite pridėti veiklų naujam darbuotojui atlikti, nuvilkite elementą **Nauja veikla** į redagavimo sritį ir įveskite veiklos pavadinimą bei aprašą.</span><span class="sxs-lookup"><span data-stu-id="61854-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="61854-165">Naujos veiklos įtraukimas į supažindinimo vadovą ar šabloną</span><span class="sxs-lookup"><span data-stu-id="61854-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="61854-166">Norėdami įtraukti raiškųjį turinį į supažindinimo vadovą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="61854-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="61854-167">Norėdami įtraukti „YouTube” vaizdo įrašą, nuvilkite elementą **YouTube** į redagavimo sritį, įveskite veiklos pavadinimą ir aprašą bei „YouTube” vaizdo įrašo URL.</span><span class="sxs-lookup"><span data-stu-id="61854-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="61854-168">Norėdami pridėti „Sway” pateiktį arba informacinį biuletenį, nuvilkite elementą **Sway** į redagavimo sritį, įveskite veiklos pavadinimą ir aprašą bei įveskite „Sway” pateikties arba informacinio biuletenio įdėtąjį URL.</span><span class="sxs-lookup"><span data-stu-id="61854-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="61854-169">Norėdami įtraukti „PowerApps” programėlę, nuvilkite elementą **PowerApps** į redagavimo sritį, įveskite veiklos pavadinimą ir aprašą, tada pasirinkite „PowerApps” programėlę arba įveskite „PowerApps” programėlės ID.</span><span class="sxs-lookup"><span data-stu-id="61854-169">To add a PowerApps app, drag the **PowerApps** item to the editing area, enter a name and description for the activity, and either select the PowerApps app or enter the PowerApps app ID.</span></span>
    - <span data-ttu-id="61854-170">Norėdami įtraukti „Microsoft Stream” vaizdo įrašą, nuvilkite elementą **Microsoft Stream** į redagavimo sritį, įveskite veiklos pavadinimą ir aprašą bei „Microsoft Stream” vaizdo įrašo URL.</span><span class="sxs-lookup"><span data-stu-id="61854-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="61854-171">Norėdami įtraukti „Microsoft Forms“ formą, nuvilkite elementą **Microsoft Forms** į redagavimo sritį, įveskite veiklos pavadinimą ir aprašą, įveskite „Microsoft Forms“ formos URL ir nurodykite ekrano srities dydį.</span><span class="sxs-lookup"><span data-stu-id="61854-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="61854-172">Norėdami įtraukti „Iframe”, kuriame yra žiniatinklio turinio, nuvilkite elementą **Web Content (iframe)** į redagavimo sritį, įveskite veiklos pavadinimą ir aprašą, įveskite žiniatinklio turinio URL ir nurodykite ekrano srities dydį.</span><span class="sxs-lookup"><span data-stu-id="61854-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="61854-173">Raiškiojo turinio įtraukimas į supažindinimo vadovą ar šabloną</span><span class="sxs-lookup"><span data-stu-id="61854-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="61854-174">Pasirinktinai: kiekvienos veiklos dešinėje srityje priskirkite veiklą konkrečiam asmeniui arba vaidmeniui, įtraukite terminą ir kontaktinį asmenį bei priskirkite kategorijos spalvą.</span><span class="sxs-lookup"><span data-stu-id="61854-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="61854-175">Kai priskiriate veiklą asmeniui ar vaidmeniui, kiekvienam asmeniui sukuriama užduotis.</span><span class="sxs-lookup"><span data-stu-id="61854-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="61854-176">Ši užduotis rodoma „Onboard” meniu **Užduotys**.</span><span class="sxs-lookup"><span data-stu-id="61854-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="61854-177">[![Veiklos priskyrimas supažindinimo vadove ar šablone](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="61854-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="61854-178">Pasirinkite **Įrašyti**, kad įrašytumėte savo darbą.</span><span class="sxs-lookup"><span data-stu-id="61854-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="61854-179">Norėdami panaikinti veiklą arba skyrių, pasirinkite mygtuką **Naikinti** (šiukšliadėžės simbolis), esantį viršutiniame dešiniajame veiklos arba skyriaus kampe.</span><span class="sxs-lookup"><span data-stu-id="61854-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="61854-180">Norėdami pertvarkyti veiklas ir skyrius, nuvilkite juos į naują vietą.</span><span class="sxs-lookup"><span data-stu-id="61854-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="61854-181">Kontaktų įtraukimas ar redagavimas</span><span class="sxs-lookup"><span data-stu-id="61854-181">Add or edit contacts</span></span>

<span data-ttu-id="61854-182">Galite įtraukti kontaktinius asmenis, kurie gali padėti jūsų naujam darbuotojui nuo pirmosios dienos.</span><span class="sxs-lookup"><span data-stu-id="61854-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="61854-183">Šie kontaktai gali būti darbdaviai, komandos nariai, priskirti pagalbos asmenys, mentoriai, administratoriai ir IT pagalbos darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="61854-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="61854-184">Skirtuke **Kontaktai** pasirinkite **Naujas kontaktas**.</span><span class="sxs-lookup"><span data-stu-id="61854-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="61854-185">Dialogo lange **Įtraukti komandos narį** įveskite kontaktinio asmens vardą arba el. pašto adresą, trumpą aprašą, paaiškinantį, kaip kontaktinis asmuo gali padėti naujam darbuotojui, ir pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="61854-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="61854-186">Kontaktų įtraukimas į supažindinimo vadovą ar šabloną</span><span class="sxs-lookup"><span data-stu-id="61854-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="61854-187">Kitu atveju, galite pasirinkti vieną ar daugiau kontaktų po elementu **Pasiūlymai**.</span><span class="sxs-lookup"><span data-stu-id="61854-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="61854-188">Pasirinkite **Įrašyti**, kad įrašytumėte savo darbą.</span><span class="sxs-lookup"><span data-stu-id="61854-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="61854-189">Norėdami panaikinti kontaktą, pasirinkite mygtuką **Naikinti** (šiukšliadėžės simbolis), esantį kontakto dešinėje.</span><span class="sxs-lookup"><span data-stu-id="61854-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="61854-190">Norėdami redaguoti kontaktą, pasirinkite mygtuką **Redaguoti** (pieštuko simbolis), esantį kontakto dešinėje.</span><span class="sxs-lookup"><span data-stu-id="61854-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="61854-191">Išteklių įtraukimas ar redagavimas</span><span class="sxs-lookup"><span data-stu-id="61854-191">Add or edit resources</span></span>

<span data-ttu-id="61854-192">Į supažindinimo vadovo skyrių **Ištekliai** galite įtraukti naudingų failų, schemų ir nuorodų.</span><span class="sxs-lookup"><span data-stu-id="61854-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="61854-193">Skirtuke **Ištekliai** pasirinkite **Nauji ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="61854-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="61854-194">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="61854-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="61854-195">Norėdami įtraukti failą, pasirinkite skirtuką **Failas** ir nuvilkite failą į paskirtą sritį.</span><span class="sxs-lookup"><span data-stu-id="61854-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="61854-196">(Taip pat galite spustelėti bet kurioje tos srities vietoje, kad rastumėte failą kompiuteryje, arba pasirinkti **Naršyti „OneDrive”**.) Įveskite failo pavadinimą ir pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="61854-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="61854-197">Norėdami įtraukti saitą, pasirinkite skirtuką **Saitas**, įveskite saito pavadinimą ir adresą, tada pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="61854-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="61854-198">Norėdami įtraukti schemą, pasirinkite skirtuką **Schema**, įveskite schemos pavadinimą ir adresą, tada pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="61854-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="61854-199">„Onboard” pateiks adreso, kurį nurodėte, schemą.</span><span class="sxs-lookup"><span data-stu-id="61854-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="61854-200">Naujų išteklių įtraukimas į supažindinimo vadovą ar šabloną</span><span class="sxs-lookup"><span data-stu-id="61854-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="61854-201">Pasirinkite **Įrašyti**, kad įrašytumėte savo darbą.</span><span class="sxs-lookup"><span data-stu-id="61854-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="61854-202">Norėdami panaikinti išteklius, pasirinkite mygtuką **Naikinti** (šiukšliadėžės simbolis), esantį išteklių dešinėje.</span><span class="sxs-lookup"><span data-stu-id="61854-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="61854-203">Norėdami redaguoti išteklius, pasirinkite mygtuką **Redaguoti** (pieštuko simbolis), esantį išteklių dešinėje.</span><span class="sxs-lookup"><span data-stu-id="61854-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="61854-204">Kiti veiksmai</span><span class="sxs-lookup"><span data-stu-id="61854-204">Next steps</span></span>

- [<span data-ttu-id="61854-205">Turinio bendrinimas su kitais bendraautoriais</span><span class="sxs-lookup"><span data-stu-id="61854-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="61854-206">Užduočių ir darbuotojų supažindinimo būsenos peržiūra</span><span class="sxs-lookup"><span data-stu-id="61854-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="61854-207">Samdos komandų kūrimas „Onboard”</span><span class="sxs-lookup"><span data-stu-id="61854-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="61854-208">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="61854-208">See also</span></span>

- [<span data-ttu-id="61854-209">Išbandykite arba įsigykite „Onboard” programėlę</span><span class="sxs-lookup"><span data-stu-id="61854-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="61854-210">Kas nauja</span><span class="sxs-lookup"><span data-stu-id="61854-210">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="61854-211">Leidimo pastabos</span><span class="sxs-lookup"><span data-stu-id="61854-211">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="61854-212">Palaikymo gavimas</span><span class="sxs-lookup"><span data-stu-id="61854-212">Get support</span></span>](./talent-support.md)
