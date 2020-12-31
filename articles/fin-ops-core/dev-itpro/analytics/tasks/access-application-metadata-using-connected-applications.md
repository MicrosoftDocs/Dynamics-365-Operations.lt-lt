---
title: Prieiga prie programos metaduomenų naudojant prijungtas programas
description: Šioje temoje pateikti veiksmai paaiškina, kaip „Regulatory configuration service“ (RCS) vartotojas gali kurti naują elektroninės ataskaitos (ER) modelio susiejimą naudodamas „Finance and Operations“ metaduomenis.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 751ac21dc056373e1cd89a5149bf38789134e0cc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682146"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="0ec58-103">Prieiga prie programos metaduomenų naudojant prijungtas programas</span><span class="sxs-lookup"><span data-stu-id="0ec58-103">Access application metadata by using connected applications</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0ec58-104">Toliau nurodyti veiksmai paaiškina, kaip „Regulatory configuration service“ (RCS) vartotojas, turintis sistemos administratoriaus arba elektroninės ataskaitos kūrėjo vaidmenį, gali kurti naują elektroninės ataskaitos (ER) modelio susiejimą naudodamas „Finance and Operations“ metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="0ec58-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="0ec58-105">Programos metaduomenys bus pasiekiami tinkle naudojant programą, prijungtą prie RCS.</span><span class="sxs-lookup"><span data-stu-id="0ec58-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="0ec58-106">Bus sukonfigūruotas ER modelio susiejimo pavyzdys, siekiant pasiekti užsienio prekybos operacijas.</span><span class="sxs-lookup"><span data-stu-id="0ec58-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="0ec58-107">Norint atlikti šiuos veiksmus, pirmiausia RCS reikia atlikti veiksmus, nurodytus temoje [Konfigūracijų teikėjų kūrimas ir jų pažymėjimas kaip aktyviais](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="0ec58-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="0ec58-108">Jei neatlikote veiksmų, nurodytų temoje [Prieiga prie programos metaduomenų naudojant ER konfigūraciją](access-application-metadata-er-configuration.md), eikite į [Elektroninių ataskaitų pavyzdžių puslapis](https://go.microsoft.com/fwlink/?linkid=862266), atsisiųskite ir įrašykite šias ER konfigūracijas: Užsienio prekybos metaduomenys.xml; Užsienio prekybos modelis.xml; Užsienio prekybos susiejimas.xml, tada atlikite procedūros veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0ec58-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0ec58-109">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="0ec58-109">Prerequisites</span></span>
1. <span data-ttu-id="0ec58-110">Eikite į **Visos darbo sritys** > **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="0ec58-111">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="0ec58-112">Jei nematote šio konfigūracijos teikėjo, atlikite procedūros [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md) veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0ec58-112">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="0ec58-113">Reikiamų ER konfigūracijų gavimas</span><span class="sxs-lookup"><span data-stu-id="0ec58-113">Get required ER configurations</span></span>
1. <span data-ttu-id="0ec58-114">Spustelėkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="0ec58-115">Jei jau atlikote [Prieiga prie programos metaduomenų naudojant ER konfigūraciją](access-application-metadata-er-configuration.md) procedūros veiksmus, jūs jau turite visas reikiamas ER konfigūracijas (užsienio prekybos metaduomenų, modelio ir susiejimo konfigūracijas) dabartiniame RCS egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="0ec58-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="0ec58-116">Galite praleisti visus kitus šios antrinės užduoties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0ec58-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="0ec58-117">Spustelėkite **Keitimas**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="0ec58-118">Spustelėkite **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="0ec58-119">Spustelėkite **Naršyti** ir pasirinkite failą **Užsienio prekybos metaduomenys.xml**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="0ec58-120">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-120">Click **OK**.</span></span> 
7. <span data-ttu-id="0ec58-121">Spustelėkite **Keitimas**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="0ec58-122">Spustelėkite **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="0ec58-123">Spustelėkite **Naršyti** ir pasirinkite failą **Užsienio prekybos modelis.xml**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="0ec58-124">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-124">Click **OK**.</span></span> 
11. <span data-ttu-id="0ec58-125">Spustelėkite **Keitimas**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="0ec58-126">Spustelėkite **Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="0ec58-127">Spustelėkite **Naršyti** ir pasirinkite failą **Užsienio prekybos susiejimas.xml**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="0ec58-128">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="0ec58-129">Prijungtos programos užregistravimas</span><span class="sxs-lookup"><span data-stu-id="0ec58-129">Register a connected application</span></span>
1. <span data-ttu-id="0ec58-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0ec58-130">Close the page.</span></span> 
2. <span data-ttu-id="0ec58-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0ec58-131">Close the page.</span></span> 
3. <span data-ttu-id="0ec58-132">Eikite į **Visos darbo sritys** > **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="0ec58-133">Spustelėkite **Prijungtos programos**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="0ec58-134">Įsitikinkite, kad sukonfigūruota programa yra „Azure“ ir pasiekiama esamam RCS vartotojui.</span><span class="sxs-lookup"><span data-stu-id="0ec58-134">Make sure that the configured application is Azure based and accessible for the current RCS user.</span></span> <span data-ttu-id="0ec58-135">Be to, esamas RCS vartotojas turi turėti prieigą prie pasirinktos programos ir turi būti užregistruotas kaip šios programos vartotojas, kuriam priskirtas vaidmuo suteikia teises pasiekti programos metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="0ec58-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving them privileges to access application's metadata.</span></span> 
6. <span data-ttu-id="0ec58-136">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-136">Click **New**.</span></span> 
7. <span data-ttu-id="0ec58-137">Lauke **Pavadinimas** įveskite MyConnectedApp.</span><span class="sxs-lookup"><span data-stu-id="0ec58-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="0ec58-138">Lauke **Programa** įveskite https:// mycompany.operations.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="0ec58-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="0ec58-139">Lauke **Nuomotojas** įveskite mycompany.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="0ec58-139">In the **Tenant** field, type 'mycompany.onmicrosoft.com'.</span></span> 
10. <span data-ttu-id="0ec58-140">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-140">Click **Save**.</span></span> 
11. <span data-ttu-id="0ec58-141">Kai tikrinate ryšį su sukonfigūruota programa, puslapyje **Prisijungti prie nuotolinės programos** spustelėkite saitą **Spustelėkite čia, kad prisijungtumėte prie pasirinktos nuotolinės programos**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="0ec58-142">Spustelėkite **Tikrinti ryšį**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="0ec58-143">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-143">Click **Close**.</span></span> 
14. <span data-ttu-id="0ec58-144">Kai ryšio patikra atliekama sėkmingai, esamame tinklelyje atnaujinama sukonfigūruotos programos versijos ir nuomotojo informacija.</span><span class="sxs-lookup"><span data-stu-id="0ec58-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="0ec58-145">Esamo modelio susiejimo konfigūracijos peržiūra</span><span class="sxs-lookup"><span data-stu-id="0ec58-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="0ec58-146">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0ec58-146">Close the page.</span></span> 
2. <span data-ttu-id="0ec58-147">Spustelėkite **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="0ec58-148">Medyje išplėskite **Užsienio prekybos modelis**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="0ec58-149">Medyje pasirinkite **Užsienio prekybos modelis\Užsienio prekybos susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="0ec58-150">Išplėskite sekciją **Būtinieji komponentai**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0ec58-151">Šiuo metu šis susiejimas nurodo metaduomenų konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="0ec58-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="0ec58-152">Kuriant šį modelio susiejimą bus siūlomi šios konfigūracijos programos metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="0ec58-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="0ec58-153">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="0ec58-154">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="0ec58-155">Medyje pasirinkite **Dynamics 365 for Operations\Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="0ec58-156">Spustelėkite **Įtraukti šakninį elementą**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="0ec58-157">Lauke **Lentelė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0ec58-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0ec58-158">Šiuo metu šis susiejimas nurodo metaduomenų konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="0ec58-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="0ec58-159">Kuriant šį modelio susiejimą bus siūlomi šios konfigūracijos programos metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="0ec58-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="0ec58-160">Spustelėkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="0ec58-161">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0ec58-161">Close the page.</span></span> 
13. <span data-ttu-id="0ec58-162">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0ec58-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="0ec58-163">Prijungtos programos priskyrimas modelio susiejimui</span><span class="sxs-lookup"><span data-stu-id="0ec58-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="0ec58-164">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="0ec58-165">Pasirinkite programą **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0ec58-166">Šiuo metu šis susiejimas nurodo pasirinktos prijungtos programos metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="0ec58-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="0ec58-167">Kai tas pats susiejimas tuo pačiu metu nurodo metaduomenų konfigūraciją ir prijungtą programą, bus naudojami prijungtos programos metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="0ec58-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="0ec58-168">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="0ec58-169">Spustelėkite **Konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="0ec58-170">Medyje pasirinkite **Dynamics 365 for Operations\Lentelės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="0ec58-171">Spustelėkite **Įtraukti šakninį elementą**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="0ec58-172">Lauke **Lentelė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0ec58-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0ec58-173">Dabar siūlomos daugiau nei dvi programos lentelės, nes šis susiejimas naudoja visus prijungtos programos, kuri buvo priskirta, metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="0ec58-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="0ec58-174">Spustelėkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="0ec58-175">Spustelėkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="0ec58-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="0ec58-176">Sėkmingai susiejome duomenų modelio elementus su duomenų šaltinių elementais, kurie aprašomi naudojant prijungtos programos, priskirtos šiam susiejimui, metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="0ec58-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="0ec58-177">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0ec58-177">Close the page.</span></span> 
11. <span data-ttu-id="0ec58-178">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0ec58-178">Close the page.</span></span> 

<span data-ttu-id="0ec58-179">Jei reikia įvertinti šio modelio susiejimą naudojant skirtingos programos versijos metaduomenis, užregistruokite kitą prijungtą programą, priskirkite ją šiam modelio susiejimui ir patikrinkite ją naudodami naujus metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="0ec58-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>
