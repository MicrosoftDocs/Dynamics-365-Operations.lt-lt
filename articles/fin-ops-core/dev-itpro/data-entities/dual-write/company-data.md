---
title: Įmonės koncepcija „Dataverse“
description: Šioje temoje aprašomas įmonės duomenų integravimas tarp „Finance and Operations“ ir „Dataverse“.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 189d1b8a68f8457d32d656fefeb6cc2a332a3b22
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560254"
---
# <a name="company-concept-in-dataverse"></a><span data-ttu-id="68e47-103">Įmonės koncepcija „Dataverse“</span><span class="sxs-lookup"><span data-stu-id="68e47-103">Company concept in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="68e47-104">„Finance and Operations“ *įmonės* koncepcija yra tiek teisinis, tiek verslo konstruktas.</span><span class="sxs-lookup"><span data-stu-id="68e47-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="68e47-105">Ji taip pat apibrėžia duomenų saugos ir matomumo ribas.</span><span class="sxs-lookup"><span data-stu-id="68e47-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="68e47-106">Vartotojai visada dirba vienos įmonės kontekste, o dauguma duomenų yra įmonės suskirstyti.</span><span class="sxs-lookup"><span data-stu-id="68e47-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="68e47-107">„Dataverse“ nenaudojama lygiavertė koncepcija.</span><span class="sxs-lookup"><span data-stu-id="68e47-107">Dataverse doesn't have an equivalent concept.</span></span> <span data-ttu-id="68e47-108">Artimiausia koncepcija yra *verslo struktūros vienetas*, kuris pirmiausia apima vartotojo duomenų saugos ir matomumo ribas.</span><span class="sxs-lookup"><span data-stu-id="68e47-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="68e47-109">Ši koncepcija neturi tokios pačios teisinės ar verslo reikšmės kaip įmonės koncepcija.</span><span class="sxs-lookup"><span data-stu-id="68e47-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="68e47-110">Verslo struktūros vienetas ir įmonė nėra lygiavertės koncepcijos, todėl „Dataverse“ integracijos tikslais negalima taikyti jų vienas su vienu (1:1) susiejimo.</span><span class="sxs-lookup"><span data-stu-id="68e47-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Dataverse integration.</span></span> <span data-ttu-id="68e47-111">Tačiau vartotojai turi, kaip numatyta, galėti peržiūrėti tas pačias eilutes programoje ir „Dataverse“, todėl „Microsoft“ pristatė naują lentelę „Dataverse”, pavadintą cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="68e47-111">However, because users must, by default, be able to see the same rows in the application and Dataverse, Microsoft has introduced a new table in Dataverse that is named cdm\_Company.</span></span> <span data-ttu-id="68e47-112">Ši lentelė yra lygiavertė įmonės lentelei programoje.</span><span class="sxs-lookup"><span data-stu-id="68e47-112">This table is equivalent to the Company table in the application.</span></span> <span data-ttu-id="68e47-113">Siekiant užtikrinti eilučių matomumo lygiavertiškumą pradėjus naudoti programą ir „Dataverse“, rekomenduojame toliau pateiktus „Dataverse“ duomenų nustatymus.</span><span class="sxs-lookup"><span data-stu-id="68e47-113">To help guarantee that visibility of rows is equivalent between the application and Dataverse out of the box, we recommend the following setup for data in Dataverse:</span></span>

