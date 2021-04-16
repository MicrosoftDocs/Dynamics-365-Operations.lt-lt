---
title: Egipto išskaitomo mokesčio deklaracija
description: Šioje temoje paaiškinama, kaip sukonfigūruoti ir sugeneruoti Egipto išskaitomo mokesčio deklaracijas.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4e3d68ac003fabaa504ffe81b8bf2f7ff8d7538d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839797"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="fb7ae-103">Egipto išskaitomo mokesčio deklaracija (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="fb7ae-104">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="fb7ae-104">Overview</span></span>
<span data-ttu-id="fb7ae-105">Šioje temoje paaiškinama, kaip nustatyti ir generuoti išskaitomo mokesčio deklaraciją ir 41 ir 11 juridinių subjektų išskaitomo mokesčio deklaravimo formas Egipte</span><span class="sxs-lookup"><span data-stu-id="fb7ae-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="fb7ae-106">Visi Egipto subjektai turi parengti 41 formą, kurioje susumuojami visi mokesčiai, saugomi iš vietinių tiekėjų ir paslaugų teikėjų.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="fb7ae-107">Be 41 formos, 11 formą reikia sugeneruoti taip, kad išsamiai būtų sugeneruoti visi užsienio teikėjų išskirstyti mokesčiai.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="fb7ae-108">Ataskaita **Išskaitomo mokesčio deklaracija**, esanti „Dynamics 365 Finance“, apima tokias ataskaitas:</span><span class="sxs-lookup"><span data-stu-id="fb7ae-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="fb7ae-109">Deklaracijos formos Nr.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-109">Declaration form No.</span></span> <span data-ttu-id="fb7ae-110">41</span><span class="sxs-lookup"><span data-stu-id="fb7ae-110">41</span></span>
- <span data-ttu-id="fb7ae-111">Deklaracijos formos Nr.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-111">Declaration form No.</span></span> <span data-ttu-id="fb7ae-112">11</span><span class="sxs-lookup"><span data-stu-id="fb7ae-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="fb7ae-113">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="fb7ae-113">Prerequisites</span></span>
<span data-ttu-id="fb7ae-114">Pagrindinis juridinio subjekto adresas turi būti Egipte.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="fb7ae-115">Darbo srityje **Funkcijų valdymas** reikia įjungti toliau pateikiamą funkciją.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="fb7ae-116">**Visuotinis išskaitomas mokestis**</span><span class="sxs-lookup"><span data-stu-id="fb7ae-116">**Global withholding tax**</span></span>

