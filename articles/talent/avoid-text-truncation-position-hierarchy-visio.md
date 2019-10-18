---
title: Kaip išvengti pareigų hierarchijos teksto trumpinimo ir ją eksportuoti į „Visio“
description: Šioje temoje paaiškinama, kaip išspręsti asmenų vardų ir (arba) pavardžių bei pareigų pavadinimų trumpinimo problemą, kai klientai peržiūri „Microsoft Dynamics 365 Talent“ pareigų hierarchiją. Dėl teksto trumpinimo gali būti sudėtinga užfiksuoti ekrano kopiją arba išspausdinti hierarchiją.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e151818f29ac37ff449daaf1dc02e44b8fb317c3
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008505"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="acd6f-104">Kaip išvengti pareigų hierarchijos teksto trumpinimo ir ją eksportuoti į „Visio“</span><span class="sxs-lookup"><span data-stu-id="acd6f-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="acd6f-105">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="acd6f-105">**Issue**</span></span>

<span data-ttu-id="acd6f-106">Kai klientas peržiūri „Microsoft Dynamics 365 Talent“ pareigų hierarchiją, asmenų vardai ir (arba) pavardės bei pareigų pavadinimai sutrumpinami.</span><span class="sxs-lookup"><span data-stu-id="acd6f-106">When a customer views the position hierarchy in Microsoft Dynamics 365 Talent, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="acd6f-107">Todėl gali būti sudėtinga užfiksuoti ekrano kopiją arba išspausdinti ir paskirstyti hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="acd6f-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Darbo vietų hierarchija](media/position-h.png)

<span data-ttu-id="acd6f-109">**Priežastis**</span><span class="sxs-lookup"><span data-stu-id="acd6f-109">**Cause**</span></span>

<span data-ttu-id="acd6f-110">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="acd6f-110">This behavior is by design.</span></span>

<span data-ttu-id="acd6f-111">**Skiriamoji geba**</span><span class="sxs-lookup"><span data-stu-id="acd6f-111">**Resolution**</span></span>

<span data-ttu-id="acd6f-112">Deja, vartotojai negali lengvai keisti teksto dydį.</span><span class="sxs-lookup"><span data-stu-id="acd6f-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="acd6f-113">Tačiau galite eksportuoti pareigų hierarchiją iš „Talent“ ir importuoti ją į „Microsoft Visio“.</span><span class="sxs-lookup"><span data-stu-id="acd6f-113">However, you can export the position hierarchy out of Talent and then import it into Microsoft Visio.</span></span> <span data-ttu-id="acd6f-114">Nors šis straipsnis buvo parašytas „Microsoft Dynamics AX 2012“, procesas vis dar taikomas „Talent“: [Pareigų hierarchijos eksportavimas į „Microsoft Visio“](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="acd6f-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Talent: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="acd6f-115">Norėdami eksportuoti į „Visio“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="acd6f-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="acd6f-116">Programoje „Talent“ atidarykite sąrašo puslapį **Pareigos**.</span><span class="sxs-lookup"><span data-stu-id="acd6f-116">In Talent, open the **Positions** list page.</span></span>

    <span data-ttu-id="acd6f-117">Norėdami įtraukti daugiau informacijos į organizacijos struktūros diagramą, įtraukite laukus į sąrašą **Pareigos**, kad jie būtų prieinami, kai vėliau šioje procedūroje naudosite vediklį.</span><span class="sxs-lookup"><span data-stu-id="acd6f-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="acd6f-118">Veiksmų srityje pasirinkite mygtuką **Atidaryti naudojant „Microsoft Office“**, tada dalyje **Eksportuoti į „Excel“** pasirinkite **Pareigos**.</span><span class="sxs-lookup"><span data-stu-id="acd6f-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="acd6f-119">Arba paspauskite Ctrl+T.</span><span class="sxs-lookup"><span data-stu-id="acd6f-119">Alternatively, press Ctrl+T.</span></span>

    ![Eksportuoti pareigų sąrašo puslapį į „Excel“](media/org-admin.png)

3. <span data-ttu-id="acd6f-121">Įrašykite eksportuotą „Excel“ failą.</span><span class="sxs-lookup"><span data-stu-id="acd6f-121">Save the Excel file that is exported.</span></span>

    ![Eksportuoti į „Excel“ dialogo langą](media/export-excel.png)