+ <span data-ttu-id="68e47-114">Kiekvienai „Finance and Operations“ įmonės eilutei, kuri įgalinta dvigubam rašymui, sukuriama susieta cdm\_Company eilutė.</span><span class="sxs-lookup"><span data-stu-id="68e47-114">For each Finance and Operations Company row that is enabled for dual-write, an associated cdm\_Company row is created.</span></span>
+ <span data-ttu-id="68e47-115">Sukūrus cdm\_Company eilutę ir įgalinus dvigubam rašymui, sukuriamas numatytasis verslo struktūros vienetas tuo pačiu pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="68e47-115">When a cdm\_Company row is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="68e47-116">Nors tam verslo struktūros vienetui automatiškai sukuriama numatytoji komanda, verslo struktūros vienetas nėra naudojamas.</span><span class="sxs-lookup"><span data-stu-id="68e47-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="68e47-117">Sukuriama atskira savininko komanda tokiu pačiu pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="68e47-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="68e47-118">Ji taip pat susiejama su verslo struktūros vienetu.</span><span class="sxs-lookup"><span data-stu-id="68e47-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="68e47-119">Pagal numatytuosius nustatymus, bet kurios eilutės, kuri sukuriama ir įrašoma dvigubu rašymu „Dataverse“, savininkas nustatomas į „DW Owner“ komandą, kuri susiejama su susijusiu verslo struktūros vienetu.</span><span class="sxs-lookup"><span data-stu-id="68e47-119">By default, the owner of any row that is created and dual-written to Dataverse is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="68e47-120">Tolesnėje iliustracijoje pateikiamas šio duomenų nustatymo „Dataverse“ pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="68e47-120">The following illustration shows an example of this data setup in Dataverse.</span></span>

![Duomenų nustatymas „Dataverse“](media/dual-write-company-1.png)

<span data-ttu-id="68e47-122">Dėl tokios konfigūracijos bet kokia eilutė, susieta su USMF įmone, priklauso komandai, kuri yra susieta su USMF verslo struktūros vienetu „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="68e47-122">Because of this configuration, any row that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Dataverse.</span></span> <span data-ttu-id="68e47-123">Todėl tas eilutes gali matyti bet kuris vartotojas, kuris turi prieigą prie to verslo struktūros vieneto pasitelkiant saugos vaidmenį, kuris nustatytas verslo struktūros vieneto lygio matomumui.</span><span class="sxs-lookup"><span data-stu-id="68e47-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those rows.</span></span> <span data-ttu-id="68e47-124">Toliau pateikiamas pavyzdys, kaip komandos gali būti naudojamos norint suteikti tinkamą prieigą prie tų eilučių.</span><span class="sxs-lookup"><span data-stu-id="68e47-124">The following example shows how teams can be used to provide the correct access to those rows.</span></span>

+ <span data-ttu-id="68e47-125">Vaidmuo „Pardavimo vadybininkas“ priskiriamas „USMF pardavimas“ komandos nariams.</span><span class="sxs-lookup"><span data-stu-id="68e47-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="68e47-126">Vartotojai, turintys vaidmenį „Pardavimo vadybininkas“, turi prieigą prie visų paskyros eilučių, kurios yra to paties verslo struktūros vieneto nariai.</span><span class="sxs-lookup"><span data-stu-id="68e47-126">Users who have the "Sales Manager" role can access any account rows that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="68e47-127">„USMF pardavimas“ komanda susiejama su anksčiau minėtu USMF verslo struktūros vienetu.</span><span class="sxs-lookup"><span data-stu-id="68e47-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="68e47-128">Todėl „USMF pardavimas“ komandos nariai gali matyti bet kurią paskyrą, priklausančią „USMF DW“ vartotojui, kuris būtų gautas iš USMF įmonės lentelės naudojant „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="68e47-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company table in Finance and Operations.</span></span>

![Komandų naudojimas](media/dual-write-company-2.png)