<span data-ttu-id="fb7ae-117">Daugiau informacijos apie tai, kaip įjungti naujas funkcijas, žr. temoje [Funkcijų valdymo apžvalga.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="fb7ae-118">Eikite į **Mokesčiai** > **Nustatymas** > **Parametrai** > **Didžiosios knygos parametrai** ir skirtuke **Išskaitomas mokestis** parinktį **Įjungti visuotinį išskaitomą mokestį** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="fb7ae-119">Darbo srityje **Elektroninių ataskaitų teikimas** importuokite šį elektroninių ataskaitų teikimo formatus iš saugyklos:</span><span class="sxs-lookup"><span data-stu-id="fb7ae-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="fb7ae-120">WHT deklaravimas „Excel“ faile (EG)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb7ae-121">Šis formatas grindžiamas **Mokesčių deklaracijos modeliu** ir naudoja **Mokesčių deklaracijos modelio susiejimą**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="fb7ae-122">Ši papildoma konfigūracija importuojama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="fb7ae-123">Daugiau informacijos apie elektroninių ataskaitų teikimo konfigūracijų importavimą, žr. [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="fb7ae-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="fb7ae-124">Elektroninių ataskaitų konfigūracijų atsisiuntimas</span><span class="sxs-lookup"><span data-stu-id="fb7ae-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="fb7ae-125">Egipto WHT deklaracijos formos diegimas grindžiamas elektroninės ataskaitos (ER) konfigūracijomis.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="fb7ae-126">Daugiau informacijos apie galimybes ir konfigūruojamų ataskaitų sąvokas žr. [Elektroninių ataskaitų teikimas](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="fb7ae-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="fb7ae-127">Norėdami rasti gamybos ir naudotojo priėmimo tikrinimo (UAT) aplinkas, vadovaukitės instrukcijomis, pateikiamomis temoje [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="fb7ae-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="fb7ae-128">Norėdami sugeneruoti išskaitomo mokesčio deklaracijas Egipto juridiniame subjekte, turite įkelti šias konfigūracijas:</span><span class="sxs-lookup"><span data-stu-id="fb7ae-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="fb7ae-129">Mokesčių deklaracija model.version.82.xml arba naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="fb7ae-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="fb7ae-130">Mokesčių deklaracija model.mapping.version.82.133.xml arba naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="fb7ae-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="fb7ae-131">WHT deklaracijos „Excel“ (EG).version.82.21 ar naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="fb7ae-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="fb7ae-132">Baigę parsisiųsti ER konfigūracijas iš „Lifecycle Services“ (LCS) arba visuotinės saugyklos, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="fb7ae-133">Eikite į darbo sritį **Elektroninės ataskaitos** ir pasirinkite plytelę **Ataskaitų konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="fb7ae-134">Puslapyje **Konfigūracijos**, veiksmų srityje pasirinkite **Keisti > Įkelti iš XML failo**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="fb7ae-135">Įkelti visus failus tokia tvarka, kokia jie yra išvardyti ankstesniuose punktuose.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="fb7ae-136">Įkėlus visas konfigūracijas, srityje „Finansai“ turėtų būti konfigūracijos medis.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="fb7ae-137">Konkrečios programos parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="fb7ae-137">Set up application-specific parameters</span></span>

<span data-ttu-id="fb7ae-138">Konkretaus prašymo parametrų pasirinktis naudotojams leidžia nustatyti kriterijus, pagal kuriuos mokesčių operacijos bus klasifikacijos ir skaičiuojamos kiekvienoje sugeneruotos ataskaitos eilutėje, atsižvelgiant į **išskaitomo mokesčio prekės grupės** konfigūraciją ar kitus kriterijus, nustatytus peržvalgos apibrėžime.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="fb7ae-139">Išskaitomo mokesčio deklaracijos 41 formoje yra konkretus stulpelis, kuriame išskaitomo mokesčio operacija turi būti klasifikuojama pagal mokesčių inspekcijos klasifikacijos, pavadintos **Nuolaidos kodo tipas**, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="fb7ae-140">Užuot šias naujas klasifikacijas įtraukus kaip naujus įvesties duomenis, kai paskeliami sandoriai, klasifikacijos apibrėžiamos pagal skirtingas peržvalgas, kurios buvo įvestos pasirinkus **Konfigūracijos** > **Konkrečios programos parametrų nustatymas** > **Sąranka**, atsižvelgiant į Egipto PVM išskaičiavimų ataskaitų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="fb7ae-141">Klasifikuojant operacijas 41 išskaitomo mokesčio deklaracijos formoje naudojama ši konfigūracija:</span><span class="sxs-lookup"><span data-stu-id="fb7ae-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="fb7ae-142">**DiscountTaxTypeLookup**-> 18 stulpelis</span><span class="sxs-lookup"><span data-stu-id="fb7ae-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="fb7ae-143">Norėdami nustatyti skirtingas peržvalgas, naudojamas WHT deklaravimo ir susijusių knygų ataskaitoms generuoti, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="fb7ae-144">Darbo srityje **Elektroninės ataskaitos** pasirinkite **Konfigūracijos** > **Sąranka**, kad nustatytumėte taisykles, skirtas operacijoms klasifikuoti WHT deklaracijos ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="fb7ae-145">Pasirinkite dabartinę versiją ir „FastTab“ skirtuke **Peržvalgos** pasirinkite peržvalgos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="fb7ae-146">Pvz., **DiscountTaxTypeLookup**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="fb7ae-147">Ši peržvalga nustato nuolaidų tipų, kurių reikalauja mokesčių inspekcija, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="fb7ae-148">„FastTab“ skirtuke **Sąlygos** pasirinkite **Pridėti** ir naujoje eilutėje, stulpelyje **Peržvalgos rezultatas** pasirinkite susijusią eilutę, kuri vaizduoja klasifikaciją **18 stulpelyje**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="fb7ae-149">Stulpelyje **Išskaičiuojamų mokesčių elementų grupė** pasirinkite susijusį kodą, kuris naudojamas klasifikacijai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="fb7ae-150">Pavyzdžiui, **Leidžiama nuolaida**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="fb7ae-151">Visoms galimoms peržvalgoms pakartokite 3 ir 4 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="fb7ae-152">Dar kartą pasirinkite **Pridėti**, jei norite įtraukti paskutinio įrašo eilutę, o stulpelyje **Peržvalgos rezultatas** pasirinkite **Netaikoma**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="fb7ae-153">Likusiuose stulpeliuose pasirinkite **Ne tuščia**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="fb7ae-154">Didžiosios knygos parametrų sąranka</span><span class="sxs-lookup"><span data-stu-id="fb7ae-154">Set up General ledger parameters</span></span>

<span data-ttu-id="fb7ae-155">Jei norite generuoti WHT deklaracijos formos ataskaitas programoje „Microsoft Excel“, apibrėžkite ER formatą puslapyje **Didžiosios knygos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="fb7ae-156">Eikite į **Mokesčiai** > **Sąranka** > **Didžiosios knygos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="fb7ae-157">Skirtuko **Išskaitomas mokestis** lauke **WHT deklaracijos formato susiejimas** pasirinkite **WHT deklaracija „Excel“ formatu (EG)**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="fb7ae-158">Jei laukelį paliekate tuščią, standartinė pardavimų mokesčių ataskaita bus generuojama SSRS formatu.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![Deklaracijos forma](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="fb7ae-160">Išskaitomo mokesčio deklaracijų formų deklaravimas</span><span class="sxs-lookup"><span data-stu-id="fb7ae-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="fb7ae-161">Tam tikro laikotarpio išskaitomo mokesčio formos paruošimo ir pateikimo procesas yra paremtas išskaitomo mokesčio operacijomis, užregistruotomis sudengimo ir mokėjimo registravimo mokesčio užduoties metu.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="fb7ae-162">Daugiau informacijos apie visuotinį išskaitomą mokestį ieškokite skyriuje [Visuotinis išskaitomas mokestis](../general-ledger/global-withholding-tax-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fb7ae-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="fb7ae-163">Atlikite šiuos veiksmus, kad sugeneruotumėte mokesčių deklaracijos ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="fb7ae-164">Eikite į **Mokestis** > **Deklaracijos** > **Išskaitomas mokestis** > \**Išskaitomo mokesčio mokėjimas*.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="fb7ae-165">Pasirinkite sudengimo laikotarpį ir tada pasirinkite ataskaitos pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="fb7ae-166">Įveskite sandorio datą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="fb7ae-167">Atidaromame dialogo lange pasirinkite vieną ar daugiau formų tipų **Forma 41**, **Forma 11** arba **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="fb7ae-168">Jei pasirinksite **Nėra**, bus sugeneruota standartinė ataskaita.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="fb7ae-169">Pasirinkti kalbą.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-169">Select the language.</span></span> <span data-ttu-id="fb7ae-170">Visos ataskaitos yra verčiamos į **en-us** ir **ar-eg** kalbas.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="fb7ae-171">Įveskite banko, kuriame bus mokami mokesčiai, filialą ir pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="fb7ae-172">Pasirinkite verslo tipą ir įveskite čekių ir dokumentų numerius.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="fb7ae-173">Įveskite objekto tipą.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="fb7ae-174">Įveskite asmens, kuris buvo užregistruotas formai priskirti, vardą ir pavardę, o norėdami patvirtinti ataskaitos generavimą paspauskite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
