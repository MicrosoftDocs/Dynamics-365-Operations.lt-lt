---
title: Pasirinktinių laukų kūrimas ir naudojimas
description: Šioje temoje parodoma, kaip vartotojo sąsajoje kurti pasirinktinius laukus ir programą pritaikyti savo verslui.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: f689bb3ec844459d1dd6e199804a30f3e0cb38bc
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112341"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="db8be-103">Pasirinktinių laukų kūrimas ir naudojimas</span><span class="sxs-lookup"><span data-stu-id="db8be-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db8be-104">Nors yra platus parengtų naudoti laukų rinkinys, skirtas valdyti įvairius verslo procesus, kartais įmonei sistemoje reikia sekti papildomą informaciją.</span><span class="sxs-lookup"><span data-stu-id="db8be-104">While there is an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="db8be-105">Nors programuotojai gali įtraukti šiuos laukus kaip plėtinius į programavimo įrankius, pasirinktinių laukų funkcija leidžia įtraukti laukus tiesiai iš vartotojo sąsajos, todėl galite pritaikyti programą prie savo įmonės per žiniatinklio naršyklę.</span><span class="sxs-lookup"><span data-stu-id="db8be-105">While programmers can be used to add those fields as extensions in the developer tools, the custom fields feature allows fields to be added directly from the user interface, thereby allowing you to tailor the application to fit your business using your web browser.</span></span>

<span data-ttu-id="db8be-106">Galimybė pridėti pasirinktinius laukus pasiekiama 13-ame ir vėlesniuose platformos naujinimuose.</span><span class="sxs-lookup"><span data-stu-id="db8be-106">The ability to add custom fields is available in platform update 13 and later.</span></span> <span data-ttu-id="db8be-107">Tik vartotojai, turintis specialias teises, turi prieigą prie šios funkcijos.</span><span class="sxs-lookup"><span data-stu-id="db8be-107">Only users with special permissions have access to this feature.</span></span>

