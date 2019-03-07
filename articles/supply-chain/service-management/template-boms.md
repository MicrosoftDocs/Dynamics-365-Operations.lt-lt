---
title: Šabloninės KS
description: Komplektavimo specifikacijos (KS) šablone pateikiamas standartizuotas komponentų sąrašas, skirtas aptarnavimo objektams, kurie aptarnaujami reguliariai.
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9c61ecd79f38301f46e3c21a33ec2801f33d19f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "341309"
---
# <a name="template-boms"></a><span data-ttu-id="e05f0-103">Šabloninės KS</span><span class="sxs-lookup"><span data-stu-id="e05f0-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e05f0-104">Komplektavimo specifikacijos (KS) šablone jums pateikiamas standartizuotas komponentų sąrašas, skirtas aptarnavimo objektams, kurie aptarnaujami reguliariai.</span><span class="sxs-lookup"><span data-stu-id="e05f0-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="e05f0-105">Komponentai, išvardyti šabloninėse KS, reiškia individualius aptarnavimo objekto papildomus komponentus.</span><span class="sxs-lookup"><span data-stu-id="e05f0-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="e05f0-106">Aptarnavimo objektui pritaikę šabloninę KS, galite įrašyti papildomus aptarnavimo komponentus, pakeistus aptarnavimo objekte.</span><span class="sxs-lookup"><span data-stu-id="e05f0-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="e05f0-107">Norėdami taikyti šablono KS aptarnavimo sutarčiai ar aptarnavimo užsakymui, pridėkite jį prie aptarnavimo objekto ryšio.</span><span class="sxs-lookup"><span data-stu-id="e05f0-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e05f0-108">Aptarnavimo objektui galite pritaikyti tik vieną šabloninę KS.</span><span class="sxs-lookup"><span data-stu-id="e05f0-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="e05f0-109">Šabloninės KS kūrimas</span><span class="sxs-lookup"><span data-stu-id="e05f0-109">Create a template BOM</span></span>

<span data-ttu-id="e05f0-110">Toliau pateiktoje lentelėje pateikiama informacija apie įvairius metodus, kuriuos galite naudoti šabloninei KS sukurti.</span><span class="sxs-lookup"><span data-stu-id="e05f0-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e05f0-111">Metodas</span><span class="sxs-lookup"><span data-stu-id="e05f0-111">Method</span></span></p></th>
<th><p><span data-ttu-id="e05f0-112">aprašymas</span><span class="sxs-lookup"><span data-stu-id="e05f0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e05f0-113">Gamyba</span><span class="sxs-lookup"><span data-stu-id="e05f0-113">Production</span></span></p></td>
<td><p><span data-ttu-id="e05f0-114">Šabloninė KS yra paremta gamybos užsakymu.</span><span class="sxs-lookup"><span data-stu-id="e05f0-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="e05f0-115">Ši parinktis taikoma tik tada, kai dirbate gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="e05f0-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="e05f0-116">Privalumas ta, kad turite dabartinį išsamų prekę sudarančių komponentų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="e05f0-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05f0-117">BOM prekė</span><span class="sxs-lookup"><span data-stu-id="e05f0-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="e05f0-118">Šabloninė KS yra paremta prekės KS.</span><span class="sxs-lookup"><span data-stu-id="e05f0-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="e05f0-119">Prekės KS, kitaip nei gamybos KS, yra statinis prekę sudarančių komponentų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="e05f0-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e05f0-120">Esamas šablonas</span><span class="sxs-lookup"><span data-stu-id="e05f0-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="e05f0-121">Šablonas paremtas esama šablonine KS.</span><span class="sxs-lookup"><span data-stu-id="e05f0-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e05f0-122">Neautomatinis</span><span class="sxs-lookup"><span data-stu-id="e05f0-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="e05f0-123">Jei tiksliai žinote, kokios aptarnavimo objekto dalys įprastai keičiamos, galite sukurti neautomatinį šabloninės KS kūrimą.</span><span class="sxs-lookup"><span data-stu-id="e05f0-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="e05f0-124">Šis būdas padeda užtikrinti, kad į šabloną įtraukti komponentai atitiks konkrečius jūsų darbo vietos reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="e05f0-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="e05f0-125">Šabloninės KS taikymas aptarnavimo sutarčiai arba aptarnavimo užsakymui</span><span class="sxs-lookup"><span data-stu-id="e05f0-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="e05f0-126">Šabloninę KS galite taikyti aptarnavimo sutarčiai, aptarnavimo užsakymui arba abiems.</span><span class="sxs-lookup"><span data-stu-id="e05f0-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="e05f0-127">Aptarnavimo sutartis paprastai aprėpia ilgalaikį ryšį su klientu.</span><span class="sxs-lookup"><span data-stu-id="e05f0-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="e05f0-128">Pakeitimų retrospektyvos, įrašytos į aptarnavimo KS, duomenys gali būti naudingi aptarnavimo sutarčiai.</span><span class="sxs-lookup"><span data-stu-id="e05f0-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="e05f0-129">Šabloninę KS taip pat galite taikyti aptarnavimo užsakymui, kad atlikto aptarnavimo retrospektyvą įrašytumėte į aptarnavimo objektą.</span><span class="sxs-lookup"><span data-stu-id="e05f0-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="e05f0-130">Aptarnavimo KS retrospektyvos kopijavimas</span><span class="sxs-lookup"><span data-stu-id="e05f0-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="e05f0-131">Aptarnavimo KS eilutės retrospektyvą galite nukopijuoti iš vienos aptarnavimo sutarties į kitą.</span><span class="sxs-lookup"><span data-stu-id="e05f0-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="e05f0-132">Kopijuodami aptarnavimo retrospektyvą iš vienos aptarnavimo sutarties į kitą, galite išsaugoti prekės pakeitimų įrašą.</span><span class="sxs-lookup"><span data-stu-id="e05f0-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="e05f0-133">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="e05f0-133">**Example**</span></span>