<span data-ttu-id="68e47-130">Kaip parodyta ankstesnėje iliustracijoje, šis 1:1 susiejimas tarp verslo struktūros vieneto, įmonės ir komandos yra tik pradžios taškas.</span><span class="sxs-lookup"><span data-stu-id="68e47-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="68e47-131">Tolesniame pavyzdyje naujas verslo struktūros vienetas „Europa“ rankiniu būdu sukuriamas „Dataverse“ kaip DEMF ir ESMF pirminis elementas.</span><span class="sxs-lookup"><span data-stu-id="68e47-131">In this example, a new "Europe" business unit is manually created in Dataverse as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="68e47-132">Šis naujas šakninis verslo struktūros vienetas nėra susijęs su dvigubu rašymu.</span><span class="sxs-lookup"><span data-stu-id="68e47-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="68e47-133">Tačiau jis gali būti naudojamas siekiant suteikti „EUR pardavimas“ komandos nariams prieigą prie paskyros duomenų tiek DEMF, tiek ESMF nustatant duomenų matomumą į **Pirminis/antrinis BU** susietam saugos vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="68e47-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="68e47-134">Paskutinėje temoje aptariama, kaip dvigubas rašymas nustato, kuriai savininkų komandai reikėtų priskirti eilutes.</span><span class="sxs-lookup"><span data-stu-id="68e47-134">A final topic to discuss is how dual-write determines which owner team it should assign rows to.</span></span> <span data-ttu-id="68e47-135">Šią veikseną kontroliuoja stulpelis **Numatytoji komanda savininkė** eilutėje cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="68e47-135">This behavior is controlled by the **Default owning team** column on the cdm\_Company row.</span></span> <span data-ttu-id="68e47-136">Kai cdm\_Company eilutė yra įgalinta dvigubam rašymui, priedas automatiškai sukuria susietą verslo struktūros vienetą ir savininko komandą (jei jos dar nėra) ir nustato **Numatytoji komanda savininkė** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="68e47-136">When a cdm\_Company row is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** column.</span></span> <span data-ttu-id="68e47-137">Administratorius gali pakeisti šį stulpelį kita reikšme.</span><span class="sxs-lookup"><span data-stu-id="68e47-137">The admin can change this column to a different value.</span></span> <span data-ttu-id="68e47-138">Tačiau administratorius negali išvalyti stulpelio tol, kol lentelei įgalintas dvigubas rašymas.</span><span class="sxs-lookup"><span data-stu-id="68e47-138">However, the admin can't clear the column as long as the table is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="68e47-139">![Stulpelis Numatytoji komanda savininkė](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="68e47-139">![Default owning team column](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="68e47-140">Įmonės paskirstymas ir įkėlimas</span><span class="sxs-lookup"><span data-stu-id="68e47-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="68e47-141">„Dataverse“ integracija suteikia įmonės lygiavertiškumą naudojant įmonės identifikatorių, skirtą paskirstyti duomenis.</span><span class="sxs-lookup"><span data-stu-id="68e47-141">Dataverse integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="68e47-142">Kaip parodyta toliau pateiktoje iliustracijoje, visos konkrečios įmonės lentelės išplečiamos taip, kad su cdm\_Company lentele turėtų ryšį „daugelis su vienu“ (N:1).</span><span class="sxs-lookup"><span data-stu-id="68e47-142">As the following illustration shows, all company-specific tables are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company table.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="68e47-143">![N:1 ryšys tarp konkrečios įmonės ir cdm_Company lentelių](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="68e47-143">![N:1 relationship between a company-specific table and the cdm_Company table](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="68e47-144">Įtraukus ir įrašius įmonę eilučių reikšmė tampa skirta tik skaityti.</span><span class="sxs-lookup"><span data-stu-id="68e47-144">For rows, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="68e47-145">Todėl vartotojai turėtų įsitikinti, kad pasirinko tinkamą įmonę.</span><span class="sxs-lookup"><span data-stu-id="68e47-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="68e47-146">Tik tos eilutės, kurios apima įmonės duomenis, gali būti dvigubo rašymo tarp programos ir „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="68e47-146">Only rows that have company data are eligible for dual-write between the application and Dataverse.</span></span>
+ <span data-ttu-id="68e47-147">Esamiems „Dataverse“ duomenims netrukus bus teikiama administratoriaus vadovaujama įkėlimo patirtis.</span><span class="sxs-lookup"><span data-stu-id="68e47-147">For existing Dataverse data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="68e47-148">Automatinis įmonės pavadinimo įvedimas „Customer engagement” programoms</span><span class="sxs-lookup"><span data-stu-id="68e47-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="68e47-149">Yra keli būdai automatiškai įvesti įmonės pavadinimą „Customer Engagement” programose.</span><span class="sxs-lookup"><span data-stu-id="68e47-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="68e47-150">Jei esate sistemos administratorius, galite nustatyti numatytąją įmonę eidami į **Išplėstiniai nustatymai > Sistema > Sauga > Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="68e47-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="68e47-151">Atidarykite formą **Vartotojas** ir skyriuje **Organizacijos informacija** nustatykite **Įmonė kaip numatytoji formose** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="68e47-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Numatytosios įmonės nustatymas skyriuje Organizacijos informacija.":::

+ <span data-ttu-id="68e47-153">Jei turite **Rašymo** prieigą prie **„SystemUser”** lentelės **Verslo vieneto** lygiu, tada galite pakeisti numatytąją įmonę bet kurioje formoje pasirinkdami įmonę iš išplečiamojo meniu **Įmonė**.</span><span class="sxs-lookup"><span data-stu-id="68e47-153">If you have **Write** access to the **SystemUser** table for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Įmonės vardo keitimas naujoje paskyroje.":::

+ <span data-ttu-id="68e47-155">Jei turite **Rašymo** prieigą prie daugiau nei vienos įmonės duomenų, tada galite keisti numatytąją įmonę pasirinkdami eilutę, priklausančią kitai įmonei.</span><span class="sxs-lookup"><span data-stu-id="68e47-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a row that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Eilutės pasirinkimas pakeičia numatytąją įmonę.":::

+ <span data-ttu-id="68e47-157">Jeigu esate sistemos konfigūratorius arba administratorius ir norite įvesti įmonės pavadinimą automatiškai pasirinktinėje formoje, galite naudoti [formų įvykius](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span><span class="sxs-lookup"><span data-stu-id="68e47-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="68e47-158">Pridėkite JavaScript nuorodą į **msdyn_/DefaultCompany.js** ir naudokite šiuos įvykius.</span><span class="sxs-lookup"><span data-stu-id="68e47-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="68e47-159">Galite naudoti bet kurią visiškai parengtą formą, pavyzdžiui **Paskyra** formą.</span><span class="sxs-lookup"><span data-stu-id="68e47-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="68e47-160">**„OnLoad”** įvykis formai: nustatykite **„defaultCompany”** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="68e47-160">**OnLoad** event for the form: Set the **defaultCompany** column.</span></span>
    + <span data-ttu-id="68e47-161">**„OnChange”** įvykis **Įmonės** stulpeliui: nustatykite **„updateDefaultCompany”** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="68e47-161">**OnChange** event for the **Company** column: Set the **updateDefaultCompany** column.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="68e47-162">Filtravimo, paremto įmonės kontekstu, taikymas</span><span class="sxs-lookup"><span data-stu-id="68e47-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="68e47-163">Norėdami taikyti filtravimą, paremtą įmonės kontekstu Jūsų pasirinktinėse formose arba pasirinktiniuose peržvalgos stulpeliuose, pridėtuose standartinėse formose, atidarykite formą ir naudokite skyrių **Susijusių įrašų filtravimas** įmonės filtro taikymui.</span><span class="sxs-lookup"><span data-stu-id="68e47-163">To apply filtering based on the company context on your custom forms or on custom lookup columns added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="68e47-164">Turite tai nustatyti kiekvienam peržvalgos stulpeliui, kuriam reikalingas filtravimas, paremtas esančia įmone pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="68e47-164">You must set this for each lookup column that requires filtering based on the underlying company on a given row.</span></span> <span data-ttu-id="68e47-165">Parametras rodomas dalyje **Paskyra** šioje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="68e47-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="Įmonės konteksto taikymas":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]