<span data-ttu-id="db8be-108">Šiame vaizdo įraše rodoma, kaip lengva į puslapį įtraukti pasirinktinį lauką: [Pasirinktinių laukų įtraukimas](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span><span class="sxs-lookup"><span data-stu-id="db8be-108">This video shows how easy it is to add a custom field to a page: [Adding custom fields](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="db8be-109">Pasirinktinių laukų kūrimas</span><span class="sxs-lookup"><span data-stu-id="db8be-109">Creating custom fields</span></span>

<span data-ttu-id="db8be-110">Nustatę papildomą informaciją, kurią norėtumėte sekti programoje, atitinkamoje lentelėje galite sukurti pasirinktinį lauką ir jį rodyti puslapyje.</span><span class="sxs-lookup"><span data-stu-id="db8be-110">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="db8be-111">Tolesniais veiksmais aprašomas pasirinktinio lauko kūrimo ir įtraukimo į formą procesas.</span><span class="sxs-lookup"><span data-stu-id="db8be-111">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="db8be-112">Pereikite į formą, kurioje reikia naujo lauko.</span><span class="sxs-lookup"><span data-stu-id="db8be-112">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="db8be-113">Kadangi galutinis tikslas yra pasirinktinį lauką rodyti formoje, pasirinktinių laukų kūrimo įvesties taškas yra personalizavimo srityje.</span><span class="sxs-lookup"><span data-stu-id="db8be-113">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="db8be-114">Atidarykite personalizavimo įrankių juostą pasirinkdami **Parinktys**, tada – **Personalizuoti šią formą**.</span><span class="sxs-lookup"><span data-stu-id="db8be-114">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="db8be-115">Spustelėkite **Įterpti**, tada – **Laukas**.</span><span class="sxs-lookup"><span data-stu-id="db8be-115">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="db8be-116">Pasirinkite formos sritį, kurioje norite rodyti naująjį lauką.</span><span class="sxs-lookup"><span data-stu-id="db8be-116">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="db8be-117">Ją pasirinkus, dialogo lange **Įterpti laukų** bus rodomas esamų laukų, kuriuos galima įtraukti į pasirinktą formos sritį, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="db8be-117">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="db8be-118">Įsitikinkite, kad jus dominančio lauko sąraše dar nėra.</span><span class="sxs-lookup"><span data-stu-id="db8be-118">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="db8be-119">Jei jis yra, galite tiesiog pasirinkti tą lauką sąraše ir spustelėti **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="db8be-119">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="db8be-120">Spustelėkite virš sąrašo esantį mygtuką **Kurti naują lauką**, kad pradėtumėte pasirinktinio lauko kūrimo procesą.</span><span class="sxs-lookup"><span data-stu-id="db8be-120">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="db8be-121">Taip atidarysite dialogo langą **Kurti naują lauką**.</span><span class="sxs-lookup"><span data-stu-id="db8be-121">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="db8be-122">Jei mygtuko **Kurti naują lauką** nematote, neturite reikiamų teisių naudoti šią funkciją.</span><span class="sxs-lookup"><span data-stu-id="db8be-122">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="db8be-123">Dialogo lange **Kurti naują lauką** įveskite tolesnę informaciją.</span><span class="sxs-lookup"><span data-stu-id="db8be-123">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="db8be-124">Pasirinkite duomenų bazės lentelę, į kurią šis laukas turėtų būti įtrauktas.</span><span class="sxs-lookup"><span data-stu-id="db8be-124">Select the database table where this field should be added.</span></span> <span data-ttu-id="db8be-125">Atkreipkite dėmesį, kad išplečiamajame sąraše bus rodomos tik pasirinktinius laukus palaikančios lentelės.</span><span class="sxs-lookup"><span data-stu-id="db8be-125">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="db8be-126">Techninės informacijos apie palaikomas lenteles rasite žemiau esančiame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="db8be-126">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="db8be-127">Pasirinkite naujojo lauko duomenų tipą.</span><span class="sxs-lookup"><span data-stu-id="db8be-127">Select the data type for the new field.</span></span> <span data-ttu-id="db8be-128">Galimi duomenų tipai yra žymės langelis, data, data ir laikas, dešimtainis skaičius, skaičius, išrinkimo sąrašas ir tekstas.</span><span class="sxs-lookup"><span data-stu-id="db8be-128">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="db8be-129">Jei pasirenkate teksto duomenų tipą, taip pat galite nurodyti didžiausią teksto, kurį galima įvesti šiame lauke, ilgį.</span><span class="sxs-lookup"><span data-stu-id="db8be-129">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="db8be-130">Jei pasirenkate išrinkimo sąrašo duomenų tipą, taip pat galite pasirinkti tinkamas lauko reikšmes.</span><span class="sxs-lookup"><span data-stu-id="db8be-130">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="db8be-131">Nurodykite lauko pavadinimą, žymą ir žinyno tekstą.</span><span class="sxs-lookup"><span data-stu-id="db8be-131">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="db8be-132">Pavadinimas atitinka fizinį lauko pavadinimą duomenų bazėje, o žyma ir žinyno tekstas yra tekstas, naudojamas šį lauką pateikti vartotojo sąsajoje.</span><span class="sxs-lookup"><span data-stu-id="db8be-132">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="db8be-133">Jei šioje formoje reikia sukurti tik šį lauką, spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="db8be-133">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="db8be-134">Jei reikia sukurti papildomų laukų, spustelėkite **Įrašyti ir kurti naują** bei grįžkite prie 7 veiksmo.</span><span class="sxs-lookup"><span data-stu-id="db8be-134">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="db8be-135">Atkreipkite dėmesį, kad šiuo metu laukų limitas yra **20 pasirinktinių laukų vienoje lentelėje**.</span><span class="sxs-lookup"><span data-stu-id="db8be-135">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="db8be-136">Išėję iš dialogo lango **Kurti naują lauką**, grįšite į dialogo langą **Įterpti laukų**.</span><span class="sxs-lookup"><span data-stu-id="db8be-136">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="db8be-137">Visi ką tik įtraukti pasirinktiniai laukai laukų sąraše bus automatiškai pažymėti, kad juos reikia įterpti į formą.</span><span class="sxs-lookup"><span data-stu-id="db8be-137">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="db8be-138">Spustelėkite **Įterpti**, kad pažymėtus laukus įterptumėte į pasirinktą formos sritį.</span><span class="sxs-lookup"><span data-stu-id="db8be-138">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="db8be-139">**Pasirenkama.** Personalizavimo įrankių juostoje įjunkite režimą **Perkelti**, kad naujuosius laukus perkeltumėte į norimą pasirinktos srities vietą.</span><span class="sxs-lookup"><span data-stu-id="db8be-139">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="db8be-140">Norėdami gauti daugiau informacijos apie tai, kaip, naudojant įvairias personalizavimo galimybes, optimizuoti formą asmeniniam naudojimui, žr. [Vartotojo patirties personalizavimas](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="db8be-140">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="db8be-141">Pasirinktinių laukų bendrinimas su kitais vartotojais</span><span class="sxs-lookup"><span data-stu-id="db8be-141">Sharing custom fields with other users</span></span>

<span data-ttu-id="db8be-142">Sukūrę pasirinktinį lauką ir jį įtraukę į formą, galbūt norėsite šį atnaujintą puslapio rodinį su naujuoju lauku bendrinti su kitais sistemos vartotojais.</span><span class="sxs-lookup"><span data-stu-id="db8be-142">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="db8be-143">Tai galima atlikti toliau nurodytais dviem skirtingais būdais, naudojant produkto personalizavimo galimybes.</span><span class="sxs-lookup"><span data-stu-id="db8be-143">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="db8be-144">Rekomenduojamas kelias – kreiptis į sistemos administratorių, kuris personalizuotą elementą gali perduoti visiems vartotojams arba vartotojų subrinkiniui.</span><span class="sxs-lookup"><span data-stu-id="db8be-144">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="db8be-145">Norėdami gauti daugiau informacijos, žr. [Vartotojo patirties personalizavimas](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="db8be-145">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="db8be-146">Arba savo keitimus (vadinamus *personalizavimais*) galite eksportuoti, nusiųsti vienam ar keliems vartotojams, kad kiekvienas iš jų jūsų keitimus importuotų.</span><span class="sxs-lookup"><span data-stu-id="db8be-146">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="db8be-147">Eksportuoti ir importuoti personalizavimus galite pasirinkę personalizavimo įrankių juostos parinktį **Valdyti**.</span><span class="sxs-lookup"><span data-stu-id="db8be-147">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="db8be-148">Pasirinktinių laukų valdymas</span><span class="sxs-lookup"><span data-stu-id="db8be-148">Managing custom fields</span></span>

<span data-ttu-id="db8be-149">Visus pasirinktinius sistemos laukus galima valdyti modulio Sistemos administravimas puslapyje **Pasirinktiniai laukai**.</span><span class="sxs-lookup"><span data-stu-id="db8be-149">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="db8be-150">Šiame puslapyje vartotojai gali pasiekti daug galimybių, įskaitant tolesnes.</span><span class="sxs-lookup"><span data-stu-id="db8be-150">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="db8be-151">Visų pasirinktinių sistemos laukų sąrašo peržiūra.</span><span class="sxs-lookup"><span data-stu-id="db8be-151">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="db8be-152">Esamų pasirinktinių laukų riboto redagavimo funkcija.</span><span class="sxs-lookup"><span data-stu-id="db8be-152">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="db8be-153">Pasirinktinių laukų naikinimas.</span><span class="sxs-lookup"><span data-stu-id="db8be-153">Deleting custom fields.</span></span>
- <span data-ttu-id="db8be-154">Pasirinktinių laukų rodymas duomenų objektuose.</span><span class="sxs-lookup"><span data-stu-id="db8be-154">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="db8be-155">Pasirinktinių laukų žymų ir žinyno teksto vertimas.</span><span class="sxs-lookup"><span data-stu-id="db8be-155">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="db8be-156">Visų pasirinktinių laukų peržiūra</span><span class="sxs-lookup"><span data-stu-id="db8be-156">Viewing all custom fields</span></span>

<span data-ttu-id="db8be-157">Puslapyje **Pasirinktiniai laukai** galima matyti visus sistemoje nustatytus pasirinktinius laukus.</span><span class="sxs-lookup"><span data-stu-id="db8be-157">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="db8be-158">Tiesiog pasirinkite jus dominančią lentelę ir puslapis atsinaujins bei bus rodomas su ta lentele susietų pasirinktinių laukų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="db8be-158">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="db8be-159">Sąraše pasirinkę kokį nors pasirinktinį lauką, galėsite peržiūrėti visą informaciją apie jį.</span><span class="sxs-lookup"><span data-stu-id="db8be-159">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="db8be-160">Pasirinktinių laukų redagavimas</span><span class="sxs-lookup"><span data-stu-id="db8be-160">Editing custom fields</span></span>

<span data-ttu-id="db8be-161">Sukūrus pasirinktinį lauką, puslapyje **Pasirinktiniai laukai** galima modifikuoti tik tam tikrą pasirinktinio lauko informaciją.</span><span class="sxs-lookup"><span data-stu-id="db8be-161">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="db8be-162">*Galite* modifikuoti tolesnius atributus.</span><span class="sxs-lookup"><span data-stu-id="db8be-162">You *can* modify these attributes:</span></span>

- <span data-ttu-id="db8be-163">Etiketė</span><span class="sxs-lookup"><span data-stu-id="db8be-163">Label</span></span>
- <span data-ttu-id="db8be-164">Žinyno tekstas</span><span class="sxs-lookup"><span data-stu-id="db8be-164">Help text</span></span>
- <span data-ttu-id="db8be-165">Ilgis, teksto laukų</span><span class="sxs-lookup"><span data-stu-id="db8be-165">Length, for Text fields</span></span>

<span data-ttu-id="db8be-166">*Negalite* redaguoti tolesnių atributų.</span><span class="sxs-lookup"><span data-stu-id="db8be-166">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="db8be-167">Lauko pavadinimas</span><span class="sxs-lookup"><span data-stu-id="db8be-167">Field name</span></span>
- <span data-ttu-id="db8be-168">Duomenų tipas</span><span class="sxs-lookup"><span data-stu-id="db8be-168">Data type</span></span>

<span data-ttu-id="db8be-169">Be to, jei laukų tipas yra išrinkimo sąrašas, galima pertvarkyti tinkamas pasirinktinio lauko reikšmes ir įtraukti naujų reikšmių; tačiau esamų išrinkimo sąrašo lauko reikšmių pašalinti negalima.</span><span class="sxs-lookup"><span data-stu-id="db8be-169">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="db8be-170">Baigę redaguoti konkrečios lentelės laukus, nepamirškite spustelėti **Taikyti keitimus**, kad keitimai būtų įrašyti.</span><span class="sxs-lookup"><span data-stu-id="db8be-170">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="db8be-171">Pasirinktinių laukų rodymas duomenų objektuose</span><span class="sxs-lookup"><span data-stu-id="db8be-171">Exposing custom fields on data entities</span></span>

<span data-ttu-id="db8be-172">Taip pat gali būti svarbu leisti, kad pasirinktiniai laukai būtų matomi duomenų objektuose.</span><span class="sxs-lookup"><span data-stu-id="db8be-172">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="db8be-173">Duomenų objektai yra naudojami funkcijoje [„Office“ integravimo apžvalga](../../dev-itpro/office-integration/office-integration.md), taip pat duomenų importavimo / eksportavimo scenarijuose.</span><span class="sxs-lookup"><span data-stu-id="db8be-173">Data entities are utilized in the [Office integration overview](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="db8be-174">Norėdami pasirinktinį lauką rodyti duomenų objekte, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="db8be-174">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="db8be-175">Formoje **Pasirinktiniai laukai** pasirinkite pasirinktinį lauką.</span><span class="sxs-lookup"><span data-stu-id="db8be-175">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="db8be-176">Išplėskite skyrių **Objektai**, kad galėtumėte peržiūrėti aktualius objektus.</span><span class="sxs-lookup"><span data-stu-id="db8be-176">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="db8be-177">Spustelėkite mygtuką **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="db8be-177">Click the **Edit** button.</span></span>
4. <span data-ttu-id="db8be-178">Modifikuokite lauką **Įjungta**, kad jį reikėtų pasirinkti prie kiekvieno objekto, kuriame turėtų būti rodomas šis laukas.</span><span class="sxs-lookup"><span data-stu-id="db8be-178">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="db8be-179">Spustelėkite **Taikyti keitimus**, kad įrašytumėte pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="db8be-179">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="db8be-180">Leidimas pasirinktinius laukus rodyti kitomis kalbomis</span><span class="sxs-lookup"><span data-stu-id="db8be-180">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="db8be-181">Kadangi pasirinktinius laukus vartotojams gali reikėti pasiekti įvairiomis kalbomis, puslapyje **Pasirinktiniai laukai** pateikiamas mechanizmas, leidžiantis pasirinktinio lauko žymos ir žinyno tekstą išversti į kitas kalbas.</span><span class="sxs-lookup"><span data-stu-id="db8be-181">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="db8be-182">Tolesniais veiksmais aprašomas pasirinktinių laukų vertimo į kitas kalbas procesas.</span><span class="sxs-lookup"><span data-stu-id="db8be-182">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="db8be-183">Puslapyje **Pasirinktiniai laukai** pasirinkite pasirinktinį lauką.</span><span class="sxs-lookup"><span data-stu-id="db8be-183">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="db8be-184">Veiksmų srityje pasirinkite mygtuką **Vertimai**.</span><span class="sxs-lookup"><span data-stu-id="db8be-184">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="db8be-185">Taip atidarysite išplečiamąjį meniu su esamais šio lauko vertimais.</span><span class="sxs-lookup"><span data-stu-id="db8be-185">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="db8be-186">Išplečiamajame meniu **Kalba** rodoma, į kurias kalbas tekstas jau išverstas.</span><span class="sxs-lookup"><span data-stu-id="db8be-186">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="db8be-187">Jei norite redaguoti esamą vertimą, meniu pasirinkite norimą kalbą ir modifikuokite žymos bei žinyno teksto reikšmes.</span><span class="sxs-lookup"><span data-stu-id="db8be-187">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="db8be-188">Kitu atveju spustelėkite mygtuką **Įtraukti kalbą**, meniu pasirinkite norimą kalbą ir nurodykite išverstas žymos bei žinyno teksto reikšmes.</span><span class="sxs-lookup"><span data-stu-id="db8be-188">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="db8be-189">Baigę spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="db8be-189">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="db8be-190">Pasirinktinių laukų naikinimas</span><span class="sxs-lookup"><span data-stu-id="db8be-190">Deleting custom fields</span></span>

<span data-ttu-id="db8be-191">Retais atvejais galite nuspręsti, kad koks nors pasirinktinis laukas yra nebereikalingas.</span><span class="sxs-lookup"><span data-stu-id="db8be-191">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="db8be-192">Tokiu atveju sistemos administratorius gali pasirinkti tokį lauką panaikinti puslapyje **Pasirinktiniai laukai**.</span><span class="sxs-lookup"><span data-stu-id="db8be-192">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="db8be-193">Norėdami tai padaryti, įsitikinkite, kad pasirinktas teisingas laukas, spustelėkite **Panaikinti**, tada – **Taip**, kad patvirtintumėte naikinimą, ir galiausiai spustelėkite **Taikyti keitimus**.</span><span class="sxs-lookup"><span data-stu-id="db8be-193">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="db8be-194">Šio veiksmo anuliuoti negalima ir juo duomenų bazėje bus visam laikui panaikinti su lauku susieti duomenys.</span><span class="sxs-lookup"><span data-stu-id="db8be-194">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="db8be-195">Priedas</span><span class="sxs-lookup"><span data-stu-id="db8be-195">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="db8be-196">Kas gali kurti pasirinktinius laukus?</span><span class="sxs-lookup"><span data-stu-id="db8be-196">Who can create custom fields?</span></span>

<span data-ttu-id="db8be-197">Siekiant apsaugoti sistemą, pagal numatytuosius nustatymus kurti pasirinktinius laukus gali tik sistemos administratoriai.</span><span class="sxs-lookup"><span data-stu-id="db8be-197">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="db8be-198">Tačiau, jei organizacija nusprendžia, kad to reikia, sistemos administratorius patyrusiems vartotojams gali suteikti teises kurti pasirinktinius laukus, naudodamas saugos vaidmenį **Patyręs vykdymo aplinkos tinkinimo vartotojas**.</span><span class="sxs-lookup"><span data-stu-id="db8be-198">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="db8be-199">Šio saugos vaidmens neturintys vartotojai pasirinktinių laukų kurti negalės, tačiau vis tiek galės matyti ir interaktyviai naudoti kitų sistemos vartotojų įtrauktus pasirinktinius laukus.</span><span class="sxs-lookup"><span data-stu-id="db8be-199">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="db8be-200">Kokios lentelės palaiko pasirinktinius laukus?</span><span class="sxs-lookup"><span data-stu-id="db8be-200">What tables support custom fields?</span></span>

<span data-ttu-id="db8be-201">Dėl našumo ir techninių priežasčių pasirinktinių laukų galima įtraukti tik į tas lenteles, kurios atitinka tolesnes sąlygas.</span><span class="sxs-lookup"><span data-stu-id="db8be-201">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="db8be-202">Lentelė turi būti pažymėta priklausanti vienai iš tolesnių grupių.</span><span class="sxs-lookup"><span data-stu-id="db8be-202">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="db8be-203">Grupuoti</span><span class="sxs-lookup"><span data-stu-id="db8be-203">Group</span></span>
    - <span data-ttu-id="db8be-204">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="db8be-204">WorksheetHeader</span></span>
    - <span data-ttu-id="db8be-205">Pagrindinis</span><span class="sxs-lookup"><span data-stu-id="db8be-205">Main</span></span>
    - <span data-ttu-id="db8be-206">Įvairios</span><span class="sxs-lookup"><span data-stu-id="db8be-206">Miscellaneous</span></span>
    - <span data-ttu-id="db8be-207">Parametras</span><span class="sxs-lookup"><span data-stu-id="db8be-207">Parameter</span></span>
    - <span data-ttu-id="db8be-208">Nuoroda</span><span class="sxs-lookup"><span data-stu-id="db8be-208">Reference</span></span>
    - <span data-ttu-id="db8be-209">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="db8be-209">TransactionHeader</span></span>

- <span data-ttu-id="db8be-210">Kitos lentelės naudojant šią lentelę išplėsti negalima.</span><span class="sxs-lookup"><span data-stu-id="db8be-210">The table cannot extend another table.</span></span>
- <span data-ttu-id="db8be-211">Lentelės negalima pažymėti sistemos lentele.</span><span class="sxs-lookup"><span data-stu-id="db8be-211">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="db8be-212">Lentelė negali būti laikina.</span><span class="sxs-lookup"><span data-stu-id="db8be-212">The table cannot be a temporary table.</span></span>

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a><span data-ttu-id="db8be-213">Ar galiu nurodyti pasirinktinius laukus iš programavimo įrankių?</span><span class="sxs-lookup"><span data-stu-id="db8be-213">Can I reference custom fields from the developer tools?</span></span>  

<span data-ttu-id="db8be-214">Pasirinktinius laukus galima valdyti tik vartotojo sąsajoje ir jų negalima nurodyti pagal kodą.</span><span class="sxs-lookup"><span data-stu-id="db8be-214">Custom fields can only be managed through the user interface and cannot be referenced by code.</span></span> 