<span data-ttu-id="e05f0-134">Sudarėte kliento automobilio trijų metų aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="e05f0-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="e05f0-135">Per šį laikotarpį klientas pripranta prie gero įmonės teikiamo aptarnavimo.</span><span class="sxs-lookup"><span data-stu-id="e05f0-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="e05f0-136">Todėl pasibaigus sutarties galiojimo laikui, klientas nori nustatyti naują.</span><span class="sxs-lookup"><span data-stu-id="e05f0-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="e05f0-137">Dabar galite derėtis dėl palankesnės įmonei sutarties.</span><span class="sxs-lookup"><span data-stu-id="e05f0-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="e05f0-138">Pakeistų komponentų įrašas gali būti naudingas ateityje, todėl galite nusikopijuoti aptarnavimo KS retrospektyvą į naują sutartį.</span><span class="sxs-lookup"><span data-stu-id="e05f0-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="e05f0-139">Šabloninės KS modifikavimas</span><span class="sxs-lookup"><span data-stu-id="e05f0-139">Modify the template BOM</span></span>

<span data-ttu-id="e05f0-140">Jei šabloninė KS nepridėta prie aptarnavimo objekto, galite modifikuoti arba panaikinti objekte esančias eilutes.</span><span class="sxs-lookup"><span data-stu-id="e05f0-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="e05f0-141">Pridėję šablono KS prie aptarnavimo objekto galite modifikuoti tik vietinę KS versiją.</span><span class="sxs-lookup"><span data-stu-id="e05f0-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="e05f0-142">Jei norite dubliuoti vietinės šablono KS versijos nustatymą, galite kurti naują šablono KS pagal vietinę versiją.</span><span class="sxs-lookup"><span data-stu-id="e05f0-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="e05f0-143">Daugiau informacijos žr. [Aptarnavimo KS modifikavimas](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="e05f0-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="e05f0-144">Jei keisite KS esančią prekę, pakeitimą galėsite užregistruoti KS eilutėje arba KS konstruktoriuje.</span><span class="sxs-lookup"><span data-stu-id="e05f0-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="e05f0-145">Pasirinktinai galite sukurti pakeitimo objekto aptarnavimo užsakymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="e05f0-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="e05f0-146">Jei sukursite aptarnavimo užsakymo eilutę, galėsite išrašyti pakeitimo prekės SF.</span><span class="sxs-lookup"><span data-stu-id="e05f0-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="e05f0-147">Jei nesukursite pakeitimo aptarnavimo užsakymo eilutės, pakeitimo registracija bus išsaugota tarp jūsų įrašų aptarnavimo objekto retrospektyvai sekti.</span><span class="sxs-lookup"><span data-stu-id="e05f0-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="e05f0-148">Informacijos pateikimo KS eilutėje keitimas</span><span class="sxs-lookup"><span data-stu-id="e05f0-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="e05f0-149">Galite pakeisti viso šablono ir KS eilutėje rodomos aptarnavimo KS informacijos pateikimo būdą.</span><span class="sxs-lookup"><span data-stu-id="e05f0-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="e05f0-150">Pakeitimai bus taikomi visoms šabloninėms KS ir aptarnavimo KS.</span><span class="sxs-lookup"><span data-stu-id="e05f0-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="e05f0-151">Tai taikoma ir prie aptarnavimo objektų pridėtoms KS.</span><span class="sxs-lookup"><span data-stu-id="e05f0-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="e05f0-152">Šabloninių KS numeracijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="e05f0-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="e05f0-153">Norėdami naudoti šablonines KS, turite nustatyti dvi skaičių numeracijas.</span><span class="sxs-lookup"><span data-stu-id="e05f0-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="e05f0-154">Vieną numeraciją nustatykite šabloninei KS, o kitą – šabloninės KS retrospektyvos eilutės numeriui.</span><span class="sxs-lookup"><span data-stu-id="e05f0-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e05f0-155">Numeracijos naudojamos norint priskirti identifikatorius tiems įrašams, kuriems jų reikia.</span><span class="sxs-lookup"><span data-stu-id="e05f0-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="e05f0-156">Prieš priskirdami numeraciją šabloninei KS arba šabloninės KS retrospektyvos eilutės numeriui, turite nustatyti numeracijos kodus.</span><span class="sxs-lookup"><span data-stu-id="e05f0-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="e05f0-157">Nustatyti numeraciją</span><span class="sxs-lookup"><span data-stu-id="e05f0-157">Set up number sequences</span></span>