4. <span data-ttu-id="acd6f-123">Programoje „Visio“ pasirinkite **„Visio“ – kurti naują**, tada pasirinkite šablono kategoriją **Įmonės**.</span><span class="sxs-lookup"><span data-stu-id="acd6f-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Nauja diagrama](media/new.png)

5. <span data-ttu-id="acd6f-125">Pasirinkite**Organizacijos struktūros diagramų vediklis**, tada pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="acd6f-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Organizacijos struktūros diagramų vediklio dialogo langas](media/orgchart-wizard.png)

6. <span data-ttu-id="acd6f-127">Pasirinkite **Informacija, kuri jau saugoma faile arba duomenų bazėje**, tada pasirinkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="acd6f-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![1 organizacijos struktūros diagramų vediklis](media/orgchart-wizard7.png)

7. <span data-ttu-id="acd6f-129">Pasirinkite **Tekstas, „Org Plus“ (\*.txt) arba „Excel“ failas**, tada pasirinkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="acd6f-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![2 organizacijos struktūros diagramų vediklis](media/orgchart-wizard3.png)

8. <span data-ttu-id="acd6f-131">Naršykite, kad pasirinktumėte eksportuotą „Excel“ failą, kuriame yra pareigų hierarchija, tada pasirinkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="acd6f-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![3 organizacijos struktūros diagramų vediklis](media/orgchart-wizard2.png)

9. <span data-ttu-id="acd6f-133">Lauką **Pavadinimas / vardas ir (arba) pavardė** nustatykite į **Pareigos**, lauką **Teikia ataskaitas** – į **Teikia ataskaitas pareigų atstovui**, tada pasirinkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="acd6f-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![4 organizacijos struktūros diagramų vediklis](media/orgchart-wizard1.png)

10. <span data-ttu-id="acd6f-135">Pasirinkite laukus, kurie turi būti rodomi kiekviename mazge, tada pasirinkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="acd6f-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![5 organizacijos struktūros diagramų vediklis](media/orgchart-wizard5.png)

11. <span data-ttu-id="acd6f-137">Įtraukite stulpelį **Pareigos** į sąrašą **Duomenų laukų formavimas**, tada pasirinkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="acd6f-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![6 organizacijos struktūros diagramų vediklis](media/orgchart-wizard6.png)

12. <span data-ttu-id="acd6f-139">Šiuo metu paveikslėlių nėra.</span><span class="sxs-lookup"><span data-stu-id="acd6f-139">Pictures aren't currently available.</span></span> <span data-ttu-id="acd6f-140">Todėl kitame puslapyje pasirinkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="acd6f-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="acd6f-141">Pasirinkite **Noriu, kad vediklis automatiškai visuose puslapiuose suskaidytų mano organizacijos diagramą**.</span><span class="sxs-lookup"><span data-stu-id="acd6f-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![7 organizacijos struktūros diagramų vediklis](media/orgchart-wizard4.png)

14. <span data-ttu-id="acd6f-143">Pasirinkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="acd6f-143">Select **Finish**.</span></span>

    <span data-ttu-id="acd6f-144">Jei yra pareigų, nesančių struktūroje, bus paprašyta įtraukti jas į diagramą.</span><span class="sxs-lookup"><span data-stu-id="acd6f-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="acd6f-145">„Visio“ sugeneruota diagrama kiekvieną vadybininką rodo atskirame darbalapyje.</span><span class="sxs-lookup"><span data-stu-id="acd6f-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="acd6f-146">Pagal laukus, kuriuos pasirinkote įtraukti į diagramą, sugeneravus „Visio“ failą, kiekvienas mazgas rodo atitinkamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="acd6f-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Hierarchijos diagrama](media/hierarchy.png)

<span data-ttu-id="acd6f-148">**Papildoma parinktis**</span><span class="sxs-lookup"><span data-stu-id="acd6f-148">**Additional option**</span></span>

<span data-ttu-id="acd6f-149">Programoje „Talent“ taip pat galėsite naudoti darbo sritį **Žmonės**, norėdami peržiūrėti tam tikrą su hierarchija susijusią informaciją.</span><span class="sxs-lookup"><span data-stu-id="acd6f-149">In Talent, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>
