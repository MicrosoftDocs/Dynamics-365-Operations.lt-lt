---
title: Duomenų eksportavimas iš „Attract“ ir „Onboard“
description: Duomenų eksportavimas iš „Dynamics 365 Talent“ – „Attract“ ir „Onboard“.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461940"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="22c1c-103">Duomenų eksportavimas iš „Attract“ ir „Onboard“</span><span class="sxs-lookup"><span data-stu-id="22c1c-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="22c1c-104">Kaip paskelbta [„Dynamics 365 Talent: Attract“ ir „Dynamics 365 Talent: Onboard“ programų panaikinime](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), panaikiname „Dynamics 365 Talent: Attract“ ir „Dynamics 365 Talent: Onboard“ nuo 2022 m. vasario 1 d.</span><span class="sxs-lookup"><span data-stu-id="22c1c-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="22c1c-105">Siekiant padėti pereiti į kitą produktą, abiejose programose dabar yra duomenų eksportavimo galimybės.</span><span class="sxs-lookup"><span data-stu-id="22c1c-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="22c1c-106">Duomenų eksportavimas iš „Attract“</span><span class="sxs-lookup"><span data-stu-id="22c1c-106">Export data from Attract</span></span>

<span data-ttu-id="22c1c-107">Galite eksportuoti duomenis be prieigos prie savo aplinkos apribojimų.</span><span class="sxs-lookup"><span data-stu-id="22c1c-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="22c1c-108">Galbūt norėsite tai atlikti testavimo tikslais arba norėdami suprasti savo duomenų struktūrą.</span><span class="sxs-lookup"><span data-stu-id="22c1c-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="22c1c-109">Kai būsite pasiruošę perkėlimui, apribokite prieigą prie savo „Attract“ aplinkos vadovaudamiesi instrukcijomis po šia procedūra.</span><span class="sxs-lookup"><span data-stu-id="22c1c-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="22c1c-110">Nepamirškite iš naujo eksportuoti savo duomenų.</span><span class="sxs-lookup"><span data-stu-id="22c1c-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="22c1c-111">Eikite į [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="22c1c-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="22c1c-112">Dalyje **Duomenų eksportavimas** pasirinkite **Prašyti duomenų eksportavimo**.</span><span class="sxs-lookup"><span data-stu-id="22c1c-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="22c1c-113">Prašyti duomenų eksportavimo iš „Attract“</span><span class="sxs-lookup"><span data-stu-id="22c1c-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="22c1c-114">Kai bus rodomas pranešimo langas **Jūsų prašymas apdorojamas**, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="22c1c-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="22c1c-115">Duomenų eksportavimas gali užtrukti iki 20 minučių, priklausomai nuo eksportavimo dydžio.</span><span class="sxs-lookup"><span data-stu-id="22c1c-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="22c1c-116">Kai eksportavimas baigiamas, prie jo pasirinkite mygtuką **Atsisiųsti**.</span><span class="sxs-lookup"><span data-stu-id="22c1c-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="22c1c-117">Visų duomenų eksportavimas galioja septynias dienas, kurioms praėjus nebegalioja saitas **Atsisiuntimas**.</span><span class="sxs-lookup"><span data-stu-id="22c1c-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="22c1c-118">Atsisiuntime yra .zip failas su jūsų „Attract“ duomenimis, įskaitant toliau nurodytus aplankus.</span><span class="sxs-lookup"><span data-stu-id="22c1c-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="22c1c-119">Aplanko pavadinimas</span><span class="sxs-lookup"><span data-stu-id="22c1c-119">Folder name</span></span> | <span data-ttu-id="22c1c-120">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="22c1c-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="22c1c-121">Administratoriaus parametrai</span><span class="sxs-lookup"><span data-stu-id="22c1c-121">Admin settings</span></span> | <span data-ttu-id="22c1c-122">„Attract“ administravimo centro konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="22c1c-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="22c1c-123">Kandidatai</span><span class="sxs-lookup"><span data-stu-id="22c1c-123">Candidates</span></span> | <span data-ttu-id="22c1c-124">Visi kandidatai, įtraukti į užduočių arba talentų telkinius.</span><span class="sxs-lookup"><span data-stu-id="22c1c-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="22c1c-125">El. laiško šablonai</span><span class="sxs-lookup"><span data-stu-id="22c1c-125">Email templates</span></span> | <span data-ttu-id="22c1c-126">Visi aplinkoje sukonfigūruoti el. laiškų šablonai.</span><span class="sxs-lookup"><span data-stu-id="22c1c-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="22c1c-127">Darbo pasiūlymų paketų šablonai</span><span class="sxs-lookup"><span data-stu-id="22c1c-127">Job offer package templates</span></span> | <span data-ttu-id="22c1c-128">Visų sukurtų darbo pasiūlymų paketų šablonai, taip pat jų susijusios konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="22c1c-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="22c1c-129">Darbo pasiūlymo taisyklių rinkiniai</span><span class="sxs-lookup"><span data-stu-id="22c1c-129">Job offer rule sets</span></span> |  <span data-ttu-id="22c1c-130">Visų taisyklių rinkinių failai, kuriuos įkėlėte pasiūlymų valdymui.</span><span class="sxs-lookup"><span data-stu-id="22c1c-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="22c1c-131">Darbo pasiūlymų šablonai</span><span class="sxs-lookup"><span data-stu-id="22c1c-131">Job offer templates</span></span> | <span data-ttu-id="22c1c-132">Visi darbo pasiūlymų dokumentų šablonai, sukurti aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="22c1c-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="22c1c-133">Laisvos darbo vietos</span><span class="sxs-lookup"><span data-stu-id="22c1c-133">Job openings</span></span> | <span data-ttu-id="22c1c-134">Visi sukurti darbai.</span><span class="sxs-lookup"><span data-stu-id="22c1c-134">All created jobs.</span></span> <span data-ttu-id="22c1c-135">Panaikinti darbai neeksportuojami.</span><span class="sxs-lookup"><span data-stu-id="22c1c-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="22c1c-136">Poaplankiuose yra kandidatų paraiškos su poaplankiais kandidatų paraiškų priedams ir pasiūlymų paketais, jei taikoma.</span><span class="sxs-lookup"><span data-stu-id="22c1c-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="22c1c-137">Darbo pasiūlymų šablonai</span><span class="sxs-lookup"><span data-stu-id="22c1c-137">Job opening templates</span></span> | <span data-ttu-id="22c1c-138">Darbo apdorojimo šablonai, sukonfigūruoti aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="22c1c-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="22c1c-139">Talentų telkiniai</span><span class="sxs-lookup"><span data-stu-id="22c1c-139">Talent pools</span></span> | <span data-ttu-id="22c1c-140">Visi sukurti talentų telkiniai, jų bendraautorių sąrašai ir talentų telkinių sąrašai.</span><span class="sxs-lookup"><span data-stu-id="22c1c-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="22c1c-141">Darbininkai</span><span class="sxs-lookup"><span data-stu-id="22c1c-141">Workers</span></span> | <span data-ttu-id="22c1c-142">Visų darbuotojų, kurie yra aplinkoje, sąrašas ir darbuotojų vaidmenys.</span><span class="sxs-lookup"><span data-stu-id="22c1c-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="22c1c-143">(šakninis aplankas)</span><span class="sxs-lookup"><span data-stu-id="22c1c-143">(root folder)</span></span> | <span data-ttu-id="22c1c-144">JSON schemos failas, aprašantis duomenų struktūros laukus.</span><span class="sxs-lookup"><span data-stu-id="22c1c-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="22c1c-145">Prieigos prie „Attract“ apribojimas</span><span class="sxs-lookup"><span data-stu-id="22c1c-145">Restrict access to Attract</span></span>

<span data-ttu-id="22c1c-146">Kai esate pasiruošę perkėlimui, apribokite ne administratorių prieigą prie „Attract“ aplinkos ir eksportuokite duomenis.</span><span class="sxs-lookup"><span data-stu-id="22c1c-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="22c1c-147">Prieiga prie „Attract“ aplinkos apribojama visam laikui ir apribojimo negalima atšaukti.</span><span class="sxs-lookup"><span data-stu-id="22c1c-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="22c1c-148">Jei norite, kad ne administratorių vartotojai galėtų toliau naudotis jūsų aplinka, praleiskite šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="22c1c-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="22c1c-149">Eikite į [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="22c1c-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="22c1c-150">Norėdami apriboti ne administratorių prieigą prie „Attract“ aplinkos, dalyje **Apriboti prieigą prie šios programos** pasirinkite **Apriboti prieigą dabar**.</span><span class="sxs-lookup"><span data-stu-id="22c1c-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="22c1c-151">Apribojus prieigą, taip pat anuliojamos visos užregistruotos aktyvios užduotys.</span><span class="sxs-lookup"><span data-stu-id="22c1c-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="22c1c-152">Ne administratorių prieigos prie „Attract“ apribojimas</span><span class="sxs-lookup"><span data-stu-id="22c1c-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="22c1c-153">Kai matote įspėjimą **Tai yra nuolatinis pakeitimas**, pasirinkite **Apriboti prieigą**, kad visam laikui apribotumėte ne administratorių vartotojų prieigą prie šios aplinkos.</span><span class="sxs-lookup"><span data-stu-id="22c1c-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="22c1c-154">Jei nesate pasirengę atlikti šio veiksmo, pasirinkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="22c1c-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="22c1c-155">Įspėjimas, kad apribota prieiga yra nuolatinis pakeitimas</span><span class="sxs-lookup"><span data-stu-id="22c1c-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="22c1c-156">Administratoriai gali toliau naudotis duomenų eksportavimo ir ataskaitų pagal asmenis puslapiais po to, kai apribojote prieigą prie „Attract“ aplinkos.</span><span class="sxs-lookup"><span data-stu-id="22c1c-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="22c1c-157">Eksportuoti duomenis iš „Onboard”</span><span class="sxs-lookup"><span data-stu-id="22c1c-157">Export data from Onboard</span></span>

<span data-ttu-id="22c1c-158">Kai būsite pasiruošę, galite atsisiųsti šablonus, vadovus ir kandidato duomenis iš „Onboard“.</span><span class="sxs-lookup"><span data-stu-id="22c1c-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="22c1c-159">Eikite į [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span><span class="sxs-lookup"><span data-stu-id="22c1c-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="22c1c-160">Dalyje **Duomenų eksportavimas** pasirinkite **Prašyti duomenų eksportavimo**.</span><span class="sxs-lookup"><span data-stu-id="22c1c-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="22c1c-161">Prašyti duomenų eksportavimo iš „Onboard“</span><span class="sxs-lookup"><span data-stu-id="22c1c-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="22c1c-162">Kai bus rodomas pranešimo langas **Jūsų prašymas apdorojamas**, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="22c1c-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="22c1c-163">Duomenų eksportavimas gali užtrukti iki 20 minučių, priklausomai nuo eksportavimo dydžio.</span><span class="sxs-lookup"><span data-stu-id="22c1c-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="22c1c-164">Kai eksportavimas baigiamas, prie jo pasirinkite mygtuką **Atsisiųsti**.</span><span class="sxs-lookup"><span data-stu-id="22c1c-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="22c1c-165">Atsisiųsti eksportuotus duomenis iš „Onboard”</span><span class="sxs-lookup"><span data-stu-id="22c1c-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="22c1c-166">Duomenis galite eksportuoti septynias dienas.</span><span class="sxs-lookup"><span data-stu-id="22c1c-166">Your data export is available for seven days.</span></span> <span data-ttu-id="22c1c-167">Po septynių dienų, saitas **Atsisiuntimas** nebegalioja, todėl turite prašyti naujo eksportavimo, jei reikia iš naujo atsiųsti duomenis.</span><span class="sxs-lookup"><span data-stu-id="22c1c-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="22c1c-168">Paleidus naują duomenų eksportavimą, visi esami atsisiuntimai nustos galioti po naujo eksportavimo.</span><span class="sxs-lookup"><span data-stu-id="22c1c-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="22c1c-169">Atsisiuntimas yra .zip failas, kuriame yra:</span><span class="sxs-lookup"><span data-stu-id="22c1c-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="22c1c-170">Aplankas **Šablonai**, kuriame yra jūsų „Onboard“ šablonai „Word“ dokumentų formatu.</span><span class="sxs-lookup"><span data-stu-id="22c1c-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="22c1c-171">Aplankas **Guides**, kuriame yra jūsų „Onboard“ vadovai „Word“ dokumentų formatu.</span><span class="sxs-lookup"><span data-stu-id="22c1c-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="22c1c-172">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="22c1c-172">See also</span></span>

[<span data-ttu-id="22c1c-173">„Dynamics 365 Talent: Attract“ ir „Dynamics 365 Talent: Onboard“ programų panaikinimas</span><span class="sxs-lookup"><span data-stu-id="22c1c-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)