1.  <span data-ttu-id="e05f0-158">Sąrašo puslapyje **Numeracijos** sukurkite šabloninių KS ir KS retrospektyvos eilutės numerio numeracijas.</span><span class="sxs-lookup"><span data-stu-id="e05f0-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="e05f0-159">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e05f0-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="e05f0-160">Spustelėkite **Numeracijos**, tada numeracijos nuorodoms, kurias sukūrėte formoje **Numeracijos**, parinkite numeracijos kodą.</span><span class="sxs-lookup"><span data-stu-id="e05f0-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="e05f0-161">Uždarę formą įrašysite savo pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="e05f0-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e05f0-162">KS retrospektyvos eilutės numeris bus reikalingas sistemai, kad KS retrospektyvos operacijas būtų galima susieti su aptarnavimo sutartimi ar aptarnavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="e05f0-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="e05f0-163">Numeris nebus rodomas vartotojo sąsajoje.</span><span class="sxs-lookup"><span data-stu-id="e05f0-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="e05f0-164">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="e05f0-164">See also</span></span>

[<span data-ttu-id="e05f0-165">Šabloninės KS kūrimas</span><span class="sxs-lookup"><span data-stu-id="e05f0-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="e05f0-166">Objekto ryšių šabloninių KS valdymas</span><span class="sxs-lookup"><span data-stu-id="e05f0-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="e05f0-167">Aptarnavimo KS modifikavimas</span><span class="sxs-lookup"><span data-stu-id="e05f0-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 


